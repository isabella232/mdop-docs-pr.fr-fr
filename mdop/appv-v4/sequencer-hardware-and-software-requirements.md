---
title: Configuration matérielle et logicielle requise pour Sequencer
description: Configuration matérielle et logicielle requise pour Sequencer
author: dansimp
ms.assetid: 36084e12-831d-452f-a4a4-45f07f9ce471
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d4e12a5803a3c9033513424826b49bc0bca5885
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806345"
---
# <span data-ttu-id="8ceb5-103">Configuration matérielle et logicielle requise pour Sequencer</span><span class="sxs-lookup"><span data-stu-id="8ceb5-103">Sequencer Hardware and Software Requirements</span></span>


<span data-ttu-id="8ceb5-104">Cette rubrique décrit la configuration matérielle et logicielle minimale recommandée pour l’ordinateur exécutant le Sequencer Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="8ceb5-104">This topic describes the minimum recommended hardware and software requirements for the computer running the Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<span data-ttu-id="8ceb5-105">Avant d’installer le Sequencer et après avoir séquencé chaque application, vous devez restaurer une nouvelle image de système d’exploitation sur l’ordinateur de séquençage.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-105">Before you install the Sequencer and after you sequence each application, you must restore a clean operating system image to the sequencing computer.</span></span> <span data-ttu-id="8ceb5-106">Pour restaurer l’ordinateur exécutant le Sequencer, vous pouvez utiliser l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="8ceb5-106">You can use one of the following methods to restore the computer running the Sequencer:</span></span>

-   <span data-ttu-id="8ceb5-107">Remettez en forme le disque dur, puis réinstallez le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-107">Reformat the hard drive and reinstall the operating system.</span></span>

-   <span data-ttu-id="8ceb5-108">Restaurez le disque dur sur l’ordinateur exécutant l’image de Sequencer à l’aide d’un autre logiciel d’imagerie de disque.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-108">Restore the hard drive on the computer running the Sequencer image by using another disk-imaging software.</span></span>

<span data-ttu-id="8ceb5-109">La liste suivante présente la configuration matérielle requise pour exécuter le Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-109">The following list outlines the recommended hardware requirements for running the App-V Sequencer.</span></span>

### <a href="" id="hardware-requirements-"></a><span data-ttu-id="8ceb5-110">Configuration matérielle requise</span><span class="sxs-lookup"><span data-stu-id="8ceb5-110">Hardware Requirements</span></span>

-   <span data-ttu-id="8ceb5-111">Processeur: Intel Pentium III, 1 GHz (32-bit ou 64 bits).</span><span class="sxs-lookup"><span data-stu-id="8ceb5-111">Processor—Intel Pentium III, 1 GHz (32-bit or 64-bit).</span></span> <span data-ttu-id="8ceb5-112">Le processus de séquençage est un processus à thread unique qui ne tire pas parti de deux processeurs.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-112">The sequencing process is a single-threaded process and does not take advantage of dual processors.</span></span>

-   <span data-ttu-id="8ceb5-113">Mémoire: 1 Go ou plus, 2 Go recommandés.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-113">Memory—1GB or above, 2 GB recommended.</span></span>

-   <span data-ttu-id="8ceb5-114">Disque dur: 40 gigaoctets (Go) d’espace disque disponible d’au moins 15 Go d’espace libre sur le disque dur.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-114">Hard Disk—40 gigabyte (GB) hard disk space with a minimum of 15 GB available hard disk space.</span></span> <span data-ttu-id="8ceb5-115">Nous vous recommandons d’avoir au moins trois fois l’espace disque disponible requis par l’application.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-115">We recommend that you have at least three times the hard disk space that the application you are sequencing requires.</span></span>

    <span data-ttu-id="8ceb5-116">**Remarques**  Le séquençage nécessite une utilisation importante du disque.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-116">**Note** Sequencing requires heavy disk usage.</span></span> <span data-ttu-id="8ceb5-117">Un débit de disque rapide peut réduire le temps de séquençage.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-117">A fast disk speed can decrease the sequencing time.</span></span>

     

### <span data-ttu-id="8ceb5-118">Configuration logicielle requise</span><span class="sxs-lookup"><span data-stu-id="8ceb5-118">Software Requirements</span></span>

<span data-ttu-id="8ceb5-119">La liste suivante répertorie les systèmes d’exploitation pris en charge pour exécuter le Sequencer.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-119">The following list outlines the supported operating systems for running the Sequencer.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8ceb5-120">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="8ceb5-120">Operating System</span></span></th>
<th align="left"><span data-ttu-id="8ceb5-121">Édition</span><span class="sxs-lookup"><span data-stu-id="8ceb5-121">Edition</span></span></th>
<th align="left"><span data-ttu-id="8ceb5-122">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8ceb5-122">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="8ceb5-123">Architecture système</span><span class="sxs-lookup"><span data-stu-id="8ceb5-123">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ceb5-124">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="8ceb5-124">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-125">Professionnel</span><span class="sxs-lookup"><span data-stu-id="8ceb5-125">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-126">SP2 ou SP3</span><span class="sxs-lookup"><span data-stu-id="8ceb5-126">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-127">x86</span><span class="sxs-lookup"><span data-stu-id="8ceb5-127">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8ceb5-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ceb5-128">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-129">Professionnel, entreprise ou intégrale</span><span class="sxs-lookup"><span data-stu-id="8ceb5-129">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-130">Aucun service pack, SP1 ou SP2</span><span class="sxs-lookup"><span data-stu-id="8ceb5-130">No service pack, SP1, or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-131">x86</span><span class="sxs-lookup"><span data-stu-id="8ceb5-131">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ceb5-132">Le</span><span class="sxs-lookup"><span data-stu-id="8ceb5-132">Windows7¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-133">Professionnel, entreprise ou édition intégrale</span><span class="sxs-lookup"><span data-stu-id="8ceb5-133">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-134">x86</span><span class="sxs-lookup"><span data-stu-id="8ceb5-134">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8ceb5-135">¹ pris en charge pour App-V 4,5 avec SP1 ou SP2 et App-V 4,6 uniquement</span><span class="sxs-lookup"><span data-stu-id="8ceb5-135">¹Supported for App-V 4.5 with SP1 or SP2, and App-V 4.6 only</span></span>

<span data-ttu-id="8ceb5-136">**Remarques**  Le Sequencer Application Virtualization (App-V) 4,6 prend en charge les versions 32 bits et 64 bits de ces systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-136">**Note** The Application Virtualization (App-V) 4.6 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="8ceb5-137">Vous devez configurer des ordinateurs exécutant le Sequencer avec les mêmes applications qui sont installées sur des ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-137">You should configure computers running the Sequencer with the same applications that are installed on target computers.</span></span>

### <span data-ttu-id="8ceb5-138">Configuration logicielle requise pour les services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="8ceb5-138">Software Requirements for Remote Desktop Services</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8ceb5-139">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="8ceb5-139">Operating System</span></span></th>
<th align="left"><span data-ttu-id="8ceb5-140">Édition</span><span class="sxs-lookup"><span data-stu-id="8ceb5-140">Edition</span></span></th>
<th align="left"><span data-ttu-id="8ceb5-141">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8ceb5-141">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="8ceb5-142">Architecture système</span><span class="sxs-lookup"><span data-stu-id="8ceb5-142">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ceb5-143">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="8ceb5-143">Windows Server2003</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-144">Éditions standard, édition entreprise ou édition Datacenter</span><span class="sxs-lookup"><span data-stu-id="8ceb5-144">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-145">SP1 ou SP2</span><span class="sxs-lookup"><span data-stu-id="8ceb5-145">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-146">x86</span><span class="sxs-lookup"><span data-stu-id="8ceb5-146">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8ceb5-147">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="8ceb5-147">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-148">Éditions standard, édition entreprise ou édition Datacenter</span><span class="sxs-lookup"><span data-stu-id="8ceb5-148">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-149">x86</span><span class="sxs-lookup"><span data-stu-id="8ceb5-149">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ceb5-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ceb5-150">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-151">Standard, entreprise ou centre de</span><span class="sxs-lookup"><span data-stu-id="8ceb5-151">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-152">SP1 ou SP2</span><span class="sxs-lookup"><span data-stu-id="8ceb5-152">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ceb5-153">x86</span><span class="sxs-lookup"><span data-stu-id="8ceb5-153">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8ceb5-154">**Remarques**  Application Virtualization (App-V) 4,6 pour les services Bureau à distance prend en charge les versions 32 bits et 64 bits de ces systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-154">**Note** Application Virtualization (App-V) 4.6 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

## <span data-ttu-id="8ceb5-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ceb5-155">Related topics</span></span>


[<span data-ttu-id="8ceb5-156">Vue d'ensemble d'Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="8ceb5-156">Application Virtualization Sequencer Overview</span></span>](application-virtualization-sequencer-overview.md)

 

 





