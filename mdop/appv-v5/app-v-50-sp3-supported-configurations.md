---
title: Configurations prises en charge d'App-V5.0 SP3
description: Configurations prises en charge d'App-V5.0 SP3
author: dansimp
ms.assetid: 08ced79a-0ed3-43c3-82e7-de01c1f33e81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b5a8858c703add3dc84c7eed4f62aa97e60ec9b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805994"
---
# <span data-ttu-id="b9881-103">Configurations prises en charge d'App-V5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="b9881-103">App-V 5.0 SP3 Supported Configurations</span></span>


<span data-ttu-id="b9881-104">Cette rubrique spécifie la configuration requise pour l’installation et l’exécution de Microsoft Application Virtualization (App-V) 5,0 SP3 dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="b9881-104">This topic specifies the requirements to install and run Microsoft Application Virtualization (App-V) 5.0 SP3 in your environment.</span></span>

## <span data-ttu-id="b9881-105">Configuration système requise pour App-V Server</span><span class="sxs-lookup"><span data-stu-id="b9881-105">App-V Server system requirements</span></span>


<span data-ttu-id="b9881-106">Cette section répertorie le système d’exploitation et la configuration matérielle requise pour tous les composants App-V Server.</span><span class="sxs-lookup"><span data-stu-id="b9881-106">This section lists the operating system and hardware requirements for all of the App-V Server components.</span></span>

### <span data-ttu-id="b9881-107">Scénarios de serveur App-V 5,0 SP3 non pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9881-107">Unsupported App-V 5.0 SP3 Server scenarios</span></span>

<span data-ttu-id="b9881-108">Le serveur App-V 5,0 SP3 ne prend pas en charge les scénarios suivants:</span><span class="sxs-lookup"><span data-stu-id="b9881-108">The App-V 5.0 SP3 Server does not support the following scenarios:</span></span>

-   <span data-ttu-id="b9881-109">Déploiement sur un ordinateur exécutant Microsoft Windows Server Core.</span><span class="sxs-lookup"><span data-stu-id="b9881-109">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="b9881-110">Déploiement sur un ordinateur qui exécute une version antérieure des composants serveur App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="b9881-110">Deployment to a computer that runs a previous version of App-V 5.0 SP3 Server components.</span></span> <span data-ttu-id="b9881-111">Vous pouvez installer l’application-V 5,0 SP3 côte à côte avec le serveur application-V 4.5 Lightweight Streaming Server (LWS) uniquement.</span><span class="sxs-lookup"><span data-stu-id="b9881-111">You can install App-V 5.0 SP3 side by side with the App-V4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="b9881-112">Le déploiement d’App-V côte à côte avec le serveur de gestion des services d’application (HWS) App-V 4,5 n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b9881-112">Deployment of App-V side by side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>

-   <span data-ttu-id="b9881-113">Déploiement sur un ordinateur qui exécute Microsoft SQL Server Express Edition.</span><span class="sxs-lookup"><span data-stu-id="b9881-113">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="b9881-114">Déploiement distant de la base de données du serveur de gestion ou de la base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="b9881-114">Remote deployment of the management server database or the reporting database.</span></span> <span data-ttu-id="b9881-115">Vous devez exécuter le programme d’installation directement sur l’ordinateur exécutant Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b9881-115">You must run the installer directly on the computer that is running Microsoft SQL Server.</span></span>

-   <span data-ttu-id="b9881-116">Déploiement sur un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="b9881-116">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="b9881-117">Chemins courts.</span><span class="sxs-lookup"><span data-stu-id="b9881-117">Short paths.</span></span> <span data-ttu-id="b9881-118">Si vous envisagez d’utiliser un chemin court, vous devez créer un nouveau volume.</span><span class="sxs-lookup"><span data-stu-id="b9881-118">If you plan to use a short path, you must create a new volume.</span></span>

### <span data-ttu-id="b9881-119">Configuration requise pour le système d’exploitation de Management Server</span><span class="sxs-lookup"><span data-stu-id="b9881-119">Management server operating system requirements</span></span>

<span data-ttu-id="b9881-120">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du serveur de gestion de l’application-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="b9881-120">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Management server installation.</span></span>

<span data-ttu-id="b9881-121">**Remarques**  Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent.</span><span class="sxs-lookup"><span data-stu-id="b9881-121">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="b9881-122">Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="b9881-122">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="b9881-123">Pour plus d’informations, consultez le [Forum aux questions sur la politique de support du support technique Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976) .</span><span class="sxs-lookup"><span data-stu-id="b9881-123">See [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) for more information.</span></span>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b9881-124">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="b9881-124">Operating system</span></span></th>
<th align="left"><span data-ttu-id="b9881-125">Service Pack</span><span class="sxs-lookup"><span data-stu-id="b9881-125">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="b9881-126">Architecture système</span><span class="sxs-lookup"><span data-stu-id="b9881-126">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-127">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b9881-127">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b9881-128">64 bits</span><span class="sxs-lookup"><span data-stu-id="b9881-128">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9881-129">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b9881-129">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b9881-130">64 bits</span><span class="sxs-lookup"><span data-stu-id="b9881-130">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-131">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9881-131">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-132">SP1</span><span class="sxs-lookup"><span data-stu-id="b9881-132">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-133">64 bits</span><span class="sxs-lookup"><span data-stu-id="b9881-133">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b9881-134">**Important**  Le déploiement du rôle serveur de gestion sur un ordinateur sur lequel le partage de bureau à distance est activé n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b9881-134">**Important** Deployment of the Management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>

 

### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="b9881-135">Configuration matérielle requise pour le serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="b9881-135">Management server hardware requirements</span></span>

-   <span data-ttu-id="b9881-136">Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="b9881-136">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="b9881-137">RAM: 1 Go de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="b9881-137">RAM—1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="b9881-138">Disque dur: 200 Mo d’espace disque disponible sans le répertoire de contenu</span><span class="sxs-lookup"><span data-stu-id="b9881-138">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="b9881-139">Exigences de base de données du serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="b9881-139">Management server database requirements</span></span>

<span data-ttu-id="b9881-140">Le tableau suivant répertorie les versions de SQL Server prises en charge pour l’installation de la base de données de gestion App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="b9881-140">The following table lists the SQL Server versions that are supported for the App-V 5.0 SP3 Management database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b9881-141">Version de SQL Server</span><span class="sxs-lookup"><span data-stu-id="b9881-141">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="b9881-142">Service Pack</span><span class="sxs-lookup"><span data-stu-id="b9881-142">Service pack</span></span></th>
<th align="left"><span data-ttu-id="b9881-143">Architecture système</span><span class="sxs-lookup"><span data-stu-id="b9881-143">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-144">MicrosoftSQLServer2014</span><span class="sxs-lookup"><span data-stu-id="b9881-144">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b9881-145">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="b9881-145">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9881-146">MicrosoftSQLServer 2012</span><span class="sxs-lookup"><span data-stu-id="b9881-146">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-147">SP2</span><span class="sxs-lookup"><span data-stu-id="b9881-147">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-148">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="b9881-148">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-149">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9881-149">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-150">3</span><span class="sxs-lookup"><span data-stu-id="b9881-150">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-151">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="b9881-151">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b9881-152">Configuration requise du système d’exploitation du serveur de publication</span><span class="sxs-lookup"><span data-stu-id="b9881-152">Publishing server operating system requirements</span></span>

<span data-ttu-id="b9881-153">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du serveur de publication App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="b9881-153">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Publishing server installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b9881-154">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="b9881-154">Operating system</span></span></th>
<th align="left"><span data-ttu-id="b9881-155">Service Pack</span><span class="sxs-lookup"><span data-stu-id="b9881-155">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="b9881-156">Architecture système</span><span class="sxs-lookup"><span data-stu-id="b9881-156">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-157">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b9881-157">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b9881-158">64 bits</span><span class="sxs-lookup"><span data-stu-id="b9881-158">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9881-159">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b9881-159">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b9881-160">64 bits</span><span class="sxs-lookup"><span data-stu-id="b9881-160">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-161">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9881-161">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-162">SP1</span><span class="sxs-lookup"><span data-stu-id="b9881-162">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-163">64 bits</span><span class="sxs-lookup"><span data-stu-id="b9881-163">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="b9881-164">Configuration matérielle requise pour le serveur de publication</span><span class="sxs-lookup"><span data-stu-id="b9881-164">Publishing server hardware requirements</span></span>

<span data-ttu-id="b9881-165">App-V n’ajoute aucune configuration requise supplémentaire au-delà de celles de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="b9881-165">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="b9881-166">Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="b9881-166">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="b9881-167">RAM: 2 Go de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="b9881-167">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="b9881-168">Disque dur: 200 Mo d’espace disque disponible sans le répertoire de contenu</span><span class="sxs-lookup"><span data-stu-id="b9881-168">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="b9881-169">Configuration requise pour le système d’exploitation du serveur de rapports</span><span class="sxs-lookup"><span data-stu-id="b9881-169">Reporting server operating system requirements</span></span>

<span data-ttu-id="b9881-170">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du serveur de création de rapports App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="b9881-170">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Reporting server installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b9881-171">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="b9881-171">Operating system</span></span></th>
<th align="left"><span data-ttu-id="b9881-172">Service Pack</span><span class="sxs-lookup"><span data-stu-id="b9881-172">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="b9881-173">Architecture système</span><span class="sxs-lookup"><span data-stu-id="b9881-173">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-174">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b9881-174">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b9881-175">64 bits</span><span class="sxs-lookup"><span data-stu-id="b9881-175">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9881-176">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b9881-176">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b9881-177">64 bits</span><span class="sxs-lookup"><span data-stu-id="b9881-177">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-178">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9881-178">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-179">SP1</span><span class="sxs-lookup"><span data-stu-id="b9881-179">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-180">64 bits</span><span class="sxs-lookup"><span data-stu-id="b9881-180">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="b9881-181">Configuration matérielle requise pour le serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="b9881-181">Reporting server hardware requirements</span></span>

<span data-ttu-id="b9881-182">App-V n’ajoute aucune configuration requise supplémentaire au-delà de celles de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="b9881-182">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="b9881-183">Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="b9881-183">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="b9881-184">RAM: 2 Go de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="b9881-184">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="b9881-185">Espace disque disponible: 200 Mo d’espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="b9881-185">Disk space—200 MB available hard disk space</span></span>

### <span data-ttu-id="b9881-186">Configuration requise pour la base de données serveur de rapport</span><span class="sxs-lookup"><span data-stu-id="b9881-186">Reporting server database requirements</span></span>

<span data-ttu-id="b9881-187">Le tableau suivant répertorie les versions de SQL Server prises en charge pour l’installation de la base de données de création de rapports App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="b9881-187">The following table lists the SQL Server versions that are supported for the App-V 5.0 SP3 Reporting database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b9881-188">Version de SQL Server</span><span class="sxs-lookup"><span data-stu-id="b9881-188">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="b9881-189">Service Pack</span><span class="sxs-lookup"><span data-stu-id="b9881-189">Service pack</span></span></th>
<th align="left"><span data-ttu-id="b9881-190">Architecture système</span><span class="sxs-lookup"><span data-stu-id="b9881-190">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-191">MicrosoftSQLServer2014</span><span class="sxs-lookup"><span data-stu-id="b9881-191">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b9881-192">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="b9881-192">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9881-193">MicrosoftSQLServer 2012</span><span class="sxs-lookup"><span data-stu-id="b9881-193">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-194">SP2</span><span class="sxs-lookup"><span data-stu-id="b9881-194">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-195">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="b9881-195">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-196">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9881-196">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-197">3</span><span class="sxs-lookup"><span data-stu-id="b9881-197">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-198">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="b9881-198">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a><span data-ttu-id="b9881-199">Configuration système requise pour le client App-V</span><span class="sxs-lookup"><span data-stu-id="b9881-199">App-V client system requirements</span></span>


<span data-ttu-id="b9881-200">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="b9881-200">The following table lists the operating systems that are supported for the App-V 5.0 SP3 client installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b9881-201">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="b9881-201">Operating system</span></span></th>
<th align="left"><span data-ttu-id="b9881-202">Service Pack</span><span class="sxs-lookup"><span data-stu-id="b9881-202">Service pack</span></span></th>
<th align="left"><span data-ttu-id="b9881-203">Architecture système</span><span class="sxs-lookup"><span data-stu-id="b9881-203">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-204">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b9881-204">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b9881-205">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="b9881-205">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9881-206">Microsoft Windows8</span><span class="sxs-lookup"><span data-stu-id="b9881-206">Microsoft Windows8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b9881-207">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="b9881-207">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-208">Plus de.</span><span class="sxs-lookup"><span data-stu-id="b9881-208">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-209">SP1</span><span class="sxs-lookup"><span data-stu-id="b9881-209">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-210">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="b9881-210">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b9881-211">Les scénarios d’installation du client App-V suivants ne sont pas pris en charge, sauf comme indiqué:</span><span class="sxs-lookup"><span data-stu-id="b9881-211">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="b9881-212">Ordinateurs exécutant Windows Server</span><span class="sxs-lookup"><span data-stu-id="b9881-212">Computers that run Windows Server</span></span>

-   <span data-ttu-id="b9881-213">Ordinateurs exécutant App-V 4.6 SP1 ou une version antérieure</span><span class="sxs-lookup"><span data-stu-id="b9881-213">Computers that run App-V4.6SP1 or earlier versions</span></span>

-   <span data-ttu-id="b9881-214">Le client App-V 5,0 SP3 service bureau à distance est uniquement pris en charge pour les serveurs RDS</span><span class="sxs-lookup"><span data-stu-id="b9881-214">The App-V 5.0 SP3 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="app-v-client-hardware-requirements-"></a><span data-ttu-id="b9881-215">Configuration matérielle requise pour le client App-V</span><span class="sxs-lookup"><span data-stu-id="b9881-215">App-V client hardware requirements</span></span>

<span data-ttu-id="b9881-216">La liste suivante présente la configuration matérielle prise en charge pour l’installation du client App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="b9881-216">The following list displays the supported hardware configuration for the App-V 5.0 SP3 client installation.</span></span>

-   <span data-ttu-id="b9881-217">Processeur: 1,4 GHz ou supérieur 32 bits (x86) ou processeur 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="b9881-217">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="b9881-218">RAM: 1 Go (32 bits) ou 2 Go (64 bits)</span><span class="sxs-lookup"><span data-stu-id="b9881-218">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="b9881-219">Disque: 100 Mo pour l’installation, sans compter l’espace disque utilisé par les applications virtualisées.</span><span class="sxs-lookup"><span data-stu-id="b9881-219">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <span data-ttu-id="b9881-220">Configuration système requise pour le client Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="b9881-220">Remote Desktop Services client system requirements</span></span>


<span data-ttu-id="b9881-221">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client App-V 5,0 SP3 (Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="b9881-221">The following table lists the operating systems that are supported for App-V 5.0 SP3 Remote Desktop Services (RDS) client installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b9881-222">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="b9881-222">Operating system</span></span></th>
<th align="left"><span data-ttu-id="b9881-223">Service Pack</span><span class="sxs-lookup"><span data-stu-id="b9881-223">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="b9881-224">Architecture système</span><span class="sxs-lookup"><span data-stu-id="b9881-224">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-225">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b9881-225">Microsoft Windows Server 2012 R2</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b9881-226">64 bits</span><span class="sxs-lookup"><span data-stu-id="b9881-226">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9881-227">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b9881-227">Microsoft Windows Server 2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b9881-228">64 bits</span><span class="sxs-lookup"><span data-stu-id="b9881-228">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-229">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9881-229">Microsoft Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-230">SP1</span><span class="sxs-lookup"><span data-stu-id="b9881-230">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-231">64 bits</span><span class="sxs-lookup"><span data-stu-id="b9881-231">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b9881-232">Configuration matérielle requise pour le client Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="b9881-232">Remote Desktop Services client hardware requirements</span></span>

<span data-ttu-id="b9881-233">App-V n’ajoute aucune configuration requise supplémentaire au-delà de celles de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="b9881-233">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="b9881-234">Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="b9881-234">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="b9881-235">RAM: 2 Go de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="b9881-235">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="b9881-236">Espace disque disponible: 200 Mo d’espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="b9881-236">Disk space—200 MB available hard disk space</span></span>

## <span data-ttu-id="b9881-237">Configuration requise pour le Sequencer</span><span class="sxs-lookup"><span data-stu-id="b9881-237">Sequencer system requirements</span></span>


<span data-ttu-id="b9881-238">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de Sequencer App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="b9881-238">The following table lists the operating systems that are supported for the App-V 5.0 SP3 Sequencer installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b9881-239">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="b9881-239">Operating system</span></span></th>
<th align="left"><span data-ttu-id="b9881-240">Service Pack</span><span class="sxs-lookup"><span data-stu-id="b9881-240">Service pack</span></span></th>
<th align="left"><span data-ttu-id="b9881-241">Architecture système</span><span class="sxs-lookup"><span data-stu-id="b9881-241">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-242">Microsoft Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="b9881-242">Microsoft Windows Server2012 R2</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="b9881-243">64 bits</span><span class="sxs-lookup"><span data-stu-id="b9881-243">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9881-244">Microsoft Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="b9881-244">Microsoft Windows Server2012</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b9881-245">64 bits</span><span class="sxs-lookup"><span data-stu-id="b9881-245">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-246">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9881-246">Microsoft Windows Server2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-247">SP1</span><span class="sxs-lookup"><span data-stu-id="b9881-247">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-248">64 bits</span><span class="sxs-lookup"><span data-stu-id="b9881-248">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9881-249">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b9881-249">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b9881-250">32bits et 64bits</span><span class="sxs-lookup"><span data-stu-id="b9881-250">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9881-251">Microsoft Windows8</span><span class="sxs-lookup"><span data-stu-id="b9881-251">Microsoft Windows8</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b9881-252">32bits et 64bits</span><span class="sxs-lookup"><span data-stu-id="b9881-252">32-bit and 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9881-253">Microsoft</span><span class="sxs-lookup"><span data-stu-id="b9881-253">Microsoft Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-254">SP1</span><span class="sxs-lookup"><span data-stu-id="b9881-254">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9881-255">32bits et 64bits</span><span class="sxs-lookup"><span data-stu-id="b9881-255">32-bit and 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b9881-256">Configuration matérielle requise pour le Sequencer</span><span class="sxs-lookup"><span data-stu-id="b9881-256">Sequencer hardware requirements</span></span>

<span data-ttu-id="b9881-257">Pour connaître la configuration matérielle requise, voir la documentation de Windows ou Windows Server.</span><span class="sxs-lookup"><span data-stu-id="b9881-257">See the Windows or Windows Server documentation for the hardware requirements.</span></span> <span data-ttu-id="b9881-258">App-V n’ajoute aucune configuration matérielle supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="b9881-258">App-V adds no additional hardware requirements.</span></span>

## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="b9881-259">Versions prises en charge de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b9881-259">Supported versions of System Center Configuration Manager</span></span>


<span data-ttu-id="b9881-260">Le client App-V prend en charge les versions suivantes de System Center Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="b9881-260">The App-V client supports the following versions of System Center Configuration Manager:</span></span>

-   <span data-ttu-id="b9881-261">MicrosoftSystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="b9881-261">MicrosoftSystemCenter2012 ConfigurationManager</span></span>

-   <span data-ttu-id="b9881-262">System Center2012R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b9881-262">System Center 2012 R2 Configuration Manager</span></span>

-   <span data-ttu-id="b9881-263">System Center2012R2 ConfigurationManagerSP1</span><span class="sxs-lookup"><span data-stu-id="b9881-263">System Center 2012 R2 Configuration Manager SP1</span></span>

<span data-ttu-id="b9881-264">Pour plus d’informations sur l’intégration de Configuration Manager à l’application-V, voir [planification de l’intégration d’App-v à la Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="b9881-264">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>






## <span data-ttu-id="b9881-265">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b9881-265">Related topics</span></span>


[<span data-ttu-id="b9881-266">Envisager de déployer App-V</span><span class="sxs-lookup"><span data-stu-id="b9881-266">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

[<span data-ttu-id="b9881-267">Composants requis d'App-V5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="b9881-267">App-V 5.0 SP3 Prerequisites</span></span>](app-v-50-sp3-prerequisites.md)

 

 





