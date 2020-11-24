---
title: Configurations prises en charge par MBAM2.5
description: Configurations prises en charge par MBAM2.5
author: dansimp
ms.assetid: ce689aff-9a55-4ae7-a968-23c7bda9b4d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 10/24/2018
ms.openlocfilehash: 8ed7915e33c5e4735a7c58674ed5f7d6da8e9a06
ms.sourcegitcommit: 9087f0a1b5bd3f81a9b790d5e39fdf39c18a2411
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2020
ms.locfileid: "11182926"
---
# <span data-ttu-id="ae4a9-103">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ae4a9-103">MBAM 2.5 Supported Configurations</span></span>


<span data-ttu-id="ae4a9-104">Vous pouvez exécuter l’outil d’administration et de surveillance de BitLocker (MBAM) 2,5 dans une topologie autonome ou dans une topologie d’intégration de Configuration Manager intégrant MBAM avec System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-104">You can run Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in a Stand-alone topology or in a Configuration Manager Integration topology that integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="ae4a9-105">Si vous utilisez la configuration recommandée pour une topologie dans un environnement de production, MBAM prend en charge jusqu’à 500 000 MBAM clients.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-105">If you use the recommended configuration for either topology in a production environment, MBAM supports up to 500,000 MBAM clients.</span></span> <span data-ttu-id="ae4a9-106">Pour plus d’informations sur l’architecture et les fonctionnalités recommandées qui sont configurées sur chaque serveur pour chaque topologie, voir [architecture de haut niveau pour MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="ae4a9-106">For information about the recommended architecture and features that are configured on each server for each topology, see [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<span data-ttu-id="ae4a9-107">Pour les configurations supplémentaires qui sont spécifiques au topologie d’intégration de Configuration Manager, voir [versions de Configuration Manager prises en charge par MBAM](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="ae4a9-107">For additional configurations that are specific to the Configuration Manager Integration topology, see [Versions of Configuration Manager that MBAM supports](#bkmk-cm-ramreqs).</span></span>

**<span data-ttu-id="ae4a9-108">Remarque</span><span class="sxs-lookup"><span data-stu-id="ae4a9-108">Note</span></span>**  
<span data-ttu-id="ae4a9-109">Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="ae4a9-110">Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="ae4a9-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="ae4a9-111">Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="ae4a9-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



## <span data-ttu-id="ae4a9-112">Langues prises en charge par MBAM</span><span class="sxs-lookup"><span data-stu-id="ae4a9-112">MBAM Supported Languages</span></span>


<span data-ttu-id="ae4a9-113">Les tableaux suivants illustrent les langues prises en charge pour le client MBAM (y compris le portail de Self-Service) et le serveur MBAM dans MBAM 2,5 et MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-113">The following tables show the languages that are supported for the MBAM Client (including the Self-Service Portal) and the MBAM Server in MBAM 2.5 and MBAM 2.5 SP1.</span></span>

**<span data-ttu-id="ae4a9-114">Langues prises en charge dans MBAM 2,5 SP1:</span><span class="sxs-lookup"><span data-stu-id="ae4a9-114">Supported Languages in MBAM 2.5 SP1:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ae4a9-115">Langues client</span><span class="sxs-lookup"><span data-stu-id="ae4a9-115">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-116">Langues du serveur</span><span class="sxs-lookup"><span data-stu-id="ae4a9-116">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-117">Tchèque (République tchèque) CS-CZ</span><span class="sxs-lookup"><span data-stu-id="ae4a9-117">Czech (Czech Republic) cs-CZ</span></span></p>
<p><span data-ttu-id="ae4a9-118">Danois (Danemark) da-DK</span><span class="sxs-lookup"><span data-stu-id="ae4a9-118">Danish (Denmark) da-DK</span></span></p>
<p><span data-ttu-id="ae4a9-119">Néerlandais (Pays-Bas) NL-NL</span><span class="sxs-lookup"><span data-stu-id="ae4a9-119">Dutch (Netherlands) nl-NL</span></span></p>
<p><span data-ttu-id="ae4a9-120">Anglais (États-Unis) en-US</span><span class="sxs-lookup"><span data-stu-id="ae4a9-120">English (United States) en-US</span></span></p>
<p><span data-ttu-id="ae4a9-121">FI (Finlande)-FI</span><span class="sxs-lookup"><span data-stu-id="ae4a9-121">Finnish (Finland) fi-FI</span></span></p>
<p><span data-ttu-id="ae4a9-122">Français (France) fr-FR</span><span class="sxs-lookup"><span data-stu-id="ae4a9-122">French (France) fr-FR</span></span></p>
<p><span data-ttu-id="ae4a9-123">Allemand (Allemagne) de-DE</span><span class="sxs-lookup"><span data-stu-id="ae4a9-123">German (Germany) de-DE</span></span></p>
<p><span data-ttu-id="ae4a9-124">Grec (Grèce) El-GR</span><span class="sxs-lookup"><span data-stu-id="ae4a9-124">Greek (Greece) el-GR</span></span></p>
<p><span data-ttu-id="ae4a9-125">Hongrois (Hongrie) HU-HU</span><span class="sxs-lookup"><span data-stu-id="ae4a9-125">Hungarian (Hungary) hu-HU</span></span></p>
<p><span data-ttu-id="ae4a9-126">IT Italien (Italie)-IT</span><span class="sxs-lookup"><span data-stu-id="ae4a9-126">Italian (Italy) it-IT</span></span></p>
<p><span data-ttu-id="ae4a9-127">Japonais (Japon) ja-JP</span><span class="sxs-lookup"><span data-stu-id="ae4a9-127">Japanese (Japan) ja-JP</span></span></p>
<p><span data-ttu-id="ae4a9-128">Coréen (Corée) ko-KR</span><span class="sxs-lookup"><span data-stu-id="ae4a9-128">Korean (Korea) ko-KR</span></span></p>
<p><span data-ttu-id="ae4a9-129">Norvégien, Bokmål (Norvège) NB-non</span><span class="sxs-lookup"><span data-stu-id="ae4a9-129">Norwegian, Bokmål (Norway) nb-NO</span></span></p>
<p><span data-ttu-id="ae4a9-130">Polonais (Pologne) PL-PL</span><span class="sxs-lookup"><span data-stu-id="ae4a9-130">Polish (Poland) pl-PL</span></span></p>
<p><span data-ttu-id="ae4a9-131">Portugais (Brésil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="ae4a9-131">Portuguese (Brazil) pt-BR</span></span></p>
<p><span data-ttu-id="ae4a9-132">Portugais (Portugal) pt-PT</span><span class="sxs-lookup"><span data-stu-id="ae4a9-132">Portuguese (Portugal) pt-PT</span></span></p>
<p><span data-ttu-id="ae4a9-133">Russe (Russie) ru-RU</span><span class="sxs-lookup"><span data-stu-id="ae4a9-133">Russian (Russia) ru-RU</span></span></p>
<p><span data-ttu-id="ae4a9-134">Slovaque (Slovaquie) SK-SK</span><span class="sxs-lookup"><span data-stu-id="ae4a9-134">Slovak (Slovakia) sk-SK</span></span></p>
<p><span data-ttu-id="ae4a9-135">Espagnol (Espagne) es-ES</span><span class="sxs-lookup"><span data-stu-id="ae4a9-135">Spanish (Spain) es-ES</span></span></p>
<p><span data-ttu-id="ae4a9-136">Suédois (Suède) sv-SE</span><span class="sxs-lookup"><span data-stu-id="ae4a9-136">Swedish (Sweden) sv-SE</span></span></p>
<p><span data-ttu-id="ae4a9-137">Turc (Turquie) TR-TR</span><span class="sxs-lookup"><span data-stu-id="ae4a9-137">Turkish (Turkey) tr-TR</span></span></p>
<p><span data-ttu-id="ae4a9-138">Slovène (Slovénie) SL-SI</span><span class="sxs-lookup"><span data-stu-id="ae4a9-138">Slovenian (Slovenia) sl-SI</span></span></p>
<p><span data-ttu-id="ae4a9-139">Chinois simplifié (RPC) zh-NC</span><span class="sxs-lookup"><span data-stu-id="ae4a9-139">Simplified Chinese (PRC) zh-CN</span></span></p>
<p><span data-ttu-id="ae4a9-140">Chinois traditionnel (Taïwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="ae4a9-140">Traditional Chinese (Taiwan) zh-TW</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ae4a9-141">Anglais (États-Unis) en-US</span><span class="sxs-lookup"><span data-stu-id="ae4a9-141">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-142">Français (France) fr-FR</span><span class="sxs-lookup"><span data-stu-id="ae4a9-142">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-143">Allemand (Allemagne) de-DE</span><span class="sxs-lookup"><span data-stu-id="ae4a9-143">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-144">IT Italien (Italie)-IT</span><span class="sxs-lookup"><span data-stu-id="ae4a9-144">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-145">Japonais (Japon) ja-JP</span><span class="sxs-lookup"><span data-stu-id="ae4a9-145">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-146">Coréen (Corée) ko-KR</span><span class="sxs-lookup"><span data-stu-id="ae4a9-146">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-147">Portugais (Brésil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="ae4a9-147">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-148">Russe (Russie) ru-RU</span><span class="sxs-lookup"><span data-stu-id="ae4a9-148">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-149">Espagnol (Espagne) es-ES</span><span class="sxs-lookup"><span data-stu-id="ae4a9-149">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-150">Chinois simplifié (RPC) zh-NC</span><span class="sxs-lookup"><span data-stu-id="ae4a9-150">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-151">Chinois traditionnel (Taïwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="ae4a9-151">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ae4a9-152">Langues prises en charge dans MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="ae4a9-152">Supported Languages in MBAM 2.5:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ae4a9-153">Langues client</span><span class="sxs-lookup"><span data-stu-id="ae4a9-153">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-154">Langues du serveur</span><span class="sxs-lookup"><span data-stu-id="ae4a9-154">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="ae4a9-155">Anglais (États-Unis) en-US</span><span class="sxs-lookup"><span data-stu-id="ae4a9-155">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-156">Français (France) fr-FR</span><span class="sxs-lookup"><span data-stu-id="ae4a9-156">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-157">Allemand (Allemagne) de-DE</span><span class="sxs-lookup"><span data-stu-id="ae4a9-157">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-158">IT Italien (Italie)-IT</span><span class="sxs-lookup"><span data-stu-id="ae4a9-158">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-159">Japonais (Japon) ja-JP</span><span class="sxs-lookup"><span data-stu-id="ae4a9-159">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-160">Coréen (Corée) ko-KR</span><span class="sxs-lookup"><span data-stu-id="ae4a9-160">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-161">Portugais (Brésil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="ae4a9-161">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-162">Russe (Russie) ru-RU</span><span class="sxs-lookup"><span data-stu-id="ae4a9-162">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-163">Espagnol (Espagne) es-ES</span><span class="sxs-lookup"><span data-stu-id="ae4a9-163">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-164">Chinois simplifié (RPC) zh-NC</span><span class="sxs-lookup"><span data-stu-id="ae4a9-164">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-165">Chinois traditionnel (Taïwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="ae4a9-165">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ae4a9-166">Anglais (États-Unis) en-US</span><span class="sxs-lookup"><span data-stu-id="ae4a9-166">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-167">Français (France) fr-FR</span><span class="sxs-lookup"><span data-stu-id="ae4a9-167">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-168">Allemand (Allemagne) de-DE</span><span class="sxs-lookup"><span data-stu-id="ae4a9-168">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-169">IT Italien (Italie)-IT</span><span class="sxs-lookup"><span data-stu-id="ae4a9-169">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-170">Japonais (Japon) ja-JP</span><span class="sxs-lookup"><span data-stu-id="ae4a9-170">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-171">Coréen (Corée) ko-KR</span><span class="sxs-lookup"><span data-stu-id="ae4a9-171">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-172">Portugais (Brésil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="ae4a9-172">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-173">Russe (Russie) ru-RU</span><span class="sxs-lookup"><span data-stu-id="ae4a9-173">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-174">Espagnol (Espagne) es-ES</span><span class="sxs-lookup"><span data-stu-id="ae4a9-174">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-175">Chinois simplifié (RPC) zh-NC</span><span class="sxs-lookup"><span data-stu-id="ae4a9-175">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="ae4a9-176">Chinois traditionnel (Taïwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="ae4a9-176">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="ae4a9-177">Configuration système requise pour MBAM Server</span><span class="sxs-lookup"><span data-stu-id="ae4a9-177">MBAM Server system requirements</span></span>


### <span data-ttu-id="ae4a9-178">Configuration requise pour le système d’exploitation MBAM</span><span class="sxs-lookup"><span data-stu-id="ae4a9-178">MBAM Server operating system requirements</span></span>

<span data-ttu-id="ae4a9-179">Nous vous recommandons vivement d’exécuter le client MBAM et MBAM Server sur la même ligne de systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-179">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="ae4a9-180">Par exemple, Windows 10 avec Windows Server 2016, Windows 8,1 avec Windows Server 2012 R2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-180">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="ae4a9-181">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-181">The following table lists the operating systems that are supported for the MBAM Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ae4a9-182">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ae4a9-182">Operating system</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-183">Édition</span><span class="sxs-lookup"><span data-stu-id="ae4a9-183">Edition</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-184">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ae4a9-184">Service pack</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-185">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ae4a9-185">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-186">Windows Server2019</span><span class="sxs-lookup"><span data-stu-id="ae4a9-186">Windows Server 2019</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-187">Standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ae4a9-187">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="ae4a9-188">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-188">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-189">Windows Server2016</span><span class="sxs-lookup"><span data-stu-id="ae4a9-189">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-190">Standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ae4a9-190">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="ae4a9-191">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-191">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-192">WindowsServer2012R2</span><span class="sxs-lookup"><span data-stu-id="ae4a9-192">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-193">Standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ae4a9-193">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-194">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-194">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-195">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="ae4a9-195">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-196">Standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ae4a9-196">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="ae4a9-197">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-197">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-198">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="ae4a9-198">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-199">Standard, entreprise ou centre de</span><span class="sxs-lookup"><span data-stu-id="ae4a9-199">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-200">SP1</span><span class="sxs-lookup"><span data-stu-id="ae4a9-200">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-201">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-201">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="ae4a9-202">Le domaine d’entreprise doit contenir au moins un contrôleur de domaine Windows Server 2008 (ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="ae4a9-202">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span>

### <a href="" id="bkmk-stand-alone-ramreqs"></a><span data-ttu-id="ae4a9-203">Configuration requise pour le processeur du serveur MBAM, la RAM et l’espace disque-topologie autonome</span><span class="sxs-lookup"><span data-stu-id="ae4a9-203">MBAM Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="ae4a9-204">Ces exigences concernent la topologie autonome MBAM.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-204">These requirements are for the MBAM Stand-alone topology.</span></span> <span data-ttu-id="ae4a9-205">Pour connaître la configuration requise pour la topologie d’intégration de Configuration Manager, voir Configuration requise pour le [processeur du serveur MBAM, la RAM et l’espace disque-topologie d’intégration de Configuration Manager](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="ae4a9-205">For the requirements for the Configuration Manager Integration topology, see [MBAM Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ae4a9-206">Élément matériel</span><span class="sxs-lookup"><span data-stu-id="ae4a9-206">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-207">Configuration minimale</span><span class="sxs-lookup"><span data-stu-id="ae4a9-207">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-208">Configuration recommandée</span><span class="sxs-lookup"><span data-stu-id="ae4a9-208">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-209">Processeur</span><span class="sxs-lookup"><span data-stu-id="ae4a9-209">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-210">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="ae4a9-210">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-211">2,33 GHz ou supérieur</span><span class="sxs-lookup"><span data-stu-id="ae4a9-211">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-212">Mémoire vive (RAM)</span><span class="sxs-lookup"><span data-stu-id="ae4a9-212">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-213">8 GO</span><span class="sxs-lookup"><span data-stu-id="ae4a9-213">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-214">12 GO</span><span class="sxs-lookup"><span data-stu-id="ae4a9-214">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-215">Espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="ae4a9-215">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-216">1 Go</span><span class="sxs-lookup"><span data-stu-id="ae4a9-216">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-217">2 Go</span><span class="sxs-lookup"><span data-stu-id="ae4a9-217">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a><span data-ttu-id="ae4a9-218">Configurations requises pour le processeur du serveur MBAM, la RAM et l’espace disque-topologie d’intégration de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ae4a9-218">MBAM Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="ae4a9-219">Le tableau suivant répertorie les conditions requises processeur de serveur, RAM et espace disque pour les serveurs MBAM lorsque vous utilisez la topologie d’intégration de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-219">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span> <span data-ttu-id="ae4a9-220">Pour connaître la configuration requise pour la topologie autonome, voir [Configuration requise pour le processeur MBAM, la RAM et l’espace disque-topologie autonome](#bkmk-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="ae4a9-220">For the requirements for the Stand-alone topology, see [MBAM Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ae4a9-221">Élément matériel</span><span class="sxs-lookup"><span data-stu-id="ae4a9-221">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-222">Configuration minimale</span><span class="sxs-lookup"><span data-stu-id="ae4a9-222">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-223">Configuration recommandée</span><span class="sxs-lookup"><span data-stu-id="ae4a9-223">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-224">Processeur</span><span class="sxs-lookup"><span data-stu-id="ae4a9-224">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-225">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="ae4a9-225">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-226">2,33 GHz ou supérieur</span><span class="sxs-lookup"><span data-stu-id="ae4a9-226">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-227">Mémoire vive (RAM)</span><span class="sxs-lookup"><span data-stu-id="ae4a9-227">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-228">4 Go</span><span class="sxs-lookup"><span data-stu-id="ae4a9-228">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-229">8 GO</span><span class="sxs-lookup"><span data-stu-id="ae4a9-229">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-230">Espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="ae4a9-230">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-231">1 Go</span><span class="sxs-lookup"><span data-stu-id="ae4a9-231">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-232">2 Go</span><span class="sxs-lookup"><span data-stu-id="ae4a9-232">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a><span data-ttu-id="ae4a9-233">Versions du gestionnaire de configurations prises en charge par MBAM</span><span class="sxs-lookup"><span data-stu-id="ae4a9-233">Versions of Configuration Manager that MBAM supports</span></span>

<span data-ttu-id="ae4a9-234">MBAM prend en charge les versions suivantes de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-234">MBAM supports the following versions of Configuration Manager.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ae4a9-235">Version prise en charge</span><span class="sxs-lookup"><span data-stu-id="ae4a9-235">Supported version</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-236">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ae4a9-236">Service pack</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-237">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ae4a9-237">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-238">Microsoft System Center Configuration Manager (branche actuelle), versions allant jusqu’à 1902</span><span class="sxs-lookup"><span data-stu-id="ae4a9-238">Microsoft System Center Configuration Manager (Current Branch), versions up to 1902</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-239">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-239">64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-240">Microsoft System Center Configuration Manager 1806</span><span class="sxs-lookup"><span data-stu-id="ae4a9-240">Microsoft System Center Configuration Manager 1806</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-241">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-241">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-242">Microsoft System Center Configuration Manager (LTSB-version 1606)</span><span class="sxs-lookup"><span data-stu-id="ae4a9-242">Microsoft System Center Configuration Manager (LTSB - version 1606)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-243">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-243">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-244">Gestionnaire de configuration de Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="ae4a9-244">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-245">SP1</span><span class="sxs-lookup"><span data-stu-id="ae4a9-245">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-246">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-246">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-247">Microsoft System Center Configuration Manager 2007 R2 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ae4a9-247">Microsoft System Center Configuration Manager 2007 R2 or later</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-248">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-248">64-bit</span></span></p>

<span data-ttu-id="ae4a9-249">&gt;<strong>Remarque </strong> bien que Configuration Manager 2007 R2 soit 32 bits, vous devez l’installer et SQL Server sur un système d’exploitation 64 bits afin de correspondre au logiciel MBAM 64.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-249">&gt;<strong>Note</strong> Although Configuration Manager 2007 R2 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span>
</td>
</tr>
</tbody>
</table>



<span data-ttu-id="ae4a9-250">Pour obtenir la liste des configurations prises en charge pour le serveur Configuration Manager, consultez la documentation TechNet appropriée pour la version de Configuration Manager que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-250">For a list of supported configurations for the Configuration Manager Server, see the appropriate TechNet documentation for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="ae4a9-251">MBAM ne possède aucune configuration système supplémentaire pour le serveur Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-251">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="ae4a9-252">Configuration requise pour la base de données SQL Server</span><span class="sxs-lookup"><span data-stu-id="ae4a9-252">SQL Server database requirements</span></span>

<span data-ttu-id="ae4a9-253">Le tableau suivant répertorie les versions de Microsoft SQL Server prises en charge pour les fonctionnalités du serveur MBAM, notamment la base de données de récupération, la base de données d’audit et de conformité, et la fonctionnalité rapports.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-253">The following table lists the Microsoft SQL Server versions that are supported for the MBAM Server features, which include the Recovery Database, Compliance and Audit Database, and the Reports feature.</span></span> <span data-ttu-id="ae4a9-254">Les versions requises s’appliquent aux topologies d’intégration autonomes et de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-254">The required versions apply to the Stand-alone or the Configuration Manager Integration topologies.</span></span>

<span data-ttu-id="ae4a9-255">Vous devez installer SQL Server à l’aide du **SQL \ _Latin1 \ _General \ _CP1 \ _CI \ _AS** collation.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-255">You must install SQL Server with the **SQL\_Latin1\_General\_CP1\_CI\_AS** collation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ae4a9-256">Version de SQL Server</span><span class="sxs-lookup"><span data-stu-id="ae4a9-256">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-257">Édition</span><span class="sxs-lookup"><span data-stu-id="ae4a9-257">Edition</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-258">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ae4a9-258">Service pack</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-259">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ae4a9-259">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-260">Microsoft SQL Server 2019</span><span class="sxs-lookup"><span data-stu-id="ae4a9-260">Microsoft SQL Server 2019</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-261">Standard, entreprise ou centre de</span><span class="sxs-lookup"><span data-stu-id="ae4a9-261">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-262">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-262">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-263">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="ae4a9-263">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-264">Standard, entreprise ou centre de</span><span class="sxs-lookup"><span data-stu-id="ae4a9-264">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-265">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-265">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-266">MicrosoftSQLServer2016</span><span class="sxs-lookup"><span data-stu-id="ae4a9-266">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-267">Standard, entreprise ou centre de</span><span class="sxs-lookup"><span data-stu-id="ae4a9-267">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-268">SP1</span><span class="sxs-lookup"><span data-stu-id="ae4a9-268">SP1</span></span></p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p><span data-ttu-id="ae4a9-269">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-269">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-270">MicrosoftSQLServer2014</span><span class="sxs-lookup"><span data-stu-id="ae4a9-270">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-271">Standard, entreprise ou centre de</span><span class="sxs-lookup"><span data-stu-id="ae4a9-271">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-272">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="ae4a9-272">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-273">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-273">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-274">MicrosoftSQLServer 2012</span><span class="sxs-lookup"><span data-stu-id="ae4a9-274">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-275">Standard, entreprise ou centre de</span><span class="sxs-lookup"><span data-stu-id="ae4a9-275">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-276">3</span><span class="sxs-lookup"><span data-stu-id="ae4a9-276">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-277">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-277">64-bit</span></span></p></td>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-278">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ae4a9-278">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-279">Standard ou Entreprise</span><span class="sxs-lookup"><span data-stu-id="ae4a9-279">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-280">3</span><span class="sxs-lookup"><span data-stu-id="ae4a9-280">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-281">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-281">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

**<span data-ttu-id="ae4a9-282">Remarque</span><span class="sxs-lookup"><span data-stu-id="ae4a9-282">Note</span></span>**  
<span data-ttu-id="ae4a9-283">MBAM possède un niveau de compatibilité maximal pris en charge de 140.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-283">MBAM has a maximum supported compatibility level of 140.</span></span> <span data-ttu-id="ae4a9-284">Le niveau de compatibilité par défaut pour les nouvelles bases de données créées sur SQL Server 2019 est 150 dont la modification doit être apportée à 140 ou une version antérieure, à l’aide de la commande modifier la base de données, après la création de la base de données.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-284">The default compatibility level for new databases created on SQL Server 2019 is 150 which will need to be altered to 140 or lower, using the ALTER DATABASE command, after the database has been created.</span></span> <span data-ttu-id="ae4a9-285">Les bases de données existantes migrées à partir de SQL Server 2017 ou d’une version antérieure seront maintenues à leur niveau de compatibilité précédent et ne doivent pas être altérées.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-285">Existing databases migrated from SQL server 2017 or below will remain at their previous compatibility level and do not need to be altered.</span></span>

<span data-ttu-id="ae4a9-286">Pour prendre en charge SQL 2016, vous devez installer le version de service de mars 2017 pour MDOP https://www.microsoft.com/download/details.aspx?id=54967  et prendre en charge sql 2017 vous devez installer la version de maintenance de juillet 2018 pour MDOP https://www.microsoft.com/download/details.aspx?id=57157 .</span><span class="sxs-lookup"><span data-stu-id="ae4a9-286">In order to support SQL 2016 you must install the March 2017 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=54967  and to support SQL 2017 you must install the July 2018 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=57157.</span></span> <span data-ttu-id="ae4a9-287">En règle générale, restez en mesure d’utiliser la mise à jour de maintenance la plus récente, car elle inclut également toutes les ainsi correctifs et nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-287">In general stay current by always using the most recent servicing update as it also includes all bugfixes and new features.</span></span>


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a><span data-ttu-id="ae4a9-288">Configuration requise pour le processeur SQL Server, la RAM et l’espace disque-topologie autonome</span><span class="sxs-lookup"><span data-stu-id="ae4a9-288">SQL Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="ae4a9-289">Le tableau suivant répertorie les exigences relatives au processeur, à la RAM et à l’espace disque recommandés pour l’ordinateur SQL Server lors de l’utilisation de la topologie autonome.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-289">The following table lists the recommended server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Stand-alone topology.</span></span> <span data-ttu-id="ae4a9-290">Utilisez ces exigences comme guide.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-290">Use these requirements as a guide.</span></span> <span data-ttu-id="ae4a9-291">Vos exigences spécifiques varient en fonction du nombre d’ordinateurs clients que vous prenez en charge au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-291">Your specific requirements will vary based on the number of client computers you are supporting in your enterprise.</span></span> <span data-ttu-id="ae4a9-292">Pour consulter la configuration requise pour la topologie d’intégration de Configuration Manager, voir Configuration requise pour le [processeur SQL Server, la RAM et l’espace disque-topologie d’intégration de Configuration Manager](#bkmk-cm-sql-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="ae4a9-292">To view the requirements for the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-sql-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ae4a9-293">Élément matériel</span><span class="sxs-lookup"><span data-stu-id="ae4a9-293">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-294">Configuration minimale</span><span class="sxs-lookup"><span data-stu-id="ae4a9-294">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-295">Configuration recommandée</span><span class="sxs-lookup"><span data-stu-id="ae4a9-295">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-296">Processeur</span><span class="sxs-lookup"><span data-stu-id="ae4a9-296">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-297">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="ae4a9-297">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-298">2,33 GHz ou supérieur</span><span class="sxs-lookup"><span data-stu-id="ae4a9-298">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-299">Mémoire vive (RAM)</span><span class="sxs-lookup"><span data-stu-id="ae4a9-299">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-300">8 GO</span><span class="sxs-lookup"><span data-stu-id="ae4a9-300">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-301">12 GO</span><span class="sxs-lookup"><span data-stu-id="ae4a9-301">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-302">Espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="ae4a9-302">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-303">5 GO</span><span class="sxs-lookup"><span data-stu-id="ae4a9-303">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-304">5 Go minimum</span><span class="sxs-lookup"><span data-stu-id="ae4a9-304">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a><span data-ttu-id="ae4a9-305">Configuration requise pour le processeur SQL Server, la RAM et l’espace disque-topologie d’intégration de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ae4a9-305">SQL Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="ae4a9-306">Le tableau suivant répertorie les exigences relatives au processeur, à la RAM et à l’espace disque pour l’ordinateur Microsoft SQL Server lors de l’utilisation de la topologie d’intégration de Configuration Manager, voir [topologie autonome du processeur SQL Server, de la RAM et de l’espace disque](#bkmk-sql-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="ae4a9-306">The following table lists the server processor, RAM, and disk space requirements for the Microsoft SQL Server computer when you are using the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-sql-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ae4a9-307">Élément matériel</span><span class="sxs-lookup"><span data-stu-id="ae4a9-307">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-308">Configuration minimale</span><span class="sxs-lookup"><span data-stu-id="ae4a9-308">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-309">Configuration recommandée</span><span class="sxs-lookup"><span data-stu-id="ae4a9-309">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-310">Processeur</span><span class="sxs-lookup"><span data-stu-id="ae4a9-310">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-311">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="ae4a9-311">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-312">2,33 GHz ou supérieur</span><span class="sxs-lookup"><span data-stu-id="ae4a9-312">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-313">Mémoire vive (RAM)</span><span class="sxs-lookup"><span data-stu-id="ae4a9-313">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-314">4 Go</span><span class="sxs-lookup"><span data-stu-id="ae4a9-314">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-315">8 GO</span><span class="sxs-lookup"><span data-stu-id="ae4a9-315">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-316">Espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="ae4a9-316">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-317">5 GO</span><span class="sxs-lookup"><span data-stu-id="ae4a9-317">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-318">5 GO</span><span class="sxs-lookup"><span data-stu-id="ae4a9-318">5 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="ae4a9-319">Configuration système requise pour le client MBAM</span><span class="sxs-lookup"><span data-stu-id="ae4a9-319">MBAM Client system requirements</span></span>


### <span data-ttu-id="ae4a9-320">Configuration requise du système d’exploitation client</span><span class="sxs-lookup"><span data-stu-id="ae4a9-320">Client operating system requirements</span></span>

<span data-ttu-id="ae4a9-321">Nous vous recommandons vivement d’exécuter le client MBAM et MBAM Server sur la même ligne de systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-321">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="ae4a9-322">Par exemple, Windows 10 avec Windows Server 2016, Windows 8,1 avec Windows Server 2012 R2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-322">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="ae4a9-323">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-323">The following table lists the operating systems that are supported for MBAM Client installation.</span></span> <span data-ttu-id="ae4a9-324">Les mêmes exigences s’appliquent aux topologies d’intégration autonome et Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-324">The same requirements apply to the Stand-alone and the Configuration Manager Integration topologies.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ae4a9-325">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ae4a9-325">Operating system</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-326">Édition</span><span class="sxs-lookup"><span data-stu-id="ae4a9-326">Edition</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-327">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ae4a9-327">Service pack</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-328">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ae4a9-328">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
    <td align="left"><p><span data-ttu-id="ae4a9-329">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="ae4a9-329">Windows 10 IoT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ae4a9-330">Enterprise</span><span class="sxs-lookup"><span data-stu-id="ae4a9-330">Enterprise</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p><span data-ttu-id="ae4a9-331">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-331">32-bit or 64-bit</span></span></p></td>
</tr><br/><tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-332">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ae4a9-332">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-333">Enterprise</span><span class="sxs-lookup"><span data-stu-id="ae4a9-333">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-334">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-334">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-335">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ae4a9-335">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-336">Enterprise</span><span class="sxs-lookup"><span data-stu-id="ae4a9-336">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-337">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-337">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-338">Windows7</span><span class="sxs-lookup"><span data-stu-id="ae4a9-338">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-339">Entreprise ou intégrale</span><span class="sxs-lookup"><span data-stu-id="ae4a9-339">Enterprise or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-340">SP1</span><span class="sxs-lookup"><span data-stu-id="ae4a9-340">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-341">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-341">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-342">WindowsToGo</span><span class="sxs-lookup"><span data-stu-id="ae4a9-342">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-343">Windows 8,1 et Windows 10 entreprise</span><span class="sxs-lookup"><span data-stu-id="ae4a9-343">Windows 8.1 and Windows 10 Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-344">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-344">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="ae4a9-345">Configuration requise pour le client RAM</span><span class="sxs-lookup"><span data-stu-id="ae4a9-345">Client RAM requirements</span></span>

<span data-ttu-id="ae4a9-346">Il n’existe aucune exigence de RAM spécifique à l’installation du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-346">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="ae4a9-347">Configuration système requise pour la stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="ae4a9-347">MBAM Group Policy system requirements</span></span>


<span data-ttu-id="ae4a9-348">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de modèles de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-348">The following table lists the operating systems that are supported for MBAM Group Policy Templates installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ae4a9-349">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ae4a9-349">Operating system</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-350">Édition</span><span class="sxs-lookup"><span data-stu-id="ae4a9-350">Edition</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-351">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ae4a9-351">Service pack</span></span></th>
<th align="left"><span data-ttu-id="ae4a9-352">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ae4a9-352">System architecture</span></span></th>
</tr>
</thead>
<tbody>
 <tr class="even">
      <td align="left"><p><span data-ttu-id="ae4a9-353">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="ae4a9-353">Windows 10 IoT</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ae4a9-354">Enterprise</span><span class="sxs-lookup"><span data-stu-id="ae4a9-354">Enterprise</span></span></p></td>
      <td align="left"><p></p></td>
      <td align="left"><p><span data-ttu-id="ae4a9-355">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-355">32-bit or 64-bit</span></span></p></td>
 </tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-356">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ae4a9-356">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-357">Enterprise</span><span class="sxs-lookup"><span data-stu-id="ae4a9-357">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-358">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-358">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-359">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ae4a9-359">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-360">Enterprise</span><span class="sxs-lookup"><span data-stu-id="ae4a9-360">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-361">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-361">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-362">Windows7</span><span class="sxs-lookup"><span data-stu-id="ae4a9-362">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-363">Entreprise ou intégrale</span><span class="sxs-lookup"><span data-stu-id="ae4a9-363">Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-364">SP1</span><span class="sxs-lookup"><span data-stu-id="ae4a9-364">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-365">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-365">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-366">WindowsServer2012R2</span><span class="sxs-lookup"><span data-stu-id="ae4a9-366">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-367">Standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ae4a9-367">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-368">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-368">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ae4a9-369">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="ae4a9-369">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-370">Standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ae4a9-370">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-371">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-371">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ae4a9-372">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="ae4a9-372">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-373">Standard, entreprise ou centre de</span><span class="sxs-lookup"><span data-stu-id="ae4a9-373">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-374">SP1</span><span class="sxs-lookup"><span data-stu-id="ae4a9-374">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ae4a9-375">64 bits</span><span class="sxs-lookup"><span data-stu-id="ae4a9-375">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="ae4a9-376">MBAM dans Azure IaaS</span><span class="sxs-lookup"><span data-stu-id="ae4a9-376">MBAM In Azure IaaS</span></span>

<span data-ttu-id="ae4a9-377">Le serveur MBAM peut être déployé dans Azure infrastructure en tant que service (IaaS) sur les versions de système d’exploitation prises en charge répertoriées ci-dessus, qui se connectent à un annuaire actif hébergé sur un site ou un Active Directory également hébergé dans Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-377">The MBAM server can be deployed in Azure Infrastructure as a Service (IaaS) on any of the supported OS versions listed above, connecting to an Active Directory hosted on premises or an Active Directory also hosted in Azure IaaS.</span></span>  <span data-ttu-id="ae4a9-378">La documentation relative à la configuration et à la configuration d’Active Directory sur Azure IaaS est disponible [ici](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span><span class="sxs-lookup"><span data-stu-id="ae4a9-378">Documentation for setting up and configuring Active Directory on Azure IaaS is [here](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span></span>

<span data-ttu-id="ae4a9-379">Le client MBAM n’est pas pris en charge sur les machines virtuelles et n’est pas non plus pris en charge sur Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="ae4a9-379">The MBAM client is not supported on virtual machines and is also not supported on Azure IaaS.</span></span>


## <span data-ttu-id="ae4a9-380">Service Releases</span><span class="sxs-lookup"><span data-stu-id="ae4a9-380">Service releases</span></span> 

- [<span data-ttu-id="ae4a9-381">Correctif 2016 d’avril</span><span class="sxs-lookup"><span data-stu-id="ae4a9-381">April 2016 hotfix</span></span>](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="ae4a9-382">2016 septembre</span><span class="sxs-lookup"><span data-stu-id="ae4a9-382">September 2016</span></span>](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [<span data-ttu-id="ae4a9-383">Décembre2016</span><span class="sxs-lookup"><span data-stu-id="ae4a9-383">December 2016</span></span>](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [<span data-ttu-id="ae4a9-384">Mars2017</span><span class="sxs-lookup"><span data-stu-id="ae4a9-384">March 2017</span></span>](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [<span data-ttu-id="ae4a9-385">Juin2017</span><span class="sxs-lookup"><span data-stu-id="ae4a9-385">June 2017</span></span>](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="ae4a9-386">Septembre2017</span><span class="sxs-lookup"><span data-stu-id="ae4a9-386">September 2017</span></span>](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [<span data-ttu-id="ae4a9-387">Mars2018</span><span class="sxs-lookup"><span data-stu-id="ae4a9-387">March 2018</span></span>](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="ae4a9-388">2018 juillet</span><span class="sxs-lookup"><span data-stu-id="ae4a9-388">July 2018</span></span>](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="ae4a9-389">2019</span><span class="sxs-lookup"><span data-stu-id="ae4a9-389">May 2019</span></span>](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## <span data-ttu-id="ae4a9-390">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ae4a9-390">Related topics</span></span>


[<span data-ttu-id="ae4a9-391">Planification du déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ae4a9-391">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="ae4a9-392">Préparation de votre environnement pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ae4a9-392">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)




## <span data-ttu-id="ae4a9-393">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="ae4a9-393">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ae4a9-394">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="ae4a9-394">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ae4a9-395">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ae4a9-395">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




