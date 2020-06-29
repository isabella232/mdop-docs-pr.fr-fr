---
title: À propos des applications Application Virtualization
description: À propos des applications Application Virtualization
author: dansimp
ms.assetid: 3bf833b7-d172-4eef-a9e8-4b4f0c7eb15b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4eeea7a0ec4454aefcdde5196ae15ed029da45b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808166"
---
# <span data-ttu-id="bafbf-103">À propos des applications Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="bafbf-103">About Application Virtualization Applications</span></span>


<span data-ttu-id="bafbf-104">Dans le cadre de la virtualisation des applications, une *application* est un programme exécutable, tel que Microsoft Visio, qui est transmis au client ou au client de bureau de la virtualisation de l’application pour les services Bureau à distance (auparavant services Terminal Server) à partir du serveur de gestion de la virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="bafbf-104">In Application Virtualization, an *application* is an executable program, such as Microsoft Visio, that is streamed to the Application Virtualization Desktop Client or Client for Remote Desktop Services (formerly Terminal Services) from an Application Virtualization Management Server.</span></span> <span data-ttu-id="bafbf-105">Pour qu’une application puisse être transformée en flux vers un client, l’application doit être préparée en vue d’une diffusion en continu en la traitant avec le Sequencer de virtualisation de l’application.</span><span class="sxs-lookup"><span data-stu-id="bafbf-105">Before an application can be streamed to a client, the application must be prepared for streaming by processing it with the Application Virtualization Sequencer.</span></span>

## <span data-ttu-id="bafbf-106">Gestion des applications</span><span class="sxs-lookup"><span data-stu-id="bafbf-106">Managing Applications</span></span>


<span data-ttu-id="bafbf-107">Vous devez ajouter des applications au système avant de pouvoir rendre les applications accessibles aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bafbf-107">You must add applications to the system before you can make the applications available to users.</span></span> <span data-ttu-id="bafbf-108">La méthode la plus courante pour ajouter des applications au système consiste à les importer.</span><span class="sxs-lookup"><span data-stu-id="bafbf-108">The most common method for adding applications to the system is to import them.</span></span> <span data-ttu-id="bafbf-109">Pour accéder à cette fonctionnalité, cliquez avec le bouton droit sur le nœud **applications** dans la console de gestion du serveur d’applications et sélectionnez **importer des applications**.</span><span class="sxs-lookup"><span data-stu-id="bafbf-109">To access this feature, right-click the **Applications** node in the Application Virtualization Server Management Console and choose **Import Applications**.</span></span>

<span data-ttu-id="bafbf-110">Vous pouvez importer plusieurs fichiers Open Software Descriptor (OSD) en même temps, ou vous pouvez importer un fichier de projet de Sequencer (SPRJ) qui peut contenir plusieurs fichiers OSD.</span><span class="sxs-lookup"><span data-stu-id="bafbf-110">You can import more than one Open Software Descriptor (OSD) file at the same time, or you can import a Sequencer Project file (SPRJ) that can contain multiple OSD files.</span></span> <span data-ttu-id="bafbf-111">Cette fonctionnalité vous permet de configurer les applications associées de manière similaire.</span><span class="sxs-lookup"><span data-stu-id="bafbf-111">This functionality enables you to configure related applications similarly.</span></span>

<span data-ttu-id="bafbf-112">Vous pouvez également utiliser les fonctionnalités suivantes pour vous aider à gérer vos applications:</span><span class="sxs-lookup"><span data-stu-id="bafbf-112">You can also use the following features to help you manage your applications:</span></span>

-   <span data-ttu-id="bafbf-113">**Groupes d’applications**: permet de créer des groupes logiques d’applications pour une gestion simplifiée.</span><span class="sxs-lookup"><span data-stu-id="bafbf-113">**Application Groups**—Enables you to create logical groups of applications for simplified management.</span></span> <span data-ttu-id="bafbf-114">Lorsque des modifications sont apportées à un groupe (par exemple, des autorisations d’accès), les modifications sont appliquées à toutes les applications du groupe.</span><span class="sxs-lookup"><span data-stu-id="bafbf-114">When changes are made to a group (for example, access permissions), the changes are applied to all applications in the group.</span></span> <span data-ttu-id="bafbf-115">Les applications d’un groupe peuvent provenir de différents packages.</span><span class="sxs-lookup"><span data-stu-id="bafbf-115">Applications in a group can come from different packages.</span></span>

-   <span data-ttu-id="bafbf-116">**Sélection multiple**: permet de sélectionner plusieurs applications à la fois en maintenant la touche CTRL enfoncée lorsque vous cliquez sur une application pour modifier les propriétés de l’application.</span><span class="sxs-lookup"><span data-stu-id="bafbf-116">**Multi Select**—Enables you to select multiple applications at once by holding the CTRL key when you click an application to modify the application properties.</span></span> <span data-ttu-id="bafbf-117">Toutefois, si vous voulez conserver une relation entre les applications, vous devez créer un groupe d’applications pour contenir les applications.</span><span class="sxs-lookup"><span data-stu-id="bafbf-117">However, if you want to maintain a relationship between the applications, you should create an application group to hold the applications.</span></span>

-   <span data-ttu-id="bafbf-118">**Copie du système entre systèmes**: permet de copier des applications d’un environnement vers un autre qui exécute la même version d’App-V en une seule étape.</span><span class="sxs-lookup"><span data-stu-id="bafbf-118">**Cross System Copy**—Enables you to copy applications from one environment to another environment that is running the same version of App-V in one step.</span></span> <span data-ttu-id="bafbf-119">Par exemple, vous pouvez avoir un environnement de test d’acceptation utilisateur dans lequel vous déployez et configurez initialement des applications.</span><span class="sxs-lookup"><span data-stu-id="bafbf-119">For example, you might have a user acceptance test environment where you initially deploy and configure applications.</span></span> <span data-ttu-id="bafbf-120">Après avoir terminé votre phase de test, vous pouvez répliquer le même ensemble d’applications (y compris les autorisations) sur l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="bafbf-120">After you finish your testing phase, you might want to replicate the same set of applications (including permissions) to the production environment.</span></span>

## <span data-ttu-id="bafbf-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bafbf-121">Related topics</span></span>


[<span data-ttu-id="bafbf-122">À propos des packages Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="bafbf-122">About Application Virtualization Packages</span></span>](about-application-virtualization-packages.md)

[<span data-ttu-id="bafbf-123">À propos d'Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="bafbf-123">About the Application Virtualization Server Management Console</span></span>](about-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="bafbf-124">Procédure pour gérer des groupes d'applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="bafbf-124">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="bafbf-125">Procédure pour gérer des applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="bafbf-125">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





