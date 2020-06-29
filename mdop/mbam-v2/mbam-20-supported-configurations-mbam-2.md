---
title: Configurations prises en charge par MBAM2.0
description: Configurations prises en charge par MBAM2.0
author: dansimp
ms.assetid: dca63391-39fe-4273-a570-76d0a2f8a0fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8f314adcf818c1bdb17b0b239a7469f97fa849e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810236"
---
# <span data-ttu-id="ebfac-103">Configurations prises en charge par MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="ebfac-103">MBAM 2.0 Supported Configurations</span></span>


<span data-ttu-id="ebfac-104">Cette rubrique spécifie la configuration requise pour l’installation et l’exécution de Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 dans votre environnement via la topologie autonome.</span><span class="sxs-lookup"><span data-stu-id="ebfac-104">This topic specifies the requirements to install and run Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 in your environment by using the Stand-alone topology.</span></span> <span data-ttu-id="ebfac-105">Pour les configurations prises en charge qui s’appliquent aux versions ultérieures, consultez la documentation de la version en vigueur.</span><span class="sxs-lookup"><span data-stu-id="ebfac-105">For supported configurations that apply to later releases, see the documentation for the applicable release.</span></span>

<span data-ttu-id="ebfac-106">Si vous envisagez d’installer MBAM 2,0 à l’aide de la topologie de Configuration Manager et que vous souhaitez consulter une liste de la configuration système requise, voir [planification du déploiement d’MBAM avec Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="ebfac-106">If you plan to install MBAM 2.0 by using the Configuration Manager topology and want to review a list of the system requirements, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="ebfac-107">La configuration recommandée pour l’exécution de MBAM dans un environnement de production consiste à utiliser deux serveurs, en fonction de vos besoins en matière d’évolutivité.</span><span class="sxs-lookup"><span data-stu-id="ebfac-107">The recommended configuration for running MBAM in a production environment is with two servers, depending on your scalability requirements.</span></span> <span data-ttu-id="ebfac-108">Cette configuration prend en charge jusqu’à 200 000 clients MBAM.</span><span class="sxs-lookup"><span data-stu-id="ebfac-108">This configuration supports up to 200,000 MBAM clients.</span></span> <span data-ttu-id="ebfac-109">Pour obtenir une image et des descriptions de l’infrastructure de serveur MBAM autonome, voir [architecture de haut niveau pour MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="ebfac-109">For an image and descriptions of the Stand-alone MBAM server infrastructure, see [High-Level Architecture for MBAM 2.0](high-level-architecture-for-mbam-20-mbam-2.md).</span></span>

<span data-ttu-id="ebfac-110">**Remarques**  Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent.</span><span class="sxs-lookup"><span data-stu-id="ebfac-110">**Note** Microsoft provides support for the current service pack and, in some cases, the immediately preceding service pack.</span></span> <span data-ttu-id="ebfac-111">Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span><span class="sxs-lookup"><span data-stu-id="ebfac-111">To find the support timelines for your product, see the [Lifecycle Supported Service Packs](https://go.microsoft.com/fwlink/p/?LinkId=31975).</span></span> <span data-ttu-id="ebfac-112">Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span><span class="sxs-lookup"><span data-stu-id="ebfac-112">For additional information about Microsoft Support Lifecycle Policy, see [Microsoft Support Lifecycle Support Policy FAQ](https://go.microsoft.com/fwlink/p/?LinkId=31976).</span></span>

 

## <a href="" id="---------mbam-server-system-requirements"></a> <span data-ttu-id="ebfac-113">Configuration système requise pour MBAM Server</span><span class="sxs-lookup"><span data-stu-id="ebfac-113">MBAM Server System Requirements</span></span>


### <span data-ttu-id="ebfac-114">Configuration requise du système d’exploitation serveur</span><span class="sxs-lookup"><span data-stu-id="ebfac-114">Server Operating System Requirements</span></span>

<span data-ttu-id="ebfac-115">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du serveur d’administration et de surveillance de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ebfac-115">The following table lists the operating systems that are supported for the Microsoft BitLocker Administration and Monitoring Server installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ebfac-116">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ebfac-116">Operating system</span></span></th>
<th align="left"><span data-ttu-id="ebfac-117">Édition</span><span class="sxs-lookup"><span data-stu-id="ebfac-117">Edition</span></span></th>
<th align="left"><span data-ttu-id="ebfac-118">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ebfac-118">Service pack</span></span></th>
<th align="left"><span data-ttu-id="ebfac-119">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ebfac-119">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebfac-120">WindowsServer2008 R2</span><span class="sxs-lookup"><span data-stu-id="ebfac-120">WindowsServer2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-121">Éditions standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ebfac-121">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-122">SP1</span><span class="sxs-lookup"><span data-stu-id="ebfac-122">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-123">64 bits</span><span class="sxs-lookup"><span data-stu-id="ebfac-123">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebfac-124">WindowsServer2012</span><span class="sxs-lookup"><span data-stu-id="ebfac-124">WindowsServer2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-125">Edition standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ebfac-125">Standard or Datacenter Edition</span></span></p></td>
<td align="left"></td>
<td align="left"><p><span data-ttu-id="ebfac-126">64 bits</span><span class="sxs-lookup"><span data-stu-id="ebfac-126">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ebfac-127">**Remarques**  Il n’y a pas de prise en charge pour l’installation des services ou des rapports MBAM sur un ordinateur contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="ebfac-127">**Note** There is no support for installing MBAM services, reports, or databases on a domain controller computer.</span></span>

 

### <a href="" id="server-processor--ram--and-disk-space-requirements-"></a><span data-ttu-id="ebfac-128">Exigences relatives au processeur du serveur, à la RAM et à l’espace disque</span><span class="sxs-lookup"><span data-stu-id="ebfac-128">Server Processor, RAM, and Disk Space Requirements</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ebfac-129">Composant matériel</span><span class="sxs-lookup"><span data-stu-id="ebfac-129">Hardware component</span></span></th>
<th align="left"><span data-ttu-id="ebfac-130">Configuration minimale</span><span class="sxs-lookup"><span data-stu-id="ebfac-130">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="ebfac-131">Configuration recommandée</span><span class="sxs-lookup"><span data-stu-id="ebfac-131">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebfac-132">Processeur</span><span class="sxs-lookup"><span data-stu-id="ebfac-132">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-133">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="ebfac-133">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-134">2,33 GHz ou supérieur</span><span class="sxs-lookup"><span data-stu-id="ebfac-134">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebfac-135">Mémoire vive (RAM)</span><span class="sxs-lookup"><span data-stu-id="ebfac-135">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-136">8 GO</span><span class="sxs-lookup"><span data-stu-id="ebfac-136">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-137">12 GO</span><span class="sxs-lookup"><span data-stu-id="ebfac-137">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebfac-138">Espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="ebfac-138">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-139">1 Go</span><span class="sxs-lookup"><span data-stu-id="ebfac-139">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-140">2 Go</span><span class="sxs-lookup"><span data-stu-id="ebfac-140">2 GB</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="sql-server-database-requirements-"></a><span data-ttu-id="ebfac-141">Configuration requise pour la base de données SQLServer</span><span class="sxs-lookup"><span data-stu-id="ebfac-141">SQLServer Database Requirements</span></span>

<span data-ttu-id="ebfac-142">Le tableau suivant répertorie les versions de SQLServer qui sont prises en charge pour l’installation de la fonctionnalité serveur d’administration et de surveillance, qui inclut la base de données de récupération, la base de données d’audit et de conformité, ainsi que les rapports d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="ebfac-142">The following table lists the SQLServer versions that are supported for the Administration and Monitoring Server feature installation, which includes the Recovery Database, Compliance and Audit Database, and Compliance and Audit Reports.</span></span> <span data-ttu-id="ebfac-143">Les bases de données requièrent également l’installation des outils de gestion SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ebfac-143">The databases additionally require the installation of SQL Server Management Tools.</span></span>

<span data-ttu-id="ebfac-144">**Remarques**  MBAM ne prend pas en charge les groupes de disponibilité ou de mise en miroir SQL.</span><span class="sxs-lookup"><span data-stu-id="ebfac-144">**Note** MBAM does not natively support SQL clustering, mirroring, or Availability Groups.</span></span> <span data-ttu-id="ebfac-145">Pour installer les bases de données, vous devez exécuter l’installation MBAM Server sur un serveur SQL autonome.</span><span class="sxs-lookup"><span data-stu-id="ebfac-145">To install the databases, you must run the MBAM Server installation on a stand-alone SQL server.</span></span>

 

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ebfac-146">Version de SQL Server</span><span class="sxs-lookup"><span data-stu-id="ebfac-146">SQL Server version</span></span></th>
<th align="left"><span data-ttu-id="ebfac-147">Édition</span><span class="sxs-lookup"><span data-stu-id="ebfac-147">Edition</span></span></th>
<th align="left"><span data-ttu-id="ebfac-148">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ebfac-148">Service pack</span></span></th>
<th align="left"><span data-ttu-id="ebfac-149">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ebfac-149">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebfac-150">MicrosoftSQLServer2008 R2</span><span class="sxs-lookup"><span data-stu-id="ebfac-150">MicrosoftSQLServer2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-151">Éditions standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ebfac-151">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-152">SP1</span><span class="sxs-lookup"><span data-stu-id="ebfac-152">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-153">64 bits</span><span class="sxs-lookup"><span data-stu-id="ebfac-153">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebfac-154">MicrosoftSQLServer2012</span><span class="sxs-lookup"><span data-stu-id="ebfac-154">MicrosoftSQLServer2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-155">Éditions standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ebfac-155">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-156">SP1</span><span class="sxs-lookup"><span data-stu-id="ebfac-156">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-157">64 bits</span><span class="sxs-lookup"><span data-stu-id="ebfac-157">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ebfac-158">Composant matériel</span><span class="sxs-lookup"><span data-stu-id="ebfac-158">Hardware component</span></span></th>
<th align="left"><span data-ttu-id="ebfac-159">Configuration minimale</span><span class="sxs-lookup"><span data-stu-id="ebfac-159">Minimum requirement</span></span></th>
<th align="left"><span data-ttu-id="ebfac-160">Configuration recommandée</span><span class="sxs-lookup"><span data-stu-id="ebfac-160">Recommended requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebfac-161">Processeur</span><span class="sxs-lookup"><span data-stu-id="ebfac-161">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-162">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="ebfac-162">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-163">2,33 GHz ou supérieur</span><span class="sxs-lookup"><span data-stu-id="ebfac-163">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebfac-164">Mémoire vive (RAM)</span><span class="sxs-lookup"><span data-stu-id="ebfac-164">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-165">8 GO</span><span class="sxs-lookup"><span data-stu-id="ebfac-165">8 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-166">12 GO</span><span class="sxs-lookup"><span data-stu-id="ebfac-166">12 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebfac-167">Espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="ebfac-167">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-168">5 GO</span><span class="sxs-lookup"><span data-stu-id="ebfac-168">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-169">5 Go minimum</span><span class="sxs-lookup"><span data-stu-id="ebfac-169">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-client-system-requirements"></a> <span data-ttu-id="ebfac-170">Configuration système requise pour le client MBAM</span><span class="sxs-lookup"><span data-stu-id="ebfac-170">MBAM Client System Requirements</span></span>


### <span data-ttu-id="ebfac-171">Configuration requise du système d’exploitation client</span><span class="sxs-lookup"><span data-stu-id="ebfac-171">Client Operating System Requirements</span></span>

<span data-ttu-id="ebfac-172">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client de gestion et de contrôle BitLocker de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ebfac-172">The following table lists the operating systems that are supported for Microsoft BitLocker Administration and Monitoring Client installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ebfac-173">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ebfac-173">Operating system</span></span></th>
<th align="left"><span data-ttu-id="ebfac-174">Édition</span><span class="sxs-lookup"><span data-stu-id="ebfac-174">Edition</span></span></th>
<th align="left"><span data-ttu-id="ebfac-175">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ebfac-175">Service pack</span></span></th>
<th align="left"><span data-ttu-id="ebfac-176">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ebfac-176">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebfac-177">Plus de.</span><span class="sxs-lookup"><span data-stu-id="ebfac-177">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-178">Edition entreprise ou édition intégrale</span><span class="sxs-lookup"><span data-stu-id="ebfac-178">Enterprise or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-179">SP1</span><span class="sxs-lookup"><span data-stu-id="ebfac-179">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-180">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ebfac-180">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebfac-181">Windows8</span><span class="sxs-lookup"><span data-stu-id="ebfac-181">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-182">Édition Entreprise</span><span class="sxs-lookup"><span data-stu-id="ebfac-182">Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ebfac-183">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ebfac-183">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebfac-184">WindowsToGo</span><span class="sxs-lookup"><span data-stu-id="ebfac-184">Windows To Go</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-185">Windows 8 entreprise Edition</span><span class="sxs-lookup"><span data-stu-id="ebfac-185">Windows 8 Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ebfac-186">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ebfac-186">32-bit or 64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="client-ram-requirements-"></a><span data-ttu-id="ebfac-187">Configuration requise pour le client RAM</span><span class="sxs-lookup"><span data-stu-id="ebfac-187">Client RAM Requirements</span></span>

<span data-ttu-id="ebfac-188">Il n’existe aucune exigence de mémoire RAM spécifique à l’installation du client d’administration et de surveillance de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ebfac-188">There are no RAM requirements that are specific to the Microsoft BitLocker Administration and Monitoring Client installation.</span></span>

## <a href="" id="---------mbam-group-policy-system-requirements"></a> <span data-ttu-id="ebfac-189">Configuration système requise pour la stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="ebfac-189">MBAM Group Policy System Requirements</span></span>


<span data-ttu-id="ebfac-190">Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de l’administration et du modèle de stratégie de groupe Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ebfac-190">The following table lists the operating systems that are supported for Microsoft BitLocker Administration and Monitoring Group Policy template installation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ebfac-191">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ebfac-191">Operating system</span></span></th>
<th align="left"><span data-ttu-id="ebfac-192">Édition</span><span class="sxs-lookup"><span data-stu-id="ebfac-192">Edition</span></span></th>
<th align="left"><span data-ttu-id="ebfac-193">Service Pack</span><span class="sxs-lookup"><span data-stu-id="ebfac-193">Service pack</span></span></th>
<th align="left"><span data-ttu-id="ebfac-194">Architecture système</span><span class="sxs-lookup"><span data-stu-id="ebfac-194">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebfac-195">Plus de.</span><span class="sxs-lookup"><span data-stu-id="ebfac-195">Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-196">Edition entreprise ou édition intégrale</span><span class="sxs-lookup"><span data-stu-id="ebfac-196">Enterprise, or Ultimate Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-197">SP1</span><span class="sxs-lookup"><span data-stu-id="ebfac-197">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-198">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ebfac-198">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebfac-199">Windows8</span><span class="sxs-lookup"><span data-stu-id="ebfac-199">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-200">Édition Entreprise</span><span class="sxs-lookup"><span data-stu-id="ebfac-200">Enterprise Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ebfac-201">32bits ou 64bits</span><span class="sxs-lookup"><span data-stu-id="ebfac-201">32-bit or 64-bit</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ebfac-202">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="ebfac-202">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-203">Éditions standard, Enterprise ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ebfac-203">Standard, Enterprise, or Datacenter Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-204">SP1</span><span class="sxs-lookup"><span data-stu-id="ebfac-204">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-205">64 bits</span><span class="sxs-lookup"><span data-stu-id="ebfac-205">64-bit</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ebfac-206">Windows Server2012</span><span class="sxs-lookup"><span data-stu-id="ebfac-206">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="ebfac-207">Edition standard ou Datacenter</span><span class="sxs-lookup"><span data-stu-id="ebfac-207">Standard or Datacenter Edition</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="ebfac-208">64 bits</span><span class="sxs-lookup"><span data-stu-id="ebfac-208">64-bit</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="ebfac-209">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ebfac-209">Related topics</span></span>


[<span data-ttu-id="ebfac-210">Planification du déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="ebfac-210">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="ebfac-211">Conditions préalables au déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="ebfac-211">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)

 

 





