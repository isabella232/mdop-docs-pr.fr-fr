---
title: Configuration des composants du serveur MBAM2.5
description: Configuration des composants du serveur MBAM2.5
author: dansimp
ms.assetid: 894d1080-5f13-48f7-8fde-82f8d440a4ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6ba2fc49086acf698f61b9997505c8fa884c0eb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809726"
---
# <span data-ttu-id="5ff21-103">Configuration des composants du serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5ff21-103">Configuring the MBAM 2.5 Server Features</span></span>


<span data-ttu-id="5ff21-104">Utilisez ces informations comme point de départ pour la configuration des fonctionnalités serveur d’administration et de surveillance de BitLocker (MBAM) 2,5 après [l’installation du logiciel MBAM 2,5 Server](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="5ff21-104">Use this information as a starting place for configuring Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server features after [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span> <span data-ttu-id="5ff21-105">Vous pouvez utiliser deux méthodes pour configurer MBAM:</span><span class="sxs-lookup"><span data-stu-id="5ff21-105">There are two methods you can use to configure MBAM:</span></span>

-   <span data-ttu-id="5ff21-106">Assistant Configuration de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="5ff21-106">MBAM Server Configuration wizard</span></span>

-   <span data-ttu-id="5ff21-107">Cmdlets Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5ff21-107">Windows PowerShell cmdlets</span></span>

## <span data-ttu-id="5ff21-108">Avant de commencer à configurer les fonctionnalités de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="5ff21-108">Before you start configuring MBAM Server features</span></span>


<span data-ttu-id="5ff21-109">Passez en revue et suivez les étapes ci-dessous avant de commencer à configurer les fonctionnalités du serveur MBAM:</span><span class="sxs-lookup"><span data-stu-id="5ff21-109">Review and complete the following steps before you start configuring the MBAM Server features:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ff21-110">Étape</span><span class="sxs-lookup"><span data-stu-id="5ff21-110">Step</span></span></th>
<th align="left"><span data-ttu-id="5ff21-111">Où obtenir des instructions</span><span class="sxs-lookup"><span data-stu-id="5ff21-111">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ff21-112">Passez en revue l’architecture recommandée pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="5ff21-112">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="5ff21-113">Architecture de hautniveau pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5ff21-113">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ff21-114">Passez en revue les configurations prises en charge pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="5ff21-114">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="5ff21-115">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5ff21-115">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ff21-116">Remplissez les conditions préalables requises sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="5ff21-116">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="5ff21-117">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</span><span class="sxs-lookup"><span data-stu-id="5ff21-117">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="5ff21-118">Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="5ff21-118">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ff21-119">Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous allez configurer une fonctionnalité de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="5ff21-119">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="5ff21-120">Installation du logiciel serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5ff21-120">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ff21-121">Reportez-vous aux conditions préalables à l’utilisation de Windows PowerShell pour configurer les fonctionnalités du serveur MBAM (si vous utilisez cette méthode pour configurer les fonctionnalités du serveur MBAM).</span><span class="sxs-lookup"><span data-stu-id="5ff21-121">Review the prerequisites for using Windows PowerShell to configure MBAM Server features (if you are using this method to configure MBAM Server features).</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="5ff21-122">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5ff21-122">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5ff21-123">Étapes de configuration des fonctionnalités de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="5ff21-123">Steps for configuring MBAM Server features</span></span>


<span data-ttu-id="5ff21-124">Chaque ligne du tableau suivant décrit les fonctionnalités que vous allez configurer sur un serveur distinct, selon l' [architecture de niveau supérieur recommandée pour MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="5ff21-124">Each row in the following table describes the features that you will configure on a separate server, according to the recommended [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ff21-125">Fonctionnalités à installer</span><span class="sxs-lookup"><span data-stu-id="5ff21-125">Features to install</span></span></th>
<th align="left"><span data-ttu-id="5ff21-126">Où obtenir des instructions</span><span class="sxs-lookup"><span data-stu-id="5ff21-126">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ff21-127">Configurez les bases de données.</span><span class="sxs-lookup"><span data-stu-id="5ff21-127">Configure the databases.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)"><span data-ttu-id="5ff21-128">Comment configurer les bases de données MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5ff21-128">How to Configure the MBAM 2.5 Databases</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ff21-129">Configurez les rapports.</span><span class="sxs-lookup"><span data-stu-id="5ff21-129">Configure the reports.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)"><span data-ttu-id="5ff21-130">Configuration des rapports MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5ff21-130">How to Configure the MBAM 2.5 Reports</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ff21-131">Configurez les applications Web.</span><span class="sxs-lookup"><span data-stu-id="5ff21-131">Configure the web applications.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="5ff21-132">Comment configurer les applications Web MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5ff21-132">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ff21-133">Configurer l’intégration de System Center Configuration Manager (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="5ff21-133">Configure the System Center Configuration Manager Integration (if applicable).</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)"><span data-ttu-id="5ff21-134">Comment configurer l'intégration de MBAM2.5 à System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="5ff21-134">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="5ff21-135">Pour obtenir la liste des événements sur la configuration des fonctionnalités de MBAM Server, voir [journaux des événements serveur](server-event-logs.md).</span><span class="sxs-lookup"><span data-stu-id="5ff21-135">For a list of events about MBAM Server feature configuration, see [Server Event Logs](server-event-logs.md).</span></span>



## <span data-ttu-id="5ff21-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ff21-136">Related topics</span></span>


<span data-ttu-id="5ff21-137">Configuration des composants du serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5ff21-137">Configuring the MBAM 2.5 Server Features</span></span>
 

 
## <span data-ttu-id="5ff21-138">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="5ff21-138">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="5ff21-139">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="5ff21-139">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="5ff21-140">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="5ff21-140">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




