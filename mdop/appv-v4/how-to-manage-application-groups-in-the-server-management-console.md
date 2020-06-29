---
title: Procédure pour gérer des groupes d'applications dans Server Management Console
description: Procédure pour gérer des groupes d'applications dans Server Management Console
author: dansimp
ms.assetid: 46997971-bdc8-4565-aefd-f47e90d6d7a6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 59a357d93ea63cc728f59a0633b7a5b9953aad14
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807013"
---
# <span data-ttu-id="645bf-103">Procédure pour gérer des groupes d'applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="645bf-103">How to Manage Application Groups in the Server Management Console</span></span>


<span data-ttu-id="645bf-104">Vous pouvez afficher et gérer une ou plusieurs applications dans les groupes d’applications dans la console de gestion du serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="645bf-104">You can display and manage one or more applications in application groups in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="645bf-105">Cela peut être utile si vous souhaitez effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="645bf-105">This can be useful when you want to do the following:</span></span>

-   <span data-ttu-id="645bf-106">Organisez de nombreux applications en sous-groupes plus gérables.</span><span class="sxs-lookup"><span data-stu-id="645bf-106">Organize many applications into more manageable subgroups.</span></span>

-   <span data-ttu-id="645bf-107">Créer des groupes d’applications spécifiques à un service ou à une autre division de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="645bf-107">Create groups of applications specific to a department or other company division.</span></span>

-   <span data-ttu-id="645bf-108">Grouper des types d’applications similaires, tels que des logiciels financiers;</span><span class="sxs-lookup"><span data-stu-id="645bf-108">Group similar types of applications, such as financial software.</span></span>

-   <span data-ttu-id="645bf-109">Simplifiez les autorisations d’accès ou la gestion des licences par groupe.</span><span class="sxs-lookup"><span data-stu-id="645bf-109">Simplify access permissions or license management by group.</span></span>

-   <span data-ttu-id="645bf-110">Modifiez les propriétés des applications et des groupes d’applications au sein d’un groupe simultanément.</span><span class="sxs-lookup"><span data-stu-id="645bf-110">Change the properties of applications and application groups within a group simultaneously.</span></span>

<span data-ttu-id="645bf-111">Vous pouvez créer un groupe, le placer à l’emplacement de votre choix dans l’arborescence **applications** de la console et importer des applications dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="645bf-111">You can create a group, place it where you would like in the console's **Applications** tree, and import applications to the group.</span></span> <span data-ttu-id="645bf-112">Vous pouvez ensuite configurer et gérer les propriétés du groupe pour qu’elles s’appliquent à toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="645bf-112">Then you can configure and manage the group's properties to affect all of its applications.</span></span> <span data-ttu-id="645bf-113">Vous pouvez également déplacer des applications entre des groupes.</span><span class="sxs-lookup"><span data-stu-id="645bf-113">You can also move applications among groups.</span></span>

<span data-ttu-id="645bf-114">**Remarques**  Le déplacement d’applications en groupes n’a pas d’incidence sur les emplacements des fichiers (SFT, OSD ou SPRJ) sur le système de fichiers du serveur.</span><span class="sxs-lookup"><span data-stu-id="645bf-114">**Note** Moving applications into groups does not affect the locations of their files (SFT, OSD, or SPRJ) on the server's file system.</span></span>

 

## <span data-ttu-id="645bf-115">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="645bf-115">In This Section</span></span>


<a href="" id="how-to-create-an-application-group"></a>[<span data-ttu-id="645bf-116">Procédure pour créer un groupe d'applications</span><span class="sxs-lookup"><span data-stu-id="645bf-116">How to Create an Application Group</span></span>](how-to-create-an-application-group.md)  
<span data-ttu-id="645bf-117">Fournit des instructions pas à pas pour la création d’un groupe d’applications.</span><span class="sxs-lookup"><span data-stu-id="645bf-117">Provides step-by-step instructions for creating an application group.</span></span>

<a href="" id="how-to-move-an-application-group"></a>[<span data-ttu-id="645bf-118">Procédure pour déplacer un groupe d'applications</span><span class="sxs-lookup"><span data-stu-id="645bf-118">How to Move an Application Group</span></span>](how-to-move-an-application-group.md)  
<span data-ttu-id="645bf-119">Fournit des instructions pas à pas pour le déplacement d’un groupe d’applications.</span><span class="sxs-lookup"><span data-stu-id="645bf-119">Provides step-by-step instructions for moving an application group.</span></span>

<a href="" id="how-to-rename-an-application-group"></a>[<span data-ttu-id="645bf-120">Procédure pour renommer un groupe d'applications</span><span class="sxs-lookup"><span data-stu-id="645bf-120">How to Rename an Application Group</span></span>](how-to-rename-an-application-group.md)  
<span data-ttu-id="645bf-121">Fournit des instructions pas à pas pour le changement de nom d’un groupe d’applications.</span><span class="sxs-lookup"><span data-stu-id="645bf-121">Provides step-by-step instructions for renaming an application group.</span></span>

<a href="" id="how-to-remove-an-application-group"></a>[<span data-ttu-id="645bf-122">Procédure pour supprimer un groupe d'applications</span><span class="sxs-lookup"><span data-stu-id="645bf-122">How to Remove an Application Group</span></span>](how-to-remove-an-application-group.md)  
<span data-ttu-id="645bf-123">Fournit des instructions pas à pas pour supprimer ou supprimer un groupe d’applications.</span><span class="sxs-lookup"><span data-stu-id="645bf-123">Provides step-by-step instructions for removing or deleting an application group.</span></span>

## <span data-ttu-id="645bf-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="645bf-124">Related topics</span></span>


[<span data-ttu-id="645bf-125">Procédure pour gérer des applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="645bf-125">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

[<span data-ttu-id="645bf-126">Procédure pour effectuer des tâches d'administration dans Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="645bf-126">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





