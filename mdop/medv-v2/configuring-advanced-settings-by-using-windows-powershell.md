---
title: Configuration de paramètres avancés à l'aide de Windows PowerShell
description: Configuration de paramètres avancés à l'aide de Windows PowerShell
author: dansimp
ms.assetid: 437a31cc-2a11-456f-b448-b0b869fb53f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a3ece3f76f6e982913aad2b25cfe0084542f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812329"
---
# <span data-ttu-id="6066a-103">Configuration de paramètres avancés à l'aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6066a-103">Configuring Advanced Settings by Using Windows PowerShell</span></span>


<span data-ttu-id="6066a-104">Le package d’espace de travail MED-V que vous créez inclut un fichier de script Windows PowerShell (. ps1) que vous pouvez modifier avant de tester et de déployer votre package d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="6066a-104">The MED-V workspace package that you create includes a Windows PowerShell script (.ps1) file that you can edit before you test and deploy your MED-V workspace package.</span></span> <span data-ttu-id="6066a-105">Cette section fournit des informations et des conseils pour vous aider à gérer les paramètres de configuration de MED-V à l’aide de Windows PowerShell avant de déployer les espaces de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="6066a-105">This section provides information and guidance to help you manage MED-V configuration settings by using Windows PowerShell before you deploy the MED-V workspaces.</span></span>

## <span data-ttu-id="6066a-106">Utilisation des cmdlets Windows PowerShell dans MED-V</span><span class="sxs-lookup"><span data-stu-id="6066a-106">Using Windows PowerShell Cmdlets in MED-V</span></span>


<span data-ttu-id="6066a-107">Les applets de commande Windows PowerShell suivantes sont disponibles dans Microsoft Enterprise Desktop Virtualization (MED-V) 2,0:</span><span class="sxs-lookup"><span data-stu-id="6066a-107">The following Windows PowerShell cmdlets are available in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0:</span></span>

**<span data-ttu-id="6066a-108">Nouveau-MedvConfiguration</span><span class="sxs-lookup"><span data-stu-id="6066a-108">New-MedvConfiguration</span></span>**

**<span data-ttu-id="6066a-109">Export-MedvConfiguration</span><span class="sxs-lookup"><span data-stu-id="6066a-109">Export-MedvConfiguration</span></span>**

**<span data-ttu-id="6066a-110">Nouveau-MedvWorkspace</span><span class="sxs-lookup"><span data-stu-id="6066a-110">New-MedvWorkspace</span></span>**

**<span data-ttu-id="6066a-111">Export-MedvWorkspace</span><span class="sxs-lookup"><span data-stu-id="6066a-111">Export-MedvWorkspace</span></span>**

<span data-ttu-id="6066a-112">Pour accéder aux cmdlets Windows PowerShell pour MED-V, ouvrez Windows PowerShell, puis tapez la commande suivante pour importer les modules MED-V.</span><span class="sxs-lookup"><span data-stu-id="6066a-112">To access Windows PowerShell cmdlets for MED-V, open Windows PowerShell and type the following command to import the MED-V modules.</span></span>

``` syntax
Import-Module microsoft.medv
```

<span data-ttu-id="6066a-113">Une fois les modules importés, vous pouvez accéder à l’aide incluse pour les applets de commande en utilisant les commandes **standard de l'** **aide de Windows PowerShell.**</span><span class="sxs-lookup"><span data-stu-id="6066a-113">After the modules are imported, you can access inline help for the cmdlets by using the standard Windows PowerShell Help commands, **man** or **get-help**.</span></span> <span data-ttu-id="6066a-114">Par exemple, pour accéder à une description de l’applet **de commande New-MedvConfiguration** et obtenir la liste complète des paramètres disponibles, tapez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="6066a-114">For example, to access a description of the **New-MedvConfiguration** cmdlet including a complete list of available parameters, type the following command.</span></span>

``` syntax
get-help New-MedvConfiguration
```

<span data-ttu-id="6066a-115">Vous pouvez également afficher l’aide de paramètres spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6066a-115">You can also view help for specific parameters.</span></span> <span data-ttu-id="6066a-116">Par exemple, pour afficher l’aide du paramètre VmMemory, tapez ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="6066a-116">For example, to view help for the parameter VmMemory, type the following:</span></span>

``` syntax
get-help New-MedvConfiguration -parameter VmMemory
```

<span data-ttu-id="6066a-117">Pour afficher la liste de tous les paramètres de configuration de MED-V et leurs valeurs par défaut, tapez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="6066a-117">To view a list of all MED-V configuration settings and their defaults, type the following command.</span></span>

``` syntax
New-MedvConfiguration -ForceDefaults
```

<span data-ttu-id="6066a-118">Pour afficher la liste de tous les paramètres de configuration de MED-V et leurs valeurs actuelles, tapez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="6066a-118">To view a list of all MED-V configuration settings and their current values, type the following command.</span></span>

``` syntax
gwmi -Class "Setting” -Namespace "root/microsoft/medv”
```

## <span data-ttu-id="6066a-119">Création d’un espace de travail MED-V avec des paramètres personnalisés</span><span class="sxs-lookup"><span data-stu-id="6066a-119">Creating a MED-V Workspace with Custom Settings</span></span>


<span data-ttu-id="6066a-120">Une fois que vous avez créé un package d’espace de travail MED-V en utilisant le gestionnaire de package MED-V, un script Windows PowerShell est généré dans le dossier que vous avez spécifié pour l’enregistrement de vos fichiers de package.</span><span class="sxs-lookup"><span data-stu-id="6066a-120">After you successfully create a MED-V workspace package by using the MED-V Workspace Packager, a Windows PowerShell script is generated in the folder you specified for saving your packager files.</span></span> <span data-ttu-id="6066a-121">Le contenu de ce script présente certains des paramètres de configuration MED-V que vous pouvez modifier.</span><span class="sxs-lookup"><span data-stu-id="6066a-121">The contents of this script show some of the available MED-V configuration settings that you can edit.</span></span>

<span data-ttu-id="6066a-122">Après avoir suivi ces étapes, vous pouvez personnaliser le script puis l’exécuter dans Windows PowerShell pour créer un espace de travail MED-V avec les nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="6066a-122">Following these steps, you can customize the script and then run it in Windows PowerShell to create a MED-V workspace with the new settings.</span></span>

<span data-ttu-id="6066a-123">**Important**  Exécutez Windows PowerShell avec des informations d’identification d’administration, et assurez-vous que la stratégie d’exécution Windows PowerShell autorise l’exécution de scripts.</span><span class="sxs-lookup"><span data-stu-id="6066a-123">**Important** Run Windows PowerShell with administrative credentials, and ensure that the Windows PowerShell execution policy allows the running of scripts.</span></span>

1.  <span data-ttu-id="6066a-124">Modifiez le script Windows PowerShell généré par le module de création de package de l’espace de travail MED-V, ou créez un nouveau script avec les paramètres de configuration de votre choix.</span><span class="sxs-lookup"><span data-stu-id="6066a-124">Edit the Windows PowerShell script that was generated by the MED-V Workspace Packager, or author a new script with the configuration settings that you want.</span></span>

2.  <span data-ttu-id="6066a-125">Exécutez Windows PowerShell avec des informations d’identification d’administration, puis à l’invite de commandes, tapez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="6066a-125">Run Windows PowerShell with administrative credentials and at the command prompt, type the following command.</span></span>

    ``` syntax
    & “.\<workspacename>.ps1”
    ```

    <span data-ttu-id="6066a-126">Cette commande exécute le script Windows PowerShell et exécute l’applet de commande **New-MedvWorkspace** pour générer un nouveau package d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="6066a-126">This command runs the Windows PowerShell script and runs the **New-MedvWorkspace** cmdlet to generate a new MED-V workspace package.</span></span> <span data-ttu-id="6066a-127">Les nouveaux fichiers du gestionnaire de package sont enregistrés dans le dossier que vous avez spécifié à l’origine pour le stockage de vos fichiers de package de package d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="6066a-127">The new packager files are saved in the folder that you originally specified for storing your MED-V Workspace Packager files.</span></span> <span data-ttu-id="6066a-128">Pour obtenir de l’aide supplémentaire sur cette cmdlet, voir l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6066a-128">For additional help about this cmdlet, see the Windows PowerShell Help.</span></span>

 

## <span data-ttu-id="6066a-129">Exportation d’une configuration MED-V vers un fichier de Registre</span><span class="sxs-lookup"><span data-stu-id="6066a-129">Exporting a MED-V Configuration to a Registry File</span></span>


<span data-ttu-id="6066a-130">Vous pouvez mettre à jour les paramètres de configuration de MED-V après l’installation de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="6066a-130">You can update MED-V configuration settings after the MED-V workspace is installed.</span></span> <span data-ttu-id="6066a-131">Utilisez l’applet de nouvelle applet de **MedvConfiguration** pour spécifier les paramètres que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="6066a-131">Use the **New-MedvConfiguration** cmdlet to specify the parameters that you want to change.</span></span> <span data-ttu-id="6066a-132">Par exemple, pour créer un fichier de Registre qui modifie le paramètre de mémoire de l’ordinateur virtuel, tapez les commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="6066a-132">For example, to create a registry file that changes the virtual machine memory setting, type the following commands.</span></span>

``` syntax
New-MedvConfiguration  -VmMemory 1024 | Export-MedvConfiguration -Path c:\medvConfiguration\myConfig.reg
```

<span data-ttu-id="6066a-133">Vous pouvez importer le fichier de Registre résultant de l’ordinateur hôte dans un espace de travail MED-V pour appliquer les nouveaux paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="6066a-133">You can import the resultant registry file from the host computer to a MED-V workspace to apply the new configuration settings.</span></span>

## <span data-ttu-id="6066a-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6066a-134">Related topics</span></span>


[<span data-ttu-id="6066a-135">Gestion des paramètres de configuration d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="6066a-135">Managing MED-V Workspace Configuration Settings</span></span>](managing-med-v-workspace-configuration-settings.md)

[<span data-ttu-id="6066a-136">Tester et déployer le package d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="6066a-136">Test And Deploy the MED-V Workspace Package</span></span>](test-and-deploy-the-med-v-workspace-package.md)

 

 





