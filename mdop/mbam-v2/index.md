---
title: Guide d’administration et d’administration de Microsoft BitLocker 2
description: Guide d’administration et d’administration de Microsoft BitLocker 2
author: dansimp
ms.assetid: fdb43f62-960a-4811-8802-50efdf04b4af
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: dd6deb6fb91c64ac8609b54114e0dd417497034a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795535"
---
# <span data-ttu-id="28a05-103">Guide d’administration et d’administration de Microsoft BitLocker 2</span><span class="sxs-lookup"><span data-stu-id="28a05-103">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>

<span data-ttu-id="28a05-104">Microsoft BitLockerAdministration et surveillance (MBAM) 2.0 fournit une interface d’administration simplifiée que vous pouvez utiliser pour gérer le chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="28a05-104">Microsoft BitLockerAdministration and Monitoring(MBAM)2.0 provides a simplified administrative interface that you can use to manage BitLocker drive encryption.</span></span> <span data-ttu-id="28a05-105">Dans BitLockerAdministration et surveillance 2.0, vous pouvez sélectionner les options de stratégie de chiffrement de lecteur BitLocker appropriées pour votre entreprise, puis les utiliser pour contrôler la conformité du client avec ces stratégies.</span><span class="sxs-lookup"><span data-stu-id="28a05-105">In BitLockerAdministration and Monitoring2.0, you can select BitLocker drive encryption policy options that are appropriate for your enterprise, and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="28a05-106">Vous pouvez également créer des rapports sur l’état de cryptage d’un ordinateur individuel et de l’ensemble de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="28a05-106">You can also report on the encryption status of an individual computer and on the enterprise as a whole.</span></span> <span data-ttu-id="28a05-107">De plus, vous pouvez accéder aux informations de clé de récupération lorsque les utilisateurs oublient leur code confidentiel ou leur mot de passe, ou lorsque leur enregistrement de BIOS ou de démarrage est modifié.</span><span class="sxs-lookup"><span data-stu-id="28a05-107">In addition, you can access recovery key information when users forget their PIN or password or when their BIOS or boot record changes.</span></span>

## <span data-ttu-id="28a05-108">Souligner</span><span class="sxs-lookup"><span data-stu-id="28a05-108">Outline</span></span>

- [<span data-ttu-id="28a05-109">Prise en main de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-109">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)
  - [<span data-ttu-id="28a05-110">À propos de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-110">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)
  - [<span data-ttu-id="28a05-111">Notes de publication de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-111">Release Notes for MBAM 2.0</span></span>](release-notes-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="28a05-112">À propos de MBAM2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="28a05-112">About MBAM 2.0 SP1</span></span>](about-mbam-20-sp1.md)
  - [<span data-ttu-id="28a05-113">Notes de publication de MBAM2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="28a05-113">Release Notes for MBAM 2.0 SP1</span></span>](release-notes-for-mbam-20-sp1.md)
  - [<span data-ttu-id="28a05-114">Évaluation de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-114">Evaluating MBAM 2.0</span></span>](evaluating-mbam-20-mbam-2.md)
  - [<span data-ttu-id="28a05-115">Architecture de hautniveau pour MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-115">High-Level Architecture for MBAM 2.0</span></span>](high-level-architecture-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="28a05-116">Accessibilité de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-116">Accessibility for MBAM 2.0</span></span>](accessibility-for-mbam-20-mbam-2.md)
- [<span data-ttu-id="28a05-117">Planification de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-117">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="28a05-118">Préparation de votre environnement pour MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-118">Preparing your Environment for MBAM 2.0</span></span>](preparing-your-environment-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="28a05-119">Conditions préalables au déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-119">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)
  - [<span data-ttu-id="28a05-120">Planification du déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-120">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)
  - [<span data-ttu-id="28a05-121">Configurations prises en charge par MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-121">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)
  - [<span data-ttu-id="28a05-122">Liste de contrôle de la planification de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-122">MBAM 2.0 Planning Checklist</span></span>](mbam-20-planning-checklist-mbam-2.md)
- [<span data-ttu-id="28a05-123">Déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-123">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)
  - [<span data-ttu-id="28a05-124">Déploiement de l'infrastructure de serveur MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-124">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)
  - [<span data-ttu-id="28a05-125">Déploiement d'objets de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-125">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)
  - [<span data-ttu-id="28a05-126">Déploiement du client MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-126">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)
  - [<span data-ttu-id="28a05-127">Liste de contrôle du déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-127">MBAM 2.0 Deployment Checklist</span></span>](mbam-20-deployment-checklist-mbam-2.md)
  - [<span data-ttu-id="28a05-128">Mise à niveau des versions précédentes de MBAM</span><span class="sxs-lookup"><span data-stu-id="28a05-128">Upgrading from Previous Versions of MBAM</span></span>](upgrading-from-previous-versions-of-mbam.md)
- [<span data-ttu-id="28a05-129">Opérations de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-129">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="28a05-130">Utilisation de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="28a05-130">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)
  - [<span data-ttu-id="28a05-131">Administration des composants de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-131">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)
  - [<span data-ttu-id="28a05-132">Surveillance et création de rapports de la conformité BitLocker avec MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-132">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)
  - [<span data-ttu-id="28a05-133">Gestion de BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="28a05-133">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)
  - [<span data-ttu-id="28a05-134">Gestion de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-134">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)
  - [<span data-ttu-id="28a05-135">Sécurité et confidentialité de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-135">Security and Privacy for MBAM 2.0</span></span>](security-and-privacy-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="28a05-136">Administration de MBAM2.0 à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="28a05-136">Administering MBAM 2.0 Using PowerShell</span></span>](administering-mbam-20-using-powershell-mbam-2.md)
- [<span data-ttu-id="28a05-137">Résolution des problèmes de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="28a05-137">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

## <span data-ttu-id="28a05-138">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="28a05-138">More Information</span></span>

- [<span data-ttu-id="28a05-139">Découverte des informations de MDOP</span><span class="sxs-lookup"><span data-stu-id="28a05-139">MDOP Information Experience</span></span>](index.md)

  <span data-ttu-id="28a05-140">Recherchez des documents, des vidéos et d’autres ressources pour MDOP technologies.</span><span class="sxs-lookup"><span data-stu-id="28a05-140">Find documentation, videos, and other resources for MDOP technologies.</span></span>

 

 





