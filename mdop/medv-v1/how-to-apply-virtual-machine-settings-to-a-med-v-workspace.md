---
title: Comment appliquer des paramètres de machine virtuelle à un espace de travail MED-V
description: Comment appliquer des paramètres de machine virtuelle à un espace de travail MED-V
author: dansimp
ms.assetid: b50d0dfb-8d61-4543-9607-a29bbb1ed45f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9662bb8202285d51971eeea8beaef938b98ed6b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811477"
---
# <span data-ttu-id="07cb2-103">Comment appliquer des paramètres de machine virtuelle à un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="07cb2-103">How to Apply Virtual Machine Settings to a MED-V Workspace</span></span>


<span data-ttu-id="07cb2-104">Chaque espace de travail MED-V doit être associé à une image Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="07cb2-104">Every MED-V workspace must have a Microsoft Virtual PC image associated with it.</span></span> <span data-ttu-id="07cb2-105">Les paramètres de l’ordinateur virtuel vous permettent d’affecter une image de PC virtuel et de définir d’autres propriétés d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="07cb2-105">The virtual machine settings enable you to assign a Virtual PC image as well as set other virtual machine properties.</span></span>

<span data-ttu-id="07cb2-106">Tous les paramètres d’ordinateur virtuel sont configurés dans le module de **stratégie** sous l’onglet Paramètres de l' **ordinateur virtuel** .</span><span class="sxs-lookup"><span data-stu-id="07cb2-106">All virtual machine settings are configured in the **Policy** module, on the **Virtual Machine Settings** tab.</span></span>

**<span data-ttu-id="07cb2-107">Pour appliquer les paramètres d’ordinateur virtuel à un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="07cb2-107">To apply virtual machine settings to a MED-V workspace</span></span>**

1.  <span data-ttu-id="07cb2-108">Cliquez sur l’espace de travail MED-V à configurer.</span><span class="sxs-lookup"><span data-stu-id="07cb2-108">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="07cb2-109">Configurez les propriétés de l’ordinateur virtuel comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="07cb2-109">Configure the virtual machine properties as described in the following table.</span></span>

3.  <span data-ttu-id="07cb2-110">Dans le menu **stratégie** , cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="07cb2-110">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="07cb2-111">Propriétés de la machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="07cb2-111">Virtual Machine Properties</span></span>**

<span data-ttu-id="07cb2-112">Description de la propriété-paramètres de l' *ordinateur virtuel*</span><span class="sxs-lookup"><span data-stu-id="07cb2-112">Property Description *Virtual Machine Settings*</span></span>

<span data-ttu-id="07cb2-113">Image affectée</span><span class="sxs-lookup"><span data-stu-id="07cb2-113">Assigned Image</span></span>

<span data-ttu-id="07cb2-114">Image de l’ordinateur virtuel Microsoft réel affectée à l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="07cb2-114">The actual Microsoft Virtual PC image assigned to the MED-V workspace.</span></span> <span data-ttu-id="07cb2-115">Le menu fournit une liste de toutes les images Virtual PC disponibles.</span><span class="sxs-lookup"><span data-stu-id="07cb2-115">The menu provides a list of all available Virtual PC images.</span></span> <span data-ttu-id="07cb2-116">Les types d’image suivants se trouvent dans la liste des images **actives** :</span><span class="sxs-lookup"><span data-stu-id="07cb2-116">The following image types are in the **Active** image list:</span></span>

-   <span data-ttu-id="07cb2-117">**Images de test locales**: images de l’ordinateur local qui ne sont pas encore empaquetées.</span><span class="sxs-lookup"><span data-stu-id="07cb2-117">**Local test images**—Images on the local computer that are not yet packed.</span></span> <span data-ttu-id="07cb2-118">Ces noms d’image sont suivis du mot «test» entre parenthèses (test) et sont uniquement à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="07cb2-118">These image names are followed by the word “test” in parentheses (test) and are for testing purposes only.</span></span>

-   <span data-ttu-id="07cb2-119">**Images compactées locales**: images empaquetées sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="07cb2-119">**Local packed images**—Packed images on the local computer.</span></span> <span data-ttu-id="07cb2-120">Ces images sont suivies du mot «local» entre parenthèses (locales) et ne peuvent pas être téléchargées par les clients tant que l’administrateur ne les a pas chargées sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="07cb2-120">These images are followed by the word “local” in parentheses (local) and cannot be downloaded by clients until the administrator uploads them to the server.</span></span>

    <span data-ttu-id="07cb2-121">Une image locale peut être sélectionnée si vous créez un package qui sera distribué au client par le biais d’un support amovible (par exemple, USB ou DVD).</span><span class="sxs-lookup"><span data-stu-id="07cb2-121">A local image can be selected if you are creating a package that will be distributed to the client via removable media (such as USB or DVD).</span></span>

-   <span data-ttu-id="07cb2-122">**Images compactées sur le serveur**: les images qui se trouvent sur le serveur et peuvent être téléchargées par les clients.</span><span class="sxs-lookup"><span data-stu-id="07cb2-122">**Packed images on server**—Images that are on the server and are available for download by clients.</span></span> <span data-ttu-id="07cb2-123">Cliquez sur Actualiser pour actualiser la liste des images.</span><span class="sxs-lookup"><span data-stu-id="07cb2-123">Click Refresh to refresh the images list.</span></span>

    <span data-ttu-id="07cb2-124">**Remarques**  Chaque image d’espace de travail MED-V ne peut être utilisée que par un seul utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="07cb2-124">**Note** Each MED-V workspace image can only be used by one Windows user.</span></span>

     

<span data-ttu-id="07cb2-125">Espace de travail permanent</span><span class="sxs-lookup"><span data-stu-id="07cb2-125">Workspace is persistent</span></span>

<span data-ttu-id="07cb2-126">Activez cette case à cocher pour configurer l’espace de travail MED-V comme permanent.</span><span class="sxs-lookup"><span data-stu-id="07cb2-126">Select this check box to configure the MED-V workspace as persistent.</span></span> <span data-ttu-id="07cb2-127">Dans un espace de travail MED-V permanent, lorsque l’espace de travail MED-V est arrêté, les modifications et les ajouts apportées à l’espace de travail MED-V sont enregistrés dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="07cb2-127">In a persistent MED-V workspace, when the MED-V workspace is stopped, changes and additions to the MED-V workspace are saved in the MED-V workspace.</span></span>

<span data-ttu-id="07cb2-128">Pour un espace de travail de domaine MED-V, cette option doit être sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="07cb2-128">For a Domain MED-V workspace, this option must be selected.</span></span>

<span data-ttu-id="07cb2-129">**Remarques**  Ce paramètre ne doit pas être modifié après le déploiement d’un espace de travail MED-V pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="07cb2-129">**Note** This setting should not be changed after a MED-V workspace is deployed to users.</span></span>

 

<span data-ttu-id="07cb2-130">Arrêter l’ordinateur virtuel lors de l’arrêt de l’espace de travail</span><span class="sxs-lookup"><span data-stu-id="07cb2-130">Shut down the VM when stopping the Workspace</span></span>

<span data-ttu-id="07cb2-131">Activez cette case à cocher pour éteindre l’ordinateur virtuel lors de l’arrêt de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="07cb2-131">Select this check box to shut down the virtual machine when stopping the MED-V workspace.</span></span> <span data-ttu-id="07cb2-132">Si cette case à cocher est désactivée, à l’achèvement de chaque session, la machine virtuelle n’est pas arrêtée, mais prend une photo de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="07cb2-132">If this check box is cleared, at the completion of each session, the virtual machine is not shut down but instead takes a snapshot of the virtual machine.</span></span> <span data-ttu-id="07cb2-133">Lors de l’initiation d’une nouvelle session, Windows démarre à partir de la capture d’une capture d’image (c’est-à-dire que Windows ne redémarre pas et qu’aucune connexion n’est requise).</span><span class="sxs-lookup"><span data-stu-id="07cb2-133">Upon the initiation of a new session, Windows starts from the snapshot (that is, Windows does not restart and no login is required).</span></span>

<span data-ttu-id="07cb2-134">**Remarques**  Cette propriété est activée uniquement si l’option **espace de travail est permanente** .</span><span class="sxs-lookup"><span data-stu-id="07cb2-134">**Note** This property is enabled only if **Workspace is persistent** is selected.</span></span>

 

<span data-ttu-id="07cb2-135">Connexion à Windows dans la VM à l’aide d’informations d’identification MED-V (SSO)</span><span class="sxs-lookup"><span data-stu-id="07cb2-135">Logon to Windows in VM using MED-V credentials (SSO)</span></span>

<span data-ttu-id="07cb2-136">Activez cette case à cocher pour vous connecter à Windows sur l’ordinateur virtuel en utilisant les informations d’identification MED-V entrées lors de la connexion au client MED-V.</span><span class="sxs-lookup"><span data-stu-id="07cb2-136">Select this check box to log in to Windows on the virtual machine by using the MED-V credentials entered when logging in to MED-V client.</span></span>

<span data-ttu-id="07cb2-137">**Remarques**  Cette propriété est uniquement activée lorsque l’option **espace de travail est permanente** .</span><span class="sxs-lookup"><span data-stu-id="07cb2-137">**Note** This property is enabled only when **Workspace is persistent** is selected.</span></span>

 

<span data-ttu-id="07cb2-138">L’espace de travail est revertible</span><span class="sxs-lookup"><span data-stu-id="07cb2-138">Workspace is revertible</span></span>

<span data-ttu-id="07cb2-139">Activez cette case à cocher pour configurer l’espace de travail MED-V en tant que revertible.</span><span class="sxs-lookup"><span data-stu-id="07cb2-139">Select this check box to configure the MED-V workspace as revertible.</span></span> <span data-ttu-id="07cb2-140">Dans un espace de travail MED-V de revertible, à l’achèvement de chaque session (autrement dit, lorsque l’utilisateur arrête l’espace de travail MED-V), l’espace de travail MED-V retrouve son état d’origine au cours du déploiement.</span><span class="sxs-lookup"><span data-stu-id="07cb2-140">In a revertible MED-V workspace, at the completion of each session (that is, when the user stops the MED-V workspace), the MED-V workspace reverts to the original state it was in during deployment.</span></span> <span data-ttu-id="07cb2-141">Aucune modification ou aucun complément n’est enregistré dans l’espace de travail MED-V entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="07cb2-141">No changes or additions that the user made are saved on the MED-V workspace between sessions.</span></span>

<span data-ttu-id="07cb2-142">**Remarques**  Ce paramètre ne doit pas être modifié après le déploiement d’un espace de travail MED-V pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="07cb2-142">**Note** This setting should not be changed after a MED-V workspace is deployed to users.</span></span>

 

<span data-ttu-id="07cb2-143">Synchroniser le fuseau horaire de l’espace de travail avec un hôte</span><span class="sxs-lookup"><span data-stu-id="07cb2-143">Synchronize Workspace time zone with host</span></span>

<span data-ttu-id="07cb2-144">Activez cette case à cocher pour synchroniser le fuseau horaire dans l’espace de travail MED-V avec l’hôte.</span><span class="sxs-lookup"><span data-stu-id="07cb2-144">Select this check box to synchronize the time zone in the MED-V workspace with the host.</span></span>

<span data-ttu-id="07cb2-145">La synchronisation fonctionne différemment selon que l’espace de travail MED-V est persistant ou revertible, comme suit:</span><span class="sxs-lookup"><span data-stu-id="07cb2-145">The synchronization works differently depending on whether the MED-V workspace is persistent or revertible, as follows:</span></span>

-   <span data-ttu-id="07cb2-146">Dans un espace de travail MED-V permanent, le fuseau horaire tente d’abord de se synchroniser avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="07cb2-146">In a persistent MED-V workspace, the time zone first tries to synchronize with the server.</span></span> <span data-ttu-id="07cb2-147">En cas d’échec, il se synchronise avec l’hôte.</span><span class="sxs-lookup"><span data-stu-id="07cb2-147">If that fails, it synchronizes with the host.</span></span>

-   <span data-ttu-id="07cb2-148">Dans un espace de travail MED-V revertible, le fuseau horaire est synchronisé avec l’hôte.</span><span class="sxs-lookup"><span data-stu-id="07cb2-148">In a revertible MED-V workspace, the time zone synchronizes with the host.</span></span>

*<span data-ttu-id="07cb2-149">Paramètres de verrouillage</span><span class="sxs-lookup"><span data-stu-id="07cb2-149">Lock Settings</span></span>*

<span data-ttu-id="07cb2-150">Verrouiller l’espace de travail sur l’hôte de secours/veille prolongée</span><span class="sxs-lookup"><span data-stu-id="07cb2-150">Lock the Workspace on host standby/hibernate event</span></span>

<span data-ttu-id="07cb2-151">Activez cette case à cocher pour verrouiller automatiquement l’espace de travail MED-V lorsque l’ordinateur hôte passe en mode veille ou mise en veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="07cb2-151">Select this check box to automatically lock the MED-V workspace when the host computer goes into standby or hibernate.</span></span>

<span data-ttu-id="07cb2-152">Verrouiller l’espace de travail après</span><span class="sxs-lookup"><span data-stu-id="07cb2-152">Lock the Workspace after</span></span>

<span data-ttu-id="07cb2-153">Activez cette case à cocher pour verrouiller l’espace de travail MED-V lorsque l’espace de travail MED-V est inactif pendant une durée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="07cb2-153">Select this check box to lock the MED-V workspace when the MED-V workspace is idle for a specified period of time.</span></span> <span data-ttu-id="07cb2-154">Lorsque cette case est cochée, la case numérique est activée.</span><span class="sxs-lookup"><span data-stu-id="07cb2-154">When selected, the number box is enabled.</span></span> <span data-ttu-id="07cb2-155">Entrez le nombre de minutes d’inactivité avant de verrouiller l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="07cb2-155">Enter the number of minutes of idle time before locking the MED-V workspace.</span></span>

<span data-ttu-id="07cb2-156">**Remarques**  Le temps d’inactivité fait référence aux applications d’espace de travail MED-V (pas aux applications hôtes).</span><span class="sxs-lookup"><span data-stu-id="07cb2-156">**Note** The idle time refers to the MED-V workspace applications (not the host applications).</span></span>

 

*<span data-ttu-id="07cb2-157">Paramètres de mise à jour d’image</span><span class="sxs-lookup"><span data-stu-id="07cb2-157">Image Update Settings</span></span>*

<span data-ttu-id="07cb2-158">Conserver seulement</span><span class="sxs-lookup"><span data-stu-id="07cb2-158">Keep only</span></span>

<span data-ttu-id="07cb2-159">Activez cette case à cocher pour limiter le nombre de versions d’anciennes images à conserver.</span><span class="sxs-lookup"><span data-stu-id="07cb2-159">Select this check box to limit the number of old image versions to keep.</span></span>

<span data-ttu-id="07cb2-160">Lorsque cette case est cochée, la case numérique est activée.</span><span class="sxs-lookup"><span data-stu-id="07cb2-160">When selected, the number box is enabled.</span></span> <span data-ttu-id="07cb2-161">Entrez le nombre d’anciennes versions à conserver.</span><span class="sxs-lookup"><span data-stu-id="07cb2-161">Enter the number of old versions to keep.</span></span>

<span data-ttu-id="07cb2-162">Suggérer une mise à jour lorsqu’une nouvelle version est disponible</span><span class="sxs-lookup"><span data-stu-id="07cb2-162">Suggest update when a new version is available</span></span>

<span data-ttu-id="07cb2-163">Activez cette case à cocher pour suggérer (mais pas forcée) une mise à jour lorsqu’une nouvelle version de l’image est disponible.</span><span class="sxs-lookup"><span data-stu-id="07cb2-163">Select this check box to suggest (but not force) an update when a new version of the image is available.</span></span>

<span data-ttu-id="07cb2-164">Les clients doivent utiliser le transfert de découpage lors du téléchargement d’images pour cet espace de travail</span><span class="sxs-lookup"><span data-stu-id="07cb2-164">Clients should use Trim Transfer when downloading images for this Workspace</span></span>

<span data-ttu-id="07cb2-165">Activez cette case à cocher pour activer le transfert de découpage (pour plus d’informations, reportez-vous à la section [technologie de transfert de coupure med-v](med-v-trim-transfer-technology-medvv2.md)) lors du téléchargement d’images associées à cet espace de travail MED-v</span><span class="sxs-lookup"><span data-stu-id="07cb2-165">Select this check box to enable Trim Transfer (for more information, see [MED-V Trim Transfer Technology](med-v-trim-transfer-technology-medvv2.md)) when downloading images associated with this MED-V workspace.</span></span> <span data-ttu-id="07cb2-166">Si cette case à cocher est désactivée, l’image complète est téléchargée.</span><span class="sxs-lookup"><span data-stu-id="07cb2-166">If this check box is cleared, the full image will be downloaded.</span></span>

<span data-ttu-id="07cb2-167">**Remarques**  Le transfert de découpage nécessite l’indexation du disque dur, ce qui peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="07cb2-167">**Note** Trim Transfer requires indexing the hard drive, which might take a considerable amount of time.</span></span> <span data-ttu-id="07cb2-168">Il est recommandé d’utiliser le transfert de découpage lors de l’indexation du disque dur pour plus d’efficacité que le téléchargement de la nouvelle version d’image, par exemple lors du téléchargement d’une version d’image similaire à la version existante.</span><span class="sxs-lookup"><span data-stu-id="07cb2-168">It is recommended to use Trim Transfer when indexing the hard drive is more efficient than downloading the new image version, such as when downloading an image version that is similar to the existing version.</span></span>

 

 

## <span data-ttu-id="07cb2-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="07cb2-169">Related topics</span></span>


[<span data-ttu-id="07cb2-170">Création d'une image MED-V</span><span class="sxs-lookup"><span data-stu-id="07cb2-170">Creating a MED-V Image</span></span>](creating-a-med-v-image.md)

[<span data-ttu-id="07cb2-171">Utilisation de l'interface utilisateur de la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="07cb2-171">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="07cb2-172">Création d'un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="07cb2-172">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





