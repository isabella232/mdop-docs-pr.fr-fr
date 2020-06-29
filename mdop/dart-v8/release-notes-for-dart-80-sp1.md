---
title: Notes de publication pour DaRT8.0SP1
description: Notes de publication pour DaRT8.0SP1
author: dansimp
ms.assetid: fa7512d8-fb00-4c27-8f65-c15f3a8ff1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a4c49d12fed07f507d2db4d56969d8e7b0559c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810757"
---
# <span data-ttu-id="061bd-103">Notes de publication pour DaRT8.0SP1</span><span class="sxs-lookup"><span data-stu-id="061bd-103">Release Notes for DaRT 8.0 SP1</span></span>


**<span data-ttu-id="061bd-104">Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="061bd-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="061bd-105">Lisez attentivement ces notes de publication avant de procéder à l’installation de Microsoft Diagnostics and Recovery Tools (DaRT) 8,0 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="061bd-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Service Pack 1 (SP1).</span></span>

<span data-ttu-id="061bd-106">Ces notes de publication contiennent des informations requises pour installer correctement les outils de diagnostics et de récupération d’outils de récupération 8,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="061bd-106">These release notes contain information that is required to successfully install Diagnostics and Recovery Toolset 8.0 SP1.</span></span> <span data-ttu-id="061bd-107">Les notes de publication contiennent également des informations qui ne sont pas disponibles dans la documentation du produit.</span><span class="sxs-lookup"><span data-stu-id="061bd-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="061bd-108">S’il existe une différence entre ces notes de publication et d’autres documents DaRT, la dernière modification doit être considérée comme faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="061bd-108">If there is a difference between these release notes and other DaRT documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="061bd-109">Ces notes de publication remplacent le contenu qui est inclus dans ce produit.</span><span class="sxs-lookup"><span data-stu-id="061bd-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="061bd-110">À propos de la documentation relative aux produits</span><span class="sxs-lookup"><span data-stu-id="061bd-110">About the product documentation</span></span>


<span data-ttu-id="061bd-111">Pour plus d’informations sur la documentation pour DaRT, consultez la [page d’accueil de DART](https://go.microsoft.com/fwlink/?LinkID=252096) sur Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="061bd-111">For information about documentation for DaRT, see the [DaRT home page](https://go.microsoft.com/fwlink/?LinkID=252096) on Microsoft TechNet.</span></span>

## <span data-ttu-id="061bd-112">Problèmes connus avec DaRT 8,0 SP1</span><span class="sxs-lookup"><span data-stu-id="061bd-112">Known issues with DaRT 8.0 SP1</span></span>


### <span data-ttu-id="061bd-113">La restauration du système échoue lorsque vous exécutez Locksmith ou l’éditeur du Registre</span><span class="sxs-lookup"><span data-stu-id="061bd-113">System restore fails when you run Locksmith or Registry Editor</span></span>

<span data-ttu-id="061bd-114">Si vous exécutez Locksmith, l’éditeur du Registre et éventuellement d’autres outils, la restauration du système échoue.</span><span class="sxs-lookup"><span data-stu-id="061bd-114">If you run Locksmith, Registry Editor, and possibly other tools, System Restore fails.</span></span>

<span data-ttu-id="061bd-115">**Solution de contournement:** Fermez et redémarrez DaRT, puis démarrez la restauration du système.</span><span class="sxs-lookup"><span data-stu-id="061bd-115">**Workaround:** Close and restart DaRT and then start System Restore.</span></span>

### <span data-ttu-id="061bd-116">L’analyse SFC ne peut pas s’exécuter lorsque vous démarrez et fermez Locksmith ou la gestion de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="061bd-116">SFC scan fails to run after you launch and close Locksmith or Computer Management</span></span>

<span data-ttu-id="061bd-117">Si vous démarrez, puis fermez l’Locksmith ou les outils de gestion de l’ordinateur, le vérificateur de fichiers système ne s’exécute pas.</span><span class="sxs-lookup"><span data-stu-id="061bd-117">If you start and then close the Locksmith or Computer Management tools, System File Checker fails to run.</span></span>

<span data-ttu-id="061bd-118">**Solution de contournement:** Fermez et redémarrez DaRT, puis démarrez SFC.</span><span class="sxs-lookup"><span data-stu-id="061bd-118">**Workaround:** Close and restart DaRT and then start SFC.</span></span>

### <a href="" id="-------------dart-installer-does-not-fail-when-adk-has-not-been-installed"></a> <span data-ttu-id="061bd-119">Le programme d’installation de DaRT ne fonctionne pas lorsque ADK n’a pas été installé</span><span class="sxs-lookup"><span data-stu-id="061bd-119">DaRT installer does not fail when ADK has not been installed</span></span>

<span data-ttu-id="061bd-120">Si vous installez DaRT 8,0 SP1 à l’aide de la ligne de commande pour exécuter le MSI et que le ADK n’a pas été installé, l’installation de DaRT échoue.</span><span class="sxs-lookup"><span data-stu-id="061bd-120">If you install DaRT 8.0 SP1 by using the command line to run the MSI, and the ADK has not been installed, the DaRT installation should fail.</span></span> <span data-ttu-id="061bd-121">Pour l’instant, le programme d’installation de DaRT 8,0 SP1 installe tous les composants, à l’exception de l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="061bd-121">Currently, the DaRT 8.0 SP1 installer installs all components except the DaRT recovery image.</span></span>

<span data-ttu-id="061bd-122">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="061bd-122">**Workaround:** None.</span></span>

### <span data-ttu-id="061bd-123">Le système Defender ne peut pas être lancé après le lancement de Locksmith, de l’analyseur de blocage et de la gestion de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="061bd-123">Defender cannot be launched after Locksmith, RegEdit, Crash Analyzer, and Computer Management are launched</span></span>

<span data-ttu-id="061bd-124">Le logiciel Defender ne se lance pas si vous avez déjà lancé Locksmith, RegEdit, analyse de blocage et gestion de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="061bd-124">Defender does not launch if you have already launched Locksmith, RegEdit, Crash Analyzer, and Computer Management.</span></span>

<span data-ttu-id="061bd-125">**Solution de contournement:** Fermez et redémarrez DaRT, puis lancez Defender.</span><span class="sxs-lookup"><span data-stu-id="061bd-125">**Workaround:** Close and restart DaRT and then launch Defender.</span></span>

### <span data-ttu-id="061bd-126">Le démarrage de Defender est ralenti</span><span class="sxs-lookup"><span data-stu-id="061bd-126">Defender may be slow to launch</span></span>

<span data-ttu-id="061bd-127">Le lancement de Defender peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="061bd-127">Defender sometimes takes a few minutes to launch.</span></span> <span data-ttu-id="061bd-128">La barre de progression indique l’état de chargement actuel.</span><span class="sxs-lookup"><span data-stu-id="061bd-128">The progress bar indicates the current loading status.</span></span>

<span data-ttu-id="061bd-129">**Solution de contournement:** Néant.</span><span class="sxs-lookup"><span data-stu-id="061bd-129">**Workaround:** None.</span></span>

## <span data-ttu-id="061bd-130">Informations de copyright des notes de publication</span><span class="sxs-lookup"><span data-stu-id="061bd-130">Release notes copyright information</span></span>


<span data-ttu-id="061bd-131">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune et WindowsPowerShell sont des marques commerciales du groupe de sociétés Microsoft.</span><span class="sxs-lookup"><span data-stu-id="061bd-131">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="061bd-132">Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.</span><span class="sxs-lookup"><span data-stu-id="061bd-132">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="061bd-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="061bd-133">Related topics</span></span>


[<span data-ttu-id="061bd-134">À propos de DaRT8.0SP1</span><span class="sxs-lookup"><span data-stu-id="061bd-134">About DaRT 8.0 SP1</span></span>](about-dart-80-sp1.md)

 

 





