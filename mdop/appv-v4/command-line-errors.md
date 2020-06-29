---
title: Erreurs de ligne de commande
description: Erreurs de ligne de commande
author: dansimp
ms.assetid: eea62568-4e90-4877-9cc7-e27ef5c05068
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab29a77dc15a8c7bd3590b918a7ca8c1ca6e8c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807894"
---
# <span data-ttu-id="23ab1-103">Erreurs de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="23ab1-103">Command-Line Errors</span></span>


<span data-ttu-id="23ab1-104">Utilisez la liste d’erreurs suivante pour identifier les raisons pour lesquelles le séquençage de la ligne de commande ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="23ab1-104">Use the following list of errors to identify the reasons why command-line sequencing is not working properly.</span></span> <span data-ttu-id="23ab1-105">Vous pouvez également consulter ces erreurs en consultant le fichier journal de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="23ab1-105">You can also see these errors by viewing the sequencer log file.</span></span>

<span data-ttu-id="23ab1-106">**Remarques**  Plus d’une erreur peut s’afficher lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="23ab1-106">**Note** More than one error might be displayed when sequencing.</span></span> <span data-ttu-id="23ab1-107">Par ailleurs, le code d’erreur affiché peut être la somme de deux codes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="23ab1-107">Furthermore, the error code displayed might be the sum of two error codes.</span></span> <span data-ttu-id="23ab1-108">Par exemple, si les paramètres */InstallPath* et */outputfile* ne sont pas répertoriés, le Sequencer de la virtualisation des applications Microsoft System Center renverra 96, c’est-à-dire la somme des deux codes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="23ab1-108">For example, if the */InstallPath* and */OutputFile* parameters are missing, the Microsoft System Center Application Virtualization Sequencer will return 96—the sum of the two error codes.</span></span>

 

<a href="" id="01"></a><span data-ttu-id="23ab1-109">nommée</span><span class="sxs-lookup"><span data-stu-id="23ab1-109">01</span></span>  
<span data-ttu-id="23ab1-110">Il n’y a pas eu d’erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="23ab1-110">There is an unspecified error.</span></span>

<a href="" id="02"></a><span data-ttu-id="23ab1-111">Arrêtés</span><span class="sxs-lookup"><span data-stu-id="23ab1-111">02</span></span>  
<span data-ttu-id="23ab1-112">Le répertoire d’installation spécifié (/INSTALLPACKAGE) spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="23ab1-112">The specified installation directory (/INSTALLPACKAGE) specified is not valid.</span></span>

<a href="" id="04"></a><span data-ttu-id="23ab1-113">04</span><span class="sxs-lookup"><span data-stu-id="23ab1-113">04</span></span>  
<span data-ttu-id="23ab1-114">Le répertoire racine du package spécifié (/INSTALLPATH) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="23ab1-114">The specified package root directory (/INSTALLPATH) is not valid.</span></span>

<a href="" id="08"></a><span data-ttu-id="23ab1-115">0,08</span><span class="sxs-lookup"><span data-stu-id="23ab1-115">08</span></span>  
<span data-ttu-id="23ab1-116">Le paramètre */outputfile* spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="23ab1-116">The */OutputFile* parameter that was specified is not valid.</span></span>

<a href="" id="16"></a><span data-ttu-id="23ab1-117">Seiz</span><span class="sxs-lookup"><span data-stu-id="23ab1-117">16</span></span>  
<span data-ttu-id="23ab1-118">Le répertoire d’installation (/INSTALLPACKAGE) n’a pas été spécifié.</span><span class="sxs-lookup"><span data-stu-id="23ab1-118">The installation directory (/INSTALLPACKAGE) was not specified.</span></span>

<a href="" id="32"></a><span data-ttu-id="23ab1-119">32</span><span class="sxs-lookup"><span data-stu-id="23ab1-119">32</span></span>  
<span data-ttu-id="23ab1-120">Le répertoire racine du package (/INSTALLPATH) n’a pas été spécifié.</span><span class="sxs-lookup"><span data-stu-id="23ab1-120">The package root directory (/INSTALLPATH) was not specified.</span></span>

<a href="" id="64"></a><span data-ttu-id="23ab1-121">64</span><span class="sxs-lookup"><span data-stu-id="23ab1-121">64</span></span>  
<span data-ttu-id="23ab1-122">Le paramètre */outputfile* n’a pas été spécifié.</span><span class="sxs-lookup"><span data-stu-id="23ab1-122">The */OutputFile* parameter was not specified.</span></span>

<a href="" id="128"></a><span data-ttu-id="23ab1-123">128</span><span class="sxs-lookup"><span data-stu-id="23ab1-123">128</span></span>  
<span data-ttu-id="23ab1-124">Le lecteur de virtualisation des applications spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="23ab1-124">The specified application virtualization drive is not valid.</span></span>

<a href="" id="256"></a><span data-ttu-id="23ab1-125">256</span><span class="sxs-lookup"><span data-stu-id="23ab1-125">256</span></span>  
<span data-ttu-id="23ab1-126">Le programme d’installation a échoué.</span><span class="sxs-lookup"><span data-stu-id="23ab1-126">The installer failed.</span></span>

<a href="" id="512"></a><span data-ttu-id="23ab1-127">512</span><span class="sxs-lookup"><span data-stu-id="23ab1-127">512</span></span>  
<span data-ttu-id="23ab1-128">Le séquençage de l’application a échoué.</span><span class="sxs-lookup"><span data-stu-id="23ab1-128">Sequencing the application failed.</span></span>

<a href="" id="1024"></a><span data-ttu-id="23ab1-129">1024</span><span class="sxs-lookup"><span data-stu-id="23ab1-129">1024</span></span>  
<span data-ttu-id="23ab1-130">Échec de l’évaluation des raccourcis installés.</span><span class="sxs-lookup"><span data-stu-id="23ab1-130">Evaluating installed shortcuts failed.</span></span>

<a href="" id="2048"></a><span data-ttu-id="23ab1-131">2048</span><span class="sxs-lookup"><span data-stu-id="23ab1-131">2048</span></span>  
<span data-ttu-id="23ab1-132">Le package d’application séquencé ne peut pas être enregistré.</span><span class="sxs-lookup"><span data-stu-id="23ab1-132">The sequenced application package cannot be saved.</span></span>

<a href="" id="4096"></a><span data-ttu-id="23ab1-133">4096</span><span class="sxs-lookup"><span data-stu-id="23ab1-133">4096</span></span>  
<span data-ttu-id="23ab1-134">Le nom du package spécifié (/PACKAGENAME) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="23ab1-134">The specified package name (/PACKAGENAME) is not valid.</span></span>

<a href="" id="8192"></a><span data-ttu-id="23ab1-135">8192</span><span class="sxs-lookup"><span data-stu-id="23ab1-135">8192</span></span>  
<span data-ttu-id="23ab1-136">La taille de bloc spécifiée (/BLOCKSIZE <em> ) </em> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="23ab1-136">The specified block size (/BLOCKSIZE<em>)</em> is not valid.</span></span>

<a href="" id="16384"></a><span data-ttu-id="23ab1-137">16384</span><span class="sxs-lookup"><span data-stu-id="23ab1-137">16384</span></span>  
<span data-ttu-id="23ab1-138">Le type de compression spécifié (/COMPRESSION) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="23ab1-138">The specified compression type (/COMPRESSION) is not valid.</span></span>

<a href="" id="32768"></a><span data-ttu-id="23ab1-139">32768</span><span class="sxs-lookup"><span data-stu-id="23ab1-139">32768</span></span>  
<span data-ttu-id="23ab1-140">Le chemin de projet spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="23ab1-140">The specified project path is not valid.</span></span>

<a href="" id="65536"></a><span data-ttu-id="23ab1-141">65536</span><span class="sxs-lookup"><span data-stu-id="23ab1-141">65536</span></span>  
<span data-ttu-id="23ab1-142">Le paramètre de mise à niveau spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="23ab1-142">The specified upgrade parameter is not valid.</span></span>

<a href="" id="131072"></a><span data-ttu-id="23ab1-143">131072</span><span class="sxs-lookup"><span data-stu-id="23ab1-143">131072</span></span>  
<span data-ttu-id="23ab1-144">Le paramètre de Project de mise à niveau spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="23ab1-144">The specified upgrade project parameter is not valid.</span></span>

<a href="" id="262144"></a><span data-ttu-id="23ab1-145">262144</span><span class="sxs-lookup"><span data-stu-id="23ab1-145">262144</span></span>  
<span data-ttu-id="23ab1-146">Le paramètre de chemin d’accès de décodage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="23ab1-146">The specified decode path parameter is not valid.</span></span>

<a href="" id="525288"></a><span data-ttu-id="23ab1-147">525288</span><span class="sxs-lookup"><span data-stu-id="23ab1-147">525288</span></span>  
<span data-ttu-id="23ab1-148">Le nom du package n’a pas été spécifié.</span><span class="sxs-lookup"><span data-stu-id="23ab1-148">The package name was not specified.</span></span>

## <span data-ttu-id="23ab1-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23ab1-149">Related topics</span></span>


[<span data-ttu-id="23ab1-150">À propos de l'utilisation de la ligne de commande de Sequencer</span><span class="sxs-lookup"><span data-stu-id="23ab1-150">About Using the Sequencer Command Line</span></span>](about-using-the-sequencer-command-line.md)

[<span data-ttu-id="23ab1-151">Paramètres de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="23ab1-151">Command-Line Parameters</span></span>](command-line-parameters.md)

 

 





