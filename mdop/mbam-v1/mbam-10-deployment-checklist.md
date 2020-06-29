---
title: Liste de contrôle du déploiement de MBAM1.0
description: Liste de contrôle du déploiement de MBAM1.0
author: dansimp
ms.assetid: 7e00be23-36a0-4b0f-8663-3c4f2c71546d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 96725183af2cb4e3d86d3f42973452c598497773
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804302"
---
# <span data-ttu-id="1960c-103">Liste de contrôle du déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="1960c-103">MBAM 1.0 Deployment Checklist</span></span>


<span data-ttu-id="1960c-104">Cette liste de vérification a été conçue pour faciliter le déploiement de l’administration et de la surveillance de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="1960c-104">This checklist is designed to facilitate your deployment of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

**<span data-ttu-id="1960c-105">Remarque</span><span class="sxs-lookup"><span data-stu-id="1960c-105">Note</span></span>**  
<span data-ttu-id="1960c-106">Cette liste de vérification souligne les étapes recommandées et fournit une liste de haut niveau des éléments à prendre en compte lorsque vous déployez les fonctionnalités de MBAM.</span><span class="sxs-lookup"><span data-stu-id="1960c-106">This checklist outlines the recommended steps and provides a high-level list of items to consider when you deploy the MBAM features.</span></span> <span data-ttu-id="1960c-107">Nous vous recommandons de copier cette liste de vérification dans un tableur et de la personnaliser en fonction de vos besoins spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1960c-107">We recommend that you copy this checklist into a spreadsheet program and customize it for your specific needs.</span></span>



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
<th align="left"><span data-ttu-id="1960c-108">Tâche</span><span class="sxs-lookup"><span data-stu-id="1960c-108">Task</span></span></th>
<th align="left"><span data-ttu-id="1960c-109">Références</span><span class="sxs-lookup"><span data-stu-id="1960c-109">References</span></span></th>
<th align="left"><span data-ttu-id="1960c-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="1960c-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="1960c-111">Achevez la phase de planification pour préparer l’environnement informatique pour le déploiement de MBAM.</span><span class="sxs-lookup"><span data-stu-id="1960c-111">Complete the planning phase to prepare the computing environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-10-planning-checklist.md" data-raw-source="[MBAM 1.0 Planning Checklist](mbam-10-planning-checklist.md)"><span data-ttu-id="1960c-112">Liste de contrôle de la planification de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="1960c-112">MBAM 1.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="1960c-113">Passez en revue les informations sur les configurations prises en charge par MBAM pour vous assurer que les ordinateurs client et serveur sélectionnés sont pris en charge pour l’installation de la fonctionnalité MBAM.</span><span class="sxs-lookup"><span data-stu-id="1960c-113">Review the information on MBAM supported configurations to make sure that your selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)"><span data-ttu-id="1960c-114">Configurations prises en charge par MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="1960c-114">MBAM 1.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="1960c-115">Exécutez le programme d’installation de MBAM pour déployer les fonctionnalités du serveur MBAM dans l’ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="1960c-115">Run MBAM Setup to deploy MBAM Server features in the following order:</span></span></p>
<ol>
<li><p><span data-ttu-id="1960c-116">Base de données de récupération et de matériel</span><span class="sxs-lookup"><span data-stu-id="1960c-116">Recovery and Hardware Database</span></span></p></li>
<li><p><span data-ttu-id="1960c-117">Base de données état de conformité</span><span class="sxs-lookup"><span data-stu-id="1960c-117">Compliance Status Database</span></span></p></li>
<li><p><span data-ttu-id="1960c-118">Rapports et audit de conformité</span><span class="sxs-lookup"><span data-stu-id="1960c-118">Compliance Audit and Reports</span></span></p></li>
<li><p><span data-ttu-id="1960c-119">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="1960c-119">Administration and Monitoring Server</span></span></p></li>
<li><p><span data-ttu-id="1960c-120">Modèle de stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="1960c-120">MBAM Group Policy Template</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="1960c-121">Remarque</span><span class="sxs-lookup"><span data-stu-id="1960c-121">Note</span></span></strong><br/><p><span data-ttu-id="1960c-122">Assurez le suivi des noms de chaque serveur sur lequel chaque fonctionnalité est installée.</span><span class="sxs-lookup"><span data-stu-id="1960c-122">Keep track of the names of the servers each feature is installed on.</span></span> <span data-ttu-id="1960c-123">Vous utiliserez ces informations tout au long du processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="1960c-123">You will use this information throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-10-server-infrastructure.md" data-raw-source="[Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md)"><span data-ttu-id="1960c-124">Déploiement de l'infrastructure de serveur MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="1960c-124">Deploying the MBAM 1.0 Server Infrastructure</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="1960c-125">Ajoutez des groupes de sécurité des services de domaine Active Directory créés lors de la phase de planification aux groupes d’administrateurs de fonctionnalités de serveur local MBAM appropriés sur les serveurs appropriés.</span><span class="sxs-lookup"><span data-stu-id="1960c-125">Add Active Directory Domain Services security groups created during the planning phase to the appropriate local MBAM Server feature administrators groups on the appropriate servers.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)"><span data-ttu-id="1960c-126">Planification des rôles d’administrateur MBAM 1,0 </a> et <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Comment gérer les rôles d’administrateur MBAM</span><span class="sxs-lookup"><span data-stu-id="1960c-126">Planning for MBAM 1.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="1960c-127">Créez et déployez les objets de stratégie de groupe MBAM requis.</span><span class="sxs-lookup"><span data-stu-id="1960c-127">Create and deploy the required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)"><span data-ttu-id="1960c-128">Déploiement d'objets de stratégie de groupe MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="1960c-128">Deploying MBAM 1.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="1960c-129">Déployez le logiciel client MBAM.</span><span class="sxs-lookup"><span data-stu-id="1960c-129">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)"><span data-ttu-id="1960c-130">Déploiement du client MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="1960c-130">Deploying the MBAM 1.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="1960c-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1960c-131">Related topics</span></span>


[<span data-ttu-id="1960c-132">Déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="1960c-132">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)









