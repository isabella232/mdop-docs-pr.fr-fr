---
title: Déploiement d'une image d'espace de travail
description: Déploiement d'une image d'espace de travail
author: dansimp
ms.assetid: ccc8e89b-1625-4b58-837e-4c6d93d46070
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4cb16b0a4c278d135fdc9b737aa7a6e9b46115e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812095"
---
# <span data-ttu-id="e503d-103">Déploiement d'une image d'espace de travail</span><span class="sxs-lookup"><span data-stu-id="e503d-103">How to Deploy a Workspace Image</span></span>


<span data-ttu-id="e503d-104">Lors de l’utilisation d’un système de distribution de logiciels d’entreprise, une nouvelle image peut être déployée sur les ordinateurs clients de l’une des façons suivantes:</span><span class="sxs-lookup"><span data-stu-id="e503d-104">When using an enterprise software distribution system, a new image can be deployed onto client computers in one of the following ways:</span></span>

-   [<span data-ttu-id="e503d-105">Téléchargement Web</span><span class="sxs-lookup"><span data-stu-id="e503d-105">Web download</span></span>](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [<span data-ttu-id="e503d-106">Pré-échelonnement d’image</span><span class="sxs-lookup"><span data-stu-id="e503d-106">Image pre-staging</span></span>](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a><span data-ttu-id="e503d-107">Déploiement d’une image d’espace de travail via le Web</span><span class="sxs-lookup"><span data-stu-id="e503d-107">How to Deploy a Workspace Image via the Web</span></span>


**<span data-ttu-id="e503d-108">Pour déployer une image d’espace de travail via le Web</span><span class="sxs-lookup"><span data-stu-id="e503d-108">To deploy a workspace image via the Web</span></span>**

1.  <span data-ttu-id="e503d-109">Téléchargez l’image MED-V sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="e503d-109">Upload the MED-V image to the server.</span></span>

    <span data-ttu-id="e503d-110">Pour plus d’informations sur le téléchargement de l’image, voir [Comment télécharger une image MED-V sur le serveur](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="e503d-110">For information on uploading the image, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

2.  <span data-ttu-id="e503d-111">À l’aide de votre système de distribution de logiciels d’entreprise, installez le package client. msi MED-V sur les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e503d-111">Using your enterprise software distribution system, install the MED-V client .msi package on users’ computers.</span></span>

    <span data-ttu-id="e503d-112">Pour plus d’informations sur l’installation du package client. msi MED-V, voir [Comment installer le client med-v](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="e503d-112">For information on installing the MED-V client .msi package, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span>

    <span data-ttu-id="e503d-113">Le client MED-V est installé et démarré pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="e503d-113">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="e503d-114">Lors du premier démarrage, le client télécharge l’image à partir de l’adresse du serveur spécifiée dans l’installation du client.</span><span class="sxs-lookup"><span data-stu-id="e503d-114">On first-time startup, the client downloads the image from the server address specified in the client installation.</span></span>

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a><span data-ttu-id="e503d-115">Déploiement d’une image d’espace de travail à l’aide du pré-Staging d’image</span><span class="sxs-lookup"><span data-stu-id="e503d-115">How to Deploy a Workspace Image Using Image Pre-staging</span></span>


**<span data-ttu-id="e503d-116">Pour déployer une image d’espace de travail à l’aide de la préinstallation d’image</span><span class="sxs-lookup"><span data-stu-id="e503d-116">To deploy a workspace image using image pre-staging</span></span>**

1.  <span data-ttu-id="e503d-117">Créer un dossier d’image en version préliminaire et le déplacer vers le dossier.</span><span class="sxs-lookup"><span data-stu-id="e503d-117">Create an image pre-stage folder, and push the image to the folder.</span></span>

    <span data-ttu-id="e503d-118">Pour plus d’informations sur la configuration d’une préinstallation d’image, voir [Comment configurer la](how-to-configure-image-pre-staging.md)préinstallation d’une image.</span><span class="sxs-lookup"><span data-stu-id="e503d-118">For information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

2.  <span data-ttu-id="e503d-119">À l’aide de votre système de distribution de logiciels d’entreprise, installez le package client. msi MED-V sur les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e503d-119">Using your enterprise software distribution system, install the MED-V client .msi package on users’ computers.</span></span>

    <span data-ttu-id="e503d-120">Pour plus d’informations sur l’installation du package client. msi MED-V, voir [Comment installer le client med-v](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="e503d-120">For information on installing the MED-V client .msi package, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span>

    <span data-ttu-id="e503d-121">Le client MED-V est installé et démarré pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="e503d-121">MED-V client is installed and started for the first time.</span></span> <span data-ttu-id="e503d-122">Lors du premier démarrage, le client récupère l’image à partir du dossier pre-stage spécifié dans l’installation du client.</span><span class="sxs-lookup"><span data-stu-id="e503d-122">On first-time startup, the client fetches the image from the pre-stage folder specified in the client installation.</span></span>

## <span data-ttu-id="e503d-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e503d-123">Related topics</span></span>


[<span data-ttu-id="e503d-124">Comment configurer le serveur de distribution Web d'images</span><span class="sxs-lookup"><span data-stu-id="e503d-124">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

 

 





