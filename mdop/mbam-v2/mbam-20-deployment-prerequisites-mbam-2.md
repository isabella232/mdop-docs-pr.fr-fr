---
title: Conditions préalables au déploiement de MBAM2.0
description: Conditions préalables au déploiement de MBAM2.0
author: dansimp
ms.assetid: 57d1c2bb-5ea3-457e-badd-dd9206ff0f20
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ef7ee64a3661009f18e0963d738c57a59885cb20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811501"
---
# <span data-ttu-id="43dc9-103">Conditions préalables au déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="43dc9-103">MBAM 2.0 Deployment Prerequisites</span></span>


<span data-ttu-id="43dc9-104">Avant de démarrer le programme d’installation de Microsoft BitLocker (MBAM), vous devez vérifier que vous remplissez les conditions préalables à l’installation du produit.</span><span class="sxs-lookup"><span data-stu-id="43dc9-104">Before you start Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should ensure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="43dc9-105">Cette section contient des informations pour vous aider à planifier votre environnement informatique avant de déployer Microsoft BitLocker administration et de surveiller les fonctionnalités et clients du serveur.</span><span class="sxs-lookup"><span data-stu-id="43dc9-105">This section contains information to help you successfully plan your computing environment before you deploy Microsoft BitLocker Administration and Monitoring Server features and Clients.</span></span> <span data-ttu-id="43dc9-106">Si vous installez MBAM avec Configuration Manager, reportez-vous à la section [planification du déploiement d’MBAM avec Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) pour obtenir d’autres conditions préalables.</span><span class="sxs-lookup"><span data-stu-id="43dc9-106">If you are installing MBAM with Configuration Manager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) for additional prerequisites.</span></span>

## <span data-ttu-id="43dc9-107">Conditions préalables à l’installation pour les fonctionnalités du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="43dc9-107">Installation Prerequisites for MBAM Server Features</span></span>


<span data-ttu-id="43dc9-108">Chacune des fonctionnalités du serveur MBAM comporte des éléments requis spécifiques qui doivent être satisfaits pour que les fonctionnalités MBAM puissent être installées avec succès.</span><span class="sxs-lookup"><span data-stu-id="43dc9-108">Each of the MBAM Server features has specific prerequisites that must be met before the MBAM features can be successfully installed.</span></span> <span data-ttu-id="43dc9-109">Le programme d’installation de MBAM vérifie que toutes les conditions préalables sont remplies avant le démarrage de l’installation.</span><span class="sxs-lookup"><span data-stu-id="43dc9-109">MBAM Setup checks that all prerequisites are met before the installation starts.</span></span>

### <span data-ttu-id="43dc9-110">Conditions préalables pour le serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="43dc9-110">Prerequisites for Administration and Monitoring Server</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="43dc9-111">Prérequises</span><span class="sxs-lookup"><span data-stu-id="43dc9-111">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="43dc9-112">Détails</span><span class="sxs-lookup"><span data-stu-id="43dc9-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="43dc9-113">Rôle du serveur Web Windows Server</span><span class="sxs-lookup"><span data-stu-id="43dc9-113">Windows Server Web Server Role</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="43dc9-114">Ce rôle doit être ajouté à un système d’exploitation serveur pris en charge pour la fonctionnalité d’administration et de surveillance du serveur.</span><span class="sxs-lookup"><span data-stu-id="43dc9-114">This role must be added to a server operating system that is supported for the Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="43dc9-115">Outils de gestion du serveur Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="43dc9-115">Web Server (IIS) Management Tools</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="43dc9-116">Sélectionnez <strong> scripts et outils de gestion IIS </strong> .</span><span class="sxs-lookup"><span data-stu-id="43dc9-116">Select <strong>IIS Management Scripts and Tools</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="43dc9-117">Certificat SSL</span><span class="sxs-lookup"><span data-stu-id="43dc9-117">SSL Certificate</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="43dc9-118">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="43dc9-118">Optional.</span></span> <span data-ttu-id="43dc9-119">Pour sécuriser les communications entre les clients et les services Web, vous devez obtenir et installer un certificat signé par une autorité de sécurité approuvée.</span><span class="sxs-lookup"><span data-stu-id="43dc9-119">To secure communication between the clients and the web services, you have to obtain and install a certificate that a trusted security authority signed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="43dc9-120">Services de rôle de serveur Web</span><span class="sxs-lookup"><span data-stu-id="43dc9-120">Web Server Role Services</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="43dc9-121">Fonctionnalités HTTP communes:</span><span class="sxs-lookup"><span data-stu-id="43dc9-121">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="43dc9-122">Contenu statique</span><span class="sxs-lookup"><span data-stu-id="43dc9-122">Static Content</span></span></p></li>
<li><p><span data-ttu-id="43dc9-123">Document par défaut</span><span class="sxs-lookup"><span data-stu-id="43dc9-123">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="43dc9-124">Développement d’applications:</span><span class="sxs-lookup"><span data-stu-id="43dc9-124">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="43dc9-125">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="43dc9-125">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="43dc9-126">Extensibilité .NET</span><span class="sxs-lookup"><span data-stu-id="43dc9-126">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="43dc9-127">Extensions ISAPI</span><span class="sxs-lookup"><span data-stu-id="43dc9-127">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="43dc9-128">Filtres ISAPI</span><span class="sxs-lookup"><span data-stu-id="43dc9-128">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="43dc9-129">Sûreté</span><span class="sxs-lookup"><span data-stu-id="43dc9-129">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="43dc9-130">Authentification Windows</span><span class="sxs-lookup"><span data-stu-id="43dc9-130">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="43dc9-131">Filtrage de requête</span><span class="sxs-lookup"><span data-stu-id="43dc9-131">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="43dc9-132">Fonctionnalités de Windows Server</span><span class="sxs-lookup"><span data-stu-id="43dc9-132">Windows Server Features</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="43dc9-133">Fonctionnalités de .NET Framework 3.5.1:</span><span class="sxs-lookup"><span data-stu-id="43dc9-133">.NET Framework 3.5.1 features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="43dc9-134">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="43dc9-134">.NET Framework 3.5.1</span></span></p></li>
<li><p><span data-ttu-id="43dc9-135">Activation WCF</span><span class="sxs-lookup"><span data-stu-id="43dc9-135">WCF Activation</span></span></p>
<ul>
<li><p><span data-ttu-id="43dc9-136">Activation HTTP</span><span class="sxs-lookup"><span data-stu-id="43dc9-136">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="43dc9-137">Activation non HTTP</span><span class="sxs-lookup"><span data-stu-id="43dc9-137">Non-HTTP Activation</span></span></p></li>
</ul></li>
</ul>
<p><strong><span data-ttu-id="43dc9-138">Service d’activation de processus Windows:</span><span class="sxs-lookup"><span data-stu-id="43dc9-138">Windows Process Activation Service:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="43dc9-139">Modèle de processus</span><span class="sxs-lookup"><span data-stu-id="43dc9-139">Process Model</span></span></p></li>
<li><p><span data-ttu-id="43dc9-140">Environnement .NET</span><span class="sxs-lookup"><span data-stu-id="43dc9-140">.NET Environment</span></span></p></li>
<li><p><span data-ttu-id="43dc9-141">API de configuration</span><span class="sxs-lookup"><span data-stu-id="43dc9-141">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="43dc9-142">Remarque</span><span class="sxs-lookup"><span data-stu-id="43dc9-142">Note</span></span>**  
<span data-ttu-id="43dc9-143">Pour obtenir la liste des systèmes d’exploitation pris en charge, voir [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="43dc9-143">For a list of supported operating systems, see [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>



### <span data-ttu-id="43dc9-144">Conditions préalables pour les rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="43dc9-144">Prerequisites for the Compliance and Audit Reports</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="43dc9-145">Prérequises</span><span class="sxs-lookup"><span data-stu-id="43dc9-145">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="43dc9-146">Détails</span><span class="sxs-lookup"><span data-stu-id="43dc9-146">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43dc9-147">Version prise en charge de SQL Server</span><span class="sxs-lookup"><span data-stu-id="43dc9-147">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="43dc9-148"><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,0.</span><span class="sxs-lookup"><span data-stu-id="43dc9-148">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="43dc9-149">Installez SQL Server avec:</span><span class="sxs-lookup"><span data-stu-id="43dc9-149">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="43dc9-150">Assemblage SQL_Latin1_General_CP1_CI_AS</span><span class="sxs-lookup"><span data-stu-id="43dc9-150">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43dc9-151">SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="43dc9-151">SQL Server Reporting Services (SSRS)</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43dc9-152">Droits d’instance SSRS: requis pour l’installation de rapports uniquement si vous installez des bases de données sur un serveur distinct des rapports.</span><span class="sxs-lookup"><span data-stu-id="43dc9-152">SSRS instance rights – required for installing reports only if you are installing databases on a separate server from the reports.</span></span></p></td>
<td align="left"><p><span data-ttu-id="43dc9-153">Droits d’instance requis:</span><span class="sxs-lookup"><span data-stu-id="43dc9-153">Required instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="43dc9-154">Créer des dossiers</span><span class="sxs-lookup"><span data-stu-id="43dc9-154">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="43dc9-155">Publier des rapports</span><span class="sxs-lookup"><span data-stu-id="43dc9-155">Publish Reports</span></span></p></li>
</ul>
<p><span data-ttu-id="43dc9-156">SSRS doit être installé et exécuté lors de l’installation de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="43dc9-156">SSRS must be installed and running during the MBAM Server installation.</span></span> <span data-ttu-id="43dc9-157">Configurez le mode «natif» dans le mode «natif» et non le mode «SharePoint» non configuré.</span><span class="sxs-lookup"><span data-stu-id="43dc9-157">Configure SSRS in “native” mode and not in unconfigured or “SharePoint” mode.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="43dc9-158">Conditions préalables pour la base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="43dc9-158">Prerequisites for the Recovery Database</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="43dc9-159">Prérequises</span><span class="sxs-lookup"><span data-stu-id="43dc9-159">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="43dc9-160">Détails</span><span class="sxs-lookup"><span data-stu-id="43dc9-160">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43dc9-161">Version prise en charge de SQL Server</span><span class="sxs-lookup"><span data-stu-id="43dc9-161">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="43dc9-162"><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,0.</span><span class="sxs-lookup"><span data-stu-id="43dc9-162">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="43dc9-163">Installez SQL Server avec:</span><span class="sxs-lookup"><span data-stu-id="43dc9-163">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="43dc9-164">Assemblage SQL_Latin1_General_CP1_CI_AS</span><span class="sxs-lookup"><span data-stu-id="43dc9-164">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
<li><p><span data-ttu-id="43dc9-165">Outils de gestion SQL Server</span><span class="sxs-lookup"><span data-stu-id="43dc9-165">SQL Server Management Tools</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43dc9-166">Autorisations SQL Server requises</span><span class="sxs-lookup"><span data-stu-id="43dc9-166">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="43dc9-167">Autorisations requises:</span><span class="sxs-lookup"><span data-stu-id="43dc9-167">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="43dc9-168">Rôles de serveurs de connexion d’instances SQL:</span><span class="sxs-lookup"><span data-stu-id="43dc9-168">SQL instance Login Server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="43dc9-169">rôles</span><span class="sxs-lookup"><span data-stu-id="43dc9-169">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="43dc9-170">processadmin</span><span class="sxs-lookup"><span data-stu-id="43dc9-170">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="43dc9-171">Droits d’instance de SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="43dc9-171">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="43dc9-172">Créer des dossiers</span><span class="sxs-lookup"><span data-stu-id="43dc9-172">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="43dc9-173">Publier des rapports</span><span class="sxs-lookup"><span data-stu-id="43dc9-173">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43dc9-174">Fonctionnalité facultative-installation du chiffrement de données (TDE) en option disponible dans SQL Server</span><span class="sxs-lookup"><span data-stu-id="43dc9-174">Optional - Install Transparent Data Encryption (TDE) feature available in SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="43dc9-175">La TDE SQL Server vous permet de chiffrer et de déchiffrer les données et les fichiers journaux en temps réel, ce qui peut vous aider à vous conformer à de nombreux lois, règlements et directives établis dans divers secteurs d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="43dc9-175">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with many laws, regulations, and guidelines established in various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="43dc9-176">Remarque</span><span class="sxs-lookup"><span data-stu-id="43dc9-176">Note</span></span></strong><br/><p><span data-ttu-id="43dc9-177">TDE exécute le déchiffrement en temps réel des informations de la base de données, ce qui signifie que si le compte sous lequel vous vous êtes connecté dispose de l’autorisation de la base de données pendant que vous consultez les informations de la clé de récupération dans les tables SQL Server, les informations de la clé de récupération sont affichées.</span><span class="sxs-lookup"><span data-stu-id="43dc9-177">TDE performs real-time decryption of database information, which means that, if the account under which you are logged on has permissions to the database while you are viewing the recovery key information in the SQL Server tables, the recovery key information is visible.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="43dc9-178">En savoir plus sur TDE: MBAM des considérations en matière de <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> sécurité 2,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="43dc9-178">More about TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)">MBAM 2.0 Security Considerations</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="43dc9-179">Conditions préalables pour la base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="43dc9-179">Prerequisites for the Compliance and Audit Database</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="43dc9-180">Prérequises</span><span class="sxs-lookup"><span data-stu-id="43dc9-180">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="43dc9-181">Détails</span><span class="sxs-lookup"><span data-stu-id="43dc9-181">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43dc9-182">Version prise en charge de SQL Server</span><span class="sxs-lookup"><span data-stu-id="43dc9-182">Supported version of SQL Server</span></span></p>
<p><span data-ttu-id="43dc9-183"><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,0.</span><span class="sxs-lookup"><span data-stu-id="43dc9-183">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="43dc9-184">Installez SQL Server avec:</span><span class="sxs-lookup"><span data-stu-id="43dc9-184">Install SQL Server with:</span></span></p>
<ul>
<li><p><span data-ttu-id="43dc9-185">Assemblage SQL_Latin1_General_CP1_CI_AS</span><span class="sxs-lookup"><span data-stu-id="43dc9-185">SQL_Latin1_General_CP1_CI_AS collation</span></span></p></li>
<li><p><span data-ttu-id="43dc9-186">Outils de gestion SQL Server</span><span class="sxs-lookup"><span data-stu-id="43dc9-186">SQL Server Management Tools</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43dc9-187">Autorisations SQL Server requises</span><span class="sxs-lookup"><span data-stu-id="43dc9-187">Required SQL Server permissions</span></span></p></td>
<td align="left"><p><span data-ttu-id="43dc9-188">Autorisations requises:</span><span class="sxs-lookup"><span data-stu-id="43dc9-188">Required permissions:</span></span></p>
<ul>
<li><p><span data-ttu-id="43dc9-189">Rôles de serveurs de connexion d’instances SQL:</span><span class="sxs-lookup"><span data-stu-id="43dc9-189">SQL instance Login Server roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="43dc9-190">rôles</span><span class="sxs-lookup"><span data-stu-id="43dc9-190">dbcreator</span></span></p></li>
<li><p><span data-ttu-id="43dc9-191">processadmin</span><span class="sxs-lookup"><span data-stu-id="43dc9-191">processadmin</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="43dc9-192">Droits d’instance de SQL Server Reporting Services:</span><span class="sxs-lookup"><span data-stu-id="43dc9-192">SQL Server Reporting Services instance rights:</span></span></p>
<ul>
<li><p><span data-ttu-id="43dc9-193">Créer des dossiers</span><span class="sxs-lookup"><span data-stu-id="43dc9-193">Create Folders</span></span></p></li>
<li><p><span data-ttu-id="43dc9-194">Publier des rapports</span><span class="sxs-lookup"><span data-stu-id="43dc9-194">Publish Reports</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43dc9-195">Fonctionnalité facultative d’installation du chiffrement de données (TDE) dans SQL Server.</span><span class="sxs-lookup"><span data-stu-id="43dc9-195">Optional - Install Transparent Data Encryption (TDE) feature in SQL Server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="43dc9-196">La TDE SQL Server vous permet de chiffrer et de déchiffrer les données et les fichiers journaux en temps réel, ce qui peut vous aider à vous conformer à de nombreux lois, règlements et directives établis dans divers secteurs d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="43dc9-196">The TDE SQL Server feature performs real-time I/O encryption and decryption of the data and log files, which can help you to comply with many laws, regulations, and guidelines established in various industries.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="43dc9-197">Remarque</span><span class="sxs-lookup"><span data-stu-id="43dc9-197">Note</span></span></strong><br/><p><span data-ttu-id="43dc9-198">TDE exécute le déchiffrement en temps réel des informations de la base de données, ce qui signifie que si le compte sous lequel vous vous êtes connecté dispose de l’autorisation de la base de données pendant que vous consultez les informations de la clé de récupération dans les tables SQL Server, les informations de la clé de récupération sont affichées.</span><span class="sxs-lookup"><span data-stu-id="43dc9-198">TDE performs real-time decryption of database information, which means that, if the account under which you are logged on has permissions to the database while you are viewing the recovery key information in the SQL Server tables, the recovery key information is visible.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="43dc9-199">En savoir plus sur TDE: MBAM des considérations en matière de <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> sécurité 2,0</span><span class="sxs-lookup"><span data-stu-id="43dc9-199">More about TDE: <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)">MBAM 2.0 Security Considerations</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43dc9-200">Les services du moteur de base de données SQL Server doivent être installés et exécutés lors de l’installation de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="43dc9-200">SQL Server must have Database Engine Services installed and running during MBAM Server installation.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43dc9-201">Le service de l’agent SQL Server doit être en cours d’exécution et configuré pour démarrer automatiquement sur les instances sélectionnées de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="43dc9-201">The SQL Server Agent service must be running and set to auto-start on the selected instances of SQL Server.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="43dc9-202">Conditions préalables pour le portail libre-service</span><span class="sxs-lookup"><span data-stu-id="43dc9-202">Prerequisites for the Self-Service Portal</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="43dc9-203">Prérequises</span><span class="sxs-lookup"><span data-stu-id="43dc9-203">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="43dc9-204">Détails</span><span class="sxs-lookup"><span data-stu-id="43dc9-204">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43dc9-205">Version prise en charge de Windows Server</span><span class="sxs-lookup"><span data-stu-id="43dc9-205">Supported version of Windows Server</span></span></p>
<p><span data-ttu-id="43dc9-206"><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,0.</span><span class="sxs-lookup"><span data-stu-id="43dc9-206">See <a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">MBAM 2.0 Supported Configurations</a> for supported versions.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43dc9-207">ASP.NET MVC 2,0</span><span class="sxs-lookup"><span data-stu-id="43dc9-207">ASP.NET MVC 2.0</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392270" data-raw-source="[ASP.NET MVC 2 download](https://go.microsoft.com/fwlink/?LinkId=392270)"><span data-ttu-id="43dc9-208">Télécharger ASP.NET MVC 2</span><span class="sxs-lookup"><span data-stu-id="43dc9-208">ASP.NET MVC 2 download</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="43dc9-209">Outils de gestion IIS de service Web</span><span class="sxs-lookup"><span data-stu-id="43dc9-209">Web Service IIS Management Tools</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="43dc9-210">Conditions préalables pour les clients MBAM</span><span class="sxs-lookup"><span data-stu-id="43dc9-210">Prerequisites for MBAM Clients</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="43dc9-211">Prérequises</span><span class="sxs-lookup"><span data-stu-id="43dc9-211">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="43dc9-212">Détails</span><span class="sxs-lookup"><span data-stu-id="43dc9-212">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="43dc9-213">Les clients Windows 7 </strong> - doivent disposer d’une fonctionnalité de module de plateforme sécurisée (TPM) uniquement.</span><span class="sxs-lookup"><span data-stu-id="43dc9-213">Windows 7 clients only</strong> - must have Trusted Platform Module (TPM) capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="43dc9-214">La version du module de plateforme sécurisée doit être 1,2 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="43dc9-214">TPM version must be 1.2 or later.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="43dc9-215">Le processeur du TPM doit être activé dans le BIOS et être Resettable du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="43dc9-215">The TPM chip must be turned on in the BIOS and be resettable from the operating system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="43dc9-216">Pour plus d’informations, consultez la documentation relative au BIOS.</span><span class="sxs-lookup"><span data-stu-id="43dc9-216">For more information, see the BIOS documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="43dc9-217">Clients Windows 8 uniquement </strong> : pour permettre à MBAM de stocker et de gérer les clés de récupération du module de plateforme sécurisée: la mise en service automatique du module de plateforme sécurisée doit être désactivée, et MBAM doit être défini en tant que propriétaire du TPM avant le déploiement d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="43dc9-217">Windows 8 clients only</strong>: To have MBAM store and manage the TPM recovery keys: TPM auto-provisioning must be turned off, and MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span> <span data-ttu-id="43dc9-218">Pour désactiver la mise en service automatique du module de plateforme sécurisée, voir <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</span><span class="sxs-lookup"><span data-stu-id="43dc9-218">To turn off TPM auto-provisioning, see <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)">Disable-TpmAutoProvisioning</a>.</span></span></p>
<ul>
<li><p><span data-ttu-id="43dc9-219">La mise en service automatique du module de plateforme sécurisée doit être désactivée.</span><span class="sxs-lookup"><span data-stu-id="43dc9-219">TPM auto-provisioning must be turned off.</span></span></p></li>
<li><p><span data-ttu-id="43dc9-220">MBAM doit être défini en tant que propriétaire du TPM avant le déploiement d’MBAM.</span><span class="sxs-lookup"><span data-stu-id="43dc9-220">MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="43dc9-221">Pour désactiver la mise en service automatique du module de plateforme sécurisée, voir <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</span><span class="sxs-lookup"><span data-stu-id="43dc9-221">To turn off TPM auto-provisioning, see <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)">Disable-TpmAutoProvisioning</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="43dc9-222">Remarque</span><span class="sxs-lookup"><span data-stu-id="43dc9-222">Note</span></span></strong><br/><p><span data-ttu-id="43dc9-223">Assurez-vous que le clavier, la vidéo ou la souris sont directement connectés et ne sont pas gérés par le biais d’un clavier, d’une vidéo ou d’un commutateur de souris (KVM).</span><span class="sxs-lookup"><span data-stu-id="43dc9-223">Ensure that the keyboard, video, or mouse are directly connected and not managed through a keyboard, video, or mouse (KVM) switch.</span></span> <span data-ttu-id="43dc9-224">Un commutateur KVM peut interférer avec la capacité de l’ordinateur à détecter la présence physique du matériel.</span><span class="sxs-lookup"><span data-stu-id="43dc9-224">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="43dc9-225">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="43dc9-225">Related topics</span></span>


[<span data-ttu-id="43dc9-226">Planification du déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="43dc9-226">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="43dc9-227">Configurations prises en charge par MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="43dc9-227">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)









