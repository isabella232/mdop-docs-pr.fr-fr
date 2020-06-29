---
title: Scénarios de serveur accessible sur Internet pour les réseaux de périmètre
description: Scénarios de serveur accessible sur Internet pour les réseaux de périmètre
author: dansimp
ms.assetid: 8a4da6e6-82c7-49e5-b9b1-1666cba02f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fcb04e651341fa107c358eaabbd7992d7ea155ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806645"
---
# <span data-ttu-id="6ebad-103">Scénarios de serveur accessible sur Internet pour les réseaux de périmètre</span><span class="sxs-lookup"><span data-stu-id="6ebad-103">Internet-Facing Server Scenarios for Perimeter Networks</span></span>


<span data-ttu-id="6ebad-104">App-V 4.5 prend en charge les scénarios de serveur Internet, dans lesquels les utilisateurs qui ne sont pas connectés au réseau d’entreprise ou qui se déconnectent du réseau peuvent continuer à utiliser App-V.</span><span class="sxs-lookup"><span data-stu-id="6ebad-104">App-V4.5 supports Internet-facing server scenarios, in which users who are not connected to the corporate network or who disconnect from the network can still use App-V.</span></span> <span data-ttu-id="6ebad-105">Comme indiqué dans l’illustration suivante, seules les protocoles sécurisés sur Internet (RTSP et HTTPs) sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6ebad-105">As shown in the following illustration, only the use of secure protocols on the Internet (RTSPS and HTTPS) is supported.</span></span>

![diagramme de positionnement de pare-feu App-v](images/appvfirewalls.gif)

<span data-ttu-id="6ebad-107">Vous pouvez configurer une solution Internet à l’aide d’un serveur ISA sur lequel l’infrastructure App-V se trouve sur le réseau interne comme suit:</span><span class="sxs-lookup"><span data-stu-id="6ebad-107">You can set up an Internet-facing solution, using an ISA Server, where the App-V infrastructure is on the internal network in the following ways:</span></span>

-   <span data-ttu-id="6ebad-108">Créez une règle de publication Web pour le serveur IIS qui héberge les fichiers ICO et OSD (et éventuellement les packages de diffusion en continu) situés sur le réseau interne.</span><span class="sxs-lookup"><span data-stu-id="6ebad-108">Create a Web Publishing rule for the IIS server that is hosting the ICO and OSD files—and optionally, the packages for streaming—located on the internal network.</span></span> <span data-ttu-id="6ebad-109">Des étapes détaillées sont disponibles à l’adresse <https://go.microsoft.com/fwlink/?LinkId=151982> .</span><span class="sxs-lookup"><span data-stu-id="6ebad-109">Detailed steps are provided at <https://go.microsoft.com/fwlink/?LinkId=151982>.</span></span>

-   <span data-ttu-id="6ebad-110">Créer une règle de publication de serveur pour le serveur de gestion des applications (RTSP).</span><span class="sxs-lookup"><span data-stu-id="6ebad-110">Create a Server Publishing rule for the App-V Web Management Server (RTSPS).</span></span> <span data-ttu-id="6ebad-111">Des étapes détaillées sont disponibles à l’adresse [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .</span><span class="sxs-lookup"><span data-stu-id="6ebad-111">Detailed steps are provided at [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983).</span></span>

<span data-ttu-id="6ebad-112">Comme le montre l’illustration ci-dessous, si l’infrastructure a implémenté d’autres pare-feu entre le client et le serveur ISA ou entre le serveur ISA et le réseau interne, vous devez créer des règles de pare-feu RTSP (TCP 322) et HTTPs (TCP 443) pour prendre en charge le flux de trafic.</span><span class="sxs-lookup"><span data-stu-id="6ebad-112">As shown in the following illustration, if the infrastructure has implemented other firewalls between the client and the ISA Server or between the ISA Server and the internal network, both RTSPS (TCP 322) and HTTPS (TCP 443) firewall rules must be created to support the flow of traffic.</span></span> <span data-ttu-id="6ebad-113">De plus, si des pare-feu sont implémentés entre le serveur ISA et le réseau interne, le trafic par défaut requis pour les membres du domaine doit être autorisé à effectuer un tunnel via le pare-feu (DNS, LDAP, Kerberos, SMB/CIFS).</span><span class="sxs-lookup"><span data-stu-id="6ebad-113">Also, if firewalls have been implemented between the ISA Server and the internal network, the default traffic required for domain members must be permitted to tunnel through the firewall (DNS, LDAP, Kerberos, SMB/CIFS).</span></span>

![diagramme de pare-feu du réseau de périmètre App-v](images/appvperimeternetworkfirewall.gif)

<span data-ttu-id="6ebad-115">Étant donné que les solutions de pare-feu varient d’un environnement à un environnement, les recommandations fournies dans cette rubrique décrivent le trafic requis pour configurer un environnement App-V dans le réseau de périmètre.</span><span class="sxs-lookup"><span data-stu-id="6ebad-115">Because the firewall solutions vary from environment to environment, the guidance provided in this topic describes the traffic that would be required to configure an Internet-facing App-V environment in the perimeter network.</span></span> <span data-ttu-id="6ebad-116">Ces informations incluent également les serveurs réseau internes recommandés.</span><span class="sxs-lookup"><span data-stu-id="6ebad-116">This information also includes the recommended internal network servers.</span></span>

<span data-ttu-id="6ebad-117">Placez les serveurs suivants dans le réseau de périmètre:</span><span class="sxs-lookup"><span data-stu-id="6ebad-117">Place the following servers in the perimeter network:</span></span>

-   <span data-ttu-id="6ebad-118">Serveur de gestion App-V</span><span class="sxs-lookup"><span data-stu-id="6ebad-118">App-V Management Server</span></span>

-   <span data-ttu-id="6ebad-119">Serveur IIS pour la publication et la diffusion en continu</span><span class="sxs-lookup"><span data-stu-id="6ebad-119">IIS server for publishing and streaming</span></span>

<span data-ttu-id="6ebad-120">**Remarques**  Il est recommandé de placer le serveur de gestion et le serveur IIS sur des ordinateurs séparés.</span><span class="sxs-lookup"><span data-stu-id="6ebad-120">**Note** It is a best practice to place the Management Server and IIS server on separate computers.</span></span>

 

<span data-ttu-id="6ebad-121">Placez les serveurs suivants sur le réseau interne:</span><span class="sxs-lookup"><span data-stu-id="6ebad-121">Place the following servers in the internal network:</span></span>

-   <span data-ttu-id="6ebad-122">Serveur de contenu</span><span class="sxs-lookup"><span data-stu-id="6ebad-122">Content server</span></span>

-   <span data-ttu-id="6ebad-123">Magasin de données (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="6ebad-123">Data store (SQL Server)</span></span>

-   <span data-ttu-id="6ebad-124">Contrôleur de domaine Active Directory</span><span class="sxs-lookup"><span data-stu-id="6ebad-124">Active Directory Domain Controller</span></span>

## <span data-ttu-id="6ebad-125">Exigences en matière de trafic</span><span class="sxs-lookup"><span data-stu-id="6ebad-125">Traffic Requirements</span></span>


<span data-ttu-id="6ebad-126">Les tableaux suivants répertorient les exigences en matière de trafic pour la communication à partir d’Internet et du réseau de périmètre, et du réseau de périmètre au réseau interne.</span><span class="sxs-lookup"><span data-stu-id="6ebad-126">The following tables list the traffic requirements for communication from the Internet and the perimeter network and from the perimeter network to the internal network.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6ebad-127">Exigences en matière de trafic entre Internet et le réseau de périmètre</span><span class="sxs-lookup"><span data-stu-id="6ebad-127">Traffic Requirements from Internet to Perimeter Network</span></span></th>
<th align="left"><span data-ttu-id="6ebad-128">Détails</span><span class="sxs-lookup"><span data-stu-id="6ebad-128">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6ebad-129">RTSP (actualisation de publication et packages de diffusion en continu)</span><span class="sxs-lookup"><span data-stu-id="6ebad-129">RTSPS (publishing refresh and streaming packages)</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ebad-130">TCP 322 par défaut; vous pouvez le modifier dans le serveur de gestion App-V.</span><span class="sxs-lookup"><span data-stu-id="6ebad-130">TCP 322 by default; this can be changed in App-V Management Server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6ebad-131">HTTPs (publication des fichiers. ICO et OSD et des packages de diffusion en continu)</span><span class="sxs-lookup"><span data-stu-id="6ebad-131">HTTPS (publishing ICO and OSD files and streaming packages)</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ebad-132">TCP 443 par défaut; ce problème peut être modifié dans la configuration IIS.</span><span class="sxs-lookup"><span data-stu-id="6ebad-132">TCP 443 by default; this can be changed in the IIS configuration.</span></span></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6ebad-133">Exigences en matière de trafic du réseau de périmètre vers réseau interne</span><span class="sxs-lookup"><span data-stu-id="6ebad-133">Traffic Requirements from Perimeter Network to Internal Network</span></span></th>
<th align="left"><span data-ttu-id="6ebad-134">Détails</span><span class="sxs-lookup"><span data-stu-id="6ebad-134">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6ebad-135">SQLServer</span><span class="sxs-lookup"><span data-stu-id="6ebad-135">SQL Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ebad-136">TCP 1433 est la valeur par défaut, mais elle peut être configurée dans SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6ebad-136">TCP 1433 is the default but can be configured in SQL Server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6ebad-137">SMB/CIFS</span><span class="sxs-lookup"><span data-stu-id="6ebad-137">SMB/CIFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ebad-138">Si le répertoire de contenu se trouve à distance à partir du ou du serveur de gestion ou du serveur IIS (recommandé).</span><span class="sxs-lookup"><span data-stu-id="6ebad-138">If the content directory is located remotely from the Management Server(s) or IIS server (recommended).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6ebad-139">Kerberos</span><span class="sxs-lookup"><span data-stu-id="6ebad-139">Kerberos</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ebad-140">TCP et UDP 88</span><span class="sxs-lookup"><span data-stu-id="6ebad-140">TCP and UDP 88</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6ebad-141">LDAP</span><span class="sxs-lookup"><span data-stu-id="6ebad-141">LDAP</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ebad-142">TCP et UDP 389</span><span class="sxs-lookup"><span data-stu-id="6ebad-142">TCP and UDP 389</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6ebad-143">DNS</span><span class="sxs-lookup"><span data-stu-id="6ebad-143">DNS</span></span></p></td>
<td align="left"><p><span data-ttu-id="6ebad-144">Pour la résolution de noms des ressources internes (qui peuvent être éliminées lors de l’utilisation du fichier hôte sur les serveurs de réseau de périmètre);</span><span class="sxs-lookup"><span data-stu-id="6ebad-144">For name resolution of internal resources (can be eliminated with the use of host’s file on perimeter network servers)</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





