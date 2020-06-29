---
title: Déplacement de composants MBAM2.0 vers un autre ordinateur
description: Déplacement de composants MBAM2.0 vers un autre ordinateur
author: dansimp
ms.assetid: 49bc0792-60a4-473f-89cc-ada30191e04a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 340d87e26d87f124a9ab64c63d33e89c293d8a86
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810938"
---
# Déplacement de composants MBAM2.0 vers un autre ordinateur


Cette rubrique décrit la procédure à suivre pour déplacer une ou plusieurs fonctionnalités d’administration et de surveillance de Microsoft BitLocker (MBAM) vers un autre ordinateur. Lorsque vous déplacez plusieurs fonctionnalités d’administration et de surveillance de BitLocker, vous devez les déplacer dans l’ordre suivant:

1.  Base de données de récupération

2.  Base de données d’audit et de conformité

3.  Rapports de conformité et d’audit

4.  Administration et surveillance

## Déplacement de la base de données de récupération


Pour déplacer la base de données de récupération d’un ordinateur à un autre (par exemple, du serveur A vers un serveur B), utilisez la procédure suivante.

1.  Arrêtez toutes les instances du site Web Administration et analyse.

2.  Exécutez le programme d’installation de MBAM sur le serveur B.

3.  Sauvegarder la base de données de récupération MBAM sur le serveur A.

4.  Déplacez la base de données de récupération MBAM du serveur A à B.

5.  Restaurez la base de données de récupération MBAM sur le serveur B.

6.  Configurer l’accès à la base de données de récupération MBAM sur le serveur B.

7.  Mettez à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM.

8.  Reprenez toutes les instances de MBAM site Web d’administration et de surveillance.

**Arrêter toutes les instances de MBAM site Web d’administration et de surveillance**

1.  Sur chacun des serveurs exécutant la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour arrêter le site Web MBAM, intitulé **administration et analyse de Microsoft BitLocker**.

2.  Pour automatiser cette procédure, vous pouvez utiliser la ligne de commande Windows PowerShell suivante:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Remarque**  
    Pour exécuter cette ligne de commande PowerShell, le module IIS pour PowerShell doit être ajouté à l’instance actuelle de PowerShell. Par ailleurs, vous devez mettre à jour la stratégie d’exécution PowerShell pour permettre l’exécution de scripts.



**Exécution de la configuration de MBAM sur le serveur B**

1.  Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez uniquement la **base de données de récupération** pour l’installation.

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer la ligne de commande semblable à ce qui suit:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ TOPOLOGY=$X$`

    **Remarque**  
    Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et de l’instance dans lesquels la base de données de récupération sera déplacée.

    -   $DOMAIN $ \ \ $SERVERNAME $-entrez les noms de domaine et de serveur de chaque serveur d’administration et de surveillance MBAM qui contactera la base de données de récupération. Utilisez un point-virgule pour séparer chaque paire de domaines et de serveurs dans la liste (par exemple, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $). Le nom de chaque serveur doit être suivi du symbole «$», comme le montre l’exemple (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).

    -   $X $-entrez **0** si vous installez la topologie autonome MBAM, ou **1** si vous installez la topologie MBAM Configuration Manager.



**Sauvegarder la base de données de récupération sur le serveur A**

1.  Pour sauvegarder la base de données de récupération sur le serveur A, utilisez SQL Server Management Studio et la tâche nommée sauvegarder. Par défaut, le nom de la base de données est **MBAM de récupération de la base de**données.

2.  Pour automatiser cette procédure, créez un fichier SQL (. Sql) contenant le script SQL suivant:

    Modifiez la base de données de récupération MBAM pour utiliser le mode de récupération complet.

    ```sql
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

       SET RECOVERY FULL;

    GO

    -- Create MBAM Recovery Database Data and MBAM Recovery logical backup devices.

    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery Database Data.bak';

    GO

    -- Back up the full MBAM Recovery Database.

    BACKUP DATABASE [MBAM Recovery and Hardware] TO [MBAM Recovery and Hardware Database Data Device];

    GO

    BACKUP CERTIFICATE [MBAM Recovery Encryption Certificate]

    TO FILE = 'Z:\SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

        FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

        ENCRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO
    ```

    **Remarque**  
    Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:

    -   $PASSWORD $-entrez le mot de passe que vous allez utiliser pour chiffrer le fichier de clé privée.



3.  Exécutez le fichier SQL en utilisant SQL Server PowerShell et une ligne de commande semblable à ce qui suit:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Remarque**  
    Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et de l’instance à partir desquels la base de données de récupération sera sauvegardée.



**Déplacer la base de données de récupération et le certificat du serveur A vers le serveur B**

1.  Déplacez le fichier suivant du serveur A vers le serveur B à l’aide de l’Explorateur Windows.

    -   Données de base de données de récupération de MBAM. bak

2.  Pour déplacer le certificat de la base de données chiffrée, utilisez les étapes d’Automation suivantes. Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:

    `PS C:\> Copy-Item “Z:\MBAM Recovery Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Remarque**  
    Remplacez la valeur suivante dans l’exemple ci-dessus par celles correspondant à votre environnement:

    -   $SERVERNAME $-entrez le nom du serveur sur lequel les fichiers sont copiés.

    -   $DESTINATIONSHARE $-entrez le nom du partage et du chemin d’accès dans lesquels les fichiers seront copiés.



**Restaurer la base de données de récupération sur le serveur B**

1.  Restaurez la base de données de récupération sur le serveur B en utilisant SQL Server Management Studio et la tâche nommée **restaurer la base de données**.

2.  Lorsque la tâche est achevée, sélectionnez le fichier de sauvegarde de la base de données en sélectionnant l’option **à partir de l’appareil** , puis utilisez la commande **Ajouter** pour sélectionner le fichier de données de la base de données de récupération MBAM. **bak** .

3.  Sélectionnez **OK** pour terminer le processus de restauration.

4.  Pour automatiser cette procédure, créez un fichier SQL (. Sql) qui contient le script SQL suivant:

    ```sql
    -- Restore MBAM Recovery Database. 

    USE master

    GO

    -- Drop certificate created by MBAM Setup.

    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO

    --Add certificate

    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z: \SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

        FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

        DECRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO

    -- Restore the MBAM Recovery Database data and log files.

    RESTORE DATABASE [MBAM Recovery and Hardware]

       FROM DISK = 'Z:\MBAM Recovery Database Data.bak'

       WITH REPLACE
    ```

    **Remarque**  
    Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:

    -   $PASSWORD $-entrez un mot de passe que vous avez utilisé pour chiffrer le fichier de clé privée.



5.  Vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Remarque**  
    Remplacez la valeur suivante dans l’exemple ci-dessus par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et de l’instance vers lesquels la base de données de récupération sera restaurée.



**Configurer l’accès à la base de données de récupération sur le serveur B**

1.  Sur le serveur B, utilisez le composant logiciel enfichable utilisateurs et groupes local dans le gestionnaire de serveur pour ajouter les comptes d’ordinateur de chaque serveur qui exécute la fonctionnalité d’administration et de surveillance MBAM au groupe local intitulé **MBAM de récupération et de BDD matériel**.

2.  Vérifiez que l’accès à la récupération de la base de données **MBAM et** de la base de données sur la base de données restaurée est mappé sur le nom de connexion **$MachineName \\MBAM de récupération et de**la base de données du matériel. Si ce n’est pas le cas, créez-en un autre avec des appartenances de groupe similaires, puis mappez-le au nom de connexion $MachineName l’accès à la **récupération \\MBAM et à la BD matérielle**.

3.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell sur le serveur B pour entrer une ligne de commande semblable à ce qui suit:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Remarque**  
    Remplacez les valeurs suivantes dans l’exemple ci-dessus avec les valeurs applicables pour votre environnement:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-entrez le domaine et le nom de l’ordinateur du serveur d’administration et de surveillance MBAM. Le nom du serveur doit être suivi d’un $, comme le montre l’exemple (par exemple, MyDomain\\MyServerName1 $).



~~~
This command line must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Mettre à jour les données de connexion de la base de données de récupération sur les serveurs d’administration et de surveillance MBAM**

1. Sur chacun des serveurs exécutant la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour les informations de la chaîne de connexion pour les applications suivantes, hébergées sur le site Web d’administration et de surveillance:

   -   MBAMAdministrationService

   -   MBAMRecoveryAndHardwareService

2. Sélectionner chaque application et utiliser la fonctionnalité **éditeur de configuration** , située sous la section **gestion** de l’affichage des **fonctionnalités**.

3. Sélectionnez l’option **configurationStrings** dans le contrôle de **liste de sections** .

4. Sélectionnez la ligne nommée **(collection)** , puis ouvrez l' **éditeur de collection** en sélectionnant le bouton à droite de la ligne.

5. Dans l' **éditeur de collection**, sélectionnez la ligne nommée **KeyRecoveryConnectionString** lors de la mise à jour de la configuration de l’application MBAMAdministrationService ou de la ligne nommée <strong> Microsoft. mbam. RecoveryAndHardwareDataStore. </strong> ConnectionString lors de la mise à jour de la configuration de MBAMRecoveryAndHardwareService.

6. Mettez à jour la **source de données =** valeur pour la propriété **configurationStrings** pour indiquer le nom du serveur et l’instance (par exemple, $SERVERNAME $ \ \ $SQLInstanceName $) où la base de données de récupération a été déplacée.

7. Pour automatiser cette procédure, vous pouvez utiliser Windows pour entrer une ligne de commande semblable à ce qui suit, sur chaque serveur d’administration et de surveillance:

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **Remarque**  
   Remplacez la valeur suivante dans l’exemple ci-dessus par celles correspondant à votre environnement:

   -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance de la base de données de récupération.



**Reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM**

1.  Sur chaque serveur exécutant la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web MBAM, intitulé **administration et analyse de Microsoft BitLocker**.

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Déplacement de la fonctionnalité de conformité et de base de données d’audit


Si vous voulez déplacer la base de données d’audit et de conformité MBAM d’un ordinateur à un autre (autrement dit, déplacez la base de données du serveur A vers le serveur B), utilisez la procédure suivante. Le processus comprend les principales étapes suivantes:

1.  Arrêtez toutes les instances du site Web d’administration et de surveillance.

2.  Exécutez le programme d’installation de MBAM sur le serveur B.

3.  Sauvegarder la base de données sur le serveur A.

4.  Déplacez la base de données du serveur A vers B.

5.  Restaurez la base de données sur le serveur B.

6.  Configurer l’accès à la base de données sur le serveur B.

7.  Mettez à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM.

8.  Mettez à jour la chaîne de connexion à la source de données des rapports SSRS avec le nouvel emplacement de la base de données d’audit et de conformité.

9.  Reprenez toutes les instances du site Web d’administration et de surveillance.

**Arrêter toutes les instances du site Web d’administration et de surveillance**

1.  Sur chaque serveur exécutant la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour arrêter d’arrêter le site Web MBAM appelé **administration et surveillance de Microsoft BitLocker**.

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:

    `PS C:\> Stop-s “Microsoft BitLocker Administration and Monitoring”`

    **Remarque**  
    Pour exécuter cette ligne de commande, vous devez ajouter le module IIS pour PowerShell à l’instance actuelle de PowerShell. Par ailleurs, vous devez mettre à jour la stratégie d’exécution PowerShell pour permettre l’exécution de scripts.



**Exécution de la configuration de MBAM sur le serveur B**

1.  Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez uniquement la **base de données d’audit et de conformité** pour l’installation.

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$ TOPOLOGY=$X$`

    **Remarque**  
    Remarque: remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance de destination de la base de données d’audit et de conformité.

    -   $DOMAIN $ \ \ $SERVERNAME $-entrez les noms de domaine et de serveur de chaque serveur d’administration et de surveillance MBAM qui contactera la base de données d’audit et de conformité. Utilisez un point-virgule pour séparer chaque paire de domaines et de serveurs dans la liste (par exemple, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $). Le nom de chaque serveur doit être suivi du symbole «$», comme le montre l’exemple (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).

    -   $DOMAIN $ \ \ $USERNAME $-entrez le domaine et le nom d’utilisateur qui seront utilisés par les rapports de conformité et d’audit pour vous connecter à la base de données d’audit et de conformité.

    -   $X $-entrez **0** si vous installez la topologie autonome MBAM, ou **1** si vous installez la topologie MBAM Configuration Manager.



**Sauvegarder la base de données de conformité et d’audit sur le serveur A**

1.  Pour sauvegarder la base de données de conformité et d’audit sur le serveur A, utilisez SQL Server Management Studio et la tâche nommée **sauvegarder**. Par défaut, le nom de la base de données est **MBAM de la base de données état de conformité**.

2.  Pour automatiser cette procédure, créez un fichier SQL (. Sql) qui contient le script SQL suivant:

    ```sql
    -- Modify the MBAM Compliance Status Database to use the full recovery model.

    USE master;

    GO

    ALTER DATABASE "MBAM Compliance Status"

       SET RECOVERY FULL;

    GO

    -- Create MBAM Compliance Status Data logical backup devices.

    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Compliance Status Database Data Device',

    'Z: \MBAM Compliance Status Database Data.bak';

    GO

    -- Back up the full MBAM Recovery database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO
    ```

3.  Exécutez le fichier SQL à l’aide d’une ligne de commande Windows PowerShell semblable à ce qui suit:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Remarque**  
    Remplacez la valeur suivante dans l’exemple ci-dessus par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance à partir desquels la base de données d’audit et de conformité sera sauvegardée.



**Déplacer la base de données d’audit et de conformité du serveur A à B**

1.  Déplacez les fichiers suivants du serveur A vers le serveur B à l’aide de l’Explorateur Windows.

    -   Données de la base de données d’état de conformité MBAM. bak

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Remarque**  
    Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:

    -   $SERVERNAME $-entrez le nom du serveur dans lequel les fichiers sont copiés.

    -   $DESTINATIONSHARE $-entrez le nom du partage dans lequel les fichiers sont copiés.



**Restaurer la base de données d’audit et de conformité sur le serveur B**

1.  Restaurez la base de données d’audit et de conformité sur le serveur B en utilisant SQL Server Management Studio et la tâche nommée **restaurer la base de données**.

2.  Une fois la tâche effectuée, sélectionnez le fichier de sauvegarde de la base de données en sélectionnant l’option **à partir de l’appareil** , puis utilisez la commande **Ajouter** pour sélectionner le fichier de données de la base de données d’état de conformité MBAM. bak. Sélectionnez **OK** pour terminer le processus de restauration.

3.  Pour automatiser cette procédure, créez un fichier SQL (. Sql) qui contient le script SQL suivant:

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  Exécutez le fichier SQL à l’aide d’une ligne de commande Windows PowerShell semblable à ce qui suit:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Remarque**  
    Remplacez la valeur suivante dans l’exemple ci-dessus par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance de destination de la base de données d’audit et de conformité.



**Configurer l’accès à la base de données de conformité et d’audit sur le serveur B**

1.  Sur le serveur B, utilisez le composant logiciel enfichable utilisateurs et groupes local dans le gestionnaire de serveur pour ajouter les comptes d’ordinateur de chaque serveur qui exécute la fonctionnalité d’administration et de surveillance MBAM au groupe local intitulé **MBAM accès**à la BD d’état de conformité.

2.  Vérifiez que l’accès aux bases de données **d’audit** de la conformité de la base de données MBAM sur la base de données restaurée est mappé sur le nom de connexion **$MachineName $ \ \ MBAM Compliance audit**. Si ce n’est pas le cas, créez-en un autre avec des appartenances de groupe similaires, puis mappez-le au nom de connexion **$MachineName $ \ \ MBAM Compliance audit Access**.

3.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande sur le serveur B qui est semblable à ce qui suit:

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Remarque**  
    Remplacez les valeurs suivantes dans l’exemple ci-dessus avec les valeurs applicables pour votre environnement:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-entrez le domaine et le nom de l’ordinateur du serveur d’administration et de surveillance MBAM. Le nom du serveur doit être suivi du «$» comme illustré dans l’exemple. (par exemple, MyDomain\\MyServerName1 $)

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-entrez le nom du compte d’utilisateur que vous avez utilisé pour configurer la source de données pour les rapports de conformité et d’audit.



~~~
The command line for adding the servers to the MBAM Compliance and Audit Database access local group must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Mettre à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM**

1.  Sur chaque serveur exécutant la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour les informations de la chaîne de connexion pour les applications suivantes qui sont hébergées sur le site Web d’administration et de surveillance:

    -   MBAMAdministrationService

    -   MBAMComplianceStatusService

2.  Sélectionner chaque application et utiliser la fonctionnalité **éditeur de configuration** , située sous la section **gestion** de l’affichage des **fonctionnalités**.

3.  Sélectionnez l’option **configurationStrings** dans le contrôle de **liste de sections** .

4.  Sélectionnez la ligne nommée **(collection)**, puis ouvrez l' **éditeur de collection** en sélectionnant le bouton à droite de la ligne.

5.  Dans l' **éditeur de collection**, sélectionnez la ligne nommée **ComplianceStatusConnectionString** lors de la mise à jour de la configuration de l’application MBAMAdministrationService ou de la ligne nommée **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString** lors de la mise à jour de la configuration pour le MBAMComplianceStatusService.

6.  Mettez à jour la **source de données =** valeur pour la propriété **configurationStrings** pour afficher le nom du serveur et de l’instance (par exemple, $SERVERNAME $ \ \ $SQLInstanceName) sur lequel la base de données de récupération a été déplacée.

7.  Pour automatiser cette procédure, vous pouvez utiliser Windows pour entrer une ligne de commande sur chaque serveur d’administration et de surveillance qui est semblable à ce qui suit:

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **Remarque**  
    Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance de la base de données de récupération.



**Reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM**

1.  Sur chaque serveur exécutant la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web MBAM appelé **administration et analyse de Microsoft BitLocker**.

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Déplacement des rapports de conformité et d’audit


Si vous voulez déplacer les rapports de conformité et d’audit MBAM d’un ordinateur à un autre (autrement dit, déplacez les rapports du serveur A vers le serveur B), utilisez la procédure suivante, qui inclut les étapes suivantes:

1.  Exécutez le programme d’installation de MBAM sur le serveur B.

2.  Configurer l’accès aux rapports de conformité et d’audit sur le serveur B.

3.  Arrêtez toutes les instances de l’MBAM site Web d’administration et de surveillance.

4.  Mettez à jour les données de connexion rapports sur les serveurs d’administration et de surveillance MBAM.

5.  Reprenez toutes les instances de MBAM site Web d’administration et de surveillance.

**Exécution de la configuration de MBAM sur le serveur B**

1.  Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez uniquement la fonctionnalité **rapports de conformité et d’audit** pour l’installation.

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$ TOPOLOGY=$X$`

    **Remarque**  
    Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance de la base de données d’audit et de conformité.

    -   $DOMAIN $ \ \ $USERNAME $-entrez le domaine et le nom d’utilisateur qui seront utilisés par les rapports de conformité et d’audit pour vous connecter à la base de données d’audit et de conformité.

    -   $PASSWORD $-entrez le mot de passe du compte d’utilisateur que vous utiliserez pour vous connecter à la base de données d’audit et de conformité.

    -   $X $-entrez **0** si vous installez la topologie autonome MBAM, ou **1** si vous installez la topologie MBAM Configuration Manager.



**Configurer l’accès aux rapports de conformité et d’audit sur le serveur B**

1.  Sur le serveur B, utilisez le composant logiciel enfichable utilisateurs et groupes local dans le gestionnaire de serveur pour ajouter les comptes d’utilisateurs qui auront accès aux rapports de conformité et d’audit. Ajoutez les comptes d’utilisateurs au groupe local intitulé utilisateurs de rapport MBAM.

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande sur le serveur B qui est semblable à ce qui suit:

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Remarque**  
    Remplacez les valeurs suivantes dans l’exemple ci-dessus avec les valeurs applicables pour votre environnement:

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-entrez le nom du compte d’utilisateur que vous avez utilisé pour configurer la source de données pour les rapports de conformité et d’audit.



~~~
The command line for adding the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**Arrêter toutes les instances de MBAM site Web d’administration et de surveillance**

1.  Sur chaque serveur exécutant la fonctionnalité de serveur d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour arrêter d’arrêter le site Web MBAM appelé **administration et analyse Microsoft BitLocker**.

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**Mettre à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM**

1. Sur chaque serveur exécutant la fonctionnalité de serveur d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour l’URL des rapports de conformité et d’audit.

2. Sélectionnez le site Web d' **administration et de contrôle Microsoft BitLocker** , puis utilisez la fonctionnalité **éditeur de configuration** qui est située sous la section **gestion** de l' **affichage des fonctionnalités**.

3. Sélectionnez l’option **appSettings** dans le contrôle de **liste de sections** .

4. Sélectionnez la ligne nommée **(collection)** , puis ouvrez l' **éditeur de collection** en sélectionnant le bouton à droite de la ligne.

5. Dans l' **éditeur de collection**, sélectionnez la ligne nommée **Microsoft. mbam. reports. URL**.

6. Mettez à jour la valeur pour **Microsoft. mbam. reports. URL** pour refléter le nom de serveur pour le serveur B. Si la fonctionnalité rapports de compatibilité et d’audit a été installée sur une instance nommée SQL Reporting Services, veillez à ajouter ou à mettre à jour le nom de l’instance à l’URL (par exemple, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/pages....).

7. Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande sur chaque serveur d’administration et de surveillance qui est semblable à ce qui suit:

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\ \sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/ Microsoft+BitLocker+Administration+and+Monitoring/”`

   **Remarque**  
   Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:

   -   $SERVERNAME $-entrez le nom du nom du serveur sur lequel sont installés les rapports de conformité et d’audit.

   -   $SRSINSTANCENAME $-entrez le nom de l’instance SQL Report services dans laquelle les rapports de conformité et d’audit ont été installés.



**Reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM**

1.  Sur chaque serveur exécutant la fonctionnalité de serveur d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web MBAM appelé **administration et analyse de Microsoft BitLocker**.

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **Remarque**  
    Pour exécuter cette ligne de commande, vous devez ajouter le module IIS pour PowerShell à l’instance actuelle de PowerShell. Par ailleurs, vous devez mettre à jour la stratégie d’exécution PowerShell pour permettre l’exécution de scripts.



## Déplacement de la fonctionnalité d’administration et de surveillance


Si vous voulez déplacer la fonctionnalité rapports d’administration et de surveillance de MBAM d’un ordinateur à un autre (autrement dit, déplacez la fonctionnalité du serveur A vers le serveur B), utilisez la procédure suivante, qui inclut les étapes de niveau supérieur suivantes:

1.  Exécutez le programme d’installation de MBAM sur le serveur B.

2.  Configurer l’accès à la base de données sur le serveur B.

**Exécution de la configuration de MBAM sur le serveur B**

1.  Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez uniquement la fonctionnalité d' **administration et de surveillance du serveur** pour l’installation.

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer, COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$ TOPOLOGY=$X$`

    **Remarque**  
    Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-pour le paramètre COMPLIDB \ _SQLINSTANCE, entrez le nom du serveur et l’instance de la base de données d’audit et de conformité. Pour le paramètre RECOVERYANDHWDB \ _SQLINSTANCE, entrez le nom du serveur et l’instance de la base de données de récupération.

    -   $DOMAIN $ \ \ $USERNAME $-entrez le domaine et le nom d’utilisateur qui seront utilisés par les rapports de conformité et d’audit pour vous connecter à la base de données d’audit et de conformité.

    -   $ REPORTSSERVERURL $-entrez l’URL de l’emplacement d’accueil du site Web de service de création de rapports SQL. Si les rapports étaient installés sur une instance de SRS par défaut, le format d’URL sera «http://$SERVERNAME $/ReportServer». Si les rapports étaient installés sur une instance de SRS par défaut, le format d’URL sera le http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $».

    -   $X $-entrez **0** si vous installez la topologie autonome MBAM, ou **1** si vous installez la topologie MBAM Configuration Manager.



**Configurer l’accès aux bases de données**

1.  Sur le ou les serveurs dans lesquels la base de données de récupération et la base de données d’audit sont déployées, utilisez le composant logiciel enfichable utilisateurs et groupes local dans le gestionnaire de serveur pour ajouter les comptes d’ordinateur de chaque serveur exécutant la fonctionnalité de serveur d' **administration et de** surveillance des MBAM de l’état de **conformité** du serveur.

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit, sur le serveur sur lequel la base de données d’audit et de conformité a été déployée.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

3.  Sur le serveur sur lequel la base de données de récupération a été déployée, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Remarque**  
    Remplacez la valeur suivante dans l’exemple ci-dessus avec les valeurs applicables pour votre environnement:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-entrez le domaine et le nom de l’ordinateur du serveur d’administration et de surveillance. Le nom du serveur doit être suivi du symbole «$», comme le montre l’exemple (par exemple, MyDomain\\MyServerName1 $).

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-entrez le nom du compte d’utilisateur que vous avez utilisé pour configurer la source de données pour les rapports de conformité et d’audit.



~~~
The command lines that are listed for adding server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## Rubriques connexes


[Gestion de MBAM2.0](maintaining-mbam-20-mbam-2.md)









