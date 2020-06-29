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
ms.openlocfilehash: 262cd8c259dc37b291cdaf02caf0e20b7515d38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810229"
---
# <span data-ttu-id="ef925-103">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ef925-103">MBAM 2.5 Supported Configurations</span></span>


<span data-ttu-id="ef925-104">Vous pouvez exécuter l’outil d’administration et de surveillance de BitLocker (MBAM) 2,5 dans une topologie autonome ou dans une topologie d’intégration de Configuration Manager intégrant MBAM avec System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ef925-104">You can run Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in a Stand-alone topology or in a Configuration Manager Integration topology that integrates MBAM with System Center Configuration Manager.</span></span> <span data-ttu-id="ef925-105">Si vous utilisez la configuration recommandée pour une topologie dans un environnement de production, MBAM prend en charge jusqu’à 500 000 MBAM clients.</span><span class="sxs-lookup"><span data-stu-id="ef925-105">If you use the recommended configuration for either topology in a production environment, MBAM supports up to 500,000 MBAM clients.</span></span> <span data-ttu-id="ef925-106">Pour plus d’informations sur l’architecture et les fonctionnalités recommandées qui sont configurées sur chaque serveur pour chaque topologie, voir [architecture de haut niveau pour MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="ef925-106">For information about the recommended architecture and features that are configured on each server for each topology, see [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

<span data-ttu-id="ef925-107">Pour les configurations supplémentaires qui sont spécifiques au topologie d’intégration de Configuration Manager, voir [versions de Configuration Manager prises en charge par MBAM](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="ef925-107">For additional configurations that are specific to the Configuration Manager Integration topology, see [Versions of Configuration Manager that MBAM supports](#bkmk-cm-ramreqs).</span></span>

**<span data-ttu-id="ef925-108">Remarque</span><span class="sxs-lookup"><span data-stu-id="ef925-108">Note</span></span>**  
<span data-ttu-id="ef925-109">Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent.</span><span class="sxs-lookup"><span data-stu-id="ef925-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="ef925-110">Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="ef925-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="ef925-111">Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="ef925-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



## <span data-ttu-id="ef925-112">Langues prises en charge par MBAM</span><span class="sxs-lookup"><span data-stu-id="ef925-112">MBAM Supported Languages</span></span>


<span data-ttu-id="ef925-113">Les tableaux suivants illustrent les langues prises en charge pour le client MBAM (y compris le portail libre-service) et le serveur MBAM dans MBAM 2,5 et MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="ef925-113">The following tables show the languages that are supported for the MBAM Client (including the Self-Service Portal) and the MBAM Server in MBAM 2.5 and MBAM 2.5 SP1.</span></span>

**<span data-ttu-id="ef925-114">Langues prises en charge dans MBAM 2,5 SP1:</span><span class="sxs-lookup"><span data-stu-id="ef925-114">Supported Languages in MBAM 2.5 SP1:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef925-115">Langues client</span><span class="sxs-lookup"><span data-stu-id="ef925-115">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="ef925-116">Langues du serveur</span><span class="sxs-lookup"><span data-stu-id="ef925-116">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-117">Tchèque (République tchèque) CS-CZ</span><span class="sxs-lookup"><span data-stu-id="ef925-117">Czech (Czech Republic) cs-CZ</span></span></p>
<p><span data-ttu-id="ef925-118">Danois (Danemark) da-DK</span><span class="sxs-lookup"><span data-stu-id="ef925-118">Danish (Denmark) da-DK</span></span></p>
<p><span data-ttu-id="ef925-119">Néerlandais (Pays-Bas) NL-NL</span><span class="sxs-lookup"><span data-stu-id="ef925-119">Dutch (Netherlands) nl-NL</span></span></p>
<p><span data-ttu-id="ef925-120">Anglais (États-Unis) en-US</span><span class="sxs-lookup"><span data-stu-id="ef925-120">English (United States) en-US</span></span></p>
<p><span data-ttu-id="ef925-121">FI (Finlande)-FI</span><span class="sxs-lookup"><span data-stu-id="ef925-121">Finnish (Finland) fi-FI</span></span></p>
<p><span data-ttu-id="ef925-122">Français (France) fr-FR</span><span class="sxs-lookup"><span data-stu-id="ef925-122">French (France) fr-FR</span></span></p>
<p><span data-ttu-id="ef925-123">Allemand (Allemagne) de-DE</span><span class="sxs-lookup"><span data-stu-id="ef925-123">German (Germany) de-DE</span></span></p>
<p><span data-ttu-id="ef925-124">Grec (Grèce) El-GR</span><span class="sxs-lookup"><span data-stu-id="ef925-124">Greek (Greece) el-GR</span></span></p>
<p><span data-ttu-id="ef925-125">Hongrois (Hongrie) HU-HU</span><span class="sxs-lookup"><span data-stu-id="ef925-125">Hungarian (Hungary) hu-HU</span></span></p>
<p><span data-ttu-id="ef925-126">IT Italien (Italie)-IT</span><span class="sxs-lookup"><span data-stu-id="ef925-126">Italian (Italy) it-IT</span></span></p>
<p><span data-ttu-id="ef925-127">Japonais (Japon) ja-JP</span><span class="sxs-lookup"><span data-stu-id="ef925-127">Japanese (Japan) ja-JP</span></span></p>
<p><span data-ttu-id="ef925-128">Coréen (Corée) ko-KR</span><span class="sxs-lookup"><span data-stu-id="ef925-128">Korean (Korea) ko-KR</span></span></p>
<p><span data-ttu-id="ef925-129">Norvégien, Bokmål (Norvège) NB-non</span><span class="sxs-lookup"><span data-stu-id="ef925-129">Norwegian, Bokmål (Norway) nb-NO</span></span></p>
<p><span data-ttu-id="ef925-130">Polonais (Pologne) PL-PL</span><span class="sxs-lookup"><span data-stu-id="ef925-130">Polish (Poland) pl-PL</span></span></p>
<p><span data-ttu-id="ef925-131">Portugais (Brésil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="ef925-131">Portuguese (Brazil) pt-BR</span></span></p>
<p><span data-ttu-id="ef925-132">Portugais (Portugal) pt-PT</span><span class="sxs-lookup"><span data-stu-id="ef925-132">Portuguese (Portugal) pt-PT</span></span></p>
<p><span data-ttu-id="ef925-133">Russe (Russie) ru-RU</span><span class="sxs-lookup"><span data-stu-id="ef925-133">Russian (Russia) ru-RU</span></span></p>
<p><span data-ttu-id="ef925-134">Slovaque (Slovaquie) SK-SK</span><span class="sxs-lookup"><span data-stu-id="ef925-134">Slovak (Slovakia) sk-SK</span></span></p>
<p><span data-ttu-id="ef925-135">Espagnol (Espagne) es-ES</span><span class="sxs-lookup"><span data-stu-id="ef925-135">Spanish (Spain) es-ES</span></span></p>
<p><span data-ttu-id="ef925-136">Suédois (Suède) sv-SE</span><span class="sxs-lookup"><span data-stu-id="ef925-136">Swedish (Sweden) sv-SE</span></span></p>
<p><span data-ttu-id="ef925-137">Turc (Turquie) TR-TR</span><span class="sxs-lookup"><span data-stu-id="ef925-137">Turkish (Turkey) tr-TR</span></span></p>
<p><span data-ttu-id="ef925-138">Slovène (Slovénie) SL-SI</span><span class="sxs-lookup"><span data-stu-id="ef925-138">Slovenian (Slovenia) sl-SI</span></span></p>
<p><span data-ttu-id="ef925-139">Chinois simplifié (RPC) zh-NC</span><span class="sxs-lookup"><span data-stu-id="ef925-139">Simplified Chinese (PRC) zh-CN</span></span></p>
<p><span data-ttu-id="ef925-140">Chinois traditionnel (Taïwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="ef925-140">Traditional Chinese (Taiwan) zh-TW</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ef925-141">Anglais (États-Unis) en-US</span><span class="sxs-lookup"><span data-stu-id="ef925-141">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="ef925-142">Français (France) fr-FR</span><span class="sxs-lookup"><span data-stu-id="ef925-142">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="ef925-143">Allemand (Allemagne) de-DE</span><span class="sxs-lookup"><span data-stu-id="ef925-143">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="ef925-144">IT Italien (Italie)-IT</span><span class="sxs-lookup"><span data-stu-id="ef925-144">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="ef925-145">Japonais (Japon) ja-JP</span><span class="sxs-lookup"><span data-stu-id="ef925-145">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="ef925-146">Coréen (Corée) ko-KR</span><span class="sxs-lookup"><span data-stu-id="ef925-146">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="ef925-147">Portugais (Brésil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="ef925-147">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="ef925-148">Russe (Russie) ru-RU</span><span class="sxs-lookup"><span data-stu-id="ef925-148">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="ef925-149">Espagnol (Espagne) es-ES</span><span class="sxs-lookup"><span data-stu-id="ef925-149">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="ef925-150">Chinois simplifié (RPC) zh-NC</span><span class="sxs-lookup"><span data-stu-id="ef925-150">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="ef925-151">Chinois traditionnel (Taïwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="ef925-151">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ef925-152">Langues prises en charge dans MBAM 2,5:</span><span class="sxs-lookup"><span data-stu-id="ef925-152">Supported Languages in MBAM 2.5:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef925-153">Langues client</span><span class="sxs-lookup"><span data-stu-id="ef925-153">Client Languages</span></span></th>
<th align="left"><span data-ttu-id="ef925-154">Langues du serveur</span><span class="sxs-lookup"><span data-stu-id="ef925-154">Server Languages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="ef925-155">Anglais (États-Unis) en-US</span><span class="sxs-lookup"><span data-stu-id="ef925-155">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="ef925-156">Français (France) fr-FR</span><span class="sxs-lookup"><span data-stu-id="ef925-156">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="ef925-157">Allemand (Allemagne) de-DE</span><span class="sxs-lookup"><span data-stu-id="ef925-157">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="ef925-158">IT Italien (Italie)-IT</span><span class="sxs-lookup"><span data-stu-id="ef925-158">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="ef925-159">Japonais (Japon) ja-JP</span><span class="sxs-lookup"><span data-stu-id="ef925-159">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="ef925-160">Coréen (Corée) ko-KR</span><span class="sxs-lookup"><span data-stu-id="ef925-160">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="ef925-161">Portugais (Brésil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="ef925-161">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="ef925-162">Russe (Russie) ru-RU</span><span class="sxs-lookup"><span data-stu-id="ef925-162">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="ef925-163">Espagnol (Espagne) es-ES</span><span class="sxs-lookup"><span data-stu-id="ef925-163">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="ef925-164">Chinois simplifié (RPC) zh-NC</span><span class="sxs-lookup"><span data-stu-id="ef925-164">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="ef925-165">Chinois traditionnel (Taïwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="ef925-165">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ef925-166">Anglais (États-Unis) en-US</span><span class="sxs-lookup"><span data-stu-id="ef925-166">English (United States) en-US</span></span></p></li>
<li><p><span data-ttu-id="ef925-167">Français (France) fr-FR</span><span class="sxs-lookup"><span data-stu-id="ef925-167">French (France) fr-FR</span></span></p></li>
<li><p><span data-ttu-id="ef925-168">Allemand (Allemagne) de-DE</span><span class="sxs-lookup"><span data-stu-id="ef925-168">German (Germany) de-DE</span></span></p></li>
<li><p><span data-ttu-id="ef925-169">IT Italien (Italie)-IT</span><span class="sxs-lookup"><span data-stu-id="ef925-169">Italian (Italy) it-IT</span></span></p></li>
<li><p><span data-ttu-id="ef925-170">Japonais (Japon) ja-JP</span><span class="sxs-lookup"><span data-stu-id="ef925-170">Japanese (Japan) ja-JP</span></span></p></li>
<li><p><span data-ttu-id="ef925-171">Coréen (Corée) ko-KR</span><span class="sxs-lookup"><span data-stu-id="ef925-171">Korean (Korea) ko-KR</span></span></p></li>
<li><p><span data-ttu-id="ef925-172">Portugais (Brésil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="ef925-172">Portuguese (Brazil) pt-BR</span></span></p></li>
<li><p><span data-ttu-id="ef925-173">Russe (Russie) ru-RU</span><span class="sxs-lookup"><span data-stu-id="ef925-173">Russian (Russia) ru-RU</span></span></p></li>
<li><p><span data-ttu-id="ef925-174">Espagnol (Espagne) es-ES</span><span class="sxs-lookup"><span data-stu-id="ef925-174">Spanish (Spain) es-ES</span></span></p></li>
<li><p><span data-ttu-id="ef925-175">Chinois simplifié (RPC) zh-NC</span><span class="sxs-lookup"><span data-stu-id="ef925-175">Simplified Chinese (PRC) zh-CN</span></span></p></li>
<li><p><span data-ttu-id="ef925-176">Chinois traditionnel (Taïwan) zh-TW</span><span class="sxs-lookup"><span data-stu-id="ef925-176">Traditional Chinese (Taiwan) zh-TW</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="ef925-177">Configuration système requise pour MBAM Server</span><span class="sxs-lookup"><span data-stu-id="ef925-177">MBAM Server system requirements</span></span>


### <span data-ttu-id="ef925-178">Configuration requise pour le système d’exploitation MBAM</span><span class="sxs-lookup"><span data-stu-id="ef925-178">MBAM Server operating system requirements</span></span>

<span data-ttu-id="ef925-179">Nous vous recommandons vivement d’exécuter le client MBAM et MBAM Server sur la même ligne de systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ef925-179">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="ef925-180">Par exemple, Windows 10 avec Windows Server 2016, Windows 8,1 avec Windows Server 2012 R2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="ef925-180">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="ef925-181">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="ef925-181">The following table lists the operating systems that are supported for the MBAM Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef925-182">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ef925-182">Operating system</span></span></th>
<th align="left"><span data-ttu-id="ef925-183">Édition</span><span class="sxs-lookup"><span data-stu-id="ef925-183">Edition</span></span></th>
<th align="left"><span data-ttu-id="ef925-184">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ef925-184">Service pack</span></span></th>
<th align="left"><span data-ttu-id="ef925-185">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ef925-185">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-186">Windows Server2016</span><span class="sxs-lookup"><span data-stu-id="ef925-186">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-187">Standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ef925-187">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="ef925-188">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-188">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef925-189">WindowsServer2012R2</span><span class="sxs-lookup"><span data-stu-id="ef925-189">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-190">Standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ef925-190">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ef925-191">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-191">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-192">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="ef925-192">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-193">Standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ef925-193">Standard or Datacenter</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="ef925-194">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-194">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-195">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="ef925-195">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-196">Standard, entreprise ou centre de</span><span class="sxs-lookup"><span data-stu-id="ef925-196">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-197">SP1</span><span class="sxs-lookup"><span data-stu-id="ef925-197">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-198">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-198">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="ef925-199">Le domaine d’entreprise doit contenir au moins un contrôleur de domaine Windows Server 2008 (ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="ef925-199">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span>

### <a href="" id="bkmk-stand-alone-ramreqs"></a><span data-ttu-id="ef925-200">Configuration requise pour le processeur du serveur MBAM, la RAM et l’espace disque-topologie autonome</span><span class="sxs-lookup"><span data-stu-id="ef925-200">MBAM Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="ef925-201">Ces exigences concernent la topologie autonome MBAM.</span><span class="sxs-lookup"><span data-stu-id="ef925-201">These requirements are for the MBAM Stand-alone topology.</span></span> <span data-ttu-id="ef925-202">Pour connaître la configuration requise pour la topologie d’intégration de Configuration Manager, voir Configuration requise pour le [processeur du serveur MBAM, la RAM et l’espace disque-topologie d’intégration de Configuration Manager](#bkmk-cm-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="ef925-202">For the requirements for the Configuration Manager Integration topology, see [MBAM Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef925-203">Élément matériel</span><span class="sxs-lookup"><span data-stu-id="ef925-203">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="ef925-204">Configuration minimale</span><span class="sxs-lookup"><span data-stu-id="ef925-204">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="ef925-205">Configuration recommandée</span><span class="sxs-lookup"><span data-stu-id="ef925-205">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-206">Processeur</span><span class="sxs-lookup"><span data-stu-id="ef925-206">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-207">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="ef925-207">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-208">2,33 GHz ou supérieur</span><span class="sxs-lookup"><span data-stu-id="ef925-208">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef925-209">Mémoire vive (RAM)</span><span class="sxs-lookup"><span data-stu-id="ef925-209">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-210">8 GO</span><span class="sxs-lookup"><span data-stu-id="ef925-210">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-211">12 GO</span><span class="sxs-lookup"><span data-stu-id="ef925-211">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-212">Espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="ef925-212">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-213">1 Go</span><span class="sxs-lookup"><span data-stu-id="ef925-213">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-214">2 Go</span><span class="sxs-lookup"><span data-stu-id="ef925-214">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-ramreqs"></a><span data-ttu-id="ef925-215">Configurations requises pour le processeur du serveur MBAM, la RAM et l’espace disque-topologie d’intégration de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ef925-215">MBAM Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="ef925-216">Le tableau suivant répertorie les conditions requises processeur de serveur, RAM et espace disque pour les serveurs MBAM lorsque vous utilisez la topologie d’intégration de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ef925-216">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span> <span data-ttu-id="ef925-217">Pour connaître la configuration requise pour la topologie autonome, voir [Configuration requise pour le processeur MBAM, la RAM et l’espace disque-topologie autonome](#bkmk-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="ef925-217">For the requirements for the Stand-alone topology, see [MBAM Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef925-218">Élément matériel</span><span class="sxs-lookup"><span data-stu-id="ef925-218">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="ef925-219">Configuration minimale</span><span class="sxs-lookup"><span data-stu-id="ef925-219">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="ef925-220">Configuration recommandée</span><span class="sxs-lookup"><span data-stu-id="ef925-220">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-221">Processeur</span><span class="sxs-lookup"><span data-stu-id="ef925-221">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-222">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="ef925-222">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-223">2,33 GHz ou supérieur</span><span class="sxs-lookup"><span data-stu-id="ef925-223">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef925-224">Mémoire vive (RAM)</span><span class="sxs-lookup"><span data-stu-id="ef925-224">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-225">4 Go</span><span class="sxs-lookup"><span data-stu-id="ef925-225">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-226">8 GO</span><span class="sxs-lookup"><span data-stu-id="ef925-226">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-227">Espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="ef925-227">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-228">1 Go</span><span class="sxs-lookup"><span data-stu-id="ef925-228">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-229">2 Go</span><span class="sxs-lookup"><span data-stu-id="ef925-229">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a><span data-ttu-id="ef925-230">Versions du gestionnaire de configurations prises en charge par MBAM</span><span class="sxs-lookup"><span data-stu-id="ef925-230">Versions of Configuration Manager that MBAM supports</span></span>

<span data-ttu-id="ef925-231">MBAM prend en charge les versions suivantes de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ef925-231">MBAM supports the following versions of Configuration Manager.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef925-232">Version prise en charge</span><span class="sxs-lookup"><span data-stu-id="ef925-232">Supported version</span></span></th>
<th align="left"><span data-ttu-id="ef925-233">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ef925-233">Service pack</span></span></th>
<th align="left"><span data-ttu-id="ef925-234">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ef925-234">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef925-235">Microsoft System Center Configuration Manager (branche actuelle), versions allant jusqu’à 1902</span><span class="sxs-lookup"><span data-stu-id="ef925-235">Microsoft System Center Configuration Manager (Current Branch), versions up to 1902</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ef925-236">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-236">64-bit</span></span></p></td>
</tr>

<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-237">Microsoft System Center Configuration Manager 1806</span><span class="sxs-lookup"><span data-stu-id="ef925-237">Microsoft System Center Configuration Manager 1806</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ef925-238">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-238">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef925-239">Microsoft System Center Configuration Manager (LTSB-version 1606)</span><span class="sxs-lookup"><span data-stu-id="ef925-239">Microsoft System Center Configuration Manager (LTSB - version 1606)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ef925-240">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-240">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-241">Gestionnaire de configuration de Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="ef925-241">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-242">SP1</span><span class="sxs-lookup"><span data-stu-id="ef925-242">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-243">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-243">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef925-244">Microsoft System Center Configuration Manager 2007 R2 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ef925-244">Microsoft System Center Configuration Manager 2007 R2 or later</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ef925-245">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-245">64-bit</span></span></p>

<span data-ttu-id="ef925-246">&gt;<strong>Remarque </strong> bien que Configuration Manager 2007 R2 soit 32 bits, vous devez l’installer et SQL Server sur un système d’exploitation 64 bits afin de correspondre au logiciel MBAM 64.</span><span class="sxs-lookup"><span data-stu-id="ef925-246">&gt;<strong>Note</strong> Although Configuration Manager 2007 R2 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span>
</td>
</tr>
</tbody>
</table>



<span data-ttu-id="ef925-247">Pour obtenir la liste des configurations prises en charge pour le serveur Configuration Manager, consultez la documentation TechNet appropriée pour la version de Configuration Manager que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="ef925-247">For a list of supported configurations for the Configuration Manager Server, see the appropriate TechNet documentation for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="ef925-248">MBAM ne possède aucune configuration système supplémentaire pour le serveur Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ef925-248">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="ef925-249">Configuration requise pour la base de données SQL Server</span><span class="sxs-lookup"><span data-stu-id="ef925-249">SQL Server database requirements</span></span>

<span data-ttu-id="ef925-250">Le tableau suivant répertorie les versions de Microsoft SQL Server prises en charge pour les fonctionnalités du serveur MBAM, notamment la base de données de récupération, la base de données d’audit et de conformité, et la fonctionnalité rapports.</span><span class="sxs-lookup"><span data-stu-id="ef925-250">The following table lists the Microsoft SQL Server versions that are supported for the MBAM Server features, which include the Recovery Database, Compliance and Audit Database, and the Reports feature.</span></span> <span data-ttu-id="ef925-251">Les versions requises s’appliquent aux topologies d’intégration autonomes et de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ef925-251">The required versions apply to the Stand-alone or the Configuration Manager Integration topologies.</span></span>

<span data-ttu-id="ef925-252">Vous devez installer SQL Server à l’aide du **SQL \ _Latin1 \ _General \ _CP1 \ _CI \ _AS** collation.</span><span class="sxs-lookup"><span data-stu-id="ef925-252">You must install SQL Server with the **SQL\_Latin1\_General\_CP1\_CI\_AS** collation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef925-253">Version de SQL Server</span><span class="sxs-lookup"><span data-stu-id="ef925-253">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="ef925-254">Édition</span><span class="sxs-lookup"><span data-stu-id="ef925-254">Edition</span></span></th>
<th align="left"><span data-ttu-id="ef925-255">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ef925-255">Service pack</span></span></th>
<th align="left"><span data-ttu-id="ef925-256">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ef925-256">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-257">Microsoft SQL Server 2017</span><span class="sxs-lookup"><span data-stu-id="ef925-257">Microsoft SQL Server 2017</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-258">Standard, entreprise ou centre de</span><span class="sxs-lookup"><span data-stu-id="ef925-258">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ef925-259">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-259">64-bit</span></span></p></td><br/><tr class="even">
<td align="left"><p><span data-ttu-id="ef925-260">MicrosoftSQLServer2016</span><span class="sxs-lookup"><span data-stu-id="ef925-260">Microsoft SQL Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-261">Standard, entreprise ou centre de</span><span class="sxs-lookup"><span data-stu-id="ef925-261">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-262">SP1</span><span class="sxs-lookup"><span data-stu-id="ef925-262">SP1</span></span></p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p><span data-ttu-id="ef925-263">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-263">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-264">MicrosoftSQLServer2014</span><span class="sxs-lookup"><span data-stu-id="ef925-264">Microsoft SQL Server 2014</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-265">Standard, entreprise ou centre de</span><span class="sxs-lookup"><span data-stu-id="ef925-265">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-266">SP1, SP2</span><span class="sxs-lookup"><span data-stu-id="ef925-266">SP1, SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-267">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-267">64-bit</span></span></p></td>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-268">MicrosoftSQLServer 2012</span><span class="sxs-lookup"><span data-stu-id="ef925-268">Microsoft SQL Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-269">Standard, entreprise ou centre de</span><span class="sxs-lookup"><span data-stu-id="ef925-269">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-270">3</span><span class="sxs-lookup"><span data-stu-id="ef925-270">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-271">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-271">64-bit</span></span></p></td>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef925-272">Microsoft SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ef925-272">Microsoft SQL Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-273">Standard ou Entreprise</span><span class="sxs-lookup"><span data-stu-id="ef925-273">Standard or Enterprise</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-274">3</span><span class="sxs-lookup"><span data-stu-id="ef925-274">SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-275">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-275">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

**<span data-ttu-id="ef925-276">Remarque</span><span class="sxs-lookup"><span data-stu-id="ef925-276">Note</span></span>**  
<span data-ttu-id="ef925-277">Pour prendre en charge SQL 2016, vous devez installer le version de service de mars 2017 pour MDOP https://www.microsoft.com/download/details.aspx?id=54967 et prendre en charge sql 2017 vous devez installer la version de maintenance de juillet 2018 pour MDOP https://www.microsoft.com/download/details.aspx?id=57157 .</span><span class="sxs-lookup"><span data-stu-id="ef925-277">In order to support SQL 2016 you must install the March 2017 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=54967  and to support SQL 2017 you must install the July 2018 Servicing Release for MDOP https://www.microsoft.com/download/details.aspx?id=57157.</span></span> <span data-ttu-id="ef925-278">En règle générale, restez en mesure d’utiliser la mise à jour de maintenance la plus récente, car elle inclut également toutes les ainsi correctifs et nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="ef925-278">In general stay current by always using the most recent servicing update as it also includes all bugfixes and new features.</span></span>


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a><span data-ttu-id="ef925-279">Configuration requise pour le processeur SQL Server, la RAM et l’espace disque-topologie autonome</span><span class="sxs-lookup"><span data-stu-id="ef925-279">SQL Server processor, RAM, and disk space requirements – Stand-alone topology</span></span>

<span data-ttu-id="ef925-280">Le tableau suivant répertorie les exigences relatives au processeur, à la RAM et à l’espace disque recommandés pour l’ordinateur SQL Server lors de l’utilisation de la topologie autonome.</span><span class="sxs-lookup"><span data-stu-id="ef925-280">The following table lists the recommended server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Stand-alone topology.</span></span> <span data-ttu-id="ef925-281">Utilisez ces exigences comme guide.</span><span class="sxs-lookup"><span data-stu-id="ef925-281">Use these requirements as a guide.</span></span> <span data-ttu-id="ef925-282">Vos exigences spécifiques varient en fonction du nombre d’ordinateurs clients que vous prenez en charge au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="ef925-282">Your specific requirements will vary based on the number of client computers you are supporting in your enterprise.</span></span> <span data-ttu-id="ef925-283">Pour consulter la configuration requise pour la topologie d’intégration de Configuration Manager, voir Configuration requise pour le [processeur SQL Server, la RAM et l’espace disque-topologie d’intégration de Configuration Manager](#bkmk-cm-sql-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="ef925-283">To view the requirements for the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements - Configuration Manager Integration Topology](#bkmk-cm-sql-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef925-284">Élément matériel</span><span class="sxs-lookup"><span data-stu-id="ef925-284">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="ef925-285">Configuration minimale</span><span class="sxs-lookup"><span data-stu-id="ef925-285">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="ef925-286">Configuration recommandée</span><span class="sxs-lookup"><span data-stu-id="ef925-286">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-287">Processeur</span><span class="sxs-lookup"><span data-stu-id="ef925-287">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-288">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="ef925-288">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-289">2,33 GHz ou supérieur</span><span class="sxs-lookup"><span data-stu-id="ef925-289">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef925-290">Mémoire vive (RAM)</span><span class="sxs-lookup"><span data-stu-id="ef925-290">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-291">8 GO</span><span class="sxs-lookup"><span data-stu-id="ef925-291">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-292">12 GO</span><span class="sxs-lookup"><span data-stu-id="ef925-292">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-293">Espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="ef925-293">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-294">5 GO</span><span class="sxs-lookup"><span data-stu-id="ef925-294">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-295">5 Go minimum</span><span class="sxs-lookup"><span data-stu-id="ef925-295">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cm-sql-ramreqs"></a><span data-ttu-id="ef925-296">Configuration requise pour le processeur SQL Server, la RAM et l’espace disque-topologie d’intégration de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ef925-296">SQL Server processor, RAM, and disk space requirements - Configuration Manager Integration topology</span></span>

<span data-ttu-id="ef925-297">Le tableau suivant répertorie les exigences relatives au processeur, à la RAM et à l’espace disque pour l’ordinateur Microsoft SQL Server lors de l’utilisation de la topologie d’intégration de Configuration Manager, voir [topologie autonome du processeur SQL Server, de la RAM et de l’espace disque](#bkmk-sql-stand-alone-ramreqs).</span><span class="sxs-lookup"><span data-stu-id="ef925-297">The following table lists the server processor, RAM, and disk space requirements for the Microsoft SQL Server computer when you are using the Configuration Manager Integration topology, see [SQL Server Processor, RAM, and Disk Space Requirements – Stand-alone Topology](#bkmk-sql-stand-alone-ramreqs).</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef925-298">Élément matériel</span><span class="sxs-lookup"><span data-stu-id="ef925-298">Hardware item</span></span></th>
<th align="left"><span data-ttu-id="ef925-299">Configuration minimale</span><span class="sxs-lookup"><span data-stu-id="ef925-299">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="ef925-300">Configuration recommandée</span><span class="sxs-lookup"><span data-stu-id="ef925-300">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-301">Processeur</span><span class="sxs-lookup"><span data-stu-id="ef925-301">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-302">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="ef925-302">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-303">2,33 GHz ou supérieur</span><span class="sxs-lookup"><span data-stu-id="ef925-303">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef925-304">Mémoire vive (RAM)</span><span class="sxs-lookup"><span data-stu-id="ef925-304">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-305">4 Go</span><span class="sxs-lookup"><span data-stu-id="ef925-305">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-306">8 GO</span><span class="sxs-lookup"><span data-stu-id="ef925-306">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-307">Espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="ef925-307">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-308">5 GO</span><span class="sxs-lookup"><span data-stu-id="ef925-308">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-309">5 GO</span><span class="sxs-lookup"><span data-stu-id="ef925-309">5 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="ef925-310">Configuration système requise pour le client MBAM</span><span class="sxs-lookup"><span data-stu-id="ef925-310">MBAM Client system requirements</span></span>


### <span data-ttu-id="ef925-311">Configuration requise du système d’exploitation client</span><span class="sxs-lookup"><span data-stu-id="ef925-311">Client operating system requirements</span></span>

<span data-ttu-id="ef925-312">Nous vous recommandons vivement d’exécuter le client MBAM et MBAM Server sur la même ligne de systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ef925-312">We strongly recommend that you run the MBAM Client and MBAM Server on the same line of operating systems.</span></span> <span data-ttu-id="ef925-313">Par exemple, Windows 10 avec Windows Server 2016, Windows 8,1 avec Windows Server 2012 R2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="ef925-313">For example, Windows 10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

<span data-ttu-id="ef925-314">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="ef925-314">The following table lists the operating systems that are supported for MBAM Client installation.</span></span> <span data-ttu-id="ef925-315">Les mêmes exigences s’appliquent aux topologies d’intégration autonome et Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ef925-315">The same requirements apply to the Stand-alone and the Configuration Manager Integration topologies.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef925-316">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ef925-316">Operating system</span></span></th>
<th align="left"><span data-ttu-id="ef925-317">Édition</span><span class="sxs-lookup"><span data-stu-id="ef925-317">Edition</span></span></th>
<th align="left"><span data-ttu-id="ef925-318">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ef925-318">Service pack</span></span></th>
<th align="left"><span data-ttu-id="ef925-319">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ef925-319">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
    <td align="left"><p><span data-ttu-id="ef925-320">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="ef925-320">Windows 10 IoT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ef925-321">Enterprise</span><span class="sxs-lookup"><span data-stu-id="ef925-321">Enterprise</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p><span data-ttu-id="ef925-322">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ef925-322">32-bit or 64-bit</span></span></p></td>
</tr><br/><tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-323">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ef925-323">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-324">Enterprise</span><span class="sxs-lookup"><span data-stu-id="ef925-324">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ef925-325">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ef925-325">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef925-326">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ef925-326">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-327">Enterprise</span><span class="sxs-lookup"><span data-stu-id="ef925-327">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ef925-328">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ef925-328">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-329">Windows7</span><span class="sxs-lookup"><span data-stu-id="ef925-329">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-330">Entreprise ou intégrale</span><span class="sxs-lookup"><span data-stu-id="ef925-330">Enterprise or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-331">SP1</span><span class="sxs-lookup"><span data-stu-id="ef925-331">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-332">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ef925-332">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef925-333">WindowsToGo</span><span class="sxs-lookup"><span data-stu-id="ef925-333">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-334">Windows 8,1 et Windows 10 entreprise</span><span class="sxs-lookup"><span data-stu-id="ef925-334">Windows 8.1 and Windows 10 Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ef925-335">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ef925-335">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="ef925-336">Configuration requise pour le client RAM</span><span class="sxs-lookup"><span data-stu-id="ef925-336">Client RAM requirements</span></span>

<span data-ttu-id="ef925-337">Il n’existe aucune exigence de RAM spécifique à l’installation du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="ef925-337">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="ef925-338">Configuration système requise pour la stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="ef925-338">MBAM Group Policy system requirements</span></span>


<span data-ttu-id="ef925-339">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de modèles de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="ef925-339">The following table lists the operating systems that are supported for MBAM Group Policy Templates installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ef925-340">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ef925-340">Operating system</span></span></th>
<th align="left"><span data-ttu-id="ef925-341">Édition</span><span class="sxs-lookup"><span data-stu-id="ef925-341">Edition</span></span></th>
<th align="left"><span data-ttu-id="ef925-342">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ef925-342">Service pack</span></span></th>
<th align="left"><span data-ttu-id="ef925-343">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ef925-343">System architecture</span></span></th>
</tr>
</thead>
<tbody>
 <tr class="even">
      <td align="left"><p><span data-ttu-id="ef925-344">Windows 10 IoT</span><span class="sxs-lookup"><span data-stu-id="ef925-344">Windows 10 IoT</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ef925-345">Enterprise</span><span class="sxs-lookup"><span data-stu-id="ef925-345">Enterprise</span></span></p></td>
      <td align="left"><p></p></td>
      <td align="left"><p><span data-ttu-id="ef925-346">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ef925-346">32-bit or 64-bit</span></span></p></td>
 </tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-347">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ef925-347">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-348">Enterprise</span><span class="sxs-lookup"><span data-stu-id="ef925-348">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ef925-349">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ef925-349">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef925-350">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ef925-350">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-351">Enterprise</span><span class="sxs-lookup"><span data-stu-id="ef925-351">Enterprise</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ef925-352">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ef925-352">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-353">Windows7</span><span class="sxs-lookup"><span data-stu-id="ef925-353">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-354">Entreprise ou intégrale</span><span class="sxs-lookup"><span data-stu-id="ef925-354">Enterprise, or Ultimate</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-355">SP1</span><span class="sxs-lookup"><span data-stu-id="ef925-355">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-356">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ef925-356">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef925-357">WindowsServer2012R2</span><span class="sxs-lookup"><span data-stu-id="ef925-357">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-358">Standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ef925-358">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ef925-359">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-359">64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ef925-360">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="ef925-360">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-361">Standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ef925-361">Standard or Datacenter</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ef925-362">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-362">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ef925-363">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="ef925-363">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-364">Standard, entreprise ou centre de</span><span class="sxs-lookup"><span data-stu-id="ef925-364">Standard, Enterprise, or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-365">SP1</span><span class="sxs-lookup"><span data-stu-id="ef925-365">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ef925-366">64 bits</span><span class="sxs-lookup"><span data-stu-id="ef925-366">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="ef925-367">MBAM dans Azure IaaS</span><span class="sxs-lookup"><span data-stu-id="ef925-367">MBAM In Azure IaaS</span></span>

<span data-ttu-id="ef925-368">Le serveur MBAM peut être déployé dans Azure infrastructure en tant que service (IaaS) sur les versions de système d’exploitation prises en charge répertoriées ci-dessus, qui se connectent à un annuaire actif hébergé sur un site ou un Active Directory également hébergé dans Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="ef925-368">The MBAM server can be deployed in Azure Infrastructure as a Service (IaaS) on any of the supported OS versions listed above, connecting to an Active Directory hosted on premises or an Active Directory also hosted in Azure IaaS.</span></span>  <span data-ttu-id="ef925-369">La documentation relative à la configuration et à la configuration d’Active Directory sur Azure IaaS est disponible [ici](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span><span class="sxs-lookup"><span data-stu-id="ef925-369">Documentation for setting up and configuring Active Directory on Azure IaaS is [here](https://msdn.microsoft.com/library/azure/jj156090.aspx).</span></span>

<span data-ttu-id="ef925-370">Le client MBAM n’est pas pris en charge sur les machines virtuelles et n’est pas non plus pris en charge sur Azure IaaS.</span><span class="sxs-lookup"><span data-stu-id="ef925-370">The MBAM client is not supported on virtual machines and is also not supported on Azure IaaS.</span></span>


## <span data-ttu-id="ef925-371">Service Releases</span><span class="sxs-lookup"><span data-stu-id="ef925-371">Service releases</span></span> 

- [<span data-ttu-id="ef925-372">Correctif 2016 d’avril</span><span class="sxs-lookup"><span data-stu-id="ef925-372">April 2016 hotfix</span></span>](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="ef925-373">2016 septembre</span><span class="sxs-lookup"><span data-stu-id="ef925-373">September 2016</span></span>](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [<span data-ttu-id="ef925-374">Décembre2016</span><span class="sxs-lookup"><span data-stu-id="ef925-374">December 2016</span></span>](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [<span data-ttu-id="ef925-375">Mars2017</span><span class="sxs-lookup"><span data-stu-id="ef925-375">March 2017</span></span>](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [<span data-ttu-id="ef925-376">Juin2017</span><span class="sxs-lookup"><span data-stu-id="ef925-376">June 2017</span></span>](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="ef925-377">Septembre2017</span><span class="sxs-lookup"><span data-stu-id="ef925-377">September 2017</span></span>](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [<span data-ttu-id="ef925-378">Mars2018</span><span class="sxs-lookup"><span data-stu-id="ef925-378">March 2018</span></span>](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="ef925-379">2018 juillet</span><span class="sxs-lookup"><span data-stu-id="ef925-379">July 2018</span></span>](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [<span data-ttu-id="ef925-380">2019</span><span class="sxs-lookup"><span data-stu-id="ef925-380">May 2019</span></span>](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## <span data-ttu-id="ef925-381">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef925-381">Related topics</span></span>


[<span data-ttu-id="ef925-382">Planification du déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ef925-382">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="ef925-383">Préparation de votre environnement pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ef925-383">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)




## <span data-ttu-id="ef925-384">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="ef925-384">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ef925-385">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="ef925-385">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ef925-386">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ef925-386">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




