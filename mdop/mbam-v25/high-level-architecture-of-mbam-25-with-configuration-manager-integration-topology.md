---
title: Architecture globale de MBAM2.5 avec la topologie Intégration Configuration Manager
description: Architecture globale de MBAM2.5 avec la topologie Intégration Configuration Manager
author: dansimp
ms.assetid: 075bafa1-792b-4c24-9d8e-5d3153e2112c
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/23/2018
ms.author: dansimp
ms.openlocfilehash: 75af2e22981d76568916c36acadbbb25648b1f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811351"
---
# <span data-ttu-id="72582-103">Architecture de haut niveau de MBAM 2,5 avec topologie d’intégration de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="72582-103">High-level architecture of MBAM 2.5 with Configuration Manager Integration topology</span></span>

<span data-ttu-id="72582-104">Cette rubrique décrit l’architecture recommandée pour le déploiement de Microsoft BitLocker administration et de la surveillance (MBAM) avec la topologie d’intégration de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="72582-104">This topic describes the recommended architecture for deploying Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="72582-105">Cette topologie intègre MBAM à System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="72582-105">This topology integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="72582-106">Pour déployer MBAM avec la topologie autonome, voir [architecture de niveau supérieur d’MBAM 2,5 avec topologie](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)autonome.</span><span class="sxs-lookup"><span data-stu-id="72582-106">To deploy MBAM with the Stand-alone topology, see [High-Level Architecture of MBAM 2.5 with Stand-alone Topology](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span></span>

<span data-ttu-id="72582-107">Pour obtenir la liste des versions prises en charge pour les logiciels mentionnés dans cette rubrique, voir [Configurations prises en charge par MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="72582-107">For a list of the supported versions of the software mentioned in this topic, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

<span data-ttu-id="72582-108">**Important**  Windows to Go n’est pas pris en charge pour l’installation de la topologie d’intégration de Configuration Manager lorsque vous utilisez Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="72582-108">**Important** Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="72582-109">Nombre de serveurs recommandés et nombre de clients pris en charge</span><span class="sxs-lookup"><span data-stu-id="72582-109">Recommended number of servers and supported number of clients</span></span>


<span data-ttu-id="72582-110">Le nombre de serveurs recommandés et le nombre de clients pris en charge dans un environnement de production sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="72582-110">The recommended number of servers and supported number of clients in a production environment is as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72582-111">Architecture recommandée</span><span class="sxs-lookup"><span data-stu-id="72582-111">Recommended architecture</span></span></th>
<th align="left"><span data-ttu-id="72582-112">Détails</span><span class="sxs-lookup"><span data-stu-id="72582-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72582-113">Nombre de serveurs et autres ordinateurs</span><span class="sxs-lookup"><span data-stu-id="72582-113">Number of servers and other computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="72582-114">Trois serveurs</span><span class="sxs-lookup"><span data-stu-id="72582-114">Three servers</span></span></p>
<p><span data-ttu-id="72582-115">Une station de travail</span><span class="sxs-lookup"><span data-stu-id="72582-115">One workstation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72582-116">Nombre d’ordinateurs clients pris en charge</span><span class="sxs-lookup"><span data-stu-id="72582-116">Number of client computers supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="72582-117">500 000</span><span class="sxs-lookup"><span data-stu-id="72582-117">500,000</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="72582-118">Différences entre l’intégration de Configuration Manager et les topologies autonomes</span><span class="sxs-lookup"><span data-stu-id="72582-118">Differences between Configuration Manager Integration and stand-alone topologies</span></span>


<span data-ttu-id="72582-119">Les principales différences entre les topologies sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="72582-119">The main differences between the topologies are:</span></span>

-   <span data-ttu-id="72582-120">Les fonctionnalités de conformité et de création de rapports sont supprimées de MBAM et sont accessibles à partir de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="72582-120">The compliance and reporting features are removed from MBAM and are accessed from Configuration Manager.</span></span>

-   <span data-ttu-id="72582-121">Les rapports sont consultés à partir de la console de gestion Configuration Manager, à l’exception du rapport d’audit de récupération, que vous continuez à consulter à partir du site Web d’administration et de surveillance de MBAM.</span><span class="sxs-lookup"><span data-stu-id="72582-121">Reports are viewed from the Configuration Manager Management Console, with the exception of the Recovery Audit Report, which you continue to view from the MBAM Administration and Monitoring Website.</span></span>

## <span data-ttu-id="72582-122">Architecture de niveau supérieur MBAM recommandée avec la topologie d’intégration de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="72582-122">Recommended MBAM high-level architecture with the Configuration Manager Integration topology</span></span>


<span data-ttu-id="72582-123">Le schéma et le tableau suivants décrivent l’architecture de haut niveau recommandée pour MBAM avec la topologie d’intégration de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="72582-123">The following diagram and table describe the recommended high-level architecture for MBAM with the Configuration Manager Integration topology.</span></span> <span data-ttu-id="72582-124">Les déploiements de forêts multiples MBAM requièrent une approbation à sens unique ou à double sens.</span><span class="sxs-lookup"><span data-stu-id="72582-124">MBAM multi-forest deployments require a one-way or two-way trust.</span></span> <span data-ttu-id="72582-125">Les approbations à sens unique requièrent que le domaine du serveur approuve le domaine client.</span><span class="sxs-lookup"><span data-stu-id="72582-125">One-way trusts require that the server domain trusts the client domain.</span></span>

![mbam2\-5](images/mbam2-5-cmserver.png)

### <span data-ttu-id="72582-127">Serveur de base de données</span><span class="sxs-lookup"><span data-stu-id="72582-127">Database server</span></span>

#### <span data-ttu-id="72582-128">Base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="72582-128">Recovery database</span></span>

<span data-ttu-id="72582-129">Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server et l’instance SQL Server prise en charge.</span><span class="sxs-lookup"><span data-stu-id="72582-129">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="72582-130">La **base de données de récupération** stocke les données de récupération collectées à partir des ordinateurs clients MBAM.</span><span class="sxs-lookup"><span data-stu-id="72582-130">The **Recovery Database** stores recovery data that is collected from MBAM Client computers.</span></span>

#### <span data-ttu-id="72582-131">Base de données d’audit</span><span class="sxs-lookup"><span data-stu-id="72582-131">Audit database</span></span>

<span data-ttu-id="72582-132">Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server et l’instance SQL Server prise en charge.</span><span class="sxs-lookup"><span data-stu-id="72582-132">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="72582-133">La **base de données d’audit** stocke les données d’activité d’audit collectées sur les ordinateurs clients ayant accédé aux données de récupération.</span><span class="sxs-lookup"><span data-stu-id="72582-133">The **Audit Database** stores audit activity data that is collected from client computers that have accessed recovery data.</span></span>

#### <span data-ttu-id="72582-134">Rapports</span><span class="sxs-lookup"><span data-stu-id="72582-134">Reports</span></span>

<span data-ttu-id="72582-135">Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server et l’instance SQL Server prise en charge.</span><span class="sxs-lookup"><span data-stu-id="72582-135">This feature is configured on a computer running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="72582-136">Les **rapports** fournissent des données d’audit de récupération pour les ordinateurs clients de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="72582-136">The **Reports** provide recovery audit data for the client computers in your enterprise.</span></span> <span data-ttu-id="72582-137">Vous pouvez afficher des rapports à partir de la console Configuration Manager ou directement à partir de SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="72582-137">You can view reports from the Configuration Manager console or directly from SQL Server Reporting Services.</span></span>

### <span data-ttu-id="72582-138">Serveur de site principal de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="72582-138">Configuration Manager primary site server</span></span>

<span data-ttu-id="72582-139">Fonctionnalité d’intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="72582-139">System Center Configuration Manager Integration feature</span></span>

-   <span data-ttu-id="72582-140">Cette fonctionnalité est configurée sur le serveur de site principal de Configuration Manager, qui est le serveur de niveau supérieur de votre infrastructure de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="72582-140">This feature is configured on the Configuration Manager Primary Site Server, which is the top-tier server in your Configuration Manager infrastructure.</span></span>

-   <span data-ttu-id="72582-141">Le **serveur Configuration Manager** collecte les informations d’inventaire matériel sur les ordinateurs clients et permet de signaler la compatibilité de BitLocker sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="72582-141">The **Configuration Manager Server** collects the hardware inventory information from client computers and is used to report BitLocker compliance of client computers.</span></span>

-   <span data-ttu-id="72582-142">Lorsque vous exécutez l’Assistant Configuration de l’administration et de la surveillance de BitLocker pour installer le logiciel de serveur, la collection d’ordinateurs pris en charge par MBAM, la planification de la configuration et les rapports sont configurées sur le serveur de site principal de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="72582-142">When you run the Microsoft BitLocker Administration and Monitoring Setup wizard to install the server software, the MBAM Supported Computers collection, configuration baseline, and reports are configured on the Configuration Manager Primary Site Server.</span></span>

-   <span data-ttu-id="72582-143">La **console Configuration Manager** doit être installée sur l’ordinateur sur lequel vous installez le logiciel serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="72582-143">The **Configuration Manager console** must be installed on the same computer on which you install the MBAM Server software.</span></span>

### <span data-ttu-id="72582-144">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="72582-144">Administration and monitoring server</span></span>

#### <span data-ttu-id="72582-145">Site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="72582-145">Administration and monitoring website</span></span>

<span data-ttu-id="72582-146">Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.</span><span class="sxs-lookup"><span data-stu-id="72582-146">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="72582-147">Le **site Web d’administration et de surveillance** permet d’effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="72582-147">The **Administration and monitoring website** is used to:</span></span>

-   <span data-ttu-id="72582-148">Aidez les utilisateurs finaux à pouvoir accéder à leur ordinateur lorsqu’ils sont bloqués. (Cette zone du site Web est souvent appelée support technique.)</span><span class="sxs-lookup"><span data-stu-id="72582-148">Help end users regain access to their computers when they are locked out. (This area of the Website is commonly called the Help Desk.)</span></span>

-   <span data-ttu-id="72582-149">Affichez le rapport d’audit de récupération, qui indique l’activité de récupération pour les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="72582-149">View the Recovery Audit Report, which shows recovery activity for client computers.</span></span> <span data-ttu-id="72582-150">D’autres rapports sont affichés dans la console Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="72582-150">Other reports are viewed from the Configuration Manager console.</span></span>

#### <span data-ttu-id="72582-151">Portail libre-service</span><span class="sxs-lookup"><span data-stu-id="72582-151">Self-service portal</span></span>

<span data-ttu-id="72582-152">Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.</span><span class="sxs-lookup"><span data-stu-id="72582-152">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="72582-153">Le **portail libre-service** est un site Web qui permet aux utilisateurs finaux sur les ordinateurs clients de se connecter de manière indépendante à un site Web pour obtenir une clé de récupération en cas de perte ou d’oubli du mot de passe BitLocker.</span><span class="sxs-lookup"><span data-stu-id="72582-153">The **Self-Service Portal** is a website that enables end users on client computers to independently log on to a website to get a recovery key if they lose or forget their BitLocker password.</span></span>

#### <span data-ttu-id="72582-154">Surveiller les services Web pour ce site Web</span><span class="sxs-lookup"><span data-stu-id="72582-154">Monitoring web services for this website</span></span>

<span data-ttu-id="72582-155">Cette fonctionnalité est installée sur un ordinateur exécutant Windows Server.</span><span class="sxs-lookup"><span data-stu-id="72582-155">This feature is installed on a computer running Windows Server.</span></span>

<span data-ttu-id="72582-156">Les **services Web de surveillance** sont utilisés par le client MBAM et les sites Web pour communiquer avec la base de données.</span><span class="sxs-lookup"><span data-stu-id="72582-156">The **monitoring web services** are used by the MBAM Client and the websites to communicate to the database.</span></span>

**<span data-ttu-id="72582-157">Important</span><span class="sxs-lookup"><span data-stu-id="72582-157">Important</span></span>**<br><span data-ttu-id="72582-158">Le service Web de surveillance n’est plus disponible dans les services d’administration et de surveillance de BitLocker (MBAM) 2,5 SP1 puisque les sites Web MBAM communiquent directement avec la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="72582-158">The Monitoring Web Service is no longer available in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 since the MBAM websites communicate directly with the Recovery Database.</span></span> 

 

### <span data-ttu-id="72582-159">Station de travail de gestion</span><span class="sxs-lookup"><span data-stu-id="72582-159">Management workstation</span></span>

#### <span data-ttu-id="72582-160">Modèles de stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="72582-160">MBAM group policy templates</span></span>

-   <span data-ttu-id="72582-161">Les **modèles de stratégie de groupe MBAM** sont des paramètres de stratégie de groupe définissant les paramètres d’implémentation de MBAM, qui vous permettent de gérer le chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="72582-161">The **MBAM Group Policy Templates** are Group Policy settings that define implementation settings for MBAM, which enable you to manage BitLocker drive encryption.</span></span>

-   <span data-ttu-id="72582-162">Avant d’exécuter MBAM, vous devez télécharger les modèles de stratégie de groupe pour [obtenir les modèles de stratégie de groupe MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) et les copier sur un serveur ou une station de travail exécutant un système d’exploitation Windows Server ou Windows pris en charge.</span><span class="sxs-lookup"><span data-stu-id="72582-162">Before you run MBAM, you must download the Group Policy Templates from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation that is running a supported Windows Server or Windows operating system.</span></span>

    **<span data-ttu-id="72582-163">REMARQUE</span><span class="sxs-lookup"><span data-stu-id="72582-163">NOTE</span></span>**<br><span data-ttu-id="72582-164">La station de travail ne doit pas nécessairement être un ordinateur dédié.</span><span class="sxs-lookup"><span data-stu-id="72582-164">The workstation does not have to be a dedicated computer.</span></span>

     

### <span data-ttu-id="72582-165">Client MBAM et ordinateur client Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="72582-165">MBAM Client and Configuration Manager Client computer</span></span>

#### <span data-ttu-id="72582-166">Logiciel client MBAM</span><span class="sxs-lookup"><span data-stu-id="72582-166">MBAM Client software</span></span>

<span data-ttu-id="72582-167">Le **client MBAM**:</span><span class="sxs-lookup"><span data-stu-id="72582-167">The **MBAM Client**:</span></span>

-   <span data-ttu-id="72582-168">Utilise des objets de stratégie de groupe pour appliquer le chiffrement de lecteur BitLocker sur les ordinateurs clients au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="72582-168">Uses Group Policy Objects to enforce BitLocker drive encryption on client computers in the enterprise.</span></span>

-   <span data-ttu-id="72582-169">Collecte la clé de récupération BitLocker pour trois types de lecteurs de données: les lecteurs du système d’exploitation, les lecteurs de données fixes et les lecteurs de données USB.</span><span class="sxs-lookup"><span data-stu-id="72582-169">Collects the BitLocker recovery key for three data drive types: operating system drives, fixed data drives, and removable (USB) data drives.</span></span>

-   <span data-ttu-id="72582-170">Recueille des informations de récupération et des informations informatiques sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="72582-170">Collects recovery information and computer information about the client computers.</span></span>

#### <span data-ttu-id="72582-171">Client Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="72582-171">Configuration Manager Client</span></span>

<span data-ttu-id="72582-172">Le **client Configuration Manager** permet à Configuration Manager de recueillir des données de compatibilité matérielle sur les ordinateurs clients et de signaler les informations de conformité.</span><span class="sxs-lookup"><span data-stu-id="72582-172">The **Configuration Manager Client** enables Configuration Manager to collect hardware compatibility data about the client computers and report compliance information.</span></span>

 

## <span data-ttu-id="72582-173">Différences du déploiement d’MBAM pour les versions prises en charge du gestionnaire de configurations</span><span class="sxs-lookup"><span data-stu-id="72582-173">Differences in MBAM deployment for supported Configuration Manager versions</span></span>


<span data-ttu-id="72582-174">Lorsque vous déployez MBAM avec la topologie d’intégration de Configuration Manager, vous pouvez installer MBAM sur un serveur de site principal.</span><span class="sxs-lookup"><span data-stu-id="72582-174">When you deploy MBAM with the Configuration Manager Integration topology, you can install MBAM on a primary site server.</span></span> <span data-ttu-id="72582-175">Toutefois, l’installation d’MBAM fonctionne différemment pour le gestionnaire de configuration de Center2012 système et de configuration Manager2007.</span><span class="sxs-lookup"><span data-stu-id="72582-175">However, the MBAM installation works differently for System Center2012 Configuration Manager and Configuration Manager2007.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72582-176">Version de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="72582-176">Configuration Manager version</span></span></th>
<th align="left"><span data-ttu-id="72582-177">Description</span><span class="sxs-lookup"><span data-stu-id="72582-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72582-178">System Center2012 R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="72582-178">System Center2012 R2 Configuration Manager</span></span></p>
<p><span data-ttu-id="72582-179">Gestionnaire de configuration système Center2012</span><span class="sxs-lookup"><span data-stu-id="72582-179">System Center2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="72582-180">Si vous installez MBAM sur un serveur de site principal ou un serveur d’administration centrale, MBAM effectue toutes les actions d’installation sur ce serveur de site.</span><span class="sxs-lookup"><span data-stu-id="72582-180">If you install MBAM on a primary site server or on a central administration server, MBAM performs all of the installation actions on that site server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72582-181">Configuration Manager2007 R2</span><span class="sxs-lookup"><span data-stu-id="72582-181">Configuration Manager2007 R2</span></span></p>
<p><span data-ttu-id="72582-182">Configuration Manager2007</span><span class="sxs-lookup"><span data-stu-id="72582-182">Configuration Manager2007</span></span></p></td>
<td align="left"><p><span data-ttu-id="72582-183">Si vous installez MBAM sur un serveur de site principal qui fait partie d’une hiérarchie de gestionnaires de configuration plus importante avec un serveur parent de site central, MBAM identifie le serveur parent du site central et effectue toutes les actions d’installation sur ce serveur parent.</span><span class="sxs-lookup"><span data-stu-id="72582-183">If you install MBAM on a primary site server that is part of a larger Configuration Manager hierarchy with a central site parent server, MBAM identifies the central site parent server and performs all of the installation actions on that parent server.</span></span> <span data-ttu-id="72582-184">L’installation inclut la vérification préalable et l’installation des objets et des rapports de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="72582-184">The installation includes checking prerequisites and installing the Configuration Manager objects and reports.</span></span></p>
<p><span data-ttu-id="72582-185">Par exemple, si vous installez MBAM sur un serveur de site principal qui est un enfant d’un serveur parent de site central, MBAM installe tous les objets et rapports de configuration du serveur parent.</span><span class="sxs-lookup"><span data-stu-id="72582-185">For example, if you install MBAM on a primary site server that is a child of a central site parent server, MBAM installs all of the Configuration Manager objects and reports on the parent server.</span></span> <span data-ttu-id="72582-186">Si vous installez MBAM sur le serveur parent, MBAM effectue toutes les actions d’installation sur ce serveur parent.</span><span class="sxs-lookup"><span data-stu-id="72582-186">If you install MBAM on the parent server, MBAM performs all of the installation actions on that parent server.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="72582-187">Fonctionnement de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="72582-187">How MBAM works with Configuration Manager</span></span>


<span data-ttu-id="72582-188">L’intégration de MBAM avec Configuration Manager est basée sur un module de configuration qui installe les éléments décrits dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="72582-188">The integration of MBAM with Configuration Manager is based on a configuration pack that installs the items described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72582-189">Éléments installés dans Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="72582-189">Items installed into Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="72582-190">Description</span><span class="sxs-lookup"><span data-stu-id="72582-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72582-191">Données de configuration</span><span class="sxs-lookup"><span data-stu-id="72582-191">Configuration data</span></span></p></td>
<td align="left"><p><span data-ttu-id="72582-192">Les données de configuration installent un planning de référence, appelé «protection BitLocker», qui contient deux éléments de configuration:</span><span class="sxs-lookup"><span data-stu-id="72582-192">The configuration data installs a configuration baseline, called “BitLocker Protection,” which contains two configuration items:</span></span></p>
<ul>
<li><p><span data-ttu-id="72582-193">Protection des lecteurs du système d’exploitation BitLocker</span><span class="sxs-lookup"><span data-stu-id="72582-193">BitLocker Operating System Drive Protection</span></span></p></li>
<li><p><span data-ttu-id="72582-194">Protection des lecteurs de données fixes BitLocker</span><span class="sxs-lookup"><span data-stu-id="72582-194">BitLocker Fixed Data Drives Protection</span></span></p></li>
</ul>
<p><span data-ttu-id="72582-195">Le planning de référence de configuration est déployé sur la collection d’ordinateurs pris en charge par MBAM, qui est également créée lors de l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="72582-195">The configuration baseline is deployed to the MBAM Supported Computers collection, which is also created when MBAM is installed.</span></span></p>
<p><span data-ttu-id="72582-196">Les deux éléments de configuration fournissent la base pour évaluer l’état de conformité des ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="72582-196">The two configuration items provide the basis for evaluating the compliance status of the client computers.</span></span> <span data-ttu-id="72582-197">Ces informations sont capturées, stockées et évaluées dans Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="72582-197">This information is captured, stored, and evaluated in Configuration Manager.</span></span></p>
<p><span data-ttu-id="72582-198">Les éléments de configuration sont basés sur les exigences en matière de conformité pour les lecteurs du système d’exploitation et les lecteurs de données fixes.</span><span class="sxs-lookup"><span data-stu-id="72582-198">The configuration items are based on the compliance requirements for operating system drives and fixed data drives.</span></span> <span data-ttu-id="72582-199">Les informations requises pour les ordinateurs déployés sont collectées afin de permettre d’évaluer la conformité de ces types de lecteurs.</span><span class="sxs-lookup"><span data-stu-id="72582-199">The required details for the deployed computers are collected so that the compliance for those drive types can be evaluated.</span></span></p>
<p><span data-ttu-id="72582-200">Par défaut, la ligne de base de configuration évalue l’état de conformité every12 heures et envoie les données de conformité à Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="72582-200">By default, the configuration baseline evaluates the compliance status every12 hours and sends the compliance data to Configuration Manager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72582-201">Collection d’ordinateurs pris en charge par MBAM</span><span class="sxs-lookup"><span data-stu-id="72582-201">MBAM Supported Computers collection</span></span></p></td>
<td align="left"><p><span data-ttu-id="72582-202">MBAM crée une collection appelée MBAM d’ordinateurs pris en charge.</span><span class="sxs-lookup"><span data-stu-id="72582-202">MBAM creates a collection that is called MBAM Supported Computers.</span></span> <span data-ttu-id="72582-203">Le planning de référence de la configuration est ciblé vers les ordinateurs clients qui se trouvent dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="72582-203">The configuration baseline is targeted to client computers that are in this collection.</span></span></p>
<p><span data-ttu-id="72582-204">Il s’agit d’une collection dynamique.</span><span class="sxs-lookup"><span data-stu-id="72582-204">This is a dynamic collection.</span></span> <span data-ttu-id="72582-205">Par défaut, il exécute every12 heures et évalue l’appartenance, en fonction de trois critères:</span><span class="sxs-lookup"><span data-stu-id="72582-205">By default, it runs every12 hours and evaluates membership, based on three criteria:</span></span></p>
<ul>
<li><p><span data-ttu-id="72582-206">L’ordinateur est une version prise en charge du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="72582-206">The computer is a supported version of the Windows operating system.</span></span></p></li>
<li><p><span data-ttu-id="72582-207">Il s’agit d’un ordinateur physique.</span><span class="sxs-lookup"><span data-stu-id="72582-207">The computer is a physical computer.</span></span> <span data-ttu-id="72582-208">Les machines virtuelles ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="72582-208">Virtual machines are not supported.</span></span></p></li>
<li><p><span data-ttu-id="72582-209">Le module de plateforme sécurisée (TPM) de l’ordinateur est disponible.</span><span class="sxs-lookup"><span data-stu-id="72582-209">The computer has a Trusted Platform Module (TPM) that is available.</span></span> <span data-ttu-id="72582-210">Une version compatible de TPM 1.2 ou version ultérieure est requise pour le son.</span><span class="sxs-lookup"><span data-stu-id="72582-210">A compatible version of TPM1.2 or later is required for Windows7.</span></span> <span data-ttu-id="72582-211">Windows 10, Windows 8.1, Windows8 et Windows to Go ne requièrent aucun module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="72582-211">Windows10, Windows8.1, Windows8, and Windows To Go do not require a TPM.</span></span></p></li>
</ul>
<p><span data-ttu-id="72582-212">La collection est évaluée par rapport à tous les ordinateurs et un sous-ensemble d’ordinateurs compatibles est créé, qui sert de base à l’évaluation de la conformité et au rapport de l’intégration d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="72582-212">The collection is evaluated against all computers and a subset of compatible computers is created, which provides the basis for compliance evaluation and reporting for the MBAM integration.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72582-213">Rapports</span><span class="sxs-lookup"><span data-stu-id="72582-213">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="72582-214">Lorsque vous configurez MBAM à l’aide de la topologie d’intégration de Configuration Manager, vous pouvez afficher tous les rapports dans Configuration Manager, à l’exception du rapport d’audit de récupération, dont vous continuez à afficher le site Web d’administration et de surveillance MBAM.</span><span class="sxs-lookup"><span data-stu-id="72582-214">When you configure MBAM with the Configuration Manager Integration topology, you view all reports in Configuration Manager, except the Recovery Audit Report, the latter of which you continue to view in the MBAM Administration and Monitoring Website.</span></span> <span data-ttu-id="72582-215">Les rapports disponibles dans Configuration Manager sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="72582-215">The reports available in Configuration Manager are:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72582-216">Rapport</span><span class="sxs-lookup"><span data-stu-id="72582-216">Report</span></span></th>
<th align="left"><span data-ttu-id="72582-217">Description</span><span class="sxs-lookup"><span data-stu-id="72582-217">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72582-218">Tableau de bord de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="72582-218">BitLocker Enterprise Compliance Dashboard</span></span></p></td>
<td align="left"><p><span data-ttu-id="72582-219">Fournit aux administrateurs informatiques trois affichages d’informations dans un seul rapport: distribution de l’état de conformité, distribution des erreurs non conforme-distribution et état de conformité par type de lecteur.</span><span class="sxs-lookup"><span data-stu-id="72582-219">Gives IT administrators three views of information in a single report: Compliance Status Distribution, Non Compliant – Errors Distribution, and Compliance Status Distribution By Drive Type.</span></span> <span data-ttu-id="72582-220">Les options d’exploration du rapport permettent aux administrateurs d’effectuer un clic sur les données et d’afficher la liste des ordinateurs qui correspondent à l’état sélectionné.</span><span class="sxs-lookup"><span data-stu-id="72582-220">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72582-221">Détails de la conformité à l’entreprise BitLocker</span><span class="sxs-lookup"><span data-stu-id="72582-221">BitLocker Enterprise Compliance Details</span></span></p></td>
<td align="left"><p><span data-ttu-id="72582-222">Permet aux administrateurs informatiques d’afficher des informations sur l’état de conformité du chiffrement BitLocker de l’entreprise et inclut l’état de conformité de chaque ordinateur.</span><span class="sxs-lookup"><span data-stu-id="72582-222">Lets IT administrators view information about the BitLocker encryption compliance status of the enterprise and includes the compliance status for each computer.</span></span> <span data-ttu-id="72582-223">Les options d’exploration du rapport permettent aux administrateurs d’effectuer un clic sur les données et d’afficher la liste des ordinateurs qui correspondent à l’état sélectionné.</span><span class="sxs-lookup"><span data-stu-id="72582-223">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72582-224">Compatibilité de l’ordinateur BitLocker</span><span class="sxs-lookup"><span data-stu-id="72582-224">BitLocker Computer Compliance</span></span></p></td>
<td align="left"><p><span data-ttu-id="72582-225">Permet aux administrateurs informatiques d’afficher un ordinateur individuel et de déterminer pourquoi il a été signalé avec un statut de conforme ou non conforme.</span><span class="sxs-lookup"><span data-stu-id="72582-225">Lets IT administrators view an individual computer and determine why it was reported with a status of compliant or not compliant.</span></span> <span data-ttu-id="72582-226">Le rapport affiche également l’état de chiffrement des lecteurs du système d’exploitation et des lecteurs de données fixes.</span><span class="sxs-lookup"><span data-stu-id="72582-226">The report also displays the encryption state of the operating system drives and fixed data drives.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72582-227">Résumé de conformité de BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="72582-227">BitLocker Enterprise Compliance Summary</span></span></p></td>
<td align="left"><p><span data-ttu-id="72582-228">Permet aux administrateurs informatiques d’afficher l’état de la conformité de la stratégie MBAM au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="72582-228">Lets IT administrators view the status of MBAM policy compliance in the enterprise.</span></span> <span data-ttu-id="72582-229">L’état de chaque ordinateur est évalué, et le rapport affiche un résumé de la conformité de tous les ordinateurs de l’entreprise par rapport à la stratégie.</span><span class="sxs-lookup"><span data-stu-id="72582-229">Each computer’s state is evaluated, and the report shows a summary of the compliance of all computers in the enterprise against the policy.</span></span> <span data-ttu-id="72582-230">Les options d’exploration du rapport permettent aux administrateurs d’effectuer un clic sur les données et d’afficher la liste des ordinateurs qui correspondent à l’état sélectionné.</span><span class="sxs-lookup"><span data-stu-id="72582-230">Drill-down options on the report let IT administrators click through the data and view a list of computers that match the selected state.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="72582-231">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="72582-231">Related topics</span></span>


[<span data-ttu-id="72582-232">Prise en main de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="72582-232">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="72582-233">Architecture globale de MBAM2.5 avec la topologie autonome</span><span class="sxs-lookup"><span data-stu-id="72582-233">High-Level Architecture of MBAM 2.5 with Stand-alone Topology</span></span>](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[<span data-ttu-id="72582-234">Illustration des composants d'un déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="72582-234">Illustrated Features of an MBAM 2.5 Deployment</span></span>](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## <span data-ttu-id="72582-235">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="72582-235">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="72582-236">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="72582-236">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="72582-237">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="72582-237">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




