---
title: Présentation du scénario basé sur un serveur Application Virtualization Server
description: Présentation du scénario basé sur un serveur Application Virtualization Server
author: dansimp
ms.assetid: 2d91392b-5085-4a5d-94f2-15eed1ed2928
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b3ac3f10a5b7c7705e6d72c122d52be801a6d50
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809149"
---
# <span data-ttu-id="87019-103">Présentation du scénario basé sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="87019-103">Application Virtualization Server-Based Scenario Overview</span></span>


<span data-ttu-id="87019-104">Si vous envisagez d’utiliser un scénario de déploiement basé sur serveur pour votre environnement Microsoft Application Virtualization, il est important de comprendre les différences entre le serveur de gestion de la *virtualisation des applications* et le serveur de diffusion de la virtualisation de l' *application*.</span><span class="sxs-lookup"><span data-stu-id="87019-104">If you plan to use a server-based deployment scenario for your Microsoft Application Virtualization environment, it is important to understand the differences between the *Application Virtualization Management Server* and the *Application Virtualization Streaming Server*.</span></span> <span data-ttu-id="87019-105">Cette rubrique décrit ces différences et fournit des informations sur les méthodes de remise des packages, les protocoles de transmission et les composants externes que vous devez prendre en considération lorsque vous effectuez votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="87019-105">This topic describes those differences and also provides information about package delivery methods, transmission protocols, and external components that you will need to consider as you proceed with your deployment.</span></span>

## <span data-ttu-id="87019-106">Serveur de gestion Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="87019-106">Application Virtualization Management Server</span></span>


<span data-ttu-id="87019-107">Le serveur de gestion de la virtualisation des applications effectue la fonction de publication et la fonction streaming.</span><span class="sxs-lookup"><span data-stu-id="87019-107">The Application Virtualization Management Server performs both the publishing function and the streaming function.</span></span> <span data-ttu-id="87019-108">Le serveur publie des icônes d’application, des raccourcis et des associations de type de fichier vers les clients App-V pour les utilisateurs autorisés.</span><span class="sxs-lookup"><span data-stu-id="87019-108">The server publishes application icons, shortcuts, and file type associations to the App-V clients for authorized users.</span></span> <span data-ttu-id="87019-109">Lors de la réception de demandes d’applications par l’utilisateur, le serveur transmet les flux de données à la demande aux utilisateurs autorisés utilisant des protocoles RTSP ou RTSP.</span><span class="sxs-lookup"><span data-stu-id="87019-109">When user requests for applications are received the server streams that data on-demand to authorized users using RTSP or RTSPS protocols.</span></span> <span data-ttu-id="87019-110">Dans la plupart des configurations utilisant ce serveur, un ou plusieurs serveurs de gestion partagent un magasin de données commun pour la configuration et les informations de package.</span><span class="sxs-lookup"><span data-stu-id="87019-110">In most configurations using this server, one or more Management Servers share a common data store for configuration and package information.</span></span>

<span data-ttu-id="87019-111">Les serveurs d’administration de la virtualisation des applications utilisent des groupes Active Directory pour gérer les autorisations des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="87019-111">The Application Virtualization Management Servers use Active Directory groups to manage user authorization.</span></span> <span data-ttu-id="87019-112">Outre les services de domaine Active Directory (AD FS), vous avez installé SQL Server pour gérer la base de données et le magasin de données.</span><span class="sxs-lookup"><span data-stu-id="87019-112">In addition to Active Directory Domain Services, these servers have SQL Server installed to manage the database and data store.</span></span> <span data-ttu-id="87019-113">Le serveur de gestion est contrôlé par le biais de la console de gestion des applications virtuelles, un composant logiciel enfichable à la console de gestion Microsoft.</span><span class="sxs-lookup"><span data-stu-id="87019-113">The Management Server is controlled through the Application Virtualization Management Console, a snap-in to the Microsoft Management Console.</span></span>

<span data-ttu-id="87019-114">Étant donné que les serveurs de gestion de l’application de la virtualisation de l’application les applications en utilisateurs finaux à la demande, ces serveurs sont idéalement adaptés aux configurations système qui disposent de réseaux locaux de grande bande passante et fiable.</span><span class="sxs-lookup"><span data-stu-id="87019-114">Because the Application Virtualization Management Servers stream applications to end-users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span>

## <span data-ttu-id="87019-115">Serveur de streaming de la virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="87019-115">Application Virtualization Streaming Server</span></span>


<span data-ttu-id="87019-116">Le serveur de diffusion en continu d’application fournit les mêmes fonctionnalités de mise à niveau de package et de mise à niveau de package fournies par le serveur de gestion, mais sans application Active Directory ou SQL Server requise.</span><span class="sxs-lookup"><span data-stu-id="87019-116">The Application Virtualization Streaming Server delivers the same streaming and package upgrade capabilities provided by the Management Server, but without its Active Directory or SQL Server requirements.</span></span> <span data-ttu-id="87019-117">Toutefois, le serveur de diffusion en continu ne possède pas de service de publication et ne dispose pas de capacités de licence ou de mesure de la gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="87019-117">However, the Streaming Server does not have a publishing service, nor does it have licensing or metering capabilities.</span></span> <span data-ttu-id="87019-118">Le service de publication d’un serveur de gestion App-V distinct est utilisé conjointement avec le serveur de streaming App-V.</span><span class="sxs-lookup"><span data-stu-id="87019-118">The publishing service of a separate App-V Management Server is used in conjunction with the App-V Streaming Server.</span></span> <span data-ttu-id="87019-119">Le serveur de streaming App-V répond aux besoins des entreprises qui souhaitent utiliser la virtualisation des applications à plusieurs endroits grâce aux fonctionnalités de streaming de la configuration de serveur classique, mais peut ne pas disposer de l’infrastructure pour la prise en charge des serveurs d’administration d’applications-V dans chaque emplacement.</span><span class="sxs-lookup"><span data-stu-id="87019-119">The App-V Streaming Server addresses the needs of businesses that want to use Application Virtualization in multiple locations with the streaming capabilities of the classic server configuration but might not have the infrastructure to support App-V Management Servers in every location.</span></span>

<span data-ttu-id="87019-120">Le serveur de diffusion en continu d’applications peut également être utilisé dans les environnements avec un système de distribution de logiciels électronique (ESD) existant.</span><span class="sxs-lookup"><span data-stu-id="87019-120">The Application Virtualization Streaming Server can also be used in environments with an existing electronic software distribution system (ESD).</span></span> <span data-ttu-id="87019-121">La gestion des applications de diffusion en continu utilise une utilisation ESD.</span><span class="sxs-lookup"><span data-stu-id="87019-121">You use the ESD to manage streaming applications.</span></span> <span data-ttu-id="87019-122">Contrairement au serveur de gestion de la virtualisation des applications, le serveur de diffusion en continu n’utilise pas SQL ou la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="87019-122">Unlike the Application Virtualization Management Server, the Streaming Server does not use SQL or a management console.</span></span> <span data-ttu-id="87019-123">Ces serveurs utilisent des listes de contrôle d’accès (ACL) pour accorder l’autorisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="87019-123">These servers use access control lists (ACLs) to grant user authorization.</span></span>

## <span data-ttu-id="87019-124">Méthodes de remise du package</span><span class="sxs-lookup"><span data-stu-id="87019-124">Package Delivery Methods</span></span>


<span data-ttu-id="87019-125">Si vous envisagez d’utiliser un serveur de virtualisation d’application en tant que méthode de remise de publication, vous devez déterminer qui utilise les méthodes de remise de package suivantes:</span><span class="sxs-lookup"><span data-stu-id="87019-125">If you plan to use an Application Virtualization Server as the publishing delivery method, you need to determine which of the following package delivery methods your scenario employs:</span></span>

-   *<span data-ttu-id="87019-126">Remise de package dynamique</span><span class="sxs-lookup"><span data-stu-id="87019-126">Dynamic package delivery</span></span>*

-   *<span data-ttu-id="87019-127">Charger à partir du fichier remise du package</span><span class="sxs-lookup"><span data-stu-id="87019-127">Load from file package delivery</span></span>*

### <span data-ttu-id="87019-128">Remise de package dynamique</span><span class="sxs-lookup"><span data-stu-id="87019-128">Dynamic Package Delivery</span></span>

<span data-ttu-id="87019-129">Lors de la remise d’un package dynamique, le serveur (Application Virtualization Management Server, serveur de diffusion en continu d’applications ou serveur IIS) fournit aux utilisateurs finaux des applications virtualisées par le biais du déploiement à la demande.</span><span class="sxs-lookup"><span data-stu-id="87019-129">During dynamic package delivery, the server (Application Virtualization Management Server, Application Virtualization Streaming Server, or IIS server) delivers the virtualized applications to the end users through on-demand deployment.</span></span> <span data-ttu-id="87019-130">Le serveur fournit les applications et packages virtualisés à un ordinateur client uniquement lorsqu’un utilisateur tente d’abord de lancer une application (à la demande).</span><span class="sxs-lookup"><span data-stu-id="87019-130">The server delivers the virtualized applications and packages to a client computer only when a user first attempts to launch an application (on demand).</span></span> <span data-ttu-id="87019-131">Le serveur transmet uniquement les blocs nécessaires pour démarrer l’application (bloc de fonctionnalité principal).</span><span class="sxs-lookup"><span data-stu-id="87019-131">The server streams only the blocks needed to start the application (primary feature block).</span></span> <span data-ttu-id="87019-132">Lorsque le bloc de fonctionnalité principal est remis au client, l’application s’exécute. le client ne reçoit pas l’application complète (déploiement incrémental), sauf si le client a besoin d’accéder à une partie de l’application qui n’est pas incluse dans le bloc de fonctionnalités principal.</span><span class="sxs-lookup"><span data-stu-id="87019-132">After the primary feature block is delivered to the client, the application runs; the client does not receive the complete application (incremental deployment) unless the client needs access to a part of the application that is not included in the primary feature block.</span></span> <span data-ttu-id="87019-133">Lorsque cela se produit, le client effectue une requête d’absence de séquence et le bloc de fonctionnalité secondaire est transmis au client.</span><span class="sxs-lookup"><span data-stu-id="87019-133">When this occurs, the client performs an out-of-sequence request and the secondary feature block is streamed to the client.</span></span> <span data-ttu-id="87019-134">La remise de packages dynamique permet un lancement rapide des applications.</span><span class="sxs-lookup"><span data-stu-id="87019-134">Dynamic package delivery allows for rapid application launch.</span></span>

### <span data-ttu-id="87019-135">Charger à partir du fichier remise du package</span><span class="sxs-lookup"><span data-stu-id="87019-135">Load from File Package Delivery</span></span>

<span data-ttu-id="87019-136">Dans le cas d’un chargement à partir d’un package de fichier, le serveur remet l’intégralité du package de l’application virtualisée sur un ordinateur client avant que l’utilisateur ne lance l’application.</span><span class="sxs-lookup"><span data-stu-id="87019-136">For load from file package delivery, the server delivers the entire virtualized application package to a client computer before the user launches the application.</span></span> <span data-ttu-id="87019-137">Dans ce scénario, les applications virtualisées sont transmises en tant que package complet, plutôt que par le biais de la méthode dynamique et incrémentielle utilisée par le modèle de remise dynamique.</span><span class="sxs-lookup"><span data-stu-id="87019-137">In this scenario, virtualized applications are delivered as a full package, rather than through the dynamic, incremental method used by the dynamic delivery model.</span></span>

<span data-ttu-id="87019-138">**Remarques**  Pour chaque méthode de remise, le processus de remise initial des applications virtuelles et le processus de mise à jour des applications virtuelles sont les mêmes. le package d’application virtuelle mis à jour remplace le package d’application d’origine.</span><span class="sxs-lookup"><span data-stu-id="87019-138">**Note** For each delivery method, the initial virtual application delivery process and the virtual application update process are the same; the updated virtual application package replaces the original application package.</span></span>

 

<span data-ttu-id="87019-139">Le tableau suivant compare les avantages et inconvénients de chaque méthode de remise du package.</span><span class="sxs-lookup"><span data-stu-id="87019-139">The following table compares the advantages and disadvantages of each package delivery method.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="87019-140">Méthode</span><span class="sxs-lookup"><span data-stu-id="87019-140">Method</span></span></th>
<th align="left"><span data-ttu-id="87019-141">Avantages</span><span class="sxs-lookup"><span data-stu-id="87019-141">Advantages</span></span></th>
<th align="left"><span data-ttu-id="87019-142">Inconvénients</span><span class="sxs-lookup"><span data-stu-id="87019-142">Disadvantages</span></span></th>
<th align="left"><span data-ttu-id="87019-143">Commentaires</span><span class="sxs-lookup"><span data-stu-id="87019-143">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87019-144">Remise de package dynamique</span><span class="sxs-lookup"><span data-stu-id="87019-144">Dynamic package delivery</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-145">Les applications sont transmises et mises à jour à la demande.</span><span class="sxs-lookup"><span data-stu-id="87019-145">Applications are delivered and updated on demand.</span></span></p>
<p><span data-ttu-id="87019-146">Les applications sont transmises et mises à jour de façon incrémentielle pour optimiser le temps de démarrage.</span><span class="sxs-lookup"><span data-stu-id="87019-146">Applications are delivered and updated incrementally to optimize launch time.</span></span></p>
<p><span data-ttu-id="87019-147">Des mises à jour sont automatiquement transmises au Bureau du client.</span><span class="sxs-lookup"><span data-stu-id="87019-147">Updates are delivered automatically to the client desktop.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-148">Encombrement plus important dans la topologie d’entreprise en raison de la configuration requise du serveur.</span><span class="sxs-lookup"><span data-stu-id="87019-148">Larger footprint in enterprise topology because of server requirements.</span></span></p>
<p><span data-ttu-id="87019-149">La diffusion d’application doit être via un réseau local. les scénarios de déploiement sur un réseau WAN ou qui utilisent une connexion intermittente ou peu fiable entre le serveur et le client peuvent être inutilisables.</span><span class="sxs-lookup"><span data-stu-id="87019-149">Application streaming should be over a LAN; deployment scenarios over a WAN or that use an unreliable or intermittent connection between the server and client might be unusable.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-150">Nécessite une infrastructure de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="87019-150">Requires a streaming infrastructure.</span></span></p>
<p><span data-ttu-id="87019-151">Programme d’installation Windows utilisé pour déployer le logiciel client de bureau de virtualisation des applications sur les ordinateurs des utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="87019-151">Windows Installer used to deploy Application Virtualization Desktop Client software to end-user computers.</span></span></p>
<p><span data-ttu-id="87019-152">Les grandes entreprises doivent utiliser des serveurs de streaming de la virtualisation des applications comme points de distribution.</span><span class="sxs-lookup"><span data-stu-id="87019-152">Large enterprises should use Application Virtualization Streaming Servers as distribution points.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87019-153">Charger à partir du fichier remise du package</span><span class="sxs-lookup"><span data-stu-id="87019-153">Load from file package delivery</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-154">Conformément aux pratiques de gestion standard de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="87019-154">Consistent with typical enterprise management practices.</span></span></p>
<p><span data-ttu-id="87019-155">Prend en charge le scénario de configuration autonome.</span><span class="sxs-lookup"><span data-stu-id="87019-155">Supports stand-alone configuration scenario.</span></span></p>
<p><span data-ttu-id="87019-156">Fournit une solution au problème de micro-succursale.</span><span class="sxs-lookup"><span data-stu-id="87019-156">Provides solution to micro–branch office problem.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-157">La livraison et la mise à jour de l’application ne peuvent pas être à la demande.</span><span class="sxs-lookup"><span data-stu-id="87019-157">Application delivery and update is not possible on-demand.</span></span></p>
<p><span data-ttu-id="87019-158">La livraison et la mise à jour de l’application ne sont pas incrémentielles; Cela augmente la consommation de ressources par rapport au service de remise dynamique.</span><span class="sxs-lookup"><span data-stu-id="87019-158">Application delivery and update is not incremental; it increases resource consumption relative to dynamic delivery.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-159">L’organisation informatique est souvent responsable de la gestion des licences d’applications, de l’autorisation des utilisateurs et de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="87019-159">The IT organization is often responsible for managing application licenses, user authorization, and authentication.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="87019-160">Protocoles liés au serveur et composants externes</span><span class="sxs-lookup"><span data-stu-id="87019-160">Server-Related Protocols and External Components</span></span>


<span data-ttu-id="87019-161">Le tableau suivant répertorie les types de serveurs qui peuvent être utilisés dans les scénarios serveur de virtualisation des applications, ainsi que les protocoles de transport correspondants et les composants externes nécessaires à la prise en charge de la configuration du serveur spécifique.</span><span class="sxs-lookup"><span data-stu-id="87019-161">The following table lists the server types that can be used in an Application Virtualization Server-based scenarios, along with their corresponding transmission protocols and the external components needed to support the specific server configuration.</span></span> <span data-ttu-id="87019-162">La table inclut également le mécanisme de création de rapports et le mécanisme de mise à niveau actif pour chaque type de serveur.</span><span class="sxs-lookup"><span data-stu-id="87019-162">The table also includes the reporting mechanism and the active upgrade mechanism for each server type.</span></span> <span data-ttu-id="87019-163">Dans la mesure où ces scénarios utilisent tous le serveur de gestion des applications virtuelles, vous pouvez utiliser la fonctionnalité de création de rapports interne intégrée au système.</span><span class="sxs-lookup"><span data-stu-id="87019-163">Because these scenarios all use the Application Virtualization Management Server, you can use the internal reporting functionality that is built into the system.</span></span> <span data-ttu-id="87019-164">Si vous utilisez une gestion de la virtualisation des applications ou un serveur de diffusion en continu de l’application pour obtenir des packages sur le client, les packages sur le serveur sont automatiquement mis à niveau lorsqu’un utilisateur se connecte au client. Si vous utilisez des serveurs IIS ou un fichier pour livrer les packages au client, les packages sur le client doivent être mis à niveau manuellement.</span><span class="sxs-lookup"><span data-stu-id="87019-164">If you use an Application Virtualization Management or an Application Virtualization Streaming Server to deliver packages to the client, packages on the server are automatically upgraded when a user logs into the client; if you use IIS servers or a file to deliver the packages to the client, the packages on the client must be upgraded manually.</span></span>

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
<th align="left"><span data-ttu-id="87019-165">Type de serveur</span><span class="sxs-lookup"><span data-stu-id="87019-165">Server Type</span></span></th>
<th align="left"><span data-ttu-id="87019-166">Protocoles</span><span class="sxs-lookup"><span data-stu-id="87019-166">Protocols</span></span></th>
<th align="left"><span data-ttu-id="87019-167">Composants externes nécessaires</span><span class="sxs-lookup"><span data-stu-id="87019-167">External Components Needed</span></span></th>
<th align="left"><span data-ttu-id="87019-168">Rapports</span><span class="sxs-lookup"><span data-stu-id="87019-168">Reporting</span></span></th>
<th align="left"><span data-ttu-id="87019-169">Mise à niveau active</span><span class="sxs-lookup"><span data-stu-id="87019-169">Active Upgrade</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87019-170">Serveur de gestion Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="87019-170">Application Virtualization Management Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-171">RTSP</span><span class="sxs-lookup"><span data-stu-id="87019-171">RTSP</span></span></p>
<p><span data-ttu-id="87019-172">RTSP</span><span class="sxs-lookup"><span data-stu-id="87019-172">RTSPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-173">Dans le cadre de l’utilisation de HTTPs, utilisez un serveur IIS pour télécharger des fichiers ICO et OSD ainsi qu’un pare-feu afin de protéger le serveur contre toute exposition à Internet.</span><span class="sxs-lookup"><span data-stu-id="87019-173">When using HTTPS, use an IIS server to download ICO and OSD files and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-174">Interne</span><span class="sxs-lookup"><span data-stu-id="87019-174">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-175">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="87019-175">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87019-176">Serveur de streaming de la virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="87019-176">Application Virtualization Streaming Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-177">RTSP</span><span class="sxs-lookup"><span data-stu-id="87019-177">RTSP</span></span></p>
<p><span data-ttu-id="87019-178">RTSP</span><span class="sxs-lookup"><span data-stu-id="87019-178">RTSPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-179">Utilisez un mécanisme pour synchroniser le contenu entre le serveur de gestion et le serveur de diffusion.</span><span class="sxs-lookup"><span data-stu-id="87019-179">Use a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="87019-180">Dans le cadre de l’utilisation de HTTPs, utilisez un serveur IIS pour télécharger des fichiers ICO et OSD et utiliser un pare-feu pour protéger votre serveur contre toute exposition à Internet.</span><span class="sxs-lookup"><span data-stu-id="87019-180">When using HTTPS, use an IIS server to download ICO and OSD files and use a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-181">Interne</span><span class="sxs-lookup"><span data-stu-id="87019-181">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-182">Pris en charge</span><span class="sxs-lookup"><span data-stu-id="87019-182">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87019-183">Serveur IIS</span><span class="sxs-lookup"><span data-stu-id="87019-183">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-184">HTTP</span><span class="sxs-lookup"><span data-stu-id="87019-184">HTTP</span></span></p>
<p><span data-ttu-id="87019-185">HTTPS</span><span class="sxs-lookup"><span data-stu-id="87019-185">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-186">Utilisez un mécanisme pour synchroniser le contenu entre le serveur de gestion et le serveur de diffusion.</span><span class="sxs-lookup"><span data-stu-id="87019-186">Use a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="87019-187">Dans le cadre de l’utilisation de HTTP ou HTTPs, utilisez un serveur IIS pour télécharger des fichiers ICO et OSD ainsi qu’un pare-feu afin de protéger le serveur contre toute exposition à Internet.</span><span class="sxs-lookup"><span data-stu-id="87019-187">When using HTTP or HTTPS, use an IIS server to download ICO and OSD files and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-188">Interne</span><span class="sxs-lookup"><span data-stu-id="87019-188">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-189">Non prise en charge</span><span class="sxs-lookup"><span data-stu-id="87019-189">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87019-190">Fichier</span><span class="sxs-lookup"><span data-stu-id="87019-190">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-191">SMB</span><span class="sxs-lookup"><span data-stu-id="87019-191">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-192">Vous avez besoin d’un moyen de synchroniser le contenu entre le serveur de gestion et le serveur de diffusion.</span><span class="sxs-lookup"><span data-stu-id="87019-192">You need a way to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="87019-193">Vous avez besoin d’un ordinateur client doté d’une fonctionnalité de partage de fichiers ou de flux.</span><span class="sxs-lookup"><span data-stu-id="87019-193">You need a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-194">Interne</span><span class="sxs-lookup"><span data-stu-id="87019-194">Internal</span></span></p></td>
<td align="left"><p><span data-ttu-id="87019-195">Non prise en charge</span><span class="sxs-lookup"><span data-stu-id="87019-195">Not Supported</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="87019-196">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="87019-196">Related topics</span></span>


[<span data-ttu-id="87019-197">Scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="87019-197">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="87019-198">Procédure pour configurer des serveurs pour un déploiement basé sur un serveur</span><span class="sxs-lookup"><span data-stu-id="87019-198">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="87019-199">Procédure pour installer les serveurs et les composants système</span><span class="sxs-lookup"><span data-stu-id="87019-199">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





