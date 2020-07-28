---
title: Nouveautés d'AGPM4.0SP3
description: Nouveautés d'AGPM4.0SP3
author: dansimp
ms.assetid: df495d55-9fbf-4f7e-a7af-3905f4f8790e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 44e7dc6c5de75ae3a5e5def638974bae20ad2a1e
ms.sourcegitcommit: 594b6e431af98562e0b806e224d2c5c7e07d2c77
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/27/2020
ms.locfileid: "10895764"
---
# <span data-ttu-id="c422a-103">Nouveautés d'AGPM4.0SP3</span><span class="sxs-lookup"><span data-stu-id="c422a-103">What's New in AGPM 4.0 SP3</span></span>


<span data-ttu-id="c422a-104">Ce contenu décrit les améliorations et les configurations prises en charge pour Microsoft Advanced Group Policy Management (AGPM) 4.0 Service Pack3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="c422a-104">This content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack3 (SP3).</span></span> <span data-ttu-id="c422a-105">S’il existe une différence entre ce contenu et une autre documentation AGPM, considérez ce contenu faisant autorité et supposez qu’il remplace l’autre documentation.</span><span class="sxs-lookup"><span data-stu-id="c422a-105">If there is a difference between this content and other AGPM documentation, consider this content authoritative and assume that it supersedes the other documentation.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="c422a-106">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="c422a-106">What’s new</span></span>


<span data-ttu-id="c422a-107">Le SP3 d’AGPM 4.0 prend en charge les fonctionnalités et fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="c422a-107">AGPM4.0 SP3 supports the following features and functionality.</span></span>

### <span data-ttu-id="c422a-108">Prise en charge de Windows 10</span><span class="sxs-lookup"><span data-stu-id="c422a-108">Support for Windows10</span></span>

<span data-ttu-id="c422a-109">Le SP3 d’AGPM 4.0 ajoute une prise en charge pour les systèmes d’exploitation Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="c422a-109">AGPM4.0 SP3 adds support for the Windows10 and Windows Server 2016 operating systems.</span></span>

### <span data-ttu-id="c422a-110">Prise en charge de PowerShell</span><span class="sxs-lookup"><span data-stu-id="c422a-110">Support for PowerShell</span></span>

<span data-ttu-id="c422a-111">Le SP3 d’AGPM 4.0 ajoute une prise en charge des cmdlets PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c422a-111">AGPM4.0 SP3 adds support for PowerShell cmdlets.</span></span> <span data-ttu-id="c422a-112">Pour obtenir la liste des applets de service disponibles dans AGPM 4.0 SP3, y compris les descriptions et la syntaxe, voir [automatisation du pack d’optimisation du bureau Microsoft avec Windows PowerShell](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps).</span><span class="sxs-lookup"><span data-stu-id="c422a-112">For a list of the cmdlets available in AGPM4.0 SP3, including descriptions and syntax, see [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps).</span></span>

### <span data-ttu-id="c422a-113">Commentaires des clients et ROLLUP de HotFix</span><span class="sxs-lookup"><span data-stu-id="c422a-113">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="c422a-114">Le SP3 d’AGPM 4,0 inclut un cumul de tous les correctifs de la gestion de la stratégie de groupe Microsoft avancée 4,0 SP2 ainsi que des solutions aux problèmes rencontrés depuis AGPM 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="c422a-114">AGPM 4.0 SP3 includes a rollup of all fixes up to and including Microsoft Advanced Group Policy Management 4.0 SP2 and any fixes for issues found since AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="c422a-115">Possibilité d’effectuer la mise à niveau vers AGPM 4.0 SP3 sans entrer de nouveau les paramètres de configuration</span><span class="sxs-lookup"><span data-stu-id="c422a-115">Ability to upgrade to AGPM4.0 SP3 without re-entering configuration parameters</span></span>

<span data-ttu-id="c422a-116">Vous pouvez mettre à niveau le client AGPM ou le serveur AGPM vers AGPM 4.0 SP3 sans être invité à entrer de nouveau les paramètres de configuration (appelé mise à niveau intelligente) uniquement dans AGPM 4.0 et les versions ultérieures, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c422a-116">You can upgrade the AGPM Client or AGPM Server to AGPM4.0 SP3 without being prompted to re-enter configuration parameters (called the Smart Upgrade) only from AGPM4.0 and later, as shown in the following table.</span></span> <span data-ttu-id="c422a-117">Si vous effectuez une mise à niveau vers AGPM 4.0 SP3 à partir d’autres versions d’AGPM, comme indiqué dans le tableau ci-dessous, vous devez utiliser la mise à niveau classique, qui nécessite d’entrer de nouveau les paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="c422a-117">If you are upgrading to AGPM4.0 SP3 from other versions of AGPM, as shown in the table, you must use the Classic Upgrade, which requires you to re-enter the configuration parameters.</span></span> <span data-ttu-id="c422a-118">Étant donné que chaque version d’AGPM est associée à un système d’exploitation spécifique, voir [choisir la version d’AGPM à installer](https://go.microsoft.com/fwlink/?LinkId=254350) et vérifier que vous effectuez une mise à niveau de votre système d’exploitation le cas échéant avant de procéder à la mise à niveau d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="c422a-118">Because each version of AGPM is associated with a particular operating system, see [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350) and make sure that you upgrade your operating system as appropriate before you upgrade AGPM.</span></span>

**<span data-ttu-id="c422a-119">Mises à jour d’AGPM 4,0 SP3 prises en charge</span><span class="sxs-lookup"><span data-stu-id="c422a-119">AGPM 4.0 SP3 supported upgrades</span></span>**

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c422a-120">Version d’AGPM à partir de laquelle vous pouvez effectuer la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="c422a-120">AGPM version from which you can upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c422a-121">2,5</span><span class="sxs-lookup"><span data-stu-id="c422a-121">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c422a-122">3,0</span><span class="sxs-lookup"><span data-stu-id="c422a-122">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c422a-123">4,0</span><span class="sxs-lookup"><span data-stu-id="c422a-123">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c422a-124">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c422a-124">4.0 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c422a-125">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="c422a-125">4.0 SP2</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="c422a-126">4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="c422a-126">4.0 SP3</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c422a-127">2,5</span><span class="sxs-lookup"><span data-stu-id="c422a-127">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-128">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c422a-128">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-129">Mise à niveau classique</span><span class="sxs-lookup"><span data-stu-id="c422a-129">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-130">Mise à niveau classique</span><span class="sxs-lookup"><span data-stu-id="c422a-130">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-131">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="c422a-131">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-132">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="c422a-132">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-133">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="c422a-133">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c422a-134">3,0</span><span class="sxs-lookup"><span data-stu-id="c422a-134">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-135">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c422a-135">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-136">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c422a-136">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-137">Mise à niveau classique</span><span class="sxs-lookup"><span data-stu-id="c422a-137">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-138">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="c422a-138">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-139">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="c422a-139">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-140">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="c422a-140">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c422a-141">4,0</span><span class="sxs-lookup"><span data-stu-id="c422a-141">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-142">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c422a-142">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-143">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c422a-143">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-144">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c422a-144">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-145">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="c422a-145">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-146">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="c422a-146">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-147">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="c422a-147">Smart Upgrade</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c422a-148">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c422a-148">4.0 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-149">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c422a-149">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-150">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c422a-150">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-151">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c422a-151">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-152">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c422a-152">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-153">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="c422a-153">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-154">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="c422a-154">Smart Upgrade</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c422a-155">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="c422a-155">4.0 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-156">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c422a-156">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-157">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c422a-157">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-158">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c422a-158">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-159">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c422a-159">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-160">Non applicable</span><span class="sxs-lookup"><span data-stu-id="c422a-160">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-161">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="c422a-161">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c422a-162">Configurations prises en charge</span><span class="sxs-lookup"><span data-stu-id="c422a-162">Supported configurations</span></span>


<span data-ttu-id="c422a-163">AGPM 4.0 SP3 prend en charge les configurations figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c422a-163">AGPM4.0 SP3 supports the configurations in the following table.</span></span> <span data-ttu-id="c422a-164">Bien qu’AGPM prenne en charge des configurations mixtes, nous vous recommandons vivement d’exécuter le client AGPM et le serveur AGPM sur la même ligne de système d’exploitation (par exemple, Windows 10 avec Windows Server 2016, Windows 8,1 avec Windows Server 2012 R2, etc.).</span><span class="sxs-lookup"><span data-stu-id="c422a-164">Although AGPM supports mixed configurations, we strongly recommend that you run the AGPM Client and AGPM Server on the same operating system line—for example, Windows10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

**<span data-ttu-id="c422a-165">Systèmes d’exploitation et systèmes d’exploitation pris en charge par AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="c422a-165">AGPM4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="c422a-166">Configurations prises en charge pour le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="c422a-166">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c422a-167">Configurations prises en charge pour le client AGPM</span><span class="sxs-lookup"><span data-stu-id="c422a-167">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="c422a-168">Prise en charge d’AGPM</span><span class="sxs-lookup"><span data-stu-id="c422a-168">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c422a-169">Windows Server 2019 ou Windows 10</span><span class="sxs-lookup"><span data-stu-id="c422a-169">Windows Server 2019 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-170">Windows10</span><span class="sxs-lookup"><span data-stu-id="c422a-170">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-171">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="c422a-171">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c422a-172">Windows Server 2016 ou Windows 10</span><span class="sxs-lookup"><span data-stu-id="c422a-172">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-173">Windows10</span><span class="sxs-lookup"><span data-stu-id="c422a-173">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-174">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="c422a-174">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c422a-175">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c422a-175">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-176">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c422a-176">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-177">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="c422a-177">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c422a-178">Windows Server2012 R2, Windows Server 2012 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c422a-178">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-179">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="c422a-179">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-180">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c422a-180">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c422a-181">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="c422a-181">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-182">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="c422a-182">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-183">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c422a-183">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c422a-184">Windows Server 2012, Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="c422a-184">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-185">Windows Server 2008 ou Vista avec Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="c422a-185">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-186">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows</span><span class="sxs-lookup"><span data-stu-id="c422a-186">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c422a-187">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="c422a-187">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-188">Windows Server 2012, Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="c422a-188">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-189">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="c422a-189">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c422a-190">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="c422a-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-191">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="c422a-191">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c422a-192">Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="c422a-192">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c422a-193">Conditions préalables à l’installation d’AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="c422a-193">Prerequisites for installing AGPM4.0 SP3</span></span>

<span data-ttu-id="c422a-194">Le tableau suivant décrit le comportement d’AGPM 4.0 SP3 du client et du serveur lorsque .NET Framework 4.5.1, PowerShell 3,0 ou la console GPMC dans les outils d’administration de serveur distant est manquant.</span><span class="sxs-lookup"><span data-stu-id="c422a-194">The following table describes the behavior of AGPM4.0 SP3 Client and Server installers when the .NET Framework4.5.1, PowerShell 3.0, or the GPMC in the Remote Server Administration Tools is missing.</span></span>

| <span data-ttu-id="c422a-195">Client AGPM</span><span class="sxs-lookup"><span data-stu-id="c422a-195">AGPM Client</span></span>            |                                                                                                 |                                                                            | <span data-ttu-id="c422a-196">Serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="c422a-196">AGPM Server</span></span>                                                                     |                                                                                                 |                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="c422a-197">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="c422a-197">Operating system</span></span>       | <span data-ttu-id="c422a-198">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="c422a-198">.NET Framework</span></span>                                                                                  | <span data-ttu-id="c422a-199">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c422a-199">PowerShell</span></span>                                                                 | <span data-ttu-id="c422a-200">Outils d'administration de serveur distant</span><span class="sxs-lookup"><span data-stu-id="c422a-200">Remote Server Administration Tools</span></span>                                              | <span data-ttu-id="c422a-201">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="c422a-201">.NET Framework</span></span>                                                                                  | <span data-ttu-id="c422a-202">Outils d'administration de serveur distant</span><span class="sxs-lookup"><span data-stu-id="c422a-202">Remote Server Administration Tools</span></span>                                              |
| <span data-ttu-id="c422a-203">Windows 10</span><span class="sxs-lookup"><span data-stu-id="c422a-203">Windows 10</span></span>             | <span data-ttu-id="c422a-204">Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="c422a-204">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="c422a-205">Si PowerShell 3,0 n’est pas installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="c422a-205">If Powershell 3.0 is not installed, the installer blocks the installation.</span></span> | <span data-ttu-id="c422a-206">Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="c422a-206">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="c422a-207">Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="c422a-207">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="c422a-208">Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="c422a-208">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> |
| <span data-ttu-id="c422a-209">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c422a-209">Windows 8.1</span></span>            | <span data-ttu-id="c422a-210">Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="c422a-210">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="c422a-211">Si PowerShell 3,0 n’est pas installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="c422a-211">If Powershell 3.0 is not installed, the installer blocks the installation.</span></span> | <span data-ttu-id="c422a-212">Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="c422a-212">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="c422a-213">Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="c422a-213">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="c422a-214">Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="c422a-214">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> |
| <span data-ttu-id="c422a-215">WindowsServer2012R2</span><span class="sxs-lookup"><span data-stu-id="c422a-215">Windows Server 2012 R2</span></span> | <span data-ttu-id="c422a-216">Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="c422a-216">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="c422a-217">Si PowerShell 3,0 n’est pas installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="c422a-217">If Powershell 3.0 is not installed, the installer blocks the installation.</span></span> | <span data-ttu-id="c422a-218">Si la console GPMC n’est pas activée, le programme d’installation l’active au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="c422a-218">If the GPMC is not enabled, the installer enables it during the installation.</span></span>   | <span data-ttu-id="c422a-219">Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="c422a-219">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="c422a-220">Si la console GPMC n’est pas activée, le programme d’installation l’active au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="c422a-220">If the GPMC is not enabled, the installer enables it during the installation.</span></span>   |

 

## <span data-ttu-id="c422a-221">Obtention de technologies MDOP</span><span class="sxs-lookup"><span data-stu-id="c422a-221">How to Get MDOP Technologies</span></span>


<span data-ttu-id="c422a-222">Le pack d’optimisation du Bureau d’AGPM 4,0 est un composant de l’application MDOP 2015.</span><span class="sxs-lookup"><span data-stu-id="c422a-222">AGPM 4.0 SP3 is a part of the Microsoft Desktop Optimization Pack (MDOP) since MDOP 2015.</span></span> <span data-ttu-id="c422a-223">MDOP fait partie de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="c422a-223">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="c422a-224">Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="c422a-224">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="c422a-225">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c422a-225">Related topics</span></span>


[<span data-ttu-id="c422a-226">Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="c422a-226">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="c422a-227">Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP3</span><span class="sxs-lookup"><span data-stu-id="c422a-227">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp3.md)

[<span data-ttu-id="c422a-228">Choix de la version d'AGPM à installer</span><span class="sxs-lookup"><span data-stu-id="c422a-228">Choosing Which Version of AGPM to Install</span></span>](choosing-which-version-of-agpm-to-install.md)

 

 





