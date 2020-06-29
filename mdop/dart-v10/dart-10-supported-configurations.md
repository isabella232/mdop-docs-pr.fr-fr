---
title: Configurations prises en charge par DaRT10
description: Configurations prises en charge par DaRT10
author: dansimp
ms.assetid: a07d6562-1fa9-499f-829c-9cc487ede0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 414b9d5cb7bf78dcfeda3fafc1c476e367709446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804752"
---
# <span data-ttu-id="fe39f-103">Configurations prises en charge par DaRT10</span><span class="sxs-lookup"><span data-stu-id="fe39f-103">DaRT 10 Supported Configurations</span></span>


<span data-ttu-id="fe39f-104">Cette rubrique spécifie les logiciels requis et les configurations de configurations prises en charge nécessaires à l’installation et à l’exécution de Microsoft Diagnostics and Recovery Tools (DaRT) 10 dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="fe39f-104">This topic specifies the prerequisite software and supported configurations requirements that are necessary to install and run Microsoft Diagnostics and Recovery Toolset (DaRT) 10 in your environment.</span></span> <span data-ttu-id="fe39f-105">La configuration requise du système d’exploitation et la configuration requise pour exécuter DaRT 10 sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="fe39f-105">Both the operating system requirements and the system requirements that are required to run DaRT 10 are specified.</span></span> <span data-ttu-id="fe39f-106">Pour plus d’informations sur les conditions préalables à envisager pour créer l’image de récupération DaRT, voir [planification de la création de l’image de récupération DART 10](planning-to-create-the-dart-10-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="fe39f-106">For information about prerequisites that you need to consider to create the DaRT recovery image, see [Planning to Create the DaRT 10 Recovery Image](planning-to-create-the-dart-10-recovery-image.md).</span></span>

<span data-ttu-id="fe39f-107">Pour les configurations prises en charge qui s’appliquent aux versions ultérieures, consultez la documentation de la version en vigueur.</span><span class="sxs-lookup"><span data-stu-id="fe39f-107">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="fe39f-108">Vous pouvez installer DaRT de l’une des deux manières suivantes.</span><span class="sxs-lookup"><span data-stu-id="fe39f-108">You can install DaRT in one of two ways.</span></span> <span data-ttu-id="fe39f-109">Vous pouvez installer toutes les fonctionnalités sur un ordinateur d’administrateur informatique, où vous exécuterez toutes les tâches associées à l’exécution de DaRT.</span><span class="sxs-lookup"><span data-stu-id="fe39f-109">You can install all functionality on an IT administrator computer, where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="fe39f-110">Vous pouvez également installer, sur l’ordinateur d’administration, uniquement la fonctionnalité DaRT qui crée l’image de récupération, puis installer la fonctionnalité utilisée pour exécuter DaRT (autrement dit, la visionneuse de connexion à distance DaRT) sur un ordinateur de bureau d’assistance.</span><span class="sxs-lookup"><span data-stu-id="fe39f-110">Alternatively, you can install, on the administrator computer, only the DaRT functionality that creates the recovery image, and then install the functionality used to run DaRT (that is, the DaRT Remote Connection Viewer) on a help desk computer.</span></span>

## <span data-ttu-id="fe39f-111">Logiciels prérequis DaRT 10</span><span class="sxs-lookup"><span data-stu-id="fe39f-111">DaRT 10 prerequisite software</span></span>


<span data-ttu-id="fe39f-112">Assurez-vous que les conditions préalables suivantes sont remplies avant l’installation de DaRT.</span><span class="sxs-lookup"><span data-stu-id="fe39f-112">Make sure that the following prerequisites are met before you install DaRT.</span></span>

### <span data-ttu-id="fe39f-113">Configuration requise pour les ordinateurs d’administration</span><span class="sxs-lookup"><span data-stu-id="fe39f-113">Administrator computer prerequisites</span></span>

<span data-ttu-id="fe39f-114">Le tableau suivant répertorie les conditions préalables à l’installation de l’ordinateur d’administration lors de l’installation de DaRT 10 et de tous les outils DaRT.</span><span class="sxs-lookup"><span data-stu-id="fe39f-114">The following table lists the installation prerequisites for the administrator computer when you are installing DaRT 10 and all of the DaRT tools.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fe39f-115">Prérequises</span><span class="sxs-lookup"><span data-stu-id="fe39f-115">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="fe39f-116">Détails</span><span class="sxs-lookup"><span data-stu-id="fe39f-116">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fe39f-117">Kit d’évaluation et de développement Windows (ADK)</span><span class="sxs-lookup"><span data-stu-id="fe39f-117">Windows Assessment and Development Kit (ADK)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fe39f-118">Requis pour l’Assistant image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="fe39f-118">Required for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="fe39f-119">Contient les outils de déploiement, qui permettent de personnaliser, de déployer et de traiter les images Windows, et contient l’environnement de préinstallation Windows (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="fe39f-119">Contains the Deployment Tools, which are used to customize, deploy, and service Windows images, and contains the Windows Preinstallation Environment (Windows PE).</span></span> <span data-ttu-id="fe39f-120">Le logiciel ADK n’est pas nécessaire si vous installez uniquement la visionneuse de connexion à distance et/ou l’analyseur d’incident.</span><span class="sxs-lookup"><span data-stu-id="fe39f-120">The ADK is not required if you are installing only the Remote Connection Viewer and/or Crash Analyzer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fe39f-121">Kit de développement Windows ou kit de développement logiciel (facultatif)</span><span class="sxs-lookup"><span data-stu-id="fe39f-121">Windows Development Kit OR Software Development Kit (optional)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fe39f-122">Crash Analyzer nécessite les outils de débogage de Windows 10 du kit de pilotes Windows pour analyser les fichiers de vidage de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe39f-122">Crash Analyzer requires the Windows 10 Debugging Tools from the Windows Driver Kit to analyze memory dump files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fe39f-123">Image ISO Windows 10 64 bits ou 32 bits</span><span class="sxs-lookup"><span data-stu-id="fe39f-123">Windows 10 64-bit or 32-bit ISO image</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fe39f-124">DaRT nécessite l’image de l’environnement de récupération Windows (Windows RE) sur Windows 10 Media.</span><span class="sxs-lookup"><span data-stu-id="fe39f-124">DaRT requires the Windows Recovery Environment (Windows RE) image from the Windows 10 media.</span></span> <span data-ttu-id="fe39f-125">Téléchargez la version 32 de Windows 10 ou 64 bits, en fonction du type d’image de récupération DaRT que vous voulez créer.</span><span class="sxs-lookup"><span data-stu-id="fe39f-125">Download the 32-bit or 64-bit version of Windows 10, depending on the type of DaRT recovery image you want to create.</span></span> <span data-ttu-id="fe39f-126">Si vous prenez en charge les deux types de systèmes dans votre environnement, téléchargez les deux versions de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="fe39f-126">If you support both system types in your environment, download both versions of Windows 10.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="fe39f-127">Configuration requise pour l’ordinateur du support technique</span><span class="sxs-lookup"><span data-stu-id="fe39f-127">Help desk computer prerequisites</span></span>

<span data-ttu-id="fe39f-128">Le tableau suivant répertorie les conditions préalables à l’installation de l’ordinateur de support technique lors de l’exécution de la visionneuse de connexion à distance DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="fe39f-128">The following table lists the installation prerequisites for the help desk computer when you are running the DaRT 10 Remote Connection Viewer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fe39f-129">Prérequises</span><span class="sxs-lookup"><span data-stu-id="fe39f-129">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="fe39f-130">Détails</span><span class="sxs-lookup"><span data-stu-id="fe39f-130">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fe39f-131">Visionneuse de connexion à distance DaRT 10</span><span class="sxs-lookup"><span data-stu-id="fe39f-131">DaRT 10 Remote Connection Viewer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fe39f-132">Doit être installé sur un système d’exploitation Windows 10.</span><span class="sxs-lookup"><span data-stu-id="fe39f-132">Must be installed on a Windows 10 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fe39f-133">Outils de débogage pour Windows</span><span class="sxs-lookup"><span data-stu-id="fe39f-133">Debugging Tools for Windows</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fe39f-134">Requis uniquement lors de l’installation de l’outil Analyseur de blocage</span><span class="sxs-lookup"><span data-stu-id="fe39f-134">Required only if you are installing the Crash Analyzer tool</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="fe39f-135">Conditions préalables sur les ordinateurs des utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="fe39f-135">End-user computer prerequisites</span></span>

<span data-ttu-id="fe39f-136">Il n’y a aucun logiciel requis devant être installé sur les ordinateurs des utilisateurs finaux, à l’exception du système d’exploitation Windows 10.</span><span class="sxs-lookup"><span data-stu-id="fe39f-136">There is no prerequisite software that must be installed on end-user computers, other than the Windows 10 operating system.</span></span>

## <a href="" id="---------dart-10-operating-system-requirements"></a> <span data-ttu-id="fe39f-137">Configuration requise pour le système d’exploitation DaRT 10</span><span class="sxs-lookup"><span data-stu-id="fe39f-137">DaRT 10 operating system requirements</span></span>


### <span data-ttu-id="fe39f-138">Configuration système requise pour l’ordinateur administrateur</span><span class="sxs-lookup"><span data-stu-id="fe39f-138">Administrator computer system requirements</span></span>

<span data-ttu-id="fe39f-139">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de l’ordinateur d’administration DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="fe39f-139">The following table lists the operating systems that are supported for the DaRT 10 administrator computer installation.</span></span>

<span data-ttu-id="fe39f-140">**Remarques**  Vérifiez que vous attribuez suffisamment d’espace pour tout autre outil que vous souhaitez installer sur l’ordinateur d’administration.</span><span class="sxs-lookup"><span data-stu-id="fe39f-140">**Note** Make sure that you allocate enough space for any additional tools that you want to install on the administrator computer.</span></span>

 

<span data-ttu-id="fe39f-141">**Remarques**  Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent.</span><span class="sxs-lookup"><span data-stu-id="fe39f-141">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="fe39f-142">Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="fe39f-142">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="fe39f-143">Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="fe39f-143">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fe39f-144">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="fe39f-144">Operating System</span></span></th>
<th align="left"><span data-ttu-id="fe39f-145">Édition</span><span class="sxs-lookup"><span data-stu-id="fe39f-145">Edition</span></span></th>
<th align="left"><span data-ttu-id="fe39f-146">Service Pack</span><span class="sxs-lookup"><span data-stu-id="fe39f-146">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="fe39f-147">Architecture système</span><span class="sxs-lookup"><span data-stu-id="fe39f-147">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="fe39f-148">Configuration requise pour le système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="fe39f-148">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="fe39f-149">RAM requise pour l’utilisation de DaRT</span><span class="sxs-lookup"><span data-stu-id="fe39f-149">RAM Requirement for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe39f-150">Windows 10</span><span class="sxs-lookup"><span data-stu-id="fe39f-150">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-151">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="fe39f-151">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-152">N/A</span><span class="sxs-lookup"><span data-stu-id="fe39f-152">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-153">64 bits</span><span class="sxs-lookup"><span data-stu-id="fe39f-153">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-154">2 Go</span><span class="sxs-lookup"><span data-stu-id="fe39f-154">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-155">2,5 GO</span><span class="sxs-lookup"><span data-stu-id="fe39f-155">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe39f-156">Windows 10</span><span class="sxs-lookup"><span data-stu-id="fe39f-156">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-157">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="fe39f-157">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-158">N/A</span><span class="sxs-lookup"><span data-stu-id="fe39f-158">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-159">32 bits</span><span class="sxs-lookup"><span data-stu-id="fe39f-159">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-160">1 Go</span><span class="sxs-lookup"><span data-stu-id="fe39f-160">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-161">1,5 GO</span><span class="sxs-lookup"><span data-stu-id="fe39f-161">1.5 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> <span data-ttu-id="fe39f-162">Configuration système requise pour l’ordinateur du support technique DaRT</span><span class="sxs-lookup"><span data-stu-id="fe39f-162">DaRT help desk computer system requirements</span></span>

<span data-ttu-id="fe39f-163">Si vous autorisez un support technique à résoudre des problèmes à distance, vous devez installer la visionneuse de connexions à distance sur l’ordinateur du support technique.</span><span class="sxs-lookup"><span data-stu-id="fe39f-163">If you allow a help desk to remotely troubleshoot computers, you must have the Remote Connection Viewer installed on the help desk computer.</span></span> <span data-ttu-id="fe39f-164">Vous pouvez éventuellement installer l’outil Analyseur d’incident sur l’ordinateur du support technique.</span><span class="sxs-lookup"><span data-stu-id="fe39f-164">You can optionally install the Crash Analyzer tool on the help desk computer.</span></span>

<span data-ttu-id="fe39f-165">DaRT 10 permet à un technicien du support technique de se connecter à un ordinateur DaRT 10 en utilisant le 7,0 DaRT, le DaRT 8,0, le DaRt 8,1 ou la visionneuse de connexion à distance DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="fe39f-165">DaRT 10 enables a help desk worker to connect to a DaRT 10 computer by using either the DaRT 7.0, DaRT 8.0, DaRt 8.1, or DaRT 10 Remote Connection Viewer.</span></span> <span data-ttu-id="fe39f-166">Le Dart 7,0, le DaRT 8,0 et le DaRt 8,1, les visionneuses de connexion à distance nécessitent respectivement les systèmes d’exploitation Windows 7, Windows 8 ou Windows 8,1, même si la visionneuse de connexion à distance DaRT 10 nécessite Windows 10.</span><span class="sxs-lookup"><span data-stu-id="fe39f-166">The DaRT 7.0, DaRT 8.0 and DaRt 8.1, Remote Connection Viewers require Windows 7, Windows 8, or Windows 8.1 operating systems respectively, while the DaRT 10 Remote Connection Viewer requires Windows 10.</span></span> <span data-ttu-id="fe39f-167">La visionneuse de connexion à distance DaRT 10 et tous les autres outils DaRT 10 peuvent être installés uniquement sur un ordinateur exécutant Windows 10.</span><span class="sxs-lookup"><span data-stu-id="fe39f-167">The DaRT 10 Remote Connection Viewer and all other DaRT 10 tools can be installed only on a computer running Windows 10.</span></span>

<span data-ttu-id="fe39f-168">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de l’ordinateur de bureau d’assistance DaRT.</span><span class="sxs-lookup"><span data-stu-id="fe39f-168">The following table lists the operating systems that are supported for the DaRT help desk computer installation.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fe39f-169">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="fe39f-169">Operating System</span></span></th>
<th align="left"><span data-ttu-id="fe39f-170">Édition</span><span class="sxs-lookup"><span data-stu-id="fe39f-170">Edition</span></span></th>
<th align="left"><span data-ttu-id="fe39f-171">Service Pack</span><span class="sxs-lookup"><span data-stu-id="fe39f-171">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="fe39f-172">Architecture système</span><span class="sxs-lookup"><span data-stu-id="fe39f-172">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="fe39f-173">Configuration requise pour le système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="fe39f-173">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="fe39f-174">RAM requise pour l’utilisation de DaRT</span><span class="sxs-lookup"><span data-stu-id="fe39f-174">RAM Requirements for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe39f-175">Windows 10</span><span class="sxs-lookup"><span data-stu-id="fe39f-175">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-176">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="fe39f-176">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-177">N/A</span><span class="sxs-lookup"><span data-stu-id="fe39f-177">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-178">64 bits</span><span class="sxs-lookup"><span data-stu-id="fe39f-178">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-179">2 Go</span><span class="sxs-lookup"><span data-stu-id="fe39f-179">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-180">2,5 GO</span><span class="sxs-lookup"><span data-stu-id="fe39f-180">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe39f-181">Windows 10 (avec la visionneuse de connexion à distance 10,0 uniquement)</span><span class="sxs-lookup"><span data-stu-id="fe39f-181">Windows10 (with Remote Connection Viewer 10.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-182">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="fe39f-182">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-183">N/A</span><span class="sxs-lookup"><span data-stu-id="fe39f-183">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-184">32 bits</span><span class="sxs-lookup"><span data-stu-id="fe39f-184">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-185">1 Go</span><span class="sxs-lookup"><span data-stu-id="fe39f-185">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-186">1,5 GO</span><span class="sxs-lookup"><span data-stu-id="fe39f-186">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe39f-187">Windows8</span><span class="sxs-lookup"><span data-stu-id="fe39f-187">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-188">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="fe39f-188">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-189">N/A</span><span class="sxs-lookup"><span data-stu-id="fe39f-189">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-190">64 bits</span><span class="sxs-lookup"><span data-stu-id="fe39f-190">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-191">2 Go</span><span class="sxs-lookup"><span data-stu-id="fe39f-191">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-192">2,5 GO</span><span class="sxs-lookup"><span data-stu-id="fe39f-192">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe39f-193">Windows8 (avec la visionneuse de connexion à distance 8,0 uniquement)</span><span class="sxs-lookup"><span data-stu-id="fe39f-193">Windows8 (with Remote Connection Viewer 8.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-194">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="fe39f-194">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-195">N/A</span><span class="sxs-lookup"><span data-stu-id="fe39f-195">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-196">32 bits</span><span class="sxs-lookup"><span data-stu-id="fe39f-196">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-197">1 Go</span><span class="sxs-lookup"><span data-stu-id="fe39f-197">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-198">1,5 GO</span><span class="sxs-lookup"><span data-stu-id="fe39f-198">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe39f-199">Windows 7 (avec la visionneuse de connexions à distance 7,0 uniquement)</span><span class="sxs-lookup"><span data-stu-id="fe39f-199">Windows 7 (with Remote Connection Viewer 7.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-200">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="fe39f-200">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-201">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="fe39f-201">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-202">64 bits ou 32 bits</span><span class="sxs-lookup"><span data-stu-id="fe39f-202">64-bit or 32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-203">1 Go</span><span class="sxs-lookup"><span data-stu-id="fe39f-203">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-204">N/A</span><span class="sxs-lookup"><span data-stu-id="fe39f-204">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe39f-205">WindowsServer2012</span><span class="sxs-lookup"><span data-stu-id="fe39f-205">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-206">Standard, entreprise, centre de données</span><span class="sxs-lookup"><span data-stu-id="fe39f-206">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-207">N/A</span><span class="sxs-lookup"><span data-stu-id="fe39f-207">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-208">64 bits</span><span class="sxs-lookup"><span data-stu-id="fe39f-208">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-209">2 Go</span><span class="sxs-lookup"><span data-stu-id="fe39f-209">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-210">1,0 GO</span><span class="sxs-lookup"><span data-stu-id="fe39f-210">1.0 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe39f-211">WindowsServer2012R2</span><span class="sxs-lookup"><span data-stu-id="fe39f-211">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-212">Standard, entreprise, centre de données</span><span class="sxs-lookup"><span data-stu-id="fe39f-212">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-213">N/A</span><span class="sxs-lookup"><span data-stu-id="fe39f-213">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-214">64 bits</span><span class="sxs-lookup"><span data-stu-id="fe39f-214">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-215">2 Go</span><span class="sxs-lookup"><span data-stu-id="fe39f-215">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-216">1,0 GO</span><span class="sxs-lookup"><span data-stu-id="fe39f-216">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="fe39f-217">Le DaRT a également besoin de la configuration matérielle minimum suivante pour l’ordinateur de l’utilisateur final:</span><span class="sxs-lookup"><span data-stu-id="fe39f-217">DaRT also has the following minimum hardware requirements for the end-user computer:</span></span>

<span data-ttu-id="fe39f-218">Un CD ou un DVD ou un port USB-requis uniquement si vous déployez DaRT au sein de votre entreprise à l’aide d’un CD, d’un DVD ou d’un lecteur USB.</span><span class="sxs-lookup"><span data-stu-id="fe39f-218">A CD or DVD drive or a USB port - required only if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.</span></span>

<span data-ttu-id="fe39f-219">Prise en charge du BIOS pour le démarrage de l’ordinateur à partir d’un CD ou d’un DVD, d’une clé USB ou d’une partition distante ou de restauration.</span><span class="sxs-lookup"><span data-stu-id="fe39f-219">BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition.</span></span>

### <a href="" id="-------------dart-10-end-user-computer-system-requirements"></a> <span data-ttu-id="fe39f-220">Configuration requise pour l’ordinateur de l’utilisateur final de DaRT 10</span><span class="sxs-lookup"><span data-stu-id="fe39f-220">DaRT 10 end-user computer system requirements</span></span>

<span data-ttu-id="fe39f-221">La fenêtre du jeu d’outils de diagnostics et de récupération dans DaRT 10 nécessite que l’ordinateur de l’utilisateur final utilise l’un des systèmes d’exploitation suivants avec la quantité de mémoire système spécifique disponible pour DaRT:</span><span class="sxs-lookup"><span data-stu-id="fe39f-221">The Diagnostics and Recovery Toolset window in DaRT 10 requires that the end-user computer use one of the following operating systems together with the specified amount of system memory available for DaRT:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fe39f-222">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="fe39f-222">Operating System</span></span></th>
<th align="left"><span data-ttu-id="fe39f-223">Édition</span><span class="sxs-lookup"><span data-stu-id="fe39f-223">Edition</span></span></th>
<th align="left"><span data-ttu-id="fe39f-224">Service Pack</span><span class="sxs-lookup"><span data-stu-id="fe39f-224">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="fe39f-225">Architecture système</span><span class="sxs-lookup"><span data-stu-id="fe39f-225">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="fe39f-226">Configuration requise pour le système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="fe39f-226">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="fe39f-227">RAM requise</span><span class="sxs-lookup"><span data-stu-id="fe39f-227">RAM Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fe39f-228">Windows 10</span><span class="sxs-lookup"><span data-stu-id="fe39f-228">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-229">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="fe39f-229">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-230">N/A</span><span class="sxs-lookup"><span data-stu-id="fe39f-230">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-231">64 bits</span><span class="sxs-lookup"><span data-stu-id="fe39f-231">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-232">2 Go</span><span class="sxs-lookup"><span data-stu-id="fe39f-232">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-233">2,5 GO</span><span class="sxs-lookup"><span data-stu-id="fe39f-233">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fe39f-234">Windows 10</span><span class="sxs-lookup"><span data-stu-id="fe39f-234">Windows10</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-235">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="fe39f-235">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-236">N/A</span><span class="sxs-lookup"><span data-stu-id="fe39f-236">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-237">32 bits</span><span class="sxs-lookup"><span data-stu-id="fe39f-237">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-238">1 Go</span><span class="sxs-lookup"><span data-stu-id="fe39f-238">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="fe39f-239">1,5 GO</span><span class="sxs-lookup"><span data-stu-id="fe39f-239">1.5 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="fe39f-240">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe39f-240">Related topics</span></span>


[<span data-ttu-id="fe39f-241">Planification du déploiement de DaRT10</span><span class="sxs-lookup"><span data-stu-id="fe39f-241">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 





