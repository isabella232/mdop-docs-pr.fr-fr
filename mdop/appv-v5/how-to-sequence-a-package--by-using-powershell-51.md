---
title: Comment séquencer un package à l’aide de PowerShell
description: Comment séquencer un package à l’aide de PowerShell
author: dansimp
ms.assetid: 6134c6be-937d-4609-a516-92d49154b290
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1bc2933fdb64080dab3b514784e7f68b0236df9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805167"
---
# <span data-ttu-id="e5c04-103">Comment séquencer un package à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5c04-103">How to Sequence a Package by Using PowerShell</span></span>


<span data-ttu-id="e5c04-104">Utilisez la procédure suivante pour créer un package App-V 5,1 à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e5c04-104">Use the following procedure to create a new App-V 5.1 package using PowerShell.</span></span>

<span data-ttu-id="e5c04-105">**Remarques**  Avant d’utiliser cette procédure, vous devez copier les fichiers du programme d’installation associé sur l’ordinateur exécutant le Sequencer et vous avez lu et compris la section de Sequencer de [planification pour le déploiement du client et du Sequencer App-V 5,1](planning-for-the-app-v-51-sequencer-and-client-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="e5c04-105">**Note** Before you use this procedure you must copy the associated installer files to the computer running the sequencer and you have read and understand the sequencer section of [Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md).</span></span>

 

**<span data-ttu-id="e5c04-106">Pour créer une nouvelle application virtuelle à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5c04-106">To create a new virtual application using PowerShell</span></span>**

1.  <span data-ttu-id="e5c04-107">Installez le Sequencer App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="e5c04-107">Install the App-V 5.1 sequencer.</span></span> <span data-ttu-id="e5c04-108">Pour plus d’informations sur l’installation de Sequencer, voir [Comment installer le Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="e5c04-108">For more information about installing the sequencer see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

2.  <span data-ttu-id="e5c04-109">Pour ouvrir une console PowerShell, cliquez sur **Démarrer** et tapez **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="e5c04-109">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="e5c04-110">Cliquez avec le bouton droit sur **Windows PowerShell**, puis sélectionnez **Exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="e5c04-110">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span>

3.  <span data-ttu-id="e5c04-111">À l’aide de la console PowerShell, tapez ce qui suit: **import-module appvsequencer**.</span><span class="sxs-lookup"><span data-stu-id="e5c04-111">Using the PowerShell console, type the following: **import-module appvsequencer**.</span></span>

4.  <span data-ttu-id="e5c04-112">Pour créer un package, utilisez l’applet **de nouvelle applet de nouveau-AppvSequencerPackage** .</span><span class="sxs-lookup"><span data-stu-id="e5c04-112">To create a package, use the **New-AppvSequencerPackage** cmdlet.</span></span> <span data-ttu-id="e5c04-113">Les paramètres suivants sont nécessaires pour créer un package:</span><span class="sxs-lookup"><span data-stu-id="e5c04-113">The following parameters are required to create a package:</span></span>

    -   <span data-ttu-id="e5c04-114">**Nom** : spécifie le nom du package.</span><span class="sxs-lookup"><span data-stu-id="e5c04-114">**Name** - specifies the name of the package.</span></span>

    -   <span data-ttu-id="e5c04-115">**PrimaryVirtualApplicationDirectory** : spécifie le chemin d’accès du répertoire qui sera utilisé pour installer l’application.</span><span class="sxs-lookup"><span data-stu-id="e5c04-115">**PrimaryVirtualApplicationDirectory** - specifies the path to the directory that will be used to install the application.</span></span> <span data-ttu-id="e5c04-116">Ce chemin doit exister.</span><span class="sxs-lookup"><span data-stu-id="e5c04-116">This path must exist.</span></span>

    -   <span data-ttu-id="e5c04-117">**Programme d’installation** : spécifie le chemin d’accès au programme d’installation d’applications associé.</span><span class="sxs-lookup"><span data-stu-id="e5c04-117">**Installer** - specifies the path to the associated application installer.</span></span>

    -   <span data-ttu-id="e5c04-118">**Path** -spécifie le répertoire de sortie du package.</span><span class="sxs-lookup"><span data-stu-id="e5c04-118">**Path** - specifies the output directory for the package.</span></span>

    <span data-ttu-id="e5c04-119">Exemple:</span><span class="sxs-lookup"><span data-stu-id="e5c04-119">For example:</span></span>

    **<span data-ttu-id="e5c04-120">New-AppvSequencerPackage-nom &lt; du package &gt; -PrimaryVirtualApplicationDirectory chemin d’accès &lt; au programme d’installation racine du package vers le &gt; &lt; répertoire exécutable du programme d’installation &gt; -OutputPath &lt; du chemin de sortie&gt;</span><span class="sxs-lookup"><span data-stu-id="e5c04-120">New-AppvSequencerPackage –Name &lt;name of Package&gt; -PrimaryVirtualApplicationDirectory &lt;path to the package root&gt; -Installer &lt;path to the installer executable&gt; -OutputPath &lt;directory of the output path&gt;</span></span>**

    <span data-ttu-id="e5c04-121">Attendez que le Sequencer crée le package.</span><span class="sxs-lookup"><span data-stu-id="e5c04-121">Wait for the sequencer to create the package.</span></span> <span data-ttu-id="e5c04-122">La création d’un package à l’aide de PowerShell peut prendre du temps.</span><span class="sxs-lookup"><span data-stu-id="e5c04-122">Creating a package using PowerShell can take time.</span></span> <span data-ttu-id="e5c04-123">Si le package n’a pas été créé correctement, une erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="e5c04-123">If the package was not created successfully an error will be returned.</span></span>

    <span data-ttu-id="e5c04-124">La liste suivante présente des paramètres facultatifs supplémentaires qui peuvent être utilisés avec l’applet **de commande New-AppvSequencerPackage** :</span><span class="sxs-lookup"><span data-stu-id="e5c04-124">The following list displays additional optional parameters that can be used with **New-AppvSequencerPackage** cmdlet:</span></span>

    -   <span data-ttu-id="e5c04-125">AcceleratorFilePath: spécifie le chemin d’accès au fichier Accelerator. cab pour générer un package.</span><span class="sxs-lookup"><span data-stu-id="e5c04-125">AcceleratorFilePath – specifies the path to the accelerator .cab file to generate a package.</span></span>

    -   <span data-ttu-id="e5c04-126">InstalledFilesPath: spécifie le chemin d’accès de l’emplacement vers lequel les fichiers locaux installés de l’application sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="e5c04-126">InstalledFilesPath - specifies the path to where the local installed files of the application are saved.</span></span>

    -   <span data-ttu-id="e5c04-127">InstallMediaPath: spécifie le chemin d’accès du support d’installation.</span><span class="sxs-lookup"><span data-stu-id="e5c04-127">InstallMediaPath - specifies the path to where the installation media is</span></span>

    -   <span data-ttu-id="e5c04-128">TemplateFilePath: spécifie le chemin d’accès d’un fichier de modèle si vous souhaitez personnaliser le processus de séquençage.</span><span class="sxs-lookup"><span data-stu-id="e5c04-128">TemplateFilePath - specifies the path to a template file if you want to customize the sequencing process.</span></span>

    -   <span data-ttu-id="e5c04-129">FullLoad: indique que le package doit être entièrement téléchargé sur l’ordinateur exécutant l’application-V 5,1 pour pouvoir être ouvert.</span><span class="sxs-lookup"><span data-stu-id="e5c04-129">FullLoad - specifies that the package must be fully downloaded to the computer running the App-V 5.1 before it can be opened.</span></span>

    <span data-ttu-id="e5c04-130">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="e5c04-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="e5c04-131">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="e5c04-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="e5c04-132">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="e5c04-132">Got an App-V issue?</span></span>** <span data-ttu-id="e5c04-133">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="e5c04-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="e5c04-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e5c04-134">Related topics</span></span>


[<span data-ttu-id="e5c04-135">Administration d'App-V5.1 à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5c04-135">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)

 

 





