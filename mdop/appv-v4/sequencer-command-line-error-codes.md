---
title: Codes des erreurs de ligne de commande de Sequencer
description: Codes des erreurs de ligne de commande de Sequencer
author: dansimp
ms.assetid: 3d491314-4923-45fd-9839-c541c5e620bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74f5bd0c1b66656ac6891dcc1c019254fa36fdac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806354"
---
# <span data-ttu-id="2e5ae-103">Codes des erreurs de ligne de commande de Sequencer</span><span class="sxs-lookup"><span data-stu-id="2e5ae-103">Sequencer Command-Line Error Codes</span></span>


<span data-ttu-id="2e5ae-104">Utilisez la liste suivante pour vous aider à identifier les erreurs liées au séquençage des applications à l’aide de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-104">Use the following list to help identify errors that are related to sequencing applications by using the command line.</span></span> <span data-ttu-id="2e5ae-105">Vous pouvez également consulter ces informations en consultant le fichier journal App-V du Sequencer associé.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-105">You can also see this information by viewing the associated App-V Sequencer log file.</span></span>

<span data-ttu-id="2e5ae-106">**Remarques**  Plusieurs erreurs peuvent se produire durant le séquençage et, si tel est le cas, le code d’erreur affiché peut être la somme de deux codes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-106">**Note** Multiple errors can occur during sequencing, and if this happens, the error code that is displayed might be the sum of two error codes.</span></span> <span data-ttu-id="2e5ae-107">Par exemple, si les paramètres */InstallPath* et */outputfile* sont manquants, le Sequencer App-V renverra **96**, c’est-à-dire la somme des deux codes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-107">For example, if the */InstallPath* and */OutputFile* parameters are missing, the App-V Sequencer will return **96**—the sum of the two error codes.</span></span>

 

<a href="" id="01"></a><span data-ttu-id="2e5ae-108">nommée</span><span class="sxs-lookup"><span data-stu-id="2e5ae-108">01</span></span>  
<span data-ttu-id="2e5ae-109">Il n’y a pas eu d’erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-109">There is an unspecified error.</span></span>

<a href="" id="02"></a><span data-ttu-id="2e5ae-110">Arrêtés</span><span class="sxs-lookup"><span data-stu-id="2e5ae-110">02</span></span>  
<span data-ttu-id="2e5ae-111">Le répertoire d’installation spécifié (/INSTALLPACKAGE) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-111">The specified installation directory (/INSTALLPACKAGE) is not valid.</span></span>

<a href="" id="04"></a><span data-ttu-id="2e5ae-112">04</span><span class="sxs-lookup"><span data-stu-id="2e5ae-112">04</span></span>  
<span data-ttu-id="2e5ae-113">Le répertoire racine du package spécifié (/INSTALLPATH) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-113">The specified package root directory (/INSTALLPATH) is not valid.</span></span>

<a href="" id="08"></a><span data-ttu-id="2e5ae-114">0,08</span><span class="sxs-lookup"><span data-stu-id="2e5ae-114">08</span></span>  
<span data-ttu-id="2e5ae-115">Le paramètre */outputfile* spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-115">The specified */OutputFile* parameter is not valid.</span></span>

<a href="" id="16"></a><span data-ttu-id="2e5ae-116">Seiz</span><span class="sxs-lookup"><span data-stu-id="2e5ae-116">16</span></span>  
<span data-ttu-id="2e5ae-117">Le répertoire d’installation (/INSTALLPACKAGE) n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-117">The installation directory (/INSTALLPACKAGE) is not specified.</span></span>

<a href="" id="32"></a><span data-ttu-id="2e5ae-118">32</span><span class="sxs-lookup"><span data-stu-id="2e5ae-118">32</span></span>  
<span data-ttu-id="2e5ae-119">Le répertoire racine du package (/INSTALLPATH) n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-119">The package root directory (/INSTALLPATH) is not specified.</span></span>

<a href="" id="64"></a><span data-ttu-id="2e5ae-120">64</span><span class="sxs-lookup"><span data-stu-id="2e5ae-120">64</span></span>  
<span data-ttu-id="2e5ae-121">Le paramètre */outputfile* n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-121">The */OutputFile* parameter is not specified.</span></span>

<a href="" id="128"></a><span data-ttu-id="2e5ae-122">128</span><span class="sxs-lookup"><span data-stu-id="2e5ae-122">128</span></span>  
<span data-ttu-id="2e5ae-123">Le lecteur de virtualisation des applications spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-123">The specified application virtualization drive is not valid.</span></span>

<a href="" id="256"></a><span data-ttu-id="2e5ae-124">256</span><span class="sxs-lookup"><span data-stu-id="2e5ae-124">256</span></span>  
<span data-ttu-id="2e5ae-125">Le programme d’installation a échoué.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-125">The installer failed.</span></span>

<a href="" id="512"></a><span data-ttu-id="2e5ae-126">512</span><span class="sxs-lookup"><span data-stu-id="2e5ae-126">512</span></span>  
<span data-ttu-id="2e5ae-127">Le séquençage de l’application a échoué.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-127">Sequencing the application failed.</span></span>

<a href="" id="1024"></a><span data-ttu-id="2e5ae-128">1024</span><span class="sxs-lookup"><span data-stu-id="2e5ae-128">1024</span></span>  
<span data-ttu-id="2e5ae-129">Échec de l’évaluation des raccourcis installés.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-129">Evaluating installed shortcuts failed.</span></span>

<a href="" id="2048"></a><span data-ttu-id="2e5ae-130">2048</span><span class="sxs-lookup"><span data-stu-id="2e5ae-130">2048</span></span>  
<span data-ttu-id="2e5ae-131">Le package d’application séquencé ne peut pas être enregistré.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-131">The sequenced application package cannot be saved.</span></span>

<a href="" id="4096"></a><span data-ttu-id="2e5ae-132">4096</span><span class="sxs-lookup"><span data-stu-id="2e5ae-132">4096</span></span>  
<span data-ttu-id="2e5ae-133">Le nom du package spécifié (/PACKAGENAME) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-133">The specified package name (/PACKAGENAME) is not valid.</span></span>

<a href="" id="8192"></a><span data-ttu-id="2e5ae-134">8192</span><span class="sxs-lookup"><span data-stu-id="2e5ae-134">8192</span></span>  
<span data-ttu-id="2e5ae-135">La taille de bloc spécifiée (/BLOCKSIZE) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-135">The specified block size (/BLOCKSIZE) is not valid.</span></span>

<a href="" id="16384"></a><span data-ttu-id="2e5ae-136">16384</span><span class="sxs-lookup"><span data-stu-id="2e5ae-136">16384</span></span>  
<span data-ttu-id="2e5ae-137">Le type de compression spécifié (/COMPRESSION) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-137">The specified compression type (/COMPRESSION) is not valid.</span></span>

<a href="" id="32768"></a><span data-ttu-id="2e5ae-138">32768</span><span class="sxs-lookup"><span data-stu-id="2e5ae-138">32768</span></span>  
<span data-ttu-id="2e5ae-139">Le chemin de projet spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-139">The specified project path is not valid.</span></span>

<a href="" id="65536"></a><span data-ttu-id="2e5ae-140">65536</span><span class="sxs-lookup"><span data-stu-id="2e5ae-140">65536</span></span>  
<span data-ttu-id="2e5ae-141">Le paramètre de mise à niveau spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-141">The specified upgrade parameter is not valid.</span></span>

<a href="" id="131072"></a><span data-ttu-id="2e5ae-142">131072</span><span class="sxs-lookup"><span data-stu-id="2e5ae-142">131072</span></span>  
<span data-ttu-id="2e5ae-143">Le paramètre de Project de mise à niveau spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-143">The specified upgrade project parameter is not valid.</span></span>

<a href="" id="262144"></a><span data-ttu-id="2e5ae-144">262144</span><span class="sxs-lookup"><span data-stu-id="2e5ae-144">262144</span></span>  
<span data-ttu-id="2e5ae-145">Le paramètre de chemin d’accès de décodage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-145">The specified decode path parameter is not valid.</span></span>

<a href="" id="525288"></a><span data-ttu-id="2e5ae-146">525288</span><span class="sxs-lookup"><span data-stu-id="2e5ae-146">525288</span></span>  
<span data-ttu-id="2e5ae-147">Le nom du package n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="2e5ae-147">The package name is not specified.</span></span>

## <span data-ttu-id="2e5ae-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2e5ae-148">Related topics</span></span>


[<span data-ttu-id="2e5ae-149">Référence d'Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="2e5ae-149">Application Virtualization Sequencer Reference</span></span>](application-virtualization-sequencer-reference.md)

[<span data-ttu-id="2e5ae-150">Paramètres de ligne de commande de Sequencer</span><span class="sxs-lookup"><span data-stu-id="2e5ae-150">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)

 

 





