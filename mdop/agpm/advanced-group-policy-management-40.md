---
title: Gestion avancée des stratégies de groupe4.0
description: Gestion avancée des stratégies de groupe4.0
author: dansimp
ms.assetid: 9873a1f7-97fc-4546-9538-b4c0308529c0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 66dea6141430ee107ab85312b772d3c5ff3c5e02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804351"
---
# <span data-ttu-id="58377-103">Gestion avancée des stratégies de groupe4.0</span><span class="sxs-lookup"><span data-stu-id="58377-103">Advanced Group Policy Management 4.0</span></span>


<span data-ttu-id="58377-104">Vous pouvez utiliser Microsoft Advanced Group Policy Management (AGPM) pour étendre les fonctionnalités de la console de gestion des stratégies de groupe (GPMC).</span><span class="sxs-lookup"><span data-stu-id="58377-104">You can use Microsoft Advanced Group Policy Management (AGPM) to extend the capabilities of the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="58377-105">AGPM fournit un contrôle de modification complet et une gestion améliorée des objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="58377-105">AGPM provides comprehensive change control and improved management of Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="58377-106">À l’aide d’AGPM, vous pouvez effectuer les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="58377-106">Using AGPM, you can do these tasks:</span></span>

-   <span data-ttu-id="58377-107">Effectuer une modification hors connexion des objets de stratégie de groupe pour pouvoir les créer et les tester avant de les déployer dans un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="58377-107">Perform offline editing of GPOs so that you can create and test them before you deploy them to a production environment.</span></span>

-   <span data-ttu-id="58377-108">Vous pouvez mettre à jour plusieurs versions d’un objet de stratégie de groupe dans une archive centrale pour pouvoir effectuer un ROLLBACK en cas de problème.</span><span class="sxs-lookup"><span data-stu-id="58377-108">Maintain multiple versions of a GPO in a central archive so that you can roll back if a problem occurs.</span></span>

-   <span data-ttu-id="58377-109">Partager la responsabilité en matière d’édition, d’approbation et de révision d’objets de stratégie de groupe entre plusieurs personnes à l’aide d’une délégation basée sur les rôles.</span><span class="sxs-lookup"><span data-stu-id="58377-109">Share the responsibility for editing, approving, and reviewing GPOs among multiple people by using role-based delegation.</span></span>

-   <span data-ttu-id="58377-110">Éliminez le risque que les administrateurs de stratégie de groupe ne remplacent le travail d’une autre personne à l’aide de la fonctionnalité d’archivage et d’extraction pour les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="58377-110">Eliminate the danger of multiple Group Policy administrators overwriting one another's work by using the check-in and check-out capability for GPOs.</span></span>

-   <span data-ttu-id="58377-111">Analysez les modifications apportées à un objet GPO en le comparant à un autre ou à une autre version du même objet de stratégie de groupe à l’aide du rapport de différences.</span><span class="sxs-lookup"><span data-stu-id="58377-111">Analyze changes to a GPO, comparing it to another GPO or another version of the same GPO by using difference reporting.</span></span>

-   <span data-ttu-id="58377-112">Simplifiez la création de nouveaux objets de stratégie de groupe à l’aide de modèles d’objets de stratégie de groupe, en stockant des paramètres de stratégie communs et des paramètres de préférence comme points de départ pour</span><span class="sxs-lookup"><span data-stu-id="58377-112">Simplify creating new GPOs by using GPO templates, storing common policy settings and preference settings to use as starting points for new GPOs.</span></span>

-   <span data-ttu-id="58377-113">Déléguez l’accès à l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="58377-113">Delegate access to the production environment.</span></span>

-   <span data-ttu-id="58377-114">Recherchez des objets de stratégie de groupe avec des attributs spécifiques et filtrez la liste d’objets de stratégie de groupe affichés.</span><span class="sxs-lookup"><span data-stu-id="58377-114">Search for GPOs with specific attributes and filter the list of GPOs displayed.</span></span>

-   <span data-ttu-id="58377-115">Exporter un objet de stratégie de groupe vers un fichier afin de le copier à partir d’un domaine dans une forêt de test vers un domaine dans une forêt de production.</span><span class="sxs-lookup"><span data-stu-id="58377-115">Export a GPO to a file so that you can copy it from a domain in a test forest to a domain in a production forest.</span></span>

<span data-ttu-id="58377-116">AGPM ajoute un dossier de **contrôle de modification** sous chaque domaine affiché dans la console de gestion des stratégies de groupe, en plus d’un onglet **historique** pour chaque lien d’objet de stratégie de groupe affiché dans la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="58377-116">AGPM adds a **Change Control** folder under each domain displayed in the GPMC, in addition to a **History** tab for each GPO and Group Policy link displayed in the GPMC.</span></span>

-   [<span data-ttu-id="58377-117">Vue d'ensemble de la Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="58377-117">Overview of Advanced Group Policy Management</span></span>](overview-of-advanced-group-policy-management-agpm40.md)

-   [<span data-ttu-id="58377-118">Meilleures pratiques en matière de gestion de version</span><span class="sxs-lookup"><span data-stu-id="58377-118">Best Practices for Version Control</span></span>](best-practices-for-version-control-agpm40.md)

-   [<span data-ttu-id="58377-119">Liste de contrôle: administrer le serveur AGPM et l'archivage</span><span class="sxs-lookup"><span data-stu-id="58377-119">Checklist: Administer the AGPM Server and Archive</span></span>](checklist-administer-the-agpm-server-and-archive-agpm40.md)

-   [<span data-ttu-id="58377-120">Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe (GPO)</span><span class="sxs-lookup"><span data-stu-id="58377-120">Checklist: Create, Edit, and Deploy a GPO</span></span>](checklist-create-edit-and-deploy-a-gpo-agpm40.md)

-   [<span data-ttu-id="58377-121">Rechercher et filtrer la liste des objets de stratégie de groupe (GPO)</span><span class="sxs-lookup"><span data-stu-id="58377-121">Search and Filter the List of GPOs</span></span>](search-and-filter-the-list-of-gpos.md)

-   [<span data-ttu-id="58377-122">Exécution de tâches d'administrateur AGPM</span><span class="sxs-lookup"><span data-stu-id="58377-122">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

-   [<span data-ttu-id="58377-123">Exécution de tâches d'éditeur</span><span class="sxs-lookup"><span data-stu-id="58377-123">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="58377-124">Exécution de tâches d'approbateur</span><span class="sxs-lookup"><span data-stu-id="58377-124">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="58377-125">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="58377-125">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

-   [<span data-ttu-id="58377-126">Résolution des problèmes d'AGPM</span><span class="sxs-lookup"><span data-stu-id="58377-126">Troubleshooting AGPM</span></span>](troubleshooting-agpm-agpm40.md)

-   [<span data-ttu-id="58377-127">Interface utilisateur: gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="58377-127">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm40.md)

 

 





