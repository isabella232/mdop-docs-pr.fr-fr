---
title: Planification de votre solution de diffusion en continu dans une implémentation de distribution électronique de logiciels
description: Planification de votre solution de diffusion en continu dans une implémentation de distribution électronique de logiciels
author: dansimp
ms.assetid: bc18772a-f169-486f-adb1-7af1a31845aa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c49d6fc0b5f8f5dee347ead3bb899ce9b0387024
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806474"
---
# <span data-ttu-id="a7dfa-103">Planification de votre solution de diffusion en continu dans une implémentation de distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="a7dfa-103">Planning Your Streaming Solution in an Electronic Software Distribution Implementation</span></span>


<span data-ttu-id="a7dfa-104">Si vous décidez d’utiliser des serveurs de diffusion en conjonction avec votre système de maintenance ESD pour rendre le contenu de l’application disponible pour les ordinateurs des utilisateurs finaux, vous pouvez choisir parmi plusieurs options, tout en tirant parti de l’infrastructure qui est déjà en place.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-104">If you decide to use streaming servers in conjunction with your ESD system to make application content available to your end user computers, you can choose from several alternatives, taking advantage of whatever infrastructure is already in place.</span></span> <span data-ttu-id="a7dfa-105">Par exemple, si votre système ESD comporte des partages de logiciels de distribution de logiciels sur des serveurs dans les succursales de votre domaine, vous pouvez placer le partage de l’application virtualisation \\CONTENT sur ces serveurs, puis configurer les clients pour qu’ils utilisent ce partage de contenu comme source de contenu de l’application.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-105">For example, if your ESD system has software distribution shares on servers in your field branch offices, you can place the Application Virtualization \\CONTENT share on those servers and then configure the clients to use that content share as their application content source.</span></span> <span data-ttu-id="a7dfa-106">L’utilisation des options prises en charge consiste à utiliser un serveur de fichiers ou un serveur IIS.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-106">The supported options include using a file server or an IIS server.</span></span> <span data-ttu-id="a7dfa-107">Vous pouvez également installer le serveur de diffusion en continu d’applications sur un serveur de fichiers ou un serveur IIS existant.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-107">You could also install the Application Virtualization Streaming Server on an existing file server or IIS server.</span></span>

<span data-ttu-id="a7dfa-108">Le serveur de diffusion en continu d’applications prend en charge la fonctionnalité de mise à niveau active de la virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-108">The Application Virtualization Streaming Server provides support for the active upgrade feature in Application Virtualization.</span></span> <span data-ttu-id="a7dfa-109">La fonction de mise à niveau active vous permet d’ajouter une nouvelle version d’une application à un serveur d’administration d’applications ou un serveur de diffusion en continu sans affecter les utilisateurs exécutant l’application.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-109">The active upgrade feature enables a new version of an application to be added to an App-V Management Server or Streaming Server without affecting users currently running the application.</span></span> <span data-ttu-id="a7dfa-110">Les clients App-V recevront automatiquement la version la plus récente de l’application à partir du serveur de gestion App-V ou du serveur de streaming lors du prochain démarrage de l’application par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-110">The App-V clients will automatically receive the latest version of the application from the App-V Management Server or Streaming Server the next time the user starts the application.</span></span> <span data-ttu-id="a7dfa-111">L’utilisation du protocole RTSP (S) est nécessaire pour cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-111">Use of the RTSP(S) protocol is required for this feature.</span></span> <span data-ttu-id="a7dfa-112">Si vous choisissez de ne pas utiliser le serveur de diffusion en continu d’applications, vous devrez gérer explicitement les mises à jour de package d’application à l’aide du système ESD.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-112">If you choose not to use the Application Virtualization Streaming Server, you will need to explicitly manage application package upgrades by using the ESD system.</span></span>

<span data-ttu-id="a7dfa-113">**Remarques**  L’accès aux applications est contrôlé par le biais des groupes de sécurité dans les services de domaine Active Directory (AD FS), vous devez donc planifier un processus de configuration d’un groupe de sécurité pour chaque application virtuelle et de gestion des utilisateurs ajoutés à chaque groupe.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-113">**Note** Access to the applications is controlled by means of Security Groups in Active Directory Domain Services, so you will need to plan a process for setting up a security group for each virtual application and for managing which users are added to each group.</span></span> <span data-ttu-id="a7dfa-114">L’administrateur système de virtualisation des applications configure chaque serveur en streaming pour utiliser ces groupes Active Directory en appliquant des LCA aux répertoires de l’application sous le partage de contenu, qui contrôle l’accès aux packages en fonction de l’appartenance aux groupes Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-114">The Application Virtualization system administrator configures each streaming server to use these Active Directory groups by applying ACLs to the application directories under the CONTENT share, which controls access to the packages based on Active Directory group membership.</span></span>

 

<span data-ttu-id="a7dfa-115">Les caractéristiques des options de streaming disponibles sont résumées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a7dfa-115">The characteristics of the available streaming options are summarized in the following table.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a7dfa-116">Type de serveur</span><span class="sxs-lookup"><span data-stu-id="a7dfa-116">Server Type</span></span></th>
<th align="left"><span data-ttu-id="a7dfa-117">Protocole</span><span class="sxs-lookup"><span data-stu-id="a7dfa-117">Protocol</span></span></th>
<th align="left"><span data-ttu-id="a7dfa-118">Avantages</span><span class="sxs-lookup"><span data-stu-id="a7dfa-118">Advantages</span></span></th>
<th align="left"><span data-ttu-id="a7dfa-119">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="a7dfa-119">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="a7dfa-120">Liens</span><span class="sxs-lookup"><span data-stu-id="a7dfa-120">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7dfa-121">Serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="a7dfa-121">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7dfa-122">SMB</span><span class="sxs-lookup"><span data-stu-id="a7dfa-122">SMB</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a7dfa-123">Solution simple et abordable pour configurer un serveur de fichiers existant avec le partage \CONTENT</span><span class="sxs-lookup"><span data-stu-id="a7dfa-123">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a7dfa-124">Aucune mise à niveau active</span><span class="sxs-lookup"><span data-stu-id="a7dfa-124">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="a7dfa-125">Procédure pour configurer le serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="a7dfa-125">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a7dfa-126">Serveur IIS</span><span class="sxs-lookup"><span data-stu-id="a7dfa-126">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7dfa-127">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="a7dfa-127">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a7dfa-128">Prend en charge la sécurité améliorée via le protocole HTTPs</span><span class="sxs-lookup"><span data-stu-id="a7dfa-128">Supports enhanced security using HTTPS protocol</span></span></p></li>
<li><p><span data-ttu-id="a7dfa-129">Prend en charge la diffusion en continu sur des ordinateurs distants via Internet</span><span class="sxs-lookup"><span data-stu-id="a7dfa-129">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="a7dfa-130">Un seul port du pare-feu pour s’ouvrir</span><span class="sxs-lookup"><span data-stu-id="a7dfa-130">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="a7dfa-131">Evolutive</span><span class="sxs-lookup"><span data-stu-id="a7dfa-131">Scalable</span></span></p></li>
<li><p><span data-ttu-id="a7dfa-132">Protocole familier</span><span class="sxs-lookup"><span data-stu-id="a7dfa-132">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a7dfa-133">Vous devez gérer les services Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="a7dfa-133">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="a7dfa-134">Aucune mise à niveau active</span><span class="sxs-lookup"><span data-stu-id="a7dfa-134">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="a7dfa-135">Procédure pour configurer le serveur IIS</span><span class="sxs-lookup"><span data-stu-id="a7dfa-135">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a7dfa-136">Serveur de streaming de la virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="a7dfa-136">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="a7dfa-137">RTSP/RTSP</span><span class="sxs-lookup"><span data-stu-id="a7dfa-137">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a7dfa-138">Mise à niveau active</span><span class="sxs-lookup"><span data-stu-id="a7dfa-138">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="a7dfa-139">Prend en charge la sécurité améliorée à l’aide du protocole RTSP</span><span class="sxs-lookup"><span data-stu-id="a7dfa-139">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="a7dfa-140">Un seul port du pare-feu pour s’ouvrir</span><span class="sxs-lookup"><span data-stu-id="a7dfa-140">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a7dfa-141">Double infrastructure</span><span class="sxs-lookup"><span data-stu-id="a7dfa-141">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="a7dfa-142">Configuration requise pour l’administration du serveur</span><span class="sxs-lookup"><span data-stu-id="a7dfa-142">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="a7dfa-143">Procédure pour configurer les serveurs Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="a7dfa-143">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a7dfa-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7dfa-144">Related topics</span></span>


[<span data-ttu-id="a7dfa-145">Procédure pour configurer des serveurs pour un déploiement basé sur ESD</span><span class="sxs-lookup"><span data-stu-id="a7dfa-145">How to Configure Servers for ESD-Based Deployment</span></span>](how-to-configure-servers-for-esd-based-deployment.md)

[<span data-ttu-id="a7dfa-146">Vue d'ensemble de la sécurité et de la protection</span><span class="sxs-lookup"><span data-stu-id="a7dfa-146">Security and Protection Overview</span></span>](security-and-protection-overview.md)

[<span data-ttu-id="a7dfa-147">Publication d'applications virtuelles à l'aide de la distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="a7dfa-147">Publishing Virtual Applications Using Electronic Software Distribution</span></span>](publishing-virtual-applications-using-electronic-software-distribution.md)

 

 





