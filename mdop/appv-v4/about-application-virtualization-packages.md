---
title: À propos des packages Application Virtualization
description: À propos des packages Application Virtualization
author: dansimp
ms.assetid: 69bd35c1-7af3-43db-931b-3074780aa926
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfe6df90881ea4179fa8cd224609ca6d28ff5f61
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808165"
---
# <span data-ttu-id="88b0b-103">À propos des packages Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="88b0b-103">About Application Virtualization Packages</span></span>


<span data-ttu-id="88b0b-104">Dans la virtualisation des applications, un *package* est la sortie du processus de séquençage.</span><span class="sxs-lookup"><span data-stu-id="88b0b-104">In Application Virtualization, a *package* is the output of the sequencing process.</span></span> <span data-ttu-id="88b0b-105">Vous utilisez des packages lorsque vous déployez d’abord des applications sur vos serveurs et que vous effectuez une mise à niveau d’applications avec une nouvelle version.</span><span class="sxs-lookup"><span data-stu-id="88b0b-105">You use packages when you first deploy applications on your servers and when you upgrade applications with a new version.</span></span> <span data-ttu-id="88b0b-106">Les packages vous permettent de contrôler les versions d’applications virtuelles sur les serveurs de gestion de la virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="88b0b-106">Packages enable you to control virtual application versions on your Application Virtualization Management Servers.</span></span> <span data-ttu-id="88b0b-107">Un package unique peut contenir une ou plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="88b0b-107">A single package can contain one or more applications.</span></span> <span data-ttu-id="88b0b-108">Chaque package d’application contient un ensemble de fichiers sous forme d’unité autonome.</span><span class="sxs-lookup"><span data-stu-id="88b0b-108">Each application package contains a set of files as a self-contained unit.</span></span>

## <span data-ttu-id="88b0b-109">Gestion des packages</span><span class="sxs-lookup"><span data-stu-id="88b0b-109">Managing Packages</span></span>


<span data-ttu-id="88b0b-110">Une fois que le Sequencer a créé un package d’une ou plusieurs applications dans le cadre de son processus, vous pouvez copier les fichiers générés par Sequencer sur un serveur de gestion des applications et les rendre accessibles pour le streaming.</span><span class="sxs-lookup"><span data-stu-id="88b0b-110">After the Sequencer creates a package of one or more applications as part of its process, you can copy the Sequencer-generated files to a Application Virtualization Management Server and make them available for streaming.</span></span>

<span data-ttu-id="88b0b-111">Les packages disponibles apparaissent sous le conteneur **packages** dans le volet gauche de la console de gestion de l’application virtualisation.</span><span class="sxs-lookup"><span data-stu-id="88b0b-111">Available packages appear under the **Packages** container in the left pane of the Application Virtualization Management Console.</span></span> <span data-ttu-id="88b0b-112">Lorsque vous importez une application à l’aide d’un fichier de Project de séquence (SPRJ) ou d’un fichier de description de logiciel ouvert (OSD), une entrée liée apparaît dans le conteneur **packages** .</span><span class="sxs-lookup"><span data-stu-id="88b0b-112">When you import an application with a Sequencer Project (SPRJ) file or an Open Software Descriptor (OSD) file, a related entry appears in the **Packages** container.</span></span> <span data-ttu-id="88b0b-113">À partir de la console de gestion du serveur d’applications, vous pouvez ensuite déployer, mettre à niveau ou supprimer des packages et des versions de celles-ci.</span><span class="sxs-lookup"><span data-stu-id="88b0b-113">From the Application Virtualization Server Management Console, you can then deploy, upgrade, or delete packages and versions of them.</span></span>

<span data-ttu-id="88b0b-114">Chaque application virtuelle est associée à un package.</span><span class="sxs-lookup"><span data-stu-id="88b0b-114">Each virtual application has an associated package.</span></span> <span data-ttu-id="88b0b-115">Ce package inclut les fichiers suivants:</span><span class="sxs-lookup"><span data-stu-id="88b0b-115">This package includes the following files:</span></span>

-   <span data-ttu-id="88b0b-116">SFT: fichier qui transmet l’application aux clients.</span><span class="sxs-lookup"><span data-stu-id="88b0b-116">SFT—The file that streams the application to clients.</span></span>

-   <span data-ttu-id="88b0b-117">Affichage à l’écran: le fichier de descripteur de logiciel ouvert contient les informations nécessaires pour rechercher et lancer l’application.</span><span class="sxs-lookup"><span data-stu-id="88b0b-117">OSD—The Open Software Descriptor file contains the information needed to find and launch the application.</span></span>

-   <span data-ttu-id="88b0b-118">ICO: il s’agit du fichier d’icône qui représente visuellement l’application dans les interfaces utilisateur et les raccourcis.</span><span class="sxs-lookup"><span data-stu-id="88b0b-118">ICO—The icon file that visually represents the application in user interfaces and shortcuts.</span></span>

-   <span data-ttu-id="88b0b-119">SPRJ: fichier de projet de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="88b0b-119">SPRJ—The Sequencer Project file.</span></span>

<span data-ttu-id="88b0b-120">Lorsque vous importez le fichier SPRJ, toutes les applications séquencées sont disponibles pour le déploiement par défaut, mais les applications ne sont pas activées pour le streaming.</span><span class="sxs-lookup"><span data-stu-id="88b0b-120">When you import the SPRJ file, all sequenced applications are available for deployment, by default, but the applications are not enabled for streaming.</span></span> <span data-ttu-id="88b0b-121">Vous pouvez choisir de diffuser en continu tout ou partie des applications du package.</span><span class="sxs-lookup"><span data-stu-id="88b0b-121">You can choose to stream all or some of the applications in the package.</span></span> <span data-ttu-id="88b0b-122">Par exemple, si vous avez séquencé et importé Microsoft Office, vous pouvez choisir de ne pas déployer certaines applications, telles que l’Assistant enregistrer mes paramètres.</span><span class="sxs-lookup"><span data-stu-id="88b0b-122">For example, if you sequenced and imported Microsoft Office, you can choose not to deploy some applications, such as the Save My Settings Wizard.</span></span> <span data-ttu-id="88b0b-123">Dans ce cas, cliquez avec le bouton droit sur chaque application que vous voulez déployer, sélectionnez **Propriétés**, puis assurez-vous que la case **activé** est cochée (vide).</span><span class="sxs-lookup"><span data-stu-id="88b0b-123">In this case, right-click each application you want to deploy, choose **Properties**, and make sure that the **Enabled** box is cleared (blank).</span></span> <span data-ttu-id="88b0b-124">Seules les applications pour lesquelles la case **activée** est activée seront transmises aux ordinateurs clients.</span><span class="sxs-lookup"><span data-stu-id="88b0b-124">Only the applications with the **Enabled** box selected will stream to client computers.</span></span>

<span data-ttu-id="88b0b-125">Une fois que vous avez reséquencé un package et produit un nouveau fichier SFT pour la diffusion en continu, vous pouvez mettre à niveau l’ancien package de façon rapide et aisée via la console de gestion du serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="88b0b-125">After you resequence a package and produce a new SFT file for streaming, you can upgrade the old package quickly and easily through the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="88b0b-126">Le seul scénario opérationnel qui nécessite l’utilisation du nœud **packages** est le cas où vous introduisez une nouvelle version (fichier SFT) pour le package.</span><span class="sxs-lookup"><span data-stu-id="88b0b-126">The only operational scenario that requires you to use the **Packages** node is when you introduce a new version (SFT file) for the package.</span></span> <span data-ttu-id="88b0b-127">Dès lors que vous importez des applications, attribuez l’accès et des licences aux applications, et ainsi de suite, le système de virtualisation des applications effectue le suivi de ces informations au niveau du package.</span><span class="sxs-lookup"><span data-stu-id="88b0b-127">Whenever you import applications, assign access and licenses to applications, and so on, the Application Virtualization System tracks this information at the package level.</span></span> <span data-ttu-id="88b0b-128">Cela signifie que lorsque vous autorisez un utilisateur à utiliser une application, vous donnez à l’utilisateur l’autorisation d’exécuter une application quelconque dans le même package.</span><span class="sxs-lookup"><span data-stu-id="88b0b-128">This means that when you authorize a user to use an application, you are giving the user permission to run any application in the same package.</span></span>

### <span data-ttu-id="88b0b-129">Version du package</span><span class="sxs-lookup"><span data-stu-id="88b0b-129">Package Version</span></span>

<span data-ttu-id="88b0b-130">Une version de package est représentée par un fichier SFT spécifique.</span><span class="sxs-lookup"><span data-stu-id="88b0b-130">A package version is represented by a specific SFT file.</span></span> <span data-ttu-id="88b0b-131">Lorsque vous mettez à niveau un package (appliquer une mise à jour à une application ou ajouter une application à un package), vous générez un nouveau fichier SFT.</span><span class="sxs-lookup"><span data-stu-id="88b0b-131">When you upgrade a package (apply an update to an application or add an application to a package), you generate a new SFT file.</span></span> <span data-ttu-id="88b0b-132">Chaque fois que vous créez un nouveau fichier SFT, vous créez une nouvelle version de package.</span><span class="sxs-lookup"><span data-stu-id="88b0b-132">Each time you create a new SFT file, you are creating a new package version.</span></span>

<span data-ttu-id="88b0b-133">Lorsque vous importez des applications par le biais de la console de gestion du serveur d’applications, le logiciel crée automatiquement un package et une version de package s’il n’existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="88b0b-133">When you import applications through the Application Virtualization Server Management Console, the software automatically creates a package and a package version if they do not already exist.</span></span>

## <span data-ttu-id="88b0b-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="88b0b-134">Related topics</span></span>


[<span data-ttu-id="88b0b-135">À propos des applications Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="88b0b-135">About Application Virtualization Applications</span></span>](about-application-virtualization-applications.md)

[<span data-ttu-id="88b0b-136">À propos d'Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="88b0b-136">About the Application Virtualization Server Management Console</span></span>](about-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="88b0b-137">Procédure pour gérer les packages dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="88b0b-137">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





