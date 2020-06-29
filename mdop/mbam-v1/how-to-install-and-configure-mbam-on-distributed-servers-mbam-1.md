---
title: Installation et configuration de MBAM sur des serveurs distribués
description: Installation et configuration de MBAM sur des serveurs distribués
author: dansimp
ms.assetid: 9ee766aa-6339-422a-8d00-4f58e4646a5e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51f56a12d4e59226f834c7e474af0f1e96c1e8e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811286"
---
# <span data-ttu-id="1b5e2-103">Installation et configuration de MBAM sur des serveurs distribués</span><span class="sxs-lookup"><span data-stu-id="1b5e2-103">How to Install and Configure MBAM on Distributed Servers</span></span>


<span data-ttu-id="1b5e2-104">Les procédures décrites dans cette rubrique décrivent l’installation complète des fonctionnalités d’administration et de surveillance de Microsoft BitLocker (MBAM) sur les serveurs distribués.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-104">The procedures in this topic describe the full installation of the Microsoft BitLocker Administration and Monitoring (MBAM) features on distributed servers.</span></span>

<span data-ttu-id="1b5e2-105">Chaque fonctionnalité de serveur comporte certaines conditions préalables.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-105">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="1b5e2-106">Pour vérifier que vous remplissez les conditions préalables et que vous avez besoin de la configuration matérielle et logicielle requise, voir Configuration requise pour le [déploiement d’MBAM 1,0](mbam-10-deployment-prerequisites.md) et [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="1b5e2-106">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span> <span data-ttu-id="1b5e2-107">De plus, certaines fonctionnalités nécessitent que vous fournissez des informations lors du processus d’installation pour déployer la fonctionnalité correctement.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-107">In addition, some features require that you provide certain information during the installation process to successfully deploy the feature.</span></span>

**<span data-ttu-id="1b5e2-108">Remarque</span><span class="sxs-lookup"><span data-stu-id="1b5e2-108">Note</span></span>**  
<span data-ttu-id="1b5e2-109">Pour obtenir les fichiers journaux d’installation, vous devez installer MBAM à l’aide du package **msiexec** et de l’option \*\*/l &lt; emplacement &gt; \*\* .</span><span class="sxs-lookup"><span data-stu-id="1b5e2-109">To obtain the setup log files, you have to install MBAM by using the **msiexec** package and the **/l &lt;location&gt;** option.</span></span> <span data-ttu-id="1b5e2-110">Les fichiers journaux sont créés à l’emplacement que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-110">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="1b5e2-111">D’autres fichiers journaux d’installation sont créés dans le dossier% Temp% de l’utilisateur qui exécute l’installation MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-111">Additional setup log files are created in the %temp% folder of the user that runs the MBAM installation.</span></span>



## <a href="" id="deploy-the-mbam-server-features-"></a><span data-ttu-id="1b5e2-112">Déployer les fonctionnalités du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="1b5e2-112">Deploy the MBAM Server features</span></span>


<span data-ttu-id="1b5e2-113">Les étapes suivantes expliquent comment installer les fonctionnalités MBAM générales.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-113">The following steps describe how to install the general MBAM features.</span></span>

**<span data-ttu-id="1b5e2-114">Remarque</span><span class="sxs-lookup"><span data-stu-id="1b5e2-114">Note</span></span>**  
<span data-ttu-id="1b5e2-115">Vérifiez que vous utilisez la configuration de 32 bits sur les serveurs 32 bits et la configuration 64 bits sur les serveurs 64.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-115">Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>



**<span data-ttu-id="1b5e2-116">Pour déployer les fonctionnalités du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="1b5e2-116">To Deploy MBAM Server features</span></span>**

1.  <span data-ttu-id="1b5e2-117">Démarrez l’Assistant Installation de MBAM, puis cliquez sur **installer** sur la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-117">Start the MBAM installation wizard, and click **Install** at the Welcome page.</span></span>

2.  <span data-ttu-id="1b5e2-118">Lisez et acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-118">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="1b5e2-119">Par défaut, toutes les fonctionnalités de MBAM sont sélectionnées pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-119">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="1b5e2-120">Effacez les fonctionnalités que vous voulez installer ailleurs.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-120">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="1b5e2-121">Les fonctionnalités que vous voulez installer sur le même ordinateur doivent être installées en même temps.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-121">Features that you want to install on the same computer must be installed all at the same time.</span></span> <span data-ttu-id="1b5e2-122">Les fonctionnalités de MBAM doivent être installées dans l’ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="1b5e2-122">MBAM features must be installed in the following order:</span></span>

    -   <span data-ttu-id="1b5e2-123">Base de données de récupération et de matériel</span><span class="sxs-lookup"><span data-stu-id="1b5e2-123">Recovery and Hardware Database</span></span>

    -   <span data-ttu-id="1b5e2-124">Base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="1b5e2-124">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="1b5e2-125">Rapports et audit de conformité</span><span class="sxs-lookup"><span data-stu-id="1b5e2-125">Compliance Audit and Reports</span></span>

    -   <span data-ttu-id="1b5e2-126">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="1b5e2-126">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="1b5e2-127">Modèle de stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="1b5e2-127">MBAM Group Policy Template</span></span>

    **<span data-ttu-id="1b5e2-128">Remarque</span><span class="sxs-lookup"><span data-stu-id="1b5e2-128">Note</span></span>**  
    <span data-ttu-id="1b5e2-129">L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-129">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="1b5e2-130">Si toutes les conditions préalables sont remplies, l’installation continue.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-130">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="1b5e2-131">Si une condition préalable manquante est détectée, vous devez résoudre les conditions préalables manquantes, puis cliquer de **nouveau sur vérifier les conditions préalables**.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-131">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="1b5e2-132">Si toutes les conditions préalables sont remplies cette fois, l’installation sera reprise.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-132">If all prerequisites are met this time, the installation will resume.</span></span>



4.  <span data-ttu-id="1b5e2-133">L’Assistant de configuration de MBAM affiche les pages d’installation correspondant aux composants sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-133">The MBAM Setup wizard will display the installation pages for the selected features.</span></span> <span data-ttu-id="1b5e2-134">Les sections suivantes décrivent les procédures d’installation pour chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-134">The following sections describe the installation procedures for each feature.</span></span>

    **<span data-ttu-id="1b5e2-135">Remarque</span><span class="sxs-lookup"><span data-stu-id="1b5e2-135">Note</span></span>**  
    <span data-ttu-id="1b5e2-136">En règle générale, chaque fonctionnalité est installée sur un serveur distinct.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-136">Typically, each feature is installed on a separate server.</span></span> <span data-ttu-id="1b5e2-137">Si vous voulez installer plusieurs fonctionnalités sur un seul serveur, vous pouvez modifier ou supprimer les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-137">If you want to install multiple features on a single server, you may change or eliminate some of the following steps.</span></span>



~~~
**To install the Recovery and Hardware Database**

1.  Choose an option for MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the names of the computers that will be running the Administration and Monitoring Server feature, to configure access to the Recovery and Hardware Database.. Once the Administration and Monitoring Server feature is deployed, it connects to the database by using its domain account.

4.  Click **Next** to continue.

5.  Specify the **Database Configuration** for the SQL Server instance that stores the recovery and hardware data. You must also specify where the database will be located and where the log information will be located.

6.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Database**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Compliance and Audit Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that will be used for encryption.

2.  Click **Next** to continue.

3.  Specify the user account that will be used to access the database for reports.

4.  Click **Next** to continue.

5.  Specify the computer names of the computers that you want to run the Administration and Monitoring Server and the Compliance and Audit Reports, to configure the access to the Compliance and Audit Database.. After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they will connect to the databases by using their domain accounts.

6.  Specify the **Database Configuration** for the SQL Server instance that will store the compliance and audit data. You must also specify where the database will be located and where the log information will be located.

7.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Reports**

1.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Compliance and Audit Database are installed.

2.  Specify the name of the Compliance and Audit Database. By default, the database name is “MBAM Compliance Status”, but you can change the name when you install the Compliance and Audit Database.

3.  Click **Next** to continue.

4.  Select the SQL Server Reporting Services instance where the Compliance and Audit Reports will be installed. Provide the username and password used to access the compliance database.

5.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Administration and Monitoring Server feature**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the remote SQL Server instance, For example, *&lt;ServerName&gt;*, where the Compliance and Audit Database are installed.

4.  Specify the name of the Compliance and Audit Database. By default, the database name is MBAM Compliance Status, but, you can change the name when you install the Compliance and Audit Database.

5.  Click **Next** to continue.

6.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Recovery and Hardware Database are installed.

7.  Specify the name of the Recovery and Hardware Database. By default, the database name is **MBAM Recovery and Hardware**, but you can change the name when you install the Recovery and Hardware Database feature.

8.  Click **Next** to continue.

9.  Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site. The default Home location of a SQL Server Reporting Services site instance is at:

    http://*&lt;NameofMBAMReportsServer&gt;/*ReportServer

    **Note**  
    If you configured the SQL Server Reporting Services as a named instance, the URL resembles the following:http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*



10. Click **Next** to continue.

11. Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server

    **Warning**  
    The port number that you specify must be an unused port number on the Administration and Monitoring server, unless you specify a unique host header name.



12. Click **Next** to continue with the MBAM Setup wizard.
~~~

5. 

   <span data-ttu-id="1b5e2-138">Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-138">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

6. <span data-ttu-id="1b5e2-139">Lorsque les informations de fonctionnalité de MBAM sélectionnées sont terminées, vous êtes prêt à démarrer l’installation d’MBAM à l’aide de l’Assistant de configuration.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-139">When the selected MBAM feature information is complete, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="1b5e2-140">Cliquez sur **retour** pour parcourir l’Assistant si vous devez revoir ou modifier vos paramètres d’installation.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-140">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="1b5e2-141">Cliquez sur **installer** pour lancer l’installation.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-141">Click **Install** to begin the installation.</span></span> <span data-ttu-id="1b5e2-142">Cliquez sur **Annuler** pour quitter l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-142">Click **Cancel** to exit the Wizard.</span></span> <span data-ttu-id="1b5e2-143">Le programme d’installation installe les fonctionnalités de MBAM que vous avez sélectionnées et vous signale que l’installation est terminée.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-143">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

7. <span data-ttu-id="1b5e2-144">Cliquez sur **Terminer** pour quitter l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-144">Click **Finish** to exit the wizard.</span></span>

8. <span data-ttu-id="1b5e2-145">Ajoutez des utilisateurs aux rôles MBAM appropriés, après l’installation des fonctionnalités de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-145">Add users to appropriate MBAM roles, after the MBAM server features are installed..</span></span> <span data-ttu-id="1b5e2-146">Pour plus d’informations, reportez-vous [à planification des rôles d’administrateur MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1b5e2-146">For more information, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

**<span data-ttu-id="1b5e2-147">Configuration après l’installation</span><span class="sxs-lookup"><span data-stu-id="1b5e2-147">Post-installation configuration</span></span>**

1.  <span data-ttu-id="1b5e2-148">Après l’installation d’MBAM, vous devez ajouter des rôles d’utilisateur pour permettre aux utilisateurs d’accéder aux fonctionnalités dans le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-148">After MBAM Setup is finished, you must add user Roles before users can access to features in the MBAM administration website.</span></span> <span data-ttu-id="1b5e2-149">Sur le serveur d’administration et de surveillance, ajoutez des utilisateurs aux groupes locaux suivants.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-149">On the Administration and Monitoring Server, add users to the following local groups.</span></span>

    -   <span data-ttu-id="1b5e2-150">**Utilisateurs matériels MBAM**: les membres de ce groupe local peuvent accéder à la fonctionnalité matérielle dans le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-150">**MBAM Hardware Users**: Members of this local group can access the Hardware feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="1b5e2-151">**Utilisateurs du support technique MBAM**: les membres de ce groupe local peuvent accéder aux fonctionnalités de récupération de lecteur et de gestion des modules de plateforme sécurisée (TPM) sur le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-151">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage Trusted Platform Modules (TPM) features in the MBAM administration website.</span></span> <span data-ttu-id="1b5e2-152">Pour un utilisateur du support technique, tous les champs de la récupération de lecteur et de la gestion de TPM sont obligatoires.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-152">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="1b5e2-153">**Utilisateurs expérimentés du support technique MBAM**: les membres de ce groupe local disposent d’un accès avancé aux fonctionnalités de récupération de lecteur et de gestion des composants de plateforme dans le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-153">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features in the MBAM administration website.</span></span> <span data-ttu-id="1b5e2-154">Pour les utilisateurs expérimentés du support technique, seul le champ ID clé est requis pour la récupération du lecteur.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-154">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="1b5e2-155">Dans gérer le module de plateforme sécurisée, seul le champ domaine de l’ordinateur et le champ nom de l’ordinateur est requis.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-155">In Manage TPM, only the Computer Domain field and Computer Name field are required.</span></span>

2.  <span data-ttu-id="1b5e2-156">Sur la base de données d’administration et de surveillance du serveur, de la conformité et de l’audit, et sur le serveur qui héberge les rapports de conformité et d’audit, ajoutez des utilisateurs au groupe local suivant pour leur permettre d’accéder à la fonctionnalité rapports dans le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-156">On the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports, add users to the following local group to give them access to the Reports feature in the MBAM administration website.</span></span>

    -   <span data-ttu-id="1b5e2-157">**Utilisateurs du rapport MBAM**: les membres de ce groupe local peuvent accéder aux rapports figurant sur le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-157">**MBAM Report Users**: Members of this local group can access the Reports in the MBAM administration website.</span></span>

    **<span data-ttu-id="1b5e2-158">Remarque</span><span class="sxs-lookup"><span data-stu-id="1b5e2-158">Note</span></span>**  
    <span data-ttu-id="1b5e2-159">Il est possible d’avoir une appartenance similaire à un utilisateur ou un groupe du groupe local **utilisateurs de rapports MBAM** sur tous les ordinateurs sur lesquels les fonctionnalités d’administration de MBAM et de surveillance de la base de données de serveur et de conformité, ainsi que les rapports de conformité et d’audit sont installés.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-159">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and the Compliance and Audit Reports are installed.</span></span>



## <span data-ttu-id="1b5e2-160">Valider l’installation de la fonctionnalité MBAM Server</span><span class="sxs-lookup"><span data-stu-id="1b5e2-160">Validate the MBAM Server feature installation</span></span>


<span data-ttu-id="1b5e2-161">Lorsque l’installation de la fonctionnalité de serveur MBAM est terminée, vous devez vérifier que l’installation a correctement configuré toutes les fonctionnalités nécessaires à MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-161">When the MBAM Server feature installation is complete, you should validate that the installation has successfully set up all the necessary features for MBAM.</span></span> <span data-ttu-id="1b5e2-162">Utilisez la procédure suivante pour vérifier que le service MBAM est fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-162">Use the following procedure to confirm that the MBAM service is functional.</span></span>

**<span data-ttu-id="1b5e2-163">Pour valider une installation MBAM</span><span class="sxs-lookup"><span data-stu-id="1b5e2-163">To validate an MBAM installation</span></span>**

1. <span data-ttu-id="1b5e2-164">Sur chaque serveur sur lequel une fonctionnalité de MBAM est déployée, ouvrez **le panneau de configuration**, cliquez sur **programmes**, puis cliquez sur **programmes et fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-164">On each server, where an MBAM feature is deployed, open **Control Panel**, click **Programs**, and then click **Programs and Features**.</span></span> <span data-ttu-id="1b5e2-165">Vérifiez que la fonctionnalité **administration et analyse de BitLocker Microsoft** s’affiche dans la liste **programmes et fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="1b5e2-165">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="1b5e2-166">Remarque</span><span class="sxs-lookup"><span data-stu-id="1b5e2-166">Note</span></span>**  
   <span data-ttu-id="1b5e2-167">Pour valider l’installation d’MBAM, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-167">To validate the MBAM installation, you must use a Domain Account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="1b5e2-168">Sur le serveur sur lequel la base de données de récupération et de matériel est installée, ouvrez SQL Server Management Studio, puis vérifiez que la base de données **MBAM et de récupération** de la base de données est installée.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-168">On the server where the Recovery and Hardware Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="1b5e2-169">Sur le serveur sur lequel la base de données d’audit et de conformité est installée, ouvrez SQL Server Management Studio et vérifiez que la base de données de **statut de conformité MBAM** est installée.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-169">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance Status** database is installed.</span></span>

4. <span data-ttu-id="1b5e2-170">Sur le serveur sur lequel sont installés les rapports de conformité et d’audit, ouvrez un navigateur Web doté de privilèges d’administration et naviguez jusqu’au site «Home» du site SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-170">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative privileges and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="1b5e2-171">L’emplacement d’accueil par défaut d’une instance de site SQL Server Reporting Services est disponible sur http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports.aspx.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-171">The default Home location of a SQL Server Reporting Services site instance can be found at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.aspx.</span></span> <span data-ttu-id="1b5e2-172">Pour trouver l’URL réelle, utilisez l’outil Gestionnaire de configuration Reporting Services et sélectionnez les instances spécifiées lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-172">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances specified during setup.</span></span>

   <span data-ttu-id="1b5e2-173">Vérifiez qu’un dossier nommé **rapports de conformité Malte** figure et qu’il contient cinq rapports et une seule source de données.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-173">Confirm that a folder named **Malta Compliance Reports** is listed and that it contains five reports and one data source.</span></span>

   **<span data-ttu-id="1b5e2-174">Remarque</span><span class="sxs-lookup"><span data-stu-id="1b5e2-174">Note</span></span>**  
   <span data-ttu-id="1b5e2-175">Si SQL Server Reporting Services a été configuré en tant qu’instance nommée, l’URL doit ressembler à ce qui suit: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="1b5e2-175">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



5. <span data-ttu-id="1b5e2-176">Sur le serveur sur lequel est installé la fonctionnalité d’administration et de surveillance, exécutez le **Gestionnaire de serveur** et recherchez les **rôles**, sélectionnez **serveur Web (IIS)**, puis cliquez sur **Gestionnaire des services Internet (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-176">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**, select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager**.</span></span> <span data-ttu-id="1b5e2-177">Dans **connexions** , naviguez jusqu’à \* &lt; nomordinateur &gt; \*, cliquez sur **sites**, puis sur **analyse et administration de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-177">In **Connections** browse to *&lt;computername&gt;*, click **Sites**, and click **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="1b5e2-178">Vérifiez que **MBAMAdministrationService**, **MBAMComplianceStatusService**et **MBAMRecoveryAndHardwareService** apparaissent.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-178">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

6. <span data-ttu-id="1b5e2-179">Sur le serveur sur lequel est installé la fonctionnalité d’administration et de contrôle, ouvrez un navigateur Web avec des privilèges d’administration et recherchez les emplacements suivants dans le site Web MBAM pour vérifier qu’ils se chargent correctement:</span><span class="sxs-lookup"><span data-stu-id="1b5e2-179">On the server where the Administration and Monitoring feature is installed, open a web browser with administrative privileges and browse to the following locations in the MBAM web site, to verify that they load successfully:</span></span>

   -   <span data-ttu-id="1b5e2-180">*http:// &lt; nomordinateur &gt; /default.aspx* et confirmez chacun des liens pour la navigation et les rapports</span><span class="sxs-lookup"><span data-stu-id="1b5e2-180">*http://&lt;computername&gt;/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="1b5e2-181">http:// &lt; nomordinateur &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="1b5e2-181">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="1b5e2-182">http:// &lt; nomordinateur &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="1b5e2-182">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="1b5e2-183">http:// &lt; nomordinateur &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="1b5e2-183">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="1b5e2-184">Remarque</span><span class="sxs-lookup"><span data-stu-id="1b5e2-184">Note</span></span>**  
   <span data-ttu-id="1b5e2-185">En général, les services sont installés sur le port 80 par défaut sans chiffrement réseau.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-185">Typically, services are installed on the default port 80 without network encryption.</span></span> <span data-ttu-id="1b5e2-186">Si les services sont installés sur un autre port, modifiez les URL pour inclure le port approprié.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-186">If the services are installed on a different port, change the URLs to include the appropriate port.</span></span> <span data-ttu-id="1b5e2-187">Par exemple, http://\* &lt; nomordinateur &gt; : &lt; port &gt; \*/default.aspx ou http:// <em> &lt; hostheadername &gt; / </em> default. aspx</span><span class="sxs-lookup"><span data-stu-id="1b5e2-187">For example, http://*&lt;computername&gt;:&lt;port&gt;*/default.aspx or http://<em>&lt;hostheadername&gt;/</em>default.aspx</span></span>

   <span data-ttu-id="1b5e2-188">Si les services ont été installés en utilisant le chiffrement réseau, modifiez http://sur https://.</span><span class="sxs-lookup"><span data-stu-id="1b5e2-188">If the services were installed with network encryption, change http:// to https://.</span></span>



~~~
Verify that each web page loads successfully.
~~~

## <span data-ttu-id="1b5e2-189">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1b5e2-189">Related topics</span></span>


[<span data-ttu-id="1b5e2-190">Déploiement de l'infrastructure de serveur MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="1b5e2-190">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)









