---
title: Procédure pour créer un modèle de projet App-V (App-V4.6 SP1)
description: Procédure pour créer un modèle de projet App-V (App-V4.6 SP1)
author: dansimp
ms.assetid: 7e87fba2-b72a-4bc9-92b8-220e25aae99a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e264d5c41b663bc9c450dc642e2b26297ee7ea1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807190"
---
# <span data-ttu-id="dcfb5-103">Procédure pour créer un modèle de projet App-V (App-V4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="dcfb5-103">How to Create an App-V Project Template (App-V 4.6 SP1)</span></span>


<span data-ttu-id="dcfb5-104">Vous pouvez utiliser un modèle de projet App-V pour enregistrer les paramètres fréquemment appliqués associés à un package d’application virtuel existant.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-104">You can use an App-V project template to save commonly applied settings associated with an existing virtual application package.</span></span> <span data-ttu-id="dcfb5-105">Ces paramètres peuvent ensuite être appliqués lorsque vous créez de nouveaux packages d’application virtuelle dans votre environnement, ce qui peut vous aider à rationaliser le processus de création de packages d’applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-105">These settings can then be applied when you create new virtual application packages in your environment which can help streamline the process of creating virtual application packages.</span></span>

<span data-ttu-id="dcfb5-106">**Remarques**  Vous pouvez appliquer un modèle de projet App-V uniquement lorsque vous créez un nouveau package d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-106">**Note** You can only apply an App-V project template when you are creating a new virtual application package.</span></span> <span data-ttu-id="dcfb5-107">L’application de modèles de projet aux packages d’applications virtuelles existants n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-107">Applying project templates to existing virtual application packages is not supported.</span></span>

 

<span data-ttu-id="dcfb5-108">Pour plus d’informations sur l’application d’un modèle de projet App-V, voir [comment appliquer un modèle de projet App-v (App-V 4,6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="dcfb5-108">For more information about applying an App-V project template, see [How to Apply an App-V Project Template (App-V 4.6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).</span></span>

<span data-ttu-id="dcfb5-109">Les modèles de projet App-V diffèrent des accélérateurs d’applications App-v, car ils sont propres aux applications et les modèles de projets App-v peuvent être appliqués à plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-109">App-V project templates differ from App-V Application Accelerators because App-V Application Accelerators are application-specific, and App-V project templates can be applied to multiple applications.</span></span> <span data-ttu-id="dcfb5-110">Par ailleurs, vous ne pouvez pas utiliser un modèle de projet lorsque vous utilisez un accélérateur de package pour créer un package d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-110">Additionally, you cannot use a project template when you use a Package Accelerator to create a virtual application package.</span></span>

<span data-ttu-id="dcfb5-111">Les paramètres généraux suivants sont enregistrés avec un modèle de projet App-V:</span><span class="sxs-lookup"><span data-stu-id="dcfb5-111">The following general settings are saved with an App-V project template:</span></span>

-   <span data-ttu-id="dcfb5-112">**Options de surveillance avancée**.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-112">**Advanced Monitoring Options**.</span></span> <span data-ttu-id="dcfb5-113">Autorise l’exécution de Microsoft Update lors de l’analyse, rebase **. dll**.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-113">Enables Microsoft Update to run during monitoring, Rebase **.dll’s**.</span></span>

-   <span data-ttu-id="dcfb5-114">**Paramètres de déploiement de package**.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-114">**Package Deployment Settings**.</span></span> <span data-ttu-id="dcfb5-115">Contient le **protocole**, le **nom d’hôte**, le **port**, le **chemin d’accès**, les **systèmes d’exploitation**, l' **application des DEscripteurs de sécurité**, la création d’un **package** **MSI**</span><span class="sxs-lookup"><span data-stu-id="dcfb5-115">Contains **Protocol**, **Host Name**, **Port**, **Path**, **Operating Systems**, **Enforce Security Descriptors**, **Create MSI**, **Compress Package**.</span></span>

-   <span data-ttu-id="dcfb5-116">**Options générales**.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-116">**General Options**.</span></span> <span data-ttu-id="dcfb5-117">Vous permet de **générer le package Microsoft Windows Installer (MSI)** , **de permettre la virtualisation des événements**, **de la virtualisation des services**, **d’ajouter la version du package à un nom de fichier**.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-117">Allows you to **Generate Microsoft Windows Installer (MSI)** package, **Allow Virtualization of Events**, **Allow Virtualization of Services**, **Append Package Version to Filename**.</span></span>

-   <span data-ttu-id="dcfb5-118">**Éléments d’exclusion**.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-118">**Exclusion Items**.</span></span> <span data-ttu-id="dcfb5-119">Contient la liste modèle d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-119">Contains the Exclusion pattern list.</span></span>

**<span data-ttu-id="dcfb5-120">Pour créer un modèle de projet</span><span class="sxs-lookup"><span data-stu-id="dcfb5-120">To create a project template</span></span>**

1.  <span data-ttu-id="dcfb5-121">Pour démarrer le Sequencer App-v, sur l’ordinateur exécutant le Sequencer App-v, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft Application Virtualization  /  **Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-121">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="dcfb5-122">Si le package d’application virtuelle est actuellement ouvert dans le Sequencer App-V, passez à l’étape 3 de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-122">If the virtual application package is currently open in the App-V Sequencer, skip to step 3 of this procedure.</span></span> <span data-ttu-id="dcfb5-123">Pour ouvrir le package d’application virtuelle existant qui contient les paramètres que vous souhaitez enregistrer avec le modèle de projet App-V, cliquez sur **fichier**  /  **ouvrir** , puis sur **modifier** le **package**.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-123">To open the existing virtual application package that contains the settings you want to save with the App-V project template, click **File** / **Open** and click **Edit** **Package**.</span></span> <span data-ttu-id="dcfb5-124">Dans la page **Sélectionner un package** , cliquez sur **Parcourir** et recherchez le package d’application virtuel que vous voulez ouvrir.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-124">On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open.</span></span> <span data-ttu-id="dcfb5-125">Cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-125">Click **Edit**.</span></span>

3.  <span data-ttu-id="dcfb5-126">Dans la console App-V du Sequencer, cliquez sur **fichier**  /  **enregistrer en tant que modèle**.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-126">In the App-V Sequencer console, click **File** / **Save As Template**.</span></span> <span data-ttu-id="dcfb5-127">Après avoir consulté les paramètres qui seront enregistrés avec le nouveau modèle, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-127">After you have reviewed the settings that will be saved with the new template, click **OK**.</span></span> <span data-ttu-id="dcfb5-128">Spécifiez un nom qui sera associé au nouveau modèle de projet App-V.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-128">Specify a name that will be associated with the new App-V project template.</span></span> <span data-ttu-id="dcfb5-129">Cliquez sur **Save**.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-129">Click **Save**.</span></span>

    <span data-ttu-id="dcfb5-130">Le nouveau modèle de projet App-V est enregistré dans l’annuaire indiqué à l’étape 3 de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="dcfb5-130">The new App-V project template is saved in the directory specified in step 3 of this procedure.</span></span>

## <span data-ttu-id="dcfb5-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dcfb5-131">Related topics</span></span>


[<span data-ttu-id="dcfb5-132">Tâches pour Application Virtualization Sequencer (App-V4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="dcfb5-132">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="dcfb5-133">Procédure pour appliquer un modèle de projet App-V (App-V4.6SP1)</span><span class="sxs-lookup"><span data-stu-id="dcfb5-133">How to Apply an App-V Project Template (App-V 4.6 SP1)</span></span>](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md)

 

 





