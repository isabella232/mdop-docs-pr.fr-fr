---
title: Planification de la capacité d'App-V5.1
description: Planification de la capacité d'App-V5.1
author: dansimp
ms.assetid: 7a98062f-5a60-49d6-ab40-dc6057e1dd5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b152536b3c61e47f3fda84489b1e102c285e01c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805988"
---
# <span data-ttu-id="7be9e-103">Planification de la capacité d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="7be9e-103">App-V 5.1 Capacity Planning</span></span>


<span data-ttu-id="7be9e-104">Les recommandations suivantes peuvent être utilisées comme planning de référence afin de vous aider à déterminer les informations de planification appropriées pour l’infrastructure App-V 5,1 de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7be9e-104">The following recommendations can be used as a baseline to help determine capacity planning information that is appropriate to your organization’s App-V 5.1 infrastructure.</span></span>

<span data-ttu-id="7be9e-105">**Important**  Utilisez les informations de cette section uniquement en tant que guide général pour la planification de votre déploiement d’application-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7be9e-105">**Important** Use the information in this section only as a general guide for planning your App-V 5.1 deployment.</span></span> <span data-ttu-id="7be9e-106">La capacité requise de votre système dépend des détails spécifiques de votre matériel et de votre environnement applicatif.</span><span class="sxs-lookup"><span data-stu-id="7be9e-106">Your system capacity requirements will depend on the specific details of your hardware and application environment.</span></span> <span data-ttu-id="7be9e-107">Par ailleurs, les numéros de performance indiqués dans ce document sont des exemples et vos résultats peuvent varier.</span><span class="sxs-lookup"><span data-stu-id="7be9e-107">Additionally, the performance numbers displayed in this document are examples and your results may vary.</span></span>

 

## <span data-ttu-id="7be9e-108">Déterminez l’objectif du projet</span><span class="sxs-lookup"><span data-stu-id="7be9e-108">Determine the Project Scope</span></span>


<span data-ttu-id="7be9e-109">Avant de concevoir l’infrastructure App-V 5,1, vous devez déterminer l’étendue du projet.</span><span class="sxs-lookup"><span data-stu-id="7be9e-109">Before you design the App-V 5.1 infrastructure, you must determine the project’s scope.</span></span> <span data-ttu-id="7be9e-110">L’étendue consiste à déterminer les applications qui seront disponibles virtuellement et à identifier les utilisateurs cibles et leurs emplacements.</span><span class="sxs-lookup"><span data-stu-id="7be9e-110">The scope consists of determining which applications will be available virtually and to also identify the target users, and their locations.</span></span> <span data-ttu-id="7be9e-111">Ces informations vous aideront à déterminer le type d’infrastructure App-V 5,1 à implémenter.</span><span class="sxs-lookup"><span data-stu-id="7be9e-111">This information will help determine what type of App-V 5.1 infrastructure should be implemented.</span></span> <span data-ttu-id="7be9e-112">Les décisions relatives à l’étendue du projet doivent être basées sur les besoins spécifiques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7be9e-112">Decisions about the scope of the project must be based on the specific needs of your organization.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7be9e-113">Tâche</span><span class="sxs-lookup"><span data-stu-id="7be9e-113">Task</span></span></th>
<th align="left"><span data-ttu-id="7be9e-114">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="7be9e-114">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-115">Déterminer l’étendue de l’application</span><span class="sxs-lookup"><span data-stu-id="7be9e-115">Determine Application Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be9e-116">En fonction des applications à virtualiser, l’infrastructure App-V 5,1 peut être définie de différentes manières.</span><span class="sxs-lookup"><span data-stu-id="7be9e-116">Depending on the applications to be virtualized, the App-V 5.1 infrastructure can be set up in different ways.</span></span> <span data-ttu-id="7be9e-117">La première tâche consiste à définir les applications que vous voulez virtualiser.</span><span class="sxs-lookup"><span data-stu-id="7be9e-117">The first task is to define what applications you want to virtualize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7be9e-118">Déterminer l’étendue de l’emplacement</span><span class="sxs-lookup"><span data-stu-id="7be9e-118">Determine Location Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be9e-119">Le champ étendue de l’emplacement fait référence aux emplacements physiques (par exemple, à l’échelle de l’entreprise ou à un emplacement géographique spécifique) sur lequel vous envisagez d’exécuter les applications virtualisées.</span><span class="sxs-lookup"><span data-stu-id="7be9e-119">Location scope refers to the physical locations (for example, enterprise-wide or a specific geographic location) where you plan to run the virtualized applications.</span></span> <span data-ttu-id="7be9e-120">Elle peut également faire référence à la population des utilisateurs (par exemple, un service unique) qui exécuteront les applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="7be9e-120">It can also refer to the user population (for example, a single department) who will run the virtual applications.</span></span> <span data-ttu-id="7be9e-121">Vous devriez obtenir une carte réseau qui inclut les chemins de connexion ainsi que la bande passante disponible vers chaque emplacement et le nombre d’utilisateurs qui utilisent des applications virtualisées et la vitesse de liaison du réseau étendu.</span><span class="sxs-lookup"><span data-stu-id="7be9e-121">You should obtain a network map that includes the connection paths as well as available bandwidth to each location and the number of users using virtualized applications and the WAN link speed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7be9e-122">Déterminer l’infrastructure App-V 5,1 requise</span><span class="sxs-lookup"><span data-stu-id="7be9e-122">Determine Which App-V 5.1 Infrastructure is Required</span></span>


<span data-ttu-id="7be9e-123">**Important**  Les deux modèles suivants requièrent que le client App-V 5,1 soit installé sur l’ordinateur sur lequel vous envisagez d’exécuter des applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="7be9e-123">**Important** Both of the following models require the App-V 5.1 client to be installed on the computer where you plan to run virtual applications.</span></span>

<span data-ttu-id="7be9e-124">Vous pouvez également gérer votre environnement App-V 5,1 à l’aide d’une solution de distribution de logiciels électronique (ESD) telle que Microsoft Systems Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7be9e-124">You can also manage your App-V 5.1 environment using an Electronic Software Distribution (ESD) solution such as Microsoft Systems Center Configuration Manager.</span></span> <span data-ttu-id="7be9e-125">Pour plus d’informations, reportez-vous [au déploiement de packages d’application V 5,1 à l’aide de la distribution de logiciels électroniques](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span><span class="sxs-lookup"><span data-stu-id="7be9e-125">For more information see [How to deploy App-V 5.1 Packages Using Electronic Software Distribution](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span></span>

 

-   <span data-ttu-id="7be9e-126">**Modèle autonome** -le modèle autonome permet aux applications virtuelles d’être activées pour la distribution sans streaming.</span><span class="sxs-lookup"><span data-stu-id="7be9e-126">**Standalone Model** - The standalone model allows virtual applications to be Windows Installer-enabled for distribution without streaming.</span></span> <span data-ttu-id="7be9e-127">App-V 5,1 en mode autonome se compose du Sequencer et du client; aucun composant supplémentaire n’est requis.</span><span class="sxs-lookup"><span data-stu-id="7be9e-127">App-V 5.1 in Standalone Mode consists of the sequencer and the client; no additional components are required.</span></span> <span data-ttu-id="7be9e-128">Les applications sont prêtes pour la virtualisation grâce à un processus appelé séquençage.</span><span class="sxs-lookup"><span data-stu-id="7be9e-128">Applications are prepared for virtualization using a process called sequencing.</span></span> <span data-ttu-id="7be9e-129">Pour plus d’informations, reportez-vous [à la section planification du déploiement d’App-V 5,1 et du déploiement du client](planning-for-the-app-v-51-sequencer-and-client-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="7be9e-129">For more information see, [Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md).</span></span> <span data-ttu-id="7be9e-130">Le modèle autonome est recommandé dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="7be9e-130">The stand-alone model is recommended for the following scenarios:</span></span>

    -   <span data-ttu-id="7be9e-131">Utilisateurs distants distants qui ne peuvent pas se connecter à l’infrastructure App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7be9e-131">With disconnected remote users who cannot connect to the App-V 5.1 infrastructure.</span></span>

    -   <span data-ttu-id="7be9e-132">Lorsque vous exécutez un système de gestion de logiciels, tel que Configuration Manager 2012.</span><span class="sxs-lookup"><span data-stu-id="7be9e-132">When you are running a software management system, such as Configuration Manager 2012.</span></span>

    -   <span data-ttu-id="7be9e-133">Lorsque les limitations de bande passante réseau empêchent la distribution de logiciels électroniques.</span><span class="sxs-lookup"><span data-stu-id="7be9e-133">When network bandwidth limitations inhibit electronic software distribution.</span></span>

-   <span data-ttu-id="7be9e-134">**Modèle d’infrastructure complète** -le modèle d’infrastructure complet fournit des fonctionnalités de distribution de logiciels, de gestion et de création de rapports. Il inclut également la diffusion en continu d’applications sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="7be9e-134">**Full Infrastructure Model** - The full infrastructure model provides for software distribution, management, and reporting capabilities; it also includes the streaming of applications across the network.</span></span> <span data-ttu-id="7be9e-135">Le modèle d’infrastructure complète App-V 5,1 comporte un ou plusieurs serveurs de gestion de l’application-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7be9e-135">The App-V 5.1 Full Infrastructure Model consists of one or more App-V 5.1 management servers.</span></span> <span data-ttu-id="7be9e-136">Le serveur de gestion peut être utilisé pour publier des applications sur tous les clients.</span><span class="sxs-lookup"><span data-stu-id="7be9e-136">The Management Server can be used to publish applications to all clients.</span></span> <span data-ttu-id="7be9e-137">Le processus de publication place les icônes et raccourcis des applications virtuelles sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="7be9e-137">The publishing process places the virtual application icons and shortcuts on the target computer.</span></span> <span data-ttu-id="7be9e-138">Il peut également diffuser des applications aux utilisateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="7be9e-138">It can also stream applications to local users.</span></span> <span data-ttu-id="7be9e-139">Pour plus d’informations sur l’installation du serveur de gestion, voir [planification du déploiement de l’application-V 5,1 Server](planning-for-the-app-v-51-server-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="7be9e-139">For more information about installing the management server see, [Planning for the App-V 5.1 Server Deployment](planning-for-the-app-v-51-server-deployment.md).</span></span> <span data-ttu-id="7be9e-140">Le modèle d’infrastructure complète est recommandé dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="7be9e-140">The full infrastructure model is recommended for the following scenarios:</span></span>

    <span data-ttu-id="7be9e-141">**Important**  Le modèle d’infrastructure complète App-V 5,1 nécessite Microsoft SQL Server pour stocker des données de configuration.</span><span class="sxs-lookup"><span data-stu-id="7be9e-141">**Important** The App-V 5.1 full infrastructure model requires Microsoft SQL Server to store configuration data.</span></span> <span data-ttu-id="7be9e-142">Pour plus d’informations, voir [Configurations prises en charge par App-V 5,1](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="7be9e-142">For more information see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

     

    -   <span data-ttu-id="7be9e-143">Lorsque vous souhaitez utiliser le serveur de gestion pour publier l’application sur des ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="7be9e-143">When you want to use the Management Server to publish the application to target computers.</span></span>

    -   <span data-ttu-id="7be9e-144">Pour la mise en service rapide des applications sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="7be9e-144">For rapid provisioning of applications to target computers.</span></span>

    -   <span data-ttu-id="7be9e-145">Lorsque vous souhaitez utiliser la création de rapports App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7be9e-145">When you want to use App-V 5.1 reporting.</span></span>

## <span data-ttu-id="7be9e-146">Recommandations en matière de dimensionnement de serveur bout en bout</span><span class="sxs-lookup"><span data-stu-id="7be9e-146">End-to-end Server Sizing Guidance</span></span>


<span data-ttu-id="7be9e-147">La section suivante fournit des informations sur la planification et le dimensionnement d’une application 5,1 de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="7be9e-147">The following section provides information about end-to-end App-V 5.1 sizing and planning.</span></span> <span data-ttu-id="7be9e-148">Pour plus d’informations, reportez-vous aux sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="7be9e-148">For more specific information, refer to the subsequent sections.</span></span>

<span data-ttu-id="7be9e-149">**Remarques**  Le temps de réponse en boucle sur le client correspond au temps écoulé par l’ordinateur exécutant le client App-V 5,1 pour recevoir une notification réussie du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="7be9e-149">**Note** Round trip response time on the client is the time taken by the computer running the App-V 5.1 client to receive a successful notification from the publishing server.</span></span> <span data-ttu-id="7be9e-150">Le temps de réponse en boucle sur le serveur de publication est le temps pris par l’ordinateur exécutant le serveur de publication pour recevoir une mise à jour de métadonnées de package réussie du serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="7be9e-150">Round trip response time on the publishing server is the time taken by the computer running the publishing server to receive a successful package metadata update from the management server.</span></span>

 

-   <span data-ttu-id="7be9e-151">les clients 20 000 peuvent cibler un serveur de publication unique pour obtenir les actualisations du package pendant une durée de boucle acceptable.</span><span class="sxs-lookup"><span data-stu-id="7be9e-151">20,000 clients can target a single publishing server to obtain the package refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="7be9e-152">( &lt; 3 secondes)</span><span class="sxs-lookup"><span data-stu-id="7be9e-152">(&lt;3 seconds)</span></span>

-   <span data-ttu-id="7be9e-153">Un serveur de gestion unique peut prendre en charge jusqu’à 50 serveurs de publication pour les mises à jour de package de métadonnées pendant une durée de boucle acceptable.</span><span class="sxs-lookup"><span data-stu-id="7be9e-153">A single management server can support up to 50 publishing servers for package metadata refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="7be9e-154">( &lt; 5 secondes)</span><span class="sxs-lookup"><span data-stu-id="7be9e-154">(&lt;5 seconds)</span></span>

## <a href="" id="---------app-v-5-1-management-server-capacity-planning-recommendations"></a> <span data-ttu-id="7be9e-155">Recommandations en matière de planification de la capacité du serveur de gestion d’application V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be9e-155">App-V 5.1 Management Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="7be9e-156">Les serveurs de publication App-V 5,1 nécessitent le serveur de gestion des demandes d’actualisation de package et des réponses d’actualisation de package.</span><span class="sxs-lookup"><span data-stu-id="7be9e-156">The App-V 5.1 publishing servers require the management server for package refresh requests and package refresh responses.</span></span> <span data-ttu-id="7be9e-157">Le serveur de gestion envoie alors les informations à la base de données de gestion pour récupérer des informations.</span><span class="sxs-lookup"><span data-stu-id="7be9e-157">The management server then sends the information to the management database to retrieve information.</span></span> <span data-ttu-id="7be9e-158">Pour plus d’informations sur les configurations prises en charge par App-V 5,1 Management Server, voir [Configurations prises en charge par app-v 5,1](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="7be9e-158">For more information about App-V 5.1 management server supported configurations see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<span data-ttu-id="7be9e-159">**Remarques**  Le délai d’actualisation par défaut dans le serveur de publication 5,1 App-V est de 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="7be9e-159">**Note** The default refresh time on the App-V 5.1 publishing server is ten minutes.</span></span>

 

<span data-ttu-id="7be9e-160">Lorsque plusieurs serveurs de publication simultanés contactent un serveur de gestion unique pour les actualisations des métadonnées du package, les trois facteurs suivants influencent le temps de réponse en boucle sur le serveur de publication:</span><span class="sxs-lookup"><span data-stu-id="7be9e-160">When multiple simultaneous publishing servers contact a single management server for package metadata refreshes, the following three factors influence the round trip response time on the publishing server:</span></span>

1.  <span data-ttu-id="7be9e-161">Nombre de serveurs de publication effectuant des demandes simultanées.</span><span class="sxs-lookup"><span data-stu-id="7be9e-161">Number of publishing servers making simultaneous requests.</span></span>

2.  <span data-ttu-id="7be9e-162">Nombre de groupes de connexion configurés sur le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="7be9e-162">Number of connection groups configured on the management server.</span></span>

3.  <span data-ttu-id="7be9e-163">Nombre de groupes d’accès configurés sur le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="7be9e-163">Number of access groups configured on the management server.</span></span>

<span data-ttu-id="7be9e-164">Le tableau suivant fournit des informations supplémentaires sur chaque facteur ayant un impact sur la durée de l’aller-retour.</span><span class="sxs-lookup"><span data-stu-id="7be9e-164">The following table displays more information about each factor that impacts round trip time.</span></span>

<span data-ttu-id="7be9e-165">**Remarques**  Le temps de réponse aller-retour est le temps écoulé par l’ordinateur exécutant le serveur de publication 5,1 App-V pour recevoir une mise à jour de package réussie du serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="7be9e-165">**Note** Round trip response time is the time taken by the computer running the App-V 5.1 publishing server to receive a successful package metadata update from the management server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7be9e-166">Facteurs affectant le temps de réponse en boucle</span><span class="sxs-lookup"><span data-stu-id="7be9e-166">Factors impacting round trip response time</span></span></th>
<th align="left"><span data-ttu-id="7be9e-167">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="7be9e-167">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-168">Nombre de serveurs de publication demandant des mises à jour de package simultanément.</span><span class="sxs-lookup"><span data-stu-id="7be9e-168">The number of publishing servers simultaneously requesting package metadata refreshes.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-169">Un serveur de gestion unique peut répondre à des serveurs de publication 320 demandant des métadonnées de publication simultanément.</span><span class="sxs-lookup"><span data-stu-id="7be9e-169">A single management server can respond to up to 320 publishing servers requesting publishing metadata simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="7be9e-170">Le temps de réponse aller-retour pour les serveurs de publication 320 est de 40 secondes.</span><span class="sxs-lookup"><span data-stu-id="7be9e-170">Round trip response time for 320 pub servers is ~40 seconds.</span></span></p></li>
<li><p><span data-ttu-id="7be9e-171">Pour &lt; les serveurs de publication 50 demandant des métadonnées simultanément, la durée de réponse d’un aller-retour est de &lt; 5 secondes.</span><span class="sxs-lookup"><span data-stu-id="7be9e-171">For &lt;50 publishing servers requesting metadata simultaneously, the round trip response time is &lt;5 seconds.</span></span></p></li>
<li><p><span data-ttu-id="7be9e-172">De 50 à 320, le temps de réponse augmente de façon linéaire (approximativement 2x).</span><span class="sxs-lookup"><span data-stu-id="7be9e-172">From 50 to 320 publishing servers, the response time increases linearly (approximately 2x).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7be9e-173">Nombre de groupes de connexion configurés sur le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="7be9e-173">The number of connection groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-174">Pour les groupes de connexions 100, il n’y a aucun changement notable dans le temps de réponse en boucle sur le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="7be9e-174">For up to 100 connection groups, there is no significant change in the round trip response time on the publishing server.</span></span></p></li>
<li><p><span data-ttu-id="7be9e-175">Pour les groupes de connexion 100-400, il existe une augmentation linéaire mineure du temps de réponse à un aller-retour.</span><span class="sxs-lookup"><span data-stu-id="7be9e-175">For 100 - 400 connection groups, there is a minor linear increase in the round trip response time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-176">Nombre de groupes d’accès configurés sur le serveur de gestion.</span><span class="sxs-lookup"><span data-stu-id="7be9e-176">The number of access groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-177">Dans le cas d’un maximum de groupes d’accès à 40, le temps de réponse d’un aller-retour est linéaire (approximativement 3 160) sur le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="7be9e-177">For up to 40 access groups, there is a linear (approximately 3x) increase in the round trip response time on the publishing server.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7be9e-178">Le tableau suivant présente des exemples de valeurs pour chacun des facteurs précédents.</span><span class="sxs-lookup"><span data-stu-id="7be9e-178">The following table displays sample values for each of the previous factors.</span></span> <span data-ttu-id="7be9e-179">Dans chaque variante, les packages 120 sont actualisés à partir du serveur de gestion App-V 5.1.</span><span class="sxs-lookup"><span data-stu-id="7be9e-179">In each variation, 120 packages are refreshed from the App-V 5.1management server.</span></span>

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
<th align="left"><span data-ttu-id="7be9e-180">Scénario</span><span class="sxs-lookup"><span data-stu-id="7be9e-180">Scenario</span></span></th>
<th align="left"><span data-ttu-id="7be9e-181">Variante</span><span class="sxs-lookup"><span data-stu-id="7be9e-181">Variation</span></span></th>
<th align="left"><span data-ttu-id="7be9e-182">Nombre de groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="7be9e-182">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="7be9e-183">Nombre de groupes d’accès</span><span class="sxs-lookup"><span data-stu-id="7be9e-183">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="7be9e-184">Nombre de serveurs de publication</span><span class="sxs-lookup"><span data-stu-id="7be9e-184">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="7be9e-185">Serveur de publication de type de connexion réseau/serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="7be9e-185">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="7be9e-186">Temps de réponse aller-retour sur le serveur de publication (en secondes)</span><span class="sxs-lookup"><span data-stu-id="7be9e-186">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="7be9e-187">Utilisation de l’UC sur le serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="7be9e-187">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-188">Serveurs de publication contactant simultanément le serveur de gestion pour les métadonnées de publication.</span><span class="sxs-lookup"><span data-stu-id="7be9e-188">Publishing servers simultaneously contacting management server for publishing metadata.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be9e-189">Nombre de serveurs de publication</span><span class="sxs-lookup"><span data-stu-id="7be9e-189">Number of publishing servers</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-190">0,4</span><span class="sxs-lookup"><span data-stu-id="7be9e-190">0</span></span></p></li>
<li><p><span data-ttu-id="7be9e-191">0,4</span><span class="sxs-lookup"><span data-stu-id="7be9e-191">0</span></span></p></li>
<li><p><span data-ttu-id="7be9e-192">0,4</span><span class="sxs-lookup"><span data-stu-id="7be9e-192">0</span></span></p></li>
<li><p><span data-ttu-id="7be9e-193">0,4</span><span class="sxs-lookup"><span data-stu-id="7be9e-193">0</span></span></p></li>
<li><p><span data-ttu-id="7be9e-194">0,4</span><span class="sxs-lookup"><span data-stu-id="7be9e-194">0</span></span></p></li>
<li><p><span data-ttu-id="7be9e-195">0,4</span><span class="sxs-lookup"><span data-stu-id="7be9e-195">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-196">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-196">1</span></span></p></li>
<li><p><span data-ttu-id="7be9e-197">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-197">1</span></span></p></li>
<li><p><span data-ttu-id="7be9e-198">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-198">1</span></span></p></li>
<li><p><span data-ttu-id="7be9e-199">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-199">1</span></span></p></li>
<li><p><span data-ttu-id="7be9e-200">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-200">1</span></span></p></li>
<li><p><span data-ttu-id="7be9e-201">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-201">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-202">50</span><span class="sxs-lookup"><span data-stu-id="7be9e-202">50</span></span></p></li>
<li><p><span data-ttu-id="7be9e-203">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-203">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-204">200</span><span class="sxs-lookup"><span data-stu-id="7be9e-204">200</span></span></p></li>
<li><p><span data-ttu-id="7be9e-205">300</span><span class="sxs-lookup"><span data-stu-id="7be9e-205">300</span></span></p></li>
<li><p><span data-ttu-id="7be9e-206">315</span><span class="sxs-lookup"><span data-stu-id="7be9e-206">315</span></span></p></li>
<li><p><span data-ttu-id="7be9e-207">320</span><span class="sxs-lookup"><span data-stu-id="7be9e-207">320</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-208">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-208">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-209">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-209">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-210">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-210">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-211">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-211">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-212">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-212">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-213">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-213">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-214">n°5</span><span class="sxs-lookup"><span data-stu-id="7be9e-214">5</span></span></p></li>
<li><p><span data-ttu-id="7be9e-215">0,10</span><span class="sxs-lookup"><span data-stu-id="7be9e-215">10</span></span></p></li>
<li><p><span data-ttu-id="7be9e-216">19,6</span><span class="sxs-lookup"><span data-stu-id="7be9e-216">19</span></span></p></li>
<li><p><span data-ttu-id="7be9e-217">32</span><span class="sxs-lookup"><span data-stu-id="7be9e-217">32</span></span></p></li>
<li><p><span data-ttu-id="7be9e-218">trente</span><span class="sxs-lookup"><span data-stu-id="7be9e-218">30</span></span></p></li>
<li><p><span data-ttu-id="7be9e-219">37</span><span class="sxs-lookup"><span data-stu-id="7be9e-219">37</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-220">Play</span><span class="sxs-lookup"><span data-stu-id="7be9e-220">17</span></span></p></li>
<li><p><span data-ttu-id="7be9e-221">Play</span><span class="sxs-lookup"><span data-stu-id="7be9e-221">17</span></span></p></li>
<li><p><span data-ttu-id="7be9e-222">Play</span><span class="sxs-lookup"><span data-stu-id="7be9e-222">17</span></span></p></li>
<li><p><span data-ttu-id="7be9e-223">0,15</span><span class="sxs-lookup"><span data-stu-id="7be9e-223">15</span></span></p></li>
<li><p><span data-ttu-id="7be9e-224">Play</span><span class="sxs-lookup"><span data-stu-id="7be9e-224">17</span></span></p></li>
<li><p><span data-ttu-id="7be9e-225">0,15</span><span class="sxs-lookup"><span data-stu-id="7be9e-225">15</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7be9e-226">Métadonnées de publication contenant des groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="7be9e-226">Publishing metadata contains connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be9e-227">Nombre de groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="7be9e-227">Number of connection groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-228">0,10</span><span class="sxs-lookup"><span data-stu-id="7be9e-228">10</span></span></p></li>
<li><p><span data-ttu-id="7be9e-229">50</span><span class="sxs-lookup"><span data-stu-id="7be9e-229">50</span></span></p></li>
<li><p><span data-ttu-id="7be9e-230">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-230">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-231">150</span><span class="sxs-lookup"><span data-stu-id="7be9e-231">150</span></span></p></li>
<li><p><span data-ttu-id="7be9e-232">300</span><span class="sxs-lookup"><span data-stu-id="7be9e-232">300</span></span></p></li>
<li><p><span data-ttu-id="7be9e-233">400</span><span class="sxs-lookup"><span data-stu-id="7be9e-233">400</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-234">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-234">1</span></span></p></li>
<li><p><span data-ttu-id="7be9e-235">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-235">1</span></span></p></li>
<li><p><span data-ttu-id="7be9e-236">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-236">1</span></span></p></li>
<li><p><span data-ttu-id="7be9e-237">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-237">1</span></span></p></li>
<li><p><span data-ttu-id="7be9e-238">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-238">1</span></span></p></li>
<li><p><span data-ttu-id="7be9e-239">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-239">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-240">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-240">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-241">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-241">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-242">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-242">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-243">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-243">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-244">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-244">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-245">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-245">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-246">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-246">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-247">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-247">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-248">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-248">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-249">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-249">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-250">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-250">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-251">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-251">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-252">0,10</span><span class="sxs-lookup"><span data-stu-id="7be9e-252">10</span></span></p></li>
<li><p><span data-ttu-id="7be9e-253">27,9</span><span class="sxs-lookup"><span data-stu-id="7be9e-253">11</span></span></p></li>
<li><p><span data-ttu-id="7be9e-254">27,9</span><span class="sxs-lookup"><span data-stu-id="7be9e-254">11</span></span></p></li>
<li><p><span data-ttu-id="7be9e-255">Seiz</span><span class="sxs-lookup"><span data-stu-id="7be9e-255">16</span></span></p></li>
<li><p><span data-ttu-id="7be9e-256">22</span><span class="sxs-lookup"><span data-stu-id="7be9e-256">22</span></span></p></li>
<li><p><span data-ttu-id="7be9e-257">1,25</span><span class="sxs-lookup"><span data-stu-id="7be9e-257">25</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-258">Play</span><span class="sxs-lookup"><span data-stu-id="7be9e-258">17</span></span></p></li>
<li><p><span data-ttu-id="7be9e-259">19,6</span><span class="sxs-lookup"><span data-stu-id="7be9e-259">19</span></span></p></li>
<li><p><span data-ttu-id="7be9e-260">22</span><span class="sxs-lookup"><span data-stu-id="7be9e-260">22</span></span></p></li>
<li><p><span data-ttu-id="7be9e-261">19,6</span><span class="sxs-lookup"><span data-stu-id="7be9e-261">19</span></span></p></li>
<li><p><span data-ttu-id="7be9e-262">CX3-20</span><span class="sxs-lookup"><span data-stu-id="7be9e-262">20</span></span></p></li>
<li><p><span data-ttu-id="7be9e-263">CX3-20</span><span class="sxs-lookup"><span data-stu-id="7be9e-263">20</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-264">Métadonnées de publication contenant des groupes d’accès</span><span class="sxs-lookup"><span data-stu-id="7be9e-264">Publishing metadata contains access groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be9e-265">Nombre de groupes d’accès</span><span class="sxs-lookup"><span data-stu-id="7be9e-265">Number of access groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-266">0,4</span><span class="sxs-lookup"><span data-stu-id="7be9e-266">0</span></span></p></li>
<li><p><span data-ttu-id="7be9e-267">0,4</span><span class="sxs-lookup"><span data-stu-id="7be9e-267">0</span></span></p></li>
<li><p><span data-ttu-id="7be9e-268">0,4</span><span class="sxs-lookup"><span data-stu-id="7be9e-268">0</span></span></p></li>
<li><p><span data-ttu-id="7be9e-269">0,4</span><span class="sxs-lookup"><span data-stu-id="7be9e-269">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-270">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-270">1</span></span></p></li>
<li><p><span data-ttu-id="7be9e-271">0,10</span><span class="sxs-lookup"><span data-stu-id="7be9e-271">10</span></span></p></li>
<li><p><span data-ttu-id="7be9e-272">CX3-20</span><span class="sxs-lookup"><span data-stu-id="7be9e-272">20</span></span></p></li>
<li><p><span data-ttu-id="7be9e-273">40</span><span class="sxs-lookup"><span data-stu-id="7be9e-273">40</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-274">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-274">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-275">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-275">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-276">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-276">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-277">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-277">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-278">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-278">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-279">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-279">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-280">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-280">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-281">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-281">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-282">0,10</span><span class="sxs-lookup"><span data-stu-id="7be9e-282">10</span></span></p></li>
<li><p><span data-ttu-id="7be9e-283">43</span><span class="sxs-lookup"><span data-stu-id="7be9e-283">43</span></span></p></li>
<li><p><span data-ttu-id="7be9e-284">153</span><span class="sxs-lookup"><span data-stu-id="7be9e-284">153</span></span></p></li>
<li><p><span data-ttu-id="7be9e-285">535</span><span class="sxs-lookup"><span data-stu-id="7be9e-285">535</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-286">Play</span><span class="sxs-lookup"><span data-stu-id="7be9e-286">17</span></span></p></li>
<li><p><span data-ttu-id="7be9e-287">26/08/03</span><span class="sxs-lookup"><span data-stu-id="7be9e-287">26</span></span></p></li>
<li><p><span data-ttu-id="7be9e-288">24</span><span class="sxs-lookup"><span data-stu-id="7be9e-288">24</span></span></p></li>
<li><p><span data-ttu-id="7be9e-289">24</span><span class="sxs-lookup"><span data-stu-id="7be9e-289">24</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7be9e-290">L’utilisation de l’UC de l’ordinateur exécutant le serveur de gestion est d’environ 25%, sans tenir compte du nombre de serveurs de publication ciblant celle-ci.</span><span class="sxs-lookup"><span data-stu-id="7be9e-290">The CPU utilization of the computer running the management server is around 25% irrespective of the number of publishing servers targeting it.</span></span> <span data-ttu-id="7be9e-291">Les transactions/s de base de données Microsoft SQL Server, les requêtes par lot/s et les connexions utilisateur sont identiques quel que soit le nombre de serveurs de publication.</span><span class="sxs-lookup"><span data-stu-id="7be9e-291">The Microsoft SQL Server database transactions/sec, batch requests/sec and user connections are identical irrespective of the number of publishing servers.</span></span> <span data-ttu-id="7be9e-292">Par exemple: transactions/s est ~ 30, les demandes de lot ~ 200 et l’utilisateur connecte ~ 6.</span><span class="sxs-lookup"><span data-stu-id="7be9e-292">For example: Transactions/sec is ~30, batch requests ~200, and user connects ~6.</span></span>

<span data-ttu-id="7be9e-293">Dans le cadre d’un déploiement distribué sur le graphique, lorsque le serveur de gestion & serveurs de publication utilise un réseau de liaison lente entre eux, le temps de réponse en boucle sur les serveurs de publication est limité à un délai de &lt; 5 secondes, même pour les demandes simultanées 100 sur un serveur de gestion unique.</span><span class="sxs-lookup"><span data-stu-id="7be9e-293">Using a geographically distributed deployment, where the management server & publishing servers utilize a slow link network between them, the round trip response time on the publishing servers is within acceptable time limits (&lt;5 seconds), even for 100 simultaneous requests on a single management server.</span></span>

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
<th align="left"><span data-ttu-id="7be9e-294">Scénario</span><span class="sxs-lookup"><span data-stu-id="7be9e-294">Scenario</span></span></th>
<th align="left"><span data-ttu-id="7be9e-295">Variante</span><span class="sxs-lookup"><span data-stu-id="7be9e-295">Variation</span></span></th>
<th align="left"><span data-ttu-id="7be9e-296">Nombre de groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="7be9e-296">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="7be9e-297">Nombre de groupes d’accès</span><span class="sxs-lookup"><span data-stu-id="7be9e-297">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="7be9e-298">Nombre de serveurs de publication</span><span class="sxs-lookup"><span data-stu-id="7be9e-298">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="7be9e-299">Serveur de publication de type de connexion réseau/serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="7be9e-299">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="7be9e-300">Temps de réponse aller-retour sur le serveur de publication (en secondes)</span><span class="sxs-lookup"><span data-stu-id="7be9e-300">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="7be9e-301">Utilisation de l’UC sur le serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="7be9e-301">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-302">Connexion réseau entre le serveur de publication et le serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="7be9e-302">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be9e-303">Réseau de liaison lente 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="7be9e-303">1.5 Mbps Slow link Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-304">0,4</span><span class="sxs-lookup"><span data-stu-id="7be9e-304">0</span></span></p></li>
<li><p><span data-ttu-id="7be9e-305">0,4</span><span class="sxs-lookup"><span data-stu-id="7be9e-305">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-306">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-306">1</span></span></p></li>
<li><p><span data-ttu-id="7be9e-307">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-307">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-308">50</span><span class="sxs-lookup"><span data-stu-id="7be9e-308">50</span></span></p></li>
<li><p><span data-ttu-id="7be9e-309">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-309">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-310">Câble ADSL de 1,5 MB/s</span><span class="sxs-lookup"><span data-stu-id="7be9e-310">1.5Mbps Cable DSL</span></span></p></li>
<li><p><span data-ttu-id="7be9e-311">Câble ADSL de 1,5 MB/s</span><span class="sxs-lookup"><span data-stu-id="7be9e-311">1.5Mbps Cable DSL</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-312">n°4</span><span class="sxs-lookup"><span data-stu-id="7be9e-312">4</span></span></p></li>
<li><p><span data-ttu-id="7be9e-313">n°5</span><span class="sxs-lookup"><span data-stu-id="7be9e-313">5</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-314">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-314">1</span></span></p></li>
<li><p><span data-ttu-id="7be9e-315">deuxième</span><span class="sxs-lookup"><span data-stu-id="7be9e-315">2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7be9e-316">Connexion réseau entre le serveur de publication et le serveur de gestion</span><span class="sxs-lookup"><span data-stu-id="7be9e-316">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be9e-317">Réseau LAN/WIFI</span><span class="sxs-lookup"><span data-stu-id="7be9e-317">LAN / WIFI Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-318">0,4</span><span class="sxs-lookup"><span data-stu-id="7be9e-318">0</span></span></p></li>
<li><p><span data-ttu-id="7be9e-319">0,4</span><span class="sxs-lookup"><span data-stu-id="7be9e-319">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-320">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-320">1</span></span></p></li>
<li><p><span data-ttu-id="7be9e-321">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-321">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-322">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-322">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-323">200</span><span class="sxs-lookup"><span data-stu-id="7be9e-323">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-324">Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="7be9e-324">Wifi</span></span></p></li>
<li><p><span data-ttu-id="7be9e-325">Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="7be9e-325">Wifi</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-326">27,9</span><span class="sxs-lookup"><span data-stu-id="7be9e-326">11</span></span></p></li>
<li><p><span data-ttu-id="7be9e-327">CX3-20</span><span class="sxs-lookup"><span data-stu-id="7be9e-327">20</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-328">0,15</span><span class="sxs-lookup"><span data-stu-id="7be9e-328">15</span></span></p></li>
<li><p><span data-ttu-id="7be9e-329">Play</span><span class="sxs-lookup"><span data-stu-id="7be9e-329">17</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7be9e-330">Le serveur de gestion et les serveurs de publication sont connectés à un réseau de liaison lente ou d’un réseau haut débit, le serveur de gestion peut gérer approximativement 15 000 demandes d’actualisation de package dans 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="7be9e-330">Whether the management server and publishing servers are connected over a slow link network, or a high speed network, the management server can handle approximately 15,000 package refresh requests in 30 minutes.</span></span>

## <a href="" id="---------app-v-5-1-reporting-server-capacity-planning-recommendations"></a> <span data-ttu-id="7be9e-331">Recommandations pour la planification de la capacité du serveur App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be9e-331">App-V 5.1 Reporting Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="7be9e-332">Les clients App-V 5,1 envoient des données de création de rapports au serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="7be9e-332">App-V 5.1 clients send reporting data to the reporting server.</span></span> <span data-ttu-id="7be9e-333">Le serveur de création de rapports enregistre ensuite les informations dans la base de données Microsoft SQL Server et renvoie une notification réussie à l’ordinateur exécutant le client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7be9e-333">The reporting server then records the information in the Microsoft SQL Server database and returns a successful notification back to the computer running App-V 5.1 client.</span></span> <span data-ttu-id="7be9e-334">Pour plus d’informations sur les configurations prises en charge par App-V 5,1 Report Server, voir [Configurations prises en charge par app-v 5,1](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="7be9e-334">For more information about App-V 5.1 Reporting Server supported configurations see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<span data-ttu-id="7be9e-335">**Remarques**  Le temps de réponse aller-retour est le temps écoulé par l’ordinateur exécutant le client App-V 5,1 pour envoyer les informations de rapport au serveur de création de rapports et recevoir une notification réussie du serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="7be9e-335">**Note** Round trip response time is the time taken by the computer running the App-V 5.1 client to send the reporting information to the reporting server and receive a successful notification from the reporting server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7be9e-336">Scénario</span><span class="sxs-lookup"><span data-stu-id="7be9e-336">Scenario</span></span></th>
<th align="left"><span data-ttu-id="7be9e-337">Résumé</span><span class="sxs-lookup"><span data-stu-id="7be9e-337">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-338">Plusieurs clients App-V 5,1 envoient simultanément des informations de rapport au serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="7be9e-338">Multiple App-V 5.1 clients send reporting information to the reporting server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-339">Le temps de réponse en boucle du serveur de rapports est de 2,6 secondes pour les clients 500.</span><span class="sxs-lookup"><span data-stu-id="7be9e-339">Round trip response time from the reporting server is 2.6 seconds for 500 clients.</span></span></p></li>
<li><p><span data-ttu-id="7be9e-340">Le temps de réponse en boucle du serveur de rapports est de 5,65 secondes pour les clients 1000.</span><span class="sxs-lookup"><span data-stu-id="7be9e-340">Round trip response time from the reporting server is 5.65 seconds for 1000 clients.</span></span></p></li>
<li><p><span data-ttu-id="7be9e-341">Le temps de réponse en boucle augmente de façon linéaire en fonction du nombre de clients.</span><span class="sxs-lookup"><span data-stu-id="7be9e-341">Round trip response time increases linearly depending on number of clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7be9e-342">Demandes par seconde traitées par le serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="7be9e-342">Requests per second processed by the reporting server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-343">Un serveur de création de rapports unique et une seule base de données peuvent traiter un maximum de demandes 139 par seconde.</span><span class="sxs-lookup"><span data-stu-id="7be9e-343">A single reporting server and a single database, can process a maximum of 139 requests per second.</span></span> <span data-ttu-id="7be9e-344">La moyenne est 121 demandes/secondes.</span><span class="sxs-lookup"><span data-stu-id="7be9e-344">The average is 121 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="7be9e-345">En utilisant deux serveurs de création de rapports sur la même base de données Microsoft SQL Server, la moyenne des demandes/secondes est similaire à un serveur de rapports unique = ~ 127, avec une limite de 278 demandes/seconde.</span><span class="sxs-lookup"><span data-stu-id="7be9e-345">Using two reporting servers reporting to the same Microsoft SQL Server database, the average requests/second is similar to a single reporting server = ~127, with a max of 278 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="7be9e-346">Un serveur de rapports unique peut traiter les connexions 500 concurrentes/actives.</span><span class="sxs-lookup"><span data-stu-id="7be9e-346">A single reporting server can process 500 concurrent/active connections.</span></span></p></li>
<li><p><span data-ttu-id="7be9e-347">Un serveur de rapports unique peut traiter une connexion simultanée 1500 maximum.</span><span class="sxs-lookup"><span data-stu-id="7be9e-347">A single reporting server can process a maximum 1500 concurrent connections.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-348">Base de données de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="7be9e-348">Reporting Database.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-349">Le verrouillage du contenu sur l’ordinateur exécutant Microsoft SQL Server est le facteur de limitation pour les demandes/secondes.</span><span class="sxs-lookup"><span data-stu-id="7be9e-349">Lock contention on the computer running Microsoft SQL Server is the limiting factor for requests/second.</span></span></p></li>
<li><p><span data-ttu-id="7be9e-350">Le débit et le temps de réponse sont indépendants de la taille de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7be9e-350">Throughput and response time are independent of database size.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7be9e-351">**Calcul du retard aléatoire**:</span><span class="sxs-lookup"><span data-stu-id="7be9e-351">**Calculating random delay**:</span></span>

<span data-ttu-id="7be9e-352">Le délai aléatoire spécifie le délai maximal (en minutes) pendant lequel les données doivent être envoyées au serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="7be9e-352">The random delay specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="7be9e-353">Lorsque la tâche planifiée est lancée, le client génère un délai aléatoire compris entre **0** et **ReportingRandomDelay** et attend la durée spécifiée avant d’envoyer des données.</span><span class="sxs-lookup"><span data-stu-id="7be9e-353">When the scheduled task is started, the client generates a random delay between **0** and **ReportingRandomDelay** and will wait the specified duration before sending data.</span></span>

<span data-ttu-id="7be9e-354">Retard aléatoire = 4 \ \* nombre de clients/demandes de moyenne par seconde.</span><span class="sxs-lookup"><span data-stu-id="7be9e-354">Random delay = 4 \* number of clients / average requests per second.</span></span>

<span data-ttu-id="7be9e-355">Exemple: pour les clients 500, avec des demandes 120 par seconde, le délai aléatoire est de 4 \ \* 500/120 = ~ 17 minutes.</span><span class="sxs-lookup"><span data-stu-id="7be9e-355">Example: For 500 clients, with 120 requests per second, the Random delay is, 4 \* 500 / 120 = ~17 minutes.</span></span>

## <a href="" id="---------app-v-5-1-publishing-server-capacity-planning-recommendations"></a> <span data-ttu-id="7be9e-356">Recommandations en matière de planification de la capacité du serveur Publisher V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be9e-356">App-V 5.1 Publishing Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="7be9e-357">Les ordinateurs exécutant le client App-V 5,1 se connectent au serveur de publication App-V 5,1 pour envoyer une demande d’actualisation de publication et recevoir une réponse.</span><span class="sxs-lookup"><span data-stu-id="7be9e-357">Computers running the App-V 5.1 client connect to the App-V 5.1 publishing server to send a publishing refresh request and to receive a response.</span></span> <span data-ttu-id="7be9e-358">La durée de réponse en boucle est mesurée sur l’ordinateur exécutant le client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7be9e-358">Round trip response time is measured on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="7be9e-359">La durée du processeur est mesurée sur le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="7be9e-359">Processor time is measured on the publishing server.</span></span> <span data-ttu-id="7be9e-360">Pour plus d’informations sur les configurations prises en charge par le serveur de publication App-V 5,1, consultez la rubrique [configurations App-v 5,1 prises en charge](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="7be9e-360">For more information about App-V 5.1 Publishing Server supported configurations see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<span data-ttu-id="7be9e-361">**Important**  La liste suivante indique les principaux facteurs à prendre en compte lors de la configuration du serveur de publication 5,1 App-V.</span><span class="sxs-lookup"><span data-stu-id="7be9e-361">**Important** The following list displays the main factors to consider when setting up the App-V 5.1 publishing server:</span></span>

-   <span data-ttu-id="7be9e-362">Nombre de clients qui se connectent simultanément à un serveur de publication unique.</span><span class="sxs-lookup"><span data-stu-id="7be9e-362">The number of clients connecting simultaneously to a single publishing server.</span></span>

-   <span data-ttu-id="7be9e-363">Nombre de packages de chaque actualisation.</span><span class="sxs-lookup"><span data-stu-id="7be9e-363">The number of packages in each refresh.</span></span>

-   <span data-ttu-id="7be9e-364">La bande passante réseau disponible dans votre environnement entre le client et le serveur de publication 5,1 de l’application.</span><span class="sxs-lookup"><span data-stu-id="7be9e-364">The available network bandwidth in your environment between the client and the App-V 5.1 publishing server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7be9e-365">Scénario</span><span class="sxs-lookup"><span data-stu-id="7be9e-365">Scenario</span></span></th>
<th align="left"><span data-ttu-id="7be9e-366">Résumé</span><span class="sxs-lookup"><span data-stu-id="7be9e-366">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-367">Plusieurs clients App-V 5,1 se connectent à un serveur de publication unique simultanément.</span><span class="sxs-lookup"><span data-stu-id="7be9e-367">Multiple App-V 5.1 clients connect to a single publishing server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-368">Un serveur de publication exécutant des processeurs double cœur peut répondre à la plupart des clients 5000 demandant une actualisation simultanée.</span><span class="sxs-lookup"><span data-stu-id="7be9e-368">A publishing server running dual core processors can respond to at most 5000 clients requesting a refresh simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="7be9e-369">Pour les clients 5000-10000, le serveur de publication nécessite un minimum de quatre cœurs.</span><span class="sxs-lookup"><span data-stu-id="7be9e-369">For 5000-10000 clients, the publishing server requires a minimum quad core.</span></span></p></li>
<li><p><span data-ttu-id="7be9e-370">Pour les clients 10000-20000, le serveur de publication doit disposer de deux cœurs pour des temps de réponse plus efficaces.</span><span class="sxs-lookup"><span data-stu-id="7be9e-370">For 10000-20000 clients, the publishing server should have dual quad cores for more efficient response times.</span></span></p></li>
<li><p><span data-ttu-id="7be9e-371">Un serveur de publication avec un noyau à quatre cœurs peut actualiser jusqu’à 10000 packages dans un délai de 3 secondes.</span><span class="sxs-lookup"><span data-stu-id="7be9e-371">A publishing server with a quad core can refresh up to 10000 packages within 3 seconds.</span></span> <span data-ttu-id="7be9e-372">(Prise en charge des clients simultanés 10000)</span><span class="sxs-lookup"><span data-stu-id="7be9e-372">(Supporting 10000 simultaneous clients)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7be9e-373">Nombre de packages de chaque actualisation.</span><span class="sxs-lookup"><span data-stu-id="7be9e-373">Number of packages in each refresh.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-374">L’augmentation du nombre de packages augmente le délai de réponse de ~ 40% (jusqu’à 1000 Packages).</span><span class="sxs-lookup"><span data-stu-id="7be9e-374">Increasing number of packages will increase response time by ~40% (up to 1000 packages).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-375">Réseau entre le client App-V 5,1 et le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="7be9e-375">Network between the App-V 5.1 client and the publishing server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-376">Sur une connexion réseau lente (bande passante 1,5 Mbps), il existe un délai de réponse d' 97% par rapport au réseau local (jusqu’à 1000 utilisateurs).</span><span class="sxs-lookup"><span data-stu-id="7be9e-376">Across a slow network (1.5 Mbps bandwidth), there is a 97% increase in response time compared to LAN (up to 1000 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7be9e-377">**Remarques**  Le taux d’utilisation de l’UC du serveur de publication est toujours élevé pendant l’intervalle de temps pendant lequel il doit traiter les demandes simultanées ( &gt; 90% dans la plupart des cas).</span><span class="sxs-lookup"><span data-stu-id="7be9e-377">**Note** The publishing server CPU usage is always high during the time interval when it has to process simultaneous requests (&gt;90% in most cases).</span></span> <span data-ttu-id="7be9e-378">Le serveur de publication peut gérer les demandes du client ~ 1500 en 1 seconde.</span><span class="sxs-lookup"><span data-stu-id="7be9e-378">The publishing server can handle ~1500 client requests in 1 second.</span></span>

 

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
<th align="left"><span data-ttu-id="7be9e-379">Scénario</span><span class="sxs-lookup"><span data-stu-id="7be9e-379">Scenario</span></span></th>
<th align="left"><span data-ttu-id="7be9e-380">Variante</span><span class="sxs-lookup"><span data-stu-id="7be9e-380">Variation</span></span></th>
<th align="left"><span data-ttu-id="7be9e-381">Nombre de clients App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be9e-381">Number of App-V 5.1 clients</span></span></th>
<th align="left"><span data-ttu-id="7be9e-382">Nombre de packages</span><span class="sxs-lookup"><span data-stu-id="7be9e-382">Number of packages</span></span></th>
<th align="left"><span data-ttu-id="7be9e-383">Configuration du processeur sur le serveur de publication</span><span class="sxs-lookup"><span data-stu-id="7be9e-383">Processor configuration on the publishing server</span></span></th>
<th align="left"><span data-ttu-id="7be9e-384">Type de connexion réseau-client de publication de type serveur/App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be9e-384">Network connection type publishing server / App-V 5.1 client</span></span></th>
<th align="left"><span data-ttu-id="7be9e-385">Durée de l’aller-retour sur le client App-V 5,1 (en secondes)</span><span class="sxs-lookup"><span data-stu-id="7be9e-385">Round trip time on the App-V 5.1 client (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="7be9e-386">Utilisation de l’UC sur le serveur de publication (en%)</span><span class="sxs-lookup"><span data-stu-id="7be9e-386">CPU utilization on publishing server (in %)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-387">Le client App-V 5,1 envoie une demande d’actualisation &amp; de publication reçoit une réponse, chaque requête contenant des packages 120</span><span class="sxs-lookup"><span data-stu-id="7be9e-387">App-V 5.1 client sends publishing refresh request &amp; receives response, each request containing 120 packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be9e-388">Nombre de clients</span><span class="sxs-lookup"><span data-stu-id="7be9e-388">Number of clients</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-389">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-389">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-390">1000</span><span class="sxs-lookup"><span data-stu-id="7be9e-390">1000</span></span></p></li>
<li><p><span data-ttu-id="7be9e-391">5000</span><span class="sxs-lookup"><span data-stu-id="7be9e-391">5000</span></span></p></li>
<li><p><span data-ttu-id="7be9e-392">10000</span><span class="sxs-lookup"><span data-stu-id="7be9e-392">10000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-393">120</span><span class="sxs-lookup"><span data-stu-id="7be9e-393">120</span></span></p></li>
<li><p><span data-ttu-id="7be9e-394">120</span><span class="sxs-lookup"><span data-stu-id="7be9e-394">120</span></span></p></li>
<li><p><span data-ttu-id="7be9e-395">120</span><span class="sxs-lookup"><span data-stu-id="7be9e-395">120</span></span></p></li>
<li><p><span data-ttu-id="7be9e-396">120</span><span class="sxs-lookup"><span data-stu-id="7be9e-396">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-397">Double cœur</span><span class="sxs-lookup"><span data-stu-id="7be9e-397">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="7be9e-398">Double cœur</span><span class="sxs-lookup"><span data-stu-id="7be9e-398">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="7be9e-399">Quadruple cœur</span><span class="sxs-lookup"><span data-stu-id="7be9e-399">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="7be9e-400">Quadruple cœur</span><span class="sxs-lookup"><span data-stu-id="7be9e-400">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-401">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-401">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-402">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-402">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-403">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-403">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-404">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-404">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-405">1</span><span class="sxs-lookup"><span data-stu-id="7be9e-405">1</span></span></p></li>
<li><p><span data-ttu-id="7be9e-406">deuxième</span><span class="sxs-lookup"><span data-stu-id="7be9e-406">2</span></span></p></li>
<li><p><span data-ttu-id="7be9e-407">deuxième</span><span class="sxs-lookup"><span data-stu-id="7be9e-407">2</span></span></p></li>
<li><p><span data-ttu-id="7be9e-408">3D</span><span class="sxs-lookup"><span data-stu-id="7be9e-408">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-409">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-409">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-410">99</span><span class="sxs-lookup"><span data-stu-id="7be9e-410">99</span></span></p></li>
<li><p><span data-ttu-id="7be9e-411">89</span><span class="sxs-lookup"><span data-stu-id="7be9e-411">89</span></span></p></li>
<li><p><span data-ttu-id="7be9e-412">77</span><span class="sxs-lookup"><span data-stu-id="7be9e-412">77</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7be9e-413">Plusieurs packages pour chaque actualisation</span><span class="sxs-lookup"><span data-stu-id="7be9e-413">Multiple packages in each refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be9e-414">Nombre de packages</span><span class="sxs-lookup"><span data-stu-id="7be9e-414">Number of packages</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-415">1000</span><span class="sxs-lookup"><span data-stu-id="7be9e-415">1000</span></span></p></li>
<li><p><span data-ttu-id="7be9e-416">1000</span><span class="sxs-lookup"><span data-stu-id="7be9e-416">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-417">500</span><span class="sxs-lookup"><span data-stu-id="7be9e-417">500</span></span></p></li>
<li><p><span data-ttu-id="7be9e-418">1000</span><span class="sxs-lookup"><span data-stu-id="7be9e-418">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-419">Quadruple cœur</span><span class="sxs-lookup"><span data-stu-id="7be9e-419">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="7be9e-420">Quadruple cœur</span><span class="sxs-lookup"><span data-stu-id="7be9e-420">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-421">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-421">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-422">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-422">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-423">deuxième</span><span class="sxs-lookup"><span data-stu-id="7be9e-423">2</span></span></p></li>
<li><p><span data-ttu-id="7be9e-424">3D</span><span class="sxs-lookup"><span data-stu-id="7be9e-424">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-425">92</span><span class="sxs-lookup"><span data-stu-id="7be9e-425">92</span></span></p></li>
<li><p><span data-ttu-id="7be9e-426">91</span><span class="sxs-lookup"><span data-stu-id="7be9e-426">91</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-427">Réseau entre le client et le serveur de publication</span><span class="sxs-lookup"><span data-stu-id="7be9e-427">Network between client and publishing server</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be9e-428">réseau de liaison lente 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="7be9e-428">1.5 Mbps Slow link network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-429">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-429">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-430">500</span><span class="sxs-lookup"><span data-stu-id="7be9e-430">500</span></span></p></li>
<li><p><span data-ttu-id="7be9e-431">1000</span><span class="sxs-lookup"><span data-stu-id="7be9e-431">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-432">120</span><span class="sxs-lookup"><span data-stu-id="7be9e-432">120</span></span></p></li>
<li><p><span data-ttu-id="7be9e-433">120</span><span class="sxs-lookup"><span data-stu-id="7be9e-433">120</span></span></p></li>
<li><p><span data-ttu-id="7be9e-434">120</span><span class="sxs-lookup"><span data-stu-id="7be9e-434">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-435">Quadruple cœur</span><span class="sxs-lookup"><span data-stu-id="7be9e-435">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="7be9e-436">Quadruple cœur</span><span class="sxs-lookup"><span data-stu-id="7be9e-436">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="7be9e-437">Quadruple cœur</span><span class="sxs-lookup"><span data-stu-id="7be9e-437">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-438">Réseau intra-continent 1,5 MB/s</span><span class="sxs-lookup"><span data-stu-id="7be9e-438">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-439">3D</span><span class="sxs-lookup"><span data-stu-id="7be9e-439">3</span></span></p></li>
<li><p><span data-ttu-id="7be9e-440">10 (avec le taux d’échec de 0,2%)</span><span class="sxs-lookup"><span data-stu-id="7be9e-440">10 (with 0.2% failure rate)</span></span></p></li>
<li><p><span data-ttu-id="7be9e-441">17 (avec un taux d’échec de 1%)</span><span class="sxs-lookup"><span data-stu-id="7be9e-441">17 (with 1% failure rate)</span></span></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-1-streaming-capacity-planning-recommendations"></a> <span data-ttu-id="7be9e-442">Recommandations en matière de planification de capacité de flux d’application V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be9e-442">App-V 5.1 Streaming Capacity Planning Recommendations</span></span>


<span data-ttu-id="7be9e-443">Les ordinateurs exécutant le client App-V 5,1 diffusent le package de l’application virtuelle à partir du serveur de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="7be9e-443">Computers running the App-V 5.1 client stream the virtual application package from the streaming server.</span></span> <span data-ttu-id="7be9e-444">La durée de réponse en boucle est mesurée sur l’ordinateur exécutant le client App-V 5,1 et est le temps nécessaire pour diffuser l’intégralité du package.</span><span class="sxs-lookup"><span data-stu-id="7be9e-444">Round trip response time is measured on the computer running the App-V 5.1 client, and is the time taken to stream the entire package.</span></span>

<span data-ttu-id="7be9e-445">**Important**  La liste suivante indique les principaux facteurs à prendre en compte lors de la configuration du serveur de streaming App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="7be9e-445">**Important** The following list identifies the main factors to consider when setting up the App-V 5.1 streaming server:</span></span>

-   <span data-ttu-id="7be9e-446">Le nombre de clients en diffusant des packages d’application simultanément depuis un serveur de diffusion unique.</span><span class="sxs-lookup"><span data-stu-id="7be9e-446">The number of clients streaming application packages simultaneously from a single streaming server.</span></span>

-   <span data-ttu-id="7be9e-447">Taille du package en cours de diffusion.</span><span class="sxs-lookup"><span data-stu-id="7be9e-447">The size of the package being streamed.</span></span>

-   <span data-ttu-id="7be9e-448">La bande passante réseau disponible dans votre environnement entre le client et le serveur de diffusion.</span><span class="sxs-lookup"><span data-stu-id="7be9e-448">The available network bandwidth in your environment between the client and the streaming server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7be9e-449">Scénario</span><span class="sxs-lookup"><span data-stu-id="7be9e-449">Scenario</span></span></th>
<th align="left"><span data-ttu-id="7be9e-450">Résumé</span><span class="sxs-lookup"><span data-stu-id="7be9e-450">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-451">Plusieurs clients App-V 5,1 diffusent simultanément des applications à partir d’un serveur en flux unique.</span><span class="sxs-lookup"><span data-stu-id="7be9e-451">Multiple App-V 5.1 clients stream applications from a single streaming server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-452">Si le nombre de clients diffusés en continu à partir du même serveur augmente, il existe une relation linéaire avec le temps de téléchargement/de diffusion du package.</span><span class="sxs-lookup"><span data-stu-id="7be9e-452">If the number of clients simultaneously streaming from the same server increases, there is a linear relationship with the package download/streaming time.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7be9e-453">Taille du package en cours de diffusion.</span><span class="sxs-lookup"><span data-stu-id="7be9e-453">Size of the package being streamed.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-454">La taille du package a un impact significatif sur le temps de diffusion/téléchargement uniquement pour les packages plus grands dont la taille est de ~ 1 Go.</span><span class="sxs-lookup"><span data-stu-id="7be9e-454">The package size has a significant impact on the streaming/download time only for larger packages with a size ~ 1GB.</span></span> <span data-ttu-id="7be9e-455">Pour les tailles de packages comprises entre 3 Mo et 100 Mo, la durée de diffusion varie de 20 secondes à 100 secondes, avec les clients simultanés 100.</span><span class="sxs-lookup"><span data-stu-id="7be9e-455">For package sizes ranging from 3 MB to 100 MB, the streaming time ranges from 20 seconds to 100 seconds, with 100 simultaneous clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-456">Réseau entre le client App-V 5,1 et le serveur de streaming.</span><span class="sxs-lookup"><span data-stu-id="7be9e-456">Network between the App-V 5.1 client and the streaming server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-457">Sur une connexion réseau lente (bande passante 1,5 Mbps), il existe un délai de réponse d' 70-80% par rapport au réseau local (jusqu’à 100 utilisateurs).</span><span class="sxs-lookup"><span data-stu-id="7be9e-457">Across a slow network (1.5 Mbps bandwidth), there is a 70-80% increase in response time compared to LAN (up to 100 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7be9e-458">Le tableau suivant présente des exemples de valeurs pour chacun des facteurs de la liste précédente:</span><span class="sxs-lookup"><span data-stu-id="7be9e-458">The following table displays sample values for each of the factors in the previous list:</span></span>

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
<th align="left"><span data-ttu-id="7be9e-459">Scénario</span><span class="sxs-lookup"><span data-stu-id="7be9e-459">Scenario</span></span></th>
<th align="left"><span data-ttu-id="7be9e-460">Variante</span><span class="sxs-lookup"><span data-stu-id="7be9e-460">Variation</span></span></th>
<th align="left"><span data-ttu-id="7be9e-461">Nombre de clients App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be9e-461">Number of App-V 5.1 clients</span></span></th>
<th align="left"><span data-ttu-id="7be9e-462">Taille de chaque package</span><span class="sxs-lookup"><span data-stu-id="7be9e-462">Size of each package</span></span></th>
<th align="left"><span data-ttu-id="7be9e-463">Serveur de type connexion réseau/client App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be9e-463">Network connection type streaming server / App-V 5.1 client</span></span></th>
<th align="left"><span data-ttu-id="7be9e-464">Durée de l’aller-retour sur le client App-V 5,1 (en secondes)</span><span class="sxs-lookup"><span data-stu-id="7be9e-464">Round trip time on the App-V 5.1 client (in seconds)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-465">Plusieurs clients App-V 5,1 diffusent des packages d’application virtuels à partir d’un serveur en flux continu.</span><span class="sxs-lookup"><span data-stu-id="7be9e-465">Multiple App-V 5.1 clients streaming virtual application packages from a streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be9e-466">Nombre de clients.</span><span class="sxs-lookup"><span data-stu-id="7be9e-466">Number of clients.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-467">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-467">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-468">200</span><span class="sxs-lookup"><span data-stu-id="7be9e-468">200</span></span></p></li>
<li><p><span data-ttu-id="7be9e-469">1000</span><span class="sxs-lookup"><span data-stu-id="7be9e-469">1000</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="7be9e-470">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-470">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-471">200</span><span class="sxs-lookup"><span data-stu-id="7be9e-471">200</span></span></p></li>
<li><p><span data-ttu-id="7be9e-472">1000</span><span class="sxs-lookup"><span data-stu-id="7be9e-472">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-473">3,5 Mo</span><span class="sxs-lookup"><span data-stu-id="7be9e-473">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="7be9e-474">3,5 Mo</span><span class="sxs-lookup"><span data-stu-id="7be9e-474">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="7be9e-475">3,5 Mo</span><span class="sxs-lookup"><span data-stu-id="7be9e-475">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="7be9e-476">5 MO</span><span class="sxs-lookup"><span data-stu-id="7be9e-476">5 MB</span></span></p></li>
<li><p><span data-ttu-id="7be9e-477">5 MO</span><span class="sxs-lookup"><span data-stu-id="7be9e-477">5 MB</span></span></p></li>
<li><p><span data-ttu-id="7be9e-478">5 MO</span><span class="sxs-lookup"><span data-stu-id="7be9e-478">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-479">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-479">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-480">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-480">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-481">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-481">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="7be9e-482">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-482">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-483">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-483">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-484">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-484">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-485">mai</span><span class="sxs-lookup"><span data-stu-id="7be9e-485">29</span></span></p></li>
<li><p><span data-ttu-id="7be9e-486">39</span><span class="sxs-lookup"><span data-stu-id="7be9e-486">39</span></span></p></li>
<li><p><span data-ttu-id="7be9e-487">391</span><span class="sxs-lookup"><span data-stu-id="7be9e-487">391</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="7be9e-488">35</span><span class="sxs-lookup"><span data-stu-id="7be9e-488">35</span></span></p></li>
<li><p><span data-ttu-id="7be9e-489">68</span><span class="sxs-lookup"><span data-stu-id="7be9e-489">68</span></span></p></li>
<li><p><span data-ttu-id="7be9e-490">461</span><span class="sxs-lookup"><span data-stu-id="7be9e-490">461</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7be9e-491">Taille de chaque package en cours de diffusion.</span><span class="sxs-lookup"><span data-stu-id="7be9e-491">Size of each package being streamed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be9e-492">Taille de chaque package.</span><span class="sxs-lookup"><span data-stu-id="7be9e-492">Size of each package.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-493">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-493">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-494">200</span><span class="sxs-lookup"><span data-stu-id="7be9e-494">200</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="7be9e-495">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-495">100</span></span></p></li>
<li><p><span data-ttu-id="7be9e-496">200</span><span class="sxs-lookup"><span data-stu-id="7be9e-496">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-497">21 MO</span><span class="sxs-lookup"><span data-stu-id="7be9e-497">21 MB</span></span></p></li>
<li><p><span data-ttu-id="7be9e-498">21 MO</span><span class="sxs-lookup"><span data-stu-id="7be9e-498">21 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="7be9e-499">109</span><span class="sxs-lookup"><span data-stu-id="7be9e-499">109</span></span></p></li>
<li><p><span data-ttu-id="7be9e-500">109</span><span class="sxs-lookup"><span data-stu-id="7be9e-500">109</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-501">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-501">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-502">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-502">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="7be9e-503">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-503">LAN</span></span></p></li>
<li><p><span data-ttu-id="7be9e-504">Réseau local</span><span class="sxs-lookup"><span data-stu-id="7be9e-504">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="7be9e-505">33</span><span class="sxs-lookup"><span data-stu-id="7be9e-505">33</span></span></p>
<p><span data-ttu-id="7be9e-506">83</span><span class="sxs-lookup"><span data-stu-id="7be9e-506">83</span></span></p>
<p></p>
<p><span data-ttu-id="7be9e-507">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-507">100</span></span></p>
<p><span data-ttu-id="7be9e-508">160</span><span class="sxs-lookup"><span data-stu-id="7be9e-508">160</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7be9e-509">Connexion réseau entre le client et le serveur de streaming App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="7be9e-509">Network connection between client and App-V 5.1 streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7be9e-510">1,5 Mbps réseau de liaison lente.</span><span class="sxs-lookup"><span data-stu-id="7be9e-510">1.5 Mbps Slow link network.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-511">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-511">100</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="7be9e-512">100</span><span class="sxs-lookup"><span data-stu-id="7be9e-512">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-513">3,5 Mo</span><span class="sxs-lookup"><span data-stu-id="7be9e-513">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="7be9e-514">5 MO</span><span class="sxs-lookup"><span data-stu-id="7be9e-514">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="7be9e-515">Réseau intra-continent 1,5 MB/s</span><span class="sxs-lookup"><span data-stu-id="7be9e-515">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="7be9e-516">102</span><span class="sxs-lookup"><span data-stu-id="7be9e-516">102</span></span></p>
<p></p>
<p><span data-ttu-id="7be9e-517">121</span><span class="sxs-lookup"><span data-stu-id="7be9e-517">121</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7be9e-518">Chaque serveur de streaming App-V 5,1 doit être en mesure de gérer un minimum de clients 200 en continu à partir d’applications virtualisées.</span><span class="sxs-lookup"><span data-stu-id="7be9e-518">Each App-V 5.1 streaming server should be able to handle a minimum of 200 clients concurrently streaming virtualized applications.</span></span>

<span data-ttu-id="7be9e-519">**Remarques**  La durée réelle du flux est déterminée principalement par le nombre de clients diffusés en continu, le nombre de packages, la taille du package, l’activité réseau du serveur et les conditions du réseau.</span><span class="sxs-lookup"><span data-stu-id="7be9e-519">**Note** The actual time to it will take to stream is determined primarily by the number of clients streaming simultaneously, number of packages, package size, the server’s network activity, and network conditions.</span></span>

 

<span data-ttu-id="7be9e-520">Par exemple, un utilisateur moyen peut diffuser un package 100 Mo en moins de 2 minutes, lorsque 100 clients simultanés sont en continu à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="7be9e-520">For example, an average user can stream a 100 MB package in less than 2 minutes, when 100 simultaneous clients are streaming from the server.</span></span> <span data-ttu-id="7be9e-521">Toutefois, un paquet d’une taille de 1 Go peut durer jusqu’à 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="7be9e-521">However, a package of size 1 GB could take up to 30 minutes.</span></span> <span data-ttu-id="7be9e-522">Dans la plupart des environnements réalistes, la diffusion en continu n’est pas uniformément distribuée, vous devez comprendre les exigences de flux maximal en matière de diffusion actuelles dans votre environnement afin de dimensionner correctement le nombre de serveurs de diffusion en continu requis.</span><span class="sxs-lookup"><span data-stu-id="7be9e-522">In most real world environments streaming demand is not uniformly distributed, you will need to understand the approximate peak streaming requirements present in your environment in order to properly size the number of required streaming servers.</span></span>

<span data-ttu-id="7be9e-523">Le nombre de clients qu’un serveur en continu peut prendre en charge peut être considérablement augmenté et les exigences en matière de flux maximal réduites si vous prémettez vos applications en cache.</span><span class="sxs-lookup"><span data-stu-id="7be9e-523">The number of clients a streaming server can support can be significantly increased and the peak streaming requirements reduced if you pre-cache your applications.</span></span> <span data-ttu-id="7be9e-524">Vous pouvez également augmenter le nombre de clients pris en charge par un serveur de diffusion en utilisant la diffusion en continu à la demande et des packages optimisés pour les flux.</span><span class="sxs-lookup"><span data-stu-id="7be9e-524">You can also increase the number of clients a streaming server can support by using on-demand streaming delivery and stream optimized packages.</span></span>

## <span data-ttu-id="7be9e-525">Combinaison des rôles de serveur App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="7be9e-525">Combining App-V 5.1 Server Roles</span></span>


<span data-ttu-id="7be9e-526">Remise de la mise à l’échelle et des exigences de tolérance de panne, le nombre minimal de serveurs nécessaires pour un emplacement avec la connectivité à Active Directory est un.</span><span class="sxs-lookup"><span data-stu-id="7be9e-526">Discounting scaling and fault-tolerance requirements, the minimum number of servers needed for a location with connectivity to Active Directory is one.</span></span> <span data-ttu-id="7be9e-527">Ce serveur va héberger le serveur de gestion, le service serveur de gestion et les rôles Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7be9e-527">This server will host the management server, management server service, and Microsoft SQL Server roles.</span></span> <span data-ttu-id="7be9e-528">Les rôles de serveur peuvent donc être organisés selon n’importe quelle combinaison souhaitée, car ils ne sont pas en conflit entre eux.</span><span class="sxs-lookup"><span data-stu-id="7be9e-528">Server roles, therefore, can be arranged in any desired combination since they do not conflict with one another.</span></span>

<span data-ttu-id="7be9e-529">En ignorant les exigences de mise à l’échelle, le nombre minimum de serveurs nécessaires à la fourniture d’une implémentation tolérante aux pannes est de quatre.</span><span class="sxs-lookup"><span data-stu-id="7be9e-529">Ignoring scaling requirements, the minimum number of servers necessary to provide a fault-tolerant implementation is four.</span></span> <span data-ttu-id="7be9e-530">Le serveur de gestion et les rôles Microsoft SQL Server pris en charge sont placés dans des configurations tolérantes aux pannes.</span><span class="sxs-lookup"><span data-stu-id="7be9e-530">The management server, and Microsoft SQL Server roles support being placed in fault-tolerant configurations.</span></span> <span data-ttu-id="7be9e-531">Le service du serveur de gestion peut être combiné avec n’importe lequel des rôles, mais il reste un point de défaillance unique.</span><span class="sxs-lookup"><span data-stu-id="7be9e-531">The management server service can be combined with any of the roles, but remains a single point of failure.</span></span>

<span data-ttu-id="7be9e-532">Bien qu’il existe un certain nombre de stratégies et de technologies de tolérance de panne disponibles, elles ne s’appliquent pas à un service donné.</span><span class="sxs-lookup"><span data-stu-id="7be9e-532">Although there are a number of fault-tolerance strategies and technologies available, not all are applicable to a given service.</span></span> <span data-ttu-id="7be9e-533">De plus, si les rôles App-V 5,1 sont combinés, certaines options de tolérance de panne risquent de ne plus être applicables en raison d’incompatibilités.</span><span class="sxs-lookup"><span data-stu-id="7be9e-533">Additionally, if App-V 5.1 roles are combined, certain fault-tolerance options may no longer apply due to incompatibilities.</span></span>






## <span data-ttu-id="7be9e-534">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7be9e-534">Related topics</span></span>


[<span data-ttu-id="7be9e-535">Configurations prises en charge par App-V5.1</span><span class="sxs-lookup"><span data-stu-id="7be9e-535">App-V 5.1 Supported Configurations</span></span>](app-v-51-supported-configurations.md)

[<span data-ttu-id="7be9e-536">Planification de la haute disponibilité avec App-V5.1</span><span class="sxs-lookup"><span data-stu-id="7be9e-536">Planning for High Availability with App-V 5.1</span></span>](planning-for-high-availability-with-app-v-51.md)

[<span data-ttu-id="7be9e-537">Envisager de déployer App-V</span><span class="sxs-lookup"><span data-stu-id="7be9e-537">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





