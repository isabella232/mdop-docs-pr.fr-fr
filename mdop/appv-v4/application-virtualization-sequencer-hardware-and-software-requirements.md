---
title: Configuration matérielle et logicielle requise pour Application Virtualization Sequencer
description: Configuration matérielle et logicielle requise pour Application Virtualization Sequencer
author: dansimp
ms.assetid: c88a1b5b-23e1-4460-afa9-a5f37e32eb05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d68afe4d4a3f6f301d38f2e86139d94319583467
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807981"
---
# <span data-ttu-id="46b34-103">Configuration matérielle et logicielle requise pour Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="46b34-103">Application Virtualization Sequencer Hardware and Software Requirements</span></span>


<span data-ttu-id="46b34-104">Cette rubrique décrit la configuration matérielle et logicielle minimale recommandée pour l’ordinateur exécutant le Sequencer Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="46b34-104">This topic describes the minimum recommended hardware and software requirements for the computer running the Microsoft Application Virtualization (App-V) Sequencer.</span></span>

<span data-ttu-id="46b34-105">**Important**  Vous devez exécuter le Sequencer App-V (**SFTSequencer.exe**) à l’aide d’un compte qui dispose de privilèges d’administrateur en raison des changements apportés par le Sequencer au système local.</span><span class="sxs-lookup"><span data-stu-id="46b34-105">**Important** You must run the App-V sequencer (**SFTSequencer.exe**) using an account that has administrator privileges because of the changes the sequencer makes to the local system.</span></span> <span data-ttu-id="46b34-106">Ces modifications peuvent inclure l’écriture de fichiers dans le répertoire **C:\\Program Files** , l’apport de modifications du Registre, le démarrage et l’arrêt de services, la mise à jour des descripteurs de sécurité pour les fichiers et la modification des autorisations.</span><span class="sxs-lookup"><span data-stu-id="46b34-106">These changes can include writing files to the **C:\\Program Files** directory, making registry changes, starting and stopping services, updating security descriptors for files, and changing permissions.</span></span>

 

<span data-ttu-id="46b34-107">Avant d’installer le Sequencer et après avoir séquencé chaque application, vous devez restaurer une nouvelle image de système d’exploitation sur l’ordinateur de séquençage.</span><span class="sxs-lookup"><span data-stu-id="46b34-107">Before you install the Sequencer and after you sequence each application, you must restore a clean operating system image to the sequencing computer.</span></span> <span data-ttu-id="46b34-108">Pour restaurer l’ordinateur exécutant le Sequencer, vous pouvez utiliser l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="46b34-108">You can use one of the following methods to restore the computer running the Sequencer:</span></span>

-   <span data-ttu-id="46b34-109">Remettez en forme le disque dur, puis réinstallez le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="46b34-109">Reformat the hard drive and reinstall the operating system.</span></span>

-   <span data-ttu-id="46b34-110">Restaurez le disque dur sur l’ordinateur exécutant l’image de Sequencer à l’aide d’un autre logiciel d’imagerie de disque.</span><span class="sxs-lookup"><span data-stu-id="46b34-110">Restore the hard drive on the computer running the Sequencer image by using another disk-imaging software.</span></span>

-   <span data-ttu-id="46b34-111">Restaurez une image de système d’exploitation virtuelle telle qu’une image Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="46b34-111">Revert a virtual operating system image such as a Microsoft Virtual PC image.</span></span> <span data-ttu-id="46b34-112">L’utilisation d’un ordinateur virtuel permet à des environnements de séquençage sains d’être facilement réutilisés avec un minimum d’administration.</span><span class="sxs-lookup"><span data-stu-id="46b34-112">Using a virtual machine allows for clean sequencing environments to be easily reused with minimal administration.</span></span>

<span data-ttu-id="46b34-113">La liste suivante présente la configuration matérielle requise pour exécuter le Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="46b34-113">The following list outlines the recommended hardware requirements for running the App-V Sequencer.</span></span>

<span data-ttu-id="46b34-114">La configuration requise est d’abord répertoriée dans Microsoft Application Virtualization (App-V) 4.6 SP2, puis dans les versions antérieures à App-V 4.6 SP2.</span><span class="sxs-lookup"><span data-stu-id="46b34-114">The requirements are listed first for Microsoft Application Virtualization (App-V)4.6 SP2, followed by the requirements for versions that preceded App-V4.6SP2.</span></span>

### <a href="" id="hardware-requirements-"></a><span data-ttu-id="46b34-115">Configuration matérielle requise</span><span class="sxs-lookup"><span data-stu-id="46b34-115">Hardware Requirements</span></span>

-   <span data-ttu-id="46b34-116">Processeur: Intel Pentium III, 1 GHz (32-bit ou 64 bits).</span><span class="sxs-lookup"><span data-stu-id="46b34-116">Processor—Intel Pentium III, 1 GHz (32-bit or 64-bit).</span></span> <span data-ttu-id="46b34-117">Le processus de séquençage est un processus à thread unique qui ne tire pas parti de deux processeurs.</span><span class="sxs-lookup"><span data-stu-id="46b34-117">The sequencing process is a single-threaded process and does not take advantage of dual processors.</span></span>

-   <span data-ttu-id="46b34-118">Mémoire: 1 Go ou plus, 2 Go recommandés.</span><span class="sxs-lookup"><span data-stu-id="46b34-118">Memory—1GB or above, 2GB recommended.</span></span>

-   <span data-ttu-id="46b34-119">Disque dur: 40 gigaoctets (Go) d’espace disque disponible d’au moins 15 Go d’espace libre sur le disque dur.</span><span class="sxs-lookup"><span data-stu-id="46b34-119">Hard disk—40 gigabyte (GB) hard disk space with a minimum of 15 GB available hard disk space.</span></span> <span data-ttu-id="46b34-120">Nous vous recommandons d’avoir au moins trois fois l’espace disque disponible requis par l’application.</span><span class="sxs-lookup"><span data-stu-id="46b34-120">We recommend that you have at least three times the hard disk space that the application you are sequencing requires.</span></span>

    <span data-ttu-id="46b34-121">**Remarques**  Le séquençage nécessite une utilisation importante du disque.</span><span class="sxs-lookup"><span data-stu-id="46b34-121">**Note** Sequencing requires heavy disk usage.</span></span> <span data-ttu-id="46b34-122">Un débit de disque rapide peut réduire le temps de séquençage.</span><span class="sxs-lookup"><span data-stu-id="46b34-122">A fast disk speed can decrease the sequencing time.</span></span>

     

### <span data-ttu-id="46b34-123">Configuration logicielle requise pour App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="46b34-123">Software Requirements for App-V 4.6 SP2</span></span>

<span data-ttu-id="46b34-124">La liste suivante répertorie les systèmes d’exploitation pris en charge pour exécuter le Sequencer App-V 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="46b34-124">The following list outlines the supported operating systems for running the App-V 4.6 SP2 Sequencer.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="46b34-125">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="46b34-125">Operating System</span></span></th>
<th align="left"><span data-ttu-id="46b34-126">Édition</span><span class="sxs-lookup"><span data-stu-id="46b34-126">Edition</span></span></th>
<th align="left"><span data-ttu-id="46b34-127">Service Pack</span><span class="sxs-lookup"><span data-stu-id="46b34-127">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="46b34-128">Architecture système</span><span class="sxs-lookup"><span data-stu-id="46b34-128">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46b34-129">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="46b34-129">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-130">Professionnel</span><span class="sxs-lookup"><span data-stu-id="46b34-130">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-131">3</span><span class="sxs-lookup"><span data-stu-id="46b34-131">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-132">x86</span><span class="sxs-lookup"><span data-stu-id="46b34-132">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46b34-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46b34-133">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-134">Professionnel, entreprise ou intégrale</span><span class="sxs-lookup"><span data-stu-id="46b34-134">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-135">SP2</span><span class="sxs-lookup"><span data-stu-id="46b34-135">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-136">x86</span><span class="sxs-lookup"><span data-stu-id="46b34-136">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46b34-137">Plus de.</span><span class="sxs-lookup"><span data-stu-id="46b34-137">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-138">Professionnel, entreprise ou édition intégrale</span><span class="sxs-lookup"><span data-stu-id="46b34-138">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-139">Aucun Service Pack ou SP1</span><span class="sxs-lookup"><span data-stu-id="46b34-139">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-140">x86 et x64</span><span class="sxs-lookup"><span data-stu-id="46b34-140">x86 and x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46b34-141">Windows8</span><span class="sxs-lookup"><span data-stu-id="46b34-141">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-142">Professionnel ou édition entreprise</span><span class="sxs-lookup"><span data-stu-id="46b34-142">Pro or Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="46b34-143">x86 et x64</span><span class="sxs-lookup"><span data-stu-id="46b34-143">x86 and x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="46b34-144">**Remarques**  Le Sequencer Application Virtualization (App-V) 4,6 SP2 prend en charge les versions 32 bits et 64 bits de ces systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="46b34-144">**Note** The Application Virtualization (App-V) 4.6 SP2 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="46b34-145">Vous devez configurer des ordinateurs exécutant le Sequencer avec les mêmes applications qui sont installées sur des ordinateurs ciblés.</span><span class="sxs-lookup"><span data-stu-id="46b34-145">You should configure computers running the Sequencer with the same applications that are installed on targeted computers.</span></span>

### <span data-ttu-id="46b34-146">Configuration logicielle requise pour les versions qui précèdent App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="46b34-146">Software Requirements for Versions that Precede App-V 4.6 SP2</span></span>

<span data-ttu-id="46b34-147">La liste suivante présente les systèmes d’exploitation pris en charge pour exécuter le Sequencer pour les versions qui précèdent App-V 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="46b34-147">The following list outlines the supported operating systems for running the Sequencer for versions that precede App-V 4.6 SP2.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="46b34-148">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="46b34-148">Operating System</span></span></th>
<th align="left"><span data-ttu-id="46b34-149">Édition</span><span class="sxs-lookup"><span data-stu-id="46b34-149">Edition</span></span></th>
<th align="left"><span data-ttu-id="46b34-150">Service Pack</span><span class="sxs-lookup"><span data-stu-id="46b34-150">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="46b34-151">Architecture système</span><span class="sxs-lookup"><span data-stu-id="46b34-151">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46b34-152">WindowsXP</span><span class="sxs-lookup"><span data-stu-id="46b34-152">WindowsXP</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-153">Professionnel</span><span class="sxs-lookup"><span data-stu-id="46b34-153">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-154">SP2 ou SP3</span><span class="sxs-lookup"><span data-stu-id="46b34-154">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-155">x86</span><span class="sxs-lookup"><span data-stu-id="46b34-155">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46b34-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46b34-156">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-157">Professionnel, entreprise ou intégrale</span><span class="sxs-lookup"><span data-stu-id="46b34-157">Business, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-158">Aucun service pack, SP1 ou SP2</span><span class="sxs-lookup"><span data-stu-id="46b34-158">No service pack, SP1, or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-159">x86</span><span class="sxs-lookup"><span data-stu-id="46b34-159">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46b34-160">Le</span><span class="sxs-lookup"><span data-stu-id="46b34-160">Windows7¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-161">Professionnel, entreprise ou édition intégrale</span><span class="sxs-lookup"><span data-stu-id="46b34-161">Professional, Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="46b34-162">x86</span><span class="sxs-lookup"><span data-stu-id="46b34-162">x86</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="46b34-163">¹ pris en charge pour App-V 4,5 avec SP1 ou SP2 et App-V 4,6 uniquement</span><span class="sxs-lookup"><span data-stu-id="46b34-163">¹Supported for App-V 4.5 with SP1 or SP2, and App-V 4.6 only</span></span>

<span data-ttu-id="46b34-164">**Remarques**  Le Sequencer Application Virtualization (App-V) 4,6 prend en charge les versions 32 bits et 64 bits de ces systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="46b34-164">**Note** The Application Virtualization (App-V) 4.6 Sequencer supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

<span data-ttu-id="46b34-165">Vous devez configurer des ordinateurs exécutant le Sequencer avec les mêmes applications qui sont installées sur des ordinateurs ciblés.</span><span class="sxs-lookup"><span data-stu-id="46b34-165">You should configure computers running the Sequencer with the same applications that are installed on targeted computers.</span></span>

### <span data-ttu-id="46b34-166">Configuration logicielle requise pour les services Bureau à distance pour App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="46b34-166">Software Requirements for Remote Desktop Services for App-V 4.6 SP2</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="46b34-167">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="46b34-167">Operating System</span></span></th>
<th align="left"><span data-ttu-id="46b34-168">Édition</span><span class="sxs-lookup"><span data-stu-id="46b34-168">Edition</span></span></th>
<th align="left"><span data-ttu-id="46b34-169">Service Pack</span><span class="sxs-lookup"><span data-stu-id="46b34-169">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="46b34-170">Architecture système</span><span class="sxs-lookup"><span data-stu-id="46b34-170">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46b34-171">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="46b34-171">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-172">Éditions standard, édition entreprise ou édition Datacenter</span><span class="sxs-lookup"><span data-stu-id="46b34-172">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-173">SP2</span><span class="sxs-lookup"><span data-stu-id="46b34-173">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-174">x86</span><span class="sxs-lookup"><span data-stu-id="46b34-174">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46b34-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46b34-175">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-176">Éditions standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="46b34-176">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-177">SP2</span><span class="sxs-lookup"><span data-stu-id="46b34-177">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-178">x86</span><span class="sxs-lookup"><span data-stu-id="46b34-178">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46b34-179">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46b34-179">Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-180">Éditions standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="46b34-180">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-181">Aucun Service Pack ou SP1</span><span class="sxs-lookup"><span data-stu-id="46b34-181">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-182">x64</span><span class="sxs-lookup"><span data-stu-id="46b34-182">x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46b34-183">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="46b34-183">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-184">Éditions standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="46b34-184">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="46b34-185">x86 ou x64</span><span class="sxs-lookup"><span data-stu-id="46b34-185">x86 or x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="46b34-186">**Remarques**  Application Virtualization (App-V) 4,6 SP2 pour les services Bureau à distance prend en charge les versions 32 bits et 64 bits de ces systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="46b34-186">**Note** Application Virtualization (App-V) 4.6 SP2 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

### <span data-ttu-id="46b34-187">Configuration logicielle requise pour les services Bureau à distance pour les versions qui précèdent App-V 4,6 SP2</span><span class="sxs-lookup"><span data-stu-id="46b34-187">Software Requirements for Remote Desktop Services for Versions that Precede App-V 4.6 SP2</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="46b34-188">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="46b34-188">Operating System</span></span></th>
<th align="left"><span data-ttu-id="46b34-189">Édition</span><span class="sxs-lookup"><span data-stu-id="46b34-189">Edition</span></span></th>
<th align="left"><span data-ttu-id="46b34-190">Service Pack</span><span class="sxs-lookup"><span data-stu-id="46b34-190">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="46b34-191">Architecture système</span><span class="sxs-lookup"><span data-stu-id="46b34-191">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46b34-192">Windows Server2003</span><span class="sxs-lookup"><span data-stu-id="46b34-192">Windows Server2003</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-193">Éditions standard, édition entreprise ou édition Datacenter</span><span class="sxs-lookup"><span data-stu-id="46b34-193">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-194">SP1 ou SP2</span><span class="sxs-lookup"><span data-stu-id="46b34-194">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-195">x86</span><span class="sxs-lookup"><span data-stu-id="46b34-195">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46b34-196">Windows Server2003 R2</span><span class="sxs-lookup"><span data-stu-id="46b34-196">Windows Server2003 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-197">Éditions standard, édition entreprise ou édition Datacenter</span><span class="sxs-lookup"><span data-stu-id="46b34-197">Standard Edition, Enterprise Edition, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-198">Aucun Service Pack ou SP2</span><span class="sxs-lookup"><span data-stu-id="46b34-198">No service pack or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-199">x86</span><span class="sxs-lookup"><span data-stu-id="46b34-199">x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="46b34-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46b34-200">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-201">Éditions standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="46b34-201">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-202">SP1 ou SP2</span><span class="sxs-lookup"><span data-stu-id="46b34-202">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-203">x86</span><span class="sxs-lookup"><span data-stu-id="46b34-203">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="46b34-204">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46b34-204">Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-205">Éditions standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="46b34-205">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-206">Aucun Service Pack ou SP1</span><span class="sxs-lookup"><span data-stu-id="46b34-206">No service pack or SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="46b34-207">x64</span><span class="sxs-lookup"><span data-stu-id="46b34-207">x64</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="46b34-208">**Remarques**  Application Virtualization (App-V) 4,6 SP2 pour les services Bureau à distance prend en charge les versions 32 bits et 64 bits de ces systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="46b34-208">**Note** Application Virtualization (App-V) 4.6 SP2 for Remote Desktop Services supports 32-bit and 64-bit versions of these operating systems.</span></span>

 

## <span data-ttu-id="46b34-209">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="46b34-209">Related topics</span></span>


[<span data-ttu-id="46b34-210">Configuration matérielle et logicielle requise pour Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="46b34-210">Application Virtualization Client Hardware and Software Requirements</span></span>](application-virtualization-client-hardware-and-software-requirements.md)

[<span data-ttu-id="46b34-211">Configuration système requise pour Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="46b34-211">Application Virtualization System Requirements</span></span>](application-virtualization-system-requirements.md)

[<span data-ttu-id="46b34-212">Procédure pour installer Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="46b34-212">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)

[<span data-ttu-id="46b34-213">Procédure pour mettre à niveau Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="46b34-213">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)

 

 





