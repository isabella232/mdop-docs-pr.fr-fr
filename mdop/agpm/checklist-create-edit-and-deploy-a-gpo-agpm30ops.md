---
title: 'Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe'
description: 'Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe'
author: dansimp
ms.assetid: a7a17706-304a-4455-9ada-52508ec620f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 35255926ba2384e2942900fc30eae06a30049a15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807774"
---
# <span data-ttu-id="9705e-103">Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="9705e-103">Checklist: Create, Edit, and Deploy a GPO</span></span>


<span data-ttu-id="9705e-104">Dans un environnement dans lequel plusieurs personnes apportent des modifications à des objets de stratégie de groupe en utilisant une gestion avancée de la stratégie de groupe (AGPM), un administrateur AGPM (contrôle total) délègue l’autorisation aux réviseurs, aux approbateurs et aux réviseurs en tant que groupes ou personnes.</span><span class="sxs-lookup"><span data-stu-id="9705e-104">In an environment where multiple people make changes to Group Policy Objects (GPOs) using Advanced Group Policy Management (AGPM), an AGPM Administrator (Full Control) delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="9705e-105">Vous trouverez ci-après un processus standard de développement d’objets de stratégie de groupe pour un éditeur et un approbateur.</span><span class="sxs-lookup"><span data-stu-id="9705e-105">The following is a typical GPO development process for an Editor and an Approver.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9705e-106">Tâche</span><span class="sxs-lookup"><span data-stu-id="9705e-106">Task</span></span></th>
<th align="left"><span data-ttu-id="9705e-107">Référence</span><span class="sxs-lookup"><span data-stu-id="9705e-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9705e-108">L’éditeur demande la création d’un nouvel objet de stratégie de groupe ou d’un approbateur qui crée un nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="9705e-108">Editor requests the creation of a new GPO or an Approver creates a new GPO.</span></span></p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm30ops.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm30ops.md)"><span data-ttu-id="9705e-109">Demander la création d'un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="9705e-109">Request the Creation of a New Controlled GPO</span></span></a></p>
<p><a href="create-a-new-controlled-gpo-agpm30ops.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm30ops.md)"><span data-ttu-id="9705e-110">Créer un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="9705e-110">Create a New Controlled GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9705e-111">L’Approbateur approuve la création de l’objet de stratégie de groupe s’il a été demandé par un éditeur.</span><span class="sxs-lookup"><span data-stu-id="9705e-111">Approver approves the creation of the GPO if it was requested by an Editor.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm30ops.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm30ops.md)"><span data-ttu-id="9705e-112">Approuver ou rejeter une action en attente</span><span class="sxs-lookup"><span data-stu-id="9705e-112">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9705e-113">L’éditeur récupère une copie de l’objet de stratégie de groupe à partir de l’archive, de sorte que personne d’autre ne puisse modifier l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="9705e-113">Editor checks out a copy of the GPO from the archive, so no one else can modify the GPO.</span></span> <span data-ttu-id="9705e-114">L’éditeur apporte des modifications à l’objet GPO, puis vérifie l’objet GPO modifié dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="9705e-114">Editor makes changes to the GPO, and then checks the modified GPO into the archive.</span></span></p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm30ops.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm30ops.md)"><span data-ttu-id="9705e-115">Modifier un objet de stratégie de groupe hors connexion</span><span class="sxs-lookup"><span data-stu-id="9705e-115">Edit a GPO Offline</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9705e-116">L’éditeur demande le déploiement de l’objet de stratégie de groupe dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="9705e-116">Editor requests deployment of the GPO to the production environment.</span></span></p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm30ops.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm30ops.md)"><span data-ttu-id="9705e-117">Demander le déploiement d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="9705e-117">Request Deployment of a GPO</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9705e-118">Les réviseurs, tels que les approbateurs ou les éditeurs, analysent l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="9705e-118">Reviewers, such as Approvers or Editors, analyze the GPO.</span></span></p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm30ops.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm30ops.md)"><span data-ttu-id="9705e-119">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="9705e-119">Performing Reviewer Tasks</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9705e-120">L’Approbateur approuve et déploie l’objet de stratégie de groupe dans l’environnement de production ou refuse l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="9705e-120">Approver approves and deploys the GPO to the production environment or rejects the GPO.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm30ops.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm30ops.md)"><span data-ttu-id="9705e-121">Approuver ou rejeter une action en attente</span><span class="sxs-lookup"><span data-stu-id="9705e-121">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="9705e-122">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9705e-122">Additional references</span></span>

[<span data-ttu-id="9705e-123">Guide des opérations de la Gestion avancée des stratégies de groupe Microsoft3.0</span><span class="sxs-lookup"><span data-stu-id="9705e-123">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





