---
title: Déploiement d'un espace de travail MED-V à l'aide d'un package de déploiement
description: Déploiement d'un espace de travail MED-V à l'aide d'un package de déploiement
author: dansimp
ms.assetid: e07fa70a-1a9f-486f-9a86-b33593b234da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc16b32fd44e45606df5502fda2e580d404dbb19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810073"
---
# <span data-ttu-id="6fc5c-103">Déploiement d'un espace de travail MED-V à l'aide d'un package de déploiement</span><span class="sxs-lookup"><span data-stu-id="6fc5c-103">Deploying a MED-V Workspace Using a Deployment Package</span></span>


<span data-ttu-id="6fc5c-104">L’installation du package de déploiement fournit une méthode d’installation du client MED-V et de l’ensemble de ses éléments requis, ainsi que des paramètres prédéfinis par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-104">The deployment package installation provides a method of installing MED-V client together with all its required prerequisites as well as any settings predefined by the administrator.</span></span>

<span data-ttu-id="6fc5c-105">Lors de l’utilisation d’un package de déploiement, le package est distribué via un réseau partagé ou un média amovible.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-105">When using a deployment package, the package is distributed via a shared network or removable media.</span></span> <span data-ttu-id="6fc5c-106">L’image peut être incluse dans le package ou être distribuée séparément.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-106">The image can be included in the package or can be distributed separately.</span></span>

<span data-ttu-id="6fc5c-107">Avant de créer un package de déploiement, assurez-vous que vous avez créé une image MED-V prête pour le déploiement.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-107">Before creating a deployment package, ensure that you have created a MED-V image ready for deployment.</span></span> <span data-ttu-id="6fc5c-108">Pour plus d’informations sur la création d’une image MED-V, voir [création d’une image med-v](creating-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="6fc5c-108">For more information on creating a MED-V image, see [Creating a MED-V Image](creating-a-med-v-image.md).</span></span>

<span data-ttu-id="6fc5c-109">Après avoir préparé l’image MED-V, considérez la meilleure méthode de distribution de l’image dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-109">After the MED-V image is prepared, consider the best method for distributing the image in your environment.</span></span> <span data-ttu-id="6fc5c-110">L’image peut être distribuée de l’une des façons suivantes:</span><span class="sxs-lookup"><span data-stu-id="6fc5c-110">The image can be distributed in one of the following ways:</span></span>

-   <span data-ttu-id="6fc5c-111">Téléchargé sur le Web et distribué via le téléchargement Web, en utilisant éventuellement la technologie de transfert de découpage.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-111">Uploaded to the Web and distributed via Web download, optionally using Trim Transfer technology.</span></span>

-   <span data-ttu-id="6fc5c-112">Distribués à l’aide de la version préliminaire d’image.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-112">Distributed using image pre-staging.</span></span>

-   <span data-ttu-id="6fc5c-113">Inclus dans le package de déploiement et répartis avec tous les autres composants MED-V.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-113">Included in the deployment package and distributed together with all the other MED-V components.</span></span>

<span data-ttu-id="6fc5c-114">Si l’image sera incluse dans le package, aucune autre configuration n’est nécessaire pour l’image.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-114">If the image will be included in the package, no other configurations are necessary for the image.</span></span> <span data-ttu-id="6fc5c-115">Si l’image ne sera pas incluse dans le package de déploiement, effectuez l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="6fc5c-115">If the image will not be included in the deployment package, do one of the following:</span></span>

-   <span data-ttu-id="6fc5c-116">Si vous déployez l’image par le biais du Web, téléchargez l’image MED-V sur le serveur de distribution Web d’images.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-116">If you are deploying the image via the Web, upload the MED-V image to the image Web distribution server.</span></span> <span data-ttu-id="6fc5c-117">Pour plus d’informations sur la configuration d’un serveur de distribution Web d’images, voir [Comment configurer le serveur de distribution Web d’images](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="6fc5c-117">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span> <span data-ttu-id="6fc5c-118">Pour plus d’informations sur le téléchargement d’une image sur le serveur, voir [Comment télécharger une image MED-V sur le serveur](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="6fc5c-118">For information on uploading an image to the server, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

-   <span data-ttu-id="6fc5c-119">Si vous déployez l’image par le biais d’une préinstallation d’image, configurez le dossier pre-Staging et transmettez l’image MED-V au dossier.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-119">If you are deploying the image via image pre-staging, configure the pre-stage folder, and push the MED-V image to the folder.</span></span> <span data-ttu-id="6fc5c-120">Pour plus d’informations sur la configuration de la pré-version d’image, voir [Comment configurer](how-to-configure-image-pre-staging.md)la préinstallation d’une image.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-120">For more information on configuring the image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

<span data-ttu-id="6fc5c-121">**Remarques**  Si vous utilisez le prédéploiement d’image, il est important de configurer le dossier d’image avant de créer le package de déploiement.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-121">**Note** If you are using image pre-staging, it is important to configure the image pre-stage folder prior to creating the deployment package.</span></span> <span data-ttu-id="6fc5c-122">Le chemin d’accès au dossier doit être inclus dans le package de déploiement.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-122">The folder path needs to be included in the deployment package.</span></span>

 

<span data-ttu-id="6fc5c-123">Enfin, créez le package de déploiement.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-123">Finally, create the deployment package.</span></span> <span data-ttu-id="6fc5c-124">Pour plus d’informations sur la création d’un package de déploiement, voir [Comment configurer un package de déploiement](how-to-configure-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="6fc5c-124">For more information on creating a deployment package, see [How to Configure a Deployment Package](how-to-configure-a-deployment-package.md).</span></span> <span data-ttu-id="6fc5c-125">Une fois le package terminé, distribuez-le pour le déploiement.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-125">After the package is complete, distribute it for deployment.</span></span>

<span data-ttu-id="6fc5c-126">Une fois le package de déploiement distribué, le client MED-V peut être installé et l’image déployée.</span><span class="sxs-lookup"><span data-stu-id="6fc5c-126">After the deployment package is distributed, MED-V client can be installed and the image deployed.</span></span> <span data-ttu-id="6fc5c-127">Pour plus d’informations sur l’installation du client MED-V, voir [Comment installer le client med-v](how-to-install-med-v-clientdeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="6fc5c-127">For more information on installing MED-V client, see [How to Install MED-V Client](how-to-install-med-v-clientdeployment-package.md).</span></span> <span data-ttu-id="6fc5c-128">Pour plus d’informations sur le déploiement de l’image, reportez-vous [à la rubrique déploiement d’une image d’espace de travail](how-to-deploy-a-workspace-imagedeployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="6fc5c-128">For more information on deploying the image, see [How to Deploy a Workspace Image](how-to-deploy-a-workspace-imagedeployment-package.md).</span></span>

 

 





