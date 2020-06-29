---
title: Choisir une méthode de diffusion en continu
description: Choisir une méthode de diffusion en continu
author: dansimp
ms.assetid: 50d5e0ec-7f48-4cea-8711-5882bd89153b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0acfd345ac55f11476cffe94b3a95b13c5d8f303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808892"
---
# <span data-ttu-id="b237b-103">Choisir une méthode de diffusion en continu</span><span class="sxs-lookup"><span data-stu-id="b237b-103">Determine Your Streaming Method</span></span>


<span data-ttu-id="b237b-104">Lorsque l’utilisateur double-clique pour la première fois sur l’icône placée sur un ordinateur par le biais du processus de publication, le client de virtualisation d’application obtiendra le contenu du package d’application virtuelle à partir d’un emplacement de source de flux.</span><span class="sxs-lookup"><span data-stu-id="b237b-104">The first time that a user double-clicks the icon that has been placed on a computer through the publishing process, the Application Virtualization client will obtain the virtual application package content from a streaming source location.</span></span>

<span data-ttu-id="b237b-105">**Remarques** 
 *Streaming* est le terme utilisé pour décrire le processus d’obtention de contenu à partir d’un package d’application séquencé, en commençant par le bloc de fonctionnalités principal et en obtenant des blocs supplémentaires selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="b237b-105">**Note**
*Streaming* is the term used to describe the process of obtaining content from a sequenced application package, starting with the primary feature block and then obtaining additional blocks as needed.</span></span>

 

<span data-ttu-id="b237b-106">En général, l’emplacement de la source est un serveur accessible à partir de l’ordinateur de l’utilisateur. Toutefois, certains systèmes de distribution électronique, tels que Microsoft Endpoint Configuration Manager, peuvent distribuer le fichier SFT sur l’ordinateur de l’utilisateur, puis diffuser le package de l’application virtuelle localement à partir du cache de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b237b-106">The streaming source location is usually a server that is accessible by the user’s computer; however, some electronic distribution systems, such as Microsoft Endpoint Configuration Manager, can distribute the SFT file to the user’s computer and then stream the virtual application package locally from that computer’s cache.</span></span>

<span data-ttu-id="b237b-107">**Remarques**  Un emplacement de source de flux pour les packages virtuels peut être configuré sur un ordinateur qui n’est pas un serveur.</span><span class="sxs-lookup"><span data-stu-id="b237b-107">**Note** A streaming source location for virtual packages can be set up on a computer that is not a server.</span></span> <span data-ttu-id="b237b-108">Cette fonction est particulièrement utile dans les petites succursales qui n’ont pas de serveur.</span><span class="sxs-lookup"><span data-stu-id="b237b-108">This is especially useful in a small branch office that has no server.</span></span>

 

<span data-ttu-id="b237b-109">Les sources de flux continu qui peuvent être utilisées pour stocker des applications séquencées sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b237b-109">The streaming sources that can be used to store sequenced applications are described in the following table.</span></span>

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
<th align="left"><span data-ttu-id="b237b-110">Type de serveur</span><span class="sxs-lookup"><span data-stu-id="b237b-110">Server Type</span></span></th>
<th align="left"><span data-ttu-id="b237b-111">Protocole</span><span class="sxs-lookup"><span data-stu-id="b237b-111">Protocol</span></span></th>
<th align="left"><span data-ttu-id="b237b-112">Avantages</span><span class="sxs-lookup"><span data-stu-id="b237b-112">Advantages</span></span></th>
<th align="left"><span data-ttu-id="b237b-113">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="b237b-113">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="b237b-114">Liens</span><span class="sxs-lookup"><span data-stu-id="b237b-114">Links</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b237b-115">Serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="b237b-115">File server</span></span></p></td>
<td align="left"><p><span data-ttu-id="b237b-116">Fichier</span><span class="sxs-lookup"><span data-stu-id="b237b-116">File</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b237b-117">Solution simple et abordable pour configurer un serveur de fichiers existant avec le partage \CONTENT</span><span class="sxs-lookup"><span data-stu-id="b237b-117">Simple low-cost solution to configure existing file server with \CONTENT share</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b237b-118">Aucune mise à niveau active</span><span class="sxs-lookup"><span data-stu-id="b237b-118">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)"><span data-ttu-id="b237b-119">Procédure pour configurer le serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="b237b-119">How to Configure the File Server</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b237b-120">Serveur IIS</span><span class="sxs-lookup"><span data-stu-id="b237b-120">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="b237b-121">HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="b237b-121">HTTP/ HTTPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b237b-122">Prend en charge la sécurité améliorée via le protocole HTTPs.</span><span class="sxs-lookup"><span data-stu-id="b237b-122">Supports enhanced security using HTTPS protocol.</span></span></p></li>
<li><p><span data-ttu-id="b237b-123">Prend en charge la diffusion en continu sur des ordinateurs distants via Internet</span><span class="sxs-lookup"><span data-stu-id="b237b-123">Supports streaming to remote computers across the Internet</span></span></p></li>
<li><p><span data-ttu-id="b237b-124">Un seul port du pare-feu pour s’ouvrir</span><span class="sxs-lookup"><span data-stu-id="b237b-124">Only one port in firewall to open</span></span></p></li>
<li><p><span data-ttu-id="b237b-125">Haute évolutivité</span><span class="sxs-lookup"><span data-stu-id="b237b-125">Highly scalable</span></span></p></li>
<li><p><span data-ttu-id="b237b-126">Protocole familier</span><span class="sxs-lookup"><span data-stu-id="b237b-126">Familiar protocol</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b237b-127">Vous devez gérer les services Internet (IIS)</span><span class="sxs-lookup"><span data-stu-id="b237b-127">Need to manage IIS</span></span></p></li>
<li><p><span data-ttu-id="b237b-128">Aucune mise à niveau active</span><span class="sxs-lookup"><span data-stu-id="b237b-128">No active upgrade</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)"><span data-ttu-id="b237b-129">Procédure pour configurer le serveur IIS</span><span class="sxs-lookup"><span data-stu-id="b237b-129">How to Configure the Server for IIS</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b237b-130">Serveur de streaming de la virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="b237b-130">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="b237b-131">RTSP/RTSP</span><span class="sxs-lookup"><span data-stu-id="b237b-131">RTSP/ RTSPS</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b237b-132">Mise à niveau active</span><span class="sxs-lookup"><span data-stu-id="b237b-132">Active upgrade</span></span></p></li>
<li><p><span data-ttu-id="b237b-133">Prend en charge la sécurité améliorée à l’aide du protocole RTSP</span><span class="sxs-lookup"><span data-stu-id="b237b-133">Supports enhanced security using RTSPS protocol</span></span></p></li>
<li><p><span data-ttu-id="b237b-134">Un seul port dans le pare-feu pour s’ouvrir (RTSP uniquement)</span><span class="sxs-lookup"><span data-stu-id="b237b-134">Only one port in firewall to open (RTSPS only)</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b237b-135">Double infrastructure</span><span class="sxs-lookup"><span data-stu-id="b237b-135">Dual infrastructure</span></span></p></li>
<li><p><span data-ttu-id="b237b-136">Configuration requise pour l’administration du serveur</span><span class="sxs-lookup"><span data-stu-id="b237b-136">Server administration requirement</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)"><span data-ttu-id="b237b-137">Procédure pour configurer les serveurs Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="b237b-137">How to Configure the Application Virtualization Management Servers</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b237b-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b237b-138">Related topics</span></span>


[<span data-ttu-id="b237b-139">Scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="b237b-139">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="b237b-140">Présentation du scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="b237b-140">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)

[<span data-ttu-id="b237b-141">Choisir une méthode de publication</span><span class="sxs-lookup"><span data-stu-id="b237b-141">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

 

 





