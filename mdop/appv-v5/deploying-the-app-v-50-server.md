---
title: Déploiement du serveur App-V5.0
description: Déploiement du serveur App-V5.0
author: dansimp
ms.assetid: a47f0dc8-2971-4e4d-8d57-6b69bbed4b63
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8fb65015a172a88d5e27d377037348dbc044654
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805827"
---
# <span data-ttu-id="3a972-103">Déploiement du serveur App-V5.0</span><span class="sxs-lookup"><span data-stu-id="3a972-103">Deploying the App-V 5.0 Server</span></span>


<span data-ttu-id="3a972-104">Vous pouvez installer les fonctionnalités du serveur App-V 5,0 à l’aide de différentes configurations de déploiement, décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="3a972-104">You can install the App-V 5.0 server features by using different deployment configurations, which described in this topic.</span></span> <span data-ttu-id="3a972-105">Avant d’installer les fonctionnalités du serveur, consultez la section serveur des [considérations relatives à la sécurité dans App-V 5,0](app-v-50-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="3a972-105">Before you install the server features, review the server section of [App-V 5.0 Security Considerations](app-v-50-security-considerations.md).</span></span>

<span data-ttu-id="3a972-106">Pour plus d’informations sur le déploiement du serveur App-V 5,0 SP3, voir [à propos de App-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).</span><span class="sxs-lookup"><span data-stu-id="3a972-106">For information about deploying the App-V 5.0 SP3 Server, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).</span></span>

<span data-ttu-id="3a972-107">**Important**  Avant d’installer et de configurer les serveurs App-V 5,0, vous devez spécifier un port sur lequel chaque composant sera hébergé.</span><span class="sxs-lookup"><span data-stu-id="3a972-107">**Important** Before you install and configure the App-V 5.0 servers, you must specify a port where each component will be hosted.</span></span> <span data-ttu-id="3a972-108">Vous devez également ajouter les règles de pare-feu associées pour permettre aux demandes entrantes d’accéder aux ports spécifiés.</span><span class="sxs-lookup"><span data-stu-id="3a972-108">You must also add the associated firewall rules to allow incoming requests to access the specified ports.</span></span> <span data-ttu-id="3a972-109">Le programme d’installation ne modifie pas les paramètres du pare-feu.</span><span class="sxs-lookup"><span data-stu-id="3a972-109">The installer does not modify firewall settings.</span></span>

 

## <a href="" id="---------app-v-5-0-server-overview"></a> <span data-ttu-id="3a972-110">Vue d’ensemble de App-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="3a972-110">App-V 5.0 Server overview</span></span>


<span data-ttu-id="3a972-111">Le serveur App-V 5,0 est composé de cinq composants.</span><span class="sxs-lookup"><span data-stu-id="3a972-111">The App-V 5.0 Server is made up of five components.</span></span> <span data-ttu-id="3a972-112">Chaque composant a un but différent au sein de l’environnement App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a972-112">Each component serves a different purpose within the App-V 5.0 environment.</span></span> <span data-ttu-id="3a972-113">Chacun des cinq composants est brièvement décrit ici:</span><span class="sxs-lookup"><span data-stu-id="3a972-113">Each of the five components is briefly described here:</span></span>

-   <span data-ttu-id="3a972-114">Serveur de gestion: fournit une fonctionnalité de gestion générale de l’infrastructure App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a972-114">Management Server – provides overall management functionality for the App-V 5.0 infrastructure.</span></span>

-   <span data-ttu-id="3a972-115">Base de données de gestion: facilite le déploiement de base de données pour la gestion d’App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a972-115">Management Database – facilitates database predeployments for App-V 5.0 management.</span></span>

-   <span data-ttu-id="3a972-116">Serveur de publication: fournit des fonctionnalités d’hébergement et de streaming pour les applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="3a972-116">Publishing Server – provides hosting and streaming functionality for virtual applications.</span></span>

-   <span data-ttu-id="3a972-117">Serveur de création de rapports-fournit une application-V 5,0 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="3a972-117">Reporting Server – provides App-V 5.0 reporting services.</span></span>

-   <span data-ttu-id="3a972-118">Base de données de création de rapports: facilite les déploiements de base de données pour la création de rapports App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a972-118">Reporting Database – facilitates database predeployments for App-V 5.0 reporting.</span></span>

## <a href="" id="---------app-v-5-0-stand-alone-deployment"></a> <span data-ttu-id="3a972-119">Déploiement autonome App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3a972-119">App-V 5.0 stand-alone deployment</span></span>


<span data-ttu-id="3a972-120">Le déploiement autonome de App-V 5,0 fournit une bonne topologie pour un déploiement ou un environnement de test de petite taille.</span><span class="sxs-lookup"><span data-stu-id="3a972-120">The App-V 5.0 standalone deployment provides a good topology for a small deployment or a test environment.</span></span> <span data-ttu-id="3a972-121">Lorsque vous utilisez ce type d’implémentation, tous les composants serveur sont déployés sur un seul ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3a972-121">When you use this type of implementation, all server components are deployed to a single computer.</span></span> <span data-ttu-id="3a972-122">Les services et bases de données associées font concurrence pour les ressources de l’ordinateur qui exécute les composants App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a972-122">The services and associated databases will compete for the resources on the computer that runs the App-V 5.0 components.</span></span> <span data-ttu-id="3a972-123">Par conséquent, vous ne devez pas utiliser cette topologie pour les déploiements de plus grande envergure.</span><span class="sxs-lookup"><span data-stu-id="3a972-123">Therefore, you should not use this topology for larger deployments.</span></span>

[<span data-ttu-id="3a972-124">Comment déployer le serveur App-V5.0</span><span class="sxs-lookup"><span data-stu-id="3a972-124">How to Deploy the App-V 5.0 Server</span></span>](how-to-deploy-the-app-v-50-server-50sp3.md)

[<span data-ttu-id="3a972-125">Déploiement du serveur App-V5.0 à l'aide d'un script</span><span class="sxs-lookup"><span data-stu-id="3a972-125">How to Deploy the App-V 5.0 Server Using a Script</span></span>](how-to-deploy-the-app-v-50-server-using-a-script.md)

## <a href="" id="---------app-v-5-0-server-distributed-deployment"></a> <span data-ttu-id="3a972-126">Déploiement distribué de App-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="3a972-126">App-V 5.0 Server distributed deployment</span></span>


<span data-ttu-id="3a972-127">La topologie de déploiement distribué peut prendre en charge une base de clients App-V 5,0 de grande taille et vous permet de gérer plus facilement votre environnement.</span><span class="sxs-lookup"><span data-stu-id="3a972-127">The distributed deployment topology can support a large App-V 5.0 client base and it allows you to more easily manage and scale your environment.</span></span> <span data-ttu-id="3a972-128">Lorsque vous utilisez ce type de déploiement, les composants serveur App-V 5,0 sont déployés sur plusieurs ordinateurs, en fonction de la structure et des besoins de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="3a972-128">When you use this type of deployment, the App-V 5.0 Server components are deployed across multiple computers, based on the structure and requirements of the organization.</span></span>

[<span data-ttu-id="3a972-129">Comment installer les bases de données de gestion et de rapports sur des ordinateurs distincts des services de gestion et de rapports</span><span class="sxs-lookup"><span data-stu-id="3a972-129">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)

[<span data-ttu-id="3a972-130">Comment installer le serveur de rapports sur un ordinateur autonome et le connecter à la base de données</span><span class="sxs-lookup"><span data-stu-id="3a972-130">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

[<span data-ttu-id="3a972-131">Déploiement du serveur App-V5.0 à l'aide d'un script</span><span class="sxs-lookup"><span data-stu-id="3a972-131">How to Deploy the App-V 5.0 Server Using a Script</span></span>](how-to-deploy-the-app-v-50-server-using-a-script.md)

[<span data-ttu-id="3a972-132">Comment installer le serveur de publication sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="3a972-132">How to Install the Publishing Server on a Remote Computer</span></span>](how-to-install-the-publishing-server-on-a-remote-computer.md)

[<span data-ttu-id="3a972-133">Comment installer le serveur de gestion sur un ordinateur autonome et le connecter à la base de données</span><span class="sxs-lookup"><span data-stu-id="3a972-133">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

## <span data-ttu-id="3a972-134">Utilisation d’une solution de distribution de logiciels d’entreprise (ESD) et App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3a972-134">Using an Enterprise Software Distribution (ESD) solution and App-V 5.0</span></span>


<span data-ttu-id="3a972-135">Vous pouvez également déployer les clients et packages App-V 5,0 à l’aide d’une ESD sans déployer App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a972-135">You can also deploy the App-V 5.0 clients and packages by using an ESD without having to deploy App-V 5.0.</span></span> <span data-ttu-id="3a972-136">Les fonctionnalités complètes d’intégration varient en fonction du niveau de ESD que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="3a972-136">The full capabilities for integration will vary depending on the ESD that you use.</span></span>

<span data-ttu-id="3a972-137">**Remarques**  Le serveur et la base de données de création de rapports App-V 5,0 peuvent toujours être déployés avec la fonctionnalité ESD pour collecter les données de rapport à partir des clients App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a972-137">**Note** The App-V 5.0 reporting server and reporting database can still be deployed alongside the ESD to collect the reporting data from the App-V 5.0 clients.</span></span> <span data-ttu-id="3a972-138">Toutefois, les trois autres composants serveur ne doivent pas être déployés, car ils vont entrer en conflit avec la fonctionnalité ESD.</span><span class="sxs-lookup"><span data-stu-id="3a972-138">However, the other three server components should not be deployed, because they will conflict with the ESD functionality.</span></span>

 

[<span data-ttu-id="3a972-139">Déploiement de packages App-V5.0 à l'aide d'une solution de distribution électronique de logiciels (ESD)</span><span class="sxs-lookup"><span data-stu-id="3a972-139">Deploying App-V 5.0 Packages by Using Electronic Software Distribution (ESD)</span></span>](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md)

## <a href="" id="---------app-v-5-0-server-logs"></a> <span data-ttu-id="3a972-140">Journaux de l’App-V 5,0 Server</span><span class="sxs-lookup"><span data-stu-id="3a972-140">App-V 5.0 Server logs</span></span>


<span data-ttu-id="3a972-141">Vous pouvez utiliser les informations du journal du serveur App-V 5,0 pour résoudre les problèmes liés à l’installation du serveur et aux événements opérationnels lors de l’utilisation d’App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a972-141">You can use App-V 5.0 server log information to help troubleshoot the server installation and operational events while using App-V 5.0.</span></span> <span data-ttu-id="3a972-142">Les informations du journal relatives au serveur peuvent être examinées à l’aide de l' **Observateur d’événements**.</span><span class="sxs-lookup"><span data-stu-id="3a972-142">The server-related log information can be reviewed with the **Event Viewer**.</span></span> <span data-ttu-id="3a972-143">La ligne suivante affiche le chemin d’accès spécifique aux événements liés au serveur:</span><span class="sxs-lookup"><span data-stu-id="3a972-143">The following line displays the specific path for Server-related events:</span></span>

**<span data-ttu-id="3a972-144">Journaux de l’observateur d’événements \ \ applications et services</span><span class="sxs-lookup"><span data-stu-id="3a972-144">Event Viewer \\ Applications and Services Logs \\ Microsoft \\ App V</span></span>**

<span data-ttu-id="3a972-145">Les journaux d’installation associés sont enregistrés dans l’annuaire suivant:</span><span class="sxs-lookup"><span data-stu-id="3a972-145">Associated setup logs are saved in the following directory:</span></span>

**<span data-ttu-id="3a972-146">temporaire</span><span class="sxs-lookup"><span data-stu-id="3a972-146">%temp%</span></span>**

<span data-ttu-id="3a972-147">Dans App-V 5,0 SP3, certains journaux ont été consolidés et déplacés.</span><span class="sxs-lookup"><span data-stu-id="3a972-147">In App-V 5.0 SP3, some logs have been consolidated and moved.</span></span> <span data-ttu-id="3a972-148">Voir [à propos de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="3a972-148">See [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

## <a href="" id="---------app-v-5-0-reporting"></a> <span data-ttu-id="3a972-149">Rapports App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="3a972-149">App-V 5.0 reporting</span></span>


<span data-ttu-id="3a972-150">Les rapports App-V 5,0 permettent aux clients App-V 5,0 de collecter des données, puis de les renvoyer dans un référentiel central.</span><span class="sxs-lookup"><span data-stu-id="3a972-150">App-V 5.0 reporting allows App-V 5.0 clients to collect data and then send it back to be stored in a central repository.</span></span> <span data-ttu-id="3a972-151">Vous pouvez utiliser ces informations pour obtenir un meilleur aperçu de l’utilisation des applications virtuelles au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3a972-151">You can use this information to get a better view of the virtual application usage within your organization.</span></span> <span data-ttu-id="3a972-152">La liste suivante présente certains types d’informations recueillies par le client App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="3a972-152">The following list displays some of the types of information the App-V 5.0 client collects:</span></span>

-   <span data-ttu-id="3a972-153">Des informations sur l’ordinateur qui exécute le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a972-153">Information about the computer that runs the App-V 5.0 client.</span></span>

-   <span data-ttu-id="3a972-154">Des informations sur les packages virtualisés sur un ordinateur spécifique exécutant le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="3a972-154">Information about virtualized packages on a specific computer that runs the App-V 5.0 client.</span></span>

-   <span data-ttu-id="3a972-155">Des informations sur l’ouverture et l’arrêt du package pour un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="3a972-155">Information about package open and shutdown for a specific user.</span></span>

<span data-ttu-id="3a972-156">Les informations de rapport seront conservées jusqu’à ce qu’elles soient correctement envoyées à la base de données du serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="3a972-156">The reporting information will be maintained until it is successfully sent to the reporting server database.</span></span> <span data-ttu-id="3a972-157">Une fois les données dans la base de données, vous pouvez utiliser Microsoft SQL Server Reporting Services pour générer les rapports nécessaires.</span><span class="sxs-lookup"><span data-stu-id="3a972-157">After the data is in the database, you can use Microsoft SQL Server Reporting Services to generate any necessary reports.</span></span>

<span data-ttu-id="3a972-158">Si vous souhaitez récupérer des informations de rapport, vous devez utiliser Microsoft SQL Server Reporting Services (SSRS) disponible avec Microsoft SQL.</span><span class="sxs-lookup"><span data-stu-id="3a972-158">If you want to retrieve report information, you must use Microsoft SQL Server Reporting Services (SSRS) which is available with Microsoft SQL.</span></span> <span data-ttu-id="3a972-159">SSRS n’est pas installé lors de l’installation du serveur de rapports App-V 5,0 et doit être déployé séparément pour générer les rapports associés.</span><span class="sxs-lookup"><span data-stu-id="3a972-159">SSRS is not installed when you install the App-V 5.0 reporting server and it must be deployed separately to generate the associated reports.</span></span>

<span data-ttu-id="3a972-160">Pour plus d’informations [sur la création de rapports App-V 5,0](about-app-v-50-reporting.md), utilisez le lien suivant.</span><span class="sxs-lookup"><span data-stu-id="3a972-160">Use the following link for more information [About App-V 5.0 Reporting](about-app-v-50-reporting.md).</span></span>

[<span data-ttu-id="3a972-161">Activation de la création de rapports sur App-V5.0 Client à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="3a972-161">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)

## <span data-ttu-id="3a972-162">Autres ressources pour le serveur App-V</span><span class="sxs-lookup"><span data-stu-id="3a972-162">Other resources for the App-V server</span></span>


[<span data-ttu-id="3a972-163">Déploiement d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="3a972-163">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)






 

 





