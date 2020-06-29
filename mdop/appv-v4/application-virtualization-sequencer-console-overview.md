---
title: Vue d'ensemble de la console Application Virtualization Sequencer
description: Vue d'ensemble de la console Application Virtualization Sequencer
author: dansimp
ms.assetid: 681bb40d-2937-4645-82aa-4a44775232d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2f977fccaaded0309181a1d74c16b749498abb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809209"
---
# <span data-ttu-id="6592f-103">Vue d'ensemble de la console Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="6592f-103">Application Virtualization Sequencer Console Overview</span></span>


<span data-ttu-id="6592f-104">Le Sequencer Application Virtualization (App-V) crée des applications pour pouvoir s’exécuter dans un environnement virtuel, en tant qu’applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="6592f-104">The Application Virtualization (App-V) Sequencer creates applications so that they can be run in a virtual environment, as virtual applications.</span></span> <span data-ttu-id="6592f-105">Après avoir séquencé une application, celle-ci peut être exécutée à partir d’un serveur App-V pour cibler les ordinateurs qui exécutent le client de bureau App-v ou le client App-V pour les services Bureau à distance (auparavant services Terminal Server) à l’aide d’un processus appelé streaming.</span><span class="sxs-lookup"><span data-stu-id="6592f-105">After an application has been sequenced, it can run from an App-V Server to target computers that are running the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using a process called streaming.</span></span> <span data-ttu-id="6592f-106">Le Sequencer App-V analyse le processus d’installation et de configuration des applications, et enregistre toutes les informations nécessaires à l’exécution de l’application dans l’environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="6592f-106">The App-V Sequencer monitors the installation and setup process for applications, and it records all the information necessary for the application to run in the virtual environment.</span></span> <span data-ttu-id="6592f-107">Ce processus détermine également les fichiers et configurations applicables à tous les utilisateurs et aux configurations que les utilisateurs peuvent personnaliser.</span><span class="sxs-lookup"><span data-stu-id="6592f-107">This process also determines which files and configurations are applicable to all users and which configurations users can customize.</span></span> <span data-ttu-id="6592f-108">Les applications virtuelles s’exécutent sur des ordinateurs cibles et n’ont aucun effet sur le système d’exploitation exécuté sur l’ordinateur cible ou sur toutes les applications installées sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="6592f-108">Virtual applications run on target computers and have no effect on the operating system running on the target computer or on any applications that are installed on the target computer.</span></span>

## <span data-ttu-id="6592f-109">Considérations en matière de sécurité du séquenceur d’applications</span><span class="sxs-lookup"><span data-stu-id="6592f-109">Application Virtualization Sequencer Security Considerations</span></span>


<span data-ttu-id="6592f-110">Le Sequencer App-V exécute tous les services détectés au moment du séquençage à l’aide du compte système local et n’applique pas les descripteurs de sécurité sur les demandes de contrôle de service.</span><span class="sxs-lookup"><span data-stu-id="6592f-110">The App-V Sequencer runs all services detected at sequencing time using the Local System account and does not enforce security descriptors on service control requests.</span></span> <span data-ttu-id="6592f-111">Si le service a été installé à l’aide d’un autre compte d’utilisateur ou si les descripteurs de sécurité sont destinés à accorder des autorisations de service spécifiques à différents groupes d’utilisateurs, Déterminez soigneusement si le service doit être virtualisé.</span><span class="sxs-lookup"><span data-stu-id="6592f-111">If the service was installed using a different user account or if the security descriptors are intended to grant different user groups specific service permissions, consider carefully whether the service should be virtualized.</span></span> <span data-ttu-id="6592f-112">Dans certains cas, vous devez installer le service localement pour vous assurer que la sécurité de service prévue est préservée.</span><span class="sxs-lookup"><span data-stu-id="6592f-112">In some cases, you should install the service locally to ensure that the intended service security is preserved.</span></span>

## <span data-ttu-id="6592f-113">Options de menu de la console de numérotation des applications</span><span class="sxs-lookup"><span data-stu-id="6592f-113">Application Virtualization Sequencer Console Menu Options</span></span>


<span data-ttu-id="6592f-114">Les éléments de menu suivants sont disponibles dans la console App-V du Sequencer:</span><span class="sxs-lookup"><span data-stu-id="6592f-114">The following menu items are available in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="6592f-115">**Fichier**: contient différentes commandes pour vous permettre de créer, d’ouvrir, de modifier et d’enregistrer des applications séquencées.</span><span class="sxs-lookup"><span data-stu-id="6592f-115">**File**—Contains various commands to help create, open, modify, and save sequenced applications.</span></span>

-   <span data-ttu-id="6592f-116">**Edit**: contient différentes commandes permettant de modifier des applications virtuelles existantes.</span><span class="sxs-lookup"><span data-stu-id="6592f-116">**Edit**—Contains various commands for editing existing virtual applications.</span></span>

-   <span data-ttu-id="6592f-117">**Affichage**: contient diverses commandes permettant d’afficher les propriétés d’une application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="6592f-117">**View**—Contains various commands for viewing properties of a virtual application.</span></span>

-   <span data-ttu-id="6592f-118">**Outils**— contient différents outils et diagnostics pour la configuration des applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="6592f-118">**Tools**—Contains various tools and diagnostics for configuring virtual applications.</span></span>

## <span data-ttu-id="6592f-119">Options de la barre d’outils de la barre de la console Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="6592f-119">Application Virtualization Sequencer Console Toolbar Options</span></span>


<span data-ttu-id="6592f-120">Les boutons de la barre d’outils suivants sont disponibles dans la console App-V du Sequencer:</span><span class="sxs-lookup"><span data-stu-id="6592f-120">The following toolbar buttons are available in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="6592f-121">**Nouveau package**: cliquez sur pour créer une application séquencée.</span><span class="sxs-lookup"><span data-stu-id="6592f-121">**New Package**—Click to create a new sequenced application.</span></span>

-   <span data-ttu-id="6592f-122">**Ouvrir**: cliquez pour ouvrir un package d’application séquencé dans la console de Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="6592f-122">**Open**—Click to open a sequenced application package in the App-V Sequencer Console.</span></span>

-   <span data-ttu-id="6592f-123">**Ouvrir pour la mise à niveau**: cliquez sur pour ouvrir une application séquencée afin de mettre à niveau ou d’appliquer une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="6592f-123">**Open for Upgrade**—Click to open a sequenced application to upgrade or apply an update.</span></span>

-   <span data-ttu-id="6592f-124">**Enregistrer**: cliquez sur pour enregistrer une application virtuelle séquencée.</span><span class="sxs-lookup"><span data-stu-id="6592f-124">**Save**—Click to save a sequenced virtual application.</span></span>

-   <span data-ttu-id="6592f-125">**Assistant de séquençage**: cliquez sur pour ouvrir l’Assistant séquençage.</span><span class="sxs-lookup"><span data-stu-id="6592f-125">**Sequencing Wizard**—Click to open the Sequencing Wizard.</span></span> <span data-ttu-id="6592f-126">Utilisez ce bouton pour démarrer l’Assistant séquençage si vous apportez des modifications sous l’onglet **général** , sous options **Outils**  /  **Options**.</span><span class="sxs-lookup"><span data-stu-id="6592f-126">You should use this button to start the Sequencing Wizard if you make any changes on the **General** tab under **Tools** / **Options**.</span></span>

## <span data-ttu-id="6592f-127">Onglets des applications virtuelles</span><span class="sxs-lookup"><span data-stu-id="6592f-127">Virtual Application Tabs</span></span>


<span data-ttu-id="6592f-128">Les onglets suivants sont affichés lors de l’affichage d’une application virtuelle dans la console de Sequencer App-V:</span><span class="sxs-lookup"><span data-stu-id="6592f-128">The following tabs are displayed when you view a virtual application in the App-V Sequencer Console:</span></span>

-   <span data-ttu-id="6592f-129">**Propriétés**: affiche des informations sur l’application virtuelle sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="6592f-129">**Properties**—Displays information about the selected virtual application.</span></span> <span data-ttu-id="6592f-130">Vous pouvez mettre à jour le **nom du package** et les **Commentaires** associés à l’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="6592f-130">You can update the **Package Name** and **Comments** associated with the virtual application.</span></span>

-   <span data-ttu-id="6592f-131">**Déploiement**: affiche des informations sur la façon dont l’application virtuelle est accessible par les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="6592f-131">**Deployment**—Displays information about how the virtual application will be accessed by target computers.</span></span> <span data-ttu-id="6592f-132">Vous pouvez configurer la méthode de remise des applications virtuelles et vous pouvez configurer les systèmes d’exploitation qui doivent s’exécuter sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="6592f-132">You can configure the virtual application delivery method, and you can configure which operating systems must be running on the target computer.</span></span> <span data-ttu-id="6592f-133">Vous pouvez également configurer les options de sortie associées.</span><span class="sxs-lookup"><span data-stu-id="6592f-133">You can also configure the associated output options.</span></span> <span data-ttu-id="6592f-134">Si vous envisagez de demander aux clients d’accéder à une application virtuelle à partir d’un fichier, utilisez le format suivant lorsque vous spécifiez le chemin d’accès: **file://Server/Share/Path/.SFT**.</span><span class="sxs-lookup"><span data-stu-id="6592f-134">If you plan to have clients access a virtual application from a file, use the following format when specifying the path: **File://server/share/path/.sft**.</span></span> <span data-ttu-id="6592f-135">Activez l’option **appliquer les descripteurs de sécurité** afin de préserver la sécurité associée au package lors d’une mise à niveau ou les autorisations seront réinitialisées lors de la mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="6592f-135">Select **Enforce Security Descriptors** to preserve security associated with the package during an upgrade, or the permissions will be reset during the upgrade.</span></span>

-   <span data-ttu-id="6592f-136">**Historique des modifications**: affiche des informations sur les mises à jour apportées à l’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="6592f-136">**Change History**—Displays information about updates that have been made to the virtual application.</span></span>

-   <span data-ttu-id="6592f-137">**Fichiers**: affiche les fichiers associés à l’application virtuelle sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="6592f-137">**Files**—Displays the files associated with the selected virtual application.</span></span> <span data-ttu-id="6592f-138">Vous pouvez effectuer des révisions secondaires des propriétés de fichier associées en utilisant les champs appropriés.</span><span class="sxs-lookup"><span data-stu-id="6592f-138">You can make minor revisions to the associated file properties by using the appropriate fields.</span></span>

-   <span data-ttu-id="6592f-139">**Registre virtuel**: affiche le registre virtuel associé à l’application virtuelle sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="6592f-139">**Virtual Registry**—Displays the virtual registry associated with the selected virtual application.</span></span> <span data-ttu-id="6592f-140">Vous pouvez ajouter ou supprimer des clés de registre en cliquant avec le bouton droit sur l’entrée appropriée.</span><span class="sxs-lookup"><span data-stu-id="6592f-140">You can add or delete registry keys by right-clicking the appropriate entry.</span></span>

-   <span data-ttu-id="6592f-141">**Système de fichiers virtuel**: affiche les systèmes de fichiers virtuels associés à l’application virtuelle sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="6592f-141">**Virtual File System**—Displays the virtual file systems associated with the selected virtual application.</span></span> <span data-ttu-id="6592f-142">Vous pouvez ajouter, supprimer ou modifier des entrées dans le système de fichiers dans cet onglet en cliquant avec le bouton droit sur l’entrée appropriée et en sélectionnant l’option.</span><span class="sxs-lookup"><span data-stu-id="6592f-142">You can add, delete, or edit file system entries on this tab by right-clicking the appropriate entry and selecting the option.</span></span>

-   <span data-ttu-id="6592f-143">**Services virtuels**: affiche les services associés à l’application virtuelle sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="6592f-143">**Virtual Services**—Displays the services associated with the selected virtual application.</span></span>

-   <span data-ttu-id="6592f-144">**OSD**: affiche les informations relatives à l’ouverture de l’OSD (Open Software Descriptor) associée à l’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="6592f-144">**OSD**—Displays information about the Open Software Descriptor (OSD) associated with the virtual application.</span></span> <span data-ttu-id="6592f-145">Vous pouvez mettre à jour les fichiers associés au fichier OSD en cliquant avec le bouton droit sur l’entrée appropriée et en sélectionnant l’action souhaitée.</span><span class="sxs-lookup"><span data-stu-id="6592f-145">You can update the files associated with the OSD file by right-clicking the appropriate entry and selecting the action that you want.</span></span>

## <span data-ttu-id="6592f-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6592f-146">Related topics</span></span>


[<span data-ttu-id="6592f-147">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="6592f-147">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





