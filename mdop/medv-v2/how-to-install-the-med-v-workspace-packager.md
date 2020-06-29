---
title: Comment installer le Gestionnaire de package de l'espace de travail MED-V
description: Comment installer le Gestionnaire de package de l'espace de travail MED-V
author: dansimp
ms.assetid: 627478e9-6798-4b32-9a50-7a1b72bea295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e23492852813752f028ae2201e656162d6189642
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810800"
---
# <span data-ttu-id="5662c-103">Comment installer le Gestionnaire de package de l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="5662c-103">How to Install the MED-V Workspace Packager</span></span>


<span data-ttu-id="5662c-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 inclut un **package d’espace de travail MED-v**, que l’administrateur de bureau utilise pour créer les packages de déploiement d’espace de travail MED-v qui sont distribués aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="5662c-104">Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 includes a **MED-V Workspace Packager**, which the desktop administrator uses to create the MED-V workspace deployment packages that are distributed to the end users.</span></span> <span data-ttu-id="5662c-105">Le gestionnaire de package fournit des instructions détaillées sur la création d’espaces de travail MED-V et contient des assistants utiles pour le processus.</span><span class="sxs-lookup"><span data-stu-id="5662c-105">The packager provides step-by-step guidance on how to create MED-V workspaces and contains wizards that help in the process.</span></span>

<span data-ttu-id="5662c-106">**Important**  Avant de commencer à exécuter les assistants, assurez-vous qu’un VHD préparé est prêt à être installé.</span><span class="sxs-lookup"><span data-stu-id="5662c-106">**Important** Before you start to run the wizards, make sure that you have a prepared VHD ready to install.</span></span> <span data-ttu-id="5662c-107">Pour plus d’informations, voir [préparer une image MED-V](prepare-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="5662c-107">For more information, see [Prepare a MED-V Image](prepare-a-med-v-image.md).</span></span>

 

<span data-ttu-id="5662c-108">Cette section fournit des instructions pas à pas pour l’installation ou la réparation de l’outil de création de **package de l’espace de travail MED-V**.</span><span class="sxs-lookup"><span data-stu-id="5662c-108">This section provides step-by-step instructions for installing or repairing the **MED-V Workspace Packager**.</span></span>

**<span data-ttu-id="5662c-109">Pour installer le module de création de package de l’espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="5662c-109">To install the MED-V Workspace Packager</span></span>**

1.  <span data-ttu-id="5662c-110">Recherchez les fichiers d’installation de MED-V que vous avez reçus dans le cadre de votre téléchargement de logiciels.</span><span class="sxs-lookup"><span data-stu-id="5662c-110">Locate the MED-V installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="5662c-111">Double-cliquez sur le fichier d’installation MED-V \ _WorkspacePackager \ _Setup.</span><span class="sxs-lookup"><span data-stu-id="5662c-111">Double-click the MED-V\_WorkspacePackager\_Setup installation file.</span></span>

    <span data-ttu-id="5662c-112">L’Assistant **de configuration de l’espace de travail Microsoft Enterprise Desktop Virtualization (MED-V)** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="5662c-112">The **Microsoft Enterprise Desktop Virtualization (MED-V) Workspace Packager Setup** wizard opens.</span></span> <span data-ttu-id="5662c-113">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="5662c-113">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="5662c-114">Acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="5662c-114">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="5662c-115">Sélectionnez le dossier de destination pour l’installation de l’application de création de package de l’espace de travail MED-V, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="5662c-115">Select the destination folder for installing the MED-V Workspace Packager, and then click **Next**.</span></span>

5.  <span data-ttu-id="5662c-116">Pour commencer l’installation, cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="5662c-116">To begin the installation, click **Install**.</span></span>

6.  <span data-ttu-id="5662c-117">Une fois l’installation terminée, cliquez sur **Terminer** pour fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="5662c-117">After the installation is completed successfully, click **Finish** to close the wizard.</span></span>

    <span data-ttu-id="5662c-118">Pour vérifier que l’installation du package est réussie, cliquez sur **Démarrer**, sur **tous les programmes**, sur **virtualisation de bureau Microsoft entreprise**, puis sur **module de création de package de l’espace de travail MED-V.**</span><span class="sxs-lookup"><span data-stu-id="5662c-118">To verify that the installation of the packager was successful, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager.**</span></span>

    <span data-ttu-id="5662c-119">Pour plus d’informations sur l’utilisation du **Gestionnaire de package med-v**, voir [créer un package d’espace de travail MED-v](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="5662c-119">For information about how to use the **MED-V Workspace Packager**, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="5662c-120">Si le gestionnaire de package ne s’ouvre pas comme prévu, vous pouvez essayer de réparer l’installation.</span><span class="sxs-lookup"><span data-stu-id="5662c-120">If the packager does not open as expected, you can try to repair the installation.</span></span>

**<span data-ttu-id="5662c-121">Pour réparer l’installation de l’outil de création de package de l’espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="5662c-121">To repair the MED-V Workspace Packager installation</span></span>**

1.  <span data-ttu-id="5662c-122">Double-cliquez sur le fichier d’installation MED-V \ _WorkspacePackager \ _Setup.</span><span class="sxs-lookup"><span data-stu-id="5662c-122">Double-click the MED-V\_WorkspacePackager\_Setup installation file.</span></span>

    <span data-ttu-id="5662c-123">L’Assistant **de configuration de l’espace de travail Microsoft Enterprise Desktop Virtualization (MED-V)** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="5662c-123">The **Microsoft Enterprise Desktop Virtualization (MED-V) Workspace Packager Setup** wizard opens.</span></span> <span data-ttu-id="5662c-124">Cliquez sur **Suivant** pour poursuivre.</span><span class="sxs-lookup"><span data-stu-id="5662c-124">Click **Next** to continue.</span></span>

2.  <span data-ttu-id="5662c-125">Pour réparer les erreurs susceptibles de se produire lors de l’installation, cliquez sur **réparer**.</span><span class="sxs-lookup"><span data-stu-id="5662c-125">To repair errors that might have occurred in the installation, click **Repair**.</span></span>

3.  <span data-ttu-id="5662c-126">Pour démarrer le processus de réparation, cliquez de nouveau sur **réparer** .</span><span class="sxs-lookup"><span data-stu-id="5662c-126">To begin the repair process, click **Repair** again.</span></span>

4.  <span data-ttu-id="5662c-127">Une fois la réparation terminée, cliquez sur **Terminer** pour fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="5662c-127">After the repair is completed successfully, click **Finish** to close the wizard.</span></span>

    <span data-ttu-id="5662c-128">Pour vérifier que la réparation du package a réussi, cliquez sur **Démarrer**, sur **tous les programmes**, sur **virtualisation de bureau Microsoft entreprise**, puis sur **module de création de package de l’espace de travail MED-V.**</span><span class="sxs-lookup"><span data-stu-id="5662c-128">To verify that the repair of the packager was successful, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager.**</span></span>

## <span data-ttu-id="5662c-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5662c-129">Related topics</span></span>


[<span data-ttu-id="5662c-130">Comment installer l'agent hôte MED-V manuellement</span><span class="sxs-lookup"><span data-stu-id="5662c-130">How to Manually Install the MED-V Host Agent</span></span>](how-to-manually-install-the-med-v-host-agent.md)

[<span data-ttu-id="5662c-131">Comment désinstaller les composants de MED-V</span><span class="sxs-lookup"><span data-stu-id="5662c-131">How to Uninstall the MED-V Components</span></span>](how-to-uninstall-the-med-v-components.md)

 

 





