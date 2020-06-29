---
title: Installation et configuration de MBAM sur des serveurs distribués
description: Installation et configuration de MBAM sur des serveurs distribués
author: dansimp
ms.assetid: 67b91e6b-ae2e-4e47-9ef2-6819aba95976
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 841b894430d14604f0fd923703708d7a3f588c07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810326"
---
# <span data-ttu-id="cd6b5-103">Installation et configuration de MBAM sur des serveurs distribués</span><span class="sxs-lookup"><span data-stu-id="cd6b5-103">How to Install and Configure MBAM on Distributed Servers</span></span>


<span data-ttu-id="cd6b5-104">Les procédures décrites dans cette rubrique décrivent l’installation de Microsoft BitLocker administration et de la surveillance (MBAM) 2,0 dans la topologie autonome sur des serveurs distribués.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-104">The procedures in this topic describe how to install Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 in the Stand-alone topology on distributed servers.</span></span> <span data-ttu-id="cd6b5-105">Pour afficher un diagramme de l’architecture recommandée, ainsi qu’une description des bases de données et des fonctionnalités, reportez-vous à la rubrique [déploiement de l’infrastructure du serveur MBAM 2,0](deploying-the-mbam-20-server-infrastructure-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="cd6b5-105">To see a diagram of the recommended architecture, along with a description of the databases and features, see [Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md).</span></span> <span data-ttu-id="cd6b5-106">Pour installer et surveiller Microsoft BitLocker avec la topologie de Configuration Manager, consultez [déploiement d’MBAM avec Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="cd6b5-106">To install Microsoft BitLocker Administration and Monitoring with the Configuration Manager topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>

<span data-ttu-id="cd6b5-107">Chaque fonctionnalité de serveur comporte certaines conditions préalables.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-107">Each server feature has certain prerequisites.</span></span> <span data-ttu-id="cd6b5-108">Pour vérifier que vous remplissez les conditions préalables et que vous avez besoin de la configuration matérielle et logicielle requise, voir Configuration requise pour le [déploiement d’MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md) et [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="cd6b5-108">To verify that you have met the prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="cd6b5-109">De plus, certaines fonctionnalités nécessitent que vous fournissez des informations lors du processus d’installation pour déployer la fonctionnalité correctement.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-109">In addition, some features require that you provide certain information during the installation process to successfully deploy the feature.</span></span> <span data-ttu-id="cd6b5-110">Vous devez également consulter la [planification du déploiement de MBAM 2,0 Server avant de](planning-for-mbam-20-server-deployment-mbam-2.md) démarrer le déploiement d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-110">You should also review [Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md) before you start the MBAM deployment.</span></span>

**<span data-ttu-id="cd6b5-111">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd6b5-111">Note</span></span>**  
<span data-ttu-id="cd6b5-112">Pour obtenir les fichiers journaux d’installation, vous devez utiliser le package msiexec et l’option **/l** &lt; emplacement &gt; pour installer MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-112">To obtain the setup log files, you have to use the Msiexec package and the **/L** &lt;location&gt; option to install MBAM.</span></span> <span data-ttu-id="cd6b5-113">Les fichiers journaux sont créés à l’emplacement que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-113">Log files are created in the location that you specify.</span></span>

<span data-ttu-id="cd6b5-114">D’autres fichiers journaux d’installation sont créés dans le dossier% Temp% sur le serveur de l’utilisateur qui installe MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-114">Additional setup log files are created in the %temp% folder on the server of the user who is installing MBAM.</span></span>



## <a href="" id="deploying-mbam-server-features-"></a><span data-ttu-id="cd6b5-115">Déploiement de fonctionnalités du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="cd6b5-115">Deploying MBAM Server Features</span></span>


<span data-ttu-id="cd6b5-116">Les étapes suivantes expliquent comment installer les fonctionnalités MBAM générales.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-116">The following steps describe how to install general MBAM features.</span></span>

**<span data-ttu-id="cd6b5-117">Pour démarrer l’Assistant Installation de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="cd6b5-117">To start the MBAM Server installation wizard</span></span>**

1.  <span data-ttu-id="cd6b5-118">Sur le serveur sur lequel vous voulez installer l’administration et le contrôle Microsoft BitLocker, exécutez **MBAMSetup.exe** pour démarrer l’Assistant Installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-118">On the server where you want to install Microsoft BitLocker Administration and Monitoring, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="cd6b5-119">Dans la page d' **Accueil** , sélectionnez éventuellement le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-119">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="cd6b5-120">Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-120">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="cd6b5-121">Dans la page de sélection de la **topologie** , sélectionnez la topologie **autonome** , puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-121">On the **Topology Selection** page, select the **Stand-alone** topology, and then click **Next**.</span></span>

    **<span data-ttu-id="cd6b5-122">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd6b5-122">Note</span></span>**  
    <span data-ttu-id="cd6b5-123">Si vous souhaitez installer MBAM avec la topologie intégrée de Configuration Manager, consultez [déploiement de MBAM avec Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span><span class="sxs-lookup"><span data-stu-id="cd6b5-123">If you want to install MBAM with the Configuration Manager integrated topology, see [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).</span></span>



5.  <span data-ttu-id="cd6b5-124">Sélectionnez les fonctionnalités que vous voulez installer.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-124">Select the features that you want to install.</span></span> <span data-ttu-id="cd6b5-125">Par défaut, toutes les fonctionnalités de MBAM sont sélectionnées pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-125">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="cd6b5-126">Effacez les fonctionnalités que vous voulez installer ailleurs.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-126">Clear the features that you want to install elsewhere.</span></span> <span data-ttu-id="cd6b5-127">Les fonctionnalités qui seront installées sur le même ordinateur doivent être installées en même temps.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-127">Features that will be installed on the same computer must be installed together at the same time.</span></span> <span data-ttu-id="cd6b5-128">Vous devez installer les fonctionnalités d’MBAM dans l’ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="cd6b5-128">You must install MBAM features in the following order:</span></span>

    -   <span data-ttu-id="cd6b5-129">Base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="cd6b5-129">Recovery Database</span></span>

    -   <span data-ttu-id="cd6b5-130">Base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="cd6b5-130">Compliance and Audit Database</span></span>

    -   <span data-ttu-id="cd6b5-131">Rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="cd6b5-131">Compliance and Audit Reports</span></span>

    -   <span data-ttu-id="cd6b5-132">Portail libre-service</span><span class="sxs-lookup"><span data-stu-id="cd6b5-132">Self-Service Portal</span></span>

    -   <span data-ttu-id="cd6b5-133">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="cd6b5-133">Administration and Monitoring Server</span></span>

    -   <span data-ttu-id="cd6b5-134">Modèle de stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="cd6b5-134">MBAM Group Policy template</span></span>

    **<span data-ttu-id="cd6b5-135">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd6b5-135">Note</span></span>**  
    <span data-ttu-id="cd6b5-136">L’Assistant installation vérifie la configuration requise pour votre installation et affiche les conditions préalables manquantes.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-136">The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="cd6b5-137">Si toutes les conditions préalables sont remplies, l’installation continue.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-137">If all of the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="cd6b5-138">Si une condition préalable manquante est détectée, vous devez résoudre les conditions préalables manquantes, puis cliquer de **nouveau sur vérifier les conditions préalables**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-138">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="cd6b5-139">Si toutes les conditions préalables sont remplies ce délai, l’installation reprend.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-139">If all prerequisites are met this time, the installation resumes.</span></span>



~~~
The MBAM Setup wizard displays installation pages for the features that you select. The following sections describe the installation procedures for each feature.

**Note**  
For the following instructions, it is assumed that each feature is to be installed on a separate server. If you install multiple features on a single server, you can change or eliminate some steps.
~~~



**<span data-ttu-id="cd6b5-140">Pour installer la base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="cd6b5-140">To install the Recovery Database</span></span>**

1.  <span data-ttu-id="cd6b5-141">Dans la page **configurer la base de données de récupération** , spécifiez les noms des ordinateurs qui exécutent la fonctionnalité d’administration et de surveillance du serveur.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-141">On the **Configure the Recovery database** page, specify the names of the computers that will be running the Administration and Monitoring Server feature.</span></span> <span data-ttu-id="cd6b5-142">Après le déploiement de la fonctionnalité d’administration et de surveillance du serveur, il utilise son compte de domaine pour se connecter à la base de données.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-142">After the Administration and Monitoring Server feature is deployed, it uses its domain account to connect to the database.</span></span>

2.  <span data-ttu-id="cd6b5-143">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-143">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="cd6b5-144">Spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données de récupération.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-144">Specify the SQL Server instance name and the name of the database that will store the recovery data.</span></span> <span data-ttu-id="cd6b5-145">Vous devez également spécifier l’emplacement de la base de données et l’emplacement où se trouvent les informations de journalisation.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-145">You must also specify both where the database will be located and where the log information will be located.</span></span>

4.  <span data-ttu-id="cd6b5-146">Cliquez sur **suivant** pour continuer à utiliser l’Assistant Configuration de MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-146">Click **Next** to continue with the MBAM Setup wizard.</span></span>

**<span data-ttu-id="cd6b5-147">Pour installer la base de données de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="cd6b5-147">To install the Compliance and Audit Database</span></span>**

1.  <span data-ttu-id="cd6b5-148">Dans la page **configuration de la conformité et de la base de données d’audit** , spécifiez le compte d’utilisateur qui sera utilisé pour accéder à la base de données pour les rapports.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-148">On the **Configure the Compliance and Audit Database** page, specify the user account that will be used to access the database for reports.</span></span>

2.  <span data-ttu-id="cd6b5-149">Spécifiez le nom de l’ordinateur qui sera exécuté sur le serveur d’administration et de surveillance ainsi que les rapports de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-149">Specify the computer names of the computers that will be running the Administration and Monitoring Server and the Compliance and Audit Reports.</span></span> <span data-ttu-id="cd6b5-150">Après le déploiement de l’administration et de la surveillance et des rapports de conformité et d’audit, ils utilisent leurs comptes de domaine pour se connecter aux bases de données.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-150">After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they use their domain accounts to connect to the databases.</span></span>

    **<span data-ttu-id="cd6b5-151">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd6b5-151">Note</span></span>**  
    <span data-ttu-id="cd6b5-152">Si vous installez la base de données de conformité et d’audit sans les rapports de conformité et d’audit, vous devez ajouter une exception sur l’ordinateur de base de données de conformité et d’audit pour activer le trafic entrant sur le port Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-152">If you are installing the Compliance and Audit Database without the Compliance and Audit Reports feature, you must add an exception on the Compliance and Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="cd6b5-153">Le numéro de port par défaut est 1433.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-153">The default port number is 1433.</span></span>



3.  <span data-ttu-id="cd6b5-154">Spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-154">Specify the SQL Server instance name and the name of the database that will store the compliance and audit data.</span></span> <span data-ttu-id="cd6b5-155">Vous devez également spécifier l’emplacement des informations de base de données et de journalisation.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-155">You must also specify where the database and log information will be located.</span></span>

4.  <span data-ttu-id="cd6b5-156">Cliquez sur **suivant** pour continuer à utiliser l’Assistant de configuration de l’administration et de la surveillance de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-156">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="cd6b5-157">Pour installer les rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="cd6b5-157">To install the Compliance and Audit Reports</span></span>**

1.  <span data-ttu-id="cd6b5-158">Sur la page **configurer les rapports de conformité et d’audit** , spécifiez le nom de l’instance SQL Server distante (par exemple, &lt; ServerName &gt; ) où la base de données d’audit et de conformité a été installée.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-158">On the **Configure the Compliance and Audit Reports** page, specify the remote SQL Server instance name (for example, &lt;ServerName&gt;) where the Compliance and Audit Database was installed.</span></span>

    **<span data-ttu-id="cd6b5-159">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd6b5-159">Note</span></span>**  
    <span data-ttu-id="cd6b5-160">Si vous installez des rapports de conformité et d’audit sans le serveur d’administration et de surveillance, vous devez ajouter une exception sur l’ordinateur du rapport de conformité et d’audit pour activer le trafic entrant sur le port du serveur de rapports (le port par défaut est 80).</span><span class="sxs-lookup"><span data-stu-id="cd6b5-160">If you are installing the Compliance and Audit Reports without the Administration and Monitoring Server, you must add an exception on the Compliance and Audit Report computer to enable inbound traffic on the Reporting Server port (the default port is 80).</span></span>



2.  <span data-ttu-id="cd6b5-161">Spécifiez le nom de la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-161">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="cd6b5-162">Par défaut, il s’agit du nom de la base de données MBAM, même si vous pouvez en modifier le nom lors de l’installation de la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-162">By default, the database name is MBAM Compliance Status, although you can change the name when you install the Compliance and Audit Database.</span></span>

3.  <span data-ttu-id="cd6b5-163">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-163">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="cd6b5-164">Sélectionnez l’instance de SQL Server Reporting Services dans laquelle les rapports de conformité et d’audit seront installés.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-164">Select the instance of SQL Server Reporting Services where the Compliance and Audit Reports will be installed.</span></span> <span data-ttu-id="cd6b5-165">Fournissez un compte d’utilisateur et un mot de passe de domaine pour accéder à la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-165">Provide a domain user account and password to access the Compliance and Audit Database.</span></span> <span data-ttu-id="cd6b5-166">Configurez le mot de passe de ce compte pour qu’il n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-166">Configure the password for this account to never expire.</span></span> <span data-ttu-id="cd6b5-167">Le compte d’utilisateur doit être en mesure d’accéder à toutes les données disponibles pour le groupe utilisateurs de reports MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-167">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span>

5.  <span data-ttu-id="cd6b5-168">Cliquez sur **suivant** pour continuer à utiliser l’Assistant de configuration de l’administration et de la surveillance de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-168">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="cd6b5-169">Pour installer le portail libre-service</span><span class="sxs-lookup"><span data-stu-id="cd6b5-169">To install the Self-Service Portal</span></span>**

1.  <span data-ttu-id="cd6b5-170">Sur la page **configurer le portail libre-service** , vous pouvez également chiffrer la communication entre le portail libre-service et les serveurs d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-170">On the **Configure the Self-Service Portal** page, you can optionally encrypt the communication between the Self-Service Portal and the Administration and Monitoring servers.</span></span> <span data-ttu-id="cd6b5-171">Si vous choisissez l’option permettant de chiffrer la communication, vous êtes invité à sélectionner le certificat d’autorité de certification à utiliser pour le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-171">If you choose the option to encrypt the communication, you are prompted to select the certification authority-provisioned certificate to use for encryption.</span></span>

2.  <span data-ttu-id="cd6b5-172">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-172">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="cd6b5-173">Spécifiez l’instance distante de SQL Server (par exemple, \* &lt; ServerName &gt; \*) où la base de données d’audit et de conformité est installée.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-173">Specify the remote instance of SQL Server (for example, *&lt;ServerName&gt;*) where the Compliance and Audit Database was installed.</span></span>

4.  <span data-ttu-id="cd6b5-174">Spécifiez le nom de la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-174">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="cd6b5-175">Par défaut, le nom de la base de données est MBAM de conformité.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-175">By default, the database name is MBAM Compliance Status.</span></span> <span data-ttu-id="cd6b5-176">Toutefois, vous pouvez modifier le nom lors de l’installation de la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-176">However, you can change the name when you install the Compliance and Audit Database.</span></span>

5.  <span data-ttu-id="cd6b5-177">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-177">Click **Next** to continue.</span></span>

6.  <span data-ttu-id="cd6b5-178">Spécifiez l’instance distante de SQL Server (par exemple, \* &lt; ServerName &gt; \*) où la base de données de récupération a été installée.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-178">Specify the remote instance of SQL Server (for example, *&lt;ServerName&gt;*) where the Recovery Database was installed.</span></span>

7.  <span data-ttu-id="cd6b5-179">Spécifiez le nom de la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-179">Specify the name of the Recovery Database.</span></span> <span data-ttu-id="cd6b5-180">Par défaut, il s’agit du nom de la base de données **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-180">By default, the database name is **MBAM Recovery and Hardware**.</span></span> <span data-ttu-id="cd6b5-181">Toutefois, vous pouvez modifier le nom lors de l’installation de la fonctionnalité de base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-181">However, you can change the name when you install the Recovery Database feature.</span></span>

8.  <span data-ttu-id="cd6b5-182">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-182">Click **Next** to continue.</span></span>

9.  <span data-ttu-id="cd6b5-183">Entrez le **numéro de port**, le **nom d’hôte** (facultatif), ainsi que le chemin d' **installation** du serveur d’administration et de surveillance de MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-183">Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring Server.</span></span>

    **<span data-ttu-id="cd6b5-184">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd6b5-184">Note</span></span>**  
    <span data-ttu-id="cd6b5-185">Le numéro de port que vous spécifiez doit être un numéro de port inutilisé sur le serveur d’administration et de surveillance sauf si vous spécifiez un nom d’en-tête d’hôte unique.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-185">The port number that you specify must be an unused port number on the Administration and Monitoring server unless you specify a unique host header name.</span></span> <span data-ttu-id="cd6b5-186">Si vous utilisez le pare-feu Windows, le port s’ouvre automatiquement.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-186">If you are using Windows Firewall, the port will be opened automatically.</span></span>



10. <span data-ttu-id="cd6b5-187">Pour éventuellement inscrire un nom de principal de service (SPN) pour le portail libre-service, sélectionnez **inscrire les noms de principal de service (SPN) de cet ordinateur auprès d’Active Directory (requis pour l’authentification Windows)**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-187">To optionally register a Service Principal Name (SPN) for the Self-Service Portal, select **Register this machine’s Service Principal Names (SPN) with Active Directory (Required for Windows Authentication)**.</span></span> <span data-ttu-id="cd6b5-188">Si vous activez cette case à cocher, le programme d’installation d’MBAM ne tente pas d’inscrire le SPN existant et vous pouvez inscrire manuellement le SPN avant ou après l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-188">If you select this check box, MBAM Setup will not try to register the existing SPNs, and you can manually register the SPN before or after the MBAM installation.</span></span> <span data-ttu-id="cd6b5-189">Pour obtenir des instructions sur l’enregistrement manuel du SPN, voir [enregistrement de SPN manuel](https://go.microsoft.com/fwlink/?LinkId=286758).</span><span class="sxs-lookup"><span data-stu-id="cd6b5-189">For instructions on registering the SPN manually, see [Manual SPN Registration](https://go.microsoft.com/fwlink/?LinkId=286758).</span></span>

11. <span data-ttu-id="cd6b5-190">Cliquez sur **suivant** pour continuer à utiliser l’Assistant de configuration de l’administration et de la surveillance de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-190">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

12. <span data-ttu-id="cd6b5-191">Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-191">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

13. <span data-ttu-id="cd6b5-192">Lorsque les informations de fonctionnalité de MBAM sélectionnées sont terminées, vous êtes prêt à démarrer l’installation d’MBAM à l’aide de l’Assistant de configuration.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-192">When the selected MBAM feature information is completed, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="cd6b5-193">Cliquez sur **retour** pour parcourir l’Assistant si vous devez revoir ou modifier vos paramètres d’installation.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-193">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="cd6b5-194">Cliquez sur **installer** pour démarrer l’installation.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-194">Click **Install** to start the installation.</span></span> <span data-ttu-id="cd6b5-195">Cliquez sur **Annuler** pour quitter l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-195">Click **Cancel** to exit the wizard.</span></span> <span data-ttu-id="cd6b5-196">Le programme d’installation installe les fonctionnalités de MBAM que vous avez sélectionnées et vous signale que l’installation est terminée.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-196">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

14. <span data-ttu-id="cd6b5-197">Cliquez sur **Terminer** pour quitter l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-197">Click **Finish** to exit the wizard.</span></span>

    **<span data-ttu-id="cd6b5-198">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd6b5-198">Note</span></span>**  
    <span data-ttu-id="cd6b5-199">Pour configurer le portail libre-service une fois l’installation terminée, marquez le portail libre-service avec le nom de votre société et d’autres informations spécifiques à votre entreprise, voir [Comment personnaliser le portail libre-service](how-to-brand-the-self-service-portal.md) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-199">To configure the Self-Service Portal after you installed it, brand the Self-Service Portal with your company name and other company-specific information, see [How to Brand the Self-Service Portal](how-to-brand-the-self-service-portal.md) for instructions.</span></span>



15. <span data-ttu-id="cd6b5-200">Si les ordinateurs clients ont accès au réseau de distribution de contenu (CDN) Microsoft, ce qui donne au portail libre-service l’accès requis à certains fichiers JavaScript, vous avez terminé l’installation du portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-200">If the client computers have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, you are finished with the Self-Service Portal installation.</span></span> <span data-ttu-id="cd6b5-201">Si les ordinateurs clients n’ont pas accès au réseau de distribution de contenu Microsoft, suivez les étapes décrites dans la section suivante pour configurer le portail libre-service pour référencer les fichiers JavaScript à partir d’une source accessible.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-201">If the client computers does not have access to the Microsoft CDN, complete the steps in the next section to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

**<span data-ttu-id="cd6b5-202">Pour configurer le portail libre-service lorsque les utilisateurs finaux ne peuvent pas accéder au réseau de distribution de contenu Microsoft</span><span class="sxs-lookup"><span data-stu-id="cd6b5-202">To configure the Self-Service Portal when end users cannot access the Microsoft Content Delivery Network</span></span>**

1. <span data-ttu-id="cd6b5-203">Si les ordinateurs clients ont accès au réseau de distribution de contenu (CDN) Microsoft, ce qui donne au portail libre-service l’accès requis à certains fichiers JavaScript, l’installation du portail libre-service est terminée.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-203">If the client computers have access to the Microsoft Content Delivery Network (CDN), which gives the Self-Service Portal the required access to certain JavaScript files, the Self-Service Portal installation is completed.</span></span> <span data-ttu-id="cd6b5-204">Si les ordinateurs client n’ont pas accès au réseau de distribution de contenu Microsoft, suivez les étapes restantes de cette section pour configurer le portail libre-service pour référencer les fichiers JavaScript à partir d’une source accessible.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-204">If the client computers do not have access to the Microsoft CDN, complete the remaining steps in this section to configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span>

2. <span data-ttu-id="cd6b5-205">Téléchargez les quatre fichiers JavaScript à partir du Microsoft CDN:</span><span class="sxs-lookup"><span data-stu-id="cd6b5-205">Download the four JavaScript files from the Microsoft CDN:</span></span>

   -   <span data-ttu-id="cd6b5-206">jQuery-1.7.2.min.js-[https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)</span><span class="sxs-lookup"><span data-stu-id="cd6b5-206">jQuery-1.7.2.min.js - [https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)</span></span>

   -   <span data-ttu-id="cd6b5-207">MicrosoftAjax.js –[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)</span><span class="sxs-lookup"><span data-stu-id="cd6b5-207">MicrosoftAjax.js –[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)</span></span>

   -   <span data-ttu-id="cd6b5-208">MicrosoftMvcAjax.js-[https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)</span><span class="sxs-lookup"><span data-stu-id="cd6b5-208">MicrosoftMvcAjax.js - [https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)</span></span>

   -   <span data-ttu-id="cd6b5-209">MicrosoftMvcValidation.js-</span><span class="sxs-lookup"><span data-stu-id="cd6b5-209">MicrosoftMvcValidation.js -</span></span> <https://go.microsoft.com/fwlink/p/?LinkId=272285>

3. <span data-ttu-id="cd6b5-210">Copiez les fichiers JavaScript dans le répertoire **scripts** du portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-210">Copy the JavaScript files to the **Scripts** directory of the Self-Service Portal.</span></span> <span data-ttu-id="cd6b5-211">Ce répertoire se trouve dans <em> &lt; MBAM répertoire d’installation de self-service &gt; \\ </em> Website\\Scripts.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-211">This directory is located in <em>&lt;MBAM Self-Service Install Directory&gt;\\</em>Self Service Website\\Scripts.</span></span>

4. <span data-ttu-id="cd6b5-212">Ouvrez le **Gestionnaire des services Internet (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-212">Open **Internet Information Services (IIS) Manager**.</span></span>

5. <span data-ttu-id="cd6b5-213">Développez **sites** &gt; **Microsoft et surveillance de BitLocker**et mettez en surbrillance **selfservice**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-213">Expand **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**, and highlight **SelfService**.</span></span>

   **<span data-ttu-id="cd6b5-214">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd6b5-214">Note</span></span>**  
   <span data-ttu-id="cd6b5-215">*Selfservice* est le nom de répertoire virtuel par défaut.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-215">*SelfService* is the default virtual directory name.</span></span> <span data-ttu-id="cd6b5-216">Si vous avez choisi un autre nom pour ce répertoire lors de l’installation, n’oubliez pas de remplacer *selfservice* dans le reste de ces instructions par le nom que vous avez choisi.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-216">If you chose a different name for this directory during installation, remember to replace *SelfService* in the rest of these instructions with the name you chose.</span></span>



6. <span data-ttu-id="cd6b5-217">Dans le volet du milieu, double-cliquez sur paramètres de l' **application**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-217">In the middle pane, double-click **Application Settings**.</span></span>

7. <span data-ttu-id="cd6b5-218">Pour chaque élément de la liste suivante, modifiez les paramètres de l’application pour référencer le nouvel emplacement en remplaçant le &lt; répertoire virtuel &gt; par/selfservice/(ou le nom que vous avez choisi lors de l’installation).</span><span class="sxs-lookup"><span data-stu-id="cd6b5-218">For each item in the following list, edit the application settings to reference the new location by replacing &lt;virtual directory&gt; with /SelfService/ (or the name you chose during installation).</span></span> <span data-ttu-id="cd6b5-219">Par exemple, le chemin d’accès du répertoire virtuel est semblable à/selfservice/scripts/jquery-1.7.2.min.js.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-219">For example, the virtual directory path will be similar to /selfservice/scripts/jquery-1.7.2.min.js.</span></span>

   -   <span data-ttu-id="cd6b5-220">jQueryPath:/ &lt; répertoire virtuel &gt; /scripts/jQuery-1.7.2.min.js</span><span class="sxs-lookup"><span data-stu-id="cd6b5-220">jQueryPath: /&lt;virtual directory&gt;/Scripts/ jQuery-1.7.2.min.js</span></span>

   -   <span data-ttu-id="cd6b5-221">MicrosoftAjaxPath:/ &lt; répertoire virtuel &gt; /scripts/MicrosoftAjax.js</span><span class="sxs-lookup"><span data-stu-id="cd6b5-221">MicrosoftAjaxPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftAjax.js</span></span>

   -   <span data-ttu-id="cd6b5-222">MicrosoftMvcAjaxPath:/ &lt; répertoire virtuel &gt; /scripts/MicrosoftMvcAjax.js</span><span class="sxs-lookup"><span data-stu-id="cd6b5-222">MicrosoftMvcAjaxPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftMvcAjax.js</span></span>

   -   <span data-ttu-id="cd6b5-223">MicrosoftMvcValidationPath:/ &lt; répertoire virtuel &gt; /scripts/MicrosoftMvcValidation.js</span><span class="sxs-lookup"><span data-stu-id="cd6b5-223">MicrosoftMvcValidationPath: /&lt;virtual directory&gt;/Scripts/ MicrosoftMvcValidation.js</span></span>

**<span data-ttu-id="cd6b5-224">Pour installer la fonctionnalité serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="cd6b5-224">To install the Administration and Monitoring Server feature</span></span>**

1. <span data-ttu-id="cd6b5-225">MBAM peut crypter la communication entre les services Web et les serveurs d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-225">MBAM can encrypt the communication between the Web Services and the Administration and Monitoring servers.</span></span> <span data-ttu-id="cd6b5-226">Si vous choisissez l’option permettant de chiffrer la communication, vous êtes invité à sélectionner le certificat d’autorité de certification à utiliser pour le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-226">If you choose the option to encrypt the communication, you are prompted to select the certification authority-provisioned certificate to use for encryption.</span></span>

2. <span data-ttu-id="cd6b5-227">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-227">Click **Next** to continue.</span></span>

3. <span data-ttu-id="cd6b5-228">Spécifiez l’instance distante de SQL Server (par exemple: \* &lt; NomServeur &gt; \*) où la base de données d’audit et de conformité est installée.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-228">Specify the remote instance of SQL Server (for example: *&lt;ServerName&gt;*) where the Compliance and Audit Database was installed.</span></span>

4. <span data-ttu-id="cd6b5-229">Spécifiez le nom de la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-229">Specify the name of the Compliance and Audit Database.</span></span> <span data-ttu-id="cd6b5-230">Par défaut, le nom de la base de données est MBAM de conformité.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-230">By default, the database name is MBAM Compliance Status.</span></span> <span data-ttu-id="cd6b5-231">Toutefois, vous pouvez modifier le nom lors de l’installation de la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-231">However, you can change the name when you install the Compliance and Audit Database.</span></span>

5. <span data-ttu-id="cd6b5-232">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-232">Click **Next** to continue.</span></span>

6. <span data-ttu-id="cd6b5-233">Spécifiez l’instance distante de SQL Server (par exemple: \* &lt; NomServeur &gt; \*) où la base de données de récupération a été installée.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-233">Specify the remote instance of SQL Server (for example: *&lt;ServerName&gt;*) where the Recovery Database was installed.</span></span>

7. <span data-ttu-id="cd6b5-234">Spécifiez le nom de la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-234">Specify the name of the Recovery Database.</span></span> <span data-ttu-id="cd6b5-235">Par défaut, il s’agit du nom de la base de données **MBAM**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-235">By default, the database name is **MBAM Recovery and Hardware**.</span></span> <span data-ttu-id="cd6b5-236">Toutefois, vous pouvez modifier le nom lors de l’installation de la fonctionnalité de base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-236">However, you can change the name when you install the Recovery Database feature.</span></span>

8. <span data-ttu-id="cd6b5-237">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-237">Click **Next** to continue.</span></span>

9. <span data-ttu-id="cd6b5-238">Spécifiez l’URL du site «Home» (SRS) SQL Server Reporting Services (SRS).</span><span class="sxs-lookup"><span data-stu-id="cd6b5-238">Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site.</span></span> <span data-ttu-id="cd6b5-239">L’emplacement d’accueil par défaut d’une instance de site SQL Server Reporting Services est le suivant:</span><span class="sxs-lookup"><span data-stu-id="cd6b5-239">The default Home location of a SQL Server Reporting Services site instance is at:</span></span>

   <span data-ttu-id="cd6b5-240">http:// <em> &lt; NameofMBAMReportsServer &gt; / </em> reportserver</span><span class="sxs-lookup"><span data-stu-id="cd6b5-240">http://<em>&lt;NameofMBAMReportsServer&gt;/</em>ReportServer</span></span>

   **<span data-ttu-id="cd6b5-241">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd6b5-241">Note</span></span>**  
   <span data-ttu-id="cd6b5-242">Si SQL Server Reporting Services a été configuré en tant qu’instance nommée, l’URL ressemble à ce qui suit: http://\* &lt; NameofMBAMReportsServer &gt; */ReportServer\_* &lt; SRSInstanceName &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-242">If SQL Server Reporting Services was configured as a named instance, the URL resembles the following: http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*.</span></span>



10. <span data-ttu-id="cd6b5-243">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-243">Click **Next** to continue.</span></span>

11. <span data-ttu-id="cd6b5-244">Entrez le **numéro de port**, le **nom d’hôte** (facultatif), ainsi que le chemin d' **installation** du serveur d’administration et de surveillance de MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-244">Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring Server.</span></span>

    **<span data-ttu-id="cd6b5-245">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd6b5-245">Note</span></span>**  
    <span data-ttu-id="cd6b5-246">Le numéro de port que vous spécifiez doit être un numéro de port inutilisé sur le serveur d’administration et de surveillance sauf si vous spécifiez un nom d’en-tête d’hôte unique.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-246">The port number that you specify must be an unused port number on the Administration and Monitoring server unless you specify a unique host header name.</span></span> <span data-ttu-id="cd6b5-247">Si vous utilisez le pare-feu Windows, le port s’ouvre automatiquement.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-247">If you are using Windows Firewall, the port will be opened automatically.</span></span>



12. <span data-ttu-id="cd6b5-248">Pour éventuellement inscrire un nom de principal de service (SPN) pour le portail libre-service, sélectionnez **inscrire les noms de principal de service (SPN) de cet ordinateur auprès d’Active Directory (requis pour l’authentification Windows)**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-248">To optionally register a Service Principal Name (SPN) for the Self-Service Portal, select **Register this machine’s Service Principal Names (SPN) with Active Directory (Required for Windows Authentication)**.</span></span> <span data-ttu-id="cd6b5-249">Si vous activez cette case à cocher, le programme d’installation d’MBAM ne tente pas d’inscrire le SPN existant et vous pouvez inscrire manuellement le SPN avant ou après l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-249">If you select this check box, MBAM Setup will not try to register the existing SPNs, and you can manually register the SPN before or after the MBAM installation.</span></span> <span data-ttu-id="cd6b5-250">Pour obtenir des instructions sur l’enregistrement manuel du SPN, voir [enregistrement de SPN manuel](https://go.microsoft.com/fwlink/?LinkId=286758).</span><span class="sxs-lookup"><span data-stu-id="cd6b5-250">For instructions on registering the SPN manually, see [Manual SPN Registration](https://go.microsoft.com/fwlink/?LinkId=286758).</span></span>

13. <span data-ttu-id="cd6b5-251">Cliquez sur **suivant** pour continuer à utiliser l’Assistant de configuration de l’administration et de la surveillance de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-251">Click **Next** to continue with the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

14. <span data-ttu-id="cd6b5-252">Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-252">Specify whether to use Microsoft Updates to help keep your computer secure, and then click **Next**.</span></span>

15. <span data-ttu-id="cd6b5-253">Lorsque les informations de fonctionnalité de MBAM sélectionnées sont terminées, vous êtes prêt à démarrer l’installation d’MBAM à l’aide de l’Assistant de configuration.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-253">When the selected MBAM feature information is completed, you are ready to start the MBAM installation by using the Setup wizard.</span></span> <span data-ttu-id="cd6b5-254">Cliquez sur **retour** pour parcourir l’Assistant si vous devez revoir ou modifier vos paramètres d’installation.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-254">Click **Back** to move through the wizard if you have to review or change your installation settings.</span></span> <span data-ttu-id="cd6b5-255">Cliquez sur **installer pour procéder** à l’installation.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-255">Click **Install** to being the installation.</span></span> <span data-ttu-id="cd6b5-256">Cliquez sur **Annuler** pour quitter l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-256">Click **Cancel** to exit the wizard.</span></span> <span data-ttu-id="cd6b5-257">Le programme d’installation installe les fonctionnalités de MBAM que vous avez sélectionnées et vous signale que l’installation est terminée.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-257">Setup installs the MBAM features that you selected and notifies you that the installation is finished.</span></span>

16. <span data-ttu-id="cd6b5-258">Cliquez sur **Terminer** pour quitter l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-258">Click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="cd6b5-259">Pour effectuer une configuration après l’installation</span><span class="sxs-lookup"><span data-stu-id="cd6b5-259">To perform post-installation configuration</span></span>**

1.  <span data-ttu-id="cd6b5-260">Sur le serveur d’administration et de surveillance, ajoutez des utilisateurs aux groupes locaux suivants pour leur permettre d’accéder aux fonctionnalités disponibles sur le site Web d’administration et de surveillance de MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-260">On the Administration and Monitoring Server, add users to the following local groups to give them access to the features on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="cd6b5-261">**Utilisateurs du support technique MBAM**: les membres de ce groupe local peuvent accéder à la récupération du lecteur et gérer les fonctionnalités du TPM sur le site Web d’administration et de surveillance MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-261">**MBAM Helpdesk Users**: Members of this local group can access the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="cd6b5-262">Pour un utilisateur du support technique, tous les champs de la récupération de lecteur et de la gestion de TPM sont obligatoires.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-262">All fields in Drive Recovery and Manage TPM are required fields for a Helpdesk User.</span></span>

    -   <span data-ttu-id="cd6b5-263">**Utilisateurs de l’assistance technique avancée MBAM**: les membres de ce groupe local disposent d’un accès avancé aux fonctionnalités de récupération et de gestion du TPM sur le site Web d’administration et de surveillance des MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-263">**MBAM Advanced Helpdesk Users**: Members of this local group have advanced access to the Drive Recovery and Manage TPM features on the MBAM Administration and Monitoring website.</span></span> <span data-ttu-id="cd6b5-264">Pour les utilisateurs expérimentés du support technique, seul le champ ID clé est requis pour la récupération du lecteur.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-264">For Advanced Helpdesk Users, only the Key ID field is required in Drive Recovery.</span></span> <span data-ttu-id="cd6b5-265">Dans **gérer le module de plateforme sécurisée**, seul le champ domaine de l' **ordinateur** et le champ nom de l' **ordinateur** est requis.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-265">In **Manage TPM**, only the **Computer Domain** field and **Computer Name** field are required.</span></span>

2.  <span data-ttu-id="cd6b5-266">Sur le serveur hébergeant l’administration et la surveillance du serveur et la base de données de conformité et d’audit, et sur le serveur qui héberge les rapports de conformité et d’audit, ajoutez des utilisateurs au groupe local suivant pour leur permettre d’accéder à la fonctionnalité rapports sur le site Web d’administration et de surveillance de MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-266">On the server that hosts Administration and Monitoring Server and the Compliance and Audit Database and on the server that hosts the Compliance and Audit Reports, add users to the following local group to give them access to the Reports feature on the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="cd6b5-267">**Utilisateurs du rapport MBAM**: les membres de ce groupe local peuvent accéder aux rapports sur le site Web d’administration et de surveillance de MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-267">**MBAM Report Users**: Members of this local group can access the reports on the MBAM Administration and Monitoring website.</span></span>

    **<span data-ttu-id="cd6b5-268">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd6b5-268">Note</span></span>**  
    <span data-ttu-id="cd6b5-269">Il est possible d’avoir une appartenance similaire à un utilisateur ou un groupe du groupe local **utilisateurs de rapports MBAM** sur tous les ordinateurs sur lesquels les fonctionnalités d’administration de MBAM et de surveillance de la base de données de serveur et de conformité, ainsi que les rapports de conformité et d’audit sont installés.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-269">Identical user or group membership of the **MBAM Report Users** local group must be maintained on all computers where the MBAM Administration and Monitoring Server features, Compliance and Audit Database, and the Compliance and Audit Reports are installed.</span></span>



## <span data-ttu-id="cd6b5-270">Validation de l’installation de la fonctionnalité MBAM Server</span><span class="sxs-lookup"><span data-stu-id="cd6b5-270">Validating the MBAM Server Feature Installation</span></span>


<span data-ttu-id="cd6b5-271">Lorsque l’installation de la fonctionnalité administration de Microsoft BitLocker et analyse du serveur est terminée, nous vous conseillons de vérifier que l’installation a correctement configuré toutes les fonctionnalités nécessaires à MBAM.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-271">When Microsoft BitLocker Administration and Monitoring Server feature installation is completed, we recommend that you validate that the installation has successfully set up all the necessary features for MBAM.</span></span> <span data-ttu-id="cd6b5-272">Utilisez la procédure suivante pour vérifier que le service d’administration et de surveillance de BitLocker est opérationnel.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-272">Use the following procedure to confirm that the Microsoft BitLocker Administration and Monitoring service is functional.</span></span>

**<span data-ttu-id="cd6b5-273">Pour valider une installation de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="cd6b5-273">To validate an MBAM Server installation</span></span>**

1. <span data-ttu-id="cd6b5-274">Sur chaque serveur sur lequel est déployée une fonctionnalité MBAM, ouvrez **le panneau de configuration**, sélectionnez **programmes**, puis sélectionnez **programmes et fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-274">On each server where an MBAM feature is deployed, open **Control Panel**, select **Programs**, and then select **Programs and Features**.</span></span> <span data-ttu-id="cd6b5-275">Vérifiez que la fonctionnalité **administration et analyse de BitLocker Microsoft** s’affiche dans la liste **programmes et fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="cd6b5-275">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the **Programs and Features** list.</span></span>

   **<span data-ttu-id="cd6b5-276">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd6b5-276">Note</span></span>**  
   <span data-ttu-id="cd6b5-277">Pour valider l’installation d’MBAM, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-277">To validate the MBAM installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>



2. <span data-ttu-id="cd6b5-278">Sur le serveur sur lequel la base de données de récupération est installée, ouvrez SQL Server Management Studio, puis vérifiez que la base de données de **récupération et de MBAM** est installée.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-278">On the server where the Recovery Database is installed, open SQL Server Management Studio and verify that the **MBAM Recovery and Hardware** database is installed.</span></span>

3. <span data-ttu-id="cd6b5-279">Sur le serveur sur lequel la base de données d’audit et de conformité est installée, ouvrez SQL Server Management Studio et vérifiez que la **base de données de statut de conformité MBAM** est installée.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-279">On the server where the Compliance and Audit Database is installed, open SQL Server Management Studio and verify that the **MBAM Compliance Status Database** is installed.</span></span>

4. <span data-ttu-id="cd6b5-280">Sur le serveur sur lequel sont installés les rapports de conformité et d’audit, ouvrez un navigateur Web contenant les informations d’identification d’administration et naviguez jusqu’au site «Home» du site SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-280">On the server where the Compliance and Audit Reports are installed, open a web browser with administrative credentials and browse to the “Home” of the SQL Server Reporting Services site.</span></span>

   <span data-ttu-id="cd6b5-281">L’emplacement local par défaut d’une instance de site SQL Server Reporting Services est disponible sur http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /reports.aspx.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-281">The default Home location of a SQL Server Reporting Services site instance can be found is at http://<em>&lt;NameofMBAMReportsServer&gt;</em>/Reports.aspx.</span></span> <span data-ttu-id="cd6b5-282">Pour trouver l’URL réelle, utilisez l’outil Gestionnaire de configuration de Reporting Services et sélectionnez les instances spécifiées lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-282">To find the actual URL, use the Reporting Services Configuration Manager tool and select the instances that were specified during setup.</span></span>

   <span data-ttu-id="cd6b5-283">Confirmez qu’un dossier de rapports intitulé **Microsoft BitLocker administration et analyse** contient une source de données appelée **MaltaDataSource** et qu’un dossier **en-US** contient quatre rapports.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-283">Confirm that a reports folder named **Microsoft BitLocker Administration and Monitoring** contains a data source called **MaltaDataSource** and that an **en-us** folder contains four reports.</span></span>

   **<span data-ttu-id="cd6b5-284">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd6b5-284">Note</span></span>**  
   <span data-ttu-id="cd6b5-285">Si SQL Server Reporting Services a été configuré en tant qu’instance nommée, l’URL doit ressembler à ce qui suit: http://\* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; \*</span><span class="sxs-lookup"><span data-stu-id="cd6b5-285">If SQL Server Reporting Services was configured as a named instance, the URL should resemble the following:http://*&lt;NameofMBAMReportsServer&gt;*/Reports\_*&lt;SRSInstanceName&gt;*</span></span>



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. <span data-ttu-id="cd6b5-286">Sur le serveur sur lequel est installée la fonctionnalité d’administration et de surveillance, exécutez le **Gestionnaire de serveur** et naviguez jusqu’à **rôles**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-286">On the server where the Administration and Monitoring feature is installed, run **Server Manager** and browse to **Roles**.</span></span> <span data-ttu-id="cd6b5-287">Sélectionnez **serveur Web (IIS)**, puis cliquez sur **Gestionnaire des services Internet (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-287">Select **Web Server (IIS)**, and then click **Internet Information Services (IIS) Manager**.</span></span>

6. <span data-ttu-id="cd6b5-288">Dans **connexions**, naviguez jusqu’à \* &lt; nomordinateur &gt; \*, sélectionnez **sites**, puis l’option **administration et analyse de Microsoft BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-288">In **Connections**, browse to *&lt;computername&gt;*, select **Sites**, and select **Microsoft BitLocker Administration and Monitoring**.</span></span> <span data-ttu-id="cd6b5-289">Vérifiez que **MBAMAdministrationService**, **MBAMComplianceStatusService**et **MBAMRecoveryAndHardwareService** apparaissent.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-289">Verify that **MBAMAdministrationService**, **MBAMComplianceStatusService**, and **MBAMRecoveryAndHardwareService** are listed.</span></span>

7. <span data-ttu-id="cd6b5-290">Sur le serveur sur lequel sont installés les fonctionnalités d’administration et de surveillance et de portail en libre-service, ouvrez un navigateur Web contenant les informations d’identification d’administration et naviguez jusqu’aux emplacements suivants pour vérifier qu’ils se chargent correctement.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-290">On the server where the Administration and Monitoring features and Self-Service Portal are installed, open a web browser with administrative credentials and browse to the following locations to verify that they load successfully.</span></span>

   **<span data-ttu-id="cd6b5-291">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd6b5-291">Note</span></span>**  
   <span data-ttu-id="cd6b5-292">Les URL se terminant par «. svc» n’affichent pas de site Web.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-292">The URLs ending in “.svc” do not display a website.</span></span> <span data-ttu-id="cd6b5-293">Le succès est indiqué par le message «la publication des métadonnées pour ce service est actuellement désactivée» ou par des informations ressemblant à du code.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-293">Success is indicated by the message “Metadata publishing for this service is currently disabled” or by information resembling code.</span></span> <span data-ttu-id="cd6b5-294">Si un autre message d’erreur s’affiche ou si la page n’est pas disponible, cela dit qu’il n’a pas été correctement chargé.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-294">If you see some other error message or if the page cannot be found, the page has not loaded successfully.</span></span>



~~~
-   *http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports

-   *http://&lt;hostname&gt;/SelfService&gt;/*

-   *http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc*

-   *http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc*

-   *http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc*

-   *http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc*

**Note**  
It is assumed that the server features were installed on the default port without network encryption. If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.aspx* or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*

If the server features were installed with network encryption, change http:// to https://.
~~~



8. <span data-ttu-id="cd6b5-295">Vérifiez que chaque page Web se charge correctement.</span><span class="sxs-lookup"><span data-stu-id="cd6b5-295">Verify that each webpage loads successfully.</span></span>

## <span data-ttu-id="cd6b5-296">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cd6b5-296">Related topics</span></span>


[<span data-ttu-id="cd6b5-297">Déploiement de l'infrastructure de serveur MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="cd6b5-297">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









