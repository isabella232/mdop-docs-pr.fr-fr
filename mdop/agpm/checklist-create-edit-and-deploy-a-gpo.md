---
title: 'Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe'
description: 'Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe'
author: dansimp
ms.assetid: 614e2d9a-c18b-4f62-99fd-e17a2ac8559d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c79fefaa65c138372ebee00b769ccc5243142e22
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807777"
---
# <span data-ttu-id="50519-103">Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="50519-103">Checklist: Create, Edit, and Deploy a GPO</span></span>


<span data-ttu-id="50519-104">Dans un environnement dans lequel plusieurs personnes apportent des modifications à des objets de stratégie de groupe (GPO), un administrateur d’AGPM (contrôle total) délègue l’autorisation aux réviseurs, aux approbateurs et aux réviseurs, en tant que groupes ou personnes.</span><span class="sxs-lookup"><span data-stu-id="50519-104">In an environment where multiple people make changes to Group Policy objects (GPOs), an AGPM Administrator (Full Control) delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="50519-105">Vous trouverez ci-après un processus standard de développement d’objets de stratégie de groupe pour un éditeur et un approbateur.</span><span class="sxs-lookup"><span data-stu-id="50519-105">The following is a typical GPO development process for an Editor and an Approver.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="50519-106">Tâche</span><span class="sxs-lookup"><span data-stu-id="50519-106">Task</span></span></th>
<th align="left"><span data-ttu-id="50519-107">Référence</span><span class="sxs-lookup"><span data-stu-id="50519-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50519-108">L’éditeur demande la création d’un nouvel objet de stratégie de groupe ou d’un approbateur qui crée un nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="50519-108">Editor requests the creation of a new GPO or an Approver creates a new GPO.</span></span></p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo.md)"><span data-ttu-id="50519-109">Demander la création d'un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="50519-109">Request the Creation of a New Controlled GPO</span></span></a></p>
<p><a href="create-a-new-controlled-gpo.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo.md)"><span data-ttu-id="50519-110">Créer un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="50519-110">Create a New Controlled GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50519-111">L’Approbateur approuve la création de l’objet de stratégie de groupe s’il a été demandé par un éditeur.</span><span class="sxs-lookup"><span data-stu-id="50519-111">Approver approves the creation of the GPO if it was requested by an Editor.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action.md)"><span data-ttu-id="50519-112">Approuver ou rejeter une action en attente</span><span class="sxs-lookup"><span data-stu-id="50519-112">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50519-113">L’éditeur récupère une copie de l’objet de stratégie de groupe à partir de l’archive, de sorte que personne d’autre ne puisse modifier l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="50519-113">Editor checks out a copy of the GPO from the archive, so no one else can modify the GPO.</span></span> <span data-ttu-id="50519-114">L’éditeur apporte des modifications à l’objet GPO, puis vérifie l’objet GPO modifié dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="50519-114">Editor makes changes to the GPO, and then checks the modified GPO into the archive.</span></span></p></td>
<td align="left"><p><a href="edit-a-gpo-offline.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline.md)"><span data-ttu-id="50519-115">Modifier un objet de stratégie de groupe hors connexion</span><span class="sxs-lookup"><span data-stu-id="50519-115">Edit a GPO Offline</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50519-116">L’éditeur demande le déploiement de l’objet de stratégie de groupe dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="50519-116">Editor requests deployment of the GPO to the production environment.</span></span></p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo.md)"><span data-ttu-id="50519-117">Demander le déploiement d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="50519-117">Request Deployment of a GPO</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="50519-118">Les réviseurs, tels que les approbateurs ou les éditeurs, analysent l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="50519-118">Reviewers, such as Approvers or Editors, analyze the GPO.</span></span></p></td>
<td align="left"><p><a href="performing-reviewer-tasks.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks.md)"><span data-ttu-id="50519-119">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="50519-119">Performing Reviewer Tasks</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="50519-120">L’Approbateur approuve et déploie l’objet de stratégie de groupe dans l’environnement de production ou refuse l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="50519-120">Approver approves and deploys the GPO to the production environment or rejects the GPO.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action.md)"><span data-ttu-id="50519-121">Approuver ou rejeter une action en attente</span><span class="sxs-lookup"><span data-stu-id="50519-121">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





