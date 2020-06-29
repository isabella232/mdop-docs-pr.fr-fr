---
title: Comment charger une image MED-V sur le serveur
description: Comment charger une image MED-V sur le serveur
author: dansimp
ms.assetid: 0e70dfdf-3e3a-4860-970c-535806caa907
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6703eb24bc3542c280af41988a257a2f14643645
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811315"
---
# <span data-ttu-id="c51e0-103">Comment charger une image MED-V sur le serveur</span><span class="sxs-lookup"><span data-stu-id="c51e0-103">How to Upload a MED-V Image to the Server</span></span>


<span data-ttu-id="c51e0-104">Après avoir testé une image MED-V, celle-ci peut être empaquetée puis chargée sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="c51e0-104">After a MED-V image has been tested, it can be packed and then uploaded to the server.</span></span> <span data-ttu-id="c51e0-105">Pour plus d’informations sur la configuration d’un serveur de distribution Web d’images, voir [Comment configurer le serveur de distribution Web d’images](how-to-configure-the-image-web-distribution-server.md).</span><span class="sxs-lookup"><span data-stu-id="c51e0-105">For information on configuring an image Web distribution server, see [How to Configure the Image Web Distribution Server](how-to-configure-the-image-web-distribution-server.md).</span></span>

<span data-ttu-id="c51e0-106">Une fois qu’une image MED-V est compactée et téléchargée sur le serveur, elle peut être distribuée aux utilisateurs à l’aide d’un centre de distribution de logiciels d’entreprise, ou elle peut être téléchargée par les utilisateurs à l’aide d’un package de déploiement.</span><span class="sxs-lookup"><span data-stu-id="c51e0-106">Once a MED-V image is packed and uploaded to the server, it can be distributed to users by using an enterprise software distribution center, or it can be downloaded by users using a deployment package.</span></span> <span data-ttu-id="c51e0-107">Pour plus d’informations sur le déploiement à l’aide d’un centre de distribution de logiciels d’entreprise, voir [déploiement d’un espace de travail MED-V à l’aide d’un système de distribution de logiciels d’entreprise](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="c51e0-107">For information on deployment using an enterprise software distribution center, see [Deploying a MED-V Workspace Using an Enterprise Software Distribution System](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md).</span></span> <span data-ttu-id="c51e0-108">Pour plus d’informations sur le déploiement à l’aide d’un package, voir [déploiement d’un espace de travail MED-V à l’aide d’un package de déploiement](deploying-a-med-v-workspace-using-a-deployment-package.md).</span><span class="sxs-lookup"><span data-stu-id="c51e0-108">For information on deployment using a package, see [Deploying a MED-V Workspace Using a Deployment Package](deploying-a-med-v-workspace-using-a-deployment-package.md).</span></span>

**<span data-ttu-id="c51e0-109">Remarque</span><span class="sxs-lookup"><span data-stu-id="c51e0-109">Note</span></span>**  
<span data-ttu-id="c51e0-110">Avant de télécharger une image, vérifiez qu’aucun proxy Web n’est défini dans les paramètres de votre navigateur et que Windows Update n’est pas en cours d’exécution actuellement.</span><span class="sxs-lookup"><span data-stu-id="c51e0-110">Before uploading an image, verify that a Web proxy is not defined in your browser settings and that Windows Update is not currently running.</span></span>



**<span data-ttu-id="c51e0-111">Pour télécharger une image MED-V sur le serveur</span><span class="sxs-lookup"><span data-stu-id="c51e0-111">To upload a MED-V image to the server</span></span>**

1.  <span data-ttu-id="c51e0-112">Dans le volet **images groupées locales** , sélectionnez l’image que vous avez créée.</span><span class="sxs-lookup"><span data-stu-id="c51e0-112">In the **Local Packed Images** pane, select the image you created.</span></span>

2.  <span data-ttu-id="c51e0-113">Cliquez sur **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="c51e0-113">Click **Upload**.</span></span>

    <span data-ttu-id="c51e0-114">L’image est téléchargée sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="c51e0-114">The image is uploaded to the server.</span></span> <span data-ttu-id="c51e0-115">Cette opération peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="c51e0-115">This might take a considerable amount of time.</span></span>

    <span data-ttu-id="c51e0-116">Les images du serveur sont définies avec les propriétés répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c51e0-116">Images on the server are defined with the properties listed in the following table.</span></span>

**<span data-ttu-id="c51e0-117">Images empaquetées sur les propriétés du serveur</span><span class="sxs-lookup"><span data-stu-id="c51e0-117">Packed Images on Server Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c51e0-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="c51e0-118">Property</span></span></th>
<th align="left"><span data-ttu-id="c51e0-119">Description</span><span class="sxs-lookup"><span data-stu-id="c51e0-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51e0-120">Nom de l’image</span><span class="sxs-lookup"><span data-stu-id="c51e0-120">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51e0-121">Nom de l’image compactée telle qu’elle a été définie lors de la création de l’image par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c51e0-121">The name of the packed image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51e0-122">Version</span><span class="sxs-lookup"><span data-stu-id="c51e0-122">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51e0-123">Version de l’image affichée.</span><span class="sxs-lookup"><span data-stu-id="c51e0-123">The version of the displayed image.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c51e0-124">Remarque</span><span class="sxs-lookup"><span data-stu-id="c51e0-124">Note</span></span></strong><br/><p><span data-ttu-id="c51e0-125">Toutes les versions précédentes sont conservées sauf si supprimées.</span><span class="sxs-lookup"><span data-stu-id="c51e0-125">All previous versions are kept unless deleted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c51e0-126">Taille du fichier (compressé)</span><span class="sxs-lookup"><span data-stu-id="c51e0-126">File Size (compressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51e0-127">Taille compressée physique de l’image.</span><span class="sxs-lookup"><span data-stu-id="c51e0-127">The physical compressed size of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c51e0-128">Taille de l’image (non compressée)</span><span class="sxs-lookup"><span data-stu-id="c51e0-128">Image Size (uncompressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c51e0-129">Taille de l’image qui n’est pas compressée.</span><span class="sxs-lookup"><span data-stu-id="c51e0-129">The physical uncompressed size of the image.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="c51e0-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c51e0-130">Related topics</span></span>


[<span data-ttu-id="c51e0-131">Comment installer le client MED-V et la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="c51e0-131">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

[<span data-ttu-id="c51e0-132">Utilisation de l'interface utilisateur de la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="c51e0-132">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="c51e0-133">Création d'une image Virtual PC pour MED-V</span><span class="sxs-lookup"><span data-stu-id="c51e0-133">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="c51e0-134">Comment empaqueter une image MED-V</span><span class="sxs-lookup"><span data-stu-id="c51e0-134">How to Pack a MED-V Image</span></span>](how-to-pack-a-med-v-image.md)









