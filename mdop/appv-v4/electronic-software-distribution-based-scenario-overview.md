---
title: Présentation du scénario basé sur une distribution électronique de logiciels
description: Présentation du scénario basé sur une distribution électronique de logiciels
author: dansimp
ms.assetid: e9e94b8a-6cba-4de8-9b57-73897796b6a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cfbdf40f5ac0f61721c05d0da5cd49e910b16154
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808850"
---
# <span data-ttu-id="f3fd0-103">Présentation du scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="f3fd0-103">Electronic Software Distribution-Based Scenario Overview</span></span>


<span data-ttu-id="f3fd0-104">Si vous envisagez d’utiliser une solution de distribution de logiciel électronique (ESD) pour déployer des applications virtuelles, il est important de bien comprendre les facteurs qui entrent en vigueur ou qui sont affectés par cette décision.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-104">If you plan to use an electronic software distribution (ESD) solution to deploy virtual applications, it is important to understand the factors that go into and are affected by that decision.</span></span> <span data-ttu-id="f3fd0-105">Cette rubrique décrit les avantages liés à l’utilisation d’un scénario de type ESD et fournit des informations sur les méthodes de publication et de flux de package que vous devez prendre en compte lors de votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-105">This topic describes the benefits of using an ESD-based scenario and provides information about the publishing and package streaming methods that you will need to consider as you proceed with your deployment.</span></span>

<span data-ttu-id="f3fd0-106">**Important**  Quelle que soit la solution ESD utilisée, vous devez être familiarisé avec les exigences de votre solution particulière.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-106">**Important** Whichever ESD solution you use, you must be familiar with the requirements of your particular solution.</span></span> <span data-ttu-id="f3fd0-107">Si vous utilisez Microsoft Endpoint Configuration Manager, consultez la documentation de Configuration Manager à l’adresse <https://go.microsoft.com/fwlink/?LinkId=66999> .</span><span class="sxs-lookup"><span data-stu-id="f3fd0-107">If you are using Microsoft Endpoint Configuration Manager, see the Configuration Manager documentation at <https://go.microsoft.com/fwlink/?LinkId=66999>.</span></span>

 

<span data-ttu-id="f3fd0-108">L’utilisation d’un système de gestion des opérations ESD existant vous offre les avantages suivants:</span><span class="sxs-lookup"><span data-stu-id="f3fd0-108">Using an existing ESD system provides you with the following benefits:</span></span>

-   <span data-ttu-id="f3fd0-109">Elimine les infrastructures à double gestion</span><span class="sxs-lookup"><span data-stu-id="f3fd0-109">Eliminates dual management infrastructures</span></span>

-   <span data-ttu-id="f3fd0-110">Réduit le coût de votre matériel supplémentaire</span><span class="sxs-lookup"><span data-stu-id="f3fd0-110">Reduces the cost of additional hardware</span></span>

-   <span data-ttu-id="f3fd0-111">Réduit le coût des licences de systèmes d’exploitation et de bases de données supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f3fd0-111">Reduces the cost of additional operating system and database licenses</span></span>

## <span data-ttu-id="f3fd0-112">Méthodes de publication</span><span class="sxs-lookup"><span data-stu-id="f3fd0-112">Publishing Methods</span></span>


<span data-ttu-id="f3fd0-113">Lors de l’utilisation d’un scénario de type ESD, vous avez le choix entre les options suivantes pour publier l’application sur les clients:</span><span class="sxs-lookup"><span data-stu-id="f3fd0-113">When using an ESD-based scenario, you have the following choices for publishing the application to the clients:</span></span>

-   **<span data-ttu-id="f3fd0-114">Programme d’installation Windows autonome.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-114">Stand-alone Windows Installer.</span></span>** <span data-ttu-id="f3fd0-115">Le fichier du programme d’installation Windows contient le manifeste ainsi que les fichiers OSD et ICO utilisés par les clients pour configurer un package.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-115">The Windows Installer file contains the manifest and the OSD and ICO files the clients use to configure a package.</span></span> <span data-ttu-id="f3fd0-116">Le fichier Windows Installer copie également le fichier SFT sur le client, car ce scénario n’utilise pas de serveur.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-116">The Windows Installer file also copies the SFT file to the client because this scenario does not use a server.</span></span>

-   **<span data-ttu-id="f3fd0-117">Windows Installer avec le manifeste du package.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-117">Windows Installer with the package manifest.</span></span>** <span data-ttu-id="f3fd0-118">Le fichier du programme d’installation Windows contient le manifeste ainsi que les fichiers OSD et ICO utilisés par les clients pour configurer un package.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-118">The Windows Installer file contains the manifest and the OSD and ICO files the clients use to configure a package.</span></span> <span data-ttu-id="f3fd0-119">Le fichier SFT est stocké sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-119">The SFT file is stored on a server.</span></span> <span data-ttu-id="f3fd0-120">Un paramètre de ligne de commande dirige le client vers l’emplacement du fichier SFT.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-120">A command-line parameter directs the client to the location of the SFT file.</span></span>

-   **<span data-ttu-id="f3fd0-121">Commandes SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-121">SFTMIME commands.</span></span>** <span data-ttu-id="f3fd0-122">Les commandes SFTMIME sont utilisées avec les fichiers Manifest, OSD, ICO et SFT pour ajouter des packages au client.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-122">SFTMIME commands are used with the manifest, OSD, ICO, and SFT files to add packages to the client.</span></span> <span data-ttu-id="f3fd0-123">Le fichier manifeste doit être disponible sur l’ordinateur client ou être accessible par le biais d’un chemin UNC.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-123">The manifest file must be on the client computer, or it must be accessible through a UNC path.</span></span> <span data-ttu-id="f3fd0-124">En fonction de la configuration du client et des options de ligne de commande, les fichiers OSD, ICO et SFT peuvent être situés sur l’ordinateur client ou sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-124">Depending on the client configuration and the command-line options, the OSD, ICO, and SFT files can be on the client computer or on a server.</span></span>

<span data-ttu-id="f3fd0-125">Pour plus d’informations sur les méthodes de publication précédentes, voir [déterminer votre méthode de publication](determine-your-publishing-method.md).</span><span class="sxs-lookup"><span data-stu-id="f3fd0-125">For more detailed information about the preceding publishing methods, see [Determine Your Publishing Method](determine-your-publishing-method.md).</span></span>

## <span data-ttu-id="f3fd0-126">Méthodes de diffusion de package</span><span class="sxs-lookup"><span data-stu-id="f3fd0-126">Package Streaming Methods</span></span>


<span data-ttu-id="f3fd0-127">Vous devez déterminer la méthode utilisée par votre système de virtualisation d’application pour diffuser en continu les packages d’application virtuelle ou les fichiers SFT du serveur aux clients.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-127">You will need to determine the method your Application Virtualization System will use to stream the virtual application packages, or SFT files, from the server to the clients.</span></span> <span data-ttu-id="f3fd0-128">Les options de streaming suivantes sont disponibles:</span><span class="sxs-lookup"><span data-stu-id="f3fd0-128">The following streaming options are available:</span></span>

-   **<span data-ttu-id="f3fd0-129">Serveur de diffusion en continu d’applications.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-129">Application Virtualization Streaming Server.</span></span>** <span data-ttu-id="f3fd0-130">Si vous utilisez un serveur de diffusion en continu d’applications dans votre configuration, les fichiers SFT sont transmis aux clients à partir de ce serveur à l’aide de protocoles RTSP ou RTSP.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-130">If you use an Application Virtualization Streaming Server in your configuration, the SFT files are streamed to the clients from that server using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="f3fd0-131">Pour installer le logiciel serveur sur un ordinateur, vous devez le configurer par le biais du Registre, mais cette configuration ne dépend pas de services tels que SQL ou services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-131">You must install the server software on a computer and you must configure it through the registry, but this configuration does not depend on services such as SQL or Active Directory Domain Services.</span></span> <span data-ttu-id="f3fd0-132">Les fichiers SFT sont stockés sur le serveur à un emplacement accessible aux clients.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-132">The SFT files are stored on the server at a location accessible by the clients.</span></span> <span data-ttu-id="f3fd0-133">Les informations de publication peuvent être distribuées aux clients via tout mécanisme de distribution.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-133">Publishing information can be distributed to the clients through any distribution mechanism.</span></span> <span data-ttu-id="f3fd0-134">Néanmoins, lors de la configuration, le client reçoit les mises à jour de package automatiquement et la mise à niveau active est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-134">However, when configured, the client receives package upgrades automatically and active upgrade is supported.</span></span>

-   **<span data-ttu-id="f3fd0-135">Serveur de gestion des applications.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-135">Application Virtualization Management Server.</span></span>** <span data-ttu-id="f3fd0-136">Si vous utilisez un serveur de gestion d’application de la virtualisation dans votre configuration, les fichiers SFT sont transmis aux clients à partir de ce serveur à l’aide de protocoles RTSP ou RTSP.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-136">If you use an Application Virtualization Management Server in your configuration, the SFT files are streamed to the clients from that server using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="f3fd0-137">Pour gérer ce serveur, vous devez utiliser la console de gestion Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-137">You manage this server through the Application Virtualization Management Console.</span></span> <span data-ttu-id="f3fd0-138">Cette configuration utilise une base de données SQL et des services Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-138">This configuration uses a SQL database and Active Directory services.</span></span> <span data-ttu-id="f3fd0-139">Le serveur peut distribuer des informations de publication aux clients afin de ne pas avoir besoin de mécanismes de publication supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-139">The server can distribute publishing information to the clients, so additional publishing mechanisms are not needed.</span></span>

-   **<span data-ttu-id="f3fd0-140">Serveur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-140">File server.</span></span>** <span data-ttu-id="f3fd0-141">Si vous utilisez un serveur de fichiers dans votre configuration, les fichiers SFT sont transmis à l’aide de protocoles SMB.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-141">If you use a file server in your configuration, the SFT files are streamed to the other client computers by using SMB protocols.</span></span> <span data-ttu-id="f3fd0-142">Pour gérer les serveurs de fichiers utilisés dans cette configuration, vous devez créer des listes de contrôle d’accès (ACL) sur le partage de fichiers et des fichiers SFT.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-142">File servers used in this configuration are managed by creating access control lists (ACLs) on the file shares and SFT files.</span></span> <span data-ttu-id="f3fd0-143">Il est nécessaire de rediriger les clients vers les fichiers appropriés sur le serveur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-143">Care must be taken to direct the clients to the correct files on the file server.</span></span>

-   **<span data-ttu-id="f3fd0-144">Serveur IIS.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-144">IIS server.</span></span>** <span data-ttu-id="f3fd0-145">Si vous utilisez un serveur IIS dans votre configuration, les fichiers SFT sont transmis aux clients à partir de ce serveur à l’aide de protocoles HTTP ou HTTPs.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-145">If you use an IIS server in your configuration, the SFT files are streamed to the clients from that server using HTTP or HTTPS protocols.</span></span> <span data-ttu-id="f3fd0-146">Le serveur IIS est facile à configurer et à gérer.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-146">The IIS server is easy to configure and manage.</span></span> <span data-ttu-id="f3fd0-147">Il est nécessaire de rediriger les clients vers les fichiers appropriés sur le serveur IIS.</span><span class="sxs-lookup"><span data-stu-id="f3fd0-147">Care must be taken to direct the clients to the correct files on the IIS server.</span></span>

<span data-ttu-id="f3fd0-148">Pour plus d’informations sur les méthodes de streaming précédentes, voir [déterminer la méthode de diffusion en continu](determine-your-streaming-method.md).</span><span class="sxs-lookup"><span data-stu-id="f3fd0-148">For more detailed information about the preceding streaming methods, see [Determine Your Streaming Method](determine-your-streaming-method.md).</span></span>

## <span data-ttu-id="f3fd0-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3fd0-149">Related topics</span></span>


[<span data-ttu-id="f3fd0-150">Paramètres de ligne de commande du programme d'installation d'Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="f3fd0-150">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

[<span data-ttu-id="f3fd0-151">Scénario basé sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="f3fd0-151">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="f3fd0-152">Choisir une méthode de publication</span><span class="sxs-lookup"><span data-stu-id="f3fd0-152">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

[<span data-ttu-id="f3fd0-153">Choisir une méthode de diffusion en continu</span><span class="sxs-lookup"><span data-stu-id="f3fd0-153">Determine Your Streaming Method</span></span>](determine-your-streaming-method.md)

[<span data-ttu-id="f3fd0-154">Scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="f3fd0-154">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="f3fd0-155">Référence de commande SFTMIME</span><span class="sxs-lookup"><span data-stu-id="f3fd0-155">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





