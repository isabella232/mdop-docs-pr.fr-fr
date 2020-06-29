---
title: Choix de la version d'AGPM à installer
description: Choix de la version d'AGPM à installer
author: dansimp
ms.assetid: 31357d2a-bc23-4e15-93f4-0beda8ab7a7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/05/2017
ms.openlocfilehash: b09ea8161b6801c62552f1c0d0ef8455dc111e2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807770"
---
# <span data-ttu-id="72aa4-103">Choix de la version d'AGPM à installer</span><span class="sxs-lookup"><span data-stu-id="72aa4-103">Choosing Which Version of AGPM to Install</span></span>


<span data-ttu-id="72aa4-104">Chaque version de MicrosoftAdvanced de gestion des stratégies de groupe (AGPM) prend en charge des versions spécifiques du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-104">Each release of MicrosoftAdvanced Group Policy Management (AGPM) supports specific versions of the Windows operating system.</span></span> <span data-ttu-id="72aa4-105">Nous vous recommandons vivement d’exécuter le client AGPM et le serveur AGPM sur la même ligne de systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="72aa4-105">We strongly recommend that you run the AGPM Client and AGPM Server on the same line of operating systems.</span></span> <span data-ttu-id="72aa4-106">Par exemple, Windows 10 avec Windows Server 2016, Windows 8.1 avec Windows Server2012 R2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="72aa4-106">For example, Windows 10 with Windows Server 2016, Windows8.1 with Windows Server2012 R2, and so on.</span></span>

<span data-ttu-id="72aa4-107">Nous vous recommandons d’installer le serveur AGPM sur la version la plus récente du système d’exploitation dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="72aa4-107">We recommend that you install the AGPM Server on the most recent version of the operating system in the domain.</span></span> <span data-ttu-id="72aa4-108">AGPM utilise la console de gestion des stratégies de groupe (GPMC) pour sauvegarder et restaurer des objets de stratégie de groupe (GPO).</span><span class="sxs-lookup"><span data-stu-id="72aa4-108">AGPM uses the Group Policy Management Console (GPMC) to back up and restore Group Policy Objects (GPOs).</span></span> <span data-ttu-id="72aa4-109">Étant donné que les versions plus récentes de la console GPMC fournissent des paramètres de stratégie supplémentaires qui ne sont pas disponibles dans les versions antérieures, vous pouvez gérer d’autres paramètres de stratégie à l’aide de la version la plus récente du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="72aa4-109">Because newer versions of the GPMC provide additional policy settings that are not available in earlier versions, you can manage more policy settings by using the most recent version of the operating system.</span></span>

<span data-ttu-id="72aa4-110">Toutes les versions d’AGPM peuvent gérer uniquement les paramètres de stratégie qui ont été introduits dans la même version ou une version antérieure du système d’exploitation sur lequel AGPM s’exécute.</span><span class="sxs-lookup"><span data-stu-id="72aa4-110">All versions of AGPM can manage only the policy settings that were introduced in the same version or an earlier version of the operating system on which AGPM is running.</span></span> <span data-ttu-id="72aa4-111">Par exemple, si vous installez AGPM 4.0 SP2 sur Windows Server 2012, vous pouvez gérer les paramètres de stratégie qui ont été introduits dans Windows Server 2012 ou une version antérieure, mais vous ne pouvez pas gérer les paramètres de stratégie introduits plus tard, dans Windows 8.1 ou Windows Server2012 R2.</span><span class="sxs-lookup"><span data-stu-id="72aa4-111">For example, if you install AGPM4.0 SP2 on Windows Server 2012, you can manage policy settings that were introduced in Windows Server 2012 or earlier, but you cannot manage policy settings that were introduced later, in Windows8.1 or Windows Server2012 R2.</span></span>

<span data-ttu-id="72aa4-112">Si la version de GPMC sur votre serveur AGPM est antérieure à la version sur les ordinateurs utilisés par les administrateurs pour gérer la stratégie de groupe, le serveur AGPM ne sera pas en mesure de stocker des paramètres de stratégie qui ne sont pas disponibles dans l’ancienne version de GPMC.</span><span class="sxs-lookup"><span data-stu-id="72aa4-112">If the version of the GPMC on your AGPM Server is older than the version on the computers that administrators use to manage Group Policy, the AGPM Server will be unable to store any policy settings that are not available in the older version of the GPMC.</span></span> <span data-ttu-id="72aa4-113">Consultez la feuille de calcul des paramètres de stratégie de groupe inclus dans Windows dans [Référence des paramètres de stratégie de groupe pour Windows et Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span><span class="sxs-lookup"><span data-stu-id="72aa4-113">For a spreadsheet of Group Policy settings included in Windows, see [Group Policy Settings Reference for Windows and Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).</span></span>

## <span data-ttu-id="72aa4-114">AGPM 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="72aa4-114">AGPM4.0 SP3</span></span>


<span data-ttu-id="72aa4-115">Si vous utilisez un ordinateur exécutant Windows 10 pour gérer les objets de stratégie de groupe, vous devez utiliser le SP3 d’AGPM 4,0.</span><span class="sxs-lookup"><span data-stu-id="72aa4-115">If you are using computers that are running Windows 10 to manage GPOs, you must use AGPM 4.0 SP3.</span></span> <span data-ttu-id="72aa4-116">Vous ne pouvez pas installer les versions antérieures d’AGPM sur les ordinateurs qui exécutent le système d’exploitation Windows 10.</span><span class="sxs-lookup"><span data-stu-id="72aa4-116">You cannot install earlier versions of AGPM on computers that are running the Windows 10 operating system.</span></span>

<span data-ttu-id="72aa4-117">Le tableau 1 recense les systèmes d’exploitation sur lesquels vous pouvez installer AGPM 4.0 SP3 et les paramètres de stratégie que vous pouvez gérer à l’aide d’AGPM 4.0 SP3.</span><span class="sxs-lookup"><span data-stu-id="72aa4-117">Table 1 lists the operating systems on which you can install AGPM4.0 SP3, and the policy settings that you can manage by using AGPM4.0 SP3.</span></span>

**<span data-ttu-id="72aa4-118">Tableau 1: systèmes d’exploitation et paramètres de stratégie pris en charge par AGPM 4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="72aa4-118">Table 1: AGPM 4.0 SP3 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="72aa4-119">Configurations prises en charge pour le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="72aa4-119">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="72aa4-120">Configurations prises en charge pour le client AGPM</span><span class="sxs-lookup"><span data-stu-id="72aa4-120">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="72aa4-121">Prise en charge d’AGPM</span><span class="sxs-lookup"><span data-stu-id="72aa4-121">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72aa4-122">Windows Server 2016 ou Windows 10</span><span class="sxs-lookup"><span data-stu-id="72aa4-122">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-123">Windows Server 2016 ou Windows 10</span><span class="sxs-lookup"><span data-stu-id="72aa4-123">Windows Server 2016 or Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-124">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="72aa4-124">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72aa4-125">Windows Server2012 R2</span><span class="sxs-lookup"><span data-stu-id="72aa4-125">Windows Server2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-126">Windows 10</span><span class="sxs-lookup"><span data-stu-id="72aa4-126">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-127">Pris en charge avec les avertissements décrits dans <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"> KB 4015786</span><span class="sxs-lookup"><span data-stu-id="72aa4-127">Supported with the caveats outlined in <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)">KB 4015786</span></span></a>
</p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72aa4-128">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="72aa4-128">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-129">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="72aa4-129">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-130">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="72aa4-130">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72aa4-131">Windows Server2012 R2, Windows Server 2012 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="72aa4-131">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-132">Windows Server 2012 ou Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="72aa4-132">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-133">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="72aa4-133">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72aa4-134">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-134">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-135">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-135">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-136">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="72aa4-136">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72aa4-137">Windows Server 2012, Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-137">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-138">Windows Server 2008 ou Vista avec Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="72aa4-138">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-139">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows</span><span class="sxs-lookup"><span data-stu-id="72aa4-139">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72aa4-140">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-140">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-141">Windows Server 2012, Windows Server2008R2, Windows 8 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="72aa4-141">Windows Server 2012, Windows Server2008R2, Windows 8, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-142">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="72aa4-142">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72aa4-143">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-143">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-144">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-144">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-145">Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-145">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="72aa4-146">AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="72aa4-146">AGPM4.0 SP2</span></span>


<span data-ttu-id="72aa4-147">Si vous utilisez des ordinateurs exécutant Windows Server2012 R2 ou Windows 8.1 pour gérer les objets de stratégie de groupe, vous devez utiliser AGPM 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="72aa4-147">If you are using computers that are running Windows Server2012 R2 or Windows8.1 to manage GPOs, you must use AGPM4.0 SP2.</span></span> <span data-ttu-id="72aa4-148">Vous ne pouvez pas installer les versions antérieures d’AGPM sur les ordinateurs qui exécutent ces systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="72aa4-148">You cannot install earlier versions of AGPM on computers that are running those operating systems.</span></span>

<span data-ttu-id="72aa4-149">Le tableau 1 recense les systèmes d’exploitation sur lesquels vous pouvez installer AGPM 4.0 SP2 et les paramètres de stratégie que vous pouvez gérer à l’aide d’AGPM 4.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="72aa4-149">Table 1 lists the operating systems on which you can install AGPM4.0 SP2, and the policy settings that you can manage by using AGPM4.0 SP2.</span></span>

**<span data-ttu-id="72aa4-150">Tableau 2: systèmes d’exploitation et paramètres de stratégie pris en charge dans AGPM 4.0 SP2</span><span class="sxs-lookup"><span data-stu-id="72aa4-150">Table 2: AGPM4.0 SP2 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="72aa4-151">Configurations prises en charge pour le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="72aa4-151">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="72aa4-152">Configurations prises en charge pour le client AGPM</span><span class="sxs-lookup"><span data-stu-id="72aa4-152">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="72aa4-153">Prise en charge d’AGPM</span><span class="sxs-lookup"><span data-stu-id="72aa4-153">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72aa4-154">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="72aa4-154">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-155">Windows Server2012 R2 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="72aa4-155">Windows Server2012 R2 or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-156">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="72aa4-156">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72aa4-157">Windows Server2012 R2, Windows Server 2012 ou Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="72aa4-157">Windows Server2012 R2, Windows Server 2012, or Windows8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-158">Windows Server 2012 ou Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="72aa4-158">Windows Server 2012 or Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-159">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="72aa4-159">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72aa4-160">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-160">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-161">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-161">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-162">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="72aa4-162">Supported, but cannot edit policy settings or preference items that exist only in Windows8.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72aa4-163">Windows Server 2012, Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-163">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-164">Windows Server 2008 ou Vista avec Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="72aa4-164">Windows Server2008 or WindowsVista with Service Pack 1 (SP1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-165">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows</span><span class="sxs-lookup"><span data-stu-id="72aa4-165">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72aa4-166">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-166">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-167">Windows Server 2012, Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-167">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-168">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="72aa4-168">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72aa4-169">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-169">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-170">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-170">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-171">Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-171">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows8.1, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="72aa4-172">AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-172">AGPM4.0 SP1</span></span>


<span data-ttu-id="72aa4-173">Le tableau 2 répertorie les systèmes d’exploitation sur lesquels vous pouvez installer AGPM 4,0 SP1 et les paramètres de stratégie que vous pouvez gérer à l’aide d’AGPM 4.0 SP1.</span><span class="sxs-lookup"><span data-stu-id="72aa4-173">Table 2 lists the operating systems on which you can install AGPM 4.0 SP1, and the policy settings that you can manage by using AGPM4.0 SP1.</span></span>

**<span data-ttu-id="72aa4-174">Tableau 3: les systèmes d’exploitation et les paramètres de stratégie pris en charge dans AGPM 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-174">Table 3: AGPM4.0 SP1 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="72aa4-175">Configurations prises en charge pour le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="72aa4-175">Supported configurations for the AGPM Server</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="72aa4-176">Configurations prises en charge pour le client AGPM</span><span class="sxs-lookup"><span data-stu-id="72aa4-176">Supported configurations for the AGPM Client</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="72aa4-177">Prise en charge d’AGPM</span><span class="sxs-lookup"><span data-stu-id="72aa4-177">AGPM Support</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72aa4-178">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="72aa4-178">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-179">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="72aa4-179">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-180">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="72aa4-180">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72aa4-181">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-181">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-182">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-182">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-183">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="72aa4-183">Supported, but cannot edit policy settings or preference items that exist only in Windows 8.1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72aa4-184">Windows Server 2012, Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-184">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-185">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-185">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-186">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2008R2 ou une</span><span class="sxs-lookup"><span data-stu-id="72aa4-186">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72aa4-187">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-187">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-188">Windows Server 2012, Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-188">Windows Server 2012, Windows Server2008R2, or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-189">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="72aa4-189">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72aa4-190">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-190">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-191">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-191">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-192">Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2008R2 ou une icône</span><span class="sxs-lookup"><span data-stu-id="72aa4-192">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2, or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="72aa4-193">AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="72aa4-193">AGPM4.0</span></span>


<span data-ttu-id="72aa4-194">Le tableau 3 recense les systèmes d’exploitation sur lesquels vous pouvez installer AGPM 4,0 et les paramètres de stratégie que vous pouvez gérer à l’aide d’AGPM 4.0.</span><span class="sxs-lookup"><span data-stu-id="72aa4-194">Table 3 lists the operating systems on which you can install AGPM 4.0, and the policy settings that you can manage by using AGPM4.0.</span></span>

**<span data-ttu-id="72aa4-195">Tableau 4: systèmes d’exploitation pris en charge par AGPM 4.0 et paramètres de stratégie</span><span class="sxs-lookup"><span data-stu-id="72aa4-195">Table 4: AGPM4.0 supported operating systems and policy settings</span></span>**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72aa4-196">Systèmes d’exploitation pris en charge pour le serveur AGPM</span><span class="sxs-lookup"><span data-stu-id="72aa4-196">Supported operating systems for the AGPM Server</span></span></th>
<th align="left"><span data-ttu-id="72aa4-197">Systèmes d’exploitation pris en charge pour le client AGPM</span><span class="sxs-lookup"><span data-stu-id="72aa4-197">Supported operating systems for the AGPM Client</span></span></th>
<th align="left"><span data-ttu-id="72aa4-198">Prise en charge d’AGPM</span><span class="sxs-lookup"><span data-stu-id="72aa4-198">AGPM Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72aa4-199">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-199">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-200">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-200">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-201">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="72aa4-201">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72aa4-202">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-202">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-203">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-203">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-204">Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2008R2 ou la touche Windows</span><span class="sxs-lookup"><span data-stu-id="72aa4-204">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72aa4-205">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-205">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-206">Windows Server2008R2 ou Windows.</span><span class="sxs-lookup"><span data-stu-id="72aa4-206">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-207">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="72aa4-207">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72aa4-208">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-208">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-209">Windows Server 2008 ou Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-209">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-210">Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2008R2 ou une icône</span><span class="sxs-lookup"><span data-stu-id="72aa4-210">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="72aa4-211">Versions d’AGPM qui précèdent AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="72aa4-211">Versions of AGPM that precede AGPM4.0</span></span>


<span data-ttu-id="72aa4-212">Le tableau 4 répertorie les systèmes d’exploitation sur lesquels vous pouvez installer les versions d’AGPM qui précèdent AGPM 4.0.</span><span class="sxs-lookup"><span data-stu-id="72aa4-212">Table 4 lists the operating systems on which you can install the versions of AGPM that precede AGPM4.0.</span></span> <span data-ttu-id="72aa4-213">Si aucun système d’exploitation n’est répertorié, vous ne pouvez pas installer AGPM sur ce système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="72aa4-213">If an operating system is not listed, you cannot install AGPM on that operating system.</span></span>

**<span data-ttu-id="72aa4-214">Tableau 5: systèmes d’exploitation pris en charge pour les versions d’AGPM qui précèdent AGPM 4.0</span><span class="sxs-lookup"><span data-stu-id="72aa4-214">Table 5: Supported operating systems for versions of AGPM that precede AGPM4.0</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72aa4-215">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="72aa4-215">Operating system</span></span></th>
<th align="left"><span data-ttu-id="72aa4-216">Version d’AGPM qui peut être installée</span><span class="sxs-lookup"><span data-stu-id="72aa4-216">Version of AGPM that can be installed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72aa4-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72aa4-217">Windows Server2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-218">3,0</span><span class="sxs-lookup"><span data-stu-id="72aa4-218">3.0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72aa4-219">Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="72aa4-219">Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-220">3,0</span><span class="sxs-lookup"><span data-stu-id="72aa4-220">3.0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72aa4-221">Vista sans Service Pack (32)</span><span class="sxs-lookup"><span data-stu-id="72aa4-221">WindowsVista with no service pack installed (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-222">2,5</span><span class="sxs-lookup"><span data-stu-id="72aa4-222">2.5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72aa4-223">Windows Server2003 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="72aa4-223">Windows Server2003 (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="72aa4-224">2,5</span><span class="sxs-lookup"><span data-stu-id="72aa4-224">2.5</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="72aa4-225">Obtention de technologies MDOP</span><span class="sxs-lookup"><span data-stu-id="72aa4-225">How to Get MDOP Technologies</span></span>


<span data-ttu-id="72aa4-226">AGPM 4,0 SP2 fait partie du pack d’optimisation de bureau de Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="72aa4-226">AGPM 4.0 SP2 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="72aa4-227">MDOP fait partie de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="72aa4-227">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="72aa4-228">Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="72aa4-228">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="72aa4-229">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="72aa4-229">Related topics</span></span>


[<span data-ttu-id="72aa4-230">Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="72aa4-230">Advanced Group Policy Management</span></span>](index.md)

 

 





