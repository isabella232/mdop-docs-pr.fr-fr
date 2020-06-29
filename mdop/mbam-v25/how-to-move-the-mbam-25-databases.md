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
# <span data-ttu-id="0f048-103">Déplacement de bases de données MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="0f048-103">How to Move the MBAM 2.5 Databases</span></span>

<span data-ttu-id="0f048-104">Utilisez les procédures suivantes pour déplacer les bases de données suivantes d’un ordinateur vers un autre. du serveur A au serveur B, par exemple:</span><span class="sxs-lookup"><span data-stu-id="0f048-104">Use these procedures to move the following databases from one computer to another; from Server A to Server B, for example:</span></span>

-   <span data-ttu-id="0f048-105">Base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="0f048-105">Compliance and Audit Database</span></span>

-   <span data-ttu-id="0f048-106">Base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="0f048-106">Recovery Database</span></span>

>[!NOTE]
><span data-ttu-id="0f048-107">Il est important que les bases de données soient restaurées sur l’ordinateur B avant d’exécuter l’Assistant Configuration MBAM pour les mettre à jour/les configurer.</span><span class="sxs-lookup"><span data-stu-id="0f048-107">It is important that the databases be restored to Machine B PRIOR to running the MBAM Configuration Wizard to update/configure them.</span></span>

<span data-ttu-id="0f048-108">S’il ne s’agit pas des bases de données, l’Assistant Configuration crée de nouvelles bases de données vides.</span><span class="sxs-lookup"><span data-stu-id="0f048-108">If the databases are NOT present, the Configuration Wizard creates NEW, empty, databases.</span></span> <span data-ttu-id="0f048-109">Une fois vos bases de données existantes restaurées, ce processus rompt la configuration de MBAM.</span><span class="sxs-lookup"><span data-stu-id="0f048-109">When your existing databases are then restored, this process will break the MBAM configuration.</span></span>

<span data-ttu-id="0f048-110">Restaurez les bases de données d’abord, puis exécutez l’Assistant Configuration MBAM, choisissez l’option de base de données, et l’Assistant Configuration va «se connecter» aux bases de données que vous avez restaurées. les mises à niveau si nécessaire dans le cadre de la procédure.</span><span class="sxs-lookup"><span data-stu-id="0f048-110">Restore the databases FIRST, then run the MBAM Configuration Wizard, choose the database option, and the Configuration Wizard will “connect” to the databases you restored; upgrading them if needed as part of the process.</span></span>

**<span data-ttu-id="0f048-111">Si vous déplacez plusieurs fonctionnalités, déplacez-les dans l’ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="0f048-111">If you are moving multiple features, move them in the following order:</span></span>**

1.  <span data-ttu-id="0f048-112">Base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="0f048-112">Recovery Database</span></span>

2.  <span data-ttu-id="0f048-113">Base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="0f048-113">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="0f048-114">Rapports</span><span class="sxs-lookup"><span data-stu-id="0f048-114">Reports</span></span>

4.  <span data-ttu-id="0f048-115">Site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="0f048-115">Administration and Monitoring Website</span></span>

5.  <span data-ttu-id="0f048-116">Portail libre-service</span><span class="sxs-lookup"><span data-stu-id="0f048-116">Self-Service Portal</span></span>

>[!Note]
><span data-ttu-id="0f048-117">Pour exécuter l’exemple de scripts Windows PowerShell fourni dans cette rubrique, vous devez mettre à jour la stratégie d’exécution Windows PowerShell pour permettre l’exécution de scripts.</span><span class="sxs-lookup"><span data-stu-id="0f048-117">To run the example Windows PowerShell scripts provided in this topic, you must update the Windows PowerShell execution policy to enable scripts to be run.</span></span> <span data-ttu-id="0f048-118">Pour obtenir des instructions, voir [exécution de scripts Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0f048-118">See [Running Windows PowerShell Scripts](https://technet.microsoft.com/library/ee176949.aspx) for instructions.</span></span>

## <span data-ttu-id="0f048-119">Déplacer la base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="0f048-119">Move the Recovery Database</span></span>

<span data-ttu-id="0f048-120">Les étapes principales pour le déplacement de la base de données de récupération sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="0f048-120">The high-level steps for moving the Recovery Database are:</span></span>

1.  <span data-ttu-id="0f048-121">Arrêter toutes les instances de MBAM site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="0f048-121">Stop all instances of the MBAM Administration and Monitoring Website</span></span>

2.  <span data-ttu-id="0f048-122">Sauvegarder la base de données de récupération sur le serveur A</span><span class="sxs-lookup"><span data-stu-id="0f048-122">Back up the Recovery Database on Server A</span></span>

3.  <span data-ttu-id="0f048-123">Déplacer la base de données de récupération du serveur A vers le serveur B</span><span class="sxs-lookup"><span data-stu-id="0f048-123">Move the Recovery Database from Server A to Server B</span></span>

4.  <span data-ttu-id="0f048-124">Restaurer la base de données de récupération sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="0f048-124">Restore the Recovery Database on Server B</span></span>

5.  <span data-ttu-id="0f048-125">Configurer l’accès à la base de données sur le serveur B et mettre à jour les données de connexion</span><span class="sxs-lookup"><span data-stu-id="0f048-125">Configure access to the Database on Server B and update connection data</span></span>

6.  <span data-ttu-id="0f048-126">Installez le logiciel serveur MBAM et exécutez l’Assistant Configuration de MBAM Server sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="0f048-126">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

7.  <span data-ttu-id="0f048-127">Reprendre l’instance du site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="0f048-127">Resume the instance of the Administration and Monitoring Website</span></span>

### <span data-ttu-id="0f048-128">Comment déplacer la base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="0f048-128">How to move the Recovery Database</span></span>

**<span data-ttu-id="0f048-129">Arrêtez toutes les instances de l’MBAM site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="0f048-129">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>** <span data-ttu-id="0f048-130">Sur chaque serveur qui exécute le site Web du serveur d’administration et de surveillance MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour arrêter le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="0f048-130">On each server that is running the MBAM Administration and Monitoring Server Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

<span data-ttu-id="0f048-131">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="0f048-131">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="0f048-132">Pour exécuter cette commande, vous devez ajouter le module Internet Information Services (IIS) pour Windows PowerShell à l’instance actuelle de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0f048-132">To run this command, you must add the Internet Information Services (IIS) module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

### <span data-ttu-id="0f048-133">Sauvegarder la base de données de récupération sur le serveur A</span><span class="sxs-lookup"><span data-stu-id="0f048-133">Back up the Recovery Database on Server A</span></span>

1.  <span data-ttu-id="0f048-134">Utilisez la tâche **sauvegarder** dans SQL Server Management Studio pour sauvegarder la base de données de récupération sur le serveur A.  Par défaut, le nom de la base de données est **MBAM de récupération de la base de**données.</span><span class="sxs-lookup"><span data-stu-id="0f048-134">Use the **Back Up** task in SQL Server Management Studio to back up the Recovery Database on Server A.  By default, the database name is **MBAM Recovery Database**.</span></span>

2.  <span data-ttu-id="0f048-135">Pour automatiser cette procédure, créez un fichier SQL (. Sql) qui contient le script SQL suivant, puis modifiez la base de données de récupération MBAM pour utiliser le mode de récupération complet:</span><span class="sxs-lookup"><span data-stu-id="0f048-135">To automate this procedure, create a SQL file (.sql) that contains the following SQL script, and change the MBAM Recovery Database to use the full recovery mode:</span></span>

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

3.  <span data-ttu-id="0f048-136">Utilisez la valeur suivante pour remplacer les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="0f048-136">Use the following value to replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="0f048-137">**$Password $** -mot de passe que vous utilisez pour chiffrer le fichier de clé privée.</span><span class="sxs-lookup"><span data-stu-id="0f048-137">**$PASSWORD$** - password that you use to encrypt the Private Key file.</span></span>

4.  <span data-ttu-id="0f048-138">Dans Windows PowerShell, exécutez le script qui est stocké dans le fichier et similaire à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="0f048-138">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile
    'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
5.  <span data-ttu-id="0f048-139">Utilisez la valeur suivante pour remplacer les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="0f048-139">Use the following value to replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="0f048-140">**$ServerName $ \ $SQLInstanceName $** -nom du serveur et de l’instance à partir desquels la base de données de récupération sera sauvegardée.</span><span class="sxs-lookup"><span data-stu-id="0f048-140">**$SERVERNAME$\$SQLINSTANCENAME$** - server name and instance from which the Recovery Database will be backed up.</span></span>

### <span data-ttu-id="0f048-141">Déplacer la base de données de récupération du serveur A vers le serveur B</span><span class="sxs-lookup"><span data-stu-id="0f048-141">Move the Recovery Database from Server A to Server B</span></span>

<span data-ttu-id="0f048-142">Utilisez l’Explorateur Windows pour déplacer le fichier **Data. bak de la base de données de récupération MBAM** du serveur A vers le serveur B.</span><span class="sxs-lookup"><span data-stu-id="0f048-142">Use Windows Explorer to move the **MBAM Recovery Database Data.bak** file from Server A to Server B.</span></span>

<span data-ttu-id="0f048-143">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour exécuter une commande similaire à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="0f048-143">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Copy-Item "Z:\MBAM Recovery Database Data.bak"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFile"
\\$SERVERNAME$\$DESTINATIONSHARE$

Copy-Item "Z:\SQLServerInstanceCertificateFilePrivateKey"
\\$SERVERNAME$\$DESTINATIONSHARE$
```
<span data-ttu-id="0f048-144">Utilisez les informations du tableau suivant pour remplacer les valeurs de l’exemple de code par des valeurs qui correspondent à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="0f048-144">Use the information in the following table to replace the values in the code example with values that match your environment.</span></span>

| **<span data-ttu-id="0f048-145">Paramètre</span><span class="sxs-lookup"><span data-stu-id="0f048-145">Parameter</span></span>**        | **<span data-ttu-id="0f048-146">Description</span><span class="sxs-lookup"><span data-stu-id="0f048-146">Description</span></span>**  |
|----------------------|------------------|
| <span data-ttu-id="0f048-147">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="0f048-147">$SERVERNAME$</span></span>       | <span data-ttu-id="0f048-148">Nom du serveur sur lequel les fichiers sont copiés.</span><span class="sxs-lookup"><span data-stu-id="0f048-148">Name of the server to which the files will be copied.</span></span> |
| <span data-ttu-id="0f048-149">$DESTINATIONSHARE $</span><span class="sxs-lookup"><span data-stu-id="0f048-149">$DESTINATIONSHARE$</span></span> | <span data-ttu-id="0f048-150">Nom du partage et du chemin d’accès dans lesquels les fichiers seront copiés.</span><span class="sxs-lookup"><span data-stu-id="0f048-150">Name of the share and path to which the files will be copied.</span></span> |


### <span data-ttu-id="0f048-151">Restaurer la base de données de récupération sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="0f048-151">Restore the Recovery Database on Server B</span></span>

1.  <span data-ttu-id="0f048-152">Restaurez la base de données de récupération sur le serveur B en utilisant la tâche **de restauration de base de données** dans SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="0f048-152">Restore the Recovery Database on Server B by using the **Restore Database** task in SQL Server Management Studio.</span></span>

2.  <span data-ttu-id="0f048-153">Lorsque la tâche précédente se termine, sélectionnez **à partir de l’appareil**, puis sélectionnez le fichier de sauvegarde de la base de données.</span><span class="sxs-lookup"><span data-stu-id="0f048-153">When the previous task finishes, select **From Device**, and then select the database backup file.</span></span>

3.  <span data-ttu-id="0f048-154">Utilisez la commande **Ajouter** pour sélectionner le fichier **de données de la base de données de récupération MBAM** , puis cliquez sur **OK** pour terminer le processus de restauration.</span><span class="sxs-lookup"><span data-stu-id="0f048-154">Use the **Add** command to select the **MBAM Recovery Database Data.bak** file, and click **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="0f048-155">Pour automatiser cette procédure, créez un fichier SQL (. Sql) contenant le script SQL suivant:</span><span class="sxs-lookup"><span data-stu-id="0f048-155">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

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

5.  <span data-ttu-id="0f048-156">Utilisez la valeur suivante pour remplacer les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="0f048-156">Use the following value to replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="0f048-157">**$Password $** -mot de passe que vous avez utilisé pour chiffrer le fichier de clé privée.</span><span class="sxs-lookup"><span data-stu-id="0f048-157">**$PASSWORD$** - password that you used to encrypt the Private Key file.</span></span>

6.  <span data-ttu-id="0f048-158">Dans Windows PowerShell, exécutez le script qui est stocké dans le fichier et similaire à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="0f048-158">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$
    ```
7.  <span data-ttu-id="0f048-159">Utilisez la valeur suivante pour remplacer les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="0f048-159">Use the following value to replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="0f048-160">**$ServerName $ \ $SQLInstanceName $** -nom du serveur et de l’instance dans lesquels la base de données de récupération sera restaurée.</span><span class="sxs-lookup"><span data-stu-id="0f048-160">**$SERVERNAME$\$SQLINSTANCENAME$** - Server name and instance to which the Recovery Database will be restored.</span></span>

### <span data-ttu-id="0f048-161">Configurer l’accès à la base de données sur le serveur B et mettre à jour les données de connexion</span><span class="sxs-lookup"><span data-stu-id="0f048-161">Configure access to the Database on Server B and update connection data</span></span>

1. <span data-ttu-id="0f048-162">Vérifiez que la connexion utilisateur de Microsoft SQL Server permettant d’accéder à la base de données de récupération sur la base de données restaurée est mappée au compte d’accès que vous avez fourni lors du processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="0f048-162">Verify that the Microsoft SQL Server user login that enables Recovery Database access on the restored database is mapped to the access account that you provided during the configuration process.</span></span>

   >[!NOTE]
   ><span data-ttu-id="0f048-163">Si la connexion n’est pas la même, créez une connexion à l’aide de SQL Server Management Studio, puis mappez-la à l’utilisateur de la base de données existante.</span><span class="sxs-lookup"><span data-stu-id="0f048-163">If the login is not the same, create a login by using SQL Server Management Studio, and map it to the existing database user.</span></span>

2. <span data-ttu-id="0f048-164">Sur le serveur qui exécute le site Web d’administration et de surveillance, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour les informations de la chaîne de connexion pour les sites Web MBAM.</span><span class="sxs-lookup"><span data-stu-id="0f048-164">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to update the connection string information for the MBAM websites.</span></span>

3. <span data-ttu-id="0f048-165">Modifiez la clé de Registre suivante:</span><span class="sxs-lookup"><span data-stu-id="0f048-165">Edit the following registry key:</span></span>

   **<span data-ttu-id="0f048-166">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString</span><span class="sxs-lookup"><span data-stu-id="0f048-166">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\RecoveryDBConnectionString</span></span>**

4. <span data-ttu-id="0f048-167">Mettez à jour la valeur de la **source de données** avec le nom du serveur et de l’instance (par exemple, \ $ServerName \ $ \ \ \ $SQLInstanceName) sur lequel la base de données de récupération a été déplacée.</span><span class="sxs-lookup"><span data-stu-id="0f048-167">Update the **Data Source** value with the name of the server and instance (for example, \$SERVERNAME\$\\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

5. <span data-ttu-id="0f048-168">Mettez à jour la valeur **initiale du catalogue** avec le nom de la base de données récupérée.</span><span class="sxs-lookup"><span data-stu-id="0f048-168">Update the **Initial Catalog** value with the recovered database name.</span></span>

6. <span data-ttu-id="0f048-169">Pour automatiser ce processus, vous pouvez utiliser l’invite de commandes Windows PowerShell pour entrer une ligne de commande sur le serveur d’administration et de surveillance qui est semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="0f048-169">To automate this process, you can use the Windows PowerShell command prompt to enter a command line on the Administration and Monitoring Server that is similar to the following:</span></span>

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
   ><span data-ttu-id="0f048-170">Cette chaîne de connexion est partagée par toutes les applications Web MBAM locales.</span><span class="sxs-lookup"><span data-stu-id="0f048-170">This connection string is shared by all local MBAM web applications.</span></span> <span data-ttu-id="0f048-171">Par conséquent, il doit être mis à jour une seule fois par serveur.</span><span class="sxs-lookup"><span data-stu-id="0f048-171">Therefore, it needs to be updated only once per server.</span></span>


7. <span data-ttu-id="0f048-172">Utilisez le tableau suivant pour remplacer les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="0f048-172">Use the following table to replace the values in the code example with values that match your environment.</span></span>

   |<span data-ttu-id="0f048-173">Paramètre</span><span class="sxs-lookup"><span data-stu-id="0f048-173">Parameter</span></span>|<span data-ttu-id="0f048-174">Description</span><span class="sxs-lookup"><span data-stu-id="0f048-174">Description</span></span>|
   |---------|-----------|
   |<span data-ttu-id="0f048-175">$SERVERNAME $/\ $SQLINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="0f048-175">$SERVERNAME$/\$SQLINSTANCENAME$</span></span>|<span data-ttu-id="0f048-176">Nom du serveur et instance de SQL Server qui héberge la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="0f048-176">Server name and instance of SQL Server where the Recovery Database is located.</span></span>|
   |<span data-ttu-id="0f048-177">$DATABASE $</span><span class="sxs-lookup"><span data-stu-id="0f048-177">$DATABASE$</span></span>|<span data-ttu-id="0f048-178">Nom de la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="0f048-178">Name of the Recovery database.</span></span>|


### <span data-ttu-id="0f048-179">Installez le logiciel serveur MBAM et exécutez l’Assistant Configuration de MBAM Server sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="0f048-179">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

1.  <span data-ttu-id="0f048-180">Installez le logiciel serveur MBAM 2,5 sur le serveur B. Pour plus d’informations, reportez-vous à [installation du logiciel serveur MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span><span class="sxs-lookup"><span data-stu-id="0f048-180">Install the MBAM 2.5 Server software on Server B. For details, see [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span></span>

2.  <span data-ttu-id="0f048-181">Sur le serveur B, démarrez l’Assistant Configuration de MBAM Server, cliquez sur **ajouter de nouvelles fonctionnalités**, puis sélectionnez uniquement la fonctionnalité **de base de données de récupération** .</span><span class="sxs-lookup"><span data-stu-id="0f048-181">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Recovery Database** feature.</span></span> <span data-ttu-id="0f048-182">Pour plus d’informations sur la configuration des bases de données, voir [Comment configurer les bases de données 2,5 de MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span><span class="sxs-lookup"><span data-stu-id="0f048-182">For details on how to configure the databases, see [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span></span>

    >[!TIP]
    ><span data-ttu-id="0f048-183">Vous pouvez également utiliser l’applet de cmdlet Windows PowerShell **Enable-MbamDatabase** pour configurer la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="0f048-183">Alternatively, you can use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the Recovery Database.</span></span>


### <span data-ttu-id="0f048-184">Reprendre l’instance du site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="0f048-184">Resume the instance of the Administration and Monitoring Website</span></span>

<span data-ttu-id="0f048-185">Sur le serveur qui exécute le site Web d’administration et de surveillance, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="0f048-185">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

<span data-ttu-id="0f048-186">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour exécuter une commande similaire à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="0f048-186">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="0f048-187">Pour exécuter cette commande, vous devez ajouter le module IIS pour Windows PowerShell à l’instance actuelle de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0f048-187">To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

## <span data-ttu-id="0f048-188">Déplacer la base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="0f048-188">Move the Compliance and Audit Database</span></span>

<span data-ttu-id="0f048-189">Les étapes principales pour le déplacement de la base de données d’audit et de conformité sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="0f048-189">The high-level steps for moving the Compliance and Audit Database are:</span></span>

1.  <span data-ttu-id="0f048-190">Arrêter toutes les instances de MBAM site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="0f048-190">Stop all instances of the MBAM Administration and Monitoring Website</span></span>

2.  <span data-ttu-id="0f048-191">Sauvegarder la base de données de conformité et d’audit sur le serveur A</span><span class="sxs-lookup"><span data-stu-id="0f048-191">Back up the Compliance and Audit Database on Server A</span></span>

3.  <span data-ttu-id="0f048-192">Déplacer la base de données d’audit et de conformité du serveur A vers le serveur B</span><span class="sxs-lookup"><span data-stu-id="0f048-192">Move the Compliance and Audit Database from Server A to Server B</span></span>

4.  <span data-ttu-id="0f048-193">Restaurer la base de données d’audit et de conformité sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="0f048-193">Restore the Compliance and Audit Database on Server B</span></span>

5.  <span data-ttu-id="0f048-194">Configurer l’accès à la base de données sur le serveur B et mettre à jour les données de connexion</span><span class="sxs-lookup"><span data-stu-id="0f048-194">Configure access to the Database on Server B and update connection data</span></span>

6.  <span data-ttu-id="0f048-195">Installez le logiciel serveur MBAM et exécutez l’Assistant Configuration de MBAM Server sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="0f048-195">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

7.  <span data-ttu-id="0f048-196">Reprendre l’instance du site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="0f048-196">Resume the instance of the Administration and Monitoring Website</span></span>

### <span data-ttu-id="0f048-197">Comment déplacer la base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="0f048-197">How to move the Compliance and Audit Database</span></span>

**<span data-ttu-id="0f048-198">Arrêtez toutes les instances de l’MBAM site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="0f048-198">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>**  <span data-ttu-id="0f048-199">Sur chaque serveur qui exécute le site Web du serveur d’administration et de surveillance MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour arrêter le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="0f048-199">On each server that is running the MBAM Administration and Monitoring Server Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

<span data-ttu-id="0f048-200">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="0f048-200">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

```powershell
Stop-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="0f048-201">Pour exécuter cette commande, vous devez ajouter le module Internet Information Services (IIS) pour Windows PowerShell à l’instance actuelle de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0f048-201">To run this command, you must add the Internet Information Services (IIS) module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

### <span data-ttu-id="0f048-202">Sauvegarder la base de données de conformité et d’audit sur le serveur A</span><span class="sxs-lookup"><span data-stu-id="0f048-202">Back up the Compliance and Audit Database on Server A</span></span>

1.  <span data-ttu-id="0f048-203">Utilisez la tâche **sauvegarder** dans SQL Server Management Studio pour sauvegarder la base de données d’audit et de conformité sur le serveur A. Par défaut, le nom de la base de données est **MBAM de la base de données état de conformité**.</span><span class="sxs-lookup"><span data-stu-id="0f048-203">Use the **Back Up** task in SQL Server Management Studio to back up the Compliance and Audit Database on Server A. By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="0f048-204">Pour automatiser cette procédure, créez un fichier SQL (. Sql) contenant le script SQL suivant:</span><span class="sxs-lookup"><span data-stu-id="0f048-204">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

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

3.  <span data-ttu-id="0f048-205">Exécutez le script qui est stocké dans le fichier. SQL en utilisant une commande Windows PowerShell semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="0f048-205">Run the script that is stored in the .sql file by using a Windows PowerShell command that is similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance     $SERVERNAME$\$SQLINSTANCENAME$

    ```

4.  <span data-ttu-id="0f048-206">À l’aide de la valeur suivante, remplacez les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="0f048-206">Using the following value, replace the values in the code example with values that match your environment:</span></span>

    <span data-ttu-id="0f048-207">**$ServerName $ \ $SQLInstanceName $** -nom du serveur et instance à partir desquels la base de données d’audit et de conformité sera sauvegardée.</span><span class="sxs-lookup"><span data-stu-id="0f048-207">**$SERVERNAME$\$SQLINSTANCENAME$** - server name and instance from which the Compliance and Audit Database will be backed up.</span></span>

### <span data-ttu-id="0f048-208">Déplacez la base de données d’audit et de conformité du serveur A vers serveur B \* \*</span><span class="sxs-lookup"><span data-stu-id="0f048-208">Move the Compliance and Audit Database from Server A to Server B\*\*</span></span>

1.  <span data-ttu-id="0f048-209">Dans l’Explorateur Windows, vous pouvez déplacer le fichier **Data. bak de la base de données de la base de données MBAM**</span><span class="sxs-lookup"><span data-stu-id="0f048-209">Use Windows Explorer to move the **MBAM Compliance Status Database Data.bak** file from Server A to Server B.</span></span>

2.  <span data-ttu-id="0f048-210">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour exécuter une commande similaire à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="0f048-210">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

    ```powershell
    Copy-Item "Z:\MBAM Compliance Status Database Data.bak"
    \\$SERVERNAME$\$DESTINATIONSHARE$
    ```

3.  <span data-ttu-id="0f048-211">À l’aide du tableau suivant, remplacez les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="0f048-211">Using the following table, replace the values in the code example with values that match your environment.</span></span>

    | **<span data-ttu-id="0f048-212">Paramètre</span><span class="sxs-lookup"><span data-stu-id="0f048-212">Parameter</span></span>**        | **<span data-ttu-id="0f048-213">Description</span><span class="sxs-lookup"><span data-stu-id="0f048-213">Description</span></span>**                                               |
    |----------------------|---------------------------------------------------------------|
    | <span data-ttu-id="0f048-214">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="0f048-214">$SERVERNAME$</span></span>       | <span data-ttu-id="0f048-215">Nom du serveur sur lequel les fichiers sont copiés.</span><span class="sxs-lookup"><span data-stu-id="0f048-215">Name of the server to which the files will be copied.</span></span>         |
    | <span data-ttu-id="0f048-216">$DESTINATIONSHARE $</span><span class="sxs-lookup"><span data-stu-id="0f048-216">$DESTINATIONSHARE$</span></span> | <span data-ttu-id="0f048-217">Nom du partage et du chemin d’accès dans lesquels les fichiers seront copiés.</span><span class="sxs-lookup"><span data-stu-id="0f048-217">Name of the share and path to which the files will be copied.</span></span> |


### <span data-ttu-id="0f048-218">Restaurer la base de données d’audit et de conformité sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="0f048-218">Restore the Compliance and Audit Database on Server B</span></span>

1.  <span data-ttu-id="0f048-219">Restaurez la base de données de conformité et d’audit sur le serveur B en utilisant la tâche **de restauration de base de données** dans SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="0f048-219">Restore the Compliance and Audit Database on Server B by using the **Restore Database** task in SQL Server Management Studio.</span></span>

2.  <span data-ttu-id="0f048-220">Lorsque la tâche précédente se termine, sélectionnez **à partir de l’appareil**, puis sélectionnez le fichier de sauvegarde de la base de données.</span><span class="sxs-lookup"><span data-stu-id="0f048-220">When the previous task finishes, select **From Device**, and then select the database backup file.</span></span>

3.  <span data-ttu-id="0f048-221">Pour terminer le processus de restauration, **sélectionnez le fichier** **de données de la base de données d’état de conformité MBAM** , puis cliquez sur **OK** .</span><span class="sxs-lookup"><span data-stu-id="0f048-221">Use the **Add** command to select the **MBAM Compliance Status Database Data.bak** file and click **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="0f048-222">Pour automatiser cette procédure, créez un fichier SQL (. Sql) contenant le script SQL suivant:</span><span class="sxs-lookup"><span data-stu-id="0f048-222">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```
    -- Create MBAM Compliance Status Database Data logical backup devices.

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

    FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

    WITH REPLACE

    ```

5.  <span data-ttu-id="0f048-223">Dans Windows PowerShell, exécutez le script qui est stocké dans le fichier et similaire à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="0f048-223">In Windows PowerShell, run the script that is stored in the file and similar to the following:</span></span>

    ```powershell
    Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$

    ```

6.  <span data-ttu-id="0f048-224">À l’aide de la valeur suivante, remplacez les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="0f048-224">Using the following value, replace the values in the code example with values that match your environment.</span></span>

    <span data-ttu-id="0f048-225">**$ServerName $ \ $SQLInstanceName $** -nom du serveur et l’instance vers laquelle la base de données d’audit et de conformité sera restaurée.</span><span class="sxs-lookup"><span data-stu-id="0f048-225">**$SERVERNAME$\$SQLINSTANCENAME$** - Server name and instance to which the Compliance and Audit Database will be restored.</span></span>

### <span data-ttu-id="0f048-226">Configurer l’accès à la base de données sur le serveur B et mettre à jour les données de connexion</span><span class="sxs-lookup"><span data-stu-id="0f048-226">Configure access to the Database on Server B and update connection data</span></span>

1. <span data-ttu-id="0f048-227">Vérifiez que la connexion utilisateur de Microsoft SQL Server qui autorise l’accès à la mise en conformité et audit de la base de données sur la base de données restaurée est mappée au compte d’accès que vous avez fourni lors du processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="0f048-227">Verify that the Microsoft SQL Server user login that enables Compliance and Audit Database access on the restored database is mapped to the access account that you provided during the configuration process.</span></span>

   >[!NOTE]
   ><span data-ttu-id="0f048-228">Si la connexion n’est pas la même, créez une connexion à l’aide de SQL Server Management Studio, puis mappez-la à l’utilisateur de la base de données existante.</span><span class="sxs-lookup"><span data-stu-id="0f048-228">If the login is not the same, create a login by using SQL Server Management Studio, and map it to the existing database user.</span></span>

2. <span data-ttu-id="0f048-229">Sur le serveur qui exécute le site Web d’administration et de surveillance, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour les informations de la chaîne de connexion pour le site Web.</span><span class="sxs-lookup"><span data-stu-id="0f048-229">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to update the connection string information for the Website.</span></span>

3. <span data-ttu-id="0f048-230">Modifiez la clé de Registre suivante:</span><span class="sxs-lookup"><span data-stu-id="0f048-230">Edit the following registry key:</span></span>

   **<span data-ttu-id="0f048-231">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString</span><span class="sxs-lookup"><span data-stu-id="0f048-231">HKLM\\Software\\Microsoft\\MBAM Server\\Web\\ComplianceDBConnectionString</span></span>**

4. <span data-ttu-id="0f048-232">Mettez à jour la valeur de la **source de données** avec le nom du serveur et de l’instance (par exemple, \ $ServerName \ $ \ \ \ $SQLInstanceName) sur lequel la base de données de récupération a été déplacée.</span><span class="sxs-lookup"><span data-stu-id="0f048-232">Update the **Data Source** value with the name of the server and instance (for example, \$SERVERNAME\$\\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

5. <span data-ttu-id="0f048-233">Mettez à jour la valeur **initiale du catalogue** avec le nom de la base de données récupérée.</span><span class="sxs-lookup"><span data-stu-id="0f048-233">Update the **Initial Catalog** value with the recovered database name.</span></span>

6. <span data-ttu-id="0f048-234">Pour automatiser ce processus, vous pouvez utiliser l’invite de commandes Windows PowerShell pour entrer une ligne de commande sur le serveur d’administration et de surveillance qui est semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="0f048-234">To automate this process, you can use the Windows PowerShell command prompt to enter a command line on the Administration and Monitoring Server that is similar to the following:</span></span>

   ```powershell
   reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web" /v
   ComplianceDBConnectionString /t REG_SZ /d "Integrated Security=SSPI;Initial
   Catalog=$DATABASE$;Data Source=$SERVERNAME$\$SQLINSTANCENAME$" /f
   ```
   >[!NOTE]
   ><span data-ttu-id="0f048-235">Cette chaîne de connexion est partagée par toutes les applications Web MBAM locales.</span><span class="sxs-lookup"><span data-stu-id="0f048-235">This connection string is shared by all local MBAM web applications.</span></span> <span data-ttu-id="0f048-236">Par conséquent, il doit être mis à jour une seule fois par serveur.</span><span class="sxs-lookup"><span data-stu-id="0f048-236">Therefore, it needs to be updated only once per server.</span></span>


7. <span data-ttu-id="0f048-237">À l’aide du tableau suivant, remplacez les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="0f048-237">Using the following table, replace the values in the code example with values that match your environment.</span></span>

   |<span data-ttu-id="0f048-238">Paramètre</span><span class="sxs-lookup"><span data-stu-id="0f048-238">Parameter</span></span> | <span data-ttu-id="0f048-239">Description</span><span class="sxs-lookup"><span data-stu-id="0f048-239">Description</span></span> |
   |---------|------------|
   |<span data-ttu-id="0f048-240">$SERVERNAME $ \ $SQLINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="0f048-240">$SERVERNAME$\$SQLINSTANCENAME$</span></span> | <span data-ttu-id="0f048-241">Nom du serveur et instance de SQL Server qui héberge la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="0f048-241">Server name and instance of SQL Server where the Recovery Database is located.</span></span>|
   |<span data-ttu-id="0f048-242">$DATABASE $</span><span class="sxs-lookup"><span data-stu-id="0f048-242">$DATABASE$</span></span>|<span data-ttu-id="0f048-243">Nom de la base de données récupérée.</span><span class="sxs-lookup"><span data-stu-id="0f048-243">Name of the recovered database.</span></span>|

### <span data-ttu-id="0f048-244">Installez le logiciel serveur MBAM et exécutez l’Assistant Configuration de MBAM Server sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="0f048-244">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>

1.  <span data-ttu-id="0f048-245">Installez le logiciel serveur MBAM 2,5 sur le serveur B. Pour plus d’informations, reportez-vous à [installation du logiciel serveur MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span><span class="sxs-lookup"><span data-stu-id="0f048-245">Install the MBAM 2.5 Server software on Server B. For details, see [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).</span></span>

2.  <span data-ttu-id="0f048-246">Sur le serveur B, démarrez l’Assistant Configuration de MBAM Server, cliquez sur **ajouter de nouvelles fonctionnalités**, puis sélectionnez uniquement la fonctionnalité **de conformité et d’audit** .</span><span class="sxs-lookup"><span data-stu-id="0f048-246">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Compliance and Audit Database** feature.</span></span> <span data-ttu-id="0f048-247">Pour plus d’informations sur la configuration des bases de données, voir [Comment configurer les bases de données 2,5 de MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span><span class="sxs-lookup"><span data-stu-id="0f048-247">For details on how to configure the databases, see [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).</span></span>

    >[!TIP]
    ><span data-ttu-id="0f048-248">Vous pouvez également utiliser l’applet de contrôle Windows PowerShell **Enable-MbamDatabase** pour configurer la conformité et l’audit.</span><span class="sxs-lookup"><span data-stu-id="0f048-248">Alternatively, you can use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the Compliance and Audit Database.</span></span>


### <span data-ttu-id="0f048-249">Reprendre l’instance du site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="0f048-249">Resume the instance of the Administration and Monitoring Website</span></span>

<span data-ttu-id="0f048-250">Sur le serveur qui exécute le site Web d’administration et de surveillance, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="0f048-250">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

<span data-ttu-id="0f048-251">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour exécuter une commande similaire à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="0f048-251">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

```powershell
Start-Website "Microsoft BitLocker Administration and Monitoring"
```

>[!NOTE]
><span data-ttu-id="0f048-252">Pour exécuter cette commande, vous devez ajouter le module IIS pour Windows PowerShell à l’instance actuelle de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0f048-252">To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>
