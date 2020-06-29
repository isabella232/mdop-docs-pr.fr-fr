---
title: Prise en main de MBAM1.0
description: Prise en main de MBAM1.0
author: dansimp
ms.assetid: 4fab4e4a-d25e-4661-b235-2b45bf5ac3e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0bbbcabfb25cfc8b24cbb4cbc3d344d4e7f209b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811057"
---
# <span data-ttu-id="f124a-103">Prise en main de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f124a-103">Getting Started with MBAM 1.0</span></span>

> <span data-ttu-id="f124a-104">**Important** MBAM 1,0 atteint la fin de la prise en charge le 14 septembre 2021.</span><span class="sxs-lookup"><span data-stu-id="f124a-104">**IMPORTANT** MBAM 1.0 will reach end of support on September 14, 2021.</span></span> 
> <span data-ttu-id="f124a-105">Pour plus d’informations, consultez notre [page de cycle de vie](https://support.microsoft.com/lifecycle/search?alpha=Microsoft%20BitLocker%20Administration%20and%20Monitoring%201.0) .</span><span class="sxs-lookup"><span data-stu-id="f124a-105">See our [lifecycle page](https://support.microsoft.com/lifecycle/search?alpha=Microsoft%20BitLocker%20Administration%20and%20Monitoring%201.0) for more information.</span></span> <span data-ttu-id="f124a-106">Nous vous recommandons de [migrer vers MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions) ou une autre version prise en charge d’MBAM, ou de migrer votre gestion de BitLocker vers le [Gestionnaire de points de terminaison Microsoft](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager).</span><span class="sxs-lookup"><span data-stu-id="f124a-106">We recommend [migrating to MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions) or another supported version of MBAM, or migrating your BitLocker management to [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager).</span></span>


<span data-ttu-id="f124a-107">Le programme d’administration et de surveillance de BitLocker Microsoft (MBAM) nécessite une planification complète avant de pouvoir le déployer ou utiliser ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="f124a-107">Microsoft BitLocker Administration and Monitoring (MBAM) requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="f124a-108">Dans la mesure où ce produit peut affecter chaque ordinateur au sein de votre organisation, vous risquez de perturber votre réseau entier si vous n’avez pas soigneusement planifié votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="f124a-108">Because this product can affect every computer in your organization, you might disrupt your entire network if you do not plan your deployment carefully.</span></span> <span data-ttu-id="f124a-109">Toutefois, si vous planifiez votre déploiement de manière précise et si vous en gérez le fonctionnement selon vos besoins professionnels, MBAM peut vous aider à réduire la charge d’administration et le coût total de propriété.</span><span class="sxs-lookup"><span data-stu-id="f124a-109">However, if you plan your deployment carefully and manage it so that it meets your business needs, MBAM can help reduce your administrative overhead and total cost of ownership.</span></span>

<span data-ttu-id="f124a-110">Si vous débutez avec ce produit, nous vous conseillons de lire entièrement la documentation.</span><span class="sxs-lookup"><span data-stu-id="f124a-110">If you are new to this product, we recommend that you read the documentation thoroughly.</span></span> <span data-ttu-id="f124a-111">Avant de déployer celle-ci dans un environnement de production, nous vous conseillons également de valider votre plan de déploiement dans un environnement réseau de test.</span><span class="sxs-lookup"><span data-stu-id="f124a-111">Before you deploy it to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="f124a-112">Vous pouvez également envisager de prendre un cours sur les technologies pertinentes.</span><span class="sxs-lookup"><span data-stu-id="f124a-112">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="f124a-113">Pour plus d’informations sur les opportunités de formation Microsoft, voir la présentation de la formation Microsoft à l’adresse <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="f124a-113">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="f124a-114">**Remarques**  Vous pouvez trouver une version téléchargeable de cette documentation et le Guide d’évaluation de MBAM à l’adresse <https://go.microsoft.com/fwlink/p/?LinkId=225356> .</span><span class="sxs-lookup"><span data-stu-id="f124a-114">**Note** You can find a downloadable version of this documentation and the MBAM Evaluation Guide at <https://go.microsoft.com/fwlink/p/?LinkId=225356>.</span></span>

 

<span data-ttu-id="f124a-115">Cette section du Guide de l’administrateur MBAM inclut des informations de haut niveau sur MBAM pour vous offrir une connaissance de base du produit avant de commencer la planification du déploiement.</span><span class="sxs-lookup"><span data-stu-id="f124a-115">This section of the MBAM Administrator’s Guide includes high-level information about MBAM to provide you with a basic understanding of the product before you begin the deployment planning.</span></span> <span data-ttu-id="f124a-116">Pour plus d’informations sur MBAM, reportez-vous à la page de téléchargement de ressources de documentation de MBAM à l’adresse <https://go.microsoft.com/fwlink/p/?LinkId=258391> .</span><span class="sxs-lookup"><span data-stu-id="f124a-116">Additional MBAM documentation can be found on the MBAM Documentation Resources Download page at <https://go.microsoft.com/fwlink/p/?LinkId=258391>.</span></span>

## <span data-ttu-id="f124a-117">Mise en route de MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="f124a-117">Getting started with MBAM 1.0</span></span>


-   [<span data-ttu-id="f124a-118">À propos de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f124a-118">About MBAM 1.0</span></span>](about-mbam-10.md)

    <span data-ttu-id="f124a-119">Fournit une vue d’ensemble générale de MBAM et la manière dont il peut être utilisé au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f124a-119">Provides a high-level overview of MBAM and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="f124a-120">Évaluation de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f124a-120">Evaluating MBAM 1.0</span></span>](evaluating-mbam-10.md)

    <span data-ttu-id="f124a-121">Fournit des informations sur la façon dont vous pouvez optimiser l’utilisation de MBAM au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f124a-121">Provides information about how you can best evaluate MBAM for use in your organization.</span></span>

-   [<span data-ttu-id="f124a-122">Architecture de haut niveau pour MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f124a-122">High Level Architecture for MBAM 1.0</span></span>](high-level-architecture-for-mbam-10.md)

    <span data-ttu-id="f124a-123">Décrit les fonctionnalités de MBAM et leur mode de fonctionnement conjoint.</span><span class="sxs-lookup"><span data-stu-id="f124a-123">Provides a description of the MBAM features and how they work together.</span></span>

-   [<span data-ttu-id="f124a-124">Accessibilité de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f124a-124">Accessibility for MBAM 1.0</span></span>](accessibility-for-mbam-10.md)

    <span data-ttu-id="f124a-125">Fournit des informations sur les fonctionnalités et les services qui rendent ce produit et sa documentation correspondante plus accessibles aux personnes atteintes de handicaps.</span><span class="sxs-lookup"><span data-stu-id="f124a-125">Provides information about features and services that make this product and its corresponding documentation more accessible for people with disabilities.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="f124a-126">Autres ressources pour ce produit</span><span class="sxs-lookup"><span data-stu-id="f124a-126">Other resources for this product</span></span>


-   [<span data-ttu-id="f124a-127">Guide d’administration et d’administration de Microsoft BitLocker 1</span><span class="sxs-lookup"><span data-stu-id="f124a-127">Microsoft BitLocker Administration and Monitoring 1 Administrator's Guide</span></span>](index.md)

-   [<span data-ttu-id="f124a-128">Planification de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f124a-128">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

-   [<span data-ttu-id="f124a-129">Déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f124a-129">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

-   [<span data-ttu-id="f124a-130">Opérations de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f124a-130">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

-   [<span data-ttu-id="f124a-131">Résolution des problèmes de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="f124a-131">Troubleshooting MBAM 1.0</span></span>](troubleshooting-mbam-10.md)

 

 





