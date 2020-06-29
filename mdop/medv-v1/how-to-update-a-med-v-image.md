---
title: Comment mettre à jour une image MED-V
description: Comment mettre à jour une image MED-V
author: dansimp
ms.assetid: 61eacf50-3a00-4bb8-b2f3-7350a6467fa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f62cbd54d8593646460700a86ea48b5df4ce437
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804272"
---
# <span data-ttu-id="bf6aa-103">Comment mettre à jour une image MED-V</span><span class="sxs-lookup"><span data-stu-id="bf6aa-103">How to Update a MED-V Image</span></span>


## <span data-ttu-id="bf6aa-104">Comment mettre à jour une image MED-V</span><span class="sxs-lookup"><span data-stu-id="bf6aa-104">How to Update a MED-V Image</span></span>


<span data-ttu-id="bf6aa-105">Une image MED-V existante peut être mise à jour, créant ainsi une nouvelle version de l’image.</span><span class="sxs-lookup"><span data-stu-id="bf6aa-105">An existing MED-V image can be updated, thereby creating a new version of the image.</span></span> <span data-ttu-id="bf6aa-106">La nouvelle version peut ensuite être déployée sur des ordinateurs client, ce qui remplace l’image existante.</span><span class="sxs-lookup"><span data-stu-id="bf6aa-106">The new version can then be deployed on client computers, replacing the existing image.</span></span>

<span data-ttu-id="bf6aa-107">**Remarques**  Lorsqu’une nouvelle version est déployée sur le client, elle remplace l’image existante.</span><span class="sxs-lookup"><span data-stu-id="bf6aa-107">**Note** When a new version is deployed on the client, it overwrites the existing image.</span></span> <span data-ttu-id="bf6aa-108">Lors de la mise à jour d’une image, assurez-vous qu’aucune donnée ne doit être enregistrée sur le client.</span><span class="sxs-lookup"><span data-stu-id="bf6aa-108">When updating an image, ensure that no data on the client needs to be saved.</span></span>

 

**<span data-ttu-id="bf6aa-109">Pour mettre à jour une image MED-V</span><span class="sxs-lookup"><span data-stu-id="bf6aa-109">To update a MED-V image</span></span>**

1.  <span data-ttu-id="bf6aa-110">Ouvrez l’image existante dans PC2007 virtuel.</span><span class="sxs-lookup"><span data-stu-id="bf6aa-110">Open the existing image in Virtual PC2007.</span></span>

2.  <span data-ttu-id="bf6aa-111">Apportez les modifications requises à l’image, en mettant à jour l’image (par exemple, l’installation d’un nouveau logiciel).</span><span class="sxs-lookup"><span data-stu-id="bf6aa-111">Make the required changes to the image, updating the image (such as installing new software).</span></span>

3.  <span data-ttu-id="bf6aa-112">Fermez les PC2007 virtuelles.</span><span class="sxs-lookup"><span data-stu-id="bf6aa-112">Close Virtual PC2007.</span></span>

4.  <span data-ttu-id="bf6aa-113">Testez l’image.</span><span class="sxs-lookup"><span data-stu-id="bf6aa-113">Test the image.</span></span>

5.  <span data-ttu-id="bf6aa-114">Une fois l’image testée, empaquetez-la sur le référentiel local en utilisant le même nom que l’image existante.</span><span class="sxs-lookup"><span data-stu-id="bf6aa-114">After the image is tested, pack it to the local repository, using the same name as the existing image.</span></span>

    <span data-ttu-id="bf6aa-115">**Remarques**  Si vous nommez l’image un nom différent de la version existante, une nouvelle image sera créée plutôt qu’une nouvelle version de l’image existante.</span><span class="sxs-lookup"><span data-stu-id="bf6aa-115">**Note** If you name the image a different name than the existing version, a new image will be created rather than a new version of the existing image.</span></span>

     

6.  <span data-ttu-id="bf6aa-116">Téléchargez la nouvelle version sur le serveur ou Répartissez-la par le biais d’un package de déploiement.</span><span class="sxs-lookup"><span data-stu-id="bf6aa-116">Upload the new version to the server or distribute it via a deployment package.</span></span>

## <span data-ttu-id="bf6aa-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bf6aa-117">Related topics</span></span>


[<span data-ttu-id="bf6aa-118">Création d'une image Virtual PC pour MED-V</span><span class="sxs-lookup"><span data-stu-id="bf6aa-118">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="bf6aa-119">Comment créer et tester une image MED-V</span><span class="sxs-lookup"><span data-stu-id="bf6aa-119">How to Create and Test a MED-V Image</span></span>](how-to-create-and-test-a-med-v-image.md)

[<span data-ttu-id="bf6aa-120">Comment empaqueter une image MED-V</span><span class="sxs-lookup"><span data-stu-id="bf6aa-120">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)

[<span data-ttu-id="bf6aa-121">Comment charger une image MED-V sur le serveur</span><span class="sxs-lookup"><span data-stu-id="bf6aa-121">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)

[<span data-ttu-id="bf6aa-122">Mise à jour d'une image d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="bf6aa-122">Updating a MED-V Workspace Image</span></span>](updating-a-med-v-workspace-image.md)

 

 





