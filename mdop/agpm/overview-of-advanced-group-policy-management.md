---
title: Vue d'ensemble de la Gestion avancée des stratégies de groupe
description: Vue d'ensemble de la Gestion avancée des stratégies de groupe
author: dansimp
ms.assetid: 028de9dd-848b-42bc-a982-65ba5c433772
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38396de6bd8bdace72d3add1bba09769ae26de32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809383"
---
# <span data-ttu-id="9fd3c-103">Vue d'ensemble de la Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="9fd3c-103">Overview of Advanced Group Policy Management</span></span>


<span data-ttu-id="9fd3c-104">Vous pouvez utiliser la gestion de la stratégie de groupe avancée (AGPM) pour étendre les fonctionnalités de la console de gestion des stratégies de groupe (GPMC), en fournissant un contrôle complet et une gestion améliorée pour les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-104">You can use Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC), providing comprehensive change control and enhanced management for Group Policy objects (GPOs).</span></span>

## <span data-ttu-id="9fd3c-105">Développement d’objets de stratégie de groupe avec le contrôle des modifications</span><span class="sxs-lookup"><span data-stu-id="9fd3c-105">Group Policy object development with change control</span></span>


<span data-ttu-id="9fd3c-106">Avec AGPM, vous pouvez stocker une copie de chaque GPO dans une archive centrale de sorte que les administrateurs de stratégie de groupe puissent l’afficher et le modifier sans préjudice de la version déployée de l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-106">With AGPM, you can store a copy of each GPO in a central archive, so Group Policy administrators can view and modify it offline without immediately impacting the deployed version of the GPO.</span></span> <span data-ttu-id="9fd3c-107">Par ailleurs, AGPM stocke une copie de chaque version de chaque GPO contrôlé dans l’archive, afin que vous puissiez revenir à une version antérieure si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-107">Additionally, AGPM stores a copy of each version of each controlled GPO in the archive so that you can roll back to an earlier version if needed.</span></span>

<span data-ttu-id="9fd3c-108">Les termes «archiver» et «extraire» sont utilisés de la même manière que dans une bibliothèque (ou dans des applications qui fournissent un contrôle de modification, le contrôle de version ou le contrôle de code source pour le développement de programmation).</span><span class="sxs-lookup"><span data-stu-id="9fd3c-108">The terms "check in" and "check out" are used in much the same way as in a library (or in applications that provide change control, version control, or source code control for programming development).</span></span> <span data-ttu-id="9fd3c-109">Pour utiliser un classeur qui se trouve dans une bibliothèque, vous devez le faire à partir de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-109">To use a book that is in a library, you check it out from the library.</span></span> <span data-ttu-id="9fd3c-110">Personne d’autre ne peut l’utiliser pendant l’extraction. Lorsque vous avez terminé d’utiliser le livre, vous le recochez dans la bibliothèque, afin que d’autres personnes puissent l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-110">No one else can use it while you have it checked out. When you are finished with the book, you check it back into the library, so others can use it.</span></span>

<span data-ttu-id="9fd3c-111">Lors du développement d’objets de stratégie de groupe avec AGPM:</span><span class="sxs-lookup"><span data-stu-id="9fd3c-111">When developing GPOs using AGPM:</span></span>

1.  <span data-ttu-id="9fd3c-112">Créer un objet de stratégie de groupe contrôlé ou un contrôle d’objet de stratégie de groupe précédemment non contrôlé.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-112">Create a new controlled GPO or control a previously uncontrolled GPO.</span></span>

2.  <span data-ttu-id="9fd3c-113">Consultez l’objet de stratégie de groupe pour vous permettre de le modifier.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-113">Check out the GPO, so you and only you can modify it.</span></span>

3.  <span data-ttu-id="9fd3c-114">Modifiez l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-114">Edit the GPO.</span></span>

4.  <span data-ttu-id="9fd3c-115">Archivez l’objet GPO modifié pour permettre aux autres utilisateurs de le modifier ou de le déployer.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-115">Check in the edited GPO, so others can modify it, or so it can be deployed.</span></span>

5.  <span data-ttu-id="9fd3c-116">Passez en revue les modifications.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-116">Review the changes.</span></span>

6.  <span data-ttu-id="9fd3c-117">Déploiement de l’objet de stratégie de groupe dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-117">Deploy the GPO to the production environment.</span></span>

## <span data-ttu-id="9fd3c-118">Délégation basée sur les rôles</span><span class="sxs-lookup"><span data-stu-id="9fd3c-118">Role-based delegation</span></span>


<span data-ttu-id="9fd3c-119">AGPM fournit une délégation basée sur les rôles complète et facile à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-119">AGPM provides comprehensive, easy-to-use role-based delegation.</span></span> <span data-ttu-id="9fd3c-120">Les autorisations au niveau du domaine permettent aux administrateurs d’AGPM de fournir l’accès à des domaines individuels sans permettre l’accès à d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-120">Domain-level permissions allow AGPM Administrators to provide access to individual domains without providing access to other domains.</span></span> <span data-ttu-id="9fd3c-121">La délégation basée sur les objets de stratégie de groupe permet aux administrateurs d’AGPM d’autoriser l’accès à des objets GPO spécifiques.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-121">GPO-based delegation enables AGPM Administrators to allow access only to specific GPOs.</span></span>

<span data-ttu-id="9fd3c-122">Dans AGPM, il existe des rôles spécifiquement définis: Administrateur AGPM (contrôle total), approbateur, éditeur et relecteur.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-122">Within AGPM, there are specifically defined roles: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="9fd3c-123">Le rôle d’administrateur AGPM inclut les autorisations pour tous les autres rôles.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-123">The AGPM Administrator role includes the permissions for all other roles.</span></span> <span data-ttu-id="9fd3c-124">Par défaut, seuls les approbateurs ont la possibilité de déployer des objets de stratégie de groupe dans l’environnement de production, en protégeant l’environnement contre les erreurs fortuites par des éditeurs moins expérimentés.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-124">By default, only Approvers have the power to deploy GPOs to the production environment, protecting the environment from inadvertent mistakes by less experienced Editors.</span></span> <span data-ttu-id="9fd3c-125">Par défaut, tous les rôles incluent le rôle de réviseur et par conséquent la possibilité d’afficher les paramètres de l’objet de stratégie de groupe dans les États.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-125">Also by default, all roles include the Reviewer role and therefore the ability to view GPO settings in reports.</span></span> <span data-ttu-id="9fd3c-126">Néanmoins, AGPM fournit à un administrateur AGPM la possibilité de personnaliser l’accès à l’objet de stratégie de groupe pour l’adapter aux besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-126">However, AGPM provides an AGPM Administrator with the flexibility to customize GPO access to fit the needs of your organization.</span></span>

## <span data-ttu-id="9fd3c-127">Délégation dans un environnement d’administration de stratégie de groupe multiples</span><span class="sxs-lookup"><span data-stu-id="9fd3c-127">Delegation in a multiple Group Policy administrator environment</span></span>


<span data-ttu-id="9fd3c-128">Dans un environnement dans lequel plusieurs personnes apportent des modifications à des objets de stratégie de groupe, un administrateur AGPM délègue l’autorisation aux réviseurs, aux approbateurs et aux réviseurs en tant que groupes ou personnes.</span><span class="sxs-lookup"><span data-stu-id="9fd3c-128">In an environment where multiple people make changes to GPOs, an AGPM Administrator delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="9fd3c-129">Pour un processus de développement d’objet GPO standard pour un éditeur et un approbateur, voir [liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe](checklist-create-edit-and-deploy-a-gpo.md).</span><span class="sxs-lookup"><span data-stu-id="9fd3c-129">For a typical GPO development process for an Editor and an Approver, see [Checklist: Create, Edit, and Deploy a GPO](checklist-create-edit-and-deploy-a-gpo.md).</span></span>

### <span data-ttu-id="9fd3c-130">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9fd3c-130">Additional references</span></span>

-   [<span data-ttu-id="9fd3c-131">Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="9fd3c-131">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo.md)

-   [<span data-ttu-id="9fd3c-132">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="9fd3c-132">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

-   [<span data-ttu-id="9fd3c-133">Exécution de tâches d'éditeur</span><span class="sxs-lookup"><span data-stu-id="9fd3c-133">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

-   [<span data-ttu-id="9fd3c-134">Exécution de tâches d'approbateur</span><span class="sxs-lookup"><span data-stu-id="9fd3c-134">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="9fd3c-135">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="9fd3c-135">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

-   [<span data-ttu-id="9fd3c-136">Résolution des problèmes de la Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="9fd3c-136">Troubleshooting Advanced Group Policy Management</span></span>](troubleshooting-advanced-group-policy-management.md)

-   [<span data-ttu-id="9fd3c-137">Interface utilisateur: gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="9fd3c-137">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management.md)

 

 





