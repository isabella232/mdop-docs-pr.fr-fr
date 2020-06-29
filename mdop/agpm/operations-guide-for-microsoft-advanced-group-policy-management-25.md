---
title: Guide des opérations de la Gestion avancée des stratégies de groupe Microsoft2.5
description: Guide des opérations de la Gestion avancée des stratégies de groupe Microsoft2.5
author: dansimp
ms.assetid: 005f0bb5-789f-42a9-bcaf-7e8c31a8df66
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c0ae04e0e8dcf62d3ea840de28a9248827ec62e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809401"
---
# <span data-ttu-id="4bc07-103">Guide des opérations de la Gestion avancée des stratégies de groupe Microsoft2.5</span><span class="sxs-lookup"><span data-stu-id="4bc07-103">Operations Guide for Microsoft Advanced Group Policy Management 2.5</span></span>


<span data-ttu-id="4bc07-104">Vous pouvez utiliser Microsoft Advanced Group Policy Management (AGPM) pour étendre les fonctionnalités de la console de gestion des stratégies de groupe (GPMC), en fournissant un contrôle de modification complet et une gestion améliorée pour les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4bc07-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy objects (GPOs).</span></span>

<span data-ttu-id="4bc07-105">Avec AGPM, vous pouvez:</span><span class="sxs-lookup"><span data-stu-id="4bc07-105">With AGPM you can:</span></span>

-   <span data-ttu-id="4bc07-106">Effectuer une modification hors connexion des objets de stratégie de groupe pour pouvoir les créer et les tester avant de procéder au déploiement dans un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="4bc07-106">Perform offline editing of GPOs, so you can create and test them before deploying to a production environment.</span></span>

-   <span data-ttu-id="4bc07-107">Conserver plusieurs versions d’un objet de stratégie de groupe dans une archive centrale, de sorte que vous puissiez revenir en arrière en cas de problème.</span><span class="sxs-lookup"><span data-stu-id="4bc07-107">Retain multiple versions of a GPO in a central archive, so you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="4bc07-108">Partager la responsabilité de la modification, de l’approbation et de l’examen d’objets de stratégie de groupe auprès de plusieurs personnes par le biais d’une délégation basée sur les rôles.</span><span class="sxs-lookup"><span data-stu-id="4bc07-108">Share the responsibility for editing, approving, and reviewing GPOs among multiple people using role-based delegation.</span></span>

-   <span data-ttu-id="4bc07-109">Éliminez le risque que les administrateurs de stratégie de groupe ne remplacent chacun d’eux à l’aide d’une fonctionnalité d’archivage/extraction pour les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4bc07-109">Eliminate the danger of multiple Group Policy administrators overwriting each other's work by using a check-in/check-out capability for GPOs.</span></span>

-   <span data-ttu-id="4bc07-110">Analysez les modifications apportées à un objet GPO en le comparant à un autre ou à une autre version du même objet de stratégie de groupe avec le rapport de différences.</span><span class="sxs-lookup"><span data-stu-id="4bc07-110">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO using difference reporting.</span></span>

-   <span data-ttu-id="4bc07-111">Simplifiez la création de nouveaux objets de stratégie de groupe à l’aide de modèles d’objets de stratégie de groupe, en stockant les paramètres standard à utiliser comme points de départ pour les nouveaux</span><span class="sxs-lookup"><span data-stu-id="4bc07-111">Simplify the creation of new GPOs by using GPO templates, storing standard settings to use as starting points for new GPOs.</span></span>

<span data-ttu-id="4bc07-112">AGPM ajoute un nœud de **contrôle de modification** sous chaque domaine affiché dans la console GPMC, ainsi que les onglets **historique** et **Extensions** pour chaque lien d’objet de stratégie de groupe affiché dans la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="4bc07-112">AGPM adds a **Change Control** node under each domain displayed in the GPMC, as well as **History** and **Extensions** tabs for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="4bc07-113">Vue d'ensemble de la Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="4bc07-113">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management.md)

-   [<span data-ttu-id="4bc07-114">Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="4bc07-114">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo.md)

-   [<span data-ttu-id="4bc07-115">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="4bc07-115">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

-   [<span data-ttu-id="4bc07-116">Exécution de tâches d'éditeur</span><span class="sxs-lookup"><span data-stu-id="4bc07-116">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

-   [<span data-ttu-id="4bc07-117">Exécution de tâches d'approbateur</span><span class="sxs-lookup"><span data-stu-id="4bc07-117">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="4bc07-118">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="4bc07-118">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

-   [<span data-ttu-id="4bc07-119">Résolution des problèmes de la Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="4bc07-119">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management.md)

-   [<span data-ttu-id="4bc07-120">Interface utilisateur: gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="4bc07-120">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management.md)

 

 





