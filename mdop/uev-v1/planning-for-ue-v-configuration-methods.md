---
title: Planification de méthodes de configuration d'UE-V
description: Planification de méthodes de configuration d'UE-V
author: dansimp
ms.assetid: 57bce7ab-1be5-434b-9ee5-c96026bbe010
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4894644d72392ae984d0de290bf634e137d5b85e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812149"
---
# <span data-ttu-id="3a9ea-103">Planification de méthodes de configuration d'UE-V</span><span class="sxs-lookup"><span data-stu-id="3a9ea-103">Planning for UE-V Configuration Methods</span></span>


<span data-ttu-id="3a9ea-104">Les configurations Microsoft User Interface Virtualization (UE-V) déterminent la manière dont les paramètres sont synchronisés au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-104">Microsoft User Experience Virtualization (UE-V) configurations determine how settings are synchronized throughout the enterprise.</span></span> <span data-ttu-id="3a9ea-105">Cette rubrique décrit comment créer des configurations UE-V pour vous aider à formuler un plan de configuration qui correspond le mieux à vos besoins professionnels.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-105">This topic describes how UE-V configurations are created to help you formulate a configuration plan that best meets your business requirements.</span></span>

## <span data-ttu-id="3a9ea-106">Méthodes de configuration pour UE-V</span><span class="sxs-lookup"><span data-stu-id="3a9ea-106">Configuration methods for UE-V</span></span>


<span data-ttu-id="3a9ea-107">Vous pouvez configurer UE-V avant, pendant ou après l’installation de l’agent, en fonction de la méthode de configuration que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-107">You can configure UE-V before, during, or after agent installation, depending on the configuration method that you use.</span></span>

<span data-ttu-id="3a9ea-108">**Stratégie de groupe:** une infrastructure de stratégie de groupe existante peut être utilisée pour configurer UE-v avant ou après le déploiement de l’agent UE-v.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-108">**Group Policy:** existing Group Policy infrastructure can be used to configure UE-V before or after UE-V Agent deployment.</span></span> <span data-ttu-id="3a9ea-109">Le modèle ADMX-V pour la gestion centralisée des options de configuration de l’agent UE-V et il comprend des paramètres pour configurer la synchronisation d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-109">The UE-V ADMX template enables the central management of common UE-V Agent configuration options, and it includes settings to configure UE-V synchronization.</span></span> <span data-ttu-id="3a9ea-110">Les environnements réseau qui utilisent une stratégie de groupe peuvent préconfigurer UE-V en prévision du déploiement de l’agent.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-110">Network environments that use Group Policy can preconfigure UE-V in anticipation of agent deployment.</span></span>

[<span data-ttu-id="3a9ea-111">Configuration d’UE-V avec les objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="3a9ea-111">Configuring UE-V with Group Policy Objects</span></span>](configuring-ue-v-with-group-policy-objects.md)

[<span data-ttu-id="3a9ea-112">Installation des modèles ADMX de stratégie de groupe UE-V</span><span class="sxs-lookup"><span data-stu-id="3a9ea-112">Installing the UE-V Group Policy ADMX Templates</span></span>](installing-the-ue-v-group-policy-admx-templates.md)

<span data-ttu-id="3a9ea-113">**L’installation d’un script de ligne de commande ou de lot:** les paramètres qui sont utilisés avec le déploiement de l’agent UE-v permettent de configurer de nombreux paramètres d’UE-v.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-113">**Command-line or Batch Script Installation:** parameters that are used with the deployment of the UE-V Agent allow the configuration of many UE-V settings.</span></span> <span data-ttu-id="3a9ea-114">Dans les systèmes de distribution de logiciels électroniques tels que System Center Configuration Manager, utilisez ces paramètres pour configurer leurs clients lors du déploiement et de l’installation du logiciel d’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-114">Electronic software distribution systems, such as System Center Configuration Manager, use these parameters to configure their clients when deploying and installing the UE-V Agent software.</span></span> <span data-ttu-id="3a9ea-115">Pour obtenir la liste des paramètres d’installation et des exemples de script d’installation, voir [déploiement de l’agent UE-V](deploying-the-ue-v-agent.md).</span><span class="sxs-lookup"><span data-stu-id="3a9ea-115">For a list of installation parameters and sample installation scripts, see [Deploying the UE-V Agent](deploying-the-ue-v-agent.md).</span></span>

<span data-ttu-id="3a9ea-116">**PowerShell et WMI:** les commandes créées à l’aide de PowerShell ou WMI peuvent être utilisées pour modifier des configurations après l’installation d’UE-V agent.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-116">**PowerShell and WMI:** scripted commands using PowerShell or WMI can be used to modify configurations after the UE-V Agent has been installed.</span></span> <span data-ttu-id="3a9ea-117">Pour obtenir la liste des commandes PowerShell et WMI, voir [gestion de l’agent et des packages d’UE-V 1,0 avec PowerShell et WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="3a9ea-117">For a list of PowerShell and WMI commands, see [Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).</span></span>

<span data-ttu-id="3a9ea-118">**Modifier les paramètres du Registre:** Les paramètres d’UE-V sont stockés dans le registre et peuvent être modifiés à l’aide de n’importe quel outil permettant de modifier les paramètres du Registre, comme RegEdit.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-118">**Edit Registry Settings:** UE-V settings are stored in the registry and can be modified by using any tool that can modify registry settings, such as RegEdit.</span></span>

<span data-ttu-id="3a9ea-119">**Remarques**  La modification du Registre peut entraîner une perte de données ou l’ordinateur ne répond plus.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-119">**Note** Registry modification can result in data loss or the computer becoming unresponsive.</span></span> <span data-ttu-id="3a9ea-120">Nous vous recommandons d’utiliser d’autres méthodes de configuration.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-120">We recommend that you use other configuration methods.</span></span>

 

### <span data-ttu-id="3a9ea-121">Paramètres de configuration d’UE-V</span><span class="sxs-lookup"><span data-stu-id="3a9ea-121">UE-V configuration settings</span></span>

<span data-ttu-id="3a9ea-122">Vous trouverez ci-dessous des exemples de paramètres de configuration UE-V:</span><span class="sxs-lookup"><span data-stu-id="3a9ea-122">The following are examples of UE-V configuration settings:</span></span>

-   <span data-ttu-id="3a9ea-123">**Définition du chemin d’accès de stockage:** spécifie l’emplacement du partage de fichiers qui stocke les paramètres UE-V.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-123">**Setting Storage Path:** specifies the location of the file share that stores the UE-V settings.</span></span>

-   <span data-ttu-id="3a9ea-124">**Modèle de modèle de paramètres:** spécifie le chemin d’accès UNC (Universal Naming Convention) qui définit l’emplacement dans lequel les nouveaux modèles d’emplacement des paramètres sont consultés.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-124">**Settings Template Catalog Path:** specifies the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span>

-   <span data-ttu-id="3a9ea-125">**Enregistrer les modèles Microsoft:** indique si les modèles Microsoft par défaut doivent être inscrits lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-125">**Register Microsoft Templates:** specifies whether the default Microsoft templates should be registered during installation.</span></span>

-   <span data-ttu-id="3a9ea-126">**Méthode de synchronisation:** indique si la fonctionnalité fichiers en mode hors connexion de Windows est utilisée pour la prise en charge hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-126">**Synchronization Method:** specifies whether the Windows Offline Files feature is used for offline support.</span></span>

-   <span data-ttu-id="3a9ea-127">**Délai d’expiration de la synchronisation:** indique le nombre de millisecondes que l’ordinateur attend avant le délai d’expiration lors de la récupération des paramètres utilisateur à partir de l’emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-127">**Synchronization Timeout:** specifies the number of milliseconds that the computer waits before timeout when retrieving the user settings from the settings storage location.</span></span>

-   <span data-ttu-id="3a9ea-128">**Activation de la synchronisation:** indique si la synchronisation des paramètres d’UE-V est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-128">**Synchronization Enable:** specifies whether the UE-V settings synchronization is enabled or disabled.</span></span>

-   <span data-ttu-id="3a9ea-129">**Taille maximale du package:** spécifie une taille de seuil du fichier de package de paramètres en octets auxquelles l’agent UE-V signale une alerte.</span><span class="sxs-lookup"><span data-stu-id="3a9ea-129">**Maximum Package Size:** specifies a settings package file threshold size in bytes at which the UE-V Agent reports a warning.</span></span>

## <span data-ttu-id="3a9ea-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a9ea-130">Related topics</span></span>


[<span data-ttu-id="3a9ea-131">Planification pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="3a9ea-131">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="3a9ea-132">Planification de la configuration d'UE-V</span><span class="sxs-lookup"><span data-stu-id="3a9ea-132">Planning for UE-V Configuration</span></span>](planning-for-ue-v-configuration.md)

 

 





