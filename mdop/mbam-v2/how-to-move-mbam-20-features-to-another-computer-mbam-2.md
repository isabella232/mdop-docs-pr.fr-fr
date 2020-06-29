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
# <span data-ttu-id="5ade8-103">Déplacement de composants MBAM2.0 vers un autre ordinateur</span><span class="sxs-lookup"><span data-stu-id="5ade8-103">How to Move MBAM 2.0 Features to Another Computer</span></span>


<span data-ttu-id="5ade8-104">Cette rubrique décrit la procédure à suivre pour déplacer une ou plusieurs fonctionnalités d’administration et de surveillance de Microsoft BitLocker (MBAM) vers un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5ade8-104">This topic describes the steps that you should take to move one or more Microsoft BitLocker Administration and Monitoring (MBAM) features to a different computer.</span></span> <span data-ttu-id="5ade8-105">Lorsque vous déplacez plusieurs fonctionnalités d’administration et de surveillance de BitLocker, vous devez les déplacer dans l’ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="5ade8-105">When moving more than one Microsoft BitLocker Administration and Monitoring feature, you should move them in the following order:</span></span>

1.  <span data-ttu-id="5ade8-106">Base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="5ade8-106">Recovery Database</span></span>

2.  <span data-ttu-id="5ade8-107">Base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="5ade8-107">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="5ade8-108">Rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="5ade8-108">Compliance and Audit Reports</span></span>

4.  <span data-ttu-id="5ade8-109">Administration et surveillance</span><span class="sxs-lookup"><span data-stu-id="5ade8-109">Administration and Monitoring</span></span>

## <span data-ttu-id="5ade8-110">Déplacement de la base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="5ade8-110">Moving the Recovery Database</span></span>


<span data-ttu-id="5ade8-111">Pour déplacer la base de données de récupération d’un ordinateur à un autre (par exemple, du serveur A vers un serveur B), utilisez la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="5ade8-111">To move the Recovery Database from one computer to another (for example, from Server A to Server B), use the following procedure.</span></span>

1.  <span data-ttu-id="5ade8-112">Arrêtez toutes les instances du site Web Administration et analyse.</span><span class="sxs-lookup"><span data-stu-id="5ade8-112">Stop all instances of the Administration and Monitoring web site.</span></span>

2.  <span data-ttu-id="5ade8-113">Exécutez le programme d’installation de MBAM sur le serveur B.</span><span class="sxs-lookup"><span data-stu-id="5ade8-113">Run MBAM Setup on Server B.</span></span>

3.  <span data-ttu-id="5ade8-114">Sauvegarder la base de données de récupération MBAM sur le serveur A.</span><span class="sxs-lookup"><span data-stu-id="5ade8-114">Back up the MBAM Recovery Database on Server A.</span></span>

4.  <span data-ttu-id="5ade8-115">Déplacez la base de données de récupération MBAM du serveur A à B.</span><span class="sxs-lookup"><span data-stu-id="5ade8-115">Move the MBAM Recovery Database from Server A to B.</span></span>

5.  <span data-ttu-id="5ade8-116">Restaurez la base de données de récupération MBAM sur le serveur B.</span><span class="sxs-lookup"><span data-stu-id="5ade8-116">Restore the MBAM Recovery Database on Server B.</span></span>

6.  <span data-ttu-id="5ade8-117">Configurer l’accès à la base de données de récupération MBAM sur le serveur B.</span><span class="sxs-lookup"><span data-stu-id="5ade8-117">Configure access to the MBAM Recovery Database on Server B.</span></span>

7.  <span data-ttu-id="5ade8-118">Mettez à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM.</span><span class="sxs-lookup"><span data-stu-id="5ade8-118">Update the database connection data on MBAM Administration and Monitoring servers.</span></span>

8.  <span data-ttu-id="5ade8-119">Reprenez toutes les instances de MBAM site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="5ade8-119">Resume all instances of the MBAM Administration and Monitoring website.</span></span>

**<span data-ttu-id="5ade8-120">Arrêter toutes les instances de MBAM site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="5ade8-120">Stop All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="5ade8-121">Sur chacun des serveurs exécutant la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour arrêter le site Web MBAM, intitulé **administration et analyse de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-121">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="5ade8-122">Pour automatiser cette procédure, vous pouvez utiliser la ligne de commande Windows PowerShell suivante:</span><span class="sxs-lookup"><span data-stu-id="5ade8-122">To automate this procedure, you can use Windows PowerShell to enter command line that is similar to the:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="5ade8-123">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-123">Note</span></span>**  
    <span data-ttu-id="5ade8-124">Pour exécuter cette ligne de commande PowerShell, le module IIS pour PowerShell doit être ajouté à l’instance actuelle de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5ade8-124">To run this PowerShell command line, the IIS Module for PowerShell must be added to current instance of PowerShell.</span></span> <span data-ttu-id="5ade8-125">Par ailleurs, vous devez mettre à jour la stratégie d’exécution PowerShell pour permettre l’exécution de scripts.</span><span class="sxs-lookup"><span data-stu-id="5ade8-125">In addition, you must update the PowerShell execution policy to enable execution of scripts.</span></span>



**<span data-ttu-id="5ade8-126">Exécution de la configuration de MBAM sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="5ade8-126">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="5ade8-127">Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez uniquement la **base de données de récupération** pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="5ade8-127">Run MBAM Setup on Server B and select only the **Recovery Database** for installation.</span></span>

2.  <span data-ttu-id="5ade8-128">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer la ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-128">To automate this procedure, you can use Windows PowerShell to enter command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ TOPOLOGY=$X$`

    **<span data-ttu-id="5ade8-129">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-129">Note</span></span>**  
    <span data-ttu-id="5ade8-130">Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-130">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="5ade8-131">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et de l’instance dans lesquels la base de données de récupération sera déplacée.</span><span class="sxs-lookup"><span data-stu-id="5ade8-131">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery Database will be moved.</span></span>

    -   <span data-ttu-id="5ade8-132">$DOMAIN $ \ \ $SERVERNAME $-entrez les noms de domaine et de serveur de chaque serveur d’administration et de surveillance MBAM qui contactera la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="5ade8-132">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Administration and Monitoring Server that will contact the Recovery Database.</span></span> <span data-ttu-id="5ade8-133">Utilisez un point-virgule pour séparer chaque paire de domaines et de serveurs dans la liste (par exemple, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $).</span><span class="sxs-lookup"><span data-stu-id="5ade8-133">Use a semi-colon to separate each domain and server pairs in the list (for example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$).</span></span> <span data-ttu-id="5ade8-134">Le nom de chaque serveur doit être suivi du symbole «$», comme le montre l’exemple (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).</span><span class="sxs-lookup"><span data-stu-id="5ade8-134">Each server name must be followed by a “$” symbol, as shown in the example (MyDomain\\MyServerName1$; MyDomain\\MyServerName2$).</span></span>

    -   <span data-ttu-id="5ade8-135">$X $-entrez **0** si vous installez la topologie autonome MBAM, ou **1** si vous installez la topologie MBAM Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5ade8-135">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="5ade8-136">Sauvegarder la base de données de récupération sur le serveur A</span><span class="sxs-lookup"><span data-stu-id="5ade8-136">Back Up the Recovery Database on Server A</span></span>**

1.  <span data-ttu-id="5ade8-137">Pour sauvegarder la base de données de récupération sur le serveur A, utilisez SQL Server Management Studio et la tâche nommée sauvegarder.</span><span class="sxs-lookup"><span data-stu-id="5ade8-137">To back up the Recovery Database on Server A, use SQL Server Management Studio and the Task named Back Up.</span></span> <span data-ttu-id="5ade8-138">Par défaut, le nom de la base de données est **MBAM de récupération de la base de**données.</span><span class="sxs-lookup"><span data-stu-id="5ade8-138">By default, the database name is **MBAM Recovery Database**.</span></span>

2.  <span data-ttu-id="5ade8-139">Pour automatiser cette procédure, créez un fichier SQL (. Sql) contenant le script SQL suivant:</span><span class="sxs-lookup"><span data-stu-id="5ade8-139">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    <span data-ttu-id="5ade8-140">Modifiez la base de données de récupération MBAM pour utiliser le mode de récupération complet.</span><span class="sxs-lookup"><span data-stu-id="5ade8-140">Modify the MBAM Recovery Database to use the full recovery mode.</span></span>

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

    **<span data-ttu-id="5ade8-141">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-141">Note</span></span>**  
    <span data-ttu-id="5ade8-142">Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-142">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="5ade8-143">$PASSWORD $-entrez le mot de passe que vous allez utiliser pour chiffrer le fichier de clé privée.</span><span class="sxs-lookup"><span data-stu-id="5ade8-143">$PASSWORD$ - Enter a password that you will use to encrypt the Private Key file.</span></span>



3.  <span data-ttu-id="5ade8-144">Exécutez le fichier SQL en utilisant SQL Server PowerShell et une ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-144">Run the SQL File by using SQL Server PowerShell and a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="5ade8-145">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-145">Note</span></span>**  
    <span data-ttu-id="5ade8-146">Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-146">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="5ade8-147">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et de l’instance à partir desquels la base de données de récupération sera sauvegardée.</span><span class="sxs-lookup"><span data-stu-id="5ade8-147">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance from which the Recovery Database will be backed up.</span></span>



**<span data-ttu-id="5ade8-148">Déplacer la base de données de récupération et le certificat du serveur A vers le serveur B</span><span class="sxs-lookup"><span data-stu-id="5ade8-148">Move the Recovery Database and Certificate from Server A to Server B</span></span>**

1.  <span data-ttu-id="5ade8-149">Déplacez le fichier suivant du serveur A vers le serveur B à l’aide de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="5ade8-149">Move the following file from Server A to Server B by using Windows Explorer.</span></span>

    -   <span data-ttu-id="5ade8-150">Données de base de données de récupération de MBAM. bak</span><span class="sxs-lookup"><span data-stu-id="5ade8-150">MBAM Recovery Database data.bak</span></span>

2.  <span data-ttu-id="5ade8-151">Pour déplacer le certificat de la base de données chiffrée, utilisez les étapes d’Automation suivantes.</span><span class="sxs-lookup"><span data-stu-id="5ade8-151">To move the certificate for the encrypted database, use the following automation steps.</span></span> <span data-ttu-id="5ade8-152">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-152">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Recovery Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="5ade8-153">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-153">Note</span></span>**  
    <span data-ttu-id="5ade8-154">Remplacez la valeur suivante dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-154">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="5ade8-155">$SERVERNAME $-entrez le nom du serveur sur lequel les fichiers sont copiés.</span><span class="sxs-lookup"><span data-stu-id="5ade8-155">$SERVERNAME$ - Enter the name of the server to which the files will be copied.</span></span>

    -   <span data-ttu-id="5ade8-156">$DESTINATIONSHARE $-entrez le nom du partage et du chemin d’accès dans lesquels les fichiers seront copiés.</span><span class="sxs-lookup"><span data-stu-id="5ade8-156">$DESTINATIONSHARE$ - Enter the name of the share and path to which the files will be copied.</span></span>



**<span data-ttu-id="5ade8-157">Restaurer la base de données de récupération sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="5ade8-157">Restore the Recovery Database on Server B</span></span>**

1.  <span data-ttu-id="5ade8-158">Restaurez la base de données de récupération sur le serveur B en utilisant SQL Server Management Studio et la tâche nommée **restaurer la base de données**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-158">Restore the Recovery Database on Server B by using SQL Server Management Studio and the task named **Restore Database**.</span></span>

2.  <span data-ttu-id="5ade8-159">Lorsque la tâche est achevée, sélectionnez le fichier de sauvegarde de la base de données en sélectionnant l’option **à partir de l’appareil** , puis utilisez la commande **Ajouter** pour sélectionner le fichier de données de la base de données de récupération MBAM. **bak** .</span><span class="sxs-lookup"><span data-stu-id="5ade8-159">Once the task has been completed, select the database backup file by selecting the **From Device** option and then use the **Add** command to select the MBAM Recovery database **Data.bak** file.</span></span>

3.  <span data-ttu-id="5ade8-160">Sélectionnez **OK** pour terminer le processus de restauration.</span><span class="sxs-lookup"><span data-stu-id="5ade8-160">Select **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="5ade8-161">Pour automatiser cette procédure, créez un fichier SQL (. Sql) qui contient le script SQL suivant:</span><span class="sxs-lookup"><span data-stu-id="5ade8-161">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

    **<span data-ttu-id="5ade8-162">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-162">Note</span></span>**  
    <span data-ttu-id="5ade8-163">Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-163">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="5ade8-164">$PASSWORD $-entrez un mot de passe que vous avez utilisé pour chiffrer le fichier de clé privée.</span><span class="sxs-lookup"><span data-stu-id="5ade8-164">$PASSWORD$ - Enter a password that you used to encrypt the Private Key file.</span></span>



5.  <span data-ttu-id="5ade8-165">Vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-165">You can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="5ade8-166">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-166">Note</span></span>**  
    <span data-ttu-id="5ade8-167">Remplacez la valeur suivante dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-167">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="5ade8-168">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et de l’instance vers lesquels la base de données de récupération sera restaurée.</span><span class="sxs-lookup"><span data-stu-id="5ade8-168">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery Database will be restored.</span></span>



**<span data-ttu-id="5ade8-169">Configurer l’accès à la base de données de récupération sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="5ade8-169">Configure Access to the Recovery Database on Server B</span></span>**

1.  <span data-ttu-id="5ade8-170">Sur le serveur B, utilisez le composant logiciel enfichable utilisateurs et groupes local dans le gestionnaire de serveur pour ajouter les comptes d’ordinateur de chaque serveur qui exécute la fonctionnalité d’administration et de surveillance MBAM au groupe local intitulé **MBAM de récupération et de BDD matériel**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-170">On Server B, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring feature to the Local Group named **MBAM Recovery and Hardware DB Access**.</span></span>

2.  <span data-ttu-id="5ade8-171">Vérifiez que l’accès à la récupération de la base de données **MBAM et** de la base de données sur la base de données restaurée est mappé sur le nom de connexion **$MachineName \\MBAM de récupération et de**la base de données du matériel.</span><span class="sxs-lookup"><span data-stu-id="5ade8-171">Verify that the SQL login **MBAM Recovery and Hardware DB Access** on the restored database is mapped to the login name **$MachineName$\\MBAM Recovery and Hardware DB Access**.</span></span> <span data-ttu-id="5ade8-172">Si ce n’est pas le cas, créez-en un autre avec des appartenances de groupe similaires, puis mappez-le au nom de connexion $MachineName l’accès à la **récupération \\MBAM et à la BD matérielle**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-172">If it is not mapped as described, create another login with similar group memberships, and map it to the login name **$MachineName$\\MBAM Recovery and Hardware DB Access**.</span></span>

3.  <span data-ttu-id="5ade8-173">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell sur le serveur B pour entrer une ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-173">To automate this procedure, you can use Windows PowerShell on Server B to enter a command line that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="5ade8-174">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-174">Note</span></span>**  
    <span data-ttu-id="5ade8-175">Remplacez les valeurs suivantes dans l’exemple ci-dessus avec les valeurs applicables pour votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-175">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="5ade8-176">$DOMAIN $ \ \ $SERVERNAME $ $-entrez le domaine et le nom de l’ordinateur du serveur d’administration et de surveillance MBAM.</span><span class="sxs-lookup"><span data-stu-id="5ade8-176">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="5ade8-177">Le nom du serveur doit être suivi d’un $, comme le montre l’exemple (par exemple, MyDomain\\MyServerName1 $).</span><span class="sxs-lookup"><span data-stu-id="5ade8-177">The server name must be followed by a $, as shown in the example (for example, MyDomain\\MyServerName1$).</span></span>



~~~
This command line must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="5ade8-178">Mettre à jour les données de connexion de la base de données de récupération sur les serveurs d’administration et de surveillance MBAM</span><span class="sxs-lookup"><span data-stu-id="5ade8-178">Update the Recovery Database Connection Data on the MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="5ade8-179">Sur chacun des serveurs exécutant la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour les informations de la chaîne de connexion pour les applications suivantes, hébergées sur le site Web d’administration et de surveillance:</span><span class="sxs-lookup"><span data-stu-id="5ade8-179">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following applications, which are hosted in the Administration and Monitoring website:</span></span>

   -   <span data-ttu-id="5ade8-180">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="5ade8-180">MBAMAdministrationService</span></span>

   -   <span data-ttu-id="5ade8-181">MBAMRecoveryAndHardwareService</span><span class="sxs-lookup"><span data-stu-id="5ade8-181">MBAMRecoveryAndHardwareService</span></span>

2. <span data-ttu-id="5ade8-182">Sélectionner chaque application et utiliser la fonctionnalité **éditeur de configuration** , située sous la section **gestion** de l’affichage des **fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-182">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="5ade8-183">Sélectionnez l’option **configurationStrings** dans le contrôle de **liste de sections** .</span><span class="sxs-lookup"><span data-stu-id="5ade8-183">Select the **configurationStrings** option from the **Section list** control.</span></span>

4. <span data-ttu-id="5ade8-184">Sélectionnez la ligne nommée **(collection)** , puis ouvrez l' **éditeur de collection** en sélectionnant le bouton à droite de la ligne.</span><span class="sxs-lookup"><span data-stu-id="5ade8-184">Select the row named **(Collection)** and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="5ade8-185">Dans l' **éditeur de collection**, sélectionnez la ligne nommée **KeyRecoveryConnectionString** lors de la mise à jour de la configuration de l’application MBAMAdministrationService ou de la ligne nommée <strong> Microsoft. mbam. RecoveryAndHardwareDataStore. </strong> ConnectionString lors de la mise à jour de la configuration de MBAMRecoveryAndHardwareService.</span><span class="sxs-lookup"><span data-stu-id="5ade8-185">In the **Collection Editor**, select the row named **KeyRecoveryConnectionString** when updating the configuration for the MBAMAdministrationService application or the row named <strong>Microsoft.Mbam.RecoveryAndHardwareDataStore.</strong>ConnectionString when updating the configuration for the MBAMRecoveryAndHardwareService.</span></span>

6. <span data-ttu-id="5ade8-186">Mettez à jour la **source de données =** valeur pour la propriété **configurationStrings** pour indiquer le nom du serveur et l’instance (par exemple, $SERVERNAME $ \ \ $SQLInstanceName $) où la base de données de récupération a été déplacée.</span><span class="sxs-lookup"><span data-stu-id="5ade8-186">Update the **Data Source=** value for the **configurationStrings** property to list the server name and instance (for example, $SERVERNAME$\\$SQLINSTANCENAME$) where the Recovery Database was moved to.</span></span>

7. <span data-ttu-id="5ade8-187">Pour automatiser cette procédure, vous pouvez utiliser Windows pour entrer une ligne de commande semblable à ce qui suit, sur chaque serveur d’administration et de surveillance:</span><span class="sxs-lookup"><span data-stu-id="5ade8-187">To automate this procedure, you can use Windows to enter a command line, that is similar to the following, on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **<span data-ttu-id="5ade8-188">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-188">Note</span></span>**  
   <span data-ttu-id="5ade8-189">Remplacez la valeur suivante dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-189">Replace the following value in the example above with those that match your environment:</span></span>

   -   <span data-ttu-id="5ade8-190">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance de la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="5ade8-190">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery Database is.</span></span>



**<span data-ttu-id="5ade8-191">Reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM</span><span class="sxs-lookup"><span data-stu-id="5ade8-191">Resume all Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="5ade8-192">Sur chaque serveur exécutant la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web MBAM, intitulé **administration et analyse de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-192">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="5ade8-193">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-193">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="5ade8-194">Déplacement de la fonctionnalité de conformité et de base de données d’audit</span><span class="sxs-lookup"><span data-stu-id="5ade8-194">Moving the Compliance and Audit Database Feature</span></span>


<span data-ttu-id="5ade8-195">Si vous voulez déplacer la base de données d’audit et de conformité MBAM d’un ordinateur à un autre (autrement dit, déplacez la base de données du serveur A vers le serveur B), utilisez la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="5ade8-195">If you want to move the MBAM Compliance and Audit Database from one computer to another (that is, move the database from Server A to Server B), use the following procedure.</span></span> <span data-ttu-id="5ade8-196">Le processus comprend les principales étapes suivantes:</span><span class="sxs-lookup"><span data-stu-id="5ade8-196">The process includes the following high-level steps:</span></span>

1.  <span data-ttu-id="5ade8-197">Arrêtez toutes les instances du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="5ade8-197">Stop all instances of the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="5ade8-198">Exécutez le programme d’installation de MBAM sur le serveur B.</span><span class="sxs-lookup"><span data-stu-id="5ade8-198">Run MBAM setup on Server B.</span></span>

3.  <span data-ttu-id="5ade8-199">Sauvegarder la base de données sur le serveur A.</span><span class="sxs-lookup"><span data-stu-id="5ade8-199">Back up the Database on Server A.</span></span>

4.  <span data-ttu-id="5ade8-200">Déplacez la base de données du serveur A vers B.</span><span class="sxs-lookup"><span data-stu-id="5ade8-200">Move the Database from Server A to B.</span></span>

5.  <span data-ttu-id="5ade8-201">Restaurez la base de données sur le serveur B.</span><span class="sxs-lookup"><span data-stu-id="5ade8-201">Restore the Database on Server B.</span></span>

6.  <span data-ttu-id="5ade8-202">Configurer l’accès à la base de données sur le serveur B.</span><span class="sxs-lookup"><span data-stu-id="5ade8-202">Configure access to the Database on Server B.</span></span>

7.  <span data-ttu-id="5ade8-203">Mettez à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM.</span><span class="sxs-lookup"><span data-stu-id="5ade8-203">Update the database connection data on the MBAM Administration and Monitoring servers.</span></span>

8.  <span data-ttu-id="5ade8-204">Mettez à jour la chaîne de connexion à la source de données des rapports SSRS avec le nouvel emplacement de la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5ade8-204">Update the SSRS reports data source connection string with the new location of the Compliance and Audit Database.</span></span>

9.  <span data-ttu-id="5ade8-205">Reprenez toutes les instances du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="5ade8-205">Resume all instances of the Administration and Monitoring website.</span></span>

**<span data-ttu-id="5ade8-206">Arrêter toutes les instances du site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="5ade8-206">Stop All Instances of the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="5ade8-207">Sur chaque serveur exécutant la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour arrêter d’arrêter le site Web MBAM appelé **administration et surveillance de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-207">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="5ade8-208">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-208">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Stop-s “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="5ade8-209">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-209">Note</span></span>**  
    <span data-ttu-id="5ade8-210">Pour exécuter cette ligne de commande, vous devez ajouter le module IIS pour PowerShell à l’instance actuelle de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5ade8-210">To run this command line, you must add the IIS Module for PowerShell to the current instance of PowerShell.</span></span> <span data-ttu-id="5ade8-211">Par ailleurs, vous devez mettre à jour la stratégie d’exécution PowerShell pour permettre l’exécution de scripts.</span><span class="sxs-lookup"><span data-stu-id="5ade8-211">In addition, you must update the PowerShell execution policy to enable scripts to be run.</span></span>



**<span data-ttu-id="5ade8-212">Exécution de la configuration de MBAM sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="5ade8-212">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="5ade8-213">Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez uniquement la **base de données d’audit et de conformité** pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="5ade8-213">Run MBAM Setup on Server B and select only the **Compliance and Audit Database** for installation.</span></span>

2.  <span data-ttu-id="5ade8-214">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-214">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$ TOPOLOGY=$X$`

    **<span data-ttu-id="5ade8-215">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-215">Note</span></span>**  
    <span data-ttu-id="5ade8-216">Remarque: remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-216">Note: Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="5ade8-217">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance de destination de la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5ade8-217">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database will be moved to.</span></span>

    -   <span data-ttu-id="5ade8-218">$DOMAIN $ \ \ $SERVERNAME $-entrez les noms de domaine et de serveur de chaque serveur d’administration et de surveillance MBAM qui contactera la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5ade8-218">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Administration and Monitoring Server that will contact the Compliance and Audit Database.</span></span> <span data-ttu-id="5ade8-219">Utilisez un point-virgule pour séparer chaque paire de domaines et de serveurs dans la liste (par exemple, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $).</span><span class="sxs-lookup"><span data-stu-id="5ade8-219">Use a semi-colon to separate each domain and server pair in the list (for example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$).</span></span> <span data-ttu-id="5ade8-220">Le nom de chaque serveur doit être suivi du symbole «$», comme le montre l’exemple (MyDomain\\MyServerName1 $; MyDomain\\MyServerName2 $).</span><span class="sxs-lookup"><span data-stu-id="5ade8-220">Each server name must be followed by a “$” symbol, as shown in the example (MyDomain\\MyServerName1$; MyDomain\\MyServerName2$).</span></span>

    -   <span data-ttu-id="5ade8-221">$DOMAIN $ \ \ $USERNAME $-entrez le domaine et le nom d’utilisateur qui seront utilisés par les rapports de conformité et d’audit pour vous connecter à la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5ade8-221">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="5ade8-222">$X $-entrez **0** si vous installez la topologie autonome MBAM, ou **1** si vous installez la topologie MBAM Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5ade8-222">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="5ade8-223">Sauvegarder la base de données de conformité et d’audit sur le serveur A</span><span class="sxs-lookup"><span data-stu-id="5ade8-223">Back Up the Compliance and Audit Database on Server A</span></span>**

1.  <span data-ttu-id="5ade8-224">Pour sauvegarder la base de données de conformité et d’audit sur le serveur A, utilisez SQL Server Management Studio et la tâche nommée **sauvegarder**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-224">To back up the Compliance and Audit Database on Server A, use SQL Server Management Studio and the task named **Back Up**.</span></span> <span data-ttu-id="5ade8-225">Par défaut, le nom de la base de données est **MBAM de la base de données état de conformité**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-225">By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="5ade8-226">Pour automatiser cette procédure, créez un fichier SQL (. Sql) qui contient le script SQL suivant:</span><span class="sxs-lookup"><span data-stu-id="5ade8-226">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

3.  <span data-ttu-id="5ade8-227">Exécutez le fichier SQL à l’aide d’une ligne de commande Windows PowerShell semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-227">Run the SQL file by using a Windows PowerShell command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="5ade8-228">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-228">Note</span></span>**  
    <span data-ttu-id="5ade8-229">Remplacez la valeur suivante dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-229">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="5ade8-230">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance à partir desquels la base de données d’audit et de conformité sera sauvegardée.</span><span class="sxs-lookup"><span data-stu-id="5ade8-230">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit database will be backed up from.</span></span>



**<span data-ttu-id="5ade8-231">Déplacer la base de données d’audit et de conformité du serveur A à B</span><span class="sxs-lookup"><span data-stu-id="5ade8-231">Move the Compliance and Audit Database from Server A to B</span></span>**

1.  <span data-ttu-id="5ade8-232">Déplacez les fichiers suivants du serveur A vers le serveur B à l’aide de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="5ade8-232">Move the following files from Server A to Server B using Windows Explorer.</span></span>

    -   <span data-ttu-id="5ade8-233">Données de la base de données d’état de conformité MBAM. bak</span><span class="sxs-lookup"><span data-stu-id="5ade8-233">MBAM Compliance Status Database Data.bak</span></span>

2.  <span data-ttu-id="5ade8-234">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-234">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="5ade8-235">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-235">Note</span></span>**  
    <span data-ttu-id="5ade8-236">Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-236">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="5ade8-237">$SERVERNAME $-entrez le nom du serveur dans lequel les fichiers sont copiés.</span><span class="sxs-lookup"><span data-stu-id="5ade8-237">$SERVERNAME$ - Enter the server name where the files will be copied to.</span></span>

    -   <span data-ttu-id="5ade8-238">$DESTINATIONSHARE $-entrez le nom du partage dans lequel les fichiers sont copiés.</span><span class="sxs-lookup"><span data-stu-id="5ade8-238">$DESTINATIONSHARE$ - Enter the name of share and path where the files will be copied to.</span></span>



**<span data-ttu-id="5ade8-239">Restaurer la base de données d’audit et de conformité sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="5ade8-239">Restore the Compliance and Audit Database on Server B</span></span>**

1.  <span data-ttu-id="5ade8-240">Restaurez la base de données d’audit et de conformité sur le serveur B en utilisant SQL Server Management Studio et la tâche nommée **restaurer la base de données**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-240">Restore the Compliance and Audit Database on Server B by using SQL Server Management Studio and the task named **Restore Database**.</span></span>

2.  <span data-ttu-id="5ade8-241">Une fois la tâche effectuée, sélectionnez le fichier de sauvegarde de la base de données en sélectionnant l’option **à partir de l’appareil** , puis utilisez la commande **Ajouter** pour sélectionner le fichier de données de la base de données d’état de conformité MBAM. bak.</span><span class="sxs-lookup"><span data-stu-id="5ade8-241">Once the task has been completed, select the database backup file by selecting the **From Device** option and then use the **Add** command to select the MBAM Compliance Status Database Data.bak file.</span></span> <span data-ttu-id="5ade8-242">Sélectionnez **OK** pour terminer le processus de restauration.</span><span class="sxs-lookup"><span data-stu-id="5ade8-242">Select **OK** to complete the restoration process.</span></span>

3.  <span data-ttu-id="5ade8-243">Pour automatiser cette procédure, créez un fichier SQL (. Sql) qui contient le script SQL suivant:</span><span class="sxs-lookup"><span data-stu-id="5ade8-243">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  <span data-ttu-id="5ade8-244">Exécutez le fichier SQL à l’aide d’une ligne de commande Windows PowerShell semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-244">Run the SQL File by using a Windows PowerShell command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="5ade8-245">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-245">Note</span></span>**  
    <span data-ttu-id="5ade8-246">Remplacez la valeur suivante dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-246">Replace the following value in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="5ade8-247">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance de destination de la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5ade8-247">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database will be restored to.</span></span>



**<span data-ttu-id="5ade8-248">Configurer l’accès à la base de données de conformité et d’audit sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="5ade8-248">Configure Access to the Compliance and Audit Database on Server B</span></span>**

1.  <span data-ttu-id="5ade8-249">Sur le serveur B, utilisez le composant logiciel enfichable utilisateurs et groupes local dans le gestionnaire de serveur pour ajouter les comptes d’ordinateur de chaque serveur qui exécute la fonctionnalité d’administration et de surveillance MBAM au groupe local intitulé **MBAM accès**à la BD d’état de conformité.</span><span class="sxs-lookup"><span data-stu-id="5ade8-249">On Server B, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring feature to the local group named **MBAM Compliance Status DB Access**.</span></span>

2.  <span data-ttu-id="5ade8-250">Vérifiez que l’accès aux bases de données **d’audit** de la conformité de la base de données MBAM sur la base de données restaurée est mappé sur le nom de connexion **$MachineName $ \ \ MBAM Compliance audit**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-250">Verify that the SQL login **MBAM Compliance Auditing DB Access** on the restored database is mapped to the login name **$MachineName$\\ MBAM Compliance Auditing DB Access**.</span></span> <span data-ttu-id="5ade8-251">Si ce n’est pas le cas, créez-en un autre avec des appartenances de groupe similaires, puis mappez-le au nom de connexion **$MachineName $ \ \ MBAM Compliance audit Access**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-251">If it is not mapped as described, create another login with similar group memberships, and map it to the login name **$MachineName$\\ MBAM Compliance Auditing DB Access**.</span></span>

3.  <span data-ttu-id="5ade8-252">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande sur le serveur B qui est semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-252">To automate this procedure, you can use Windows PowerShell to enter a command line on Server B that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="5ade8-253">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-253">Note</span></span>**  
    <span data-ttu-id="5ade8-254">Remplacez les valeurs suivantes dans l’exemple ci-dessus avec les valeurs applicables pour votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-254">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="5ade8-255">$DOMAIN $ \ \ $SERVERNAME $ $-entrez le domaine et le nom de l’ordinateur du serveur d’administration et de surveillance MBAM.</span><span class="sxs-lookup"><span data-stu-id="5ade8-255">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="5ade8-256">Le nom du serveur doit être suivi du «$» comme illustré dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="5ade8-256">The server name must be followed by a “$” as shown in the example.</span></span> <span data-ttu-id="5ade8-257">(par exemple, MyDomain\\MyServerName1 $)</span><span class="sxs-lookup"><span data-stu-id="5ade8-257">(for example, MyDomain\\MyServerName1$)</span></span>

    -   <span data-ttu-id="5ade8-258">$DOMAIN $ \ \ $REPORTSUSERNAME $-entrez le nom du compte d’utilisateur que vous avez utilisé pour configurer la source de données pour les rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="5ade8-258">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit Reports.</span></span>



~~~
The command line for adding the servers to the MBAM Compliance and Audit Database access local group must be run for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="5ade8-259">Mettre à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM</span><span class="sxs-lookup"><span data-stu-id="5ade8-259">Update the Database Connection Data on MBAM Administration and Monitoring Servers</span></span>**

1.  <span data-ttu-id="5ade8-260">Sur chaque serveur exécutant la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour les informations de la chaîne de connexion pour les applications suivantes qui sont hébergées sur le site Web d’administration et de surveillance:</span><span class="sxs-lookup"><span data-stu-id="5ade8-260">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the connection string information for the following applications, which are hosted in the Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="5ade8-261">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="5ade8-261">MBAMAdministrationService</span></span>

    -   <span data-ttu-id="5ade8-262">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="5ade8-262">MBAMComplianceStatusService</span></span>

2.  <span data-ttu-id="5ade8-263">Sélectionner chaque application et utiliser la fonctionnalité **éditeur de configuration** , située sous la section **gestion** de l’affichage des **fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-263">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3.  <span data-ttu-id="5ade8-264">Sélectionnez l’option **configurationStrings** dans le contrôle de **liste de sections** .</span><span class="sxs-lookup"><span data-stu-id="5ade8-264">Select the **configurationStrings** option from the **Section list** control.</span></span>

4.  <span data-ttu-id="5ade8-265">Sélectionnez la ligne nommée **(collection)**, puis ouvrez l' **éditeur de collection** en sélectionnant le bouton à droite de la ligne.</span><span class="sxs-lookup"><span data-stu-id="5ade8-265">Select the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5.  <span data-ttu-id="5ade8-266">Dans l' **éditeur de collection**, sélectionnez la ligne nommée **ComplianceStatusConnectionString** lors de la mise à jour de la configuration de l’application MBAMAdministrationService ou de la ligne nommée **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString** lors de la mise à jour de la configuration pour le MBAMComplianceStatusService.</span><span class="sxs-lookup"><span data-stu-id="5ade8-266">In the **Collection Editor**, select the row named **ComplianceStatusConnectionString** when updating the configuration for the MBAMAdministrationService application, or the row named **Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString** when updating the configuration for the MBAMComplianceStatusService.</span></span>

6.  <span data-ttu-id="5ade8-267">Mettez à jour la **source de données =** valeur pour la propriété **configurationStrings** pour afficher le nom du serveur et de l’instance (par exemple, $SERVERNAME $ \ \ $SQLInstanceName) sur lequel la base de données de récupération a été déplacée.</span><span class="sxs-lookup"><span data-stu-id="5ade8-267">Update the **Data Source=** value for the **configurationStrings** property to list the name of the server and instance (for example, $SERVERNAME$\\$SQLINSTANCENAME) to which the Recovery Database was moved.</span></span>

7.  <span data-ttu-id="5ade8-268">Pour automatiser cette procédure, vous pouvez utiliser Windows pour entrer une ligne de commande sur chaque serveur d’administration et de surveillance qui est semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-268">To automate this procedure, you can use Windows to enter a command line on each Administration and Monitoring Server that is similar to the following:</span></span>

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft Bitlocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **<span data-ttu-id="5ade8-269">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-269">Note</span></span>**  
    <span data-ttu-id="5ade8-270">Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-270">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="5ade8-271">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance de la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="5ade8-271">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery Database is located.</span></span>



**<span data-ttu-id="5ade8-272">Reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM</span><span class="sxs-lookup"><span data-stu-id="5ade8-272">Resume All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="5ade8-273">Sur chaque serveur exécutant la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web MBAM appelé **administration et analyse de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-273">On each server that is running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="5ade8-274">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-274">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="5ade8-275">Déplacement des rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="5ade8-275">Moving the Compliance and Audit Reports</span></span>


<span data-ttu-id="5ade8-276">Si vous voulez déplacer les rapports de conformité et d’audit MBAM d’un ordinateur à un autre (autrement dit, déplacez les rapports du serveur A vers le serveur B), utilisez la procédure suivante, qui inclut les étapes suivantes:</span><span class="sxs-lookup"><span data-stu-id="5ade8-276">If you want to move the MBAM Compliance and Audit Reports from one computer to another (that is, move the reports from Server A to Server B), use the following procedure, which includes the following high-level steps:</span></span>

1.  <span data-ttu-id="5ade8-277">Exécutez le programme d’installation de MBAM sur le serveur B.</span><span class="sxs-lookup"><span data-stu-id="5ade8-277">Run MBAM setup on Server B.</span></span>

2.  <span data-ttu-id="5ade8-278">Configurer l’accès aux rapports de conformité et d’audit sur le serveur B.</span><span class="sxs-lookup"><span data-stu-id="5ade8-278">Configure access to the Compliance and Audit Reports on Server B.</span></span>

3.  <span data-ttu-id="5ade8-279">Arrêtez toutes les instances de l’MBAM site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="5ade8-279">Stop all instances of the MBAM Administration and Monitoring website.</span></span>

4.  <span data-ttu-id="5ade8-280">Mettez à jour les données de connexion rapports sur les serveurs d’administration et de surveillance MBAM.</span><span class="sxs-lookup"><span data-stu-id="5ade8-280">Update the reports connection data on MBAM Administration and Monitoring servers.</span></span>

5.  <span data-ttu-id="5ade8-281">Reprenez toutes les instances de MBAM site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="5ade8-281">Resume all instances of the MBAM Administration and Monitoring website.</span></span>

**<span data-ttu-id="5ade8-282">Exécution de la configuration de MBAM sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="5ade8-282">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="5ade8-283">Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez uniquement la fonctionnalité **rapports de conformité et d’audit** pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="5ade8-283">Run MBAM Setup on Server B and select only the **Compliance and Audit Reports** feature for installation.</span></span>

2.  <span data-ttu-id="5ade8-284">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-284">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$ TOPOLOGY=$X$`

    **<span data-ttu-id="5ade8-285">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-285">Note</span></span>**  
    <span data-ttu-id="5ade8-286">Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-286">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="5ade8-287">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance de la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5ade8-287">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance and Audit Database is located.</span></span>

    -   <span data-ttu-id="5ade8-288">$DOMAIN $ \ \ $USERNAME $-entrez le domaine et le nom d’utilisateur qui seront utilisés par les rapports de conformité et d’audit pour vous connecter à la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5ade8-288">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="5ade8-289">$PASSWORD $-entrez le mot de passe du compte d’utilisateur que vous utiliserez pour vous connecter à la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5ade8-289">$PASSWORD$ - Enter the password of the user account that will be used to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="5ade8-290">$X $-entrez **0** si vous installez la topologie autonome MBAM, ou **1** si vous installez la topologie MBAM Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5ade8-290">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="5ade8-291">Configurer l’accès aux rapports de conformité et d’audit sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="5ade8-291">Configure Access to the Compliance and Audit Reports on Server B</span></span>**

1.  <span data-ttu-id="5ade8-292">Sur le serveur B, utilisez le composant logiciel enfichable utilisateurs et groupes local dans le gestionnaire de serveur pour ajouter les comptes d’utilisateurs qui auront accès aux rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="5ade8-292">On Server B, use the Local user and Groups snap-in from Server Manager to add the user accounts that will have access to the Compliance and Audit Reports.</span></span> <span data-ttu-id="5ade8-293">Ajoutez les comptes d’utilisateurs au groupe local intitulé utilisateurs de rapport MBAM.</span><span class="sxs-lookup"><span data-stu-id="5ade8-293">Add the user accounts to the local group named MBAM Report Users.</span></span>

2.  <span data-ttu-id="5ade8-294">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande sur le serveur B qui est semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-294">To automate this procedure, you can use Windows PowerShell to enter a command line on Server B that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="5ade8-295">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-295">Note</span></span>**  
    <span data-ttu-id="5ade8-296">Remplacez les valeurs suivantes dans l’exemple ci-dessus avec les valeurs applicables pour votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-296">Replace the following values in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="5ade8-297">$DOMAIN $ \ \ $REPORTSUSERNAME $-entrez le nom du compte d’utilisateur que vous avez utilisé pour configurer la source de données pour les rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="5ade8-297">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports.</span></span>



~~~
The command line for adding the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**<span data-ttu-id="5ade8-298">Arrêter toutes les instances de MBAM site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="5ade8-298">Stop All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="5ade8-299">Sur chaque serveur exécutant la fonctionnalité de serveur d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour arrêter d’arrêter le site Web MBAM appelé **administration et analyse Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-299">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="5ade8-300">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-300">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**<span data-ttu-id="5ade8-301">Mettre à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM</span><span class="sxs-lookup"><span data-stu-id="5ade8-301">Update the Database Connection Data on the MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="5ade8-302">Sur chaque serveur exécutant la fonctionnalité de serveur d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour l’URL des rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="5ade8-302">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to update the Compliance and Audit Reports URL.</span></span>

2. <span data-ttu-id="5ade8-303">Sélectionnez le site Web d' **administration et de contrôle Microsoft BitLocker** , puis utilisez la fonctionnalité **éditeur de configuration** qui est située sous la section **gestion** de l' **affichage des fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-303">Select the **Microsoft BitLocker Administration and Monitoring** website, and use the **Configuration Editor** feature that is location under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="5ade8-304">Sélectionnez l’option **appSettings** dans le contrôle de **liste de sections** .</span><span class="sxs-lookup"><span data-stu-id="5ade8-304">Select the **appSettings** option from the **Section list** control.</span></span>

4. <span data-ttu-id="5ade8-305">Sélectionnez la ligne nommée **(collection)** , puis ouvrez l' **éditeur de collection** en sélectionnant le bouton à droite de la ligne.</span><span class="sxs-lookup"><span data-stu-id="5ade8-305">Select the row named **(Collection)** and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="5ade8-306">Dans l' **éditeur de collection**, sélectionnez la ligne nommée **Microsoft. mbam. reports. URL**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-306">In the **Collection Editor**, select the row named **Microsoft.Mbam.Reports.Url**.</span></span>

6. <span data-ttu-id="5ade8-307">Mettez à jour la valeur pour **Microsoft. mbam. reports. URL** pour refléter le nom de serveur pour le serveur B. Si la fonctionnalité rapports de compatibilité et d’audit a été installée sur une instance nommée SQL Reporting Services, veillez à ajouter ou à mettre à jour le nom de l’instance à l’URL (par exemple, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/pages....).</span><span class="sxs-lookup"><span data-stu-id="5ade8-307">Update the value for **Microsoft.Mbam.Reports.Url** to reflect the server name for Server B. If the Compliance and Audit Reports feature was installed on a named SQL Reporting Services instance, be sure to add or update the name of the instance to the URL (for example, http://$SERVERNAME$/ReportServer\_$SQLSRSINSTANCENAME$/Pages....)</span></span>

7. <span data-ttu-id="5ade8-308">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande sur chaque serveur d’administration et de surveillance qui est semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-308">To automate this procedure, you can use Windows PowerShell to enter a command line on each Administration and Monitoring Server that is similar to the following:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\ \sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/ Microsoft+BitLocker+Administration+and+Monitoring/”`

   **<span data-ttu-id="5ade8-309">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-309">Note</span></span>**  
   <span data-ttu-id="5ade8-310">Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-310">Replace the following values in the example above with those that match your environment:</span></span>

   -   <span data-ttu-id="5ade8-311">$SERVERNAME $-entrez le nom du nom du serveur sur lequel sont installés les rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="5ade8-311">$SERVERNAME$ - Enter the name of the server name to which the Compliance and Audit Reports were installed.</span></span>

   -   <span data-ttu-id="5ade8-312">$SRSINSTANCENAME $-entrez le nom de l’instance SQL Report services dans laquelle les rapports de conformité et d’audit ont été installés.</span><span class="sxs-lookup"><span data-stu-id="5ade8-312">$SRSINSTANCENAME$ - Enter the name of the SQL Reporting Services instance to which the Compliance and Audit Reports were installed.</span></span>



**<span data-ttu-id="5ade8-313">Reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM</span><span class="sxs-lookup"><span data-stu-id="5ade8-313">Resume All Instances of the MBAM Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="5ade8-314">Sur chaque serveur exécutant la fonctionnalité de serveur d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web MBAM appelé **administration et analyse de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="5ade8-314">On each server that is running the MBAM Administration and Monitoring Server feature, use the Internet Information Services (IIS) Manager console to Start the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="5ade8-315">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-315">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="5ade8-316">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-316">Note</span></span>**  
    <span data-ttu-id="5ade8-317">Pour exécuter cette ligne de commande, vous devez ajouter le module IIS pour PowerShell à l’instance actuelle de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5ade8-317">To run this command line, you must add the IIS Module for PowerShell to current instance of PowerShell.</span></span> <span data-ttu-id="5ade8-318">Par ailleurs, vous devez mettre à jour la stratégie d’exécution PowerShell pour permettre l’exécution de scripts.</span><span class="sxs-lookup"><span data-stu-id="5ade8-318">In addition, you must update the PowerShell execution policy to enable scripts to be run.</span></span>



## <span data-ttu-id="5ade8-319">Déplacement de la fonctionnalité d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="5ade8-319">Moving the Administration and Monitoring Feature</span></span>


<span data-ttu-id="5ade8-320">Si vous voulez déplacer la fonctionnalité rapports d’administration et de surveillance de MBAM d’un ordinateur à un autre (autrement dit, déplacez la fonctionnalité du serveur A vers le serveur B), utilisez la procédure suivante, qui inclut les étapes de niveau supérieur suivantes:</span><span class="sxs-lookup"><span data-stu-id="5ade8-320">If you want to move the MBAM Administration and Monitoring Reports feature from one computer to another (that is, move the feature from Server A to Server B), use the following procedure, which includes the following high-level steps:</span></span>

1.  <span data-ttu-id="5ade8-321">Exécutez le programme d’installation de MBAM sur le serveur B.</span><span class="sxs-lookup"><span data-stu-id="5ade8-321">Run MBAM Setup on Server B.</span></span>

2.  <span data-ttu-id="5ade8-322">Configurer l’accès à la base de données sur le serveur B.</span><span class="sxs-lookup"><span data-stu-id="5ade8-322">Configure access to the Database on Server B.</span></span>

**<span data-ttu-id="5ade8-323">Exécution de la configuration de MBAM sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="5ade8-323">Run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="5ade8-324">Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez uniquement la fonctionnalité d' **administration et de surveillance du serveur** pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="5ade8-324">Run MBAM Setup on Server B and select only the **Administration and Monitoring Server** feature for installation.</span></span>

2.  <span data-ttu-id="5ade8-325">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-325">To automate this procedure, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer, COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$ TOPOLOGY=$X$`

    **<span data-ttu-id="5ade8-326">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-326">Note</span></span>**  
    <span data-ttu-id="5ade8-327">Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-327">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="5ade8-328">$SERVERNAME $ \ \ $SQLINSTANCENAME $-pour le paramètre COMPLIDB \ _SQLINSTANCE, entrez le nom du serveur et l’instance de la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5ade8-328">$SERVERNAME$\\$SQLINSTANCENAME$ - For the COMPLIDB\_SQLINSTANCE parameter, enter the server name and instance where the Compliance and Audit Database is located.</span></span> <span data-ttu-id="5ade8-329">Pour le paramètre RECOVERYANDHWDB \ _SQLINSTANCE, entrez le nom du serveur et l’instance de la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="5ade8-329">For the RECOVERYANDHWDB\_SQLINSTANCE parameter, enter the server name and instance where the Recovery Database is located.</span></span>

    -   <span data-ttu-id="5ade8-330">$DOMAIN $ \ \ $USERNAME $-entrez le domaine et le nom d’utilisateur qui seront utilisés par les rapports de conformité et d’audit pour vous connecter à la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5ade8-330">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit Reports feature to connect to the Compliance and Audit Database.</span></span>

    -   <span data-ttu-id="5ade8-331">$ REPORTSSERVERURL $-entrez l’URL de l’emplacement d’accueil du site Web de service de création de rapports SQL.</span><span class="sxs-lookup"><span data-stu-id="5ade8-331">$ REPORTSSERVERURL$ - Enter the URL for the Home location of the SQL Reporting Service website.</span></span> <span data-ttu-id="5ade8-332">Si les rapports étaient installés sur une instance de SRS par défaut, le format d’URL sera «http://$SERVERNAME $/ReportServer».</span><span class="sxs-lookup"><span data-stu-id="5ade8-332">If the reports were installed to a default SRS instance, the URL format will have the format “http:// $SERVERNAME$/ReportServer”.</span></span> <span data-ttu-id="5ade8-333">Si les rapports étaient installés sur une instance de SRS par défaut, le format d’URL sera le http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $».</span><span class="sxs-lookup"><span data-stu-id="5ade8-333">If the reports were installed to a default SRS instance, the URL format will have the format “http://$SERVERNAME$/ReportServer\_$SQLINSTANCENAME$”.</span></span>

    -   <span data-ttu-id="5ade8-334">$X $-entrez **0** si vous installez la topologie autonome MBAM, ou **1** si vous installez la topologie MBAM Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5ade8-334">$X$ - Enter **0** if you are installing the MBAM Stand-alone topology, or **1** if you are installing the MBAM Configuration Manager topology.</span></span>



**<span data-ttu-id="5ade8-335">Configurer l’accès aux bases de données</span><span class="sxs-lookup"><span data-stu-id="5ade8-335">Configure Access to the Databases</span></span>**

1.  <span data-ttu-id="5ade8-336">Sur le ou les serveurs dans lesquels la base de données de récupération et la base de données d’audit sont déployées, utilisez le composant logiciel enfichable utilisateurs et groupes local dans le gestionnaire de serveur pour ajouter les comptes d’ordinateur de chaque serveur exécutant la fonctionnalité de serveur d' **administration et de** surveillance des MBAM de l’état de **conformité** du serveur.</span><span class="sxs-lookup"><span data-stu-id="5ade8-336">On the server or servers where the Recovery Database and Compliance and Audit Database are deployed, use the Local user and Groups snap-in from Server Manager to add the computer accounts from each server that is running the MBAM Administration and Monitoring Server feature to the local groups named **MBAM Recovery and Hardware DB Access** (Recovery DB Server) and **MBAM Compliance Status DB Access** (Compliance and Audit Database Server).</span></span>

2.  <span data-ttu-id="5ade8-337">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit, sur le serveur sur lequel la base de données d’audit et de conformité a été déployée.</span><span class="sxs-lookup"><span data-stu-id="5ade8-337">To automate this procedure, you can use Windows PowerShell to enter a command line, that is similar to the following, on the server where the Compliance and Audit Database was deployed.</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

3.  <span data-ttu-id="5ade8-338">Sur le serveur sur lequel la base de données de récupération a été déployée, vous pouvez utiliser Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="5ade8-338">On the server where the Recovery database was deployed, you can use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="5ade8-339">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ade8-339">Note</span></span>**  
    <span data-ttu-id="5ade8-340">Remplacez la valeur suivante dans l’exemple ci-dessus avec les valeurs applicables pour votre environnement:</span><span class="sxs-lookup"><span data-stu-id="5ade8-340">Replace the following value in the example above with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="5ade8-341">$DOMAIN $ \ \ $SERVERNAME $ $-entrez le domaine et le nom de l’ordinateur du serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="5ade8-341">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the Administration and Monitoring Server.</span></span> <span data-ttu-id="5ade8-342">Le nom du serveur doit être suivi du symbole «$», comme le montre l’exemple (par exemple, MyDomain\\MyServerName1 $).</span><span class="sxs-lookup"><span data-stu-id="5ade8-342">The server name must be followed by a “$” symbol, as shown in the example (for example, MyDomain\\MyServerName1$).</span></span>

    -   <span data-ttu-id="5ade8-343">$DOMAIN $ \ \ $REPORTSUSERNAME $-entrez le nom du compte d’utilisateur que vous avez utilisé pour configurer la source de données pour les rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="5ade8-343">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit Reports.</span></span>



~~~
The command lines that are listed for adding server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## <span data-ttu-id="5ade8-344">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ade8-344">Related topics</span></span>


[<span data-ttu-id="5ade8-345">Gestion de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="5ade8-345">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)









