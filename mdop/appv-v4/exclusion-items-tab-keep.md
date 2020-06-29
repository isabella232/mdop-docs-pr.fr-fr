---
title: Onglet Éléments d'exclusion
description: Onglet Éléments d'exclusion
author: dansimp
ms.assetid: 864e46dd-3d6e-4a1b-acf4-9dc00548117e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f472fb61c121a1977c3c4ff927bd1ba6f680d86
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808838"
---
# <span data-ttu-id="1eb9b-103">Onglet Éléments d'exclusion</span><span class="sxs-lookup"><span data-stu-id="1eb9b-103">Exclusion Items Tab</span></span>


<span data-ttu-id="1eb9b-104">L’onglet **éléments d’exclusion** affiche les expressions que le Sequencer de virtualisation d’application exclut du Registre virtuel ou du système de fichiers virtuel.</span><span class="sxs-lookup"><span data-stu-id="1eb9b-104">The **Exclusion Items** tab displays the expressions that the Application Virtualization Sequencer excludes from the virtual file system or virtual registry.</span></span> <span data-ttu-id="1eb9b-105">Ces expressions sont exclues pour garantir que le package d’application séquencé puisse s’exécuter sur des clients de bureau de la virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="1eb9b-105">These expressions are excluded to ensure that the sequenced application package can run on Application Virtualization Desktop Clients.</span></span> <span data-ttu-id="1eb9b-106">Vous pouvez également exclure les répertoires d’installation non standard qui peuvent être indésirables lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="1eb9b-106">You can also exclude non-standard installation directories that might be unwanted in the sequencing.</span></span>

<span data-ttu-id="1eb9b-107">Cet onglet contient les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="1eb9b-107">This tab contains the following elements.</span></span>

<a href="" id="exclude-path"></a>**<span data-ttu-id="1eb9b-108">Exclure le chemin</span><span class="sxs-lookup"><span data-stu-id="1eb9b-108">Exclude Path</span></span>**  
<span data-ttu-id="1eb9b-109">Affiche les noms de variables que le Sequencer exclut s’il est rencontré lors de l’analyse des éléments du système de fichiers virtuel ou des éléments du Registre virtuel.</span><span class="sxs-lookup"><span data-stu-id="1eb9b-109">Displays variable names that the Sequencer excludes if encountered while parsing virtual file system items or virtual registry items.</span></span>

<a href="" id="resolves-to"></a>**<span data-ttu-id="1eb9b-110">Est résolu en</span><span class="sxs-lookup"><span data-stu-id="1eb9b-110">Resolves To</span></span>**  
<span data-ttu-id="1eb9b-111">Affiche les chemins d’accès réels correspondant aux variables de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="1eb9b-111">Displays the actual paths that correspond to the Sequencer variables.</span></span>

<a href="" id="map-type"></a>**<span data-ttu-id="1eb9b-112">Type de carte</span><span class="sxs-lookup"><span data-stu-id="1eb9b-112">Map Type</span></span>**  
<span data-ttu-id="1eb9b-113">Affiche les règles de mappage auxquelles le Sequencer s’applique pour analyser les éléments dans le système de fichiers virtuel ou le registre virtuel.</span><span class="sxs-lookup"><span data-stu-id="1eb9b-113">Displays mapping rules that the Sequencer applies to parse items in the virtual file system or virtual registry.</span></span> <span data-ttu-id="1eb9b-114">L’une des valeurs suivantes peut se produire:</span><span class="sxs-lookup"><span data-stu-id="1eb9b-114">One of the following values can occur:</span></span>

<a href="" id="new"></a>**<span data-ttu-id="1eb9b-115">Nouveau</span><span class="sxs-lookup"><span data-stu-id="1eb9b-115">New</span></span>**  
<span data-ttu-id="1eb9b-116">Cliquez pour entrer un nouvel élément d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="1eb9b-116">Click to enter a new exclusion item.</span></span>

<a href="" id="edit"></a>**<span data-ttu-id="1eb9b-117">Edit</span><span class="sxs-lookup"><span data-stu-id="1eb9b-117">Edit</span></span>**  
<span data-ttu-id="1eb9b-118">Cliquez pour modifier une exclusion sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="1eb9b-118">Click to edit a selected exclusion.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="1eb9b-119">Delete</span><span class="sxs-lookup"><span data-stu-id="1eb9b-119">Delete</span></span>**  
<span data-ttu-id="1eb9b-120">Cliquez pour supprimer une exclusion sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="1eb9b-120">Click to remove a selected exclusion.</span></span>

<a href="" id="save-as-default"></a>**<span data-ttu-id="1eb9b-121">Enregistrer par défaut</span><span class="sxs-lookup"><span data-stu-id="1eb9b-121">Save As Default</span></span>**  
<span data-ttu-id="1eb9b-122">Cliquez sur cette option pour enregistrer les éléments d’exclusion actuels comme éléments par défaut.</span><span class="sxs-lookup"><span data-stu-id="1eb9b-122">Click to save the current exclusion items as your default.</span></span>

<a href="" id="restore-defaults"></a>**<span data-ttu-id="1eb9b-123">Restaurer les valeurs par défaut</span><span class="sxs-lookup"><span data-stu-id="1eb9b-123">Restore Defaults</span></span>**  
<span data-ttu-id="1eb9b-124">Cliquez pour restaurer les éléments d’exclusion par défaut assignés et supprimer les éléments que vous avez ajoutés.</span><span class="sxs-lookup"><span data-stu-id="1eb9b-124">Click to restore default-assigned exclusion items and remove any items you added.</span></span>

<a href="" id="ok"></a>**<span data-ttu-id="1eb9b-125">OK</span><span class="sxs-lookup"><span data-stu-id="1eb9b-125">OK</span></span>**  
<span data-ttu-id="1eb9b-126">Cliquez sur pour accepter les exceptions affichées.</span><span class="sxs-lookup"><span data-stu-id="1eb9b-126">Click to accept the displayed exceptions.</span></span>

<a href="" id="cancel"></a>**<span data-ttu-id="1eb9b-127">Annuler</span><span class="sxs-lookup"><span data-stu-id="1eb9b-127">Cancel</span></span>**  
<span data-ttu-id="1eb9b-128">Cliquez sur pour annuler les modifications que vous avez apportées.</span><span class="sxs-lookup"><span data-stu-id="1eb9b-128">Click to cancel any changes you have made.</span></span>

## <span data-ttu-id="1eb9b-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1eb9b-129">Related topics</span></span>


[<span data-ttu-id="1eb9b-130">Boite de dialogue Options d'Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="1eb9b-130">Application Virtualization Sequencer Options Dialog Box</span></span>](application-virtualization-sequencer-options-dialog-box.md)

[<span data-ttu-id="1eb9b-131">Boîte de dialogue Élément d'exclusion</span><span class="sxs-lookup"><span data-stu-id="1eb9b-131">Exclusion Item Dialog Box</span></span>](exclusion-item-dialog-box.md)

 

 





