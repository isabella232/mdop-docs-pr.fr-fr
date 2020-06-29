---
title: Compactage des disques durs virtuels MED-V
description: Compactage des disques durs virtuels MED-V
author: dansimp
ms.assetid: 5e6122d1-9847-4b33-adab-594919eec3c5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f71aefb1e4e901078b4d0a421065b7bd5acdf0ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809858"
---
# <span data-ttu-id="72f88-103">Compactage des disques durs virtuels MED-V</span><span class="sxs-lookup"><span data-stu-id="72f88-103">Compacting the MED-V Virtual Hard Disk</span></span>


<span data-ttu-id="72f88-104">Même s’il est facultatif, vous pouvez compacter le disque dur virtuel (VHD) pour récupérer l’espace libre sur le disque et réduire la taille du VHD avant de configurer l’image du PC virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="72f88-104">Although it is optional, you can compact the virtual hard disk (VHD) to reclaim empty disk space and reduce the size of the VHD before you configure the Windows Virtual PC image.</span></span>

<span data-ttu-id="72f88-105">**Important**  Avant de continuer, créez une copie de sauvegarde de votre image Windows XP.</span><span class="sxs-lookup"><span data-stu-id="72f88-105">**Important** Before you proceed, create a backup copy of your Windows XP image.</span></span>

 

**<span data-ttu-id="72f88-106">Préparation du disque dur virtuel</span><span class="sxs-lookup"><span data-stu-id="72f88-106">Preparing the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="72f88-107">Ouvrez votre image Windows XP.</span><span class="sxs-lookup"><span data-stu-id="72f88-107">Open your Windows XP image.</span></span>

    <span data-ttu-id="72f88-108">Cliquez sur **Démarrer**, sur **tous les programmes**, sur **PC virtuel Windows**, sur **PC virtuel Windows**, puis double-cliquez sur votre image Windows XP.</span><span class="sxs-lookup"><span data-stu-id="72f88-108">Click **Start**, click **All Programs**, click **Windows Virtual PC**, click **Windows Virtual PC**, then double-click your Windows XP image.</span></span>

2.  <span data-ttu-id="72f88-109">Effacez le cache DLL.</span><span class="sxs-lookup"><span data-stu-id="72f88-109">Clear the DLL cache.</span></span>

    1.  <span data-ttu-id="72f88-110">À l’invite de commandes dans l’ordinateur virtuel, tapez **SFC/CacheSize = 1**.</span><span class="sxs-lookup"><span data-stu-id="72f88-110">At a command prompt in the virtual machine, type **sfc /cachesize=1**.</span></span>

    2.  <span data-ttu-id="72f88-111">Redémarrez l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="72f88-111">Restart the virtual machine.</span></span>

    3.  <span data-ttu-id="72f88-112">À l’invite de commandes dans l’ordinateur virtuel, tapez **sfc/purgecache**.</span><span class="sxs-lookup"><span data-stu-id="72f88-112">At a command prompt in the virtual machine, type **sfc /purgecache**.</span></span>

3.  <span data-ttu-id="72f88-113">Supprimez les fichiers inutiles, tels que les programmes de désinstallation, les fichiers temporaires, les fichiers journaux, les fichiers de page, les dossiers partagés, etc.</span><span class="sxs-lookup"><span data-stu-id="72f88-113">Delete unnecessary files, such as uninstallers, temp files, log files, page files, shared folders, and so on.</span></span>

4.  <span data-ttu-id="72f88-114">Désactiver la restauration du système.</span><span class="sxs-lookup"><span data-stu-id="72f88-114">Turn off System Restore.</span></span> <span data-ttu-id="72f88-115">Vous pouvez également spécifier cette étape dans votre fichier Sysprep. inf.</span><span class="sxs-lookup"><span data-stu-id="72f88-115">You can also specify this step in your Sysprep.inf file.</span></span>

    1.  <span data-ttu-id="72f88-116">Dans le **panneau**de configuration, double-cliquez sur **système**, puis sélectionnez l’onglet **restauration du système** .</span><span class="sxs-lookup"><span data-stu-id="72f88-116">In **Control Panel**, double-click **System**, and then select the **System Restore** tab.</span></span>

    2.  <span data-ttu-id="72f88-117">Sélectionnez **désactiver la restauration du système**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="72f88-117">Select **Turn off System Restore**, and then click **OK**.</span></span>

5.  <span data-ttu-id="72f88-118">Définissez les tailles maximales du journal des événements et effacez tous les événements.</span><span class="sxs-lookup"><span data-stu-id="72f88-118">Set maximum event log sizes and clear all events.</span></span>

    1.  <span data-ttu-id="72f88-119">Ouvrez l’observateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="72f88-119">Open the event viewer.</span></span>

        <span data-ttu-id="72f88-120">Cliquez sur **Démarrer**, sur **panneau de configuration**, double-cliquez sur **Outils d’administration**, puis double-cliquez sur **Observateur d’événements**.</span><span class="sxs-lookup"><span data-stu-id="72f88-120">Click **Start**, click **Control Panel**, double-click **Administrative Tools**, then double-click **Event Viewer**.</span></span>

    2.  <span data-ttu-id="72f88-121">Cliquez avec le bouton droit sur **application**, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="72f88-121">Right-click **Application**, and click **Properties**.</span></span>

    3.  <span data-ttu-id="72f88-122">Dans la zone **taille du journal** , définissez **taille maximale du journal** sur 512 Ko, puis sélectionnez **remplacer les événements selon les besoins**.</span><span class="sxs-lookup"><span data-stu-id="72f88-122">In the **Log Size** area, set **Maximum Log Size** to 512KB and then select **Overwrite events as needed**.</span></span>

    4.  <span data-ttu-id="72f88-123">Cliquez sur **effacer le journal**.</span><span class="sxs-lookup"><span data-stu-id="72f88-123">Click **Clear Log**.</span></span> <span data-ttu-id="72f88-124">Dans la boîte de dialogue **Observateur d’événements** qui s’affiche, cliquez sur **non**.</span><span class="sxs-lookup"><span data-stu-id="72f88-124">In the **Event Viewer** dialog box that appears, click **No**.</span></span>

    5.  <span data-ttu-id="72f88-125">Dans la fenêtre **Propriétés** , cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="72f88-125">In the **Properties** window, click **OK**.</span></span>

    6.  <span data-ttu-id="72f88-126">Répétez les étapes a à e pour les journaux **système** et de **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="72f88-126">Repeat steps a through e for the **Security** and **System** logs.</span></span>

6.  <span data-ttu-id="72f88-127">Exécutez l’outil Nettoyage de disque.</span><span class="sxs-lookup"><span data-stu-id="72f88-127">Run the Disk Cleanup Tool.</span></span>

    <span data-ttu-id="72f88-128">Cliquez **sur Démarrer**, **sur tous les programmes**, sur **accessoires**, sur **Outils système**, puis sur **nettoyage de disque**.</span><span class="sxs-lookup"><span data-stu-id="72f88-128">Click **Start**, click **All Programs**, click **Accessories**, click **System Tools**, and then click **Disk Cleanup**.</span></span>

7.  <span data-ttu-id="72f88-129">Configurez votre fichier de page selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="72f88-129">Configure your page file as needed for your applications.</span></span>

    1.  <span data-ttu-id="72f88-130">Dans le **panneau de configuration**, double-cliquez sur **système**, puis sélectionnez l’onglet **avancé** .</span><span class="sxs-lookup"><span data-stu-id="72f88-130">In **Control Panel**, double-click **System**, and then select the **Advanced** tab.</span></span>

    2.  <span data-ttu-id="72f88-131">Dans la zone **performance** , cliquez sur **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="72f88-131">In the **Performance** area, click **Settings**.</span></span>

    3.  <span data-ttu-id="72f88-132">Dans la zone **mémoire virtuelle** , cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="72f88-132">In the **Virtual Memory** area, click **Change**.</span></span>

    4.  <span data-ttu-id="72f88-133">Configurez les paramètres de votre fichier page.</span><span class="sxs-lookup"><span data-stu-id="72f88-133">Configure your page file settings.</span></span>

8.  <span data-ttu-id="72f88-134">Fermez l’image Windows XP.</span><span class="sxs-lookup"><span data-stu-id="72f88-134">Shut down the Windows XP image.</span></span>

**<span data-ttu-id="72f88-135">Défragmentation et précompactage du disque dur virtuel</span><span class="sxs-lookup"><span data-stu-id="72f88-135">Defragmenting and Pre-compacting the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="72f88-136">Dans **le panneau de configuration** de l’ordinateur hôte exécutant Windows 7, cliquez sur **Outils d’administration**, double-cliquez sur gestion de l' **ordinateur**, puis cliquez sur gestion des **disques**.</span><span class="sxs-lookup"><span data-stu-id="72f88-136">In **Control Panel** on the host computer that is running Windows 7, click **Administrative Tools**, double-click **Computer Management**, then click **Disk Management**.</span></span>

2.  <span data-ttu-id="72f88-137">À l’aide de la console de gestion des disques, joignez (montez) le disque dur virtuel, puis défragmentez le disque.</span><span class="sxs-lookup"><span data-stu-id="72f88-137">By using the Disk Management Console, attach (mount) the virtual hard disk and then defragment the disk.</span></span>

3.  <span data-ttu-id="72f88-138">À l’aide d’un outil d’extraction ISO, extrayez la précompact. ISO située dans le dossier C:\\Program Files\\Windows Virtual PC\\Integration composants.</span><span class="sxs-lookup"><span data-stu-id="72f88-138">By using an ISO extraction tool, extract the precompact.iso located in the \\Program Files\\Windows Virtual PC\\Integration Components folder.</span></span>

4.  <span data-ttu-id="72f88-139">Utilisez le programme precompact.exe pour compresser le disque dur virtuel Windows XP.</span><span class="sxs-lookup"><span data-stu-id="72f88-139">Use the precompact.exe program to compress the Windows XP virtual hard disk.</span></span>

5.  <span data-ttu-id="72f88-140">À l’aide de la console de gestion des disques, détachez le disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="72f88-140">By using the Disk Management Console, detach the virtual hard disk.</span></span>

**<span data-ttu-id="72f88-141">Compression du disque dur virtuel</span><span class="sxs-lookup"><span data-stu-id="72f88-141">Compacting the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="72f88-142">Ouvrez l’ordinateur virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="72f88-142">Open Windows Virtual PC.</span></span>

    <span data-ttu-id="72f88-143">Cliquez sur **Démarrer**, sur **tous les programmes**, sur **PC virtuel Windows**, puis sur **PC virtuel Windows**.</span><span class="sxs-lookup"><span data-stu-id="72f88-143">Click **Start**, click **All Programs**, click **Windows Virtual PC**, then click **Windows Virtual PC**.</span></span>

2.  <span data-ttu-id="72f88-144">Cliquez avec le bouton droit sur votre image Windows XP, puis sélectionnez **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="72f88-144">Right-click your Windows XP image and select **Settings**.</span></span>

3.  <span data-ttu-id="72f88-145">Cliquez sur **disque dur** pour la personne qui correspond à votre image Windows XP, puis cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="72f88-145">Click **Hard Disk** for the one that corresponds to your Windows XP image, and then click **Modify**.</span></span>

4.  <span data-ttu-id="72f88-146">Cliquez sur **Compact disque dur virtuel**.</span><span class="sxs-lookup"><span data-stu-id="72f88-146">Click **Compact virtual hard disk**.</span></span>

5.  <span data-ttu-id="72f88-147">Cliquez sur **compact** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="72f88-147">Click **Compact** and then click **OK**.</span></span>

<span data-ttu-id="72f88-148">Créez une copie de sauvegarde de votre disque dur virtuel compacté.</span><span class="sxs-lookup"><span data-stu-id="72f88-148">Create a backup copy of your compacted virtual hard disk.</span></span>

## <span data-ttu-id="72f88-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="72f88-149">Related topics</span></span>


[<span data-ttu-id="72f88-150">Configuration d'une image Windows Virtual PC pour MED-V</span><span class="sxs-lookup"><span data-stu-id="72f88-150">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="72f88-151">Informations techniques de référence pour MED-V</span><span class="sxs-lookup"><span data-stu-id="72f88-151">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





