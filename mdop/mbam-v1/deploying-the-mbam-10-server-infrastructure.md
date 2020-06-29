---
title: Déploiement de l'infrastructure de serveur MBAM1.0
description: Déploiement de l'infrastructure de serveur MBAM1.0
author: dansimp
ms.assetid: 90529379-b70e-4c92-b188-3d7aaf1844af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de136db557233a097d95f47ef0a1bba5996798c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810998"
---
# <span data-ttu-id="4ff7b-103">Déploiement de l'infrastructure de serveur MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="4ff7b-103">Deploying the MBAM 1.0 Server Infrastructure</span></span>


<span data-ttu-id="4ff7b-104">Vous pouvez installer les fonctionnalités serveur d’administration et de surveillance de BitLocker (MBAM) de Microsoft dans différentes configurations en utilisant un à cinq serveurs.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-104">You can install Microsoft BitLocker Administration and Monitoring (MBAM) Server features in different configurations by using one to five servers.</span></span> <span data-ttu-id="4ff7b-105">En règle générale, vous devez utiliser une configuration de trois à cinq serveurs pour les environnements de production, en fonction de vos besoins en matière de modularité.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-105">Generally, you should use a configuration of three to five servers for production environments, depending on your scalability needs.</span></span> <span data-ttu-id="4ff7b-106">Pour plus d’informations sur l’évolutivité des performances des topologies de déploiement MBAM et recommandées, consultez le livre blanc sur l' [évolutivité et la haute disponibilité du MBAM](https://go.microsoft.com/fwlink/p/?LinkId=258314).</span><span class="sxs-lookup"><span data-stu-id="4ff7b-106">For more information about performance scalability of MBAM and recommended deployment topologies, see the [MBAM Scalability and High-Availability Guide White Paper](https://go.microsoft.com/fwlink/p/?LinkId=258314).</span></span>

## <span data-ttu-id="4ff7b-107">Déploiement de tous les 1,0 MBAM sur un serveur unique</span><span class="sxs-lookup"><span data-stu-id="4ff7b-107">Deploy all MBAM 1.0 on a single server</span></span>


<span data-ttu-id="4ff7b-108">Dans cette configuration, toutes les fonctionnalités de MBAM sont installées sur un seul serveur.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-108">In this configuration, all MBAM features are installed on a single server.</span></span> <span data-ttu-id="4ff7b-109">Cette topologie de déploiement pour l’infrastructure de serveur MBAM prend en charge jusqu’à 21 000 ordinateurs client MBAM.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-109">This deployment topology for MBAM server infrastructure will support up to 21,000 MBAM client computers.</span></span>

<span data-ttu-id="4ff7b-110">**Important**  Cette configuration est prise en charge, mais nous vous recommandons de la tester uniquement.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-110">**Important** This configuration is supported, but we recommend it for testing only.</span></span>

 

<span data-ttu-id="4ff7b-111">Les procédures dans cette section décrivent l’installation complète des fonctionnalités MBAM sur un serveur unique.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-111">The procedures in this section describe the full installation of the MBAM features on a single server.</span></span>

[<span data-ttu-id="4ff7b-112">Installation et configuration de MBAM sur un seul serveur</span><span class="sxs-lookup"><span data-stu-id="4ff7b-112">How to Install and Configure MBAM on a Single Server</span></span>](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## <span data-ttu-id="4ff7b-113">Déploiement de MBAM 1,0 sur des serveurs distribués</span><span class="sxs-lookup"><span data-stu-id="4ff7b-113">Deploy MBAM 1.0 on distributed servers</span></span>


<span data-ttu-id="4ff7b-114">Les fonctionnalités de MBAM peuvent être installées dans différentes configurations, en fonction de vos besoins en matière de modularité.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-114">MBAM features can be installed in different configurations, depending on your scalability needs.</span></span> <span data-ttu-id="4ff7b-115">Pour plus d’informations sur la planification du déploiement de fonctionnalités MBAM Server, voir [planification du déploiement de MBAM 1,0 Server](planning-for-mbam-10-server-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="4ff7b-115">For more information about how to plan for MBAM server feature deployment, see [Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md).</span></span>

<span data-ttu-id="4ff7b-116">Les procédures dans cette section décrivent l’installation complète des fonctionnalités MBAM sur les serveurs distribués.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-116">The procedures in this section describe the full installation of the MBAM features on distributed servers.</span></span>

### <span data-ttu-id="4ff7b-117">Configuration à trois ordinateurs</span><span class="sxs-lookup"><span data-stu-id="4ff7b-117">Three-computer configuration</span></span>

<span data-ttu-id="4ff7b-118">Le diagramme suivant montre la topologie de déploiement à trois ordinateurs pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-118">The following diagram displays the three-computer deployment topology for MBAM.</span></span> <span data-ttu-id="4ff7b-119">Nous vous recommandons d’utiliser cette topologie pour les environnements de production qui prennent en charge jusqu’aux clients MBAM 55 000.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-119">We recommend this topology for production environments that support up to 55,000 MBAM Clients.</span></span>

![MBAM trois topologie de déploiement d’ordinateur](images/mbam-3-server.jpg)

<span data-ttu-id="4ff7b-121">Dans cette configuration, les fonctionnalités de MBAM sont installées dans la configuration suivante:</span><span class="sxs-lookup"><span data-stu-id="4ff7b-121">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="4ff7b-122">Les rapports de conformité et de base de données matérielle, de conformité et d’audit sont installés sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-122">Recovery and Hardware Database, Compliance and Audit Database, and Compliance and Audit Reports are installed on a server.</span></span>

2.  <span data-ttu-id="4ff7b-123">La fonctionnalité d’administration et de surveillance du serveur est installée sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-123">Administration and Monitoring Server feature is installed on a server.</span></span>

3.  <span data-ttu-id="4ff7b-124">MBAM modèle de stratégie de groupe est installé sur un ordinateur capable de modifier des objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-124">MBAM Group Policy template is installed on a computer that is capable of modifying Group Policy Objects (GPO).</span></span>

### <span data-ttu-id="4ff7b-125">Configuration à quatre ordinateurs</span><span class="sxs-lookup"><span data-stu-id="4ff7b-125">Four-computer configuration</span></span>

<span data-ttu-id="4ff7b-126">Le diagramme ci-après présente la topologie de déploiement à quatre ordinateurs pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-126">The following diagram displays the four-computer deployment topology for MBAM.</span></span> <span data-ttu-id="4ff7b-127">Nous vous recommandons d’utiliser cette topologie pour les environnements de production qui prennent en charge jusqu’aux clients MBAM 110 000.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-127">We recommended this topology for production environments that support up to 110,000 MBAM Clients.</span></span>

![MBAM 4 topologie de déploiement d’ordinateur.](images/mbam-4-computer.jpg)

<span data-ttu-id="4ff7b-129">Dans cette configuration, les fonctionnalités de MBAM sont installées dans la configuration suivante:</span><span class="sxs-lookup"><span data-stu-id="4ff7b-129">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="4ff7b-130">Les rapports de conformité et de base de données matérielle, de conformité et d’audit sont installés sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-130">Recovery and Hardware Database, Compliance and Audit Database, and Compliance and Audit Reports are installed on a server.</span></span>

2.  <span data-ttu-id="4ff7b-131">La fonctionnalité d’administration et de surveillance du serveur est installée sur un serveur configuré dans un cluster de serveurs de l’équilibrage de charge réseau.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-131">Administration and Monitoring Server feature is installed on a server that is configured in a Network Load Balancing (NLB) Server Cluster.</span></span>

3.  <span data-ttu-id="4ff7b-132">MBAM modèle de stratégie de groupe est installé sur un ordinateur capable de modifier les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-132">MBAM Group Policy template is installed on a computer that is capable of modifying the Group Policy Objects.</span></span>

### <span data-ttu-id="4ff7b-133">Configuration de cinq ordinateurs</span><span class="sxs-lookup"><span data-stu-id="4ff7b-133">Five-computer configuration</span></span>

<span data-ttu-id="4ff7b-134">Le diagramme suivant présente la topologie de déploiement à cinq ordinateurs pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-134">The following diagram displays the five-computer deployment topology for MBAM.</span></span> <span data-ttu-id="4ff7b-135">Nous vous recommandons d’utiliser cette topologie pour les environnements de production qui prennent en charge jusqu’aux clients MBAM 135 000.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-135">We recommend this topology for production environments that support up to 135,000 MBAM Clients.</span></span>

![MBAM cinq topologie de déploiement d’ordinateur.](images/mbam-5-computer.jpg)

<span data-ttu-id="4ff7b-137">Dans cette configuration, les fonctionnalités de MBAM sont installées dans la configuration suivante:</span><span class="sxs-lookup"><span data-stu-id="4ff7b-137">In this configuration, MBAM features are installed in the following configuration:</span></span>

1.  <span data-ttu-id="4ff7b-138">La base de données de récupération et de matériel est installée sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-138">Recovery and Hardware Database is installed on a server.</span></span>

2.  <span data-ttu-id="4ff7b-139">Les rapports de conformité et d’audit sont installés sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-139">The Compliance and Audit Database and Compliance and Audit Reports are installed on a server.</span></span>

3.  <span data-ttu-id="4ff7b-140">La fonctionnalité d’administration et de surveillance du serveur est installée sur un serveur configuré dans un cluster de serveurs de l’équilibrage de charge réseau.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-140">Administration and Monitoring Server feature is installed on a server that is configured in a Network Load Balancing (NLB) Server Cluster.</span></span>

4.  <span data-ttu-id="4ff7b-141">MBAM modèle de stratégie de groupe est installé sur un ordinateur capable de modifier des objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4ff7b-141">MBAM Group Policy template is installed on a computer that is capable of modifying Group Policy Objects.</span></span>

[<span data-ttu-id="4ff7b-142">Installation et configuration de MBAM sur des serveurs distribués</span><span class="sxs-lookup"><span data-stu-id="4ff7b-142">How to Install and Configure MBAM on Distributed Servers</span></span>](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[<span data-ttu-id="4ff7b-143">Configurer l'équilibrage de la charge réseau pour MBAM</span><span class="sxs-lookup"><span data-stu-id="4ff7b-143">How to Configure Network Load Balancing for MBAM</span></span>](how-to-configure-network-load-balancing-for-mbam.md)

## <span data-ttu-id="4ff7b-144">Autres ressources pour le déploiement de fonctionnalités MBAM 1,0 Server</span><span class="sxs-lookup"><span data-stu-id="4ff7b-144">Other resources for MBAM 1.0 Server features deployment</span></span>


[<span data-ttu-id="4ff7b-145">Déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="4ff7b-145">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





