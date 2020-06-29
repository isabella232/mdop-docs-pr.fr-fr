---
title: Déplacement de bases de données MBAM2.5
description: Déplacement de bases de données MBAM2.5
author: dansimp
ms.assetid: 34b46f2d-0add-4377-8e4e-04b628fdfcf1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 63c509e7ae1460ece815ef6c0a22350f76b52018
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804200"
---
# Déplacement de bases de données MBAM2.5

Utilisez les procédures suivantes pour déplacer les bases de données suivantes d’un ordinateur vers un autre. du serveur A au serveur B, par exemple:

-   Base de données d’audit et de conformité

-   Base de données de récupération

>[!NOTE]
>Il est important que les bases de données soient restaurées sur l’ordinateur B avant d’exécuter l’Assistant Configuration MBAM pour les mettre à jour/les configurer.

S’il ne s’agit pas des bases de données, l’Assistant Configuration crée de nouvelles bases de données vides. Une fois vos bases de données existantes restaurées, ce processus rompt la configuration de MBAM.

Restaurez les bases de données d’abord, puis exécutez l’Assistant Configuration MBAM, choisissez l’option de base de données, et l’Assistant Configuration va «se connecter» aux bases de données que vous avez restaurées. les mises à niveau si nécessaire dans le cadre de la procédure.

**Si vous déplacez plusieurs fonctionnalités, déplacez-les dans l’ordre suivant:**

1.  Base de données de récupération

2.  Base de données d’audit et de conformité

3.  Rapports

4.  Site Web d’administration et de surveillance

5.  Portail libre-service

>[!Note]
>Pour exécuter l’exemple de scripts Windows PowerShell fourni dans cette rubrique, vous devez mettre à jour la stratégie d’exécution Windows PowerShell pour permettre l’exécution de scripts. Pour obtenir des instructions, voir [exécution de scripts Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) .

## Déplacer la base de données de récupération

Les étapes principales pour le déplacement de la base de données de récupération sont les suivantes:

1.  Arrêter toutes les instances de MBAM site Web d’administration et de surveillance

2.  Sauvegarder la base de données de récupération sur le serveur A

3.  Déplacer la base de données de récupération du serveur A vers le serveur B

4.  Restaurer la base de données de récupération sur le serveur B

5.  Configurer l’accès à la base de données sur le serveur B et mettre à jour les données de connexion

6.  Installez le logiciel serveur MBAM et exécutez l’Assistant Configuration de MBAM Server sur le serveur B

7.  Reprendre l’instance du site Web d’administration et de surveillance

### Comment déplacer la base de données de récupération

**Arrêtez toutes les instances de l’MBAM site Web d’administration et de surveillance.** Sur chaque serveur qui exécute le site Web du serveur d’administration et de surveillance MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour arrêter le site Web d’administration et de surveillance.

Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une commande semblable à ce qui suit:

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Pour exécuter cette commande, vous devez ajouter le module Internet Information Services (IIS) pour Windows PowerShell à l’instance actuelle de Windows PowerShell.

### Sauvegarder la base de données de récupération sur le serveur A

1.  Utilisez la tâche **sauvegarder** dans SQL Server Management Studio pour sauvegarder la base de données de récupération sur le serveur A.  Par défaut, le nom de la base de données est **MBAM de récupération de la base de**données.

2.  Pour automatiser cette procédure, créez un fichier SQL (. Sql) qui contient le script SQL suivant, puis modifiez la base de données de récupération MBAM pour utiliser le mode de récupération complet:

    ```
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

3.  Utilisez la valeur suivante pour remplacer les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement:

    **$Password $** -mot de passe que vous utilisez pour chiffrer le fichier de clé privée.

4.  Dans Windows PowerShell, exécutez le script qui est stocké dans le fichier et similaire à ce qui suit:

    ```powershell
    Invoke-Sqlcmd -InputFile
    'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
5.  Utilisez la valeur suivante pour remplacer les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement:

    **$ServerName $ \ $SQLInstanceName $** -nom du serveur et de l’instance à partir desquels la base de données de récupération sera sauvegardée.

### Déplacer la base de données de récupération du serveur A vers le serveur B

Utilisez l’Explorateur Windows pour déplacer le fichier **Data. bak de la base de données de récupération MBAM** du serveur A vers le serveur B.

Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour exécuter une commande similaire à ce qui suit:

```powershell
Copy-Item "Z:\MBAM Recovery Database Data.bak"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFile"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFilePrivateKey"
\\$SERVERNAME$\$DESTINATIONSHARE$
```
Utilisez les informations du tableau suivant pour remplacer les valeurs de l’exemple de code par des valeurs qui correspondent à votre environnement.

| **Paramètre**        | **Description**  |
|----------------------|------------------|
| $SERVERNAME $       | Nom du serveur sur lequel les fichiers sont copiés. |
| $DESTINATIONSHARE $ | Nom du partage et du chemin d’accès dans lesquels les fichiers seront copiés. |


### Restaurer la base de données de récupération sur le serveur B

1.  Restaurez la base de données de récupération sur le serveur B en utilisant la tâche **de restauration de base de données** dans SQL Server Management Studio.

2.  Lorsque la tâche précédente se termine, sélectionnez **à partir de l’appareil**, puis sélectionnez le fichier de sauvegarde de la base de données.

3.  Utilisez la commande **Ajouter** pour sélectionner le fichier **de données de la base de données de récupération MBAM** , puis cliquez sur **OK** pour terminer le processus de restauration.

4.  Pour automatiser cette procédure, créez un fichier SQL (. Sql) contenant le script SQL suivant:

    ```
    -- Restore MBAM Recovery Database.

    USE master

    GO

    -- Drop certificate created by MBAM Setup.

    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO

    --Add certificate

    CREATE CERTIFICATE [MBAM Recovery Encryption Certificate]

    FROM FILE = 'Z:\SQLServerInstanceCertificateFile'

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

5.  Utilisez la valeur suivante pour remplacer les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement.

    **$Password $** -mot de passe que vous avez utilisé pour chiffrer le fichier de clé privée.

6.  Dans Windows PowerShell, exécutez le script qui est stocké dans le fichier et similaire à ce qui suit:

    ```powershell
    Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
7.  Utilisez la valeur suivante pour remplacer les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement.

    **$ServerName $ \ $SQLInstanceName $** -nom du serveur et de l’instance dans lesquels la base de données de récupération sera restaurée.

### Configurer l’accès à la base de données sur le serveur B et mettre à jour les données de connexion

1. Vérifiez que la connexion utilisateur de Microsoft SQL Server permettant d’accéder à la base de données de récupération sur la base de données restaurée est mappée au compte d’accès que vous avez fourni lors du processus de configuration.

   >[!NOTE]
   >Si la connexion n’est pas la même, créez une connexion à l’aide de SQL Server Management Studio, puis mappez-la à l’utilisateur de la base de données existante.

2. Sur le serveur qui exécute le site Web d’administration et de surveillance, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour les informations de la chaîne de connexion pour les sites Web MBAM.

3. Modifiez la clé de Registre suivante:

   **HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString**

4. Mettez à jour la valeur de la **source de données** avec le nom du serveur et de l’instance (par exemple, \ $ServerName \ $ \ \ \ $SQLInstanceName) sur lequel la base de données de récupération a été déplacée.

5. Mettez à jour la valeur **initiale du catalogue** avec le nom de la base de données récupérée.

6. Pour automatiser ce processus, vous pouvez utiliser l’invite de commandes Windows PowerShell pour entrer une ligne de commande sur le serveur d’administration et de surveillance qui est semblable à ce qui suit:

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\\Microsoft\MBAM Server\\Web" /v
   RecoveryDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f

   Set-WebConfigurationProperty
   'connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath
   "IIS:\sites\Microsoft Bitlocker Administration and
   Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data
   Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and
   Hardware;Integrated Security=SSPI;"

   Set-WebConfigurationProperty
   'connectionStrings/add[\@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]'
   -PSPath "IIS:\sites\Microsoft Bitlocker Administration and
   Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value
   "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery
   and Hardware;Integrated Security=SSPI;"
   ```

   >[!Note]
   >Cette chaîne de connexion est partagée par toutes les applications Web MBAM locales. Par conséquent, il doit être mis à jour une seule fois par serveur.


7. Utilisez le tableau suivant pour remplacer les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement.

   |Paramètre|Description|
   |---------|-----------|
   |$SERVERNAME $/\ $SQLINSTANCENAME $|Nom du serveur et instance de SQL Server qui héberge la base de données de récupération.|
   |$DATABASE $|Nom de la base de données de récupération.|


### Installez le logiciel serveur MBAM et exécutez l’Assistant Configuration de MBAM Server sur le serveur B

1.  Installez le logiciel serveur MBAM 2,5 sur le serveur B. Pour plus d’informations, reportez-vous à [installation du logiciel serveur MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

2.  Sur le serveur B, démarrez l’Assistant Configuration de MBAM Server, cliquez sur **ajouter de nouvelles fonctionnalités**, puis sélectionnez uniquement la fonctionnalité **de base de données de récupération** . Pour plus d’informations sur la configuration des bases de données, voir [Comment configurer les bases de données 2,5 de MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

    >[!TIP]
    >Vous pouvez également utiliser l’applet de cmdlet Windows PowerShell **Enable-MbamDatabase** pour configurer la base de données de récupération.


### Reprendre l’instance du site Web d’administration et de surveillance

Sur le serveur qui exécute le site Web d’administration et de surveillance, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web d’administration et de surveillance.

Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour exécuter une commande similaire à ce qui suit:

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Pour exécuter cette commande, vous devez ajouter le module IIS pour Windows PowerShell à l’instance actuelle de Windows PowerShell.

## Déplacer la base de données d’audit et de conformité

Les étapes principales pour le déplacement de la base de données d’audit et de conformité sont les suivantes:

1.  Arrêter toutes les instances de MBAM site Web d’administration et de surveillance

2.  Sauvegarder la base de données de conformité et d’audit sur le serveur A

3.  Déplacer la base de données d’audit et de conformité du serveur A vers le serveur B

4.  Restaurer la base de données d’audit et de conformité sur le serveur B

5.  Configurer l’accès à la base de données sur le serveur B et mettre à jour les données de connexion

6.  Installez le logiciel serveur MBAM et exécutez l’Assistant Configuration de MBAM Server sur le serveur B

7.  Reprendre l’instance du site Web d’administration et de surveillance

### Comment déplacer la base de données d’audit et de conformité

**Arrêtez toutes les instances de l’MBAM site Web d’administration et de surveillance.**  Sur chaque serveur qui exécute le site Web du serveur d’administration et de surveillance MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour arrêter le site Web d’administration et de surveillance.

Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une commande semblable à ce qui suit:

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Pour exécuter cette commande, vous devez ajouter le module Internet Information Services (IIS) pour Windows PowerShell à l’instance actuelle de Windows PowerShell.

### Sauvegarder la base de données de conformité et d’audit sur le serveur A

1.  Utilisez la tâche **sauvegarder** dans SQL Server Management Studio pour sauvegarder la base de données d’audit et de conformité sur le serveur A. Par défaut, le nom de la base de données est **MBAM de la base de données état de conformité**.

2.  Pour automatiser cette procédure, créez un fichier SQL (. Sql) contenant le script SQL suivant:

    ```
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

    -- Back up the full MBAM Compliance Recovery database.

    BACKUP DATABASE [MBAM Compliance Status] TO [MBAM Compliance Status Database Data Device];

    GO

    ```

3.  Exécutez le script qui est stocké dans le fichier. SQL en utilisant une commande Windows PowerShell semblable à ce qui suit:

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance     $SERVERNAME$\$SQLINSTANCENAME$

    ```

4.  À l’aide de la valeur suivante, remplacez les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement:

    **$ServerName $ \ $SQLInstanceName $** -nom du serveur et instance à partir desquels la base de données d’audit et de conformité sera sauvegardée.

### Déplacez la base de données d’audit et de conformité du serveur A vers serveur B * *

1.  Dans l’Explorateur Windows, vous pouvez déplacer le fichier **Data. bak de la base de données de la base de données MBAM**

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour exécuter une commande similaire à ce qui suit:

    ```powershell
    Copy-Item "Z:\MBAM Compliance Status Database Data.bak"
    \\$SERVERNAME$\$DESTINATIONSHARE$
    ```

3.  À l’aide du tableau suivant, remplacez les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement.

    | **Paramètre**        | **Description**                                               |
    |----------------------|---------------------------------------------------------------|
    | $SERVERNAME $       | Nom du serveur sur lequel les fichiers sont copiés.         |
    | $DESTINATIONSHARE $ | Nom du partage et du chemin d’accès dans lesquels les fichiers seront copiés. |


### Restaurer la base de données d’audit et de conformité sur le serveur B

1.  Restaurez la base de données de conformité et d’audit sur le serveur B en utilisant la tâche **de restauration de base de données** dans SQL Server Management Studio.

2.  Lorsque la tâche précédente se termine, sélectionnez **à partir de l’appareil**, puis sélectionnez le fichier de sauvegarde de la base de données.

3.  Pour terminer le processus de restauration, **sélectionnez le fichier** **de données de la base de données d’état de conformité MBAM** , puis cliquez sur **OK** .

4.  Pour automatiser cette procédure, créez un fichier SQL (. Sql) contenant le script SQL suivant:

    ```
    -- Create MBAM Compliance Status Database Data logical backup devices.

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

    FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

    WITH REPLACE

    ```

5.  Dans Windows PowerShell, exécutez le script qui est stocké dans le fichier et similaire à ce qui suit:

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$

    ```

6.  À l’aide de la valeur suivante, remplacez les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement.

    **$ServerName $ \ $SQLInstanceName $** -nom du serveur et l’instance vers laquelle la base de données d’audit et de conformité sera restaurée.

### Configurer l’accès à la base de données sur le serveur B et mettre à jour les données de connexion

1. Vérifiez que la connexion utilisateur de Microsoft SQL Server qui autorise l’accès à la mise en conformité et audit de la base de données sur la base de données restaurée est mappée au compte d’accès que vous avez fourni lors du processus de configuration.

   >[!NOTE]
   >Si la connexion n’est pas la même, créez une connexion à l’aide de SQL Server Management Studio, puis mappez-la à l’utilisateur de la base de données existante.

2. Sur le serveur qui exécute le site Web d’administration et de surveillance, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour les informations de la chaîne de connexion pour le site Web.

3. Modifiez la clé de Registre suivante:

   **HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString**

4. Mettez à jour la valeur de la **source de données** avec le nom du serveur et de l’instance (par exemple, \ $ServerName \ $ \ \ \ $SQLInstanceName) sur lequel la base de données de récupération a été déplacée.

5. Mettez à jour la valeur **initiale du catalogue** avec le nom de la base de données récupérée.

6. Pour automatiser ce processus, vous pouvez utiliser l’invite de commandes Windows PowerShell pour entrer une ligne de commande sur le serveur d’administration et de surveillance qui est semblable à ce qui suit:

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web" /v
   ComplianceDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f
   ```
   >[!NOTE]
   >Cette chaîne de connexion est partagée par toutes les applications Web MBAM locales. Par conséquent, il doit être mis à jour une seule fois par serveur.


7. À l’aide du tableau suivant, remplacez les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement.

   |Paramètre | Description |
   |---------|------------|
   |$SERVERNAME $ \ $SQLINSTANCENAME $ | Nom du serveur et instance de SQL Server qui héberge la base de données de récupération.|
   |$DATABASE $|Nom de la base de données récupérée.|

### Installez le logiciel serveur MBAM et exécutez l’Assistant Configuration de MBAM Server sur le serveur B

1.  Installez le logiciel serveur MBAM 2,5 sur le serveur B. Pour plus d’informations, reportez-vous à [installation du logiciel serveur MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

2.  Sur le serveur B, démarrez l’Assistant Configuration de MBAM Server, cliquez sur **ajouter de nouvelles fonctionnalités**, puis sélectionnez uniquement la fonctionnalité **de conformité et d’audit** . Pour plus d’informations sur la configuration des bases de données, voir [Comment configurer les bases de données 2,5 de MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

    >[!TIP]
    >Vous pouvez également utiliser l’applet de contrôle Windows PowerShell **Enable-MbamDatabase** pour configurer la conformité et l’audit.


### Reprendre l’instance du site Web d’administration et de surveillance

Sur le serveur qui exécute le site Web d’administration et de surveillance, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web d’administration et de surveillance.

Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour exécuter une commande similaire à ce qui suit:

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
>Pour exécuter cette commande, vous devez ajouter le module IIS pour Windows PowerShell à l’instance actuelle de Windows PowerShell.
