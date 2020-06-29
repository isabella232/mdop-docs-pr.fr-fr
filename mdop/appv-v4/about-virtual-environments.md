---
title: À propos des environnements virtuels
description: À propos des environnements virtuels
author: dansimp
ms.assetid: e03a8c72-56c1-4ae9-aa45-0283c50a154c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15f3ae29ae8d5586f83baa98ea6821e09ae5c305
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809329"
---
# <span data-ttu-id="53e58-103">À propos des environnements virtuels</span><span class="sxs-lookup"><span data-stu-id="53e58-103">About Virtual Environments</span></span>


<span data-ttu-id="53e58-104">Les applications virtuelles s’exécutent en environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="53e58-104">Virtual applications run in virtual environments.</span></span> <span data-ttu-id="53e58-105">Les environnements virtuels permettent à chaque application de s’exécuter sur un ordinateur de bureau, un ordinateur portable ou un serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="53e58-105">Virtual environments enable each application to run on a desktop, laptop, or Remote Desktop Session Host (RDSession Host) server without installation and alteration of the host operating system.</span></span> <span data-ttu-id="53e58-106">Chaque application possède ses propres informations de configuration dans l’environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="53e58-106">Each application carries its own configuration information in the virtual environment.</span></span> <span data-ttu-id="53e58-107">Par conséquent, de nombreuses applications sont exécutées côte à côte avec d’autres applications sur le même ordinateur sans aucun conflit.</span><span class="sxs-lookup"><span data-stu-id="53e58-107">As a result, many applications run side by side with other applications on the same computer without any conflicts.</span></span>

<span data-ttu-id="53e58-108">Les applications virtuelles s’exécutent en local, de sorte qu’elles s’exécutent avec les performances complètes, les fonctionnalités et l’accès aux services locaux que vous attendez d’une application installée en local.</span><span class="sxs-lookup"><span data-stu-id="53e58-108">Virtual applications run locally, so they run with the full performance, functionality, and access to local services that you would expect from any application installed locally.</span></span>

<span data-ttu-id="53e58-109">Dans la mesure où chaque application s’exécute dans un environnement virtuel, les problèmes suivants sont réduits:</span><span class="sxs-lookup"><span data-stu-id="53e58-109">Because each application runs in a virtual environment, the following problems are reduced:</span></span>

-   <span data-ttu-id="53e58-110">Conflits d’application: dans les environnements qui n’utilisent pas la virtualisation de l’application, vous devez tester soigneusement chaque application pour vérifier qu’elle n’interfère pas avec d’autres applications installées.</span><span class="sxs-lookup"><span data-stu-id="53e58-110">Application conflicts—In environments that do not use Application Virtualization, you must thoroughly test every application to ensure that it does not interfere with other installed applications.</span></span>

-   <span data-ttu-id="53e58-111">Tests de régression: dans la mesure où l’application ne modifie pas le système d’exploitation sous-jacent, le test de régression de longue durée est éliminé.</span><span class="sxs-lookup"><span data-stu-id="53e58-111">Regression testing—Because the application does not change the underlying operating system, lengthy regression testing is eliminated.</span></span>

-   <span data-ttu-id="53e58-112">Incompatibilités de version: différentes versions d’une même application peuvent être exécutées simultanément sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="53e58-112">Version incompatibilities—Different versions of the same application can run simultaneously on the same computer.</span></span>

-   <span data-ttu-id="53e58-113">Accès multi-utilisateurs: les applications qui ne sont pas exécutées en mode multiutilisateur et qui ne peuvent pas être exécutées au sein d’un hôte RDSession, peuvent désormais le faire et fonctionner correctement pour plusieurs utilisateurs sur un seul hôte RDSession.</span><span class="sxs-lookup"><span data-stu-id="53e58-113">Multiuser access—Applications that do not run in multiuser mode, and therefore cannot run within an RDSession Host, can now do so and function correctly for multiple users on a single RDSession Host.</span></span>

-   <span data-ttu-id="53e58-114">Problèmes de location mutualisée: deux instances de la même application qui utilisent des configurations différentes peuvent être exécutées sur le même ordinateur en même temps.</span><span class="sxs-lookup"><span data-stu-id="53e58-114">Multitenancy issues—Two instances of the same application that use different configurations can run on the same computer at the same time.</span></span>

-   <span data-ttu-id="53e58-115">Les silos de serveurs: le nombre de batteries de serveurs distinctes est éliminé.</span><span class="sxs-lookup"><span data-stu-id="53e58-115">Server siloing—The need for many separate server farms is eliminated.</span></span>

<span data-ttu-id="53e58-116">Les environnements virtuels incluent un registre virtuel pour chaque application.</span><span class="sxs-lookup"><span data-stu-id="53e58-116">Virtual environments include a virtual registry for each application.</span></span> <span data-ttu-id="53e58-117">Les paramètres de Registre créés par une application ne sont pas visibles par d’autres applications ou utilitaires tels que Regedit.</span><span class="sxs-lookup"><span data-stu-id="53e58-117">Registry settings created by one application cannot be seen by other applications or utilities such as Regedit.</span></span> <span data-ttu-id="53e58-118">Au lieu de copier l’intégralité du Registre, le registre virtuel utilise une méthode de *superposition* .</span><span class="sxs-lookup"><span data-stu-id="53e58-118">Rather than copying the entire registry, the virtual registry uses an *overlay* method.</span></span> <span data-ttu-id="53e58-119">Les éléments du registre client peuvent être lus par l’application tant qu’une copie virtuelle de cet élément de Registre n’est pas incluse dans le registre virtuel.</span><span class="sxs-lookup"><span data-stu-id="53e58-119">Items in the client registry can be read by the application as long as a virtual copy of that registry item is not included in the virtual registry.</span></span> <span data-ttu-id="53e58-120">Toutes les écritures apportées à l’application du Registre sont contenues dans le registre virtuel.</span><span class="sxs-lookup"><span data-stu-id="53e58-120">All application writes to the registry are contained in the virtual registry.</span></span>

<span data-ttu-id="53e58-121">Les environnements virtuels incluent également un système de fichiers virtuel et d’autres composants virtuels, notamment les services virtuels et le COM virtuel.</span><span class="sxs-lookup"><span data-stu-id="53e58-121">Virtual environments also include a virtual file system and other virtual components, including virtual services and virtual COM.</span></span>

## <span data-ttu-id="53e58-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="53e58-122">Related topics</span></span>


[<span data-ttu-id="53e58-123">Vue d'ensemble d'Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="53e58-123">Application Virtualization Client Management Console Overview</span></span>](application-virtualization-client-management-console-overview.md)

 

 





