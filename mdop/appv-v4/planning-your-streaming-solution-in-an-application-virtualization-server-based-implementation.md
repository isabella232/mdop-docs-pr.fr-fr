---
title: Planification de votre solution de diffusion en continu dans une implémentation basée sur un serveur Application Virtualization Server
description: Planification de votre solution de diffusion en continu dans une implémentation basée sur un serveur Application Virtualization Server
author: dansimp
ms.assetid: 3a57306e-5c54-4fde-8593-fe3b788f18d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d315f554eb99fc5c05c231630eaa41d4f505535
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806478"
---
# <span data-ttu-id="f5a72-103">Planification de votre solution de diffusion en continu dans une implémentation basée sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="f5a72-103">Planning Your Streaming Solution in an Application Virtualization Server-Based Implementation</span></span>


<span data-ttu-id="f5a72-104">Si vous souhaitez utiliser des serveurs de diffusion de la virtualisation des applications conjointement avec votre implémentation basée sur le serveur de gestion des applications, vous avez le choix entre plusieurs options, tout en tirant parti de l’infrastructure déjà en place.</span><span class="sxs-lookup"><span data-stu-id="f5a72-104">If you want to use Application Virtualization Streaming Servers in conjunction with your Application Virtualization Management Server-based implementation, you can choose from several alternatives, taking advantage of whatever infrastructure is already in place.</span></span> <span data-ttu-id="f5a72-105">Par exemple, si vous avez déjà des serveurs dans les succursales de votre champ, vous pouvez placer le partage d’application \\CONTENT de partage sur ces serveurs, puis configurer ces derniers pour qu’ils utilisent ce partage de contenu en tant que source de contenu de l’application.</span><span class="sxs-lookup"><span data-stu-id="f5a72-105">For example, if you already have servers in your field branch offices, you can place the Application Virtualization \\CONTENT share on those servers and then configure the clients to use that content share as their application content source.</span></span> <span data-ttu-id="f5a72-106">Si vous choisissez d’utiliser uniquement des serveurs de gestion de la virtualisation des applications (par exemple, vous n’avez qu’un seul bureau), les clients peuvent diffuser du contenu de ce serveur.</span><span class="sxs-lookup"><span data-stu-id="f5a72-106">If you choose to use only Application Virtualization Management Servers—for example, because you have only a single office—the clients can stream content from that server.</span></span>

<span data-ttu-id="f5a72-107">Les options prises en charge sont notamment l’utilisation d’un serveur de fichiers, d’un serveur IIS ou d’un serveur de diffusion de la virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="f5a72-107">The supported options include using a file server, an IIS server, or an Application Virtualization Streaming Server.</span></span> <span data-ttu-id="f5a72-108">Vous pouvez également installer le serveur de diffusion en continu d’applications sur un serveur de fichiers ou un serveur IIS existant.</span><span class="sxs-lookup"><span data-stu-id="f5a72-108">You could also install the Application Virtualization Streaming Server on an existing file server or IIS server.</span></span> <span data-ttu-id="f5a72-109">Les caractéristiques de ces différentes options sont résumées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f5a72-109">The characteristics of these different options are summarized in the following table.</span></span>

<span data-ttu-id="f5a72-110">**Remarques**  La fonction de mise à niveau active vous permet d’ajouter une nouvelle version d’une application à un serveur d’administration d’applications ou un serveur de diffusion en continu sans affecter les utilisateurs exécutant l’application.</span><span class="sxs-lookup"><span data-stu-id="f5a72-110">**Note** The active upgrade feature enables a new version of an application to be added to an App-V Management Server or Streaming Server without affecting users currently running the application.</span></span> <span data-ttu-id="f5a72-111">Les clients App-V recevront automatiquement la version la plus récente de l’application à partir du serveur de gestion App-V ou du serveur de streaming lors du prochain démarrage de l’application par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f5a72-111">The App-V clients will automatically receive the latest version of the application from the App-V Management Server or Streaming Server the next time the user starts the application.</span></span> <span data-ttu-id="f5a72-112">L’utilisation du protocole RTSP (S) est nécessaire pour cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="f5a72-112">Use of the RTSP(S) protocol is required for this feature.</span></span>

 

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
<th align="left"><span data-ttu-id="f5a72-113">Type de serveur</span><span class="sxs-lookup"><span data-stu-id="f5a72-113">Server Type</span></span></th>
<th align="left"><span data-ttu-id="f5a72-114">Protocole</span><span class="sxs-lookup"><span data-stu-id="f5a72-114">Protocol</span></span></th>
<th align="left"><span data-ttu-id="f5a72-115">Avantages</span><span class="sxs-lookup"><span data-stu-id="f5a72-115">Advantages</span></span></th>
<th align="left"><span data-ttu-id="f5a72-116">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="f5a72-116">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="f5a72-117">Liens</span><span class="sxs-lookup"><span data-stu-id="f5a72-117">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5a72-118">Serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="f5a72-118">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5a72-119">SMB</span><span class="sxs-lookup"><span data-stu-id="f5a72-119">SMB</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f5a72-120">Solution simple et abordable pour configurer un serveur de fichiers existant avec le partage \CONTENT</span><span class="sxs-lookup"><span data-stu-id="f5a72-120">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f5a72-121">Aucune mise à niveau active</span><span class="sxs-lookup"><span data-stu-id="f5a72-121">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="f5a72-122">Procédure pour configurer le serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="f5a72-122">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5a72-123">Serveur IIS</span><span class="sxs-lookup"><span data-stu-id="f5a72-123">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5a72-124">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="f5a72-124">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f5a72-125">Prend en charge la sécurité améliorée via le protocole HTTPs</span><span class="sxs-lookup"><span data-stu-id="f5a72-125">Supports enhanced security using HTTPS protocol</span></span></p></li>
<li><p><span data-ttu-id="f5a72-126">Prend en charge la diffusion en continu sur des ordinateurs distants via Internet</span><span class="sxs-lookup"><span data-stu-id="f5a72-126">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="f5a72-127">Un seul port du pare-feu pour s’ouvrir</span><span class="sxs-lookup"><span data-stu-id="f5a72-127">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="f5a72-128">Evolutive</span><span class="sxs-lookup"><span data-stu-id="f5a72-128">Scalable</span></span></p></li>
<li><p><span data-ttu-id="f5a72-129">Protocole familier</span><span class="sxs-lookup"><span data-stu-id="f5a72-129">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f5a72-130">Vous devez gérer les services Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="f5a72-130">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="f5a72-131">Aucune mise à niveau active</span><span class="sxs-lookup"><span data-stu-id="f5a72-131">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="f5a72-132">Procédure pour configurer le serveur IIS</span><span class="sxs-lookup"><span data-stu-id="f5a72-132">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5a72-133">Serveur de streaming de la virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="f5a72-133">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5a72-134">RTSP/RTSP</span><span class="sxs-lookup"><span data-stu-id="f5a72-134">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f5a72-135">Mise à niveau active</span><span class="sxs-lookup"><span data-stu-id="f5a72-135">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="f5a72-136">Prend en charge la sécurité améliorée à l’aide du protocole RTSP</span><span class="sxs-lookup"><span data-stu-id="f5a72-136">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="f5a72-137">Un seul port du pare-feu pour s’ouvrir</span><span class="sxs-lookup"><span data-stu-id="f5a72-137">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f5a72-138">Double infrastructure</span><span class="sxs-lookup"><span data-stu-id="f5a72-138">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="f5a72-139">Configuration requise pour l’administration du serveur</span><span class="sxs-lookup"><span data-stu-id="f5a72-139">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)"><span data-ttu-id="f5a72-140">Procédure pour configurer les serveurs Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="f5a72-140">How to Configure the Application Virtualization Streaming Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5a72-141">Serveur de gestion Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f5a72-141">Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5a72-142">RTSP/RTSP</span><span class="sxs-lookup"><span data-stu-id="f5a72-142">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f5a72-143">Mise à niveau active</span><span class="sxs-lookup"><span data-stu-id="f5a72-143">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="f5a72-144">Prend en charge la sécurité améliorée à l’aide du protocole RTSP</span><span class="sxs-lookup"><span data-stu-id="f5a72-144">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="f5a72-145">Un seul port du pare-feu pour s’ouvrir</span><span class="sxs-lookup"><span data-stu-id="f5a72-145">Only one port in firewall to open</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f5a72-146">Double infrastructure</span><span class="sxs-lookup"><span data-stu-id="f5a72-146">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="f5a72-147">Configuration requise pour l’administration du serveur</span><span class="sxs-lookup"><span data-stu-id="f5a72-147">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="f5a72-148">Procédure pour configurer les serveurs Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="f5a72-148">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f5a72-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f5a72-149">Related topics</span></span>


[<span data-ttu-id="f5a72-150">Scénario basé sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="f5a72-150">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="f5a72-151">Présentation des composants du système Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f5a72-151">Overview of the Application Virtualization System Components</span></span>](overview-of-the-application-virtualization-system-components.md)

[<span data-ttu-id="f5a72-152">Publication d'applications virtuelles à l'aide de serveurs Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="f5a72-152">Publishing Virtual Applications Using Application Virtualization Management Servers</span></span>](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





