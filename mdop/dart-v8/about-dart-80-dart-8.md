---
title: À propos de DaRT8.0
description: À propos de DaRT8.0
author: dansimp
ms.assetid: ce91efd6-7d78-44cb-bb8f-1f43f768ebaa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e70816425dc4775b11596b91d7b5c0045830c6ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808663"
---
# <span data-ttu-id="cb663-103">À propos de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="cb663-103">About DaRT 8.0</span></span>


<span data-ttu-id="cb663-104">Microsoft Diagnostics and Recovery Tools (DaRT) 8,0 vous aide à résoudre les problèmes liés à l’ordinateur Windows.</span><span class="sxs-lookup"><span data-stu-id="cb663-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 helps you troubleshoot and repair Windows-based computers.</span></span> <span data-ttu-id="cb663-105">Cela inclut les ordinateurs qui ne peuvent pas être démarrés.</span><span class="sxs-lookup"><span data-stu-id="cb663-105">This includes those computers that cannot be started.</span></span> <span data-ttu-id="cb663-106">DaRT 8,0 est un puissant outil d’outils qui étend l’environnement de récupération Windows (WinRE).</span><span class="sxs-lookup"><span data-stu-id="cb663-106">DaRT 8.0 is a powerful set of tools that extend the Windows Recovery Environment (WinRE).</span></span> <span data-ttu-id="cb663-107">À l’aide de DaRT, vous pouvez analyser un problème pour en déterminer la cause, par exemple, en inspectant le journal des événements ou le Registre du système de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cb663-107">By using DaRT, you can analyze an issue to determine its cause, for example, by inspecting the computer’s event log or system registry.</span></span> <span data-ttu-id="cb663-108">Le DaRT prend en charge la récupération des disques durs de base qui contiennent des partitions (par exemple, partitions principales et lecteurs logiques) et prend en charge la récupération des volumes.</span><span class="sxs-lookup"><span data-stu-id="cb663-108">DaRT supports the recovery of basic hard disks that contain partitions, for example, primary partitions and logical drives, and supports the recovery of volumes.</span></span>

<span data-ttu-id="cb663-109">**Remarques**  Le DaRT ne prend pas en charge la récupération des disques dynamiques.</span><span class="sxs-lookup"><span data-stu-id="cb663-109">**Note** DaRT does not support the recovery of dynamic disks.</span></span>

 

<span data-ttu-id="cb663-110">Le DaRT fournit également des outils pour vous aider à résoudre un problème dès que vous déterminez la cause du problème.</span><span class="sxs-lookup"><span data-stu-id="cb663-110">DaRT also provides tools to help you fix a problem as soon as you determine the cause.</span></span> <span data-ttu-id="cb663-111">Par exemple, vous pouvez utiliser les outils dans DaRT pour désactiver un pilote de périphérique défectueux, supprimer les correctifs, restaurer des fichiers supprimés et analyser l’ordinateur à la recherche de logiciels malveillants, même si vous ne pouvez pas démarrer le système d’exploitation Windows installé.</span><span class="sxs-lookup"><span data-stu-id="cb663-111">For example, you can use the tools in DaRT to disable a faulty device driver, remove hotfixes, restore deleted files, and scan the computer for malware even when you cannot or should not start the installed Windows operating system.</span></span>

<span data-ttu-id="cb663-112">Le DaRT peut vous aider à récupérer rapidement des ordinateurs qui exécutent des versions 32 bits ou 64 bits de Windows 8, généralement plus longtemps que nécessaire pour réutiliser l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cb663-112">DaRT can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 8, typically in less time than it would take to reimage the computer.</span></span>

<span data-ttu-id="cb663-113">Les fonctionnalités de DaRT vous permettent de créer une image de récupération.</span><span class="sxs-lookup"><span data-stu-id="cb663-113">Functionality in DaRT lets you create a recovery image.</span></span> <span data-ttu-id="cb663-114">L’image de récupération démarre l’environnement de récupération Windows, à partir duquel vous pouvez démarrer la fenêtre du **jeu d’outils de diagnostics et de récupération** et accéder aux outils Dart.</span><span class="sxs-lookup"><span data-stu-id="cb663-114">The recovery image starts Windows Recovery Environment (Windows RE), from which you can start the **Diagnostics and Recovery Toolset** window and access the DaRT tools.</span></span>

<span data-ttu-id="cb663-115">Utilisez l' **Assistant image de récupération DART** pour créer l’image de récupération Dart.</span><span class="sxs-lookup"><span data-stu-id="cb663-115">Use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span> <span data-ttu-id="cb663-116">Par défaut, l’Assistant crée un fichier image ISO (International Organization for Standardization) et un fichier WIM (Windows Imaging Format) et vous permet de graver l’image sur un CD, un DVD ou un lecteur USB.</span><span class="sxs-lookup"><span data-stu-id="cb663-116">By default, the wizard creates an International Organization for Standardization (ISO) image file and a Windows Imaging Format (WIM) file and let you burn the image to a CD, DVD, or USB.</span></span> <span data-ttu-id="cb663-117">Vous pouvez déployer l’image localement sur les ordinateurs des utilisateurs finaux ou vous pouvez la déployer à partir d’une partition réseau distante ou d’une partition de récupération sur le disque dur local.</span><span class="sxs-lookup"><span data-stu-id="cb663-117">You can deploy the image locally at end user’s computers, or you can deploy it from a remote network partition or a recovery partition on the local hard drive.</span></span>

## <a href="" id="what-s-new-in-dart-8-0"></a><span data-ttu-id="cb663-118">Nouveautés de DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="cb663-118">What’s new in DaRT 8.0</span></span>


<span data-ttu-id="cb663-119">Le DaRT 8,0 peut vous aider à récupérer rapidement des ordinateurs qui exécutent des versions 32 bits ou 64 bits de Windows 8, généralement plus longtemps que nécessaire pour réutiliser l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cb663-119">DaRT 8.0 can help you quickly recover computers that are running either 32-bit or 64-bit versions of Windows 8, typically in less time than it would take to reimage the computer.</span></span> <span data-ttu-id="cb663-120">Le DaRT 8,0 offre les nouvelles fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb663-120">DaRT 8.0 has the following new features.</span></span>

### <span data-ttu-id="cb663-121">Créer des images DaRT à l’aide de Windows 8 ou Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cb663-121">Create DaRT images by using Windows 8 or Windows Server 2012</span></span>

<span data-ttu-id="cb663-122">Le DaRT 8,0 vous permet de créer des images DaRT en utilisant Windows® 8 ou Windows Server® 2012.</span><span class="sxs-lookup"><span data-stu-id="cb663-122">DaRT 8.0 enables you to create DaRT images using either Windows® 8 or Windows Server® 2012.</span></span> <span data-ttu-id="cb663-123">Pour les versions de Windows antérieures à Windows 8 et Windows Server 2012, les clients doivent continuer à utiliser les versions antérieures de DaRT.</span><span class="sxs-lookup"><span data-stu-id="cb663-123">For versions of Windows earlier than Windows 8 and Windows Server 2012, customers should continue to use earlier versions of DaRT.</span></span>

### <span data-ttu-id="cb663-124">Générer des images 32 et 64 bits à partir d’un ordinateur</span><span class="sxs-lookup"><span data-stu-id="cb663-124">Generate both 32- and 64-bit images from one computer</span></span>

<span data-ttu-id="cb663-125">Le DaRT 8,0 vous permet de générer des images 32 bits et 64 bits à partir d’un ordinateur exécutant DaRT, qu’il s’agisse d’un ordinateur 32 ou d’un ordinateur 64.</span><span class="sxs-lookup"><span data-stu-id="cb663-125">DaRT 8.0 enables you to generate both 32-bit and 64-bit images from a single computer that is running DaRT, regardless of whether the computer is a 32-bit or 64-bit computer.</span></span> <span data-ttu-id="cb663-126">Dans DaRT7, l’image qui a été créée devait être de la même manière que celle de l’ordinateur exécutant DaRT.</span><span class="sxs-lookup"><span data-stu-id="cb663-126">In DaRT7, the image that was created had to be the same, bit-wise, as the computer that was running DaRT.</span></span>

### <span data-ttu-id="cb663-127">Créer une image qui prend en charge les ordinateurs équipés d’une interface BIOS ou UEFI</span><span class="sxs-lookup"><span data-stu-id="cb663-127">Create one image that supports computers that have either a BIOS or UEFI interface</span></span>

<span data-ttu-id="cb663-128">La prise en charge de DaRT 8.0 pour les interfaces d’interface de microprogrammes unifiées (UEFI) et de BIOS vous permet de créer une seule image qui fonctionne avec des ordinateurs dotés d’une interface.</span><span class="sxs-lookup"><span data-stu-id="cb663-128">DaRT 8.0’s support for both the Unified Extensible Firmware Interface (UEFI) and BIOS interfaces enables you to create just one image that works with computers that have either interface.</span></span>

### <span data-ttu-id="cb663-129">Utiliser une table de partitions GUID (GPT) pour partitionner</span><span class="sxs-lookup"><span data-stu-id="cb663-129">Use a GUID partition table (GPT) for partitioning</span></span>

<span data-ttu-id="cb663-130">Les outils 8,0 DaRT prennent désormais en charge les disques GPT Windows 8, qui fournissent un mécanisme plus flexible pour partitionner des disques que l’ancien modèle de partitionnement d’enregistrement de démarrage principal (MBR).</span><span class="sxs-lookup"><span data-stu-id="cb663-130">DaRT 8.0 tools now support Windows 8 GPT disks, which provide a more flexible mechanism for partitioning disks than the older master boot record (MBR) partitioning scheme.</span></span> <span data-ttu-id="cb663-131">Les outils 8,0 de DaRT continuent de prendre en charge une partition MBR.</span><span class="sxs-lookup"><span data-stu-id="cb663-131">DaRT 8.0 tools continue to support MBR partitioning.</span></span>

### <span data-ttu-id="cb663-132">Installer Windows 8 et Windows Server 2012 sur le disque dur local</span><span class="sxs-lookup"><span data-stu-id="cb663-132">Install Windows 8 and Windows Server 2012 on the local hard disk</span></span>

<span data-ttu-id="cb663-133">Les outils 8,0 DaRT peuvent être utilisés uniquement lorsque Windows 8 et Windows Server 2012 sont installés sur le disque dur local.</span><span class="sxs-lookup"><span data-stu-id="cb663-133">DaRT 8.0 tools can be used only when Windows 8 and Windows Server 2012 are installed on the local hard disk.</span></span> <span data-ttu-id="cb663-134">Pour le moment, il n’y a pas de prise en charge pour Windows to go.</span><span class="sxs-lookup"><span data-stu-id="cb663-134">Currently, there is no support for Windows To Go.</span></span>

### <a href="" id="-------------dart-8-0-release-notes"></a> <span data-ttu-id="cb663-135">Notes de publication de DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="cb663-135">DaRT 8.0 release notes</span></span>

<span data-ttu-id="cb663-136">Pour plus d’informations et pour les actualités de dernière minute qui n’ont pas été intégrées à la documentation, voir les [notes de publication de DaRT 8,0](release-notes-for-dart-80--dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="cb663-136">For more information, and for late-breaking news that did not make it into the documentation, see the [Release Notes for DaRT 8.0](release-notes-for-dart-80--dart-8.md).</span></span>

## <span data-ttu-id="cb663-137">Obtention de la 8,0 DaRT</span><span class="sxs-lookup"><span data-stu-id="cb663-137">How to Get DaRT 8.0</span></span>


<span data-ttu-id="cb663-138">Cette technologie fait partie du pack d’optimisation de bureau Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="cb663-138">This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="cb663-139">MDOP fait partie de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="cb663-139">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="cb663-140">Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="cb663-140">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="cb663-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb663-141">Related topics</span></span>


[<span data-ttu-id="cb663-142">Prise en main de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="cb663-142">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)

[<span data-ttu-id="cb663-143">Notes de publication pour DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="cb663-143">Release Notes for DaRT 8.0</span></span>](release-notes-for-dart-80--dart-8.md)

 

 





