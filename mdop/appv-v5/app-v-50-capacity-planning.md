---
title: Planification de la capacité d'App-V5.0
description: Planification de la capacité d'App-V5.0
author: dansimp
ms.assetid: 56f48b00-cd91-4280-9481-5372a0e2e792
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e828457a286f6f686c227a935828679514d87ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806037"
---
# <span data-ttu-id="9a68d-103">Planification de la capacité d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="9a68d-103">App-V 5.0 Capacity Planning</span></span>


<span data-ttu-id="9a68d-104">Les recommandations suivantes peuvent être utilisées comme planning de référence afin de vous aider à déterminer les informations de planification appropriées pour l’infrastructure App-V 5,0 de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9a68d-104">The following recommendations can be used as a baseline to help determine capacity planning information that is appropriate to your organization’s App-V 5.0 infrastructure.</span></span>

<span data-ttu-id="9a68d-105">**Important**  Utilisez les informations de cette section uniquement en tant que guide général pour la planification de votre déploiement d’application-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9a68d-105">**Important** Use the information in this section only as a general guide for planning your App-V 5.0 deployment.</span></span> <span data-ttu-id="9a68d-106">La capacité requise de votre système dépend des détails spécifiques de votre matériel et de votre environnement applicatif.</span><span class="sxs-lookup"><span data-stu-id="9a68d-106">Your system capacity requirements will depend on the specific details of your hardware and application environment.</span></span> <span data-ttu-id="9a68d-107">Par ailleurs, les numéros de performance indiqués dans ce document sont des exemples et vos résultats peuvent varier.</span><span class="sxs-lookup"><span data-stu-id="9a68d-107">Additionally, the performance numbers displayed in this document are examples and your results may vary.</span></span>

 

## <span data-ttu-id="9a68d-108">Déterminez l’objectif du projet</span><span class="sxs-lookup"><span data-stu-id="9a68d-108">Determine the Project Scope</span></span>


<span data-ttu-id="9a68d-109">Avant de concevoir l’infrastructure App-V 5,0, vous devez déterminer l’étendue du projet.</span><span class="sxs-lookup"><span data-stu-id="9a68d-109">Before you design the App-V 5.0 infrastructure, you must determine the project’s scope.</span></span> <span data-ttu-id="9a68d-110">L’étendue consiste à déterminer les applications qui seront disponibles virtuellement et à identifier les utilisateurs cibles et leurs emplacements.</span><span class="sxs-lookup"><span data-stu-id="9a68d-110">The scope consists of determining which applications will be available virtually and to also identify the target users, and their locations.</span></span> <span data-ttu-id="9a68d-111">Ces informations vous aideront à déterminer le type d’infrastructure App-V 5,0 à implémenter.</span><span class="sxs-lookup"><span data-stu-id="9a68d-111">This information will help determine what type of App-V 5.0 infrastructure should be implemented.</span></span> <span data-ttu-id="9a68d-112">Les décisions relatives à l’étendue du projet doivent être basées sur les besoins spécifiques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9a68d-112">Decisions about the scope of the project must be based on the specific needs of your organization.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9a68d-113">Tâche</span><span class="sxs-lookup"><span data-stu-id="9a68d-113">Task</span></span></th>
<th align="left"><span data-ttu-id="9a68d-114">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9a68d-114">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-115">Déterminer l’étendue de l’application</span><span class="sxs-lookup"><span data-stu-id="9a68d-115">Determine Application Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a68d-116">En fonction des applications à virtualiser, l’infrastructure App-V 5,0 peut être définie de différentes manières.</span><span class="sxs-lookup"><span data-stu-id="9a68d-116">Depending on the applications to be virtualized, the App-V 5.0 infrastructure can be set up in different ways.</span></span> <span data-ttu-id="9a68d-117">La première tâche consiste à définir les applications que vous voulez virtualiser.</span><span class="sxs-lookup"><span data-stu-id="9a68d-117">The first task is to define what applications you want to virtualize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a68d-118">Déterminer l’étendue de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="9a68d-118">Determine Location Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a68d-119">Le champ étendue de l’emplacement fait référence aux emplacements physiques (par exemple, à l’échelle de l’entreprise ou à un emplacement géographique spécifique) sur lequel vous envisagez d’exécuter les applications virtualisées.</span><span class="sxs-lookup"><span data-stu-id="9a68d-119">Location scope refers to the physical locations (for example, enterprise-wide or a specific geographic location) where you plan to run the virtualized applications.</span></span> <span data-ttu-id="9a68d-120">Elle peut également faire référence à la population des utilisateurs (par exemple, un service unique) qui exécuteront les applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="9a68d-120">It can also refer to the user population (for example, a single department) who will run the virtual applications.</span></span> <span data-ttu-id="9a68d-121">Vous devriez obtenir une carte réseau qui inclut les chemins de connexion ainsi que la bande passante disponible vers chaque emplacement et le nombre d’utilisateurs qui utilisent des applications virtualisées et la vitesse de liaison du réseau étendu.</span><span class="sxs-lookup"><span data-stu-id="9a68d-121">You should obtain a network map that includes the connection paths as well as available bandwidth to each location and the number of users using virtualized applications and the WAN link speed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9a68d-122">Déterminer l’infrastructure App-V 5,0 requise</span><span class="sxs-lookup"><span data-stu-id="9a68d-122">Determine Which App-V 5.0 Infrastructure is Required</span></span>


<span data-ttu-id="9a68d-123">**Important**  Les deux modèles suivants requièrent que le client App-V 5,0 soit installé sur l’ordinateur sur lequel vous envisagez d’exécuter des applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="9a68d-123">**Important** Both of the following models require the App-V 5.0 client to be installed on the computer where you plan to run virtual applications.</span></span>

<span data-ttu-id="9a68d-124">Vous pouvez également gérer votre environnement App-V 5,0 à l’aide d’une solution de distribution de logiciels électronique (ESD) telle que Microsoft Systems Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9a68d-124">You can also manage your App-V 5.0 environment using an Electronic Software Distribution (ESD) solution such as Microsoft Systems Center Configuration Manager.</span></span> <span data-ttu-id="9a68d-125">Pour plus d’informations, reportez-vous à [déploiement de packages App-V 5,0 à l’aide de la distribution de logiciels électroniques](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md).</span><span class="sxs-lookup"><span data-stu-id="9a68d-125">For more information see [Deploying App-V 5.0 Packages by Using Electronic Software Distribution (ESD)](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md).</span></span>

 

-   <span data-ttu-id="9a68d-126">**Modèle autonome** -le modèle autonome permet aux applications virtuelles d’être activées pour la distribution sans streaming.</span><span class="sxs-lookup"><span data-stu-id="9a68d-126">**Standalone Model** - The standalone model allows virtual applications to be Windows Installer-enabled for distribution without streaming.</span></span> <span data-ttu-id="9a68d-127">App-V 5,0 en mode autonome se compose du Sequencer et du client; aucun composant supplémentaire n’est requis.</span><span class="sxs-lookup"><span data-stu-id="9a68d-127">App-V 5.0 in Standalone Mode consists of the sequencer and the client; no additional components are required.</span></span> <span data-ttu-id="9a68d-128">Les applications sont prêtes pour la virtualisation grâce à un processus appelé séquençage.</span><span class="sxs-lookup"><span data-stu-id="9a68d-128">Applications are prepared for virtualization using a process called sequencing.</span></span> <span data-ttu-id="9a68d-129">Pour plus d’informations, reportez-vous [à la section planification du déploiement d’App-V 5,0 et du déploiement du client](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="9a68d-129">For more information see, [Planning for the App-V 5.0 Sequencer and Client Deployment](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span></span> <span data-ttu-id="9a68d-130">Le modèle autonome est recommandé dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="9a68d-130">The stand-alone model is recommended for the following scenarios:</span></span>

    -   <span data-ttu-id="9a68d-131">Utilisateurs distants distants qui ne peuvent pas se connecter à l’infrastructure App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9a68d-131">With disconnected remote users who cannot connect to the App-V 5.0 infrastructure.</span></span>

    -   <span data-ttu-id="9a68d-132">Lorsque vous exécutez un système de gestion de logiciels, tel que Configuration Manager 2012.</span><span class="sxs-lookup"><span data-stu-id="9a68d-132">When you are running a software management system, such as Configuration Manager 2012.</span></span>

    -   <span data-ttu-id="9a68d-133">Lorsque les limitations de bande passante réseau empêchent la distribution de logiciels électroniques.</span><span class="sxs-lookup"><span data-stu-id="9a68d-133">When network bandwidth limitations inhibit electronic software distribution.</span></span>

-   <span data-ttu-id="9a68d-134">**Modèle d’infrastructure complète** -le modèle d’infrastructure complet fournit des fonctionnalités de distribution de logiciels, de gestion et de création de rapports. Il inclut également la diffusion en continu d’applications sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="9a68d-134">**Full Infrastructure Model** - The full infrastructure model provides for software distribution, management, and reporting capabilities; it also includes the streaming of applications across the network.</span></span> <span data-ttu-id="9a68d-135">Le modèle d’infrastructure complète App-V 5,0 comporte un ou plusieurs serveurs de gestion de l’application-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9a68d-135">The App-V 5.0 Full Infrastructure Model consists of one or more App-V 5.0 management servers.</span></span> <span data-ttu-id="9a68d-136">Le serveur de gestion peut être utilisé pour publier des applications sur tous les clients.</span><span class="sxs-lookup"><span data-stu-id="9a68d-136">The Management Server can be used to publish applications to all clients.</span></span> <span data-ttu-id="9a68d-137">Le processus de publication place les icônes et raccourcis des applications virtuelles sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="9a68d-137">The publishing process places the virtual application icons and shortcuts on the target computer.</span></span> <span data-ttu-id="9a68d-138">Il peut également diffuser des applications aux utilisateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="9a68d-138">It can also stream applications to local users.</span></span> <span data-ttu-id="9a68d-139">Pour plus d’informations sur l’installation du serveur de gestion, voir [planification du déploiement de l’application-V 5,0 Server](planning-for-the-app-v-50-server-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="9a68d-139">For more information about installing the management server see, [Planning for the App-V 5.0 Server Deployment](planning-for-the-app-v-50-server-deployment.md).</span></span> <span data-ttu-id="9a68d-140">Le modèle d’infrastructure complète est recommandé dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="9a68d-140">The full infrastructure model is recommended for the following scenarios:</span></span>

    <span data-ttu-id="9a68d-141">**Important**  Le modèle d’infrastructure complète App-V 5,0 nécessite Microsoft SQL Server pour stocker des données de configuration.</span><span class="sxs-lookup"><span data-stu-id="9a68d-141">**Important** The App-V 5.0 full infrastructure model requires Microsoft SQL Server to store configuration data.</span></span> <span data-ttu-id="9a68d-142">Pour plus d’informations, voir [Configurations prises en charge par App-V 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="9a68d-142">For more information see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

     

    -   <span data-ttu-id="9a68d-143">Lorsque vous souhaitez utiliser le serveur de gestion pour publier l’application sur des ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="9a68d-143">When you want to use the Management Server to publish the application to target computers.</span></span>

    -   <span data-ttu-id="9a68d-144">Pour la mise en service rapide des applications sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="9a68d-144">For rapid provisioning of applications to target computers.</span></span>

    -   <span data-ttu-id="9a68d-145">Lorsque vous souhaitez utiliser la création de rapports App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9a68d-145">When you want to use App-V 5.0 reporting.</span></span>

## <span data-ttu-id="9a68d-146">Recommandations en matière de dimensionnement de serveur bout en bout</span><span class="sxs-lookup"><span data-stu-id="9a68d-146">End-to-end Server Sizing Guidance</span></span>


<span data-ttu-id="9a68d-147">La section suivante fournit des informations sur la planification et le dimensionnement d’une application 5,0 de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="9a68d-147">The following section provides information about end-to-end App-V 5.0 sizing and planning.</span></span> <span data-ttu-id="9a68d-148">Pour plus d’informations, reportez-vous aux sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="9a68d-148">For more specific information, refer to the subsequent sections.</span></span>

<span data-ttu-id="9a68d-149">**Remarques**  Le temps de réponse en boucle sur le client correspond au temps écoulé par l’ordinateur exécutant le client App-V 5,0 pour recevoir une notification réussie du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="9a68d-149">**Note** Round trip response time on the client is the time taken by the computer running the App-V 5.0 client to receive a successful notification from the publishing server.</span></span> <span data-ttu-id="9a68d-150">Le temps de réponse en boucle sur le serveur de publication est le temps pris par l’ordinateur exécutant le serveur de publication pour recevoir une mise à jour de métadonnées de package réussie du serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="9a68d-150">Round trip response time on the publishing server is the time taken by the computer running the publishing server to receive a successful package metadata update from the management server.</span></span>

 

-   <span data-ttu-id="9a68d-151">les clients 20 000 peuvent cibler un serveur de publication unique pour obtenir les actualisations du package pendant une durée de boucle acceptable.</span><span class="sxs-lookup"><span data-stu-id="9a68d-151">20,000 clients can target a single publishing server to obtain the package refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="9a68d-152">( &lt; 3 secondes)</span><span class="sxs-lookup"><span data-stu-id="9a68d-152">(&lt;3 seconds)</span></span>

-   <span data-ttu-id="9a68d-153">Un serveur de gestion unique peut prendre en charge jusqu’à 50 serveurs de publication pour les mises à jour de package de métadonnées pendant une durée de boucle acceptable.</span><span class="sxs-lookup"><span data-stu-id="9a68d-153">A single management server can support up to 50 publishing servers for package metadata refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="9a68d-154">( &lt; 5 secondes)</span><span class="sxs-lookup"><span data-stu-id="9a68d-154">(&lt;5 seconds)</span></span>

## <a href="" id="---------app-v-5-0-management-server-capacity-planning-recommendations"></a> <span data-ttu-id="9a68d-155">Recommandations en matière de planification de la capacité du serveur de gestion d’application V 5,0</span><span class="sxs-lookup"><span data-stu-id="9a68d-155">App-V 5.0 Management Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="9a68d-156">Les serveurs de publication App-V 5,0 nécessitent le serveur de gestion des demandes d’actualisation de package et des réponses d’actualisation de package.</span><span class="sxs-lookup"><span data-stu-id="9a68d-156">The App-V 5.0 publishing servers require the management server for package refresh requests and package refresh responses.</span></span> <span data-ttu-id="9a68d-157">Le serveur de gestion envoie alors les informations à la base de données de gestion pour récupérer des informations.</span><span class="sxs-lookup"><span data-stu-id="9a68d-157">The management server then sends the information to the management database to retrieve information.</span></span> <span data-ttu-id="9a68d-158">Pour plus d’informations sur les configurations prises en charge par App-V 5,0 Management Server, voir [Configurations prises en charge par app-v 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="9a68d-158">For more information about App-V 5.0 management server supported configurations see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="9a68d-159">**Remarques**  Le délai d’actualisation par défaut dans le serveur de publication 5,0 App-V est de 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="9a68d-159">**Note** The default refresh time on the App-V 5.0 publishing server is ten minutes.</span></span>

 

<span data-ttu-id="9a68d-160">Lorsque plusieurs serveurs de publication simultanés contactent un serveur de gestion unique pour les actualisations des métadonnées du package, les trois facteurs suivants influencent le temps de réponse en boucle sur le serveur de publication:</span><span class="sxs-lookup"><span data-stu-id="9a68d-160">When multiple simultaneous publishing servers contact a single management server for package metadata refreshes, the following three factors influence the round trip response time on the publishing server:</span></span>

1.  <span data-ttu-id="9a68d-161">Nombre de serveurs de publication effectuant des demandes simultanées.</span><span class="sxs-lookup"><span data-stu-id="9a68d-161">Number of publishing servers making simultaneous requests.</span></span>

2.  <span data-ttu-id="9a68d-162">Nombre de groupes de connexion configurés sur le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="9a68d-162">Number of connection groups configured on the management server.</span></span>

3.  <span data-ttu-id="9a68d-163">Nombre de groupes d’accès configurés sur le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="9a68d-163">Number of access groups configured on the management server.</span></span>

<span data-ttu-id="9a68d-164">Le tableau suivant fournit des informations supplémentaires sur chaque facteur ayant un impact sur la durée de l’aller-retour.</span><span class="sxs-lookup"><span data-stu-id="9a68d-164">The following table displays more information about each factor that impacts round trip time.</span></span>

<span data-ttu-id="9a68d-165">**Remarques**  Le temps de réponse aller-retour est le temps écoulé par l’ordinateur exécutant le serveur de publication 5,0 App-V pour recevoir une mise à jour de package réussie du serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="9a68d-165">**Note** Round trip response time is the time taken by the computer running the App-V 5.0 publishing server to receive a successful package metadata update from the management server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9a68d-166">Facteurs affectant le temps de réponse en boucle</span><span class="sxs-lookup"><span data-stu-id="9a68d-166">Factors impacting round trip response time</span></span></th>
<th align="left"><span data-ttu-id="9a68d-167">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9a68d-167">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-168">Nombre de serveurs de publication demandant des mises à jour de package simultanément.</span><span class="sxs-lookup"><span data-stu-id="9a68d-168">The number of publishing servers simultaneously requesting package metadata refreshes.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-169">Un serveur de gestion unique peut répondre à des serveurs de publication 320 demandant des métadonnées de publication simultanément.</span><span class="sxs-lookup"><span data-stu-id="9a68d-169">A single management server can respond to up to 320 publishing servers requesting publishing metadata simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="9a68d-170">Le temps de réponse aller-retour pour les serveurs de publication 320 est de 40 secondes.</span><span class="sxs-lookup"><span data-stu-id="9a68d-170">Round trip response time for 320 pub servers is ~40 seconds.</span></span></p></li>
<li><p><span data-ttu-id="9a68d-171">Pour &lt; les serveurs de publication 50 demandant des métadonnées simultanément, la durée de réponse d’un aller-retour est de &lt; 5 secondes.</span><span class="sxs-lookup"><span data-stu-id="9a68d-171">For &lt;50 publishing servers requesting metadata simultaneously, the round trip response time is &lt;5 seconds.</span></span></p></li>
<li><p><span data-ttu-id="9a68d-172">De 50 à 320, le temps de réponse augmente de façon linéaire (approximativement 2x).</span><span class="sxs-lookup"><span data-stu-id="9a68d-172">From 50 to 320 publishing servers, the response time increases linearly (approximately 2x).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a68d-173">Nombre de groupes de connexion configurés sur le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="9a68d-173">The number of connection groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-174">Pour les groupes de connexions 100, il n’y a aucun changement notable dans le temps de réponse en boucle sur le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="9a68d-174">For up to 100 connection groups, there is no significant change in the round trip response time on the publishing server.</span></span></p></li>
<li><p><span data-ttu-id="9a68d-175">Pour les groupes de connexion 100-400, il existe une augmentation linéaire mineure du temps de réponse à un aller-retour.</span><span class="sxs-lookup"><span data-stu-id="9a68d-175">For 100 - 400 connection groups, there is a minor linear increase in the round trip response time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-176">Nombre de groupes d’accès configurés sur le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="9a68d-176">The number of access groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-177">Dans le cas d’un maximum de groupes d’accès à 40, le temps de réponse d’un aller-retour est linéaire (approximativement 3 160) sur le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="9a68d-177">For up to 40 access groups, there is a linear (approximately 3x) increase in the round trip response time on the publishing server.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9a68d-178">Le tableau suivant présente des exemples de valeurs pour chacun des facteurs précédents.</span><span class="sxs-lookup"><span data-stu-id="9a68d-178">The following table displays sample values for each of the previous factors.</span></span> <span data-ttu-id="9a68d-179">Dans chaque variante, les packages 120 sont actualisés à partir du serveur de gestion App-V 5.0.</span><span class="sxs-lookup"><span data-stu-id="9a68d-179">In each variation, 120 packages are refreshed from the App-V 5.0management server.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9a68d-180">Scénario</span><span class="sxs-lookup"><span data-stu-id="9a68d-180">Scenario</span></span></th>
<th align="left"><span data-ttu-id="9a68d-181">Variante</span><span class="sxs-lookup"><span data-stu-id="9a68d-181">Variation</span></span></th>
<th align="left"><span data-ttu-id="9a68d-182">Nombre de groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="9a68d-182">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="9a68d-183">Nombre de groupes d’accès</span><span class="sxs-lookup"><span data-stu-id="9a68d-183">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="9a68d-184">Nombre de serveurs de publication</span><span class="sxs-lookup"><span data-stu-id="9a68d-184">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="9a68d-185">Serveur de publication de type de connexion réseau/serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="9a68d-185">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="9a68d-186">Temps de réponse aller-retour sur le serveur de publication (en secondes)</span><span class="sxs-lookup"><span data-stu-id="9a68d-186">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="9a68d-187">Utilisation de l’UC sur le serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="9a68d-187">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-188">Serveurs de publication contactant simultanément le serveur de gestion pour les métadonnées de publication.</span><span class="sxs-lookup"><span data-stu-id="9a68d-188">Publishing servers simultaneously contacting management server for publishing metadata.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a68d-189">Nombre de serveurs de publication</span><span class="sxs-lookup"><span data-stu-id="9a68d-189">Number of publishing servers</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-190">0,4</span><span class="sxs-lookup"><span data-stu-id="9a68d-190">0</span></span></p></li>
<li><p><span data-ttu-id="9a68d-191">0,4</span><span class="sxs-lookup"><span data-stu-id="9a68d-191">0</span></span></p></li>
<li><p><span data-ttu-id="9a68d-192">0,4</span><span class="sxs-lookup"><span data-stu-id="9a68d-192">0</span></span></p></li>
<li><p><span data-ttu-id="9a68d-193">0,4</span><span class="sxs-lookup"><span data-stu-id="9a68d-193">0</span></span></p></li>
<li><p><span data-ttu-id="9a68d-194">0,4</span><span class="sxs-lookup"><span data-stu-id="9a68d-194">0</span></span></p></li>
<li><p><span data-ttu-id="9a68d-195">0,4</span><span class="sxs-lookup"><span data-stu-id="9a68d-195">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-196">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-196">1</span></span></p></li>
<li><p><span data-ttu-id="9a68d-197">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-197">1</span></span></p></li>
<li><p><span data-ttu-id="9a68d-198">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-198">1</span></span></p></li>
<li><p><span data-ttu-id="9a68d-199">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-199">1</span></span></p></li>
<li><p><span data-ttu-id="9a68d-200">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-200">1</span></span></p></li>
<li><p><span data-ttu-id="9a68d-201">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-201">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-202">50</span><span class="sxs-lookup"><span data-stu-id="9a68d-202">50</span></span></p></li>
<li><p><span data-ttu-id="9a68d-203">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-203">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-204">200</span><span class="sxs-lookup"><span data-stu-id="9a68d-204">200</span></span></p></li>
<li><p><span data-ttu-id="9a68d-205">300</span><span class="sxs-lookup"><span data-stu-id="9a68d-205">300</span></span></p></li>
<li><p><span data-ttu-id="9a68d-206">315</span><span class="sxs-lookup"><span data-stu-id="9a68d-206">315</span></span></p></li>
<li><p><span data-ttu-id="9a68d-207">320</span><span class="sxs-lookup"><span data-stu-id="9a68d-207">320</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-208">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-208">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-209">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-209">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-210">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-210">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-211">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-211">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-212">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-212">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-213">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-213">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-214">n°5</span><span class="sxs-lookup"><span data-stu-id="9a68d-214">5</span></span></p></li>
<li><p><span data-ttu-id="9a68d-215">0,10</span><span class="sxs-lookup"><span data-stu-id="9a68d-215">10</span></span></p></li>
<li><p><span data-ttu-id="9a68d-216">19,6</span><span class="sxs-lookup"><span data-stu-id="9a68d-216">19</span></span></p></li>
<li><p><span data-ttu-id="9a68d-217">32</span><span class="sxs-lookup"><span data-stu-id="9a68d-217">32</span></span></p></li>
<li><p><span data-ttu-id="9a68d-218">trente</span><span class="sxs-lookup"><span data-stu-id="9a68d-218">30</span></span></p></li>
<li><p><span data-ttu-id="9a68d-219">37</span><span class="sxs-lookup"><span data-stu-id="9a68d-219">37</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-220">Play</span><span class="sxs-lookup"><span data-stu-id="9a68d-220">17</span></span></p></li>
<li><p><span data-ttu-id="9a68d-221">Play</span><span class="sxs-lookup"><span data-stu-id="9a68d-221">17</span></span></p></li>
<li><p><span data-ttu-id="9a68d-222">Play</span><span class="sxs-lookup"><span data-stu-id="9a68d-222">17</span></span></p></li>
<li><p><span data-ttu-id="9a68d-223">0,15</span><span class="sxs-lookup"><span data-stu-id="9a68d-223">15</span></span></p></li>
<li><p><span data-ttu-id="9a68d-224">Play</span><span class="sxs-lookup"><span data-stu-id="9a68d-224">17</span></span></p></li>
<li><p><span data-ttu-id="9a68d-225">0,15</span><span class="sxs-lookup"><span data-stu-id="9a68d-225">15</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a68d-226">Métadonnées de publication contenant des groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="9a68d-226">Publishing metadata contains connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a68d-227">Nombre de groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="9a68d-227">Number of connection groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-228">0,10</span><span class="sxs-lookup"><span data-stu-id="9a68d-228">10</span></span></p></li>
<li><p><span data-ttu-id="9a68d-229">50</span><span class="sxs-lookup"><span data-stu-id="9a68d-229">50</span></span></p></li>
<li><p><span data-ttu-id="9a68d-230">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-230">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-231">150</span><span class="sxs-lookup"><span data-stu-id="9a68d-231">150</span></span></p></li>
<li><p><span data-ttu-id="9a68d-232">300</span><span class="sxs-lookup"><span data-stu-id="9a68d-232">300</span></span></p></li>
<li><p><span data-ttu-id="9a68d-233">400</span><span class="sxs-lookup"><span data-stu-id="9a68d-233">400</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-234">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-234">1</span></span></p></li>
<li><p><span data-ttu-id="9a68d-235">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-235">1</span></span></p></li>
<li><p><span data-ttu-id="9a68d-236">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-236">1</span></span></p></li>
<li><p><span data-ttu-id="9a68d-237">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-237">1</span></span></p></li>
<li><p><span data-ttu-id="9a68d-238">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-238">1</span></span></p></li>
<li><p><span data-ttu-id="9a68d-239">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-239">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-240">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-240">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-241">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-241">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-242">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-242">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-243">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-243">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-244">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-244">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-245">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-245">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-246">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-246">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-247">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-247">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-248">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-248">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-249">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-249">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-250">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-250">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-251">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-251">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-252">0,10</span><span class="sxs-lookup"><span data-stu-id="9a68d-252">10</span></span></p></li>
<li><p><span data-ttu-id="9a68d-253">27,9</span><span class="sxs-lookup"><span data-stu-id="9a68d-253">11</span></span></p></li>
<li><p><span data-ttu-id="9a68d-254">27,9</span><span class="sxs-lookup"><span data-stu-id="9a68d-254">11</span></span></p></li>
<li><p><span data-ttu-id="9a68d-255">Seiz</span><span class="sxs-lookup"><span data-stu-id="9a68d-255">16</span></span></p></li>
<li><p><span data-ttu-id="9a68d-256">22</span><span class="sxs-lookup"><span data-stu-id="9a68d-256">22</span></span></p></li>
<li><p><span data-ttu-id="9a68d-257">1,25</span><span class="sxs-lookup"><span data-stu-id="9a68d-257">25</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-258">Play</span><span class="sxs-lookup"><span data-stu-id="9a68d-258">17</span></span></p></li>
<li><p><span data-ttu-id="9a68d-259">19,6</span><span class="sxs-lookup"><span data-stu-id="9a68d-259">19</span></span></p></li>
<li><p><span data-ttu-id="9a68d-260">22</span><span class="sxs-lookup"><span data-stu-id="9a68d-260">22</span></span></p></li>
<li><p><span data-ttu-id="9a68d-261">19,6</span><span class="sxs-lookup"><span data-stu-id="9a68d-261">19</span></span></p></li>
<li><p><span data-ttu-id="9a68d-262">CX3-20</span><span class="sxs-lookup"><span data-stu-id="9a68d-262">20</span></span></p></li>
<li><p><span data-ttu-id="9a68d-263">CX3-20</span><span class="sxs-lookup"><span data-stu-id="9a68d-263">20</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-264">Métadonnées de publication contenant des groupes d’accès</span><span class="sxs-lookup"><span data-stu-id="9a68d-264">Publishing metadata contains access groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a68d-265">Nombre de groupes d’accès</span><span class="sxs-lookup"><span data-stu-id="9a68d-265">Number of access groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-266">0,4</span><span class="sxs-lookup"><span data-stu-id="9a68d-266">0</span></span></p></li>
<li><p><span data-ttu-id="9a68d-267">0,4</span><span class="sxs-lookup"><span data-stu-id="9a68d-267">0</span></span></p></li>
<li><p><span data-ttu-id="9a68d-268">0,4</span><span class="sxs-lookup"><span data-stu-id="9a68d-268">0</span></span></p></li>
<li><p><span data-ttu-id="9a68d-269">0,4</span><span class="sxs-lookup"><span data-stu-id="9a68d-269">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-270">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-270">1</span></span></p></li>
<li><p><span data-ttu-id="9a68d-271">0,10</span><span class="sxs-lookup"><span data-stu-id="9a68d-271">10</span></span></p></li>
<li><p><span data-ttu-id="9a68d-272">CX3-20</span><span class="sxs-lookup"><span data-stu-id="9a68d-272">20</span></span></p></li>
<li><p><span data-ttu-id="9a68d-273">40</span><span class="sxs-lookup"><span data-stu-id="9a68d-273">40</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-274">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-274">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-275">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-275">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-276">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-276">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-277">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-277">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-278">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-278">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-279">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-279">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-280">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-280">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-281">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-281">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-282">0,10</span><span class="sxs-lookup"><span data-stu-id="9a68d-282">10</span></span></p></li>
<li><p><span data-ttu-id="9a68d-283">43</span><span class="sxs-lookup"><span data-stu-id="9a68d-283">43</span></span></p></li>
<li><p><span data-ttu-id="9a68d-284">153</span><span class="sxs-lookup"><span data-stu-id="9a68d-284">153</span></span></p></li>
<li><p><span data-ttu-id="9a68d-285">535</span><span class="sxs-lookup"><span data-stu-id="9a68d-285">535</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-286">Play</span><span class="sxs-lookup"><span data-stu-id="9a68d-286">17</span></span></p></li>
<li><p><span data-ttu-id="9a68d-287">26/08/03</span><span class="sxs-lookup"><span data-stu-id="9a68d-287">26</span></span></p></li>
<li><p><span data-ttu-id="9a68d-288">24</span><span class="sxs-lookup"><span data-stu-id="9a68d-288">24</span></span></p></li>
<li><p><span data-ttu-id="9a68d-289">24</span><span class="sxs-lookup"><span data-stu-id="9a68d-289">24</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9a68d-290">L’utilisation de l’UC de l’ordinateur exécutant le serveur de gestion est d’environ 25%, sans tenir compte du nombre de serveurs de publication ciblant celle-ci.</span><span class="sxs-lookup"><span data-stu-id="9a68d-290">The CPU utilization of the computer running the management server is around 25% irrespective of the number of publishing servers targeting it.</span></span> <span data-ttu-id="9a68d-291">Les transactions/s de base de données Microsoft SQL Server, les requêtes par lot/s et les connexions utilisateur sont identiques quel que soit le nombre de serveurs de publication.</span><span class="sxs-lookup"><span data-stu-id="9a68d-291">The Microsoft SQL Server database transactions/sec, batch requests/sec and user connections are identical irrespective of the number of publishing servers.</span></span> <span data-ttu-id="9a68d-292">Par exemple: transactions/s est ~ 30, les demandes de lot ~ 200 et l’utilisateur connecte ~ 6.</span><span class="sxs-lookup"><span data-stu-id="9a68d-292">For example: Transactions/sec is ~30, batch requests ~200, and user connects ~6.</span></span>

<span data-ttu-id="9a68d-293">Dans le cadre d’un déploiement distribué sur le graphique, lorsque le serveur de gestion & serveurs de publication utilise un réseau de liaison lente entre eux, le temps de réponse en boucle sur les serveurs de publication est limité à un délai de &lt; 5 secondes, même pour les demandes simultanées 100 sur un serveur de gestion unique.</span><span class="sxs-lookup"><span data-stu-id="9a68d-293">Using a geographically distributed deployment, where the management server & publishing servers utilize a slow link network between them, the round trip response time on the publishing servers is within acceptable time limits (&lt;5 seconds), even for 100 simultaneous requests on a single management server.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9a68d-294">Scénario</span><span class="sxs-lookup"><span data-stu-id="9a68d-294">Scenario</span></span></th>
<th align="left"><span data-ttu-id="9a68d-295">Variante</span><span class="sxs-lookup"><span data-stu-id="9a68d-295">Variation</span></span></th>
<th align="left"><span data-ttu-id="9a68d-296">Nombre de groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="9a68d-296">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="9a68d-297">Nombre de groupes d’accès</span><span class="sxs-lookup"><span data-stu-id="9a68d-297">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="9a68d-298">Nombre de serveurs de publication</span><span class="sxs-lookup"><span data-stu-id="9a68d-298">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="9a68d-299">Serveur de publication de type de connexion réseau/serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="9a68d-299">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="9a68d-300">Temps de réponse aller-retour sur le serveur de publication (en secondes)</span><span class="sxs-lookup"><span data-stu-id="9a68d-300">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="9a68d-301">Utilisation de l’UC sur le serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="9a68d-301">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-302">Connexion réseau entre le serveur de publication et le serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="9a68d-302">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a68d-303">Réseau de liaison lente 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="9a68d-303">1.5 Mbps Slow link Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-304">0,4</span><span class="sxs-lookup"><span data-stu-id="9a68d-304">0</span></span></p></li>
<li><p><span data-ttu-id="9a68d-305">0,4</span><span class="sxs-lookup"><span data-stu-id="9a68d-305">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-306">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-306">1</span></span></p></li>
<li><p><span data-ttu-id="9a68d-307">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-307">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-308">50</span><span class="sxs-lookup"><span data-stu-id="9a68d-308">50</span></span></p></li>
<li><p><span data-ttu-id="9a68d-309">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-309">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-310">Câble ADSL de 1,5 MB/s</span><span class="sxs-lookup"><span data-stu-id="9a68d-310">1.5Mbps Cable DSL</span></span></p></li>
<li><p><span data-ttu-id="9a68d-311">Câble ADSL de 1,5 MB/s</span><span class="sxs-lookup"><span data-stu-id="9a68d-311">1.5Mbps Cable DSL</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-312">n°4</span><span class="sxs-lookup"><span data-stu-id="9a68d-312">4</span></span></p></li>
<li><p><span data-ttu-id="9a68d-313">n°5</span><span class="sxs-lookup"><span data-stu-id="9a68d-313">5</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-314">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-314">1</span></span></p></li>
<li><p><span data-ttu-id="9a68d-315">deuxième</span><span class="sxs-lookup"><span data-stu-id="9a68d-315">2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a68d-316">Connexion réseau entre le serveur de publication et le serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="9a68d-316">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a68d-317">Réseau LAN/WIFI</span><span class="sxs-lookup"><span data-stu-id="9a68d-317">LAN / WIFI Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-318">0,4</span><span class="sxs-lookup"><span data-stu-id="9a68d-318">0</span></span></p></li>
<li><p><span data-ttu-id="9a68d-319">0,4</span><span class="sxs-lookup"><span data-stu-id="9a68d-319">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-320">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-320">1</span></span></p></li>
<li><p><span data-ttu-id="9a68d-321">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-321">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-322">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-322">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-323">200</span><span class="sxs-lookup"><span data-stu-id="9a68d-323">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-324">Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="9a68d-324">Wifi</span></span></p></li>
<li><p><span data-ttu-id="9a68d-325">Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="9a68d-325">Wifi</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-326">27,9</span><span class="sxs-lookup"><span data-stu-id="9a68d-326">11</span></span></p></li>
<li><p><span data-ttu-id="9a68d-327">CX3-20</span><span class="sxs-lookup"><span data-stu-id="9a68d-327">20</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-328">0,15</span><span class="sxs-lookup"><span data-stu-id="9a68d-328">15</span></span></p></li>
<li><p><span data-ttu-id="9a68d-329">Play</span><span class="sxs-lookup"><span data-stu-id="9a68d-329">17</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9a68d-330">Le serveur de gestion et les serveurs de publication sont connectés à un réseau de liaison lente ou d’un réseau haut débit, le serveur de gestion peut gérer approximativement 15 000 demandes d’actualisation de package dans 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="9a68d-330">Whether the management server and publishing servers are connected over a slow link network, or a high speed network, the management server can handle approximately 15,000 package refresh requests in 30 minutes.</span></span>

## <a href="" id="---------app-v-5-0-reporting-server-capacity-planning-recommendations"></a> <span data-ttu-id="9a68d-331">Recommandations pour la planification de la capacité du serveur App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="9a68d-331">App-V 5.0 Reporting Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="9a68d-332">Les clients App-V 5,0 envoient des données de création de rapports au serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="9a68d-332">App-V 5.0 clients send reporting data to the reporting server.</span></span> <span data-ttu-id="9a68d-333">Le serveur de création de rapports enregistre ensuite les informations dans la base de données Microsoft SQL Server et renvoie une notification réussie à l’ordinateur exécutant le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9a68d-333">The reporting server then records the information in the Microsoft SQL Server database and returns a successful notification back to the computer running App-V 5.0 client.</span></span> <span data-ttu-id="9a68d-334">Pour plus d’informations sur les configurations prises en charge par App-V 5,0 Report Server, voir [Configurations prises en charge par app-v 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="9a68d-334">For more information about App-V 5.0 Reporting Server supported configurations see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="9a68d-335">**Remarques**  Le temps de réponse aller-retour est le temps écoulé par l’ordinateur exécutant le client App-V 5,0 pour envoyer les informations de rapport au serveur de création de rapports et recevoir une notification réussie du serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="9a68d-335">**Note** Round trip response time is the time taken by the computer running the App-V 5.0 client to send the reporting information to the reporting server and receive a successful notification from the reporting server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9a68d-336">Scénario</span><span class="sxs-lookup"><span data-stu-id="9a68d-336">Scenario</span></span></th>
<th align="left"><span data-ttu-id="9a68d-337">Résumé</span><span class="sxs-lookup"><span data-stu-id="9a68d-337">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-338">Plusieurs clients App-V 5,0 envoient simultanément des informations de rapport au serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="9a68d-338">Multiple App-V 5.0 clients send reporting information to the reporting server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-339">Le temps de réponse en boucle du serveur de rapports est de 2,6 secondes pour les clients 500.</span><span class="sxs-lookup"><span data-stu-id="9a68d-339">Round trip response time from the reporting server is 2.6 seconds for 500 clients.</span></span></p></li>
<li><p><span data-ttu-id="9a68d-340">Le temps de réponse en boucle du serveur de rapports est de 5,65 secondes pour les clients 1000.</span><span class="sxs-lookup"><span data-stu-id="9a68d-340">Round trip response time from the reporting server is 5.65 seconds for 1000 clients.</span></span></p></li>
<li><p><span data-ttu-id="9a68d-341">Le temps de réponse en boucle augmente de façon linéaire en fonction du nombre de clients.</span><span class="sxs-lookup"><span data-stu-id="9a68d-341">Round trip response time increases linearly depending on number of clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a68d-342">Demandes par seconde traitées par le serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="9a68d-342">Requests per second processed by the reporting server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-343">Un serveur de création de rapports unique et une seule base de données peuvent traiter un maximum de demandes 139 par seconde.</span><span class="sxs-lookup"><span data-stu-id="9a68d-343">A single reporting server and a single database, can process a maximum of 139 requests per second.</span></span> <span data-ttu-id="9a68d-344">La moyenne est 121 demandes/secondes.</span><span class="sxs-lookup"><span data-stu-id="9a68d-344">The average is 121 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="9a68d-345">En utilisant deux serveurs de création de rapports sur la même base de données Microsoft SQL Server, la moyenne des demandes/secondes est similaire à un serveur de rapports unique = ~ 127, avec une limite de 278 demandes/seconde.</span><span class="sxs-lookup"><span data-stu-id="9a68d-345">Using two reporting servers reporting to the same Microsoft SQL Server database, the average requests/second is similar to a single reporting server = ~127, with a max of 278 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="9a68d-346">Un serveur de rapports unique peut traiter les connexions 500 concurrentes/actives.</span><span class="sxs-lookup"><span data-stu-id="9a68d-346">A single reporting server can process 500 concurrent/active connections.</span></span></p></li>
<li><p><span data-ttu-id="9a68d-347">Un serveur de rapports unique peut traiter une connexion simultanée 1500 maximum.</span><span class="sxs-lookup"><span data-stu-id="9a68d-347">A single reporting server can process a maximum 1500 concurrent connections.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-348">Base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="9a68d-348">Reporting Database.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-349">Le verrouillage du contenu sur l’ordinateur exécutant Microsoft SQL Server est le facteur de limitation pour les demandes/secondes.</span><span class="sxs-lookup"><span data-stu-id="9a68d-349">Lock contention on the computer running Microsoft SQL Server is the limiting factor for requests/second.</span></span></p></li>
<li><p><span data-ttu-id="9a68d-350">Le débit et le temps de réponse sont indépendants de la taille de la base de données.</span><span class="sxs-lookup"><span data-stu-id="9a68d-350">Throughput and response time are independent of database size.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9a68d-351">**Calcul du retard aléatoire**:</span><span class="sxs-lookup"><span data-stu-id="9a68d-351">**Calculating random delay**:</span></span>

<span data-ttu-id="9a68d-352">Le délai aléatoire spécifie le délai maximal (en minutes) pendant lequel les données doivent être envoyées au serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="9a68d-352">The random delay specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="9a68d-353">Lorsque la tâche planifiée est lancée, le client génère un délai aléatoire compris entre **0** et **ReportingRandomDelay** et attend la durée spécifiée avant d’envoyer des données.</span><span class="sxs-lookup"><span data-stu-id="9a68d-353">When the scheduled task is started, the client generates a random delay between **0** and **ReportingRandomDelay** and will wait the specified duration before sending data.</span></span>

<span data-ttu-id="9a68d-354">Retard aléatoire = 4 \ \* nombre de clients/demandes de moyenne par seconde.</span><span class="sxs-lookup"><span data-stu-id="9a68d-354">Random delay = 4 \* number of clients / average requests per second.</span></span>

<span data-ttu-id="9a68d-355">Exemple: pour les clients 500, avec des demandes 120 par seconde, le délai aléatoire est de 4 \ \* 500/120 = ~ 17 minutes.</span><span class="sxs-lookup"><span data-stu-id="9a68d-355">Example: For 500 clients, with 120 requests per second, the Random delay is, 4 \* 500 / 120 = ~17 minutes.</span></span>

## <a href="" id="---------app-v-5-0-publishing-server-capacity-planning-recommendations"></a> <span data-ttu-id="9a68d-356">Recommandations en matière de planification de la capacité du serveur Publisher V 5,0</span><span class="sxs-lookup"><span data-stu-id="9a68d-356">App-V 5.0 Publishing Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="9a68d-357">Les ordinateurs exécutant le client App-V 5,0 se connectent au serveur de publication App-V 5,0 pour envoyer une demande d’actualisation de publication et recevoir une réponse.</span><span class="sxs-lookup"><span data-stu-id="9a68d-357">Computers running the App-V 5.0 client connect to the App-V 5.0 publishing server to send a publishing refresh request and to receive a response.</span></span> <span data-ttu-id="9a68d-358">La durée de réponse en boucle est mesurée sur l’ordinateur exécutant le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9a68d-358">Round trip response time is measured on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="9a68d-359">La durée du processeur est mesurée sur le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="9a68d-359">Processor time is measured on the publishing server.</span></span> <span data-ttu-id="9a68d-360">Pour plus d’informations sur les configurations prises en charge par le serveur de publication App-V 5,0, consultez la rubrique [configurations App-v 5,0 prises en charge](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="9a68d-360">For more information about App-V 5.0 Publishing Server supported configurations see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

<span data-ttu-id="9a68d-361">**Important**  La liste suivante indique les principaux facteurs à prendre en compte lors de la configuration du serveur de publication 5,0 App-V.</span><span class="sxs-lookup"><span data-stu-id="9a68d-361">**Important** The following list displays the main factors to consider when setting up the App-V 5.0 publishing server:</span></span>

-   <span data-ttu-id="9a68d-362">Nombre de clients qui se connectent simultanément à un serveur de publication unique.</span><span class="sxs-lookup"><span data-stu-id="9a68d-362">The number of clients connecting simultaneously to a single publishing server.</span></span>

-   <span data-ttu-id="9a68d-363">Nombre de packages de chaque actualisation.</span><span class="sxs-lookup"><span data-stu-id="9a68d-363">The number of packages in each refresh.</span></span>

-   <span data-ttu-id="9a68d-364">La bande passante réseau disponible dans votre environnement entre le client et le serveur de publication 5,0 de l’application.</span><span class="sxs-lookup"><span data-stu-id="9a68d-364">The available network bandwidth in your environment between the client and the App-V 5.0 publishing server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9a68d-365">Scénario</span><span class="sxs-lookup"><span data-stu-id="9a68d-365">Scenario</span></span></th>
<th align="left"><span data-ttu-id="9a68d-366">Résumé</span><span class="sxs-lookup"><span data-stu-id="9a68d-366">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-367">Plusieurs clients App-V 5,0 se connectent à un serveur de publication unique simultanément.</span><span class="sxs-lookup"><span data-stu-id="9a68d-367">Multiple App-V 5.0 clients connect to a single publishing server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-368">Un serveur de publication exécutant des processeurs double cœur peut répondre à la plupart des clients 5000 demandant une actualisation simultanée.</span><span class="sxs-lookup"><span data-stu-id="9a68d-368">A publishing server running dual core processors can respond to at most 5000 clients requesting a refresh simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="9a68d-369">Pour les clients 5000-10000, le serveur de publication nécessite un minimum de quatre cœurs.</span><span class="sxs-lookup"><span data-stu-id="9a68d-369">For 5000-10000 clients, the publishing server requires a minimum quad core.</span></span></p></li>
<li><p><span data-ttu-id="9a68d-370">Pour les clients 10000-20000, le serveur de publication doit disposer de deux cœurs pour des temps de réponse plus efficaces.</span><span class="sxs-lookup"><span data-stu-id="9a68d-370">For 10000-20000 clients, the publishing server should have dual quad cores for more efficient response times.</span></span></p></li>
<li><p><span data-ttu-id="9a68d-371">Un serveur de publication avec un noyau à quatre cœurs peut actualiser jusqu’à 10000 packages dans un délai de 3 secondes.</span><span class="sxs-lookup"><span data-stu-id="9a68d-371">A publishing server with a quad core can refresh up to 10000 packages within 3 seconds.</span></span> <span data-ttu-id="9a68d-372">(Prise en charge des clients simultanés 10000)</span><span class="sxs-lookup"><span data-stu-id="9a68d-372">(Supporting 10000 simultaneous clients)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a68d-373">Nombre de packages de chaque actualisation.</span><span class="sxs-lookup"><span data-stu-id="9a68d-373">Number of packages in each refresh.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-374">L’augmentation du nombre de packages augmente le délai de réponse de ~ 40% (jusqu’à 1000 Packages).</span><span class="sxs-lookup"><span data-stu-id="9a68d-374">Increasing number of packages will increase response time by ~40% (up to 1000 packages).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-375">Réseau entre le client App-V 5,0 et le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="9a68d-375">Network between the App-V 5.0 client and the publishing server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-376">Sur une connexion réseau lente (bande passante 1,5 Mbps), il existe un délai de réponse d' 97% par rapport au réseau local (jusqu’à 1000 utilisateurs).</span><span class="sxs-lookup"><span data-stu-id="9a68d-376">Across a slow network (1.5 Mbps bandwidth), there is a 97% increase in response time compared to LAN (up to 1000 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9a68d-377">**Remarques**  Le taux d’utilisation de l’UC du serveur de publication est toujours élevé pendant l’intervalle de temps pendant lequel il doit traiter les demandes simultanées ( &gt; 90% dans la plupart des cas).</span><span class="sxs-lookup"><span data-stu-id="9a68d-377">**Note** The publishing server CPU usage is always high during the time interval when it has to process simultaneous requests (&gt;90% in most cases).</span></span> <span data-ttu-id="9a68d-378">Le serveur de publication peut gérer les demandes du client ~ 1500 en 1 seconde.</span><span class="sxs-lookup"><span data-stu-id="9a68d-378">The publishing server can handle ~1500 client requests in 1 second.</span></span>

 

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9a68d-379">Scénario</span><span class="sxs-lookup"><span data-stu-id="9a68d-379">Scenario</span></span></th>
<th align="left"><span data-ttu-id="9a68d-380">Variante</span><span class="sxs-lookup"><span data-stu-id="9a68d-380">Variation</span></span></th>
<th align="left"><span data-ttu-id="9a68d-381">Nombre de clients App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="9a68d-381">Number of App-V 5.0 clients</span></span></th>
<th align="left"><span data-ttu-id="9a68d-382">Nombre de packages</span><span class="sxs-lookup"><span data-stu-id="9a68d-382">Number of packages</span></span></th>
<th align="left"><span data-ttu-id="9a68d-383">Configuration du processeur sur le serveur de publication</span><span class="sxs-lookup"><span data-stu-id="9a68d-383">Processor configuration on the publishing server</span></span></th>
<th align="left"><span data-ttu-id="9a68d-384">Type de connexion réseau-client de publication de type serveur/App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="9a68d-384">Network connection type publishing server / App-V 5.0 client</span></span></th>
<th align="left"><span data-ttu-id="9a68d-385">Durée de l’aller-retour sur le client App-V 5,0 (en secondes)</span><span class="sxs-lookup"><span data-stu-id="9a68d-385">Round trip time on the App-V 5.0 client (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="9a68d-386">Utilisation de l’UC sur le serveur de publication (en%)</span><span class="sxs-lookup"><span data-stu-id="9a68d-386">CPU utilization on publishing server (in %)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-387">Le client App-V 5,0 envoie une demande d’actualisation &amp; de publication reçoit une réponse, chaque requête contenant des packages 120</span><span class="sxs-lookup"><span data-stu-id="9a68d-387">App-V 5.0 client sends publishing refresh request &amp; receives response, each request containing 120 packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a68d-388">Nombre de clients</span><span class="sxs-lookup"><span data-stu-id="9a68d-388">Number of clients</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-389">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-389">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-390">1000</span><span class="sxs-lookup"><span data-stu-id="9a68d-390">1000</span></span></p></li>
<li><p><span data-ttu-id="9a68d-391">5000</span><span class="sxs-lookup"><span data-stu-id="9a68d-391">5000</span></span></p></li>
<li><p><span data-ttu-id="9a68d-392">10000</span><span class="sxs-lookup"><span data-stu-id="9a68d-392">10000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-393">120</span><span class="sxs-lookup"><span data-stu-id="9a68d-393">120</span></span></p></li>
<li><p><span data-ttu-id="9a68d-394">120</span><span class="sxs-lookup"><span data-stu-id="9a68d-394">120</span></span></p></li>
<li><p><span data-ttu-id="9a68d-395">120</span><span class="sxs-lookup"><span data-stu-id="9a68d-395">120</span></span></p></li>
<li><p><span data-ttu-id="9a68d-396">120</span><span class="sxs-lookup"><span data-stu-id="9a68d-396">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-397">Double cœur</span><span class="sxs-lookup"><span data-stu-id="9a68d-397">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="9a68d-398">Double cœur</span><span class="sxs-lookup"><span data-stu-id="9a68d-398">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="9a68d-399">Quadruple cœur</span><span class="sxs-lookup"><span data-stu-id="9a68d-399">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="9a68d-400">Quadruple cœur</span><span class="sxs-lookup"><span data-stu-id="9a68d-400">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-401">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-401">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-402">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-402">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-403">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-403">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-404">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-404">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-405">1</span><span class="sxs-lookup"><span data-stu-id="9a68d-405">1</span></span></p></li>
<li><p><span data-ttu-id="9a68d-406">deuxième</span><span class="sxs-lookup"><span data-stu-id="9a68d-406">2</span></span></p></li>
<li><p><span data-ttu-id="9a68d-407">deuxième</span><span class="sxs-lookup"><span data-stu-id="9a68d-407">2</span></span></p></li>
<li><p><span data-ttu-id="9a68d-408">3D</span><span class="sxs-lookup"><span data-stu-id="9a68d-408">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-409">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-409">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-410">99</span><span class="sxs-lookup"><span data-stu-id="9a68d-410">99</span></span></p></li>
<li><p><span data-ttu-id="9a68d-411">89</span><span class="sxs-lookup"><span data-stu-id="9a68d-411">89</span></span></p></li>
<li><p><span data-ttu-id="9a68d-412">77</span><span class="sxs-lookup"><span data-stu-id="9a68d-412">77</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a68d-413">Plusieurs packages pour chaque actualisation</span><span class="sxs-lookup"><span data-stu-id="9a68d-413">Multiple packages in each refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a68d-414">Nombre de packages</span><span class="sxs-lookup"><span data-stu-id="9a68d-414">Number of packages</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-415">1000</span><span class="sxs-lookup"><span data-stu-id="9a68d-415">1000</span></span></p></li>
<li><p><span data-ttu-id="9a68d-416">1000</span><span class="sxs-lookup"><span data-stu-id="9a68d-416">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-417">500</span><span class="sxs-lookup"><span data-stu-id="9a68d-417">500</span></span></p></li>
<li><p><span data-ttu-id="9a68d-418">1000</span><span class="sxs-lookup"><span data-stu-id="9a68d-418">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-419">Quadruple cœur</span><span class="sxs-lookup"><span data-stu-id="9a68d-419">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="9a68d-420">Quadruple cœur</span><span class="sxs-lookup"><span data-stu-id="9a68d-420">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-421">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-421">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-422">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-422">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-423">deuxième</span><span class="sxs-lookup"><span data-stu-id="9a68d-423">2</span></span></p></li>
<li><p><span data-ttu-id="9a68d-424">3D</span><span class="sxs-lookup"><span data-stu-id="9a68d-424">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-425">92</span><span class="sxs-lookup"><span data-stu-id="9a68d-425">92</span></span></p></li>
<li><p><span data-ttu-id="9a68d-426">91</span><span class="sxs-lookup"><span data-stu-id="9a68d-426">91</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-427">Réseau entre le client et le serveur de publication</span><span class="sxs-lookup"><span data-stu-id="9a68d-427">Network between client and publishing server</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a68d-428">réseau de liaison lente 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="9a68d-428">1.5 Mbps Slow link network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-429">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-429">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-430">500</span><span class="sxs-lookup"><span data-stu-id="9a68d-430">500</span></span></p></li>
<li><p><span data-ttu-id="9a68d-431">1000</span><span class="sxs-lookup"><span data-stu-id="9a68d-431">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-432">120</span><span class="sxs-lookup"><span data-stu-id="9a68d-432">120</span></span></p></li>
<li><p><span data-ttu-id="9a68d-433">120</span><span class="sxs-lookup"><span data-stu-id="9a68d-433">120</span></span></p></li>
<li><p><span data-ttu-id="9a68d-434">120</span><span class="sxs-lookup"><span data-stu-id="9a68d-434">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-435">Quadruple cœur</span><span class="sxs-lookup"><span data-stu-id="9a68d-435">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="9a68d-436">Quadruple cœur</span><span class="sxs-lookup"><span data-stu-id="9a68d-436">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="9a68d-437">Quadruple cœur</span><span class="sxs-lookup"><span data-stu-id="9a68d-437">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-438">Réseau intra-continent 1,5 MB/s</span><span class="sxs-lookup"><span data-stu-id="9a68d-438">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-439">3D</span><span class="sxs-lookup"><span data-stu-id="9a68d-439">3</span></span></p></li>
<li><p><span data-ttu-id="9a68d-440">10 (avec le taux d’échec de 0,2%)</span><span class="sxs-lookup"><span data-stu-id="9a68d-440">10 (with 0.2% failure rate)</span></span></p></li>
<li><p><span data-ttu-id="9a68d-441">17 (avec un taux d’échec de 1%)</span><span class="sxs-lookup"><span data-stu-id="9a68d-441">17 (with 1% failure rate)</span></span></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-0-streaming-capacity-planning-recommendations"></a> <span data-ttu-id="9a68d-442">Recommandations en matière de planification de capacité de flux d’application V 5,0</span><span class="sxs-lookup"><span data-stu-id="9a68d-442">App-V 5.0 Streaming Capacity Planning Recommendations</span></span>


<span data-ttu-id="9a68d-443">Les ordinateurs exécutant le client App-V 5,0 diffusent le package de l’application virtuelle à partir du serveur de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="9a68d-443">Computers running the App-V 5.0 client stream the virtual application package from the streaming server.</span></span> <span data-ttu-id="9a68d-444">La durée de réponse en boucle est mesurée sur l’ordinateur exécutant le client App-V 5,0 et est le temps nécessaire pour diffuser l’intégralité du package.</span><span class="sxs-lookup"><span data-stu-id="9a68d-444">Round trip response time is measured on the computer running the App-V 5.0 client, and is the time taken to stream the entire package.</span></span>

<span data-ttu-id="9a68d-445">**Important**  La liste suivante indique les principaux facteurs à prendre en compte lors de la configuration du serveur de streaming App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="9a68d-445">**Important** The following list identifies the main factors to consider when setting up the App-V 5.0 streaming server:</span></span>

-   <span data-ttu-id="9a68d-446">Le nombre de clients en diffusant des packages d’application simultanément depuis un serveur de diffusion unique.</span><span class="sxs-lookup"><span data-stu-id="9a68d-446">The number of clients streaming application packages simultaneously from a single streaming server.</span></span>

-   <span data-ttu-id="9a68d-447">Taille du package en cours de diffusion.</span><span class="sxs-lookup"><span data-stu-id="9a68d-447">The size of the package being streamed.</span></span>

-   <span data-ttu-id="9a68d-448">La bande passante réseau disponible dans votre environnement entre le client et le serveur de diffusion.</span><span class="sxs-lookup"><span data-stu-id="9a68d-448">The available network bandwidth in your environment between the client and the streaming server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9a68d-449">Scénario</span><span class="sxs-lookup"><span data-stu-id="9a68d-449">Scenario</span></span></th>
<th align="left"><span data-ttu-id="9a68d-450">Résumé</span><span class="sxs-lookup"><span data-stu-id="9a68d-450">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-451">Plusieurs clients App-V 5,0 diffusent simultanément des applications à partir d’un serveur en flux unique.</span><span class="sxs-lookup"><span data-stu-id="9a68d-451">Multiple App-V 5.0 clients stream applications from a single streaming server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-452">Si le nombre de clients diffusés en continu à partir du même serveur augmente, il existe une relation linéaire avec le temps de téléchargement/de diffusion du package.</span><span class="sxs-lookup"><span data-stu-id="9a68d-452">If the number of clients simultaneously streaming from the same server increases, there is a linear relationship with the package download/streaming time.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a68d-453">Taille du package en cours de diffusion.</span><span class="sxs-lookup"><span data-stu-id="9a68d-453">Size of the package being streamed.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-454">La taille du package a un impact significatif sur le temps de diffusion/téléchargement uniquement pour les packages plus grands dont la taille est de ~ 1 Go.</span><span class="sxs-lookup"><span data-stu-id="9a68d-454">The package size has a significant impact on the streaming/download time only for larger packages with a size ~ 1GB.</span></span> <span data-ttu-id="9a68d-455">Pour les tailles de packages comprises entre 3 Mo et 100 Mo, la durée de diffusion varie de 20 secondes à 100 secondes, avec les clients simultanés 100.</span><span class="sxs-lookup"><span data-stu-id="9a68d-455">For package sizes ranging from 3 MB to 100 MB, the streaming time ranges from 20 seconds to 100 seconds, with 100 simultaneous clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-456">Réseau entre le client App-V 5,0 et le serveur de streaming.</span><span class="sxs-lookup"><span data-stu-id="9a68d-456">Network between the App-V 5.0 client and the streaming server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-457">Sur une connexion réseau lente (bande passante 1,5 Mbps), il existe un délai de réponse d' 70-80% par rapport au réseau local (jusqu’à 100 utilisateurs).</span><span class="sxs-lookup"><span data-stu-id="9a68d-457">Across a slow network (1.5 Mbps bandwidth), there is a 70-80% increase in response time compared to LAN (up to 100 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9a68d-458">Le tableau suivant présente des exemples de valeurs pour chacun des facteurs de la liste précédente:</span><span class="sxs-lookup"><span data-stu-id="9a68d-458">The following table displays sample values for each of the factors in the previous list:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9a68d-459">Scénario</span><span class="sxs-lookup"><span data-stu-id="9a68d-459">Scenario</span></span></th>
<th align="left"><span data-ttu-id="9a68d-460">Variante</span><span class="sxs-lookup"><span data-stu-id="9a68d-460">Variation</span></span></th>
<th align="left"><span data-ttu-id="9a68d-461">Nombre de clients App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="9a68d-461">Number of App-V 5.0 clients</span></span></th>
<th align="left"><span data-ttu-id="9a68d-462">Taille de chaque package</span><span class="sxs-lookup"><span data-stu-id="9a68d-462">Size of each package</span></span></th>
<th align="left"><span data-ttu-id="9a68d-463">Serveur de type connexion réseau/client App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="9a68d-463">Network connection type streaming server / App-V 5.0 client</span></span></th>
<th align="left"><span data-ttu-id="9a68d-464">Durée de l’aller-retour sur le client App-V 5,0 (en secondes)</span><span class="sxs-lookup"><span data-stu-id="9a68d-464">Round trip time on the App-V 5.0 client (in seconds)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-465">Plusieurs clients App-V 5,0 diffusent des packages d’application virtuels à partir d’un serveur en flux continu.</span><span class="sxs-lookup"><span data-stu-id="9a68d-465">Multiple App-V 5.0 clients streaming virtual application packages from a streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a68d-466">Nombre de clients.</span><span class="sxs-lookup"><span data-stu-id="9a68d-466">Number of clients.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-467">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-467">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-468">200</span><span class="sxs-lookup"><span data-stu-id="9a68d-468">200</span></span></p></li>
<li><p><span data-ttu-id="9a68d-469">1000</span><span class="sxs-lookup"><span data-stu-id="9a68d-469">1000</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="9a68d-470">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-470">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-471">200</span><span class="sxs-lookup"><span data-stu-id="9a68d-471">200</span></span></p></li>
<li><p><span data-ttu-id="9a68d-472">1000</span><span class="sxs-lookup"><span data-stu-id="9a68d-472">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-473">3,5 Mo</span><span class="sxs-lookup"><span data-stu-id="9a68d-473">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="9a68d-474">3,5 Mo</span><span class="sxs-lookup"><span data-stu-id="9a68d-474">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="9a68d-475">3,5 Mo</span><span class="sxs-lookup"><span data-stu-id="9a68d-475">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="9a68d-476">5 MO</span><span class="sxs-lookup"><span data-stu-id="9a68d-476">5 MB</span></span></p></li>
<li><p><span data-ttu-id="9a68d-477">5 MO</span><span class="sxs-lookup"><span data-stu-id="9a68d-477">5 MB</span></span></p></li>
<li><p><span data-ttu-id="9a68d-478">5 MO</span><span class="sxs-lookup"><span data-stu-id="9a68d-478">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-479">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-479">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-480">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-480">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-481">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-481">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="9a68d-482">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-482">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-483">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-483">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-484">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-484">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-485">mai</span><span class="sxs-lookup"><span data-stu-id="9a68d-485">29</span></span></p></li>
<li><p><span data-ttu-id="9a68d-486">39</span><span class="sxs-lookup"><span data-stu-id="9a68d-486">39</span></span></p></li>
<li><p><span data-ttu-id="9a68d-487">391</span><span class="sxs-lookup"><span data-stu-id="9a68d-487">391</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="9a68d-488">35</span><span class="sxs-lookup"><span data-stu-id="9a68d-488">35</span></span></p></li>
<li><p><span data-ttu-id="9a68d-489">68</span><span class="sxs-lookup"><span data-stu-id="9a68d-489">68</span></span></p></li>
<li><p><span data-ttu-id="9a68d-490">461</span><span class="sxs-lookup"><span data-stu-id="9a68d-490">461</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a68d-491">Taille de chaque package en cours de diffusion.</span><span class="sxs-lookup"><span data-stu-id="9a68d-491">Size of each package being streamed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a68d-492">Taille de chaque package.</span><span class="sxs-lookup"><span data-stu-id="9a68d-492">Size of each package.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-493">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-493">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-494">200</span><span class="sxs-lookup"><span data-stu-id="9a68d-494">200</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="9a68d-495">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-495">100</span></span></p></li>
<li><p><span data-ttu-id="9a68d-496">200</span><span class="sxs-lookup"><span data-stu-id="9a68d-496">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-497">21 MO</span><span class="sxs-lookup"><span data-stu-id="9a68d-497">21 MB</span></span></p></li>
<li><p><span data-ttu-id="9a68d-498">21 MO</span><span class="sxs-lookup"><span data-stu-id="9a68d-498">21 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="9a68d-499">109</span><span class="sxs-lookup"><span data-stu-id="9a68d-499">109</span></span></p></li>
<li><p><span data-ttu-id="9a68d-500">109</span><span class="sxs-lookup"><span data-stu-id="9a68d-500">109</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-501">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-501">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-502">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-502">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="9a68d-503">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-503">LAN</span></span></p></li>
<li><p><span data-ttu-id="9a68d-504">Réseau local</span><span class="sxs-lookup"><span data-stu-id="9a68d-504">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="9a68d-505">33</span><span class="sxs-lookup"><span data-stu-id="9a68d-505">33</span></span></p>
<p><span data-ttu-id="9a68d-506">83</span><span class="sxs-lookup"><span data-stu-id="9a68d-506">83</span></span></p>
<p></p>
<p><span data-ttu-id="9a68d-507">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-507">100</span></span></p>
<p><span data-ttu-id="9a68d-508">160</span><span class="sxs-lookup"><span data-stu-id="9a68d-508">160</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a68d-509">Connexion réseau entre le client et le serveur de streaming App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9a68d-509">Network connection between client and App-V 5.0 streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a68d-510">1,5 Mbps réseau de liaison lente.</span><span class="sxs-lookup"><span data-stu-id="9a68d-510">1.5 Mbps Slow link network.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-511">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-511">100</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="9a68d-512">100</span><span class="sxs-lookup"><span data-stu-id="9a68d-512">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-513">3,5 Mo</span><span class="sxs-lookup"><span data-stu-id="9a68d-513">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="9a68d-514">5 MO</span><span class="sxs-lookup"><span data-stu-id="9a68d-514">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="9a68d-515">Réseau intra-continent 1,5 MB/s</span><span class="sxs-lookup"><span data-stu-id="9a68d-515">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="9a68d-516">102</span><span class="sxs-lookup"><span data-stu-id="9a68d-516">102</span></span></p>
<p></p>
<p><span data-ttu-id="9a68d-517">121</span><span class="sxs-lookup"><span data-stu-id="9a68d-517">121</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9a68d-518">Chaque serveur de streaming App-V 5,0 doit être en mesure de gérer un minimum de clients 200 en continu à partir d’applications virtualisées.</span><span class="sxs-lookup"><span data-stu-id="9a68d-518">Each App-V 5.0 streaming server should be able to handle a minimum of 200 clients concurrently streaming virtualized applications.</span></span>

<span data-ttu-id="9a68d-519">**Remarques**  La durée réelle du flux est déterminée principalement par le nombre de clients diffusés en continu, le nombre de packages, la taille du package, l’activité réseau du serveur et les conditions du réseau.</span><span class="sxs-lookup"><span data-stu-id="9a68d-519">**Note** The actual time to it will take to stream is determined primarily by the number of clients streaming simultaneously, number of packages, package size, the server’s network activity, and network conditions.</span></span>

 

<span data-ttu-id="9a68d-520">Par exemple, un utilisateur moyen peut diffuser un package 100 Mo en moins de 2 minutes, lorsque 100 clients simultanés sont en continu à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="9a68d-520">For example, an average user can stream a 100 MB package in less than 2 minutes, when 100 simultaneous clients are streaming from the server.</span></span> <span data-ttu-id="9a68d-521">Toutefois, un paquet d’une taille de 1 Go peut durer jusqu’à 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="9a68d-521">However, a package of size 1 GB could take up to 30 minutes.</span></span> <span data-ttu-id="9a68d-522">Dans la plupart des environnements réalistes, la diffusion en continu n’est pas uniformément distribuée, vous devez comprendre les exigences de flux maximal en matière de diffusion actuelles dans votre environnement afin de dimensionner correctement le nombre de serveurs de diffusion en continu requis.</span><span class="sxs-lookup"><span data-stu-id="9a68d-522">In most real world environments streaming demand is not uniformly distributed, you will need to understand the approximate peak streaming requirements present in your environment in order to properly size the number of required streaming servers.</span></span>

<span data-ttu-id="9a68d-523">Le nombre de clients qu’un serveur en continu peut prendre en charge peut être considérablement augmenté et les exigences en matière de flux maximal réduites si vous prémettez vos applications en cache.</span><span class="sxs-lookup"><span data-stu-id="9a68d-523">The number of clients a streaming server can support can be significantly increased and the peak streaming requirements reduced if you pre-cache your applications.</span></span> <span data-ttu-id="9a68d-524">Vous pouvez également augmenter le nombre de clients pris en charge par un serveur de diffusion en utilisant la diffusion en continu à la demande et des packages optimisés pour les flux.</span><span class="sxs-lookup"><span data-stu-id="9a68d-524">You can also increase the number of clients a streaming server can support by using on-demand streaming delivery and stream optimized packages.</span></span>

## <span data-ttu-id="9a68d-525">Combinaison des rôles de serveur App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="9a68d-525">Combining App-V 5.0 Server Roles</span></span>


<span data-ttu-id="9a68d-526">Remise de la mise à l’échelle et des exigences de tolérance de panne, le nombre minimal de serveurs nécessaires pour un emplacement avec la connectivité à Active Directory est un.</span><span class="sxs-lookup"><span data-stu-id="9a68d-526">Discounting scaling and fault-tolerance requirements, the minimum number of servers needed for a location with connectivity to Active Directory is one.</span></span> <span data-ttu-id="9a68d-527">Ce serveur va héberger le serveur de gestion, le service serveur de gestion et les rôles Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9a68d-527">This server will host the management server, management server service, and Microsoft SQL Server roles.</span></span> <span data-ttu-id="9a68d-528">Les rôles de serveur peuvent donc être organisés selon n’importe quelle combinaison souhaitée, car ils ne sont pas en conflit entre eux.</span><span class="sxs-lookup"><span data-stu-id="9a68d-528">Server roles, therefore, can be arranged in any desired combination since they do not conflict with one another.</span></span>

<span data-ttu-id="9a68d-529">En ignorant les exigences de mise à l’échelle, le nombre minimum de serveurs nécessaires à la fourniture d’une implémentation tolérante aux pannes est de quatre.</span><span class="sxs-lookup"><span data-stu-id="9a68d-529">Ignoring scaling requirements, the minimum number of servers necessary to provide a fault-tolerant implementation is four.</span></span> <span data-ttu-id="9a68d-530">Le serveur de gestion et les rôles Microsoft SQL Server pris en charge sont placés dans des configurations tolérantes aux pannes.</span><span class="sxs-lookup"><span data-stu-id="9a68d-530">The management server, and Microsoft SQL Server roles support being placed in fault-tolerant configurations.</span></span> <span data-ttu-id="9a68d-531">Le service du serveur de gestion peut être combiné avec n’importe lequel des rôles, mais il reste un point de défaillance unique.</span><span class="sxs-lookup"><span data-stu-id="9a68d-531">The management server service can be combined with any of the roles, but remains a single point of failure.</span></span>

<span data-ttu-id="9a68d-532">Bien qu’il existe un certain nombre de stratégies et de technologies de tolérance de panne disponibles, elles ne s’appliquent pas à un service donné.</span><span class="sxs-lookup"><span data-stu-id="9a68d-532">Although there are a number of fault-tolerance strategies and technologies available, not all are applicable to a given service.</span></span> <span data-ttu-id="9a68d-533">De plus, si les rôles App-V 5,0 sont combinés, certaines options de tolérance de panne risquent de ne plus être applicables en raison d’incompatibilités.</span><span class="sxs-lookup"><span data-stu-id="9a68d-533">Additionally, if App-V 5.0 roles are combined, certain fault-tolerance options may no longer apply due to incompatibilities.</span></span>






## <span data-ttu-id="9a68d-534">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9a68d-534">Related topics</span></span>


[<span data-ttu-id="9a68d-535">Configurations prises en charge d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="9a68d-535">App-V 5.0 Supported Configurations</span></span>](app-v-50-supported-configurations.md)

[<span data-ttu-id="9a68d-536">Planification de la haute disponibilité avec App-V5.0</span><span class="sxs-lookup"><span data-stu-id="9a68d-536">Planning for High Availability with App-V 5.0</span></span>](planning-for-high-availability-with-app-v-50.md)

[<span data-ttu-id="9a68d-537">Envisager de déployer App-V</span><span class="sxs-lookup"><span data-stu-id="9a68d-537">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v.md)

 

 





