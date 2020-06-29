---
title: Liste de contrôle du déploiement de MBAM2.0
description: Liste de contrôle du déploiement de MBAM2.0
author: dansimp
ms.assetid: 7905d31d-f21c-4683-b9c4-95b815e08fab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d8d0ce1a3ff48d4bf2f84e61b4a578b170264a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811754"
---
# <span data-ttu-id="ab714-103">Liste de contrôle du déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="ab714-103">MBAM 2.0 Deployment Checklist</span></span>


<span data-ttu-id="ab714-104">Cette liste de vérification peut être utilisée pour vous aider lors du déploiement de Microsoft BitLocker administration et de la surveillance (MBAM) avec une topologie autonome.</span><span class="sxs-lookup"><span data-stu-id="ab714-104">This checklist can be used to help you during Microsoft BitLocker Administration and Monitoring (MBAM) deployment with a Stand-alone topology.</span></span>

**<span data-ttu-id="ab714-105">Remarque</span><span class="sxs-lookup"><span data-stu-id="ab714-105">Note</span></span>**  
<span data-ttu-id="ab714-106">Cette liste de vérification décrit les étapes recommandées et une liste générale des éléments à prendre en compte lors du déploiement des fonctionnalités d’administration et de surveillance de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ab714-106">This checklist outlines the recommended steps and a high-level list of items to consider when deploying Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="ab714-107">Il est recommandé de copier cette liste de vérification dans un tableur et de la personnaliser pour votre utilisation.</span><span class="sxs-lookup"><span data-stu-id="ab714-107">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



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
<th align="left"><span data-ttu-id="ab714-108">Tâche</span><span class="sxs-lookup"><span data-stu-id="ab714-108">Task</span></span></th>
<th align="left"><span data-ttu-id="ab714-109">Références</span><span class="sxs-lookup"><span data-stu-id="ab714-109">References</span></span></th>
<th align="left"><span data-ttu-id="ab714-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="ab714-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ab714-111">Achevez la phase de planification pour préparer l’environnement informatique pour le déploiement de MBAM.</span><span class="sxs-lookup"><span data-stu-id="ab714-111">Complete the planning phase to prepare the computing environment for MBAM deployment.</span></span></p></td>
<td align="left"><p><a href="mbam-20-planning-checklist-mbam-2.md" data-raw-source="[MBAM 2.0 Planning Checklist](mbam-20-planning-checklist-mbam-2.md)"><span data-ttu-id="ab714-112">Liste de contrôle de la planification de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="ab714-112">MBAM 2.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ab714-113">Passez en revue les informations de configurations prises en charge par MBAM pour vous assurer que les ordinateurs client et serveur sélectionnés sont pris en charge pour l’installation de la fonctionnalité MBAM.</span><span class="sxs-lookup"><span data-stu-id="ab714-113">Review the MBAM supported configurations information to make sure selected client and server computers are supported for MBAM feature installation.</span></span></p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)"><span data-ttu-id="ab714-114">Configurations prises en charge par MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="ab714-114">MBAM 2.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ab714-115">Exécutez le programme d’installation de MBAM pour déployer les fonctionnalités du serveur MBAM dans l’ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="ab714-115">Run MBAM Setup to deploy MBAM Server features in the following order:</span></span></p>
<ol>
<li><p><span data-ttu-id="ab714-116">Base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="ab714-116">Recovery Database</span></span></p></li>
<li><p><span data-ttu-id="ab714-117">Base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="ab714-117">Compliance and Audit Database</span></span></p></li>
<li><p><span data-ttu-id="ab714-118">Rapports et audit de conformité</span><span class="sxs-lookup"><span data-stu-id="ab714-118">Compliance Audit and Reports</span></span></p></li>
<li><p><span data-ttu-id="ab714-119">Serveur libre-service</span><span class="sxs-lookup"><span data-stu-id="ab714-119">Self-Service Server</span></span></p></li>
<li><p><span data-ttu-id="ab714-120">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="ab714-120">Administration and Monitoring Server</span></span></p></li>
<li><p><span data-ttu-id="ab714-121">Modèle de stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="ab714-121">MBAM Group Policy template</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="ab714-122">Remarque</span><span class="sxs-lookup"><span data-stu-id="ab714-122">Note</span></span></strong><br/><p><span data-ttu-id="ab714-123">Assurez le suivi des noms de chaque serveur sur lequel chaque fonctionnalité est installée.</span><span class="sxs-lookup"><span data-stu-id="ab714-123">Keep track of the names of the servers each feature is installed on.</span></span> <span data-ttu-id="ab714-124">Ces informations seront utilisées tout au long du processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="ab714-124">This information will be used throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-20-server-infrastructure-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md)"><span data-ttu-id="ab714-125">Déploiement de l'infrastructure de serveur MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="ab714-125">Deploying the MBAM 2.0 Server Infrastructure</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ab714-126">Ajoutez des groupes de sécurité des services de domaine Active Directory créés lors de la phase de planification aux groupes d’administrateurs de fonctionnalités de serveur local MBAM appropriés sur les serveurs appropriés.</span><span class="sxs-lookup"><span data-stu-id="ab714-126">Add Active Directory Domain Services security groups created during the planning phase to the appropriate local MBAM Server feature administrators groups on appropriate servers.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="ab714-127">Planification des rôles d’administrateur MBAM 2,0 </a> et <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Comment gérer les rôles d’administrateur MBAM</span><span class="sxs-lookup"><span data-stu-id="ab714-127">Planning for MBAM 2.0 Administrator Roles</a> and <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)">How to Manage MBAM Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ab714-128">Créer et déployer des objets de stratégie de groupe MBAM requis.</span><span class="sxs-lookup"><span data-stu-id="ab714-128">Create and deploy required MBAM Group Policy Objects.</span></span></p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)"><span data-ttu-id="ab714-129">Déploiement d'objets de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="ab714-129">Deploying MBAM 2.0 Group Policy Objects</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="ab714-130">Déployez le logiciel client MBAM.</span><span class="sxs-lookup"><span data-stu-id="ab714-130">Deploy the MBAM Client software.</span></span></p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)"><span data-ttu-id="ab714-131">Déploiement du client MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="ab714-131">Deploying the MBAM 2.0 Client</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="ab714-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ab714-132">Related topics</span></span>


[<span data-ttu-id="ab714-133">Déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="ab714-133">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)









