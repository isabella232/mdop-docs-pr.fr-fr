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
# <span data-ttu-id="a291e-103">Déplacement de composants MBAM1.0 vers un autre ordinateur</span><span class="sxs-lookup"><span data-stu-id="a291e-103">How to Move MBAM 1.0 Features to Another Computer</span></span>


<span data-ttu-id="a291e-104">Cette rubrique décrit la procédure à suivre pour déplacer une ou plusieurs fonctionnalités d’administration et de surveillance de Microsoft BitLocker (MBAM) vers un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a291e-104">This topic describes the steps that you should take to move one or more Microsoft BitLocker Administration and Monitoring (MBAM) features to a different computer.</span></span> <span data-ttu-id="a291e-105">Lorsque vous déplacez plusieurs fonctionnalités MBAM vers un autre ordinateur, vous devez les déplacer dans l’ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="a291e-105">When you move more than one MBAM feature to another computer, you should move them in the following order:</span></span>

1.  <span data-ttu-id="a291e-106">Base de données de récupération et de matériel</span><span class="sxs-lookup"><span data-stu-id="a291e-106">Recovery and Hardware Database</span></span>

2.  <span data-ttu-id="a291e-107">Base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="a291e-107">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="a291e-108">Rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="a291e-108">Compliance and Audit Reports</span></span>

4.  <span data-ttu-id="a291e-109">Administration et surveillance</span><span class="sxs-lookup"><span data-stu-id="a291e-109">Administration and Monitoring</span></span>

## <span data-ttu-id="a291e-110">Pour déplacer la base de données de récupération et de matériel</span><span class="sxs-lookup"><span data-stu-id="a291e-110">To move the Recovery and Hardware Database</span></span>


<span data-ttu-id="a291e-111">Vous pouvez utiliser la procédure suivante pour déplacer la base de données de récupération MBAM et de base de données matérielle d’un ordinateur vers un autre (vous pouvez déplacer cette fonctionnalité MBAM Server du serveur A vers le serveur B):</span><span class="sxs-lookup"><span data-stu-id="a291e-111">You can use the following procedure to move the MBAM Recovery and Hardware Database from one computer to another (you can move this MBAM Server feature from Server A to Server B):</span></span>

****

1.  <span data-ttu-id="a291e-112">Arrêtez toutes les instances du site Web d’administration et de contrôle MBAM.</span><span class="sxs-lookup"><span data-stu-id="a291e-112">Stop all instances of the MBAM Administration and Monitoring web site.</span></span>

2.  <span data-ttu-id="a291e-113">Exécutez le programme d’installation de MBAM sur le serveur B.</span><span class="sxs-lookup"><span data-stu-id="a291e-113">Run the MBAM Setup on Server B.</span></span>

3.  <span data-ttu-id="a291e-114">Sauvegarder la base de données de récupération MBAM et matérielle sur le serveur A.</span><span class="sxs-lookup"><span data-stu-id="a291e-114">Back up the MBAM Recovery and Hardware database on Server A.</span></span>

4.  <span data-ttu-id="a291e-115">MBAM la base de données matérielle et de récupération du serveur A à B</span><span class="sxs-lookup"><span data-stu-id="a291e-115">MBAM Recovery and Hardware database from Server A to B</span></span>

5.  <span data-ttu-id="a291e-116">Restaurer la base de données matérielle et de récupération MBAM sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-116">Restore the MBAM Recovery and Hardware database on Server B</span></span>

6.  <span data-ttu-id="a291e-117">Configurer l’accès à la MBAM de récupération et de la base de données matérielle du serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-117">Configure the access to the MBAM Recovery and Hardware database on Server B</span></span>

7.  <span data-ttu-id="a291e-118">Mettre à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-118">Update the database connection data on MBAM Administration and Monitoring servers</span></span>

8.  <span data-ttu-id="a291e-119">Reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-119">Resume all instances of the MBAM Administration and Monitoring web site</span></span>

**<span data-ttu-id="a291e-120">Pour arrêter toutes les occurrences du site Web d’administration et de contrôle MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-120">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="a291e-121">Utilisez la console Gestionnaire des services Internet (IIS) pour arrêter le site Web MBAM sur chacun des serveurs exécutant la fonctionnalité d’administration et de surveillance d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="a291e-121">Use the Internet Information Services (IIS) Manager console to stop the MBAM website on each of the servers that run the MBAM Administration and Monitoring feature.</span></span> <span data-ttu-id="a291e-122">Le site Web MBAM est intitulé **administration et analyse Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="a291e-122">The MBAM website is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="a291e-123">Pour automatiser cette procédure, vous pouvez utiliser la commande suivante à l’invite de commandes, qui est semblable à ce qui suit, à l’aide de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a291e-123">To automate this procedure, you can use a command at the command prompt that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="a291e-124">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-124">Note</span></span>**  
    <span data-ttu-id="a291e-125">Pour exécuter l’invite de commandes PowerShell, vous devez ajouter le module IIS pour PowerShell à l’instance actuelle de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a291e-125">To run this PowerShell command prompt, you must add the IIS Module for PowerShell to the current instance of PowerShell.</span></span> <span data-ttu-id="a291e-126">Par ailleurs, vous devez mettre à jour la stratégie d’exécution PowerShell pour permettre l’exécution de scripts.</span><span class="sxs-lookup"><span data-stu-id="a291e-126">In addition, you must update the PowerShell execution policy to enable the execution of scripts.</span></span>



**<span data-ttu-id="a291e-127">Pour exécuter la configuration de MBAM sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-127">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="a291e-128">Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez la base de données de récupération et de matériel pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="a291e-128">Run the MBAM setup on Server B and select the Recovery and Hardware Database for installation.</span></span>

2.  <span data-ttu-id="a291e-129">Pour automatiser cette procédure, vous pouvez utiliser la commande suivante à l’invite de commandes, qui est semblable à ce qui suit, à l’aide de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a291e-129">To automate this procedure, you can use a command at the command prompt that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=KeyDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="a291e-130">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-130">Note</span></span>**  
    <span data-ttu-id="a291e-131">Remplacez les valeurs suivantes dans l’exemple ci-dessus par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-131">Replace the following values in the example above with those that match your environment:</span></span>

    -   <span data-ttu-id="a291e-132">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et de l’instance dans lesquels la base de données de récupération et de matériel seront déplacées.</span><span class="sxs-lookup"><span data-stu-id="a291e-132">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and instance to which the Recovery and Hardware database will be moved.</span></span>

    -   <span data-ttu-id="a291e-133">$DOMAIN $ \ \ $SERVERNAME $-entrez les noms de domaine et de serveur de chaque application MBAM et serveur de surveillance qui contactera la base de données de récupération et de matériel.</span><span class="sxs-lookup"><span data-stu-id="a291e-133">$DOMAIN$\\$SERVERNAME$ - Enter the domain and server names of each MBAM Application and Monitoring Server that will contact the Recovery and Hardware database.</span></span> <span data-ttu-id="a291e-134">S’il existe plusieurs noms de domaine et de serveur, séparez-les par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="a291e-134">If there are multiple domain and server names, use a semicolon to separate each one of them in the list.</span></span> <span data-ttu-id="a291e-135">Par exemple, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $.</span><span class="sxs-lookup"><span data-stu-id="a291e-135">For example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$.</span></span> <span data-ttu-id="a291e-136">Par ailleurs, chaque nom de serveur doit être suivi de a **$** .</span><span class="sxs-lookup"><span data-stu-id="a291e-136">Additionally, each server name must be followed by a **$**.</span></span> <span data-ttu-id="a291e-137">Par exemple, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.</span><span class="sxs-lookup"><span data-stu-id="a291e-137">For example, MyDomain\\MyServerName1$, MyDomain\\MyServerName2$.</span></span>



**<span data-ttu-id="a291e-138">Pour sauvegarder la base de données sur le serveur A</span><span class="sxs-lookup"><span data-stu-id="a291e-138">To back up the Database on Server A</span></span>**

1.  <span data-ttu-id="a291e-139">Pour sauvegarder la base de données de récupération et de matériel du serveur A, utilisez SQL Server Management Studio et la tâche nommée **sauvegarder...**.</span><span class="sxs-lookup"><span data-stu-id="a291e-139">To back up the Recovery and Hardware database on Server A, use SQL Server Management Studio and the Task named **Back Up…**.</span></span> <span data-ttu-id="a291e-140">Par défaut, le nom de la base de données est **MBAM récupération et la base de données matérielle**.</span><span class="sxs-lookup"><span data-stu-id="a291e-140">By default, the database name is **MBAM Recovery and Hardware Database**.</span></span>

2.  <span data-ttu-id="a291e-141">Pour automatiser cette procédure, créez un fichier SQL (. Sql) contenant le script SQL suivant:</span><span class="sxs-lookup"><span data-stu-id="a291e-141">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    <span data-ttu-id="a291e-142">Modifiez la base de données de récupération et de matériel MBAM pour utiliser le mode de récupération complet.</span><span class="sxs-lookup"><span data-stu-id="a291e-142">Modify the MBAM Recovery and Hardware Database to use the full recovery mode.</span></span>

    ```sql
    USE master;

    GO

    ALTER DATABASE "MBAM Recovery and Hardware"

       SET RECOVERY FULL;

    GO
    ```

    <span data-ttu-id="a291e-143">Créez des MBAM de données de la base de données matérielle et de récupération des informations et MBAM de sauvegarde logique de restauration.</span><span class="sxs-lookup"><span data-stu-id="a291e-143">Create MBAM Recovery and Hardware Database Data and MBAM Recovery logical backup devices.</span></span>

    ```sql
    USE master

    GO

    EXEC sp_addumpdevice 'disk', 'MBAM Recovery and Hardware Database Data Device',

    'Z:\MBAM Recovery and Hardware Database Data.bak';

    GO
    ```

    <span data-ttu-id="a291e-144">Sauvegardez l’intégralité de la base de données MBAM et de récupération du matériel.</span><span class="sxs-lookup"><span data-stu-id="a291e-144">Back up the full MBAM Recovery and Hardware database.</span></span>

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

    **<span data-ttu-id="a291e-145">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-145">Note</span></span>**  
    <span data-ttu-id="a291e-146">Remplacez les valeurs de l’exemple précédent par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-146">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="a291e-147">$PASSWORD $-entrez le mot de passe que vous allez utiliser pour chiffrer le fichier de clé privée.</span><span class="sxs-lookup"><span data-stu-id="a291e-147">$PASSWORD$ - Enter a password that you will use to encrypt the Private Key file.</span></span>



3.  <span data-ttu-id="a291e-148">Exécutez le fichier SQL en utilisant SQL Server PowerShell et une commande similaire à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="a291e-148">Execute the SQL file by using SQL Server PowerShell and a command that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\BackupMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="a291e-149">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-149">Note</span></span>**  
    <span data-ttu-id="a291e-150">Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-150">Replace the value in the previous example with those that match your environment:</span></span>

    -   <span data-ttu-id="a291e-151">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance à partir de laquelle vous sauvegardez la base de données de récupération et de matériel.</span><span class="sxs-lookup"><span data-stu-id="a291e-151">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and the instance from which you back up the Recovery and Hardware database.</span></span>



**<span data-ttu-id="a291e-152">Pour déplacer la base de données et le certificat du serveur A vers B</span><span class="sxs-lookup"><span data-stu-id="a291e-152">To move the Database and Certificate from Server A to B</span></span>**

1.  <span data-ttu-id="a291e-153">Déplacez les données de la base de données de récupération et de MBAM du matériel du serveur A vers le serveur B à l’aide de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="a291e-153">Move the MBAM Recovery and Hardware database data.bak from Server A to Server B by using Windows Explorer.</span></span>

2.  <span data-ttu-id="a291e-154">Pour déplacer le certificat de la base de données chiffrée, vous devez utiliser les étapes d’Automation suivantes.</span><span class="sxs-lookup"><span data-stu-id="a291e-154">To move the certificate for the encrypted database, you will need to use the following automation steps.</span></span> <span data-ttu-id="a291e-155">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="a291e-155">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Recovery and Hardware Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFile” \\$SERVERNAME$\$DESTINATIONSHARE$`

    `PS C:\> Copy-Item “Z:\SQLServerInstanceCertificateFilePrivateKey” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="a291e-156">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-156">Note</span></span>**  
    <span data-ttu-id="a291e-157">Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-157">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="a291e-158">$SERVERNAME $-entrez le nom du serveur sur lequel les fichiers sont copiés.</span><span class="sxs-lookup"><span data-stu-id="a291e-158">$SERVERNAME$ - Enter the name of the server to which the files will be copied.</span></span>

    -   <span data-ttu-id="a291e-159">$DESTINATIONSHARE $-entrez le nom du partage et du chemin d’accès dans lesquels les fichiers seront copiés.</span><span class="sxs-lookup"><span data-stu-id="a291e-159">$DESTINATIONSHARE$ - Enter the name of the share and path to which the files will be copied.</span></span>



**<span data-ttu-id="a291e-160">Pour restaurer la base de données sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-160">To restore the Database on Server B</span></span>**

1.  <span data-ttu-id="a291e-161">Restaurez la base de données de récupération et de matériel sur le serveur B en utilisant SQL Server Management Studio et la tâche nommée **restaurer la base de données**.</span><span class="sxs-lookup"><span data-stu-id="a291e-161">Restore the Recovery and Hardware database on Server B by using the SQL Server Management Studio and the Task named **Restore Database**.</span></span>

2.  <span data-ttu-id="a291e-162">Après l’exécution de la tâche, sélectionnez le fichier de sauvegarde de la base de données en sélectionnant l’option **à partir de l’appareil** , puis utilisez la commande **Ajouter** pour choisir le fichier de données de la base de données MBAM et de la base de données du matériel **.**</span><span class="sxs-lookup"><span data-stu-id="a291e-162">Once the task has been executed, choose the database backup file by selecting the **From Device** option, and then use the **Add** command to choose the MBAM Recovery and Hardware database **Data.bak** file.</span></span>

3.  <span data-ttu-id="a291e-163">Sélectionnez **OK** pour terminer le processus de restauration.</span><span class="sxs-lookup"><span data-stu-id="a291e-163">Select **OK** to complete the restoration process.</span></span>

4.  <span data-ttu-id="a291e-164">Pour automatiser cette procédure, créez un fichier SQL (. Sql) contenant le script SQL suivant:</span><span class="sxs-lookup"><span data-stu-id="a291e-164">To automate this procedure, create a SQL file (.sql) that contains the following SQL script:</span></span>

    ```sql
    -- Restore MBAM Recovery and Hardware Database. 

    USE master

    GO
    ```

    <span data-ttu-id="a291e-165">Supprimez le certificat créé par MBAM Setup.</span><span class="sxs-lookup"><span data-stu-id="a291e-165">Drop the certificate created by MBAM Setup.</span></span>

    ```sql
    DROP CERTIFICATE [MBAM Recovery Encryption Certificate]

    GO
    ```

    <span data-ttu-id="a291e-166">Ajouter un certificat</span><span class="sxs-lookup"><span data-stu-id="a291e-166">Add certificate</span></span>

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

    <span data-ttu-id="a291e-167">Restaurez les données de base de données matérielle et de récupération MBAM et les fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="a291e-167">Restore the MBAM Recovery and Hardware database data and the log files.</span></span>

    ```sql
    RESTORE DATABASE [MBAM Recovery and Hardware]

       FROM DISK = 'Z:\MBAM Recovery and Hardware Database Data.bak'

       WITH REPLACE
    ```

    **<span data-ttu-id="a291e-168">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-168">Note</span></span>**  
    <span data-ttu-id="a291e-169">Remplacez les valeurs de l’exemple précédent par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-169">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="a291e-170">$PASSWORD $-entrez le mot de passe que vous avez utilisé pour chiffrer le fichier de clé privée.</span><span class="sxs-lookup"><span data-stu-id="a291e-170">$PASSWORD$ - Enter the password that you used to encrypt the Private Key file.</span></span>



5.  <span data-ttu-id="a291e-171">Utilisez Windows PowerShell pour entrer une ligne de commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="a291e-171">Use Windows PowerShell to enter a command line that is similar to the following:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile 'Z:\RestoreMBAMRecoveryandHardwarDatabaseScript.sql' -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="a291e-172">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-172">Note</span></span>**  
    <span data-ttu-id="a291e-173">Remplacez la valeur de l’exemple de passe par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-173">Replace the value from the receding example with those that match your environment:</span></span>

    -   <span data-ttu-id="a291e-174">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance vers laquelle la base de données de récupération et de matériel sera restaurée.</span><span class="sxs-lookup"><span data-stu-id="a291e-174">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the name of the server and the instance to which the Recovery and Hardware Database will be restored.</span></span>



**<span data-ttu-id="a291e-175">Configurer l’accès à la base de données sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-175">Configure the access to the Database on Server B</span></span>**

1.  <span data-ttu-id="a291e-176">Sur le serveur B, utilisez le composant logiciel enfichable utilisateurs et groupes local dans le gestionnaire de serveur pour ajouter les comptes d’ordinateur de chaque serveur qui exécute la fonctionnalité d’administration et de surveillance MBAM au groupe local intitulé **MBAM de récupération et de BDD matériel**.</span><span class="sxs-lookup"><span data-stu-id="a291e-176">On Server B, use the Local user and Groups snap-in from Server Manager, to add the computer accounts from each server that runs the MBAM Administration and Monitoring feature to the Local Group named **MBAM Recovery and Hardware DB Access**.</span></span>

2.  <span data-ttu-id="a291e-177">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell sur le serveur B pour entrer une commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="a291e-177">To automate this procedure, you can use Windows PowerShell on Server B to enter a command that is similar to the following:</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="a291e-178">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-178">Note</span></span>**  
    <span data-ttu-id="a291e-179">Remplacez les valeurs de l’exemple précédent par les valeurs applicables pour votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-179">Replace the values from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="a291e-180">$DOMAIN $ \ \ $SERVERNAME $ $-entrez le nom de domaine et le nom de l’ordinateur du serveur d’administration et de surveillance MBAM.</span><span class="sxs-lookup"><span data-stu-id="a291e-180">$DOMAIN$\\$SERVERNAME$$ - Enter the domain name and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="a291e-181">Le nom du serveur doit être suivi d’un **$** (par exemple, MyDomain\\MyServerName1 $).</span><span class="sxs-lookup"><span data-stu-id="a291e-181">The server name must be followed by a **$**, for example, MyDomain\\MyServerName1$.</span></span>



~~~
You must run the command for each Administration and Monitoring Server that will be accessing the database in your environment.
~~~

**<span data-ttu-id="a291e-182">Pour mettre à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-182">To update the Database Connection data on MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="a291e-183">Sur chacun des serveurs qui exécutent la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour les informations de la chaîne de connexion pour les applications suivantes qui sont hébergées dans le site Web d’administration et de contrôle de Microsoft BitLocker:</span><span class="sxs-lookup"><span data-stu-id="a291e-183">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following applications, which are hosted in the Microsoft BitLocker Administration and Monitoring website:</span></span>

   -   <span data-ttu-id="a291e-184">Service d’administration MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-184">MBAM Administration Service</span></span>

   -   <span data-ttu-id="a291e-185">Services de récupération et de matériel de MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-185">MBAM Recovery And Hardware Service</span></span>

2. <span data-ttu-id="a291e-186">Sélectionner chaque application et utiliser la fonctionnalité **éditeur de configuration** , située sous la section **gestion** de l’affichage des **fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="a291e-186">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="a291e-187">Sélectionnez l’option **configurationStrings** dans le contrôle de liste de sections.</span><span class="sxs-lookup"><span data-stu-id="a291e-187">Select the **configurationStrings** option from the Section list control.</span></span>

4. <span data-ttu-id="a291e-188">Sélectionnez la ligne nommée **(collection)**, puis ouvrez l' **éditeur de collection** en sélectionnant le bouton à droite de la ligne.</span><span class="sxs-lookup"><span data-stu-id="a291e-188">Choose the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="a291e-189">Dans l' **éditeur de collection**, sélectionnez la ligne nommée **KeyRecoveryConnectionString** lorsque vous avez mis à jour la configuration de l’application «MBAMAdministrationService», ou sélectionnez la ligne nommée <strong> Microsoft. mbam. RecoveryAndHardwareDataStore. </strong> ChaîneConnexion, lors de la mise à jour de la configuration pour «MBAMRecoveryAndHardwareService».</span><span class="sxs-lookup"><span data-stu-id="a291e-189">In the **Collection Editor**, choose the row named **KeyRecoveryConnectionString** when you updated the configuration for the ‘MBAMAdministrationService’ application, or choose the row named <strong>Microsoft.Mbam.RecoveryAndHardwareDataStore.</strong>ConnectionString, when updating the configuration for the ‘MBAMRecoveryAndHardwareService’.</span></span>

6. <span data-ttu-id="a291e-190">Mettez à jour la **source de données =** valeur pour la propriété **configurationStrings** pour indiquer le nom du serveur et l’instance vers laquelle la base de données de récupération et de matériel a été déplacée.</span><span class="sxs-lookup"><span data-stu-id="a291e-190">Update the **Data Source=** value for the **configurationStrings** property to list the server name and the instance where the Recovery and Hardware Database was moved to.</span></span> <span data-ttu-id="a291e-191">Par exemple, $SERVERNAME $ \ \ $SQLINSTANCENAME $.</span><span class="sxs-lookup"><span data-stu-id="a291e-191">For example, $SERVERNAME$\\$SQLINSTANCENAME$.</span></span>

7. <span data-ttu-id="a291e-192">Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, en utilisant Windows PowerShell sur chaque serveur d’administration et de surveillance:</span><span class="sxs-lookup"><span data-stu-id="a291e-192">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="KeyRecoveryConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value “Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;”`

   `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Mbam.RecoveryAndHardwareDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMRecoveryAndHardwareService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Recovery and Hardware;Integrated Security=SSPI;"`

   **<span data-ttu-id="a291e-193">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-193">Note</span></span>**  
   <span data-ttu-id="a291e-194">Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-194">Replace the value from the preceding example with those that match your environment:</span></span>

   -   <span data-ttu-id="a291e-195">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance de la base de données de récupération et de matériel.</span><span class="sxs-lookup"><span data-stu-id="a291e-195">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Recovery and Hardware database is.</span></span>



**<span data-ttu-id="a291e-196">Pour reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-196">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="a291e-197">Sur chacun des serveurs qui exécutent la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web MBAM, intitulé **administration et analyse de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="a291e-197">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Start the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="a291e-198">Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, à l’aide de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a291e-198">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

## <span data-ttu-id="a291e-199">Pour déplacer la fonctionnalité de base de données état de conformité</span><span class="sxs-lookup"><span data-stu-id="a291e-199">To move the Compliance Status Database feature</span></span>


<span data-ttu-id="a291e-200">Si vous choisissez de déplacer la fonctionnalité de base de données état de conformité d’MBAM d’un ordinateur vers un autre, par exemple du serveur A vers le serveur B, utilisez la procédure suivante:</span><span class="sxs-lookup"><span data-stu-id="a291e-200">If you choose to move the MBAM Compliance Status Database feature from one computer to another, such as from Server A to Server B, you should use the following procedure:</span></span>

1.  <span data-ttu-id="a291e-201">Arrêter toutes les instances de MBAM site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="a291e-201">Stop all instances of the MBAM Administration and Monitoring website</span></span>

2.  <span data-ttu-id="a291e-202">Exécution de la configuration de MBAM sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-202">Run MBAM setup on Server B</span></span>

3.  <span data-ttu-id="a291e-203">Sauvegarder la base de données sur le serveur A</span><span class="sxs-lookup"><span data-stu-id="a291e-203">Backup the Database on Server A</span></span>

4.  <span data-ttu-id="a291e-204">Déplacer la base de données du serveur A vers B</span><span class="sxs-lookup"><span data-stu-id="a291e-204">Move the Database from Server A to B</span></span>

5.  <span data-ttu-id="a291e-205">Restaurer la base de données sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-205">Restore the Database on Server B</span></span>

6.  <span data-ttu-id="a291e-206">Configurer l’accès à la base de données sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-206">Configure Access to the Database on Server B</span></span>

7.  <span data-ttu-id="a291e-207">Mettre à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-207">Update database connection data on MBAM Administration and Monitoring servers</span></span>

8.  <span data-ttu-id="a291e-208">Reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-208">Resume all instances of the MBAM Administration and Monitoring website</span></span>

**<span data-ttu-id="a291e-209">Pour arrêter toutes les occurrences du site Web d’administration et de contrôle MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-209">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="a291e-210">Sur chacun des serveurs qui exécutent la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour arrêter le site Web MBAM, intitulé **administration et analyse de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="a291e-210">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Stop the MBAM website, which is named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="a291e-211">Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, à l’aide de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a291e-211">To automate this procedure, you can use a command that is similar to the following one,by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="a291e-212">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-212">Note</span></span>**  
    <span data-ttu-id="a291e-213">Pour exécuter cette commande, vous devez ajouter le module IIS pour PowerShell à l’instance actuelle de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a291e-213">To execute this command, you must add the IIS Module for PowerShell to current instance of PowerShell.</span></span> <span data-ttu-id="a291e-214">Par ailleurs, vous devez mettre à jour la stratégie d’exécution PowerShell pour permettre l’exécution de scripts.</span><span class="sxs-lookup"><span data-stu-id="a291e-214">In addition, you must update the PowerShell execution policy to enable the execution of scripts.</span></span>



**<span data-ttu-id="a291e-215">Pour exécuter la configuration de MBAM sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-215">To run MBAM Setup on Server B</span></span>**

1.  <span data-ttu-id="a291e-216">Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez la fonctionnalité de base de données état de conformité pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="a291e-216">Run MBAM Setup on Server B and select the Compliance Status Database feature for installation.</span></span>

2.  <span data-ttu-id="a291e-217">Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, à l’aide de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a291e-217">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal= ReportsDatabase ADMINANDMON_MACHINENAMES=$DOMAIN$\$SERVERNAME$ COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNT=$DOMAIN$\$USERNAME$`

    **<span data-ttu-id="a291e-218">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-218">Note</span></span>**  
    <span data-ttu-id="a291e-219">Remplacez les valeurs de l’exemple précédent par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-219">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="a291e-220">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance de destination de la base de données d’état de conformité.</span><span class="sxs-lookup"><span data-stu-id="a291e-220">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database will be moved to.</span></span>

    -   <span data-ttu-id="a291e-221">$DOMAIN $ \ \ $SERVERNAME $-entrez les noms de domaine et les noms de serveurs de chaque application MBAM et serveur de surveillance qui contactera la base de données d’état de conformité.</span><span class="sxs-lookup"><span data-stu-id="a291e-221">$DOMAIN$\\$SERVERNAME$ - Enter the domain names and server names of each MBAM Application and Monitoring Server that will contact the Compliance Status Database.</span></span> <span data-ttu-id="a291e-222">S’il existe plusieurs noms de domaine et noms de serveurs, utilisez un point-virgule pour séparer chacun d’eux dans la liste.</span><span class="sxs-lookup"><span data-stu-id="a291e-222">If there are multiple domain names and server names, use a semicolon to separate each one of them in the list.</span></span> <span data-ttu-id="a291e-223">Par exemple, $DOMAIN \\SERVERNAME $; $DOMAIN \ \ $SERVERNAME $ $.</span><span class="sxs-lookup"><span data-stu-id="a291e-223">For example, $DOMAIN\\SERVERNAME$;$DOMAIN\\$SERVERNAME$$.</span></span> <span data-ttu-id="a291e-224">Le nom de chaque serveur doit être suivi de a **$** comme illustré dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="a291e-224">Each server name must be followed by a **$** as shown in the example.</span></span> <span data-ttu-id="a291e-225">Par exemple, MyDomain\\MyServerName1 $, MyDomain\\MyServerName2 $.</span><span class="sxs-lookup"><span data-stu-id="a291e-225">For example, MyDomain\\MyServerName1$, MyDomain\\MyServerName2$.</span></span>

    -   <span data-ttu-id="a291e-226">$DOMAIN $ \ \ $USERNAME $-entrez le domaine et le nom d’utilisateur qui seront utilisés par les rapports de conformité et d’audit pour vous connecter à la base de données état de conformité.</span><span class="sxs-lookup"><span data-stu-id="a291e-226">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>



**<span data-ttu-id="a291e-227">Pour sauvegarder la base de données de conformité du serveur A</span><span class="sxs-lookup"><span data-stu-id="a291e-227">To back up the Compliance Database on Server A</span></span>**

1.  <span data-ttu-id="a291e-228">Pour sauvegarder la base de données de conformité du serveur A, utilisez SQL Server Management Studio et la tâche nommée **sauvegarder...**.</span><span class="sxs-lookup"><span data-stu-id="a291e-228">To back up the Compliance Database on Server A, use SQL Server Management Studio and the Task named **Back Up…**.</span></span> <span data-ttu-id="a291e-229">Par défaut, le nom de la base de données est **MBAM de la base de données état de conformité**.</span><span class="sxs-lookup"><span data-stu-id="a291e-229">By default, the database name is **MBAM Compliance Status Database**.</span></span>

2.  <span data-ttu-id="a291e-230">Pour automatiser cette procédure, créez un fichier SQL (. Sql) qui contient le script SQL suivant:</span><span class="sxs-lookup"><span data-stu-id="a291e-230">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

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

3.  <span data-ttu-id="a291e-231">Exécutez le fichier SQL avec une commande similaire à celle qui suit, en utilisant SQL Server PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a291e-231">Run the SQL file with a command that is similar to the following one, by using the SQL Server PowerShell:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\BackupMBAMComplianceStatusDatabaseScript.sql" –ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="a291e-232">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-232">Note</span></span>**  
    <span data-ttu-id="a291e-233">Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-233">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="a291e-234">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance à partir de laquelle la base de données d’état de conformité sera sauvegardée.</span><span class="sxs-lookup"><span data-stu-id="a291e-234">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and the instance from where the Compliance Status database will be backed up.</span></span>



**<span data-ttu-id="a291e-235">Pour déplacer la base de données du serveur A vers B</span><span class="sxs-lookup"><span data-stu-id="a291e-235">To move the Database from Server A to B</span></span>**

1.  <span data-ttu-id="a291e-236">Dans l’Explorateur Windows, déplacez les fichiers suivants du serveur A vers le serveur B:</span><span class="sxs-lookup"><span data-stu-id="a291e-236">Move the following files from Server A to Server B, by using Windows Explorer:</span></span>

    -   <span data-ttu-id="a291e-237">Données de la base de données d’état de conformité MBAM. bak</span><span class="sxs-lookup"><span data-stu-id="a291e-237">MBAM Compliance Status Database Data.bak</span></span>

2.  <span data-ttu-id="a291e-238">Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit dans Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a291e-238">To automate this procedure, you can use a command that is similar to the following using Windows PowerShell:</span></span>

    `PS C:\> Copy-Item “Z:\MBAM Compliance Status Database Data.bak” \\$SERVERNAME$\$DESTINATIONSHARE$`

    **<span data-ttu-id="a291e-239">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-239">Note</span></span>**  
    <span data-ttu-id="a291e-240">Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-240">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="a291e-241">$SERVERNAME $-entrez le nom du serveur dans lequel les fichiers sont copiés.</span><span class="sxs-lookup"><span data-stu-id="a291e-241">$SERVERNAME$ - Enter the server name where the files will be copied to.</span></span>

    -   <span data-ttu-id="a291e-242">$DESTINATIONSHARE $-entrez le nom du partage dans lequel les fichiers sont copiés.</span><span class="sxs-lookup"><span data-stu-id="a291e-242">$DESTINATIONSHARE$ - Enter the name of share and path where the files will be copied to.</span></span>



**<span data-ttu-id="a291e-243">Pour restaurer la base de données sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-243">To restore the Database on Server B</span></span>**

1.  <span data-ttu-id="a291e-244">Restaurez la base de données d’état de conformité sur le serveur B en utilisant SQL Server Management Studio et la tâche nommée **restaurer la base de données...**.</span><span class="sxs-lookup"><span data-stu-id="a291e-244">Restore the Compliance Status database on Server B by using SQL Server Management Studio and the Task named **Restore Database…**.</span></span>

2.  <span data-ttu-id="a291e-245">Après l’exécution de la tâche, sélectionnez le fichier de sauvegarde de la base de données en sélectionnant l’option à partir de l’appareil, puis utilisez la commande Ajouter pour choisir le fichier de données de la base de données d’état de compatibilité MBAM. bak.</span><span class="sxs-lookup"><span data-stu-id="a291e-245">Once the task is executed, select the database backup file, by selecting the From Device option, and then use the Add command to choose the MBAM Compliance Status Database Data.bak file.</span></span> <span data-ttu-id="a291e-246">Cliquez sur OK pour terminer le processus de restauration.</span><span class="sxs-lookup"><span data-stu-id="a291e-246">Click OK to complete the restoration process.</span></span>

3.  <span data-ttu-id="a291e-247">Pour automatiser cette procédure, créez un fichier SQL (. Sql) qui contient le script SQL suivant:</span><span class="sxs-lookup"><span data-stu-id="a291e-247">To automate this procedure, create a SQL file (.sql) that contains the following-SQL script:</span></span>

    ```sql
    -- Create MBAM Compliance Status Database Data logical backup devices. 

    Use master

    GO

    -- Restore the MBAM Compliance Status database data files.

    RESTORE DATABASE [MBAM Compliance Status Database]

       FROM DISK = 'C:\test\MBAM Compliance Status Database Data.bak'

       WITH REPLACE
    ```

4.  <span data-ttu-id="a291e-248">Exécutez le fichier SQL avec une commande similaire à celle qui suit, en utilisant SQL Server PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a291e-248">Run the SQL File with a command that is similar to the following one, by using the SQL Server PowerShell:</span></span>

    `PS C:\> Invoke-Sqlcmd -InputFile "Z:\RestoreMBAMComplianceStatusDatabaseScript.sql" -ServerInstance $SERVERNAME$\$SQLINSTANCENAME$`

    **<span data-ttu-id="a291e-249">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-249">Note</span></span>**  
    <span data-ttu-id="a291e-250">Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-250">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="a291e-251">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance où la base de données d’état de conformité sera restaurée.</span><span class="sxs-lookup"><span data-stu-id="a291e-251">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database will be restored to.</span></span>



**<span data-ttu-id="a291e-252">Pour configurer l’accès à la base de données sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-252">To configure the Access to the Database on Server B</span></span>**

1.  <span data-ttu-id="a291e-253">Sur le serveur B, utilisez le composant logiciel enfichable utilisateurs et groupes local dans le gestionnaire de serveur pour ajouter les comptes d’ordinateur de chaque serveur qui exécute la fonctionnalité d’administration et de surveillance de MBAM dans le groupe local intitulé MBAM de la **BD état de conformité**.</span><span class="sxs-lookup"><span data-stu-id="a291e-253">On Server B use the Local user and Groups snap-in from Server Manager to add the machine accounts from each server that runs the MBAM Administration and Monitoring feature to the Local Group named **MBAM Compliance Status DB Access**.</span></span>

2.  <span data-ttu-id="a291e-254">Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, en utilisant Windows PowerShell sur le serveur B:</span><span class="sxs-lookup"><span data-stu-id="a291e-254">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on Server B:</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="a291e-255">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-255">Note</span></span>**  
    <span data-ttu-id="a291e-256">Remplacez la valeur de l’exemple précédent par les valeurs applicables pour votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-256">Replace the value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="a291e-257">$DOMAIN $ \ \ $SERVERNAME $ $-entrez le domaine et le nom de l’ordinateur du serveur d’administration et de surveillance MBAM.</span><span class="sxs-lookup"><span data-stu-id="a291e-257">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="a291e-258">Le nom du serveur doit être suivi de a **$** . Par exemple, MyDomain\\MyServerName1 $.</span><span class="sxs-lookup"><span data-stu-id="a291e-258">The server name must be followed by a **$**.For example, MyDomain\\MyServerName1$.</span></span>

    -   <span data-ttu-id="a291e-259">$DOMAIN $ \ \ $REPORTSUSERNAME $-entrez le nom du compte d’utilisateur que vous avez utilisé pour configurer la source de données pour les rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="a291e-259">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports</span></span>



~~~
For each Administration and Monitoring Server that will access the database of your environment, you must run the command that will add the servers to the MBAM Compliance Auditing DB Access local group.
~~~

**<span data-ttu-id="a291e-260">Pour mettre à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-260">To update the database connection data on MBAM Administration and Monitoring servers</span></span>**

1.  <span data-ttu-id="a291e-261">Sur chacun des serveurs qui exécutent la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour les informations de la chaîne de connexion pour les applications suivantes qui sont hébergées dans le site Web d’administration et de contrôle de Microsoft BitLocker:</span><span class="sxs-lookup"><span data-stu-id="a291e-261">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to update the Connection String information for the following Applications, which are hosted in the Microsoft BitLocker Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="a291e-262">MBAMAdministrationService</span><span class="sxs-lookup"><span data-stu-id="a291e-262">MBAMAdministrationService</span></span>

    -   <span data-ttu-id="a291e-263">MBAMComplianceStatusService</span><span class="sxs-lookup"><span data-stu-id="a291e-263">MBAMComplianceStatusService</span></span>

2.  <span data-ttu-id="a291e-264">Sélectionner chaque application et utiliser la fonctionnalité **éditeur de configuration** , située sous la section **gestion** de l’affichage des **fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="a291e-264">Select each application and use the **Configuration Editor** feature, which is located under the **Management** section of the **Feature View**.</span></span>

3.  <span data-ttu-id="a291e-265">Sélectionnez l’option **configurationStrings** dans le contrôle de liste de sections.</span><span class="sxs-lookup"><span data-stu-id="a291e-265">Select the **configurationStrings** option from the Section list control.</span></span>

4.  <span data-ttu-id="a291e-266">Sélectionnez la ligne nommée **(collection)**, puis ouvrez l’éditeur de collection en sélectionnant le bouton à droite de la ligne.</span><span class="sxs-lookup"><span data-stu-id="a291e-266">Select the row named **(Collection)**, and open the Collection Editor by selecting the button on the right side of the row.</span></span>

5.  <span data-ttu-id="a291e-267">Dans l' **éditeur de collection**, sélectionnez la ligne nommée **ComplianceStatusConnectionString**, lorsque vous mettez à jour la configuration de l’application MBAMAdministrationService, ou la ligne nommée **Microsoft. Windows. MDOP. BitLockerManagement. StatusReportDataStore. ConnectionString**, lorsque vous mettez à jour la configuration pour le MBAMComplianceStatusService.</span><span class="sxs-lookup"><span data-stu-id="a291e-267">In the **Collection Editor**, select the row named **ComplianceStatusConnectionString**, when you update the configuration for the MBAMAdministrationService application, or the row named **Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString**, when you update the configuration for the MBAMComplianceStatusService.</span></span>

6.  <span data-ttu-id="a291e-268">Mettez à jour la **source de données =** valeur pour la propriété **configurationStrings** pour afficher le nom du serveur et le nom de l’instance.</span><span class="sxs-lookup"><span data-stu-id="a291e-268">Update the **Data Source=** value for the **configurationStrings** property to list the server name and the instance name.</span></span> <span data-ttu-id="a291e-269">Par exemple, $SERVERNAME $ \ \ $SQLINSTANCENAME, sur lequel la base de données de récupération et de matériel a été déplacée.</span><span class="sxs-lookup"><span data-stu-id="a291e-269">For example, $SERVERNAME$\\$SQLINSTANCENAME, to which the Recovery and Hardware Database was moved.</span></span>

7.  <span data-ttu-id="a291e-270">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une commande similaire à celle qui suit dans chaque serveur d’administration et de surveillance:</span><span class="sxs-lookup"><span data-stu-id="a291e-270">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following one on each Administration and Monitoring Server:</span></span>

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="ComplianceStatusConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMAdministrationService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME$;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    `PS C:\> Set-WebConfigurationProperty '/connectionStrings/add[@name="Microsoft.Windows.Mdop.BitLockerManagement.StatusReportDataStore.ConnectionString"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring\MBAMComplianceStatusService" -Name "connectionString" -Value "Data Source=$SERVERNAME$\$SQLINSTANCENAME;Initial Catalog=MBAM Compliance Status;Integrated Security=SSPI;"`

    **<span data-ttu-id="a291e-271">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-271">Note</span></span>**  
    <span data-ttu-id="a291e-272">Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-272">Replace the value from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="a291e-273">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et le nom de l’instance où se trouve la base de données de récupération et de matériel.</span><span class="sxs-lookup"><span data-stu-id="a291e-273">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance name where the Recovery and Hardware Database is located.</span></span>



**<span data-ttu-id="a291e-274">Pour reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-274">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="a291e-275">Sur chacun des serveurs exécutant la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web MBAM appelé **administration et analyse Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="a291e-275">On each of the servers running the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to start the MBAM web site named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="a291e-276">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="a291e-276">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    **<span data-ttu-id="a291e-277">PS C:\\ &gt; Start-site Web «Administration et surveillance de Microsoft BitLocker»</span><span class="sxs-lookup"><span data-stu-id="a291e-277">PS C:\\&gt; Start-Website “Microsoft BitLocker Administration and Monitoring”</span></span>**

## <span data-ttu-id="a291e-278">Pour déplacer les rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="a291e-278">To moving the Compliance and Audit Reports</span></span>


<span data-ttu-id="a291e-279">Si vous choisissez de déplacer les rapports de conformité et d’audit MBAM d’un ordinateur à un autre (en particulier, si vous déplacez la fonctionnalité du serveur A vers le serveur B), vous devez utiliser la procédure et les étapes suivantes:</span><span class="sxs-lookup"><span data-stu-id="a291e-279">If you choose to move the MBAM Compliance and Audit Reports from one computer to another (specifically, if you move feature from Server A to Server B), you should use the following procedure and steps:</span></span>

1.  <span data-ttu-id="a291e-280">Exécution de la configuration de MBAM sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-280">Run MBAM setup on Server B</span></span>

2.  <span data-ttu-id="a291e-281">Configurer l’accès aux rapports de conformité et d’audit sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-281">Configure Access to the Compliance and Audit Reports on Server B</span></span>

3.  <span data-ttu-id="a291e-282">Arrêter toutes les instances de MBAM site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="a291e-282">Stop all instances of the MBAM Administration and Monitoring website</span></span>

4.  <span data-ttu-id="a291e-283">Mettre à jour les données de connexion aux rapports sur les serveurs d’administration et de surveillance MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-283">Update the reports connection data on MBAM Administration and Monitoring servers</span></span>

5.  <span data-ttu-id="a291e-284">Reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-284">Resume all instances of the MBAM Administration and Monitoring website</span></span>

**<span data-ttu-id="a291e-285">Pour exécuter la configuration de MBAM sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-285">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="a291e-286">Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez uniquement la fonctionnalité conformité et audit pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="a291e-286">Run MBAM setup on Server B and only select the Compliance and Audit feature for installation.</span></span>

2.  <span data-ttu-id="a291e-287">Pour automatiser cette procédure, vous pouvez utiliser une commande semblable à la suivante, à l’aide de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a291e-287">To automate this procedure, you can use a command that is similar to the following, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=Reports COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ REPORTS_USERACCOUNTPW=$PASSWORD$`

    **<span data-ttu-id="a291e-288">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-288">Note</span></span>**  
    <span data-ttu-id="a291e-289">Remplacez les valeurs de l’exemple précédent par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-289">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="a291e-290">$SERVERNAME $ \ \ $SQLINSTANCENAME $-entrez le nom du serveur et l’instance d’emplacement de la base de données d’état de conformité.</span><span class="sxs-lookup"><span data-stu-id="a291e-290">$SERVERNAME$\\$SQLINSTANCENAME$ - Enter the server name and instance where the Compliance Status Database is located.</span></span>

    -   <span data-ttu-id="a291e-291">$DOMAIN $ \ \ $USERNAME $-entrez le nom de domaine et le nom d’utilisateur qui seront utilisés par les rapports de conformité et d’audit pour vous connecter à la base de données d’état de conformité.</span><span class="sxs-lookup"><span data-stu-id="a291e-291">$DOMAIN$\\$USERNAME$ - Enter the domain name and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>

    -   <span data-ttu-id="a291e-292">$PASSWORD $-entrez le mot de passe du compte d’utilisateur que vous utiliserez pour vous connecter à la base de données d’état de conformité.</span><span class="sxs-lookup"><span data-stu-id="a291e-292">$PASSWORD$ - Enter the password of the user account that will be used to connect to the Compliance Status Database.</span></span>



**<span data-ttu-id="a291e-293">Pour configurer l’accès aux rapports de conformité et d’audit sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-293">To configure the access to the Compliance and Audit Reports on Server B</span></span>**

1.  <span data-ttu-id="a291e-294">Sur le serveur B, utilisez le composant logiciel enfichable utilisateurs et groupes local dans le gestionnaire de serveur pour ajouter les comptes d’utilisateurs qui auront accès aux rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="a291e-294">On Server B, use the Local user and Groups snap-in from Server Manager to add the user accounts that will have access to the Compliance and Audit Reports.</span></span> <span data-ttu-id="a291e-295">Ajoutez les comptes d’utilisateurs au groupe local intitulé «utilisateurs du rapport MBAM».</span><span class="sxs-lookup"><span data-stu-id="a291e-295">Add the user accounts to the local group named “MBAM Report Users”.</span></span>

2.  <span data-ttu-id="a291e-296">Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à ce qui suit, en utilisant Windows PowerShell sur le serveur B.</span><span class="sxs-lookup"><span data-stu-id="a291e-296">To automate this procedure, you can use a command that is similar to the following, by using Windows PowerShell on Server B.</span></span>

    `PS C:\> net localgroup "MBAM Report Users" $DOMAIN$\$REPORTSUSERNAME$  /add`

    **<span data-ttu-id="a291e-297">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-297">Note</span></span>**  
    <span data-ttu-id="a291e-298">Remplacez la valeur suivante de l’exemple précédent par les valeurs applicables pour votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-298">Replace the following value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="a291e-299">$DOMAIN $ \ \ $REPORTSUSERNAME $-entrez le nom du compte d’utilisateur que vous avez utilisé pour configurer la source de données pour les rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="a291e-299">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports</span></span>



~~~
The command to add the users to the MBAM Report Users local group must be run for each user that will be accessing the reports in your environment.
~~~

**<span data-ttu-id="a291e-300">Pour arrêter toutes les occurrences du site Web d’administration et de contrôle MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-300">To stop all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="a291e-301">Sur chacun des serveurs qui exécutent la fonctionnalité d’administration et de surveillance de MBAM, vous pouvez utiliser la console du gestionnaire des services Internet (IIS) pour arrêter le site Web MBAM appelé **administration et surveillance de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="a291e-301">On each of the servers that run the MBAM Administration and Monitoring Feature use the Internet Information Services (IIS) Manager console to Stop the MBAM website named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="a291e-302">Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, à l’aide de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a291e-302">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Stop-Website “Microsoft BitLocker Administration and Monitoring”`

**<span data-ttu-id="a291e-303">Pour mettre à jour les données de connexion de base de données sur les serveurs d’administration et de surveillance MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-303">To update the Database Connection Data on MBAM Administration and Monitoring Servers</span></span>**

1. <span data-ttu-id="a291e-304">Sur chacun des serveurs qui exécutent la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour mettre à jour l’URL des rapports de conformité.</span><span class="sxs-lookup"><span data-stu-id="a291e-304">On each of the servers that run the MBAM Administration and Monitoring Feature, use the Internet Information Services (IIS) Manager console to update the Compliance Reports URL.</span></span>

2. <span data-ttu-id="a291e-305">Sélectionnez le site Web d' **administration et de contrôle Microsoft BitLocker** , puis utilisez la fonctionnalité **éditeur de configuration** qui se trouve dans la section **gestion** de l' **affichage des fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="a291e-305">Select the **Microsoft BitLocker Administration and Monitoring** website and use the **Configuration Editor** feature which can be found under the **Management** section of the **Feature View**.</span></span>

3. <span data-ttu-id="a291e-306">Sélectionnez l’option **appSettings** dans le contrôle de liste de sections.</span><span class="sxs-lookup"><span data-stu-id="a291e-306">Select the **appSettings** option from the Section list control.</span></span>

4. <span data-ttu-id="a291e-307">À partir de là, sélectionnez la ligne nommée **(collection)**, puis ouvrez l' **éditeur de collection** en sélectionnant le bouton à droite de la ligne.</span><span class="sxs-lookup"><span data-stu-id="a291e-307">From here, select the row named **(Collection)**, and open the **Collection Editor** by selecting the button on the right side of the row.</span></span>

5. <span data-ttu-id="a291e-308">Dans l' **éditeur de collection**, sélectionnez la ligne nommée «Microsoft. mbam. reports. URL».</span><span class="sxs-lookup"><span data-stu-id="a291e-308">In the **Collection Editor**, select the row named “Microsoft.Mbam.Reports.Url”.</span></span>

6. <span data-ttu-id="a291e-309">Mettez à jour la valeur pour Microsoft. mbam. reports. URL pour refléter le nom de serveur pour le serveur B. Si la fonctionnalité rapports de conformité et d’audit a été installée sur une instance nommée SQL Reporting Services, assurez-vous d’ajouter ou de mettre à jour le nom de l’instance à l’URL.</span><span class="sxs-lookup"><span data-stu-id="a291e-309">Update the value for Microsoft.Mbam.Reports.Url to reflect the server name for Server B. If the Compliance and Audit reports feature was installed on a named SQL Reporting Services instance, make sure that you add or update the name of the instance to the URL.</span></span> <span data-ttu-id="a291e-310">Par exemple, http://$SERVERNAME $/ReportServer\_ $ SQLSRSINSTANCENAME $/pages....</span><span class="sxs-lookup"><span data-stu-id="a291e-310">For example, http://$SERVERNAME$/ReportServer\_$SQLSRSINSTANCENAME$/Pages....</span></span>

7. <span data-ttu-id="a291e-311">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une commande similaire à celle qui suit dans chaque serveur d’administration et de surveillance:</span><span class="sxs-lookup"><span data-stu-id="a291e-311">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following one on each Administration and Monitoring Server:</span></span>

   `PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\sites\Microsoft BitLocker Administration and Monitoring" -Name "Value" -Value “http://$SERVERNAME$/ReportServer_$SRSINSTANCENAME$/Pages/ReportViewer.aspx?/Malta+Compliance+Reports/”`

   **<span data-ttu-id="a291e-312">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-312">Note</span></span>**  
   <span data-ttu-id="a291e-313">Remplacez la valeur de l’exemple précédent par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-313">Replace the value from the preceding example with those that match your environment:</span></span>

   -   <span data-ttu-id="a291e-314">$SERVERNAME $-entrez le nom du serveur sur lequel sont installés les rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="a291e-314">$SERVERNAME$ - Enter the name of the server to which the Compliance and Audit Reports were installed.</span></span>

   -   <span data-ttu-id="a291e-315">$SRSINSTANCENAME $-entrez le nom de l’instance SQL Report services dans laquelle les rapports de conformité et d’audit ont été installés.</span><span class="sxs-lookup"><span data-stu-id="a291e-315">$SRSINSTANCENAME$ - Enter the name of the SQL Reporting Services instance to which the Compliance and Audit Reports were installed.</span></span>



**<span data-ttu-id="a291e-316">Pour reprendre toutes les occurrences du site Web d’administration et de surveillance de MBAM</span><span class="sxs-lookup"><span data-stu-id="a291e-316">To resume all instances of the MBAM Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="a291e-317">Sur chacun des serveurs qui exécutent la fonctionnalité d’administration et de surveillance de MBAM, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web MBAM appelé **administration et surveillance de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="a291e-317">On each of the servers that run the MBAM Administration and Monitoring feature, use the Internet Information Services (IIS) Manager console to Start the MBAM web site named **Microsoft BitLocker Administration and Monitoring**.</span></span>

2.  <span data-ttu-id="a291e-318">Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, à l’aide de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a291e-318">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> Start-Website “Microsoft BitLocker Administration and Monitoring”`

    **<span data-ttu-id="a291e-319">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-319">Note</span></span>**  
    <span data-ttu-id="a291e-320">Pour exécuter cette commande, le module IIS pour PowerShell doit être ajouté à l’instance actuelle de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a291e-320">To execute this command, the IIS Module for PowerShell must be added to the current instance of PowerShell.</span></span> <span data-ttu-id="a291e-321">Par ailleurs, vous devez mettre à jour la stratégie d’exécution PowerShell pour permettre l’exécution de scripts.</span><span class="sxs-lookup"><span data-stu-id="a291e-321">In addition, you must update the PowerShell execution policy to enable execution of scripts.</span></span>



## <span data-ttu-id="a291e-322">Pour déplacer la fonctionnalité d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="a291e-322">To move the Administration and Monitoring feature</span></span>


<span data-ttu-id="a291e-323">Si vous choisissez de déplacer la fonctionnalité rapports d’administration et de surveillance de MBAM à partir d’un ordinateur vers un autre (si vous déplacez la fonctionnalité du serveur A vers le serveur B), vous devez utiliser la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="a291e-323">If you choose to move the MBAM Administration and Monitoring Reports feature from one computer to another, (if you move feature from Server A to Server B), you should use the following procedure.</span></span> <span data-ttu-id="a291e-324">Le processus comprend les étapes suivantes:</span><span class="sxs-lookup"><span data-stu-id="a291e-324">The process includes the following steps:</span></span>

1.  <span data-ttu-id="a291e-325">Exécution de la configuration de MBAM sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-325">Run MBAM setup on Server B</span></span>

2.  <span data-ttu-id="a291e-326">Configurer l’accès à la base de données sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-326">Configure Access to the Database on Server B</span></span>

**<span data-ttu-id="a291e-327">Pour exécuter la configuration de MBAM sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="a291e-327">To run MBAM setup on Server B</span></span>**

1.  <span data-ttu-id="a291e-328">Exécutez le programme d’installation de MBAM sur le serveur B et sélectionnez uniquement la fonctionnalité d’administration pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="a291e-328">Run MBAM setup on Server B and only select the Administration feature for installation.</span></span>

2.  <span data-ttu-id="a291e-329">Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, à l’aide de Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a291e-329">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell:</span></span>

    `PS C:\> MbamSetup.exe /qn I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 AddLocal=AdministrationMonitoringServer,HardwareCompatibility COMPLIDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ RECOVERYANDHWDB_SQLINSTANCE=$SERVERNAME$\$SQLINSTANCENAME$ SRS_REPORTSITEURL=$REPORTSSERVERURL$`

    **<span data-ttu-id="a291e-330">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-330">Note</span></span>**  
    <span data-ttu-id="a291e-331">Remplacez les valeurs de l’exemple précédent par celles correspondant à votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-331">Replace the values from the preceding example with those that match your environment:</span></span>

    -   <span data-ttu-id="a291e-332">$SERVERNAME $ \ \ $SQLINSTANCENAME $-pour le paramètre COMPLIDB \ _SQLINSTANCE, entrez le nom du serveur et l’instance où se trouve la base de données d’état de conformité.</span><span class="sxs-lookup"><span data-stu-id="a291e-332">$SERVERNAME$\\$SQLINSTANCENAME$ - For the COMPLIDB\_SQLINSTANCE parameter, input the server name and instance where the Compliance Status Database is located.</span></span> <span data-ttu-id="a291e-333">Pour le paramètre RECOVERYANDHWDB \ _SQLINSTANCE, entrez le nom du serveur et l’instance de la base de données de récupération et de matériel.</span><span class="sxs-lookup"><span data-stu-id="a291e-333">For the RECOVERYANDHWDB\_SQLINSTANCE parameter, input the server name and instance where the Recovery and Hardware Database is located.</span></span>

    -   <span data-ttu-id="a291e-334">$DOMAIN $ \ \ $USERNAME $-entrez le domaine et le nom d’utilisateur qui seront utilisés par les rapports de conformité et d’audit pour vous connecter à la base de données état de conformité.</span><span class="sxs-lookup"><span data-stu-id="a291e-334">$DOMAIN$\\$USERNAME$ - Enter the domain and user name that will be used by the Compliance and Audit reports feature to connect to the Compliance Status Database.</span></span>

    -   <span data-ttu-id="a291e-335">$ REPORTSSERVERURL $-entrez l’URL de l’emplacement d’accueil du site Web de service de création de rapports SQL.</span><span class="sxs-lookup"><span data-stu-id="a291e-335">$ REPORTSSERVERURL$ - Enter the URL for the Home location of the SQL Reporting Service website.</span></span> <span data-ttu-id="a291e-336">Si les rapports étaient installés sur une instance de SRS par défaut, le format d’URL sera formaté «http://$SERVERNAME $/ReportServer».</span><span class="sxs-lookup"><span data-stu-id="a291e-336">If the reports were installed to a default SRS instance the URL format will formatted “http:// $SERVERNAME$/ReportServer”.</span></span> <span data-ttu-id="a291e-337">Si les rapports étaient installés sur une instance de SRS par défaut, le format d’URL sera formaté en «http://$SERVERNAME $/ReportServer\_ $ SQLINSTANCENAME $».</span><span class="sxs-lookup"><span data-stu-id="a291e-337">If the reports were installed to a default SRS instance, the URL format will be formatted to “http://$SERVERNAME$/ReportServer\_$SQLINSTANCENAME$”.</span></span>



**<span data-ttu-id="a291e-338">Pour configurer l’accès aux bases de données</span><span class="sxs-lookup"><span data-stu-id="a291e-338">To configure the Access to the Databases</span></span>**

1.  <span data-ttu-id="a291e-339">Sur un serveur ou un serveur sur lequel la récupération et le matériel sont les bases de données de conformité et d’audit sont déployées, utilisez le composant logiciel enfichable utilisateurs et groupes locaux dans le gestionnaire de serveur pour ajouter les comptes d’ordinateur de chaque serveur qui exécute la fonctionnalité d’administration et d’analyse du MBAM aux groupes locaux intitulés «MBAM de récupération et de la base de données d’audit de la base de données</span><span class="sxs-lookup"><span data-stu-id="a291e-339">On server or servers where the Recovery and Hardware, and Compliance and Audit databases are deployed, use the Local user and Groups snap-in from Server Manager to add the machine accounts from each server that run the MBAM Administration and Monitoring feature to the Local Groups named “MBAM Recovery and Hardware DB Access” (Recovery and Hardware DB Server) and “MBAM Compliance Status DB Access” (Compliance and Audit DB Server).</span></span>

2.  <span data-ttu-id="a291e-340">Pour automatiser cette procédure, vous pouvez utiliser une commande similaire à celle qui suit, en utilisant Windows PowerShell sur le serveur sur lequel les bases de données d’audit et de conformité ont été déployées.</span><span class="sxs-lookup"><span data-stu-id="a291e-340">To automate this procedure, you can use a command that is similar to the following one, by using Windows PowerShell on the server where the Compliance and Audit databases were deployed.</span></span>

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    `PS C:\> net localgroup "MBAM Compliance Auditing DB Access" $DOMAIN$\$REPORTSUSERNAME$  /add`

3.  <span data-ttu-id="a291e-341">Sur le serveur sur lequel les bases de données de récupération et de matériel ont été déployées, exécutez une commande similaire à celle qui suit, à l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a291e-341">On the server where the Recovery and Hardware databases were deployed, run a command that is similar to the following one, by using Windows PowerShell.</span></span>

    `PS C:\> net localgroup "MBAM Recovery and Hardware DB Access" $DOMAIN$\$SERVERNAME$$  /add`

    **<span data-ttu-id="a291e-342">Remarque</span><span class="sxs-lookup"><span data-stu-id="a291e-342">Note</span></span>**  
    <span data-ttu-id="a291e-343">Remplacez la valeur de l’exemple précédent par les valeurs applicables pour votre environnement:</span><span class="sxs-lookup"><span data-stu-id="a291e-343">Replace the value from the preceding example with the applicable values for your environment:</span></span>

    -   <span data-ttu-id="a291e-344">$DOMAIN $ \ \ $SERVERNAME $ $-entrez le domaine et le nom de l’ordinateur du serveur d’administration et de surveillance MBAM.</span><span class="sxs-lookup"><span data-stu-id="a291e-344">$DOMAIN$\\$SERVERNAME$$ - Enter the domain and machine name of the MBAM Administration and Monitoring Server.</span></span> <span data-ttu-id="a291e-345">Le nom du serveur doit être suivi de a **$** .</span><span class="sxs-lookup"><span data-stu-id="a291e-345">The server name must be followed by a **$**.</span></span> <span data-ttu-id="a291e-346">Par exemple, MyDomain\\MyServerName1 $)</span><span class="sxs-lookup"><span data-stu-id="a291e-346">For example, MyDomain\\MyServerName1$)</span></span>

    -   <span data-ttu-id="a291e-347">$DOMAIN $ \ \ $REPORTSUSERNAME $-entrez le nom du compte d’utilisateur que vous avez utilisé pour configurer la source de données pour les rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="a291e-347">$DOMAIN$\\$REPORTSUSERNAME$ - Enter the user account name that was used to configure the data source for the Compliance and Audit reports.</span></span>



~~~
The commands listed for adding the server computer accounts to the MBAM local groups must be run for each Administration and Monitoring Server that will be accessing the databases in your environment.
~~~

## <span data-ttu-id="a291e-348">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a291e-348">Related topics</span></span>


[<span data-ttu-id="a291e-349">Administration des composants de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="a291e-349">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)









