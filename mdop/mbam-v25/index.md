---
title: Microsoft BitLocker Administration and Monitoring2.5
description: Microsoft BitLocker Administration and Monitoring2.5
author: dansimp
ms.assetid: fd81d7de-b166-47e8-b6c7-d984830762b6
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 2e5243131853207f0ed3cbb6d0cd8fb8e3d56108
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795507"
---
# <span data-ttu-id="ca8b8-103">Microsoft BitLocker Administration and Monitoring2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-103">Microsoft BitLocker Administration and Monitoring 2.5</span></span>

<span data-ttu-id="ca8b8-104">L’outil d’administration et de surveillance de BitLocker (MBAM 2,5) de Microsoft fournit une interface d’administration simplifiée que vous pouvez utiliser pour gérer le chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="ca8b8-104">Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 provides a simplified administrative interface that you can use to manage BitLocker Drive Encryption.</span></span> <span data-ttu-id="ca8b8-105">Vous pouvez configurer des modèles de stratégie de groupe MBAM qui vous permettent de définir des options de stratégie de chiffrement de lecteur BitLocker appropriées pour votre entreprise, puis de les utiliser pour contrôler la conformité du client avec ces stratégies.</span><span class="sxs-lookup"><span data-stu-id="ca8b8-105">You configure MBAM Group Policy Templates that enable you to set BitLocker Drive Encryption policy options that are appropriate for your enterprise, and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="ca8b8-106">Vous pouvez également créer des rapports sur l’état de cryptage d’un ordinateur individuel et de l’ensemble de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ca8b8-106">You can also report on the encryption status of an individual computer and on the enterprise as a whole.</span></span> <span data-ttu-id="ca8b8-107">De plus, vous pouvez accéder aux informations de clé de récupération lorsque les utilisateurs oublient leur code confidentiel ou leur mot de passe, ou lorsque leur enregistrement de BIOS ou de démarrage est modifié.</span><span class="sxs-lookup"><span data-stu-id="ca8b8-107">In addition, you can access recovery key information when users forget their PIN or password or when their BIOS or boot record changes.</span></span> <span data-ttu-id="ca8b8-108">Pour une description plus détaillée de MBAM, voir [à propos de MBAM 2,5](about-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="ca8b8-108">For a more detailed description of MBAM, see [About MBAM 2.5](about-mbam-25.md).</span></span>

<span data-ttu-id="ca8b8-109">Pour obtenir MBAM, reportez-vous à [la rubrique Comment obtenir MDOP](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop).</span><span class="sxs-lookup"><span data-stu-id="ca8b8-109">To obtain MBAM, see [How Do I Get MDOP](https://docs.microsoft.com/microsoft-desktop-optimization-pack/index#how-to-get-mdop).</span></span>

## <span data-ttu-id="ca8b8-110">Souligner</span><span class="sxs-lookup"><span data-stu-id="ca8b8-110">Outline</span></span>

- <a href="" id="getting-started-with-mbam-2-5"></a>[<span data-ttu-id="ca8b8-111">Prise en main de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-111">Getting Started with MBAM 2.5</span></span>](getting-started-with-mbam-25.md)
  - [<span data-ttu-id="ca8b8-112">À propos de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-112">About MBAM 2.5</span></span>](about-mbam-25.md)
  - [<span data-ttu-id="ca8b8-113">Notes de publication de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-113">Release Notes for MBAM 2.5</span></span>](release-notes-for-mbam-25.md)
  - [<span data-ttu-id="ca8b8-114">À propos de MBAM2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="ca8b8-114">About MBAM 2.5 SP1</span></span>](about-mbam-25-sp1.md)
  - [<span data-ttu-id="ca8b8-115">Notes de publication de MBAM2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="ca8b8-115">Release Notes for MBAM 2.5 SP1</span></span>](release-notes-for-mbam-25-sp1.md)
  - [<span data-ttu-id="ca8b8-116">Évaluation de MBAM2.5 dans un environnement de test</span><span class="sxs-lookup"><span data-stu-id="ca8b8-116">Evaluating MBAM 2.5 in a Test Environment</span></span>](evaluating-mbam-25-in-a-test-environment.md)
  - [<span data-ttu-id="ca8b8-117">Architecture de hautniveau pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-117">High-Level Architecture for MBAM 2.5</span></span>](high-level-architecture-for-mbam-25.md)
  - [<span data-ttu-id="ca8b8-118">Accessibilité de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-118">Accessibility for MBAM 2.5</span></span>](accessibility-for-mbam-25.md)
- <a href="" id="planning-for-mbam-2-5"></a>[<span data-ttu-id="ca8b8-119">Planification de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-119">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)
  - [<span data-ttu-id="ca8b8-120">Préparation de votre environnement pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-120">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)
  - [<span data-ttu-id="ca8b8-121">Conditions préalables au déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-121">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)
  - [<span data-ttu-id="ca8b8-122">Planification des exigences en matière de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-122">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)
  - [<span data-ttu-id="ca8b8-123">Planification des comptes et groupes MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-123">Planning for MBAM 2.5 Groups and Accounts</span></span>](planning-for-mbam-25-groups-and-accounts.md)
  - [<span data-ttu-id="ca8b8-124">Planification de la sécurisation des sites web MBAM</span><span class="sxs-lookup"><span data-stu-id="ca8b8-124">Planning How to Secure the MBAM Websites</span></span>](planning-how-to-secure-the-mbam-websites.md)
  - [<span data-ttu-id="ca8b8-125">Planification du déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-125">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)
  - [<span data-ttu-id="ca8b8-126">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-126">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)
  - [<span data-ttu-id="ca8b8-127">Planification de la haute disponibilité de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-127">Planning for MBAM 2.5 High Availability</span></span>](planning-for-mbam-25-high-availability.md)
  - [<span data-ttu-id="ca8b8-128">Considérations relatives à la sécurité pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-128">MBAM 2.5 Security Considerations</span></span>](mbam-25-security-considerations.md)
  - [<span data-ttu-id="ca8b8-129">Liste de contrôle de la planification de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-129">MBAM 2.5 Planning Checklist</span></span>](mbam-25-planning-checklist.md)
- <a href="" id="deploying-mbam-2-5"></a>[<span data-ttu-id="ca8b8-130">Déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-130">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)
  - [<span data-ttu-id="ca8b8-131">Déploiement de l'infrastructure de serveur MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-131">Deploying the MBAM 2.5 Server Infrastructure</span></span>](deploying-the-mbam-25-server-infrastructure.md)
  - [<span data-ttu-id="ca8b8-132">Déploiement d'objets de stratégie de groupe MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-132">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)
  - [<span data-ttu-id="ca8b8-133">Déploiement du client MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-133">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)
  - [<span data-ttu-id="ca8b8-134">Liste de contrôle du déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-134">MBAM 2.5 Deployment Checklist</span></span>](mbam-25-deployment-checklist.md)
  - [<span data-ttu-id="ca8b8-135">Mise à niveau vers MBAM2.5 ou MBAM2.5 SP1 àpartir de versions antérieures</span><span class="sxs-lookup"><span data-stu-id="ca8b8-135">Upgrading to MBAM 2.5 or MBAM 2.5 SP1 from Previous Versions</span></span>](upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions.md)
  - [<span data-ttu-id="ca8b8-136">Suppression du logiciel ou des composants serveur de MBAM</span><span class="sxs-lookup"><span data-stu-id="ca8b8-136">Removing MBAM Server Features or Software</span></span>](removing-mbam-server-features-or-software.md)
- <a href="" id="operations-for-mbam-2-5"></a>[<span data-ttu-id="ca8b8-137">Opérations de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-137">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)
  - [<span data-ttu-id="ca8b8-138">Administration des composants de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-138">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)
  - [<span data-ttu-id="ca8b8-139">Surveillance et création de rapports de la conformité BitLocker avec MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-139">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)
  - [<span data-ttu-id="ca8b8-140">Gestion de BitLocker avec MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-140">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)
  - [<span data-ttu-id="ca8b8-141">Gestion de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-141">Maintaining MBAM 2.5</span></span>](maintaining-mbam-25.md)
  - [<span data-ttu-id="ca8b8-142">Utilisation de Windows PowerShell pour administrer MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-142">Using Windows PowerShell to Administer MBAM 2.5</span></span>](using-windows-powershell-to-administer-mbam-25.md)
- <a href="" id="troubleshooting-mbam-2-5"></a>[<span data-ttu-id="ca8b8-143">Résolution des problèmes MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-143">Troubleshooting MBAM 2.5</span></span>](troubleshooting-mbam-25.md)
- <a href="" id="technical-reference-for-mbam-2-5"></a>[<span data-ttu-id="ca8b8-144">Document de référence technique pour MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="ca8b8-144">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)
  - [<span data-ttu-id="ca8b8-145">Journaux des événements clients</span><span class="sxs-lookup"><span data-stu-id="ca8b8-145">Client Event Logs</span></span>](client-event-logs.md)
  - [<span data-ttu-id="ca8b8-146">Journaux des événements serveur</span><span class="sxs-lookup"><span data-stu-id="ca8b8-146">Server Event Logs</span></span>](server-event-logs.md)

## <span data-ttu-id="ca8b8-147">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="ca8b8-147">More Information</span></span>

- [<span data-ttu-id="ca8b8-148">Découverte des informations de MDOP</span><span class="sxs-lookup"><span data-stu-id="ca8b8-148">MDOP Information Experience</span></span>](index.md)

  <span data-ttu-id="ca8b8-149">Recherchez des documents, des vidéos et d’autres ressources pour MDOP technologies.</span><span class="sxs-lookup"><span data-stu-id="ca8b8-149">Find documentation, videos, and other resources for MDOP technologies.</span></span>

- [<span data-ttu-id="ca8b8-150">Guide de déploiement MBAM</span><span class="sxs-lookup"><span data-stu-id="ca8b8-150">MBAM Deployment Guide</span></span>](https://www.microsoft.com/download/details.aspx?id=38398)

  <span data-ttu-id="ca8b8-151">Obtenez de l’aide pour choisir une méthode de déploiement pour MBAM, y compris des instructions pas à pas pour chaque méthode.</span><span class="sxs-lookup"><span data-stu-id="ca8b8-151">Get help in choosing a deployment method for MBAM, including step-by-step instructions for each method.</span></span>
    
- [<span data-ttu-id="ca8b8-152">Appliquer des correctifs sur MBAM 2,5 SP1 Server</span><span class="sxs-lookup"><span data-stu-id="ca8b8-152">Apply Hotfixes on MBAM 2.5 SP1 Server</span></span>](apply-hotfix-for-mbam-25-sp1.md)

  <span data-ttu-id="ca8b8-153">Guide illustrant l’application des correctifs du serveur MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="ca8b8-153">Guide of how to apply MBAM 2.5 SP1 Server hotfixes</span></span>
