---
title: Déploiement d'une image d'espace de travail
description: Déploiement d'une image d'espace de travail
author: dansimp
ms.assetid: b2c77e0d-101d-4956-a27c-8beb0e4f262e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d691514691286c92bd62d6fda6666345e17eb9f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812101"
---
# <span data-ttu-id="ee609-103">Déploiement d'une image d'espace de travail</span><span class="sxs-lookup"><span data-stu-id="ee609-103">How to Deploy a Workspace Image</span></span>


<span data-ttu-id="ee609-104">Lors de l’utilisation d’un package de déploiement, une nouvelle image peut être déployée sur les ordinateurs clients de l’une des façons suivantes:</span><span class="sxs-lookup"><span data-stu-id="ee609-104">When using a deployment package, a new image can be deployed onto client computers in one of the following ways:</span></span>

-   [<span data-ttu-id="ee609-105">Téléchargement Web</span><span class="sxs-lookup"><span data-stu-id="ee609-105">Web download</span></span>](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [<span data-ttu-id="ee609-106">Pré-échelonnement d’image</span><span class="sxs-lookup"><span data-stu-id="ee609-106">Image pre-staging</span></span>](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

-   [<span data-ttu-id="ee609-107">Déploiement de l’image dans le package de déploiement</span><span class="sxs-lookup"><span data-stu-id="ee609-107">Deploying the image inside the deployment package</span></span>](#bkmk-howtodeployaworkspaceimageusingadeploymentapackage)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a><span data-ttu-id="ee609-108">Déploiement d’une image d’espace de travail via le Web</span><span class="sxs-lookup"><span data-stu-id="ee609-108">How to Deploy a Workspace Image via the Web</span></span>


**<span data-ttu-id="ee609-109">Pour déployer une image d’espace de travail via le Web</span><span class="sxs-lookup"><span data-stu-id="ee609-109">To deploy a workspace image via the Web</span></span>**

1.  <span data-ttu-id="ee609-110">Téléchargez l’image MED-V sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="ee609-110">Upload the MED-V image to the server.</span></span>

    <span data-ttu-id="ee609-111">Pour plus d’informations sur le téléchargement de l’image, voir [Comment télécharger une image MED-V sur le serveur](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="ee609-111">For information on uploading the image, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

2.  <span data-ttu-id="ee609-112">Créez un package de déploiement, puis incluez le chemin d’accès du serveur à l’emplacement de l’image.</span><span class="sxs-lookup"><span data-stu-id="ee609-112">Create a deployment package, and include the server path to the location of the image.</span></span>

    <span data-ttu-id="ee609-113">Pour plus d’informations sur la création d’un package de déploiement, voir [Comment configurer un package de déploiement](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="ee609-113">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

3.  <span data-ttu-id="ee609-114">Déployer le package auprès des utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="ee609-114">Deploy the package to end users.</span></span>

    <span data-ttu-id="ee609-115">Pour plus d’informations sur le déploiement du package, voir [Comment installer le client MED-V](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="ee609-115">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="ee609-116">Le client MED-V est installé et démarré pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="ee609-116">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="ee609-117">Lors du premier démarrage, le client télécharge l’image à partir de l’adresse du serveur spécifiée dans l’installation du client.</span><span class="sxs-lookup"><span data-stu-id="ee609-117">On first-time startup, the client downloads the image from the server address specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a><span data-ttu-id="ee609-118">Déploiement d’une image d’espace de travail à l’aide du pré-Staging d’image</span><span class="sxs-lookup"><span data-stu-id="ee609-118">How to Deploy a Workspace Image Using Image Pre-staging</span></span>


**<span data-ttu-id="ee609-119">Pour déployer une image d’espace de travail à l’aide de la préinstallation d’image</span><span class="sxs-lookup"><span data-stu-id="ee609-119">To deploy a workspace image using image pre-staging</span></span>**

1.  <span data-ttu-id="ee609-120">Créer un dossier d’image en version préliminaire et le déplacer vers le dossier.</span><span class="sxs-lookup"><span data-stu-id="ee609-120">Create an image pre-stage folder, and push the image to the folder.</span></span>

    <span data-ttu-id="ee609-121">Pour plus d’informations sur la configuration d’une préinstallation d’image, voir [Comment configurer la](how-to-configure-image-pre-staging.md)préinstallation d’une image.</span><span class="sxs-lookup"><span data-stu-id="ee609-121">For information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

2.  <span data-ttu-id="ee609-122">Créez un package de déploiement, puis incluez le chemin d’accès au dossier d’image au préalable.</span><span class="sxs-lookup"><span data-stu-id="ee609-122">Create a deployment package, and include the path to the image pre-stage folder.</span></span>

    <span data-ttu-id="ee609-123">Pour plus d’informations sur la création d’un package de déploiement, voir [Comment configurer un package de déploiement](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="ee609-123">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

3.  <span data-ttu-id="ee609-124">Déployer le package auprès des utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="ee609-124">Deploy the package to end users.</span></span>

    <span data-ttu-id="ee609-125">Pour plus d’informations sur le déploiement du package, voir [Comment installer le client MED-V](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="ee609-125">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="ee609-126">Le client MED-V est installé et démarré pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="ee609-126">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="ee609-127">Lors du premier démarrage, le client récupère l’image à partir du dossier pre-stage spécifié dans l’installation du client.</span><span class="sxs-lookup"><span data-stu-id="ee609-127">On first-time startup, the client fetches the image from the pre-stage folder specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingadeploymentapackage"></a><span data-ttu-id="ee609-128">Déploiement d’une image d’espace de travail à l’aide d’un package de déploiement</span><span class="sxs-lookup"><span data-stu-id="ee609-128">How to Deploy a Workspace Image Using a Deployment Package</span></span>


**<span data-ttu-id="ee609-129">Pour déployer une image d’espace de travail à l’aide d’un package de déploiement</span><span class="sxs-lookup"><span data-stu-id="ee609-129">To deploy a workspace image using a deployment package</span></span>**

1.  <span data-ttu-id="ee609-130">Créez un package de déploiement, puis incluez l’image dans le package.</span><span class="sxs-lookup"><span data-stu-id="ee609-130">Create a deployment package, and include the image in the package.</span></span>

    <span data-ttu-id="ee609-131">Pour plus d’informations sur la création d’un package de déploiement, voir [Comment configurer un package de déploiement](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="ee609-131">For information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span>

2.  <span data-ttu-id="ee609-132">Déployer le package auprès des utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="ee609-132">Deploy the package to end users.</span></span>

    <span data-ttu-id="ee609-133">Pour plus d’informations sur le déploiement du package, voir [Comment installer le client MED-V](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="ee609-133">For information on deploying the package, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span>

    <span data-ttu-id="ee609-134">L’image est importée dans l’hôte dans le cadre de l’installation du package.</span><span class="sxs-lookup"><span data-stu-id="ee609-134">The image is imported to the host as part of the package installation.</span></span>

## <span data-ttu-id="ee609-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ee609-135">Related topics</span></span>


[<span data-ttu-id="ee609-136">Comment configurer le serveur de distribution Web d'images</span><span class="sxs-lookup"><span data-stu-id="ee609-136">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

[<span data-ttu-id="ee609-137">Comment configurer un package de déploiement</span><span class="sxs-lookup"><span data-stu-id="ee609-137">How to Configure a Deployment Package</span></span>](how-to-configure-a-deployment-package.md)

 

 





