---
title: Prise en main de User Experience Virtualization1.0
description: Prise en main de User Experience Virtualization1.0
author: dansimp
ms.assetid: 74a068dc-4f87-4cb4-b114-8ca2a37149f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 010cefc42c8f2d65ac7f815eff51ec2df42df4d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812162"
---
# <span data-ttu-id="b7e59-103">Prise en main de User Experience Virtualization1.0</span><span class="sxs-lookup"><span data-stu-id="b7e59-103">Getting Started With User Experience Virtualization 1.0</span></span>


<span data-ttu-id="b7e59-104">Microsoft User Interface Virtualization (UE-V) capture et centralise les paramètres d’application et les paramètres du système d’exploitation Windows pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b7e59-104">Microsoft User Experience Virtualization (UE-V) captures and centralizes application settings and Windows operating system settings for the user.</span></span> <span data-ttu-id="b7e59-105">Ces paramètres sont ensuite appliqués aux différents ordinateurs consultés par l’utilisateur, tels que des ordinateurs de bureau, des ordinateurs portables et des sessions VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="b7e59-105">These settings are then applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="b7e59-106">UE-V propose une synchronisation des paramètres pour les applications Microsoft courantes et les paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="b7e59-106">UE-V offers settings synchronization for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="b7e59-107">Il fournit également des paramètres utilisateur à tout moment, quel que soit l’endroit où les utilisateurs travaillent au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="b7e59-107">It also delivers user settings at any time to wherever users work throughout the enterprise.</span></span> <span data-ttu-id="b7e59-108">UE-V permet aux administrateurs de spécifier les paramètres de l’application et les paramètres de fenêtre itinérants.</span><span class="sxs-lookup"><span data-stu-id="b7e59-108">UE-V allows administrators to specify which application settings and Windows settings roam.</span></span> <span data-ttu-id="b7e59-109">UE-V aide les administrateurs à créer des modèles d’emplacement des paramètres personnalisés pour des applications tierces ou métier employées dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="b7e59-109">UE-V helps administrators to create custom settings location templates for third-party or line-of-business applications that are used in the enterprise.</span></span>

<span data-ttu-id="b7e59-110">La virtualisation de l’utilisation des utilisateurs offre une meilleure interface de virtualisation de l’état utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b7e59-110">User Experience Virtualization delivers an enhanced user state virtualization experience.</span></span> <span data-ttu-id="b7e59-111">Il fournit une personnalisation cohérente des paramètres de l’utilisateur dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="b7e59-111">It provides consistent personalization of the user’s settings in the following scenarios:</span></span>

-   <span data-ttu-id="b7e59-112">Itinérance des paramètres d’application utilisateur et de Windows entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="b7e59-112">Roaming user application and Windows settings between computers.</span></span>

-   <span data-ttu-id="b7e59-113">Itinérance des paramètres utilisateur entre les instances d’une application déployées à l’aide de méthodes différentes:</span><span class="sxs-lookup"><span data-stu-id="b7e59-113">Roaming user settings between the instances of an application that are deployed by using different methods:</span></span>

    -   <span data-ttu-id="b7e59-114">Applications installées</span><span class="sxs-lookup"><span data-stu-id="b7e59-114">Installed applications</span></span>

    -   <span data-ttu-id="b7e59-115">Applications de virtualisation des applications (App-V)</span><span class="sxs-lookup"><span data-stu-id="b7e59-115">Application Virtualization (App-V) sequenced applications</span></span>

    -   <span data-ttu-id="b7e59-116">Applications RemoteApp (virtualisation Bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="b7e59-116">RemoteApp (Remote Desktop Virtualization) applications</span></span>

-   <span data-ttu-id="b7e59-117">Récupérez les paramètres d’un ordinateur après un remplacement, une mise à niveau matérielle ou une renouvelle image.</span><span class="sxs-lookup"><span data-stu-id="b7e59-117">Recovering settings for a computer after replacement, hardware upgrade, or reimage.</span></span>

<span data-ttu-id="b7e59-118">Le déploiement de ce produit nécessite une planification complète avant son déploiement ou ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="b7e59-118">This product requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="b7e59-119">Dans la mesure où ce produit peut affecter chaque ordinateur au sein de votre organisation, vous risquez de perturber votre réseau entier si vous n’avez pas soigneusement planifié votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="b7e59-119">Because this product can affect every computer in your organization, you might disrupt your entire network if you do not plan your deployment carefully.</span></span> <span data-ttu-id="b7e59-120">Toutefois, si vous planifiez votre déploiement de manière précise et que vous le gérez de manière à répondre aux besoins de votre entreprise, ce produit peut vous aider à réduire la charge d’administration et le coût total de propriété.</span><span class="sxs-lookup"><span data-stu-id="b7e59-120">However, if you plan your deployment carefully and manage it so that it meets your business needs, this product can help reduce your administrative overhead and total cost of ownership.</span></span>

<span data-ttu-id="b7e59-121">Si vous débutez avec ce produit, nous vous conseillons de lire la documentation soigneusement.</span><span class="sxs-lookup"><span data-stu-id="b7e59-121">If you are new to this product, we recommend that you read the documentation carefully.</span></span> <span data-ttu-id="b7e59-122">Avant de déployer le produit dans un environnement de production, nous vous conseillons également de valider votre plan de déploiement dans un environnement réseau de test.</span><span class="sxs-lookup"><span data-stu-id="b7e59-122">Before you deploy the product to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="b7e59-123">Vous pouvez également envisager de prendre un cours sur les technologies pertinentes.</span><span class="sxs-lookup"><span data-stu-id="b7e59-123">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="b7e59-124">Pour plus d’informations sur les opportunités de formation Microsoft, voir la présentation de la formation Microsoft à l’adresse <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="b7e59-124">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="b7e59-125">**Remarques**  La version téléchargeable du Guide de l’administrateur n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="b7e59-125">**Note** A downloadable version of this administrator’s guide is not available.</span></span> <span data-ttu-id="b7e59-126">En revanche, vous pouvez en savoir plus sur un mode spécial de la bibliothèque TechNet qui vous permet de sélectionner des articles, de les regrouper dans une collection et de les imprimer ou de les exporter vers un fichier à partir de <https://go.microsoft.com/fwlink/?LinkId=272497> ( https://go.microsoft.com/fwlink/?LinkId=272497) .</span><span class="sxs-lookup"><span data-stu-id="b7e59-126">However, you can learn about a special mode of the TechNet Library that allows you to select articles, group them in a collection, and print them or export them to a file at <https://go.microsoft.com/fwlink/?LinkId=272497> (https://go.microsoft.com/fwlink/?LinkId=272497).</span></span>

 

## <span data-ttu-id="b7e59-127">Introduction aux rubriques sur la virtualisation de l’utilisation de Microsoft</span><span class="sxs-lookup"><span data-stu-id="b7e59-127">Getting started with Microsoft User Experience Virtualization topics</span></span>


-   [<span data-ttu-id="b7e59-128">À propos d'User Experience Virtualization1.0</span><span class="sxs-lookup"><span data-stu-id="b7e59-128">About User Experience Virtualization 1.0</span></span>](about-user-experience-virtualization-10.md)

    <span data-ttu-id="b7e59-129">Décrit les fonctionnalités de la virtualisation de l’utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b7e59-129">Describes the functionality and features of User Experience Virtualization.</span></span>

-   [<span data-ttu-id="b7e59-130">Architecture de haut niveau pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="b7e59-130">High-Level Architecture for UE-V 1.0</span></span>](high-level-architecture-for-ue-v-10.md)

    <span data-ttu-id="b7e59-131">Décrit les fonctionnalités de la virtualisation de l’utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b7e59-131">Explains the features of User Experience Virtualization.</span></span>

-   [<span data-ttu-id="b7e59-132">Notes de publication pour Microsoft User Experience Virtualization (UE-V)1.0</span><span class="sxs-lookup"><span data-stu-id="b7e59-132">Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--10-release-notes.md)

    <span data-ttu-id="b7e59-133">Décrit les problèmes connus pour UE-V.</span><span class="sxs-lookup"><span data-stu-id="b7e59-133">Describes the known issues for UE-V.</span></span>

-   [<span data-ttu-id="b7e59-134">Accessibilité d'UE-V</span><span class="sxs-lookup"><span data-stu-id="b7e59-134">Accessibility for UE-V</span></span>](accessibility-for-ue-v.md)

    <span data-ttu-id="b7e59-135">Décrit les raccourcis clavier et les informations d’accessibilité pour UE-V.</span><span class="sxs-lookup"><span data-stu-id="b7e59-135">Describes the keyboard shortcuts and accessibility information for UE-V.</span></span>

## <span data-ttu-id="b7e59-136">Autres ressources pour ce produit</span><span class="sxs-lookup"><span data-stu-id="b7e59-136">Other resources for this product</span></span>


-   [<span data-ttu-id="b7e59-137">Microsoft User Experience Virtualization (UE-V)1.0</span><span class="sxs-lookup"><span data-stu-id="b7e59-137">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

-   [<span data-ttu-id="b7e59-138">Planification pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="b7e59-138">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

-   [<span data-ttu-id="b7e59-139">Déploiement d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="b7e59-139">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

-   [<span data-ttu-id="b7e59-140">Opérations d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="b7e59-140">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

-   [<span data-ttu-id="b7e59-141">Résolution des problèmes liés à UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="b7e59-141">Troubleshooting UE-V 1.0</span></span>](troubleshooting-ue-v-10.md)

 

 





