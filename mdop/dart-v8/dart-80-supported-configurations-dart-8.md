---
title: Configurations prises en charge par DaRT8.0
description: Configurations prises en charge par DaRT8.0
author: dansimp
ms.assetid: 95d68e5c-d202-4f4a-adef-d2098328172e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02c891555992652bf2a9b2b674ab8377536ef9d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810248"
---
# <span data-ttu-id="5f540-103">Configurations prises en charge par DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="5f540-103">DaRT 8.0 Supported Configurations</span></span>


<span data-ttu-id="5f540-104">Cette rubrique spécifie les logiciels requis et la configuration requise pour les configurations prises en charge pour l’installation et l’exécution de Microsoft Diagnostics and Recovery Tools (DaRT) 8,0 dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="5f540-104">This topic specifies the prerequisite software and supported configurations requirements that are necessary to install and run Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 in your environment.</span></span> <span data-ttu-id="5f540-105">La configuration requise du système d’exploitation et la configuration système requise pour exécuter DaRT 8,0 sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="5f540-105">Both the operating system requirements and the system requirements that are required to run DaRT 8.0 are specified.</span></span> <span data-ttu-id="5f540-106">Pour plus d’informations sur les conditions préalables à envisager pour créer l’image de récupération DaRT, voir [planification de la création de l’image de récupération 8,0 de DART](planning-to-create-the-dart-80-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="5f540-106">For information about prerequisites that you need to consider to create the DaRT recovery image, see [Planning to Create the DaRT 8.0 Recovery Image](planning-to-create-the-dart-80-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="5f540-107">Pour les configurations prises en charge qui s’appliquent aux versions ultérieures, consultez la documentation de la version en vigueur.</span><span class="sxs-lookup"><span data-stu-id="5f540-107">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="5f540-108">Vous pouvez installer DaRT de l’une des deux manières suivantes.</span><span class="sxs-lookup"><span data-stu-id="5f540-108">You can install DaRT in one of two ways.</span></span> <span data-ttu-id="5f540-109">Vous pouvez installer toutes les fonctionnalités sur un ordinateur d’administrateur informatique, où vous exécuterez toutes les tâches associées à l’exécution de DaRT.</span><span class="sxs-lookup"><span data-stu-id="5f540-109">You can install all functionality on an IT administrator computer, where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="5f540-110">Vous pouvez également installer, sur l’ordinateur d’administration, uniquement la fonctionnalité DaRT qui crée l’image de récupération, puis installer la fonctionnalité utilisée pour exécuter DaRT (autrement dit, la visionneuse de connexion à distance DaRT) sur un ordinateur de bureau d’assistance.</span><span class="sxs-lookup"><span data-stu-id="5f540-110">Alternatively, you can install, on the administrator computer, only the DaRT functionality that creates the recovery image, and then install the functionality used to run DaRT (that is, the DaRT Remote Connection Viewer) on a help desk computer.</span></span>

## <a href="" id="---------dart-8-0-prerequisite-software"></a> <span data-ttu-id="5f540-111">Logiciels prérequis de DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="5f540-111">DaRT 8.0 prerequisite software</span></span>


<span data-ttu-id="5f540-112">Assurez-vous que les conditions préalables suivantes sont remplies avant l’installation de DaRT.</span><span class="sxs-lookup"><span data-stu-id="5f540-112">Make sure that the following prerequisites are met before you install DaRT.</span></span>

### <span data-ttu-id="5f540-113">Configuration requise pour les ordinateurs d’administration</span><span class="sxs-lookup"><span data-stu-id="5f540-113">Administrator computer prerequisites</span></span>

<span data-ttu-id="5f540-114">Le tableau suivant répertorie les conditions préalables à l’installation de l’ordinateur d’administration lors de l’installation de DaRT 8,0 et de tous les outils DaRT.</span><span class="sxs-lookup"><span data-stu-id="5f540-114">The following table lists the installation prerequisites for the administrator computer when you are installing DaRT 8.0 and all of the DaRT tools.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f540-115">Prérequises</span><span class="sxs-lookup"><span data-stu-id="5f540-115">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="5f540-116">Détails</span><span class="sxs-lookup"><span data-stu-id="5f540-116">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5f540-117">Kit d’évaluation et de développement Windows (ADK)</span><span class="sxs-lookup"><span data-stu-id="5f540-117">Windows Assessment and Development Kit (ADK)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5f540-118">Requis pour l’Assistant image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="5f540-118">Required for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="5f540-119">Contient les outils de déploiement, qui permettent de personnaliser, de déployer et de traiter les images Windows, et contient l’environnement de préinstallation Windows (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="5f540-119">Contains the Deployment Tools, which are used to customize, deploy, and service Windows images, and contains the Windows Preinstallation Environment (Windows PE).</span></span> <span data-ttu-id="5f540-120">Le logiciel ADK n’est pas nécessaire si vous installez uniquement la visionneuse de connexion à distance et/ou l’analyseur d’incident.</span><span class="sxs-lookup"><span data-stu-id="5f540-120">The ADK is not required if you are installing only the Remote Connection Viewer and/or Crash Analyzer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5f540-121">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="5f540-121">.NET Framework 4.5</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5f540-122">Requis par l’Assistant image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="5f540-122">Required by the DaRT Recovery Image wizard.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5f540-123">Kit de développement Windows ou kit de développement logiciel (facultatif)</span><span class="sxs-lookup"><span data-stu-id="5f540-123">Windows Development Kit OR Software Development Kit (optional)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5f540-124">Crash Analyzer nécessite les outils de débogage de Windows 8 du kit de pilotes Windows pour analyser les fichiers de vidage de mémoire.</span><span class="sxs-lookup"><span data-stu-id="5f540-124">Crash Analyzer requires the Windows 8 Debugging Tools from the Windows Driver Kit to analyze memory dump files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5f540-125">Image ISO Windows 8 64 bits</span><span class="sxs-lookup"><span data-stu-id="5f540-125">Windows 8 64-bit ISO image</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5f540-126">DaRT nécessite l’image de l’environnement de récupération Windows sur Windows 8 Media.</span><span class="sxs-lookup"><span data-stu-id="5f540-126">DaRT requires the Windows Recovery Environment (Windows RE) image from the Windows 8 media.</span></span> <span data-ttu-id="5f540-127">Téléchargez la version 32 bits ou 64 bits de Windows 8, en fonction du type d’image de récupération DaRT que vous voulez créer.</span><span class="sxs-lookup"><span data-stu-id="5f540-127">Download the 32-bit or 64-bit version of Windows 8, depending on the type of DaRT recovery image you want to create.</span></span> <span data-ttu-id="5f540-128">Si vous prenez en charge les deux types de systèmes dans votre environnement, téléchargez les deux versions de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5f540-128">If you support both system types in your environment, download both versions of Windows 8.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="5f540-129">Configuration requise pour l’ordinateur du support technique</span><span class="sxs-lookup"><span data-stu-id="5f540-129">Help desk computer prerequisites</span></span>

<span data-ttu-id="5f540-130">Le tableau suivant répertorie les conditions préalables à l’installation de l’ordinateur de support technique lors de l’exécution de la visionneuse de connexion à distance DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="5f540-130">The following table lists the installation prerequisites for the help desk computer when you are running the DaRT 8.0 Remote Connection Viewer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f540-131">Prérequises</span><span class="sxs-lookup"><span data-stu-id="5f540-131">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="5f540-132">Détails</span><span class="sxs-lookup"><span data-stu-id="5f540-132">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5f540-133">Visionneuse de connexions à distance DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="5f540-133">DaRT 8.0 Remote Connection Viewer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5f540-134">Doit être installé sur un système d’exploitation Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5f540-134">Must be installed on a Windows 8 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="5f540-135">.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="5f540-135">NET Framework 4.5</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5f540-136">Requis par l’Assistant image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="5f540-136">Required by the DaRT Recovery Image wizard</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="5f540-137">Outils de débogage pour Windows</span><span class="sxs-lookup"><span data-stu-id="5f540-137">Debugging Tools for Windows</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="5f540-138">Requis uniquement lors de l’installation de l’outil Analyseur de blocage</span><span class="sxs-lookup"><span data-stu-id="5f540-138">Required only if you are installing the Crash Analyzer tool</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="5f540-139">Conditions préalables sur les ordinateurs des utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="5f540-139">End-user computer prerequisites</span></span>

<span data-ttu-id="5f540-140">Aucun logiciel requis ne doit être installé sur les ordinateurs des utilisateurs finaux, autre que le système d’exploitation Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5f540-140">There is no prerequisite software that must be installed on end-user computers, other than the Windows 8 operating system.</span></span>

## <a href="" id="---------dart-operating-system-requirements"></a> <span data-ttu-id="5f540-141">Configuration requise pour le système d’exploitation DaRT</span><span class="sxs-lookup"><span data-stu-id="5f540-141">DaRT operating system requirements</span></span>


### <span data-ttu-id="5f540-142">Configuration système requise pour l’ordinateur administrateur</span><span class="sxs-lookup"><span data-stu-id="5f540-142">Administrator computer system requirements</span></span>

<span data-ttu-id="5f540-143">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de l’ordinateur d’administration DaRT.</span><span class="sxs-lookup"><span data-stu-id="5f540-143">The following table lists the operating systems that are supported for the DaRT administrator computer installation.</span></span>

<span data-ttu-id="5f540-144">**Remarques**  Vérifiez que vous attribuez suffisamment d’espace pour tout autre outil que vous souhaitez installer sur l’ordinateur d’administration.</span><span class="sxs-lookup"><span data-stu-id="5f540-144">**Note** Make sure that you allocate enough space for any additional tools that you want to install on the administrator computer.</span></span>

 

<span data-ttu-id="5f540-145">**Remarques**  Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent.</span><span class="sxs-lookup"><span data-stu-id="5f540-145">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="5f540-146">Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="5f540-146">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="5f540-147">Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="5f540-147">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

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
<th align="left"><span data-ttu-id="5f540-148">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="5f540-148">Operating System</span></span></th>
<th align="left"><span data-ttu-id="5f540-149">Édition</span><span class="sxs-lookup"><span data-stu-id="5f540-149">Edition</span></span></th>
<th align="left"><span data-ttu-id="5f540-150">Service Pack</span><span class="sxs-lookup"><span data-stu-id="5f540-150">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="5f540-151">Architecture système</span><span class="sxs-lookup"><span data-stu-id="5f540-151">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="5f540-152">Configuration requise pour le système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="5f540-152">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="5f540-153">RAM requise pour l’utilisation de DaRT</span><span class="sxs-lookup"><span data-stu-id="5f540-153">RAM Requirement for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f540-154">Windows8</span><span class="sxs-lookup"><span data-stu-id="5f540-154">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-155">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="5f540-155">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-156">N/A</span><span class="sxs-lookup"><span data-stu-id="5f540-156">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-157">64 bits</span><span class="sxs-lookup"><span data-stu-id="5f540-157">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-158">2 Go</span><span class="sxs-lookup"><span data-stu-id="5f540-158">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-159">2,5 GO</span><span class="sxs-lookup"><span data-stu-id="5f540-159">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f540-160">Windows8</span><span class="sxs-lookup"><span data-stu-id="5f540-160">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-161">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="5f540-161">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-162">N/A</span><span class="sxs-lookup"><span data-stu-id="5f540-162">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-163">32 bits</span><span class="sxs-lookup"><span data-stu-id="5f540-163">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-164">1 Go</span><span class="sxs-lookup"><span data-stu-id="5f540-164">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-165">1,5 GO</span><span class="sxs-lookup"><span data-stu-id="5f540-165">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f540-166">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="5f540-166">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-167">Standard, entreprise, centre de données</span><span class="sxs-lookup"><span data-stu-id="5f540-167">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-168">N/A</span><span class="sxs-lookup"><span data-stu-id="5f540-168">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-169">64 bits</span><span class="sxs-lookup"><span data-stu-id="5f540-169">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-170">512 MO</span><span class="sxs-lookup"><span data-stu-id="5f540-170">512 MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-171">1.0 GO</span><span class="sxs-lookup"><span data-stu-id="5f540-171">1 .0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> <span data-ttu-id="5f540-172">Configuration système requise pour l’ordinateur du support technique DaRT</span><span class="sxs-lookup"><span data-stu-id="5f540-172">DaRT help desk computer system requirements</span></span>

<span data-ttu-id="5f540-173">Si vous autorisez un support technique à résoudre des problèmes à distance, vous devez installer la visionneuse de connexions à distance sur l’ordinateur du support technique.</span><span class="sxs-lookup"><span data-stu-id="5f540-173">If you allow a help desk to remotely troubleshoot computers, you must have the Remote Connection Viewer installed on the help desk computer.</span></span> <span data-ttu-id="5f540-174">Vous pouvez éventuellement installer l’outil Analyseur d’incident sur l’ordinateur du support technique.</span><span class="sxs-lookup"><span data-stu-id="5f540-174">You can optionally install the Crash Analyzer tool on the help desk computer.</span></span>

<span data-ttu-id="5f540-175">Le DaRT 8,0 permet à un service d’assistance technique de se connecter à un ordinateur DaRT 8,0 à l’aide de la visionneuse de connexions à distance Dart 7,0 ou DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="5f540-175">DaRT 8.0 enables a help desk worker to connect to a DaRT 8.0 computer by using either the DaRT 7.0 or DaRT 8.0 Remote Connection Viewer.</span></span> <span data-ttu-id="5f540-176">La visionneuse de connexions à distance DaRT 7,0 nécessite un système d’exploitation Windows 7, tandis que la visionneuse de connexion à distance DaRT 8,0 nécessite Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5f540-176">The DaRT 7.0 Remote Connection Viewer requires a Windows 7 operating system, while the DaRT 8.0 Remote Connection Viewer requires Windows 8.</span></span> <span data-ttu-id="5f540-177">La visionneuse de connexion à distance DaRT 8,0 et tous les autres outils DaRT 8,0 peuvent être installés uniquement sur un ordinateur exécutant Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5f540-177">The DaRT 8.0 Remote Connection Viewer and all other DaRT 8.0 tools can be installed only on a computer running Windows 8.</span></span>

<span data-ttu-id="5f540-178">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de l’ordinateur de bureau d’assistance DaRT.</span><span class="sxs-lookup"><span data-stu-id="5f540-178">The following table lists the operating systems that are supported for the DaRT help desk computer installation.</span></span>

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
<th align="left"><span data-ttu-id="5f540-179">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="5f540-179">Operating System</span></span></th>
<th align="left"><span data-ttu-id="5f540-180">Édition</span><span class="sxs-lookup"><span data-stu-id="5f540-180">Edition</span></span></th>
<th align="left"><span data-ttu-id="5f540-181">Service Pack</span><span class="sxs-lookup"><span data-stu-id="5f540-181">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="5f540-182">Architecture système</span><span class="sxs-lookup"><span data-stu-id="5f540-182">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="5f540-183">Configuration requise pour le système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="5f540-183">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="5f540-184">RAM requise pour l’utilisation de DaRT</span><span class="sxs-lookup"><span data-stu-id="5f540-184">RAM Requirements for Running DaRT</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f540-185">Windows8</span><span class="sxs-lookup"><span data-stu-id="5f540-185">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-186">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="5f540-186">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-187">N/A</span><span class="sxs-lookup"><span data-stu-id="5f540-187">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-188">64 bits</span><span class="sxs-lookup"><span data-stu-id="5f540-188">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-189">2 Go</span><span class="sxs-lookup"><span data-stu-id="5f540-189">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-190">2,5 GO</span><span class="sxs-lookup"><span data-stu-id="5f540-190">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f540-191">Windows8 (avec la visionneuse de connexion à distance 8,0 uniquement)</span><span class="sxs-lookup"><span data-stu-id="5f540-191">Windows8 (with Remote Connection Viewer 8.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-192">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="5f540-192">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-193">N/A</span><span class="sxs-lookup"><span data-stu-id="5f540-193">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-194">32 bits</span><span class="sxs-lookup"><span data-stu-id="5f540-194">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-195">1 Go</span><span class="sxs-lookup"><span data-stu-id="5f540-195">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-196">1,5 GO</span><span class="sxs-lookup"><span data-stu-id="5f540-196">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f540-197">Windows 7 (avec la visionneuse de connexions à distance 7,0 uniquement)</span><span class="sxs-lookup"><span data-stu-id="5f540-197">Windows 7 (with Remote Connection Viewer 7.0 only)</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-198">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="5f540-198">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-199">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="5f540-199">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-200">64 bits ou 32 bits</span><span class="sxs-lookup"><span data-stu-id="5f540-200">64-bit or 32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-201">1 Go</span><span class="sxs-lookup"><span data-stu-id="5f540-201">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-202">N/A</span><span class="sxs-lookup"><span data-stu-id="5f540-202">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f540-203">WindowsServer2012</span><span class="sxs-lookup"><span data-stu-id="5f540-203">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-204">Standard, entreprise, centre de données</span><span class="sxs-lookup"><span data-stu-id="5f540-204">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-205">N/A</span><span class="sxs-lookup"><span data-stu-id="5f540-205">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-206">64 bits</span><span class="sxs-lookup"><span data-stu-id="5f540-206">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-207">51</span><span class="sxs-lookup"><span data-stu-id="5f540-207">51</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-208">1,0 GO</span><span class="sxs-lookup"><span data-stu-id="5f540-208">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="5f540-209">Le DaRT a également besoin de la configuration matérielle minimum suivante pour l’ordinateur de l’utilisateur final:</span><span class="sxs-lookup"><span data-stu-id="5f540-209">DaRT also has the following minimum hardware requirements for the end-user computer:</span></span>

<span data-ttu-id="5f540-210">Un CD ou un DVD ou un port USB-requis uniquement si vous déployez DaRT au sein de votre entreprise à l’aide d’un CD, d’un DVD ou d’un lecteur USB.</span><span class="sxs-lookup"><span data-stu-id="5f540-210">A CD or DVD drive or a USB port - required only if you are deploying DaRT in your enterprise by using a CD, DVD, or USB.</span></span>

<span data-ttu-id="5f540-211">Prise en charge du BIOS pour le démarrage de l’ordinateur à partir d’un CD ou d’un DVD, d’une clé USB ou d’une partition distante ou de restauration.</span><span class="sxs-lookup"><span data-stu-id="5f540-211">BIOS support for starting the computer from a CD or DVD, a USB flash drive, or from a remote or recovery partition.</span></span>

### <a href="" id="-------------dart-end-user-computer-system-requirements"></a> <span data-ttu-id="5f540-212">Configuration système requise pour l’ordinateur de l’utilisateur final DaRT</span><span class="sxs-lookup"><span data-stu-id="5f540-212">DaRT end-user computer system requirements</span></span>

<span data-ttu-id="5f540-213">La fenêtre du jeu d’outils de diagnostics et de récupération dans DaRT nécessite que l’ordinateur de l’utilisateur final utilise l’un des systèmes d’exploitation suivants avec la quantité de mémoire système disponible pour DaRT:</span><span class="sxs-lookup"><span data-stu-id="5f540-213">The Diagnostics and Recovery Toolset window in DaRT requires that the end-user computer use one of the following operating systems together with the specified amount of system memory available for DaRT:</span></span>

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
<th align="left"><span data-ttu-id="5f540-214">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="5f540-214">Operating System</span></span></th>
<th align="left"><span data-ttu-id="5f540-215">Édition</span><span class="sxs-lookup"><span data-stu-id="5f540-215">Edition</span></span></th>
<th align="left"><span data-ttu-id="5f540-216">Service Pack</span><span class="sxs-lookup"><span data-stu-id="5f540-216">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="5f540-217">Architecture système</span><span class="sxs-lookup"><span data-stu-id="5f540-217">System Architecture</span></span></th>
<th align="left"><span data-ttu-id="5f540-218">Configuration requise pour le système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="5f540-218">Operating System Requirements</span></span></th>
<th align="left"><span data-ttu-id="5f540-219">RAM requise</span><span class="sxs-lookup"><span data-stu-id="5f540-219">RAM Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f540-220">Windows8</span><span class="sxs-lookup"><span data-stu-id="5f540-220">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-221">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="5f540-221">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-222">N/A</span><span class="sxs-lookup"><span data-stu-id="5f540-222">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-223">64 bits</span><span class="sxs-lookup"><span data-stu-id="5f540-223">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-224">2 Go</span><span class="sxs-lookup"><span data-stu-id="5f540-224">2 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-225">2,5 GO</span><span class="sxs-lookup"><span data-stu-id="5f540-225">2.5 GB</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f540-226">Windows8</span><span class="sxs-lookup"><span data-stu-id="5f540-226">Windows8</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-227">Toutes les éditions</span><span class="sxs-lookup"><span data-stu-id="5f540-227">All editions</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-228">N/A</span><span class="sxs-lookup"><span data-stu-id="5f540-228">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-229">32 bits</span><span class="sxs-lookup"><span data-stu-id="5f540-229">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-230">1 Go</span><span class="sxs-lookup"><span data-stu-id="5f540-230">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-231">1,5 GO</span><span class="sxs-lookup"><span data-stu-id="5f540-231">1.5 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f540-232">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="5f540-232">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-233">Standard, entreprise, centre de données</span><span class="sxs-lookup"><span data-stu-id="5f540-233">Standard, Enterprise, Data Center</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-234">N/A</span><span class="sxs-lookup"><span data-stu-id="5f540-234">N/A</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-235">64 bits</span><span class="sxs-lookup"><span data-stu-id="5f540-235">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-236">512 MO</span><span class="sxs-lookup"><span data-stu-id="5f540-236">512 MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f540-237">1,0 GO</span><span class="sxs-lookup"><span data-stu-id="5f540-237">1.0 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5f540-238">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f540-238">Related topics</span></span>


[<span data-ttu-id="5f540-239">Planification du déploiement de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="5f540-239">Planning to Deploy DaRT 8.0</span></span>](planning-to-deploy-dart-80-dart-8.md)

 

 





