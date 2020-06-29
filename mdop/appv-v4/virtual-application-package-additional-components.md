---
title: Composants supplémentaires d'un package d'application virtuelle
description: Composants supplémentaires d'un package d'application virtuelle
author: dansimp
ms.assetid: 476b0f40-ebd6-4296-92fa-61fa9495c03c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d30c2c6561b0d2c08fd75e0c977bf4590d7e6688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806162"
---
# <span data-ttu-id="3a981-103">Composants supplémentaires d'un package d'application virtuelle</span><span class="sxs-lookup"><span data-stu-id="3a981-103">Virtual Application Package Additional Components</span></span>


<span data-ttu-id="3a981-104">Le Sequencer App-V a détecté un répertoire qui contient les exécutables 64 bits et 32 bits et/ou les fichiers de bibliothèque de liens dynamiques (. dll) qui varient en fonction du même assemblage côte à côte.</span><span class="sxs-lookup"><span data-stu-id="3a981-104">The App-V Sequencer has detected a directory that contains 64-bit and 32-bit executables and/or dynamic-link library (.dll) files that depend on the same side-by-side assembly.</span></span> <span data-ttu-id="3a981-105">En règle générale, le Sequencer crée des assemblys côte à côte privés pour tous les assemblys publics utilisés par le package. Néanmoins, il n’est pas possible de créer des versions 32 bits et 64 bits des assemblys privés dans le même annuaire.</span><span class="sxs-lookup"><span data-stu-id="3a981-105">Typically, the Sequencer creates private side-by-side assemblies for all public assemblies that are used by the package; however, it is not possible to create 32-bit and 64-bit versions of the private assemblies in the same directory.</span></span>

<span data-ttu-id="3a981-106">Si le Sequencer détecte un conflit unique, il effectue les actions suivantes:</span><span class="sxs-lookup"><span data-stu-id="3a981-106">If the Sequencer detects a single conflict, it will perform the following actions:</span></span>

-   <span data-ttu-id="3a981-107">Supprimez tous les assemblys privés 64 bits existants dans l’intégralité du package, qu’il s’agisse d’un conflit ou non.</span><span class="sxs-lookup"><span data-stu-id="3a981-107">Remove all of the existing 64-bit private assemblies in the entire package, whether or not the directory has a conflict.</span></span>

-   <span data-ttu-id="3a981-108">Créer uniquement des versions 32 bits des assemblys côte à côte privés.</span><span class="sxs-lookup"><span data-stu-id="3a981-108">Create only 32-bit versions of the private side-by-side assemblies.</span></span>

<span data-ttu-id="3a981-109">Vous devez installer en natif les versions publiques de tous les assemblys 64 bits requis sur l’ordinateur exécutant le Sequencer et sur tous les ordinateurs clients App-V.</span><span class="sxs-lookup"><span data-stu-id="3a981-109">You should natively install public versions of all the required 64-bit assemblies on the computer running the Sequencer and on all App-V client computers.</span></span>

<span data-ttu-id="3a981-110">Pour localiser les assemblys publics existants requis, ouvrez le répertoire où le package est enregistré et recherchez-le dans le dossier **VFS** .</span><span class="sxs-lookup"><span data-stu-id="3a981-110">To locate the required existing public assemblies, open the directory where the package is saved and look in the **VFS** folder.</span></span> <span data-ttu-id="3a981-111">Par exemple, si la racine du package est **Q:\\MyApp**, lors de l’ordre de l’application, recherchez dans **Q:\\MyApp\\VFS\\CSIDL\ _Windows \\winsxs\\manifests** et repérez tous les assemblys publics existants.</span><span class="sxs-lookup"><span data-stu-id="3a981-111">For example, if the package root is **Q:\\MyApp**, when you sequence the application, look in **Q:\\MyApp\\VFS\\CSIDL\_Windows\\WinSxS\\Manifests** and locate all of the existing public assemblies.</span></span> <span data-ttu-id="3a981-112">Les versions 64 bits de ces fichiers commencent toujours par le texte suivant au début du nom du manifeste: **amd64...**.</span><span class="sxs-lookup"><span data-stu-id="3a981-112">The 64-bit versions of these files will always start with the following text at the beginning of the manifest name: **amd64…**.</span></span> <span data-ttu-id="3a981-113">Le nom exact et la version de l’assembly se trouvent dans le fichier manifeste associé.</span><span class="sxs-lookup"><span data-stu-id="3a981-113">The exact name and version of the assembly can be found in the associated manifest file.</span></span>

<span data-ttu-id="3a981-114">Pour télécharger et installer la version correcte des éléments requis, utilisez l’un des liens suivants:</span><span class="sxs-lookup"><span data-stu-id="3a981-114">Use any of the following links to download and install the correct version of the required prerequisites:</span></span>

-   [<span data-ttu-id="3a981-115">Package redistribuable 2005 Microsoft Visual C++ (x64)</span><span class="sxs-lookup"><span data-stu-id="3a981-115">Microsoft Visual C++ 2005 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152697)

-   [<span data-ttu-id="3a981-116">Package redistribuable Microsoft Visual C++ 2005 SP1 (x64)</span><span class="sxs-lookup"><span data-stu-id="3a981-116">Microsoft Visual C++ 2005 SP1 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152698)

-   [<span data-ttu-id="3a981-117">Package redistribuable 2008 Microsoft Visual C++ (x64)</span><span class="sxs-lookup"><span data-stu-id="3a981-117">Microsoft Visual C++ 2008 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152699)

-   [<span data-ttu-id="3a981-118">Package redistribuable Microsoft Visual C++ 2008 SP1 (x64)</span><span class="sxs-lookup"><span data-stu-id="3a981-118">Microsoft Visual C++ 2008 SP1 Redistributable Package (x64)</span></span>](https://go.microsoft.com/fwlink/?LinkId=152700)

 

 





