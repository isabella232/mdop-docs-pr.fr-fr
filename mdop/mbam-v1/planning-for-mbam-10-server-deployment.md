---
title: Planification du déploiement de serveursMBAM1.0
description: Planification du déploiement de serveursMBAM1.0
author: dansimp
ms.assetid: 3cbef284-3092-4c42-9234-2826b18ddef1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 76ff9c444ce3f9c39161341610fb0cd9a763dc6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804219"
---
# <span data-ttu-id="c4bcf-103">Planification du déploiement de serveursMBAM1.0</span><span class="sxs-lookup"><span data-stu-id="c4bcf-103">Planning for MBAM 1.0 Server Deployment</span></span>


<span data-ttu-id="c4bcf-104">L’infrastructure du serveur d’administration et de surveillance de BitLocker (MBAM) Microsoft dépend d’un ensemble de fonctionnalités serveur qui peuvent être installées sur un ou plusieurs ordinateurs serveur, en fonction des besoins de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="c4bcf-104">The Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of your enterprise.</span></span>

## <span data-ttu-id="c4bcf-105">Planification du déploiement de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="c4bcf-105">Planning for MBAM Server deployment</span></span>


<span data-ttu-id="c4bcf-106">Les fonctionnalités MBAM suivantes représentent l’infrastructure serveur pour un déploiement de MBAM Server:</span><span class="sxs-lookup"><span data-stu-id="c4bcf-106">The following MBAM features represent the server infrastructure for an MBAM server deployment:</span></span>

-   <span data-ttu-id="c4bcf-107">Base de données de récupération et de matériel</span><span class="sxs-lookup"><span data-stu-id="c4bcf-107">Recovery and Hardware Database</span></span>

-   <span data-ttu-id="c4bcf-108">Base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="c4bcf-108">Compliance and Audit Database</span></span>

-   <span data-ttu-id="c4bcf-109">Rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="c4bcf-109">Compliance and Audit Reports</span></span>

-   <span data-ttu-id="c4bcf-110">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="c4bcf-110">Administration and Monitoring Server</span></span>

<span data-ttu-id="c4bcf-111">Les fonctionnalités et bases de données de MBAM Server peuvent être installées dans différentes configurations, en fonction de vos besoins en matière de modularité.</span><span class="sxs-lookup"><span data-stu-id="c4bcf-111">MBAM server databases and features can be installed in different configurations, depending on your scalability needs.</span></span> <span data-ttu-id="c4bcf-112">Toutes les fonctionnalités de MBAM Server peuvent être installées sur un serveur unique ou distribuées sur plusieurs serveurs.</span><span class="sxs-lookup"><span data-stu-id="c4bcf-112">All MBAM Server features can be installed on a single server or distributed across multiple servers.</span></span> <span data-ttu-id="c4bcf-113">En général, nous vous recommandons d’utiliser une configuration à trois ou cinq serveurs pour les environnements de production, même si les configurations de deux ou quatre serveurs peuvent également être utilisées, en fonction de vos besoins informatiques.</span><span class="sxs-lookup"><span data-stu-id="c4bcf-113">Generally, we recommend that you use a three-server or five-server configuration for production environments, although configurations of two or four servers can also be used, depending on your computing needs.</span></span>

<span data-ttu-id="c4bcf-114">**Remarques**  Pour plus d’informations sur l’évolutivité des performances des topologies de déploiement MBAM et recommandées, consultez le livre blanc sur l’évolutivité et la haute disponibilité du MBAM à l’adresse <https://go.microsoft.com/fwlink/p/?LinkId=258314> .</span><span class="sxs-lookup"><span data-stu-id="c4bcf-114">**Note** For more information about performance scalability of MBAM and recommended deployment topologies, see the MBAM Scalability and High-Availability Guide white paper at <https://go.microsoft.com/fwlink/p/?LinkId=258314>.</span></span>

 

<span data-ttu-id="c4bcf-115">Chaque fonctionnalité MBAM comporte des éléments requis spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c4bcf-115">Each MBAM feature has specific prerequisites.</span></span> <span data-ttu-id="c4bcf-116">Pour obtenir la liste complète des conditions préalables pour les fonctionnalités du serveur et la configuration matérielle et logicielle requise, voir Configuration requise pour le [déploiement d’MBAM 1,0](mbam-10-deployment-prerequisites.md) et [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="c4bcf-116">For a full list of server feature prerequisites and hardware and software requirements, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) and [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

<span data-ttu-id="c4bcf-117">Outre les fonctionnalités de MBAM liées au serveur, l’application de configuration du serveur inclut un modèle de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="c4bcf-117">In addition to the server-related MBAM features, the server Setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="c4bcf-118">Ce modèle peut être installé sur n’importe quel ordinateur qui peut exécuter la console de gestion des stratégies de groupe (GPMC) ou Advanced Group Policy Management (AGPM).</span><span class="sxs-lookup"><span data-stu-id="c4bcf-118">This template can be installed on any computer that is able to run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

## <span data-ttu-id="c4bcf-119">Ordre de déploiement des fonctionnalités du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="c4bcf-119">Order of deployment of MBAM Server Features</span></span>


<span data-ttu-id="c4bcf-120">Lorsque vous déployez les fonctionnalités du serveur MBAM, installez les fonctionnalités dans l’ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="c4bcf-120">When you deploy the MBAM Server features, install the features in the following order:</span></span>

1.  <span data-ttu-id="c4bcf-121">Base de données de récupération et de matériel</span><span class="sxs-lookup"><span data-stu-id="c4bcf-121">Recovery and Hardware Database</span></span>

2.  <span data-ttu-id="c4bcf-122">Base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="c4bcf-122">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="c4bcf-123">Rapports et audit de conformité</span><span class="sxs-lookup"><span data-stu-id="c4bcf-123">Compliance Audit and Reports</span></span>

4.  <span data-ttu-id="c4bcf-124">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="c4bcf-124">Administration and Monitoring Server</span></span>

5.  <span data-ttu-id="c4bcf-125">Modèle de stratégie</span><span class="sxs-lookup"><span data-stu-id="c4bcf-125">Policy Template</span></span>

<span data-ttu-id="c4bcf-126">**Remarques**  Assurez le suivi des noms des ordinateurs sur lesquels vous installez chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="c4bcf-126">**Note** Keep track of the names of the computers on which you install each feature.</span></span> <span data-ttu-id="c4bcf-127">Vous utiliserez ces informations tout au long du processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="c4bcf-127">You will use this information throughout the installation process.</span></span> <span data-ttu-id="c4bcf-128">Vous pouvez imprimer et utiliser une liste de vérification de déploiement pour vous aider dans le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="c4bcf-128">You can print and use a deployment checklist to assist you in the installation process.</span></span> <span data-ttu-id="c4bcf-129">Pour plus d’informations sur la liste de vérification de déploiement d’MBAM, voir [liste de vérification de déploiement 1,0 MBAM](mbam-10-deployment-checklist.md).</span><span class="sxs-lookup"><span data-stu-id="c4bcf-129">For more information about the MBAM deployment checklist, see [MBAM 1.0 Deployment Checklist](mbam-10-deployment-checklist.md).</span></span>

 

## <span data-ttu-id="c4bcf-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4bcf-130">Related topics</span></span>


[<span data-ttu-id="c4bcf-131">Planification du déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="c4bcf-131">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="c4bcf-132">Déploiement de l'infrastructure de serveur MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="c4bcf-132">Deploying the MBAM 1.0 Server Infrastructure</span></span>](deploying-the-mbam-10-server-infrastructure.md)

 

 





