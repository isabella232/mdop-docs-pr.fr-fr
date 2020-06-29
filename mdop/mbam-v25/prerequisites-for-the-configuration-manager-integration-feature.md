---
title: Conditions préalables pour le composant Intégration Configuration Manager
description: Conditions préalables pour le composant Intégration Configuration Manager
author: dansimp
ms.assetid: b318cbd3-b009-44b8-991b-f7364c1cae88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af7abd50f6218810dd6718f091512b48fee32652
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810901"
---
# <span data-ttu-id="ba684-103">Conditions préalables pour le composant Intégration Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ba684-103">Prerequisites for the Configuration Manager Integration Feature</span></span>


<span data-ttu-id="ba684-104">Si vous déployez MBAM avec la topologie d’intégration System Center Configuration Manager, nous vous recommandons d’utiliser une architecture à trois serveurs, comme décrit dans [architecture de niveau supérieur d’MBAM 2,5 avec la topologie d’intégration de Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="ba684-104">If you deploy MBAM with the System Center Configuration Manager Integration topology, we recommend a three-server architecture, as described in [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).</span></span> <span data-ttu-id="ba684-105">Cette architecture peut prendre en charge des ordinateurs clients 500 000.</span><span class="sxs-lookup"><span data-stu-id="ba684-105">This architecture can support 500,000 client computers.</span></span>

**<span data-ttu-id="ba684-106">Important</span><span class="sxs-lookup"><span data-stu-id="ba684-106">Important</span></span>**  
<span data-ttu-id="ba684-107">Windows to Go n’est pas pris en charge pour l’installation de la topologie d’intégration de Configuration Manager lorsque vous utilisez Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="ba684-107">Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>



## <span data-ttu-id="ba684-108">Conditions générales requises pour la fonctionnalité d’intégration de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ba684-108">General prerequisites for the Configuration Manager Integration feature</span></span>


<span data-ttu-id="ba684-109">Lorsque vous installez MBAM avec Configuration Manager, les conditions préalables supplémentaires suivantes sont requises en plus de la configuration requise pour la topologie autonome.</span><span class="sxs-lookup"><span data-stu-id="ba684-109">When you install MBAM with Configuration Manager, the following additional prerequisites are required in addition to the prerequisites for the Stand-alone topology.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ba684-110">Prérequises</span><span class="sxs-lookup"><span data-stu-id="ba684-110">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="ba684-111">Informations complémentaires</span><span class="sxs-lookup"><span data-stu-id="ba684-111">Additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba684-112">Le serveur Configuration Manager est un site principal dans le système Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ba684-112">The Configuration Manager Server is a primary site in the Configuration Manager system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba684-113">N/A</span><span class="sxs-lookup"><span data-stu-id="ba684-113">N/A</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba684-114">L’agent client d’inventaire matériel est sur le serveur Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ba684-114">The Hardware Inventory Client Agent is on the Configuration Manager Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba684-115">Pour le gestionnaire de configuration de System Center 2012, voir <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> Comment configurer l’inventaire matériel dans Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="ba684-115">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)">How to Configure Hardware Inventory in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="ba684-116">Pour Configuration Manager 2007, voir <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> Comment configurer l’inventaire matériel d’un site </a> .</span><span class="sxs-lookup"><span data-stu-id="ba684-116">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)">How to Configure Hardware Inventory for a Site</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba684-117">L’une des options suivantes est activée, en fonction de la version de Configuration Manager que vous utilisez:</span><span class="sxs-lookup"><span data-stu-id="ba684-117">One of the following is enabled, depending on the version of Configuration Manager that you are using:</span></span></p>
<ul>
<li><p><span data-ttu-id="ba684-118">Paramètres de conformité-(gestionnaire de configuration de System Center 2012)</span><span class="sxs-lookup"><span data-stu-id="ba684-118">Compliance Settings - (System Center 2012 Configuration Manager)</span></span></p></li>
<li><p><span data-ttu-id="ba684-119">Agent client de gestion des configurations souhaité (DCM) – (Configuration Manager 2007)</span><span class="sxs-lookup"><span data-stu-id="ba684-119">Desired Configuration Management (DCM) Client Agent – (Configuration Manager 2007)</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="ba684-120">Pour System Center 2012 Configuration Manager, consultez <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> la rubrique Configuration des paramètres de conformité dans Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="ba684-120">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)">Configuring Compliance Settings in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="ba684-121">Pour Configuration Manager 2007, voir <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> Propriétés de l’agent du client de gestion de configuration souhaitées </a> .</span><span class="sxs-lookup"><span data-stu-id="ba684-121">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)">Desired Configuration Management Client Agent Properties</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba684-122">Un point Report services est défini dans Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ba684-122">A reporting services point is defined in Configuration Manager.</span></span> <span data-ttu-id="ba684-123">Requis pour SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="ba684-123">Required for SQL Server Reporting Services (SSRS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba684-124">Pour le gestionnaire de configuration de System Center 2012, voir la configuration <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> requise pour la création de rapports dans Configuration Manager </a> .</span><span class="sxs-lookup"><span data-stu-id="ba684-124">For System Center 2012 Configuration Manager, see <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)">Prerequisites for Reporting in Configuration Manager</a>.</span></span></p>
<p><span data-ttu-id="ba684-125">Pour Configuration Manager 2007, voir <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> création d’un point de Reporting Services pour SQL Reporting Services </a> .</span><span class="sxs-lookup"><span data-stu-id="ba684-125">For Configuration Manager 2007, see <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)">How to Create a Reporting Services Point for SQL Reporting Services</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba684-126">Configuration Manager 2007 nécessite Microsoft .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="ba684-126">Configuration Manager 2007 requires Microsoft .NET Framework 2.0</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba684-127">L’agent client de gestion des configurations souhaité (DCM) dans Configuration Manager 2007 nécessite .NET Framework 2,0 pour signaler la conformité.</span><span class="sxs-lookup"><span data-stu-id="ba684-127">The Desired Configuration Management (DCM) Client Agent in Configuration Manager 2007 requires .NET Framework 2.0 to report compliance.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="ba684-128">Remarque</span><span class="sxs-lookup"><span data-stu-id="ba684-128">Note</span></span></strong><br/><p><span data-ttu-id="ba684-129">L’installation de .NET Framework 3,5 installe automatiquement .NET Framework 2,0.</span><span class="sxs-lookup"><span data-stu-id="ba684-129">Installing .NET Framework 3.5 automatically installs .NET Framework 2.0.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="ba684-130">Autorisations requises pour installer MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ba684-130">Required permissions to install MBAM with Configuration Manager</span></span>


<span data-ttu-id="ba684-131">Pour installer MBAM avec Configuration Manager, vous devez disposer d’un utilisateur administratif dans Configuration Manager ayant un rôle de sécurité avec les autorisations minimales indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ba684-131">To install MBAM with Configuration Manager, you must have an administrative user in Configuration Manager who has a security role with the minimum permissions listed in the following table.</span></span> <span data-ttu-id="ba684-132">Le tableau ci-dessous indique également les droits dont vous avez besoin au-delà des droits d’administrateur d’ordinateur de base pour installer le serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="ba684-132">The table also shows the rights that you must have, beyond basic computer administrator rights, to install the MBAM Server.</span></span>

**<span data-ttu-id="ba684-133">Les autorisations figurant dans le tableau ci-dessous s’appliquent aux deux versions de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ba684-133">The permissions in the following table apply to both versions of Configuration Manager.</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ba684-134">Autorisations</span><span class="sxs-lookup"><span data-stu-id="ba684-134">Permissions</span></span></th>
<th align="left"><span data-ttu-id="ba684-135">Fonctionnalité du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="ba684-135">MBAM Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba684-136">Rôles de serveurs de connexion d’instances SQL Server:-dbcreator-processadmin</span><span class="sxs-lookup"><span data-stu-id="ba684-136">SQL Server instance login server roles: - dbcreator- processadmin</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="ba684-137">Base de données de récupération-base de données d’audit</span><span class="sxs-lookup"><span data-stu-id="ba684-137">Recovery Database- Audit Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba684-138">Droits d’instance SSRS:-créer des dossiers-publier des rapports</span><span class="sxs-lookup"><span data-stu-id="ba684-138">SSRS instance rights: - Create Folders- Publish Reports</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="ba684-139">Intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ba684-139">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ba684-140">System Center2012 Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ba684-140">System Center 2012 Configuration Manager</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ba684-141">Autorisations</span><span class="sxs-lookup"><span data-stu-id="ba684-141">Permissions</span></span></th>
<th align="left"><span data-ttu-id="ba684-142">Fonctionnalité serveur Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ba684-142">Configuration Manager Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba684-143">Droits de site Configuration Manager:-lecture</span><span class="sxs-lookup"><span data-stu-id="ba684-143">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba684-144">Intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ba684-144">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba684-145">Droits de collection de Configuration Manager:-création-suppression-lecture-modification-déploiement des éléments de configuration</span><span class="sxs-lookup"><span data-stu-id="ba684-145">Configuration Manager collection rights: - Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba684-146">Intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ba684-146">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba684-147">Configuration des éléments de configuration de Configuration Manager:-création-suppression-lecture</span><span class="sxs-lookup"><span data-stu-id="ba684-147">Configuration Manager configuration item rights: - Create- Delete- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba684-148">Intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ba684-148">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ba684-149">Gestionnaire de configuration 2007</span><span class="sxs-lookup"><span data-stu-id="ba684-149">Configuration Manager 2007</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ba684-150">Autorisations</span><span class="sxs-lookup"><span data-stu-id="ba684-150">Permissions</span></span></th>
<th align="left"><span data-ttu-id="ba684-151">Fonctionnalité serveur Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ba684-151">Configuration Manager Server feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba684-152">Droits de site Configuration Manager:-lecture</span><span class="sxs-lookup"><span data-stu-id="ba684-152">Configuration Manager site rights:- Read</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba684-153">Intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ba684-153">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ba684-154">Droits de collection de Configuration Manager:-création-suppression-lecture-ReadResource</span><span class="sxs-lookup"><span data-stu-id="ba684-154">Configuration Manager collection rights: - Create- Delete- Read- ReadResource</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba684-155">Intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ba684-155">System Center Configuration Manager Integration</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ba684-156">Configuration des éléments de configuration de Configuration Manager:-création-suppression-lecture/distribution</span><span class="sxs-lookup"><span data-stu-id="ba684-156">Configuration Manager configuration item rights: - Create- Delete- Read- Distribute</span></span></p></td>
<td align="left"><p><span data-ttu-id="ba684-157">Intégration de System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ba684-157">System Center Configuration Manager Integration</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="ba684-158">Modifications requises pour les fichiers. mof</span><span class="sxs-lookup"><span data-stu-id="ba684-158">Required changes for the .mof files</span></span>


<span data-ttu-id="ba684-159">Pour permettre aux ordinateurs clients de signaler les détails de conformité BitLocker par le biais des rapports du gestionnaire de configuration MBAM, vous devez modifier le fichier de configuration. mof et le fichier SMS \ _def. mof pour System Center 2012 Configuration Manager et Microsoft System Center Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="ba684-159">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the Configuration.mof file and Sms\_def.mof file for System Center 2012 Configuration Manager and Microsoft System Center Configuration Manager 2007.</span></span> <span data-ttu-id="ba684-160">Pour obtenir des instructions, consultez [la configuration requise pour le serveur MBAM 2,5 qui s’applique uniquement à la topologie d’intégration de Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="ba684-160">For instructions, see [MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span></span>



## <span data-ttu-id="ba684-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ba684-161">Related topics</span></span>


[<span data-ttu-id="ba684-162">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</span><span class="sxs-lookup"><span data-stu-id="ba684-162">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

[<span data-ttu-id="ba684-163">Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ba684-163">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)



## <span data-ttu-id="ba684-164">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="ba684-164">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ba684-165">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="ba684-165">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ba684-166">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ba684-166">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





