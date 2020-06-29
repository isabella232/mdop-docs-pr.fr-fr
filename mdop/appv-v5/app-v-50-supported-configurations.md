---
title: Configurations prises en charge d'App-V5.0
description: Configurations prises en charge d'App-V5.0
author: dansimp
ms.assetid: 3787ff63-7ce7-45a8-8f01-81b4b6dced34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 60236743d2a6b418ca7f4705168a7bf064b82156
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805989"
---
# <span data-ttu-id="a9a3b-103">Configurations prises en charge d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="a9a3b-103">App-V 5.0 Supported Configurations</span></span>


<span data-ttu-id="a9a3b-104">Cette rubrique spécifie les exigences nécessaires pour l’installation et l’exécution de Microsoft Application Virtualization (App-V) 5,0 dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-104">This topic specifies the requirements that are necessary to install and run Microsoft Application Virtualization (App-V) 5.0 in your environment.</span></span>

**<span data-ttu-id="a9a3b-105">Important</span><span class="sxs-lookup"><span data-stu-id="a9a3b-105">Important</span></span>**  
<span data-ttu-id="a9a3b-106">**Les configurations prises en charge dans cet article s’appliquent uniquement à l’App-V 5,0**.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-106">**The supported configurations in this article apply only to App-V 5.0**.</span></span> <span data-ttu-id="a9a3b-107">Pour plus d’informations sur les configurations prises en charge qui s’appliquent aux service packs 5,0 App-V, consultez les pages Web suivantes:</span><span class="sxs-lookup"><span data-stu-id="a9a3b-107">For supported configurations that apply to App-V 5.0 Service Packs, see the following web pages:</span></span>

-   [<span data-ttu-id="a9a3b-108">Nouveautés dans App-V5.0 SP1</span><span class="sxs-lookup"><span data-stu-id="a9a3b-108">What's new in App-V 5.0 SP1</span></span>](whats-new-in-app-v-50-sp1.md)

-   [<span data-ttu-id="a9a3b-109">À propos d'App-V5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-109">About App-V 5.0 SP2</span></span>](about-app-v-50-sp2.md)

-   [<span data-ttu-id="a9a3b-110">Configurations prises en charge d'App-V5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="a9a3b-110">App-V 5.0 SP3 Supported Configurations</span></span>](app-v-50-sp3-supported-configurations.md)



## <a href="" id="---------app-v-5-0-server-system-requirements"></a> <span data-ttu-id="a9a3b-111">Configuration système requise pour le serveur App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a9a3b-111">App-V 5.0 server system requirements</span></span>


**<span data-ttu-id="a9a3b-112">Important</span><span class="sxs-lookup"><span data-stu-id="a9a3b-112">Important</span></span>**  
<span data-ttu-id="a9a3b-113">Le serveur App-V 5,0 ne prend pas en charge les scénarios suivants:</span><span class="sxs-lookup"><span data-stu-id="a9a3b-113">The App-V 5.0 server does not support the following scenarios:</span></span>



-   <span data-ttu-id="a9a3b-114">Déploiement sur un ordinateur exécutant Microsoft Windows Server Core.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-114">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="a9a3b-115">Déploiement sur un ordinateur qui exécute une version antérieure des composants serveur App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-115">Deployment to a computer that runs a previous version of App-V 5.0 server components.</span></span>

    **<span data-ttu-id="a9a3b-116">Remarque</span><span class="sxs-lookup"><span data-stu-id="a9a3b-116">Note</span></span>**  
    <span data-ttu-id="a9a3b-117">Vous pouvez installer App-V 5,0 côte à côte avec le serveur App-V 4,5 Lightweight Streaming Server (LWS) uniquement.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-117">You can install App-V 5.0 side-by-side with the App-V 4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="a9a3b-118">Le déploiement d’App-V 5,0 côte à côte avec le serveur de gestion des applications (HWS) App-V 4,5 n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-118">Deployment of App-V 5.0 side-by-side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>



-   <span data-ttu-id="a9a3b-119">Déploiement sur un ordinateur qui exécute Microsoft SQL Server Express Edition.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-119">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="a9a3b-120">Déploiement distant de la base de données du serveur de gestion ou de la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-120">Remote deployment of the management server database or the reporting database.</span></span> <span data-ttu-id="a9a3b-121">Le programme d’installation doit être exécuté directement sur l’ordinateur exécutant Microsoft SQL pour que l’installation de la base de données réussisse.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-121">The installer must be run directly on the computer running Microsoft SQL for the database installation to succeed.</span></span>

-   <span data-ttu-id="a9a3b-122">Déploiement sur un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-122">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="a9a3b-123">Les chemins d’accès courts ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-123">Short paths are not supported.</span></span> <span data-ttu-id="a9a3b-124">Si vous envisagez d’utiliser un chemin court, vous devez créer un nouveau volume.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-124">If you plan to use a short path you must create a new volume.</span></span>

### <span data-ttu-id="a9a3b-125">Configuration requise pour le système d’exploitation de Management Server</span><span class="sxs-lookup"><span data-stu-id="a9a3b-125">Management Server operating system requirements</span></span>

<span data-ttu-id="a9a3b-126">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation d’App-V 5,0 Management Server.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-126">The following table lists the operating systems that are supported for the App-V 5.0 management server installation.</span></span>

**<span data-ttu-id="a9a3b-127">Remarque</span><span class="sxs-lookup"><span data-stu-id="a9a3b-127">Note</span></span>**  
<span data-ttu-id="a9a3b-128">Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-128">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="a9a3b-129">Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="a9a3b-129">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="a9a3b-130">Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="a9a3b-130">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9a3b-131">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="a9a3b-131">Operating system</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-132">Édition</span><span class="sxs-lookup"><span data-stu-id="a9a3b-132">Edition</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-133">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a9a3b-133">Service pack</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-134">Architecture système</span><span class="sxs-lookup"><span data-stu-id="a9a3b-134">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9a3b-135">Microsoft Windows Server 2008 (standard, entreprise, centre de connaissances ou serveur Web)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-135">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-136">R2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-136">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-137">SP1 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a9a3b-137">SP1 and higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-138">64 bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-138">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9a3b-139">Microsoft Windows Server 2012 (standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-139">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="a9a3b-140">64 bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-140">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9a3b-141">Microsoft Windows Server 2012 (standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-141">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-142">R2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-142">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="a9a3b-143">64 bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-143">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="a9a3b-144">Important</span><span class="sxs-lookup"><span data-stu-id="a9a3b-144">Important</span></span>**  
<span data-ttu-id="a9a3b-145">Le déploiement du rôle serveur de gestion sur un ordinateur sur lequel le partage de bureau à distance est activé n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-145">Deployment of the management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>



### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="a9a3b-146">Configuration matérielle requise pour le serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="a9a3b-146">Management Server hardware requirements</span></span>

-   <span data-ttu-id="a9a3b-147">Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-147">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="a9a3b-148">RAM: 1 Go de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-148">RAM— 1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="a9a3b-149">Disque dur: 200 Mo d’espace disque disponible, sans inclure le répertoire de contenu.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-149">Disk space—200 MB available hard disk space, not including the content directory.</span></span>

### <span data-ttu-id="a9a3b-150">Configuration requise du système d’exploitation du serveur de publication</span><span class="sxs-lookup"><span data-stu-id="a9a3b-150">Publishing Server operating system requirements</span></span>

<span data-ttu-id="a9a3b-151">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de serveur de publication 5,0 App-V.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-151">The following table lists the operating systems that are supported for the App-V 5.0 publishing server installation.</span></span>

**<span data-ttu-id="a9a3b-152">Remarque</span><span class="sxs-lookup"><span data-stu-id="a9a3b-152">Note</span></span>**  
<span data-ttu-id="a9a3b-153">Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-153">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="a9a3b-154">Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="a9a3b-154">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="a9a3b-155">Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="a9a3b-155">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9a3b-156">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="a9a3b-156">Operating system</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-157">Édition</span><span class="sxs-lookup"><span data-stu-id="a9a3b-157">Edition</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-158">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a9a3b-158">Service pack</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-159">Architecture système</span><span class="sxs-lookup"><span data-stu-id="a9a3b-159">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9a3b-160">Microsoft Windows Server 2008 (standard, entreprise, centre de connaissances ou serveur Web)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-160">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-161">R2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-161">R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-162">64 bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-162">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9a3b-163">Microsoft Windows Server 2012 (standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-163">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="a9a3b-164">64 bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-164">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9a3b-165">Microsoft Windows Server 2012 (standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-165">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-166">R2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-166">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="a9a3b-167">64 bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-167">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="a9a3b-168">Configuration matérielle requise pour le serveur de publication</span><span class="sxs-lookup"><span data-stu-id="a9a3b-168">Publishing Server hardware requirements</span></span>

-   <span data-ttu-id="a9a3b-169">Processeur: 1,4 GHz ou plus rapide.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-169">Processor—1.4 GHz or faster.</span></span> <span data-ttu-id="a9a3b-170">processeur 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-170">64-bit (x64) processor</span></span>

-   <span data-ttu-id="a9a3b-171">RAM: 2 Go de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-171">RAM— 2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="a9a3b-172">Disque dur: 200 Mo d’espace disque disponible.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-172">Disk space—200 MB available hard disk space.</span></span> <span data-ttu-id="a9a3b-173">Répertoire de contenu non inclus</span><span class="sxs-lookup"><span data-stu-id="a9a3b-173">not including content directory</span></span>

### <span data-ttu-id="a9a3b-174">Configuration requise pour le système d’exploitation du serveur de rapports</span><span class="sxs-lookup"><span data-stu-id="a9a3b-174">Reporting Server operating system requirements</span></span>

<span data-ttu-id="a9a3b-175">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de serveur de création de rapports App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-175">The following table lists the operating systems that are supported for the App-V 5.0 reporting server installation.</span></span>

**<span data-ttu-id="a9a3b-176">Remarque</span><span class="sxs-lookup"><span data-stu-id="a9a3b-176">Note</span></span>**  
<span data-ttu-id="a9a3b-177">Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-177">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="a9a3b-178">Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="a9a3b-178">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="a9a3b-179">Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="a9a3b-179">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9a3b-180">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="a9a3b-180">Operating system</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-181">Édition</span><span class="sxs-lookup"><span data-stu-id="a9a3b-181">Edition</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-182">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a9a3b-182">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-183">Architecture système</span><span class="sxs-lookup"><span data-stu-id="a9a3b-183">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9a3b-184">Microsoft Windows Server 2008 (standard, entreprise, centre de connaissances ou serveur Web)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-184">Microsoft Windows Server 2008 (Standard, Enterprise, Datacenter, or Web Server)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-185">R2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-185">R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-186">64 bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-186">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9a3b-187">Microsoft Windows Server 2012 (standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-187">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="a9a3b-188">64 bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-188">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9a3b-189">Microsoft Windows Server 2012 (standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-189">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-190">R2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-190">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="a9a3b-191">64 bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-191">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="a9a3b-192">Configuration matérielle requise pour le serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="a9a3b-192">Reporting Server hardware requirements</span></span>

-   <span data-ttu-id="a9a3b-193">Processeur: 1,4 GHz ou plus rapide.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-193">Processor—1.4 GHz or faster.</span></span> <span data-ttu-id="a9a3b-194">processeur 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-194">64-bit (x64) processor</span></span>

-   <span data-ttu-id="a9a3b-195">RAM: 2 Go de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-195">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="a9a3b-196">Espace disque disponible: 200 Mo d’espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="a9a3b-196">Disk space—200 MB available hard disk space</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="a9a3b-197">Configuration requise pour la base de données SQL Server</span><span class="sxs-lookup"><span data-stu-id="a9a3b-197">SQL Server database requirements</span></span>

<span data-ttu-id="a9a3b-198">Le tableau suivant répertorie les versions de SQL Server prises en charge pour la base de données et l’installation du serveur App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-198">The following table lists the SQL Server versions that are supported for the App-V 5.0 database and server installation.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9a3b-199">Type de serveur App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a9a3b-199">App-V 5.0 server type</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-200">Version de SQL Server</span><span class="sxs-lookup"><span data-stu-id="a9a3b-200">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-201">Édition</span><span class="sxs-lookup"><span data-stu-id="a9a3b-201">Edition</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-202">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a9a3b-202">Service pack</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-203">Architecture système</span><span class="sxs-lookup"><span data-stu-id="a9a3b-203">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9a3b-204">Gestion/création de rapports</span><span class="sxs-lookup"><span data-stu-id="a9a3b-204">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-205">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9a3b-205">Microsoft SQL Server 2008</span></span></p>
<p><span data-ttu-id="a9a3b-206">(Standard, entreprise, Datacenter ou édition développeur avec la fonctionnalité suivante: <strong> Services du moteur de base de données </strong> .)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-206">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-207">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-207">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9a3b-208">Gestion/création de rapports</span><span class="sxs-lookup"><span data-stu-id="a9a3b-208">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-209">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9a3b-209">Microsoft SQL Server 2008</span></span> </p>
<p><span data-ttu-id="a9a3b-210">(Standard, entreprise, Datacenter ou édition développeur avec la fonctionnalité suivante: <strong> Services du moteur de base de données </strong> .)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-210">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-211">R2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-211">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-212">SP2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-212">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-213">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-213">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9a3b-214">Gestion/création de rapports</span><span class="sxs-lookup"><span data-stu-id="a9a3b-214">Management / Reporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-215">MicrosoftSQLServer 2012</span><span class="sxs-lookup"><span data-stu-id="a9a3b-215">Microsoft SQL Server 2012</span></span></p>
<p><span data-ttu-id="a9a3b-216">(Standard, entreprise, Datacenter ou édition développeur avec la fonctionnalité suivante: <strong> Services du moteur de base de données </strong> .)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-216">(Standard, Enterprise, Datacenter, or the Developer Edition with the following feature: <strong>Database Engine Services</strong>.)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-217">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-217">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-client-supp-cfgs"></a> <span data-ttu-id="a9a3b-218">Configuration système requise pour le client App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a9a3b-218">App-V 5.0 client system requirements</span></span>


<span data-ttu-id="a9a3b-219">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-219">The following table lists the operating systems that are supported for the App-V 5.0 client installation.</span></span>

**<span data-ttu-id="a9a3b-220">Remarque</span><span class="sxs-lookup"><span data-stu-id="a9a3b-220">Note</span></span>**  
<span data-ttu-id="a9a3b-221">Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-221">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="a9a3b-222">Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="a9a3b-222">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="a9a3b-223">Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="a9a3b-223">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9a3b-224">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="a9a3b-224">Operating system</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-225">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a9a3b-225">Service pack</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-226">Architecture système</span><span class="sxs-lookup"><span data-stu-id="a9a3b-226">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9a3b-227">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9a3b-227">Microsoft Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-228">SP1</span><span class="sxs-lookup"><span data-stu-id="a9a3b-228">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-229">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-229">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9a3b-230">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="a9a3b-230">Microsoft Windows 8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-231">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-231">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong><span data-ttu-id="a9a3b-232">Important</span><span class="sxs-lookup"><span data-stu-id="a9a3b-232">Important</span></span></strong><br/><p><span data-ttu-id="a9a3b-233">Windows 8,1 est uniquement pris en charge par App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-233">Windows 8.1 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="a9a3b-234">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a9a3b-234">Windows 8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-235">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-235">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="a9a3b-236">Les scénarios d’installation du client App-V suivants ne sont pas pris en charge, sauf comme indiqué:</span><span class="sxs-lookup"><span data-stu-id="a9a3b-236">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="a9a3b-237">Ordinateurs exécutant Windows Server</span><span class="sxs-lookup"><span data-stu-id="a9a3b-237">Computers that run Windows Server</span></span>

-   <span data-ttu-id="a9a3b-238">Ordinateurs exécutant App-V 4,6 SP1 ou versions antérieures</span><span class="sxs-lookup"><span data-stu-id="a9a3b-238">Computers that run App-V 4.6 SP1 or earlier versions</span></span>

-   <span data-ttu-id="a9a3b-239">Le client App-V 5,0 Bureau à distance est uniquement pris en charge pour les serveurs RDS</span><span class="sxs-lookup"><span data-stu-id="a9a3b-239">The App-V 5.0 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="client-hardware-requirements-"></a><span data-ttu-id="a9a3b-240">Configuration matérielle requise pour le client</span><span class="sxs-lookup"><span data-stu-id="a9a3b-240">Client hardware requirements</span></span>

<span data-ttu-id="a9a3b-241">La liste suivante présente la configuration matérielle prise en charge pour l’installation du client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-241">The following list displays the supported hardware configuration for the App-V 5.0 client installation.</span></span>

-   <span data-ttu-id="a9a3b-242">Processeur: 1,4 GHz ou supérieur 32 bits (x86) ou processeur 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-242">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="a9a3b-243">RAM: 1 Go (32 bits) ou 2 Go (64 bits)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-243">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="a9a3b-244">Disque: 100 Mo pour l’installation, sans compter l’espace disque utilisé par les applications virtualisées.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-244">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <a href="" id="---------app-v-5-0-remote-desktop-client-system-requirements"></a> <span data-ttu-id="a9a3b-245">Configuration système requise pour le client de bureau à distance App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a9a3b-245">App-V 5.0 Remote Desktop client system requirements</span></span>


<span data-ttu-id="a9a3b-246">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client de bureau à distance App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-246">The following table lists the operating systems that are supported for App-V 5.0 Remote Desktop client installation.</span></span>

**<span data-ttu-id="a9a3b-247">Remarque</span><span class="sxs-lookup"><span data-stu-id="a9a3b-247">Note</span></span>**  
<span data-ttu-id="a9a3b-248">Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-248">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="a9a3b-249">Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="a9a3b-249">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="a9a3b-250">Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="a9a3b-250">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<span data-ttu-id="a9a3b-251">Operating System Edition Service Pack Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9a3b-251">Operating system Edition Service pack Microsoft Windows Server 2008</span></span>

<span data-ttu-id="a9a3b-252">R2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-252">R2</span></span>

<span data-ttu-id="a9a3b-253">SP1</span><span class="sxs-lookup"><span data-stu-id="a9a3b-253">SP1</span></span>

<span data-ttu-id="a9a3b-254">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9a3b-254">Microsoft Windows Server 2012</span></span>

**<span data-ttu-id="a9a3b-255">Important</span><span class="sxs-lookup"><span data-stu-id="a9a3b-255">Important</span></span>**  
<span data-ttu-id="a9a3b-256">Windows Server 2012 R2 est uniquement pris en charge par App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-256">Windows Server 2012 R2 is only supported by App-V 5.0 SP2</span></span>



<span data-ttu-id="a9a3b-257">Microsoft Windows Server 2012 (standard, Datacenter)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-257">Microsoft Windows Server 2012 (Standard, Datacenter)</span></span>

<span data-ttu-id="a9a3b-258">R2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-258">R2</span></span>

<span data-ttu-id="a9a3b-259">64 bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-259">64-bit</span></span>



### <a href="" id="remote-desktop-client-hardware-requirements-"></a><span data-ttu-id="a9a3b-260">Configuration matérielle requise pour le client Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="a9a3b-260">Remote Desktop client hardware requirements</span></span>

<span data-ttu-id="a9a3b-261">La liste suivante présente la configuration matérielle prise en charge pour l’installation du client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-261">The following list displays the supported hardware configuration for the App-V 5.0 client installation.</span></span>

-   <span data-ttu-id="a9a3b-262">Processeur: 1,4 GHz ou supérieur 32 bits (x86) ou processeur 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-262">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="a9a3b-263">RAM: 1 Go (32 bits) ou 2 Go (64 bits)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-263">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="a9a3b-264">Disque: 100 Mo pour l’installation, sans compter l’espace disque utilisé par les applications virtualisées.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-264">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <a href="" id="---------app-v-5-0-sequencer-system-requirements"></a> <span data-ttu-id="a9a3b-265">Configuration requise pour le Sequencer App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a9a3b-265">App-V 5.0 Sequencer system requirements</span></span>


<span data-ttu-id="a9a3b-266">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de Sequencer App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-266">The following table lists the operating systems that are supported for App-V 5.0 Sequencer installation.</span></span>

**<span data-ttu-id="a9a3b-267">Remarque</span><span class="sxs-lookup"><span data-stu-id="a9a3b-267">Note</span></span>**  
<span data-ttu-id="a9a3b-268">Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-268">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="a9a3b-269">Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="a9a3b-269">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="a9a3b-270">Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="a9a3b-270">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9a3b-271">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="a9a3b-271">Operating system</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-272">Édition</span><span class="sxs-lookup"><span data-stu-id="a9a3b-272">Edition</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-273">Service Pack</span><span class="sxs-lookup"><span data-stu-id="a9a3b-273">Service pack</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-274">Architecture système</span><span class="sxs-lookup"><span data-stu-id="a9a3b-274">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9a3b-275">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9a3b-275">Microsoft Windows 7</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="a9a3b-276">SP1</span><span class="sxs-lookup"><span data-stu-id="a9a3b-276">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-277">32bits et 64bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-277">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9a3b-278">Microsoft Windows 8</span><span class="sxs-lookup"><span data-stu-id="a9a3b-278">Microsoft Windows 8</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-279">32bits et 64bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-279">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong><span data-ttu-id="a9a3b-280">Important</span><span class="sxs-lookup"><span data-stu-id="a9a3b-280">Important</span></span></strong><br/><p><span data-ttu-id="a9a3b-281">Windows 8,1 est uniquement pris en charge par App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-281">Windows 8.1 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="a9a3b-282">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a9a3b-282">Windows 8.1</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-283">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-283">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9a3b-284">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9a3b-284">Microsoft Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-285">R2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-285">R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-286">SP1</span><span class="sxs-lookup"><span data-stu-id="a9a3b-286">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-287">32bits et 64bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-287">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9a3b-288">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9a3b-288">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-289">32bits et 64bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-289">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><div class="alert">
<strong><span data-ttu-id="a9a3b-290">Important</span><span class="sxs-lookup"><span data-stu-id="a9a3b-290">Important</span></span></strong><br/><p><span data-ttu-id="a9a3b-291">Windows Server 2012 R2 est uniquement pris en charge par App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-291">Windows Server 2012 R2 is only supported by App-V 5.0 SP2</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="a9a3b-292">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9a3b-292">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="a9a3b-293">R2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-293">R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="a9a3b-294">64 bits</span><span class="sxs-lookup"><span data-stu-id="a9a3b-294">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="a9a3b-295">Versions prises en charge de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a9a3b-295">Supported versions of System Center Configuration Manager</span></span>


<span data-ttu-id="a9a3b-296">Vous pouvez utiliser Microsoft System Center 2012 Configuration Manager ou System Center 2012 R2 Configuration Manager pour gérer les applications virtuelles App-V, la création de rapports et d’autres fonctions.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-296">You can use Microsoft System Center 2012 Configuration Manager or System Center 2012 R2 Configuration Manager to manage App-V virtual applications, reporting, and other functions.</span></span> <span data-ttu-id="a9a3b-297">Le tableau suivant répertorie les versions prises en charge de Configuration Manager pour chaque version applicable d’App-V.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-297">The following table lists the supported versions of Configuration Manager for each applicable version of App-V.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a9a3b-298">Version du gestionnaire de configurations prise en charge</span><span class="sxs-lookup"><span data-stu-id="a9a3b-298">Supported Configuration Manager version</span></span></th>
<th align="left"><span data-ttu-id="a9a3b-299">Version App-V</span><span class="sxs-lookup"><span data-stu-id="a9a3b-299">App-V version</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a9a3b-300">Gestionnaire de configuration de Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="a9a3b-300">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a9a3b-301">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a9a3b-301">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="a9a3b-302">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="a9a3b-302">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="a9a3b-303">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-303">App-V 5.0 SP2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a9a3b-304">System Center2012R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a9a3b-304">System Center 2012 R2 Configuration Manager</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a9a3b-305">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a9a3b-305">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="a9a3b-306">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="a9a3b-306">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="a9a3b-307">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="a9a3b-307">App-V 5.0 SP2</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



<span data-ttu-id="a9a3b-308">Pour plus d’informations sur l’intégration de Configuration Manager à l’application-V, voir [planification de l’intégration d’App-v à la Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="a9a3b-308">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>






## <span data-ttu-id="a9a3b-309">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a9a3b-309">Related topics</span></span>


[<span data-ttu-id="a9a3b-310">Envisager de déployer App-V</span><span class="sxs-lookup"><span data-stu-id="a9a3b-310">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="a9a3b-311">Composants requis d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="a9a3b-311">App-V 5.0 Prerequisites</span></span>](app-v-50-prerequisites.md)









