---
title: Comment créer et tester une image MED-V
description: Comment créer et tester une image MED-V
author: dansimp
ms.assetid: 40e4aba6-12cb-4794-967d-2c09dc20d808
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f7989871a695b09c987124ab02c0143082148f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812119"
---
# <span data-ttu-id="95073-103">Comment créer et tester une image MED-V</span><span class="sxs-lookup"><span data-stu-id="95073-103">How to Create and Test a MED-V Image</span></span>


<span data-ttu-id="95073-104">L’administrateur MED-V crée une image MED-V pour qu’elle puisse être chargée, associée à un espace de travail MED-v, puis distribuée au client via le Web, ajoutée à un package MED-V, ou téléchargée sur le client par le biais d’un système tiers.</span><span class="sxs-lookup"><span data-stu-id="95073-104">The MED-V administrator creates a MED-V image so that it can be uploaded, associated with a MED-V workspace, and then distributed to the client over the Web, added to a MED-V package, or downloaded to the client by using a third-party system.</span></span> <span data-ttu-id="95073-105">Il est recommandé de commencer par créer une image de test et de la tester sur un client MED-V avant de la déployer.</span><span class="sxs-lookup"><span data-stu-id="95073-105">It is recommended to first create a test image and test it on MED-V client before deploying it.</span></span>

<span data-ttu-id="95073-106">Lors de la création d’une image MED-V, il passe par les étapes suivantes:</span><span class="sxs-lookup"><span data-stu-id="95073-106">When creating a MED-V image, it goes through the following stages:</span></span>

1.  <span data-ttu-id="95073-107">**Image de test locale**: image de base qui peut être testée localement.</span><span class="sxs-lookup"><span data-stu-id="95073-107">**Local test image**—A basic image that can be tested locally.</span></span>

2.  <span data-ttu-id="95073-108">**Image empaquetée locale**: après test de l’image, l’image est empaquetée tel qu’il existait avant le test.</span><span class="sxs-lookup"><span data-stu-id="95073-108">**Local packed image**—After the image is tested, the image is packed as it existed prior to testing.</span></span> <span data-ttu-id="95073-109">Aucune modification n’est apportée pendant le test n’est incluse dans l’image empaquetée.</span><span class="sxs-lookup"><span data-stu-id="95073-109">No changes made during testing are included in the packed image.</span></span>

3.  <span data-ttu-id="95073-110">**Image empaquetée sur le serveur**: l’image compactée est téléchargée sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="95073-110">**Packed image on server**—The packed image is uploaded to the server.</span></span>

## <span data-ttu-id="95073-111">Comment créer une image de test MED-V</span><span class="sxs-lookup"><span data-stu-id="95073-111">How to Create a MED-V Test Image</span></span>


**<span data-ttu-id="95073-112">Pour créer une nouvelle image de test MED-V</span><span class="sxs-lookup"><span data-stu-id="95073-112">To create a new MED-V test image</span></span>**

1.  <span data-ttu-id="95073-113">Cliquez sur le bouton gestion des **images** .</span><span class="sxs-lookup"><span data-stu-id="95073-113">Click the **Images** management button.</span></span>

    <span data-ttu-id="95073-114">Le module **images** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="95073-114">The **Images** module appears.</span></span>

    -   <span data-ttu-id="95073-115">Le module **images** se compose des volets suivants:</span><span class="sxs-lookup"><span data-stu-id="95073-115">The **Images** module consists of the following panes:</span></span>

        -   <span data-ttu-id="95073-116">**Images de test locales**: images de test locales.</span><span class="sxs-lookup"><span data-stu-id="95073-116">**Local Test Images**—Local unpacked images.</span></span>

        -   <span data-ttu-id="95073-117">**Images compactées locales**: toutes les images compactées sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="95073-117">**Local Packed Images**—All packed images on the local computer.</span></span>

        -   <span data-ttu-id="95073-118">**Images compactées sur le serveur**: toutes les images qui ont été empaquetées et chargées sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="95073-118">**Packed Images on Server**—All images that have been packed and uploaded to the server.</span></span>

    -   <span data-ttu-id="95073-119">Dans les **images compactées locales** et sur les volets **serveur** , la version la plus récente de chaque image est affichée en tant que nœud parent.</span><span class="sxs-lookup"><span data-stu-id="95073-119">In the **Local Packed Images** and **Packed Images on Server** panes, the most recent version of each image is displayed as the parent node.</span></span> <span data-ttu-id="95073-120">Cliquez sur le nœud parent pour afficher toutes les autres versions existantes de l’image.</span><span class="sxs-lookup"><span data-stu-id="95073-120">Click the parent node to view all other existing versions of the image.</span></span>

2.  <span data-ttu-id="95073-121">Dans le volet **images de test locales** , cliquez sur **nouveau**.</span><span class="sxs-lookup"><span data-stu-id="95073-121">In the **Local Test Images** pane, click **New**.</span></span>

3.  <span data-ttu-id="95073-122">Dans la boîte de dialogue de **création d’image de test** , sélectionnez l’image d’ordinateur virtuel que vous voulez configurer en tant qu’image de test MED-V en effectuant l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="95073-122">On the **Test Image Creation** dialog box, select the virtual machine image that you want to configure as a MED-V test image by doing one of the following:</span></span>

    -   <span data-ttu-id="95073-123">Dans le champ fichier **image de base** , tapez le chemin d’accès complet au répertoire dans lequel se trouve l’image Microsoft Virtual PC préparée pour MED-V.</span><span class="sxs-lookup"><span data-stu-id="95073-123">In the **Base image** file field, type the full path to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

    -   <span data-ttu-id="95073-124">Cliquez sur **Parcourir** pour accéder au répertoire dans lequel se trouve l’image Microsoft Virtual PC préparée pour MED-V.</span><span class="sxs-lookup"><span data-stu-id="95073-124">Click **Browse** to browse to the directory where the Microsoft Virtual PC image prepared for MED-V is located.</span></span>

4.  <span data-ttu-id="95073-125">Dans le champ nom de l' **image** , tapez ou sélectionnez le nom souhaité.</span><span class="sxs-lookup"><span data-stu-id="95073-125">In the **Image name** field, type or select the desired name.</span></span>

    <span data-ttu-id="95073-126">**Remarques**  Les caractères suivants ne peuvent pas être inclus dans le nom de l’image: Space " &lt; &gt; | \\ / : \* ?</span><span class="sxs-lookup"><span data-stu-id="95073-126">**Note** The following characters cannot be included in the image name: space " &lt; &gt; | \\ / : \* ?</span></span>

     

5.  <span data-ttu-id="95073-127">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="95073-127">Click **OK**.</span></span>

    <span data-ttu-id="95073-128">Une nouvelle image de test MED-V est créée sur votre ordinateur hôte avec les propriétés définies dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="95073-128">A new MED-V test image is created on your host computer with the properties defined in the following table.</span></span>

    <span data-ttu-id="95073-129">Pour plus d’informations sur la configuration de l’image d’espace de travail MED-V, voir [Configuration des stratégies d’espace de travail MED-v](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="95073-129">For more information about configuring the MED-V workspace image, refer to [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

**<span data-ttu-id="95073-130">Propriétés des images de test locales</span><span class="sxs-lookup"><span data-stu-id="95073-130">Local Test Images Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="95073-131">Propriété</span><span class="sxs-lookup"><span data-stu-id="95073-131">Property</span></span></th>
<th align="left"><span data-ttu-id="95073-132">Description</span><span class="sxs-lookup"><span data-stu-id="95073-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95073-133">Nom de l’image</span><span class="sxs-lookup"><span data-stu-id="95073-133">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="95073-134">Nom de l’image de test telle qu’elle a été définie lors de la création de l’image par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="95073-134">The name of the test image as it was defined when the administrator created the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95073-135">Trajectoire d’image</span><span class="sxs-lookup"><span data-stu-id="95073-135">Image Path</span></span></p></td>
<td align="left"><p><span data-ttu-id="95073-136">Path local de l’image de test.</span><span class="sxs-lookup"><span data-stu-id="95073-136">The local path of the test image.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95073-137">Générée</span><span class="sxs-lookup"><span data-stu-id="95073-137">Created</span></span></p></td>
<td align="left"><p><span data-ttu-id="95073-138">Date de création de l’image de test.</span><span class="sxs-lookup"><span data-stu-id="95073-138">The date the test image was created.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="95073-139">Test d’une image MED-V à partir du client MED-V</span><span class="sxs-lookup"><span data-stu-id="95073-139">How to Test a MED-V Image from the MED-V Client</span></span>


<span data-ttu-id="95073-140">Après avoir créé une image de test MED-V, utilisez la procédure suivante pour tester l’image localement.</span><span class="sxs-lookup"><span data-stu-id="95073-140">After a MED-V test image is created, use the following procedure to test the image locally.</span></span>

**<span data-ttu-id="95073-141">Pour tester une image MED-V</span><span class="sxs-lookup"><span data-stu-id="95073-141">To test a MED-V image</span></span>**

1.  <span data-ttu-id="95073-142">Cliquez sur le bouton de gestion des **stratégies** .</span><span class="sxs-lookup"><span data-stu-id="95073-142">Click the **Policy** management button.</span></span>

2.  <span data-ttu-id="95073-143">Dans le module **stratégie** , affectez l’image de test med-v à un espace de travail MED-v en procédant comme suit:</span><span class="sxs-lookup"><span data-stu-id="95073-143">In the **Policy** module, assign the MED-V test image to a MED-V workspace by doing the following:</span></span>

    1.  <span data-ttu-id="95073-144">Cliquez sur l’onglet **machine virtuelle** .</span><span class="sxs-lookup"><span data-stu-id="95073-144">Click the **Virtual Machine** tab.</span></span>

    2.  <span data-ttu-id="95073-145">Dans le champ **image affectée** , sélectionnez l’image de test MED-V que vous avez créée.</span><span class="sxs-lookup"><span data-stu-id="95073-145">In the **Assigned Image** field, select the MED-V test image you created.</span></span> <span data-ttu-id="95073-146">Si votre image de test ne figure pas dans la liste, cliquez sur **Actualiser**.</span><span class="sxs-lookup"><span data-stu-id="95073-146">If your test image is not in the list, click **Refresh**.</span></span>

    3.  <span data-ttu-id="95073-147">Dans la barre d’outils, cliquez sur **enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="95073-147">On the toolbar, click **Save changes**.</span></span>

3.  <span data-ttu-id="95073-148">Configurez les autres paramètres d’espace de travail MED-V à tester.</span><span class="sxs-lookup"><span data-stu-id="95073-148">Configure any other MED-V workspace settings to be tested.</span></span> <span data-ttu-id="95073-149">Pour plus d’informations, reportez-vous à [Configuration des stratégies d’espace de travail MED-V](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="95073-149">For more information, see [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

4.  <span data-ttu-id="95073-150">Démarrez le client MED-V.</span><span class="sxs-lookup"><span data-stu-id="95073-150">Start MED-V client.</span></span>

5.  <span data-ttu-id="95073-151">Dans la boîte de confirmation **confirmer l’exécution du test** , cliquez sur utiliser l’image de **test**.</span><span class="sxs-lookup"><span data-stu-id="95073-151">In the **Confirm Running Test** confirmation box, click **Use Test Image**.</span></span>

6.  <span data-ttu-id="95073-152">Testez l’image de test de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="95073-152">Test the MED-V workspace test image.</span></span>

    <span data-ttu-id="95073-153">Pour plus d’informations sur le démarrage et l’exécution du client MED-V, voir [opérations du client med-v](med-v-client-operations.md).</span><span class="sxs-lookup"><span data-stu-id="95073-153">For information about starting and running MED-V client, see [MED-V Client Operations](med-v-client-operations.md).</span></span>

<span data-ttu-id="95073-154">**Remarques**  Lorsque vous testez une image, n’ouvrez pas VPC et apportez les modifications à l’image.</span><span class="sxs-lookup"><span data-stu-id="95073-154">**Note** While testing an image, do not open VPC and make changes to the image.</span></span>

 

<span data-ttu-id="95073-155">**Remarques**  Lorsque vous testez une image, aucune modification n’est enregistrée dans l’image entre les sessions; ils sont enregistrés dans un fichier temporaire distinct.</span><span class="sxs-lookup"><span data-stu-id="95073-155">**Note** When testing an image, no changes are saved to the image between sessions; instead, they are saved in a separate, temporary file.</span></span> <span data-ttu-id="95073-156">Cela permet de s’assurer que lorsque l’image est empaquetée et exécutée sur l’environnement de production, il s’agit de l’image originale et claire.</span><span class="sxs-lookup"><span data-stu-id="95073-156">This is to ensure that when the image is packed and run on the production environment, it is the original, clean image.</span></span>

 

## <span data-ttu-id="95073-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95073-157">Related topics</span></span>


[<span data-ttu-id="95073-158">Création d'une image Virtual PC pour MED-V</span><span class="sxs-lookup"><span data-stu-id="95073-158">Creating a Virtual PC Image for MED-V</span></span>](creating-a-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="95073-159">Création d'un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="95073-159">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="95073-160">Configuration de stratégies d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="95073-160">Configuring MED-V Workspace Policies</span></span>](configuring-med-v-workspace-policies.md)

[<span data-ttu-id="95073-161">Opérations du client MED-V</span><span class="sxs-lookup"><span data-stu-id="95073-161">MED-V Client Operations</span></span>](med-v-client-operations.md)

 

 





