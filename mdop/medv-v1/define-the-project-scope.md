---
title: Définir la portée du projet
description: Définir la portée du projet
author: dansimp
ms.assetid: 84637d2a-2e30-417d-b150-dc81f414b3a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4f33562452327bba9036f56d9f6f96650f00c1f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810079"
---
# <span data-ttu-id="3ff2b-103">Définir la portée du projet</span><span class="sxs-lookup"><span data-stu-id="3ff2b-103">Define the Project Scope</span></span>


<span data-ttu-id="3ff2b-104">Lors de la définition de l’étendue du projet, déterminez les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="3ff2b-104">When defining the project scope, determine the following:</span></span>

1.  <span data-ttu-id="3ff2b-105">Utilisateurs finaux MED-V: l’emplacement et le nombre d’utilisateurs finaux sont utilisés pour déterminer l’emplacement des installations du client MED-V et le nombre d’instances MED-v, ainsi que le nombre et la position des référentiels d’image MED-V.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-105">The MED-V end users—the location and number of end users are used in determining the location of MED-V client installations and the number of MED-V instances, as well as the number and placement of MED-V image repositories.</span></span>

2.  <span data-ttu-id="3ff2b-106">Les images d’ordinateur virtuel (VM) devant être gérées par MED-V, afin de déterminer la méthode de distribution d’images et de placement des référentiels d’image.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-106">The virtual machine (VM) images to be managed by MED-V—to determine the method of distributing images and placement of image repositories.</span></span>

3.  <span data-ttu-id="3ff2b-107">Les attentes en matière de niveau de service de l’organisation, afin de déterminer les besoins en matière de performances et de tolérance de panne pour le serveur et la base de données MED-V, ainsi que le référentiel d’images.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-107">The organization’s service level expectations—to determine the performance and fault-tolerance requirements for the MED-V server and database as well as the image repository.</span></span>

4.  <span data-ttu-id="3ff2b-108">Valider avec l’entreprise: Assurez-vous d’avoir une idée complète des répercussions de l’infrastructure planifiée sur l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-108">Validate with the business—ensure there is a complete understanding of how the planned infrastructure affects the business.</span></span>

## <span data-ttu-id="3ff2b-109">Définir les utilisateurs finaux de MED-V</span><span class="sxs-lookup"><span data-stu-id="3ff2b-109">Define the MED-V End Users</span></span>


<span data-ttu-id="3ff2b-110">Tout d’abord, déterminez où se trouvent les utilisateurs finaux, ainsi que le nombre d’utilisateurs dans chaque emplacement.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-110">First, determine where the end users are located, as well as the number of users in each location.</span></span> <span data-ttu-id="3ff2b-111">Deuxièmement, procurez-vous un diagramme d’infrastructure réseau qui affiche les emplacements des utilisateurs et la bande passante disponible vers ces emplacements.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-111">Second, obtain a network infrastructure diagram that displays the user locations and the available bandwidth to those locations.</span></span> <span data-ttu-id="3ff2b-112">Enfin, vérifiez si les utilisateurs voyagent entre eux.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-112">Third, find out if users travel between locations.</span></span> <span data-ttu-id="3ff2b-113">Si les utilisateurs voyagent, des capacités supplémentaires peuvent être nécessaires pour la conception de l’infrastructure du serveur et des référentiels d’image.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-113">If users travel, additional capacity may be required in the design of the server infrastructure and image repositories.</span></span>

## <span data-ttu-id="3ff2b-114">Déterminez les images MED-V à gérer par MED-V.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-114">Determine the MED-V Images to Be Managed by MED-V</span></span>


<span data-ttu-id="3ff2b-115">Une fois les utilisateurs finaux MED-V définis, Déterminez quels ordinateurs virtuels seront gérés par MED-V pour les utilisateurs de chaque emplacement.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-115">After the MED-V end users have been defined, determine which VMs will be managed by MED-V for the users in each location.</span></span>

<span data-ttu-id="3ff2b-116">Si l’un des ordinateurs virtuels est stocké dans une bibliothèque centralisée, déterminez l’emplacement de la bibliothèque de manière à ce qu’il puisse être évalué pour une utilisation comme un référentiel MED-V.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-116">If any of the VMs are stored in a centralized library, determine the location of the library so that it may be evaluated for use as a MED-V repository.</span></span>

## <a href="" id="determine-the-organization-s-service-level-expectations"></a><span data-ttu-id="3ff2b-117">Déterminez les attentes en matière de niveau de service de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-117">Determine the Organization’s Service Level Expectations</span></span>


<span data-ttu-id="3ff2b-118">Pour chaque espace de travail MED-V, notez la durée acceptable du chargement d’une nouvelle image et la période de déploiement des mises à jour critiques.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-118">For each MED-V workspace, note the acceptable time for a new image to load and the timeframe for critical updates to be deployed.</span></span>

<span data-ttu-id="3ff2b-119">Le cas échéant, notez les attentes en matière de niveau de service pour la création de rapports MED-V, qui doivent être utilisées dans la conception de l’infrastructure du serveur.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-119">If applicable, record the service level expectations for MED-V reporting, to be used in the design of the server infrastructure.</span></span>

## <span data-ttu-id="3ff2b-120">Valider avec l’entreprise</span><span class="sxs-lookup"><span data-stu-id="3ff2b-120">Validate with the Business</span></span>


<span data-ttu-id="3ff2b-121">Posez les questions suivantes aux parties prenantes et aux propriétaires d’applications:</span><span class="sxs-lookup"><span data-stu-id="3ff2b-121">Ask business stakeholders and application owners the following questions:</span></span>

-   <span data-ttu-id="3ff2b-122">Existe-t-il des images qui peuvent être combinées?</span><span class="sxs-lookup"><span data-stu-id="3ff2b-122">Are there any existing images that can be combined?</span></span> <span data-ttu-id="3ff2b-123">Par exemple, si l’application A sur WindowsXP est une image VPC et que l’application B sur WindowsXP est une autre image VPC, il est possible qu’une seule image puisse contenir les deux applications, ce qui permet de réduire l’espace de stockage et la bande passante requise pour le téléchargement d’images.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-123">For example, if application A on WindowsXP is one VPC image and application B on WindowsXP is another VPC image, perhaps a single image can contain both applications, thereby reducing repository space and bandwidth required for image download.</span></span>

-   <span data-ttu-id="3ff2b-124">Est-ce que les applications dans le cadre d’une licence peuvent être gérées et prises en charge dans le cadre d’une VM par MED-V?</span><span class="sxs-lookup"><span data-stu-id="3ff2b-124">Are the in-scope applications licensable and supportable if delivered in a VM by MED-V?</span></span> <span data-ttu-id="3ff2b-125">Contactez le fournisseur de l’application pour veiller à ce que le contrat de licence et d’assistance ne soit pas violé en livrant l’application par MED-V.</span><span class="sxs-lookup"><span data-stu-id="3ff2b-125">Check with the application supplier to ensure that licensing and support terms will not be violated by delivering the application through MED-V.</span></span>

 

 





