---
title: Comment configurer les bases de données MBAM2.5
description: Comment configurer les bases de données MBAM2.5
author: dansimp
ms.assetid: 66e1c81b-f785-4398-9175-bb5f112c2a35
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c11cb58d8fd9266bd0322e4cf9aa96256b7fbb6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811867"
---
# <span data-ttu-id="b53eb-103">Comment configurer les bases de données MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="b53eb-103">How to Configure the MBAM 2.5 Databases</span></span>


<span data-ttu-id="b53eb-104">Cet article décrit la configuration de la base de données de compatibilité et d’audit de Microsoft BitLocker (MBAM 2,5) et de la base de données d’audit et de la base de données de récupération en utilisant les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="b53eb-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Compliance and Audit Database and the Recovery Database by using:</span></span>

-   <span data-ttu-id="b53eb-105">Une applet de cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b53eb-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="b53eb-106">Assistant Configuration de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="b53eb-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="b53eb-107">Les instructions sont basées sur l’architecture recommandée dans [architecture de haut niveau pour MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="b53eb-107">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="b53eb-108">Avant de démarrer la configuration:</span><span class="sxs-lookup"><span data-stu-id="b53eb-108">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b53eb-109">Étape</span><span class="sxs-lookup"><span data-stu-id="b53eb-109">Step</span></span></th>
<th align="left"><span data-ttu-id="b53eb-110">Où obtenir des instructions</span><span class="sxs-lookup"><span data-stu-id="b53eb-110">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b53eb-111">Passez en revue l’architecture recommandée pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="b53eb-111">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="b53eb-112">Architecture de hautniveau pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="b53eb-112">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b53eb-113">Passez en revue les configurations prises en charge pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="b53eb-113">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="b53eb-114">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="b53eb-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b53eb-115">Remplissez les conditions préalables requises sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="b53eb-115">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="b53eb-116">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</span><span class="sxs-lookup"><span data-stu-id="b53eb-116">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="b53eb-117">MBAM 2,5 requis par le serveur qui ne s’appliquent qu’à la topologie d’intégration de Configuration Manager </a> (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="b53eb-117">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b53eb-118">Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous envisagez de configurer une fonctionnalité de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="b53eb-118">Install the MBAM Server software on each server where you plan to configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b53eb-119">Remarque</span><span class="sxs-lookup"><span data-stu-id="b53eb-119">Note</span></span></strong><br/><p><span data-ttu-id="b53eb-120">Vous pouvez installer les bases de données sur un ordinateur distant SQL Server à l’aide de Windows PowerShell ou d’un package d’application de couche de données (DAC) exporté.</span><span class="sxs-lookup"><span data-stu-id="b53eb-120">You can install the databases to a remote SQL Server computer by using Windows PowerShell or an exported data-tier application (DAC) package.</span></span> <span data-ttu-id="b53eb-121">Pour plus d’informations sur les packages DAC, voir <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> applications à couches de données </a> .</span><span class="sxs-lookup"><span data-stu-id="b53eb-121">For more information about DAC packages, see <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)">Data-tier Applications</a>.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="b53eb-122">Installation du logiciel serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="b53eb-122">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b53eb-123">Passez en revue la configuration requise pour l’utilisation de Windows PowerShell Si vous envisagez d’utiliser des cmdlets Windows PowerShell pour configurer les fonctionnalités du serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="b53eb-123">Review the prerequisites for using Windows PowerShell if you plan to use Windows PowerShell cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="b53eb-124">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b53eb-124">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="b53eb-125">Pour configurer la base de données à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b53eb-125">To configure the databases by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="b53eb-126">Avant de commencer la configuration, reportez-vous à la rubrique [Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) pour consulter les conditions préalables à l’utilisation de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b53eb-126">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="b53eb-127">Utilisez l’applet de cmdlet Windows PowerShell **Enable-MbamDatabase** pour configurer les bases de données.</span><span class="sxs-lookup"><span data-stu-id="b53eb-127">Use the **Enable-MbamDatabase** Windows PowerShell cmdlet to configure the databases.</span></span> <span data-ttu-id="b53eb-128">Pour obtenir des informations sur cette applet de cmdlet Windows PowerShell, tapez **Get-Help-MbamDatabase**.</span><span class="sxs-lookup"><span data-stu-id="b53eb-128">To get information about this Windows PowerShell cmdlet, type **Get-Help Enable-MbamDatabase**.</span></span>

**<span data-ttu-id="b53eb-129">Pour configurer la conformité et la base de données d’audit à l’aide de l’Assistant</span><span class="sxs-lookup"><span data-stu-id="b53eb-129">To configure the Compliance and Audit Database by using the wizard</span></span>**

1. <span data-ttu-id="b53eb-130">Sur le serveur sur lequel vous voulez configurer les bases de données, démarrez l’Assistant **configuration de MBAM Server** .</span><span class="sxs-lookup"><span data-stu-id="b53eb-130">On the server where you want to configure the databases, start the **MBAM Server Configuration** wizard.</span></span> <span data-ttu-id="b53eb-131">Vous pouvez sélectionner **MBAM de configuration de serveur** dans le menu **Démarrer** pour ouvrir l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="b53eb-131">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="b53eb-132">Cliquez **sur Ajouter de nouvelles fonctionnalités**, sélectionnez **conformité et audit** et **base**de données d’audit, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="b53eb-132">Click **Add New Features**, select **Compliance and Audit Database** and **Recovery Database**, and then click **Next**.</span></span> <span data-ttu-id="b53eb-133">L’Assistant vérifie que toutes les conditions préalables pour les bases de données sont remplies.</span><span class="sxs-lookup"><span data-stu-id="b53eb-133">The wizard checks that all prerequisites for the databases have been met.</span></span>

3. <span data-ttu-id="b53eb-134">Si la vérification de la configuration requise est réussie, cliquez sur **suivant** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="b53eb-134">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="b53eb-135">Dans le cas contraire, résolvez les conditions préalables manquantes, puis cliquez **à nouveau sur vérifier les conditions préalables**.</span><span class="sxs-lookup"><span data-stu-id="b53eb-135">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4. <span data-ttu-id="b53eb-136">À l’aide des descriptions suivantes, entrez les valeurs de champ dans l’Assistant:</span><span class="sxs-lookup"><span data-stu-id="b53eb-136">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="b53eb-137">Champ</span><span class="sxs-lookup"><span data-stu-id="b53eb-137">Field</span></span></th>
   <th align="left"><span data-ttu-id="b53eb-138">Description</span><span class="sxs-lookup"><span data-stu-id="b53eb-138">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b53eb-139">Nom SQL Server</span><span class="sxs-lookup"><span data-stu-id="b53eb-139">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b53eb-140">Nom du serveur sur lequel vous configurez la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="b53eb-140">Name of the server where you are configuring the Compliance and Audit Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="b53eb-141">Remarque</span><span class="sxs-lookup"><span data-stu-id="b53eb-141">Note</span></span></strong><br/><p><span data-ttu-id="b53eb-142">Vous devez ajouter une exception dans l’ordinateur de la base de données d’audit et de conformité pour activer le trafic entrant sur le port Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b53eb-142">You must add an exception on the Compliance and Audit Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="b53eb-143">Le numéro de port par défaut est 1433.</span><span class="sxs-lookup"><span data-stu-id="b53eb-143">The default port number is 1433.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b53eb-144">Instance de base de données SQL Server</span><span class="sxs-lookup"><span data-stu-id="b53eb-144">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b53eb-145">Nom de l’instance de base de données dans laquelle les données d’audit et de conformité seront stockées.</span><span class="sxs-lookup"><span data-stu-id="b53eb-145">Name of the database instance where the compliance and audit data will be stored.</span></span> <span data-ttu-id="b53eb-146">Vous devez également spécifier l’emplacement des informations de la base de données.</span><span class="sxs-lookup"><span data-stu-id="b53eb-146">You must also specify where the database information will be located.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b53eb-147">Nom de la base de données</span><span class="sxs-lookup"><span data-stu-id="b53eb-147">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b53eb-148">Nom de la base de données qui stockera les données de conformité.</span><span class="sxs-lookup"><span data-stu-id="b53eb-148">Name of the database that will store the compliance data.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="b53eb-149">Remarque</span><span class="sxs-lookup"><span data-stu-id="b53eb-149">Note</span></span></strong><br/><p><span data-ttu-id="b53eb-150">Si vous effectuez une mise à niveau à partir d’une version précédente de MBAM, vous devez utiliser le même nom de base de données que le nom utilisé dans votre ancien déploiement.</span><span class="sxs-lookup"><span data-stu-id="b53eb-150">If you are upgrading from a previous version of MBAM, you must use the same database name as the name that was used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b53eb-151">Utilisateur ou groupe d’accès en lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b53eb-151">Read/write access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b53eb-152">Utilisateur ou groupe ayant une autorisation en lecture/écriture à cette base de données pour permettre aux applications Web d’accéder aux données et rapports de cette base de données.</span><span class="sxs-lookup"><span data-stu-id="b53eb-152">Domain user or group that has read/write permission to this database to enable the web applications to access the data and reports in this database.</span></span></p>
   <p><span data-ttu-id="b53eb-153">Si vous entrez un utilisateur dans ce champ, il doit avoir la même valeur que la valeur figurant dans le <strong> champ compte de domaine du pool d’applications de service Web </strong> de la <strong> page configurer des applications Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="b53eb-153">If you enter a user in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
   <p><span data-ttu-id="b53eb-154">Si vous entrez un groupe dans ce champ, la valeur du <strong> champ compte de domaine du pool d’applications de service Web </strong> de la <strong> page configurer des applications Web </strong> doit être membre du groupe que vous entrez dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="b53eb-154">If you enter a group in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b53eb-155">Utilisateur ou groupe d’accès en lecture seule</span><span class="sxs-lookup"><span data-stu-id="b53eb-155">Read-only access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b53eb-156">Nom de l’utilisateur ou du groupe disposant d’une autorisation en lecture seule sur cette base de données pour permettre aux rapports d’accéder aux données de conformité de cette base de données.</span><span class="sxs-lookup"><span data-stu-id="b53eb-156">Name of the user or group that will have read-only permission to this database to enable the reports to access the compliance data in this database.</span></span></p>
   <p><span data-ttu-id="b53eb-157">Si vous entrez un utilisateur dans ce champ, il doit être le même que celui que vous avez spécifié dans le <strong> champ domaine de la base de données de conformité et d’audit </strong> de la <strong> page configurer des rapports </strong> .</span><span class="sxs-lookup"><span data-stu-id="b53eb-157">If you enter a user in this field, it must be the same user as the one you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page.</span></span></p>
   <p><span data-ttu-id="b53eb-158">Si vous entrez un groupe dans ce champ, la valeur que vous spécifiez dans le <strong> champ compte de domaine de la base de données de conformité et d’audit </strong> de la <strong> page configurer des rapports </strong> doit être membre du groupe que vous spécifiez dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="b53eb-158">If you enter a group in this field, the value that you specify in the <strong>Compliance and Audit Database domain account</strong> field on the <strong>Configure Reports</strong> page must be a member of the group that you specify in this field.</span></span></p></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="b53eb-159">Passez à la section suivante pour configurer la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="b53eb-159">Continue to the next section to configure the Recovery Database.</span></span>

**<span data-ttu-id="b53eb-160">Pour configurer la base de données de récupération à l’aide de l’Assistant</span><span class="sxs-lookup"><span data-stu-id="b53eb-160">To configure the Recovery Database by using the wizard</span></span>**

1. <span data-ttu-id="b53eb-161">À l’aide des descriptions suivantes, entrez les valeurs de champ dans l’Assistant:</span><span class="sxs-lookup"><span data-stu-id="b53eb-161">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="b53eb-162">Champ</span><span class="sxs-lookup"><span data-stu-id="b53eb-162">Field</span></span></th>
   <th align="left"><span data-ttu-id="b53eb-163">Description</span><span class="sxs-lookup"><span data-stu-id="b53eb-163">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b53eb-164">Nom SQL Server</span><span class="sxs-lookup"><span data-stu-id="b53eb-164">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b53eb-165">Nom du serveur sur lequel vous configurez la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="b53eb-165">Name of the server where you are configuring the Recovery Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="b53eb-166">Remarque</span><span class="sxs-lookup"><span data-stu-id="b53eb-166">Note</span></span></strong><br/><p><span data-ttu-id="b53eb-167">Vous devez ajouter une exception sur l’ordinateur de base de données de récupération pour activer le trafic entrant sur le port Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b53eb-167">You must add an exception on the Recovery Database computer to enable inbound traffic on the Microsoft SQL Server port.</span></span> <span data-ttu-id="b53eb-168">Le numéro de port par défaut est 1433.</span><span class="sxs-lookup"><span data-stu-id="b53eb-168">The default port number is 1433.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b53eb-169">Instance de base de données SQL Server</span><span class="sxs-lookup"><span data-stu-id="b53eb-169">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b53eb-170">Nom de l’instance de base de données dans laquelle les données de récupération seront stockées.</span><span class="sxs-lookup"><span data-stu-id="b53eb-170">Name of the database instance where the recovery data will be stored.</span></span> <span data-ttu-id="b53eb-171">Vous devez également spécifier l’emplacement des informations de la base de données.</span><span class="sxs-lookup"><span data-stu-id="b53eb-171">You must also specify where the database information will be located.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b53eb-172">Nom de la base de données</span><span class="sxs-lookup"><span data-stu-id="b53eb-172">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b53eb-173">Nom de la base de données qui stockera les données de récupération.</span><span class="sxs-lookup"><span data-stu-id="b53eb-173">Name of the database that will store the recovery data.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="b53eb-174">Remarque</span><span class="sxs-lookup"><span data-stu-id="b53eb-174">Note</span></span></strong><br/><p><span data-ttu-id="b53eb-175">Si vous effectuez une mise à niveau à partir d’une version précédente de MBAM, vous devez utiliser le même nom de base de données que le nom utilisé dans votre ancien déploiement.</span><span class="sxs-lookup"><span data-stu-id="b53eb-175">If you are upgrading from a previous version of MBAM, you must use the same database name as the name that was used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b53eb-176">Utilisateur ou groupe d’accès en lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b53eb-176">Read/write access domain user or group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b53eb-177">Utilisateur ou groupe ayant une autorisation en lecture/écriture à cette base de données pour permettre aux applications Web d’accéder aux données et rapports de cette base de données.</span><span class="sxs-lookup"><span data-stu-id="b53eb-177">Domain user or group that has read/write permission to this database to enable the web applications to access the data and reports in this database.</span></span></p>
   <p><span data-ttu-id="b53eb-178">Si vous entrez un utilisateur dans ce champ, il doit avoir la même valeur que la valeur figurant dans le <strong> champ compte de domaine du pool d’applications de service Web </strong> de la <strong> page configurer des applications Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="b53eb-178">If you enter a user in this field, it must be the same value as the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page.</span></span></p>
   <p><span data-ttu-id="b53eb-179">Si vous entrez un groupe dans ce champ, la valeur du <strong> champ compte de domaine du pool d’applications de service Web </strong> de la <strong> page configurer des applications Web </strong> doit être membre du groupe que vous entrez dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="b53eb-179">If you enter a group in this field, the value in the <strong>Web service application pool domain account</strong> field on the <strong>Configure Web Applications</strong> page must be a member of the group you enter in this field.</span></span></p></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="b53eb-180">Lorsque vous avez terminé, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="b53eb-180">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="b53eb-181">L’Assistant vérifie que toutes les conditions préalables pour les bases de données sont remplies.</span><span class="sxs-lookup"><span data-stu-id="b53eb-181">The wizard checks that all prerequisites for the databases have been met.</span></span>

3. <span data-ttu-id="b53eb-182">Si la vérification de la configuration requise est réussie, cliquez sur **suivant** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="b53eb-182">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="b53eb-183">Dans le cas contraire, résolvez les conditions préalables manquantes, puis cliquez de nouveau sur **suivant** .</span><span class="sxs-lookup"><span data-stu-id="b53eb-183">Otherwise, resolve any missing prerequisites, and then click **Next** again.</span></span>

4. <span data-ttu-id="b53eb-184">Dans la page **Résumé** , passez en revue les fonctionnalités qui seront ajoutées.</span><span class="sxs-lookup"><span data-stu-id="b53eb-184">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="b53eb-185">Remarque</span><span class="sxs-lookup"><span data-stu-id="b53eb-185">Note</span></span>**  
   <span data-ttu-id="b53eb-186">Pour créer un script Windows PowerShell des entrées que vous venez de créer, cliquez sur **Exporter le script PowerShell**, puis enregistrez le script.</span><span class="sxs-lookup"><span data-stu-id="b53eb-186">To create a Windows PowerShell script of the entries that you just made, click **Export PowerShell Script**, and then save the script.</span></span>



5. <span data-ttu-id="b53eb-187">Cliquez sur **Ajouter** pour ajouter les bases de données MBAM sur le serveur, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b53eb-187">Click **Add** to add the MBAM databases on the server, and then click **Close**.</span></span>



## <span data-ttu-id="b53eb-188">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b53eb-188">Related topics</span></span>


[<span data-ttu-id="b53eb-189">Journaux des événements serveur</span><span class="sxs-lookup"><span data-stu-id="b53eb-189">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="b53eb-190">Configuration des composants du serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="b53eb-190">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="b53eb-191">Configuration des rapports MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="b53eb-191">How to Configure the MBAM 2.5 Reports</span></span>](how-to-configure-the-mbam-25-reports.md)

[<span data-ttu-id="b53eb-192">Comment configurer les applications Web MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="b53eb-192">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="b53eb-193">Validation de la configuration des composants serveur de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="b53eb-193">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)



## <span data-ttu-id="b53eb-194">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="b53eb-194">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="b53eb-195">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="b53eb-195">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="b53eb-196">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="b53eb-196">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





