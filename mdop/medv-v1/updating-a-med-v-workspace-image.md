---
title: Mise à jour d'une image d'espace de travail MED-V
description: Mise à jour d'une image d'espace de travail MED-V
author: dansimp
ms.assetid: 1b9c4a73-3487-43d2-98e3-43dbc79e10e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60a5d12622e0cb7012c6d0a22124d63c085f6d0a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811405"
---
# <span data-ttu-id="854f3-103">Mise à jour d'une image d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="854f3-103">Updating a MED-V Workspace Image</span></span>


<span data-ttu-id="854f3-104">Il est possible de mettre à jour une image de l’une des façons suivantes:</span><span class="sxs-lookup"><span data-stu-id="854f3-104">An image can be updated in one of the following ways:</span></span>

-   <span data-ttu-id="854f3-105">La mise à jour peut être poussée vers le système d’exploitation invité à l’aide de votre système de distribution de logiciels d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="854f3-105">The update can be pushed to the guest operating system using your enterprise software distribution system.</span></span>

-   <span data-ttu-id="854f3-106">La mise à jour peut être téléchargée sur le serveur de distribution Web d’images, puis téléchargée par le client et appliquée à l’image MED-V.</span><span class="sxs-lookup"><span data-stu-id="854f3-106">The update can be uploaded to the image Web distribution server, and then downloaded by the client and applied to the MED-V image.</span></span>

-   <span data-ttu-id="854f3-107">L’image de base MED-V peut être mise à jour et redéployée.</span><span class="sxs-lookup"><span data-stu-id="854f3-107">The MED-V base image can be updated and redeployed.</span></span>

## <a href="" id="bkmk-howtoupdateamedvimageusinganesd"></a><span data-ttu-id="854f3-108">Comment mettre à jour une image MED-V à l’aide d’un système de distribution de logiciels d’entreprise</span><span class="sxs-lookup"><span data-stu-id="854f3-108">How to Update a MED-V Image Using an Enterprise Software Distribution System</span></span>


**<span data-ttu-id="854f3-109">Pour mettre à jour une image MED-V à l’aide d’un système de distribution de logiciels d’entreprise</span><span class="sxs-lookup"><span data-stu-id="854f3-109">To update a MED-V image using an enterprise software distribution system</span></span>**

-   <span data-ttu-id="854f3-110">Reportez-vous à la documentation du système que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="854f3-110">Refer to the documentation of the system you are using.</span></span>

## <a href="" id="bkmk-howtoupdateamedvimageusingwebdownload"></a><span data-ttu-id="854f3-111">Comment mettre à jour une image MED-V à l’aide du téléchargement Web</span><span class="sxs-lookup"><span data-stu-id="854f3-111">How to Update a MED-V Image Using Web Download</span></span>


**<span data-ttu-id="854f3-112">Pour mettre à jour une image MED-V à l’aide du téléchargement Web</span><span class="sxs-lookup"><span data-stu-id="854f3-112">To update a MED-V image using Web download</span></span>**

1.  <span data-ttu-id="854f3-113">Dans le cadre de la gestion de MED-V, sur l’onglet **machine virtuelle** , assurez-vous que les paramètres suivants s’appliquent aux stratégies d’espace de travail MED-v qui sont associées à la mise à jour de l’image med-v:</span><span class="sxs-lookup"><span data-stu-id="854f3-113">In MED-V management, on the **Virtual Machine** tab, ensure that the following settings are applied to the MED-V workspace policies that are associated with the MED-V image being updated:</span></span>

    -   <span data-ttu-id="854f3-114">La case à cocher **suggérer une mise à jour lorsqu’une nouvelle version est disponible** est activée.</span><span class="sxs-lookup"><span data-stu-id="854f3-114">The **Suggest update when a new version is available** check box is selected.</span></span>

    -   <span data-ttu-id="854f3-115">Le cas échéant, les **clients doivent utiliser l’option découper lors du téléchargement d’images pour cet espace de travail** est activée.</span><span class="sxs-lookup"><span data-stu-id="854f3-115">Optionally, the **Clients should use Trim Transfer when downloading images for this Workspace** check box is selected.</span></span>

    <span data-ttu-id="854f3-116">Pour plus d’informations, reportez-vous [à la rubrique Comment appliquer des paramètres d’ordinateur virtuel à un espace de travail MED-V](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="854f3-116">For more information, see [How to Apply Virtual Machine Settings to a MED-V Workspace](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).</span></span>

2.  <span data-ttu-id="854f3-117">Téléchargez la mise à jour d’image vers le serveur de distribution Web d’images.</span><span class="sxs-lookup"><span data-stu-id="854f3-117">Upload the image update to the image Web distribution server.</span></span>

    <span data-ttu-id="854f3-118">Tous les clients contenant des images qui doivent être mises à jour sont automatiquement téléchargés et appliqués à l’image.</span><span class="sxs-lookup"><span data-stu-id="854f3-118">All clients with images that need to be updated automatically download the update and apply it to the image.</span></span>

## <a href="" id="bkmk-howtoupdateamedvbaseimage"></a><span data-ttu-id="854f3-119">Comment mettre à jour une image de base MED-V</span><span class="sxs-lookup"><span data-stu-id="854f3-119">How to Update a MED-V Base Image</span></span>


**<span data-ttu-id="854f3-120">Pour mettre à jour une image de base MED-V</span><span class="sxs-lookup"><span data-stu-id="854f3-120">To update a MED-V base image</span></span>**

1.  <span data-ttu-id="854f3-121">Ouvrez l’image existante dans PC2007 virtuel.</span><span class="sxs-lookup"><span data-stu-id="854f3-121">Open the existing image in Virtual PC2007.</span></span>

2.  <span data-ttu-id="854f3-122">Apportez les modifications requises à l’image, en mettant à jour l’image (par exemple, l’installation d’un nouveau logiciel).</span><span class="sxs-lookup"><span data-stu-id="854f3-122">Make the required changes to the image, updating the image (such as installing new software).</span></span>

3.  <span data-ttu-id="854f3-123">Fermez les PC2007 virtuelles.</span><span class="sxs-lookup"><span data-stu-id="854f3-123">Close Virtual PC2007.</span></span>

4.  <span data-ttu-id="854f3-124">Testez l’image.</span><span class="sxs-lookup"><span data-stu-id="854f3-124">Test the image.</span></span>

5.  <span data-ttu-id="854f3-125">Une fois l’image testée, empaquetez-la sur le référentiel local en utilisant le même nom que l’image existante.</span><span class="sxs-lookup"><span data-stu-id="854f3-125">After the image is tested, pack it to the local repository, using the same name as the existing image.</span></span>

    <span data-ttu-id="854f3-126">**Remarques**  Si vous nommez l’image un nom différent de la version existante, une nouvelle image sera créée plutôt qu’une nouvelle version de l’image existante.</span><span class="sxs-lookup"><span data-stu-id="854f3-126">**Note** If you name the image a different name than the existing version, a new image will be created rather than a new version of the existing image.</span></span>

     

6.  <span data-ttu-id="854f3-127">Téléchargez la nouvelle version sur le serveur, encadrez-la dans le dossier d’image prédéfinie ou distribuez-la par le biais d’un package de déploiement.</span><span class="sxs-lookup"><span data-stu-id="854f3-127">Upload the new version to the server, push it to the image pre-stage folder, or distribute it via a deployment package.</span></span>

## <span data-ttu-id="854f3-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="854f3-128">Related topics</span></span>


[<span data-ttu-id="854f3-129">Création d'une image MED-V</span><span class="sxs-lookup"><span data-stu-id="854f3-129">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)

[<span data-ttu-id="854f3-130">Comment mettre à jour une image MED-V</span><span class="sxs-lookup"><span data-stu-id="854f3-130">How to Update a MED-V Image</span></span>](how-to-update-a-med-v-image.md)

[<span data-ttu-id="854f3-131">Configuration de stratégies d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="854f3-131">Configuring MED-V Workspace Policies</span></span>](configuring-med-v-workspace-policies.md)

[<span data-ttu-id="854f3-132">Comment configurer le serveur de distribution Web d'images</span><span class="sxs-lookup"><span data-stu-id="854f3-132">How to Configure the Image Web Distribution Server</span></span>](how-to-configure-the-image-web-distribution-server.md)

 

 





