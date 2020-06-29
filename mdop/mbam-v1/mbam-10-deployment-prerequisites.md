---
title: Conditions préalables au déploiement de MBAM1.0
description: Conditions préalables au déploiement de MBAM1.0
author: dansimp
ms.assetid: bd9e1010-7d25-43e7-8dc6-b521226a659d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ed14343d37a859364bcabbe6ca72c041502a23c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809491"
---
# <span data-ttu-id="93da2-103">Conditions préalables au déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="93da2-103">MBAM 1.0 Deployment Prerequisites</span></span>


<span data-ttu-id="93da2-104">Avant de commencer la configuration de l’administration et de la surveillance de BitLocker (MBAM) Microsoft, assurez-vous que vous remplissez les conditions préalables nécessaires pour installer le produit.</span><span class="sxs-lookup"><span data-stu-id="93da2-104">Before you begin the Microsoft BitLocker Administration and Monitoring (MBAM) Setup, make sure that you meet the necessary prerequisites to install the product.</span></span> <span data-ttu-id="93da2-105">Cette section contient des informations pour vous aider à préparer votre environnement informatique avant de déployer les clients MBAM et les fonctionnalités du serveur.</span><span class="sxs-lookup"><span data-stu-id="93da2-105">This section contains information to help you successfully prepare your computing environment before you deploy the MBAM Clients and Server features.</span></span>

## <span data-ttu-id="93da2-106">Conditions préalables à l’installation pour les fonctionnalités du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="93da2-106">Installation prerequisites for MBAM Server features</span></span>


<span data-ttu-id="93da2-107">Chacune des fonctionnalités du serveur MBAM possède des éléments requis spécifiques qui doivent être satisfaits pour pouvoir être installés correctement.</span><span class="sxs-lookup"><span data-stu-id="93da2-107">Each of the MBAM server features has specific prerequisites that must be met before they can be successfully installed.</span></span> <span data-ttu-id="93da2-108">La configuration de MBAM vérifie si toutes les conditions préalables sont remplies avant le démarrage de l’installation.</span><span class="sxs-lookup"><span data-stu-id="93da2-108">MBAM Setup verifies if all prerequisites are met before the installation starts.</span></span>

### <span data-ttu-id="93da2-109">Conditions préalables à l’installation du serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="93da2-109">Installation prerequisites for Administration and Monitoring Server</span></span>

<span data-ttu-id="93da2-110">Le tableau suivant répertorie les conditions préalables à l’installation du serveur d’administration et de surveillance MBAM:</span><span class="sxs-lookup"><span data-stu-id="93da2-110">The following table contains the installation prerequisites for the MBAM Administration and Monitoring Server:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="93da2-111">Prérequises</span><span class="sxs-lookup"><span data-stu-id="93da2-111">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="93da2-112">Détails</span><span class="sxs-lookup"><span data-stu-id="93da2-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="93da2-113">Rôle du serveur Windows ServerWeb</span><span class="sxs-lookup"><span data-stu-id="93da2-113">Windows ServerWeb Server Role</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="93da2-114">Ce rôle doit être ajouté au système d’exploitation du serveur pris en charge pour la fonctionnalité d’administration et de contrôle du serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="93da2-114">This role must be added to a server operating system supported for the mbam Administration and Monitoring Server feature.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="93da2-115">Outils de gestion du serveur Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="93da2-115">Web Server (IIS) Management Tools</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="93da2-116">Outils et scripts de gestion IIS</span><span class="sxs-lookup"><span data-stu-id="93da2-116">IIS Management Scripts and Tools</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="93da2-117">Services de rôle de serveur Web</span><span class="sxs-lookup"><span data-stu-id="93da2-117">Web Server Role Services</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="93da2-118">Fonctionnalités HTTP communes:</span><span class="sxs-lookup"><span data-stu-id="93da2-118">Common HTTP Features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="93da2-119">Contenu statique</span><span class="sxs-lookup"><span data-stu-id="93da2-119">Static Content</span></span></p></li>
<li><p><span data-ttu-id="93da2-120">Document par défaut</span><span class="sxs-lookup"><span data-stu-id="93da2-120">Default Document</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="93da2-121">Développement d’applications:</span><span class="sxs-lookup"><span data-stu-id="93da2-121">Application Development:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="93da2-122">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="93da2-122">ASP.NET</span></span></p></li>
<li><p><span data-ttu-id="93da2-123">Extensibilité .NET</span><span class="sxs-lookup"><span data-stu-id="93da2-123">.NET Extensibility</span></span></p></li>
<li><p><span data-ttu-id="93da2-124">Extensions ISAPI</span><span class="sxs-lookup"><span data-stu-id="93da2-124">ISAPI Extensions</span></span></p></li>
<li><p><span data-ttu-id="93da2-125">Filtres ISAPI</span><span class="sxs-lookup"><span data-stu-id="93da2-125">ISAPI Filters</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="93da2-126">Sûreté</span><span class="sxs-lookup"><span data-stu-id="93da2-126">Security:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="93da2-127">Authentification Windows</span><span class="sxs-lookup"><span data-stu-id="93da2-127">Windows Authentication</span></span></p></li>
<li><p><span data-ttu-id="93da2-128">Filtrage de requête</span><span class="sxs-lookup"><span data-stu-id="93da2-128">Request Filtering</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="93da2-129">Fonctionnalités de Windows Server</span><span class="sxs-lookup"><span data-stu-id="93da2-129">Windows Server Features</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="93da2-130">Fonctionnalités de Microsoft .NET Framework 3.5.1:</span><span class="sxs-lookup"><span data-stu-id="93da2-130">Microsoft .NET Framework 3.5.1 features:</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="93da2-131">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="93da2-131">.NET Framework 3.5.1</span></span></p></li>
<li><p><span data-ttu-id="93da2-132">Activation WCF</span><span class="sxs-lookup"><span data-stu-id="93da2-132">WCF Activation</span></span></p>
<ul>
<li><p><span data-ttu-id="93da2-133">Activation HTTP</span><span class="sxs-lookup"><span data-stu-id="93da2-133">HTTP Activation</span></span></p></li>
<li><p><span data-ttu-id="93da2-134">Activation non HTTP</span><span class="sxs-lookup"><span data-stu-id="93da2-134">Non-HTTP Activation</span></span></p></li>
</ul></li>
</ul>
<p><strong><span data-ttu-id="93da2-135">Service d'activation des processus Windows</span><span class="sxs-lookup"><span data-stu-id="93da2-135">Windows Process Activation Service</span></span></strong></p>
<ul>
<li><p><span data-ttu-id="93da2-136">Modèle de processus</span><span class="sxs-lookup"><span data-stu-id="93da2-136">Process Model</span></span></p></li>
<li><p><span data-ttu-id="93da2-137">Environnement .NET</span><span class="sxs-lookup"><span data-stu-id="93da2-137">.NET Environment</span></span></p></li>
<li><p><span data-ttu-id="93da2-138">API de configuration</span><span class="sxs-lookup"><span data-stu-id="93da2-138">Configuration APIs</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="93da2-139">**Remarques**  Pour obtenir la liste des systèmes d’exploitation pris en charge, voir [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="93da2-139">**Note** For a list of supported operating systems, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

### <span data-ttu-id="93da2-140">Conditions préalables à l’installation des rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="93da2-140">Installation prerequisites for the Compliance and Audit Reports</span></span>

<span data-ttu-id="93da2-141">Les rapports de conformité et d’audit doivent être installés sur une version prise en charge de SQLServer.</span><span class="sxs-lookup"><span data-stu-id="93da2-141">The Compliance and Audit Reports must be installed on a supported version of SQLServer.</span></span> <span data-ttu-id="93da2-142">Les conditions préalables à l’installation de cette fonctionnalité incluent SQL Server Reporting Services (SSRS).</span><span class="sxs-lookup"><span data-stu-id="93da2-142">Installation prerequisites for this feature include SQL Server Reporting Services (SSRS).</span></span>

<span data-ttu-id="93da2-143">SSRS doit être installé et exécuté lors de l’installation de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="93da2-143">SSRS must be installed and running during MBAM server installation.</span></span> <span data-ttu-id="93da2-144">SSRS doit également être configuré en mode «natif», pas dans le mode «non configuré» ou «SharePoint».</span><span class="sxs-lookup"><span data-stu-id="93da2-144">SSRS should also be configured in “native” mode, not in the “unconfigured” or “SharePoint” mode.</span></span>

<span data-ttu-id="93da2-145">**Remarques**  Pour obtenir la liste des systèmes d’exploitation et versions SQLServer pris en charge, voir [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="93da2-145">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

### <span data-ttu-id="93da2-146">Conditions préalables à l’installation de la base de données de récupération et de matériel</span><span class="sxs-lookup"><span data-stu-id="93da2-146">Installation prerequisites for the Recovery and Hardware Database</span></span>

<span data-ttu-id="93da2-147">La base de données de récupération et de matériel doit être installée sur une version prise en charge de SQLServer.</span><span class="sxs-lookup"><span data-stu-id="93da2-147">The Recovery and Hardware Database must be installed on a supported version of SQLServer.</span></span>

<span data-ttu-id="93da2-148">Les services du moteur de base de données SQL Server doivent être installés et exécutés pendant l’installation du serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="93da2-148">SQL Server must have Database Engine Services installed and running during the MBAM server installation.</span></span> <span data-ttu-id="93da2-149">La fonction de chiffrement de données (TDE) doit être activée.</span><span class="sxs-lookup"><span data-stu-id="93da2-149">The Transparent Data Encryption (TDE) feature must be enabled.</span></span>

<span data-ttu-id="93da2-150">**Remarques**  Pour obtenir la liste des systèmes d’exploitation et versions SQLServer pris en charge, voir [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="93da2-150">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

<span data-ttu-id="93da2-151">La fonctionnalité SQLServer TDE permet d’effectuer le chiffrement et le déchiffrement des données et des fichiers journaux en temps réel.</span><span class="sxs-lookup"><span data-stu-id="93da2-151">The TDE SQLServer feature performs real-time input/output (I/O) encryption and decryption of the data and log files.</span></span> <span data-ttu-id="93da2-152">TDE protège les données «au repos», qui incluent les données et les fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="93da2-152">TDE protects data that is "at rest,” which include the data and the log files.</span></span> <span data-ttu-id="93da2-153">Elle offre la possibilité de se conformer à de nombreuses lois, règlements et recommandations définis dans divers secteurs.</span><span class="sxs-lookup"><span data-stu-id="93da2-153">It provides the ability to comply with many laws, regulations, and guidelines that are established in various industries.</span></span>

<span data-ttu-id="93da2-154">**Remarques**  Dans la mesure où TDE effectue le déchiffrement en temps réel des informations de la base de données, les informations de la clé de récupération seront visibles si le compte sous lequel vous vous êtes connecté dispose des autorisations de la base de données lorsque vous affichez les tables SQL informations clés de récupération.</span><span class="sxs-lookup"><span data-stu-id="93da2-154">**Note** Because TDE performs real-time decryption of database information, the recovery key information will be visible if the account under which you are logged in has permissions to the database when you view the recovery key information SQL tables.</span></span>

 

### <span data-ttu-id="93da2-155">Conditions préalables à l’installation de la base de données de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="93da2-155">Installation prerequisites for the Compliance and Audit Database</span></span>

<span data-ttu-id="93da2-156">La base de données d’audit et de conformité doit être installée sur une version prise en charge de SQLServer.</span><span class="sxs-lookup"><span data-stu-id="93da2-156">The Compliance and Audit Database must be installed on a supported version of SQLServer.</span></span>

<span data-ttu-id="93da2-157">Les services du moteur de base de données SQL Server doivent être installés et exécutés lors de l’installation de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="93da2-157">SQL Server must have Database Engine Services installed and running during MBAM server installation.</span></span>

<span data-ttu-id="93da2-158">**Remarques**  Pour obtenir la liste des systèmes d’exploitation et versions SQLServer pris en charge, voir [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="93da2-158">**Note** For a list of supported operating systems and SQLServer versions, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

## <span data-ttu-id="93da2-159">Conditions préalables à l’installation pour les clients MBAM</span><span class="sxs-lookup"><span data-stu-id="93da2-159">Installation prerequisites for MBAM Clients</span></span>


<span data-ttu-id="93da2-160">Pour pouvoir commencer l’installation du client MBAM, vous devez disposer des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="93da2-160">The necessary prerequisites that you must meet before you begin the MBAM Client installation are the following:</span></span>

-   <span data-ttu-id="93da2-161">Fonctionnalité du module de plateforme sécurisée (TPM) v 1.2</span><span class="sxs-lookup"><span data-stu-id="93da2-161">Trusted Platform Module (TPM) v1.2 capability</span></span>

-   <span data-ttu-id="93da2-162">Le processeur du TPM doit être activé dans le BIOS et il doit être Resettable du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="93da2-162">The TPM chip must be turned on in the BIOS and it must be resettable from the operating system.</span></span> <span data-ttu-id="93da2-163">Pour plus d’informations, consultez la documentation relative au BIOS.</span><span class="sxs-lookup"><span data-stu-id="93da2-163">For more information, see the BIOS documentation.</span></span>

<span data-ttu-id="93da2-164">**Avertissement**  Assurez-vous que le clavier, la souris et la vidéo sont directement connectés à l’ordinateur au lieu d’un clavier, d’une vidéo et d’un commutateur de souris (KVM).</span><span class="sxs-lookup"><span data-stu-id="93da2-164">**Warning** Ensure that the keyboard, mouse, and video are directly connected to the computer, instead of to a keyboard, video, mouse (KVM) switch.</span></span> <span data-ttu-id="93da2-165">Un commutateur KVM peut interférer avec la capacité de l’ordinateur à détecter la présence physique du matériel.</span><span class="sxs-lookup"><span data-stu-id="93da2-165">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span>

 

## <span data-ttu-id="93da2-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="93da2-166">Related topics</span></span>


[<span data-ttu-id="93da2-167">Planification du déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="93da2-167">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="93da2-168">Configurations prises en charge par MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="93da2-168">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)

 

 





