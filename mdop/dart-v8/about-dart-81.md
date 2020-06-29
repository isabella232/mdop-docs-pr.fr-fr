---
title: À propos de DaRT8.1
description: À propos de DaRT8.1
author: dansimp
ms.assetid: dcaddc57-0111-4a9d-8be9-f5ada0eefa7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 29c7522b4f5a5da3b451b23f2fd200db44bb9481
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808651"
---
# <span data-ttu-id="27917-103">À propos de DaRT8.1</span><span class="sxs-lookup"><span data-stu-id="27917-103">About DaRT 8.1</span></span>


<span data-ttu-id="27917-104">Microsoft Diagnostics and Recovery Tools (DaRT) 8,1 fournit les améliorations suivantes décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="27917-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.1 provides the following enhancements, which are described in this topic.</span></span>

## <a href="" id="what-s-new"></a><span data-ttu-id="27917-105">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="27917-105">What’s new</span></span>


-   **<span data-ttu-id="27917-106">Prise en charge de WIMBoot</span><span class="sxs-lookup"><span data-stu-id="27917-106">Support for WIMBoot</span></span>**

    <span data-ttu-id="27917-107">Outils de diagnostics et de récupération 8,1 prend en charge l’environnement de démarrage de fichiers image Windows (WIMBoot) si les conditions suivantes sont remplies:</span><span class="sxs-lookup"><span data-stu-id="27917-107">Diagnostics and Recovery Toolset 8.1 supports the Windows image file boot (WIMBoot) environment if these conditions are met:</span></span>

    -   <span data-ttu-id="27917-108">WIMBoot repose sur Windows 8,1 Update 1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="27917-108">WIMBoot is based on Windows 8.1 Update 1 or later.</span></span>

    -   <span data-ttu-id="27917-109">L’image 8,1 DaRT est basée sur Windows 8,1 Update 1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="27917-109">The DaRT 8.1 image is built on Windows 8.1 Update 1 or later.</span></span>

    <span data-ttu-id="27917-110">Pour plus d’informations sur WIMBoot, voir [vue d’ensemble de Windows image file Boot (WIMBoot)](https://go.microsoft.com/fwlink/?LinkId=517536).</span><span class="sxs-lookup"><span data-stu-id="27917-110">For more information about WIMBoot, see [Windows Image File Boot (WIMBoot) Overview](https://go.microsoft.com/fwlink/?LinkId=517536).</span></span>

-   **<span data-ttu-id="27917-111">Prise en charge de Windows Server 2012 R2 et Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="27917-111">Support for Windows Server 2012 R2 and Windows 8.1</span></span>**

    <span data-ttu-id="27917-112">Vous pouvez créer des images DaRT en utilisant Windows Server 2012 R2 ou Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="27917-112">You can create DaRT images by using Windows Server 2012 R2 or Windows 8.1.</span></span>

    **<span data-ttu-id="27917-113">Remarque</span><span class="sxs-lookup"><span data-stu-id="27917-113">Note</span></span>**  
    <span data-ttu-id="27917-114">Pour les versions antérieures du système d’exploitation Windows Server et Windows, continuez à utiliser les versions précédentes de DaRT.</span><span class="sxs-lookup"><span data-stu-id="27917-114">For earlier versions of the Windows Server and Windows operating systems, continue to use the earlier versions of DaRT.</span></span>



-   **<span data-ttu-id="27917-115">Retour d’expérience du client</span><span class="sxs-lookup"><span data-stu-id="27917-115">Customer feedback</span></span>**

    <span data-ttu-id="27917-116">Le 8,1 DaRT inclut des mises à jour qui concernent les problèmes rencontrés depuis la version DaRT 8,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="27917-116">DaRT 8.1 includes updates that address issues found since the DaRT 8.0 SP1 release.</span></span>

-   **<span data-ttu-id="27917-117">WindowsDefender</span><span class="sxs-lookup"><span data-stu-id="27917-117">Windows Defender</span></span>**

    <span data-ttu-id="27917-118">Windows Defender dans Windows 8,1 inclut une protection améliorée.</span><span class="sxs-lookup"><span data-stu-id="27917-118">Windows Defender in Windows 8.1 includes improved protection.</span></span> <span data-ttu-id="27917-119">Les modifications n’ont aucun impact sur l’utilisation de DaRT avec Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="27917-119">The changes do not impact how you use DaRT with Windows Defender.</span></span>

## <span data-ttu-id="27917-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27917-120">Requirements</span></span>


-   **<span data-ttu-id="27917-121">Kit d’évaluation et de développement Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="27917-121">Windows Assessment and Development Kit 8.1</span></span>**

    <span data-ttu-id="27917-122">Le kit d’évaluation et de développement Windows (ADK) 8,1 est une condition requise requise pour l’Assistant image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="27917-122">Windows Assessment and Development Kit (ADK) 8.1 is a required prerequisite for the DaRT Recovery Image Wizard.</span></span> <span data-ttu-id="27917-123">Windows ADK 8,1 contient des outils de déploiement qui permettent de personnaliser, de déployer et de traiter les images Windows.</span><span class="sxs-lookup"><span data-stu-id="27917-123">Windows ADK 8.1 contains deployment tools that are used to customize, deploy, and service Windows images.</span></span> <span data-ttu-id="27917-124">Il contient également l’environnement de préinstallation Windows (Windows PE).</span><span class="sxs-lookup"><span data-stu-id="27917-124">It also contains the Windows Preinstallation Environment (Windows PE).</span></span>

    **<span data-ttu-id="27917-125">Remarque</span><span class="sxs-lookup"><span data-stu-id="27917-125">Note</span></span>**  
    <span data-ttu-id="27917-126">Windows ADK 8,1 n’est pas requis si vous installez uniquement la visionneuse de connexions à distance ou l’analyseur d’incidents.</span><span class="sxs-lookup"><span data-stu-id="27917-126">Windows ADK 8.1 is not required if you are installing only Remote Connection Viewer or Crash Analyzer.</span></span>



~~~
To download Windows ADK 8.1, see [Windows Assessment and Deployment Kit (Windows ADK) for Windows 8.1](https://www.microsoft.com/download/details.aspx?id=39982) in the Microsoft Download Center.
~~~

-   **<span data-ttu-id="27917-127">Microsoft .NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="27917-127">Microsoft .NET Framework 4.5.1</span></span>**

    <span data-ttu-id="27917-128">Le 8,1 de DaRT nécessite l’installation de .NET Framework 4.5.1.</span><span class="sxs-lookup"><span data-stu-id="27917-128">DaRT 8.1 requires that .NET Framework 4.5.1 is installed.</span></span> <span data-ttu-id="27917-129">Pour le télécharger, voir [Microsoft.NET Framework 4.5.1](https://go.microsoft.com/fwlink/?LinkId=329038) dans le centre de téléchargement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="27917-129">To download, see [Microsoft.NET Framework 4.5.1](https://go.microsoft.com/fwlink/?LinkId=329038) in the Microsoft Download Center.</span></span>

-   **<span data-ttu-id="27917-130">Outils de débogage Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="27917-130">Windows 8.1 Debugging Tools</span></span>**

    <span data-ttu-id="27917-131">Pour utiliser l’outil d’analyse des incidents dans DaRT 8,1, vous avez besoin des outils de débogage requis disponibles dans le kit de développement logiciel pour Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="27917-131">To use the Crash Analyzer tool in DaRT 8.1, you need the required debugging tools, which are available in the Software Development Kit for Windows 8.1.</span></span>

    <span data-ttu-id="27917-132">Pour le télécharger, voir [Kit de développement logiciel (SDK) Windows pour windows 8,1](https://msdn.microsoft.com/library/windows/desktop/bg162891.aspx) dans le centre de téléchargement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="27917-132">To download, see [Windows Software Development Kit (SDK) for Windows 8.1](https://msdn.microsoft.com/library/windows/desktop/bg162891.aspx) in the Microsoft Download Center.</span></span>

## <span data-ttu-id="27917-133">Langues disponibles</span><span class="sxs-lookup"><span data-stu-id="27917-133">Language availability</span></span>


<span data-ttu-id="27917-134">Le 8,1 DaRT est disponible dans les langues suivantes:</span><span class="sxs-lookup"><span data-stu-id="27917-134">DaRT 8.1 is available in the following languages:</span></span>

-   <span data-ttu-id="27917-135">Anglais (États-Unis) en-US</span><span class="sxs-lookup"><span data-stu-id="27917-135">English (United States) en-US</span></span>

-   <span data-ttu-id="27917-136">Français (France) fr-FR</span><span class="sxs-lookup"><span data-stu-id="27917-136">French (France) fr-FR</span></span>

-   <span data-ttu-id="27917-137">IT Italien (Italie)-IT</span><span class="sxs-lookup"><span data-stu-id="27917-137">Italian (Italy) it-IT</span></span>

-   <span data-ttu-id="27917-138">Allemand (Allemagne) de-DE</span><span class="sxs-lookup"><span data-stu-id="27917-138">German (Germany) de-DE</span></span>

-   <span data-ttu-id="27917-139">Espagnol, international (Espagne) es-ES</span><span class="sxs-lookup"><span data-stu-id="27917-139">Spanish, International Sort (Spain) es-ES</span></span>

-   <span data-ttu-id="27917-140">Coréen (Corée) ko-KR</span><span class="sxs-lookup"><span data-stu-id="27917-140">Korean (Korea) ko-KR</span></span>

-   <span data-ttu-id="27917-141">Japonais (Japon) ja-JP</span><span class="sxs-lookup"><span data-stu-id="27917-141">Japanese (Japan) ja-JP</span></span>

-   <span data-ttu-id="27917-142">Portugais (Brésil) pt-BR</span><span class="sxs-lookup"><span data-stu-id="27917-142">Portuguese (Brazil) pt-BR</span></span>

-   <span data-ttu-id="27917-143">Russe (Russie) ru-RU</span><span class="sxs-lookup"><span data-stu-id="27917-143">Russian (Russia) ru-RU</span></span>

-   <span data-ttu-id="27917-144">Chinois traditionnel zh-TW</span><span class="sxs-lookup"><span data-stu-id="27917-144">Chinese Traditional zh-TW</span></span>

-   <span data-ttu-id="27917-145">Chinois simplifié zh-NC</span><span class="sxs-lookup"><span data-stu-id="27917-145">Chinese Simplified zh-CN</span></span>

## <span data-ttu-id="27917-146">Obtention de technologies MDOP</span><span class="sxs-lookup"><span data-stu-id="27917-146">How to Get MDOP Technologies</span></span>


<span data-ttu-id="27917-147">DaRT 8,1 fait partie du pack d’optimisation de bureau Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="27917-147">DaRT 8.1 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="27917-148">MDOP fait partie de Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="27917-148">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="27917-149">Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="27917-149">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="27917-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27917-150">Related topics</span></span>


[<span data-ttu-id="27917-151">Notes de publication pour DaRT8.1</span><span class="sxs-lookup"><span data-stu-id="27917-151">Release Notes for DaRT 8.1</span></span>](release-notes-for-dart-81.md)









