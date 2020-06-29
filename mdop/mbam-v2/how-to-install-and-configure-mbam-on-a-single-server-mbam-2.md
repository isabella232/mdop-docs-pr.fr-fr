---
title: Installation et configuration de MBAM sur un seul serveur
description: Installation et configuration de MBAM sur un seul serveur
author: dansimp
ms.assetid: 45e6a012-6c8c-4d90-902c-d09de9a0cbea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53e170f421bdce8dd6f771af3902af627a15a085
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810332"
---
# <span data-ttu-id="f05f4-103">Installation et configuration de MBAM sur un seul serveur</span><span class="sxs-lookup"><span data-stu-id="f05f4-103">How to Install and Configure MBAM on a Single Server</span></span>


<span data-ttu-id="f05f4-104">Les procédures décrites dans cette rubrique expliquent comment installer l’administration et la surveillance de BitLocker Microsoft (MBAM) dans la topologie autonome sur un serveur unique.</span><span class="sxs-lookup"><span data-stu-id="f05f4-104">The procedures in this topic describe how to install Microsoft BitLocker Administration and Monitoring (MBAM) in the Stand-alone topology on a single server.</span></span> <span data-ttu-id="f05f4-105">Utilisez la configuration serveur unique uniquement dans un environnement de test.</span><span class="sxs-lookup"><span data-stu-id="f05f4-105">Use the single-server configuration only in a test environment.</span></span> <span data-ttu-id="f05f4-106">Pour les environnements de production, utilisez au moins deux serveurs.</span><span class="sxs-lookup"><span data-stu-id="f05f4-106">For production environments, use two or more servers.</span></span> <span data-ttu-id="f05f4-107">Si vous installez le contrôle et l’administration de BitLocker à l’aide de la topologie Configuration Manager, consultez [déploiement d’MBAM avec Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="f05f4-107">If you are installing Microsoft BitLocker Administration and Monitoring by using the Configuration Manager topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>

<span data-ttu-id="f05f4-108">Le schéma suivant illustre un exemple d’architecture à un serveur unique.</span><span class="sxs-lookup"><span data-stu-id="f05f4-108">The following diagram shows an example of a single-server architecture.</span></span> <span data-ttu-id="f05f4-109">Pour obtenir une description des bases de données et fonctionnalités, voir [architecture de haut niveau pour MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="f05f4-109">For a description of the databases and features, see [High-Level Architecture for MBAM 2.0](high-level-architecture-for-mbam-20-mbam-2.md).</span></span>

![topologie de déploiement de serveur unique MBAM 2](images/mbam2-1-server.gif)

<span data-ttu-id="f05f4-111">Chaque fonctionnalité de serveur comporte certaines conditions préalables.</span><span class="sxs-lookup"><span data-stu-id="f05f4-111">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="f05f4-112">Pour vérifier que vous remplissez les conditions préalables et que vous avez besoin de la configuration matérielle et logicielle requise, voir Configuration requise pour le [déploiement d’MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md) et [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="f05f4-112">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="f05f4-113">De plus, certaines fonctions disposent également d’informations qui doivent être fournies pendant le processus d’installation pour le déploiement de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="f05f4-113">In addition, some features also have information that must be provided during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="f05f4-114">Vous devez également consulter [préparer votre environnement pour MBAM 2,0 avant de](preparing-your-environment-for-mbam-20-mbam-2.md) commencer MBAM déploiement.</span><span class="sxs-lookup"><span data-stu-id="f05f4-114">You should also review [Preparing your Environment for MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md) before you start MBAM deployment.</span></span>

**<span data-ttu-id="f05f4-115">Remarque</span><span class="sxs-lookup"><span data-stu-id="f05f4-115">Note</span></span>**  
<span data-ttu-id="f05f4-116">Pour obtenir les fichiers journaux d’installation, vous devez utiliser le package msiexec et l’option **/l** &lt; emplacement &gt; pour installer MBAM.</span><span class="sxs-lookup"><span data-stu-id="f05f4-116">To obtain the setup log files, you have use the Msiexec package and the **/L** &lt;location&gt; option to install MBAM.</span></span> <span data-ttu-id="f05f4-117">Les fichiers journaux sont créés à l’emplacement que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="f05f4-117">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="f05f4-118">D’autres fichiers journaux d’installation sont créés dans le dossier% Temp% sur le serveur de l’utilisateur qui installe MBAM.</span><span class="sxs-lookup"><span data-stu-id="f05f4-118">Additional setup log files are created in the %temp% folder on the server of the user who is installing MBAM.</span></span>



## <span data-ttu-id="f05f4-119">Pour installer les fonctionnalités du serveur MBAM sur un serveur unique</span><span class="sxs-lookup"><span data-stu-id="f05f4-119">To install MBAM Server features on a single server</span></span>


<span data-ttu-id="f05f4-120">Les étapes suivantes expliquent comment installer les fonctionnalités MBAM générales.</span><span class="sxs-lookup"><span data-stu-id="f05f4-120">The following steps describe how to install general MBAM features.</span></span>

**<span data-ttu-id="f05f4-121">Pour démarrer l’installation de fonctionnalités de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="f05f4-121">To start the MBAM Server features installation</span></span>**

1.  <span data-ttu-id="f05f4-122">Sur le serveur sur lequel vous souhaitez installer MBAM, exécutez **MBAMSetup.exe** pour démarrer l’Assistant Installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="f05f4-122">On the server where you want to install MBAM, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="f05f4-123">Dans la page d' **Accueil** , sélectionnez éventuellement le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="f05f4-123">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="f05f4-124">Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="f05f4-124">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="f05f4-125">Dans la page de sélection de la **topologie** , sélectionnez la topologie **autonome** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="f05f4-125">On the **Topology Selection** page, select the **Stand-alone** topology, and then click **Next**.</span></span>

5.  <span data-ttu-id="f05f4-126">Dans la page **Sélectionner les fonctionnalités à installer** , sélectionnez les fonctionnalités que vous voulez installer.</span><span class="sxs-lookup"><span data-stu-id="f05f4-126">On the **Select features to install** page, select the features that you want to install.</span></span> <span data-ttu-id="f05f4-127">Par défaut, toutes les fonctionnalités de MBAM sont sélectionnées pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="f05f4-127">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="f05f4-128">Les fonctionnalités qui doivent être installées sur le même ordinateur doivent être installées en même temps.</span><span class="sxs-lookup"><span data-stu-id="f05f4-128">Features that are to be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="f05f4-129">Désactivez les cases à cocher des fonctionnalités que vous voulez installer ailleurs.</span><span class="sxs-lookup"><span data-stu-id="f05f4-129">Clear the check boxes for any features that you want to install elsewhere.</span></span> <span data-ttu-id="f05f4-130">Vous devez installer les fonctionnalités d’MBAM dans l’ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="f05f4-130">You must install MBAM features in the following order:</span></span>

    -   <span data-ttu-id="f05f4-131">Base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="f05f4-131">Recovery Database</span></span>

    -   <span data-ttu-id="f05f4-132">Base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="f05f4-132">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="f05f4-133">Rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="f05f4-133">Compliance and Audit Reports</span></span>

    -   <span data-ttu-id="f05f4-134">Serveur libre-service</span><span class="sxs-lookup"><span data-stu-id="f05f4-134">Self-Service Server</span></span>

    -   <span data-ttu-id="f05f4-135">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="f05f4-135">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="f05f4-136">Modèle de stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="f05f4-136">MBAM Group Policy template</span></span>

    **<span data-ttu-id="f05f4-137">Remarque</span><span class="sxs-lookup"><span data-stu-id="f05f4-137">Note</span></span>**  
    <span data-ttu-id="f05f4-138">L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes.</span><span class="sxs-lookup"><span data-stu-id="f05f4-138">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="f05f4-139">Si toutes les conditions préalables sont remplies, l’installation continue.</span><span class="sxs-lookup"><span data-stu-id="f05f4-139">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="f05f4-140">Si une condition préalable manquante est détectée, vous devez résoudre les conditions préalables manquantes, puis cliquer de **nouveau sur vérifier les conditions préalables**.</span><span class="sxs-lookup"><span data-stu-id="f05f4-140">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="f05f4-141">Si toutes les conditions préalables sont remplies ce délai, l’installation reprend.</span><span class="sxs-lookup"><span data-stu-id="f05f4-141">If all prerequisites are met this time, the installation resumes.</span></span>



6.  <span data-ttu-id="f05f4-142">Dans la page **configure Network Communication Security** , choisissez de chiffrer les communications entre les services Web sur le serveur d’administration et de surveillance et les clients.</span><span class="sxs-lookup"><span data-stu-id="f05f4-142">On the **Configure network communication security** page, choose whether to encrypt the communication between the Web Services on the Administration and Monitoring Server and the clients.</span></span> <span data-ttu-id="f05f4-143">Si vous décidez de chiffrer la communication, sélectionnez le certificat de certification d’autorité de certification à utiliser pour le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="f05f4-143">If you decide to encrypt the communication, select the certification authority-provisioned certificate to use for encryption.</span></span> <span data-ttu-id="f05f4-144">Le certificat doit être créé avant cette étape pour vous permettre de le sélectionner dans cette page.</span><span class="sxs-lookup"><span data-stu-id="f05f4-144">The certificate must be created prior to this step to enable you to select it on this page.</span></span>

    **<span data-ttu-id="f05f4-145">Remarque</span><span class="sxs-lookup"><span data-stu-id="f05f4-145">Note</span></span>**  
    <span data-ttu-id="f05f4-146">Cette page s’affiche uniquement si vous avez sélectionné le portail libre-service ou la fonctionnalité de serveur administration et analyse dans la page **Sélectionner les fonctionnalités à installer** .</span><span class="sxs-lookup"><span data-stu-id="f05f4-146">This page appears only if you selected the Self-Service Portal or the Administration and Monitoring Server feature on the **Select features to install** page.</span></span>



7.  <span data-ttu-id="f05f4-147">Cliquez sur **suivant**, puis passez aux étapes suivantes pour configurer les fonctionnalités du serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="f05f4-147">Click **Next**, and then continue to the next set of steps to configure the MBAM Server features.</span></span>

**<span data-ttu-id="f05f4-148">Pour configurer les fonctionnalités du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="f05f4-148">To configure the MBAM Server features</span></span>**

1.  <span data-ttu-id="f05f4-149">Sur la page **configurer la base de données de récupération** , spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données de récupération.</span><span class="sxs-lookup"><span data-stu-id="f05f4-149">On the **Configure the Recovery database** page, specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="f05f4-150">Vous devez également spécifier les emplacements où se trouvent les fichiers de base de données et l’emplacement où se trouvent les informations de journalisation.</span><span class="sxs-lookup"><span data-stu-id="f05f4-150">You must also specify both where the database files will be located and where the log information will be located.</span></span>

2.  <span data-ttu-id="f05f4-151">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="f05f4-151">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="f05f4-152">Sur la page **configurer la conformité et la base de données d’audit** , spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="f05f4-152">On the **Configure the Compliance and Audit database** page, specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="f05f4-153">Vous devez également spécifier l’emplacement où se trouvent les fichiers de base de données et l’emplacement où se trouvent les informations de journalisation.</span><span class="sxs-lookup"><span data-stu-id="f05f4-153">You must also specify where the database files will be located and where the log information will be located.</span></span>

4.  <span data-ttu-id="f05f4-154">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="f05f4-154">Click **Next** to continue.</span></span>

5.  <span data-ttu-id="f05f4-155">Sur la page **configurer les rapports de conformité et d’audit** , spécifiez l’instance de SQL Server Reporting Services dans laquelle les rapports de conformité et d’audit seront installés, puis fournissez un compte d’utilisateur et un mot de passe de domaine pour accéder à la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="f05f4-155">On the **Configure the Compliance and Audit Reports** page, specify the SQL Server Reporting Services instance where the Compliance and Audit reports will be installed, and provide a domain user account and password for accessing the Compliance and Audit database.</span></span> <span data-ttu-id="f05f4-156">Configurez le mot de passe de ce compte pour qu’il n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="f05f4-156">Configure the password for this account to never expire.</span></span> <span data-ttu-id="f05f4-157">Le compte d’utilisateur doit être en mesure d’accéder à toutes les données disponibles dans le groupe utilisateurs de reports MBAM.</span><span class="sxs-lookup"><span data-stu-id="f05f4-157">The user account should be able to access all data available to the MBAM Reports Users group.</span></span>

6.  <span data-ttu-id="f05f4-158">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="f05f4-158">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="f05f4-159">Dans la page **configurer le portail libre-service** , entrez le numéro de port, le nom d’hôte, le nom du répertoire virtuel et le chemin d’installation du portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="f05f4-159">On the **Configure the Self-Service Portal** page, enter the port number, host name, virtual directory name, and installation path for the Self-Service Portal.</span></span>

    **<span data-ttu-id="f05f4-160">Remarque</span><span class="sxs-lookup"><span data-stu-id="f05f4-160">Note</span></span>**  
    <span data-ttu-id="f05f4-161">Le numéro de port que vous spécifiez doit être un numéro de port inutilisé sur le serveur d’administration et de surveillance sauf si vous spécifiez un nom d’en-tête d’hôte unique.</span><span class="sxs-lookup"><span data-stu-id="f05f4-161">The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span> <span data-ttu-id="f05f4-162">Si vous utilisez le pare-feu Windows, le port s’ouvre automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f05f4-162">If you are using Windows Firewall, the port will be opened automatically.</span></span>



8.  <span data-ttu-id="f05f4-163">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="f05f4-163">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="f05f4-164">Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="f05f4-164">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span> <span data-ttu-id="f05f4-165">Les mises à jour automatiques ne sont pas activées dans Windows.</span><span class="sxs-lookup"><span data-stu-id="f05f4-165">This does not turn on Automatic Updates in Windows.</span></span>

10. <span data-ttu-id="f05f4-166">Sur la page **configurer le serveur d’administration et de surveillance** , entrez le numéro de port, le nom d’hôte, le nom du répertoire virtuel et le chemin d’installation du support technique du support technique.</span><span class="sxs-lookup"><span data-stu-id="f05f4-166">On the **Configure the Administration and Monitoring Server** page, enter the port number, host name, virtual directory name, and installation path for the Help Desk website.</span></span>

    **<span data-ttu-id="f05f4-167">Remarque</span><span class="sxs-lookup"><span data-stu-id="f05f4-167">Note</span></span>**  
    <span data-ttu-id="f05f4-168">Le numéro de port que vous spécifiez doit être un numéro de port inutilisé sur le serveur d’administration et de surveillance sauf si vous spécifiez un nom d’en-tête d’hôte unique.</span><span class="sxs-lookup"><span data-stu-id="f05f4-168">The port number that you specify must be an unused port number on the Administration and Monitoring Server unless you specify a unique host header name.</span></span> <span data-ttu-id="f05f4-169">Si vous utilisez le pare-feu Windows, le port s’ouvre automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f05f4-169">If you are using Windows Firewall, the port will be opened automatically.</span></span>



11. <span data-ttu-id="f05f4-170">Dans la page Résumé de l' **installation** , examinez la liste des fonctionnalités qui seront installées, puis cliquez sur **installer** pour commencer à installer les fonctionnalités MBAM.</span><span class="sxs-lookup"><span data-stu-id="f05f4-170">On the **Installation Summary** page, review the list of features that will be installed, and click **Install** to start installing the MBAM features.</span></span> <span data-ttu-id="f05f4-171">Cliquez sur **retour** pour revenir à l’Assistant pour revoir ou modifier vos paramètres d’installation ou cliquez sur **Annuler** pour quitter le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="f05f4-171">Click **Back** to move back through the wizard if you have to review or change your installation settings, or click **Cancel** to exit Setup.</span></span> <span data-ttu-id="f05f4-172">Le programme d’installation installe les fonctionnalités de MBAM et vous signale que l’installation est terminée.</span><span class="sxs-lookup"><span data-stu-id="f05f4-172">Setup installs the MBAM features and notifies you that the installation is complete.</span></span>

12. <span data-ttu-id="f05f4-173">Cliquez sur **Terminer** pour quitter l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="f05f4-173">Click **Finish** to exit the wizard.</span></span> <span data-ttu-id="f05f4-174">Une fois les fonctionnalités d’administration et de contrôle du serveur Microsoft BitLocker installées, passez à la section suivante et suivez les étapes nécessaires pour ajouter des utilisateurs aux rôles d’administration et de contrôle Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f05f4-174">After the Microsoft BitLocker Administration and Monitoring Server features have been installed, continue to the next section and complete the steps have to add users to the Microsoft BitLocker Administration and Monitoring roles.</span></span> <span data-ttu-id="f05f4-175">Pour plus d’informations sur les rôles, voir [planification des rôles d’administrateur MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="f05f4-175">For more information about roles, see [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).</span></span>

**<span data-ttu-id="f05f4-176">Pour effectuer une configuration après l’installation</span><span class="sxs-lookup"><span data-stu-id="f05f4-176">To perform post-installation configuration</span></span>**

1.  <span data-ttu-id="f05f4-177">Sur le serveur d’administration et de surveillance, ajoutez des utilisateurs aux groupes locaux suivants pour leur permettre d’accéder aux fonctionnalités de site Web du support technique MBAM:</span><span class="sxs-lookup"><span data-stu-id="f05f4-177">On the Administration and Monitoring Server, add users to the following local groups to give them access to the MBAM Help Desk website features:</span></span>

    -   <span data-ttu-id="f05f4-178">**Utilisateurs du support technique MBAM**: les membres de ce groupe local peuvent accéder à la récupération du lecteur et gérer les fonctionnalités du TPM sur le site Web d’administration et de surveillance MBAM.</span><span class="sxs-lookup"><span data-stu-id="f05f4-178">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="f05f4-179">Pour un utilisateur du support technique, tous les champs de la récupération de lecteur et de la gestion de TPM sont obligatoires.</span><span class="sxs-lookup"><span data-stu-id="f05f4-179">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="f05f4-180">**Utilisateurs de l’assistance technique avancée MBAM**: les membres de ce groupe local disposent d’un accès avancé aux fonctionnalités de récupération et de gestion du TPM sur le site Web d’administration et de surveillance des MBAM.</span><span class="sxs-lookup"><span data-stu-id="f05f4-180">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="f05f4-181">Pour les utilisateurs expérimentés du support technique, seul le champ **ID clé** est requis pour la récupération du lecteur.</span><span class="sxs-lookup"><span data-stu-id="f05f4-181">For Advanced Helpdesk Users, only the **Key ID** field is required in Drive Recovery.</span></span> <span data-ttu-id="f05f4-182">Dans gérer le module de plateforme sécurisée, seul le champ domaine de l' **ordinateur** et le champ nom de l' **ordinateur** est requis.</span><span class="sxs-lookup"><span data-stu-id="f05f4-182">In Manage TPM, only the **Computer Domain** field and **Computer Name** field are required.</span></span>

2.  <span data-ttu-id="f05f4-183">Sur le serveur d’administration et de surveillance, ajoutez des utilisateurs au groupe local suivant pour leur permettre d’accéder à la fonctionnalité rapports sur le site Web d’administration et de surveillance de MBAM:</span><span class="sxs-lookup"><span data-stu-id="f05f4-183">On the Administration and Monitoring Server, add users to the following local group to enable them to access the Reports feature on the MBAM Administration and Monitoring website:</span></span>

    -   <span data-ttu-id="f05f4-184">**Utilisateurs du rapport MBAM**: les membres de ce groupe local peuvent accéder aux fonctionnalités de rapport sur le site Web d’administration et de surveillance de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f05f4-184">**MBAM Report Users**: Members of this local group can access the Reports features on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="f05f4-185">Marquez le portail libre-service avec le nom de votre société, le texte du message d’avis et d’autres informations spécifiques à la société.</span><span class="sxs-lookup"><span data-stu-id="f05f4-185">Brand the Self-Service Portal with your company name, notice text, and other company-specific information.</span></span> <span data-ttu-id="f05f4-186">Pour obtenir des instructions, reportez-vous [à la rubrique Personnalisation du portail libre-service](how-to-brand-the-self-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="f05f4-186">For instructions, see [How to Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md).</span></span>

    **<span data-ttu-id="f05f4-187">Remarque</span><span class="sxs-lookup"><span data-stu-id="f05f4-187">Note</span></span>**  
    <span data-ttu-id="f05f4-188">Il est possible d’avoir une appartenance similaire à un utilisateur ou un groupe du groupe local **utilisateurs de rapports MBAM** sur tous les ordinateurs sur lesquels les fonctionnalités d’administration et de surveillance des MBAM, ainsi que les rapports de conformité et d’audit sont installés.</span><span class="sxs-lookup"><span data-stu-id="f05f4-188">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span> <span data-ttu-id="f05f4-189">Pour cela, nous vous recommandons de créer un groupe de sécurité de domaine et d’ajouter ce groupe de domaine à chaque groupe de utilisateurs de rapport MBAM local.</span><span class="sxs-lookup"><span data-stu-id="f05f4-189">The recommended way to do this is to create a domain security group and add that domain group to each local MBAM Report Users group.</span></span> <span data-ttu-id="f05f4-190">Lorsque vous utilisez ce processus, gérez les appartenances aux groupes par le biais du groupe de domaines.</span><span class="sxs-lookup"><span data-stu-id="f05f4-190">When you use this process, manage the group memberships by way of the domain group.</span></span>



## <span data-ttu-id="f05f4-191">Validation de l’installation de la fonctionnalité MBAM Server</span><span class="sxs-lookup"><span data-stu-id="f05f4-191">Validating the MBAM Server feature installation</span></span>


<span data-ttu-id="f05f4-192">Lorsque l’installation de l’administration et du suivi de BitLocker est terminée, vérifiez que l’installation a correctement configuré toutes les fonctionnalités MBAM nécessaires pour la gestion de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f05f4-192">When the Microsoft BitLocker Administration and Monitoring installation is completed, validate that the installation has successfully set up all the necessary MBAM features that are required for BitLocker management.</span></span> <span data-ttu-id="f05f4-193">Utilisez la procédure suivante pour vérifier que le service MBAM est fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="f05f4-193">Use the following procedure to confirm that the MBAM service is functional.</span></span>

**<span data-ttu-id="f05f4-194">Pour valider l’installation de la fonctionnalité MBAM Server</span><span class="sxs-lookup"><span data-stu-id="f05f4-194">To validate the MBAM Server feature installation</span></span>**

1. <span data-ttu-id="f05f4-195">Sur chaque serveur sur lequel est déployée une fonctionnalité MBAM, ouvrez **le panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="f05f4-195">On each server where a MBAM feature is deployed, open **Control Panel**.</span></span> <span data-ttu-id="f05f4-196">Sélectionnez **programmes**, puis sélectionnez **programmes et fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="f05f4-196">Select **Programs**, and then select **Programs and Features**.</span></span> <span data-ttu-id="f05f4-197">Vérifiez que la fonctionnalité **administration et analyse de BitLocker Microsoft** s’affiche dans la liste **programmes et fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="f05f4-197">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="f05f4-198">Remarque</span><span class="sxs-lookup"><span data-stu-id="f05f4-198">Note</span></span>**  
   <span data-ttu-id="f05f4-199">Pour valider l’installation, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="f05f4-199">To validate the installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="f05f4-200">Sur le serveur sur lequel la base de données de récupération est installée, ouvrez SQL Server Management Studio, puis vérifiez que la base de données **MBAM et de récupération** de la base de données est installée.</span><span class="sxs-lookup"><span data-stu-id="f05f4-200">On the server where the Recovery Database is installed, open SQL Server Management Studio, and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="f05f4-201">Sur le serveur sur lequel la base de données d’audit et de conformité est installée, ouvrez SQL Server Management Studio, puis vérifiez que la **base de données de statut de conformité MBAM** est installée.</span><span class="sxs-lookup"><span data-stu-id="f05f4-201">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio, and verify that the **MBAM Compliance Status Database** is installed.</span></span>

4. <span data-ttu-id="f05f4-202">Sur le serveur sur lequel sont installés les rapports de conformité et d’audit, ouvrez un navigateur Web contenant les informations d’identification d’administration et naviguez jusqu’au site «Home» du site SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="f05f4-202">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative credentials and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="f05f4-203">L’emplacement d’accueil par défaut d’une instance de site SQL Server Reporting Services se trouve sur http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports.</span><span class="sxs-lookup"><span data-stu-id="f05f4-203">The default Home location of a SQL Server Reporting Services site instance is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.</span></span> <span data-ttu-id="f05f4-204">Pour trouver l’URL réelle, utilisez l’outil Gestionnaire de configuration Reporting Services et sélectionnez les instances spécifiées lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="f05f4-204">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that are specified during setup.</span></span>

   <span data-ttu-id="f05f4-205">Confirmez qu’un dossier de rapports intitulé Microsoft BitLocker administration et analyse contient une source de données appelée **MaltaDataSource** et qu’un dossier **en-US** contient quatre rapports.</span><span class="sxs-lookup"><span data-stu-id="f05f4-205">Confirm that a Reports folder named Microsoft BitLocker Administration and Monitoring contains a data source called **MaltaDataSource** and that an **en-us** folder contains four reports.</span></span>

   **<span data-ttu-id="f05f4-206">Remarque</span><span class="sxs-lookup"><span data-stu-id="f05f4-206">Note</span></span>**  
   <span data-ttu-id="f05f4-207">Si SQL Server Reporting Services a été configuré en tant qu’instance nommée, l’URL doit ressembler à ce qui suit: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="f05f4-207">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following: http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. <span data-ttu-id="f05f4-208">Sur le serveur sur lequel est installée la fonctionnalité d’administration et de surveillance, exécutez le **Gestionnaire de serveur** et naviguez jusqu’à **rôles**.</span><span class="sxs-lookup"><span data-stu-id="f05f4-208">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**.</span></span> <span data-ttu-id="f05f4-209">Sélectionnez **serveur Web (IIS)**, puis cliquez sur **Gestionnaire des services Internet (IIS).**</span><span class="sxs-lookup"><span data-stu-id="f05f4-209">Select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager.**</span></span>

6. <span data-ttu-id="f05f4-210">Dans **connexions,** naviguez jusqu’à \* &lt; &gt; nomordinateur\*, sélectionnez **sites**, puis cliquez sur **analyse et analyse BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="f05f4-210">In **Connections,** browse to *&lt;computername&gt;*, select **Sites**, and then select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="f05f4-211">Vérifiez que **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**et **MBAMRecoveryAndHardwareService** sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="f05f4-211">Verify that **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="f05f4-212">Sur le serveur sur lequel sont installés les fonctionnalités d’administration et de surveillance et de portail en libre-service, ouvrez un navigateur Web contenant les informations d’identification d’administration et naviguez jusqu’aux emplacements suivants pour vérifier qu’ils se chargent correctement:</span><span class="sxs-lookup"><span data-stu-id="f05f4-212">On the server where the Administration and Monitoring features and Self-Service Portal are installed, open a web browser with administrative credentials and browse to the following locations to verify that they load successfully:</span></span>

   -   <span data-ttu-id="f05f4-213">*http:// &lt; hostname &gt; /helpdesk/default.aspx* et confirmez chacun des liens pour la navigation et les rapports</span><span class="sxs-lookup"><span data-stu-id="f05f4-213">*http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports</span></span>

   -   *<span data-ttu-id="f05f4-214">http:// &lt; hostname &gt; /selfservice&gt;/</span><span class="sxs-lookup"><span data-stu-id="f05f4-214">http://&lt;hostname&gt;/SelfService&gt;/</span></span>*

   -   *<span data-ttu-id="f05f4-215">http:// &lt; nomordinateur &gt; /MBAMAdministrationService/AdministrationService.svc</span><span class="sxs-lookup"><span data-stu-id="f05f4-215">http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc</span></span>*

   -   *<span data-ttu-id="f05f4-216">http:// &lt; hostname &gt; /MBAMUserSupportService/UserSupportService.svc</span><span class="sxs-lookup"><span data-stu-id="f05f4-216">http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc</span></span>*

   -   *<span data-ttu-id="f05f4-217">http:// &lt; nomordinateur &gt; /MBAMComplianceStatusService/StatusReportingService.svc</span><span class="sxs-lookup"><span data-stu-id="f05f4-217">http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc</span></span>*

   -   *<span data-ttu-id="f05f4-218">http:// &lt; nomordinateur &gt; /MBAMRecoveryAndHardwareService/CoreService.svc</span><span class="sxs-lookup"><span data-stu-id="f05f4-218">http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc</span></span>*

   **<span data-ttu-id="f05f4-219">Remarque</span><span class="sxs-lookup"><span data-stu-id="f05f4-219">Note</span></span>**  
   <span data-ttu-id="f05f4-220">Les fonctionnalités du serveur sont supposées être installées sur le port par défaut sans chiffrement réseau.</span><span class="sxs-lookup"><span data-stu-id="f05f4-220">It is assumed that the server features were installed on the default port without network encryption.</span></span> <span data-ttu-id="f05f4-221">Si vous avez installé les fonctionnalités du serveur sur un autre port ou répertoire virtuel, modifiez les URL pour inclure le port approprié (par exemple, *http:// &lt; hostname &gt; : &lt; port &gt; /helpdesk/default.asp*x ou*http:// &lt; hostname &gt; : &lt; port &gt; / &lt; VirtualDirectory &gt; /default.aspx*</span><span class="sxs-lookup"><span data-stu-id="f05f4-221">If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.asp*x or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*</span></span>

   <span data-ttu-id="f05f4-222">Si les fonctionnalités du serveur ont été installées avec le chiffrement réseau, modifiez http://sur https://.</span><span class="sxs-lookup"><span data-stu-id="f05f4-222">If the server features were installed with network encryption, change http:// to https://.</span></span>



## <span data-ttu-id="f05f4-223">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f05f4-223">Related topics</span></span>


[<span data-ttu-id="f05f4-224">Déploiement de l'infrastructure de serveur MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="f05f4-224">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









