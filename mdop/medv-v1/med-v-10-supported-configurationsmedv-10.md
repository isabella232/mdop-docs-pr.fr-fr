---
title: Configurations prises en charge par MED-V1.0
description: Configurations prises en charge par MED-V1.0
author: dansimp
ms.assetid: 74643de6-549e-4177-a559-6407e156ed3a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3b8ffdfb6e34fe7888ea5ace0ff7264bd978a548
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804356"
---
# <span data-ttu-id="ebc01-103">Configurations prises en charge par MED-V1.0</span><span class="sxs-lookup"><span data-stu-id="ebc01-103">MED-V 1.0 Supported Configurations</span></span>


<span data-ttu-id="ebc01-104">Cette rubrique précise les exigences nécessaires à l’installation et à l’exécution de Microsoft Enterprise Desktop Virtualization (MED-V) 1,0 dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="ebc01-104">This topic specifies the requirements necessary to install and run Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 in your environment.</span></span>

## <span data-ttu-id="ebc01-105">Configuration système requise pour le client MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="ebc01-105">MED-V 1.0 Client System Requirements</span></span>


### <span data-ttu-id="ebc01-106">Configuration requise pour le système d’exploitation MED-V</span><span class="sxs-lookup"><span data-stu-id="ebc01-106">MED-V Client Operating System Requirements</span></span>

<span data-ttu-id="ebc01-107">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="ebc01-107">The following table lists the operating systems that are supported for MED-V 1.0 client installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ebc01-108">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="ebc01-108">Operating System</span></span></th>
<th align="left"><span data-ttu-id="ebc01-109">Édition</span><span class="sxs-lookup"><span data-stu-id="ebc01-109">Edition</span></span></th>
<th align="left"><span data-ttu-id="ebc01-110">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ebc01-110">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="ebc01-111">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ebc01-111">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebc01-112">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ebc01-112">Windows XP</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-113">Edition professionnelle</span><span class="sxs-lookup"><span data-stu-id="ebc01-113">Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-114">SP2 ou SP3</span><span class="sxs-lookup"><span data-stu-id="ebc01-114">SP2 or SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-115">x86</span><span class="sxs-lookup"><span data-stu-id="ebc01-115">x86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebc01-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebc01-116">Windows Vista</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-117">Edition professionnelle, entreprise ou édition intégrale</span><span class="sxs-lookup"><span data-stu-id="ebc01-117">Business, Enterprise, or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-118">SP1 ou SP2</span><span class="sxs-lookup"><span data-stu-id="ebc01-118">SP1 or SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-119">x86</span><span class="sxs-lookup"><span data-stu-id="ebc01-119">x86</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ebc01-120">Remarque</span><span class="sxs-lookup"><span data-stu-id="ebc01-120">Note</span></span>**  
<span data-ttu-id="ebc01-121">Le client MED-V ne s’exécute pas en mode x64 natif.</span><span class="sxs-lookup"><span data-stu-id="ebc01-121">MED-V client does not run in native x64 mode.</span></span> <span data-ttu-id="ebc01-122">Au lieu de cela, MED-V s’exécute en mode Windows 64 bits (WOW64) sur les ordinateurs 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ebc01-122">Instead, MED-V runs in Windows on Windows 64-bit (WOW64) mode on 64-bit computers.</span></span>



### <a href="" id="med-v-1-0-client-configuration-"></a><span data-ttu-id="ebc01-123">Configuration du client MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="ebc01-123">MED-V 1.0 Client Configuration</span></span>

**<span data-ttu-id="ebc01-124">Version du .NET Framework</span><span class="sxs-lookup"><span data-stu-id="ebc01-124">.NET Framework Version</span></span>**

<span data-ttu-id="ebc01-125">Les versions suivantes de Microsoft .NET Framework sont prises en charge pour l’installation du client MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="ebc01-125">The following versions of the Microsoft .NET Framework are supported for MED-V 1.0 client installation:</span></span>

-   <span data-ttu-id="ebc01-126">.NET Framework 2,0 ou .NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ebc01-126">.NET Framework 2.0 or .NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="ebc01-127">.NET Framework 3,0 ou .NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ebc01-127">.NET Framework 3.0 or .NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="ebc01-128">.NET Framework 3,5 ou .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="ebc01-128">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="ebc01-129">Moteur de virtualisation</span><span class="sxs-lookup"><span data-stu-id="ebc01-129">Virtualization Engine</span></span>**

<span data-ttu-id="ebc01-130">Microsoft Virtual PC 2007 SP1 avec le correctif décrit dans l’article 974918 de la base de connaissances Microsoft est pris en charge pour l’installation du client MED-V 1,0 dans les configurations suivantes:</span><span class="sxs-lookup"><span data-stu-id="ebc01-130">Microsoft Virtual PC 2007 SP1 with the hotfix that is described in Microsoft Knowledge Base article 974918 is supported for MED-V 1.0 client installation in the following configurations:</span></span>

-   <span data-ttu-id="ebc01-131">Fichier de disque dur virtuel statique (VHD)</span><span class="sxs-lookup"><span data-stu-id="ebc01-131">Static Virtual Hard Disk (VHD) file</span></span>

-   <span data-ttu-id="ebc01-132">Plusieurs fichiers VHD situés dans le même répertoire</span><span class="sxs-lookup"><span data-stu-id="ebc01-132">Multiple VHD files located within the same directory</span></span>

-   <span data-ttu-id="ebc01-133">Fichier de disque dur virtuel dynamique</span><span class="sxs-lookup"><span data-stu-id="ebc01-133">Dynamic VHD file</span></span>

**<span data-ttu-id="ebc01-134">Navigateur Internet</span><span class="sxs-lookup"><span data-stu-id="ebc01-134">Internet Browser</span></span>**

<span data-ttu-id="ebc01-135">Windows Internet Explorer 7 et Windows Internet Explorer 8 sont pris en charge pour l’installation du client MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="ebc01-135">Windows Internet Explorer 7 and Windows Internet Explorer 8 are supported for MED-V 1.0 client installation.</span></span>

**<span data-ttu-id="ebc01-136">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="ebc01-136">Microsoft Hyper-V Server</span></span>**

<span data-ttu-id="ebc01-137">Le client MED-V n’est pas pris en charge dans un environnement Microsoft Hyper-V Server.</span><span class="sxs-lookup"><span data-stu-id="ebc01-137">The MED-V client is not supported in a Microsoft Hyper-V server environment.</span></span>

## <span data-ttu-id="ebc01-138">Configuration requise pour le système d’espace de travail MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="ebc01-138">MED-V 1.0 Workspace System Requirements</span></span>


### <span data-ttu-id="ebc01-139">Configuration requise pour le système d’exploitation MED-V</span><span class="sxs-lookup"><span data-stu-id="ebc01-139">MED-V Workspace Operating System Requirements</span></span>

<span data-ttu-id="ebc01-140">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour les espaces de travail MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="ebc01-140">The following table lists the operating systems supported for MED-V 1.0 workspaces.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ebc01-141">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="ebc01-141">Operating System</span></span></th>
<th align="left"><span data-ttu-id="ebc01-142">Édition</span><span class="sxs-lookup"><span data-stu-id="ebc01-142">Edition</span></span></th>
<th align="left"><span data-ttu-id="ebc01-143">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ebc01-143">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="ebc01-144">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ebc01-144">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebc01-145">Windows2000</span><span class="sxs-lookup"><span data-stu-id="ebc01-145">Windows 2000</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-146">Professionnel</span><span class="sxs-lookup"><span data-stu-id="ebc01-146">Professional</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-147">REPLISTOR6.2SP4</span><span class="sxs-lookup"><span data-stu-id="ebc01-147">SP4</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-148">Processeur</span><span class="sxs-lookup"><span data-stu-id="ebc01-148">X86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebc01-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ebc01-149">Windows XP</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-150">Edition professionnelle</span><span class="sxs-lookup"><span data-stu-id="ebc01-150">Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-151">SP2 ou SP3</span><span class="sxs-lookup"><span data-stu-id="ebc01-151">SP2 or SP3</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ebc01-152">Remarque</span><span class="sxs-lookup"><span data-stu-id="ebc01-152">Note</span></span></strong><br/><p><span data-ttu-id="ebc01-153">SP3 est recommandé de s’assurer que l’espace de travail MED-V est compatible avec des versions ultérieures de MED-V.</span><span class="sxs-lookup"><span data-stu-id="ebc01-153">SP3 is recommended to ensure that the MED-V workspace will be compatible with future versions of MED-V.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="ebc01-154">x86</span><span class="sxs-lookup"><span data-stu-id="ebc01-154">x86</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-workspace-configuration-"></a><span data-ttu-id="ebc01-155">Configuration de l’espace de travail MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="ebc01-155">MED-V 1.0 Workspace Configuration</span></span>

**<span data-ttu-id="ebc01-156">Version du .NET Framework</span><span class="sxs-lookup"><span data-stu-id="ebc01-156">.NET Framework Version</span></span>**

<span data-ttu-id="ebc01-157">MED-V nécessite une des versions prises en charge suivantes de l’installation de Microsoft .NET Framework pour MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="ebc01-157">MED-V requires one of the following supported versions of the Microsoft .NET Framework for MED-V 1.0 workspace installation:</span></span>

-   <span data-ttu-id="ebc01-158">.NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ebc01-158">.NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="ebc01-159">.NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ebc01-159">.NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="ebc01-160">.NET Framework 3,5 ou .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="ebc01-160">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="ebc01-161">Remarque</span><span class="sxs-lookup"><span data-stu-id="ebc01-161">Note</span></span>**  
<span data-ttu-id="ebc01-162">.NET Framework 3,5 SP1 est recommandé de s’assurer que l’espace de travail MED-V est compatible avec des versions ultérieures de MED-V.</span><span class="sxs-lookup"><span data-stu-id="ebc01-162">.NET Framework 3.5 SP1 is recommended to ensure that the MED-V workspace will be compatible with future versions of MED-V.</span></span>



**<span data-ttu-id="ebc01-163">Navigateur Internet</span><span class="sxs-lookup"><span data-stu-id="ebc01-163">Internet Browser</span></span>**

<span data-ttu-id="ebc01-164">Windows Internet Explorer 6 SP2 et Windows Internet Explorer 7 sont pris en charge pour l’installation de l’espace de travail 1,0 de MED-V.</span><span class="sxs-lookup"><span data-stu-id="ebc01-164">Windows Internet Explorer 6 SP2 and Windows Internet Explorer 7 are supported for the MED-V 1.0 workspace installation.</span></span>

### <a href="" id="med-v-workspace-images-"></a><span data-ttu-id="ebc01-165">Images d’espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="ebc01-165">MED-V Workspace Images</span></span>

<span data-ttu-id="ebc01-166">Les images d’espace de travail MED-V doivent être créées à l’aide de Virtual PC 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="ebc01-166">MED-V workspace images must be created by using Virtual PC 2007 SP1.</span></span>

## <span data-ttu-id="ebc01-167">Configuration système requise pour MED-V 1,0 Server</span><span class="sxs-lookup"><span data-stu-id="ebc01-167">MED-V 1.0 Server System Requirements</span></span>


### <span data-ttu-id="ebc01-168">Configuration requise pour le système d’exploitation MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="ebc01-168">MED-V 1.0 Server Operating System Requirements</span></span>

<span data-ttu-id="ebc01-169">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour les installations du serveur MED-V 1,0.</span><span class="sxs-lookup"><span data-stu-id="ebc01-169">The following table lists the operating systems supported for MED-V 1.0 server installations.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ebc01-170">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="ebc01-170">Operating System</span></span></th>
<th align="left"><span data-ttu-id="ebc01-171">Édition</span><span class="sxs-lookup"><span data-stu-id="ebc01-171">Edition</span></span></th>
<th align="left"><span data-ttu-id="ebc01-172">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ebc01-172">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="ebc01-173">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ebc01-173">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebc01-174">WindowsServer2008</span><span class="sxs-lookup"><span data-stu-id="ebc01-174">Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-175">Standard ou Entreprise</span><span class="sxs-lookup"><span data-stu-id="ebc01-175">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-176">None</span><span class="sxs-lookup"><span data-stu-id="ebc01-176">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-177">X86 ou x64</span><span class="sxs-lookup"><span data-stu-id="ebc01-177">X86 or x64</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="med-v-1-0-server-configuration-"></a><span data-ttu-id="ebc01-178">Configuration du serveur MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="ebc01-178">MED-V 1.0 Server Configuration</span></span>

**<span data-ttu-id="ebc01-179">Version du .NET Framework</span><span class="sxs-lookup"><span data-stu-id="ebc01-179">.NET Framework Version</span></span>**

<span data-ttu-id="ebc01-180">MED-V nécessite une des versions prises en charge suivantes de l’installation de Microsoft .NET Framework pour MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="ebc01-180">MED-V requires one of the following supported versions of the Microsoft .NET Framework for MED-V 1.0 workspace installation:</span></span>

-   <span data-ttu-id="ebc01-181">.NET Framework 2,0 ou .NET Framework 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ebc01-181">.NET Framework 2.0 or .NET Framework 2.0 SP1</span></span>

-   <span data-ttu-id="ebc01-182">.NET Framework 3,0 ou .NET Framework 3,0 SP1</span><span class="sxs-lookup"><span data-stu-id="ebc01-182">.NET Framework 3.0 or .NET Framework 3.0 SP1</span></span>

-   <span data-ttu-id="ebc01-183">.NET Framework 3,5 ou .NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="ebc01-183">.NET Framework 3.5 or .NET Framework 3.5 SP1</span></span>

**<span data-ttu-id="ebc01-184">Version de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="ebc01-184">Microsoft SQL Server Version</span></span>**

<span data-ttu-id="ebc01-185">Les versions suivantes de Microsoft SQL Server sont prises en charge pour MED-V 1,0 lorsque SQL Server est installé en local ou à distance à partir du serveur MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="ebc01-185">The following versions of Microsoft SQL Server are supported for MED-V 1.0 when SQL Server is installed locally or remotely from the MED-V 1.0 Server:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ebc01-186">Version de SQL Server</span><span class="sxs-lookup"><span data-stu-id="ebc01-186">SQL Server Version</span></span></th>
<th align="left"><span data-ttu-id="ebc01-187">Édition</span><span class="sxs-lookup"><span data-stu-id="ebc01-187">Edition</span></span></th>
<th align="left"><span data-ttu-id="ebc01-188">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ebc01-188">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="ebc01-189">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ebc01-189">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebc01-190">SQL Server 2005</span><span class="sxs-lookup"><span data-stu-id="ebc01-190">SQL Server 2005</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-191">Edition rapide, standard ou entreprise</span><span class="sxs-lookup"><span data-stu-id="ebc01-191">Express, Standard, or Enterprise Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-192">SP2</span><span class="sxs-lookup"><span data-stu-id="ebc01-192">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-193">X86 ou x64</span><span class="sxs-lookup"><span data-stu-id="ebc01-193">X86 or x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebc01-194">SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebc01-194">SQL Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-195">Express, standard ou entreprise</span><span class="sxs-lookup"><span data-stu-id="ebc01-195">Express, Standard, or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-196">None</span><span class="sxs-lookup"><span data-stu-id="ebc01-196">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebc01-197">X86 ou x64</span><span class="sxs-lookup"><span data-stu-id="ebc01-197">X86 or x64</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ebc01-198">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="ebc01-198">Microsoft Hyper-V Server</span></span>**

<span data-ttu-id="ebc01-199">Le serveur MED-V est pris en charge dans un environnement Microsoft Hyper-V Server.</span><span class="sxs-lookup"><span data-stu-id="ebc01-199">The MED-V server is supported in a Microsoft Hyper-V server environment.</span></span>

## <span data-ttu-id="ebc01-200">Informations de globalisation MED-V 1,0</span><span class="sxs-lookup"><span data-stu-id="ebc01-200">MED-V 1.0 Globalization Information</span></span>


<span data-ttu-id="ebc01-201">Bien que MED-V ne soit pas divulgué dans des langues autres que l’anglais, les versions suivantes du système d’exploitation Windows sont prises en charge pour le client et les installations serveur MED-V 1,0:</span><span class="sxs-lookup"><span data-stu-id="ebc01-201">Although MED-V is not released in languages other than English, the following Windows operating system language versions are supported for the MED-V 1.0 client, workspace, and server installations:</span></span>

-   <span data-ttu-id="ebc01-202">Anglais</span><span class="sxs-lookup"><span data-stu-id="ebc01-202">English</span></span>

-   <span data-ttu-id="ebc01-203">Français</span><span class="sxs-lookup"><span data-stu-id="ebc01-203">French</span></span>

-   <span data-ttu-id="ebc01-204">Allemand</span><span class="sxs-lookup"><span data-stu-id="ebc01-204">German</span></span>

-   <span data-ttu-id="ebc01-205">Italien</span><span class="sxs-lookup"><span data-stu-id="ebc01-205">Italian</span></span>

-   <span data-ttu-id="ebc01-206">Espagnol</span><span class="sxs-lookup"><span data-stu-id="ebc01-206">Spanish</span></span>

-   <span data-ttu-id="ebc01-207">Portugais (Brésil)</span><span class="sxs-lookup"><span data-stu-id="ebc01-207">Portuguese (Brazil)</span></span>









