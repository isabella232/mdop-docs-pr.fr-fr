---
title: Planification du déploiement d'Application Virtualization Client
description: Planification du déploiement d'Application Virtualization Client
author: dansimp
ms.assetid: a352f80f-f0f9-4fbf-ac10-24c510b2d6be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c9fc4f29020af83a8606827015947e78761f4d7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806513"
---
# <span data-ttu-id="6501c-103">Planification du déploiement d'Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="6501c-103">Planning for Application Virtualization Client Deployment</span></span>


<span data-ttu-id="6501c-104">Une fois que vous avez décidé du mode de publication et de déploiement des packages d’application virtuels sur les ordinateurs des utilisateurs finaux, vous devez planifier le déploiement du logiciel client de virtualisation d’applications.</span><span class="sxs-lookup"><span data-stu-id="6501c-104">After you have decided how you will publish and deploy virtual application packages to your end user computers, you should plan the deployment of the Application Virtualization Client software.</span></span>

<span data-ttu-id="6501c-105">Le client de virtualisation des applications est le composant qui exécute réellement les applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="6501c-105">The Application Virtualization Client is the component that actually runs the virtual applications.</span></span> <span data-ttu-id="6501c-106">Le client de virtualisation des applications permet aux utilisateurs d’interagir avec des icônes et de double-cliquer sur les types de fichiers pour démarrer une application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="6501c-106">The Application Virtualization Client enables users to interact with icons and to double-click file types to start a virtual application.</span></span> <span data-ttu-id="6501c-107">Il gère également la diffusion en continu du contenu de l’application à partir d’un serveur en flux continu et la cache avant de démarrer l’application.</span><span class="sxs-lookup"><span data-stu-id="6501c-107">It also handles streaming of the application content from a streaming server and caches it before starting the application.</span></span> <span data-ttu-id="6501c-108">Le contenu de l’application est structuré de telle sorte que tout le contenu nécessaire au démarrage de l’application et le traitement de l’interaction utilisateur initiale soient transmis d’abord à l’ordinateur de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="6501c-108">The application content is structured such that all the content needed to start the application and handle initial user interaction is streamed to the end user computer first.</span></span> <span data-ttu-id="6501c-109">Il existe deux types différents de logiciels de client de virtualisation d’application: le client de virtualisation d’application pour les services Bureau à distance (anciennement services Terminal Server), qui est utilisé sur les systèmes serveur du serveur hôte de bureau RDSession, et le client de bureau de virtualisation des applications, qui est utilisé pour tous les autres ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="6501c-109">There are two different types of Application Virtualization Client software: the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services), which is used on Remote Desktop Session Host (RDSession Host) server systems, and the Application Virtualization Desktop Client, which is used for all other computers.</span></span>

<span data-ttu-id="6501c-110">Le client de virtualisation des applications doit être configuré au moment de l’installation, soit dans la console de gestion de l’application, soit via la ligne de commande du programme d’installation, avec un certain nombre de paramètres importants, dont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="6501c-110">The Application Virtualization Client should be configured at installation time, either in the Application Virtualization Management Console or via the installer command line, with a number of important settings, including the following:</span></span>

-   <span data-ttu-id="6501c-111">Emplacements des icônes pour toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="6501c-111">Locations of the icons for all the applications.</span></span>

-   <span data-ttu-id="6501c-112">Emplacement du fichier OSD qui contient les informations de définition du package.</span><span class="sxs-lookup"><span data-stu-id="6501c-112">The location of the OSD file that contains the package definition information.</span></span>

-   <span data-ttu-id="6501c-113">Source de contenu de l’application.</span><span class="sxs-lookup"><span data-stu-id="6501c-113">The application content source.</span></span>

-   <span data-ttu-id="6501c-114">Protocole de communication à utiliser pour récupérer les éléments précédents.</span><span class="sxs-lookup"><span data-stu-id="6501c-114">The communications protocol to be used when retrieving the preceding items.</span></span>

-   <span data-ttu-id="6501c-115">La taille de cache et la méthode de gestion de la taille de cache à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6501c-115">The cache size and cache size management method to be used.</span></span>

<span data-ttu-id="6501c-116">Pour promouvoir le déploiement du logiciel client de virtualisation des applications lors de l’utilisation d’une solution de distribution de logiciel électronique (ESD), les paramètres précédents doivent être définis à l’avance.</span><span class="sxs-lookup"><span data-stu-id="6501c-116">To expedite the deployment of the Application Virtualization Client software when using an electronic software distribution (ESD) solution, the preceding settings must be defined carefully in advance.</span></span> <span data-ttu-id="6501c-117">C’est particulièrement important lorsque vous disposez d’ordinateurs dans différents bureaux et que leurs clients doivent être configurés de manière à utiliser des emplacements sources différents.</span><span class="sxs-lookup"><span data-stu-id="6501c-117">This is especially important when you have computers in different offices, where their clients would need to be configured to use different source locations.</span></span>

**<span data-ttu-id="6501c-118">Remarque</span><span class="sxs-lookup"><span data-stu-id="6501c-118">Note</span></span>**  
-   <span data-ttu-id="6501c-119">L’emplacement de l’icône et les valeurs du fichier OSD sont un facteur important à prendre en considération lors du choix de votre méthode de publication, que vous utilisiez Windows Installer ou SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="6501c-119">The icon location and OSD file values are an important factor to consider when choosing your publishing method, whether using Windows Installer or SFTMIME.</span></span> <span data-ttu-id="6501c-120">Le paramètre de la source de contenu de l’application est défini par votre choix de méthode de streaming.</span><span class="sxs-lookup"><span data-stu-id="6501c-120">The setting for the application content source is defined by your choice of streaming method.</span></span>

-   <span data-ttu-id="6501c-121">Pour vous assurer que le cache dispose de suffisamment d’espace alloué pour tous les packages qui peuvent être déployés, utilisez le paramètre **utiliser le seuil d’espace disque libre** lorsque vous configurez le client de manière à ce que le cache puisse augmenter selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="6501c-121">To ensure that the cache has sufficient space allocated for all packages that might be deployed, use the **Use free disk space threshold** setting when you configure the client so that the cache can grow as needed.</span></span> <span data-ttu-id="6501c-122">Par ailleurs, vous pouvez déterminer à l’avance la quantité d’espace disque nécessaire pour le cache de l’application V et au moment de l’installation, définir la taille de cache en conséquence.</span><span class="sxs-lookup"><span data-stu-id="6501c-122">Alternatively, determine in advance how much disk space will be needed for the App-V cache, and at installation time, set the cache size accordingly.</span></span> <span data-ttu-id="6501c-123">Pour plus d’informations sur la fonctionnalité de gestion de l’espace dans le cache, voir **comment utiliser la fonctionnalité de gestion de l’espace** dans le cache du Guide des opérations de Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="6501c-123">For more information about the cache space management feature, see **How to Use the Cache Space Management Feature** in the Microsoft Application Virtualization (App-V) Operations Guide.</span></span>

-   <span data-ttu-id="6501c-124">Au cours des opérations de diffusion en continu de publication et HTTP (S), les clients App-V 4,5 SP1 utilisent les paramètres du serveur proxy configurés dans Internet Explorer sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6501c-124">During both the publishing and HTTP(S) streaming operations,App-V 4.5 SP1 clients use the proxy server settings that are configured in Internet Explorer on the user’s computer.</span></span>

<span data-ttu-id="6501c-125">Pour plus d’informations sur la configuration des paramètres d’installation du client, voir [paramètres de ligne de commande du programme de virtualisation des applications](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6501c-125">For more information about configuring the client installation parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

 

<span data-ttu-id="6501c-126">Enfin, vous devez déterminer le mode de déploiement du logiciel client de bureau Virtualization pour les clients de bureau.</span><span class="sxs-lookup"><span data-stu-id="6501c-126">Finally, you need to determine how to deploy the Application Virtualization Desktop Client software for the desktop clients.</span></span> <span data-ttu-id="6501c-127">Même s’il est possible de déployer manuellement le client de bureau de virtualisation d’application sur chaque ordinateur, la plupart des organisations doivent procéder par le biais d’un processus automatisé.</span><span class="sxs-lookup"><span data-stu-id="6501c-127">Although it is possible to deploy the Application Virtualization Desktop Client manually on each computer, most organizations would need to do this through some automated process.</span></span> <span data-ttu-id="6501c-128">Dans le cas d’une entreprise moyenne ou de grande taille, il est possible qu’elle ait un système ESD et qu’il s’agissait d’une méthode idéale pour déployer le client.</span><span class="sxs-lookup"><span data-stu-id="6501c-128">A medium or large organization might have an ESD system in operation, and that would be an ideal way to deploy the client.</span></span> <span data-ttu-id="6501c-129">S’il n’existe aucun système ESD, vous pouvez utiliser votre méthode standard d’installation de logiciels au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6501c-129">If no ESD system exists, you can use your standard method of installing software in your organization.</span></span> <span data-ttu-id="6501c-130">Les choix incluent une stratégie de groupe ou différentes techniques de script.</span><span class="sxs-lookup"><span data-stu-id="6501c-130">Choices include Group Policy or various scripting techniques.</span></span> <span data-ttu-id="6501c-131">Selon le nombre et la taille des bureaux dont vous disposez, ce processus de déploiement peut être complexe, et il est essentiel de prendre une approche structurée pour garantir que tous les ordinateurs obtiennent un client avec la configuration correcte.</span><span class="sxs-lookup"><span data-stu-id="6501c-131">Depending on the number and size of the offices you have, this deployment process can be complex, and it is essential that you take a structured approach to ensure all computers get a client installed with the correct configuration.</span></span>

## <span data-ttu-id="6501c-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6501c-132">Related topics</span></span>


[<span data-ttu-id="6501c-133">Planification du déploiement du système Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="6501c-133">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

[<span data-ttu-id="6501c-134">Procédure pour installer le client via la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="6501c-134">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

[<span data-ttu-id="6501c-135">Procédure pour publier une application virtuelle sur le client</span><span class="sxs-lookup"><span data-stu-id="6501c-135">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="6501c-136">Procédure pour mettre à niveau Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="6501c-136">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)

[<span data-ttu-id="6501c-137">Procédure pour désinstaller App-V Client</span><span class="sxs-lookup"><span data-stu-id="6501c-137">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)

 

 





