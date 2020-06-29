---
title: Architecture globale de MBAM2.5 avec la topologie autonome
description: Architecture globale de MBAM2.5 avec la topologie autonome
author: dansimp
ms.assetid: 35f8c5f6-8be3-443d-baf0-56d68b08f3bc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 75e878e24b4675f2f2f574791d0f06ecadd0196d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811826"
---
# <span data-ttu-id="fd12c-103">Architecture globale de MBAM2.5 avec la topologie autonome</span><span class="sxs-lookup"><span data-stu-id="fd12c-103">High-Level Architecture of MBAM 2.5 with Stand-alone Topology</span></span>


<span data-ttu-id="fd12c-104">Cette rubrique décrit l’architecture recommandée pour le déploiement de Microsoft BitLocker administration et de la surveillance (MBAM) avec la topologie autonome de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fd12c-104">This topic describes the recommended architecture for deploying Microsoft BitLocker Administration and Monitoring (MBAM) with the Configuration Manager Stand-alone topology.</span></span> <span data-ttu-id="fd12c-105">Dans cette topologie, MBAM est déployé en tant que produit autonome.</span><span class="sxs-lookup"><span data-stu-id="fd12c-105">In this topology, MBAM is deployed as a stand-alone product.</span></span> <span data-ttu-id="fd12c-106">Vous pouvez également déployer MBAM avec la topologie d’intégration de Configuration Manager, qui intègre MBAM avec Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fd12c-106">You can alternatively deploy MBAM with the Configuration Manager Integration topology, which integrates MBAM with Configuration Manager.</span></span> <span data-ttu-id="fd12c-107">Pour plus d’informations, reportez-vous à la rubrique [architecture de niveau supérieur de MBAM 2,5 avec la topologie d’intégration de Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="fd12c-107">For more information, see [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span>

<span data-ttu-id="fd12c-108">Pour obtenir la liste des versions prises en charge pour les logiciels mentionnés dans cette rubrique, voir [Configurations prises en charge par MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="fd12c-108">For a list of the supported versions of the software mentioned in this topic, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

<span data-ttu-id="fd12c-109">**Remarques**  Nous vous recommandons d’utiliser une architecture serveur unique uniquement dans les environnements de test.</span><span class="sxs-lookup"><span data-stu-id="fd12c-109">**Note** We recommend you use a single-server architecture in test environments only.</span></span>

 

## <span data-ttu-id="fd12c-110">Nombre de serveurs recommandés et nombre de clients pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd12c-110">Recommended number of servers and supported number of clients</span></span>


<span data-ttu-id="fd12c-111">Le nombre de serveurs recommandés et le nombre de clients pris en charge dans un environnement de production sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="fd12c-111">The recommended number of servers and supported number of clients in a production environment is as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fd12c-112">Architecture recommandée dans un environnement de production</span><span class="sxs-lookup"><span data-stu-id="fd12c-112">Recommended architecture in a production environment</span></span></th>
<th align="left"><span data-ttu-id="fd12c-113">Détails</span><span class="sxs-lookup"><span data-stu-id="fd12c-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fd12c-114">Nombre de serveurs et autres ordinateurs</span><span class="sxs-lookup"><span data-stu-id="fd12c-114">Number of servers and other computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="fd12c-115">Deux serveurs</span><span class="sxs-lookup"><span data-stu-id="fd12c-115">Two servers</span></span></p>
<p><span data-ttu-id="fd12c-116">Une station de travail</span><span class="sxs-lookup"><span data-stu-id="fd12c-116">One workstation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fd12c-117">Nombre d’ordinateurs clients pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd12c-117">Number of client computers supported</span></span></p></td>
<td align="left"><p><span data-ttu-id="fd12c-118">500 000</span><span class="sxs-lookup"><span data-stu-id="fd12c-118">500,000</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fd12c-119">Architecture de niveau supérieur MBAM recommandée avec la topologie autonome</span><span class="sxs-lookup"><span data-stu-id="fd12c-119">Recommended MBAM high-level architecture with the Stand-alone topology</span></span>


<span data-ttu-id="fd12c-120">Le schéma et le tableau ci-dessous décrivent l’architecture de serveur à double niveau recommandée pour MBAM avec la topologie autonome.</span><span class="sxs-lookup"><span data-stu-id="fd12c-120">The following diagram and table describe the recommended high-level, two-server architecture for MBAM with the Stand-alone topology.</span></span> <span data-ttu-id="fd12c-121">Les déploiements de forêts multiples MBAM requièrent une approbation à sens unique ou à double sens.</span><span class="sxs-lookup"><span data-stu-id="fd12c-121">MBAM multi-forest deployments require a one-way or two-way trust.</span></span> <span data-ttu-id="fd12c-122">Les approbations à sens unique requièrent que le domaine du serveur approuve le domaine client.</span><span class="sxs-lookup"><span data-stu-id="fd12c-122">One-way trusts require that the server domain trusts the client domain.</span></span>

![mbam2](images/mbam2-5-2servers.png)

<span data-ttu-id="fd12c-124">Fonctionnalités serveur à configurer sur le serveur de base de données de description du serveur</span><span class="sxs-lookup"><span data-stu-id="fd12c-124">Server Features to configure on this server Description Database server</span></span>

<span data-ttu-id="fd12c-125">Base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="fd12c-125">Compliance and Audit Database</span></span>

<span data-ttu-id="fd12c-126">Cette fonctionnalité est configurée sur un serveur exécutant Windows Server et l’instance SQL Server prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fd12c-126">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="fd12c-127">La **base de données d’audit et de conformité** stocke les données de conformité, qui est principalement utilisée pour les rapports hébergés par SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="fd12c-127">The **Compliance and Audit Database** stores compliance data, which is used primarily for reports that SQL Server Reporting Services hosts.</span></span>

<span data-ttu-id="fd12c-128">Base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="fd12c-128">Recovery Database</span></span>

<span data-ttu-id="fd12c-129">Cette fonctionnalité est configurée sur un serveur exécutant Windows Server et l’instance SQL Server prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fd12c-129">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="fd12c-130">La **base de données de récupération** stocke les données de récupération collectées à partir des ordinateurs clients MBAM.</span><span class="sxs-lookup"><span data-stu-id="fd12c-130">The **Recovery Database** stores recovery data that is collected from MBAM client computers.</span></span>

<span data-ttu-id="fd12c-131">Rapports</span><span class="sxs-lookup"><span data-stu-id="fd12c-131">Reports</span></span>

<span data-ttu-id="fd12c-132">Cette fonctionnalité est configurée sur un serveur exécutant Windows Server et l’instance SQL Server prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fd12c-132">This feature is configured on a server running Windows Server and supported SQL Server instance.</span></span>

<span data-ttu-id="fd12c-133">Les **rapports** fournissent des données d’audit de récupération et de conformité sur les ordinateurs clients de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="fd12c-133">The **Reports** provide recovery audit and compliance status data about the client computers in your enterprise.</span></span> <span data-ttu-id="fd12c-134">Vous pouvez accéder aux rapports à partir du site Web d’administration et de surveillance ou directement à partir de SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="fd12c-134">You can access the reports from the Administration and Monitoring Website or directly from SQL Server Reporting Services.</span></span>

<span data-ttu-id="fd12c-135">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="fd12c-135">Administration and Monitoring Server</span></span>

<span data-ttu-id="fd12c-136">Site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="fd12c-136">Administration and Monitoring Website</span></span>

<span data-ttu-id="fd12c-137">Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.</span><span class="sxs-lookup"><span data-stu-id="fd12c-137">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="fd12c-138">Le **site Web d’administration et de surveillance** permet d’effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="fd12c-138">The **Administration and Monitoring Website** is used to:</span></span>

-   <span data-ttu-id="fd12c-139">Aidez les utilisateurs finaux à pouvoir accéder à leur ordinateur lorsqu’ils sont bloqués. (Cette zone du site Web est souvent appelée support technique.)</span><span class="sxs-lookup"><span data-stu-id="fd12c-139">Help end users regain access to their computers when they are locked out. (This area of the Website is commonly called the Help Desk.)</span></span>

-   <span data-ttu-id="fd12c-140">Affichez des rapports qui présentent l’état de conformité et l’activité de récupération pour les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="fd12c-140">View reports that show compliance status and recovery activity for client computers.</span></span>

<span data-ttu-id="fd12c-141">Portail libre-service</span><span class="sxs-lookup"><span data-stu-id="fd12c-141">Self-Service Portal</span></span>

<span data-ttu-id="fd12c-142">Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.</span><span class="sxs-lookup"><span data-stu-id="fd12c-142">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="fd12c-143">Le **portail libre-service** est un site Web qui permet aux utilisateurs finaux sur les ordinateurs clients de se connecter de manière indépendante à un site Web pour obtenir une clé de récupération en cas de perte ou d’oubli du mot de passe BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fd12c-143">The **Self-Service Portal** is a website that enables end users on client computers to independently log on to a website to get a recovery key if they lose or forget their BitLocker password.</span></span>

<span data-ttu-id="fd12c-144">Surveiller les services Web pour ce site Web</span><span class="sxs-lookup"><span data-stu-id="fd12c-144">Monitoring web services for this website</span></span>

<span data-ttu-id="fd12c-145">Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.</span><span class="sxs-lookup"><span data-stu-id="fd12c-145">This feature is configured on a computer running Windows Server.</span></span>

<span data-ttu-id="fd12c-146">Les **services Web de surveillance** sont utilisés par le client MBAM et les sites Web pour communiquer avec la base de données.</span><span class="sxs-lookup"><span data-stu-id="fd12c-146">The **monitoring web services** are used by the MBAM Client and the websites to communicate to the database.</span></span>

<span data-ttu-id="fd12c-147">**Important**  Le service Web de surveillance n’est plus disponible dans les services d’administration et de surveillance de BitLocker (MBAM) 2,5 SP1 puisque les sites Web MBAM communiquent directement avec la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="fd12c-147">**Important** The Monitoring Web Service is no longer available in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 since the MBAM websites communicate directly with the Recovery Database.</span></span>

 

<span data-ttu-id="fd12c-148">Station de travail de gestion</span><span class="sxs-lookup"><span data-stu-id="fd12c-148">Management workstation</span></span>

<span data-ttu-id="fd12c-149">Modèles de stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="fd12c-149">MBAM Group Policy Templates</span></span>

-   <span data-ttu-id="fd12c-150">Les modèles de stratégie de groupe MBAM sont des paramètres de stratégie de groupe définissant les paramètres d’implémentation de MBAM, qui vous permettent de gérer le chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fd12c-150">The MBAM Group Policy Templates are Group Policy settings that define implementation settings for MBAM, which enable you to manage BitLocker Drive Encryption.</span></span>

-   <span data-ttu-id="fd12c-151">Avant d’exécuter MBAM, vous devez télécharger les modèles de stratégie de groupe pour [obtenir les modèles de stratégie de groupe MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) et les copier sur un serveur ou une station de travail exécutant un système d’exploitation Windows Server ou Windows pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fd12c-151">Before you run MBAM, you must download the Group Policy Templates from [How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941) and copy them to a server or workstation that is running a supported Windows Server or Windows operating system.</span></span>

-   <span data-ttu-id="fd12c-152">La station de travail ne doit pas nécessairement être un ordinateur dédié.</span><span class="sxs-lookup"><span data-stu-id="fd12c-152">The workstation does not have to be a dedicated computer.</span></span>

<span data-ttu-id="fd12c-153">Client MBAM et ordinateur client Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="fd12c-153">MBAM Client and Configuration Manager client computer</span></span>

<span data-ttu-id="fd12c-154">Logiciel client MBAM</span><span class="sxs-lookup"><span data-stu-id="fd12c-154">MBAM Client software</span></span>

<span data-ttu-id="fd12c-155">Le client MBAM:</span><span class="sxs-lookup"><span data-stu-id="fd12c-155">The MBAM Client:</span></span>

-   <span data-ttu-id="fd12c-156">Utilise des objets de stratégie de groupe pour appliquer le chiffrement de lecteur BitLocker sur les ordinateurs clients au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="fd12c-156">Uses Group Policy Objects to enforce BitLocker Drive Encryption on client computers in the enterprise.</span></span>

-   <span data-ttu-id="fd12c-157">Collecte la clé de récupération BitLocker pour trois types de lecteurs de données: les lecteurs du système d’exploitation, les lecteurs de données fixes et les lecteurs de données USB.</span><span class="sxs-lookup"><span data-stu-id="fd12c-157">Collects the Bitlocker recovery key for three data drive types: operating system drives, fixed data drives, and removable (USB) data drives.</span></span>

-   <span data-ttu-id="fd12c-158">Recueille des informations de récupération et des informations informatiques sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="fd12c-158">Collects recovery information and computer information about the client computers.</span></span>



## <span data-ttu-id="fd12c-159">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fd12c-159">Related topics</span></span>


[<span data-ttu-id="fd12c-160">Prise en main de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="fd12c-160">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)

[<span data-ttu-id="fd12c-161">Architecture globale de MBAM2.5 avec la topologie Intégration Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="fd12c-161">High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology</span></span>](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[<span data-ttu-id="fd12c-162">Illustration des composants d'un déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="fd12c-162">Illustrated Features of an MBAM 2.5 Deployment</span></span>](illustrated-features-of-an-mbam-25-deployment.md)

 

## <span data-ttu-id="fd12c-163">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="fd12c-163">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="fd12c-164">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="fd12c-164">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="fd12c-165">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="fd12c-165">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





