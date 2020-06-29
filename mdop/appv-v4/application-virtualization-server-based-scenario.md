---
title: Scénario basé sur un serveur Application Virtualization Server
description: Scénario basé sur un serveur Application Virtualization Server
author: dansimp
ms.assetid: 10ed0b18-087d-470f-951b-5083f4cb076f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6699bdc734258f67e4938e33266a2f061531939
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807942"
---
# <span data-ttu-id="bba7e-103">Scénario basé sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="bba7e-103">Application Virtualization Server-Based Scenario</span></span>


<span data-ttu-id="bba7e-104">Si vous envisagez d’utiliser un scénario de déploiement basé sur un serveur pour votre environnement Microsoft Application Virtualization (App-V), vous devez comprendre les différences entre le serveur de gestion de la virtualisation des applications et le serveur de diffusion de la virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="bba7e-104">If you plan to use a server-based deployment scenario for your Microsoft Application Virtualization (App-V) environment, you should understand the differences between the Application Virtualization Management Server and the Application Virtualization Streaming Server.</span></span> <span data-ttu-id="bba7e-105">Les rubriques de cette section décrivent ces différences et fournissent également des informations sur les méthodes de remise de packages, les protocoles de transmission et les composants externes que vous devez prendre en compte lors du déploiement.</span><span class="sxs-lookup"><span data-stu-id="bba7e-105">The topics in this section describe those differences and also provide information about package delivery methods, transmission protocols, and external components that you have to consider as you continue with your deployment.</span></span> <span data-ttu-id="bba7e-106">Cette section fournit également des procédures pas à pas pour l’installation et la configuration du serveur de gestion des applications-V et des serveurs de diffusion en continu d’applications.</span><span class="sxs-lookup"><span data-stu-id="bba7e-106">This section also provides step-by-step procedures for installing and configuring the App-V Management Server and the Application Virtualization Streaming Servers.</span></span>

## <span data-ttu-id="bba7e-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="bba7e-107">In This Section</span></span>


<a href="" id="application-virtualization-server-based-scenario-overview"></a>[<span data-ttu-id="bba7e-108">Présentation du scénario basé sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="bba7e-108">Application Virtualization Server-Based Scenario Overview</span></span>](application-virtualization-server-based-scenario-overview.md)  
<span data-ttu-id="bba7e-109">Fournit des informations importantes sur le déploiement du serveur de gestion des applications, le serveur de diffusion de la virtualisation des applications, ainsi que les méthodes de remise des packages, les protocoles et les composants externes pertinents pour votre plan de déploiement serveur.</span><span class="sxs-lookup"><span data-stu-id="bba7e-109">Provides important deployment information about the Application Virtualization Management Server, the Application Virtualization Streaming Server, and the package delivery methods, protocols, and external components relevant to your server-based deployment plan.</span></span>

<a href="" id="how-to-install-the-servers-and-system-components"></a>[<span data-ttu-id="bba7e-110">Procédure pour installer les serveurs et les composants système</span><span class="sxs-lookup"><span data-stu-id="bba7e-110">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)  
<span data-ttu-id="bba7e-111">Décrit comment installer les composants de plateforme Microsoft Application Virtualization requis pour votre déploiement serveur.</span><span class="sxs-lookup"><span data-stu-id="bba7e-111">Describes how to install the Microsoft Application Virtualization platform components required for your server-based deployment.</span></span>

<a href="" id="how-to-configure-servers-for-server-based-deployment"></a>[<span data-ttu-id="bba7e-112">Procédure pour configurer des serveurs pour un déploiement basé sur un serveur</span><span class="sxs-lookup"><span data-stu-id="bba7e-112">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)  
<span data-ttu-id="bba7e-113">Décrit la procédure de configuration du serveur de gestion de la virtualisation des applications, serveur de diffusion en continu d’applications, serveur IIS (Internet Information Integration) et serveur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="bba7e-113">Describes how to configure the Application Virtualization Management Server, the Application Virtualization Streaming Server, the Internet Information Integration (IIS) server, and the file server.</span></span>

<a href="" id="how-to-configure-a-read-only-cache-on-the-app-v-client--vdi-"></a>[<span data-ttu-id="bba7e-114">Procédure pour configurer un cache en lecture seule dans App-V Client (VDI)</span><span class="sxs-lookup"><span data-stu-id="bba7e-114">How to Configure a Read-only Cache on the App-V Client (VDI)</span></span>](how-to-configure-a-read-only-cache-on-the-app-v-client--vdi-.md)  
<span data-ttu-id="bba7e-115">Décrit comment configurer le client App-V pour utiliser le cache en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="bba7e-115">Describes how to configure the App-V client to use read-only cache.</span></span>

<a href="" id="how-to-configure-a-read-only-cache-on-the-app-v-client--rds-"></a>[<span data-ttu-id="bba7e-116">Procédure pour configurer un cache en lecture seule dans App-V Client (RDS)</span><span class="sxs-lookup"><span data-stu-id="bba7e-116">How to Configure a Read-only Cache on the App-V Client (RDS)</span></span>](how-to-configure-a-read-only-cache-on-the-app-v-client--rds--sp1.md)  
<span data-ttu-id="bba7e-117">Décrit comment configurer le client App-V pour utiliser le cache en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="bba7e-117">Describes how to configure the App-V client to use read-only cache.</span></span>

<a href="" id="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v"></a>[<span data-ttu-id="bba7e-118">Procédure pour configurer la prise en charge de la mise en miroir de Microsoft SQL Server pour App-V</span><span class="sxs-lookup"><span data-stu-id="bba7e-118">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span>](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)  
<span data-ttu-id="bba7e-119">Décrit la configuration de la mise en miroir de la base de données à l’aide de Microsoft SQL Server pour votre système App-V.</span><span class="sxs-lookup"><span data-stu-id="bba7e-119">Describes how to configure database mirroring by using Microsoft SQL Server for your App-V system.</span></span>

## <span data-ttu-id="bba7e-120">Référence</span><span class="sxs-lookup"><span data-stu-id="bba7e-120">Reference</span></span>


[<span data-ttu-id="bba7e-121">Paramètres de ligne de commande du programme d'installation d'Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="bba7e-121">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

## <span data-ttu-id="bba7e-122">Sections connexes</span><span class="sxs-lookup"><span data-stu-id="bba7e-122">Related Sections</span></span>


[<span data-ttu-id="bba7e-123">Scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="bba7e-123">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

## <span data-ttu-id="bba7e-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bba7e-124">Related topics</span></span>


[<span data-ttu-id="bba7e-125">Aspects à prendre en compte pour le déploiement et la mise à niveau d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="bba7e-125">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

[<span data-ttu-id="bba7e-126">Scénario de distribution autonome pour les clients Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="bba7e-126">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





