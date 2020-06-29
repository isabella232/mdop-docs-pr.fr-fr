---
title: Comment créer et utiliser un modèle de projet
description: Comment créer et utiliser un modèle de projet
author: dansimp
ms.assetid: 2063f0b3-47a1-4090-bf99-0f26b107331c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e7640b9dc1e7baec194315400ee5672dfa83f394
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805593"
---
# <span data-ttu-id="03d6c-103">Comment créer et utiliser un modèle de projet</span><span class="sxs-lookup"><span data-stu-id="03d6c-103">How to Create and Use a Project Template</span></span>


<span data-ttu-id="03d6c-104">Vous pouvez utiliser un modèle de projet App-V 5,0 pour enregistrer les paramètres fréquemment appliqués associés à un package d’application virtuel existant.</span><span class="sxs-lookup"><span data-stu-id="03d6c-104">You can use an App-V 5.0 project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="03d6c-105">Ces paramètres peuvent ensuite être appliqués lors de la création de nouveaux packages d’application virtuelle dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="03d6c-105">These settings can then be applied when you create new virtual application packages in your environment.</span></span> <span data-ttu-id="03d6c-106">L’utilisation d’un modèle de projet peut simplifier le processus de création de packages d’applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="03d6c-106">Using a project template can streamline the process of creating virtual application packages.</span></span>

<span data-ttu-id="03d6c-107">**Remarques**  Vous pouvez également appliquer un modèle de projet App-V 5,0 lors d’une mise à niveau de package.</span><span class="sxs-lookup"><span data-stu-id="03d6c-107">**Note** You can, and often should apply an App-V 5.0 project template during a package upgrade.</span></span> <span data-ttu-id="03d6c-108">Par exemple, si vous avez séquencé une application avec une liste d’exclusion personnalisée, il est recommandé qu’un modèle associé soit créé et enregistré pour une utilisation ultérieure lors de la mise à niveau de l’application séquencée.</span><span class="sxs-lookup"><span data-stu-id="03d6c-108">For example, if you sequenced an application with a custom exclusion list, it is recommended that an associated template is created and saved for later use while upgrading the sequenced application.</span></span>

<span data-ttu-id="03d6c-109">Les modèles de projet App-V 5,0 diffèrent des accélérateurs d’application à l’application-V 5,0, car les accélérateurs d’application-V 5,0 sont propres à l’application et les modèles de projets App-V 5,0 peuvent être appliqués à plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="03d6c-109">App-V 5.0 project templates differ from App-V 5.0 Application Accelerators because App-V 5.0 Application Accelerators are application-specific, and App-V 5.0 project templates can be applied to multiple applications.</span></span>

<span data-ttu-id="03d6c-110">Pour créer et appliquer un nouveau modèle, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="03d6c-110">Use the following procedures to create and apply a new template.</span></span>

**<span data-ttu-id="03d6c-111">Pour créer un modèle de projet</span><span class="sxs-lookup"><span data-stu-id="03d6c-111">To create a project template</span></span>**

1.  <span data-ttu-id="03d6c-112">Pour démarrer le Sequencer App-V 5,0, sur l’ordinateur exécutant le Sequencer, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft  /  **Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="03d6c-112">To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

<span data-ttu-id="03d6c-113">**Remarques**  Si le package d’application virtuelle est actuellement ouvert dans la console App-V 5,0 Sequencer, passez à l’étape 3 de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="03d6c-113">**Note** If the virtual application package is currently open in the App-V 5.0 Sequencer console, skip to step 3 of this procedure.</span></span>

2. <span data-ttu-id="03d6c-114">Pour ouvrir le package d’application virtuelle existant qui contient les paramètres que vous souhaitez enregistrer avec le modèle de projet App-V 5,0, cliquez sur **fichier**  /  **ouvrir**, puis sur **modifier le package**.</span><span class="sxs-lookup"><span data-stu-id="03d6c-114">To open the existing virtual application package that contains the settings you want to save with the App-V 5.0 project template, click **File** / **Open**, and then click **Edit Package**.</span></span> <span data-ttu-id="03d6c-115">Dans la page **Sélectionner un package** , cliquez sur **Parcourir** et recherchez le package d’application virtuel que vous voulez ouvrir.</span><span class="sxs-lookup"><span data-stu-id="03d6c-115">On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open.</span></span> <span data-ttu-id="03d6c-116">Cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="03d6c-116">Click **Edit**.</span></span>

3. <span data-ttu-id="03d6c-117">Dans la console App-V 5,0, pour enregistrer le fichier de modèle, cliquez sur **fichier**  /  **enregistrer en tant que modèle**.</span><span class="sxs-lookup"><span data-stu-id="03d6c-117">In the App-V 5.0 Sequencer console, to save the template file, click **File** / **Save As Template**.</span></span> <span data-ttu-id="03d6c-118">Après avoir consulté les paramètres qui seront enregistrés avec le nouveau modèle, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="03d6c-118">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="03d6c-119">Spécifiez un nom qui sera associé au nouveau modèle de projet App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="03d6c-119">Specify a name that will be associated with the new App-V 5.0 project template.</span></span> <span data-ttu-id="03d6c-120">Cliquez sur Save.</span><span class="sxs-lookup"><span data-stu-id="03d6c-120">Click Save.</span></span>
   <span data-ttu-id="03d6c-121">Le nouveau modèle de projet App-V 5,0 est enregistré dans l’annuaire indiqué à l’étape 3 de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="03d6c-121">The new App-V 5.0 project template is saved in the directory specified in step 3 of this procedure.</span></span>

**<span data-ttu-id="03d6c-122">Pour appliquer un modèle de projet</span><span class="sxs-lookup"><span data-stu-id="03d6c-122">To apply a project template</span></span>**

<span data-ttu-id="03d6c-123">**Important**  La création d’un package d’application virtuelle à l’aide d’un modèle de projet en conjonction avec un accélérateur de package n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="03d6c-123">**Important** Creating a virtual application package using a project template in conjunction with a Package Accelerator is not supported.</span></span>

1.  <span data-ttu-id="03d6c-124">Pour démarrer le Sequencer App-V 5,0, sur l’ordinateur exécutant le Sequencer, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft  /  **Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="03d6c-124">To start the App-V 5.0 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="03d6c-125">Pour créer ou mettre à niveau un nouveau package d’application virtuelle à l’aide d’un modèle de projet App-V 5,0, cliquez sur **fichier**  /  **nouveau à partir d’un modèle**.</span><span class="sxs-lookup"><span data-stu-id="03d6c-125">To create or upgrade a new virtual application package by using an App-V 5.0 project template, click **File** / **New From Template**.</span></span>

3.  <span data-ttu-id="03d6c-126">Pour sélectionner le modèle de projet que vous voulez utiliser, accédez au répertoire où le modèle de projet est enregistré, sélectionnez le modèle de projet, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="03d6c-126">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

    <span data-ttu-id="03d6c-127">Créez le nouveau package d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="03d6c-127">Create the new virtual application package.</span></span> <span data-ttu-id="03d6c-128">Les paramètres enregistrés avec le modèle spécifié seront appliqués au nouveau package d’application virtuel que vous êtes en train de créer.</span><span class="sxs-lookup"><span data-stu-id="03d6c-128">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span>

    <span data-ttu-id="03d6c-129">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="03d6c-129">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="03d6c-130">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="03d6c-130">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="03d6c-131">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="03d6c-131">Got an App-V issue?</span></span>** <span data-ttu-id="03d6c-132">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="03d6c-132">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="03d6c-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03d6c-133">Related topics</span></span>


[<span data-ttu-id="03d6c-134">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="03d6c-134">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









