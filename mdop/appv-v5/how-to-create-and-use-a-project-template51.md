---
title: Comment créer et utiliser un modèle de projet
description: Comment créer et utiliser un modèle de projet
author: dansimp
ms.assetid: e5ac1dc8-a88f-4b16-8e3c-df07ef5e4c3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de3471eca39d3804e8c5f070c5ec37560fae5dc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805586"
---
# <span data-ttu-id="3bd32-103">Comment créer et utiliser un modèle de projet</span><span class="sxs-lookup"><span data-stu-id="3bd32-103">How to Create and Use a Project Template</span></span>


<span data-ttu-id="3bd32-104">Vous pouvez utiliser un modèle de projet App-V 5,1 pour enregistrer les paramètres fréquemment appliqués associés à un package d’application virtuel existant.</span><span class="sxs-lookup"><span data-stu-id="3bd32-104">You can use an App-V 5.1 project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="3bd32-105">Ces paramètres peuvent ensuite être appliqués lors de la création de nouveaux packages d’application virtuelle dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="3bd32-105">These settings can then be applied when you create new virtual application packages in your environment.</span></span> <span data-ttu-id="3bd32-106">L’utilisation d’un modèle de projet peut simplifier le processus de création de packages d’applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="3bd32-106">Using a project template can streamline the process of creating virtual application packages.</span></span>

**<span data-ttu-id="3bd32-107">Remarque</span><span class="sxs-lookup"><span data-stu-id="3bd32-107">Note</span></span>**  
<span data-ttu-id="3bd32-108">Vous pouvez également appliquer un modèle de projet App-V 5,1 lors d’une mise à niveau de package.</span><span class="sxs-lookup"><span data-stu-id="3bd32-108">You can, and often should apply an App-V 5.1 project template during a package upgrade.</span></span> <span data-ttu-id="3bd32-109">Par exemple, si vous avez séquencé une application avec une liste d’exclusion personnalisée, il est recommandé qu’un modèle associé soit créé et enregistré pour une utilisation ultérieure lors de la mise à niveau de l’application séquencée.</span><span class="sxs-lookup"><span data-stu-id="3bd32-109">For example, if you sequenced an application with a custom exclusion list, it is recommended that an associated template is created and saved for later use while upgrading the sequenced application.</span></span>



<span data-ttu-id="3bd32-110">Les modèles de projet App-V 5,1 diffèrent des accélérateurs d’application à l’application-V 5,1, car les accélérateurs d’application-V 5,1 sont propres à l’application et les modèles de projets App-V 5,1 peuvent être appliqués à plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="3bd32-110">App-V 5.1 project templates differ from App-V 5.1 Application Accelerators because App-V 5.1 Application Accelerators are application-specific, and App-V 5.1 project templates can be applied to multiple applications.</span></span>

<span data-ttu-id="3bd32-111">Pour créer et appliquer un nouveau modèle, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="3bd32-111">Use the following procedures to create and apply a new template.</span></span>

**<span data-ttu-id="3bd32-112">Pour créer un modèle de projet</span><span class="sxs-lookup"><span data-stu-id="3bd32-112">To create a project template</span></span>**

1.  <span data-ttu-id="3bd32-113">Pour démarrer le Sequencer App-V 5,1, sur l’ordinateur exécutant le Sequencer, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft  /  **Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="3bd32-113">To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  **<span data-ttu-id="3bd32-114">Remarque</span><span class="sxs-lookup"><span data-stu-id="3bd32-114">Note</span></span>**  
    <span data-ttu-id="3bd32-115">Si le package d’application virtuelle est actuellement ouvert dans la console App-V 5,1 Sequencer, passez à l’étape 3 de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="3bd32-115">If the virtual application package is currently open in the App-V 5.1 Sequencer console, skip to step 3 of this procedure.</span></span>



~~~
To open the existing virtual application package that contains the settings you want to save with the App-V 5.1 project template, click **File** / **Open**, and then click **Edit Package**. On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open. Click **Edit**.
~~~

3. <span data-ttu-id="3bd32-116">Dans la console App-V 5,1, pour enregistrer le fichier de modèle, cliquez sur **fichier**  /  **enregistrer en tant que modèle**.</span><span class="sxs-lookup"><span data-stu-id="3bd32-116">In the App-V 5.1 Sequencer console, to save the template file, click **File** / **Save As Template**.</span></span> <span data-ttu-id="3bd32-117">Après avoir consulté les paramètres qui seront enregistrés avec le nouveau modèle, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3bd32-117">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="3bd32-118">Spécifiez un nom qui sera associé au nouveau modèle de projet App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="3bd32-118">Specify a name that will be associated with the new App-V 5.1 project template.</span></span> <span data-ttu-id="3bd32-119">Cliquez sur Save.</span><span class="sxs-lookup"><span data-stu-id="3bd32-119">Click Save.</span></span>

   <span data-ttu-id="3bd32-120">Le nouveau modèle de projet App-V 5,1 est enregistré dans l’annuaire indiqué à l’étape 3 de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="3bd32-120">The new App-V 5.1 project template is saved in the directory specified in step 3 of this procedure.</span></span>

**<span data-ttu-id="3bd32-121">Pour appliquer un modèle de projet</span><span class="sxs-lookup"><span data-stu-id="3bd32-121">To apply a project template</span></span>**

1.  **<span data-ttu-id="3bd32-122">Important</span><span class="sxs-lookup"><span data-stu-id="3bd32-122">Important</span></span>**  
    <span data-ttu-id="3bd32-123">La création d’un package d’application virtuelle à l’aide d’un modèle de projet en conjonction avec un accélérateur de package n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="3bd32-123">Creating a virtual application package using a project template in conjunction with a Package Accelerator is not supported.</span></span>



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="3bd32-124">Pour créer ou mettre à niveau un nouveau package d’application virtuelle à l’aide d’un modèle de projet App-V 5,1, cliquez sur **fichier**  /  **nouveau à partir d’un modèle**.</span><span class="sxs-lookup"><span data-stu-id="3bd32-124">To create or upgrade a new virtual application package by using an App-V 5.1 project template, click **File** / **New From Template**.</span></span>

3. <span data-ttu-id="3bd32-125">Pour sélectionner le modèle de projet que vous voulez utiliser, accédez au répertoire où le modèle de projet est enregistré, sélectionnez le modèle de projet, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="3bd32-125">To select the project template that you want to use, browse to the directory where the project template is saved, select the project template, and then click **Open**.</span></span>

   <span data-ttu-id="3bd32-126">Créez le nouveau package d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="3bd32-126">Create the new virtual application package.</span></span> <span data-ttu-id="3bd32-127">Les paramètres enregistrés avec le modèle spécifié seront appliqués au nouveau package d’application virtuel que vous êtes en train de créer.</span><span class="sxs-lookup"><span data-stu-id="3bd32-127">The settings saved with the specified template will be applied to the new virtual application package that you are creating.</span></span>

   <span data-ttu-id="3bd32-128">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="3bd32-128">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="3bd32-129">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="3bd32-129">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="3bd32-130">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="3bd32-130">Got an App-V issue?</span></span>** <span data-ttu-id="3bd32-131">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="3bd32-131">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="3bd32-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3bd32-132">Related topics</span></span>


[<span data-ttu-id="3bd32-133">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="3bd32-133">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









