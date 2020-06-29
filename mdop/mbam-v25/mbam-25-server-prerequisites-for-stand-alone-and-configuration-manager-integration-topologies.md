---
title: Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome
description: Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome
author: dansimp
ms.assetid: 76a6047a-5c6e-42ff-af09-a6f382a69537
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9af551b1d867f61912bbf3b759574a840b0645c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811490"
---
# <span data-ttu-id="fb277-103">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</span><span class="sxs-lookup"><span data-stu-id="fb277-103">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>


<span data-ttu-id="fb277-104">Avant de démarrer l’installation de l’administration et de la surveillance de BitLocker (MBAM) Microsoft, vous devez remplir les conditions préalables indiquées dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="fb277-104">Before starting the Microsoft BitLocker Administration and Monitoring (MBAM) installation, you must complete the prerequisites listed in this topic.</span></span> <span data-ttu-id="fb277-105">Ces conditions préalables s’appliquent à la topologie autonome MBAM et System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fb277-105">These prerequisites apply to the MBAM Stand-alone topology and System Center Configuration Manager Integration topology.</span></span>

<span data-ttu-id="fb277-106">Si vous déployez MBAM à l’aide de System Center Configuration Manager, vous devez renseigner des éléments requis supplémentaires, qui sont répertoriés dans [MBAM 2,5 Server Prerequisites qui ne s’appliquent qu’à la topologie d’intégration de Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span><span class="sxs-lookup"><span data-stu-id="fb277-106">If you are deploying MBAM with System Center Configuration Manager, you must complete additional prerequisites, which are listed in [MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).</span></span>

<span data-ttu-id="fb277-107">Pour obtenir la liste des matériels et systèmes d’exploitation pris en charge pour MBAM, voir [Configurations prises en charge par MBAM 2,5](mbam-25-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="fb277-107">For a list of the supported hardware and operating systems for MBAM, see [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).</span></span>

**<span data-ttu-id="fb277-108">Important</span><span class="sxs-lookup"><span data-stu-id="fb277-108">Important</span></span>**  
<span data-ttu-id="fb277-109">Si BitLocker a été utilisé sans MBAM, vous devez déchiffrer le lecteur puis effacer TPM à l’aide de TPM. msc.</span><span class="sxs-lookup"><span data-stu-id="fb277-109">If BitLocker was used without MBAM, you must decrypt the drive and then clear TPM using tpm.msc.</span></span> <span data-ttu-id="fb277-110">MBAM ne peut pas prendre la propriété de TPM si le PC client est déjà chiffré et que le mot de passe du propriétaire du TPM a été créé.</span><span class="sxs-lookup"><span data-stu-id="fb277-110">MBAM cannot take ownership of TPM if the client PC is already encrypted and the TPM owner password created.</span></span>



## <span data-ttu-id="fb277-111">Rôles et comptes MBAM requis</span><span class="sxs-lookup"><span data-stu-id="fb277-111">Required MBAM roles and accounts</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb277-112">Prérequises</span><span class="sxs-lookup"><span data-stu-id="fb277-112">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="fb277-113">Détails</span><span class="sxs-lookup"><span data-stu-id="fb277-113">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-114">Groupes créés dans les services de domaine Active Directory (AD DS)</span><span class="sxs-lookup"><span data-stu-id="fb277-114">Groups created in Active Directory Domain Services (AD DS)</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-115"><a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)"> </a> Pour obtenir une description de ces groupes et comptes, voir Planification des groupes et comptes MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="fb277-115">See <a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)">Planning for MBAM 2.5 Groups and Accounts</a> for a description of these groups and accounts.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fb277-116">Conditions préalables pour la base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="fb277-116">Prerequisites for the Recovery Database</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb277-117">Prérequises</span><span class="sxs-lookup"><span data-stu-id="fb277-117">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="fb277-118">Détails</span><span class="sxs-lookup"><span data-stu-id="fb277-118">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-119">Version prise en charge de SQL Server</span><span class="sxs-lookup"><span data-stu-id="fb277-119">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-120">Installez Microsoft SQL Server avec SQL_Latin1_General_CP1_CI_AS collation.</span><span class="sxs-lookup"><span data-stu-id="fb277-120">Install Microsoft SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="fb277-121"><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,5.</span><span class="sxs-lookup"><span data-stu-id="fb277-121">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb277-122">Autorisations SQL Server requises</span><span class="sxs-lookup"><span data-stu-id="fb277-122">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-123">Autorisations requises:</span><span class="sxs-lookup"><span data-stu-id="fb277-123">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="fb277-124">Rôles de serveurs de connexion d’instances SQL Server:</span><span class="sxs-lookup"><span data-stu-id="fb277-124">SQL Server instance login server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="fb277-125">rôles</span><span class="sxs-lookup"><span data-stu-id="fb277-125">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="fb277-126">processadmin</span><span class="sxs-lookup"><span data-stu-id="fb277-126">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="fb277-127">Droits d’instance de SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="fb277-127">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="fb277-128">Créer des dossiers</span><span class="sxs-lookup"><span data-stu-id="fb277-128">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="fb277-129">Publier des rapports</span><span class="sxs-lookup"><span data-stu-id="fb277-129">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-130">Facultatif: installation de la fonctionnalité de chiffrement de données (TDE) transparente disponible dans SQL Server</span><span class="sxs-lookup"><span data-stu-id="fb277-130">Optional - Install the Transparent Data Encryption (TDE) feature available in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-131">La TDE SQL Server vous permet de chiffrer et de déchiffrer les données et les fichiers journaux en temps réel, ce qui peut vous aider à vous conformer aux lois, réglementations et recommandations applicables à divers secteurs d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="fb277-131">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with laws, regulations, and guidelines that apply to various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fb277-132">Remarque</span><span class="sxs-lookup"><span data-stu-id="fb277-132">Note</span></span></strong><br/><p><span data-ttu-id="fb277-133">TDE procède au déchiffrement en temps réel des informations de la base de données.</span><span class="sxs-lookup"><span data-stu-id="fb277-133">TDE performs real-time decryption of database information.</span></span> <span data-ttu-id="fb277-134">Cela signifie que si vous affichez les informations de clé de récupération dans la base de données SQL Server et que vous êtes connecté sous un compte qui dispose des autorisations de la base de données, les informations de clé de récupération sont affichées.</span><span class="sxs-lookup"><span data-stu-id="fb277-134">This means that, if you are viewing recovery key information in the SQL Server database and you are logged on under an account that has permissions to the database, the recovery key information is visible.</span></span> <span data-ttu-id="fb277-135">Pour en savoir plus sur TDE, reportez-vous à la section <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considérations relatives à la sécurité dans 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="fb277-135">To read more about TDE, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb277-136">Services du moteur de base de données SQL Server</span><span class="sxs-lookup"><span data-stu-id="fb277-136">SQL Server Database Engine Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-137">Les services du moteur de base de données SQL Server doivent être installés et exécutés lors de l’installation de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="fb277-137">SQL Server Database Engine Services must be installed and running during MBAM Server installation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-138">Windows PowerShell 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fb277-138">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-139">Il n’est pas nécessaire d’installer Windows PowerShell sur le serveur de base de données de récupération si vous utilisez Windows PowerShell pour configurer la base de données à partir d’un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="fb277-139">Windows PowerShell does not have to be installed on the Recovery Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fb277-140">Conditions préalables pour la base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="fb277-140">Prerequisites for the Compliance and Audit Database</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb277-141">Prérequises</span><span class="sxs-lookup"><span data-stu-id="fb277-141">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="fb277-142">Détails</span><span class="sxs-lookup"><span data-stu-id="fb277-142">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-143">Version prise en charge de SQL Server</span><span class="sxs-lookup"><span data-stu-id="fb277-143">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-144">Installez SQL Server avec SQL_Latin1_General_CP1_CI_AS collation.</span><span class="sxs-lookup"><span data-stu-id="fb277-144">Install SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="fb277-145"><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,5.</span><span class="sxs-lookup"><span data-stu-id="fb277-145">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb277-146">Autorisations SQL Server requises</span><span class="sxs-lookup"><span data-stu-id="fb277-146">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-147">Autorisations requises:</span><span class="sxs-lookup"><span data-stu-id="fb277-147">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="fb277-148">Rôles de serveurs de connexion d’instances SQL Server:</span><span class="sxs-lookup"><span data-stu-id="fb277-148">SQL Server instance login server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="fb277-149">rôles</span><span class="sxs-lookup"><span data-stu-id="fb277-149">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="fb277-150">processadmin</span><span class="sxs-lookup"><span data-stu-id="fb277-150">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="fb277-151">Droits d’instance de SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="fb277-151">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="fb277-152">Créer des dossiers</span><span class="sxs-lookup"><span data-stu-id="fb277-152">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="fb277-153">Publier des rapports</span><span class="sxs-lookup"><span data-stu-id="fb277-153">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-154">Option facultative: installation de la fonctionnalité de chiffrement de données (TDE) transparente dans SQL Server</span><span class="sxs-lookup"><span data-stu-id="fb277-154">Optional - Install the Transparent Data Encryption (TDE) feature in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-155">La TDE SQL Server vous permet de chiffrer et de déchiffrer les données et les fichiers journaux en temps réel, ce qui peut vous aider à vous conformer aux lois, réglementations et recommandations applicables à divers secteurs d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="fb277-155">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with laws, regulations, and guidelines that apply to various industries.</span></span></p>
<p><span data-ttu-id="fb277-156">TDE procède au déchiffrement en temps réel des informations de la base de données.</span><span class="sxs-lookup"><span data-stu-id="fb277-156">TDE performs real-time decryption of database information.</span></span> <span data-ttu-id="fb277-157">Cela signifie que si vous affichez les informations de clé de récupération dans la base de données SQL Server et que vous êtes connecté sous un compte qui dispose des autorisations de la base de données, les informations de clé de récupération sont affichées.</span><span class="sxs-lookup"><span data-stu-id="fb277-157">This means that, if you are viewing recovery key information in the SQL Server database and you are logged on under an account that has permissions to the database, the recovery key information is visible.</span></span> <span data-ttu-id="fb277-158">Pour en savoir plus sur TDE, reportez-vous à la section <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considérations relatives à la sécurité dans 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="fb277-158">To read more about TDE, see <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">MBAM 2.5 Security Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb277-159">Services du moteur de base de données SQL Server</span><span class="sxs-lookup"><span data-stu-id="fb277-159">SQL Server Database Engine Services</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-160">Les services du moteur de base de données SQL Server doivent être installés et exécutés lors de l’installation de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="fb277-160">SQL Server Database Engine Services must be installed and running during MBAM Server installation.</span></span> <span data-ttu-id="fb277-161">Toutefois, SQL Server peut être exécuté à distance; Il n’est pas nécessaire de se trouver sur le même serveur sur lequel vous installez le logiciel serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="fb277-161">However, SQL Server can be running remotely; it doesn’t have to be on the same server on which you are installing the MBAM Server software.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-162">Windows PowerShell 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fb277-162">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-163">Pour configurer la base de données à partir d’un ordinateur distant, il n’est pas nécessaire d’installer Windows PowerShell sur le serveur de base de données de conformité et d’audit si vous utilisez Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fb277-163">Windows PowerShell does not have to be installed on the Compliance and Audit Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fb277-164">Conditions préalables pour les rapports</span><span class="sxs-lookup"><span data-stu-id="fb277-164">Prerequisites for the Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb277-165">Prérequises</span><span class="sxs-lookup"><span data-stu-id="fb277-165">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="fb277-166">Détails</span><span class="sxs-lookup"><span data-stu-id="fb277-166">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-167">Version prise en charge de SQL Server</span><span class="sxs-lookup"><span data-stu-id="fb277-167">Supported version of SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-168">Installez SQL Server avec SQL_Latin1_General_CP1_CI_AS collation.</span><span class="sxs-lookup"><span data-stu-id="fb277-168">Install SQL Server with SQL_Latin1_General_CP1_CI_AS collation.</span></span></p>
<p><span data-ttu-id="fb277-169"><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,5.</span><span class="sxs-lookup"><span data-stu-id="fb277-169">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb277-170">SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="fb277-170">SQL Server Reporting Services (SSRS)</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-171">SSRS doit être installé et exécuté lors de l’installation de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="fb277-171">SSRS must be installed and running during the MBAM Server installation.</span></span></p>
<p><span data-ttu-id="fb277-172">Configurer SSRS en &quot; &quot; mode natif et non en mode non configuré ou &quot; SharePoint &quot; .</span><span class="sxs-lookup"><span data-stu-id="fb277-172">Configure SSRS in &quot;native&quot; mode and not in unconfigured or &quot;SharePoint&quot; mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-173">Droits d’instance SSRS: requis pour la configuration des rapports uniquement si vous installez des bases de données sur un serveur distinct du serveur sur lequel les rapports sont configurés.</span><span class="sxs-lookup"><span data-stu-id="fb277-173">SSRS instance rights – required for configuring Reports only if you are installing databases on a separate server from the server where Reports are configured.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-174">Droits d’instance requis:</span><span class="sxs-lookup"><span data-stu-id="fb277-174">Required instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="fb277-175">Créer des dossiers</span><span class="sxs-lookup"><span data-stu-id="fb277-175">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="fb277-176">Publier des rapports</span><span class="sxs-lookup"><span data-stu-id="fb277-176">Publish Reports</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb277-177">Windows PowerShell 3,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fb277-177">Windows PowerShell 3.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-178">Pour configurer la base de données à partir d’un ordinateur distant, il n’est pas nécessaire d’installer Windows PowerShell sur ce serveur de base de données si vous utilisez Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fb277-178">Windows PowerShell does not have to be installed on this Database server if you are using Windows PowerShell to configure the database from a remote computer.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-prereqsams"></a><span data-ttu-id="fb277-179">Conditions préalables pour le serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="fb277-179">Prerequisites for the Administration and Monitoring Server</span></span>


<span data-ttu-id="fb277-180">Le tableau suivant répertorie les conditions préalables à l’installation du serveur d’administration et de surveillance MBAM.</span><span class="sxs-lookup"><span data-stu-id="fb277-180">The following table lists the installation prerequisites for the MBAM Administration and Monitoring Server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb277-181">Prérequises</span><span class="sxs-lookup"><span data-stu-id="fb277-181">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="fb277-182">Détails</span><span class="sxs-lookup"><span data-stu-id="fb277-182">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-183">Rôle du serveur Web Windows Server</span><span class="sxs-lookup"><span data-stu-id="fb277-183">Windows Server Web Server Role</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-184">Ce rôle doit être ajouté à un système d’exploitation serveur pris en charge pour la fonctionnalité d’administration et de surveillance du serveur.</span><span class="sxs-lookup"><span data-stu-id="fb277-184">This role must be added to a server operating system that is supported for the Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb277-185">Outils de gestion du serveur Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="fb277-185">Web Server (IIS) Management Tools</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-186">Cliquez sur <strong> scripts et outils de gestion IIS </strong> .</span><span class="sxs-lookup"><span data-stu-id="fb277-186">Click <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb277-187">Certificat SSL</span><span class="sxs-lookup"><span data-stu-id="fb277-187">SSL Certificate</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb277-188">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="fb277-188">Optional.</span></span> <span data-ttu-id="fb277-189">Pour sécuriser les communications entre les ordinateurs client et les services Web, vous devez obtenir et installer un certificat qu’une autorité de sécurité fiable a signée.</span><span class="sxs-lookup"><span data-stu-id="fb277-189">To secure communication between the client computers and the web services, you must obtain and install a certificate that a trusted security authority signed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb277-190">Services de rôle de serveur Web</span><span class="sxs-lookup"><span data-stu-id="fb277-190">Web Server Role Services</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="fb277-191">Fonctionnalités HTTP communes:</span><span class="sxs-lookup"><span data-stu-id="fb277-191">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="fb277-192">Contenu statique</span><span class="sxs-lookup"><span data-stu-id="fb277-192">Static Content</span></span></p></li>
<li><p><span data-ttu-id="fb277-193">Document par défaut</span><span class="sxs-lookup"><span data-stu-id="fb277-193">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="fb277-194">Développement d’applications:</span><span class="sxs-lookup"><span data-stu-id="fb277-194">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="fb277-195">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="fb277-195">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="fb277-196">Extensibilité .NET</span><span class="sxs-lookup"><span data-stu-id="fb277-196">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="fb277-197">Extensions ISAPI</span><span class="sxs-lookup"><span data-stu-id="fb277-197">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="fb277-198">Filtres ISAPI</span><span class="sxs-lookup"><span data-stu-id="fb277-198">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="fb277-199">Sûreté</span><span class="sxs-lookup"><span data-stu-id="fb277-199">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="fb277-200">Authentification Windows</span><span class="sxs-lookup"><span data-stu-id="fb277-200">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="fb277-201">Filtrage de requête</span><span class="sxs-lookup"><span data-stu-id="fb277-201">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-202">Fonctionnalités de Windows Server</span><span class="sxs-lookup"><span data-stu-id="fb277-202">Windows Server Features</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="fb277-203">Fonctionnalités de .NET Framework 4,5:</span><span class="sxs-lookup"><span data-stu-id="fb277-203">.NET Framework 4.5 features:</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="fb277-204">.NET Framework 4,5 ou 4,6</span><span class="sxs-lookup"><span data-stu-id="fb277-204">.NET Framework 4.5 or 4.6</span></span></strong></p>
<ul>
<li><p><strong><span data-ttu-id="fb277-205">Windows Server 2016 </strong> - .net Framework 4,6 est déjà installé pour ces versions de Windows Server, mais vous devez l’activer.</span><span class="sxs-lookup"><span data-stu-id="fb277-205">Windows Server 2016</strong> - .NET Framework 4.6 is already installed for these versions of Windows Server, but you must enable it.</span></span></p></li>  
<li><p><strong><span data-ttu-id="fb277-206">Windows Server 2012 ou Windows Server 2012 R2 </strong> - .net Framework 4,5 est déjà installé pour ces versions de Windows Server, mais vous devez l’activer.</span><span class="sxs-lookup"><span data-stu-id="fb277-206">Windows Server 2012 or Windows Server 2012 R2</strong> - .NET Framework 4.5 is already installed for these versions of Windows Server, but you must enable it.</span></span></p></li>
<li><p><strong><span data-ttu-id="fb277-207">Windows Server 2008 R2 </strong> - .net Framework 4,5 n’est pas inclus dans windows Server 2008 R2, vous devez donc <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)"> Télécharger Microsoft .NET Framework 4,5 </a> et l’installer séparément.</span><span class="sxs-lookup"><span data-stu-id="fb277-207">Windows Server 2008 R2</strong> - .NET Framework 4.5 is not included with Windows Server 2008 R2, so you must <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)">download Microsoft .NET Framework 4.5</a> and install it separately.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fb277-208">Remarque</span><span class="sxs-lookup"><span data-stu-id="fb277-208">Note</span></span></strong><br/><p><span data-ttu-id="fb277-209">Si vous effectuez une mise à niveau à partir de MBAM 2,0 ou MBAM 2,0 SP1 et que vous devez installer .NET Framework 4,5, voir <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)"> les notes de publication pour MBAM 2,5 </a> pour une étape supplémentaire requise pour le fonctionnement des sites Web.</span><span class="sxs-lookup"><span data-stu-id="fb277-209">If you are upgrading from MBAM 2.0 or MBAM 2.0 SP1 and need to install .NET Framework 4.5, see <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)">Release Notes for MBAM 2.5</a> for an additional required step to make the websites work.</span></span></p>
</div>
<div>

</div></li>
</ul></li>
<li><p><strong><span data-ttu-id="fb277-210">Activation WCF</span><span class="sxs-lookup"><span data-stu-id="fb277-210">WCF Activation</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="fb277-211">Activation HTTP</span><span class="sxs-lookup"><span data-stu-id="fb277-211">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="fb277-212">Activation non HTTP (uniquement pour Windows Server 2008, 2012 et 2012 R2)</span><span class="sxs-lookup"><span data-stu-id="fb277-212">Non-HTTP Activation (Only for Windows Server 2008, 2012, and 2012 R2)</span></span></p>
<p></p></li>
</ul></li>
<li><p><strong><span data-ttu-id="fb277-213">Activation TCP</span><span class="sxs-lookup"><span data-stu-id="fb277-213">TCP Activation</span></span></strong></p></li>
</ul>
<p><strong><span data-ttu-id="fb277-214">Service d’activation de processus Windows:</span><span class="sxs-lookup"><span data-stu-id="fb277-214">Windows Process Activation Service:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="fb277-215">Modèle de processus</span><span class="sxs-lookup"><span data-stu-id="fb277-215">Process Model</span></span></p></li>
<li><p><span data-ttu-id="fb277-216">Environnement .NET Framework</span><span class="sxs-lookup"><span data-stu-id="fb277-216">.NET Framework Environment</span></span></p></li>
<li><p><span data-ttu-id="fb277-217">API de configuration</span><span class="sxs-lookup"><span data-stu-id="fb277-217">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb277-218">ASP.NET MVC 4,0</span><span class="sxs-lookup"><span data-stu-id="fb277-218">ASP.NET MVC 4.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)"><span data-ttu-id="fb277-219">Télécharger ASP.NET MVC 4</span><span class="sxs-lookup"><span data-stu-id="fb277-219">ASP.NET MVC 4 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-220">Nom de principal de service (SPN)</span><span class="sxs-lookup"><span data-stu-id="fb277-220">Service Principal Name (SPN)</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-221">Les applications Web requièrent un SPN pour le nom d’hôte virtuel sous le compte de domaine que vous utilisez pour les pools d’applications Web.</span><span class="sxs-lookup"><span data-stu-id="fb277-221">The web applications require an SPN for the virtual host name under the domain account that you use for the web application pools.</span></span></p>
<p><span data-ttu-id="fb277-222">Si vos droits d’administrateur vous permettent de créer des SPN dans les services de domaine Active Directory (AD FS), MBAM crée le SPN pour vous.</span><span class="sxs-lookup"><span data-stu-id="fb277-222">If your administrative rights permit you to create SPNs in Active Directory Domain Services, MBAM creates the SPN for you.</span></span> <span data-ttu-id="fb277-223">Voir <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> setspn </a> pour plus d’informations sur les droits nécessaires à la création de SPN.</span><span class="sxs-lookup"><span data-stu-id="fb277-223">See <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Setspn</a> for information about the rights required to create SPNs.</span></span></p>
<p><span data-ttu-id="fb277-224">Si vous ne disposez pas des droits d’administration pour créer des SPN, vous devez demander à l’administrateur Active Directory de votre organisation de créer le SPN pour vous en utilisant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="fb277-224">If you do not have administrative rights to create SPNs, you must ask the Active Directory administrators in your organization to create the SPN for you by using the following command.</span></span></p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p><span data-ttu-id="fb277-225">Dans l’exemple de code, le nom d’hôte virtuel est mbamvirtual.contoso.com et le compte de domaine utilisé pour les pools d’applications Web est contoso\mbamapppooluser.</span><span class="sxs-lookup"><span data-stu-id="fb277-225">In the code example, the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\mbamapppooluser.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fb277-226">Remarque</span><span class="sxs-lookup"><span data-stu-id="fb277-226">Note</span></span></strong><br/><p><span data-ttu-id="fb277-227">Si vous configurez l’équilibrage de charge, utilisez le même compte de pool d’applications sur tous les serveurs.</span><span class="sxs-lookup"><span data-stu-id="fb277-227">If you are setting up Load Balancing, use the same application pool account on all servers.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="fb277-228">Pour plus d’informations sur l’inscription de SPN pour les noms d’hôtes complets, NetBIOS et personnalisés, voir <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> planification de la sécurisation des sites Web MBAM </a> .</span><span class="sxs-lookup"><span data-stu-id="fb277-228">For more information about registering SPNs for fully qualified, NetBIOS, and custom host names, see <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planning How to Secure the MBAM Websites</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fb277-229">Conditions préalables pour le portail libre-service</span><span class="sxs-lookup"><span data-stu-id="fb277-229">Prerequisites for the Self-Service Portal</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb277-230">Prérequises</span><span class="sxs-lookup"><span data-stu-id="fb277-230">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="fb277-231">Détails</span><span class="sxs-lookup"><span data-stu-id="fb277-231">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-232">Version prise en charge de Windows Server</span><span class="sxs-lookup"><span data-stu-id="fb277-232">Supported version of Windows Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-233"><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,5.</span><span class="sxs-lookup"><span data-stu-id="fb277-233">See <a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">MBAM 2.5 Supported Configurations</a> for supported versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb277-234">ASP.NET MVC 4,0</span><span class="sxs-lookup"><span data-stu-id="fb277-234">ASP.NET MVC 4.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)"><span data-ttu-id="fb277-235">Télécharger ASP.NET MVC 4</span><span class="sxs-lookup"><span data-stu-id="fb277-235">ASP.NET MVC 4 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-236">Outils de gestion IIS de service Web</span><span class="sxs-lookup"><span data-stu-id="fb277-236">Web Service IIS Management Tools</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb277-237">Nom de principal de service (SPN)</span><span class="sxs-lookup"><span data-stu-id="fb277-237">Service Principal Name (SPN)</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-238">Les applications Web requièrent un SPN pour le nom d’hôte virtuel sous le compte de domaine que vous utilisez pour les pools d’applications Web.</span><span class="sxs-lookup"><span data-stu-id="fb277-238">The web applications require an SPN for the virtual host name under the domain account that you use for the web application pools.</span></span></p>
<p><span data-ttu-id="fb277-239">Si vos droits d’administrateur vous permettent de créer des SPN dans les services de domaine Active Directory (AD FS), MBAM crée le SPN pour vous.</span><span class="sxs-lookup"><span data-stu-id="fb277-239">If your administrative rights permit you to create SPNs in Active Directory Domain Services, MBAM creates the SPN for you.</span></span> <span data-ttu-id="fb277-240">Voir <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> setspn </a> pour plus d’informations sur les droits nécessaires à la création de SPN.</span><span class="sxs-lookup"><span data-stu-id="fb277-240">See <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)">Setspn</a> for information about the rights required to create SPNs.</span></span></p>
<p><span data-ttu-id="fb277-241">Si vous ne disposez pas des droits d’administration pour créer des SPN, vous devez demander à l’administrateur Active Directory de votre organisation de créer le SPN pour vous en utilisant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="fb277-241">If you do not have administrative rights to create SPNs, you must ask the Active Directory administrators in your organization administrators in your organization to create the SPN for you by using the following command.</span></span></p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p><span data-ttu-id="fb277-242">Dans l’exemple de code, le nom d’hôte virtuel est mbamvirtual.contoso.com et le compte de domaine utilisé pour les pools d’applications Web est contoso\mbamapppooluser.</span><span class="sxs-lookup"><span data-stu-id="fb277-242">In the code example, the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\mbamapppooluser.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="fb277-243">Remarque</span><span class="sxs-lookup"><span data-stu-id="fb277-243">Note</span></span></strong><br/><p><span data-ttu-id="fb277-244">Si vous configurez l’équilibrage de charge, utilisez le même compte de pool d’applications sur tous les serveurs.</span><span class="sxs-lookup"><span data-stu-id="fb277-244">If you are setting up Load Balancing, use the same application pool account on all servers.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="fb277-245">Pour plus d’informations sur l’inscription de SPN pour les noms d’hôtes complets, NetBIOS et personnalisés, voir <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> planification de la sécurisation des sites Web MBAM </a> .</span><span class="sxs-lookup"><span data-stu-id="fb277-245">For more information about registering SPNs for fully qualified, NetBIOS, and custom host names, see <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planning How to Secure the MBAM Websites</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="fb277-246">Conditions préalables pour la station de travail de gestion</span><span class="sxs-lookup"><span data-stu-id="fb277-246">Prerequisites for the Management Workstation</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb277-247">Prérequises</span><span class="sxs-lookup"><span data-stu-id="fb277-247">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="fb277-248">Détails</span><span class="sxs-lookup"><span data-stu-id="fb277-248">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-249">Avant d’installer le client MBAM, téléchargez les modèles de stratégie de groupe MBAM à partir de la <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> section obtention de modèles de stratégie de groupe MDOP (. admx) </a> et configurez-les avec les paramètres que vous voulez implémenter dans votre entreprise pour le chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fb277-249">Before installing the MBAM Client, download the MBAM Group Policy Templates from <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)">How to Get MDOP Group Policy (.admx) Templates</a> and configure them with the settings that you want to implement in your enterprise for BitLocker Drive Encryption.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb277-250">Avant d’installer le client MBAM, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="fb277-250">Before installing the MBAM Client, do the following:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb277-251">À faire</span><span class="sxs-lookup"><span data-stu-id="fb277-251">What to do</span></span></th>
<th align="left"><span data-ttu-id="fb277-252">Où obtenir des instructions</span><span class="sxs-lookup"><span data-stu-id="fb277-252">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb277-253">Copier les modèles de stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="fb277-253">Copy the MBAM Group Policy Templates</span></span></p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)"><span data-ttu-id="fb277-254">Copie des modèles de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="fb277-254">Copying the MBAM 2.5 Group Policy Templates</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb277-255">Modifier les paramètres de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="fb277-255">Edit the Group Policy settings</span></span></p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"><span data-ttu-id="fb277-256">Modification des paramètres de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="fb277-256">Editing the MBAM 2.5 Group Policy Settings</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>





## <span data-ttu-id="fb277-257">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb277-257">Related topics</span></span>


[<span data-ttu-id="fb277-258">Préparation de votre environnement pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="fb277-258">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="fb277-259">Planification du déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="fb277-259">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="fb277-260">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="fb277-260">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)




## <span data-ttu-id="fb277-261">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="fb277-261">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="fb277-262">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="fb277-262">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="fb277-263">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="fb277-263">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




