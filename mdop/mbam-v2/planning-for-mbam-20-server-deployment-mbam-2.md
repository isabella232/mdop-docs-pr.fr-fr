---
title: Planification du déploiement de serveursMBAM2.0
description: Planification du déploiement de serveursMBAM2.0
author: dansimp
ms.assetid: b57f1a42-134f-4997-8697-7fbed08e2fc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57e6510556522dce029c958172bd89a361e06b83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804357"
---
# <span data-ttu-id="1b23d-103">Planification du déploiement de serveursMBAM2.0</span><span class="sxs-lookup"><span data-stu-id="1b23d-103">Planning for MBAM 2.0 Server Deployment</span></span>


<span data-ttu-id="1b23d-104">L’infrastructure du serveur d’administration et de surveillance de BitLocker (MBAM) Microsoft dépend d’un ensemble de fonctionnalités serveur qui peuvent être installées sur un ou plusieurs ordinateurs serveur, en fonction des besoins de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="1b23d-104">The Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="1b23d-105">Si vous installez l’administration et la surveillance de BitLocker avec la topologie de Configuration Manager, consultez [planification du déploiement d’MBAM avec Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="1b23d-105">If you are installing Microsoft BitLocker Administration and Monitoring with the Configuration Manager topology, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="1b23d-106">**Remarques**  Les installations de l’administration et de l’analyse de BitLocker sur un seul serveur sont recommandées uniquement pour les environnements de test.</span><span class="sxs-lookup"><span data-stu-id="1b23d-106">**Note** Installations of Microsoft BitLocker Administration and Monitoring on a single server are recommended only for test environments.</span></span>

 

## <span data-ttu-id="1b23d-107">Planification du déploiement de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="1b23d-107">Planning for MBAM Server Deployment</span></span>


<span data-ttu-id="1b23d-108">L’infrastructure d’un déploiement MBAM Server inclut les fonctionnalités suivantes:</span><span class="sxs-lookup"><span data-stu-id="1b23d-108">The infrastructure for an MBAM Server deployment includes the following features:</span></span>

-   <span data-ttu-id="1b23d-109">Base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="1b23d-109">Recovery Database</span></span>

-   <span data-ttu-id="1b23d-110">Base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="1b23d-110">Compliance and Audit Database</span></span>

-   <span data-ttu-id="1b23d-111">Rapports de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="1b23d-111">Compliance and Audit Reports</span></span>

-   <span data-ttu-id="1b23d-112">Portail libre-service</span><span class="sxs-lookup"><span data-stu-id="1b23d-112">Self-Service Portal</span></span>

-   <span data-ttu-id="1b23d-113">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="1b23d-113">Administration and Monitoring Server</span></span>

-   <span data-ttu-id="1b23d-114">Modèle de stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="1b23d-114">MBAM Group Policy Template</span></span>

<span data-ttu-id="1b23d-115">Les fonctionnalités et bases de données de MBAM Server peuvent être installées dans différentes configurations, en fonction de vos besoins en matière de modularité.</span><span class="sxs-lookup"><span data-stu-id="1b23d-115">MBAM Server databases and features can be installed in different configurations, depending on your scalability requirements.</span></span> <span data-ttu-id="1b23d-116">Toutes les fonctionnalités de MBAM Server peuvent être installées sur un serveur unique ou distribuées sur plusieurs serveurs.</span><span class="sxs-lookup"><span data-stu-id="1b23d-116">All MBAM Server features can be installed on a single server or distributed across multiple servers.</span></span> <span data-ttu-id="1b23d-117">Nous vous recommandons d’utiliser une configuration à deux serveurs pour les environnements de production, même si les configurations de 2 à 4 serveurs peuvent également être utilisées, en fonction de vos besoins informatiques.</span><span class="sxs-lookup"><span data-stu-id="1b23d-117">We recommend that you use a two-server configuration for production environments, although configurations of two to four servers can also be used, depending on your computing requirements.</span></span>

<span data-ttu-id="1b23d-118">Chaque fonctionnalité MBAM comporte des éléments requis spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1b23d-118">Each MBAM feature has specific prerequisites.</span></span> <span data-ttu-id="1b23d-119">Pour obtenir la liste complète des conditions préalables pour les fonctionnalités du serveur et la configuration matérielle et logicielle requise, voir Configuration requise pour le [déploiement d’MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md) et [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="1b23d-119">For a full list of server feature prerequisites and hardware and software requirements, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) and [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md).</span></span>

<span data-ttu-id="1b23d-120">Outre les fonctionnalités de MBAM liées au serveur, l’application de configuration du serveur inclut un modèle de stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="1b23d-120">In addition to the server-related MBAM features, the Server Setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="1b23d-121">Le modèle contient des paramètres d’objets de stratégie de groupe que vous configurez pour gérer le chiffrement de lecteur BitLocker au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="1b23d-121">The template contains Group Policy Object (GPO) settings that you configure to manage BitLocker Drive Encryption in the enterprise.</span></span> <span data-ttu-id="1b23d-122">Vous pouvez installer ce modèle sur n’importe quel ordinateur qui peut exécuter la console de gestion des stratégies de groupe (GPMC) ou Advanced Group Policy Management (AGPM).</span><span class="sxs-lookup"><span data-stu-id="1b23d-122">You can install this template on any computer that can run the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="1b23d-123">Lorsque vous planifiez le déploiement du serveur MBAM, envisagez d’utiliser des clés de récupération BitLocker dans MBAM pour une utilisation unique, après avoir expiré les clés de récupération.</span><span class="sxs-lookup"><span data-stu-id="1b23d-123">As you plan the MBAM Server deployment, consider that BitLocker recovery keys in MBAM are intended for single use only, after which recovery keys expire.</span></span> <span data-ttu-id="1b23d-124">Pour que les clés expirent après utilisation, elles doivent être récupérées par le biais du portail du support technique ou du portail libre-service.</span><span class="sxs-lookup"><span data-stu-id="1b23d-124">In order for the keys to expire after use, they must be retrieved through the Help Desk Portal or the Self-Service Portal.</span></span>

## <span data-ttu-id="1b23d-125">Ordre de déploiement des fonctionnalités du serveur MBAM</span><span class="sxs-lookup"><span data-stu-id="1b23d-125">Order of Deployment of MBAM Server Features</span></span>


<span data-ttu-id="1b23d-126">Pour déployer les fonctionnalités MBAM sur plusieurs serveurs, vous devez installer les fonctionnalités dans l’ordre suivant:</span><span class="sxs-lookup"><span data-stu-id="1b23d-126">To deploy MBAM features on multiple servers, you have to install the features in the following order:</span></span>

1.  <span data-ttu-id="1b23d-127">Base de données de récupération</span><span class="sxs-lookup"><span data-stu-id="1b23d-127">Recovery Database</span></span>

2.  <span data-ttu-id="1b23d-128">Base de données d’audit et de conformité</span><span class="sxs-lookup"><span data-stu-id="1b23d-128">Compliance and Audit Database</span></span>

3.  <span data-ttu-id="1b23d-129">Rapports et audit de conformité</span><span class="sxs-lookup"><span data-stu-id="1b23d-129">Compliance Audit and Reports</span></span>

4.  <span data-ttu-id="1b23d-130">Portail libre-service</span><span class="sxs-lookup"><span data-stu-id="1b23d-130">Self-Service Portal</span></span>

5.  <span data-ttu-id="1b23d-131">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="1b23d-131">Administration and Monitoring Server</span></span>

6.  <span data-ttu-id="1b23d-132">Modèle de stratégie de groupe MBAM</span><span class="sxs-lookup"><span data-stu-id="1b23d-132">MBAM Group Policy Template</span></span>

<span data-ttu-id="1b23d-133">**Remarques**  Assurez le suivi des noms des ordinateurs sur lesquels vous installez chaque fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1b23d-133">**Note** Keep track of the names of the computers on which you install each feature.</span></span> <span data-ttu-id="1b23d-134">Vous devez utiliser ces informations tout au long du processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="1b23d-134">You have to use this information throughout the installation process.</span></span> <span data-ttu-id="1b23d-135">Vous pouvez imprimer et utiliser une liste de vérification de déploiement pour faciliter la tâche.</span><span class="sxs-lookup"><span data-stu-id="1b23d-135">You can print and use a deployment checklist to assist in this effort.</span></span> <span data-ttu-id="1b23d-136">Pour plus d’informations sur la liste de vérification de déploiement d’MBAM, voir [liste de vérification de déploiement 2,0 MBAM](mbam-20-deployment-checklist-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="1b23d-136">For more information about the MBAM Deployment Checklist, see [MBAM 2.0 Deployment Checklist](mbam-20-deployment-checklist-mbam-2.md).</span></span>

 

## <span data-ttu-id="1b23d-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1b23d-137">Related topics</span></span>


[<span data-ttu-id="1b23d-138">Planification du déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="1b23d-138">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="1b23d-139">Déploiement de l'infrastructure de serveur MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="1b23d-139">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





