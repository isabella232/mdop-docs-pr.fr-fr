---
title: Procédure pour migrer la base de données SQL d'App-V vers un autre SQL Server
description: Procédure pour migrer la base de données SQL d'App-V vers un autre SQL Server
author: dansimp
ms.assetid: 353892a1-9327-4489-a19c-4ec7bd1b736f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e3d84b0cb328873db3722ad3eb9af6a2b442fdcf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806961"
---
# <span data-ttu-id="a211c-103">Procédure pour migrer la base de données SQL d'App-V vers un autre SQL Server</span><span class="sxs-lookup"><span data-stu-id="a211c-103">How to Migrate the App-V SQL Database to a Different SQL Server</span></span>


<span data-ttu-id="a211c-104">Les procédures suivantes décrivent en détail la migration de la base de données SQL du serveur de gestion Microsoft application (App-V) vers un autre serveur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a211c-104">The following procedures describe in detail how to migrate the SQL database of the Microsoft Application Virtualization (App-V) Management Server to a different SQL Server.</span></span>

<span data-ttu-id="a211c-105">**Important**  Cette procédure requiert l’arrêt du service App-V Server et cela empêchera les utilisateurs finaux d’utiliser leurs applications.</span><span class="sxs-lookup"><span data-stu-id="a211c-105">**Important** This procedure requires that the App-V server service is stopped and this will prevent end-users from using their applications.</span></span>

 

**<span data-ttu-id="a211c-106">Pour sauvegarder la base de données SQL App-V</span><span class="sxs-lookup"><span data-stu-id="a211c-106">To back up the App-V SQL database</span></span>**

1.  <span data-ttu-id="a211c-107">Ouvrez le programme services. msc, puis arrêtez le service App-V Management Server sur tous les serveurs de gestion utilisant la base de données à migrer.</span><span class="sxs-lookup"><span data-stu-id="a211c-107">Open the Services.msc program and stop the App-V Management Server service on all Management Servers that use the database to be migrated.</span></span>

2.  <span data-ttu-id="a211c-108">Sur l’ordinateur sur lequel se trouve la base de données App-V, ouvrez SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="a211c-108">On the computer where the App-V database is located, open SQL Server Management Studio.</span></span>

3.  <span data-ttu-id="a211c-109">Développez le nœud **bases de données** et recherchez la base de données App-V (le nom par défaut est APPVIRT).</span><span class="sxs-lookup"><span data-stu-id="a211c-109">Expand the **Databases** node and locate the App-V database (default name is APPVIRT).</span></span>

4.  <span data-ttu-id="a211c-110">Cliquez avec le bouton droit sur la base de données, puis sélectionnez **tâches** et **sauvegarder**.</span><span class="sxs-lookup"><span data-stu-id="a211c-110">Right-click the database and select **Tasks** and then select **Back Up**.</span></span>

5.  <span data-ttu-id="a211c-111">Vérifiez que le **modèle de récupération** est défini sur **simple** et que le **type de sauvegarde** est défini sur **complet**.</span><span class="sxs-lookup"><span data-stu-id="a211c-111">Verify that **Recovery model** is set to **SIMPLE** and the **Backup type** is set to **Full**.</span></span> <span data-ttu-id="a211c-112">Modifiez les paramètres de **destination** et de **jeu de sauvegarde** , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="a211c-112">Change the **Backup set** and **Destination** settings if it is necessary.</span></span>

6.  <span data-ttu-id="a211c-113">Cliquez sur **OK** pour sauvegarder la base de données.</span><span class="sxs-lookup"><span data-stu-id="a211c-113">Click **OK** to back up the database.</span></span> <span data-ttu-id="a211c-114">Lorsque la sauvegarde a été effectuée avec succès, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a211c-114">After the backup has completed successfully, click **OK**.</span></span>

7.  <span data-ttu-id="a211c-115">Ouvrez l’Explorateur Windows et naviguez jusqu’au dossier contenant le fichier de sauvegarde de la base de données (par exemple, APPVIRT. BAK.</span><span class="sxs-lookup"><span data-stu-id="a211c-115">Open Windows Explorer and browse to the folder that contains the database backup file, for example APPVIRT.BAK.</span></span> <span data-ttu-id="a211c-116">Copiez le fichier de sauvegarde de la base de données sur l’ordinateur de destination exécutant SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a211c-116">Copy the database backup file to the destination computer that is running SQL Server.</span></span>

**<span data-ttu-id="a211c-117">Pour restaurer la base de données SQL App-V sur l’ordinateur de destination</span><span class="sxs-lookup"><span data-stu-id="a211c-117">To restore the App-V SQL database to the destination computer</span></span>**

1.  <span data-ttu-id="a211c-118">Sur l’ordinateur de destination, ouvrez SQL Server Management Studio, cliquez avec le bouton droit sur le nœud **bases de données** , puis sélectionnez **restaurer la base de données**.</span><span class="sxs-lookup"><span data-stu-id="a211c-118">On the destination computer, open SQL Server Management Studio, right-click the **Databases** node and select **Restore Database**.</span></span>

2.  <span data-ttu-id="a211c-119">Sous **source pour la restauration**, choisissez **à partir de l’appareil** , puis cliquez sur «**...».**</span><span class="sxs-lookup"><span data-stu-id="a211c-119">Under **Source for Restore**, choose **From device** and then click the “**…**”</span></span> <span data-ttu-id="a211c-120">.</span><span class="sxs-lookup"><span data-stu-id="a211c-120">button.</span></span>

3.  <span data-ttu-id="a211c-121">Dans la boîte de dialogue **spécifier la sauvegarde** , assurez-vous que l’option **média de sauvegarde** est définie sur **fichier** , puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="a211c-121">In the **Specify Backup** dialog box, make sure that the **Backup Media** is set to **File** and then click **Add**.</span></span>

4.  <span data-ttu-id="a211c-122">Sélectionnez le fichier de sauvegarde que vous avez copié à partir de l’ordinateur d’origine exécutant SQL Server, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a211c-122">Select the backup file that you copied from the original computer that is running SQL Server, and then click **OK**.</span></span>

5.  <span data-ttu-id="a211c-123">Cliquez sur **OK** , puis sélectionnez le jeu de sauvegarde à restaurer.</span><span class="sxs-lookup"><span data-stu-id="a211c-123">Click **OK** and then click to select the backup set to restore.</span></span>

6.  <span data-ttu-id="a211c-124">Sous **destination pour la restauration**, cliquez sur la liste déroulante pour la **base de données** , puis sélectionnez le nom de la base de données App-V (par exemple, APPVIRT.</span><span class="sxs-lookup"><span data-stu-id="a211c-124">Under **Destination for restore**, click the drop-down for **To database** and select the App-V database name, for example APPVIRT.</span></span>

7.  <span data-ttu-id="a211c-125">Cliquez sur **OK** pour démarrer la restauration.</span><span class="sxs-lookup"><span data-stu-id="a211c-125">Click **OK** to start the restore.</span></span> <span data-ttu-id="a211c-126">Lorsque la restauration s’est déroulée correctement, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a211c-126">After the restore has completed successfully, click **OK**.</span></span>

8.  <span data-ttu-id="a211c-127">Développez le nœud **sécurité** , cliquez avec le bouton droit sur **connexions** et sélectionnez **nouvelle connexion**.</span><span class="sxs-lookup"><span data-stu-id="a211c-127">Expand the **Security** node, right-click **Logins** and select **New Login**.</span></span>

9.  <span data-ttu-id="a211c-128">Dans le champ **nom de connexion** , entrez les informations de compte de service réseau pour le serveur de gestion de l’application-V au format DOMAIN\\SERVERNAME $.</span><span class="sxs-lookup"><span data-stu-id="a211c-128">In the **Login Name** field, enter the Network Service account details for the App-V Management Server in the format of DOMAIN\\SERVERNAME$.</span></span>

10. <span data-ttu-id="a211c-129">Dans la page **général** de la **base de données par défaut** , sélectionnez le nom de la base de données App-V (par exemple, APPVIRT), puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a211c-129">On the **General** page under **Default database** select the App-V database name, for example, APPVIRT, and then click **OK**.</span></span>

11. <span data-ttu-id="a211c-130">Sous **Sélectionner une page**, cliquez sur la page de **mappage utilisateur** pour la sélectionner.</span><span class="sxs-lookup"><span data-stu-id="a211c-130">Under **Select a page**, click to select the **User Mapping** page.</span></span> <span data-ttu-id="a211c-131">Sous **utilisateurs mappés à cette connexion**, activez la case à cocher dans la colonne **carte** pour sélectionner la base de données App-V.</span><span class="sxs-lookup"><span data-stu-id="a211c-131">Under **Users mapped to this login**, click the check box in the **Map** column to select the App-V database.</span></span>

12. <span data-ttu-id="a211c-132">Sous **appartenance au rôle de base de données pour: &lt; &gt; appvdatabasename**, cliquez pour sélectionner **SFTEveryone** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a211c-132">Under **Database role membership for: &lt;appvdatabasename&gt;**, click to select **SFTEveryone** and then click **OK**.</span></span>

13. <span data-ttu-id="a211c-133">Assurez-vous que le pare-feu Windows sur le nouvel ordinateur exécutant SQL Server est configuré pour permettre au serveur de gestion des applications d’accéder au système.</span><span class="sxs-lookup"><span data-stu-id="a211c-133">Make sure that the Windows Firewall on the new computer that is running SQL Server is configured to allow the App-V Management Server to access the system.</span></span> <span data-ttu-id="a211c-134">Sous **Outils d’administration**, utilisez le programme **pare-feu Windows avec Advanced Security** pour créer une **règle de trafic entrant** pour le port utilisé par SQL Server (par défaut, le port 1433).</span><span class="sxs-lookup"><span data-stu-id="a211c-134">Under **Administrative Tools**, use the **Windows Firewall with Advanced Security** program to create an **Inbound Rule** for the port that is used by SQL Server (default is port 1433).</span></span>

**<span data-ttu-id="a211c-135">Pour migrer les tâches de l’agent App-V SQL Server</span><span class="sxs-lookup"><span data-stu-id="a211c-135">To migrate the App-V SQL Server Agent jobs</span></span>**

1.  <span data-ttu-id="a211c-136">Sur l’ordinateur d’origine exécutant SQL Server, dans SQL Server Management Studio, développez le nœud de l' **agent SQL Server** , puis développez le nœud **Jobs** .</span><span class="sxs-lookup"><span data-stu-id="a211c-136">On the original computer that is running SQL Server, in SQL Server Management Studio, expand the **SQL Server Agent** node, and then expand the **Jobs** node.</span></span>

2.  <span data-ttu-id="a211c-137">Cliquez avec le bouton droit sur les quatre tâches App-V suivantes, puis sélectionnez \*\*tâche de script en tant que | CRÉER sur | \*\*Enregistrez chaque script dans un dossier et attribuez un nom descriptif à chaque script.</span><span class="sxs-lookup"><span data-stu-id="a211c-137">Right-click the following four App-V jobs and select **Script Job as | CREATE to | File**, and save each script to a folder and give each script a descriptive name.</span></span>

    -   **<span data-ttu-id="a211c-138">Base de données SoftGrid (appvdbname) vérifier l’historique d’utilisation</span><span class="sxs-lookup"><span data-stu-id="a211c-138">Softgrid Database (appvdbname) Check Usage History</span></span>**

    -   **<span data-ttu-id="a211c-139">Base de données appvdbname pour fermer les sessions orphelines</span><span class="sxs-lookup"><span data-stu-id="a211c-139">Softgrid Database (appvdbname) Close Orphaned Sessions</span></span>**

    -   **<span data-ttu-id="a211c-140">La base de données appvdbname est limitée à la taille</span><span class="sxs-lookup"><span data-stu-id="a211c-140">Softgrid Database (appvdbname) Enforce Size Limit</span></span>**

    -   **<span data-ttu-id="a211c-141">Base de données sur le moniteur de base de données (appvdbname)</span><span class="sxs-lookup"><span data-stu-id="a211c-141">Softgrid Database (appvdbname) Monitor Alert/Job Status</span></span>**

3.  <span data-ttu-id="a211c-142">Dans l’ordinateur de destination exécutant SQL Server et Open SQL Server Management Studio, copiez les quatre fichiers de script (. Sql).</span><span class="sxs-lookup"><span data-stu-id="a211c-142">Copy the four script files (.sql) to the destination computer that is running SQL Server and open SQL Server Management Studio.</span></span>

4.  <span data-ttu-id="a211c-143">Dans l’Explorateur Windows, cliquez avec le bouton droit sur chaque fichier. SQL, puis cliquez sur **exécuter**.</span><span class="sxs-lookup"><span data-stu-id="a211c-143">In Windows Explorer, right-click each .sql file and then click **Run**.</span></span> <span data-ttu-id="a211c-144">Chaque script s’ouvre dans une fenêtre de requête dans SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="a211c-144">Each script will open in a query window in SQL Server Management Studio.</span></span> <span data-ttu-id="a211c-145">Cliquez sur **exécuter** pour chaque script et vérifiez que chacun d’eux est correctement exécuté.</span><span class="sxs-lookup"><span data-stu-id="a211c-145">Click **Execute** for each script and verify that each is completed successfully.</span></span>

5.  <span data-ttu-id="a211c-146">Actualisez le nœud **tâches** sous le nœud de l' **agent SQL Server** , puis vérifiez que les quatre tâches sont correctement créées.</span><span class="sxs-lookup"><span data-stu-id="a211c-146">Refresh the **Jobs** node under the **SQL Server Agent** node and confirm that the four jobs are created successfully.</span></span>

**<span data-ttu-id="a211c-147">Pour mettre à jour la configuration du serveur de gestion App-V</span><span class="sxs-lookup"><span data-stu-id="a211c-147">To update the configuration of the App-V Management Server</span></span>**

1.  <span data-ttu-id="a211c-148">Sur le serveur de gestion App-V, modifiez les clés de Registre suivantes:</span><span class="sxs-lookup"><span data-stu-id="a211c-148">On the App-V Management Server, modify the following registry keys:</span></span>

    -   <span data-ttu-id="a211c-149">**SQLServerName**  =  SqlServerName &lt; newservername&gt;</span><span class="sxs-lookup"><span data-stu-id="a211c-149">**SQLServerName** = &lt;newservername&gt;</span></span>

    -   <span data-ttu-id="a211c-150">**SQLServerPort**  =  SQLServerPort &lt; newserverport&gt;</span><span class="sxs-lookup"><span data-stu-id="a211c-150">**SQLServerPort** = &lt;newserverport&gt;</span></span>

    <span data-ttu-id="a211c-151">Redémarrez ensuite le service App-V Server.</span><span class="sxs-lookup"><span data-stu-id="a211c-151">Then restart the App-V server service.</span></span>

2.  <span data-ttu-id="a211c-152">Recherchez le fichier SftMgmt. UDL sous le répertoire d’installation de l’application-V Management Server (la valeur par défaut est C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Service).</span><span class="sxs-lookup"><span data-stu-id="a211c-152">Browse to find the file SftMgmt.udl under the App-V Management Server installation directory (default is C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Service).</span></span> <span data-ttu-id="a211c-153">Cliquez avec le bouton droit sur le fichier, puis sélectionnez **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="a211c-153">Right-click the file and select **Open**.</span></span>

3.  <span data-ttu-id="a211c-154">Dans l’onglet **connexion** , entrez le nom de l’ordinateur de destination exécutant SQL Server, puis cliquez sur **tester la connexion**.</span><span class="sxs-lookup"><span data-stu-id="a211c-154">On the **Connection** tab, enter the name of the destination computer that is running SQL Server, and then click **Test Connection**.</span></span> <span data-ttu-id="a211c-155">Une fois le test terminé, cliquez sur **OK** , puis de nouveau sur **OK** .</span><span class="sxs-lookup"><span data-stu-id="a211c-155">When the test is successful, click **OK** and then click **OK** again.</span></span>

4.  <span data-ttu-id="a211c-156">Pour les versions Server App-V de gestion antérieures à 4,5 SP2, vous devez mettre à jour les paramètres de journalisation SQL.</span><span class="sxs-lookup"><span data-stu-id="a211c-156">For App-V Management Server versions before 4.5 SP2, you must update the SQL Logging settings.</span></span> <span data-ttu-id="a211c-157">Sous **groupes de serveurs**, cliquez avec le bouton droit sur le groupe de serveurs dont le serveur est membre, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="a211c-157">Under **Server Groups**, right-click the server group the server is a member of and select **Properties**.</span></span>

5.  <span data-ttu-id="a211c-158">Dans l’onglet **journalisation** , cliquez sur l’entrée **de la base de données SQL** pour la sélectionner, puis cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="a211c-158">On the **Logging** tab click to select the **SQL Database** entry and then click **Edit**.</span></span>

6.  <span data-ttu-id="a211c-159">Remplacez le **nom d’hôte DNS** par le nom d’hôte du nouvel ordinateur exécutant SQL Server, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a211c-159">Change the **DNS Host Name** to the host name of the new computer that is running SQL Server and then click **OK**.</span></span> <span data-ttu-id="a211c-160">Cliquez sur **OK** deux fois de plus, puis redémarrez le service App-V Server.</span><span class="sxs-lookup"><span data-stu-id="a211c-160">Click **OK** two times more, and then restart the App-V server service.</span></span>

7.  <span data-ttu-id="a211c-161">Ouvrez la console de gestion App-V, cliquez avec le bouton droit sur le nœud **applications** et sélectionnez **Actualiser**.</span><span class="sxs-lookup"><span data-stu-id="a211c-161">Open the App-V Management Console, right-click the **Applications** node and select **Refresh**.</span></span> <span data-ttu-id="a211c-162">La liste des applications doit être affichée comme auparavant.</span><span class="sxs-lookup"><span data-stu-id="a211c-162">The list of applications should be displayed as before.</span></span>

 

 





