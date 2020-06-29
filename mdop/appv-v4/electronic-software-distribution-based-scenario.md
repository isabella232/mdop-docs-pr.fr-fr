---
title: Scénario basé sur une distribution électronique de logiciels
description: Scénario basé sur une distribution électronique de logiciels
author: dansimp
ms.assetid: 18be0f8d-60ee-449b-aa83-93c86d1a908e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 52b9a30f2b1d403ec41090252f331a984225fd19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808849"
---
# <span data-ttu-id="9239f-103">Scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="9239f-103">Electronic Software Distribution-Based Scenario</span></span>


<span data-ttu-id="9239f-104">Si vous envisagez d’utiliser un scénario de déploiement de distribution de logiciels électronique (ESD) pour votre environnement Microsoft Application Virtualization, il est important de bien comprendre les facteurs qui entrent en vigueur ou qui sont concernés par cette décision.</span><span class="sxs-lookup"><span data-stu-id="9239f-104">If you plan to use an electronic software distribution (ESD) deployment scenario for your Microsoft Application Virtualization environment, it is important to understand the factors that go into and are affected by that decision.</span></span> <span data-ttu-id="9239f-105">Les rubriques de cette section décrivent le scénario ESD et fournissent des informations sur les méthodes de remise du package, les protocoles de transmission et les composants externes que vous devrez envisager dans votre stratégie de déploiement.</span><span class="sxs-lookup"><span data-stu-id="9239f-105">The topics in this section describe the ESD scenario and provide information about package delivery methods, transmission protocols, and external components that you will need to consider in your deployment strategy.</span></span> <span data-ttu-id="9239f-106">Vous pouvez également suivre les procédures décrites dans cette section pour terminer votre déploiement, de la phase de configuration du serveur à la phase de vérification du déploiement.</span><span class="sxs-lookup"><span data-stu-id="9239f-106">You can also use the procedures in this section to complete your deployment, from the server configuration phase through the deployment verification phase.</span></span>

## <span data-ttu-id="9239f-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="9239f-107">In This Section</span></span>


<a href="" id="electronic-software-distribution-based-scenario-overview"></a>[<span data-ttu-id="9239f-108">Présentation du scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="9239f-108">Electronic Software Distribution-Based Scenario Overview</span></span>](electronic-software-distribution-based-scenario-overview.md)  
<span data-ttu-id="9239f-109">Fournit des informations importantes sur les méthodes de publication et de diffusion en continu que vous pouvez utiliser pour un déploiement ESD.</span><span class="sxs-lookup"><span data-stu-id="9239f-109">Provides important information about the publishing and streaming methods you can use for an ESD-based deployment.</span></span>

<a href="" id="how-to-configure-servers-for-esd-based-deployment"></a>[<span data-ttu-id="9239f-110">Procédure pour configurer des serveurs pour un déploiement basé sur ESD</span><span class="sxs-lookup"><span data-stu-id="9239f-110">How to Configure Servers for ESD-Based Deployment</span></span>](how-to-configure-servers-for-esd-based-deployment.md)  
<span data-ttu-id="9239f-111">Cette section contient des procédures que vous pouvez utiliser pour configurer les serveurs de streaming de la virtualisation des applications, le serveur IIS et le serveur de fichiers pour votre stratégie de déploiement basée sur la distribution de logiciels électroniques.</span><span class="sxs-lookup"><span data-stu-id="9239f-111">This section provides procedures you can use to configure the Application Virtualization Streaming Servers, the IIS server, and the file server for your electronic software distribution–based deployment strategy.</span></span>

<a href="" id="how-to-install-the-client-by-using-the-command-line"></a>[<span data-ttu-id="9239f-112">Procédure pour installer le client via la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="9239f-112">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)  
<span data-ttu-id="9239f-113">Fournit des procédures de ligne de commande pour l’installation du client de virtualisation des applications, à l’aide du fichier setup.exe ou setup.msi.</span><span class="sxs-lookup"><span data-stu-id="9239f-113">Provides command-line procedures for installing the Application Virtualization Client, using either the setup.exe or the setup.msi file.</span></span>

<a href="" id="how-to-uninstall-the-app-v-client"></a>[<span data-ttu-id="9239f-114">Procédure pour désinstaller App-V Client</span><span class="sxs-lookup"><span data-stu-id="9239f-114">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)  
<span data-ttu-id="9239f-115">Fournit une procédure détaillée que vous pouvez utiliser pour vérifier que le client de virtualisation d’application a été installé et fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="9239f-115">Provides a step-by-step procedure you can use to confirm that the Application Virtualization Client has been installed and is functioning correctly.</span></span>

<a href="" id="how-to-publish-a-virtual-application-on-the-client"></a>[<span data-ttu-id="9239f-116">Procédure pour publier une application virtuelle sur le client</span><span class="sxs-lookup"><span data-stu-id="9239f-116">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)  
<span data-ttu-id="9239f-117">Fournit des procédures de ligne de commande pour la publication d’un package d’application, à l’aide du programme d’installation Windows ou SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="9239f-117">Provides command-line procedures for publishing an application package, using either Windows Installer or SFTMIME.</span></span>

## <span data-ttu-id="9239f-118">Référence</span><span class="sxs-lookup"><span data-stu-id="9239f-118">Reference</span></span>


[<span data-ttu-id="9239f-119">Paramètres de ligne de commande du programme d'installation d'Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="9239f-119">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

## <span data-ttu-id="9239f-120">Sections connexes</span><span class="sxs-lookup"><span data-stu-id="9239f-120">Related Sections</span></span>


[<span data-ttu-id="9239f-121">Scénario basé sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="9239f-121">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

## <span data-ttu-id="9239f-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9239f-122">Related topics</span></span>


[<span data-ttu-id="9239f-123">Aspects à prendre en compte pour le déploiement et la mise à niveau d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="9239f-123">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

[<span data-ttu-id="9239f-124">Scénario de distribution autonome pour les clients Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="9239f-124">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





