---
title: Planification du déploiement de MBAM2.0
description: Planification du déploiement de MBAM2.0
author: dansimp
ms.assetid: 2dc05fcd-aed9-4315-aeaf-92aaa9e0e955
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c7f065e52655212261dfe8b6b3f081f697142473
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811273"
---
# <span data-ttu-id="3029e-103">Planification du déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="3029e-103">Planning to Deploy MBAM 2.0</span></span>


<span data-ttu-id="3029e-104">Vous devez prendre en considération un certain nombre de configurations et de configurations de déploiement différentes pour pouvoir créer votre plan de déploiement pour l’administration et la surveillance de BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="3029e-104">You should consider a number of different deployment configurations and prerequisites before you create your deployment plan for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="3029e-105">Cette section contient des informations qui vous aideront à collecter les informations nécessaires pour formuler une offre de déploiement adaptée à vos besoins professionnels.</span><span class="sxs-lookup"><span data-stu-id="3029e-105">This section includes information that can help you gather the necessary information to formulate a deployment plan that best meets your business requirements.</span></span> <span data-ttu-id="3029e-106">Si vous installez MBAM avec la topologie Configuration Manager, consultez [planification du déploiement de MBAM avec Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) pour plus d’informations de planification.</span><span class="sxs-lookup"><span data-stu-id="3029e-106">If you are installing MBAM with the Configuration Manager topology, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) for additional planning information.</span></span>

## <span data-ttu-id="3029e-107">Examiner les configurations prises en charge par MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="3029e-107">Review the MBAM 2.0 Supported Configurations</span></span>


<span data-ttu-id="3029e-108">Après avoir préparé votre environnement informatique pour l’installation de la fonctionnalité client et MBAM Server et, assurez-vous d’examiner les configurations prises en charge pour vérifier que les ordinateurs sur lesquels vous installez MBAM présentent la configuration minimale requise en matière de matériel et de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3029e-108">After preparing your computing environment for the MBAM Server and Client feature installation, make sure that you review the Supported Configurations to confirm that the computers on which you are installing MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="3029e-109">Pour plus d’informations sur les conditions préalables pour le déploiement d’MBAM, voir [conditions préalables pour le déploiement d’MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="3029e-109">For more information about MBAM deployment prerequisites, see [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md).</span></span>

[<span data-ttu-id="3029e-110">Configurations prises en charge par MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="3029e-110">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)

## <span data-ttu-id="3029e-111">Planifier le déploiement du serveur et du client MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="3029e-111">Plan for MBAM 2.0 Server and Client Deployment</span></span>


<span data-ttu-id="3029e-112">L’infrastructure du serveur MBAM dépend d’un ensemble de fonctionnalités serveur qui peuvent être installées sur un ou plusieurs ordinateurs serveur, en fonction des besoins de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="3029e-112">The MBAM Server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="3029e-113">Ces fonctionnalités peuvent être installées dans une configuration distribuée sur plusieurs serveurs.</span><span class="sxs-lookup"><span data-stu-id="3029e-113">These features can be installed in a distributed configuration across multiple servers.</span></span>

<span data-ttu-id="3029e-114">**Remarques**  Une installation MBAM sur un seul serveur est recommandée uniquement dans les environnements de laboratoire.</span><span class="sxs-lookup"><span data-stu-id="3029e-114">**Note** An MBAM installation on a single server is recommended only for lab environments.</span></span>

 

<span data-ttu-id="3029e-115">Le client MBAM permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="3029e-115">The MBAM Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="3029e-116">Le client BitLocker peut être intégré au sein d’une organisation en déployant le client par le biais d’un système de distribution de logiciels d’entreprise ou en installant l’agent client sur les ordinateurs clients dans le cadre du processus d’image initial.</span><span class="sxs-lookup"><span data-stu-id="3029e-116">The BitLocker client can be integrated into an organization by deploying the client through an enterprise software delivery system or by installing the client agent on client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="3029e-117">Avec MBAM, vous pouvez chiffrer un ordinateur au sein de votre organisation avant d’avoir reçu l’ordinateur, ou après une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="3029e-117">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer, or afterwards by using Group Policy.</span></span>

[<span data-ttu-id="3029e-118">Planification du déploiement de serveursMBAM2.0</span><span class="sxs-lookup"><span data-stu-id="3029e-118">Planning for MBAM 2.0 Server Deployment</span></span>](planning-for-mbam-20-server-deployment-mbam-2.md)

[<span data-ttu-id="3029e-119">Planification du déploiement de clients MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="3029e-119">Planning for MBAM 2.0 Client Deployment</span></span>](planning-for-mbam-20-client-deployment-mbam-2.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="3029e-120">Autres ressources pour la planification de MBAM</span><span class="sxs-lookup"><span data-stu-id="3029e-120">Other Resources for MBAM Planning</span></span>


[<span data-ttu-id="3029e-121">Planification de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="3029e-121">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

 

 





