---
title: Planification du déploiement de serveursMBAM2.5
description: Planification du déploiement de serveursMBAM2.5
author: dansimp
ms.assetid: 88774c89-31c8-4eb8-a845-a00bbec8c870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2ecb510fab821118ce210577f9ffb83c39be050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811621"
---
# <span data-ttu-id="da3d1-103">Planification du déploiement de serveursMBAM2.5</span><span class="sxs-lookup"><span data-stu-id="da3d1-103">Planning for MBAM 2.5 Server Deployment</span></span>


<span data-ttu-id="da3d1-104">Cette rubrique répertorie les fonctionnalités que vous déployez pour les topologies autonomes et de gestionnaire de configuration MBAM et indique l’ordre dans lequel vous devez les déployer.</span><span class="sxs-lookup"><span data-stu-id="da3d1-104">This topic lists the features that you deploy for the MBAM Stand-alone and Configuration Manager topologies and lists the order in which you need to deploy them.</span></span> <span data-ttu-id="da3d1-105">Il existe une configuration recommandée pour chaque topologie.</span><span class="sxs-lookup"><span data-stu-id="da3d1-105">There is a recommended configuration for each topology.</span></span> <span data-ttu-id="da3d1-106">Toutefois, vous pouvez configurer les fonctionnalités et bases de données serveur MBAM dans différentes configurations et sur plusieurs serveurs, en fonction de vos besoins en matière d’évolutivité.</span><span class="sxs-lookup"><span data-stu-id="da3d1-106">However, you can configure MBAM server databases and features in different configurations and across multiple servers, depending on your scalability requirements.</span></span>

## <span data-ttu-id="da3d1-107">Remarques importantes en matière de planification pour les deux topologies</span><span class="sxs-lookup"><span data-stu-id="da3d1-107">Important planning considerations for both topologies</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="da3d1-108">Concernant</span><span class="sxs-lookup"><span data-stu-id="da3d1-108">Considerations</span></span></th>
<th align="left"><span data-ttu-id="da3d1-109">Détails ou objectif</span><span class="sxs-lookup"><span data-stu-id="da3d1-109">Details or purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3d1-110">Passez en revue les éléments suivants avant de commencer le déploiement:</span><span class="sxs-lookup"><span data-stu-id="da3d1-110">Review the following before you start the deployment:</span></span></p>
<ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="da3d1-111">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</span><span class="sxs-lookup"><span data-stu-id="da3d1-111">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="da3d1-112">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="da3d1-112">MBAM 2.5 Supported Configurations</span></span></a></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="da3d1-113">Chaque fonctionnalité MBAM comporte des éléments requis spécifiques qui doivent être satisfaits avant de démarrer l’installation d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="da3d1-113">Each MBAM feature has specific prerequisites that must be met before you start the MBAM installation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da3d1-114">Les clés de récupération BitLocker dans MBAM expirent après une utilisation unique.</span><span class="sxs-lookup"><span data-stu-id="da3d1-114">BitLocker recovery keys in MBAM expire after a single use.</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3d1-115">Une utilisation unique signifie que la clé de récupération a été récupérée via le site Web d’administration et de contrôle (également appelé support technique), portail libre-service ou à l’aide de l’applet de contrôle <strong> Windows PowerShell Get-MbamBitLockerRecoveryKey </strong> .</span><span class="sxs-lookup"><span data-stu-id="da3d1-115">A single use means that the recovery key has been retrieved through the Administration and Monitoring Website (also known as Help Desk), Self-Service Portal, or by using the Get-<strong>MbamBitLockerRecoveryKey</strong> Windows PowerShell cmdlet.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="da3d1-116">Assurez le suivi des noms des ordinateurs sur lesquels vous configurez chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="da3d1-116">Keep track of the names of the computers on which you configure each feature.</span></span> <span data-ttu-id="da3d1-117">Vous utiliserez ces informations tout au long du processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="da3d1-117">You will use this information throughout the configuration process.</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3d1-118">Vous pouvez utiliser la <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"> liste de vérification de déploiement de MBAM 2,5 </a> à cette fin.</span><span class="sxs-lookup"><span data-stu-id="da3d1-118">You may want to use the <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)">MBAM 2.5 Deployment Checklist</a> for this purpose.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="da3d1-119">Configurez uniquement les paramètres de stratégie de groupe du nœud MDOP MBAM (gestion BitLocker).</span><span class="sxs-lookup"><span data-stu-id="da3d1-119">Configure only the Group Policy settings in the MDOP MBAM (BitLocker Management) node.</span></span> <span data-ttu-id="da3d1-120">Ne modifiez pas les paramètres de stratégie de groupe du nœud BitLocker Drive Encryption.</span><span class="sxs-lookup"><span data-stu-id="da3d1-120">Do not change the Group Policy settings in the BitLocker Drive Encryption node.</span></span></p></td>
<td align="left"><p><span data-ttu-id="da3d1-121">Si vous modifiez les paramètres de stratégie de groupe dans le nœud BitLocker Drive Encryption, MBAM ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="da3d1-121">If you change the Group Policy settings in the BitLocker Drive Encryption node, MBAM will not work.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="planning-for-mbam-server-deployment---stand-alone-topology"></a><span data-ttu-id="da3d1-122">Planification du déploiement de MBAM Server-topologie autonome</span><span class="sxs-lookup"><span data-stu-id="da3d1-122">Planning for MBAM Server deployment – Stand-alone topology</span></span>


<span data-ttu-id="da3d1-123">Dans le cas d’une topologie autonome, il est recommandé de configurer deux serveurs pour les environnements de production, même si les configurations de trois à quatre serveurs peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="da3d1-123">For the Stand-alone topology, a two-server configuration is recommended for production environments, although configurations of three to four servers can be used.</span></span>

<span data-ttu-id="da3d1-124">L’infrastructure de serveur pour la topologie autonome MBAM contient les fonctionnalités suivantes, qui doivent être configurées dans l’ordre indiqué:</span><span class="sxs-lookup"><span data-stu-id="da3d1-124">The Server infrastructure for the MBAM Stand-alone topology contains the following features, which must be configured in the order listed:</span></span>

1.  <span data-ttu-id="da3d1-125">Bases de données (bases de données d’audit et de conformité)</span><span class="sxs-lookup"><span data-stu-id="da3d1-125">Databases (Compliance and Audit Database and Recovery Database)</span></span>

2.  <span data-ttu-id="da3d1-126">Rapports</span><span class="sxs-lookup"><span data-stu-id="da3d1-126">Reports</span></span>

3.  <span data-ttu-id="da3d1-127">Applications Web (et leurs services Web correspondants)</span><span class="sxs-lookup"><span data-stu-id="da3d1-127">Web applications (and their corresponding web services)</span></span>

    -   <span data-ttu-id="da3d1-128">Site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="da3d1-128">Administration and Monitoring Website</span></span>

    -   <span data-ttu-id="da3d1-129">Portail libre-service</span><span class="sxs-lookup"><span data-stu-id="da3d1-129">Self-Service Portal</span></span>

<span data-ttu-id="da3d1-130">Pour obtenir une description de ces fonctionnalités, voir [architecture de niveau supérieur de MBAM 2,5 avec topologie autonome](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span><span class="sxs-lookup"><span data-stu-id="da3d1-130">For a description of these features, see [High-Level Architecture of MBAM 2.5 with Stand-alone Topology](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).</span></span>

## <a href="" id="planning-for-mbam-server-deployment---configuration-manager-topology"></a><span data-ttu-id="da3d1-131">Planification du déploiement de MBAM Server – topologie de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="da3d1-131">Planning for MBAM Server deployment – Configuration Manager topology</span></span>


<span data-ttu-id="da3d1-132">Pour la topologie d’intégration de Configuration Manager, une configuration à trois serveurs est recommandée pour les environnements de production, même si des configurations de serveurs supplémentaires peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="da3d1-132">For the Configuration Manager Integration topology, a three-server configuration is recommended for production environments, although configurations of additional servers can be used.</span></span>

<span data-ttu-id="da3d1-133">L’infrastructure de serveur pour la topologie du gestionnaire de configuration MBAM contient les fonctionnalités suivantes, qui doivent être configurées ou exécutées dans l’ordre indiqué:</span><span class="sxs-lookup"><span data-stu-id="da3d1-133">The Server infrastructure for the MBAM Configuration Manager topology contains the following features, which must be configured or performed in the order listed:</span></span>

1.  <span data-ttu-id="da3d1-134">Bases de données (bases de données d’audit et de conformité)</span><span class="sxs-lookup"><span data-stu-id="da3d1-134">Databases (Compliance and Audit Database and Recovery Database)</span></span>

2.  <span data-ttu-id="da3d1-135">Rapports</span><span class="sxs-lookup"><span data-stu-id="da3d1-135">Reports</span></span>

3.  <span data-ttu-id="da3d1-136">Applications Web (et leurs services Web correspondants)</span><span class="sxs-lookup"><span data-stu-id="da3d1-136">Web applications (and their corresponding web services)</span></span>

    -   <span data-ttu-id="da3d1-137">Site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="da3d1-137">Administration and Monitoring Website</span></span>

    -   <span data-ttu-id="da3d1-138">Portail libre-service</span><span class="sxs-lookup"><span data-stu-id="da3d1-138">Self-Service Portal</span></span>

4.  <span data-ttu-id="da3d1-139">Intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="da3d1-139">System Center Configuration Manager Integration</span></span>

<span data-ttu-id="da3d1-140">Pour obtenir une description de ces fonctionnalités, voir [architecture de niveau supérieur de MBAM 2,5 avec topologie d’intégration de Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="da3d1-140">For a description of these features, see [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span>



## <span data-ttu-id="da3d1-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da3d1-141">Related topics</span></span>


[<span data-ttu-id="da3d1-142">Planification du déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="da3d1-142">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="da3d1-143">Déploiement de l'infrastructure de serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="da3d1-143">Deploying the MBAM 2.5 Server Infrastructure</span></span>](deploying-the-mbam-25-server-infrastructure.md)

 

## <span data-ttu-id="da3d1-144">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="da3d1-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="da3d1-145">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="da3d1-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="da3d1-146">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="da3d1-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





