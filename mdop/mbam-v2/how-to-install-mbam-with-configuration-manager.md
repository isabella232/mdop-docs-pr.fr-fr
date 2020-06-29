---
title: Installation de MBAM avec Configuration Manager
description: Installation de MBAM avec Configuration Manager
author: dansimp
ms.assetid: fd0832e4-3b79-4e56-9550-d2f396be6d09
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a556ce961e6a423caecdd0766cf8623383897b58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810968"
---
# <span data-ttu-id="dd39c-103">Installation de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="dd39c-103">How to Install MBAM with Configuration Manager</span></span>


<span data-ttu-id="dd39c-104">Cette section décrit la procédure d’installation d’MBAM avec Configuration Manager à l’aide de la configuration recommandée, illustrée dans la section [mise en route de MBAM avec Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="dd39c-104">This section describes the steps to install MBAM with Configuration Manager by using the recommended configuration, which is illustrated in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="dd39c-105">Les étapes sont divisées en tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="dd39c-105">The steps are divided into the following tasks:</span></span>

-   <span data-ttu-id="dd39c-106">Installer et configurer MBAM sur le serveur Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="dd39c-106">Install and configure MBAM on the Configuration Manager Server</span></span>

-   <span data-ttu-id="dd39c-107">Installer les bases de données de récupération et d’audit sur le serveur de base de données</span><span class="sxs-lookup"><span data-stu-id="dd39c-107">Install the Recovery and Audit Databases on the Database Server</span></span>

-   <span data-ttu-id="dd39c-108">Installer les fonctionnalités d’administration et de surveillance du serveur sur le serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="dd39c-108">Install the Administration and Monitoring Server features on the Administration and Monitoring Server</span></span>

<span data-ttu-id="dd39c-109">Avant de commencer l’installation, assurez-vous d’avoir modifié ou créé les fichiers MOF nécessaires.</span><span class="sxs-lookup"><span data-stu-id="dd39c-109">Before you begin the installation, ensure that you have edited or created the necessary mof files.</span></span> <span data-ttu-id="dd39c-110">Pour obtenir des instructions, reportez-vous [à création ou modification des fichiers MOF](how-to-create-or-edit-the-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="dd39c-110">For instructions, see [How to Create or Edit the mof Files](how-to-create-or-edit-the-mof-files.md).</span></span>

<span data-ttu-id="dd39c-111">**Important**  Si vous utilisez une instance de SQL Server Reporting Services (SSRS) qui n’est pas définie par défaut, vous devez démarrer la configuration d’MBAM à l’aide de la ligne de commande suivante pour spécifier l’instance nommée SSRS:</span><span class="sxs-lookup"><span data-stu-id="dd39c-111">**Important** If you are using a non-default SQL Server Reporting Services (SSRS) instance, you must start the MBAM Setup by using the following command line to specify the SSRS named instance:</span></span>

`MbamSetup.exe CM_SSRS_INSTANCE_NAME=<NamedInstance>`

 

**<span data-ttu-id="dd39c-112">Pour installer MBAM sur le serveur Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="dd39c-112">To install MBAM on the Configuration Manager Server</span></span>**

1.  <span data-ttu-id="dd39c-113">Sur le serveur Configuration Manager, exécutez **MBAMSetup.exe** pour démarrer l’Assistant Installation de MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd39c-113">On the Configuration Manager Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

    <span data-ttu-id="dd39c-114">**Remarques**  Pour obtenir les fichiers journaux d’installation, vous devez utiliser le package msiexec et l’option **/l** &lt; emplacement &gt; pour installer Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="dd39c-114">**Note** To obtain the setup log files, you have to use the Msiexec package and the **/L** &lt;location&gt; option to install Configuration Manager.</span></span> <span data-ttu-id="dd39c-115">Les fichiers journaux sont créés à l’emplacement que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="dd39c-115">Log files are created in the location that you specify.</span></span>

    <span data-ttu-id="dd39c-116">D’autres fichiers journaux d’installation sont créés dans le dossier% Temp% sur l’ordinateur de l’utilisateur qui installe le gestionnaire de configuration.</span><span class="sxs-lookup"><span data-stu-id="dd39c-116">Additional setup log files are created in the %temp% folder on the computer of the user who is installing Configuration Manager.</span></span>

     

2.  <span data-ttu-id="dd39c-117">Dans la page d' **Accueil** , sélectionnez éventuellement le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="dd39c-117">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="dd39c-118">Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="dd39c-118">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="dd39c-119">Dans la page de sélection de la **topologie** , sélectionnez **intégration de System Center Configuration Manager**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="dd39c-119">On the **Topology Selection** page, select **System Center Configuration Manager Integration**, and then click **Next**.</span></span>

5.  <span data-ttu-id="dd39c-120">Dans la page **Sélectionner les fonctionnalités à installer** , sélectionnez **intégration de System Center Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="dd39c-120">On the **Select features to install** page, select **System Center Configuration Manager Integration**.</span></span>

    <span data-ttu-id="dd39c-121">**Remarques**  Sur la page **vérification des éléments requis** , cliquez sur **suivant** lorsque l’Assistant installation vérifie la configuration requise pour votre installation et confirme qu’aucun élément n’est manquant.</span><span class="sxs-lookup"><span data-stu-id="dd39c-121">**Note** On the **Checking Prerequisites** page, click **Next** after the installation wizard checks the prerequisites for your installation and confirms that none are missing.</span></span> <span data-ttu-id="dd39c-122">Si une condition préalable manquante est détectée, vous devez résoudre les conditions préalables manquantes, puis cliquer de **nouveau sur vérifier les conditions préalables.**</span><span class="sxs-lookup"><span data-stu-id="dd39c-122">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again.**</span></span>

     

6.  <span data-ttu-id="dd39c-123">Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="dd39c-123">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="dd39c-124">L’utilisation des mises à jour de Microsoft n’active pas les mises à jour automatiques dans Windows.</span><span class="sxs-lookup"><span data-stu-id="dd39c-124">Using Microsoft Updates does not turn on Automatic Updates in Windows.</span></span>

7.  <span data-ttu-id="dd39c-125">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="dd39c-125">Click **Next** to continue.</span></span>

8.  <span data-ttu-id="dd39c-126">Dans la page Résumé de l' **installation** , examinez la liste des fonctionnalités qui seront installées, puis cliquez sur **installer** pour commencer à installer les fonctionnalités MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd39c-126">On the **Installation Summary** page, review the list of features that will be installed, and click **Install** to start installing the MBAM features.</span></span> <span data-ttu-id="dd39c-127">Cliquez sur **retour** pour revenir à l’Assistant pour revoir ou modifier vos paramètres d’installation ou cliquez sur **Annuler** pour quitter le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="dd39c-127">Click **Back** to move back through the wizard if you have to review or change your installation settings, or click **Cancel** to exit Setup.</span></span> <span data-ttu-id="dd39c-128">Le programme d’installation installe les fonctionnalités de MBAM et vous signale que l’installation est terminée.</span><span class="sxs-lookup"><span data-stu-id="dd39c-128">Setup installs the MBAM features and notifies you that the installation is completed.</span></span>

9.  <span data-ttu-id="dd39c-129">Cliquez sur **Terminer** pour quitter l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="dd39c-129">Click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="dd39c-130">Pour installer les bases de données de récupération et d’audit sur le serveur de base de données</span><span class="sxs-lookup"><span data-stu-id="dd39c-130">To install the Recovery and Audit Databases on the Database Server</span></span>**

1.  <span data-ttu-id="dd39c-131">Sur le serveur de base de données, exécutez **MBAMSetup.exe** pour démarrer l’Assistant Installation de MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd39c-131">On the Database Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="dd39c-132">Dans la page d' **Accueil** , sélectionnez éventuellement le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="dd39c-132">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="dd39c-133">Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="dd39c-133">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="dd39c-134">Dans la page de sélection de la **topologie** , sélectionnez la topologie **intégration de System Center Configuration Manager** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="dd39c-134">On the **Topology Selection** page, select the **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="dd39c-135">Dans la liste des fonctionnalités à installer, sélectionnez **base de données de récupération** et **base de données d’audit**, puis décochez les autres fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="dd39c-135">From the list of features to install, select **Recovery Database** and **Audit Database**, and clear the remaining features.</span></span>

    <span data-ttu-id="dd39c-136">**Remarques**  L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes.</span><span class="sxs-lookup"><span data-stu-id="dd39c-136">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="dd39c-137">Si toutes les conditions préalables sont remplies, l’installation continue.</span><span class="sxs-lookup"><span data-stu-id="dd39c-137">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="dd39c-138">Si une condition préalable manquante est détectée, vous devez résoudre les conditions préalables manquantes, puis cliquer de **nouveau sur vérifier les conditions préalables**.</span><span class="sxs-lookup"><span data-stu-id="dd39c-138">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="dd39c-139">Si toutes les conditions préalables sont remplies ce délai, l’installation reprend.</span><span class="sxs-lookup"><span data-stu-id="dd39c-139">If all prerequisites are met this time, the installation resumes.</span></span>

     

6.  <span data-ttu-id="dd39c-140">Dans la page **configurer la base de données de récupération** , spécifiez les noms des ordinateurs qui exécutent la fonctionnalité d’administration et de surveillance du serveur.</span><span class="sxs-lookup"><span data-stu-id="dd39c-140">On the **Configure the Recovery Database** page, specify the names of the computers that will be running the Administration and Monitoring Server feature.</span></span> <span data-ttu-id="dd39c-141">Après le déploiement de la fonctionnalité d’administration et de surveillance du serveur, il utilise son compte de domaine pour se connecter à la base de données.</span><span class="sxs-lookup"><span data-stu-id="dd39c-141">After the Administration and Monitoring Server feature is deployed, it uses its domain account to connect to the database.</span></span>

7.  <span data-ttu-id="dd39c-142">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="dd39c-142">Click **Next** to continue.</span></span>

8.  <span data-ttu-id="dd39c-143">Spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données de récupération.</span><span class="sxs-lookup"><span data-stu-id="dd39c-143">Specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="dd39c-144">Vous devez également spécifier l’emplacement de la base de données et l’emplacement où se trouvent les informations de journalisation.</span><span class="sxs-lookup"><span data-stu-id="dd39c-144">You must also specify both where the database will be located and where the log information will be located.</span></span>

9.  <span data-ttu-id="dd39c-145">Cliquez sur **suivant** pour continuer avec l’Assistant Installation de MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd39c-145">Click **Next** to continue with the MBAM Setup installation wizard.</span></span>

10. <span data-ttu-id="dd39c-146">Dans la page **configurer la base de données d’audit** , spécifiez le compte d’utilisateur qui sera utilisé pour accéder à la base de données pour les rapports.</span><span class="sxs-lookup"><span data-stu-id="dd39c-146">On the **Configure the Audit Database** page, specify the user account that will be used to access the database for reports.</span></span>

11. <span data-ttu-id="dd39c-147">Spécifiez le nom de l’ordinateur qui sera exécuté sur le serveur d’administration et de surveillance ainsi que les rapports d’audit.</span><span class="sxs-lookup"><span data-stu-id="dd39c-147">Specify the computer names of the computers that will be running the Administration and Monitoring Server and the Audit Reports.</span></span> <span data-ttu-id="dd39c-148">Après le déploiement des fonctionnalités d’administration et de surveillance et des rapports d’audit, leurs comptes de domaine sont utilisés pour se connecter aux bases de données.</span><span class="sxs-lookup"><span data-stu-id="dd39c-148">After the Administration and Monitoring and the Audit Reports features are deployed, their domain accounts will be used to connect to the databases.</span></span>

    <span data-ttu-id="dd39c-149">**Remarques**  Si vous installez la base de données d’audit sans la fonctionnalité rapports d’audit, vous devez ajouter une exception sur l’ordinateur de la base de données d’audit pour activer le trafic entrant sur le port Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dd39c-149">**Note** If you are installing the Audit Database without the Audit Reports feature, you must add an exception on the Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="dd39c-150">Le numéro de port par défaut est 1433.</span><span class="sxs-lookup"><span data-stu-id="dd39c-150">The default port number is 1433.</span></span>

     

12. <span data-ttu-id="dd39c-151">Spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données d’audit.</span><span class="sxs-lookup"><span data-stu-id="dd39c-151">Specify the SQL Server instance name and the name of the database that will store the audit data.</span></span> <span data-ttu-id="dd39c-152">Vous devez également spécifier l’emplacement des informations de base de données et de journalisation.</span><span class="sxs-lookup"><span data-stu-id="dd39c-152">You must also specify where the database and log information will be located.</span></span>

13. <span data-ttu-id="dd39c-153">Cliquez sur **installer** pour démarrer l’installation, puis cliquez sur **Terminer** pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="dd39c-153">Click **Install** to start the installation, and then click **Finish** to complete the installation.</span></span>

**<span data-ttu-id="dd39c-154">Pour installer les fonctionnalités d’administration et de surveillance du serveur sur le serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="dd39c-154">To install the Administration and Monitoring Server features on the Administration and Monitoring Server</span></span>**

1.  <span data-ttu-id="dd39c-155">Sur le serveur d’administration et de surveillance, exécutez **MBAMSetup.exe** pour démarrer l’Assistant Installation de MBAM.</span><span class="sxs-lookup"><span data-stu-id="dd39c-155">On the Administration and Monitoring Server, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="dd39c-156">Dans la page d' **Accueil** , sélectionnez éventuellement le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="dd39c-156">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="dd39c-157">Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="dd39c-157">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="dd39c-158">Dans la page de sélection de la **topologie** , sélectionnez la topologie **intégration de System Center Configuration Manager** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="dd39c-158">On the **Topology Selection** page, select the **System Center Configuration Manager Integration** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="dd39c-159">Dans la liste des fonctionnalités à installer, sélectionnez **administration et analyse du serveur** et du **portail libre-service**, puis désactivez les autres fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="dd39c-159">From the list of features to install, select **Administration and Monitoring Server** and **Self-Service Portal**, and clear the remaining features.</span></span>

    <span data-ttu-id="dd39c-160">**Remarques**  L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes.</span><span class="sxs-lookup"><span data-stu-id="dd39c-160">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="dd39c-161">Si toutes les conditions préalables sont remplies, l’installation continue.</span><span class="sxs-lookup"><span data-stu-id="dd39c-161">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="dd39c-162">Si une condition préalable manquante est détectée, vous devez résoudre les conditions préalables manquantes, puis cliquer de **nouveau sur vérifier les conditions préalables**.</span><span class="sxs-lookup"><span data-stu-id="dd39c-162">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="dd39c-163">Si toutes les conditions préalables sont remplies ce délai, l’installation reprend.</span><span class="sxs-lookup"><span data-stu-id="dd39c-163">If all prerequisites are met this time, the installation resumes.</span></span>

     

6.  <span data-ttu-id="dd39c-164">Installez le portail libre-service en suivant les étapes décrites dans la section **installation du portail libre-service** de l' [installation et de la configuration de MBAM sur des serveurs distribués](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="dd39c-164">Install the Self-Service Portal by following the steps in the **To install the Self-Service Portal** section in [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span></span>

    <span data-ttu-id="dd39c-165">**Remarques**  Si les ordinateurs clients n’ont pas accès au réseau de distribution de contenu (CDN) Microsoft, ce qui donne au portail libre-service l’accès requis à certains fichiers JavaScript, suivez les étapes décrites dans la section **pour configurer le portail libre-service lorsque les utilisateurs ne peuvent pas accéder à la section sur le réseau de distribution de contenu Microsoft** [Comment installer et configurer MBAM sur des serveurs distribués](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) pour configurer le portail libre-service de manière à référencer les fichiers JavaScript à partir d’une source accessible.</span><span class="sxs-lookup"><span data-stu-id="dd39c-165">**Note** If the client computers will not have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, complete the steps in the **To configure the Self-Service Portal when end users cannot access the Microsoft Content Delivery Network** section [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

     

7.  <span data-ttu-id="dd39c-166">Installez les fonctionnalités d’administration et de surveillance du serveur en suivant les étapes décrites dans la section **installation de la fonctionnalité d’administration et de surveillance du serveur** dans [Comment installer et configurer MBAM sur des serveurs distribués](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="dd39c-166">Install the Administration and Monitoring Server features by following the steps in the **To install the Administration and Monitoring Server feature** section in [How to Install and Configure MBAM on Distributed Servers](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).</span></span>

8.  <span data-ttu-id="dd39c-167">Cliquez sur **Terminer** pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="dd39c-167">Click **Finish** to complete the installation.</span></span>

## <span data-ttu-id="dd39c-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dd39c-168">Related topics</span></span>


[<span data-ttu-id="dd39c-169">Validation de l'installation de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="dd39c-169">How to Validate the MBAM Installation with Configuration Manager</span></span>](how-to-validate-the-mbam-installation-with-configuration-manager.md)

[<span data-ttu-id="dd39c-170">Déploiement de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="dd39c-170">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





