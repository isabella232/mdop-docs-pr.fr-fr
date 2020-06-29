---
title: Architecture de haut niveau
description: Architecture de haut niveau
author: dansimp
ms.assetid: a00edb9f-207b-4f32-9e8f-522ea2739d2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a5db4a56b2abfb0df19b0d6d86f4bf88380c2bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812269"
---
# <span data-ttu-id="d63be-103">Architecture de haut niveau</span><span class="sxs-lookup"><span data-stu-id="d63be-103">High-Level Architecture</span></span>


<span data-ttu-id="d63be-104">Cette section décrit l’architecture système de niveau supérieur et la conception des composants de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="d63be-104">This section describes the high-level system architecture and component design of Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="d63be-105">Architecture système</span><span class="sxs-lookup"><span data-stu-id="d63be-105">System Architecture</span></span>


<span data-ttu-id="d63be-106">MED-V améliore le PC virtuel Windows pour exécuter deux systèmes d’exploitation sur un appareil, l’ajout d’une remise d’image virtuelle, la mise en service basée sur une stratégie de groupe et la gestion centralisée.</span><span class="sxs-lookup"><span data-stu-id="d63be-106">MED-V enhances Windows Virtual PC to run two operating systems on one device, adding virtual image delivery, Group Policy-based provisioning, and centralized management.</span></span> <span data-ttu-id="d63be-107">Grâce à l’utilisation de MED-V, vous pouvez facilement configurer, déployer et gérer des images d’entreprise virtuelles PC Windows sur n’importe quel ordinateur de bureau Windows 7 professionnel, entreprise ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d63be-107">By using MED-V, you can easily configure, deploy, and manage corporate Windows Virtual PC images on any Windows-based desktop running Windows 7 Professional, Enterprise, or Windows 7 Ultimate.</span></span> <span data-ttu-id="d63be-108">La solution MED-V inclut les composants suivants:</span><span class="sxs-lookup"><span data-stu-id="d63be-108">The MED-V solution includes the following components:</span></span>

<a href="" id="---------------med-v-host"></a> **<span data-ttu-id="d63be-109">Hôte MED-V</span><span class="sxs-lookup"><span data-stu-id="d63be-109">MED-V Host</span></span>**  
<span data-ttu-id="d63be-110">Un environnement Windows 7 qui inclut un agent hôte MED-V, un système de distribution de logiciels électronique (ESD), un système de gestion du Registre et un invité MED-V.</span><span class="sxs-lookup"><span data-stu-id="d63be-110">A Windows 7 environment that includes a MED-V Host Agent, an electronic software distribution (ESD) system, a registry management system, and a MED-V guest.</span></span> <span data-ttu-id="d63be-111">L’hôte MED-V interagit avec l’invité MED-V de façon à ce que certaines fonctions de configuration et informations système puissent être traitées.</span><span class="sxs-lookup"><span data-stu-id="d63be-111">The MED-V host interacts with the MED-V guest so that certain setup functions and system information can be processed.</span></span>

<a href="" id="-------------------med-v-host-agent"></a> **<span data-ttu-id="d63be-112">Agent hôte MED-V</span><span class="sxs-lookup"><span data-stu-id="d63be-112">MED-V Host Agent</span></span>**  
<span data-ttu-id="d63be-113">Le logiciel MED-V contenu dans l’hôte MED-V, qui fournit un canal permettant de communiquer avec l’invité MED-V.</span><span class="sxs-lookup"><span data-stu-id="d63be-113">The MED-V software contained in the MED-V host that provides a channel to communicate with the MED-V guest.</span></span> <span data-ttu-id="d63be-114">Il fournit également des fonctionnalités telles que la première configuration et la publication d’applications.</span><span class="sxs-lookup"><span data-stu-id="d63be-114">It also provides functionality such as first time setup and application publishing.</span></span>

<span data-ttu-id="d63be-115">**Remarques**  Après l’installation de MED-V et de ses composants nécessaires, MED-V doit être configuré.</span><span class="sxs-lookup"><span data-stu-id="d63be-115">**Note** After MED-V and its required components are installed MED-V must be configured.</span></span> <span data-ttu-id="d63be-116">La configuration de MED-V est désignée sous le nom de configuration pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="d63be-116">The configuration of MED-V is referred to as first time setup.</span></span>

 

<a href="" id="esd-system"></a>**<span data-ttu-id="d63be-117">Système ESD</span><span class="sxs-lookup"><span data-stu-id="d63be-117">ESD System</span></span>**  
<span data-ttu-id="d63be-118">Votre méthode de distribution de logiciels existante qui vous permet de déployer et d’installer les fichiers de package d’espace de travail MED-V créés par MED-V.</span><span class="sxs-lookup"><span data-stu-id="d63be-118">Your existing software distribution method that lets you deploy and install the MED-V workspace package files that MED-V creates.</span></span>

<a href="" id="registry-management-system"></a>**<span data-ttu-id="d63be-119">Système de gestion du Registre</span><span class="sxs-lookup"><span data-stu-id="d63be-119">Registry Management System</span></span>**  
<span data-ttu-id="d63be-120">Votre méthode de gestion des paramètres de stratégie de groupe et des préférences.</span><span class="sxs-lookup"><span data-stu-id="d63be-120">Your existing method of managing Group Policy settings and preferences.</span></span>

<a href="" id="windows-virtual-pc-image"></a>**<span data-ttu-id="d63be-121">Image de l’ordinateur virtuel Windows</span><span class="sxs-lookup"><span data-stu-id="d63be-121">Windows Virtual PC Image</span></span>**  
<span data-ttu-id="d63be-122">Une machine virtuelle définie par l’administrateur qui contient les composants suivants:</span><span class="sxs-lookup"><span data-stu-id="d63be-122">An administrator-defined virtual machine that contains the following components:</span></span>

<a href="" id="corporate-operating-system"></a>**<span data-ttu-id="d63be-123">Système d’exploitation de l’entreprise</span><span class="sxs-lookup"><span data-stu-id="d63be-123">Corporate Operating System</span></span>**  
<span data-ttu-id="d63be-124">Votre système d’exploitation standard.</span><span class="sxs-lookup"><span data-stu-id="d63be-124">Your standard corporate operating system.</span></span>

<a href="" id="management-and-security-tools"></a>**<span data-ttu-id="d63be-125">Outils de gestion et de sécurité</span><span class="sxs-lookup"><span data-stu-id="d63be-125">Management and Security Tools</span></span>**  
<span data-ttu-id="d63be-126">Vos outils de gestion standard et de sécurité, tels que la protection antivirus.</span><span class="sxs-lookup"><span data-stu-id="d63be-126">Your standard management and security tools, such as virus protection.</span></span>

<a href="" id="-----------------------med-v-guest"></a> **<span data-ttu-id="d63be-127">Invité MED-V</span><span class="sxs-lookup"><span data-stu-id="d63be-127">MED-V Guest</span></span>**  
<span data-ttu-id="d63be-128">Un environnement Windows XP SP3, dans le cadre d’un PC virtuel Windows exécuté sur Windows 7 qui contient les composants suivants:</span><span class="sxs-lookup"><span data-stu-id="d63be-128">A Windows XP SP3 environment, as part of a Windows Virtual PC running on Windows 7 that contains the following components:</span></span>

<a href="" id="---------------------------med-v-guest-agent"></a> **<span data-ttu-id="d63be-129">Agent d’invité MED-V</span><span class="sxs-lookup"><span data-stu-id="d63be-129">MED-V Guest Agent</span></span>**  
<span data-ttu-id="d63be-130">Le logiciel MED-V contenu dans l’invité MED-V, qui fournit un canal permettant de communiquer avec l’hôte MED-V.</span><span class="sxs-lookup"><span data-stu-id="d63be-130">The MED-V software contained in the MED-V guest that provides a channel to communicate with the MED-V host.</span></span> <span data-ttu-id="d63be-131">Il prend également en charge l’agent hôte MED-V avec des fonctions telles que la première configuration.</span><span class="sxs-lookup"><span data-stu-id="d63be-131">It also supports the MED-V Host Agent with functions like performing first time setup.</span></span>

<span data-ttu-id="d63be-132">**Remarques**  L’agent d’invité MED-V est automatiquement installé lors de la première configuration.</span><span class="sxs-lookup"><span data-stu-id="d63be-132">**Note** The MED-V Guest Agent is installed automatically during first time setup.</span></span>

 

<a href="" id="esd-client"></a>**<span data-ttu-id="d63be-133">Client ESD</span><span class="sxs-lookup"><span data-stu-id="d63be-133">ESD Client</span></span>**  
<span data-ttu-id="d63be-134">Partie facultative de votre système ESD qui installe les packages logiciels et signale l’état du système ESD.</span><span class="sxs-lookup"><span data-stu-id="d63be-134">An optional part of your ESD system that installs software packages and reports status to the ESD system.</span></span>

## <span data-ttu-id="d63be-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d63be-135">Related topics</span></span>


[<span data-ttu-id="d63be-136">Planification de la compatibilité du système d'exploitation avec les applications</span><span class="sxs-lookup"><span data-stu-id="d63be-136">Planning for Application Operating System Compatibility</span></span>](planning-for-application-operating-system-compatibility.md)

[<span data-ttu-id="d63be-137">Préparer l'environnement de déploiement de MED-V</span><span class="sxs-lookup"><span data-stu-id="d63be-137">Prepare the Deployment Environment for MED-V</span></span>](prepare-the-deployment-environment-for-med-v.md)

 

 





