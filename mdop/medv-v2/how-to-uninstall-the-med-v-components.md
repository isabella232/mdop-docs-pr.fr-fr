---
title: Comment désinstaller les composants de MED-V
description: Comment désinstaller les composants de MED-V
author: dansimp
ms.assetid: c121dd27-6b2f-4d41-a21a-c6e8608c5c41
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 514ec8227b858b34289ca2330f7cfb038bc4f00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804669"
---
# <span data-ttu-id="91e85-103">Comment désinstaller les composants de MED-V</span><span class="sxs-lookup"><span data-stu-id="91e85-103">How to Uninstall the MED-V Components</span></span>


<span data-ttu-id="91e85-104">Dans certains cas, vous voudrez peut-être désinstaller tout ou partie des composants 2,0 de Microsoft Enterprise Desktop Virtualization (MED-V) de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="91e85-104">Under certain circumstances, you might want to uninstall all or part of the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 components from your enterprise.</span></span> <span data-ttu-id="91e85-105">Par exemple, vous avez résolu tous les problèmes de compatibilité du système d’exploitation des applications ou vous voulez déployer un autre espace de travail MED-V dans votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="91e85-105">For example, you have resolved all application operating system compatibility issues, or you want to deploy a different MED-V workspace in your enterprise.</span></span>

<span data-ttu-id="91e85-106">En règle générale, vous pouvez configurer votre système de distribution de logiciels électroniques pour désinstaller les composants MED-V à l’aide d’un programme d’installation Windows.</span><span class="sxs-lookup"><span data-stu-id="91e85-106">Typically, you can configure your electronic software distribution (ESD) system to uninstall the MED-V components by using a Windows-based Installer.</span></span> <span data-ttu-id="91e85-107">Vous pouvez également désinstaller les composants MED-V manuellement.</span><span class="sxs-lookup"><span data-stu-id="91e85-107">Alternately, you can uninstall all or some MED-V components manually.</span></span>

<span data-ttu-id="91e85-108">**Important**  Avant de désinstaller l’agent hôte MED-V, vous devez d’abord désinstaller les espaces de travail MED-V installés.</span><span class="sxs-lookup"><span data-stu-id="91e85-108">**Important** Before you can uninstall the MED-V Host Agent, you must first uninstall any installed MED-V workspace.</span></span>

 

<span data-ttu-id="91e85-109">Pour désinstaller les composants MED-V de votre entreprise, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="91e85-109">Use the following procedures to uninstall the MED-V components from your enterprise.</span></span>

**<span data-ttu-id="91e85-110">Pour désinstaller MED-V à l’aide d’un système de distribution de logiciels électronique</span><span class="sxs-lookup"><span data-stu-id="91e85-110">To uninstall MED-V using an electronic software distribution System</span></span>**

1.  <span data-ttu-id="91e85-111">Utilisez votre système ESD pour distribuer un script qui appelle le programme exécutable uninstall.exe pour chaque espace de travail MED-V que vous voulez désinstaller.</span><span class="sxs-lookup"><span data-stu-id="91e85-111">Use your ESD system to distribute a script that invokes the uninstall.exe executable program for every MED-V workspace that you want to uninstall.</span></span> <span data-ttu-id="91e85-112">Le fichier se trouve sur C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span><span class="sxs-lookup"><span data-stu-id="91e85-112">The file is located at C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span></span> <span data-ttu-id="91e85-113">Vous pouvez définir un indicateur pour exécuter le programme de désinstallation du programme exécutable en silence de sorte que les utilisateurs finaux ne connaissent pas la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="91e85-113">You can set a flag to run the uninstall executable program silently so that end users are unaware of the uninstallation.</span></span>

2.  <span data-ttu-id="91e85-114">Créer un package pour distribuer le fichier d’installation de l’agent hôte MED-V sur chaque ordinateur sur lequel un espace de travail MED-V a été désinstallé.</span><span class="sxs-lookup"><span data-stu-id="91e85-114">Create a package to distribute the MED-V Host Agent installation file to each computer on which a MED-V workspace was uninstalled.</span></span> <span data-ttu-id="91e85-115">Configurez le package pour exécuter la désinstallation en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="91e85-115">Configure the package to run the uninstallation in silent mode.</span></span>

<span data-ttu-id="91e85-116">Le client ESD reconnaît lorsque les nouveaux packages sont disponibles et commence à désinstaller les packages conformément à la définition et aux exigences.</span><span class="sxs-lookup"><span data-stu-id="91e85-116">The ESD client recognizes when the new packages are available and starts to uninstall the packages per the definition and requirements.</span></span>

**<span data-ttu-id="91e85-117">Pour désinstaller manuellement un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="91e85-117">To manually uninstall a MED-V workspace</span></span>**

1.  <span data-ttu-id="91e85-118">Sur l’ordinateur hôte, cliquez sur **Démarrer**, sur **panneau de configuration**, puis sur **programmes et fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="91e85-118">On the host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="91e85-119">Dans la fenêtre **programmes et fonctionnalités** , sélectionnez l’espace de travail MED-V que vous voulez supprimer, puis cliquez sur **désinstaller**.</span><span class="sxs-lookup"><span data-stu-id="91e85-119">In the **Programs and Features** window, select the MED-V workspace that you want to remove, and then click **Uninstall**.</span></span> <span data-ttu-id="91e85-120">(L’espace de travail MED-V est nommé «MED-V Workspace- &lt; *espace de travail \ _name* &gt; ").</span><span class="sxs-lookup"><span data-stu-id="91e85-120">(The MED-V workspace is named "MED-V Workspace - &lt;*workspace\_name*&gt;").</span></span> <span data-ttu-id="91e85-121">L' &lt; Assistant *de configuration de l’espace de travail \ _name* &gt; **Setup Wizard** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="91e85-121">The &lt;*workspace\_name*&gt; **Setup Wizard** opens.</span></span>

3.  <span data-ttu-id="91e85-122">Dans l' **Assistant Configuration**, cliquez sur **suivant**, puis sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="91e85-122">On the **Setup Wizard**, click **Next**, and then click **Remove**.</span></span>

4.  <span data-ttu-id="91e85-123">Si vous le souhaitez, activez la case à cocher pour supprimer le disque dur virtuel maître et les disques de différenciation créés par MED-V.</span><span class="sxs-lookup"><span data-stu-id="91e85-123">If you prefer, select the check box to delete the master VHD disk and differencing disks created by MED-V.</span></span> <span data-ttu-id="91e85-124">Cette opération n’est pas obligatoire, mais libère de l’espace disque après la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="91e85-124">This is not required, but frees disk space after the uninstallation finishes.</span></span>

5.  <span data-ttu-id="91e85-125">Cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="91e85-125">Click **Remove**.</span></span>

    <span data-ttu-id="91e85-126">**Remarques**  Si MED-V est en cours d’exécution, une boîte de dialogue s’affiche et vous demande si vous souhaitez l’arrêter.</span><span class="sxs-lookup"><span data-stu-id="91e85-126">**Note** If MED-V is currently running, a dialog box appears and prompts you whether you want to shut it down.</span></span> <span data-ttu-id="91e85-127">Cliquez sur **Oui** pour continuer la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="91e85-127">Click **Yes** to continue with the uninstallation.</span></span> <span data-ttu-id="91e85-128">Cliquez sur **non** pour annuler la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="91e85-128">Click **No** to cancel the uninstallation.</span></span>

     

<span data-ttu-id="91e85-129">Vous pouvez également supprimer un espace de travail MED-V en exécutant le `uninstall.exe` fichier qui se trouve généralement sur C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span><span class="sxs-lookup"><span data-stu-id="91e85-129">Alternately, you can remove a MED-V workspace by running the `uninstall.exe` file, typically located at C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span></span>

**<span data-ttu-id="91e85-130">Pour désinstaller manuellement l’agent hôte MED-V</span><span class="sxs-lookup"><span data-stu-id="91e85-130">To manually uninstall the MED-V Host Agent</span></span>**

1.  <span data-ttu-id="91e85-131">Sur l’ordinateur hôte de Windows 7, cliquez sur **Démarrer**, sur **panneau de configuration**, puis sur **programmes et fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="91e85-131">On the Windows 7 host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="91e85-132">Dans la fenêtre **programmes et fonctionnalités** , sélectionnez **agent d’hébergement MED-V**, puis cliquez sur **désinstaller**.</span><span class="sxs-lookup"><span data-stu-id="91e85-132">In the **Programs and Features** window, select **MED-V Host Agent**, and then click **Uninstall**.</span></span>

    <span data-ttu-id="91e85-133">Le programme d’installation de Windows supprime l’agent hôte MED-V.</span><span class="sxs-lookup"><span data-stu-id="91e85-133">The Windows Installer removes the MED-V Host Agent.</span></span>

    <span data-ttu-id="91e85-134">**Remarques**  Si vous essayez de désinstaller l’agent hôte MED-V avant de désinstaller l’espace de travail MED-V, une boîte de dialogue s’affiche pour indiquer que vous devez d’abord désinstaller l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="91e85-134">**Note** If you try to uninstall the MED-V Host Agent before you uninstall the MED-V workspace, a dialog box appears that states that you must first uninstall the MED-V workspace.</span></span> <span data-ttu-id="91e85-135">Cliquez sur **OK** pour continuer.</span><span class="sxs-lookup"><span data-stu-id="91e85-135">Click **OK** to continue.</span></span>

     

**<span data-ttu-id="91e85-136">Pour désinstaller manuellement le module de création de package de l’espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="91e85-136">To manually uninstall the MED-V Workspace Packager</span></span>**

1.  <span data-ttu-id="91e85-137">Sur l’ordinateur hôte, cliquez sur **Démarrer**, sur **panneau de configuration**, puis sur **programmes et fonctionnalités**.</span><span class="sxs-lookup"><span data-stu-id="91e85-137">On the host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="91e85-138">Dans la fenêtre **programmes et fonctionnalités** , sélectionnez **Gestionnaire de package d’espace de travail MED-V**, puis cliquez sur **désinstaller**.</span><span class="sxs-lookup"><span data-stu-id="91e85-138">In the **Programs and Features** window, select **MED-V Workspace Packager**, and then click **Uninstall**.</span></span>

    <span data-ttu-id="91e85-139">Le programme d’installation de Windows supprime le module de création de package de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="91e85-139">The Windows Installer removes the MED-V Workspace Packager.</span></span>

    <span data-ttu-id="91e85-140">**Remarques**  Vous pouvez désinstaller le module de création de package de l’espace de travail MED-V à tout moment sans affecter les espaces de travail MED-V déployés.</span><span class="sxs-lookup"><span data-stu-id="91e85-140">**Note** You can uninstall the MED-V Workspace Packager at any time without affecting any deployed MED-V workspaces.</span></span>

     

## <span data-ttu-id="91e85-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="91e85-141">Related topics</span></span>


[<span data-ttu-id="91e85-142">Déployer les composants MED-V</span><span class="sxs-lookup"><span data-stu-id="91e85-142">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)

 

 





