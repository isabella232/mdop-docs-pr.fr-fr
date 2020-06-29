---
title: Paramètres de ligne de commande
description: Paramètres de ligne de commande
author: dansimp
ms.assetid: d90a0591-f1ce-4cb8-b244-85cc70461922
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31d6ca1215648e2519e9818817ab5cc779a746d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807893"
---
# <span data-ttu-id="c992f-103">Paramètres de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="c992f-103">Command-Line Parameters</span></span>


<span data-ttu-id="c992f-104">Pour séquencer une application et mettre à niveau un package d’application séquencé à l’invite de commandes, utilisez les paramètres de séquenceur d’applications suivants.</span><span class="sxs-lookup"><span data-stu-id="c992f-104">Use the following Application Virtualization Sequencer parameters to sequence an application and to upgrade a sequenced application package at the command prompt.</span></span> <span data-ttu-id="c992f-105">Dans le répertoire Microsoft Application Virtualization Sequencer, entrez **SFTSequencer**, suivi du paramètre approprié.</span><span class="sxs-lookup"><span data-stu-id="c992f-105">In the Microsoft Application Virtualization Sequencer directory, you would enter **SFTSequencer**, followed by the appropriate parameter.</span></span>

<a href="" id="-help-or---"></a><span data-ttu-id="c992f-106">*/Help* ou */?*</span><span class="sxs-lookup"><span data-stu-id="c992f-106">*/HELP* or */?*</span></span>  
<span data-ttu-id="c992f-107">Permet d’afficher la liste des paramètres disponibles pour le séquençage de lignes de commande.</span><span class="sxs-lookup"><span data-stu-id="c992f-107">Use to display the list of parameters available for command-line sequencing.</span></span>

<a href="" id="-installpackage-or--i"></a><span data-ttu-id="c992f-108">*/INSTALLPACKAGE* ou */i*</span><span class="sxs-lookup"><span data-stu-id="c992f-108">*/INSTALLPACKAGE* or */I*</span></span>  
<span data-ttu-id="c992f-109">Permet de spécifier le programme d’installation ou un fichier de commandes que l’application doit être séquencée.</span><span class="sxs-lookup"><span data-stu-id="c992f-109">Use to specify the installer or a batch file for the application to be sequenced.</span></span>

<a href="" id="-installpath-or--p"></a><span data-ttu-id="c992f-110">*/InstallPath* ou */p*</span><span class="sxs-lookup"><span data-stu-id="c992f-110">*/INSTALLPATH* or */P*</span></span>  
<span data-ttu-id="c992f-111">Utiliser pour spécifier le répertoire racine du package.</span><span class="sxs-lookup"><span data-stu-id="c992f-111">Use to specify the package root directory.</span></span>

<a href="" id="-outputfile-or--o"></a><span data-ttu-id="c992f-112">*/Outputfile* ou */o*</span><span class="sxs-lookup"><span data-stu-id="c992f-112">*/OUTPUTFILE* or */O*</span></span>  
<span data-ttu-id="c992f-113">Utiliser pour spécifier le chemin d’accès et le nom de fichier du fichier SPRJ qui sera généré.</span><span class="sxs-lookup"><span data-stu-id="c992f-113">Use to specify the path and file name of the SPRJ file that will be generated.</span></span>

<span data-ttu-id="c992f-114">**Important**  Le paramètre */outputfile* n’est pas disponible lors de l’ouverture d’un package que vous ne souhaitez pas mettre à niveau.</span><span class="sxs-lookup"><span data-stu-id="c992f-114">**Important** The */OUTPUTFILE* parameter is not available when opening a package that you do not intend to upgrade.</span></span>

 

<a href="" id="-fullload-or--f"></a><span data-ttu-id="c992f-115">*/FULLLOAD* ou */f*</span><span class="sxs-lookup"><span data-stu-id="c992f-115">*/FULLLOAD* or */F*</span></span>  
<span data-ttu-id="c992f-116">Permet de spécifier si les éléments doivent être placés dans le bloc de fonctionnalités principal.</span><span class="sxs-lookup"><span data-stu-id="c992f-116">Use to specify whether to put everything in the primary feature block.</span></span>

<a href="" id="-packagename-or--k"></a><span data-ttu-id="c992f-117">*/PackageName* ou */k*</span><span class="sxs-lookup"><span data-stu-id="c992f-117">*/PACKAGENAME* or */K*</span></span>  
<span data-ttu-id="c992f-118">Utiliser pour spécifier le nom du package de l’application séquencée.</span><span class="sxs-lookup"><span data-stu-id="c992f-118">Use to specify the package name of the sequenced application.</span></span>

<a href="" id="-blocksize"></a>*<span data-ttu-id="c992f-119">/BLOCKSIZE</span><span class="sxs-lookup"><span data-stu-id="c992f-119">/BLOCKSIZE</span></span>*  
<span data-ttu-id="c992f-120">Spécifie la taille de bloc de fichiers SFT qui sera utilisée pour diffuser le package sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="c992f-120">Specifies the SFT file block size that will be used to stream the package to client computers.</span></span> <span data-ttu-id="c992f-121">Vous pouvez sélectionner l’une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="c992f-121">You can select one of the following values:</span></span>

-   <span data-ttu-id="c992f-122">4 KO</span><span class="sxs-lookup"><span data-stu-id="c992f-122">4 KB</span></span>

-   <span data-ttu-id="c992f-123">16 KO</span><span class="sxs-lookup"><span data-stu-id="c992f-123">16 KB</span></span>

-   <span data-ttu-id="c992f-124">32 KO</span><span class="sxs-lookup"><span data-stu-id="c992f-124">32 KB</span></span>

-   <span data-ttu-id="c992f-125">64 KO</span><span class="sxs-lookup"><span data-stu-id="c992f-125">64 KB</span></span>

<span data-ttu-id="c992f-126">Vous devez prendre en considération la taille du fichier SFT lorsque vous spécifiez la taille du bloc.</span><span class="sxs-lookup"><span data-stu-id="c992f-126">You should consider the size of the SFT file when you specify the block size.</span></span> <span data-ttu-id="c992f-127">Le flux d’un fichier dont la taille de blocs est plus petite prend plus de temps sur le réseau, mais nécessite moins de bande passante.</span><span class="sxs-lookup"><span data-stu-id="c992f-127">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="c992f-128">Les fichiers de tailles de blocs plus grandes utilisent davantage de bande passante réseau.</span><span class="sxs-lookup"><span data-stu-id="c992f-128">Files with larger block sizes use more network bandwidth.</span></span>

<a href="" id="-compression"></a>*<span data-ttu-id="c992f-129">/COMPRESSION</span><span class="sxs-lookup"><span data-stu-id="c992f-129">/COMPRESSION</span></span>*  
<span data-ttu-id="c992f-130">Utiliser pour spécifier la méthode permettant de compresser le fichier SFT lors de son flux vers le client.</span><span class="sxs-lookup"><span data-stu-id="c992f-130">Use to specify the method for compressing the SFT file as it is streamed to the client.</span></span>

<a href="" id="-msi-or--m"></a><span data-ttu-id="c992f-131">*/MSI* ou */m*</span><span class="sxs-lookup"><span data-stu-id="c992f-131">*/MSI* or */M*</span></span>  
<span data-ttu-id="c992f-132">Permet de spécifier la génération d’un package Microsoft Windows Installer pour l’application séquencée.</span><span class="sxs-lookup"><span data-stu-id="c992f-132">Use to specify generating a Microsoft Windows Installer package for the sequenced application.</span></span>

<a href="" id="-default"></a>*<span data-ttu-id="c992f-133">/DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c992f-133">/DEFAULT</span></span>*  
<span data-ttu-id="c992f-134">Spécifie le fichier SPRJ par défaut qui sera utilisé lors de la création d’un package d’application virtuel.</span><span class="sxs-lookup"><span data-stu-id="c992f-134">Specifies the default SPRJ file that will be used when creating a virtual application package.</span></span> <span data-ttu-id="c992f-135">Ce fichier est utilisé comme modèle. sprj lorsque l’application est séquencée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="c992f-135">This file is used as the .sprj template when the application is sequenced for the first time.</span></span>

<a href="" id="-upgrade"></a>*<span data-ttu-id="c992f-136">/UPGRADE</span><span class="sxs-lookup"><span data-stu-id="c992f-136">/UPGRADE</span></span>*  
<span data-ttu-id="c992f-137">Spécifie le chemin d’accès et le nom de fichier du fichier SPRJ qui sera mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="c992f-137">Specifies the path and file name of the SPRJ file that will be upgraded.</span></span>

<a href="" id="-decodepath"></a>*<span data-ttu-id="c992f-138">/DECODEPATH</span><span class="sxs-lookup"><span data-stu-id="c992f-138">/DECODEPATH</span></span>*  
<span data-ttu-id="c992f-139">Spécifie le répertoire sur l’ordinateur de séquençage dans lequel les fichiers associés au package d’application séquencé sont installés.</span><span class="sxs-lookup"><span data-stu-id="c992f-139">Specifies the directory on the sequencing computer where the files associated with the sequenced application package are installed.</span></span> <span data-ttu-id="c992f-140">Lorsque vous spécifiez le répertoire, utilisez l’un des formats suivants:</span><span class="sxs-lookup"><span data-stu-id="c992f-140">Use one of the following formats when specifying the directory:</span></span>

-   <span data-ttu-id="c992f-141">/DECODEPATH: Q:</span><span class="sxs-lookup"><span data-stu-id="c992f-141">/decodepath:Q:</span></span>

-   <span data-ttu-id="c992f-142">/decodepath:Q:.</span><span class="sxs-lookup"><span data-stu-id="c992f-142">/decodepath:Q:.</span></span>

-   <span data-ttu-id="c992f-143">/decodepath:"Q:."</span><span class="sxs-lookup"><span data-stu-id="c992f-143">/decodepath:”Q:.”</span></span>

-   <span data-ttu-id="c992f-144">/DECODEPATH: "Q:"</span><span class="sxs-lookup"><span data-stu-id="c992f-144">/decodepath:”Q:”</span></span>

## <span data-ttu-id="c992f-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c992f-145">Related topics</span></span>


[<span data-ttu-id="c992f-146">À propos de l'utilisation de la ligne de commande de Sequencer</span><span class="sxs-lookup"><span data-stu-id="c992f-146">About Using the Sequencer Command Line</span></span>](about-using-the-sequencer-command-line.md)

[<span data-ttu-id="c992f-147">Procédure pour ouvrir une application séquencée à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="c992f-147">How to Open a Sequenced Application Using the Command Line</span></span>](how-to-open-a-sequenced-application-using-the-command-line.md)

[<span data-ttu-id="c992f-148">Procédure pour mettre à niveau un package à l'aide de la commande Ouvrir un package</span><span class="sxs-lookup"><span data-stu-id="c992f-148">How to Upgrade a Package Using the Open Package Command</span></span>](how-to-upgrade-a-package-using-the-open-package-command.md)

 

 





