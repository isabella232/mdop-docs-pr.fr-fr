---
title: Composants requis pour l'installation de MED-V
description: Composants requis pour l'installation de MED-V
author: dansimp
ms.assetid: cf3c0906-23eb-4c4a-8951-a65741720f95
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2b432b8c2b06e171eb339aab6c7b15efb20d5919
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810872"
---
# <span data-ttu-id="35d3d-103">Composants requis pour l'installation de MED-V</span><span class="sxs-lookup"><span data-stu-id="35d3d-103">MED-V Installation Prerequisites</span></span>


<span data-ttu-id="35d3d-104">Vous trouverez ci-après les conditions préalables à l’installation de MED-V:</span><span class="sxs-lookup"><span data-stu-id="35d3d-104">The following are prerequisites for installing MED-V:</span></span>

[<span data-ttu-id="35d3d-105">Configuration requise pour Active Directory</span><span class="sxs-lookup"><span data-stu-id="35d3d-105">Active Directory Requirements</span></span>](#bkmk-activedirectoryrequirements)

[<span data-ttu-id="35d3d-106">Rapport de base de données</span><span class="sxs-lookup"><span data-stu-id="35d3d-106">Report Database</span></span>](#bkmk-howtoinstallthereportdatabase)

[<span data-ttu-id="35d3d-107">Configuration de logiciels antivirus/de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="35d3d-107">Antivirus/Backup Software Configuration</span></span>](#bkmk-antivirusbackupsoftwareconfiguration)

[<span data-ttu-id="35d3d-108">Microsoft Virtual PC 2007 SP1</span><span class="sxs-lookup"><span data-stu-id="35d3d-108">Microsoft Virtual PC 2007 SP1</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1)

## <a href="" id="bkmk-activedirectoryrequirements"></a><span data-ttu-id="35d3d-109">Configuration requise pour Active Directory</span><span class="sxs-lookup"><span data-stu-id="35d3d-109">Active Directory Requirements</span></span>


<span data-ttu-id="35d3d-110">Lors de la configuration du serveur MED-V, si les utilisateurs ne font pas partie du même domaine auquel le serveur appartient, une approbation doit être définie entre les domaines.</span><span class="sxs-lookup"><span data-stu-id="35d3d-110">When configuring the MED-V server, if users are not part of the same domain the server belongs to, a trust must be set between the domains.</span></span>

## <a href="" id="bkmk-howtoinstallthereportdatabase"></a><span data-ttu-id="35d3d-111">Comment installer la base de données de rapport</span><span class="sxs-lookup"><span data-stu-id="35d3d-111">How to Install the Report Database</span></span>


<span data-ttu-id="35d3d-112">La base de données de rapports est nécessaire pour stocker tous les journaux d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="35d3d-112">The report database is required for storing all MED-V workspace logs.</span></span> <span data-ttu-id="35d3d-113">La base de données journal est alors utilisée pour générer des rapports MED-V.</span><span class="sxs-lookup"><span data-stu-id="35d3d-113">The log database is then used for generating MED-V reports.</span></span> <span data-ttu-id="35d3d-114">Pour plus d’informations sur les rapports, voir [création de rapports MED-V](med-v-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="35d3d-114">For information about reports, see [MED-V Reporting](med-v-reporting.md).</span></span>

<span data-ttu-id="35d3d-115">SQL Server peut être installé sur le même serveur que le serveur MED-V ou sur un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="35d3d-115">SQL Server can be installed on the same server as the MED-V server or on a remote server.</span></span> <span data-ttu-id="35d3d-116">Si vous effectuez une installation sur un serveur distant, reportez-vous à la rubrique [installation de SQL Server sur un serveur distant](#bkmk-installingsqlserveronaremoteserver).</span><span class="sxs-lookup"><span data-stu-id="35d3d-116">If installing on a remote server, see [Installing SQL Server on a Remote Server](#bkmk-installingsqlserveronaremoteserver).</span></span>

### <a href="" id="bkmk-installingsqlserveronaremoteserver"></a><span data-ttu-id="35d3d-117">Installation de SQL Server sur un serveur distant</span><span class="sxs-lookup"><span data-stu-id="35d3d-117">Installing SQL Server on a Remote Server</span></span>

**<span data-ttu-id="35d3d-118">Pour installer SQL Server sur un serveur distant</span><span class="sxs-lookup"><span data-stu-id="35d3d-118">To install SQL Server on a remote server</span></span>**

1.  <span data-ttu-id="35d3d-119">Configurez les éléments suivants sur le serveur distant:</span><span class="sxs-lookup"><span data-stu-id="35d3d-119">Configure the following on the remote server:</span></span>

    -   <span data-ttu-id="35d3d-120">Nom de l’instance: instance par défaut</span><span class="sxs-lookup"><span data-stu-id="35d3d-120">Instance name—Default instance</span></span>

    -   <span data-ttu-id="35d3d-121">Mode d’authentification: mode mixte</span><span class="sxs-lookup"><span data-stu-id="35d3d-121">Authentication mode—Mixed mode</span></span>

    -   <span data-ttu-id="35d3d-122">Utilisateur: l’utilisateur créé par défaut est «sa».</span><span class="sxs-lookup"><span data-stu-id="35d3d-122">User—The default user created is “sa”</span></span>

    -   <span data-ttu-id="35d3d-123">Mot de passe: mot de passe souhaité</span><span class="sxs-lookup"><span data-stu-id="35d3d-123">Password—Desired password</span></span>

    -   <span data-ttu-id="35d3d-124">Paramètres d’assemblage (par défaut)</span><span class="sxs-lookup"><span data-stu-id="35d3d-124">Collation Settings—Default</span></span>

    -   <span data-ttu-id="35d3d-125">Erreur dans les paramètres des rapports d’utilisation (par défaut)</span><span class="sxs-lookup"><span data-stu-id="35d3d-125">Error in usage report settings—Default</span></span>

2.  <span data-ttu-id="35d3d-126">Installez les fichiers suivants sur le serveur MED-V:</span><span class="sxs-lookup"><span data-stu-id="35d3d-126">Install the following files on the MED-V server:</span></span>

    -   <span data-ttu-id="35d3d-127">Pour installer la configuration requise pour la collection d’objets du pack d’administration pour Microsoft SQL Server 2008, téléchargez le [client natif Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=164039) à partir du centre de téléchargement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="35d3d-127">To install the prerequisites for the management pack objects collection for Microsoft SQL Server2008, download [Microsoft SQL Server2008 Native Client](https://go.microsoft.com/fwlink/?LinkId=164039) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="35d3d-128">Pour installer la configuration requise pour la collection d’objets du pack d’administration pour Microsoft SQL Server2005, téléchargez le [client natif Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=164038) à partir du centre de téléchargement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="35d3d-128">To install the prerequisites for the management pack objects collection for Microsoft SQL Server2005, download [Microsoft SQL Server2005 Native Client](https://go.microsoft.com/fwlink/?LinkId=164038) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="35d3d-129">Pour installer les fichiers dll requis pour Microsoft SQL Server 2008, téléchargez la [collection Microsoft SQL Server 2008 Management Objects](https://go.microsoft.com/fwlink/?LinkId=164041) à partir du centre de téléchargement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="35d3d-129">To install the required dll files for Microsoft SQL Server2008, download [Microsoft SQL Server 2008 Management Objects Collection](https://go.microsoft.com/fwlink/?LinkId=164041) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="35d3d-130">Pour installer les fichiers dll requis pour Microsoft SQL Server2005, téléchargez [Microsoft SQL Server2005 Management Objects](https://go.microsoft.com/fwlink/?LinkId=164040) à partir du centre de téléchargement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="35d3d-130">To install the required dll files for Microsoft SQL Server2005, download [Microsoft SQL Server2005 Management Objects](https://go.microsoft.com/fwlink/?LinkId=164040) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="35d3d-131">Pour installer les packages d’installation autonomes qui fournissent des valeurs supplémentaires pour SQL Server 2008, téléchargez le [Feature Pack Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163960) à partir du centre de téléchargement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="35d3d-131">To install the stand-alone install packages that provide additional value for SQL Server2008, download the [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="35d3d-132">Pour installer les packages d’installation autonomes qui fournissent des valeurs supplémentaires pour SQL Server2005, téléchargez le [Pack de fonctionnalités pour Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) à partir du centre de téléchargement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="35d3d-132">To install the stand-alone install packages that provide additional value for SQL Server2005, download the [Feature Pack for Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) from the Microsoft Download Center.</span></span>

    <span data-ttu-id="35d3d-133">Pour plus d’informations sur ces fichiers, voir [module de fonctionnalités Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163960) sur le centre de téléchargement Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163960) ou [Feature Pack pour Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) sur le centre de téléchargement Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163961) .</span><span class="sxs-lookup"><span data-stu-id="35d3d-133">For more information about these files, see [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) on the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=163960) or [Feature Pack for Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) on the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=163961).</span></span>

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a><span data-ttu-id="35d3d-134">Configuration de logiciels antivirus/de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="35d3d-134">Antivirus/Backup Software Configuration</span></span>


<span data-ttu-id="35d3d-135">Pour empêcher les activités de protection antivirus d’affecter les performances de la version de bureau virtuelle, il est recommandé, dans la mesure du possible, d’exclure les types de fichiers d’ordinateur virtuel suivants de tout logiciel antivirus ou de processus de sauvegarde exécuté sur l’hôte:</span><span class="sxs-lookup"><span data-stu-id="35d3d-135">To prevent antivirus activity from affecting the performance of the virtual desktop, it is recommended where possible to exclude the following virtual machine file types from any antivirus or backup processing running on the host:</span></span>

-   <span data-ttu-id="35d3d-136">\*. COMPATIBLE</span><span class="sxs-lookup"><span data-stu-id="35d3d-136">\*.VMC</span></span>

-   <span data-ttu-id="35d3d-137">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="35d3d-137">\*.VUD</span></span>

-   <span data-ttu-id="35d3d-138">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="35d3d-138">\*.VSV</span></span>

-   <span data-ttu-id="35d3d-139">\*. CKM</span><span class="sxs-lookup"><span data-stu-id="35d3d-139">\*.CKM</span></span>

-   <span data-ttu-id="35d3d-140">\*. EVHD</span><span class="sxs-lookup"><span data-stu-id="35d3d-140">\*.EVHD</span></span>

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1"></a><span data-ttu-id="35d3d-141">Installer et configurer Microsoft Virtual PC2007 SP1</span><span class="sxs-lookup"><span data-stu-id="35d3d-141">How to Install and Configure Microsoft Virtual PC2007 SP1</span></span>


<span data-ttu-id="35d3d-142">**Important**  S’il existe le PC virtuel pour Windows sur l’ordinateur hôte, désinstallez-le avant d’installer Virtual PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="35d3d-142">**Important** If Virtual PC for Windows exists on the host computer, uninstall it before installing Virtual PC2007 SP1.</span></span>

 

**<span data-ttu-id="35d3d-143">Pour installer Microsoft Virtual PC2007 SP1</span><span class="sxs-lookup"><span data-stu-id="35d3d-143">To install Microsoft Virtual PC2007 SP1</span></span>**

1.  <span data-ttu-id="35d3d-144">Téléchargez Virtual PC2007 SP1 à partir du centre de téléchargement Microsoft [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994).</span><span class="sxs-lookup"><span data-stu-id="35d3d-144">Download Virtual PC2007 SP1 from the Microsoft Download Center [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994).</span></span>

2.  <span data-ttu-id="35d3d-145">Exécutez le fichier d’installation sur l’ordinateur hôte, puis suivez l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="35d3d-145">Run the installation file on the host computer, and follow the wizard.</span></span>

3.  <span data-ttu-id="35d3d-146">Installez la mise à jour virtuelle de PC2007 SP1 sur l’ordinateur hôte en mode d’élévation.</span><span class="sxs-lookup"><span data-stu-id="35d3d-146">Install Virtual PC2007 SP1 update on the host computer in elevated mode.</span></span>

    <span data-ttu-id="35d3d-147">Pour plus d’informations, reportez-vous à [la description du package de correctif logiciel pour Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).</span><span class="sxs-lookup"><span data-stu-id="35d3d-147">For more information, see [the description of the hotfix package for Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).</span></span>

    <span data-ttu-id="35d3d-148">**Remarques**  La mise à jour virtuelle PC2007 SP1 est nécessaire pour exécuter Virtual PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="35d3d-148">**Note** The Virtual PC2007 SP1 update is required for running Virtual PC2007 SP1.</span></span>

     

## <span data-ttu-id="35d3d-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="35d3d-149">Related topics</span></span>


[<span data-ttu-id="35d3d-150">Configurations prises en charge</span><span class="sxs-lookup"><span data-stu-id="35d3d-150">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

 

 





