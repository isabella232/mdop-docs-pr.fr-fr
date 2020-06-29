---
title: Préparation de votre environnement pour MBAM1.0
description: Préparation de votre environnement pour MBAM1.0
author: dansimp
ms.assetid: 915f7c3c-70ad-4a90-a434-73e7fba97ecb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a2de4e825d5c89aeabcf57d78dc856bacb03e11
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809809"
---
# <span data-ttu-id="a5e2c-103">Préparation de votre environnement pour MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="a5e2c-103">Preparing your Environment for MBAM 1.0</span></span>


<span data-ttu-id="a5e2c-104">Avant de commencer la configuration de l’administration et de la surveillance de BitLocker (MBAM) Microsoft, assurez-vous que vous remplissez les conditions préalables nécessaires pour installer le produit.</span><span class="sxs-lookup"><span data-stu-id="a5e2c-104">Before you begin the Microsoft BitLocker Administration and Monitoring (MBAM) Setup, make sure that you have met the necessary prerequisites to install the product.</span></span> <span data-ttu-id="a5e2c-105">Si vous connaissez les conditions préalables à l’avance, vous pouvez déployer efficacement le produit et activer ses fonctionnalités, qui peuvent prendre en charge les objectifs métiers de votre organisation de manière plus efficace.</span><span class="sxs-lookup"><span data-stu-id="a5e2c-105">If you know the prerequisites in advance, you can efficiently deploy the product and enable its features, which can support the business objectives of your organization more effectively.</span></span>

## <span data-ttu-id="a5e2c-106">Consulter la configuration requise pour le déploiement d’MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="a5e2c-106">Review MBAM 1.0 deployment prerequisites</span></span>


<span data-ttu-id="a5e2c-107">Le client MBAM et toutes les fonctionnalités du serveur MBAM possèdent des éléments requis spécifiques qui doivent être satisfaits pour pouvoir être installés correctement.</span><span class="sxs-lookup"><span data-stu-id="a5e2c-107">The MBAM Client and each of the MBAM Server features have specific prerequisites that must be met before they can be successfully installed.</span></span>

<span data-ttu-id="a5e2c-108">Pour garantir la réussite de l’installation de clients MBAM et de fonctionnalités de serveur MBAM, vous devez vous assurer que les ordinateurs spécifiés pour l’installation du client MBAM ou du MBAM Server sont correctement préparés pour l’installation de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a5e2c-108">To ensure successful installation of MBAM Clients and MBAM Server features, you should plan to ensure that computers specified for MBAM Client or MBAM Server feature installation are properly prepared for MBAM Setup.</span></span>

<span data-ttu-id="a5e2c-109">**Remarques**  La configuration de MBAM vérifie si toutes les conditions préalables sont remplies avant le début de l’installation.</span><span class="sxs-lookup"><span data-stu-id="a5e2c-109">**Note** MBAM Setup verifies if all prerequisites are met before installation starts.</span></span> <span data-ttu-id="a5e2c-110">Si ce n’est pas le cas, cela peut échouer.</span><span class="sxs-lookup"><span data-stu-id="a5e2c-110">If they are not met, Setup will fail.</span></span>

 

[<span data-ttu-id="a5e2c-111">Conditions préalables au déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="a5e2c-111">MBAM 1.0 Deployment Prerequisites</span></span>](mbam-10-deployment-prerequisites.md)

## <span data-ttu-id="a5e2c-112">Plan pour les exigences de la stratégie de groupe MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="a5e2c-112">Plan for MBAM 1.0 Group Policy requirements</span></span>


<span data-ttu-id="a5e2c-113">Avant que MBAM ne puisse gérer des clients au sein de l’entreprise, vous devez définir la stratégie de groupe pour les besoins de chiffrement de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="a5e2c-113">Before MBAM can manage clients in the enterprise, you must define the Group Policy for the encryption requirements of your environment.</span></span>

<span data-ttu-id="a5e2c-114">**Important**  MBAM ne fonctionne pas avec des stratégies pour le chiffrement de lecteur BitLocker autonome.</span><span class="sxs-lookup"><span data-stu-id="a5e2c-114">**Important** MBAM will not work with policies for stand-alone BitLocker drive encryption.</span></span> <span data-ttu-id="a5e2c-115">La stratégie de groupe doit être définie pour MBAM; dans le cas contraire, le chiffrement et l’application de BitLocker échouent.</span><span class="sxs-lookup"><span data-stu-id="a5e2c-115">Group Policy must be defined for MBAM; otherwise, the BitLocker encryption and enforcement will fail.</span></span>

 

[<span data-ttu-id="a5e2c-116">Planification des exigences en matière de stratégie de groupe MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="a5e2c-116">Planning for MBAM 1.0 Group Policy Requirements</span></span>](planning-for-mbam-10-group-policy-requirements.md)

## <span data-ttu-id="a5e2c-117">Planifier les rôles d’administrateur MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="a5e2c-117">Plan for MBAM 1.0 administrator roles</span></span>


<span data-ttu-id="a5e2c-118">Les rôles d’administrateur MBAM sont gérés par des groupes locaux créés par MBAM, lorsque vous installez ce qui suit: le serveur d’administration et de surveillance BitLocker, la fonctionnalité de conformité et d’audit, ainsi que la base de données état de conformité et d’audit.</span><span class="sxs-lookup"><span data-stu-id="a5e2c-118">MBAM administrator roles are managed by local groups that are created by MBAM Setup when you install the following: BitLocker Administration and Monitoring Server, the Compliance and Audit Reports feature, and the Compliance and Audit Status Database.</span></span>

<span data-ttu-id="a5e2c-119">L’appartenance aux rôles MBAM peut être gérée plus efficacement si vous créez des groupes de sécurité dans ActiveDirectoryDomainServices, ajoutez les comptes d’administrateur appropriés à ces groupes, puis ajoutez ces groupes de sécurité aux groupes locaux MBAM.</span><span class="sxs-lookup"><span data-stu-id="a5e2c-119">The membership of MBAM roles can be managed more effectively if you create security groups in ActiveDirectoryDomainServices, add the appropriate administrator accounts to those groups, and then add those security groups to the MBAM local groups.</span></span> <span data-ttu-id="a5e2c-120">Pour plus d’informations, reportez-vous [à la rubrique gestion des rôles d’administrateur de MBAM](how-to-manage-mbam-administrator-roles-mbam-1.md).</span><span class="sxs-lookup"><span data-stu-id="a5e2c-120">For more information, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md).</span></span>

[<span data-ttu-id="a5e2c-121">Planification des rôles administrateur de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="a5e2c-121">Planning for MBAM 1.0 Administrator Roles</span></span>](planning-for-mbam-10-administrator-roles.md)

## <span data-ttu-id="a5e2c-122">Autres ressources pour la planification de MBAM</span><span class="sxs-lookup"><span data-stu-id="a5e2c-122">Other resources for MBAM planning</span></span>


[<span data-ttu-id="a5e2c-123">Planification de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="a5e2c-123">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

 

 





