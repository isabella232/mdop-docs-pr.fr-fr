---
title: Configurations prises en charge par MBAM1.0
description: Configurations prises en charge par MBAM1.0
author: dansimp
ms.assetid: 1f5ac58e-6a3f-47df-8a9b-4b57631ab9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2c72320379d1c9328a6b40537d37998402b1b38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811454"
---
# <span data-ttu-id="2ff12-103">Configurations prises en charge par MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="2ff12-103">MBAM 1.0 Supported Configurations</span></span>


<span data-ttu-id="2ff12-104">Cette rubrique spécifie les exigences nécessaires à l’installation et à l’exécution de Microsoft BitLocker administration et de la surveillance (MBAM) dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="2ff12-104">This topic specifies the necessary requirements to install and run Microsoft BitLocker Administration and Monitoring (MBAM) in your environment.</span></span>

## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="2ff12-105">Configuration système requise pour MBAM Server</span><span class="sxs-lookup"><span data-stu-id="2ff12-105">MBAM server system Requirements</span></span>


### <span data-ttu-id="2ff12-106">Configuration requise du système d’exploitation serveur</span><span class="sxs-lookup"><span data-stu-id="2ff12-106">Server operating system requirements</span></span>

<span data-ttu-id="2ff12-107">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du serveur d’administration et de surveillance de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2ff12-107">The following table lists the operating systems that are supported for the Microsoft BitLocker Administration and Monitoring Server installation.</span></span>

**<span data-ttu-id="2ff12-108">Remarque</span><span class="sxs-lookup"><span data-stu-id="2ff12-108">Note</span></span>**  
<span data-ttu-id="2ff12-109">Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent.</span><span class="sxs-lookup"><span data-stu-id="2ff12-109">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="2ff12-110">Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="2ff12-110">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="2ff12-111">Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="2ff12-111">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ff12-112">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="2ff12-112">Operating System</span></span></th>
<th align="left"><span data-ttu-id="2ff12-113">Édition</span><span class="sxs-lookup"><span data-stu-id="2ff12-113">Edition</span></span></th>
<th align="left"><span data-ttu-id="2ff12-114">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2ff12-114">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="2ff12-115">Architecture système</span><span class="sxs-lookup"><span data-stu-id="2ff12-115">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff12-116">WindowsServer2008</span><span class="sxs-lookup"><span data-stu-id="2ff12-116">Windows Server 2008</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-117">Standard, entreprise, Datacenter ou serveur Web</span><span class="sxs-lookup"><span data-stu-id="2ff12-117">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-118">SP2 uniquement</span><span class="sxs-lookup"><span data-stu-id="2ff12-118">SP2 only</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-119">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="2ff12-119">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ff12-120">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="2ff12-120">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-121">Standard, entreprise, Datacenter ou serveur Web</span><span class="sxs-lookup"><span data-stu-id="2ff12-121">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="2ff12-122">64 bits</span><span class="sxs-lookup"><span data-stu-id="2ff12-122">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="2ff12-123">Warning</span><span class="sxs-lookup"><span data-stu-id="2ff12-123">Warning</span></span>**  
<span data-ttu-id="2ff12-124">Il n’y a pas de prise en charge pour l’installation des services ou des rapports MBAM sur un ordinateur contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="2ff12-124">There is no support for installing MBAM services, reports, or databases on a domain controller computer.</span></span>



### <a href="" id="server-random-access-memory--ram--requirements-"></a><span data-ttu-id="2ff12-125">Configuration requise pour la mémoire RAM (Random Access Memory) du serveur</span><span class="sxs-lookup"><span data-stu-id="2ff12-125">Server random access memory (RAM) requirements</span></span>

<span data-ttu-id="2ff12-126">Il n’existe aucune exigence de RAM spécifique à l’installation de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="2ff12-126">There are no RAM requirements that are specific to MBAM Server installation.</span></span>

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="2ff12-127">Configuration requise pour la base de données SQL Server</span><span class="sxs-lookup"><span data-stu-id="2ff12-127">SQL Server Database requirements</span></span>

<span data-ttu-id="2ff12-128">Le tableau suivant répertorie les versions de SQL Server prises en charge pour l’installation de la fonctionnalité de serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="2ff12-128">The following table lists the SQL Server versions that are supported for the MBAM Server feature installation.</span></span>

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
<th align="left"><span data-ttu-id="2ff12-129">Fonctionnalité du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="2ff12-129">MBAM Server Feature</span></span></th>
<th align="left"><span data-ttu-id="2ff12-130">Version de SQL Server</span><span class="sxs-lookup"><span data-stu-id="2ff12-130">SQL Server Version</span></span></th>
<th align="left"><span data-ttu-id="2ff12-131">Édition</span><span class="sxs-lookup"><span data-stu-id="2ff12-131">Edition</span></span></th>
<th align="left"><span data-ttu-id="2ff12-132">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2ff12-132">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="2ff12-133">Architecture système</span><span class="sxs-lookup"><span data-stu-id="2ff12-133">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff12-134">Rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="2ff12-134">Compliance and Audit Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-135">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ff12-135">Microsoft SQL Server 2008</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2ff12-136">R2, standard, entreprise, Datacenter ou édition développeur</span><span class="sxs-lookup"><span data-stu-id="2ff12-136">R2, Standard, Enterprise, Datacenter, or Developer Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-137">SP2</span><span class="sxs-lookup"><span data-stu-id="2ff12-137">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-138">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="2ff12-138">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ff12-139">Base de données de récupération et de matériel</span><span class="sxs-lookup"><span data-stu-id="2ff12-139">Recovery and Hardware Database</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-140">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ff12-140">Microsoft SQL Server 2008</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2ff12-141">R2, entreprise, Datacenter ou édition développeur</span><span class="sxs-lookup"><span data-stu-id="2ff12-141">R2, Enterprise, Datacenter, or Developer Edition</span></span></p>
<div class="alert">
<strong><span data-ttu-id="2ff12-142">Important</span><span class="sxs-lookup"><span data-stu-id="2ff12-142">Important</span></span></strong><br/><p><span data-ttu-id="2ff12-143">Les éditions de SQL Server standard ne sont pas prises en charge pour l’installation de la fonctionnalité de restauration MBAM et de base de données matérielle.</span><span class="sxs-lookup"><span data-stu-id="2ff12-143">SQL Server Standard Editions are not supported for MBAM Recovery and Hardware Database Server feature installation.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="2ff12-144">SP2</span><span class="sxs-lookup"><span data-stu-id="2ff12-144">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-145">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="2ff12-145">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff12-146">Base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="2ff12-146">Compliance and Audit Database</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-147">Microsoft SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ff12-147">Microsoft SQL Server 2008</span></span> </p></td>
<td align="left"><p><span data-ttu-id="2ff12-148">R2, standard, entreprise, Datacenter ou édition développeur</span><span class="sxs-lookup"><span data-stu-id="2ff12-148">R2, Standard, Enterprise, Datacenter, or Developer Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-149">SP2</span><span class="sxs-lookup"><span data-stu-id="2ff12-149">SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-150">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="2ff12-150">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="2ff12-151">Configuration système requise pour le client MBAM</span><span class="sxs-lookup"><span data-stu-id="2ff12-151">MBAM Client system requirements</span></span>


### <span data-ttu-id="2ff12-152">Configuration requise du système d’exploitation client</span><span class="sxs-lookup"><span data-stu-id="2ff12-152">Client operating system requirements</span></span>

<span data-ttu-id="2ff12-153">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="2ff12-153">The following table lists the operating systems that are supported for MBAM Client installation.</span></span>

**<span data-ttu-id="2ff12-154">Remarque</span><span class="sxs-lookup"><span data-stu-id="2ff12-154">Note</span></span>**  
<span data-ttu-id="2ff12-155">Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent.</span><span class="sxs-lookup"><span data-stu-id="2ff12-155">Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="2ff12-156">Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="2ff12-156">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="2ff12-157">Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="2ff12-157">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ff12-158">Systèmed’exploitation</span><span class="sxs-lookup"><span data-stu-id="2ff12-158">Operating System</span></span></th>
<th align="left"><span data-ttu-id="2ff12-159">Édition</span><span class="sxs-lookup"><span data-stu-id="2ff12-159">Edition</span></span></th>
<th align="left"><span data-ttu-id="2ff12-160">Service Pack</span><span class="sxs-lookup"><span data-stu-id="2ff12-160">Service Pack</span></span></th>
<th align="left"><span data-ttu-id="2ff12-161">Architecture système</span><span class="sxs-lookup"><span data-stu-id="2ff12-161">System Architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ff12-162">Windows7</span><span class="sxs-lookup"><span data-stu-id="2ff12-162">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-163">Édition Entreprise</span><span class="sxs-lookup"><span data-stu-id="2ff12-163">Enterprise Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-164">Aucun, SP1</span><span class="sxs-lookup"><span data-stu-id="2ff12-164">None, SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-165">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="2ff12-165">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2ff12-166">Windows7</span><span class="sxs-lookup"><span data-stu-id="2ff12-166">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-167">Édition intégrale</span><span class="sxs-lookup"><span data-stu-id="2ff12-167">Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-168">Aucun, SP1</span><span class="sxs-lookup"><span data-stu-id="2ff12-168">None, SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ff12-169">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="2ff12-169">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="2ff12-170">Configuration requise pour le client RAM</span><span class="sxs-lookup"><span data-stu-id="2ff12-170">Client RAM requirements</span></span>

<span data-ttu-id="2ff12-171">Il n’existe aucune exigence de RAM spécifique à l’installation du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="2ff12-171">There are no RAM requirements that are specific to the MBAM Client installation.</span></span>

## <span data-ttu-id="2ff12-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ff12-172">Related topics</span></span>


[<span data-ttu-id="2ff12-173">Planification du déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="2ff12-173">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="2ff12-174">Conditions préalables au déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="2ff12-174">MBAM 1.0 Deployment Prerequisites</span></span>](mbam-10-deployment-prerequisites.md)









