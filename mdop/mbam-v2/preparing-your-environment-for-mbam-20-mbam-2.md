---
title: Préparation de votre environnement pour MBAM2.0
description: Préparation de votre environnement pour MBAM2.0
author: dansimp
ms.assetid: 5fb01da9-620e-4992-9e54-2ed3fb69e6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1be989112d456064db302952d50159d00b5597a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811256"
---
# <span data-ttu-id="bf4d6-103">Préparation de votre environnement pour MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="bf4d6-103">Preparing your Environment for MBAM 2.0</span></span>


<span data-ttu-id="bf4d6-104">Avant de lancer le programme d’installation de Microsoft BitLocker (MBAM), vous devez vérifier que vous remplissez les conditions préalables à l’installation du produit.</span><span class="sxs-lookup"><span data-stu-id="bf4d6-104">Before beginning Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should make sure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="bf4d6-105">Lorsque vous savez ce que sont les conditions préalables, vous pouvez déployer le produit de façon efficace et activer ses fonctionnalités afin qu’il prenne en charge les objectifs métiers de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bf4d6-105">When you know what the prerequisites are ahead of time, you can efficiently deploy the product and enable its features so that it most effectively supports your organization’s business objectives.</span></span>

<span data-ttu-id="bf4d6-106">Si vous déployez l’administration et la surveillance de BitLocker avec Microsoft System Center Configuration Manager 2007 ou MicrosoftSystemCenter2012, voir [planification du déploiement d’MBAM avec Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="bf4d6-106">If you are deploying Microsoft BitLocker Administration and Monitoring with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

## <span data-ttu-id="bf4d6-107">Consulter la configuration requise pour le déploiement d’MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="bf4d6-107">Review MBAM 2.0 Deployment Prerequisites</span></span>


<span data-ttu-id="bf4d6-108">Le client MBAM et toutes les fonctionnalités du serveur MBAM possèdent des éléments requis spécifiques qui doivent être satisfaits pour pouvoir être installés correctement.</span><span class="sxs-lookup"><span data-stu-id="bf4d6-108">The MBAM Client and each of the MBAM Server features have specific prerequisites that must be met before they can be successfully installed.</span></span>

<span data-ttu-id="bf4d6-109">Pour garantir la réussite de l’installation des clients MBAM et des fonctionnalités du serveur MBAM, assurez-vous que les ordinateurs spécifiés pour l’installation de la fonctionnalité du client MBAM ou MBAM du serveur sont bien préparés pour l’installation de MBAM.</span><span class="sxs-lookup"><span data-stu-id="bf4d6-109">To ensure successful installation of MBAM Clients and MBAM Server features, ensure that computers specified for MBAM Client or MBAM Server feature installation are properly prepared for MBAM Setup.</span></span>

<span data-ttu-id="bf4d6-110">**Remarques**  Le programme d’installation de MBAM vérifie que toutes les conditions préalables sont remplies avant le début de l’installation.</span><span class="sxs-lookup"><span data-stu-id="bf4d6-110">**Note** MBAM Setup checks that all prerequisites are met before installation starts.</span></span> <span data-ttu-id="bf4d6-111">Si toutes les conditions préalables ne sont pas remplies, le programme d’installation ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="bf4d6-111">If all prerequisites are not met, Setup will fail.</span></span>

 

[<span data-ttu-id="bf4d6-112">Conditions préalables au déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="bf4d6-112">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)

## <span data-ttu-id="bf4d6-113">Plan pour les exigences de la stratégie de groupe MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="bf4d6-113">Plan for MBAM 2.0 Group Policy Requirements</span></span>


<span data-ttu-id="bf4d6-114">Avant que MBAM ne puisse gérer des clients au sein de l’entreprise, vous devez définir une stratégie de groupe pour les besoins de chiffrement de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="bf4d6-114">Before MBAM can manage clients in the enterprise, you must define Group Policy for the encryption requirements of your environment.</span></span>

<span data-ttu-id="bf4d6-115">**Important**  MBAM ne fonctionne pas avec des stratégies pour le chiffrement de lecteur BitLocker autonome.</span><span class="sxs-lookup"><span data-stu-id="bf4d6-115">**Important** MBAM will not work with policies for stand-alone BitLocker drive encryption.</span></span> <span data-ttu-id="bf4d6-116">Les paramètres de stratégie de groupe doivent être définis pour MBAM ou le chiffrement et l’application de BitLocker échoueront.</span><span class="sxs-lookup"><span data-stu-id="bf4d6-116">Group Policy settings must be defined for MBAM, or BitLocker encryption and enforcement will fail.</span></span>

 

[<span data-ttu-id="bf4d6-117">Planification des exigences en matière de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="bf4d6-117">Planning for MBAM 2.0 Group Policy Requirements</span></span>](planning-for-mbam-20-group-policy-requirements-mbam-2.md)

## <span data-ttu-id="bf4d6-118">Planifier les rôles d’administrateur MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="bf4d6-118">Plan for MBAM 2.0 Administrator Roles</span></span>


<span data-ttu-id="bf4d6-119">Les rôles d’administrateur MBAM sont gérés par des groupes locaux créés par MBAM, lorsque vous installez le serveur d’administration et de surveillance de BitLocker, que vous utilisez la fonctionnalité rapports de conformité et d’audit, ainsi que la base de données état de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="bf4d6-119">MBAM administrator roles are managed by local groups that are created by MBAM Setup when you install the BitLocker Administration and Monitoring Server, the Compliance and Audit Reports feature, and the Compliance and Audit Status Database.</span></span>

<span data-ttu-id="bf4d6-120">L’appartenance aux rôles d’administration et de surveillance de BitLocker peut être mieux gérée en créant des groupes de sécurité dans ActiveDirectoryDomainServices, en ajoutant les comptes d’administrateur appropriés à ces groupes, puis en ajoutant ces groupes de sécurité à l’administration de BitLocker et en surveillant les groupes locaux.</span><span class="sxs-lookup"><span data-stu-id="bf4d6-120">The membership of Microsoft BitLocker Administration and Monitoring roles can best be managed by creating security groups in ActiveDirectoryDomainServices, adding the appropriate administrator accounts to those groups, and then adding those security groups to the BitLocker Administration and Monitoring local groups.</span></span> <span data-ttu-id="bf4d6-121">Pour plus d’informations, reportez-vous [à la rubrique gestion des rôles d’administrateur de MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="bf4d6-121">For more information, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md).</span></span>

## <span data-ttu-id="bf4d6-122">Autres ressources pour la planification de MBAM</span><span class="sxs-lookup"><span data-stu-id="bf4d6-122">Other Resources for MBAM Planning</span></span>


[<span data-ttu-id="bf4d6-123">Planification de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="bf4d6-123">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="bf4d6-124">Configurations prises en charge par MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="bf4d6-124">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)

 

 





