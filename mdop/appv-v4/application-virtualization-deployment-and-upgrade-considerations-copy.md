---
title: Aspects à prendre en compte pour le déploiement et la mise à niveau d'Application Virtualization
description: Aspects à prendre en compte pour le déploiement et la mise à niveau d'Application Virtualization
author: dansimp
ms.assetid: c3c38930-0da3-43e6-b240-945edfd00a01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09e6943c74c7f17b6a61bc7be4bcde925a54be56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809257"
---
# <span data-ttu-id="8bbd9-103">Aspects à prendre en compte pour le déploiement et la mise à niveau d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8bbd9-103">Application Virtualization Deployment and Upgrade Considerations</span></span>


<span data-ttu-id="8bbd9-104">Avant de commencer le déploiement de Microsoft Application Virtualization (App-V), il se peut que vous deviez revoir la configuration requise pour votre environnement qui inclut la configuration matérielle et logicielle requise pour l’installation des différents composants de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="8bbd9-104">Before you begin the deployment of Microsoft Application Virtualization (App-V), you might have to review your environment requirements that includes the hardware and software requirements for installing the various Application Virtualization components.</span></span> <span data-ttu-id="8bbd9-105">Par ailleurs, si vous effectuez une mise à niveau à partir d’une version antérieure, les rubriques de cette section fournissent des informations sur la mise à niveau de votre séquence, de votre serveur et de vos versions de client actuelles.</span><span class="sxs-lookup"><span data-stu-id="8bbd9-105">Also, if you are upgrading from an earlier version, the topics in this section provide information about how to upgrade your current Sequencer, Server, and Client versions.</span></span>

## <span data-ttu-id="8bbd9-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="8bbd9-106">In This Section</span></span>


<a href="" id="application-virtualization-deployment-requirements"></a>[<span data-ttu-id="8bbd9-107">Configuration requise pour le déploiement d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8bbd9-107">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)  
<span data-ttu-id="8bbd9-108">Fournit des informations générales sur la configuration système requise et les considérations en matière de mise à niveau pour le déploiement de la virtualisation de l’application.</span><span class="sxs-lookup"><span data-stu-id="8bbd9-108">Provides general information about system requirements and upgrade considerations for your Application Virtualization deployment.</span></span>

<a href="" id="application-virtualization-deployment-and-upgrade-checklists"></a>[<span data-ttu-id="8bbd9-109">Listes de contrôle pour le déploiement et la mise à niveau d'Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8bbd9-109">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)  
<span data-ttu-id="8bbd9-110">Fournit des listes détaillées de tâches d’installation et de mise à niveau avec des liens vers les procédures spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8bbd9-110">Provides detailed lists of installation and upgrade tasks with links to the specific procedures.</span></span>

<a href="" id="how-to-install-the-servers-and-system-components"></a>[<span data-ttu-id="8bbd9-111">Procédure pour installer les serveurs et les composants système</span><span class="sxs-lookup"><span data-stu-id="8bbd9-111">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)  
<span data-ttu-id="8bbd9-112">Décrit comment installer les composants de plateforme Application Virtualization (App-V) requis pour votre déploiement serveur.</span><span class="sxs-lookup"><span data-stu-id="8bbd9-112">Describes how to install the Application Virtualization (App-V) platform components required for your server-based deployment.</span></span>

<a href="" id="how-to-manually-install-the-application-virtualization-client"></a>[<span data-ttu-id="8bbd9-113">Procédure pour installer manuellement Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="8bbd9-113">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)  
<span data-ttu-id="8bbd9-114">Décrit comment installer le logiciel client de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="8bbd9-114">Describes how to install the Application Virtualization Client software.</span></span>

<a href="" id="how-to-install-the-application-virtualization-sequencer"></a>[<span data-ttu-id="8bbd9-115">Procédure pour installer Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="8bbd9-115">How to Install the Application Virtualization Sequencer</span></span>](how-to-install-the-application-virtualization-sequencer.md)  
<span data-ttu-id="8bbd9-116">Décrit comment installer le Sequencer de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="8bbd9-116">Describes how to install the Application Virtualization Sequencer.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-client"></a>[<span data-ttu-id="8bbd9-117">Procédure pour mettre à niveau Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="8bbd9-117">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)  
<span data-ttu-id="8bbd9-118">Décrit la mise à niveau du client de bureau de virtualisation des applications ou du client de virtualisation des applications pour les services Bureau à distance (anciennement services Terminal Server).</span><span class="sxs-lookup"><span data-stu-id="8bbd9-118">Describes how to upgrade the Application Virtualization Desktop Client or the Application Virtualization Client for Remote Desktop Services (formerly Terminal Services).</span></span>

<a href="" id="how-to-upgrade-the-servers-and-system-components"></a>[<span data-ttu-id="8bbd9-119">Procédure pour mettre à niveau les serveurs et les composants système</span><span class="sxs-lookup"><span data-stu-id="8bbd9-119">How to Upgrade the Servers and System Components</span></span>](how-to-upgrade-the-servers-and-system-components.md)  
<span data-ttu-id="8bbd9-120">Décrit la procédure de mise à niveau des composants logiciels installés sur tous les ordinateurs du système de gestion des applications.</span><span class="sxs-lookup"><span data-stu-id="8bbd9-120">Describes how to upgrade the software components installed on all Application Virtualization Management System computers.</span></span>

<a href="" id="how-to-upgrade-the-application-virtualization-sequencer"></a>[<span data-ttu-id="8bbd9-121">Procédure pour mettre à niveau Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="8bbd9-121">How to Upgrade the Application Virtualization Sequencer</span></span>](how-to-upgrade-the-application-virtualization-sequencer.md)  
<span data-ttu-id="8bbd9-122">Décrit comment mettre à niveau le Sequencer sur des ordinateurs exécutant Vista ou WindowsXP.</span><span class="sxs-lookup"><span data-stu-id="8bbd9-122">Describes how to upgrade the Sequencer on computers that are running WindowsVista or WindowsXP.</span></span>

## <span data-ttu-id="8bbd9-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8bbd9-123">Related topics</span></span>


[<span data-ttu-id="8bbd9-124">Référence à Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8bbd9-124">Application Virtualization Reference</span></span>](application-virtualization-reference.md)

[<span data-ttu-id="8bbd9-125">Scénario basé sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="8bbd9-125">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="8bbd9-126">Scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="8bbd9-126">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="8bbd9-127">Scénario de distribution autonome pour les clients Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="8bbd9-127">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





