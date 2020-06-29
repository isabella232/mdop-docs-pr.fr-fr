---
title: Déplacement de composants MBAM1.0 vers un autre ordinateur
description: Déplacement de composants MBAM1.0 vers un autre ordinateur
author: dansimp
ms.assetid: e1907d92-6b42-4ba3-b0e4-60a9cc8285cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 874c3983220f341e39fa5fb7c60f655e2f208082
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804609"
---
# Déplacement de composants MBAM1.0 vers un autre ordinateur


Cette rubrique décrit la procédure à suivre pour déplacer une ou plusieurs fonctionnalités d’administration et de surveillance de Microsoft BitLocker (MBAM) vers un autre ordinateur. Lorsque vous déplacez plusieurs fonctionnalités MBAM vers un autre ordinateur, vous devez les déplacer dans l’ordre suivant:

1.  Base de données de récupération et de matériel

2.  Base de données d’audit et de conformité

3.  Rapports de conformité et d’audit

4.  Administration et surveillance

## Pour déplacer la base de données de récupération et de matériel


Vous pouvez utiliser la procédure suivante pour déplacer la base de données de récupération MBAM et de base de données matérielle d’un ordinateur vers un autre (vous pouvez déplacer cette fonctionnalité MBAM Server du serveur A vers le serveur B):

****

1.  Arrêtez toutes les instances du site Web d’administration et de contrôle MBAM.

2.  Exécutez le programme d’installation de MBAM sur le serveur B.

3.  Sauvegarder la base de données de récupération MBAM et matérielle sur le serveur A.

4.  MBAM la base de données matérielle et de récupération du serveur A à B

5.  Restaurer la base de données matérielle et de récupération MBAM sur le serveur B

6.  Configurer l’accès à la MBAM de récupération et de la base de données matérielle du serveur B

7.  Mettre à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM

8.  Reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM

**Pour arrêter toutes les occurrences du site Web d’administration et de contrôle MBAM**

1.  Utilisez la console Gestionnaire des services Internet (IIS) pour arrêter le site Web MBAM sur chacun des serveurs exécutant la fonctionnalité d’administration et de surveillance d’MBAM. Le site Web MBAM est intitulé **administration et analyse Microsoft BitLocker**.

2.  Pour automatiser cette procédure, vous pouvez utiliser la commande suivante à l’invite de commandes, qui est semblable à ce qui suit, à l’aide de Windows PowerShell:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Remarque**  
    Pour exécuter l’invite de commandes PowerShell, vous devez ajouter le module IIS pour PowerShell à l’instance actuelle de PowerShell. Par ailleurs, vous devez mettre à jour la stratégie d’exécution PowerShell pour permettre l’exécution de scripts.



**Pour exécuter la configuration de MBAM sur le serveur B**

1.  Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez la base de données de récupération et de matériel pour l’installation.

2.  Pour automatiser cette procédure, vous pouvez utiliser la commande suivante à l’invite de commandes, qui est semblable à ce qui suit, à l’aide de Windows PowerShell:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$`

    **Remarque**  
    Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et de l’instance dans lesquels la base de données de récupération et de matériel seront déplacées.

    -   $DOMAIN $ \ \ $SERVERNAME $-entrez les noms de domaine et de serveur de chaque application MBAM et serveur de surveillance qui contactera la base de données de récupération et de matériel. S’il existe plusieurs noms de domaine et de serveur, séparez-les par un point-virgule. Par exemple, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $. Par ailleurs, chaque nom de serveur doit être suivi de a **$** . Par exemple, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.



**Pour sauvegarder la base de données sur le serveur A**

1.  Pour sauvegarder la base de données de récupération et de matériel du serveur A, utilisez SQL Server Management Studio et la tâche nommée **sauvegarder...**. Par défaut, le nom de la base de données est **MBAM récupération et la base de données matérielle**.

2.  Pour automatiser cette procédure, créez un fichier SQL (. Sql) contenant le script SQL suivant:

    Modifiez la base de données de récupération et de matériel MBAM pour utiliser le mode de récupération complet.

    ```sql
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

       SET RECOVERY FULL;

    GO
    ```

    Créez des MBAM de données de la base de données matérielle et de récupération des informations et MBAM de sauvegarde logique de restauration.

    ```sql
    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery and Hardware Database Data.bak';

    GO
    ```

    Sauvegardez l’intégralité de la base de données MBAM et de récupération du matériel.

    ```sql
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
    Remplacez les valeurs de l’exemple précédent par celles correspondant à votre environnement:

    -   $PASSWORD $-entrez le mot de passe que vous allez utiliser pour chiffrer le fichier de clé privée.



3.  Exécutez le fichier SQL en utilisant SQL Server PowerShell et une commande similaire à ce qui suit:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Remarque**  
    Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance à partir de laquelle vous sauvegardez la base de données de récupération et de matériel.



**Pour déplacer la base de données et le certificat du serveur A vers B**

1.  Déplacez les données de la base de données de récupération et de MBAM du matériel du serveur A vers le serveur B à l’aide de l’Explorateur Windows.

2.  Pour déplacer le certificat de la base de données chiffrée, vous devez utiliser les étapes d’Automation suivantes. Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une commande semblable à ce qui suit:

    `PS C:\> Copy-Item “Z:\MBAM Recovery and Hardware Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Remarque**  
    Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:

    -   $SERVERNAME $-entrez le nom du serveur sur lequel les fichiers sont copiés.

    -   $DESTINATIONSHARE $-entrez le nom du partage et du chemin d’accès dans lesquels les fichiers seront copiés.



**Pour restaurer la base de données sur le serveur B**

1.  Restaurez la base de données de récupération et de matériel sur le serveur B en utilisant SQL Server Management Studio et la tâche nommée **restaurer la base de données**.

2.  Après l’exécution de la tâche, sélectionnez le fichier de sauvegarde de la base de données en sélectionnant l’option **à partir de l’appareil** , puis utilisez la commande **Ajouter** pour choisir le fichier de données de la base de données MBAM et de la base de données du matériel **.**

3.  Sélectionnez **OK** pour terminer le processus de restauration.

4.  Pour automatiser cette procédure, créez un fichier SQL (. Sql) contenant le script SQL suivant:

    ```sql
    -- Restore MBAM Recovery and Hardware Database. 

    USE master

    GO
    ```

    Supprimez le certificat créé par MBAM Setup.

    ```sql
    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO
    ```

    Ajouter un certificat

    ```sql
    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z: \SQLServerInstanceCertificateFile'

    WITH PRIVATE KEY

    (

        FILE = ' Z:\SQLServerInstanceCertificateFilePrivateKey',

        DECRYPTION BY PASSWORD = '$PASSWORD$'

    );

    GO
    ```

    Restaurez les données de base de données matérielle et de récupération MBAM et les fichiers journaux.

    ```sql
    RESTORE DATABASE [MBAM Recovery and Hardware]

       FROM DISK = 'Z:\MBAM Recovery and Hardware Database Data.bak'

       WITH REPLACE
    ```

    **Remarque**  
    Remplacez les valeurs de l’exemple précédent par celles correspondant à votre environnement:

    -   $PASSWORD $-entrez le mot de passe que vous avez utilisé pour chiffrer le fichier de clé privée.



5.  Utilisez Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Remarque**  
    Remplacez la valeur de l’exemple de passe par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance vers laquelle la base de données de récupération et de matériel sera restaurée.



**Configurer l’accès à la base de données sur le serveur B**

1.  Sur le serveur B, utilisez le composant logiciel enfichable utilisateurs et groupes local dans le gestionnaire de serveur pour ajouter les comptes d’ordinateur de chaque serveur qui exécute la fonctionnalité d’administration et de surveillance MBAM au groupe local intitulé **MBAM de récupération et de BDD matériel**.

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell sur le serveur B pour entrer une commande semblable à ce qui suit:

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Remarque**  
    Remplacez les valeurs de l’exemple précédent par les valeurs applicables pour votre environnement:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-entrez le nom de domaine et le nom de l’ordinateur du serveur d’administration et de surveillance MBAM. Le nom du serveur doit être suivi d’un **$** (par exemple, MyDomain\\MyServerName1 $).



~~~
You must run the command for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**Pour mettre à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM**

1. Sur chacun des serveurs qui exécutent la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour les informations de la chaîne de connexion pour les applications suivantes qui sont hébergées dans le site Web d’administration et de contrôle de Microsoft BitLocker:

   -   Service d’administration MBAM

   -   Services de récupération et de matériel de MBAM

2. Sélectionner chaque application et utiliser la fonctionnalité **éditeur de configuration** , située sous la section **gestion** de l’affichage des **fonctionnalités**.

3. Sélectionnez l’option **configurationStrings** dans le contrôle de liste de sections.

4. Sélectionnez la ligne nommée **(collection)**, puis ouvrez l' **éditeur de collection** en sélectionnant le bouton à droite de la ligne.

5. Dans l' **éditeur de collection**, sélectionnez la ligne nommée **KeyRecoveryConnectionString** lorsque vous avez mis à jour la configuration de l’application «MBAMAdministrationService», ou sélectionnez la ligne nommée <strong> Microsoft. mbam. RecoveryAndHardwareDataStore. </strong> ChaîneConnexion, lors de la mise à jour de la configuration pour «MBAMRecoveryAndHardwareService».

6. Mettez à jour la **source de données =** valeur pour la propriété **configurationStrings** pour indiquer le nom du serveur et l’instance vers laquelle la base de données de récupération et de matériel a été déplacée. Par exemple, $SERVERNAME $ \ \ $SQLINSTANCENAME $.

7. Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, en utilisant Windows PowerShell sur chaque serveur d’administration et de surveillance:

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **Remarque**  
   Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:

   -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance de la base de données de récupération et de matériel.



**Pour reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM**

1.  Sur chacun des serveurs qui exécutent la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web MBAM, intitulé **administration et analyse de Microsoft BitLocker**.

2.  Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, à l’aide de Windows PowerShell:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## Pour déplacer la fonctionnalité de base de données état de conformité


Si vous choisissez de déplacer la fonctionnalité de base de données état de conformité d’MBAM d’un ordinateur vers un autre, par exemple du serveur A vers le serveur B, utilisez la procédure suivante:

1.  Arrêter toutes les instances de MBAM site Web d’administration et de surveillance

2.  Exécution de la configuration de MBAM sur le serveur B

3.  Sauvegarder la base de données sur le serveur A

4.  Déplacer la base de données du serveur A vers B

5.  Restaurer la base de données sur le serveur B

6.  Configurer l’accès à la base de données sur le serveur B

7.  Mettre à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM

8.  Reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM

**Pour arrêter toutes les occurrences du site Web d’administration et de contrôle MBAM**

1.  Sur chacun des serveurs qui exécutent la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour arrêter le site Web MBAM, intitulé **administration et analyse de Microsoft BitLocker**.

2.  Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, à l’aide de Windows PowerShell:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **Remarque**  
    Pour exécuter cette commande, vous devez ajouter le module IIS pour PowerShell à l’instance actuelle de PowerShell. Par ailleurs, vous devez mettre à jour la stratégie d’exécution PowerShell pour permettre l’exécution de scripts.



**Pour exécuter la configuration de MBAM sur le serveur B**

1.  Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez la fonctionnalité de base de données état de conformité pour l’installation.

2.  Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, à l’aide de Windows PowerShell:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$`

    **Remarque**  
    Remplacez les valeurs de l’exemple précédent par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance de destination de la base de données d’état de conformité.

    -   $DOMAIN $ \ \ $SERVERNAME $-entrez les noms de domaine et les noms de serveurs de chaque application MBAM et serveur de surveillance qui contactera la base de données d’état de conformité. S’il existe plusieurs noms de domaine et noms de serveurs, utilisez un point-virgule pour séparer chacun d’eux dans la liste. Par exemple, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $. Le nom de chaque serveur doit être suivi de a **$** comme illustré dans l’exemple. Par exemple, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.

    -   $DOMAIN $ \ \ $USERNAME $-entrez le domaine et le nom d’utilisateur qui seront utilisés par les rapports de conformité et d’audit pour vous connecter à la base de données état de conformité.



**Pour sauvegarder la base de données de conformité du serveur A**

1.  Pour sauvegarder la base de données de conformité du serveur A, utilisez SQL Server Management Studio et la tâche nommée **sauvegarder...**. Par défaut, le nom de la base de données est **MBAM de la base de données état de conformité**.

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

    -- Back up the full MBAM Recovery and Hardware database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO
    ```

3.  Exécutez le fichier SQL avec une commande similaire à celle qui suit, en utilisant SQL Server PowerShell:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Remarque**  
    Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance à partir de laquelle la base de données d’état de conformité sera sauvegardée.



**Pour déplacer la base de données du serveur A vers B**

1.  Dans l’Explorateur Windows, déplacez les fichiers suivants du serveur A vers le serveur B:

    -   Données de la base de données d’état de conformité MBAM. bak

2.  Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit dans Windows PowerShell:

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **Remarque**  
    Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:

    -   $SERVERNAME $-entrez le nom du serveur dans lequel les fichiers sont copiés.

    -   $DESTINATIONSHARE $-entrez le nom du partage dans lequel les fichiers sont copiés.



**Pour restaurer la base de données sur le serveur B**

1.  Restaurez la base de données d’état de conformité sur le serveur B en utilisant SQL Server Management Studio et la tâche nommée **restaurer la base de données...**.

2.  Après l’exécution de la tâche, sélectionnez le fichier de sauvegarde de la base de données en sélectionnant l’option à partir de l’appareil, puis utilisez la commande Ajouter pour choisir le fichier de données de la base de données d’état de compatibilité MBAM. bak. Cliquez sur OK pour terminer le processus de restauration.

3.  Pour automatiser cette procédure, créez un fichier SQL (. Sql) qui contient le script SQL suivant:

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status Database]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  Exécutez le fichier SQL avec une commande similaire à celle qui suit, en utilisant SQL Server PowerShell:

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **Remarque**  
    Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance où la base de données d’état de conformité sera restaurée.



**Pour configurer l’accès à la base de données sur le serveur B**

1.  Sur le serveur B, utilisez le composant logiciel enfichable utilisateurs et groupes local dans le gestionnaire de serveur pour ajouter les comptes d’ordinateur de chaque serveur qui exécute la fonctionnalité d’administration et de surveillance de MBAM dans le groupe local intitulé MBAM de la **BD état de conformité**.

2.  Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, en utilisant Windows PowerShell sur le serveur B:

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Remarque**  
    Remplacez la valeur de l’exemple précédent par les valeurs applicables pour votre environnement:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-entrez le domaine et le nom de l’ordinateur du serveur d’administration et de surveillance MBAM. Le nom du serveur doit être suivi de a **$** . Par exemple, MyDomain\\MyServerName1 $.

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-entrez le nom du compte d’utilisateur que vous avez utilisé pour configurer la source de données pour les rapports de conformité et d’audit



~~~
For each Administration and Monitoring Server that will access the database of your environment, you must run the command that will add the servers to the MBAM Compliance Auditing DB Access local group.
~~~

**Pour mettre à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM**

1.  Sur chacun des serveurs qui exécutent la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour les informations de la chaîne de connexion pour les applications suivantes qui sont hébergées dans le site Web d’administration et de contrôle de Microsoft BitLocker:

    -   MBAMAdministrationService

    -   MBAMComplianceStatusService

2.  Sélectionner chaque application et utiliser la fonctionnalité **éditeur de configuration** , située sous la section **gestion** de l’affichage des **fonctionnalités**.

3.  Sélectionnez l’option **configurationStrings** dans le contrôle de liste de sections.

4.  Sélectionnez la ligne nommée **(collection)**, puis ouvrez l’éditeur de collection en sélectionnant le bouton à droite de la ligne.

5.  Dans l' **éditeur de collection**, sélectionnez la ligne nommée **ComplianceStatusConnectionString**, lorsque vous mettez à jour la configuration de l’application MBAMAdministrationService, ou la ligne nommée **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString**, lorsque vous mettez à jour la configuration pour le MBAMComplianceStatusService.

6.  Mettez à jour la **source de données =** valeur pour la propriété **configurationStrings** pour afficher le nom du serveur et le nom de l’instance. Par exemple, $SERVERNAME $ \ \ $SQLINSTANCENAME, sur lequel la base de données de récupération et de matériel a été déplacée.

7.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une commande similaire à celle qui suit dans chaque serveur d’administration et de surveillance:

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **Remarque**  
    Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et le nom de l’instance où se trouve la base de données de récupération et de matériel.



**Pour reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM**

1.  Sur chacun des serveurs exécutant la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web MBAM appelé **administration et analyse Microsoft BitLocker**.

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une commande semblable à ce qui suit:

    **PS C:\\ &gt; Start-site Web «Administration et surveillance de Microsoft BitLocker»**

## Pour déplacer les rapports de conformité et d’audit


Si vous choisissez de déplacer les rapports de conformité et d’audit MBAM d’un ordinateur à un autre (en particulier, si vous déplacez la fonctionnalité du serveur A vers le serveur B), vous devez utiliser la procédure et les étapes suivantes:

1.  Exécution de la configuration de MBAM sur le serveur B

2.  Configurer l’accès aux rapports de conformité et d’audit sur le serveur B

3.  Arrêter toutes les instances de MBAM site Web d’administration et de surveillance

4.  Mettre à jour les données de connexion aux rapports sur les serveurs d’administration et de surveillance MBAM

5.  Reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM

**Pour exécuter la configuration de MBAM sur le serveur B**

1.  Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez uniquement la fonctionnalité conformité et audit pour l’installation.

2.  Pour automatiser cette procédure, vous pouvez utiliser une commande semblable à la suivante, à l’aide de Windows PowerShell:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$`

    **Remarque**  
    Remplacez les valeurs de l’exemple précédent par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance d’emplacement de la base de données d’état de conformité.

    -   $DOMAIN $ \ \ $USERNAME $-entrez le nom de domaine et le nom d’utilisateur qui seront utilisés par les rapports de conformité et d’audit pour vous connecter à la base de données d’état de conformité.

    -   $PASSWORD $-entrez le mot de passe du compte d’utilisateur que vous utiliserez pour vous connecter à la base de données d’état de conformité.



**Pour configurer l’accès aux rapports de conformité et d’audit sur le serveur B**

1.  Sur le serveur B, utilisez le composant logiciel enfichable utilisateurs et groupes local dans le gestionnaire de serveur pour ajouter les comptes d’utilisateurs qui auront accès aux rapports de conformité et d’audit. Ajoutez les comptes d’utilisateurs au groupe local intitulé «utilisateurs du rapport MBAM».

2.  Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à ce qui suit, en utilisant Windows PowerShell sur le serveur B.

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **Remarque**  
    Remplacez la valeur suivante de l’exemple précédent par les valeurs applicables pour votre environnement:

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-entrez le nom du compte d’utilisateur que vous avez utilisé pour configurer la source de données pour les rapports de conformité et d’audit



~~~
The command to add the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**Pour arrêter toutes les occurrences du site Web d’administration et de contrôle MBAM**

1.  Sur chacun des serveurs qui exécutent la fonctionnalité d’administration et de surveillance de MBAM, vous pouvez utiliser la console du gestionnaire des services Internet (IIS) pour arrêter le site Web MBAM appelé **administration et surveillance de Microsoft BitLocker**.

2.  Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, à l’aide de Windows PowerShell:

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**Pour mettre à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM**

1. Sur chacun des serveurs qui exécutent la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour l’URL des rapports de conformité.

2. Sélectionnez le site Web d' **administration et de contrôle Microsoft BitLocker** , puis utilisez la fonctionnalité **éditeur de configuration** qui se trouve dans la section **gestion** de l' **affichage des fonctionnalités**.

3. Sélectionnez l’option **appSettings** dans le contrôle de liste de sections.

4. À partir de là, sélectionnez la ligne nommée **(collection)**, puis ouvrez l' **éditeur de collection** en sélectionnant le bouton à droite de la ligne.

5. Dans l' **éditeur de collection**, sélectionnez la ligne nommée «Microsoft. mbam. reports. URL».

6. Mettez à jour la valeur pour Microsoft. mbam. reports. URL pour refléter le nom de serveur pour le serveur B. Si la fonctionnalité rapports de conformité et d’audit a été installée sur une instance nommée SQL Reporting Services, assurez-vous d’ajouter ou de mettre à jour le nom de l’instance à l’URL. Par exemple, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/pages....

7. Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une commande similaire à celle qui suit dans chaque serveur d’administration et de surveillance:

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/Malta+Compliance+Reports/”`

   **Remarque**  
   Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:

   -   $SERVERNAME $-entrez le nom du serveur sur lequel sont installés les rapports de conformité et d’audit.

   -   $SRSINSTANCENAME $-entrez le nom de l’instance SQL Report services dans laquelle les rapports de conformité et d’audit ont été installés.



**Pour reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM**

1.  Sur chacun des serveurs qui exécutent la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web MBAM appelé **administration et surveillance de Microsoft BitLocker**.

2.  Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, à l’aide de Windows PowerShell:

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **Remarque**  
    Pour exécuter cette commande, le module IIS pour PowerShell doit être ajouté à l’instance actuelle de PowerShell. Par ailleurs, vous devez mettre à jour la stratégie d’exécution PowerShell pour permettre l’exécution de scripts.



## Pour déplacer la fonctionnalité d’administration et de surveillance


Si vous choisissez de déplacer la fonctionnalité rapports d’administration et de surveillance de MBAM à partir d’un ordinateur vers un autre (si vous déplacez la fonctionnalité du serveur A vers le serveur B), vous devez utiliser la procédure suivante. Le processus comprend les étapes suivantes:

1.  Exécution de la configuration de MBAM sur le serveur B

2.  Configurer l’accès à la base de données sur le serveur B

**Pour exécuter la configuration de MBAM sur le serveur B**

1.  Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez uniquement la fonctionnalité d’administration pour l’installation.

2.  Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, à l’aide de Windows PowerShell:

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer,HardwareCompatibility COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$`

    **Remarque**  
    Remplacez les valeurs de l’exemple précédent par celles correspondant à votre environnement:

    -   $SERVERNAME $ \ \ $SQLINSTANCENAME $-pour le paramètre COMPLIDB \ _SQLINSTANCE, entrez le nom du serveur et l’instance où se trouve la base de données d’état de conformité. Pour le paramètre RECOVERYANDHWDB \ _SQLINSTANCE, entrez le nom du serveur et l’instance de la base de données de récupération et de matériel.

    -   $DOMAIN $ \ \ $USERNAME $-entrez le domaine et le nom d’utilisateur qui seront utilisés par les rapports de conformité et d’audit pour vous connecter à la base de données état de conformité.

    -   $ REPORTSSERVERURL $-entrez l’URL de l’emplacement d’accueil du site Web de service de création de rapports SQL. Si les rapports étaient installés sur une instance de SRS par défaut, le format d’URL sera formaté «http://$SERVERNAME $/ReportServer». Si les rapports étaient installés sur une instance de SRS par défaut, le format d’URL sera formaté en «http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $».



**Pour configurer l’accès aux bases de données**

1.  Sur un serveur ou un serveur sur lequel la récupération et le matériel sont les bases de données de conformité et d’audit sont déployées, utilisez le composant logiciel enfichable utilisateurs et groupes locaux dans le gestionnaire de serveur pour ajouter les comptes d’ordinateur de chaque serveur qui exécute la fonctionnalité d’administration et d’analyse du MBAM aux groupes locaux intitulés «MBAM de récupération et de la base de données d’audit de la base de données

2.  Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, en utilisant Windows PowerShell sur le serveur sur lequel les bases de données d’audit et de conformité ont été déployées.

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

3.  Sur le serveur sur lequel les bases de données de récupération et de matériel ont été déployées, exécutez une commande similaire à celle qui suit, à l’aide de Windows PowerShell.

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **Remarque**  
    Remplacez la valeur de l’exemple précédent par les valeurs applicables pour votre environnement:

    -   $DOMAIN $ \ \ $SERVERNAME $ $-entrez le domaine et le nom de l’ordinateur du serveur d’administration et de surveillance MBAM. Le nom du serveur doit être suivi de a **$** . Par exemple, MyDomain\\MyServerName1 $)

    -   $DOMAIN $ \ \ $REPORTSUSERNAME $-entrez le nom du compte d’utilisateur que vous avez utilisé pour configurer la source de données pour les rapports de conformité et d’audit.



~~~
The commands listed for adding the server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## Rubriques connexes


[Administration des composants de MBAM1.0](administering-mbam-10-features.md)









