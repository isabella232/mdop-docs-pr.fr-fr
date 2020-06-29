---
title: Vue d'ensemble de la Gestion avancée des stratégies de groupe
description: Vue d'ensemble de la Gestion avancée des stratégies de groupe
author: dansimp
ms.assetid: 2c12f3b4-8472-4c5b-b7f8-1c98a80d6b47
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94e47075ae865096f9fe7d327cc7b11cb54217d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809384"
---
# <span data-ttu-id="b882f-103">Vue d'ensemble de la Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="b882f-103">Overview of Advanced Group Policy Management</span></span>


<span data-ttu-id="b882f-104">Vous pouvez utiliser la gestion de la stratégie de groupe avancée (AGPM) pour étendre les fonctionnalités de la console de gestion des stratégies de groupe (GPMC) afin de fournir un contrôle de modification complet et une gestion améliorée pour les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b882f-104">You can use Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC) to provide comprehensive change control and improved management for Group Policy Objects (GPOs).</span></span>

## <span data-ttu-id="b882f-105">Développement d’objets de stratégie de groupe avec le contrôle des modifications</span><span class="sxs-lookup"><span data-stu-id="b882f-105">Group Policy object development with change control</span></span>


<span data-ttu-id="b882f-106">Avec AGPM, vous pouvez stocker une copie de chaque GPO dans une archive centrale de sorte que les administrateurs de stratégie de groupe puissent l’afficher et le modifier sans affecter immédiatement la version déployée de l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="b882f-106">With AGPM, you can store a copy of each GPO in a central archive so that Group Policy administrators can view and change it offline without immediately affecting the deployed version of the GPO.</span></span> <span data-ttu-id="b882f-107">Par ailleurs, AGPM stocke une copie de chaque version de chaque GPO contrôlé dans l’archive, afin que vous puissiez revenir à une version antérieure si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b882f-107">Additionally, AGPM stores a copy of each version of each controlled GPO in the archive so that you can roll back to an earlier version if necessary.</span></span>

<span data-ttu-id="b882f-108">Les termes «archiver» et «extraire» sont utilisés de la même façon que dans une bibliothèque (ou dans des applications qui fournissent le contrôle de changement, le contrôle de version ou le contrôle de code source pour le développement de programmation).</span><span class="sxs-lookup"><span data-stu-id="b882f-108">The terms "check in" and "check out" are used just as in a library (or in applications that provide change control, version control, or source control for programming development).</span></span> <span data-ttu-id="b882f-109">Pour utiliser un classeur qui se trouve dans une bibliothèque, vous devez le faire à partir de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b882f-109">To use a book that is in a library, you check it out from the library.</span></span> <span data-ttu-id="b882f-110">Personne d’autre ne peut l’utiliser pendant l’extraction. Lorsque vous avez terminé d’utiliser le livre, vous le recochez dans la bibliothèque, afin que d’autres personnes puissent l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="b882f-110">No one else can use it while you have it checked out. When you are finished with the book, you check it back into the library, so others can use it.</span></span>

<span data-ttu-id="b882f-111">Pour utiliser ces fonctionnalités de contrôle d’objet de stratégie de groupe, vous devez cliquer sur un nœud de contrôle de modification dans l’éditeur de gestion des stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="b882f-111">To use these GPO control features, you will click a Change Control node in the Group Policy Management editor.</span></span> <span data-ttu-id="b882f-112">Le nœud de contrôle de modification apparaît uniquement si vous avez installé le client AGPM.</span><span class="sxs-lookup"><span data-stu-id="b882f-112">The Change Control node appears only if you have installed the AGPM Client.</span></span>

<span data-ttu-id="b882f-113">Lorsque vous développez des objets de stratégie de groupe à l’aide d’AGPM:</span><span class="sxs-lookup"><span data-stu-id="b882f-113">When you develop GPOs by using AGPM:</span></span>

1.  <span data-ttu-id="b882f-114">Créer un objet de stratégie de groupe contrôlé ou un contrôle d’objet de stratégie de groupe précédemment non contrôlé.</span><span class="sxs-lookup"><span data-stu-id="b882f-114">Create a new controlled GPO or control a previously uncontrolled GPO.</span></span>

2.  <span data-ttu-id="b882f-115">Consultez l’objet de stratégie de groupe pour pouvoir le modifier.</span><span class="sxs-lookup"><span data-stu-id="b882f-115">Check out the GPO, so that you and only you can change it.</span></span>

3.  <span data-ttu-id="b882f-116">Modifiez l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b882f-116">Edit the GPO.</span></span>

4.  <span data-ttu-id="b882f-117">Archivez l’objet GPO modifié pour permettre aux autres utilisateurs de le modifier ou de le déployer.</span><span class="sxs-lookup"><span data-stu-id="b882f-117">Check in the edited GPO, so that others can change it, or so that it can be deployed.</span></span>

5.  <span data-ttu-id="b882f-118">Passez en revue les modifications.</span><span class="sxs-lookup"><span data-stu-id="b882f-118">Review the changes.</span></span>

6.  <span data-ttu-id="b882f-119">Déploiement de l’objet de stratégie de groupe dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="b882f-119">Deploy the GPO to the production environment.</span></span>

## <span data-ttu-id="b882f-120">Délégation basée sur les rôles</span><span class="sxs-lookup"><span data-stu-id="b882f-120">Role-based delegation</span></span>


<span data-ttu-id="b882f-121">AGPM fournit une délégation complète et facile à utiliser basée sur les rôles pour gérer l’accès aux objets de stratégie de groupe dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="b882f-121">AGPM provides comprehensive, easy-to-use role-based delegation for managing access to GPOs in the archive.</span></span> <span data-ttu-id="b882f-122">Les autorisations au niveau du domaine permettent aux administrateurs d’AGPM d’offrir un accès aux domaines individuels sans avoir accès à d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="b882f-122">Domain-level permissions enable AGPM Administrators to provide access to individual domains without providing access to other domains.</span></span> <span data-ttu-id="b882f-123">La délégation basée sur un ensemble d’objets permet aux administrateurs d’AGPM d’offrir un accès à des objets de stratégie de groupe spécifiques sans fournir un accès à l’échelle du domaine</span><span class="sxs-lookup"><span data-stu-id="b882f-123">GPO-based delegation enables AGPM Administrators to provide access to specific GPOs without providing domain-wide access.</span></span>

<span data-ttu-id="b882f-124">Dans AGPM, il existe des rôles spécifiquement définis: Administrateur AGPM (contrôle total), approbateur, éditeur et relecteur.</span><span class="sxs-lookup"><span data-stu-id="b882f-124">Within AGPM, there are specifically defined roles: AGPM Administrator (Full Control), Approver, Editor, and Reviewer.</span></span> <span data-ttu-id="b882f-125">Le rôle d’administrateur AGPM inclut les autorisations pour tous les autres rôles.</span><span class="sxs-lookup"><span data-stu-id="b882f-125">The AGPM Administrator role includes the permissions for all other roles.</span></span> <span data-ttu-id="b882f-126">Par défaut, seuls les approbateurs ont la possibilité de déployer des objets de stratégie de groupe dans l’environnement de production d’un domaine, en protégeant l’environnement contre les erreurs, par des éditeurs moins expérimentés.</span><span class="sxs-lookup"><span data-stu-id="b882f-126">By default, only Approvers have the power to deploy GPOs to the production environment of a domain, protecting the environment from mistakes by less experienced Editors.</span></span> <span data-ttu-id="b882f-127">Par défaut, tous les rôles incluent le rôle de réviseur et par conséquent la possibilité d’afficher les paramètres de l’objet de stratégie de groupe dans les États.</span><span class="sxs-lookup"><span data-stu-id="b882f-127">Also by default, all roles include the Reviewer role and therefore the ability to view GPO settings in reports.</span></span> <span data-ttu-id="b882f-128">Néanmoins, AGPM fournit à un administrateur AGPM la possibilité de personnaliser l’accès à l’objet de stratégie de groupe pour l’adapter aux besoins de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b882f-128">However, AGPM provides an AGPM Administrator with the flexibility to customize GPO access to fit the needs of your organization.</span></span>

## <span data-ttu-id="b882f-129">Délégation dans un environnement d’administration de stratégie de groupe multiples</span><span class="sxs-lookup"><span data-stu-id="b882f-129">Delegation in a multiple Group Policy administrator environment</span></span>


<span data-ttu-id="b882f-130">Dans un environnement dans lequel plusieurs personnes changent d’objets de stratégie de groupe, un administrateur d’AGPM délègue l’autorisation aux réviseurs, aux approbateurs et aux réviseurs en tant que groupes ou personnes.</span><span class="sxs-lookup"><span data-stu-id="b882f-130">In an environment where multiple people change GPOs, an AGPM Administrator delegates permission to Editors, Approvers, and Reviewers, either as groups or as individuals.</span></span> <span data-ttu-id="b882f-131">Pour un processus de développement d’objet GPO standard pour un éditeur et un approbateur, voir [liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe](checklist-create-edit-and-deploy-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="b882f-131">For a typical GPO development process for an Editor and an Approver, see [Checklist: Create, Edit, and Deploy a GPO](checklist-create-edit-and-deploy-a-gpo-agpm40.md).</span></span>

### <span data-ttu-id="b882f-132">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="b882f-132">Additional references</span></span>

-   [<span data-ttu-id="b882f-133">Gestion avancée des stratégies de groupe4.0</span><span class="sxs-lookup"><span data-stu-id="b882f-133">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





