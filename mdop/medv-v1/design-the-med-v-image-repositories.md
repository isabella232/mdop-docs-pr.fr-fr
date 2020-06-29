---
title: Concevoir les référentiel d'images MED-V
description: Concevoir les référentiel d'images MED-V
author: dansimp
ms.assetid: e153154d-2751-4990-b94d-a2d76242c15f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0c59a0dd2d1b3a78bd211c6a6353a86c77d8fc2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810061"
---
# <span data-ttu-id="7ba17-103">Concevoir les référentiel d'images MED-V</span><span class="sxs-lookup"><span data-stu-id="7ba17-103">Design the MED-V Image Repositories</span></span>


<span data-ttu-id="7ba17-104">Une fois les images MED-V créées et conditionnées, elles peuvent être stockées sur un serveur de fichiers dans n’importe quel emplacement.</span><span class="sxs-lookup"><span data-stu-id="7ba17-104">After MED-V images are created and packed, they can be stored on a file server in any location.</span></span> <span data-ttu-id="7ba17-105">Les fichiers sont envoyés sur HTTP ou HTTPs par un ou plusieurs serveurs IIS.</span><span class="sxs-lookup"><span data-stu-id="7ba17-105">The files may be sent over HTTP or HTTPS by one or more IIS servers.</span></span> <span data-ttu-id="7ba17-106">Le référentiel d’images peut être partagé par plusieurs instances MED-V.</span><span class="sxs-lookup"><span data-stu-id="7ba17-106">The image repository can be shared by multiple MED-V instances.</span></span>

<span data-ttu-id="7ba17-107">Pour concevoir les référentiels d’image, vous devez d’abord déterminer la façon dont les images seront déployées sur chaque client, puis si ce client nécessite un référentiel d’image local.</span><span class="sxs-lookup"><span data-stu-id="7ba17-107">To design the image repositories, you must first decide how the images will be deployed to each client and then whether that client requires a local image repository.</span></span> <span data-ttu-id="7ba17-108">Tout référentiel est alors conçu et placé, ainsi que le serveur IIS qui lui est associé.</span><span class="sxs-lookup"><span data-stu-id="7ba17-108">Each repository is then designed and placed, along with its accompanying IIS server.</span></span>

## <span data-ttu-id="7ba17-109">Déterminer la façon dont les images seront déployées</span><span class="sxs-lookup"><span data-stu-id="7ba17-109">Determine How Images Will Be Deployed</span></span>


<span data-ttu-id="7ba17-110">Pour chaque espace de travail MED-V, déterminez le mode de déploiement d’images MED-V vers le client.</span><span class="sxs-lookup"><span data-stu-id="7ba17-110">For each MED-V workspace, decide how you plan to deploy MED-V images to the client.</span></span> <span data-ttu-id="7ba17-111">Il est important de déterminer le nombre de référentiels nécessaires au stockage des images compactées, où ces référentiels seront placés, puis de concevoir ces référentiels.</span><span class="sxs-lookup"><span data-stu-id="7ba17-111">This is important in determining how many repositories are necessary to store the packed images, where those repositories will be placed, and then to design those repositories.</span></span>

<span data-ttu-id="7ba17-112">Les images compactées peuvent être déployées comme suit:</span><span class="sxs-lookup"><span data-stu-id="7ba17-112">Packed images can be deployed in the following ways:</span></span>

-   <span data-ttu-id="7ba17-113">Téléchargé sur le réseau à partir d’un serveur de distribution d’images, qui comprend un serveur de fichiers et un serveur IIS.</span><span class="sxs-lookup"><span data-stu-id="7ba17-113">Downloaded over the network from an image distribution server, which comprises a file server and IIS server.</span></span>

-   <span data-ttu-id="7ba17-114">Sur un support amovible, tel qu’un lecteur USB ou un DVD.</span><span class="sxs-lookup"><span data-stu-id="7ba17-114">On removable media, such as a USB drive or DVD.</span></span>

-   <span data-ttu-id="7ba17-115">Pré-intermédiaire vers un répertoire de magasin d’images sur l’ordinateur client à l’aide d’un centre de distribution de logiciels d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="7ba17-115">Pre-staged to an image store directory on the client computer using an enterprise software distribution center.</span></span>

<span data-ttu-id="7ba17-116">Déterminez la méthode à utiliser pour déployer des images MED-V vers chacun des clients et si l’emplacement nécessite un référentiel d’image.</span><span class="sxs-lookup"><span data-stu-id="7ba17-116">Decide which method, or methods, will be used to deploy MED-V images to each of the clients and whether the location will require an image repository.</span></span>

## <span data-ttu-id="7ba17-117">Déterminer le nombre de référentiels d’images</span><span class="sxs-lookup"><span data-stu-id="7ba17-117">Determine the Number of Image Repositories</span></span>


<span data-ttu-id="7ba17-118">À présent que vous avez déterminé le nombre minimum de référentiels dont vous avez besoin, ajoutez des informations supplémentaires si l’un des critères suivants s’applique:</span><span class="sxs-lookup"><span data-stu-id="7ba17-118">Now that you have determined the minimum number of repositories you need, add more if any of the following criteria apply:</span></span>

-   <span data-ttu-id="7ba17-119">Des raisons organisationnelles ou réglementaires permettant de séparer les images MED-V, il est possible que certaines images MED-V ne puissent pas coexister dans le même référentiel.</span><span class="sxs-lookup"><span data-stu-id="7ba17-119">Organizational or regulatory reasons to separate the MED-V images—some MED-V images may not be able to coexist in the same repository.</span></span> <span data-ttu-id="7ba17-120">Par exemple, les données personnelles sensibles peuvent exiger le stockage sur un serveur qui n’est disponible que pour un ensemble limité d’employés qui ont besoin d’accéder à ces données.</span><span class="sxs-lookup"><span data-stu-id="7ba17-120">For example, sensitive personal data may require storage on a server that is only available to a limited set of employees who need access to the data.</span></span>

-   <span data-ttu-id="7ba17-121">Clients sur réseaux isolés: si des images sont déployées sur le réseau, déterminez si des réseaux sont isolés et nécessitent un référentiel distinct.</span><span class="sxs-lookup"><span data-stu-id="7ba17-121">Clients in isolated networks—if images will be deployed over the network, determine whether any networks are isolated and require a separate repository.</span></span> <span data-ttu-id="7ba17-122">Par exemple, les organisations isolent souvent les réseaux de laboratoire des réseaux de production.</span><span class="sxs-lookup"><span data-stu-id="7ba17-122">For example, organizations often isolate lab networks from production networks.</span></span>

-   <span data-ttu-id="7ba17-123">Clients sur réseaux distants: si des images sont déployées sur le réseau, il est possible que certains ordinateurs clients soient séparés du référentiel par des liens réseau disposant d’une bande passante insuffisante pour offrir une connaissance appropriée lorsqu’un client charge un espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="7ba17-123">Clients in remote networks—if images will be deployed over the network, some client machines may be separated from the repository by network links that have insufficient bandwidth to provide an adequate experience when a client loads a MED-V workspace.</span></span> <span data-ttu-id="7ba17-124">Le cas échéant, concevez des instances MED-V supplémentaires pour répondre à ce besoin.</span><span class="sxs-lookup"><span data-stu-id="7ba17-124">If necessary, design additional MED-V instances to address this need.</span></span>

<span data-ttu-id="7ba17-125">Ajoutez ces référentiels à la conception.</span><span class="sxs-lookup"><span data-stu-id="7ba17-125">Add these repositories to the design.</span></span> <span data-ttu-id="7ba17-126">Déterminez le nom de chaque référentiel et la raison pour le concevoir.</span><span class="sxs-lookup"><span data-stu-id="7ba17-126">Decide on a name for each repository and the reason for designing it.</span></span> <span data-ttu-id="7ba17-127">Déterminez les images MED-V que les référentiels comprendront et quels sont les clients MED-v qui chargera des espaces de travail MED-v avec des images du référentiel.</span><span class="sxs-lookup"><span data-stu-id="7ba17-127">Decide which MED-V images the repositories will hold and which MED-V clients will load MED-V workspaces with images from the repository.</span></span>

## <span data-ttu-id="7ba17-128">Conception et placement des référentiels d’images</span><span class="sxs-lookup"><span data-stu-id="7ba17-128">Design and Place the Image Repositories</span></span>


<span data-ttu-id="7ba17-129">Lorsqu’une nouvelle image est disponible pour les clients, les clients commencent à télécharger l’image en même temps.</span><span class="sxs-lookup"><span data-stu-id="7ba17-129">When a new image is available to clients, clients begin downloading the image, possibly simultaneously.</span></span> <span data-ttu-id="7ba17-130">Cela crée une forte demande sur le référentiel et doit être pris en compte lors de la conception du référentiel d’images.</span><span class="sxs-lookup"><span data-stu-id="7ba17-130">This creates a high demand on the repository and must be taken into account when designing the image repository.</span></span>

<span data-ttu-id="7ba17-131">Pour chaque référentiel, déterminez la quantité de données qu’elle va stocker.</span><span class="sxs-lookup"><span data-stu-id="7ba17-131">For each repository, determine the amount of data it will store.</span></span> <span data-ttu-id="7ba17-132">Somme de la taille d’images qui seront stockées dans le référentiel.</span><span class="sxs-lookup"><span data-stu-id="7ba17-132">Sum the sizes of images that will be stored in the repository.</span></span> <span data-ttu-id="7ba17-133">Il s’agit de la valeur de l’espace disque requis sur le serveur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7ba17-133">This is the value of the disk space required on the file server.</span></span>

<span data-ttu-id="7ba17-134">Ensuite, ajoutez le nombre de clients susceptibles de télécharger des images MED-V à partir du référentiel.</span><span class="sxs-lookup"><span data-stu-id="7ba17-134">Next, add up the number of clients that may download MED-V images from the repository.</span></span> <span data-ttu-id="7ba17-135">C’est le nombre maximal de téléchargements simultanés qui peuvent se produire quand une nouvelle image MED-V est chargée dans le référentiel.</span><span class="sxs-lookup"><span data-stu-id="7ba17-135">This is the maximum number of concurrent downloads that can occur when a new MED-V image is loaded into the repository.</span></span> <span data-ttu-id="7ba17-136">Le serveur de fichiers doit être conçu avec un sous-système de disque capable de répondre aux demandes d’e/s qui seront créées.</span><span class="sxs-lookup"><span data-stu-id="7ba17-136">The file server must be designed with a disk subsystem that can meet the IO demands this will create.</span></span>

<span data-ttu-id="7ba17-137">Le référentiel d’images peut résider sur le même système que le serveur MED-V et au serveur exécutant SQL Server, ou sur un partage de fichiers distant.</span><span class="sxs-lookup"><span data-stu-id="7ba17-137">The image repository can reside on the same system as the MED-V server and the server running SQL Server, or on a remote file share.</span></span> <span data-ttu-id="7ba17-138">Vous pouvez également l’exécuter sur un ordinateur virtuel Windows Server 2008 Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="7ba17-138">You can also run it in a Windows Server2008 Hyper-V VM.</span></span> <span data-ttu-id="7ba17-139">Vérifiez l’emplacement réseau des clients que le référentiel d’images va traiter et placez le référentiel à un emplacement réseau où il disposera d’une bande passante suffisante pour répondre aux attentes du niveau de service de ces clients.</span><span class="sxs-lookup"><span data-stu-id="7ba17-139">Check the network location of the clients that the image repository will service, and place the repository in a network location where it will have sufficient bandwidth to meet the service level expectations of those clients.</span></span>

### <span data-ttu-id="7ba17-140">Tolérance de panne</span><span class="sxs-lookup"><span data-stu-id="7ba17-140">Fault Tolerance</span></span>

<span data-ttu-id="7ba17-141">Si le référentiel d’image n’est pas disponible, les clients ne seront pas en mesure de télécharger les images MED-V nouvelles ou mises à jour.</span><span class="sxs-lookup"><span data-stu-id="7ba17-141">If the image repository is unavailable, clients will not be able to download new or updated MED-V images.</span></span> <span data-ttu-id="7ba17-142">Pour concevoir des options de tolérance de panne pour le serveur de fichiers et les disques à tolérance de panne, voir le Guide de [planification et de conception de l’infrastructure Microsoft SQL server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) .</span><span class="sxs-lookup"><span data-stu-id="7ba17-142">To design fault-tolerance options for the file server and fault-tolerant disks, see the [Infrastructure Planning and Design Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) guide.</span></span>

## <span data-ttu-id="7ba17-143">Conception et placement des serveurs IIS</span><span class="sxs-lookup"><span data-stu-id="7ba17-143">Design and Place the IIS Servers</span></span>


<span data-ttu-id="7ba17-144">Cette section ne concerne que les clients qui téléchargent des fichiers image à l’aide de HTTP ou HTTPs.</span><span class="sxs-lookup"><span data-stu-id="7ba17-144">This section is only relevant if clients will download image files over the network using HTTP or HTTPS.</span></span>

<span data-ttu-id="7ba17-145">Le serveur IIS peut cohabiter sur le même système que le serveur MED-V et au serveur exécutant SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7ba17-145">The IIS server can coexist on the same system as the MED-V server and the server running SQL Server.</span></span> <span data-ttu-id="7ba17-146">Il peut également être exécuté sur un ordinateur virtuel Windows Server 2008 Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="7ba17-146">It can also run in a Windows Server2008 Hyper-V VM.</span></span> <span data-ttu-id="7ba17-147">L’infrastructure du serveur IIS doit disposer d’un débit suffisant pour livrer des images aux clients au sein des attentes de niveau de service de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="7ba17-147">The IIS server infrastructure must have sufficient throughput to deliver images to clients within the service level expectations of the organization.</span></span> <span data-ttu-id="7ba17-148">Elle doit être conçue avec un sous-système de disque capable de répondre aux demandes d’e/s créées.</span><span class="sxs-lookup"><span data-stu-id="7ba17-148">It must be designed with a disk subsystem that can meet the IO demands this creates.</span></span>

<span data-ttu-id="7ba17-149">Pour chaque référentiel d’images, totalisez le nombre de clients qui peuvent télécharger des images MED-V à l’aide d’IIS.</span><span class="sxs-lookup"><span data-stu-id="7ba17-149">For each image repository, sum the number of clients that may download MED-V images using IIS.</span></span> <span data-ttu-id="7ba17-150">C’est le nombre maximal de téléchargements simultanés qui peuvent se produire lors du chargement d’une image dans le référentiel.</span><span class="sxs-lookup"><span data-stu-id="7ba17-150">This is the maximum number of concurrent downloads that can occur when an image is loaded into the repository.</span></span> <span data-ttu-id="7ba17-151">Utiliser la somme du débit et les prévisions de niveau de service définies dans [définir l’étendue du projet](define-the-project-scope.md) pour planifier la conception de l’infrastructure du serveur IIS et déterminer la quantité de bande passante nécessaire à l’allocation pour le référentiel.</span><span class="sxs-lookup"><span data-stu-id="7ba17-151">Use the throughput sum and the service level expectations determined in [Define the Project Scope](define-the-project-scope.md) to plan the design of the IIS server infrastructure and to determine the appropriate amount of bandwidth to allocate for the repository.</span></span>

<span data-ttu-id="7ba17-152">Pour concevoir l’infrastructure IIS, voir le Guide de [planification et de conception de l’infrastructure Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .</span><span class="sxs-lookup"><span data-stu-id="7ba17-152">To design the IIS infrastructure, see the [Infrastructure Planning and Design Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) guide.</span></span>

### <span data-ttu-id="7ba17-153">Tolérance de panne</span><span class="sxs-lookup"><span data-stu-id="7ba17-153">Fault Tolerance</span></span>

<span data-ttu-id="7ba17-154">Si l’infrastructure du serveur IIS n’est pas disponible, les clients ne seront pas en mesure de télécharger des images nouvelles ou mises à jour.</span><span class="sxs-lookup"><span data-stu-id="7ba17-154">If the IIS server infrastructure is unavailable, clients will not be able to download new or updated images.</span></span> <span data-ttu-id="7ba17-155">Pour configurer la tolérance de panne, le serveur IIS Server 2008 Windows peut être placé dans un cluster de basculement.</span><span class="sxs-lookup"><span data-stu-id="7ba17-155">To configure fault tolerance, the Windows Server2008-based IIS server can be placed in a failover cluster.</span></span> <span data-ttu-id="7ba17-156">Pour concevoir la tolérance de panne pour l’infrastructure du serveur IIS, voir le Guide de [planification et de conception de l’infrastructure Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .</span><span class="sxs-lookup"><span data-stu-id="7ba17-156">To design the fault tolerance for the IIS server infrastructure, see the [Infrastructure Planning and Design Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) guide.</span></span>

## <span data-ttu-id="7ba17-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ba17-157">Related topics</span></span>


[<span data-ttu-id="7ba17-158">Déploiement d'un espace de travail MED-V à l'aide d'un système de distribution de logiciels d'entreprise</span><span class="sxs-lookup"><span data-stu-id="7ba17-158">Deploying a MED-V Workspace Using an Enterprise Software Distribution System</span></span>](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md)

[<span data-ttu-id="7ba17-159">Déploiement d'un espace de travail MED-V à l'aide d'un package de déploiement</span><span class="sxs-lookup"><span data-stu-id="7ba17-159">Deploying a MED-V Workspace Using a Deployment Package</span></span>](deploying-a-med-v-workspace-using-a-deployment-package.md)

 

 





