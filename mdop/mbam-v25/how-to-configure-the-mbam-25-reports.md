---
title: Configuration des rapports MBAM2.5
description: Configuration des rapports MBAM2.5
author: dansimp
ms.assetid: ec462879-0253-4d9c-83c7-a9bcad479725
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b372bd6bc38a3729aef43354ecf19b2619b7856
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811862"
---
# <span data-ttu-id="5ed18-103">Configuration des rapports MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5ed18-103">How to Configure the MBAM 2.5 Reports</span></span>


<span data-ttu-id="5ed18-104">Cet article explique comment configurer la fonctionnalité de rapports 2,5 d’administration et de surveillance de Microsoft BitLocker (MBAM) à l’aide des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="5ed18-104">This topic explains how to configure the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Reports feature by using:</span></span>

-   <span data-ttu-id="5ed18-105">Une applet de cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5ed18-105">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="5ed18-106">Assistant Configuration de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="5ed18-106">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="5ed18-107">Les instructions sont basées sur l’architecture recommandée dans [architecture de haut niveau pour MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="5ed18-107">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="5ed18-108">Avant de démarrer la configuration:</span><span class="sxs-lookup"><span data-stu-id="5ed18-108">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5ed18-109">Étape</span><span class="sxs-lookup"><span data-stu-id="5ed18-109">Step</span></span></th>
<th align="left"><span data-ttu-id="5ed18-110">Où obtenir des instructions</span><span class="sxs-lookup"><span data-stu-id="5ed18-110">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ed18-111">Passez en revue l’architecture recommandée pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="5ed18-111">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="5ed18-112">Architecture de hautniveau pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5ed18-112">High-Level Architecture for MBAM 2.5</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ed18-113">Passez en revue les configurations prises en charge pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="5ed18-113">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="5ed18-114">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5ed18-114">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ed18-115">Remplissez les conditions préalables requises sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="5ed18-115">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="5ed18-116">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</span><span class="sxs-lookup"><span data-stu-id="5ed18-116">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="5ed18-117">MBAM 2,5 requis par le serveur qui ne s’appliquent qu’à la topologie d’intégration de Configuration Manager </a> (le cas échéant)</span><span class="sxs-lookup"><span data-stu-id="5ed18-117">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</a> (if applicable)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5ed18-118">Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous envisagez de configurer une fonctionnalité de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="5ed18-118">Install the MBAM Server software on each server where you plan to configure an MBAM Server feature.</span></span></p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="5ed18-119">Installation du logiciel serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5ed18-119">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5ed18-120">Passez en revue la configuration requise pour l’utilisation de Windows PowerShell Si vous envisagez d’utiliser des cmdlets Windows PowerShell pour configurer les fonctionnalités du serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="5ed18-120">Review the prerequisites for using Windows PowerShell if you plan to use Windows PowerShell cmdlets to configure MBAM Server features.</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="5ed18-121">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5ed18-121">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="5ed18-122">Pour configurer les rapports à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5ed18-122">To configure the Reports by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="5ed18-123">Avant de commencer la configuration, reportez-vous à la rubrique [Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) pour consulter les conditions préalables à l’utilisation de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5ed18-123">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="5ed18-124">Utilisez l’applet de cmdlet Windows PowerShell **Enable-MbamReport** pour configurer les rapports.</span><span class="sxs-lookup"><span data-stu-id="5ed18-124">Use the **Enable-MbamReport** Windows PowerShell cmdlet to configure the Reports.</span></span> <span data-ttu-id="5ed18-125">Pour obtenir des informations sur cette applet de cmdlet Windows PowerShell, tapez **Get-Help-MbamReport**.</span><span class="sxs-lookup"><span data-stu-id="5ed18-125">To get information about this Windows PowerShell cmdlet, type **Get-Help Enable-MbamReport**.</span></span>

**<span data-ttu-id="5ed18-126">Pour configurer les rapports à l’aide de l’Assistant</span><span class="sxs-lookup"><span data-stu-id="5ed18-126">To configure the Reports by using the wizard</span></span>**

1. <span data-ttu-id="5ed18-127">Sur le serveur sur lequel vous voulez configurer les rapports, démarrez l’Assistant **configuration de MBAM Server** .</span><span class="sxs-lookup"><span data-stu-id="5ed18-127">On the server where you want to configure the Reports, start the **MBAM Server Configuration** wizard.</span></span> <span data-ttu-id="5ed18-128">Vous pouvez sélectionner **MBAM de configuration de serveur** dans le menu **Démarrer** pour ouvrir l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="5ed18-128">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2. <span data-ttu-id="5ed18-129">Cliquez sur **ajouter de nouvelles fonctionnalités**, sélectionnez **rapports**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="5ed18-129">Click **Add New Features**, select **Reports**, and then click **Next**.</span></span> <span data-ttu-id="5ed18-130">L’Assistant vérifie que toutes les conditions préalables pour les rapports sont remplies.</span><span class="sxs-lookup"><span data-stu-id="5ed18-130">The wizard checks that all prerequisites for the Reports have been met.</span></span>

3. <span data-ttu-id="5ed18-131">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="5ed18-131">Click **Next** to continue.</span></span>

4. <span data-ttu-id="5ed18-132">À l’aide des descriptions suivantes, entrez les valeurs de champ dans l’Assistant:</span><span class="sxs-lookup"><span data-stu-id="5ed18-132">Using the following descriptions, enter the field values in the wizard:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="5ed18-133">Champ</span><span class="sxs-lookup"><span data-stu-id="5ed18-133">Field</span></span></th>
   <th align="left"><span data-ttu-id="5ed18-134">Description</span><span class="sxs-lookup"><span data-stu-id="5ed18-134">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5ed18-135">Instance de SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="5ed18-135">SQL Server Reporting Services instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ed18-136">Instance de SQL Server Reporting Services où les rapports seront configurés.</span><span class="sxs-lookup"><span data-stu-id="5ed18-136">Instance of SQL Server Reporting Services where the Reports will be configured.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="5ed18-137">Groupe de domaine de rôle de rapport</span><span class="sxs-lookup"><span data-stu-id="5ed18-137">Reporting role domain group</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ed18-138">Nom du groupe d’utilisateurs du domaine dont les membres ont le droit d’accéder aux rapports sur le serveur d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="5ed18-138">Name of the domain Users group whose members have rights to access the reports on the Administration and Monitoring Server.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5ed18-139">Nom SQL Server</span><span class="sxs-lookup"><span data-stu-id="5ed18-139">SQL Server name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ed18-140">Nom du serveur sur lequel la base de données d’audit et de conformité est configurée.</span><span class="sxs-lookup"><span data-stu-id="5ed18-140">Name of the server where the Compliance and Audit Database is configured.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="5ed18-141">Instance de base de données SQL Server</span><span class="sxs-lookup"><span data-stu-id="5ed18-141">SQL Server database instance</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ed18-142">Nom de l’instance de SQL Server (par exemple, <em> MSSQLSERVER </em> ) où la base de données d’audit et de conformité est configurée.</span><span class="sxs-lookup"><span data-stu-id="5ed18-142">Name of the instance of SQL Server (for example, <em>MSSQLSERVER</em>) where the Compliance and Audit Database is configured.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="5ed18-143">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ed18-143">Note</span></span></strong><br/><p><span data-ttu-id="5ed18-144">Vous devez ajouter une exception sur l’ordinateur rapports pour activer le trafic entrant sur le port du serveur de création de rapports (le port par défaut est 80).</span><span class="sxs-lookup"><span data-stu-id="5ed18-144">You must add an exception on the Reports computer to enable inbound traffic on the port of the Reporting Server (the default port is 80).</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="5ed18-145">Nom de la base de données</span><span class="sxs-lookup"><span data-stu-id="5ed18-145">Database name</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ed18-146">Nom de la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5ed18-146">Name of the Compliance and Audit Database.</span></span> <span data-ttu-id="5ed18-147">Par défaut, il s’agit du nom de la base de données <strong> MBAM </strong> , même si vous pouvez en modifier le nom lorsque vous configurez la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5ed18-147">By default, the database name is <strong>MBAM Compliance Status</strong>, although you can change the name when you configure the Compliance and Audit Database.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="5ed18-148">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ed18-148">Note</span></span></strong><br/><p><span data-ttu-id="5ed18-149">Si vous effectuez une mise à niveau à partir d’une version précédente de MBAM, vous devez utiliser le même nom de base de données que le nom utilisé dans votre ancien déploiement.</span><span class="sxs-lookup"><span data-stu-id="5ed18-149">If you are upgrading from a previous version of MBAM, you must use the same database name as the name used in your previous deployment.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="5ed18-150">Vérification de la conformité et de la base de données du compte de domaine</span><span class="sxs-lookup"><span data-stu-id="5ed18-150">Compliance and Audit Database domain account</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="5ed18-151">Compte d’utilisateur et mot de passe de domaine pour accéder à la base de données d’audit et de conformité.</span><span class="sxs-lookup"><span data-stu-id="5ed18-151">Domain user account and password to access the Compliance and Audit Database.</span></span></p>
   <p><span data-ttu-id="5ed18-152">Si la valeur que vous entrez dans le <strong> champ d’utilisateur ou de groupe d’accès en lecture seule </strong> de la <strong> page configurer des bases de données </strong> est un utilisateur, vous devez entrer cette même valeur dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="5ed18-152">If the value you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a user, you must enter that same value in this field.</span></span></p>
   <p><span data-ttu-id="5ed18-153">Si la valeur que vous entrez dans le <strong> champ d’utilisateur ou de groupe d’accès en lecture seule </strong> de la <strong> page Configurer les bases de données </strong> est un groupe, la valeur que vous entrez dans ce champ doit être membre du groupe.</span><span class="sxs-lookup"><span data-stu-id="5ed18-153">If the value that you enter in the <strong>Read-only access domain user or group</strong> field on the <strong>Configure Databases</strong> page is a group, the value that you enter in this field must be a member of that group.</span></span></p>
   <p><span data-ttu-id="5ed18-154">Configurez le mot de passe de ce compte pour qu’il n’expire jamais.</span><span class="sxs-lookup"><span data-stu-id="5ed18-154">Configure the password for this account to never expire.</span></span> <span data-ttu-id="5ed18-155">Le compte d’utilisateur doit être en mesure d’accéder à toutes les données disponibles pour le groupe utilisateurs de reports MBAM.</span><span class="sxs-lookup"><span data-stu-id="5ed18-155">The user account should be able to access all data that is available to the MBAM Reports Users group.</span></span></p></td>
   </tr>
   </tbody>
   </table>



5. <span data-ttu-id="5ed18-156">Lorsque vous avez terminé, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="5ed18-156">When you finish your entries, click **Next**.</span></span>

   <span data-ttu-id="5ed18-157">L’Assistant vérifie que toutes les conditions préalables pour la fonctionnalité rapports sont remplies.</span><span class="sxs-lookup"><span data-stu-id="5ed18-157">The wizard checks that all prerequisites for the Reports feature have been met.</span></span>

6. <span data-ttu-id="5ed18-158">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="5ed18-158">Click **Next** to continue.</span></span>

7. <span data-ttu-id="5ed18-159">Dans la page **Résumé** , passez en revue les fonctionnalités qui seront ajoutées.</span><span class="sxs-lookup"><span data-stu-id="5ed18-159">On the **Summary** page, review the features that will be added.</span></span>

   **<span data-ttu-id="5ed18-160">Remarque</span><span class="sxs-lookup"><span data-stu-id="5ed18-160">Note</span></span>**  
   <span data-ttu-id="5ed18-161">Pour créer un script Windows PowerShell des entrées que vous venez de créer, cliquez sur **Exporter le script PowerShell**, puis enregistrez le script.</span><span class="sxs-lookup"><span data-stu-id="5ed18-161">To create a Windows PowerShell script of the entries that you just made, click **Export PowerShell Script**, and then save the script.</span></span>



8. <span data-ttu-id="5ed18-162">Cliquez sur **Ajouter** pour ajouter les rapports sur le serveur, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="5ed18-162">Click **Add** to add the Reports on the server, and then click **Close**.</span></span>



## <span data-ttu-id="5ed18-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ed18-163">Related topics</span></span>


[<span data-ttu-id="5ed18-164">Journaux des événements serveur</span><span class="sxs-lookup"><span data-stu-id="5ed18-164">Server Event Logs</span></span>](server-event-logs.md)

[<span data-ttu-id="5ed18-165">Configuration des composants du serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5ed18-165">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="5ed18-166">Comment configurer les applications Web MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5ed18-166">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="5ed18-167">Validation de la configuration des composants serveur de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5ed18-167">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)


## <span data-ttu-id="5ed18-168">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="5ed18-168">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="5ed18-169">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="5ed18-169">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="5ed18-170">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="5ed18-170">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






