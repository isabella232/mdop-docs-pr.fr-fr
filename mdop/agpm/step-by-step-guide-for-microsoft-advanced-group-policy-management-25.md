---
title: Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft2.5
description: Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft2.5
author: dansimp
ms.assetid: 454298c9-0fab-497a-9808-c0246a4c8db5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 67925e417e4fb1f5398dfd030f366936f1d36909
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808209"
---
# <span data-ttu-id="e662a-103">Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft2.5</span><span class="sxs-lookup"><span data-stu-id="e662a-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 2.5</span></span>


<span data-ttu-id="e662a-104">Ce guide pas à pas décrit les techniques avancées de gestion des stratégies de groupe à l’aide de la console de gestion des stratégies de groupe (GPMC) et de la gestion de la stratégie de groupe Microsoft avancée (AGPM).</span><span class="sxs-lookup"><span data-stu-id="e662a-104">This step-by-step guide demonstrates advanced techniques for Group Policy management using the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="e662a-105">AGPM augmente les capacités de la console de gestion des stratégies de GPMC et fournit les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="e662a-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="e662a-106">Rôles standard pour la délégation d’autorisations pour gérer des objets de stratégie de groupe pour plusieurs administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-106">Standard roles for delegating permissions to manage Group Policy objects (GPOs) to multiple Group Policy administrators.</span></span>

-   <span data-ttu-id="e662a-107">Archive permettant aux administrateurs de stratégie de groupe de créer et de modifier des objets de stratégie de groupe hors ligne avant de les déployer dans un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="e662a-107">An archive to enable Group Policy administrators to create and modify GPOs offline before deploying them to a production environment.</span></span>

-   <span data-ttu-id="e662a-108">La possibilité de revenir à une version précédente d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-108">The ability to roll back to any previous version of a GPO.</span></span>

-   <span data-ttu-id="e662a-109">La fonctionnalité d’archivage/extraction pour les objets de stratégie de groupe permet de s’assurer que les administrateurs de stratégie de groupe n’écrasent pas par inadvertance les tâches d’un autre groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-109">Check-in/check-out capability for GPOs to ensure that Group Policy administrators do not inadvertently overwrite each other's work.</span></span>

## <span data-ttu-id="e662a-110">Vue d’ensemble du scénario AGPM</span><span class="sxs-lookup"><span data-stu-id="e662a-110">AGPM scenario overview</span></span>


<span data-ttu-id="e662a-111">Pour ce scénario, vous allez utiliser un compte d’utilisateur distinct pour chaque rôle dans AGPM et montrer comment la stratégie de groupe peut être gérée dans un environnement doté de plusieurs administrateurs de stratégie de groupe disposant de différents niveaux d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="e662a-111">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment with multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="e662a-112">Plus précisément, vous devez effectuer les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="e662a-112">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="e662a-113">À l’aide d’un compte membre du groupe administrateurs de domaine, installez le serveur AGPM et attribuez le rôle d’administrateur AGPM à un compte ou à un groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-113">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="e662a-114">À l’aide des comptes auxquels vous allez attribuer des rôles AGPM, installez le client AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-114">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="e662a-115">À l’aide d’un compte ayant le rôle d’administrateur AGPM, configurez l’accès AGPM et déléguez aux objets de stratégie de groupe en attribuant des rôles à d’autres comptes.</span><span class="sxs-lookup"><span data-stu-id="e662a-115">Using an account with the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="e662a-116">En utilisant un compte doté du rôle d’éditeur, demandez la création d’un objet de stratégie de groupe, que vous approuvez ensuite en utilisant un compte doté du rôle Approbateur.</span><span class="sxs-lookup"><span data-stu-id="e662a-116">Using an account with the Editor role, request the creation of a GPO, which you then approve using an account with the Approver role.</span></span> <span data-ttu-id="e662a-117">Avec le compte de l’éditeur, recherchez l’objet de stratégie de groupe à partir de l’archive, modifiez-le, puis consultez l’objet de stratégie de groupe dans l’archive et demandez le déploiement.</span><span class="sxs-lookup"><span data-stu-id="e662a-117">With the Editor account, check the GPO out of the archive, edit the GPO, check the GPO into the archive, and request deployment.</span></span>

-   <span data-ttu-id="e662a-118">En utilisant un compte doté du rôle Approbateur, passez en revue l’objet de stratégie de groupe et déployez-le dans votre environnement de production.</span><span class="sxs-lookup"><span data-stu-id="e662a-118">Using an account with the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="e662a-119">À l’aide d’un compte avec le rôle d’éditeur, créez un modèle d’objet de stratégie de groupe et utilisez-le comme point de départ pour créer un nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-119">Using an account with the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="e662a-120">En utilisant un compte doté du rôle Approbateur, supprimez et restaurez un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-120">Using an account with the Approver role, delete and restore a GPO.</span></span>

![processus de développement d’objets de stratégie de groupe](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="e662a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e662a-122">Requirements</span></span>


<span data-ttu-id="e662a-123">Les ordinateurs sur lesquels vous souhaitez installer AGPM doivent respecter les exigences suivantes et vous devez créer des comptes à utiliser dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="e662a-123">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

### <span data-ttu-id="e662a-124">Configuration requise pour le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="e662a-124">AGPM Server requirements</span></span>

<span data-ttu-id="e662a-125">Le serveur AGPM Server 2.5 nécessite Vista® (version 32 bits) sans Service Pack ou Windows Server® 2003 (32 bits), ainsi que la console de gestion des stratégies de GPMC.</span><span class="sxs-lookup"><span data-stu-id="e662a-125">AGPM Server2.5 requires WindowsVista® (32-bit version) with no service packs installed or Windows Server®2003 (32-bit version), as well as the GPMC.</span></span> <span data-ttu-id="e662a-126">Par ailleurs, vous devez être membre du groupe Domain Admins pour installer le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-126">Additionally, you must be a member of the Domain Admins group to install AGPM Server.</span></span>

<span data-ttu-id="e662a-127">Vous devez installer le serveur AGPM sur un serveur membre ou un contrôleur de domaine avec la version la plus récente de GPMC qui est disponible pour vous et pris en charge par AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-127">You should install AGPM Server on a member server or domain controller with the most recent version of the GPMC that is available to you and supported by AGPM.</span></span> <span data-ttu-id="e662a-128">AGPM utilise la console GPMC pour sauvegarder et restaurer des objets de stratégie de groupe, et les versions plus récentes de la console GPMC fournissent des paramètres de stratégie supplémentaires qui ne sont pas disponibles dans les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="e662a-128">AGPM uses the GPMC to back up and restore GPOs, and newer versions of the GPMC provide additional policy settings not available in preceding versions.</span></span> <span data-ttu-id="e662a-129">Si la version de GPMC sur votre serveur AGPM est antérieure à la version sur les ordinateurs utilisés par les administrateurs pour gérer la stratégie de groupe, le serveur AGPM ne sera pas en mesure de stocker ces paramètres de stratégie qui ne sont pas disponibles dans l’ancienne version de GPMC.</span><span class="sxs-lookup"><span data-stu-id="e662a-129">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store those policy settings not available in the older version of the GPMC.</span></span>

<span data-ttu-id="e662a-130">Plus précisément, si votre serveur AGPM exécute Windows Server2003 et la version de la console de gestion des stratégies de groupe qui l’accompagnent et que les ordinateurs de l’administrateur de la stratégie de groupe exécutent Vista et la version de la console de gestion des stratégies de groupe, vous pouvez toujours gérer la plupart des paramètres de stratégie.</span><span class="sxs-lookup"><span data-stu-id="e662a-130">Specifically, if your AGPM Server is running Windows Server2003 and the version of the GPMC that accompanied it, and your Group Policy administrators’ computers are running WindowsVista and the version of the GPMC that accompanied it, you can still manage most policy settings.</span></span> <span data-ttu-id="e662a-131">Toutefois, les paramètres de stratégie de la console GPMC dans Windows Vista qui ne sont pas disponibles dans la console GPMC de Windows Server 2003, tels que ceux liés à la redirection de dossiers, au réseau sans fil (IEEE 802,11) et aux imprimantes déployées, ne peuvent pas être stockés par le serveur AGPM, même si les administrateurs peuvent les configurer à l’aide d’AGPM sur leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e662a-131">However, policy settings from the GPMC in Windows Vista that are not available in the GPMC in Windows Server 2003—such as those related to folder redirection, wireless networking (IEEE 802.11), and deployed printers—cannot be stored by the AGPM Server, even though administrators can configure them using AGPM on their computers.</span></span>

<span data-ttu-id="e662a-132">Si vous devez installer le serveur AGPM sur un ordinateur doté d’une version plus ancienne de GPMC que les administrateurs de stratégie de groupe en cours d’exécution, voir les informations de référence des paramètres de stratégie de groupe pour plus d’informations sur les paramètres de stratégie disponibles pour les systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e662a-132">If you must install AGPM Server on a computer with an older version of GPMC than your Group Policy administrators are running, see the Group Policy Settings Reference for details about which policy settings are available with which operating systems.</span></span> <span data-ttu-id="e662a-133">Pour télécharger la référence des paramètres de stratégie de groupe, reportez-vous à la section <https://go.microsoft.com/fwlink/?LinkID=106147> .</span><span class="sxs-lookup"><span data-stu-id="e662a-133">To download the Group Policy Settings Reference, see <https://go.microsoft.com/fwlink/?LinkID=106147>.</span></span>

<span data-ttu-id="e662a-134">**Remarques**  Les archives ne peuvent pas être déplacées à partir d’un serveur AGPM ou d’un serveur GPOVault exécutant Windows Server2003 vers un serveur AGPM exécutant Vista.</span><span class="sxs-lookup"><span data-stu-id="e662a-134">**Note** Archives cannot be migrated from an AGPM Server or a GPOVault Server running Windows Server2003 to an AGPM Server running WindowsVista.</span></span>

<span data-ttu-id="e662a-135">Pour Windows Server2003, si GPOVault Server est installé sur l’ordinateur sur lequel vous voulez installer le serveur AGPM, il est recommandé de ne pas désinstaller GPOVault Server avant de commencer l’installation.</span><span class="sxs-lookup"><span data-stu-id="e662a-135">For Windows Server2003, if GPOVault Server is installed on the computer on which you want to install AGPM Server, it is recommended that you do not uninstall GPOVault Server before beginning the installation.</span></span> <span data-ttu-id="e662a-136">L’installation d’AGPM Server désinstallera GPOVault Server et transférera automatiquement vos données d’archive GPOVault existantes vers une archive AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-136">The installation of AGPM Server will uninstall GPOVault Server and automatically transfer your existing GPOVault archive data to an AGPM archive.</span></span>

 

### <span data-ttu-id="e662a-137">Configuration requise pour le client AGPM</span><span class="sxs-lookup"><span data-stu-id="e662a-137">AGPM Client requirements</span></span>

<span data-ttu-id="e662a-138">Le client AGPM est requis pour Vista (version 32 bits) sans Service Pack ou Windows Server2003 (version 32 bits), ainsi que la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="e662a-138">AGPM Client2.5 requires WindowsVista (32-bit version) with no service packs installed or Windows Server2003 (32-bit version), as well as the GPMC.</span></span> <span data-ttu-id="e662a-139">Le client AGPM peut être installé sur un ordinateur exécutant AGPM Server.</span><span class="sxs-lookup"><span data-stu-id="e662a-139">AGPM Client can be installed on a computer running AGPM Server.</span></span>

### <span data-ttu-id="e662a-140">Exigences de scénarios</span><span class="sxs-lookup"><span data-stu-id="e662a-140">Scenario requirements</span></span>

<span data-ttu-id="e662a-141">Avant de commencer ce scénario, vous devez créer quatre comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e662a-141">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="e662a-142">Pendant le scénario, vous devez attribuer l’un des rôles AGPM suivants à chacun de ces comptes: Administrateur AGPM (contrôle total), approbateur, éditeur et relecteur.</span><span class="sxs-lookup"><span data-stu-id="e662a-142">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="e662a-143">Ces comptes doivent être en mesure d’envoyer et de recevoir des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="e662a-143">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="e662a-144">Attribution d’autorisations d’accès aux **objets liés** aux comptes avec l’administrateur d’AGPM, l’approbateur et (facultatif) des rôles d’éditeur.</span><span class="sxs-lookup"><span data-stu-id="e662a-144">Assign **Link GPOs** permission to the accounts with the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="e662a-145">**Remarques** 
 L’autorisation **lier les objets de stratégie de groupe** est affectée par défaut aux membres des administrateurs de domaine et des administrateurs d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="e662a-145">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="e662a-146">Pour affecter **des** autorisations d’accès de l’utilisateur à des groupes ou des utilisateurs supplémentaires (par exemple, des comptes ayant le rôle d’administrateur ou d’approbation AGPM), cliquez sur le nœud du domaine, puis cliquez sur l’onglet **délégation** , sélectionnez **lier les objets de stratégie de groupe**, cliquez sur **Ajouter**, et sélectionnez des utilisateurs ou des groupes auxquels vous voulez accorder l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="e662a-146">To assign **Link GPOs** permission to additional users or groups (such as accounts with the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which to assign the permission.</span></span>

 

<span data-ttu-id="e662a-147">Pour ce scénario, vous devez effectuer des actions avec différents comptes.</span><span class="sxs-lookup"><span data-stu-id="e662a-147">For this scenario, you perform actions with different accounts.</span></span> <span data-ttu-id="e662a-148">Vous pouvez vous connecter avec chaque compte comme indiqué, ou utiliser la commande **exécuter en tant que** pour démarrer la console de gestion des stratégies de gestion des stratégies avec le compte indiqué.</span><span class="sxs-lookup"><span data-stu-id="e662a-148">You can either log on with each account as indicated, or you can use the **Run as** command to start the GPMC with the indicated account.</span></span>

<span data-ttu-id="e662a-149">**Remarques**  Pour utiliser la commande **exécuter en tant que** avec la console GPMC sur Windows Server2003, cliquez sur **Démarrer**, pointez sur **Outils d’administration**, cliquez avec le bouton droit sur **gestion des stratégies de groupe**, puis cliquez sur **exécuter en tant que**.</span><span class="sxs-lookup"><span data-stu-id="e662a-149">**Note** To use the **Run as** command with GPMC on Windows Server2003, click **Start**, point to **Administrative Tools**, right-click **Group Policy Management**, and click **Run as**.</span></span> <span data-ttu-id="e662a-150">Cliquez sur **l’utilisateur suivant** et entrez les informations d’identification d’un compte.</span><span class="sxs-lookup"><span data-stu-id="e662a-150">Click **The following user** and enter credentials for an account.</span></span>

<span data-ttu-id="e662a-151">Pour utiliser la commande **exécuter en tant que** avec la console GPMC sur Windows Vista, cliquez sur le bouton **Démarrer** , pointez sur **exécuter**, puis tapez **runas/user:** <em> DomainName\\UserName </em> **"mmc%windir%\\system32\\gpmc.msc"**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e662a-151">To use the **Run as** command with GPMC on Windows Vista, click the **Start** button, point to **Run**, and type **runas /user:**<em>DomainName\\UserName</em>**"mmc %windir%\\system32\\gpmc.msc"**, and click **OK**.</span></span> <span data-ttu-id="e662a-152">Lorsque vous y êtes invité, entrez le mot de passe du compte.</span><span class="sxs-lookup"><span data-stu-id="e662a-152">Type the password for the account when prompted.</span></span>

 

## <span data-ttu-id="e662a-153">Procédures d’installation et de configuration d’AGPM</span><span class="sxs-lookup"><span data-stu-id="e662a-153">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="e662a-154">Pour installer et configurer AGPM, vous devez procéder comme suit.</span><span class="sxs-lookup"><span data-stu-id="e662a-154">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="e662a-155">Étape 1: installer le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="e662a-155">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="e662a-156">Étape 2: installer le client AGPM</span><span class="sxs-lookup"><span data-stu-id="e662a-156">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="e662a-157">Étape 3: configurer une connexion de serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="e662a-157">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="e662a-158">Étape 4: configurer les notifications par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="e662a-158">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="e662a-159">Étape 5: accès délégué</span><span class="sxs-lookup"><span data-stu-id="e662a-159">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="e662a-160">Étape 1: installer le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="e662a-160">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="e662a-161">Dans cette étape, vous installez le serveur AGPM sur le serveur membre ou le contrôleur de domaine qui exécute le service AGPM et vous configurez l’archive.</span><span class="sxs-lookup"><span data-stu-id="e662a-161">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="e662a-162">Toutes les opérations AGPM sont gérées par le biais de ce service Windows et sont exécutées avec les informations d’identification du service.</span><span class="sxs-lookup"><span data-stu-id="e662a-162">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="e662a-163">L’archive gérée par un serveur AGPM peut être hébergée sur ce serveur ou sur un autre serveur dans la même forêt.</span><span class="sxs-lookup"><span data-stu-id="e662a-163">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="e662a-164">Pour installer le serveur AGPM sur l’ordinateur qui hébergera le service AGPM</span><span class="sxs-lookup"><span data-stu-id="e662a-164">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="e662a-165">Ouvrez une session avec un compte membre du groupe administrateurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="e662a-165">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="e662a-166">Démarrez le CD-ROM Microsoft Desktop Optimization Pack et suivez les instructions qui s’affichent à l’écran pour sélectionner **Advanced Group Management Policy-Server**.</span><span class="sxs-lookup"><span data-stu-id="e662a-166">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="e662a-167">Dans la boîte de dialogue **Bienvenue** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e662a-167">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="e662a-168">Dans la boîte de dialogue **termes du contrat de licence logiciel Microsoft** , acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e662a-168">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

5.  <span data-ttu-id="e662a-169">Dans la boîte de dialogue Path de l' **application** , sélectionnez un emplacement pour installer le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-169">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="e662a-170">L’ordinateur sur lequel le serveur AGPM est installé doit héberger le service AGPM et gérer l’archive.</span><span class="sxs-lookup"><span data-stu-id="e662a-170">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="e662a-171">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e662a-171">Click **Next**.</span></span>

6.  <span data-ttu-id="e662a-172">Dans la boîte de dialogue **path Archive** , sélectionnez un emplacement pour l’archivage relatif au serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-172">In the **Archive Path** dialog box, select a location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="e662a-173">Le chemin d’accès d’archive peut pointer vers un dossier sur le serveur AGPM ou un autre emplacement, mais vous devez sélectionner un emplacement dont l’espace disponible est suffisant pour stocker tous les objets de stratégie de groupe et les données d’historique gérés par ce serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-173">The archive path can point to a folder on the AGPM Server or elsewhere, but you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="e662a-174">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e662a-174">Click **Next**.</span></span>

7.  <span data-ttu-id="e662a-175">Dans la boîte de dialogue **compte de service AGPM** , sélectionnez un compte de service sous lequel le service AGPM sera exécuté, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e662a-175">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

8.  <span data-ttu-id="e662a-176">Dans la boîte de dialogue **Archiver le propriétaire** , sélectionnez le compte ou le groupe auquel attribuer le rôle d’administrateur AGPM (contrôle total).</span><span class="sxs-lookup"><span data-stu-id="e662a-176">In the **Archive Owner** dialog box, select an account or group to which to initially assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="e662a-177">Cet administrateur AGPM peut attribuer des rôles et autorisations d’AGPM aux autres administrateurs de stratégie de groupe (y compris le rôle d’administrateur AGPM).</span><span class="sxs-lookup"><span data-stu-id="e662a-177">This AGPM Administrator can assign AGPM roles and permissions to other Group Policy administrators (including the role of AGPM Administrator).</span></span> <span data-ttu-id="e662a-178">Pour ce scénario, sélectionnez le compte que vous voulez faire dans le rôle administrateur d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-178">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="e662a-179">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e662a-179">Click **Next**.</span></span>

9.  <span data-ttu-id="e662a-180">Cliquez sur **installer**, puis cliquez sur **Terminer** pour quitter l’Assistant installation.</span><span class="sxs-lookup"><span data-stu-id="e662a-180">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="e662a-181">**Attention**  Ne modifiez pas les paramètres du service AGPM via les outils et **services** **d’administration** du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e662a-181">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="e662a-182">Cela peut empêcher le démarrage du service AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-182">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="e662a-183">Pour plus d’informations sur la modification des paramètres du service, voir aide pour la gestion avancée des stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-183">For information on how to modify settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="e662a-184">Étape 2: installer le client AGPM</span><span class="sxs-lookup"><span data-stu-id="e662a-184">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="e662a-185">Chaque administrateur de stratégie de groupe (qui crée, modifie, déploie, révise ou supprime des objets de stratégie de groupe) doit disposer d’un client AGPM sur les ordinateurs qu’il utilise pour gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-185">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="e662a-186">Pour ce scénario, vous installez le client AGPM sur au moins un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e662a-186">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="e662a-187">Vous n’avez pas besoin d’installer le client AGPM sur les ordinateurs des utilisateurs finaux qui n’effectuent pas d’administration de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-187">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="e662a-188">Pour installer le client AGPM sur l’ordinateur d’un administrateur de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-188">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="e662a-189">Démarrez le CD-ROM Microsoft Desktop Optimization Pack et suivez les instructions à l’écran pour sélectionner **Advanced Group Management Policy-client**.</span><span class="sxs-lookup"><span data-stu-id="e662a-189">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="e662a-190">Dans la boîte de dialogue **Bienvenue** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e662a-190">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="e662a-191">Dans la boîte de dialogue **termes du contrat de licence logiciel Microsoft** , acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="e662a-191">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

4.  <span data-ttu-id="e662a-192">Dans la boîte de dialogue Path de l' **application** , sélectionnez un emplacement pour installer le client AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-192">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="e662a-193">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e662a-193">Click **Next**.</span></span>

5.  <span data-ttu-id="e662a-194">Dans la boîte de dialogue **serveur AGPM** , tapez le nom complet de l’ordinateur et le port du serveur AGPM auquel vous voulez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="e662a-194">In the **AGPM Server** dialog box, type the fully-qualified computer name and the port for the AGPM Server to which to connect.</span></span> <span data-ttu-id="e662a-195">Le port par défaut du service AGPM est 4600.</span><span class="sxs-lookup"><span data-stu-id="e662a-195">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="e662a-196">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e662a-196">Click **Next**.</span></span>

6.  <span data-ttu-id="e662a-197">Cliquez sur **installer**, puis cliquez sur **Terminer** pour quitter l’Assistant installation.</span><span class="sxs-lookup"><span data-stu-id="e662a-197">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="e662a-198">Étape 3: configurer une connexion de serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="e662a-198">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="e662a-199">AGPM stocke toutes les versions de chaque objet de stratégie de groupe contrôlé (GPO), c’est-à-dire un objet de stratégie de groupe pour lequel AGPM fournit le contrôle des modifications, dans une archive centrale, de sorte que les administrateurs de stratégie de groupe puissent afficher et modifier les objets de stratégie de groupe hors connexion sans avoir d’impact sur la version déployée de chaque GPO.</span><span class="sxs-lookup"><span data-stu-id="e662a-199">AGPM stores all versions of each controlled Group Policy object (GPO)—a GPO for which AGPM provides change control—in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="e662a-200">Dans cette étape, vous configurez une connexion de serveur AGPM et assurez-vous que tous les administrateurs de stratégie de groupe se connectent au même serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-200">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="e662a-201">(Pour plus d’informations sur la configuration de plusieurs serveurs AGPM, voir aide pour la gestion avancée des stratégies de groupe.)</span><span class="sxs-lookup"><span data-stu-id="e662a-201">(For information about configuring multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="e662a-202">Pour configurer une connexion de serveur AGPM pour tous les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-202">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="e662a-203">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous à l’aide du compte d’utilisateur que vous avez sélectionné comme propriétaire d’archive.</span><span class="sxs-lookup"><span data-stu-id="e662a-203">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="e662a-204">Cet utilisateur a le rôle d’administrateur AGPM (contrôle total).</span><span class="sxs-lookup"><span data-stu-id="e662a-204">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="e662a-205">Cliquez sur **Démarrer**, pointez sur **Outils d’administration**, puis cliquez sur **gestion des stratégies de groupe** pour ouvrir la console de gestion des stratégies de **groupe (GPMC)**.</span><span class="sxs-lookup"><span data-stu-id="e662a-205">Click **Start**, point to **Administrative Tools**, and click **Group Policy Management** to open the **Group Policy Management Console (GPMC)**.</span></span>

3.  <span data-ttu-id="e662a-206">Dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet GPO qui est appliqué à tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-206">In the **Group Policy Management Console** tree, edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="e662a-207">Dans la fenêtre de l' **éditeur d’objets de stratégie de groupe** , cliquez sur **Configuration utilisateur**, **modèles d’administration**et **composants Windows**.</span><span class="sxs-lookup"><span data-stu-id="e662a-207">In the **Group Policy Object Editor** window, click **User Configuration**, **Administrative Templates**, and **Windows Components**.</span></span>

5.  <span data-ttu-id="e662a-208">Si **AGPM** ne figure pas dans la liste **composants Windows**:</span><span class="sxs-lookup"><span data-stu-id="e662a-208">If **AGPM** is not listed under **Windows Components**:</span></span>

    1.  <span data-ttu-id="e662a-209">Cliquez avec le bouton droit sur **modèles d’administration** et sélectionnez **Ajouter/supprimer des modèles**.</span><span class="sxs-lookup"><span data-stu-id="e662a-209">Right-click **Administrative Templates** and select **Add/Remove Templates**.</span></span>

    2.  <span data-ttu-id="e662a-210">Cliquez **sur Ajouter**, sélectionnez **AGPM. admx** ou **AGPM. adm**, cliquez sur **ouvrir**, puis sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-210">Click **Add**, select **agpm.admx** or **agpm.adm**, click **Open**, and then click **Close**.</span></span>

6.  <span data-ttu-id="e662a-211">Sous **composants Windows**, double-cliquez sur **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="e662a-211">Under **Windows Components**, double-click **AGPM**.</span></span>

7.  <span data-ttu-id="e662a-212">Dans le volet Détails, double-cliquez sur le **serveur AGPM (tous les domaines)**.</span><span class="sxs-lookup"><span data-stu-id="e662a-212">In the details pane, double-click **AGPM Server (all domains)**.</span></span>

8.  <span data-ttu-id="e662a-213">Dans la fenêtre de **Propriétés de serveur AGPM (toutes les domaines)** , sélectionnez **activé** , puis entrez le nom et le port complets de l’ordinateur (par exemple, Server.contoso.com:4600) pour le serveur hébergeant l’archive.</span><span class="sxs-lookup"><span data-stu-id="e662a-213">In the **AGPM Server (all domains) Properties** window, select **Enabled** and type the fully-qualified computer name and port (for example, server.contoso.com:4600) for the server hosting the archive.</span></span> <span data-ttu-id="e662a-214">Le port utilisé par le service AGPM est le port 4600.</span><span class="sxs-lookup"><span data-stu-id="e662a-214">The port used by the AGPM Service is port 4600.</span></span>

9.  <span data-ttu-id="e662a-215">Cliquez sur **OK**, puis fermez la fenêtre **éditeur d’objets de stratégie de groupe** .</span><span class="sxs-lookup"><span data-stu-id="e662a-215">Click **OK**, and then close the **Group Policy Object Editor** window.</span></span> <span data-ttu-id="e662a-216">Lorsque la stratégie de groupe est mise à jour, la connexion au serveur AGPM est configurée pour chaque administrateur de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-216">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="e662a-217">Étape 4: configurer les notifications par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="e662a-217">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="e662a-218">En tant qu’administrateur AGPM (contrôle total), vous désignez les adresses de courrier des approbateurs et des administrateurs AGPM auxquels un message électronique contenant une demande est envoyé lorsqu’un éditeur tente de créer, de déployer ou de supprimer un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-218">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message containing a request is sent when an Editor attempts to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="e662a-219">Vous déterminez également l’alias à partir duquel ces messages sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="e662a-219">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="e662a-220">Pour configurer les notifications par courrier électronique pour AGPM</span><span class="sxs-lookup"><span data-stu-id="e662a-220">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="e662a-221">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-221">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e662a-222">Dans le volet Détails, cliquez sur l’onglet **délégation de domaine** .</span><span class="sxs-lookup"><span data-stu-id="e662a-222">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="e662a-223">Dans le champ **de** , tapez l’alias de messagerie pour AGPM à partir duquel envoyer les notifications.</span><span class="sxs-lookup"><span data-stu-id="e662a-223">In the **From** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="e662a-224">Dans le champ **à** , tapez l’adresse de courrier du compte d’utilisateur auquel vous souhaitez attribuer le rôle d’approbateur.</span><span class="sxs-lookup"><span data-stu-id="e662a-224">In the **To** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

5.  <span data-ttu-id="e662a-225">Dans le champ **serveur SMTP** , tapez un serveur de messagerie SMTP valide.</span><span class="sxs-lookup"><span data-stu-id="e662a-225">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="e662a-226">Dans les champs **nom d’utilisateur** et **mot de passe** , tapez les informations d’identification d’un utilisateur ayant accès au service SMTP.</span><span class="sxs-lookup"><span data-stu-id="e662a-226">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="e662a-227">Cliquez sur **Apply** (Appliquer).</span><span class="sxs-lookup"><span data-stu-id="e662a-227">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="e662a-228">Étape 5: accès délégué</span><span class="sxs-lookup"><span data-stu-id="e662a-228">Step 5: Delegate access</span></span>

<span data-ttu-id="e662a-229">En tant qu’administrateur AGPM (contrôle total), vous déléguez l’accès au niveau du domaine aux objets de stratégie de groupe, en attribuant des rôles au compte de chaque administrateur de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-229">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="e662a-230">**Remarques**  Vous pouvez également déléguer l’accès au niveau de l’objet GPO plutôt qu’au niveau du domaine.</span><span class="sxs-lookup"><span data-stu-id="e662a-230">**Note** You can also delegate access at the GPO level rather than the domain level.</span></span> <span data-ttu-id="e662a-231">Pour plus d’informations, consultez aide pour la gestion avancée des stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-231">For details, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="e662a-232">**Important**  Nous vous conseillons de limiter l’appartenance au groupe de propriétaires de la stratégie de groupe, afin qu’il ne puisse pas être utilisé pour contourner la gestion d’AGPM d’Access aux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-232">**Important** You should restrict membership in the Group Policy Creator Owners group, so it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="e662a-233">(Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)</span><span class="sxs-lookup"><span data-stu-id="e662a-233">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="e662a-234">Pour déléguer l’accès à tous les objets de stratégie de groupe dans un domaine</span><span class="sxs-lookup"><span data-stu-id="e662a-234">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="e662a-235">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-235">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="e662a-236">Dans l’onglet **délégation de domaine** , cliquez sur le bouton **avancé** .</span><span class="sxs-lookup"><span data-stu-id="e662a-236">On the **Domain Delegation** tab, click the **Advanced** button.</span></span>

3.  <span data-ttu-id="e662a-237">Dans la boîte de dialogue **autorisations** :</span><span class="sxs-lookup"><span data-stu-id="e662a-237">In the **Permissions** dialog box:</span></span>

    1.  <span data-ttu-id="e662a-238">Cliquez sur le compte d’utilisateur d’un administrateur de stratégie de groupe, puis activez la case à cocher **approbateur** pour attribuer ce rôle au compte.</span><span class="sxs-lookup"><span data-stu-id="e662a-238">Click the user account of a Group Policy administrator, and then select the **Approver** check box to assign that role to the account.</span></span> <span data-ttu-id="e662a-239">Désactivez la case à cocher **éditeur** .</span><span class="sxs-lookup"><span data-stu-id="e662a-239">Clear the **Editor** check box.</span></span> <span data-ttu-id="e662a-240">(Ce rôle inclut le rôle de réviseur.)</span><span class="sxs-lookup"><span data-stu-id="e662a-240">(This role includes the Reviewer role.)</span></span>

    2.  <span data-ttu-id="e662a-241">Cliquez sur le compte d’utilisateur d’un autre administrateur de stratégie de groupe, puis activez la case à cocher **éditeur** pour attribuer ce rôle au compte.</span><span class="sxs-lookup"><span data-stu-id="e662a-241">Click the user account of another Group Policy administrator, and then select the **Editor** check box to assign that role to the account.</span></span> <span data-ttu-id="e662a-242">(Ce rôle inclut le rôle de réviseur.)</span><span class="sxs-lookup"><span data-stu-id="e662a-242">(This role includes the Reviewer role.)</span></span>

    3.  <span data-ttu-id="e662a-243">Cliquez sur un troisième compte, puis activez la case à cocher **relecteur** pour affecter uniquement le rôle de réviseur au compte de l’administrateur de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-243">Click a third account and then select the **Reviewer** check box to assign only the Reviewer role to the account of that Group Policy administrator.</span></span> <span data-ttu-id="e662a-244">Désactivez la case à cocher **éditeur** .</span><span class="sxs-lookup"><span data-stu-id="e662a-244">Clear the **Editor** check box.</span></span>

    4.  <span data-ttu-id="e662a-245">Cliquez sur le bouton **avancé** .</span><span class="sxs-lookup"><span data-stu-id="e662a-245">Click the **Advanced** button.</span></span>

4.  <span data-ttu-id="e662a-246">Dans la boîte de dialogue **paramètres de sécurité avancés** :</span><span class="sxs-lookup"><span data-stu-id="e662a-246">In the **Advanced Security Settings** dialog box:</span></span>

    1.  <span data-ttu-id="e662a-247">Sélectionnez un administrateur de stratégie de groupe, puis cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="e662a-247">Select a Group Policy administrator, and then click **Edit**.</span></span>

    2.  <span data-ttu-id="e662a-248">Pour **appliquer**à, sélectionnez **cet objet et les objets imbriqués**, puis cliquez sur **OK** dans la boîte de dialogue **entrée** d' **autorisation** .</span><span class="sxs-lookup"><span data-stu-id="e662a-248">For **Apply onto**, select **This object and nested objects**, and then click **OK** in the **Permission** **Entry** dialog box.</span></span>

    3.  <span data-ttu-id="e662a-249">Répétez l’opération pour chaque administrateur de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-249">Repeat for each Group Policy administrator.</span></span>

5.  <span data-ttu-id="e662a-250">Dans la boîte de dialogue **paramètres de sécurité avancés** , cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e662a-250">In the **Advanced Security Settings** dialog box, click **OK**.</span></span>

6.  <span data-ttu-id="e662a-251">Dans la boîte de dialogue **autorisations** , cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e662a-251">In the **Permissions** dialog box, click **OK**.</span></span>

## <span data-ttu-id="e662a-252">Procédure de gestion des objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-252">Steps for managing GPOs</span></span>


<span data-ttu-id="e662a-253">Vous devez effectuer les étapes suivantes pour créer, modifier, réviser et déployer des objets de stratégie de groupe à l’aide d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-253">You must complete the following steps to create, edit, review, and deploy GPOs using AGPM.</span></span> <span data-ttu-id="e662a-254">Par ailleurs, vous allez créer un modèle, supprimer un objet de stratégie de groupe, puis restaurer un objet GPO supprimé.</span><span class="sxs-lookup"><span data-stu-id="e662a-254">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="e662a-255">Étape 1: créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-255">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="e662a-256">Étape 2: modifier un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-256">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="e662a-257">Étape 3: vérifier et déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-257">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="e662a-258">Étape 4: utiliser un modèle pour créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-258">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="e662a-259">Étape 5: supprimer et restaurer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-259">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="e662a-260">Étape 1: créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-260">Step 1: Create a GPO</span></span>

<span data-ttu-id="e662a-261">Dans un environnement doté de plusieurs administrateurs de stratégie de groupe, les utilisateurs dotés du rôle d’éditeur peuvent demander la création de nouveaux objets de stratégie de groupe, mais une telle demande doit être approuvée par une personne ayant le rôle d’approbateur, car la création d’un nouvel objet GPO a un impact sur l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="e662a-261">In an environment with multiple Group Policy administrators, those with the Editor role have the ability to request the creation of new GPOs, but such a request must be approved by someone with the Approver role because the creation of a new GPO impacts the production environment.</span></span>

<span data-ttu-id="e662a-262">Dans cette étape, vous utiliserez un compte avec le rôle d’éditeur pour demander la création d’un nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-262">In this step, you use an account with the Editor role to request the creation of a new GPO.</span></span> <span data-ttu-id="e662a-263">En utilisant un compte doté du rôle Approbateur, vous approuvez cette demande et terminerez la création d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-263">Using an account with the Approver role, you approve this request and complete the creation of a GPO.</span></span>

**<span data-ttu-id="e662a-264">Pour demander la création d’un nouvel objet de stratégie de groupe géré via AGPM</span><span class="sxs-lookup"><span data-stu-id="e662a-264">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="e662a-265">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’éditeur a été attribué dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-265">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="e662a-266">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-266">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="e662a-267">Cliquez avec le bouton droit sur le nœud de **contrôle de modification** , puis cliquez sur **nouvel objet de stratégie de**contrôle.</span><span class="sxs-lookup"><span data-stu-id="e662a-267">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="e662a-268">Dans la boîte de dialogue **nouvel objet GPO contrôlé** :</span><span class="sxs-lookup"><span data-stu-id="e662a-268">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="e662a-269">Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .</span><span class="sxs-lookup"><span data-stu-id="e662a-269">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="e662a-270">Tapez **MyGPO** comme nom du nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-270">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="e662a-271">Tapez un commentaire pour le nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-271">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="e662a-272">Cliquez sur **créer Live** pour que le nouvel objet GPO soit déployé sur l’environnement de production immédiatement après approbation.</span><span class="sxs-lookup"><span data-stu-id="e662a-272">Click **Create live** so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="e662a-273">Cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-273">Click **Submit**.</span></span>

5.  <span data-ttu-id="e662a-274">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-274">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e662a-275">Le nouvel objet GPO est affiché dans l’onglet **en attente** .</span><span class="sxs-lookup"><span data-stu-id="e662a-275">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="e662a-276">Pour approuver la demande en attente de création d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-276">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="e662a-277">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’approbateur dans AGPM s’est attribué.</span><span class="sxs-lookup"><span data-stu-id="e662a-277">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="e662a-278">Ouvrez la boîte de réception de votre compte et notez que vous avez reçu un message électronique de l’alias AGPM avec la demande de l’éditeur pour créer un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-278">Open the e-mail inbox for the account, and note that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="e662a-279">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-279">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="e662a-280">Dans l’onglet **contenu** , cliquez sur l’onglet **en attente** pour afficher les objets de stratégie de groupe en attente.</span><span class="sxs-lookup"><span data-stu-id="e662a-280">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="e662a-281">Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **approuver**.</span><span class="sxs-lookup"><span data-stu-id="e662a-281">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="e662a-282">Cliquez sur **Oui** pour confirmer l’approbation de la création de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-282">Click **Yes** to confirm approval of the creation of the GPO.</span></span> <span data-ttu-id="e662a-283">L’objet de stratégie de groupe est déplacé vers l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="e662a-283">The GPO is moved to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="e662a-284">Étape 2: modifier un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-284">Step 2: Edit a GPO</span></span>

<span data-ttu-id="e662a-285">Vous pouvez utiliser les objets de stratégie de groupe pour configurer les paramètres de l’ordinateur ou de l’utilisateur et les déployer sur de nombreux ordinateurs ou utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e662a-285">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="e662a-286">Dans cette étape, vous utiliserez un compte avec le rôle d’éditeur pour extraire un objet de stratégie de groupe de l’archive, modifier l’objet de stratégie de groupe en mode hors connexion, Rechercher l’objet GPO modifié dans l’archive et demander le déploiement de l’objet de stratégie de groupe dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="e662a-286">In this step, you use an account with the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="e662a-287">Pour ce scénario, vous devez configurer un paramètre dans l’objet de stratégie de groupe pour exiger que le mot de passe comporte au moins huit caractères.</span><span class="sxs-lookup"><span data-stu-id="e662a-287">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters in length.</span></span>

**<span data-ttu-id="e662a-288">Pour extraire l’objet de stratégie de groupe de l’archive en vue de le modifier</span><span class="sxs-lookup"><span data-stu-id="e662a-288">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="e662a-289">Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’éditeur a été attribué dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-289">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="e662a-290">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-290">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="e662a-291">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="e662a-291">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="e662a-292">Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **extraire**.</span><span class="sxs-lookup"><span data-stu-id="e662a-292">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="e662a-293">Tapez un commentaire à afficher dans l' **historique** de l’objet de stratégie de groupe lors de son extraction, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e662a-293">Type a comment to be displayed in the **History** of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="e662a-294">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-294">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e662a-295">Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **extrait**.</span><span class="sxs-lookup"><span data-stu-id="e662a-295">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="e662a-296">Pour modifier l’objet de stratégie de groupe hors connexion et configurer la longueur de mot de passe minimum</span><span class="sxs-lookup"><span data-stu-id="e662a-296">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="e662a-297">Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **modifier** pour ouvrir la fenêtre Éditeur d’objets de stratégie de groupe et apporter des modifications à une copie hors connexion de l’objet de stratégie de **groupe** .</span><span class="sxs-lookup"><span data-stu-id="e662a-297">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Object Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="e662a-298">Pour ce scénario, configurez la longueur minimale du mot de passe:</span><span class="sxs-lookup"><span data-stu-id="e662a-298">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="e662a-299">Sous **Configuration ordinateur**, double-cliquez sur **Paramètres Windows**, cliquez deux fois sur **paramètres de sécurité**, double-cliquez sur stratégies de **compte**, puis double-cliquez sur **stratégie de mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="e662a-299">Under **Computer Configuration**, double-click **Windows Settings**, double-click **Security Settings**, double-click **Account Policies**, and double-click **Password Policy**.</span></span>

    2.  <span data-ttu-id="e662a-300">Dans le volet Détails, double-cliquez sur **longueur minimale du mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="e662a-300">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="e662a-301">Dans la fenêtre Propriétés, activez la case à cocher **définir ce paramètre de stratégie** , définissez le nombre de caractères sur **8**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e662a-301">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="e662a-302">Fermez la fenêtre de l' **éditeur d’objets de stratégie de groupe** .</span><span class="sxs-lookup"><span data-stu-id="e662a-302">Close the **Group Policy Object Editor** window.</span></span>

**<span data-ttu-id="e662a-303">Pour archiver l’objet de stratégie de groupe dans l’archive</span><span class="sxs-lookup"><span data-stu-id="e662a-303">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="e662a-304">Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyGPO** , puis cliquez sur **Archiver**.</span><span class="sxs-lookup"><span data-stu-id="e662a-304">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="e662a-305">Tapez un commentaire, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e662a-305">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="e662a-306">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-306">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e662a-307">Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **Archivé**.</span><span class="sxs-lookup"><span data-stu-id="e662a-307">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="e662a-308">Pour demander le déploiement de l’objet de stratégie de groupe dans l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="e662a-308">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="e662a-309">Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyGPO** , puis cliquez sur **déployer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-309">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="e662a-310">Dans la mesure où ce compte n’est pas un approbateur ou un administrateur AGPM, vous devez fournir une demande de déploiement.</span><span class="sxs-lookup"><span data-stu-id="e662a-310">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="e662a-311">Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .</span><span class="sxs-lookup"><span data-stu-id="e662a-311">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="e662a-312">Tapez un commentaire à afficher dans l' **historique** de l’objet de stratégie de groupe, puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="e662a-312">Type a comment to be displayed in the **History** of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="e662a-313">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-313">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e662a-314">**MyGPO** s’affiche dans la liste des objets de stratégie de groupe sous l’onglet **en attente** .</span><span class="sxs-lookup"><span data-stu-id="e662a-314">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="e662a-315">Étape 3: vérifier et déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-315">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="e662a-316">Dans le cadre de cette étape, vous agissez en tant qu’approbateur, vous créez des rapports et vous analysez les paramètres et les modifications apportées aux paramètres dans l’objet de stratégie de groupe pour déterminer s’ils doivent être approuvés.</span><span class="sxs-lookup"><span data-stu-id="e662a-316">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="e662a-317">Après avoir évalué l’objet de stratégie de groupe, vous le déployez dans l’environnement de production et le liez à un domaine ou à une unité d’organisation (UO) de sorte qu’il soit appliqué lorsque la stratégie de groupe est actualisée pour les ordinateurs de ce domaine ou UO.</span><span class="sxs-lookup"><span data-stu-id="e662a-317">After evaluating the GPO, you deploy it to the production environment and link it to a domain or an organizational unit (OU) so that it takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="e662a-318">Pour vérifier les paramètres de l’objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-318">To review settings in the GPO</span></span>**

1.  <span data-ttu-id="e662a-319">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’approbateur dans AGPM s’est attribué.</span><span class="sxs-lookup"><span data-stu-id="e662a-319">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="e662a-320">(N’importe quel administrateur de stratégie de groupe avec le rôle de relecteur, qui est inclus dans tous les autres rôles, peut consulter les paramètres d’un objet de stratégie de groupe).</span><span class="sxs-lookup"><span data-stu-id="e662a-320">(Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.)</span></span>

2.  <span data-ttu-id="e662a-321">Ouvrez la boîte de réception du compte et notez que vous avez reçu un message électronique de l’alias AGPM avec une demande d’éditeur pour le déploiement d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-321">Open the e-mail inbox for the account and note that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3.  <span data-ttu-id="e662a-322">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-322">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="e662a-323">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **en attente** .</span><span class="sxs-lookup"><span data-stu-id="e662a-323">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5.  <span data-ttu-id="e662a-324">Double-cliquez sur **MyGPO** pour afficher son historique.</span><span class="sxs-lookup"><span data-stu-id="e662a-324">Double-click **MyGPO** to display its history.</span></span>

6.  <span data-ttu-id="e662a-325">Passez en revue les paramètres dans la version la plus récente de MyGPO:</span><span class="sxs-lookup"><span data-stu-id="e662a-325">Review the settings in the most recent version of MyGPO:</span></span>

    1.  <span data-ttu-id="e662a-326">Dans la fenêtre **historique** , cliquez avec le bouton droit sur la version de l’objet de stratégie de groupe avec le dateur le plus récent, cliquez sur **paramètres**, puis sur **rapport HTML** pour afficher un récapitulatif des paramètres de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-326">In the **History** window, right-click the GPO version with the most recent timestamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

    2.  <span data-ttu-id="e662a-327">Dans le navigateur Web, cliquez sur **Afficher tout** pour afficher tous les paramètres de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-327">In the Web browser, click **show all** to display all of the settings in the GPO.</span></span>

    3.  <span data-ttu-id="e662a-328">Fermez le navigateur.</span><span class="sxs-lookup"><span data-stu-id="e662a-328">Close the browser.</span></span>

7.  <span data-ttu-id="e662a-329">Comparez la version la plus récente de MyGPO à la première version archivée dans l’archive:</span><span class="sxs-lookup"><span data-stu-id="e662a-329">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

    1.  <span data-ttu-id="e662a-330">Dans la fenêtre **historique** , cliquez sur la version de l’objet de stratégie de groupe avec le dateur le plus récent.</span><span class="sxs-lookup"><span data-stu-id="e662a-330">In the **History** window, click the GPO version with the most recent timestamp.</span></span> <span data-ttu-id="e662a-331">Maintenez la **touche CTRL enfoncée** et cliquez sur la version de l’objet de stratégie de groupe le plus ancien avec l’état **Archivé**.</span><span class="sxs-lookup"><span data-stu-id="e662a-331">Press **CTRL** and click the oldest GPO version that has a state of **Checked In**.</span></span>

    2.  <span data-ttu-id="e662a-332">Cliquez sur le bouton **différences** .</span><span class="sxs-lookup"><span data-stu-id="e662a-332">Click the **Differences** button.</span></span> <span data-ttu-id="e662a-333">La section **stratégies de compte/stratégie de mot de passe** est mise en évidence en vert et précédée de **\ [+ \]**, ce qui indique que ce paramètre est configuré uniquement dans la dernière version de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-333">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**, indicating that this setting is configured only in the latter version of the GPO.</span></span>

    3.  <span data-ttu-id="e662a-334">Cliquez sur **stratégies de compte/stratégie de mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="e662a-334">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="e662a-335">Le paramètre de **longueur minimum du mot de passe** est également mis en surbrillance en vert et précédé de **\ [+ \]** indiquant qu’il est configuré uniquement dans la dernière version de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-335">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

    4.  <span data-ttu-id="e662a-336">Fermez le navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="e662a-336">Close the Web browser.</span></span>

**<span data-ttu-id="e662a-337">Pour déployer l’objet de stratégie de groupe dans l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="e662a-337">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="e662a-338">Dans l’onglet **en attente** , cliquez avec le bouton droit sur **MyGPO** , puis cliquez sur **approuver**.</span><span class="sxs-lookup"><span data-stu-id="e662a-338">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="e662a-339">Tapez un commentaire à inclure dans l’historique de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-339">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="e662a-340">Cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="e662a-340">Click **Yes**.</span></span> <span data-ttu-id="e662a-341">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-341">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e662a-342">L’objet de stratégie de groupe est déployé dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="e662a-342">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="e662a-343">Pour lier l’objet de stratégie de groupe à un domaine ou une unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="e662a-343">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="e662a-344">Dans la console GPMC, cliquez avec le bouton droit sur le domaine ou l’unité d’organisation à laquelle vous voulez appliquer l’objet de stratégie de groupe que vous avez configuré, puis cliquez sur **lier un objet de stratégie de groupe existant**.</span><span class="sxs-lookup"><span data-stu-id="e662a-344">In the GPMC, right-click the domain or an OU to which to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="e662a-345">Dans la boîte de dialogue **Sélectionner un objet GPO** , cliquez sur **MyGPO**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e662a-345">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="e662a-346">Étape 4: utiliser un modèle pour créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-346">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="e662a-347">Dans le cadre de cette étape, vous utiliserez un compte avec le rôle d’éditeur pour créer un modèle (version non modifiable et statique d’un objet de stratégie de groupe) à utiliser comme point de départ pour la création de nouveaux objets de stratégie de groupe, puis créez un nouvel objet de stratégie de groupe basé sur ce modèle.</span><span class="sxs-lookup"><span data-stu-id="e662a-347">In this step, you use an account with the Editor role to create a template—an uneditable, static version of a GPO for use as a starting point for creating new GPOs—and then create a new GPO based upon that template.</span></span> <span data-ttu-id="e662a-348">Les modèles permettent de créer rapidement plusieurs objets de stratégie de groupe qui incluent un grand nombre des mêmes paramètres.</span><span class="sxs-lookup"><span data-stu-id="e662a-348">Templates are useful for quickly creating multiple GPOs that include many of the same settings.</span></span>

**<span data-ttu-id="e662a-349">Pour créer un modèle sur la base d’un objet de stratégie de groupe existant</span><span class="sxs-lookup"><span data-stu-id="e662a-349">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="e662a-350">Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’éditeur a été attribué dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-350">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="e662a-351">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-351">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="e662a-352">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="e662a-352">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="e662a-353">Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **enregistrer en tant que modèle** pour créer un modèle contenant tous les paramètres actuellement dans MyGPO.</span><span class="sxs-lookup"><span data-stu-id="e662a-353">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="e662a-354">Tapez **MyTemplate** comme nom pour le modèle et un commentaire, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e662a-354">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="e662a-355">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-355">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e662a-356">Le nouveau modèle s’affiche sous l’onglet **modèles** .</span><span class="sxs-lookup"><span data-stu-id="e662a-356">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="e662a-357">Pour demander la création d’un nouvel objet de stratégie de groupe géré via AGPM</span><span class="sxs-lookup"><span data-stu-id="e662a-357">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="e662a-358">Cliquez sur l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="e662a-358">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="e662a-359">Cliquez avec le bouton droit sur le nœud de **contrôle de modification** , puis cliquez sur **nouvel objet de stratégie de**contrôle.</span><span class="sxs-lookup"><span data-stu-id="e662a-359">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="e662a-360">Dans la boîte de dialogue **nouvel objet GPO contrôlé** :</span><span class="sxs-lookup"><span data-stu-id="e662a-360">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="e662a-361">Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .</span><span class="sxs-lookup"><span data-stu-id="e662a-361">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="e662a-362">Tapez **MyOtherGPO** comme nom du nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-362">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="e662a-363">Tapez un commentaire pour le nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-363">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="e662a-364">Cliquez sur **créer Live**pour que le nouvel objet GPO soit déployé sur l’environnement de production immédiatement après approbation.</span><span class="sxs-lookup"><span data-stu-id="e662a-364">Click **Create live**, so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="e662a-365">Dans **modèle d’objet de stratégie de groupe**, sélectionnez **MyTemplate**.</span><span class="sxs-lookup"><span data-stu-id="e662a-365">For **From GPO template**, select **MyTemplate**.</span></span>

    6.  <span data-ttu-id="e662a-366">Cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-366">Click **Submit**.</span></span>

4.  <span data-ttu-id="e662a-367">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-367">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e662a-368">Le nouvel objet GPO est affiché dans l’onglet **en attente** .</span><span class="sxs-lookup"><span data-stu-id="e662a-368">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="e662a-369">Utilisez un compte qui a été affecté le rôle d’approbateur pour approuver la demande en attente de création de l’objet de stratégie de groupe, comme vous l’avez fait à l' [étape 1: créer un objet de stratégie de groupe](#bkmk-manage1).</span><span class="sxs-lookup"><span data-stu-id="e662a-369">Use an account that has been assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="e662a-370">MyTemplate incorpore tous les paramètres que vous avez configurés dans MyGPO.</span><span class="sxs-lookup"><span data-stu-id="e662a-370">MyTemplate incorporates all of the settings that you configured in MyGPO.</span></span> <span data-ttu-id="e662a-371">Dans la mesure où MyOtherGPO a été créé à l’aide de MyTemplate, il contient tous les paramètres qui MyGPO contenus au moment de la création de MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="e662a-371">Because MyOtherGPO was created using MyTemplate, it initially contains all of the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="e662a-372">Pour confirmer cela, vous pouvez générer un rapport de différences et comparer MyOtherGPO à MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="e662a-372">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="e662a-373">Pour extraire l’objet de stratégie de groupe de l’archive en vue de le modifier</span><span class="sxs-lookup"><span data-stu-id="e662a-373">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="e662a-374">Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’éditeur a été attribué dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="e662a-374">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="e662a-375">Cliquez avec le bouton droit sur **MyOtherGPO**, puis cliquez sur **extraire**.</span><span class="sxs-lookup"><span data-stu-id="e662a-375">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="e662a-376">Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe lors de son extraction, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e662a-376">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="e662a-377">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-377">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e662a-378">Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **extrait**.</span><span class="sxs-lookup"><span data-stu-id="e662a-378">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="e662a-379">Pour modifier l’objet de stratégie de groupe hors connexion et configurer la durée de verrouillage du compte</span><span class="sxs-lookup"><span data-stu-id="e662a-379">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="e662a-380">Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyOtherGPO**, puis cliquez sur **modifier** pour ouvrir la fenêtre Éditeur d’objets de stratégie de groupe et apporter des modifications à une copie hors connexion de l’objet de stratégie de **groupe** .</span><span class="sxs-lookup"><span data-stu-id="e662a-380">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Object Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="e662a-381">Pour ce scénario, configurez la longueur minimale du mot de passe:</span><span class="sxs-lookup"><span data-stu-id="e662a-381">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="e662a-382">Sous **Configuration ordinateur**, double-cliquez sur **Paramètres Windows**, cliquez deux fois sur **paramètres de sécurité**, double-cliquez sur stratégies de **compte**, puis double-cliquez sur stratégie de **verrouillage du compte**.</span><span class="sxs-lookup"><span data-stu-id="e662a-382">Under **Computer Configuration**, double-click **Windows Settings**, double-click **Security Settings**, double-click **Account Policies**, and double-click **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="e662a-383">Dans le volet Détails, double-cliquez sur **durée de verrouillage du compte**.</span><span class="sxs-lookup"><span data-stu-id="e662a-383">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="e662a-384">Dans la fenêtre Propriétés, activez la case à cocher **définir ce paramètre de stratégie**, définissez une durée de **30** minutes, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e662a-384">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="e662a-385">Fermez la fenêtre de l' **éditeur d’objets de stratégie de groupe** .</span><span class="sxs-lookup"><span data-stu-id="e662a-385">Close the **Group Policy Object Editor** window.</span></span>

<span data-ttu-id="e662a-386">Consultez MyOtherGPO dans l’archive et demandez le déploiement comme vous l’avez fait pour MyGPO à l' [étape 2: modifier un objet de stratégie de groupe](#bkmk-manage2).</span><span class="sxs-lookup"><span data-stu-id="e662a-386">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="e662a-387">Vous pouvez comparer MyOtherGPO à MyGPO ou à MyTemplate à l’aide de rapports de différences.</span><span class="sxs-lookup"><span data-stu-id="e662a-387">You can compare MyOtherGPO to MyGPO or to MyTemplate using difference reports.</span></span> <span data-ttu-id="e662a-388">Tout compte qui inclut le rôle de réviseur (Administrateur AGPM [contrôle total \], approbateur, éditeur ou réviseur) peut générer des rapports.</span><span class="sxs-lookup"><span data-stu-id="e662a-388">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="e662a-389">Pour comparer un objet GPO à un autre et à un modèle</span><span class="sxs-lookup"><span data-stu-id="e662a-389">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="e662a-390">Pour comparer MyGPO et MyOtherGPO:</span><span class="sxs-lookup"><span data-stu-id="e662a-390">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="e662a-391">Dans l’onglet **contrôlé** , cliquez sur **MyGPO**.</span><span class="sxs-lookup"><span data-stu-id="e662a-391">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="e662a-392">Appuyez sur **CTRL** et cliquez sur **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="e662a-392">Press **CTRL** and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="e662a-393">Cliquez avec le bouton droit sur **MyOtherGPO**, pointez sur **différences**, puis cliquez sur **rapport HTML**.</span><span class="sxs-lookup"><span data-stu-id="e662a-393">Right-click **MyOtherGPO**, point to **Differences**, and click **HTML Report**.</span></span>

2.  <span data-ttu-id="e662a-394">Pour comparer MyOtherGPO et MyTemplate:</span><span class="sxs-lookup"><span data-stu-id="e662a-394">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="e662a-395">Dans l’onglet **contrôlé** , cliquez sur **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="e662a-395">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="e662a-396">Cliquez avec le bouton droit sur **MyOtherGPO**, pointez sur **différences**, puis cliquez sur **modèle**.</span><span class="sxs-lookup"><span data-stu-id="e662a-396">Right-click **MyOtherGPO**, point to **Differences**, and click **Template**.</span></span>

    3.  <span data-ttu-id="e662a-397">Sélectionnez **MyTemplate** et **HTML Report**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e662a-397">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="e662a-398">Étape 5: supprimer et restaurer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-398">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="e662a-399">Dans le cadre de cette étape, vous jouerez le rôle d’approbateur pour supprimer un objet GPO.</span><span class="sxs-lookup"><span data-stu-id="e662a-399">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="e662a-400">Pour supprimer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-400">To delete a GPO</span></span>**

1.  <span data-ttu-id="e662a-401">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’approbateur a été attribué.</span><span class="sxs-lookup"><span data-stu-id="e662a-401">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver.</span></span>

2.  <span data-ttu-id="e662a-402">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-402">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="e662a-403">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="e662a-403">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="e662a-404">Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-404">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="e662a-405">Cliquez sur **Supprimer l’objet GPO d’archive et de production** pour supprimer la version dans l’archive ainsi que la version déployée de l’objet de stratégie de groupe dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="e662a-405">Click **Delete GPO from archive and production** to delete both the version in the archive as well as the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="e662a-406">Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e662a-406">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="e662a-407">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-407">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e662a-408">L’objet de stratégie de groupe est supprimé de l’onglet **contrôlé** et s’affiche sous l’onglet de la **Corbeille** , où il peut être restauré ou détruit.</span><span class="sxs-lookup"><span data-stu-id="e662a-408">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="e662a-409">Occasionnellement, il est possible que vous puissiez découvrir après avoir supprimé un objet GPO qu’il est toujours nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e662a-409">Occasionally you may discover after deleting a GPO that it is still needed.</span></span> <span data-ttu-id="e662a-410">Dans le cadre de cette étape, vous vous attendez en tant qu’approbateur de la restauration d’un objet de stratégie de groupe qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="e662a-410">In this step, you act as an Approver to restore a GPO that has been deleted.</span></span>

**<span data-ttu-id="e662a-411">Pour restaurer un objet de stratégie de groupe supprimé</span><span class="sxs-lookup"><span data-stu-id="e662a-411">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="e662a-412">Dans l’onglet **contenu** , cliquez sur l’onglet **Corbeille** pour afficher les objets de stratégie de groupe supprimés.</span><span class="sxs-lookup"><span data-stu-id="e662a-412">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="e662a-413">Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **restaurer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-413">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="e662a-414">Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e662a-414">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="e662a-415">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-415">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e662a-416">L’objet de stratégie de groupe est supprimé de l’onglet **Corbeille** et s’affiche sous l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="e662a-416">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="e662a-417">**Remarques**  La restauration d’un objet de stratégie de groupe dans l’archive ne le redéploie pas automatiquement dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="e662a-417">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="e662a-418">Pour renvoyer l’objet de stratégie de groupe à l’environnement de production, déployez l’objet GPO comme à l' [étape 3: passer en revue et déployer un objet de stratégie de groupe](#bkmk-manage3).</span><span class="sxs-lookup"><span data-stu-id="e662a-418">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="e662a-419">Après la modification et le déploiement d’un objet de stratégie de groupe, il est possible que les modifications récentes apportées à l’objet GPO causent un problème.</span><span class="sxs-lookup"><span data-stu-id="e662a-419">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="e662a-420">Dans le cadre de cette étape, vous faites Office d’approbateur pour restaurer une version précédente de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-420">In this step, you act as an Approver to roll back to a previous version of the GPO.</span></span> <span data-ttu-id="e662a-421">Vous pouvez revenir à une version quelconque de l’historique de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e662a-421">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="e662a-422">Vous pouvez utiliser des commentaires et des étiquettes pour identifier les versions connues et en cas de modifications spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e662a-422">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="e662a-423">Pour restaurer une version précédente d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e662a-423">To roll back to a previous version of a GPO</span></span>**

1.  <span data-ttu-id="e662a-424">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="e662a-424">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="e662a-425">Double-cliquez sur **MyGPO** pour afficher son historique.</span><span class="sxs-lookup"><span data-stu-id="e662a-425">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="e662a-426">Cliquez avec le bouton droit sur la version que vous voulez déployer, cliquez sur **déployer**, puis sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="e662a-426">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="e662a-427">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-427">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="e662a-428">Dans la fenêtre **historique** , cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="e662a-428">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="e662a-429">**Remarques**  Pour vérifier que la version qui a été redéployée est la version prévue, examinez un rapport de différences pour les deux versions.</span><span class="sxs-lookup"><span data-stu-id="e662a-429">**Note** To verify that the version that has been redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="e662a-430">Dans la fenêtre **historique** de l’objet de stratégie de groupe, sélectionnez les deux versions, cliquez dessus avec le bouton droit, pointez sur **différence**, puis cliquez sur rapport **HTML** ou sur **rapport XML**.</span><span class="sxs-lookup"><span data-stu-id="e662a-430">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





