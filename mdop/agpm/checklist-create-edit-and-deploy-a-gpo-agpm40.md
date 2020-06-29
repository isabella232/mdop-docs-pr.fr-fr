---
title: 'Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe'
description: 'Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe'
author: dansimp
ms.assetid: 44631bed-16d2-4b5a-af70-17a73fb5f6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d8bea9109040aa81a20df62356ef1d307d5eac0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807773"
---
# <span data-ttu-id="c9c82-103">Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c9c82-103">Checklist: Create, Edit, and Deploy a GPO</span></span>


<span data-ttu-id="c9c82-104">Dans un environnement dans lequel plusieurs personnes modifient les objets de stratégie de groupe (GPO) en utilisant la gestion avancée des stratégies de groupe (AGPM), un administrateur AGPM (contrôle total) délègue les autorisations à des éditeurs, approbateurs et réviseurs en tant que groupes ou personnes.</span><span class="sxs-lookup"><span data-stu-id="c9c82-104">In an environment where multiple people change Group Policy Objects (GPOs) by using Advanced Group Policy Management (AGPM), an AGPM Administrator (Full Control) delegates permission to Editors, Approvers, and Reviewers either as groups or as individuals.</span></span> <span data-ttu-id="c9c82-105">Vous trouverez ci-après un processus standard de développement d’objets de stratégie de groupe pour un éditeur et un approbateur.</span><span class="sxs-lookup"><span data-stu-id="c9c82-105">The following is a typical GPO development process for an Editor and an Approver.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c9c82-106">Tâche</span><span class="sxs-lookup"><span data-stu-id="c9c82-106">Task</span></span></th>
<th align="left"><span data-ttu-id="c9c82-107">Référence</span><span class="sxs-lookup"><span data-stu-id="c9c82-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9c82-108">L’éditeur demande la création d’un objet de stratégie de groupe ou l’approbation d’un nouvel objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c9c82-108">Editor requests that a new GPO be created or an Approver creates a new GPO.</span></span></p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm40.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm40.md)"><span data-ttu-id="c9c82-109">Demander la création d'un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="c9c82-109">Request the Creation of a New Controlled GPO</span></span></a></p>
<p><a href="create-a-new-controlled-gpo-agpm40.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md)"><span data-ttu-id="c9c82-110">Créer un objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="c9c82-110">Create a New Controlled GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9c82-111">L’Approbateur approuve la création de l’objet de stratégie de groupe s’il a été demandé par un éditeur.</span><span class="sxs-lookup"><span data-stu-id="c9c82-111">Approver approves the creation of the GPO if it was requested by an Editor.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)"><span data-ttu-id="c9c82-112">Approuver ou rejeter une action en attente</span><span class="sxs-lookup"><span data-stu-id="c9c82-112">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9c82-113">L’éditeur récupère une copie de l’objet de stratégie de groupe à partir de l’archive afin que personne d’autre ne puisse modifier l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="c9c82-113">Editor checks out a copy of the GPO from the archive so that no one else can modify the GPO.</span></span> <span data-ttu-id="c9c82-114">L’éditeur apporte des modifications à l’objet GPO, puis vérifie l’objet GPO modifié dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="c9c82-114">Editor makes changes to the GPO, and then checks the modified GPO into the archive.</span></span></p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm40.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm40.md)"><span data-ttu-id="c9c82-115">Modifier un objet de stratégie de groupe hors connexion</span><span class="sxs-lookup"><span data-stu-id="c9c82-115">Edit a GPO Offline</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9c82-116">Si vous développez dans une forêt de test, l’éditeur exporte l’objet GPO vers un fichier, transfère le fichier dans la forêt de production et importe le fichier.</span><span class="sxs-lookup"><span data-stu-id="c9c82-116">If developing in a test forest, Editor exports the GPO to a file, transfers the file to the production forest, and imports the file.</span></span> <span data-ttu-id="c9c82-117">Par ailleurs, un éditeur peut lier l’objet de stratégie de groupe à une unité d’organisation qui contient des ordinateurs et des utilisateurs de test.</span><span class="sxs-lookup"><span data-stu-id="c9c82-117">Additionally, an Editor can link the GPO to an organizational unit that contains test computers and users.</span></span></p></td>
<td align="left"><p><a href="using-a-test-environment.md" data-raw-source="[Using a Test Environment](using-a-test-environment.md)"><span data-ttu-id="c9c82-118">Utilisation d'un environnement de test</span><span class="sxs-lookup"><span data-stu-id="c9c82-118">Using a Test Environment</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9c82-119">L’éditeur demande le déploiement de l’objet de stratégie de groupe dans l’environnement de production du domaine.</span><span class="sxs-lookup"><span data-stu-id="c9c82-119">Editor requests deployment of the GPO to the production environment of the domain.</span></span></p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm40.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm40.md)"><span data-ttu-id="c9c82-120">Demander le déploiement d'un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c9c82-120">Request Deployment of a GPO</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9c82-121">Les réviseurs, tels que les approbateurs ou les éditeurs, analysent l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c9c82-121">Reviewers, such as Approvers or Editors, analyze the GPO.</span></span></p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm40.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md)"><span data-ttu-id="c9c82-122">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="c9c82-122">Performing Reviewer Tasks</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9c82-123">L’Approbateur approuve et déploie l’objet de stratégie de groupe dans l’environnement de production du domaine ou rejeter l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c9c82-123">Approver approves and deploys the GPO to the production environment of the domain or rejects the GPO.</span></span></p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)"><span data-ttu-id="c9c82-124">Approuver ou rejeter une action en attente</span><span class="sxs-lookup"><span data-stu-id="c9c82-124">Approve or Reject a Pending Action</span></span></a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c9c82-125">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="c9c82-125">Additional references</span></span>

[<span data-ttu-id="c9c82-126">Gestion avancée des stratégies de groupe4.0</span><span class="sxs-lookup"><span data-stu-id="c9c82-126">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





