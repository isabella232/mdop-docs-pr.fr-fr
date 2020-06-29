---
title: À propos d'Application Virtualization Sequencer
description: À propos d'Application Virtualization Sequencer
author: dansimp
ms.assetid: bee193ca-58bd-40c9-b41a-310435633895
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83709bcceabe3312fba34512b47d28a24b4dc52c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808130"
---
# <span data-ttu-id="200dc-103">À propos d'Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="200dc-103">About the Application Virtualization Sequencer</span></span>


<span data-ttu-id="200dc-104">Le Sequencer Microsoft Application Virtualization (App-V) vérifie et enregistre tous les processus d’installation et de configuration pour une application et crée les fichiers suivants: **ico**, **OSD**, **SFT**et **SPRJ**.</span><span class="sxs-lookup"><span data-stu-id="200dc-104">The Microsoft Application Virtualization (App-V) Sequencer monitors and records all installation and setup processes for an application and creates the following files: **ICO**, **OSD**, **SFT**, and **SPRJ**.</span></span> <span data-ttu-id="200dc-105">Ces fichiers contiennent toutes les informations nécessaires sur une application afin que l’application puisse s’exécuter dans un environnement virtuel sur des ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="200dc-105">These files contain all the necessary information about an application so the application can run in a virtual environment on target computers.</span></span> <span data-ttu-id="200dc-106">Vous pouvez utiliser le Sequencer Microsoft Application Virtualization (App-V) pour créer des applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="200dc-106">You can use the Microsoft Application Virtualization (App-V) Sequencer to create virtual applications.</span></span> <span data-ttu-id="200dc-107">Après avoir séquencé une application, celle-ci peut être diffusée sur des ordinateurs cibles, ou les ordinateurs cibles peuvent exécuter l’application virtuelle en téléchargeant le contenu du package d’application virtuelle et en exécutant l’application localement.</span><span class="sxs-lookup"><span data-stu-id="200dc-107">After you sequence an application, it can be streamed to target computers, or target computers can run the virtual application by downloading the contents of the virtual application package and running the application locally.</span></span>

<span data-ttu-id="200dc-108">**Important**  Pour exécuter un package d’application virtuelle, l’ordinateur cible doit exécuter la version appropriée du client App-V.</span><span class="sxs-lookup"><span data-stu-id="200dc-108">**Important** To run a virtual application package the target computer must be running the appropriate version of the App-V client.</span></span>

 

<span data-ttu-id="200dc-109">Les packages d’applications virtuelles s’exécutent sur des ordinateurs cibles sans interagir avec le système d’exploitation sous-jacent sur l’ordinateur cible, car chaque application s’exécute dans un environnement virtuel et est isolé d’autres applications installées ou exécutées sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="200dc-109">Virtual application packages run on target computers without interacting with the underlying operating system on the target computer because each application runs in a virtual environment and is isolated from other applications that are installed or running on the target computer.</span></span> <span data-ttu-id="200dc-110">Cette isolation peut réduire les conflits d’application et permettre de réduire le nombre d’applications de test avant déploiement nécessaires.</span><span class="sxs-lookup"><span data-stu-id="200dc-110">This isolation can reduce application conflicts and can help decrease the required amount of application pre-deployment testing.</span></span>

## <span data-ttu-id="200dc-111">Terminologie de Sequencer</span><span class="sxs-lookup"><span data-stu-id="200dc-111">Sequencer Terminology</span></span>


<a href="" id="application-virtualization-drive"></a><span data-ttu-id="200dc-112">Lecteur de virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="200dc-112">Application Virtualization drive</span></span>  
<span data-ttu-id="200dc-113">Le lecteur d’applications virtuelles est le lecteur par défaut (Q:\) de l’ordinateur cible à partir duquel les applications séquencées sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="200dc-113">The application virtualization drive is the default drive (Q:\) on the target computer from which sequenced applications are run.</span></span>

<a href="" id="ico-file"></a><span data-ttu-id="200dc-114">Fichier ICO</span><span class="sxs-lookup"><span data-stu-id="200dc-114">ICO file</span></span>  
<span data-ttu-id="200dc-115">Fichier d’icône sur le Bureau du client utilisé pour lancer une application séquencée.</span><span class="sxs-lookup"><span data-stu-id="200dc-115">The icon file on the client desktop which is used to launch a sequenced application.</span></span>

<a href="" id="installation-directory"></a><span data-ttu-id="200dc-116">Répertoire d’installation</span><span class="sxs-lookup"><span data-stu-id="200dc-116">Installation directory</span></span>  
<span data-ttu-id="200dc-117">Répertoire utilisé par le Sequencer pour placer les fichiers d’installation lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="200dc-117">The directory used by the sequencer to place installation files during setup.</span></span>

<a href="" id="open-software-descriptor--osd--file"></a><span data-ttu-id="200dc-118">Ouvrir un fichier d’OSD (Open Software Descriptor)</span><span class="sxs-lookup"><span data-stu-id="200dc-118">Open Software Descriptor (OSD) file</span></span>  
<span data-ttu-id="200dc-119">Fichier XML demandant au client App-V de récupérer l’application séquencée à partir du serveur de streaming App-V et l’exécution de l’application séquencée dans l’environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="200dc-119">An XML-based file that instructs the App-V client how to retrieve the sequenced application from the App-V streaming server and how to run the sequenced application in the virtual environment.</span></span>

<a href="" id="package-root-directory"></a><span data-ttu-id="200dc-120">Répertoire racine du package</span><span class="sxs-lookup"><span data-stu-id="200dc-120">Package root directory</span></span>  
<span data-ttu-id="200dc-121">Le répertoire sur l’ordinateur de séquençage sur lequel sont installés les fichiers pour le package d’application séquencé.</span><span class="sxs-lookup"><span data-stu-id="200dc-121">The directory on the sequencing computer on which files for the sequenced application package are installed.</span></span> <span data-ttu-id="200dc-122">Ce répertoire existe également virtuellement sur l’ordinateur sur lequel une application séquencée sera diffusée.</span><span class="sxs-lookup"><span data-stu-id="200dc-122">This directory also exists virtually on the computer to which a sequenced application will be streamed.</span></span>

<a href="" id="sequenced-application"></a><span data-ttu-id="200dc-123">Application séquencée</span><span class="sxs-lookup"><span data-stu-id="200dc-123">Sequenced application</span></span>  
<span data-ttu-id="200dc-124">Application surveillée par le Sequencer, réparties dans des blocs de fonctionnalités principaux et secondaires, diffusées sur un ordinateur cible exécutant le client App-V et exécutant un environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="200dc-124">An application that has been monitored by the sequencer, broken up into primary and secondary feature blocks, streamed to a target computer running the App-V client t, and runs a virtual environment.</span></span>

<a href="" id="sequenced-application-package"></a><span data-ttu-id="200dc-125">Package d’application séquencé</span><span class="sxs-lookup"><span data-stu-id="200dc-125">Sequenced application package</span></span>  
<span data-ttu-id="200dc-126">Fichiers comprenant une application virtuelle et autorisant l’exécution d’une application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="200dc-126">The files that comprise a virtual application and allow a virtual application to run.</span></span> <span data-ttu-id="200dc-127">Ces fichiers sont créés après le séquençage et incluent spécifiquement les fichiers **. OSD**, **. SFT**, **. sprj**et **. ico** .</span><span class="sxs-lookup"><span data-stu-id="200dc-127">These files are created after sequencing and specifically include **.osd**, **.sft**, **.sprj**, and **.ico** files.</span></span>

<a href="" id="sequencing"></a><span data-ttu-id="200dc-128">Séquençage</span><span class="sxs-lookup"><span data-stu-id="200dc-128">Sequencing</span></span>  
<span data-ttu-id="200dc-129">Processus de création d’un package d’application à l’aide du Sequencer App-V.</span><span class="sxs-lookup"><span data-stu-id="200dc-129">The process of creating an application package using the App-V Sequencer.</span></span> <span data-ttu-id="200dc-130">Dans ce processus, une application est surveillée, ses raccourcis sont configurés et un package d’application séquencé est créé.</span><span class="sxs-lookup"><span data-stu-id="200dc-130">In this process, an application is monitored, its shortcuts are configured, and a sequenced application package is created.</span></span>

<a href="" id="sequencing-computer"></a><span data-ttu-id="200dc-131">Séquençage d’un ordinateur</span><span class="sxs-lookup"><span data-stu-id="200dc-131">Sequencing computer</span></span>  
<span data-ttu-id="200dc-132">Ordinateur utilisé pour séquencer une application.</span><span class="sxs-lookup"><span data-stu-id="200dc-132">The computer used to sequence an application.</span></span>

<a href="" id="virtual-application"></a><span data-ttu-id="200dc-133">Application virtuelle</span><span class="sxs-lookup"><span data-stu-id="200dc-133">Virtual application</span></span>  
<span data-ttu-id="200dc-134">Application empaquetée par le Sequencer pour s’exécuter dans un environnement virtuel autonome.</span><span class="sxs-lookup"><span data-stu-id="200dc-134">An application packaged by the Sequencer to run in a self-contained, virtual environment.</span></span> <span data-ttu-id="200dc-135">L’environnement virtuel contient les informations nécessaires à l’exécution de l’application sur le client sans installer l’application localement.</span><span class="sxs-lookup"><span data-stu-id="200dc-135">The virtual environment contains the information necessary to run the application on the client without installing the application locally.</span></span>

<a href="" id="primary-feature-block"></a><span data-ttu-id="200dc-136">Bloc de fonctions principal</span><span class="sxs-lookup"><span data-stu-id="200dc-136">Primary feature block</span></span>  
<span data-ttu-id="200dc-137">Le contenu minimal d’un package d’application virtuel qui est nécessaire pour qu’une application s’exécute sur un ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="200dc-137">The minimum content in a virtual application package that is necessary for an application to run on a target computer.</span></span> <span data-ttu-id="200dc-138">Le contenu du bloc de fonctionnalité principal est identifié lors de la phase d’application du séquençage et se compose généralement du contenu des fonctionnalités d’application les plus utilisées.</span><span class="sxs-lookup"><span data-stu-id="200dc-138">The content in the primary feature block is identified during the application phase of sequencing and typically consists of the content for the most used application features.</span></span>

## <a href="" id="sequencing-applications-"></a><span data-ttu-id="200dc-139">Séquençage des applications</span><span class="sxs-lookup"><span data-stu-id="200dc-139">Sequencing Applications</span></span>


<span data-ttu-id="200dc-140">Il existe deux méthodes pour créer et modifier des packages d’application virtuels dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="200dc-140">There are two methods to create and modify virtual application packages in your environment.</span></span> <span data-ttu-id="200dc-141">La première méthode consiste à utiliser l’Assistant **séquençage** .</span><span class="sxs-lookup"><span data-stu-id="200dc-141">The first method is by using the **Sequencing** wizard.</span></span> <span data-ttu-id="200dc-142">L’Assistant **séquençage** vous permet de créer de nouveaux packages d’applications virtuelles ou de modifier ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="200dc-142">The **Sequencing** wizard allows you to create new, or modify existing virtual application packages.</span></span> <span data-ttu-id="200dc-143">Pour plus d’informations sur l’utilisation de l’Assistant **séquençage** , voir [Comment séquencer une nouvelle application](how-to-sequence-a-new-application.md).</span><span class="sxs-lookup"><span data-stu-id="200dc-143">For more information about using the **Sequencing** wizard see, [How to Sequence a New Application](how-to-sequence-a-new-application.md).</span></span> <span data-ttu-id="200dc-144">La deuxième méthode consiste à utiliser la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="200dc-144">The second method is by using the command-line.</span></span> <span data-ttu-id="200dc-145">La ligne de commande vous permet de créer de nouveaux packages d’applications virtuelles ou de modifier ceux-ci à l’aide de l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="200dc-145">The command-line allows you to create new, or modify existing virtual application packages using the command prompt.</span></span> <span data-ttu-id="200dc-146">Pour plus d’informations sur l’utilisation de la ligne de commande, voir [Comment gérer des applications virtuelles à l’aide de la ligne de commande](how-to-manage-virtual-applications-using-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="200dc-146">For more information about using the command line see, [How to Manage Virtual Applications Using the Command Line](how-to-manage-virtual-applications-using-the-command-line.md).</span></span>

<span data-ttu-id="200dc-147">L’Assistant **séquençage** fournit les fonctions suivantes pour créer des packages d’applications virtuelles:</span><span class="sxs-lookup"><span data-stu-id="200dc-147">The **Sequencing** wizard provides the following functions for creating virtual application packages:</span></span>

1.  <span data-ttu-id="200dc-148">**Configuration du package**: l’Assistant de **séquençage** invite à entrer les informations de configuration de package nécessaires pour compléter le fichier d’affichage de description du logiciel (OSD) ouvert, qui est un fichier requis pour le démarrage d’un package d’application séquencé.</span><span class="sxs-lookup"><span data-stu-id="200dc-148">**Package Configuration**: The **Sequencing** Wizard prompts for package configuration information necessary to complete the Open Software Descriptor (OSD) file, which is a required file for starting a sequenced application package.</span></span>

2.  <span data-ttu-id="200dc-149">**Installation**de l’application: l’Assistant **séquençage** recueille des informations sur les configurations de démarrage et d’installation d’une application.</span><span class="sxs-lookup"><span data-stu-id="200dc-149">**Application Installation**: The **Sequencing** Wizard gathers information about an application’s installation and startup configurations.</span></span> <span data-ttu-id="200dc-150">Il surveille et enregistre les informations d’installation et de démarrage associées à l’application afin de créer les fichiers nécessaires à la création d’un package d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="200dc-150">It monitors and records the installation and startup information associated with the application to create the files necessary for a virtual application package.</span></span>

3.  <span data-ttu-id="200dc-151">**Démarrage**de l’application: l’Assistant **séquençage** recueille des informations pour compiler et commander les blocs de code nécessaires à l’exécution initiale du package d’application séquencé sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="200dc-151">**Application Startup**: The **Sequencing** Wizard gathers information for compiling and ordering the blocks of code necessary to perform the initial startup of the sequenced application package on the target computer.</span></span> <span data-ttu-id="200dc-152">Le bloc de code de compilation est appelé bloc de fonctionnalité principal.</span><span class="sxs-lookup"><span data-stu-id="200dc-152">The compilation of the code block is referred to as the primary feature block.</span></span>

## <span data-ttu-id="200dc-153">Considérations en matière de sécurité du séquenceur d’applications</span><span class="sxs-lookup"><span data-stu-id="200dc-153">Application Virtualization Sequencer Security Considerations</span></span>


<span data-ttu-id="200dc-154">Le Sequencer App-V exécute tous les services détectés au moment du séquençage à l’aide du compte système local et n’applique pas les descripteurs de sécurité sur les demandes de contrôle de service.</span><span class="sxs-lookup"><span data-stu-id="200dc-154">The App-V Sequencer runs all services detected at sequencing time using the Local System account and does not enforce security descriptors on service control requests.</span></span> <span data-ttu-id="200dc-155">Si le service a été installé à l’aide d’un autre compte d’utilisateur ou si les descripteurs de sécurité sont destinés à accorder des autorisations de service spécifiques à différents groupes d’utilisateurs, Déterminez soigneusement si le service doit être virtualisé.</span><span class="sxs-lookup"><span data-stu-id="200dc-155">If the service was installed using a different user account or if the security descriptors are intended to grant different user groups specific service permissions, consider carefully whether the service should be virtualized.</span></span> <span data-ttu-id="200dc-156">Dans certains cas, vous devez installer le service localement pour vous assurer que la sécurité de service prévue est préservée.</span><span class="sxs-lookup"><span data-stu-id="200dc-156">In some cases, you should install the service locally to ensure that the intended service security is preserved.</span></span>

<span data-ttu-id="200dc-157">**Important**  Vous devez toujours enregistrer les packages d’application virtuels dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="200dc-157">**Important** You should always save virtual application packages in a secure location.</span></span>

 

## <span data-ttu-id="200dc-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="200dc-158">Related topics</span></span>


[<span data-ttu-id="200dc-159">Vue d'ensemble d'Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="200dc-159">Application Virtualization Sequencer Overview</span></span>](application-virtualization-sequencer-overview.md)

 

 





