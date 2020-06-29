---
title: Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft3.0
description: Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft3.0
author: dansimp
ms.assetid: d067f465-d7c8-4f6d-b311-66b9b06874f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b4efa5075027e99a3e50a344aafcdf6f6f69a147
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807462"
---
# <span data-ttu-id="d2875-103">Guide pas à pas de la Gestion avancée des stratégies de groupe Microsoft3.0</span><span class="sxs-lookup"><span data-stu-id="d2875-103">Step-by-Step Guide for Microsoft Advanced Group Policy Management 3.0</span></span>


<span data-ttu-id="d2875-104">Ce guide pas à pas décrit les techniques avancées de gestion des stratégies de groupe à l’aide de la console de gestion des stratégies de groupe (GPMC) et de la gestion de la stratégie de groupe Microsoft avancée (AGPM).</span><span class="sxs-lookup"><span data-stu-id="d2875-104">This step-by-step guide demonstrates advanced techniques for Group Policy management using the Group Policy Management Console (GPMC) and Microsoft Advanced Group Policy Management (AGPM).</span></span> <span data-ttu-id="d2875-105">AGPM augmente les capacités de la console de gestion des stratégies de GPMC et fournit les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="d2875-105">AGPM increases the capabilities of the GPMC, providing:</span></span>

-   <span data-ttu-id="d2875-106">Rôles standard pour la délégation d’autorisations pour gérer des objets de stratégie de groupe pour plusieurs administrateurs de stratégie de groupe, ainsi que la possibilité de déléguer l’accès à des objets de stratégie de groupe dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="d2875-106">Standard roles for delegating permissions to manage Group Policy objects (GPOs) to multiple Group Policy administrators, as well as the ability to delegate access to GPOs in the production environment.</span></span>

-   <span data-ttu-id="d2875-107">Archive permettant aux administrateurs de stratégie de groupe de créer et de modifier des objets de stratégie de groupe hors ligne avant de les déployer dans un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="d2875-107">An archive to enable Group Policy administrators to create and modify GPOs offline before deploying them to a production environment.</span></span>

-   <span data-ttu-id="d2875-108">La possibilité de revenir à une version précédente d’un objet de stratégie de groupe dans l’archive et de limiter le nombre de versions stockées dans l’archive;</span><span class="sxs-lookup"><span data-stu-id="d2875-108">The ability to roll back to any previous version of a GPO in the archive and to limit the number of versions stored in the archive.</span></span>

-   <span data-ttu-id="d2875-109">La fonctionnalité d’archivage/extraction pour les objets de stratégie de groupe permet de s’assurer que les administrateurs de stratégie de groupe n’écrasent pas par inadvertance les tâches d’un autre groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-109">Check-in/check-out capability for GPOs to ensure that Group Policy administrators do not inadvertently overwrite each other's work.</span></span>

## <span data-ttu-id="d2875-110">Vue d’ensemble du scénario AGPM</span><span class="sxs-lookup"><span data-stu-id="d2875-110">AGPM scenario overview</span></span>


<span data-ttu-id="d2875-111">Pour ce scénario, vous allez utiliser un compte d’utilisateur distinct pour chaque rôle dans AGPM et montrer comment la stratégie de groupe peut être gérée dans un environnement doté de plusieurs administrateurs de stratégie de groupe disposant de différents niveaux d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="d2875-111">For this scenario, you will use a separate user account for each role in AGPM to demonstrate how Group Policy can be managed in an environment with multiple Group Policy administrators who have different levels of permissions.</span></span> <span data-ttu-id="d2875-112">Plus précisément, vous devez effectuer les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="d2875-112">Specifically, you will perform the following tasks:</span></span>

-   <span data-ttu-id="d2875-113">À l’aide d’un compte membre du groupe administrateurs de domaine, installez le serveur AGPM et attribuez le rôle d’administrateur AGPM à un compte ou à un groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-113">Using an account that is a member of the Domain Admins group, install AGPM Server and assign the AGPM Administrator role to an account or group.</span></span>

-   <span data-ttu-id="d2875-114">À l’aide des comptes auxquels vous allez attribuer des rôles AGPM, installez le client AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-114">Using accounts to which you will assign AGPM roles, install AGPM Client.</span></span>

-   <span data-ttu-id="d2875-115">À l’aide d’un compte ayant le rôle d’administrateur AGPM, configurez l’accès AGPM et déléguez aux objets de stratégie de groupe en attribuant des rôles à d’autres comptes.</span><span class="sxs-lookup"><span data-stu-id="d2875-115">Using an account with the AGPM Administrator role, configure AGPM and delegate access to GPOs by assigning roles to other accounts.</span></span>

-   <span data-ttu-id="d2875-116">En utilisant un compte doté du rôle d’éditeur, demandez la création d’un objet de stratégie de groupe, que vous approuvez ensuite en utilisant un compte doté du rôle Approbateur.</span><span class="sxs-lookup"><span data-stu-id="d2875-116">Using an account with the Editor role, request the creation of a GPO, which you then approve using an account with the Approver role.</span></span> <span data-ttu-id="d2875-117">Avec le compte de l’éditeur, recherchez l’objet de stratégie de groupe à partir de l’archive, modifiez-le, puis consultez l’objet de stratégie de groupe dans l’archive et demandez le déploiement.</span><span class="sxs-lookup"><span data-stu-id="d2875-117">With the Editor account, check the GPO out of the archive, edit the GPO, check the GPO into the archive, and request deployment.</span></span>

-   <span data-ttu-id="d2875-118">En utilisant un compte doté du rôle Approbateur, passez en revue l’objet de stratégie de groupe et déployez-le dans votre environnement de production.</span><span class="sxs-lookup"><span data-stu-id="d2875-118">Using an account with the Approver role, review the GPO and deploy it to your production environment.</span></span>

-   <span data-ttu-id="d2875-119">À l’aide d’un compte avec le rôle d’éditeur, créez un modèle d’objet de stratégie de groupe et utilisez-le comme point de départ pour créer un nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-119">Using an account with the Editor role, create a GPO template and use it as a starting point to create a new GPO.</span></span>

-   <span data-ttu-id="d2875-120">En utilisant un compte doté du rôle Approbateur, supprimez et restaurez un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-120">Using an account with the Approver role, delete and restore a GPO.</span></span>

![processus de développement d’objets de stratégie de groupe](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <span data-ttu-id="d2875-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2875-122">Requirements</span></span>


<span data-ttu-id="d2875-123">Les ordinateurs sur lesquels vous souhaitez installer AGPM doivent respecter les exigences suivantes et vous devez créer des comptes à utiliser dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="d2875-123">Computers on which you want to install AGPM must meet the following requirements, and you must create accounts for use in this scenario.</span></span>

<span data-ttu-id="d2875-124">**Remarques**  Si AGPM 2,5 est installé et que vous effectuez une mise à niveau de Windows Server® 2003 vers Windows Server 2008 ou® Vista sans Service Pack installé sur Vista avec Service Pack1, vous devez mettre à niveau le système d’exploitation avant de procéder à la mise à niveau vers AGPM 3.0.</span><span class="sxs-lookup"><span data-stu-id="d2875-124">**Note** If you have AGPM 2.5 installed and are upgrading from Windows Server®2003 to Windows Server2008 or WindowsVista® with no service packs installed to WindowsVista with Service Pack1, you must upgrade the operating system before you can upgrade to AGPM3.0.</span></span>

 

### <span data-ttu-id="d2875-125">Configuration requise pour le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="d2875-125">AGPM Server requirements</span></span>

<span data-ttu-id="d2875-126">Pour AGPM Server 3.0, vous avez besoin de Windows Server 2008 ou Vista avec Service Pack1 et de la console GPMC des outils d’administration de serveur distant installés.</span><span class="sxs-lookup"><span data-stu-id="d2875-126">AGPM Server3.0 requires Windows Server2008 or WindowsVista with Service Pack1 and the GPMC from Remote Server Administration Tools (RSAT) installed.</span></span> <span data-ttu-id="d2875-127">Les versions 32 bits et 64 bits sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d2875-127">Both 32-bit and 64-bit versions are supported.</span></span>

<span data-ttu-id="d2875-128">Avant d’installer le serveur AGPM, vous devez être membre du groupe administrateurs de domaine et les fonctionnalités Windows suivantes doivent être présentes sauf indication contraire:</span><span class="sxs-lookup"><span data-stu-id="d2875-128">Before you install AGPM Server, you must be a member of the Domain Admins group and the following Windows features must be present unless otherwise noted:</span></span>

-   <span data-ttu-id="d2875-129">GESTION</span><span class="sxs-lookup"><span data-stu-id="d2875-129">GPMC</span></span>

    -   <span data-ttu-id="d2875-130">Windows Server 2008: la console de gestion des stratégies de GPMC est automatiquement installée par AGPM en cas de non-présentation.</span><span class="sxs-lookup"><span data-stu-id="d2875-130">Windows Server 2008: The GPMC is automatically installed by AGPM if not present.</span></span>

    -   <span data-ttu-id="d2875-131">Windows Vista: vous devez installer la console de gestion des stratégies de votre console à partir de RSAT avant d’installer AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-131">Windows Vista: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="d2875-132">Pour plus d’informations, voir <https://go.microsoft.com/fwlink/?LinkID=116179>.</span><span class="sxs-lookup"><span data-stu-id="d2875-132">For more information, see <https://go.microsoft.com/fwlink/?LinkID=116179>.</span></span>

-   <span data-ttu-id="d2875-133">.NET Framework 3.5</span><span class="sxs-lookup"><span data-stu-id="d2875-133">.NET Framework 3.5</span></span>

<span data-ttu-id="d2875-134">Les fonctionnalités Windows suivantes sont requises par le serveur AGPM et sont installées automatiquement en cas de non-présentation:</span><span class="sxs-lookup"><span data-stu-id="d2875-134">The following Windows features are required by AGPM Server and will be automatically installed if not present:</span></span>

-   <span data-ttu-id="d2875-135">Activation WCF; Activation non HTTP</span><span class="sxs-lookup"><span data-stu-id="d2875-135">WCF Activation; Non-HTTP Activation</span></span>

-   <span data-ttu-id="d2875-136">Service d'activation des processus Windows</span><span class="sxs-lookup"><span data-stu-id="d2875-136">Windows Process Activation Service</span></span>

    -   <span data-ttu-id="d2875-137">Modèle de processus</span><span class="sxs-lookup"><span data-stu-id="d2875-137">Process Model</span></span>

    -   <span data-ttu-id="d2875-138">Environnement .NET</span><span class="sxs-lookup"><span data-stu-id="d2875-138">.NET Environment</span></span>

    -   <span data-ttu-id="d2875-139">API de configuration</span><span class="sxs-lookup"><span data-stu-id="d2875-139">Configuration APIs</span></span>

### <span data-ttu-id="d2875-140">Configuration requise pour le client AGPM</span><span class="sxs-lookup"><span data-stu-id="d2875-140">AGPM Client requirements</span></span>

<span data-ttu-id="d2875-141">Pour le client AGPM, il est nécessaire que Windows Server 2008 ou Vista avec Service Pack 1 et la console GPMC des outils d’administration de serveur distant soient installés.</span><span class="sxs-lookup"><span data-stu-id="d2875-141">AGPM Client3.0 requires Windows Server2008 or WindowsVista with Service Pack 1 and the GPMC from Remote Server Administration Tools (RSAT) installed.</span></span> <span data-ttu-id="d2875-142">Les versions 32 bits et 64 bits sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d2875-142">Both 32-bit and 64-bit versions are supported.</span></span> <span data-ttu-id="d2875-143">Le client AGPM peut être installé sur un ordinateur exécutant AGPM Server.</span><span class="sxs-lookup"><span data-stu-id="d2875-143">AGPM Client can be installed on a computer running AGPM Server.</span></span>

<span data-ttu-id="d2875-144">Les fonctionnalités Windows suivantes sont requises par le client AGPM et sont installées automatiquement en cas de non-présentation sauf indication contraire:</span><span class="sxs-lookup"><span data-stu-id="d2875-144">The following Windows features are required by AGPM Client and will be automatically installed if not present unless otherwise noted:</span></span>

-   <span data-ttu-id="d2875-145">GESTION</span><span class="sxs-lookup"><span data-stu-id="d2875-145">GPMC</span></span>

    -   <span data-ttu-id="d2875-146">Windows Server 2008: la console de gestion des stratégies de GPMC est automatiquement installée par AGPM en cas de non-présentation.</span><span class="sxs-lookup"><span data-stu-id="d2875-146">Windows Server 2008: The GPMC is automatically installed by AGPM if not present.</span></span>

    -   <span data-ttu-id="d2875-147">Windows Vista: vous devez installer la console de gestion des stratégies de votre console à partir de RSAT avant d’installer AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-147">Windows Vista: You must install the GPMC from RSAT before you install AGPM.</span></span> <span data-ttu-id="d2875-148">Pour plus d’informations, voir <https://go.microsoft.com/fwlink/?LinkID=116179>.</span><span class="sxs-lookup"><span data-stu-id="d2875-148">For more information, see <https://go.microsoft.com/fwlink/?LinkID=116179>.</span></span>

-   <span data-ttu-id="d2875-149">.NET Framework 3,0</span><span class="sxs-lookup"><span data-stu-id="d2875-149">.NET Framework 3.0</span></span>

### <span data-ttu-id="d2875-150">Exigences de scénarios</span><span class="sxs-lookup"><span data-stu-id="d2875-150">Scenario requirements</span></span>

<span data-ttu-id="d2875-151">Avant de commencer ce scénario, vous devez créer quatre comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d2875-151">Before you begin this scenario, create four user accounts.</span></span> <span data-ttu-id="d2875-152">Pendant le scénario, vous devez attribuer l’un des rôles AGPM suivants à chacun de ces comptes: Administrateur AGPM (contrôle total), approbateur, éditeur et relecteur.</span><span class="sxs-lookup"><span data-stu-id="d2875-152">During the scenario, you will assign one of the following AGPM roles to each of these accounts: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="d2875-153">Ces comptes doivent être en mesure d’envoyer et de recevoir des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="d2875-153">These accounts must be able to send and receive e-mail messages.</span></span> <span data-ttu-id="d2875-154">Attribution d’autorisations d’accès aux **objets liés** aux comptes avec l’administrateur d’AGPM, l’approbateur et (facultatif) des rôles d’éditeur.</span><span class="sxs-lookup"><span data-stu-id="d2875-154">Assign **Link GPOs** permission to the accounts with the AGPM Administrator, Approver, and (optionally) Editor roles.</span></span>

<span data-ttu-id="d2875-155">**Remarques** 
 L’autorisation **lier les objets de stratégie de groupe** est affectée par défaut aux membres des administrateurs de domaine et des administrateurs d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="d2875-155">**Note**
**Link GPOs** permission is assigned to members of Domain Administrators and Enterprise Administrators by default.</span></span> <span data-ttu-id="d2875-156">Pour affecter **des** autorisations d’accès de l’utilisateur à des groupes ou des utilisateurs supplémentaires (par exemple, des comptes ayant le rôle d’administrateur ou d’approbation AGPM), cliquez sur le nœud du domaine, puis cliquez sur l’onglet **délégation** , sélectionnez **lier les objets de stratégie de groupe**, cliquez sur **Ajouter**, et sélectionnez des utilisateurs ou des groupes auxquels vous voulez accorder l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="d2875-156">To assign **Link GPOs** permission to additional users or groups (such as accounts with the roles of AGPM Administrator or Approver), click the node for the domain and then click the **Delegation** tab, select **Link GPOs**, click **Add**, and select users or groups to which to assign the permission.</span></span>

 

## <span data-ttu-id="d2875-157">Procédures d’installation et de configuration d’AGPM</span><span class="sxs-lookup"><span data-stu-id="d2875-157">Steps for installing and configuring AGPM</span></span>


<span data-ttu-id="d2875-158">Pour installer et configurer AGPM, vous devez procéder comme suit.</span><span class="sxs-lookup"><span data-stu-id="d2875-158">You must complete the following steps to install and configure AGPM.</span></span>

[<span data-ttu-id="d2875-159">Étape 1: installer le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="d2875-159">Step 1: Install AGPM Server</span></span>](#bkmk-config1)

[<span data-ttu-id="d2875-160">Étape 2: installer le client AGPM</span><span class="sxs-lookup"><span data-stu-id="d2875-160">Step 2: Install AGPM Client</span></span>](#bkmk-config2)

[<span data-ttu-id="d2875-161">Étape 3: configurer une connexion de serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="d2875-161">Step 3: Configure an AGPM Server connection</span></span>](#bkmk-config3)

[<span data-ttu-id="d2875-162">Étape 4: configurer les notifications par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="d2875-162">Step 4: Configure e-mail notification</span></span>](#bkmk-config4)

[<span data-ttu-id="d2875-163">Étape 5: accès délégué</span><span class="sxs-lookup"><span data-stu-id="d2875-163">Step 5: Delegate access</span></span>](#bkmk-config5)

### <a href="" id="bkmk-config1"></a><span data-ttu-id="d2875-164">Étape 1: installer le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="d2875-164">Step 1: Install AGPM Server</span></span>

<span data-ttu-id="d2875-165">Dans cette étape, vous installez le serveur AGPM sur le serveur membre ou le contrôleur de domaine qui exécute le service AGPM et vous configurez l’archive.</span><span class="sxs-lookup"><span data-stu-id="d2875-165">In this step, you install AGPM Server on the member server or domain controller that will run the AGPM Service, and you configure the archive.</span></span> <span data-ttu-id="d2875-166">Toutes les opérations AGPM sont gérées par le biais de ce service Windows et sont exécutées avec les informations d’identification du service.</span><span class="sxs-lookup"><span data-stu-id="d2875-166">All AGPM operations are managed through this Windows service and are executed with the service's credentials.</span></span> <span data-ttu-id="d2875-167">L’archive gérée par un serveur AGPM peut être hébergée sur ce serveur ou sur un autre serveur dans la même forêt.</span><span class="sxs-lookup"><span data-stu-id="d2875-167">The archive managed by an AGPM Server can be hosted on that server or on another server in the same forest.</span></span>

**<span data-ttu-id="d2875-168">Pour installer le serveur AGPM sur l’ordinateur qui hébergera le service AGPM</span><span class="sxs-lookup"><span data-stu-id="d2875-168">To install AGPM Server on the computer that will host the AGPM Service</span></span>**

1.  <span data-ttu-id="d2875-169">Ouvrez une session avec un compte membre du groupe administrateurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="d2875-169">Log on with an account that is a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="d2875-170">Démarrez le CD-ROM Microsoft Desktop Optimization Pack et suivez les instructions qui s’affichent à l’écran pour sélectionner **Advanced Group Management Policy-Server**.</span><span class="sxs-lookup"><span data-stu-id="d2875-170">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Server**.</span></span>

3.  <span data-ttu-id="d2875-171">Dans la boîte de dialogue **Bienvenue** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d2875-171">In the **Welcome** dialog box, click **Next**.</span></span>

4.  <span data-ttu-id="d2875-172">Dans la boîte de dialogue **termes du contrat de licence logiciel Microsoft** , acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d2875-172">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

5.  <span data-ttu-id="d2875-173">Dans la boîte de dialogue Path de l' **application** , sélectionnez un emplacement pour installer le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-173">In the **Application Path** dialog box, select a location in which to install AGPM Server.</span></span> <span data-ttu-id="d2875-174">L’ordinateur sur lequel le serveur AGPM est installé doit héberger le service AGPM et gérer l’archive.</span><span class="sxs-lookup"><span data-stu-id="d2875-174">The computer on which AGPM Server is installed will host the AGPM Service and manage the archive.</span></span> <span data-ttu-id="d2875-175">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d2875-175">Click **Next**.</span></span>

6.  <span data-ttu-id="d2875-176">Dans la boîte de dialogue **path Archive** , sélectionnez un emplacement pour l’archivage relatif au serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-176">In the **Archive Path** dialog box, select a location for the archive relative to the AGPM Server.</span></span> <span data-ttu-id="d2875-177">Le chemin d’accès d’archive peut pointer vers un dossier sur le serveur AGPM ou un autre emplacement, mais vous devez sélectionner un emplacement dont l’espace disponible est suffisant pour stocker tous les objets de stratégie de groupe et les données d’historique gérés par ce serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-177">The archive path can point to a folder on the AGPM Server or elsewhere, but you should select a location with sufficient space to store all GPOs and history data managed by this AGPM Server.</span></span> <span data-ttu-id="d2875-178">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d2875-178">Click **Next**.</span></span>

7.  <span data-ttu-id="d2875-179">Dans la boîte de dialogue **compte de service AGPM** , sélectionnez un compte de service sous lequel le service AGPM sera exécuté, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d2875-179">In the **AGPM Service Account** dialog box, select a service account under which the AGPM Service will run and then click **Next**.</span></span>

8.  <span data-ttu-id="d2875-180">Dans la boîte de dialogue **Archiver le propriétaire** , sélectionnez le compte ou le groupe auquel attribuer le rôle d’administrateur AGPM (contrôle total).</span><span class="sxs-lookup"><span data-stu-id="d2875-180">In the **Archive Owner** dialog box, select an account or group to which to initially assign the AGPM Administrator (Full Control) role.</span></span> <span data-ttu-id="d2875-181">Cet administrateur AGPM peut attribuer des rôles et autorisations d’AGPM aux autres administrateurs de stratégie de groupe (y compris le rôle d’administrateur AGPM).</span><span class="sxs-lookup"><span data-stu-id="d2875-181">This AGPM Administrator can assign AGPM roles and permissions to other Group Policy administrators (including the role of AGPM Administrator).</span></span> <span data-ttu-id="d2875-182">Pour ce scénario, sélectionnez le compte que vous voulez faire dans le rôle administrateur d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-182">For this scenario, select the account to serve in the AGPM Administrator role.</span></span> <span data-ttu-id="d2875-183">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d2875-183">Click **Next**.</span></span>

9.  <span data-ttu-id="d2875-184">Dans la boîte de dialogue **configuration du port** , tapez un port sur lequel le service AGPM doit écouter.</span><span class="sxs-lookup"><span data-stu-id="d2875-184">In the **Port Configuration** dialog box, type a port on which the AGPM Service should listen.</span></span> <span data-ttu-id="d2875-185">Ne désactivez pas la case à cocher **Ajouter une exception de port à un pare-feu** sauf si vous configurez manuellement les exceptions de port ou utilisez des règles pour configurer les exceptions de port</span><span class="sxs-lookup"><span data-stu-id="d2875-185">Do not clear the **Add port exception to firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="d2875-186">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d2875-186">Click **Next**.</span></span>

10. <span data-ttu-id="d2875-187">Dans la boîte de dialogue **langues** , sélectionnez une ou plusieurs langues d’affichage à installer pour le serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-187">In the **Languages** dialog box, select one or more display languages to install for AGPM Server.</span></span>

11. <span data-ttu-id="d2875-188">Cliquez sur **installer**, puis cliquez sur **Terminer** pour quitter l’Assistant installation.</span><span class="sxs-lookup"><span data-stu-id="d2875-188">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

    <span data-ttu-id="d2875-189">**Attention**  Ne modifiez pas les paramètres du service AGPM via les outils et **services** **d’administration** du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d2875-189">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="d2875-190">Cela peut empêcher le démarrage du service AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-190">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="d2875-191">Pour plus d’informations sur la modification des paramètres du service, voir aide pour la gestion avancée des stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-191">For information on how to modify settings for the service, see Help for Advanced Group Policy Management.</span></span>

     

### <a href="" id="bkmk-config2"></a><span data-ttu-id="d2875-192">Étape 2: installer le client AGPM</span><span class="sxs-lookup"><span data-stu-id="d2875-192">Step 2: Install AGPM Client</span></span>

<span data-ttu-id="d2875-193">Chaque administrateur de stratégie de groupe (qui crée, modifie, déploie, révise ou supprime des objets de stratégie de groupe) doit disposer d’un client AGPM sur les ordinateurs qu’il utilise pour gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-193">Each Group Policy administrator—anyone who creates, edits, deploys, reviews, or deletes GPOs—must have AGPM Client installed on computers that they use to manage GPOs.</span></span> <span data-ttu-id="d2875-194">Pour ce scénario, vous installez le client AGPM sur au moins un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d2875-194">For this scenario, you install AGPM Client on at least one computer.</span></span> <span data-ttu-id="d2875-195">Vous n’avez pas besoin d’installer le client AGPM sur les ordinateurs des utilisateurs finaux qui n’effectuent pas d’administration de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-195">You do not need to install AGPM Client on the computers of end users who do not perform Group Policy administration.</span></span>

**<span data-ttu-id="d2875-196">Pour installer le client AGPM sur l’ordinateur d’un administrateur de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-196">To install AGPM Client on the computer of a Group Policy administrator</span></span>**

1.  <span data-ttu-id="d2875-197">Démarrez le CD-ROM Microsoft Desktop Optimization Pack et suivez les instructions à l’écran pour sélectionner **Advanced Group Management Policy-client**.</span><span class="sxs-lookup"><span data-stu-id="d2875-197">Start the Microsoft Desktop Optimization Pack CD and follow the instructions on screen to select **Advanced Group Policy Management - Client**.</span></span>

2.  <span data-ttu-id="d2875-198">Dans la boîte de dialogue **Bienvenue** , cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d2875-198">In the **Welcome** dialog box, click **Next**.</span></span>

3.  <span data-ttu-id="d2875-199">Dans la boîte de dialogue **termes du contrat de licence logiciel Microsoft** , acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d2875-199">In the **Microsoft Software License Terms** dialog box, accept the terms and click **Next**.</span></span>

4.  <span data-ttu-id="d2875-200">Dans la boîte de dialogue Path de l' **application** , sélectionnez un emplacement pour installer le client AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-200">In the **Application Path** dialog box, select a location in which to install AGPM Client.</span></span> <span data-ttu-id="d2875-201">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d2875-201">Click **Next**.</span></span>

5.  <span data-ttu-id="d2875-202">Dans la boîte de dialogue **serveur AGPM** , tapez le nom complet de l’ordinateur pour le serveur AGPM et le port auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="d2875-202">In the **AGPM Server** dialog box, type the fully-qualified computer name for the AGPM Server and the port to which to connect.</span></span> <span data-ttu-id="d2875-203">Le port par défaut du service AGPM est 4600.</span><span class="sxs-lookup"><span data-stu-id="d2875-203">The default port for the AGPM Service is 4600.</span></span> <span data-ttu-id="d2875-204">Ne désactivez pas la case à cocher **autoriser Microsoft Management Console via le pare-feu** sauf si vous configurez manuellement les exceptions de port ou utilisez des règles pour configurer les exceptions de port.</span><span class="sxs-lookup"><span data-stu-id="d2875-204">Do not clear the **Allow Microsoft Management Console through the firewall** check box unless you manually configure port exceptions or use rules to configure port exceptions.</span></span> <span data-ttu-id="d2875-205">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d2875-205">Click **Next**.</span></span>

6.  <span data-ttu-id="d2875-206">Dans la boîte de dialogue **langues** , sélectionnez une ou plusieurs langues d’affichage à installer pour le client AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-206">In the **Languages** dialog box, select one or more display languages to install for AGPM Client.</span></span>

7.  <span data-ttu-id="d2875-207">Cliquez sur **installer**, puis cliquez sur **Terminer** pour quitter l’Assistant installation.</span><span class="sxs-lookup"><span data-stu-id="d2875-207">Click **Install**, and then click **Finish** to exit the Setup Wizard.</span></span>

### <a href="" id="bkmk-config3"></a><span data-ttu-id="d2875-208">Étape 3: configurer une connexion de serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="d2875-208">Step 3: Configure an AGPM Server connection</span></span>

<span data-ttu-id="d2875-209">AGPM stocke toutes les versions de chaque objet de stratégie de groupe contrôlé (GPO), c’est-à-dire un objet de stratégie de groupe pour lequel AGPM fournit le contrôle des modifications, dans une archive centrale, de sorte que les administrateurs de stratégie de groupe puissent afficher et modifier les objets de stratégie de groupe hors connexion sans avoir d’impact sur la version déployée de chaque GPO.</span><span class="sxs-lookup"><span data-stu-id="d2875-209">AGPM stores all versions of each controlled Group Policy object (GPO)—a GPO for which AGPM provides change control—in a central archive, so Group Policy administrators can view and modify GPOs offline without immediately impacting the deployed version of each GPO.</span></span>

<span data-ttu-id="d2875-210">Dans cette étape, vous configurez une connexion de serveur AGPM et assurez-vous que tous les administrateurs de stratégie de groupe se connectent au même serveur AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-210">In this step, you configure an AGPM Server connection and ensure that all Group Policy administrators connect to the same AGPM Server.</span></span> <span data-ttu-id="d2875-211">(Pour plus d’informations sur la configuration de plusieurs serveurs AGPM, voir aide pour la gestion avancée des stratégies de groupe.)</span><span class="sxs-lookup"><span data-stu-id="d2875-211">(For information about configuring multiple AGPM Servers, see Help for Advanced Group Policy Management.)</span></span>

**<span data-ttu-id="d2875-212">Pour configurer une connexion de serveur AGPM pour tous les administrateurs de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-212">To configure an AGPM Server connection for all Group Policy administrators</span></span>**

1.  <span data-ttu-id="d2875-213">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous à l’aide du compte d’utilisateur que vous avez sélectionné comme propriétaire d’archive.</span><span class="sxs-lookup"><span data-stu-id="d2875-213">On a computer on which you have installed AGPM Client, log on with the user account that you selected as the Archive Owner.</span></span> <span data-ttu-id="d2875-214">Cet utilisateur a le rôle d’administrateur AGPM (contrôle total).</span><span class="sxs-lookup"><span data-stu-id="d2875-214">This user has the role of AGPM Administrator (Full Control).</span></span>

2.  <span data-ttu-id="d2875-215">Cliquez sur **Démarrer**, pointez sur **Outils d’administration**, puis cliquez sur gestion de la **stratégie de groupe** pour ouvrir la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="d2875-215">Click **Start**, point to **Administrative Tools**, and click **Group Policy Management** to open the GPMC.</span></span>

3.  <span data-ttu-id="d2875-216">Modification d’un objet de stratégie de groupe qui est appliqué à tous les administrateurs de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-216">Edit a GPO that is applied to all Group Policy administrators.</span></span>

4.  <span data-ttu-id="d2875-217">Dans la fenêtre de l' **éditeur de gestion des stratégies de groupe** , double-cliquez sur **Configuration utilisateur**, **stratégies**, **modèles d’administration**, **composants Windows**et **AGPM**.</span><span class="sxs-lookup"><span data-stu-id="d2875-217">In the **Group Policy Management Editor** window, double-click **User Configuration**, **Policies**, **Administrative Templates**, **Windows Components**, and **AGPM**.</span></span>

5.  <span data-ttu-id="d2875-218">Dans le volet Détails, double-cliquez sur **AGPM: spécifiez le serveur AGPM par défaut (tous les domaines)**.</span><span class="sxs-lookup"><span data-stu-id="d2875-218">In the details pane, double-click **AGPM: Specify default AGPM Server (all domains)**.</span></span>

6.  <span data-ttu-id="d2875-219">Dans la fenêtre **Propriétés** , sélectionnez **activé** , puis entrez le nom complet et le port de l’ordinateur (par exemple, **Server.contoso.com:4600**) pour le serveur hébergeant l’archive.</span><span class="sxs-lookup"><span data-stu-id="d2875-219">In the **Properties** window, select **Enabled** and type the fully-qualified computer name and port (for example, **server.contoso.com:4600**) for the server hosting the archive.</span></span> <span data-ttu-id="d2875-220">Par défaut, le service AGPM utilise le port 4600.</span><span class="sxs-lookup"><span data-stu-id="d2875-220">By default, the AGPM Service uses port 4600.</span></span>

7.  <span data-ttu-id="d2875-221">Cliquez sur **OK**, puis fermez la fenêtre **éditeur de gestion des stratégies de groupe** .</span><span class="sxs-lookup"><span data-stu-id="d2875-221">Click **OK**, and then close the **Group Policy Management Editor** window.</span></span> <span data-ttu-id="d2875-222">Lorsque la stratégie de groupe est mise à jour, la connexion au serveur AGPM est configurée pour chaque administrateur de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-222">When Group Policy is updated, the AGPM Server connection is configured for each Group Policy administrator.</span></span>

### <a href="" id="bkmk-config4"></a><span data-ttu-id="d2875-223">Étape 4: configurer les notifications par courrier électronique</span><span class="sxs-lookup"><span data-stu-id="d2875-223">Step 4: Configure e-mail notification</span></span>

<span data-ttu-id="d2875-224">En tant qu’administrateur AGPM (contrôle total), vous désignez les adresses de courrier des approbateurs et des administrateurs AGPM auxquels un message électronique contenant une demande est envoyé lorsqu’un éditeur tente de créer, de déployer ou de supprimer un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-224">As an AGPM Administrator (Full Control), you designate the e-mail addresses of Approvers and AGPM Administrators to whom an e-mail message containing a request is sent when an Editor attempts to create, deploy, or delete a GPO.</span></span> <span data-ttu-id="d2875-225">Vous déterminez également l’alias à partir duquel ces messages sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="d2875-225">You also determine the alias from which these messages are sent.</span></span>

**<span data-ttu-id="d2875-226">Pour configurer les notifications par courrier électronique pour AGPM</span><span class="sxs-lookup"><span data-stu-id="d2875-226">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="d2875-227">Dans le volet Détails, cliquez sur l’onglet **délégation de domaine** .</span><span class="sxs-lookup"><span data-stu-id="d2875-227">In the details pane, click the **Domain Delegation** tab.</span></span>

2.  <span data-ttu-id="d2875-228">Dans le champ **à partir de l’adresse de messagerie** , entrez l’adresse de messagerie d’AGPM à partir de laquelle les notifications doivent être envoyées.</span><span class="sxs-lookup"><span data-stu-id="d2875-228">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

3.  <span data-ttu-id="d2875-229">Dans le champ **adresse de messagerie** , entrez l’adresse de messagerie du compte d’utilisateur auquel vous souhaitez attribuer le rôle d’approbateur.</span><span class="sxs-lookup"><span data-stu-id="d2875-229">In the **To e-mail address** field, type the e-mail address for the user account to which you intend to assign the Approver role.</span></span>

4.  <span data-ttu-id="d2875-230">Dans le champ **serveur SMTP** , tapez un serveur de messagerie SMTP valide.</span><span class="sxs-lookup"><span data-stu-id="d2875-230">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

5.  <span data-ttu-id="d2875-231">Dans les champs **nom d’utilisateur** et **mot de passe** , tapez les informations d’identification d’un utilisateur ayant accès au service SMTP.</span><span class="sxs-lookup"><span data-stu-id="d2875-231">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span> <span data-ttu-id="d2875-232">Cliquez sur **Apply** (Appliquer).</span><span class="sxs-lookup"><span data-stu-id="d2875-232">Click **Apply**.</span></span>

### <a href="" id="bkmk-config5"></a><span data-ttu-id="d2875-233">Étape 5: accès délégué</span><span class="sxs-lookup"><span data-stu-id="d2875-233">Step 5: Delegate access</span></span>

<span data-ttu-id="d2875-234">En tant qu’administrateur AGPM (contrôle total), vous déléguez l’accès au niveau du domaine aux objets de stratégie de groupe, en attribuant des rôles au compte de chaque administrateur de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-234">As an AGPM Administrator (Full Control), you delegate domain-level access to GPOs, assigning roles to the account of each Group Policy administrator.</span></span>

<span data-ttu-id="d2875-235">**Remarques**  Vous pouvez également déléguer l’accès au niveau de l’objet GPO plutôt qu’au niveau du domaine.</span><span class="sxs-lookup"><span data-stu-id="d2875-235">**Note** You can also delegate access at the GPO level rather than the domain level.</span></span> <span data-ttu-id="d2875-236">Pour plus d’informations, consultez aide pour la gestion avancée des stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-236">For details, see Help for Advanced Group Policy Management.</span></span>

 

<span data-ttu-id="d2875-237">**Important**  Nous vous conseillons de limiter l’appartenance au groupe de propriétaires de la stratégie de groupe, afin qu’il ne puisse pas être utilisé pour contourner la gestion d’AGPM d’Access aux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-237">**Important** You should restrict membership in the Group Policy Creator Owners group, so it cannot be used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="d2875-238">(Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)</span><span class="sxs-lookup"><span data-stu-id="d2875-238">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

 

**<span data-ttu-id="d2875-239">Pour déléguer l’accès à tous les objets de stratégie de groupe dans un domaine</span><span class="sxs-lookup"><span data-stu-id="d2875-239">To delegate access to all GPOs throughout a domain</span></span>**

1.  <span data-ttu-id="d2875-240">Dans l’onglet **délégation de domaine** , cliquez sur le bouton **Ajouter** , sélectionnez le compte d’utilisateur de l’administrateur de stratégie de groupe comme approbateur, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2875-240">On the **Domain Delegation** tab, click the **Add** button, select the user account of the Group Policy administrator to serve as Approver, and then click **OK**.</span></span>

2.  <span data-ttu-id="d2875-241">Dans la boîte de dialogue **Ajouter un groupe ou un utilisateur** , sélectionnez le rôle **approbateur** pour attribuer le rôle au compte, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2875-241">In the **Add Group or User** dialog box, select the **Approver** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="d2875-242">(Ce rôle inclut le rôle de réviseur.)</span><span class="sxs-lookup"><span data-stu-id="d2875-242">(This role includes the Reviewer role.)</span></span>

3.  <span data-ttu-id="d2875-243">Cliquez sur le bouton **Ajouter** , sélectionnez le compte d’utilisateur de l’administrateur de stratégie de groupe pour faire office d’éditeur, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2875-243">Click the **Add** button, select the user account of the Group Policy administrator to serve as Editor, and then click **OK**.</span></span>

4.  <span data-ttu-id="d2875-244">Dans la boîte de dialogue **Ajouter un groupe ou un utilisateur** , sélectionnez le rôle d' **éditeur** pour attribuer le rôle au compte, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2875-244">In the **Add Group or User** dialog box, select the **Editor** role to assign that role to the account, and then click **OK**.</span></span> <span data-ttu-id="d2875-245">(Ce rôle inclut le rôle de réviseur.)</span><span class="sxs-lookup"><span data-stu-id="d2875-245">(This role includes the Reviewer role.)</span></span>

5.  <span data-ttu-id="d2875-246">Cliquez sur le bouton **Ajouter** , sélectionnez le compte d’utilisateur de l’administrateur de stratégie de groupe pour qu’il serve de relecteur, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2875-246">Click the **Add** button, select the user account of the Group Policy administrator to serve as Reviewer, and then click **OK**.</span></span>

6.  <span data-ttu-id="d2875-247">Dans la boîte de dialogue **Ajouter un groupe ou un utilisateur** , sélectionnez le rôle de **réviseur** pour affecter uniquement ce rôle au compte.</span><span class="sxs-lookup"><span data-stu-id="d2875-247">In the **Add Group or User** dialog box, select the **Reviewer** role to assign only that role to the account.</span></span>

## <span data-ttu-id="d2875-248">Procédure de gestion des objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-248">Steps for managing GPOs</span></span>


<span data-ttu-id="d2875-249">Vous devez effectuer les étapes suivantes pour créer, modifier, réviser et déployer des objets de stratégie de groupe à l’aide d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-249">You must complete the following steps to create, edit, review, and deploy GPOs using AGPM.</span></span> <span data-ttu-id="d2875-250">Par ailleurs, vous allez créer un modèle, supprimer un objet de stratégie de groupe, puis restaurer un objet GPO supprimé.</span><span class="sxs-lookup"><span data-stu-id="d2875-250">Additionally, you will create a template, delete a GPO, and restore a deleted GPO.</span></span>

[<span data-ttu-id="d2875-251">Étape 1: créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-251">Step 1: Create a GPO</span></span>](#bkmk-manage1)

[<span data-ttu-id="d2875-252">Étape 2: modifier un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-252">Step 2: Edit a GPO</span></span>](#bkmk-manage2)

[<span data-ttu-id="d2875-253">Étape 3: vérifier et déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-253">Step 3: Review and deploy a GPO</span></span>](#bkmk-manage3)

[<span data-ttu-id="d2875-254">Étape 4: utiliser un modèle pour créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-254">Step 4: Use a template to create a GPO</span></span>](#bkmk-manage4)

[<span data-ttu-id="d2875-255">Étape 5: supprimer et restaurer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-255">Step 5: Delete and restore a GPO</span></span>](#bkmk-manage5)

### <a href="" id="bkmk-manage1"></a><span data-ttu-id="d2875-256">Étape 1: créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-256">Step 1: Create a GPO</span></span>

<span data-ttu-id="d2875-257">Dans un environnement doté de plusieurs administrateurs de stratégie de groupe, les utilisateurs dotés du rôle d’éditeur peuvent demander la création de nouveaux objets de stratégie de groupe, mais une telle demande doit être approuvée par une personne ayant le rôle d’approbateur, car la création d’un nouvel objet GPO a un impact sur l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="d2875-257">In an environment with multiple Group Policy administrators, those with the Editor role have the ability to request the creation of new GPOs, but such a request must be approved by someone with the Approver role because the creation of a new GPO impacts the production environment.</span></span>

<span data-ttu-id="d2875-258">Dans cette étape, vous utiliserez un compte avec le rôle d’éditeur pour demander la création d’un nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-258">In this step, you use an account with the Editor role to request the creation of a new GPO.</span></span> <span data-ttu-id="d2875-259">En utilisant un compte doté du rôle Approbateur, vous approuvez cette demande et terminerez la création d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-259">Using an account with the Approver role, you approve this request and complete the creation of a GPO.</span></span>

**<span data-ttu-id="d2875-260">Pour demander la création d’un nouvel objet de stratégie de groupe géré via AGPM</span><span class="sxs-lookup"><span data-stu-id="d2875-260">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="d2875-261">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’éditeur a été attribué dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-261">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the Editor role in AGPM.</span></span>

2.  <span data-ttu-id="d2875-262">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-262">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="d2875-263">Cliquez avec le bouton droit sur le nœud de **contrôle de modification** , puis cliquez sur **nouvel objet de stratégie de**contrôle.</span><span class="sxs-lookup"><span data-stu-id="d2875-263">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

4.  <span data-ttu-id="d2875-264">Dans la boîte de dialogue **nouvel objet GPO contrôlé** :</span><span class="sxs-lookup"><span data-stu-id="d2875-264">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="d2875-265">Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .</span><span class="sxs-lookup"><span data-stu-id="d2875-265">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="d2875-266">Tapez **MyGPO** comme nom du nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-266">Type **MyGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="d2875-267">Tapez un commentaire pour le nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-267">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="d2875-268">Cliquez sur **créer Live** pour que le nouvel objet GPO soit déployé sur l’environnement de production immédiatement après approbation.</span><span class="sxs-lookup"><span data-stu-id="d2875-268">Click **Create live** so the new GPO will be deployed to the production environment immediately upon approval.</span></span> <span data-ttu-id="d2875-269">Cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-269">Click **Submit**.</span></span>

5.  <span data-ttu-id="d2875-270">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-270">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d2875-271">Le nouvel objet GPO est affiché dans l’onglet **en attente** .</span><span class="sxs-lookup"><span data-stu-id="d2875-271">The new GPO is displayed on the **Pending** tab.</span></span>

**<span data-ttu-id="d2875-272">Pour approuver la demande en attente de création d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-272">To approve the pending request to create a GPO</span></span>**

1.  <span data-ttu-id="d2875-273">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’approbateur dans AGPM s’est attribué.</span><span class="sxs-lookup"><span data-stu-id="d2875-273">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span>

2.  <span data-ttu-id="d2875-274">Ouvrez la boîte de réception de votre compte et notez que vous avez reçu un message électronique de l’alias AGPM avec la demande de l’éditeur pour créer un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-274">Open the e-mail inbox for the account, and note that you have received an e-mail message from the AGPM alias with the Editor's request to create a GPO.</span></span>

3.  <span data-ttu-id="d2875-275">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-275">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4.  <span data-ttu-id="d2875-276">Dans l’onglet **contenu** , cliquez sur l’onglet **en attente** pour afficher les objets de stratégie de groupe en attente.</span><span class="sxs-lookup"><span data-stu-id="d2875-276">On the **Contents** tab, click the **Pending** tab to display the pending GPOs.</span></span>

5.  <span data-ttu-id="d2875-277">Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **approuver**.</span><span class="sxs-lookup"><span data-stu-id="d2875-277">Right-click **MyGPO**, and then click **Approve**.</span></span>

6.  <span data-ttu-id="d2875-278">Cliquez sur **Oui** pour confirmer l’approbation de la création de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-278">Click **Yes** to confirm approval of the creation of the GPO.</span></span> <span data-ttu-id="d2875-279">L’objet de stratégie de groupe est déplacé vers l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="d2875-279">The GPO is moved to the **Controlled** tab.</span></span>

### <a href="" id="bkmk-manage2"></a><span data-ttu-id="d2875-280">Étape 2: modifier un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-280">Step 2: Edit a GPO</span></span>

<span data-ttu-id="d2875-281">Vous pouvez utiliser les objets de stratégie de groupe pour configurer les paramètres de l’ordinateur ou de l’utilisateur et les déployer sur de nombreux ordinateurs ou utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d2875-281">You can use GPOs to configure computer or user settings and deploy them to many computers or users.</span></span> <span data-ttu-id="d2875-282">Dans cette étape, vous utiliserez un compte avec le rôle d’éditeur pour extraire un objet de stratégie de groupe de l’archive, modifier l’objet de stratégie de groupe en mode hors connexion, Rechercher l’objet GPO modifié dans l’archive et demander le déploiement de l’objet de stratégie de groupe dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="d2875-282">In this step, you use an account with the Editor role to check out a GPO from the archive, edit the GPO offline, check the edited GPO into the archive, and request deployment of the GPO to the production environment.</span></span> <span data-ttu-id="d2875-283">Pour ce scénario, vous devez configurer un paramètre dans l’objet de stratégie de groupe pour exiger que le mot de passe comporte au moins huit caractères.</span><span class="sxs-lookup"><span data-stu-id="d2875-283">For this scenario, you configure a setting in the GPO to require that the password be at least eight characters in length.</span></span>

**<span data-ttu-id="d2875-284">Pour extraire l’objet de stratégie de groupe de l’archive en vue de le modifier</span><span class="sxs-lookup"><span data-stu-id="d2875-284">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="d2875-285">Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’éditeur a été attribué dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-285">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="d2875-286">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-286">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="d2875-287">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="d2875-287">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="d2875-288">Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **extraire**.</span><span class="sxs-lookup"><span data-stu-id="d2875-288">Right-click **MyGPO**, and then click **Check Out**.</span></span>

5.  <span data-ttu-id="d2875-289">Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe lors de son extraction, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2875-289">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

6.  <span data-ttu-id="d2875-290">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-290">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d2875-291">Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **extrait**.</span><span class="sxs-lookup"><span data-stu-id="d2875-291">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="d2875-292">Pour modifier l’objet de stratégie de groupe hors connexion et configurer la longueur de mot de passe minimum</span><span class="sxs-lookup"><span data-stu-id="d2875-292">To edit the GPO offline and configure the minimum password length</span></span>**

1.  <span data-ttu-id="d2875-293">Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **modifier** pour ouvrir la fenêtre de l’éditeur de gestion des stratégies de groupe et apporter des modifications à une copie hors connexion de l’objet de stratégie de **groupe** .</span><span class="sxs-lookup"><span data-stu-id="d2875-293">On the **Controlled** tab, right-click **MyGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="d2875-294">Pour ce scénario, configurez la longueur minimale du mot de passe:</span><span class="sxs-lookup"><span data-stu-id="d2875-294">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="d2875-295">Sous **Configuration ordinateur**, double-cliquez sur **stratégies**, **Paramètres Windows**, **paramètres de sécurité**, stratégies de **compte**et **stratégie de mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="d2875-295">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Password Policy**.</span></span>

    2.  <span data-ttu-id="d2875-296">Dans le volet Détails, double-cliquez sur **longueur minimale du mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="d2875-296">In the details pane, double-click **Minimum password length**.</span></span>

    3.  <span data-ttu-id="d2875-297">Dans la fenêtre Propriétés, activez la case à cocher **définir ce paramètre de stratégie** , définissez le nombre de caractères sur **8**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2875-297">In the properties window, select the **Define this policy setting** check box, set the number of characters to **8**, and then click **OK**.</span></span>

2.  <span data-ttu-id="d2875-298">Fermez la fenêtre de l' **éditeur de gestion des stratégies de groupe** .</span><span class="sxs-lookup"><span data-stu-id="d2875-298">Close the **Group Policy Management Editor** window.</span></span>

**<span data-ttu-id="d2875-299">Pour archiver l’objet de stratégie de groupe dans l’archive</span><span class="sxs-lookup"><span data-stu-id="d2875-299">To check the GPO into the archive</span></span>**

1.  <span data-ttu-id="d2875-300">Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyGPO** , puis cliquez sur **Archiver**.</span><span class="sxs-lookup"><span data-stu-id="d2875-300">On the **Controlled** tab, right-click **MyGPO** and then click **Check In**.</span></span>

2.  <span data-ttu-id="d2875-301">Tapez un commentaire, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2875-301">Type a comment, and then click **OK**.</span></span>

3.  <span data-ttu-id="d2875-302">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-302">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d2875-303">Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **Archivé**.</span><span class="sxs-lookup"><span data-stu-id="d2875-303">On the **Controlled** tab, the state of the GPO is identified as **Checked In**.</span></span>

**<span data-ttu-id="d2875-304">Pour demander le déploiement de l’objet de stratégie de groupe dans l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="d2875-304">To request the deployment of the GPO to the production environment</span></span>**

1.  <span data-ttu-id="d2875-305">Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyGPO** , puis cliquez sur **déployer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-305">On the **Controlled** tab, right-click **MyGPO** and then click **Deploy**.</span></span>

2.  <span data-ttu-id="d2875-306">Dans la mesure où ce compte n’est pas un approbateur ou un administrateur AGPM, vous devez fournir une demande de déploiement.</span><span class="sxs-lookup"><span data-stu-id="d2875-306">Because this account is not an Approver or AGPM Administrator, you must submit a request for deployment.</span></span> <span data-ttu-id="d2875-307">Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .</span><span class="sxs-lookup"><span data-stu-id="d2875-307">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="d2875-308">Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe, puis cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="d2875-308">Type a comment to be displayed in the history of the GPO, and then click **Submit**.</span></span>

3.  <span data-ttu-id="d2875-309">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-309">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d2875-310">**MyGPO** s’affiche dans la liste des objets de stratégie de groupe sous l’onglet **en attente** .</span><span class="sxs-lookup"><span data-stu-id="d2875-310">**MyGPO** is displayed on the list of GPOs on the **Pending** tab.</span></span>

### <a href="" id="bkmk-manage3"></a><span data-ttu-id="d2875-311">Étape 3: vérifier et déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-311">Step 3: Review and deploy a GPO</span></span>

<span data-ttu-id="d2875-312">Dans le cadre de cette étape, vous agissez en tant qu’approbateur, vous créez des rapports et vous analysez les paramètres et les modifications apportées aux paramètres dans l’objet de stratégie de groupe pour déterminer s’ils doivent être approuvés.</span><span class="sxs-lookup"><span data-stu-id="d2875-312">In this step, you act as an Approver, creating reports and analyzing the settings and changes to settings in the GPO to determine whether you should approve them.</span></span> <span data-ttu-id="d2875-313">Après avoir évalué l’objet de stratégie de groupe, vous le déployez dans l’environnement de production et le liez à un domaine ou à une unité d’organisation (UO) de sorte qu’il soit appliqué lorsque la stratégie de groupe est actualisée pour les ordinateurs de ce domaine ou UO.</span><span class="sxs-lookup"><span data-stu-id="d2875-313">After evaluating the GPO, you deploy it to the production environment and link it to a domain or an organizational unit (OU) so that it takes effect when Group Policy is refreshed for computers in that domain or OU.</span></span>

**<span data-ttu-id="d2875-314">Pour vérifier les paramètres de l’objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-314">To review settings in the GPO</span></span>**

1. <span data-ttu-id="d2875-315">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’approbateur dans AGPM s’est attribué.</span><span class="sxs-lookup"><span data-stu-id="d2875-315">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver in AGPM.</span></span> <span data-ttu-id="d2875-316">(N’importe quel administrateur de stratégie de groupe avec le rôle de relecteur, qui est inclus dans tous les autres rôles, peut consulter les paramètres d’un objet de stratégie de groupe).</span><span class="sxs-lookup"><span data-stu-id="d2875-316">(Any Group Policy administrator with the Reviewer role, which is included in all of the other roles, can review the settings in a GPO.)</span></span>

2. <span data-ttu-id="d2875-317">Ouvrez la boîte de réception du compte et notez que vous avez reçu un message électronique de l’alias AGPM avec une demande d’éditeur pour le déploiement d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-317">Open the e-mail inbox for the account and note that you have received an e-mail message from the AGPM alias with an Editor's request to deploy a GPO.</span></span>

3. <span data-ttu-id="d2875-318">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-318">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

4. <span data-ttu-id="d2875-319">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **en attente** .</span><span class="sxs-lookup"><span data-stu-id="d2875-319">On the **Contents** tab in the details pane, click the **Pending** tab.</span></span>

5. <span data-ttu-id="d2875-320">Double-cliquez sur **MyGPO** pour afficher son historique.</span><span class="sxs-lookup"><span data-stu-id="d2875-320">Double-click **MyGPO** to display its history.</span></span>

6. <span data-ttu-id="d2875-321">Passez en revue les paramètres dans la version la plus récente de MyGPO:</span><span class="sxs-lookup"><span data-stu-id="d2875-321">Review the settings in the most recent version of MyGPO:</span></span>

   1.  <span data-ttu-id="d2875-322">Dans la fenêtre **historique** , cliquez avec le bouton droit sur la version de l’objet de stratégie de groupe avec le dateur le plus récent, cliquez sur **paramètres**, puis sur **rapport HTML** pour afficher un récapitulatif des paramètres de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-322">In the **History** window, right-click the GPO version with the most recent timestamp, click **Settings**, and then click **HTML Report** to display a summary of the GPO's settings.</span></span>

   2.  <span data-ttu-id="d2875-323">Dans le navigateur Web, cliquez sur **Afficher tout** pour afficher tous les paramètres de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-323">In the Web browser, click **show all** to display all of the settings in the GPO.</span></span> <span data-ttu-id="d2875-324">Fermez le navigateur.</span><span class="sxs-lookup"><span data-stu-id="d2875-324">Close the browser.</span></span>

7. <span data-ttu-id="d2875-325">Comparez la version la plus récente de MyGPO à la première version archivée dans l’archive:</span><span class="sxs-lookup"><span data-stu-id="d2875-325">Compare the most recent version of MyGPO to the first version checked in to the archive:</span></span>

   1. <span data-ttu-id="d2875-326">Dans la fenêtre **historique** , cliquez sur la version de l’objet de stratégie de groupe avec le cachet d’heure le plus récent.</span><span class="sxs-lookup"><span data-stu-id="d2875-326">In the **History** window, click the GPO version with the most recent time stamp.</span></span> <span data-ttu-id="d2875-327">Maintenez la touche CTRL enfoncée et cliquez sur la version la plus ancienne **de l’objet**</span><span class="sxs-lookup"><span data-stu-id="d2875-327">Press CTRL and click the oldest GPO version for which the **Computer Version** is not \*\*\\*\*\*.</span></span>

   2. <span data-ttu-id="d2875-328">Cliquez sur le bouton **différences** .</span><span class="sxs-lookup"><span data-stu-id="d2875-328">Click the **Differences** button.</span></span> <span data-ttu-id="d2875-329">La section **stratégies de compte/stratégie de mot de passe** est mise en évidence en vert et précédée de **\ [+ \]**, ce qui indique que ce paramètre est configuré uniquement dans la dernière version de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-329">The **Account Policies/Password Policy** section is highlighted in green and preceded by **\[+\]**, indicating that this setting is configured only in the latter version of the GPO.</span></span>

   3. <span data-ttu-id="d2875-330">Cliquez sur **stratégies de compte/stratégie de mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="d2875-330">Click **Account Policies/Password Policy**.</span></span> <span data-ttu-id="d2875-331">Le paramètre de **longueur minimum du mot de passe** est également mis en surbrillance en vert et précédé de **\ [+ \]** indiquant qu’il est configuré uniquement dans la dernière version de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-331">The **Minimum password length** setting is also highlighted in green and preceded by **\[+\]**, indicating that it is configured only in the latter version of the GPO.</span></span>

   4. <span data-ttu-id="d2875-332">Fermez le navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="d2875-332">Close the Web browser.</span></span>

**<span data-ttu-id="d2875-333">Pour déployer l’objet de stratégie de groupe dans l’environnement de production</span><span class="sxs-lookup"><span data-stu-id="d2875-333">To deploy the GPO to the production environment</span></span>**

1.  <span data-ttu-id="d2875-334">Dans l’onglet **en attente** , cliquez avec le bouton droit sur **MyGPO** , puis cliquez sur **approuver**.</span><span class="sxs-lookup"><span data-stu-id="d2875-334">On the **Pending** tab, right-click **MyGPO** and then click **Approve**.</span></span>

2.  <span data-ttu-id="d2875-335">Tapez un commentaire à inclure dans l’historique de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-335">Type a comment to include in the history of the GPO.</span></span>

3.  <span data-ttu-id="d2875-336">Cliquez sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="d2875-336">Click **Yes**.</span></span> <span data-ttu-id="d2875-337">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-337">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d2875-338">L’objet de stratégie de groupe est déployé dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="d2875-338">The GPO is deployed to the production environment.</span></span>

**<span data-ttu-id="d2875-339">Pour lier l’objet de stratégie de groupe à un domaine ou une unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="d2875-339">To link the GPO to a domain or organizational unit</span></span>**

1.  <span data-ttu-id="d2875-340">Dans la console GPMC, cliquez avec le bouton droit sur le domaine ou l’unité d’organisation à laquelle vous voulez appliquer l’objet de stratégie de groupe que vous avez configuré, puis cliquez sur **lier un objet de stratégie de groupe existant**.</span><span class="sxs-lookup"><span data-stu-id="d2875-340">In the GPMC, right-click the domain or an OU to which to apply the GPO that you configured, and then click **Link an Existing GPO**.</span></span>

2.  <span data-ttu-id="d2875-341">Dans la boîte de dialogue **Sélectionner un objet GPO** , cliquez sur **MyGPO**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2875-341">In the **Select GPO** dialog box, click **MyGPO**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage4"></a><span data-ttu-id="d2875-342">Étape 4: utiliser un modèle pour créer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-342">Step 4: Use a template to create a GPO</span></span>

<span data-ttu-id="d2875-343">Dans le cadre de cette étape, vous utiliserez un compte avec le rôle d’éditeur pour créer un modèle (version non modifiable et statique d’un objet de stratégie de groupe) à utiliser comme point de départ pour la création de nouveaux objets de stratégie de groupe, puis créez un nouvel objet de stratégie de groupe basé sur ce modèle.</span><span class="sxs-lookup"><span data-stu-id="d2875-343">In this step, you use an account with the Editor role to create a template—an uneditable, static version of a GPO for use as a starting point for creating new GPOs—and then create a new GPO based upon that template.</span></span> <span data-ttu-id="d2875-344">Les modèles permettent de créer rapidement plusieurs objets de stratégie de groupe qui incluent un grand nombre des mêmes paramètres.</span><span class="sxs-lookup"><span data-stu-id="d2875-344">Templates are useful for quickly creating multiple GPOs that include many of the same settings.</span></span>

**<span data-ttu-id="d2875-345">Pour créer un modèle sur la base d’un objet de stratégie de groupe existant</span><span class="sxs-lookup"><span data-stu-id="d2875-345">To create a template based on an existing GPO</span></span>**

1.  <span data-ttu-id="d2875-346">Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’éditeur a été attribué dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-346">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="d2875-347">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-347">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="d2875-348">Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="d2875-348">On the **Contents** tab in the details pane, click the **Controlled** tab.</span></span>

4.  <span data-ttu-id="d2875-349">Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **enregistrer en tant que modèle** pour créer un modèle contenant tous les paramètres actuellement dans MyGPO.</span><span class="sxs-lookup"><span data-stu-id="d2875-349">Right-click **MyGPO**, and then click **Save as Template** to create a template incorporating all settings currently in MyGPO.</span></span>

5.  <span data-ttu-id="d2875-350">Tapez **MyTemplate** comme nom pour le modèle et un commentaire, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2875-350">Type **MyTemplate** as the name for the template and a comment, and then click **OK**.</span></span>

6.  <span data-ttu-id="d2875-351">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-351">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d2875-352">Le nouveau modèle s’affiche sous l’onglet **modèles** .</span><span class="sxs-lookup"><span data-stu-id="d2875-352">The new template appears on the **Templates** tab.</span></span>

**<span data-ttu-id="d2875-353">Pour demander la création d’un nouvel objet de stratégie de groupe géré via AGPM</span><span class="sxs-lookup"><span data-stu-id="d2875-353">To request the creation of a new GPO managed through AGPM</span></span>**

1.  <span data-ttu-id="d2875-354">Cliquez sur l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="d2875-354">Click the **Controlled** tab.</span></span>

2.  <span data-ttu-id="d2875-355">Cliquez avec le bouton droit sur le nœud de **contrôle de modification** , puis cliquez sur **nouvel objet de stratégie de**contrôle.</span><span class="sxs-lookup"><span data-stu-id="d2875-355">Right-click the **Change Control** node, and then click **New Controlled GPO**.</span></span>

3.  <span data-ttu-id="d2875-356">Dans la boîte de dialogue **nouvel objet GPO contrôlé** :</span><span class="sxs-lookup"><span data-stu-id="d2875-356">In the **New Controlled GPO** dialog box:</span></span>

    1.  <span data-ttu-id="d2875-357">Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** .</span><span class="sxs-lookup"><span data-stu-id="d2875-357">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span>

    2.  <span data-ttu-id="d2875-358">Tapez **MyOtherGPO** comme nom du nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-358">Type **MyOtherGPO** as the name for the new GPO.</span></span>

    3.  <span data-ttu-id="d2875-359">Tapez un commentaire pour le nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-359">Type a comment for the new GPO.</span></span>

    4.  <span data-ttu-id="d2875-360">Cliquez sur **créer Live**pour que le nouvel objet GPO soit déployé sur l’environnement de production immédiatement après approbation.</span><span class="sxs-lookup"><span data-stu-id="d2875-360">Click **Create live**, so the new GPO will be deployed to the production environment immediately upon approval.</span></span>

    5.  <span data-ttu-id="d2875-361">Dans **modèle d’objet de stratégie de groupe**, sélectionnez **MyTemplate**.</span><span class="sxs-lookup"><span data-stu-id="d2875-361">For **From GPO template**, select **MyTemplate**.</span></span> <span data-ttu-id="d2875-362">Cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-362">Click **Submit**.</span></span>

4.  <span data-ttu-id="d2875-363">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-363">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d2875-364">Le nouvel objet GPO est affiché dans l’onglet **en attente** .</span><span class="sxs-lookup"><span data-stu-id="d2875-364">The new GPO is displayed on the **Pending** tab.</span></span>

<span data-ttu-id="d2875-365">Utilisez un compte qui a été affecté le rôle d’approbateur pour approuver la demande en attente de création de l’objet de stratégie de groupe, comme vous l’avez fait à l' [étape 1: créer un objet de stratégie de groupe](#bkmk-manage1).</span><span class="sxs-lookup"><span data-stu-id="d2875-365">Use an account that has been assigned the role of Approver to approve the pending request to create the GPO as you did in [Step 1: Create a GPO](#bkmk-manage1).</span></span> <span data-ttu-id="d2875-366">MyTemplate incorpore tous les paramètres que vous avez configurés dans MyGPO.</span><span class="sxs-lookup"><span data-stu-id="d2875-366">MyTemplate incorporates all of the settings that you configured in MyGPO.</span></span> <span data-ttu-id="d2875-367">Dans la mesure où MyOtherGPO a été créé à l’aide de MyTemplate, il contient tous les paramètres qui MyGPO contenus au moment de la création de MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="d2875-367">Because MyOtherGPO was created using MyTemplate, it initially contains all of the settings that MyGPO contained at the time that MyTemplate was created.</span></span> <span data-ttu-id="d2875-368">Pour confirmer cela, vous pouvez générer un rapport de différences et comparer MyOtherGPO à MyTemplate.</span><span class="sxs-lookup"><span data-stu-id="d2875-368">You can confirm this by generating a difference report to compare MyOtherGPO to MyTemplate.</span></span>

**<span data-ttu-id="d2875-369">Pour extraire l’objet de stratégie de groupe de l’archive en vue de le modifier</span><span class="sxs-lookup"><span data-stu-id="d2875-369">To check the GPO out from the archive for editing</span></span>**

1.  <span data-ttu-id="d2875-370">Sur un ordinateur sur lequel vous avez installé le client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’éditeur a été attribué dans AGPM.</span><span class="sxs-lookup"><span data-stu-id="d2875-370">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Editor in AGPM.</span></span>

2.  <span data-ttu-id="d2875-371">Cliquez avec le bouton droit sur **MyOtherGPO**, puis cliquez sur **extraire**.</span><span class="sxs-lookup"><span data-stu-id="d2875-371">Right-click **MyOtherGPO**, and then click **Check Out**.</span></span>

3.  <span data-ttu-id="d2875-372">Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe lors de son extraction, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2875-372">Type a comment to be displayed in the history of the GPO while it is checked out, and then click **OK**.</span></span>

4.  <span data-ttu-id="d2875-373">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-373">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d2875-374">Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **extrait**.</span><span class="sxs-lookup"><span data-stu-id="d2875-374">On the **Controlled** tab, the state of the GPO is identified as **Checked Out**.</span></span>

**<span data-ttu-id="d2875-375">Pour modifier l’objet de stratégie de groupe hors connexion et configurer la durée de verrouillage du compte</span><span class="sxs-lookup"><span data-stu-id="d2875-375">To edit the GPO offline and configure the account lockout duration</span></span>**

1.  <span data-ttu-id="d2875-376">Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur **MyOtherGPO**, puis cliquez sur **modifier** pour ouvrir la fenêtre de l’éditeur de gestion des stratégies de groupe et apporter des modifications à une copie hors connexion de l’objet de stratégie de **groupe** .</span><span class="sxs-lookup"><span data-stu-id="d2875-376">On the **Controlled** tab, right-click **MyOtherGPO**, and then click **Edit** to open the **Group Policy Management Editor** window and make changes to an offline copy of the GPO.</span></span> <span data-ttu-id="d2875-377">Pour ce scénario, configurez la longueur minimale du mot de passe:</span><span class="sxs-lookup"><span data-stu-id="d2875-377">For this scenario, configure the minimum password length:</span></span>

    1.  <span data-ttu-id="d2875-378">Sous **Configuration ordinateur**, double-cliquez sur **stratégies**, **Paramètres Windows**, **paramètres de sécurité**, stratégies de **compte**et stratégie de **verrouillage du compte**.</span><span class="sxs-lookup"><span data-stu-id="d2875-378">Under **Computer Configuration**, double-click **Policies**, **Windows Settings**, **Security Settings**, **Account Policies**, and **Account Lockout Policy**.</span></span>

    2.  <span data-ttu-id="d2875-379">Dans le volet Détails, double-cliquez sur **durée de verrouillage du compte**.</span><span class="sxs-lookup"><span data-stu-id="d2875-379">In the details pane, double-click **Account lockout duration**.</span></span>

    3.  <span data-ttu-id="d2875-380">Dans la fenêtre Propriétés, activez la case à cocher **définir ce paramètre de stratégie**, définissez une durée de **30** minutes, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2875-380">In the properties window, check **Define this policy setting**, set the duration to **30** minutes, and then click **OK**.</span></span>

2.  <span data-ttu-id="d2875-381">Fermez la fenêtre de l' **éditeur de gestion des stratégies de groupe** .</span><span class="sxs-lookup"><span data-stu-id="d2875-381">Close the **Group Policy Management Editor** window.</span></span>

<span data-ttu-id="d2875-382">Consultez MyOtherGPO dans l’archive et demandez le déploiement comme vous l’avez fait pour MyGPO à l' [étape 2: modifier un objet de stratégie de groupe](#bkmk-manage2).</span><span class="sxs-lookup"><span data-stu-id="d2875-382">Check MyOtherGPO into the archive and request deployment as you did for MyGPO in [Step 2: Edit a GPO](#bkmk-manage2).</span></span> <span data-ttu-id="d2875-383">Vous pouvez comparer MyOtherGPO à MyGPO ou à MyTemplate à l’aide de rapports de différences.</span><span class="sxs-lookup"><span data-stu-id="d2875-383">You can compare MyOtherGPO to MyGPO or to MyTemplate using difference reports.</span></span> <span data-ttu-id="d2875-384">Tout compte qui inclut le rôle de réviseur (Administrateur AGPM [contrôle total \], approbateur, éditeur ou réviseur) peut générer des rapports.</span><span class="sxs-lookup"><span data-stu-id="d2875-384">Any account that includes the Reviewer role (AGPM Administrator \[Full Control\], Approver, Editor, or Reviewer) can generate reports.</span></span>

**<span data-ttu-id="d2875-385">Pour comparer un objet GPO à un autre et à un modèle</span><span class="sxs-lookup"><span data-stu-id="d2875-385">To compare a GPO to another GPO and to a template</span></span>**

1.  <span data-ttu-id="d2875-386">Pour comparer MyGPO et MyOtherGPO:</span><span class="sxs-lookup"><span data-stu-id="d2875-386">To compare MyGPO and MyOtherGPO:</span></span>

    1.  <span data-ttu-id="d2875-387">Dans l’onglet **contrôlé** , cliquez sur **MyGPO**.</span><span class="sxs-lookup"><span data-stu-id="d2875-387">On the **Controlled** tab, click **MyGPO**.</span></span> <span data-ttu-id="d2875-388">Appuyez sur CTRL et cliquez sur **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="d2875-388">Press CTRL and then click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="d2875-389">Cliquez avec le bouton droit sur **MyOtherGPO**, pointez sur **différences**, puis cliquez sur **rapport HTML**.</span><span class="sxs-lookup"><span data-stu-id="d2875-389">Right-click **MyOtherGPO**, point to **Differences**, and click **HTML Report**.</span></span>

2.  <span data-ttu-id="d2875-390">Pour comparer MyOtherGPO et MyTemplate:</span><span class="sxs-lookup"><span data-stu-id="d2875-390">To compare MyOtherGPO and MyTemplate:</span></span>

    1.  <span data-ttu-id="d2875-391">Dans l’onglet **contrôlé** , cliquez sur **MyOtherGPO**.</span><span class="sxs-lookup"><span data-stu-id="d2875-391">On the **Controlled** tab, click **MyOtherGPO**.</span></span>

    2.  <span data-ttu-id="d2875-392">Cliquez avec le bouton droit sur **MyOtherGPO**, pointez sur **différences**, puis cliquez sur **modèle**.</span><span class="sxs-lookup"><span data-stu-id="d2875-392">Right-click **MyOtherGPO**, point to **Differences**, and click **Template**.</span></span>

    3.  <span data-ttu-id="d2875-393">Sélectionnez **MyTemplate** et **HTML Report**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2875-393">Select **MyTemplate** and **HTML Report**, and then click **OK**.</span></span>

### <a href="" id="bkmk-manage5"></a><span data-ttu-id="d2875-394">Étape 5: supprimer et restaurer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-394">Step 5: Delete and restore a GPO</span></span>

<span data-ttu-id="d2875-395">Dans le cadre de cette étape, vous jouerez le rôle d’approbateur pour supprimer un objet GPO.</span><span class="sxs-lookup"><span data-stu-id="d2875-395">In this step, you act as an Approver to delete a GPO.</span></span>

**<span data-ttu-id="d2875-396">Pour supprimer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-396">To delete a GPO</span></span>**

1.  <span data-ttu-id="d2875-397">Sur un ordinateur sur lequel vous avez installé un client AGPM, connectez-vous avec un compte d’utilisateur auquel le rôle d’approbateur a été attribué.</span><span class="sxs-lookup"><span data-stu-id="d2875-397">On a computer on which you have installed AGPM Client, log on with a user account that has been assigned the role of Approver.</span></span>

2.  <span data-ttu-id="d2875-398">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-398">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

3.  <span data-ttu-id="d2875-399">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="d2875-399">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

4.  <span data-ttu-id="d2875-400">Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-400">Right-click **MyGPO**, and then click **Delete**.</span></span> <span data-ttu-id="d2875-401">Cliquez sur **Supprimer l’objet GPO d’archive et de production** pour supprimer la version dans l’archive ainsi que la version déployée de l’objet de stratégie de groupe dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="d2875-401">Click **Delete GPO from archive and production** to delete both the version in the archive as well as the deployed version of the GPO in the production environment.</span></span>

5.  <span data-ttu-id="d2875-402">Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2875-402">Type a comment to be displayed in the audit trail for the GPO, and then click **OK**.</span></span>

6.  <span data-ttu-id="d2875-403">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-403">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d2875-404">L’objet de stratégie de groupe est supprimé de l’onglet **contrôlé** et s’affiche sous l’onglet de la **Corbeille** , où il peut être restauré ou détruit.</span><span class="sxs-lookup"><span data-stu-id="d2875-404">The GPO is removed from the **Controlled** tab and is displayed on the **Recycle Bin** tab, where it can be restored or destroyed.</span></span>

<span data-ttu-id="d2875-405">Occasionnellement, il est possible que vous puissiez découvrir après avoir supprimé un objet GPO qu’il est toujours nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d2875-405">Occasionally you may discover after deleting a GPO that it is still needed.</span></span> <span data-ttu-id="d2875-406">Dans le cadre de cette étape, vous vous attendez en tant qu’approbateur de la restauration d’un objet de stratégie de groupe qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="d2875-406">In this step, you act as an Approver to restore a GPO that has been deleted.</span></span>

**<span data-ttu-id="d2875-407">Pour restaurer un objet de stratégie de groupe supprimé</span><span class="sxs-lookup"><span data-stu-id="d2875-407">To restore a deleted GPO</span></span>**

1.  <span data-ttu-id="d2875-408">Dans l’onglet **contenu** , cliquez sur l’onglet **Corbeille** pour afficher les objets de stratégie de groupe supprimés.</span><span class="sxs-lookup"><span data-stu-id="d2875-408">On the **Contents** tab, click the **Recycle Bin** tab to display deleted GPOs.</span></span>

2.  <span data-ttu-id="d2875-409">Cliquez avec le bouton droit sur **MyGPO**, puis cliquez sur **restaurer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-409">Right-click **MyGPO**, and then click **Restore**.</span></span>

3.  <span data-ttu-id="d2875-410">Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2875-410">Type a comment to be displayed in the history of the GPO, and then click **OK**.</span></span>

4.  <span data-ttu-id="d2875-411">Lorsque la fenêtre de **progression d’AGPM** indique la progression globale de l’opération, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-411">When the **AGPM Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d2875-412">L’objet de stratégie de groupe est supprimé de l’onglet **Corbeille** et s’affiche sous l’onglet **contrôlé** .</span><span class="sxs-lookup"><span data-stu-id="d2875-412">The GPO is removed from the **Recycle Bin** tab and is displayed on the **Controlled** tab.</span></span>

    <span data-ttu-id="d2875-413">**Remarques**  La restauration d’un objet de stratégie de groupe dans l’archive ne le redéploie pas automatiquement dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="d2875-413">**Note** Restoring a GPO to the archive does not automatically redeploy it to the production environment.</span></span> <span data-ttu-id="d2875-414">Pour renvoyer l’objet de stratégie de groupe à l’environnement de production, déployez l’objet GPO comme à l' [étape 3: passer en revue et déployer un objet de stratégie de groupe](#bkmk-manage3).</span><span class="sxs-lookup"><span data-stu-id="d2875-414">To return the GPO to the production environment, deploy the GPO as in [Step 3: Review and deploy a GPO](#bkmk-manage3).</span></span>

     

<span data-ttu-id="d2875-415">Après la modification et le déploiement d’un objet de stratégie de groupe, il est possible que les modifications récentes apportées à l’objet GPO causent un problème.</span><span class="sxs-lookup"><span data-stu-id="d2875-415">After editing and deploying a GPO, you may discover that recent changes to the GPO are causing a problem.</span></span> <span data-ttu-id="d2875-416">Dans le cadre de cette étape, vous faites Office d’approbateur pour restaurer une version précédente de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-416">In this step, you act as an Approver to roll back to a previous version of the GPO.</span></span> <span data-ttu-id="d2875-417">Vous pouvez revenir à une version quelconque de l’historique de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2875-417">You can roll back to any version in the history of the GPO.</span></span> <span data-ttu-id="d2875-418">Vous pouvez utiliser des commentaires et des étiquettes pour identifier les versions connues et en cas de modifications spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d2875-418">You can use comments and labels to identify known good versions and when specific changes were made.</span></span>

**<span data-ttu-id="d2875-419">Pour restaurer une version précédente d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="d2875-419">To roll back to a previous version of a GPO</span></span>**

1.  <span data-ttu-id="d2875-420">Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.</span><span class="sxs-lookup"><span data-stu-id="d2875-420">On the **Contents** tab, click the **Controlled** tab to display the controlled GPOs.</span></span>

2.  <span data-ttu-id="d2875-421">Double-cliquez sur **MyGPO** pour afficher son historique.</span><span class="sxs-lookup"><span data-stu-id="d2875-421">Double-click **MyGPO** to display its history.</span></span>

3.  <span data-ttu-id="d2875-422">Cliquez avec le bouton droit sur la version que vous voulez déployer, cliquez sur **déployer**, puis sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="d2875-422">Right-click the version to be deployed, click **Deploy**, and then click **Yes**.</span></span>

4.  <span data-ttu-id="d2875-423">Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-423">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="d2875-424">Dans la fenêtre **historique** , cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="d2875-424">In the **History** window, click **Close**.</span></span>

    <span data-ttu-id="d2875-425">**Remarques**  Pour vérifier que la version qui a été redéployée est la version prévue, examinez un rapport de différences pour les deux versions.</span><span class="sxs-lookup"><span data-stu-id="d2875-425">**Note** To verify that the version that has been redeployed is the version intended, examine a difference report for the two versions.</span></span> <span data-ttu-id="d2875-426">Dans la fenêtre **historique** de l’objet de stratégie de groupe, sélectionnez les deux versions, cliquez dessus avec le bouton droit, pointez sur **différence**, puis cliquez sur rapport **HTML** ou sur **rapport XML**.</span><span class="sxs-lookup"><span data-stu-id="d2875-426">In the **History** window for the GPO, select the two versions, right-click them, point to **Difference**, and then click either **HTML Report** or **XML Report**.</span></span>

     

 

 





