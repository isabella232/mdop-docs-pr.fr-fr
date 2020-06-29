---
title: Déploiement d'UE-V1.0
description: Déploiement d'UE-V1.0
author: dansimp
ms.assetid: 519598bb-8c81-4af7-bee7-357696bff880
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a1c515f9be950d8ca7b0a199344d34f7852073d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812180"
---
# <span data-ttu-id="b2bdd-103">Déploiement d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="b2bdd-103">Deploying UE-V 1.0</span></span>


<span data-ttu-id="b2bdd-104">Il existe diverses configurations de déploiement prises en charge par Microsoft User User Virtualization (UE-V).</span><span class="sxs-lookup"><span data-stu-id="b2bdd-104">There are a number of different deployment configurations that Microsoft User Experience Virtualization (UE-V) supports.</span></span> <span data-ttu-id="b2bdd-105">Cette section contient des informations générales et des procédures pas à pas pour vous aider à effectuer les tâches que vous devez effectuer à différentes étapes de votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="b2bdd-105">This section includes general information and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

## <span data-ttu-id="b2bdd-106">Informations de déploiement pour UE-V</span><span class="sxs-lookup"><span data-stu-id="b2bdd-106">Deployment information for UE-V</span></span>


<span data-ttu-id="b2bdd-107">Le déploiement d’UE-V nécessite un emplacement de stockage des paramètres sur un partage réseau et un agent UE-V installé sur chaque ordinateur qui synchronise les paramètres.</span><span class="sxs-lookup"><span data-stu-id="b2bdd-107">A UE-V deployment requires a settings storage location on a network share and a UE-V agent installed on every computer that synchronizes settings.</span></span> <span data-ttu-id="b2bdd-108">Les modèles de stratégie de groupe UE-V peuvent être utilisés pour gérer les paramètres d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="b2bdd-108">The UE-V Group Policy templates can be used to manage UE-V settings.</span></span> <span data-ttu-id="b2bdd-109">Les rubriques suivantes décrivent le déploiement de ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="b2bdd-109">The following topics describe how to deploy these features.</span></span>

[<span data-ttu-id="b2bdd-110">Déploiement de l'emplacement de stockage des paramètres pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="b2bdd-110">Deploying the Settings Storage Location for UE-V 1.0</span></span>](deploying-the-settings-storage-location-for-ue-v-10.md)

<span data-ttu-id="b2bdd-111">Toutes les solutions de déploiement d’UE-V requièrent un emplacement de stockage des paramètres dans lequel se trouvent les packages de paramètres qui contiennent les valeurs de paramètre synchronisées.</span><span class="sxs-lookup"><span data-stu-id="b2bdd-111">All UE-V deployments require a settings storage location where the settings packages that contain the synchronized setting values are located.</span></span>

[<span data-ttu-id="b2bdd-112">Déploiement de l'agent UE-V</span><span class="sxs-lookup"><span data-stu-id="b2bdd-112">Deploying the UE-V Agent</span></span>](deploying-the-ue-v-agent.md)

<span data-ttu-id="b2bdd-113">Pour synchroniser les paramètres à l’aide d’UE-V, l’agent UE-V doit être installé et exécuté sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b2bdd-113">To synchronize settings by using UE-V, a computer must have the UE-V Agent installed and running.</span></span>

[<span data-ttu-id="b2bdd-114">Installation des modèles ADMX de stratégie de groupe UE-V</span><span class="sxs-lookup"><span data-stu-id="b2bdd-114">Installing the UE-V Group Policy ADMX Templates</span></span>](installing-the-ue-v-group-policy-admx-templates.md)

<span data-ttu-id="b2bdd-115">Vous pouvez utiliser une stratégie de groupe pour préconfigurer les paramètres d’UE-V avant de déployer l’agent UE-V ainsi que la configuration standard pour UE-V.</span><span class="sxs-lookup"><span data-stu-id="b2bdd-115">You can use Group Policy to preconfigure UE-V settings before you deploy the UE-V Agent as well as standard UE-V configuration.</span></span>

## <span data-ttu-id="b2bdd-116">Informations de déploiement pour le déploiement de modèles personnalisés</span><span class="sxs-lookup"><span data-stu-id="b2bdd-116">Deployment information for custom template deployment</span></span>


<span data-ttu-id="b2bdd-117">Si vous envisagez de créer des modèles d’emplacement des paramètres personnalisés pour des applications autres que les applications Microsoft incluses dans UE-V, telles que des applications métier, vous pouvez déployer un catalogue de modèles de paramètres et vous devez installer le générateur UE-V pour créer ces modèles.</span><span class="sxs-lookup"><span data-stu-id="b2bdd-117">If you plan to create custom settings location templates for applications other than the Microsoft applications that are included in UE-V, such as line-of-business applications, then you can deploy a settings template catalog and you must install the UE-V Generator to create those templates.</span></span> <span data-ttu-id="b2bdd-118">Pour plus d’informations, consultez [planification du déploiement de modèles personnalisés pour UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="b2bdd-118">For more information, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

[<span data-ttu-id="b2bdd-119">Installation du Générateur UE-V</span><span class="sxs-lookup"><span data-stu-id="b2bdd-119">Installing the UE-V Generator</span></span>](installing-the-ue-v-generator.md)

<span data-ttu-id="b2bdd-120">Le générateur UE-V permet de créer, de modifier et de valider des modèles d’emplacements de paramètres personnalisés qui permettent de synchroniser les paramètres d’applications autres que les applications par défaut.</span><span class="sxs-lookup"><span data-stu-id="b2bdd-120">Use the UE-V Generator to create, edit, and validate custom settings location templates that help synchronize settings of applications other than the default applications.</span></span>

[<span data-ttu-id="b2bdd-121">Déploiement du catalogue de modèles de paramètres pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="b2bdd-121">Deploying the Settings Template Catalog for UE-V 1.0</span></span>](deploying-the-settings-template-catalog-for-ue-v-10.md)

<span data-ttu-id="b2bdd-122">Si vous devez déployer des modèles d’emplacement des paramètres personnalisés pour prendre en charge des applications autres que les applications par défaut de l’agent UE-V, vous devez configurer un catalogue de modèles de paramètres pour les stocker.</span><span class="sxs-lookup"><span data-stu-id="b2bdd-122">If you need to deploy custom settings location templates to support applications other than the default applications in the UE-V Agent, you must configure a settings template catalog to store them.</span></span>

[<span data-ttu-id="b2bdd-123">Déploiement de modèles d'emplacement de paramètres UE-V pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="b2bdd-123">Deploying UE-V Settings Location Templates for UE-V 1.0</span></span>](deploying-ue-v-settings-location-templates-for-ue-v-10.md)

<span data-ttu-id="b2bdd-124">Si vous avez besoin de synchroniser des applications qui ne sont pas les applications par défaut dans l’agent UE-V, les modèles d’emplacement des paramètres personnalisés créés avec le générateur UE-V peuvent être distribués dans le catalogue de modèles de paramètres d’UE-v.</span><span class="sxs-lookup"><span data-stu-id="b2bdd-124">If you need to synchronize applications other than the default applications in the UE-V Agent, the custom setting location templates that are created with UE-V Generator can be distributed to the UE-V settings template catalog.</span></span>

<span data-ttu-id="b2bdd-125">**Remarques**  Le déploiement de modèles personnalisés nécessite un catalogue de modèles de paramètres.</span><span class="sxs-lookup"><span data-stu-id="b2bdd-125">**Note** Deploying custom templates requires a settings template catalog.</span></span> <span data-ttu-id="b2bdd-126">Les modèles d’application Microsoft par défaut sont déployés avec UE-V agent.</span><span class="sxs-lookup"><span data-stu-id="b2bdd-126">The default Microsoft application templates are deployed with the UE-V Agent.</span></span>

 

## <span data-ttu-id="b2bdd-127">Rubriques relatives à ce produit</span><span class="sxs-lookup"><span data-stu-id="b2bdd-127">Topics for this product</span></span>


[<span data-ttu-id="b2bdd-128">Microsoft User Experience Virtualization (UE-V)1.0</span><span class="sxs-lookup"><span data-stu-id="b2bdd-128">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="b2bdd-129">Prise en main de User Experience Virtualization1.0</span><span class="sxs-lookup"><span data-stu-id="b2bdd-129">Getting Started With User Experience Virtualization 1.0</span></span>](getting-started-with-user-experience-virtualization-10.md)

[<span data-ttu-id="b2bdd-130">Planification pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="b2bdd-130">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="b2bdd-131">Opérations d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="b2bdd-131">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

[<span data-ttu-id="b2bdd-132">Résolution des problèmes liés à UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="b2bdd-132">Troubleshooting UE-V 1.0</span></span>](troubleshooting-ue-v-10.md)

 

 





