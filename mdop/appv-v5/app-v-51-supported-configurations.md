---
title: Configurations prises en charge par App-V5.1
description: Configurations prises en charge par App-V5.1
author: dansimp
ms.assetid: 8b8db63b-f71c-4ae9-80e7-a6752334e1f6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/02/2020
ms.openlocfilehash: fbda364de66b1f7b8730dca38f864a84f7848e58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805941"
---
# <span data-ttu-id="45498-103">Configurations prises en charge par App-V5.1</span><span class="sxs-lookup"><span data-stu-id="45498-103">App-V 5.1 Supported Configurations</span></span>

><span data-ttu-id="45498-104">S’applique à: Windows 10, version 1607; Windows Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (mise à jour de sécurité étendue)</span><span class="sxs-lookup"><span data-stu-id="45498-104">Applies to: Windows 10, version 1607; Window Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (Extended Security Update)</span></span>

<span data-ttu-id="45498-105">Cette rubrique spécifie la configuration requise pour l’installation et l’exécution de Microsoft Application Virtualization (App-V) 5,1 dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="45498-105">This topic specifies the requirements to install and run Microsoft Application Virtualization (App-V) 5.1 in your environment.</span></span>

## <span data-ttu-id="45498-106">Configuration système requise pour App-V Server</span><span class="sxs-lookup"><span data-stu-id="45498-106">App-V Server system requirements</span></span>

<span data-ttu-id="45498-107">Cette section répertorie le système d’exploitation et la configuration matérielle requise pour tous les composants App-V Server.</span><span class="sxs-lookup"><span data-stu-id="45498-107">This section lists the operating system and hardware requirements for all of the App-V Server components.</span></span>

### <span data-ttu-id="45498-108">Scénarios App-V 5,1 Server non pris en charge</span><span class="sxs-lookup"><span data-stu-id="45498-108">Unsupported App-V 5.1 Server scenarios</span></span>

<span data-ttu-id="45498-109">Le serveur App-V 5,1 ne prend pas en charge les scénarios suivants:</span><span class="sxs-lookup"><span data-stu-id="45498-109">The App-V 5.1 Server does not support the following scenarios:</span></span>

-   <span data-ttu-id="45498-110">Déploiement sur un ordinateur exécutant Microsoft Windows Server Core.</span><span class="sxs-lookup"><span data-stu-id="45498-110">Deployment to a computer that runs Microsoft Windows Server Core.</span></span>

-   <span data-ttu-id="45498-111">Déploiement sur un ordinateur qui exécute une version antérieure des composants serveur App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="45498-111">Deployment to a computer that runs a previous version of App-V 5.1 Server components.</span></span> <span data-ttu-id="45498-112">Vous pouvez installer l’application-V 5,1 côte à côte avec l’App-V 4.5 Lightweight Streaming Server (LWS) uniquement.</span><span class="sxs-lookup"><span data-stu-id="45498-112">You can install App-V 5.1 side by side with the App-V4.5 Lightweight Streaming Server (LWS) server only.</span></span> <span data-ttu-id="45498-113">Le déploiement d’App-V côte à côte avec le serveur de gestion des services d’application (HWS) App-V 4,5 n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="45498-113">Deployment of App-V side by side with the App-V 4.5 Application Virtualization Management Service (HWS) server is not supported.</span></span>

-   <span data-ttu-id="45498-114">Déploiement sur un ordinateur qui exécute Microsoft SQL Server Express Edition.</span><span class="sxs-lookup"><span data-stu-id="45498-114">Deployment to a computer that runs Microsoft SQL Server Express edition.</span></span>

-   <span data-ttu-id="45498-115">Déploiement sur un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="45498-115">Deployment to a domain controller.</span></span>

-   <span data-ttu-id="45498-116">Chemins courts.</span><span class="sxs-lookup"><span data-stu-id="45498-116">Short paths.</span></span> <span data-ttu-id="45498-117">Si vous envisagez d’utiliser un chemin court, vous devez créer un nouveau volume.</span><span class="sxs-lookup"><span data-stu-id="45498-117">If you plan to use a short path, you must create a new volume.</span></span>

### <span data-ttu-id="45498-118">Configuration requise pour le système d’exploitation de Management Server</span><span class="sxs-lookup"><span data-stu-id="45498-118">Management server operating system requirements</span></span>

<span data-ttu-id="45498-119">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation d’App-V 5,1 Management Server.</span><span class="sxs-lookup"><span data-stu-id="45498-119">The following table lists the operating systems that are supported for the App-V 5.1 Management server installation.</span></span>

> [!NOTE]
> <span data-ttu-id="45498-120">Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent.</span><span class="sxs-lookup"><span data-stu-id="45498-120">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="45498-121">Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="45498-121">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="45498-122">Pour plus d’informations, consultez le [Forum aux questions sur la politique de support du support technique Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976) .</span><span class="sxs-lookup"><span data-stu-id="45498-122">See [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976) for more information.</span></span>

 | <span data-ttu-id="45498-123">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="45498-123">Operating System</span></span>                 | <span data-ttu-id="45498-124">Service Pack</span><span class="sxs-lookup"><span data-stu-id="45498-124">Service Pack</span></span> | <span data-ttu-id="45498-125">Architecture système</span><span class="sxs-lookup"><span data-stu-id="45498-125">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="45498-126">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="45498-126">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="45498-127">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-127">64-bit</span></span>       |
| <span data-ttu-id="45498-128">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="45498-128">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="45498-129">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-129">64-bit</span></span>       |
| <span data-ttu-id="45498-130">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="45498-130">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="45498-131">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-131">64-bit</span></span>       |
| <span data-ttu-id="45498-132">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45498-132">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="45498-133">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-133">64-bit</span></span>       |
| <span data-ttu-id="45498-134">[Mise à jour de sécurité étendue](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="45498-134">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span>|      <span data-ttu-id="45498-135">SP1</span><span class="sxs-lookup"><span data-stu-id="45498-135">SP1</span></span>     |        <span data-ttu-id="45498-136">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-136">64-bit</span></span>       |
 

<span data-ttu-id="45498-137">**Important**  Le déploiement du rôle serveur de gestion sur un ordinateur sur lequel le partage de bureau à distance est activé n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="45498-137">**Important** Deployment of the Management server role to a computer with Remote Desktop Sharing (RDS) enabled is not supported.</span></span>

 

### <a href="" id="management-server-hardware-requirements-"></a><span data-ttu-id="45498-138">Configuration matérielle requise pour le serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="45498-138">Management server hardware requirements</span></span>

-   <span data-ttu-id="45498-139">Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="45498-139">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="45498-140">RAM: 1 Go de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="45498-140">RAM—1 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="45498-141">Disque dur: 200 Mo d’espace disque disponible sans le répertoire de contenu</span><span class="sxs-lookup"><span data-stu-id="45498-141">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="45498-142">Exigences de base de données du serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="45498-142">Management server database requirements</span></span>

<span data-ttu-id="45498-143">Le tableau suivant répertorie les versions de SQL Server prises en charge pour l’installation de la base de données de gestion App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="45498-143">The following table lists the SQL Server versions that are supported for the App-V 5.1 Management database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="45498-144">Version de SQL Server</span><span class="sxs-lookup"><span data-stu-id="45498-144">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="45498-145">Service Pack</span><span class="sxs-lookup"><span data-stu-id="45498-145">Service pack</span></span></th>
<th align="left"><span data-ttu-id="45498-146">Architecture système</span><span class="sxs-lookup"><span data-stu-id="45498-146">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="45498-147">Microsoft SQL Server 2019</span><span class="sxs-lookup"><span data-stu-id="45498-147">Microsoft SQL Server 2019</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45498-148">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-148">32-bit or 64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="45498-149">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="45498-149">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45498-150">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-150">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45498-151">MicrosoftSQLServer2016</span><span class="sxs-lookup"><span data-stu-id="45498-151">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-152">SP2</span><span class="sxs-lookup"><span data-stu-id="45498-152">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-153">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-153">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45498-154">MicrosoftSQLServer2014</span><span class="sxs-lookup"><span data-stu-id="45498-154">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-155">SP2</span><span class="sxs-lookup"><span data-stu-id="45498-155">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-156">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-156">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45498-157">MicrosoftSQLServer 2012</span><span class="sxs-lookup"><span data-stu-id="45498-157">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-158">SP2</span><span class="sxs-lookup"><span data-stu-id="45498-158">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-159">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-159">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45498-160">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="45498-160">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-161">3</span><span class="sxs-lookup"><span data-stu-id="45498-161">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-162">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-162">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="45498-163">Pour plus d’informations sur les fichiers de configuration utilisateur avec SQL Server 2016 ou une version ultérieure, voir l' [article de support technique](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).</span><span class="sxs-lookup"><span data-stu-id="45498-163">For more information on user configuration files with SQL server 2016 or later, see the [support article](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).</span></span>

### <span data-ttu-id="45498-164">Configuration requise du système d’exploitation du serveur de publication</span><span class="sxs-lookup"><span data-stu-id="45498-164">Publishing server operating system requirements</span></span>

<span data-ttu-id="45498-165">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de serveur de publication 5,1 App-V.</span><span class="sxs-lookup"><span data-stu-id="45498-165">The following table lists the operating systems that are supported for the App-V 5.1 Publishing server installation.</span></span>

| <span data-ttu-id="45498-166">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="45498-166">Operating System</span></span>                 | <span data-ttu-id="45498-167">Service Pack</span><span class="sxs-lookup"><span data-stu-id="45498-167">Service Pack</span></span> | <span data-ttu-id="45498-168">Architecture système</span><span class="sxs-lookup"><span data-stu-id="45498-168">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="45498-169">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="45498-169">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="45498-170">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-170">64-bit</span></span>       |
| <span data-ttu-id="45498-171">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="45498-171">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="45498-172">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-172">64-bit</span></span>       |
| <span data-ttu-id="45498-173">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="45498-173">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="45498-174">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-174">64-bit</span></span>       |
| <span data-ttu-id="45498-175">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45498-175">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="45498-176">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-176">64-bit</span></span>       |
| <span data-ttu-id="45498-177">[Mise à jour de sécurité étendue](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="45498-177">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="45498-178">SP1</span><span class="sxs-lookup"><span data-stu-id="45498-178">SP1</span></span>     |        <span data-ttu-id="45498-179">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-179">64-bit</span></span>       |

### <a href="" id="publishing-server-hardware-requirements-"></a><span data-ttu-id="45498-180">Configuration matérielle requise pour le serveur de publication</span><span class="sxs-lookup"><span data-stu-id="45498-180">Publishing server hardware requirements</span></span>

<span data-ttu-id="45498-181">App-V n’ajoute aucune configuration requise supplémentaire au-delà de celles de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="45498-181">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="45498-182">Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="45498-182">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="45498-183">RAM: 2 Go de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="45498-183">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="45498-184">Disque dur: 200 Mo d’espace disque disponible sans le répertoire de contenu</span><span class="sxs-lookup"><span data-stu-id="45498-184">Disk space—200 MB available hard disk space, not including the content directory</span></span>

### <span data-ttu-id="45498-185">Configuration requise pour le système d’exploitation du serveur de rapports</span><span class="sxs-lookup"><span data-stu-id="45498-185">Reporting server operating system requirements</span></span>

<span data-ttu-id="45498-186">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de serveur de création de rapports App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="45498-186">The following table lists the operating systems that are supported for the App-V 5.1 Reporting server installation.</span></span>

| <span data-ttu-id="45498-187">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="45498-187">Operating System</span></span>                 | <span data-ttu-id="45498-188">Service Pack</span><span class="sxs-lookup"><span data-stu-id="45498-188">Service Pack</span></span> | <span data-ttu-id="45498-189">Architecture système</span><span class="sxs-lookup"><span data-stu-id="45498-189">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="45498-190">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="45498-190">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="45498-191">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-191">64-bit</span></span>       |
| <span data-ttu-id="45498-192">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="45498-192">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="45498-193">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-193">64-bit</span></span>       |
| <span data-ttu-id="45498-194">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="45498-194">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="45498-195">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-195">64-bit</span></span>       |
| <span data-ttu-id="45498-196">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45498-196">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="45498-197">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-197">64-bit</span></span>       |
| <span data-ttu-id="45498-198">[Mise à jour de sécurité étendue](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="45498-198">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="45498-199">SP1</span><span class="sxs-lookup"><span data-stu-id="45498-199">SP1</span></span>     |        <span data-ttu-id="45498-200">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-200">64-bit</span></span>       |

### <a href="" id="reporting-server-hardware-requirements-"></a><span data-ttu-id="45498-201">Configuration matérielle requise pour le serveur de création de rapports</span><span class="sxs-lookup"><span data-stu-id="45498-201">Reporting server hardware requirements</span></span>

<span data-ttu-id="45498-202">App-V n’ajoute aucune configuration requise supplémentaire au-delà de celles de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="45498-202">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="45498-203">Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="45498-203">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="45498-204">RAM: 2 Go de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="45498-204">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="45498-205">Espace disque disponible: 200 Mo d’espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="45498-205">Disk space—200 MB available hard disk space</span></span>

### <span data-ttu-id="45498-206">Configuration requise pour la base de données serveur de rapport</span><span class="sxs-lookup"><span data-stu-id="45498-206">Reporting server database requirements</span></span>

<span data-ttu-id="45498-207">Le tableau suivant répertorie les versions de SQL Server prises en charge pour l’installation de la base de données de création de rapports App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="45498-207">The following table lists the SQL Server versions that are supported for the App-V 5.1 Reporting database installation.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="45498-208">Version de SQL Server</span><span class="sxs-lookup"><span data-stu-id="45498-208">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="45498-209">Service Pack</span><span class="sxs-lookup"><span data-stu-id="45498-209">Service pack</span></span></th>
<th align="left"><span data-ttu-id="45498-210">Architecture système</span><span class="sxs-lookup"><span data-stu-id="45498-210">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45498-211">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="45498-211">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45498-212">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-212">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45498-213">MicrosoftSQLServer2016</span><span class="sxs-lookup"><span data-stu-id="45498-213">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-214">SP2</span><span class="sxs-lookup"><span data-stu-id="45498-214">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-215">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-215">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45498-216">MicrosoftSQLServer2014</span><span class="sxs-lookup"><span data-stu-id="45498-216">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-217">SP2</span><span class="sxs-lookup"><span data-stu-id="45498-217">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-218">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-218">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45498-219">MicrosoftSQLServer 2012</span><span class="sxs-lookup"><span data-stu-id="45498-219">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-220">SP2</span><span class="sxs-lookup"><span data-stu-id="45498-220">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-221">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-221">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45498-222">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="45498-222">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-223">3</span><span class="sxs-lookup"><span data-stu-id="45498-223">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-224">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-224">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a><span data-ttu-id="45498-225">Configuration système requise pour le client App-V</span><span class="sxs-lookup"><span data-stu-id="45498-225">App-V client system requirements</span></span>

<span data-ttu-id="45498-226">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="45498-226">The following table lists the operating systems that are supported for the App-V 5.1 client installation.</span></span>

> [!NOTE]
> <span data-ttu-id="45498-227">Dans le cadre de la mise à jour anniversaire Windows 10 (c’est-à-dire la version 1607), le client App-V est en cours de blocage de l’installation de toute version antérieure du client App-V.</span><span class="sxs-lookup"><span data-stu-id="45498-227">With the Windows 10 Anniversary release (aka 1607 version), the App-V client is in-box and will block installation of any previous version of the App-V client</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="45498-228">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="45498-228">Operating system</span></span></th>
<th align="left"><span data-ttu-id="45498-229">Service Pack</span><span class="sxs-lookup"><span data-stu-id="45498-229">Service pack</span></span></th>
<th align="left"><span data-ttu-id="45498-230">Architecture système</span><span class="sxs-lookup"><span data-stu-id="45498-230">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45498-231">Microsoft Windows 10 (version antérieure à 1607)</span><span class="sxs-lookup"><span data-stu-id="45498-231">Microsoft Windows10 (pre-1607 version)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45498-232">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-232">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45498-233">Microsoft Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="45498-233">Microsoft Windows8.1</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="45498-234">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-234">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45498-235">Plus de.</span><span class="sxs-lookup"><span data-stu-id="45498-235">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-236">SP1</span><span class="sxs-lookup"><span data-stu-id="45498-236">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-237">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-237">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="45498-238">Les scénarios d’installation du client App-V suivants ne sont pas pris en charge, sauf comme indiqué:</span><span class="sxs-lookup"><span data-stu-id="45498-238">The following App-V client installation scenarios are not supported, except as noted:</span></span>

-   <span data-ttu-id="45498-239">Ordinateurs exécutant Windows Server</span><span class="sxs-lookup"><span data-stu-id="45498-239">Computers that run Windows Server</span></span>

-   <span data-ttu-id="45498-240">Ordinateurs exécutant App-V 4.6 SP1 ou une version antérieure</span><span class="sxs-lookup"><span data-stu-id="45498-240">Computers that run App-V4.6SP1 or earlier versions</span></span>

-   <span data-ttu-id="45498-241">Le client App-V 5,1 Bureau à distance est uniquement pris en charge pour les serveurs RDS</span><span class="sxs-lookup"><span data-stu-id="45498-241">The App-V 5.1 Remote Desktop services client is supported only for RDS-enabled servers</span></span>

### <a href="" id="app-v-client-hardware-requirements-"></a><span data-ttu-id="45498-242">Configuration matérielle requise pour le client App-V</span><span class="sxs-lookup"><span data-stu-id="45498-242">App-V client hardware requirements</span></span>

<span data-ttu-id="45498-243">La liste suivante présente la configuration matérielle prise en charge pour l’installation du client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="45498-243">The following list displays the supported hardware configuration for the App-V 5.1 client installation.</span></span>

-   <span data-ttu-id="45498-244">Processeur: 1,4 GHz ou supérieur 32 bits (x86) ou processeur 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="45498-244">Processor— 1.4 GHz or faster 32-bit (x86) or 64-bit (x64) processor</span></span>

-   <span data-ttu-id="45498-245">RAM: 1 Go (32 bits) ou 2 Go (64 bits)</span><span class="sxs-lookup"><span data-stu-id="45498-245">RAM— 1 GB (32-bit) or 2 GB (64-bit)</span></span>

-   <span data-ttu-id="45498-246">Disque: 100 Mo pour l’installation, sans compter l’espace disque utilisé par les applications virtualisées.</span><span class="sxs-lookup"><span data-stu-id="45498-246">Disk— 100 MB for installation, not including the disk space that is used by virtualized applications.</span></span>

## <span data-ttu-id="45498-247">Configuration système requise pour le client Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="45498-247">Remote Desktop Services client system requirements</span></span>


<span data-ttu-id="45498-248">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client App-V 5,1 Desktop Services (RDS).</span><span class="sxs-lookup"><span data-stu-id="45498-248">The following table lists the operating systems that are supported for App-V 5.1 Remote Desktop Services (RDS) client installation.</span></span>

| <span data-ttu-id="45498-249">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="45498-249">Operating System</span></span>                 | <span data-ttu-id="45498-250">Service Pack</span><span class="sxs-lookup"><span data-stu-id="45498-250">Service Pack</span></span> | <span data-ttu-id="45498-251">Architecture système</span><span class="sxs-lookup"><span data-stu-id="45498-251">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="45498-252">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="45498-252">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="45498-253">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-253">64-bit</span></span>       |
| <span data-ttu-id="45498-254">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="45498-254">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="45498-255">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-255">64-bit</span></span>       |
| <span data-ttu-id="45498-256">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="45498-256">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="45498-257">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-257">64-bit</span></span>       |
| <span data-ttu-id="45498-258">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45498-258">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="45498-259">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-259">64-bit</span></span>       |
| <span data-ttu-id="45498-260">[Mise à jour de sécurité étendue](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="45498-260">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="45498-261">SP1</span><span class="sxs-lookup"><span data-stu-id="45498-261">SP1</span></span>     |        <span data-ttu-id="45498-262">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-262">64-bit</span></span>       |

### <span data-ttu-id="45498-263">Configuration matérielle requise pour le client Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="45498-263">Remote Desktop Services client hardware requirements</span></span>

<span data-ttu-id="45498-264">App-V n’ajoute aucune configuration requise supplémentaire au-delà de celles de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="45498-264">App-V adds no additional requirements beyond those of Windows Server.</span></span>

-   <span data-ttu-id="45498-265">Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)</span><span class="sxs-lookup"><span data-stu-id="45498-265">Processor—1.4 GHz or faster, 64-bit (x64) processor</span></span>

-   <span data-ttu-id="45498-266">RAM: 2 Go de RAM (64 bits)</span><span class="sxs-lookup"><span data-stu-id="45498-266">RAM—2 GB RAM (64-bit)</span></span>

-   <span data-ttu-id="45498-267">Espace disque disponible: 200 Mo d’espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="45498-267">Disk space—200 MB available hard disk space</span></span>

## <span data-ttu-id="45498-268">Configuration requise pour le Sequencer</span><span class="sxs-lookup"><span data-stu-id="45498-268">Sequencer system requirements</span></span>

<span data-ttu-id="45498-269">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de Sequencer App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="45498-269">The following table lists the operating systems that are supported for the App-V 5.1 Sequencer installation.</span></span>

| <span data-ttu-id="45498-270">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="45498-270">Operating System</span></span>                 | <span data-ttu-id="45498-271">Service Pack</span><span class="sxs-lookup"><span data-stu-id="45498-271">Service Pack</span></span> | <span data-ttu-id="45498-272">Architecture système</span><span class="sxs-lookup"><span data-stu-id="45498-272">System Architecture</span></span> |
|----------------------------------|--------------|---------------------|
| <span data-ttu-id="45498-273">Microsoft Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="45498-273">Microsoft Windows Server 2019</span></span>    |              |        <span data-ttu-id="45498-274">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-274">64-bit</span></span>       |
| <span data-ttu-id="45498-275">Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="45498-275">Microsoft Windows Server 2016</span></span>    |              |        <span data-ttu-id="45498-276">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-276">64-bit</span></span>       |
| <span data-ttu-id="45498-277">Microsoft Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="45498-277">Microsoft Windows Server 2012 R2</span></span> |              |        <span data-ttu-id="45498-278">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-278">64-bit</span></span>       |
| <span data-ttu-id="45498-279">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45498-279">Microsoft Windows Server 2012</span></span>    |              |        <span data-ttu-id="45498-280">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-280">64-bit</span></span>       |
| <span data-ttu-id="45498-281">[Mise à jour de sécurité étendue](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="45498-281">Microsoft Windows Server 2008 R2 [Extended Security Update](https://www.microsoft.com/windows-server/extended-security-updates)</span></span> |      <span data-ttu-id="45498-282">SP1</span><span class="sxs-lookup"><span data-stu-id="45498-282">SP1</span></span>     |        <span data-ttu-id="45498-283">64 bits</span><span class="sxs-lookup"><span data-stu-id="45498-283">64-bit</span></span>       |
| <span data-ttu-id="45498-284">Microsoft Windows 10</span><span class="sxs-lookup"><span data-stu-id="45498-284">Microsoft Windows 10</span></span>             |              | <span data-ttu-id="45498-285">32bits et 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-285">32-bit and 64-bit</span></span>   |
| <span data-ttu-id="45498-286">Microsoft Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="45498-286">Microsoft Windows 8.1</span></span>            |              | <span data-ttu-id="45498-287">32bits et 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-287">32-bit and 64-bit</span></span>   |
| <span data-ttu-id="45498-288">Microsoft Windows 7</span><span class="sxs-lookup"><span data-stu-id="45498-288">Microsoft Windows 7</span></span>              |      <span data-ttu-id="45498-289">SP1</span><span class="sxs-lookup"><span data-stu-id="45498-289">SP1</span></span>     | <span data-ttu-id="45498-290">32bits et 64bits</span><span class="sxs-lookup"><span data-stu-id="45498-290">32-bit and 64-bit</span></span>   |

### <span data-ttu-id="45498-291">Configuration matérielle requise pour le Sequencer</span><span class="sxs-lookup"><span data-stu-id="45498-291">Sequencer hardware requirements</span></span>

<span data-ttu-id="45498-292">Pour connaître la configuration matérielle requise, voir la documentation de Windows ou Windows Server.</span><span class="sxs-lookup"><span data-stu-id="45498-292">See the Windows or Windows Server documentation for the hardware requirements.</span></span> <span data-ttu-id="45498-293">App-V n’ajoute aucune configuration matérielle supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="45498-293">App-V adds no additional hardware requirements.</span></span>

## <a href="" id="bkmk-supp-ver-sccm"></a><span data-ttu-id="45498-294">Versions prises en charge de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="45498-294">Supported versions of System Center Configuration Manager</span></span>

<span data-ttu-id="45498-295">Le client App-V prend en charge les versions suivantes de System Center Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="45498-295">The App-V client supports the following versions of System Center Configuration Manager:</span></span>

-   <span data-ttu-id="45498-296">MicrosoftSystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="45498-296">MicrosoftSystemCenter2012 ConfigurationManager</span></span>

-   <span data-ttu-id="45498-297">System Center2012R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="45498-297">System Center 2012 R2 Configuration Manager</span></span>

-   <span data-ttu-id="45498-298">System Center2012R2 ConfigurationManagerSP1</span><span class="sxs-lookup"><span data-stu-id="45498-298">System Center 2012 R2 Configuration Manager SP1</span></span>

<span data-ttu-id="45498-299">Les matrices de version de l’application-V et System Center Configuration Manager suivantes montrent toutes les combinaisons officiellement prises en charge par App-V et Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="45498-299">The following App-V and System Center Configuration Manager version matrix shows all officially supported combinations of App-V and Configuration Manager.</span></span>

> [!NOTE]
> <span data-ttu-id="45498-300">La prise en charge standard de l’application-V 4,5 et 4,6 a été fermée.</span><span class="sxs-lookup"><span data-stu-id="45498-300">Both App-V 4.5 and 4.6 have exited Mainstream support.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="45498-301">Version App-V</span><span class="sxs-lookup"><span data-stu-id="45498-301">App-V Version</span></span></th>
<th align="left"><span data-ttu-id="45498-302">System Center Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="45498-302">System Center Configuration Manager 2007</span></span></th>
<th align="left"><span data-ttu-id="45498-303">SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="45498-303">System Center 2012 Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="45498-304">SystemCenter2012 ConfigurationManagerSP1</span><span class="sxs-lookup"><span data-stu-id="45498-304">System Center 2012 Configuration Manager SP1</span></span></th>
<th align="left"><span data-ttu-id="45498-305">System Center2012R2 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="45498-305">System Center 2012 R2 Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="45498-306">System Center2012R2 ConfigurationManagerSP1</span><span class="sxs-lookup"><span data-stu-id="45498-306">System Center 2012 R2 Configuration Manager SP1</span></span></th>
<th align="left"><span data-ttu-id="45498-307">SystemCenter2012 ConfigurationManagerSP2</span><span class="sxs-lookup"><span data-stu-id="45498-307">System Center 2012 Configuration Manager SP2</span></span></th>
<th align="left"><span data-ttu-id="45498-308">System Center Configuration Manager version 1511</span><span class="sxs-lookup"><span data-stu-id="45498-308">System Center Configuration Manager Version 1511</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="45498-309">App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="45498-309">App-V 5.0 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-310">MSI-wrapper uniquement</span><span class="sxs-lookup"><span data-stu-id="45498-310">MSI-Wrapper Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-311">Non</span><span class="sxs-lookup"><span data-stu-id="45498-311">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-312">2012 SP1 CU4</span><span class="sxs-lookup"><span data-stu-id="45498-312">2012 SP1 CU4</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-313">2012 R2 CU1</span><span class="sxs-lookup"><span data-stu-id="45498-313">2012 R2 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-314">Oui</span><span class="sxs-lookup"><span data-stu-id="45498-314">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-315">Oui</span><span class="sxs-lookup"><span data-stu-id="45498-315">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-316">Oui</span><span class="sxs-lookup"><span data-stu-id="45498-316">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="45498-317">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="45498-317">App-V 5.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-318">MSI-wrapper uniquement</span><span class="sxs-lookup"><span data-stu-id="45498-318">MSI-Wrapper Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-319">Non</span><span class="sxs-lookup"><span data-stu-id="45498-319">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-320">2012 SP1 CU4</span><span class="sxs-lookup"><span data-stu-id="45498-320">2012 SP1 CU4</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-321">2012 R2 CU1</span><span class="sxs-lookup"><span data-stu-id="45498-321">2012 R2 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-322">Oui</span><span class="sxs-lookup"><span data-stu-id="45498-322">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-323">Oui</span><span class="sxs-lookup"><span data-stu-id="45498-323">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="45498-324">Oui</span><span class="sxs-lookup"><span data-stu-id="45498-324">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="45498-325">Pour plus d’informations sur l’intégration de Configuration Manager à l’application-V, voir [planification de l’intégration d’App-v à la Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span><span class="sxs-lookup"><span data-stu-id="45498-325">For more information about how Configuration Manager integrates with App-V, see [Planning for App-V Integration with Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).</span></span>

## <span data-ttu-id="45498-326">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45498-326">Related topics</span></span>

[<span data-ttu-id="45498-327">Envisager de déployer App-V</span><span class="sxs-lookup"><span data-stu-id="45498-327">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

[<span data-ttu-id="45498-328">Composants requis d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="45498-328">App-V 5.1 Prerequisites</span></span>](app-v-51-prerequisites.md)
