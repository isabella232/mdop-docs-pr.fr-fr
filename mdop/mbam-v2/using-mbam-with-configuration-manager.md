---
title: Utilisation de MBAM avec Configuration Manager
description: Utilisation de MBAM avec Configuration Manager
author: dansimp
ms.assetid: 03868717-4aa7-4897-8166-9a3df5e9519e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e3c5dd199010ac758ab701b0753d913ea323efd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810164"
---
# <span data-ttu-id="d9faf-103">Utilisation de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d9faf-103">Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="d9faf-104">Lorsque vous installez Microsoft BitLocker administration et la surveillance (MBAM), vous pouvez choisir une installation qui intègre Microsoft BitLocker administration et l’analyse à l’aide de System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d9faf-104">When you install Microsoft BitLocker Administration and Monitoring (MBAM), you can choose an installation that integrates Microsoft BitLocker Administration and Monitoring with System Center Configuration Manager.</span></span> <span data-ttu-id="d9faf-105">Pour obtenir la liste des versions prises en charge de Configuration Manager, consultez [planification du déploiement d’MBAM avec Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="d9faf-105">For a list of the supported versions of Configuration Manager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="d9faf-106">Cette intégration transfère l’infrastructure d’administration et de création de rapports de Microsoft BitLocker dans l’environnement natif de Microsoft System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d9faf-106">This integration moves the Microsoft BitLocker Administration and Monitoring compliance and reporting infrastructure into the native environment of Microsoft System Center Configuration Manager.</span></span> <span data-ttu-id="d9faf-107">La topologie de Configuration Manager permet aux administrateurs informatiques d’afficher des rapports et l’état de conformité de leur entreprise à partir de la console de gestion de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d9faf-107">With the Configuration Manager topology, IT administrators can view reports and the compliance status of their enterprise from the Configuration Manager Management Console.</span></span>

<span data-ttu-id="d9faf-108">**Important**  Windows to Go n’est pas pris en charge lorsque vous installez la topologie intégrée de MBAM avec Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="d9faf-108">**Important** Windows To Go is not supported when you install the integrated topology of MBAM with Configuration Manager 2007.</span></span>

 

## <a href="" id="getting-started---using-mbam-with-configuration-manager"></a><span data-ttu-id="d9faf-109">Mise en route – utilisation de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d9faf-109">Getting Started – Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="d9faf-110">Cette section décrit l’utilisation de MBAM avec Configuration Manager et décrit l’architecture recommandée pour le déploiement d’MBAM à l’aide de la topologie d’intégration de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d9faf-110">This section describes how MBAM works with Configuration Manager and explains the recommended architecture for deploying MBAM with the Configuration Manager Integration topology.</span></span>

[<span data-ttu-id="d9faf-111">Prise en main - Utilisation de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d9faf-111">Getting Started - Using MBAM with Configuration Manager</span></span>](getting-started---using-mbam-with-configuration-manager.md)

## <span data-ttu-id="d9faf-112">Planification du déploiement de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d9faf-112">Planning to Deploy MBAM with Configuration Manager</span></span>


<span data-ttu-id="d9faf-113">Dans cette section, vous devez prendre en compte les conditions préalables à l’installation, les configurations prises en charge et la configuration matérielle et logicielle requise avant d’installer MBAM avec la topologie de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d9faf-113">This section describes the installation prerequisites, supported configurations, and hardware and software requirements that you need to consider before you install MBAM with the Configuration Manager topology.</span></span>

[<span data-ttu-id="d9faf-114">Planification du déploiement de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d9faf-114">Planning to Deploy MBAM with Configuration Manager</span></span>](planning-to-deploy-mbam-with-configuration-manager-2.md)

## <span data-ttu-id="d9faf-115">Déploiement de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d9faf-115">Deploying MBAM with Configuration Manager</span></span>


<span data-ttu-id="d9faf-116">Cette section décrit le déploiement d’MBAM avec Configuration Manager, ainsi que des instructions pour l’installation et la configuration d’MBAM sur le serveur d’administration et de surveillance et sur le serveur Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d9faf-116">This section describes how to deploy MBAM with Configuration Manager, and includes instructions for installing and configuring the MBAM on the Administration and Monitoring Server and Configuration Manager Server.</span></span>

[<span data-ttu-id="d9faf-117">Déploiement de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d9faf-117">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

## <span data-ttu-id="d9faf-118">Présentation des rapports MBAM dans Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d9faf-118">Understanding MBAM Reports in Configuration Manager</span></span>


<span data-ttu-id="d9faf-119">Cette section décrit les rapports MBAM que vous pouvez exécuter à partir de Configuration Manager afin de montrer la conformité de votre entreprise et de la conformité d’ordinateurs individuels au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="d9faf-119">This section describes the MBAM reports that you can run from Configuration Manager to show the compliance of your enterprise and compliance of individual computers in your enterprise.</span></span>

[<span data-ttu-id="d9faf-120">Présentation des rapports MBAM dans Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d9faf-120">Understanding MBAM Reports in Configuration Manager</span></span>](understanding-mbam-reports-in-configuration-manager.md)

## <span data-ttu-id="d9faf-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d9faf-121">Related topics</span></span>


[<span data-ttu-id="d9faf-122">Opérations de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="d9faf-122">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





