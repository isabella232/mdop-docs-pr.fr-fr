---
title: Comment empaqueter une image MED-V
description: Comment empaqueter une image MED-V
author: dansimp
ms.assetid: e1ce2307-0f1b-4bf8-b146-e4012dc138d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a330b8feca922239691bed083767c3acc57105d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810698"
---
# <span data-ttu-id="a1174-103">Comment empaqueter une image MED-V</span><span class="sxs-lookup"><span data-stu-id="a1174-103">How to Pack a MED-V Image</span></span>


<span data-ttu-id="a1174-104">Une image MED-V doit être empaquetée avant d’être ajoutée à un package de déploiement ou chargée sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="a1174-104">A MED-V image must be packed before it can be added to a deployment package or uploaded to the server.</span></span>

**<span data-ttu-id="a1174-105">Pour créer une image MED-V empaquetée</span><span class="sxs-lookup"><span data-stu-id="a1174-105">To create a packed MED-V image</span></span>**

1.  <span data-ttu-id="a1174-106">Cliquez sur le bouton gestion des **images** .</span><span class="sxs-lookup"><span data-stu-id="a1174-106">Click the **Images** management button.</span></span>

2.  <span data-ttu-id="a1174-107">Dans le module **images** , dans le volet **images groupées locales** , cliquez sur **nouveau**.</span><span class="sxs-lookup"><span data-stu-id="a1174-107">In the **Images** module, in the **Local Packed Images** pane, click **New**.</span></span>

3.  <span data-ttu-id="a1174-108">Dans la boîte de dialogue **création d’images compactées** , sélectionnez l’image de l’ordinateur virtuel en effectuant l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="a1174-108">In the **Packed Image Creation** dialog box, select the virtual machine image by doing one of the following:</span></span>

    -   <span data-ttu-id="a1174-109">Dans le champ **fichier image de base** , tapez le chemin d’accès complet au répertoire dans lequel se trouve l’image Microsoft Virtual PC préparée pour MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1174-109">In the **Base image file** field, type the full path to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

    -   <span data-ttu-id="a1174-110">Cliquez sur **Parcourir** pour accéder au répertoire dans lequel se trouve l’image Microsoft Virtual PC préparée pour MED-V.</span><span class="sxs-lookup"><span data-stu-id="a1174-110">Click **Browse** to browse to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

4.  <span data-ttu-id="a1174-111">Spécifiez le nom de la nouvelle image en effectuant l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="a1174-111">Specify the name of the new image by doing one of the following:</span></span>

    -   <span data-ttu-id="a1174-112">Dans le champ nom de l' **image** , tapez le nom souhaité.</span><span class="sxs-lookup"><span data-stu-id="a1174-112">In the **Image name** field, type the desired name.</span></span>

        **<span data-ttu-id="a1174-113">Remarque</span><span class="sxs-lookup"><span data-stu-id="a1174-113">Note</span></span>**  
        <span data-ttu-id="a1174-114">Les caractères suivants ne peuvent pas être inclus dans le nom de l’image: Space " &lt; &gt; | \\ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="a1174-114">The following characters cannot be included in the image name: space " &lt; &gt; | \\ / : \* ?</span></span>



~~~
    A new packed image will be created.

-   From the drop-down list, select an existing name.

    A new version of the existing image will be created.
~~~

5. <span data-ttu-id="a1174-115">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a1174-115">Click **OK**.</span></span>

   <span data-ttu-id="a1174-116">Une nouvelle image empaquetée MED-V est créée sur votre ordinateur hôte avec les propriétés définies dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a1174-116">A new MED-V packed image is created on your host computer with the properties defined in the following table.</span></span>

**<span data-ttu-id="a1174-117">Remarque</span><span class="sxs-lookup"><span data-stu-id="a1174-117">Note</span></span>**  
<span data-ttu-id="a1174-118">Dans les **images compactées locales** et sur les volets **serveur** , la version la plus récente de chaque image est affichée en tant que nœud parent.</span><span class="sxs-lookup"><span data-stu-id="a1174-118">In the **Local Packed Images** and **Packed Images on Server** panes, the most recent version of each image is displayed as the parent node.</span></span> <span data-ttu-id="a1174-119">Cliquez sur le nœud parent pour afficher toutes les autres versions existantes de l’image.</span><span class="sxs-lookup"><span data-stu-id="a1174-119">Click the parent node to view all other existing versions of the image.</span></span>



**<span data-ttu-id="a1174-120">Propriétés d’images compactées locales</span><span class="sxs-lookup"><span data-stu-id="a1174-120">Local Packed Images Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a1174-121">Propriété</span><span class="sxs-lookup"><span data-stu-id="a1174-121">Property</span></span></th>
<th align="left"><span data-ttu-id="a1174-122">Description</span><span class="sxs-lookup"><span data-stu-id="a1174-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a1174-123">Nom de l’image</span><span class="sxs-lookup"><span data-stu-id="a1174-123">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a1174-124">Nom de l’image compactée telle qu’elle a été définie lors de la création de l’image par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="a1174-124">The name of the packed image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a1174-125">Version</span><span class="sxs-lookup"><span data-stu-id="a1174-125">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="a1174-126">Version de l’image affichée.</span><span class="sxs-lookup"><span data-stu-id="a1174-126">The version of the displayed image.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a1174-127">Remarque</span><span class="sxs-lookup"><span data-stu-id="a1174-127">Note</span></span></strong><br/><p><span data-ttu-id="a1174-128">Toutes les versions précédentes sont conservées sauf si supprimées.</span><span class="sxs-lookup"><span data-stu-id="a1174-128">All previous versions are kept unless deleted.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a1174-129">Taille du fichier (compressé)</span><span class="sxs-lookup"><span data-stu-id="a1174-129">File Size (compressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a1174-130">Taille compressée physique de l’image.</span><span class="sxs-lookup"><span data-stu-id="a1174-130">The physical compressed size of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a1174-131">Taille de l’image (non compressée)</span><span class="sxs-lookup"><span data-stu-id="a1174-131">Image Size (uncompressed)</span></span></p></td>
<td align="left"><p><span data-ttu-id="a1174-132">Taille de l’image qui n’est pas compressée.</span><span class="sxs-lookup"><span data-stu-id="a1174-132">The physical uncompressed size of the image.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="a1174-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a1174-133">Related topics</span></span>


[<span data-ttu-id="a1174-134">Comment installer le client MED-V et la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="a1174-134">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

[<span data-ttu-id="a1174-135">Utilisation de l'interface utilisateur de la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="a1174-135">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="a1174-136">Création d'une image Virtual PC pour MED-V</span><span class="sxs-lookup"><span data-stu-id="a1174-136">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)









