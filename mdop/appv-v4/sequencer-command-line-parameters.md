---
title: Paramètres de ligne de commande de Sequencer
description: Paramètres de ligne de commande de Sequencer
author: dansimp
ms.assetid: 28fb875a-c302-4d95-b2e0-8dc0c5dbb0f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ecfa269de04cf3dcba30cbb4a40f9176f03f6571
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806353"
---
# <span data-ttu-id="f7dc2-103">Paramètres de ligne de commande de Sequencer</span><span class="sxs-lookup"><span data-stu-id="f7dc2-103">Sequencer Command-Line Parameters</span></span>


<span data-ttu-id="f7dc2-104">Vous pouvez utiliser les paramètres de Sequencer d’application Virtualization suivants (App-V) pour séquencer une application et mettre à niveau une application virtuelle existante à l’aide d’une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-104">You can use the following Application Virtualization (App-V) Sequencer parameters to sequence an application and to upgrade an existing virtual application by using a command line.</span></span> <span data-ttu-id="f7dc2-105">Pour plus d’informations sur le séquençage d’une application à l’aide d’une ligne de commande, voir [Comment séquencer une nouvelle application à l’aide de la ligne de commande](how-to-sequence-a-new-application-by-using-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="f7dc2-105">For more information about sequencing an application by using a command line, see [How to Sequence a New Application by Using the Command Line](how-to-sequence-a-new-application-by-using-the-command-line.md).</span></span>

## <span data-ttu-id="f7dc2-106">Paramètres de ligne de commande de Sequencer</span><span class="sxs-lookup"><span data-stu-id="f7dc2-106">Sequencer Command-Line Parameters</span></span>


<a href="" id="-help-or---"></a>**<span data-ttu-id="f7dc2-107">/HELP ou/?</span><span class="sxs-lookup"><span data-stu-id="f7dc2-107">/HELP or /?</span></span>**  
<span data-ttu-id="f7dc2-108">Affiche des informations sur les paramètres disponibles pour l’utilisation de la ligne de commande pour la séquence des applications.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-108">Displays information about parameters that are available for using a command line to sequence applications.</span></span>

<a href="" id="-installpackage-or--i"></a>**<span data-ttu-id="f7dc2-109">/INSTALLPACKAGE ou/I</span><span class="sxs-lookup"><span data-stu-id="f7dc2-109">/INSTALLPACKAGE or /I</span></span>**  
<span data-ttu-id="f7dc2-110">Spécifie le programme d’installation Windows ou un fichier de commandes qui sera utilisé pour installer une application de manière à ce qu’elle puisse être séquencée.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-110">Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</span></span>

<a href="" id="-installpath-or--p"></a>**<span data-ttu-id="f7dc2-111">/INSTALLPATH ou/P</span><span class="sxs-lookup"><span data-stu-id="f7dc2-111">/INSTALLPATH or /P</span></span>**  
<span data-ttu-id="f7dc2-112">Spécifie le répertoire racine du package pour une application.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-112">Specifies the package root directory for an application.</span></span>

<a href="" id="-outputfile-or--o"></a>**<span data-ttu-id="f7dc2-113">/OUTPUTFILE ou/O</span><span class="sxs-lookup"><span data-stu-id="f7dc2-113">/OUTPUTFILE or /O</span></span>**  
<span data-ttu-id="f7dc2-114">Spécifie le chemin d’accès et le nom de fichier du fichier SPRJ qui sera généré.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-114">Specifies the path and file name of the SPRJ file that will be generated.</span></span>

<a href="" id="-fullload-or--f"></a>**<span data-ttu-id="f7dc2-115">/FULLLOAD ou/F</span><span class="sxs-lookup"><span data-stu-id="f7dc2-115">/FULLLOAD or /F</span></span>**  
<span data-ttu-id="f7dc2-116">Spécifie si tous les fichiers doivent figurer dans le bloc de fonctionnalités principal.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-116">Specifies whether all files will be contained in the primary feature block.</span></span> <span data-ttu-id="f7dc2-117">Si le paramètre **/FULLLOAD** est spécifié sur la ligne de commande, toutes les données d’application associées sont ajoutées au bloc de fonctionnalités principal.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-117">If the **/FULLLOAD** parameter is specified on the command line, all of the associated application data is added to primary feature block.</span></span> <span data-ttu-id="f7dc2-118">Si le paramètre **/FULLLOAD** n’est pas spécifié sur la ligne de commande, aucune des données d’application associées n’est ajoutée au bloc de fonctionnalités principal.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-118">If the **/FULLLOAD** parameter is not specified on the command line, then none of the associated application data is added to the primary feature block.</span></span>

<a href="" id="-packagename-or--k"></a>**<span data-ttu-id="f7dc2-119">/PACKAGENAME ou/K</span><span class="sxs-lookup"><span data-stu-id="f7dc2-119">/PACKAGENAME or /K</span></span>**  
<span data-ttu-id="f7dc2-120">Spécifie le nom du package qui sera affecté à l’application séquencée.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-120">Specifies the package name that will be assigned to the sequenced application.</span></span>

<a href="" id="-blocksize"></a>**<span data-ttu-id="f7dc2-121">/BLOCKSIZE</span><span class="sxs-lookup"><span data-stu-id="f7dc2-121">/BLOCKSIZE</span></span>**  
<span data-ttu-id="f7dc2-122">Spécifie la taille de bloc de fichiers SFT qui sera utilisée pour diffuser le package sur les ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-122">Specifies the SFT file block size that will be used to stream the package to client computers.</span></span> <span data-ttu-id="f7dc2-123">Vous pouvez sélectionner l’une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="f7dc2-123">You can select one of the following values:</span></span>

-   <span data-ttu-id="f7dc2-124">4 KO</span><span class="sxs-lookup"><span data-stu-id="f7dc2-124">4 KB</span></span>

-   <span data-ttu-id="f7dc2-125">16 KO</span><span class="sxs-lookup"><span data-stu-id="f7dc2-125">16 KB</span></span>

-   <span data-ttu-id="f7dc2-126">32 KO</span><span class="sxs-lookup"><span data-stu-id="f7dc2-126">32 KB</span></span>

-   <span data-ttu-id="f7dc2-127">64 KO</span><span class="sxs-lookup"><span data-stu-id="f7dc2-127">64 KB</span></span>

<span data-ttu-id="f7dc2-128">Vous devez prendre en considération la taille du fichier SFT lorsque vous spécifiez la taille du bloc.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-128">You should consider the size of the SFT file when you specify the block size.</span></span> <span data-ttu-id="f7dc2-129">Le flux d’un fichier dont la taille de blocs est plus petite prend plus de temps sur le réseau, mais nécessite moins de bande passante.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-129">A file with a smaller block size takes longer to stream over the network but is less bandwidth-intensive.</span></span> <span data-ttu-id="f7dc2-130">Les fichiers de tailles de blocs plus grandes utilisent davantage de bande passante réseau.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-130">Files with larger block sizes use more network bandwidth.</span></span>

<a href="" id="-compression"></a>**<span data-ttu-id="f7dc2-131">/COMPRESSION</span><span class="sxs-lookup"><span data-stu-id="f7dc2-131">/COMPRESSION</span></span>**  
<span data-ttu-id="f7dc2-132">Spécifie la méthode permettant de compresser le fichier SFT qui sera transmis au client.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-132">Specifies the method for compressing the SFT file that will be streamed to the client.</span></span>

<a href="" id="-msi-or--m"></a>**<span data-ttu-id="f7dc2-133">/MSI ou/M</span><span class="sxs-lookup"><span data-stu-id="f7dc2-133">/MSI or /M</span></span>**  
<span data-ttu-id="f7dc2-134">Indique si un programme d’installation Windows pour l’application séquencée doit être créé.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-134">Specifies whether a Windows Installer for the sequenced application should be created.</span></span>

<a href="" id="-default"></a>**<span data-ttu-id="f7dc2-135">/DEFAULT</span><span class="sxs-lookup"><span data-stu-id="f7dc2-135">/DEFAULT</span></span>**  
<span data-ttu-id="f7dc2-136">Spécifie le fichier SPRJ par défaut qui sera utilisé lors de la création d’un package d’application virtuel.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-136">Specifies the default SPRJ file that will be used when creating a virtual application package.</span></span> <span data-ttu-id="f7dc2-137">Ce fichier est utilisé comme modèle. sprj lorsque l’application est séquencée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-137">This file is used as the .sprj template when the application is sequenced for the first time.</span></span>

<a href="" id="-upgrade"></a>**<span data-ttu-id="f7dc2-138">/UPGRADE</span><span class="sxs-lookup"><span data-stu-id="f7dc2-138">/UPGRADE</span></span>**  
<span data-ttu-id="f7dc2-139">Spécifie le chemin d’accès et le nom de fichier du fichier SPRJ qui sera mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-139">Specifies the path and file name of the SPRJ file that will be upgraded.</span></span>

<a href="" id="-decodepath"></a>**<span data-ttu-id="f7dc2-140">/DECODEPATH</span><span class="sxs-lookup"><span data-stu-id="f7dc2-140">/DECODEPATH</span></span>**  
<span data-ttu-id="f7dc2-141">Spécifie le répertoire sur l’ordinateur de séquençage dans lequel les fichiers associés au package d’application séquencé sont installés.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-141">Specifies the directory on the sequencing computer where the files associated with the sequenced application package are installed.</span></span> <span data-ttu-id="f7dc2-142">Lorsque vous spécifiez le répertoire, utilisez l’un des formats suivants:</span><span class="sxs-lookup"><span data-stu-id="f7dc2-142">Use one of the following formats when specifying the directory:</span></span>

-   <span data-ttu-id="f7dc2-143">/DECODEPATH: Q:</span><span class="sxs-lookup"><span data-stu-id="f7dc2-143">/decodepath:Q:</span></span>

-   <span data-ttu-id="f7dc2-144">/decodepath:Q:.</span><span class="sxs-lookup"><span data-stu-id="f7dc2-144">/decodepath:Q:.</span></span>

-   <span data-ttu-id="f7dc2-145">/decodepath:"Q:."</span><span class="sxs-lookup"><span data-stu-id="f7dc2-145">/decodepath:”Q:.”</span></span>

-   <span data-ttu-id="f7dc2-146">/DECODEPATH: "Q:"</span><span class="sxs-lookup"><span data-stu-id="f7dc2-146">/decodepath:”Q:”</span></span>

## <span data-ttu-id="f7dc2-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f7dc2-147">Related topics</span></span>


[<span data-ttu-id="f7dc2-148">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="f7dc2-148">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

[<span data-ttu-id="f7dc2-149">Codes des erreurs de ligne de commande de Sequencer</span><span class="sxs-lookup"><span data-stu-id="f7dc2-149">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

 

 





