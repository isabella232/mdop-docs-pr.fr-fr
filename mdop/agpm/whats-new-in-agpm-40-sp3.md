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
ms.openlocfilehash: a98bda82fab561113522382b4de6539a9dc23d0c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808178"
---
# <span data-ttu-id="413b4-103">Nouveautés d'AGPM4.0SP3</span><span class="sxs-lookup"><span data-stu-id="413b4-103">What's New in AGPM 4.0 SP3</span></span>


<span data-ttu-id="413b4-104">Ce contenu décrit les améliorations et les configurations prises en charge pour Microsoft Advanced Group Policy Management (AGPM) 4.0 Service Pack3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="413b4-104">This content describes enhancements and supported configurations for Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack3 (SP3).</span></span> <span data-ttu-id="413b4-105">S’il existe une différence entre ce contenu et une autre documentation AGPM, considérez ce contenu faisant autorité et supposez qu’il remplace l’autre documentation.</span><span class="sxs-lookup"><span data-stu-id="413b4-105">If there is a difference between this content and other AGPM documentation, consider this content authoritative and assume that it supersedes the other documentation.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="413b4-106">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="413b4-106">What’s new</span></span>


<span data-ttu-id="413b4-107">Le SP3 d’AGPM 4.0 prend en charge les fonctionnalités et fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="413b4-107">AGPM4.0 SP3 supports the following features and functionality.</span></span>

### <span data-ttu-id="413b4-108">Prise en charge de Windows 10</span><span class="sxs-lookup"><span data-stu-id="413b4-108">Support for Windows10</span></span>

<span data-ttu-id="413b4-109">Le SP3 d’AGPM 4.0 ajoute une prise en charge pour les systèmes d’exploitation Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="413b4-109">AGPM4.0 SP3 adds support for the Windows10 and Windows Server 2016 operating systems.</span></span>

### <span data-ttu-id="413b4-110">Prise en charge de PowerShell</span><span class="sxs-lookup"><span data-stu-id="413b4-110">Support for PowerShell</span></span>

<span data-ttu-id="413b4-111">Le SP3 d’AGPM 4.0 ajoute une prise en charge des cmdlets PowerShell.</span><span class="sxs-lookup"><span data-stu-id="413b4-111">AGPM4.0 SP3 adds support for PowerShell cmdlets.</span></span> <span data-ttu-id="413b4-112">Pour obtenir la liste des applets de service disponibles dans AGPM 4.0 SP3, y compris les descriptions et la syntaxe, voir [automatisation du pack d’optimisation du bureau Microsoft avec Windows PowerShell](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps).</span><span class="sxs-lookup"><span data-stu-id="413b4-112">For a list of the cmdlets available in AGPM4.0 SP3, including descriptions and syntax, see [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps).</span></span>

### <span data-ttu-id="413b4-113">Commentaires des clients et ROLLUP de HotFix</span><span class="sxs-lookup"><span data-stu-id="413b4-113">Customer feedback and hotfix rollup</span></span>

<span data-ttu-id="413b4-114">Le SP3 d’AGPM 4,0 inclut un cumul de tous les correctifs de la gestion de la stratégie de groupe Microsoft avancée 4,0 SP2 ainsi que des solutions aux problèmes rencontrés depuis AGPM 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="413b4-114">AGPM 4.0 SP3 includes a rollup of all fixes up to and including Microsoft Advanced Group Policy Management 4.0 SP2 and any fixes for issues found since AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="413b4-115">Possibilité d’effectuer la mise à niveau vers AGPM 4.0 SP3 sans entrer de nouveau les paramètres de configuration</span><span class="sxs-lookup"><span data-stu-id="413b4-115">Ability to upgrade to AGPM4.0 SP3 without re-entering configuration parameters</span></span>

<span data-ttu-id="413b4-116">Vous pouvez mettre à niveau le client AGPM ou le serveur AGPM vers AGPM 4.0 SP3 sans être invité à entrer de nouveau les paramètres de configuration (appelé mise à niveau intelligente) uniquement dans AGPM 4.0 et les versions ultérieures, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="413b4-116">You can upgrade the AGPM Client or AGPM Server to AGPM4.0 SP3 without being prompted to re-enter configuration parameters (called the Smart Upgrade) only from AGPM4.0 and later, as shown in the following table.</span></span> <span data-ttu-id="413b4-117">Si vous effectuez une mise à niveau vers AGPM 4.0 SP3 à partir d’autres versions d’AGPM, comme indiqué dans le tableau ci-dessous, vous devez utiliser la mise à niveau classique, qui nécessite d’entrer de nouveau les paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="413b4-117">If you are upgrading to AGPM4.0 SP3 from other versions of AGPM, as shown in the table, you must use the Classic Upgrade, which requires you to re-enter the configuration parameters.</span></span> <span data-ttu-id="413b4-118">Étant donné que chaque version d’AGPM est associée à un système d’exploitation spécifique, voir [choisir la version d’AGPM à installer](https://go.microsoft.com/fwlink/?LinkId=254350) et vérifier que vous effectuez une mise à niveau de votre système d’exploitation le cas échéant avant de procéder à la mise à niveau d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="413b4-118">Because each version of AGPM is associated with a particular operating system, see [Choosing Which Version of AGPM to Install](https://go.microsoft.com/fwlink/?LinkId=254350) and make sure that you upgrade your operating system as appropriate before you upgrade AGPM.</span></span>

**<span data-ttu-id="413b4-119">Mises à jour d’AGPM 4,0 SP3 prises en charge</span><span class="sxs-lookup"><span data-stu-id="413b4-119">AGPM 4.0 SP3 supported upgrades</span></span>**

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
<td align="left"><p><strong><span data-ttu-id="413b4-120">Version d’AGPM à partir de laquelle vous pouvez effectuer la mise à niveau</span><span class="sxs-lookup"><span data-stu-id="413b4-120">AGPM version from which you can upgrade</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="413b4-121">2,5</span><span class="sxs-lookup"><span data-stu-id="413b4-121">2.5</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="413b4-122">3,0</span><span class="sxs-lookup"><span data-stu-id="413b4-122">3.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="413b4-123">4,0</span><span class="sxs-lookup"><span data-stu-id="413b4-123">4.0</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="413b4-124">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="413b4-124">4.0 SP1</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="413b4-125">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="413b4-125">4.0 SP2</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="413b4-126">4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="413b4-126">4.0 SP3</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="413b4-127">2,5</span><span class="sxs-lookup"><span data-stu-id="413b4-127">2.5</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-128">Non applicable</span><span class="sxs-lookup"><span data-stu-id="413b4-128">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-129">Mise à niveau classique</span><span class="sxs-lookup"><span data-stu-id="413b4-129">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-130">Mise à niveau classique</span><span class="sxs-lookup"><span data-stu-id="413b4-130">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-131">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="413b4-131">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-132">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="413b4-132">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-133">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="413b4-133">Installation is blocked</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="413b4-134">3,0</span><span class="sxs-lookup"><span data-stu-id="413b4-134">3.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-135">Non applicable</span><span class="sxs-lookup"><span data-stu-id="413b4-135">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-136">Non applicable</span><span class="sxs-lookup"><span data-stu-id="413b4-136">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-137">Mise à niveau classique</span><span class="sxs-lookup"><span data-stu-id="413b4-137">Classic Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-138">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="413b4-138">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-139">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="413b4-139">Installation is blocked</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-140">L’installation est bloquée.</span><span class="sxs-lookup"><span data-stu-id="413b4-140">Installation is blocked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="413b4-141">4,0</span><span class="sxs-lookup"><span data-stu-id="413b4-141">4.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-142">Non applicable</span><span class="sxs-lookup"><span data-stu-id="413b4-142">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-143">Non applicable</span><span class="sxs-lookup"><span data-stu-id="413b4-143">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-144">Non applicable</span><span class="sxs-lookup"><span data-stu-id="413b4-144">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-145">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="413b4-145">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-146">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="413b4-146">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-147">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="413b4-147">Smart Upgrade</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="413b4-148">4,0 SP1</span><span class="sxs-lookup"><span data-stu-id="413b4-148">4.0 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-149">Non applicable</span><span class="sxs-lookup"><span data-stu-id="413b4-149">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-150">Non applicable</span><span class="sxs-lookup"><span data-stu-id="413b4-150">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-151">Non applicable</span><span class="sxs-lookup"><span data-stu-id="413b4-151">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-152">Non applicable</span><span class="sxs-lookup"><span data-stu-id="413b4-152">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-153">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="413b4-153">Smart Upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-154">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="413b4-154">Smart Upgrade</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="413b4-155">4,0 SP2</span><span class="sxs-lookup"><span data-stu-id="413b4-155">4.0 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-156">Non applicable</span><span class="sxs-lookup"><span data-stu-id="413b4-156">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-157">Non applicable</span><span class="sxs-lookup"><span data-stu-id="413b4-157">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-158">Non applicable</span><span class="sxs-lookup"><span data-stu-id="413b4-158">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-159">Non applicable</span><span class="sxs-lookup"><span data-stu-id="413b4-159">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-160">Non applicable</span><span class="sxs-lookup"><span data-stu-id="413b4-160">Not applicable</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-161">Mise à niveau intelligente</span><span class="sxs-lookup"><span data-stu-id="413b4-161">Smart Upgrade</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="413b4-162">Configurations prises en charge</span><span class="sxs-lookup"><span data-stu-id="413b4-162">Supported configurations</span></span>


<span data-ttu-id="413b4-163">AGPM 4.0 SP3 prend en charge les configurations figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="413b4-163">AGPM4.0 SP3 supports the configurations in the following table.</span></span> <span data-ttu-id="413b4-164">Bien qu’AGPM prenne en charge des configurations mixtes, nous vous recommandons vivement d’exécuter le client AGPM et le serveur AGPM sur la même ligne de système d’exploitation (par exemple, Windows 10 avec Windows Server 2016, Windows 8,1 avec Windows Server 2012 R2, etc.).</span><span class="sxs-lookup"><span data-stu-id="413b4-164">Although AGPM supports mixed configurations, we strongly recommend that you run the AGPM Client and AGPM Server on the same operating system line—for example, Windows10 with Windows Server 2016, Windows 8.1 with Windows Server 2012 R2, and so on.</span></span>

**<span data-ttu-id="413b4-165">Systèmes d’exploitation et systèmes d’exploitation pris en charge par AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="413b4-165">AGPM4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="413b4-166">Configurations prises en charge pour le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="413b4-166">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="413b4-167">Configurations prises en charge pour le client AGPM</span><span class="sxs-lookup"><span data-stu-id="413b4-167">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="413b4-168">Prise en charge d’AGPM</span><span class="sxs-lookup"><span data-stu-id="413b4-168">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="413b4-169">Windows Server 2016 ou Windows 10</span><span class="sxs-lookup"><span data-stu-id="413b4-169">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-170">Windows10</span><span class="sxs-lookup"><span data-stu-id="413b4-170">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-171">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="413b4-171">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="413b4-172">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="413b4-172">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-173">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="413b4-173">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-174">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="413b4-174">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="413b4-175">Windows Server2012 R2, Windows Server 2012 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="413b4-175">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-176">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="413b4-176">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-177">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="413b4-177">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="413b4-178">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="413b4-178">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-179">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="413b4-179">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-180">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="413b4-180">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="413b4-181">Windows Server 2012, Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="413b4-181">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-182">Windows Server 2008 ou Vista avec Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="413b4-182">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-183">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows</span><span class="sxs-lookup"><span data-stu-id="413b4-183">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="413b4-184">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="413b4-184">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-185">Windows Server 2012, Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="413b4-185">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-186">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="413b4-186">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="413b4-187">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="413b4-187">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-188">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="413b4-188">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="413b4-189">Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="413b4-189">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="413b4-190">Conditions préalables à l’installation d’AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="413b4-190">Prerequisites for installing AGPM4.0 SP3</span></span>

<span data-ttu-id="413b4-191">Le tableau suivant décrit le comportement d’AGPM 4.0 SP3 du client et du serveur lorsque .NET Framework 4.5.1, PowerShell 3,0 ou la console GPMC dans les outils d’administration de serveur distant est manquant.</span><span class="sxs-lookup"><span data-stu-id="413b4-191">The following table describes the behavior of AGPM4.0 SP3 Client and Server installers when the .NET Framework4.5.1, PowerShell 3.0, or the GPMC in the Remote Server Administration Tools is missing.</span></span>

| <span data-ttu-id="413b4-192">Client AGPM</span><span class="sxs-lookup"><span data-stu-id="413b4-192">AGPM Client</span></span>            |                                                                                                 |                                                                            | <span data-ttu-id="413b4-193">Serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="413b4-193">AGPM Server</span></span>                                                                     |                                                                                                 |                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="413b4-194">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="413b4-194">Operating system</span></span>       | <span data-ttu-id="413b4-195">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="413b4-195">.NET Framework</span></span>                                                                                  | <span data-ttu-id="413b4-196">PowerShell</span><span class="sxs-lookup"><span data-stu-id="413b4-196">PowerShell</span></span>                                                                 | <span data-ttu-id="413b4-197">Outils d'administration de serveur distant</span><span class="sxs-lookup"><span data-stu-id="413b4-197">Remote Server Administration Tools</span></span>                                              | <span data-ttu-id="413b4-198">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="413b4-198">.NET Framework</span></span>                                                                                  | <span data-ttu-id="413b4-199">Outils d'administration de serveur distant</span><span class="sxs-lookup"><span data-stu-id="413b4-199">Remote Server Administration Tools</span></span>                                              |
| <span data-ttu-id="413b4-200">Windows 10</span><span class="sxs-lookup"><span data-stu-id="413b4-200">Windows 10</span></span>             | <span data-ttu-id="413b4-201">Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="413b4-201">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="413b4-202">Si PowerShell 3,0 n’est pas installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="413b4-202">If Powershell 3.0 is not installed, the installer blocks the installation.</span></span> | <span data-ttu-id="413b4-203">Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="413b4-203">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="413b4-204">Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="413b4-204">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="413b4-205">Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="413b4-205">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> |
| <span data-ttu-id="413b4-206">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="413b4-206">Windows 8.1</span></span>            | <span data-ttu-id="413b4-207">Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="413b4-207">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="413b4-208">Si PowerShell 3,0 n’est pas installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="413b4-208">If Powershell 3.0 is not installed, the installer blocks the installation.</span></span> | <span data-ttu-id="413b4-209">Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="413b4-209">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="413b4-210">Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="413b4-210">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="413b4-211">Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="413b4-211">If the GPMC is not enabled or installed, the installer blocks the installation.</span></span> |
| <span data-ttu-id="413b4-212">WindowsServer2012R2</span><span class="sxs-lookup"><span data-stu-id="413b4-212">Windows Server 2012 R2</span></span> | <span data-ttu-id="413b4-213">Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="413b4-213">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="413b4-214">Si PowerShell 3,0 n’est pas installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="413b4-214">If Powershell 3.0 is not installed, the installer blocks the installation.</span></span> | <span data-ttu-id="413b4-215">Si la console GPMC n’est pas activée, le programme d’installation l’active au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="413b4-215">If the GPMC is not enabled, the installer enables it during the installation.</span></span>   | <span data-ttu-id="413b4-216">Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation.</span><span class="sxs-lookup"><span data-stu-id="413b4-216">If the .NET Framework 4.5.1 is not enabled or installed, the installer blocks the installation.</span></span> | <span data-ttu-id="413b4-217">Si la console GPMC n’est pas activée, le programme d’installation l’active au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="413b4-217">If the GPMC is not enabled, the installer enables it during the installation.</span></span>   |

 

## <span data-ttu-id="413b4-218">Obtention de technologies MDOP</span><span class="sxs-lookup"><span data-stu-id="413b4-218">How to Get MDOP Technologies</span></span>


<span data-ttu-id="413b4-219">Le pack d’optimisation du Bureau d’AGPM 4,0 est un composant de l’application MDOP 2015.</span><span class="sxs-lookup"><span data-stu-id="413b4-219">AGPM 4.0 SP3 is a part of the Microsoft Desktop Optimization Pack (MDOP) since MDOP 2015.</span></span> <span data-ttu-id="413b4-220">MDOP fait partie de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="413b4-220">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="413b4-221">Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="413b4-221">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="413b4-222">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="413b4-222">Related topics</span></span>


[<span data-ttu-id="413b4-223">Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="413b4-223">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="413b4-224">Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP3</span><span class="sxs-lookup"><span data-stu-id="413b4-224">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>](release-notes-for-microsoft-advanced-group-policy-management-40-sp3.md)

[<span data-ttu-id="413b4-225">Choix de la version d'AGPM à installer</span><span class="sxs-lookup"><span data-stu-id="413b4-225">Choosing Which Version of AGPM to Install</span></span>](choosing-which-version-of-agpm-to-install.md)

 

 





