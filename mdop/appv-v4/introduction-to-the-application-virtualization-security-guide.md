---
title: Introduction au Guide de sécurité d’application Virtualization
description: Introduction au Guide de sécurité d’application Virtualization
author: dansimp
ms.assetid: 50e1d220-7a95-45b8-933b-3dadddebe26f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4b41c65c5ad753aa606d47d2eafe4a28e035cc4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806638"
---
# <span data-ttu-id="9eb3e-103">Introduction au Guide de sécurité d’application Virtualization</span><span class="sxs-lookup"><span data-stu-id="9eb3e-103">Introduction to the Application Virtualization Security Guide</span></span>


<span data-ttu-id="9eb3e-104">Ce guide de sécurité de Microsoft Application Virtualization (App-V) fournit des instructions pour les administrateurs chargés de la configuration des fonctionnalités de sécurité sélectionnées pour le déploiement d’App-V.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-104">This Microsoft Application Virtualization (App-V) security guide provides instructions for administrators who are responsible for configuring the security features that were selected for the App-V deployment.</span></span>

<span data-ttu-id="9eb3e-105">**Remarques**  Cette documentation ne fournit pas d’aide pour choisir les options de sécurité spécifiques.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-105">**Note** This documentation does not provide guidance for choosing the specific security options.</span></span> <span data-ttu-id="9eb3e-106">Ces informations sont fournies dans le livre blanc App-V Security meilleures pratiques disponible sur le <https://go.microsoft.com/fwlink/?LinkId=127120> .</span><span class="sxs-lookup"><span data-stu-id="9eb3e-106">That information is provided in the App-V Security Best Practices white paper available at <https://go.microsoft.com/fwlink/?LinkId=127120>.</span></span>

 

<span data-ttu-id="9eb3e-107">En tant qu’administrateur d’application-V utilisant ce guide, vous devez être familiarisé avec les technologies suivantes en matière de sécurité:</span><span class="sxs-lookup"><span data-stu-id="9eb3e-107">As an App-V administrator using this guide, you should be familiar with the following security-related technologies:</span></span>

-   <span data-ttu-id="9eb3e-108">Services de domaine ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="9eb3e-108">Active Directory Domain Services</span></span>

-   <span data-ttu-id="9eb3e-109">Infrastructure à clé publique (PKI)</span><span class="sxs-lookup"><span data-stu-id="9eb3e-109">Public key infrastructure (PKI)</span></span>

-   <span data-ttu-id="9eb3e-110">Sécurité du protocole Internet (IPsec)</span><span class="sxs-lookup"><span data-stu-id="9eb3e-110">Internet Protocol Security (IPsec)</span></span>

-   <span data-ttu-id="9eb3e-111">Stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="9eb3e-111">Group Policies</span></span>

-   <span data-ttu-id="9eb3e-112">Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="9eb3e-112">Internet Information Services (IIS)</span></span>

## <span data-ttu-id="9eb3e-113">Composants d’infrastructure APP-V</span><span class="sxs-lookup"><span data-stu-id="9eb3e-113">APP-V Infrastructure Components</span></span>


<span data-ttu-id="9eb3e-114">Lors de la planification d’un environnement d’application de sécurité améliorée, vous pouvez envisager différents modèles d’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-114">When planning an enhanced security App-V environment, you can consider several different infrastructure models.</span></span>

<span data-ttu-id="9eb3e-115">**Remarques**  Pour plus d’informations sur les modèles d’infrastructure App-V, voir la documentation suivante:</span><span class="sxs-lookup"><span data-stu-id="9eb3e-115">**Note** For more information about App-V infrastructure models, see the following documentation:</span></span>

-   [<span data-ttu-id="9eb3e-116">Guide de planification et de déploiement d’App-V</span><span class="sxs-lookup"><span data-stu-id="9eb3e-116">App-V Planning and Deployment Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [<span data-ttu-id="9eb3e-117">Série de guides de planification et de conception d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="9eb3e-117">Infrastructure Planning and Design Guide Series</span></span>](https://go.microsoft.com/fwlink/?LinkId=151986)

 

<span data-ttu-id="9eb3e-118">Ces modèles utilisent certains composants de l’application-V, mais ce n’est pas tout illustré dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-118">These models utilize some but possibly not all of the App-V components depicted in the following illustration.</span></span>

![diagramme d’intersuccursales App-v](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a><span data-ttu-id="9eb3e-120">Serveur de gestion Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="9eb3e-120">Application Virtualization (App-V) Management Server</span></span>  
<span data-ttu-id="9eb3e-121">Le serveur de gestion App-V diffuse le contenu du package et publie les raccourcis et les associations de types de fichiers sur le client App-V.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-121">The App-V Management Server streams the package content and publishes the shortcuts and file-type associations to the App-V Client.</span></span> <span data-ttu-id="9eb3e-122">Le serveur de gestion App-V prend également en charge la mise à niveau active, la gestion des licences et une base de données qui peut être utilisée pour la création de rapports.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-122">The App-V Management Server also supports active upgrade, license management, and a database that can be used for reporting.</span></span>

<a href="" id="application-virtualization--app-v--streaming-server"></a><span data-ttu-id="9eb3e-123">Serveur de diffusion en continu d’applications (App-V)</span><span class="sxs-lookup"><span data-stu-id="9eb3e-123">Application Virtualization (App-V) Streaming Server</span></span>  
<span data-ttu-id="9eb3e-124">Le serveur de streaming App-V héberge les packages de diffusion en continu pour les clients App-v dans les environnements, tels que les succursales, où la bande passante pour la connexion au serveur de gestion de l’application-V est insuffisante pour le contenu du package de diffusion en continu vers les clients.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-124">The App-V Streaming Server hosts the packages for streaming to App-V Clients in environments such as branch offices, where the bandwidth of the connection to the App-V Management Server is insufficient for streaming package content to clients.</span></span> <span data-ttu-id="9eb3e-125">Le serveur de diffusion en continu comporte uniquement une fonctionnalité de diffusion en continu et ne vous permet pas d’utiliser la console de gestion des applications ou le service Web App-V.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-125">The Streaming Server contains only streaming functionality and does not provide you with the App-V Management Console or the App-V Management Web Service.</span></span>

<a href="" id="application-virtualization--app-v--data-store"></a><span data-ttu-id="9eb3e-126">Magasin de données Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="9eb3e-126">Application Virtualization (App-V) Data Store</span></span>  
<span data-ttu-id="9eb3e-127">Le magasin de données App-V, dans la base de données SQL, conserve les informations relatives à l’infrastructure App-V.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-127">The App-V data store, in the SQL database, retains information related to the App-V infrastructure.</span></span> <span data-ttu-id="9eb3e-128">Les informations contenues dans le magasin de données App-V incluent tous les enregistrements d’application, les affectations d’application et les groupes qui gèrent l’environnement de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-128">The information in the App-V data store includes all application records, application assignments, and which groups manage the Application Virtualization environment.</span></span>

<a href="" id="application-virtualization--app-v--management-service"></a><span data-ttu-id="9eb3e-129">Service de gestion Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="9eb3e-129">Application Virtualization (App-V) Management Service</span></span>  
<span data-ttu-id="9eb3e-130">Le service de gestion App-V transmet les demandes en lecture/écriture au magasin de données de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-130">The App-V Management Service communicates read/write requests to the Application Virtualization data store.</span></span> <span data-ttu-id="9eb3e-131">Ce composant peut être installé sur le même ordinateur que le serveur de gestion de l’application-V ou sur un autre ordinateur sur lequel IIS est installé.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-131">This component can be installed on the same computer as the App-V Management Server or on a separate computer with IIS installed.</span></span>

<a href="" id="application-virtualization--app-v--management-console"></a><span data-ttu-id="9eb3e-132">Console de gestion Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="9eb3e-132">Application Virtualization (App-V) Management Console</span></span>  
<span data-ttu-id="9eb3e-133">La console de gestion App-V est un utilitaire de gestion des composants enfichables pour l’administration de l’application-V Server.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-133">The App-V Management Console is a snap-in management utility for App-V Server administration.</span></span> <span data-ttu-id="9eb3e-134">Ce composant peut être installé sur le même ordinateur que le serveur App-V ou sur une station de travail distincte disposant de MMC 3.0 et. .NET 2.0 installé.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-134">This component can be installed on the same computer as the App-V Server or on a separate workstation that has MMC3.0 and .NET2.0 installed.</span></span>

<a href="" id="application-virtualization--app-v--sequencer"></a><span data-ttu-id="9eb3e-135">Sequencer Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="9eb3e-135">Application Virtualization (App-V) Sequencer</span></span>  
<span data-ttu-id="9eb3e-136">Le Sequencer App-V surveille et capture l’installation d’applications et crée des packages d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-136">The App-V Sequencer monitors and captures the installation of applications and creates virtual application packages.</span></span> <span data-ttu-id="9eb3e-137">La sortie du Sequencer se compose de l’icône de l’application, du fichier OSD contenant des informations de définition d’application, d’un fichier manifeste de package et d’un fichier SFT contenant les fichiers de contenu de l’application.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-137">The output of the Sequencer consists of the application icon, the OSD file containing application definition information, a package manifest file, and an SFT file containing the application’s content files.</span></span> <span data-ttu-id="9eb3e-138">Vous pouvez également créer un fichier Windows Installer pour installer le package sans utiliser l’infrastructure App-V.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-138">Optionally, a Windows Installer file can be created for installing the package without using the App-V infrastructure.</span></span>

<a href="" id="application-virtualization--app-v--client"></a><span data-ttu-id="9eb3e-139">Client Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="9eb3e-139">Application Virtualization (App-V) Client</span></span>  
<span data-ttu-id="9eb3e-140">Le client App-V est installé sur l’ordinateur client de bureau App-v ou sur l’ordinateur client de services Terminal Server App-v.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-140">The App-V Client is installed on the App-V Desktop Client computer or on the App-V Terminal Services Client computer.</span></span> <span data-ttu-id="9eb3e-141">Il fournit l’environnement virtuel pour les packages d’applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-141">It provides the virtual environment for the virtual application packages.</span></span> <span data-ttu-id="9eb3e-142">Le client App-V gère le package en flux continu sur le cache, l’actualisation de la publication des applications virtuelles et l’interaction avec les serveurs de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="9eb3e-142">The App-V Client manages the package streaming to the cache, virtual application publishing refresh, and interaction with the Application Virtualization Servers.</span></span>

 

 





