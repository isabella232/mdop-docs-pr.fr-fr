---
title: Comment configurer l'intégration de MBAM2.5 à System Center Configuration Manager
description: Comment configurer l'intégration de MBAM2.5 à System Center Configuration Manager
author: dansimp
ms.assetid: 2b8a4c13-1dad-41e8-89ac-6889c5f7e051
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c6fb0a0b06399baf1dc6493a40d17e76a51741f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804231"
---
# <span data-ttu-id="8bcec-103">Comment configurer l'intégration de MBAM2.5 à System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8bcec-103">How to Configure the MBAM 2.5 System Center Configuration Manager Integration</span></span>


<span data-ttu-id="8bcec-104">Cet article explique comment configurer l’administration et la surveillance de l’utilisation de Microsoft BitLocker (MBAM) pour utiliser la topologie d’intégration de System Center Configuration Manager, qui intègre MBAM avec Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8bcec-104">This topic explains how to configure Microsoft BitLocker Administration and Monitoring (MBAM) to use the System Center Configuration Manager Integration topology, which integrates MBAM with Configuration Manager.</span></span>

<span data-ttu-id="8bcec-105">Les instructions expliquent comment configurer l’intégration de Configuration Manager à l’aide des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="8bcec-105">The instructions explain how to configure Configuration Manager Integration by using:</span></span>

-   <span data-ttu-id="8bcec-106">Une applet de cmdlet Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8bcec-106">A Windows PowerShell cmdlet</span></span>

-   <span data-ttu-id="8bcec-107">Assistant Configuration de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="8bcec-107">The MBAM Server Configuration wizard</span></span>

<span data-ttu-id="8bcec-108">Les instructions sont basées sur l’architecture recommandée dans [architecture de haut niveau pour MBAM 2,5](high-level-architecture-for-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="8bcec-108">The instructions are based on the recommended architecture in [High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md).</span></span>

**<span data-ttu-id="8bcec-109">Avant de démarrer la configuration:</span><span class="sxs-lookup"><span data-stu-id="8bcec-109">Before you start the configuration:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8bcec-110">Étape</span><span class="sxs-lookup"><span data-stu-id="8bcec-110">Step</span></span></th>
<th align="left"><span data-ttu-id="8bcec-111">Où obtenir des instructions</span><span class="sxs-lookup"><span data-stu-id="8bcec-111">Where to get instructions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8bcec-112">Passez en revue l’architecture recommandée pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="8bcec-112">Review the recommended architecture for MBAM.</span></span></p></td>
<td align="left"><p><a href="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md" data-raw-source="[High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)"><span data-ttu-id="8bcec-113">Architecture globale de MBAM2.5 avec la topologie Intégration Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8bcec-113">High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8bcec-114">Passez en revue les configurations prises en charge pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="8bcec-114">Review the supported configurations for MBAM.</span></span></p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="8bcec-115">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8bcec-115">MBAM 2.5 Supported Configurations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8bcec-116">Remplissez les conditions préalables requises sur chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="8bcec-116">Complete the required prerequisites on each server.</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="8bcec-117">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</span><span class="sxs-lookup"><span data-stu-id="8bcec-117">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)"><span data-ttu-id="8bcec-118">Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8bcec-118">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8bcec-119">Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous allez configurer une fonctionnalité de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="8bcec-119">Install the MBAM Server software on each server where you will configure an MBAM Server feature.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8bcec-120">Remarque</span><span class="sxs-lookup"><span data-stu-id="8bcec-120">Note</span></span></strong><br/><p><span data-ttu-id="8bcec-121">Pour cette topologie, vous devez installer la console Configuration Manager sur l’ordinateur sur lequel vous installez le logiciel serveur MBAM.</span><span class="sxs-lookup"><span data-stu-id="8bcec-121">For this topology, you must install the Configuration Manager console on the computer where you are installing the MBAM Server software.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)"><span data-ttu-id="8bcec-122">Installation du logiciel serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8bcec-122">Installing the MBAM 2.5 Server Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8bcec-123">Passez en revue la configuration requise pour Windows PowerShell (s’applique uniquement si vous envisagez d’utiliser des cmdlets Windows PowerShell pour configurer MBAM).</span><span class="sxs-lookup"><span data-stu-id="8bcec-123">Review Windows PowerShell prerequisites (applicable only if you are going to use Windows PowerShell cmdlets to configure MBAM).</span></span></p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"><span data-ttu-id="8bcec-124">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8bcec-124">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="8bcec-125">Pour configurer l’intégration de Configuration Manager à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8bcec-125">To configure Configuration Manager Integration by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="8bcec-126">Avant de commencer la configuration, reportez-vous à la rubrique [Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) pour consulter les conditions préalables à l’utilisation de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8bcec-126">Before you start the configuration, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) to review the prerequisites for using Windows PowerShell.</span></span>

2.  <span data-ttu-id="8bcec-127">Utilisez l’applet de cmdlet Windows PowerShell **Enable-MbamCMIntegration** pour configurer les rapports.</span><span class="sxs-lookup"><span data-stu-id="8bcec-127">Use the **Enable-MbamCMIntegration** Windows PowerShell cmdlet to configure the Reports.</span></span> <span data-ttu-id="8bcec-128">Pour obtenir des informations sur cette cmdlet, tapez **Get-Help-MbamCMIntegration**.</span><span class="sxs-lookup"><span data-stu-id="8bcec-128">To get information about this cmdlet, type **Get-Help Enable-MbamCMIntegration**.</span></span>

**<span data-ttu-id="8bcec-129">Pour configurer l’intégration de System Center Configuration Manager à l’aide de l’Assistant</span><span class="sxs-lookup"><span data-stu-id="8bcec-129">To configure the System Center Configuration Manager Integration by using the wizard</span></span>**

1.  <span data-ttu-id="8bcec-130">Sur le serveur sur lequel vous voulez configurer la fonctionnalité d’intégration de System Center Configuration Manager, démarrez l’Assistant Configuration de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="8bcec-130">On the server where you want to configure the System Center Configuration Manager Integration feature, start the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="8bcec-131">Vous pouvez sélectionner **MBAM de configuration de serveur** dans le menu **Démarrer** pour ouvrir l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="8bcec-131">You can select **MBAM Server Configuration** from the **Start** menu to open the wizard.</span></span>

2.  <span data-ttu-id="8bcec-132">Cliquez sur **ajouter de nouvelles fonctionnalités**, sélectionnez **intégration de System Center Configuration Manager**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="8bcec-132">Click **Add New Features**, select **System Center Configuration Manager Integration**, and then click **Next**.</span></span>

    <span data-ttu-id="8bcec-133">L’Assistant vérifie que toutes les conditions préalables pour l’intégration de Configuration Manager sont remplies.</span><span class="sxs-lookup"><span data-stu-id="8bcec-133">The wizard checks that all prerequisites for the Configuration Manager Integration have been met.</span></span>

3.  <span data-ttu-id="8bcec-134">Si la vérification de la configuration requise est réussie, cliquez sur **suivant** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="8bcec-134">If the prerequisite check is successful, click **Next** to continue.</span></span> <span data-ttu-id="8bcec-135">Dans le cas contraire, résolvez les conditions préalables manquantes, puis cliquez **à nouveau sur vérifier les conditions préalables**.</span><span class="sxs-lookup"><span data-stu-id="8bcec-135">Otherwise, resolve any missing prerequisites, and then click **Check prerequisites again**.</span></span>

4.  <span data-ttu-id="8bcec-136">Utilisez les descriptions suivantes pour entrer les valeurs de champ dans l’Assistant:</span><span class="sxs-lookup"><span data-stu-id="8bcec-136">Use the following descriptions to enter the field values in the wizard:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="8bcec-137">Champ</span><span class="sxs-lookup"><span data-stu-id="8bcec-137">Field</span></span></th>
    <th align="left"><span data-ttu-id="8bcec-138">Description</span><span class="sxs-lookup"><span data-stu-id="8bcec-138">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="8bcec-139">Serveur SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="8bcec-139">SQL Server Reporting Services server</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="8bcec-140">Nom de domaine complet (FQDN) du serveur doté du rôle de point de service de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="8bcec-140">Fully qualified domain name (FQDN) of the server with the Reporting Service point role.</span></span> <span data-ttu-id="8bcec-141">Il s’agit du serveur sur lequel sont déployés les rapports du gestionnaire de configuration MBAM.</span><span class="sxs-lookup"><span data-stu-id="8bcec-141">This is the server to which the MBAM Configuration Manager Reports are deployed.</span></span></p>
    <p><span data-ttu-id="8bcec-142">Si vous ne spécifiez pas de serveur, les rapports du gestionnaire de configuration seront déployés sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="8bcec-142">If you don’t specify a server, the Configuration Manager Reports will be deployed to the local server.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="8bcec-143">Instance de SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="8bcec-143">SQL Server Reporting Services instance</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="8bcec-144">Nom de l’instance SQL Server Reporting Services (SSRS) dans laquelle les rapports Configuration Manager sont déployés.</span><span class="sxs-lookup"><span data-stu-id="8bcec-144">Name of the SQL Server Reporting Services (SSRS) instance where the Configuration Manager Reports are deployed.</span></span></p>
    <p><span data-ttu-id="8bcec-145">Si vous ne spécifiez pas d’instance, les rapports du gestionnaire de configuration seront déployés sur le nom d’instance SSRS par défaut.</span><span class="sxs-lookup"><span data-stu-id="8bcec-145">If you don’t specify an instance, the Configuration Manager Reports will be deployed to the default SSRS instance name.</span></span> <span data-ttu-id="8bcec-146">La valeur que vous entrez est ignorée si le serveur a installé le gestionnaire de configuration de System Center 2012.</span><span class="sxs-lookup"><span data-stu-id="8bcec-146">The value you enter is ignored if the server has System Center 2012 Configuration Manager installed.</span></span></p></td>
    </tr>
    </tbody>
    </table>



5.  <span data-ttu-id="8bcec-147">Dans la page **Résumé** , passez en revue les fonctionnalités qui seront ajoutées.</span><span class="sxs-lookup"><span data-stu-id="8bcec-147">On the **Summary** page, review the features that will be added.</span></span>

    **<span data-ttu-id="8bcec-148">Remarque</span><span class="sxs-lookup"><span data-stu-id="8bcec-148">Note</span></span>**  
    <span data-ttu-id="8bcec-149">Pour créer un script Windows PowerShell des entrées que vous venez de créer, cliquez sur **Exporter le script PowerShell** et enregistrez le script.</span><span class="sxs-lookup"><span data-stu-id="8bcec-149">To create a Windows PowerShell script of the entries you just made, click **Export PowerShell Script** and save the script.</span></span>



6.  <span data-ttu-id="8bcec-150">Cliquez sur **Ajouter** pour ajouter la fonctionnalité d’intégration de Configuration Manager au serveur, puis cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="8bcec-150">Click **Add** to add the Configuration Manager Integration feature to the server, and then click **Close**.</span></span>



## <span data-ttu-id="8bcec-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8bcec-151">Related topics</span></span>


[<span data-ttu-id="8bcec-152">Configuration des composants du serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8bcec-152">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="8bcec-153">Validation de la configuration des composants serveur de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8bcec-153">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)


## <span data-ttu-id="8bcec-154">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="8bcec-154">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8bcec-155">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="8bcec-155">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8bcec-156">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8bcec-156">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






