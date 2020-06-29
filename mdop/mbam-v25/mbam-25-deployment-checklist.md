---
title: Liste de contrôle du déploiement de MBAM2.5
description: Liste de contrôle du déploiement de MBAM2.5
author: dansimp
ms.assetid: 2ba7de17-e3a4-4798-99e0-cd1dc28c5b76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11609b3d6d44d62b032e35005e5d967ca6d4e83b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809593"
---
# <span data-ttu-id="99e2b-103">Liste de contrôle du déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="99e2b-103">MBAM 2.5 Deployment Checklist</span></span>


<span data-ttu-id="99e2b-104">Vous pouvez utiliser cette liste de contrôle pour vous aider lors du déploiement de Microsoft BitLocker administration et de la surveillance (MBAM) avec une topologie autonome.</span><span class="sxs-lookup"><span data-stu-id="99e2b-104">You can use this checklist to help you during Microsoft BitLocker Administration and Monitoring (MBAM) deployment with a Stand-alone topology.</span></span>

**<span data-ttu-id="99e2b-105">Remarque</span><span class="sxs-lookup"><span data-stu-id="99e2b-105">Note</span></span>**  
<span data-ttu-id="99e2b-106">Cette liste de vérification décrit les étapes recommandées et une liste générale des éléments à prendre en compte lorsque vous déployez les fonctionnalités d’administration et de surveillance de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="99e2b-106">This checklist outlines the recommended steps and a high-level list of items to consider when you deploy Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="99e2b-107">Nous vous recommandons de copier cette liste de vérification dans un tableur et de la personnaliser pour votre utilisation.</span><span class="sxs-lookup"><span data-stu-id="99e2b-107">We recommend that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="99e2b-108">Tâche</span><span class="sxs-lookup"><span data-stu-id="99e2b-108">Task</span></span></th>
<th align="left"><span data-ttu-id="99e2b-109">Références</span><span class="sxs-lookup"><span data-stu-id="99e2b-109">References</span></span></th>
<th align="left"><span data-ttu-id="99e2b-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="99e2b-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="99e2b-111">Passez en revue et effectuez toutes les étapes de planification pour préparer votre environnement pour le déploiement de MBAM.</span><span class="sxs-lookup"><span data-stu-id="99e2b-111">Review and complete all planning steps to prepare your environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-25-planning-checklist.md" data-raw-source="[MBAM 2.5 Planning Checklist](mbam-25-planning-checklist.md)"><span data-ttu-id="99e2b-112">Liste de contrôle de la planification de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="99e2b-112">MBAM 2.5 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="99e2b-113">Passez en revue les informations de configurations prises en charge pour vous assurer que MBAM prend en charge les ordinateurs client et serveur sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="99e2b-113">Review the supported configurations information to ensure that MBAM supports the selected client and server computers.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="99e2b-114">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="99e2b-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="99e2b-115">Installez le logiciel serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="99e2b-115">Install the MBAM Server software.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="99e2b-116">Installation du logiciel serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="99e2b-116">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="99e2b-117">Configurer les fonctionnalités du serveur MBAM:</span><span class="sxs-lookup"><span data-stu-id="99e2b-117">Configure the MBAM Server features:</span></span></p>
<ul>
<li><p><span data-ttu-id="99e2b-118">Conformité et audit de la base de données et de la base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="99e2b-118">Compliance and Audit Database and Recovery Database</span></span></p></li>
<li><p><span data-ttu-id="99e2b-119">Rapports</span><span class="sxs-lookup"><span data-stu-id="99e2b-119">Reports</span></span></p></li>
<li><p><span data-ttu-id="99e2b-120">Applications Web</span><span class="sxs-lookup"><span data-stu-id="99e2b-120">Web applications</span></span></p></li>
<li><p><span data-ttu-id="99e2b-121">Topologie d’intégration de Configuration Manager (requis uniquement si vous exécutez MBAM avec cette topologie)</span><span class="sxs-lookup"><span data-stu-id="99e2b-121">Configuration Manager Integration topology (needed only if you are running MBAM with this topology)</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="99e2b-122">Remarque</span><span class="sxs-lookup"><span data-stu-id="99e2b-122">Note</span></span></strong><br/><p><span data-ttu-id="99e2b-123">Notez les noms des serveurs sur lesquels vous configurez chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="99e2b-123">Note the names of the servers on which you configure each feature.</span></span> <span data-ttu-id="99e2b-124">Vous utiliserez ces informations tout au long du processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="99e2b-124">You will use this information throughout the configuration process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="configuring-the-mbam-25-server-features.md" data-raw-source="[Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md)"><span data-ttu-id="99e2b-125">Configuration des composants du serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="99e2b-125">Configuring the MBAM 2.5 Server Features</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="99e2b-126">Validez la configuration MBAM.</span><span class="sxs-lookup"><span data-stu-id="99e2b-126">Validate the MBAM configuration.</span></span></p></td>
<td align="left"><p><a href="validating-the-mbam-25-server-feature-configuration.md" data-raw-source="[Validating the MBAM 2.5 Server Feature Configuration](validating-the-mbam-25-server-feature-configuration.md)"><span data-ttu-id="99e2b-127">Validation de la configuration des composants serveur de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="99e2b-127">Validating the MBAM 2.5 Server Feature Configuration</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="99e2b-128">Copiez le modèle de stratégie de groupe MBAM et modifiez les paramètres de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="99e2b-128">Copy the MBAM Group Policy Template and edit the Group Policy settings.</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="99e2b-129">Copie des modèles de stratégie de groupe MBAM 2,5 </a> et <a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"> modification des paramètres de stratégie de groupe MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="99e2b-129">Copying the MBAM 2.5 Group Policy Templates</a> and <a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">Editing the MBAM 2.5 Group Policy Settings</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="99e2b-130">Déployez le logiciel client MBAM.</span><span class="sxs-lookup"><span data-stu-id="99e2b-130">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-25-client.md" data-raw-source="[Deploying the MBAM 2.5 Client](deploying-the-mbam-25-client.md)"><span data-ttu-id="99e2b-131">Déploiement du client MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="99e2b-131">Deploying the MBAM 2.5 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>




## <span data-ttu-id="99e2b-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="99e2b-132">Related topics</span></span>


[<span data-ttu-id="99e2b-133">Déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="99e2b-133">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)




## <span data-ttu-id="99e2b-134">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="99e2b-134">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="99e2b-135">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="99e2b-135">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="99e2b-136">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="99e2b-136">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




