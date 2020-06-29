---
title: Déploiement de MBAM1.0 Language Release Update
description: Déploiement de MBAM1.0 Language Release Update
author: dansimp
ms.assetid: 9dbd85c3-e470-4752-a90f-25754dd46dab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a819be81594efd9349e3f6c0f6559c2b810bdc9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804518"
---
# <span data-ttu-id="fa067-103">Déploiement de MBAM1.0 Language Release Update</span><span class="sxs-lookup"><span data-stu-id="fa067-103">Deploying the MBAM 1.0 Language Release Update</span></span>


<span data-ttu-id="fa067-104">La version linguistique de Microsoft BitLocker Analysis and Monitoring (MBAM) 1.0 est une mise à jour de MBAM et inclut la prise en charge de nouvelles langues.</span><span class="sxs-lookup"><span data-stu-id="fa067-104">Microsoft BitLocker Administration and Monitoring (MBAM)1.0 Language Release is an update to MBAM and includes the support of new languages.</span></span> <span data-ttu-id="fa067-105">Les nouvelles langues sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="fa067-105">The new languages are:</span></span>

-   <span data-ttu-id="fa067-106">Anglais (fr-fr)</span><span class="sxs-lookup"><span data-stu-id="fa067-106">English (en-us)</span></span>

-   <span data-ttu-id="fa067-107">Français (fr)</span><span class="sxs-lookup"><span data-stu-id="fa067-107">French (fr)</span></span>

-   <span data-ttu-id="fa067-108">Italien (IT)</span><span class="sxs-lookup"><span data-stu-id="fa067-108">Italian (it)</span></span>

-   <span data-ttu-id="fa067-109">Allemand (de)</span><span class="sxs-lookup"><span data-stu-id="fa067-109">German (de)</span></span>

-   <span data-ttu-id="fa067-110">Espagnol (es)</span><span class="sxs-lookup"><span data-stu-id="fa067-110">Spanish (es)</span></span>

-   <span data-ttu-id="fa067-111">Coréen (Ko)</span><span class="sxs-lookup"><span data-stu-id="fa067-111">Korean (ko)</span></span>

-   <span data-ttu-id="fa067-112">Japonais (ja)</span><span class="sxs-lookup"><span data-stu-id="fa067-112">Japanese (ja)</span></span>

-   <span data-ttu-id="fa067-113">Portugais (Brésil)</span><span class="sxs-lookup"><span data-stu-id="fa067-113">Brazilian Portuguese (pt-br)</span></span>

-   <span data-ttu-id="fa067-114">Russe (RU)</span><span class="sxs-lookup"><span data-stu-id="fa067-114">Russian (ru)</span></span>

-   <span data-ttu-id="fa067-115">Chinois traditionnel (zh-TW)</span><span class="sxs-lookup"><span data-stu-id="fa067-115">Chinese Traditional (zh-tw)</span></span>

-   <span data-ttu-id="fa067-116">Chinois simplifié (zh-NC)</span><span class="sxs-lookup"><span data-stu-id="fa067-116">Chinese Simplified (zh-cn)</span></span>

<span data-ttu-id="fa067-117">La mise à jour du langage MBAM 1.0 va changer le numéro de version de MBAM 1.0.1237.1 à MBAM 1.0.2001.</span><span class="sxs-lookup"><span data-stu-id="fa067-117">The MBAM1.0 language update will change the version number from MBAM 1.0.1237.1 to MBAM 1.0.2001.</span></span>

<span data-ttu-id="fa067-118">Vous n’avez pas besoin de réinstaller toutes les fonctionnalités MBAM pour ajouter ces langues supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="fa067-118">You do not need to reinstall all of the MBAM features in order to add these additional languages.</span></span> <span data-ttu-id="fa067-119">Cette rubrique définit les étapes nécessaires à l’ajout de nouvelles langues prises en charge.</span><span class="sxs-lookup"><span data-stu-id="fa067-119">This topic defines the steps required to add the newly supported languages.</span></span>

## <span data-ttu-id="fa067-120">Déploiement de la version internationale de MBAM sur les fonctionnalités de MBAM Server</span><span class="sxs-lookup"><span data-stu-id="fa067-120">Deploy the MBAM international release to MBAM Server features</span></span>


<span data-ttu-id="fa067-121">Pour commencer, vous devez mettre à jour les fonctionnalités suivantes du serveur MBAM:</span><span class="sxs-lookup"><span data-stu-id="fa067-121">To begin, you must update the following MBAM server features:</span></span>

-   <span data-ttu-id="fa067-122">Rapport de conformité et d’audit</span><span class="sxs-lookup"><span data-stu-id="fa067-122">Compliance and Audit Report</span></span>

-   <span data-ttu-id="fa067-123">Serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="fa067-123">Administration and Monitoring Server</span></span>

-   <span data-ttu-id="fa067-124">Modèles de stratégie</span><span class="sxs-lookup"><span data-stu-id="fa067-124">Policy Templates</span></span>

<span data-ttu-id="fa067-125">Ensuite, vous devez exécuter **MbamSetup.exe** pour mettre à niveau les fonctionnalités MBAM qui s’exécutent sur le même serveur en même temps.</span><span class="sxs-lookup"><span data-stu-id="fa067-125">Then, you must run **MbamSetup.exe** to upgrade the MBAM features that run on the same server at the same time.</span></span>

[<span data-ttu-id="fa067-126">Installation de MBAM Language Update sur un serveur unique</span><span class="sxs-lookup"><span data-stu-id="fa067-126">How to Install the MBAM Language Update on a Single Server</span></span>](how-to-install-the-mbam-language-update-on-a-single-server-mbam-1.md)

[<span data-ttu-id="fa067-127">Installation de MBAM Language Update sur des serveurs distribués</span><span class="sxs-lookup"><span data-stu-id="fa067-127">How to Install the MBAM Language Update on Distributed Servers</span></span>](how-to-install-the-mbam-language-update-on-distributed-servers-mbam-1.md)

## <span data-ttu-id="fa067-128">Installer la mise à jour de langue MBAM pour les stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="fa067-128">Install the MBAM language update for Group Policies</span></span>


<span data-ttu-id="fa067-129">Les modèles de stratégie de groupe MBAM peuvent être installés sur chaque station de travail de gestion ou copiés sur le magasin central de stratégies de groupe, afin de rendre les modèles accessibles aux administrateurs de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="fa067-129">The MBAM Group Policy templates can be installed on each management workstation or they can be copied to the Group Policy central store, in order to make the templates available to all Group Policy administrators.</span></span> <span data-ttu-id="fa067-130">Les modèles de stratégie ne peuvent pas être installés directement sur un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="fa067-130">The policy templates cannot be directly installed on a domain controller.</span></span> <span data-ttu-id="fa067-131">Si vous n’utilisez pas un magasin central de stratégies de groupe, vous devez les copier manuellement vers chaque contrôleur de domaine qui gère la stratégie de groupe MBAM.</span><span class="sxs-lookup"><span data-stu-id="fa067-131">If you do not use a Group Policy central store, then you must copy the policies manually to each domain controller that manages MBAM Group Policy.</span></span>

<span data-ttu-id="fa067-132">Pour ajouter les modèles de stratégies de langue de MBAM, copiez les fichiers de langue de stratégie de groupe à partir de%SystemRoot%\\PolicyDefinitions sur l’ordinateur sur lequel le rôle «modèles de stratégie» a été installé au même emplacement sur l’ordinateur de poste de travail.</span><span class="sxs-lookup"><span data-stu-id="fa067-132">To add the MBAM language policies templates, copy the Group Policy language files from %SystemRoot%\\PolicyDefinitions on the computer where the “Policy Templates” role was installed to the same location on the workstation computer.</span></span> <span data-ttu-id="fa067-133">Voici quelques exemples de fichiers de stratégie de groupe:</span><span class="sxs-lookup"><span data-stu-id="fa067-133">Here are some examples of Group Policy files:</span></span>

-   <span data-ttu-id="fa067-134">BitLockerManagement. admx</span><span class="sxs-lookup"><span data-stu-id="fa067-134">BitLockerManagement.admx</span></span>

-   <span data-ttu-id="fa067-135">BitLockerUserManagement. admx</span><span class="sxs-lookup"><span data-stu-id="fa067-135">BitLockerUserManagement.admx</span></span>

-   <span data-ttu-id="fa067-136">en-us\\BitLockerManagement.adml</span><span class="sxs-lookup"><span data-stu-id="fa067-136">en-us\\BitLockerManagement.adml</span></span>

-   <span data-ttu-id="fa067-137">en-us\\BitLockerUserManagement.adml</span><span class="sxs-lookup"><span data-stu-id="fa067-137">en-us\\BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="fa067-138">fr-fr\\ BitLockerManagement. adml</span><span class="sxs-lookup"><span data-stu-id="fa067-138">fr-fr\\ BitLockerManagement.adml</span></span>

-   <span data-ttu-id="fa067-139">fr-fr\\ BitLockerUserManagement. adml</span><span class="sxs-lookup"><span data-stu-id="fa067-139">fr-fr\\ BitLockerUserManagement.adml</span></span>

-   <span data-ttu-id="fa067-140">(et de la même manière pour chaque langue prise en charge)</span><span class="sxs-lookup"><span data-stu-id="fa067-140">(and similarly for each supported language)</span></span>

## <span data-ttu-id="fa067-141">Problèmes connus dans la version internationale de MBAM</span><span class="sxs-lookup"><span data-stu-id="fa067-141">Known issues in the MBAM international release</span></span>


<span data-ttu-id="fa067-142">Cette rubrique décrit les problèmes connus liés à l’administration de Microsoft BitLocker et à l’analyse internationale.</span><span class="sxs-lookup"><span data-stu-id="fa067-142">This topic contains known issues for Microsoft BitLocker Administration and Monitoring International Release.</span></span>

[<span data-ttu-id="fa067-143">Problèmes connus dans MBAM International Release</span><span class="sxs-lookup"><span data-stu-id="fa067-143">Known Issues in the MBAM International Release</span></span>](known-issues-in-the-mbam-international-release-mbam-1.md)

## <span data-ttu-id="fa067-144">Autres ressources pour le déploiement de la mise à jour de langue de MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="fa067-144">Other resources for deploying the MBAM 1.0 Language Update</span></span>


[<span data-ttu-id="fa067-145">Déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="fa067-145">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

 

 





