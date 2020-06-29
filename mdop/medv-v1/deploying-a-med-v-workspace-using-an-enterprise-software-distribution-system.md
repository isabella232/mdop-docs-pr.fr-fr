---
title: Déploiement d'un espace de travail MED-V à l'aide d'un système de distribution de logiciels d'entreprise
description: Déploiement d'un espace de travail MED-V à l'aide d'un système de distribution de logiciels d'entreprise
author: dansimp
ms.assetid: 867faed6-74ce-4573-84be-8bf26e66c08c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb9ebbc0fb605f84c5a8e67fc77fd9be51b29ff4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810068"
---
# <span data-ttu-id="bf276-103">Déploiement d'un espace de travail MED-V à l'aide d'un système de distribution de logiciels d'entreprise</span><span class="sxs-lookup"><span data-stu-id="bf276-103">Deploying a MED-V Workspace Using an Enterprise Software Distribution System</span></span>


<span data-ttu-id="bf276-104">Le client MED-V peut être distribué à l’aide d’un système de distribution de logiciels d’entreprise, tel que Microsoft System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bf276-104">MED-V client can be distributed using an enterprise software distribution system, such as Microsoft System Center Configuration Manager.</span></span>

<span data-ttu-id="bf276-105">**Remarques**  Si MED-V est installé à l’aide de Microsoft System Center Configuration Manager, lors de la création d’un package pour MED-V, définissez le mode d’exécution sur droits d’administration.</span><span class="sxs-lookup"><span data-stu-id="bf276-105">**Note** If MED-V is installed by using Microsoft System Center Configuration Manager, when creating a package for MED-V, set the run mode to administrative rights.</span></span>

 

<span data-ttu-id="bf276-106">Avant de déployer MED-V à l’aide d’un système de distribution de logiciels d’entreprise, assurez-vous que vous avez créé une image MED-V prête pour le déploiement.</span><span class="sxs-lookup"><span data-stu-id="bf276-106">Before deploying MED-V using an enterprise software distribution system, ensure that you have created a MED-V image ready for deployment.</span></span> <span data-ttu-id="bf276-107">Pour plus d’informations sur la création d’une image MED-V, voir [création d’une image med-v](creating-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="bf276-107">For more information on creating a MED-V image, see [Creating a MED-V Image](creating-a-med-v-image.md).</span></span>

<span data-ttu-id="bf276-108">Après avoir préparé l’image MED-V, considérez la meilleure méthode de distribution de l’image dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="bf276-108">After the MED-V image is prepared, consider the best method for distributing the image in your environment.</span></span> <span data-ttu-id="bf276-109">L’image peut être distribuée de l’une des façons suivantes:</span><span class="sxs-lookup"><span data-stu-id="bf276-109">The image can be distributed in one of the following ways:</span></span>

-   <span data-ttu-id="bf276-110">Téléchargé sur le Web et distribué via le téléchargement Web, en utilisant éventuellement la technologie de transfert de découpage.</span><span class="sxs-lookup"><span data-stu-id="bf276-110">Uploaded to the Web and distributed via Web download, optionally utilizing Trim Transfer technology.</span></span>

-   <span data-ttu-id="bf276-111">Distribués à l’aide de la version préliminaire d’image.</span><span class="sxs-lookup"><span data-stu-id="bf276-111">Distributed using image pre-staging.</span></span>

## <span data-ttu-id="bf276-112">Déploiement de l’image par le biais du Web</span><span class="sxs-lookup"><span data-stu-id="bf276-112">Deploying the Image via the Web</span></span>


<span data-ttu-id="bf276-113">Si vous déployez l’image par le biais du Web, téléchargez l’image MED-V sur un serveur de distribution Web image.</span><span class="sxs-lookup"><span data-stu-id="bf276-113">If you are deploying the image via the Web, upload the MED-V image to an image Web distribution server.</span></span> <span data-ttu-id="bf276-114">Pour plus d’informations sur la configuration d’un serveur de distribution Web d’images, voir [Comment configurer le serveur de distribution Web d’images](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="bf276-114">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span> <span data-ttu-id="bf276-115">Pour plus d’informations sur le téléchargement d’une image sur le serveur, voir [Comment télécharger une image MED-V sur le serveur](how-to-upload-a-med-v-image-to-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="bf276-115">For information on uploading an image to the server, see [How to Upload a MED-V Image to the Server](how-to-upload-a-med-v-image-to-the-server.md).</span></span>

## <span data-ttu-id="bf276-116">Déploiement de l’image par pré-Staging</span><span class="sxs-lookup"><span data-stu-id="bf276-116">Deploying the Image via Pre-staging</span></span>


<span data-ttu-id="bf276-117">Si vous déployez l’image par le biais d’une préinstallation d’image, configurez le dossier pre-Staging et transmettez l’image MED-V au dossier.</span><span class="sxs-lookup"><span data-stu-id="bf276-117">If you are deploying the image via image pre-staging, configure the pre-stage folder, and push the MED-V image to the folder.</span></span> <span data-ttu-id="bf276-118">Pour plus d’informations sur la configuration d’une préinstallation d’image, voir [Comment configurer la](how-to-configure-image-pre-staging.md)préinstallation d’une image.</span><span class="sxs-lookup"><span data-stu-id="bf276-118">For more information on configuring image pre-staging, see [How to Configure Image Pre-staging](how-to-configure-image-pre-staging.md).</span></span>

<span data-ttu-id="bf276-119">**Remarques**  Si vous utilisez le prédéploiement d’image, il est important de configurer le dossier d’image avant de pousser le package client. msi.</span><span class="sxs-lookup"><span data-stu-id="bf276-119">**Note** If you are using image pre-staging, it is important to configure the image pre-stage folder prior to pushing the client .msi package.</span></span> <span data-ttu-id="bf276-120">Le chemin d’accès au dossier doit être inclus dans le package client. msi.</span><span class="sxs-lookup"><span data-stu-id="bf276-120">The folder path needs to be included in the client .msi package.</span></span>

 

<span data-ttu-id="bf276-121">Enfin, envoyez le package client. msi à l’aide du centre de distribution de logiciels de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="bf276-121">Finally, push the client .msi package using your enterprise software distribution center.</span></span> <span data-ttu-id="bf276-122">MED-V peut alors être installé et l’image déployée.</span><span class="sxs-lookup"><span data-stu-id="bf276-122">MED-V can then be installed and the image deployed.</span></span> <span data-ttu-id="bf276-123">Pour plus d’informations sur l’installation du client MED-V, voir [Comment installer le client med-v](how-to-install-med-v-clientesds.md).</span><span class="sxs-lookup"><span data-stu-id="bf276-123">For more information on installing MED-V client, see [How to Install MED-V Client](how-to-install-med-v-clientesds.md).</span></span> <span data-ttu-id="bf276-124">Pour plus d’informations sur le déploiement de l’image, reportez-vous [à la rubrique déploiement d’une image d’espace de travail](how-to-deploy-a-workspace-imageesds.md).</span><span class="sxs-lookup"><span data-stu-id="bf276-124">For more information on deploying the image, see [How to Deploy a Workspace Image](how-to-deploy-a-workspace-imageesds.md).</span></span>

 

 





