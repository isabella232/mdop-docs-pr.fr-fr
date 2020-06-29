---
title: Planification du déploiement du serveur App-V5.1
description: Planification du déploiement du serveur App-V5.1
author: dansimp
ms.assetid: eedd97c9-bee0-4749-9d1e-ab9528fba398
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31e3a116eb511356b061e6ccb18c7e25c060a66e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804975"
---
# <span data-ttu-id="b54c5-103">Planification du déploiement du serveur App-V5.1</span><span class="sxs-lookup"><span data-stu-id="b54c5-103">Planning for the App-V 5.1 Server Deployment</span></span>


<span data-ttu-id="b54c5-104">L’infrastructure de serveur Microsoft Application Virtualization (App-V) 5,1 inclut un ensemble de fonctionnalités spécialisées qui peuvent être installées sur un ou plusieurs ordinateurs serveur, en fonction des besoins de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="b54c5-104">The Microsoft Application Virtualization (App-V) 5.1 server infrastructure consists of a set of specialized features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span>

## <span data-ttu-id="b54c5-105">Planification du déploiement de l’application-V 5,1 Server</span><span class="sxs-lookup"><span data-stu-id="b54c5-105">Planning for App-V 5.1 Server Deployment</span></span>


<span data-ttu-id="b54c5-106">Le serveur App-V 5,1 comprend les fonctionnalités suivantes:</span><span class="sxs-lookup"><span data-stu-id="b54c5-106">The App-V 5.1 server consists of the following features:</span></span>

-   <span data-ttu-id="b54c5-107">Serveur de gestion: fournit une fonctionnalité de gestion générale de l’infrastructure App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b54c5-107">Management Server – provides overall management functionality for the App-V 5.1 infrastructure.</span></span>

-   <span data-ttu-id="b54c5-108">Base de données de gestion: facilite le déploiement de base de données pour la gestion d’App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b54c5-108">Management Database – facilitates database predeployments for App-V 5.1 management.</span></span>

-   <span data-ttu-id="b54c5-109">Serveur de publication: fournit des fonctionnalités d’hébergement et de streaming pour les applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="b54c5-109">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>

-   <span data-ttu-id="b54c5-110">Serveur de création de rapports-fournit une application-V 5,1 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="b54c5-110">Reporting Server – provides App-V 5.1 reporting services.</span></span>

-   <span data-ttu-id="b54c5-111">Base de données de création de rapports: facilite les déploiements de base de données pour la création de rapports App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b54c5-111">Reporting Database – facilitates database predeployments for App-V 5.1 reporting.</span></span>

<span data-ttu-id="b54c5-112">La liste suivante présente les méthodes recommandées pour l’installation de l’infrastructure du serveur App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="b54c5-112">The following list displays the recommended methods for installing the App-V 5.1 server infrastructure:</span></span>

-   <span data-ttu-id="b54c5-113">Installez le serveur App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b54c5-113">Install the App-V 5.1 server.</span></span> <span data-ttu-id="b54c5-114">Pour plus d’informations, reportez-vous à la rubrique [déploiement du serveur App-V 5,1](how-to-deploy-the-app-v-51-server.md).</span><span class="sxs-lookup"><span data-stu-id="b54c5-114">For more information, see [How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md).</span></span>

-   <span data-ttu-id="b54c5-115">Installez les fonctionnalités de base de données, de création de rapports et de gestion sur des ordinateurs séparés.</span><span class="sxs-lookup"><span data-stu-id="b54c5-115">Install the database, reporting, and management features on separate computers.</span></span> <span data-ttu-id="b54c5-116">Pour plus d’informations, reportez-vous à la rubrique [Comment installer les bases de données de gestion et de création de rapports sur des ordinateurs séparés à partir de Management et Reporting Services](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md).</span><span class="sxs-lookup"><span data-stu-id="b54c5-116">For more information, see [How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md).</span></span>

-   <span data-ttu-id="b54c5-117">Utiliser la distribution de logiciels électroniques.</span><span class="sxs-lookup"><span data-stu-id="b54c5-117">Use Electronic Software Distribution (ESD).</span></span> <span data-ttu-id="b54c5-118">Pour plus d’informations, reportez-vous [à la rubrique déploiement de packages App-V 5,1 à l’aide de la distribution de logiciels électroniques](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span><span class="sxs-lookup"><span data-stu-id="b54c5-118">For more information, see [How to deploy App-V 5.1 Packages Using Electronic Software Distribution](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span></span>

-   <span data-ttu-id="b54c5-119">Installez toutes les fonctionnalités du serveur sur un seul ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b54c5-119">Install all server features on a single computer.</span></span>

## <a href="" id="---------app-v-5-1-server-interaction"></a> <span data-ttu-id="b54c5-120">Interaction App-V 5,1 Server</span><span class="sxs-lookup"><span data-stu-id="b54c5-120">App-V 5.1 Server Interaction</span></span>


<span data-ttu-id="b54c5-121">Cette section contient des informations sur la façon dont les différents rôles de serveur App-V 5,1 interagissent entre eux.</span><span class="sxs-lookup"><span data-stu-id="b54c5-121">This section contains information about how the various App-V 5.1 server roles interact with each other.</span></span>

<span data-ttu-id="b54c5-122">Le serveur de gestion App-V 5,1 contient le référentiel des packages et leurs configurations affectées.</span><span class="sxs-lookup"><span data-stu-id="b54c5-122">The App-V 5.1 Management Server contains the repository of packages and their assigned configurations.</span></span> <span data-ttu-id="b54c5-123">Pour les serveurs de publication qui sont inscrits auprès du serveur de gestion, les métadonnées associées sont fournies aux serveurs de publication pour une utilisation lors de la publication de demandes d’actualisation d’ordinateurs exécutant le client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b54c5-123">For Publishing Servers that are registered with the Management Server, the associated metadata is provided to the Publishing servers for use when publishing refresh requests are received from computers running the App-V 5.1 Client.</span></span> <span data-ttu-id="b54c5-124">Les serveurs de publication App-V 5,1 gérés par un serveur de gestion unique peuvent utiliser différents clients et peuvent avoir des noms de site Web et des liaisons de port différents.</span><span class="sxs-lookup"><span data-stu-id="b54c5-124">App-V 5.1 publishing servers managed by a single management server can be serving different clients and can have different website names and port bindings.</span></span> <span data-ttu-id="b54c5-125">De plus, tous les serveurs de publication gérés par le même serveur de gestion sont répliques les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="b54c5-125">Additionally, all Publishing Servers managed by the same Management Server are replicas of each other.</span></span>

<span data-ttu-id="b54c5-126">**Remarques**  Le serveur de gestion n’effectue aucun équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="b54c5-126">**Note** The Management Server does not perform any load balancing.</span></span> <span data-ttu-id="b54c5-127">Les métadonnées associées sont simplement transmises au serveur de publication pour être utilisées lors du traitement des requêtes client.</span><span class="sxs-lookup"><span data-stu-id="b54c5-127">The associated metadata is simply passed to the publishing server for use when processing client requests.</span></span>

 

## <span data-ttu-id="b54c5-128">Protocoles liés au serveur et fonctionnalités externes</span><span class="sxs-lookup"><span data-stu-id="b54c5-128">Server-Related Protocols and External Features</span></span>


<span data-ttu-id="b54c5-129">L’exemple suivant affiche des informations sur les protocoles liés au serveur utilisés par les serveurs App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b54c5-129">The following displays information about server-related protocols used by the App-V 5.1 servers.</span></span> <span data-ttu-id="b54c5-130">La table inclut également le mécanisme de création de rapports pour chaque type de serveur.</span><span class="sxs-lookup"><span data-stu-id="b54c5-130">The table also includes the reporting mechanism for each server type.</span></span>

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
<th align="left"><span data-ttu-id="b54c5-131">Type de serveur</span><span class="sxs-lookup"><span data-stu-id="b54c5-131">Server Type</span></span></th>
<th align="left"><span data-ttu-id="b54c5-132">Protocoles</span><span class="sxs-lookup"><span data-stu-id="b54c5-132">Protocols</span></span></th>
<th align="left"><span data-ttu-id="b54c5-133">Fonctionnalités externes nécessaires</span><span class="sxs-lookup"><span data-stu-id="b54c5-133">External Features Needed</span></span></th>
<th align="left"><span data-ttu-id="b54c5-134">Rapports</span><span class="sxs-lookup"><span data-stu-id="b54c5-134">Reporting</span></span></th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b54c5-135">Serveur IIS</span><span class="sxs-lookup"><span data-stu-id="b54c5-135">IIS server</span></span></p></td>
<td align="left"><p><span data-ttu-id="b54c5-136">HTTP</span><span class="sxs-lookup"><span data-stu-id="b54c5-136">HTTP</span></span></p>
<p><span data-ttu-id="b54c5-137">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b54c5-137">HTTPS</span></span></p></td>
<td align="left"><p><span data-ttu-id="b54c5-138">Cette combinaison de protocoles serveur nécessite un mécanisme de synchronisation du contenu entre le serveur de gestion et le serveur de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="b54c5-138">This server-protocol combination requires a mechanism to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="b54c5-139">Dans le cadre de l’utilisation de HTTP ou HTTPs, utilisez un serveur IIS et un pare-feu pour protéger votre serveur contre son exposition à Internet.</span><span class="sxs-lookup"><span data-stu-id="b54c5-139">When using HTTP or HTTPS, use an IIS server and a firewall to protect the server from exposure to the Internet.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b54c5-140">Interne</span><span class="sxs-lookup"><span data-stu-id="b54c5-140">Internal</span></span></p></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b54c5-141">Fichier</span><span class="sxs-lookup"><span data-stu-id="b54c5-141">File</span></span></p></td>
<td align="left"><p><span data-ttu-id="b54c5-142">SMB</span><span class="sxs-lookup"><span data-stu-id="b54c5-142">SMB</span></span></p></td>
<td align="left"><p><span data-ttu-id="b54c5-143">Cette combinaison de protocoles serveur nécessite une prise en charge de la synchronisation du contenu entre le serveur de gestion et le serveur de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="b54c5-143">This server-protocol combination requires support to synchronize the content between the Management Server and the Streaming Server.</span></span> <span data-ttu-id="b54c5-144">Utiliser un ordinateur client avec la fonctionnalité de partage de fichiers ou de flux.</span><span class="sxs-lookup"><span data-stu-id="b54c5-144">Use a client computer with file sharing or streaming capability.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b54c5-145">Interne</span><span class="sxs-lookup"><span data-stu-id="b54c5-145">Internal</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="b54c5-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b54c5-146">Related topics</span></span>


[<span data-ttu-id="b54c5-147">Envisager de déployer App-V</span><span class="sxs-lookup"><span data-stu-id="b54c5-147">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

[<span data-ttu-id="b54c5-148">Déploiement d'App-V5.1 Server</span><span class="sxs-lookup"><span data-stu-id="b54c5-148">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

 

 





