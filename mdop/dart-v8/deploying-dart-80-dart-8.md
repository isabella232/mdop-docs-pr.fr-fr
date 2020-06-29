---
title: Déploiement de DaRT8.0
description: Déploiement de DaRT8.0
author: dansimp
ms.assetid: 5a976d4e-3372-4ef6-9095-1b48e99af21b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7cc847836587abb0eaa22c009c8fd18d0ba0899b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810391"
---
# <span data-ttu-id="45700-103">Déploiement de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="45700-103">Deploying DaRT 8.0</span></span>


<span data-ttu-id="45700-104">Microsoft Diagnostics and Recovery Tools (DaRT) 8,0 prend en charge plusieurs configurations de déploiement.</span><span class="sxs-lookup"><span data-stu-id="45700-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 supports a number of different deployment configurations.</span></span> <span data-ttu-id="45700-105">Cette section comprend des informations que vous devez prendre en compte sur le déploiement de la 8,0 et des procédures pas à pas pour vous aider à effectuer les tâches que vous devez effectuer à différentes étapes de votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="45700-105">This section includes information you should consider about the deployment of DaRT 8.0 and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

## <span data-ttu-id="45700-106">Informations de déploiement</span><span class="sxs-lookup"><span data-stu-id="45700-106">Deployment Information</span></span>


-   [<span data-ttu-id="45700-107">Déploiement de DaRT8.0 sur les ordinateurs des administrateurs</span><span class="sxs-lookup"><span data-stu-id="45700-107">Deploying DaRT 8.0 to Administrator Computers</span></span>](deploying-dart-80-to-administrator-computers-dart-8.md)

    <span data-ttu-id="45700-108">Cette section décrit les différentes options de déploiement DaRT correspondant à vos besoins et explique comment les déployer.</span><span class="sxs-lookup"><span data-stu-id="45700-108">This section describes the different DaRT deployment options for your requirements and explains how to deploy them.</span></span>

-   [<span data-ttu-id="45700-109">Création de l'image de récupération DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="45700-109">Creating the DaRT 8.0 Recovery Image</span></span>](creating-the-dart-80-recovery-image-dart-8.md)

    <span data-ttu-id="45700-110">Cette section décrit les méthodes que vous pouvez utiliser pour créer l’image de récupération DaRT et fournit des instructions pour créer l’image de récupération à l’aide de l’Assistant image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="45700-110">This section describes the methods you can use to create the DaRT recovery image and provides instructions to create the recovery image by using the DaRT Recovery Image wizard.</span></span>

-   [<span data-ttu-id="45700-111">Déploiement de l'image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="45700-111">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-8.md)

    <span data-ttu-id="45700-112">Cette section fournit des informations pour vous aider à déterminer la meilleure option de déploiement d’image de récupération DaRT pour vos exigences et fournit des instructions sur le déploiement de l’image de récupération.</span><span class="sxs-lookup"><span data-stu-id="45700-112">This section provides information to help you decide on the best DaRT recovery image deployment option for your requirements and provides instructions on how to deploy the recovery image.</span></span>

-   [<span data-ttu-id="45700-113">Liste de contrôle du déploiement de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="45700-113">DaRT 8.0 Deployment Checklist</span></span>](dart-80-deployment-checklist-dart-8.md)

    <span data-ttu-id="45700-114">Cette section contient une liste de vérification de déploiement qui peut vous aider à déployer DaRT.</span><span class="sxs-lookup"><span data-stu-id="45700-114">This section contains a deployment checklist that can help you to deploy DaRT.</span></span>

### <span data-ttu-id="45700-115">Comment obtenir DaRT</span><span class="sxs-lookup"><span data-stu-id="45700-115">How to get DaRT</span></span>

<span data-ttu-id="45700-116">Cette technologie fait partie du pack d’optimisation de bureau Microsoft (MDOP).</span><span class="sxs-lookup"><span data-stu-id="45700-116">This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="45700-117">Les clients d’entreprise peuvent obtenir MDOP avec Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="45700-117">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="45700-118">Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/p/?LinkId=322049) ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="45700-118">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/p/?LinkId=322049) (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

## <span data-ttu-id="45700-119">Autres ressources pour le déploiement de DaRT</span><span class="sxs-lookup"><span data-stu-id="45700-119">Other Resources for deploying DaRT</span></span>


[<span data-ttu-id="45700-120">Guide de l’administrateur des outils de diagnostics et de récupération</span><span class="sxs-lookup"><span data-stu-id="45700-120">Diagnostics and Recovery Toolset 8 Administrator's Guide</span></span>](index.md)

[<span data-ttu-id="45700-121">Prise en main de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="45700-121">Getting Started with DaRT 8.0</span></span>](getting-started-with-dart-80-dart-8.md)

[<span data-ttu-id="45700-122">Planification de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="45700-122">Planning for DaRT 8.0</span></span>](planning-for-dart-80-dart-8.md)

[<span data-ttu-id="45700-123">Opérations de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="45700-123">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

[<span data-ttu-id="45700-124">Résolution des problèmes liés à DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="45700-124">Troubleshooting DaRT 8.0</span></span>](troubleshooting-dart-80-dart-8.md)

 

 





