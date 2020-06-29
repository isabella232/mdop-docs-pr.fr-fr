---
title: Planification du déploiement de MBAM avec Configuration Manager
description: Planification du déploiement de MBAM avec Configuration Manager
author: dansimp
ms.assetid: fb768306-48c2-40b4-ac4e-c279db987391
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e8588ce03c86a8a5138d591327e5f95503dce5ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811268"
---
# <span data-ttu-id="8ef03-103">Planification du déploiement de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-103">Planning to Deploy MBAM with Configuration Manager</span></span>


<span data-ttu-id="8ef03-104">Pour déployer MBAM avec la topologie Configuration Manager, il est recommandé d’utiliser une architecture à trois serveurs qui prend en charge les clients 200 000.</span><span class="sxs-lookup"><span data-stu-id="8ef03-104">To deploy MBAM with the Configuration Manager topology, a three-server architecture, which supports 200,000 clients, is recommended.</span></span> <span data-ttu-id="8ef03-105">Utilisez un serveur distinct pour exécuter Configuration Manager, puis installez les fonctionnalités d’administration et de surveillance de base sur deux serveurs, comme indiqué dans l’image d’architecture de la rubrique [mise en route de l’utilisation de MBAM avec Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="8ef03-105">Use a separate server to run Configuration Manager, and install the basic Administration and Monitoring features on two servers, as shown in the architecture image in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span>

**<span data-ttu-id="8ef03-106">Important</span><span class="sxs-lookup"><span data-stu-id="8ef03-106">Important</span></span>**  
<span data-ttu-id="8ef03-107">Windows to Go n’est pas pris en charge lorsque vous installez la topologie intégrée de MBAM avec Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="8ef03-107">Windows To Go is not supported when you install the integrated topology of MBAM with Configuration Manager 2007.</span></span>



## <span data-ttu-id="8ef03-108">Prérequis de déploiement pour l’installation d’MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-108">Deployment Prerequisites for Installing MBAM with Configuration Manager</span></span>


<span data-ttu-id="8ef03-109">Vérifiez que vous remplissez les conditions préalables suivantes avant d’installer MBAM avec Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="8ef03-109">Ensure that you have met the following prerequisites before you install MBAM with Configuration Manager:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8ef03-110">Prérequises</span><span class="sxs-lookup"><span data-stu-id="8ef03-110">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="8ef03-111">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="8ef03-111">Additional Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ef03-112">Assurez-vous que le serveur Configuration Manager est un site principal dans le système Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8ef03-112">Ensure that the Configuration Manager Server is a primary site in the Configuration Manager system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-113">N/A</span><span class="sxs-lookup"><span data-stu-id="8ef03-113">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8ef03-114">Activez l’agent client d’inventaire matériel sur le serveur Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8ef03-114">Enable the Hardware Inventory Client Agent on the Configuration Manager Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-115">Pour Configuration Manager 2007, voir <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> Comment configurer l’inventaire matériel d’un site </a> .</span><span class="sxs-lookup"><span data-stu-id="8ef03-115">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)">How to Configure Hardware Inventory for a Site</a>.</span></span></p>
<p><span data-ttu-id="8ef03-116">Pour le gestionnaire de configuration de System Center 2012, voir <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> Comment configurer l’inventaire matériel dans Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="8ef03-116">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)">How to Configure Hardware Inventory in Configuration Manager</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ef03-117">Activez l’agent de gestion de la configuration (DCM) souhaité ou les paramètres de conformité, en fonction de la version de Configuration Manager que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="8ef03-117">Enable the Desired Configuration Management (DCM) agent or the compliance settings, depending on the version of Configuration Manager that you are using.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-118">Pour Configuration Manager 2007, activez les propriétés de l' <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> agent client de gestion de la configuration souhaitées </a> .</span><span class="sxs-lookup"><span data-stu-id="8ef03-118">For Configuration Manager 2007, enable the see <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)">Desired Configuration Management Client Agent Properties</a>.</span></span></p>
<p><span data-ttu-id="8ef03-119">Pour System Center 2012 Configuration Manager, consultez <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> la rubrique Configuration des paramètres de conformité dans Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="8ef03-119">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)">Configuring Compliance Settings in Configuration Manager</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8ef03-120">Définissez un point Report services dans Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8ef03-120">Define a reporting services point in Configuration Manager.</span></span> <span data-ttu-id="8ef03-121">Requis pour les services de rapport SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8ef03-121">Required for SQL Reporting Services.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-122">Pour Configuration Manager 2007, voir <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> création d’un point de Reporting Services pour SQL Reporting Services </a> .</span><span class="sxs-lookup"><span data-stu-id="8ef03-122">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)">How to Create a Reporting Services Point for SQL Reporting Services</a>.</span></span></p>
<p><span data-ttu-id="8ef03-123">Pour le gestionnaire de configuration de System Center 2012, voir la configuration <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> requise pour la création de rapports dans Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="8ef03-123">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)">Prerequisites for Reporting in Configuration Manager</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------configuration-manager-supported-versions"></a> <span data-ttu-id="8ef03-124">Versions prises en charge par Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-124">Configuration Manager Supported Versions</span></span>


<span data-ttu-id="8ef03-125">MBAM prend en charge les versions suivantes de Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="8ef03-125">MBAM supports the following versions of Configuration Manager:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8ef03-126">Version prise en charge</span><span class="sxs-lookup"><span data-stu-id="8ef03-126">Supported version</span></span></th>
<th align="left"><span data-ttu-id="8ef03-127">Service Pack</span><span class="sxs-lookup"><span data-stu-id="8ef03-127">Service pack</span></span></th>
<th align="left"><span data-ttu-id="8ef03-128">Architecture système</span><span class="sxs-lookup"><span data-stu-id="8ef03-128">System architecture</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ef03-129">Microsoft System Center Configuration Manager 2007 R2</span><span class="sxs-lookup"><span data-stu-id="8ef03-129">Microsoft System Center Configuration Manager 2007 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-130">SP1 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8ef03-130">SP1 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-131">64 bits</span><span class="sxs-lookup"><span data-stu-id="8ef03-131">64-bit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8ef03-132">Remarque</span><span class="sxs-lookup"><span data-stu-id="8ef03-132">Note</span></span></strong><br/><p><span data-ttu-id="8ef03-133">Même si Configuration Manager 2007 est 32 bits, vous devez l’installer et SQL Server sur un système d’exploitation 64 bits afin de correspondre au logiciel MBAM 64.</span><span class="sxs-lookup"><span data-stu-id="8ef03-133">Although Configuration Manager 2007 is 32 bit, you must install it and SQL Server on a 64-bit operating system in order to match the 64-bit MBAM software.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8ef03-134">Gestionnaire de configuration de Microsoft System Center 2012</span><span class="sxs-lookup"><span data-stu-id="8ef03-134">Microsoft System Center 2012 Configuration Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-135">SP1</span><span class="sxs-lookup"><span data-stu-id="8ef03-135">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-136">64 bits</span><span class="sxs-lookup"><span data-stu-id="8ef03-136">64-bit</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="8ef03-137">Pour obtenir la liste des configurations prises en charge pour le serveur Configuration Manager, consultez la page Web appropriée pour la version de Configuration Manager que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="8ef03-137">For a list of supported configurations for the Configuration Manager Server, see the appropriate webpage for the version of Configuration Manager that you are using.</span></span> <span data-ttu-id="8ef03-138">MBAM ne possède aucune configuration système supplémentaire pour le serveur Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8ef03-138">MBAM has no additional system requirements for the Configuration Manager Server.</span></span>

## <a href="" id="---------mbam-and-sql-server-system-requirements"></a> <span data-ttu-id="8ef03-139">Configuration système requise pour MBAM et SQL Server</span><span class="sxs-lookup"><span data-stu-id="8ef03-139">MBAM and SQL Server System Requirements</span></span>


<span data-ttu-id="8ef03-140">Les configurations prises en charge et la configuration système requise pour les serveurs MBAM et SQL Server pour la topologie de Configuration Manager sont les mêmes que celles de la topologie autonome.</span><span class="sxs-lookup"><span data-stu-id="8ef03-140">The supported configurations and system requirements for the MBAM servers and SQL Server for the Configuration Manager topology are the same as those for the Stand-alone topology.</span></span> <span data-ttu-id="8ef03-141">Pour la configuration système autonome requise, voir [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="8ef03-141">For the Stand-alone system requirements, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span> <span data-ttu-id="8ef03-142">Pour le serveur MBAM et le processeur SQL Server, la RAM et l’espace disque requis pour la topologie Configuration Manager, consultez les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="8ef03-142">For the MBAM Server and SQL Server processor, RAM, and disk space requirements for the Configuration Manager topology, see the following sections.</span></span>

## <span data-ttu-id="8ef03-143">MBAM, RAM et espace disque requis pour MBAM</span><span class="sxs-lookup"><span data-stu-id="8ef03-143">MBAM Server Processor, RAM, and Disk Space Requirements for MBAM</span></span>


<span data-ttu-id="8ef03-144">Le tableau suivant répertorie les conditions requises processeur de serveur, RAM et espace disque pour les serveurs MBAM lorsque vous utilisez la topologie d’intégration de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8ef03-144">The following table lists the server processor, RAM, and disk space requirements for MBAM servers when you are using the Configuration Manager Integration topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8ef03-145">Composant matériel</span><span class="sxs-lookup"><span data-stu-id="8ef03-145">Hardware Component</span></span></th>
<th align="left"><span data-ttu-id="8ef03-146">Configuration minimale</span><span class="sxs-lookup"><span data-stu-id="8ef03-146">Minimum Requirement</span></span></th>
<th align="left"><span data-ttu-id="8ef03-147">Configuration recommandée</span><span class="sxs-lookup"><span data-stu-id="8ef03-147">Recommended Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ef03-148">Processeur</span><span class="sxs-lookup"><span data-stu-id="8ef03-148">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-149">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="8ef03-149">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-150">2,33 GHz ou supérieur</span><span class="sxs-lookup"><span data-stu-id="8ef03-150">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8ef03-151">Mémoire vive (RAM)</span><span class="sxs-lookup"><span data-stu-id="8ef03-151">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-152">4 Go</span><span class="sxs-lookup"><span data-stu-id="8ef03-152">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-153">8 GO</span><span class="sxs-lookup"><span data-stu-id="8ef03-153">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ef03-154">Espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="8ef03-154">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-155">1 Go</span><span class="sxs-lookup"><span data-stu-id="8ef03-155">1 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-156">2 Go</span><span class="sxs-lookup"><span data-stu-id="8ef03-156">2 GB</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8ef03-157">Configuration requise pour le processeur SQL Server, la RAM et l’espace disque</span><span class="sxs-lookup"><span data-stu-id="8ef03-157">SQL Server Processor, RAM, and Disk Space Requirements</span></span>


<span data-ttu-id="8ef03-158">Le tableau suivant répertorie les exigences relatives au processeur du serveur, à la RAM et à l’espace disque pour l’ordinateur SQL Server lorsque vous utilisez la topologie d’intégration de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8ef03-158">The following table lists the server processor, RAM, and disk space requirements for the SQL Server computer when you are using the Configuration Manager Integration topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8ef03-159">Composant matériel</span><span class="sxs-lookup"><span data-stu-id="8ef03-159">Hardware Component</span></span></th>
<th align="left"><span data-ttu-id="8ef03-160">Configuration minimale</span><span class="sxs-lookup"><span data-stu-id="8ef03-160">Minimum Requirement</span></span></th>
<th align="left"><span data-ttu-id="8ef03-161">Configuration recommandée</span><span class="sxs-lookup"><span data-stu-id="8ef03-161">Recommended Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ef03-162">Processeur</span><span class="sxs-lookup"><span data-stu-id="8ef03-162">Processor</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-163">2,33 GHz</span><span class="sxs-lookup"><span data-stu-id="8ef03-163">2.33 GHz</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-164">2,33 GHz ou supérieur</span><span class="sxs-lookup"><span data-stu-id="8ef03-164">2.33 GHz or greater</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8ef03-165">Mémoire vive (RAM)</span><span class="sxs-lookup"><span data-stu-id="8ef03-165">RAM</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-166">4 Go</span><span class="sxs-lookup"><span data-stu-id="8ef03-166">4 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-167">8 GO</span><span class="sxs-lookup"><span data-stu-id="8ef03-167">8 GB</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ef03-168">Espace disque disponible</span><span class="sxs-lookup"><span data-stu-id="8ef03-168">Free disk space</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-169">5 GO</span><span class="sxs-lookup"><span data-stu-id="8ef03-169">5 GB</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-170">5 Go minimum</span><span class="sxs-lookup"><span data-stu-id="8ef03-170">5 GB or greater</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8ef03-171">Autorisations requises pour installer le serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="8ef03-171">Required permissions to install the MBAM Server</span></span>


<span data-ttu-id="8ef03-172">Pour installer MBAM avec Configuration Manager, vous devez disposer d’un utilisateur administratif dans Configuration Manager ayant un rôle de sécurité avec les autorisations minimales indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8ef03-172">To install MBAM with Configuration Manager, you must have an administrative user in Configuration Manager who has a security role with the minimum permissions listed in the following table.</span></span> <span data-ttu-id="8ef03-173">Le tableau ci-dessous indique également les droits dont vous avez besoin au-delà des droits d’administrateur d’ordinateur de base pour installer le serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="8ef03-173">The table also shows the rights that you must have, beyond basic computer administrator rights, to install the MBAM Server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8ef03-174">Autorisations</span><span class="sxs-lookup"><span data-stu-id="8ef03-174">Permissions</span></span></th>
<th align="left"><span data-ttu-id="8ef03-175">Fonctionnalité du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="8ef03-175">MBAM Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ef03-176">Rôles de serveurs de connexion d’instances SQL:-dbcreator-processadmin</span><span class="sxs-lookup"><span data-stu-id="8ef03-176">SQL instance Login Server Roles: - dbcreator- processadmin</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="8ef03-177">Base de données de récupération-base de données d’audit</span><span class="sxs-lookup"><span data-stu-id="8ef03-177">Recovery Database- Audit Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8ef03-178">Droits d’instance SQL Server Reporting Services:-créer des dossiers-publier des rapports</span><span class="sxs-lookup"><span data-stu-id="8ef03-178">SQL Server Reporting Services instance rights: - Create Folders- Publish Reports</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="8ef03-179">Intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-179">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="8ef03-180">System Center2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-180">System Center 2012 Configuration Manager</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8ef03-181">Autorisations</span><span class="sxs-lookup"><span data-stu-id="8ef03-181">Permissions</span></span></th>
<th align="left"><span data-ttu-id="8ef03-182">Fonctionnalité serveur Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-182">Configuration Manager Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ef03-183">Droits de site Configuration Manager:-lecture</span><span class="sxs-lookup"><span data-stu-id="8ef03-183">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-184">Intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-184">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8ef03-185">Droits de collection de Configuration Manager:-création-suppression-lecture-modification-déploiement des éléments de configuration</span><span class="sxs-lookup"><span data-stu-id="8ef03-185">Configuration Manager collection rights: - Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-186">Intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-186">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ef03-187">Configuration des éléments de configuration de Configuration Manager:-création-suppression-lecture</span><span class="sxs-lookup"><span data-stu-id="8ef03-187">Configuration Manager configuration item rights: - Create- Delete- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-188">Intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-188">System Center Configuration Manager integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="8ef03-189">Gestionnaire de configuration 2007</span><span class="sxs-lookup"><span data-stu-id="8ef03-189">Configuration Manager 2007</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8ef03-190">Autorisations</span><span class="sxs-lookup"><span data-stu-id="8ef03-190">Permissions</span></span></th>
<th align="left"><span data-ttu-id="8ef03-191">Fonctionnalité serveur Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-191">Configuration Manager Server Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ef03-192">Droits de site Configuration Manager:-lecture</span><span class="sxs-lookup"><span data-stu-id="8ef03-192">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-193">Intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-193">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8ef03-194">Droits de collection de Configuration Manager:-création-suppression-lecture-ReadResource</span><span class="sxs-lookup"><span data-stu-id="8ef03-194">Configuration Manager collection rights: - Create- Delete- Read- ReadResource</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-195">Intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-195">System Center Configuration Manager integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8ef03-196">Configuration des éléments de configuration de Configuration Manager:-création-suppression-lecture/distribution</span><span class="sxs-lookup"><span data-stu-id="8ef03-196">Configuration Manager configuration item rights: - Create- Delete- Read- Distribute</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-197">Intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-197">System Center Configuration Manager integration</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8ef03-198">Ordre de déploiement des fonctionnalités MBAM pour la topologie de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-198">Order of Deployment of MBAM Features for the Configuration Manager Topology</span></span>


<span data-ttu-id="8ef03-199">Lors du déploiement de MBAM sur le serveur Configuration Manager, vous devez effectuer les tâches de déploiement dans l’ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="8ef03-199">When deploying MBAM on the Configuration Manager Server, you must complete the deployment tasks in the following order:</span></span>

1.  <span data-ttu-id="8ef03-200">Modifiez le fichier Configuration. mof sur le serveur Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8ef03-200">Edit the configuration.mof file on the Configuration Manager Server.</span></span>

2.  <span data-ttu-id="8ef03-201">Créez ou modifiez le serveur SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="8ef03-201">Create or edit the sms\_def.mof file Configuration Manager Server.</span></span>

3.  <span data-ttu-id="8ef03-202">Installation de MBAM sur le serveur Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8ef03-202">Install MBAM on the Configuration Manager Server.</span></span>

4.  <span data-ttu-id="8ef03-203">Installation de la base de données de récupération et de la base de données d’audit sur le serveur de base de données.</span><span class="sxs-lookup"><span data-stu-id="8ef03-203">Install the Recovery Database and the Audit Database on the Database server.</span></span>

5.  <span data-ttu-id="8ef03-204">Installez les fonctionnalités de MBAM sur le serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="8ef03-204">Install the MBAM features on the Administration and Monitoring Server.</span></span>

## <span data-ttu-id="8ef03-205">Liste de contrôle de planification pour l’installation d’MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-205">Planning Checklist for Installing MBAM with Configuration Manager</span></span>


<span data-ttu-id="8ef03-206">Cette liste de vérification décrit les étapes recommandées et une liste générale des éléments à prendre en compte lors de la planification d’un déploiement de l’administration et de la surveillance de Microsoft BitLocker avec Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8ef03-206">This checklist outlines the recommended steps and a high-level list of items to consider when planning for an Microsoft BitLocker Administration and Monitoring deployment with Configuration Manager.</span></span> <span data-ttu-id="8ef03-207">Il est recommandé de copier cette liste de vérification dans un tableur et de la personnaliser pour votre utilisation.</span><span class="sxs-lookup"><span data-stu-id="8ef03-207">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="8ef03-208">Tâche</span><span class="sxs-lookup"><span data-stu-id="8ef03-208">Task</span></span></th>
<th align="left"><span data-ttu-id="8ef03-209">Références</span><span class="sxs-lookup"><span data-stu-id="8ef03-209">References</span></span></th>
<th align="left"><span data-ttu-id="8ef03-210">Remarques</span><span class="sxs-lookup"><span data-stu-id="8ef03-210">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8ef03-211">Passez en revue les informations de mise en route, qui décrivent comment Configuration Manager fonctionne avec MBAM et montre l’architecture de haut niveau recommandée.</span><span class="sxs-lookup"><span data-stu-id="8ef03-211">Review the getting started information, which describes how Configuration Manager works with MBAM and shows the recommended high-level architecture.</span></span></p></td>
<td align="left"><p><a href="getting-started---using-mbam-with-configuration-manager.md" data-raw-source="[Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)"><span data-ttu-id="8ef03-212">Prise en main - Utilisation de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-212">Getting Started - Using MBAM with Configuration Manager</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8ef03-213">Passez en revue les informations de planification qui décrivent les prérequis de déploiement, les configurations prises en charge, les autorisations requises et l’ordre de déploiement pour chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8ef03-213">Review the planning information, which describes the deployment prerequisites, supported configurations, required permissions, and deployment order for each feature.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8ef03-214">Planification du déploiement de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-214">Planning to Deploy MBAM with Configuration Manager</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8ef03-215">Planifiez et configurez les exigences de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="8ef03-215">Plan for and configure MBAM Group Policy requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)"><span data-ttu-id="8ef03-216">Planification des exigences en matière de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="8ef03-216">Planning for MBAM 2.0 Group Policy Requirements</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8ef03-217">Prévoyez et créez des groupes de sécurité de services de domaine Active Directory requis et planifiez les exigences d’appartenance au groupe de sécurité local MBAM.</span><span class="sxs-lookup"><span data-stu-id="8ef03-217">Plan for and create necessary Active Directory Domain Services security groups and plan for MBAM local security group membership requirements.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)"><span data-ttu-id="8ef03-218">Planification des rôles administrateur de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="8ef03-218">Planning for MBAM 2.0 Administrator Roles</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="8ef03-219">Plan de déploiement du déploiement du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="8ef03-219">Plan for deploying MBAM Client deployment.</span></span></p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)"><span data-ttu-id="8ef03-220">Planification du déploiement de clients MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="8ef03-220">Planning for MBAM 2.0 Client Deployment</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8ef03-221">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ef03-221">Related topics</span></span>


[<span data-ttu-id="8ef03-222">Utilisation de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8ef03-222">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)









