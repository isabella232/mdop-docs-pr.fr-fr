---
title: Scénarios de déploiement de bout en bout pour MED-V2.0
description: Scénarios de déploiement de bout en bout pour MED-V2.0
author: dansimp
ms.assetid: 91bb5a9a-5fb1-4743-8494-9d4dee2ec222
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6d56e70ad359ebf2d76cf3f30f54f73cd9ca1c66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811597"
---
# <span data-ttu-id="9187d-103">Scénarios de déploiement de bout en bout pour MED-V2.0</span><span class="sxs-lookup"><span data-stu-id="9187d-103">End-to-End Deployment Scenario for MED-V 2.0</span></span>


<span data-ttu-id="9187d-104">Cet exemple de scénario de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 vous permet de déployer les composants MED-V au sein de votre entreprise à l’aide de plusieurs scénarios de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="9187d-104">This sample scenario for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 helps you deploy the MED-V components in your enterprise by using multiple scenarios end-to-end.</span></span> <span data-ttu-id="9187d-105">Vous pouvez considérer cet exemple de scénario en tant qu’étude de cas, qui permet de mettre en place les différentes procédures et scénarios.</span><span class="sxs-lookup"><span data-stu-id="9187d-105">You can think of this sample scenario as a case study that helps put the individual scenarios and procedures in context.</span></span>

<span data-ttu-id="9187d-106">Cette section fournit des informations et des indications de base pour le déploiement de composants MED-V en tant que solution de bout en bout au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="9187d-106">This section provides basic information and directions for deploying MED-V components as an end-to-end solution in your enterprise.</span></span>

## <span data-ttu-id="9187d-107">Scénario détaillé de déploiement MED-V</span><span class="sxs-lookup"><span data-stu-id="9187d-107">MED-V Deployment Step-by-step Scenario</span></span>


<span data-ttu-id="9187d-108">Les rubriques de cette procédure pas à pas sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="9187d-108">The topics in this step-by-step scenario include the following:</span></span>

-   <span data-ttu-id="9187d-109">Les [Configurations prises en charge par MED-V 2,0](med-v-20-supported-configurations.md) traitent de la configuration requise pour l’installation et l’exécution de Microsoft Enterprise Desktop Virtualization (med-v) 2.0 dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="9187d-109">[MED-V 2.0 Supported Configurations](med-v-20-supported-configurations.md) discusses the requirements that you must have to install and run Microsoft Enterprise Desktop Virtualization (MED-V) 2.0in your environment.</span></span> <span data-ttu-id="9187d-110">Cette rubrique spécifie la configuration requise du système d’exploitation, la configuration requise pour l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="9187d-110">This topic specifies the operating system requirements, configuration requirements, and MED-V workspace requirements.</span></span> <span data-ttu-id="9187d-111">Cette rubrique inclut également des informations sur la localisation des langues prises en charge par MED-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="9187d-111">This topic also includes localization information about the languages that MED-V 2.0 supports.</span></span>

-   <span data-ttu-id="9187d-112">La [vue d’ensemble du déploiement de MED-V 2,0](med-v-20-deployment-overview.md) traite des informations générales et des instructions pour vous aider à installer et déployer med-v au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="9187d-112">[MED-V 2.0 Deployment Overview](med-v-20-deployment-overview.md) discusses general information and instructions to help you install and deploy MED-V throughout your enterprise.</span></span> <span data-ttu-id="9187d-113">Les composants MED-V sont basés sur le client et sont remis et gérés en utilisant vos processus et infrastructure d’entreprise existants.</span><span class="sxs-lookup"><span data-stu-id="9187d-113">The MED-V components are client-based and are delivered and managed by using your existing enterprise infrastructure and processes.</span></span> <span data-ttu-id="9187d-114">Cette rubrique fournit une vue d’ensemble de la solution MED-V qui inclut des informations sur les fichiers d’installation de MED-V et les composants MED-V que vous déployez.</span><span class="sxs-lookup"><span data-stu-id="9187d-114">This topic provides an overview of the MED-V solution that includes information about the MED-V installation files and the MED-V components that you deploy.</span></span> <span data-ttu-id="9187d-115">Cette rubrique fournit également une vue d’ensemble de l’installation et du processus de déploiement de MED-V.</span><span class="sxs-lookup"><span data-stu-id="9187d-115">This topic also provides a high-level overview of the MED-V installation and deployment process.</span></span>

-   <span data-ttu-id="9187d-116">[Préparer l’environnement de déploiement pour med-v](prepare-the-deployment-environment-for-med-v.md) explique comment préparer votre environnement pour un déploiement 2,0 MED-V.</span><span class="sxs-lookup"><span data-stu-id="9187d-116">[Prepare the Deployment Environment for MED-V](prepare-the-deployment-environment-for-med-v.md) discusses how to prepare your environment for a MED-V 2.0 deployment.</span></span> <span data-ttu-id="9187d-117">Cette section décrit les conditions préalables requises pour l’environnement MED-V, comme Microsoft Windows 7 et une infrastructure Active Directory dans laquelle vous utilisez une stratégie de groupe pour assurer une gestion centralisée et la configuration des systèmes d’exploitation, des applications et des paramètres des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9187d-117">This section describes the prerequisites that are required for the MED-V environment, such as Microsoft Windows 7 and an Active Directory infrastructure in which you use Group Policy to provide centralized management and configuration of operating systems, applications, and users' settings.</span></span> <span data-ttu-id="9187d-118">Cette section décrit également les prérequis requis pour l’installation et le déploiement de MED-V 2,0 au sein de votre entreprise, tels que le PC virtuel Windows et la mise à jour de PC virtuel Windows requise.</span><span class="sxs-lookup"><span data-stu-id="9187d-118">This section also describes the prerequisites that you must have for installing and deploying MED-V 2.0 throughout your enterprise, such as Windows Virtual PC and the required Windows Virtual PC update.</span></span>

-   <span data-ttu-id="9187d-119">Le [déploiement des composants med-v](deploy-the-med-v-components.md) aborde les différentes méthodes d’installation de tous les fichiers d’installation nécessaires et des composants MED-V au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="9187d-119">[Deploy the MED-V Components](deploy-the-med-v-components.md) discusses the different ways you can install all of the necessary installation files and MED-V components throughout your enterprise.</span></span> <span data-ttu-id="9187d-120">Pour installer et déployer MED-V, vous devez généralement procéder comme suit:</span><span class="sxs-lookup"><span data-stu-id="9187d-120">To install and deploy MED-V, you typically follow these steps:</span></span>

    1.  <span data-ttu-id="9187d-121">Installez le module de création de **package d’espace de travail MED-v** sur l’ordinateur d’administration que vous utiliserez pour générer les packages d’espace de travail MED-v.</span><span class="sxs-lookup"><span data-stu-id="9187d-121">Install the **MED-V Workspace Packager** on the administrator computer that you will use to build the MED-V workspace packages.</span></span> <span data-ttu-id="9187d-122">Pour plus d’informations, reportez-vous [à la rubrique Comment installer le gestionnaire de package MED-V](how-to-install-the-med-v-workspace-packager.md).</span><span class="sxs-lookup"><span data-stu-id="9187d-122">For more information, see [How to Install the MED-V Workspace Packager](how-to-install-the-med-v-workspace-packager.md).</span></span>

    2.  <span data-ttu-id="9187d-123">Créez et testez vos packages d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="9187d-123">Create and test your MED-V workspace packages.</span></span> <span data-ttu-id="9187d-124">Pour plus d’informations, consultez [créer un package d’espace de travail MED-v](create-a-med-v-workspace-package.md) et [tester le package d’espace de travail MED-v](testing-the-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="9187d-124">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md) and [Testing the MED-V Workspace Package](testing-the-med-v-workspace-package.md).</span></span>

    3.  <span data-ttu-id="9187d-125">Déployez MED-V au sein de votre entreprise à l’aide de la méthode existante de votre entreprise pour le déploiement d’applications.</span><span class="sxs-lookup"><span data-stu-id="9187d-125">Deploy MED-V throughout your enterprise by using your company’s existing method for deploying applications.</span></span> <span data-ttu-id="9187d-126">Pour plus d’informations, reportez-vous à [déploiement du package d’espace de travail MED-V](deploying-the-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="9187d-126">For more information, see [Deploying the MED-V Workspace Package](deploying-the-med-v-workspace-package.md).</span></span>

## <span data-ttu-id="9187d-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9187d-127">Related topics</span></span>


[<span data-ttu-id="9187d-128">Déploiement de MED-V</span><span class="sxs-lookup"><span data-stu-id="9187d-128">Deployment of MED-V</span></span>](deployment-of-med-v.md)

[<span data-ttu-id="9187d-129">Scénarios de planification de bout en bout pour MED-V2.0</span><span class="sxs-lookup"><span data-stu-id="9187d-129">End-to-End Planning Scenario for MED-V 2.0</span></span>](end-to-end-planning-scenario-for-med-v-20.md)

[<span data-ttu-id="9187d-130">Scénario d'opérations de bout en bout pour MED-V2.0</span><span class="sxs-lookup"><span data-stu-id="9187d-130">End-to-End Operations Scenario for MED-V 2.0</span></span>](end-to-end-operations-scenario-for-med-v-20.md)

 

 





