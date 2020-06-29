---
title: Planification du déploiement de MBAM1.0
description: Planification du déploiement de MBAM1.0
author: dansimp
ms.assetid: 30ad4304-45c6-427d-8e33-ebe8053c7871
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2ff25e705717db5086150ed08a5640335bbacb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809804"
---
# <span data-ttu-id="45931-103">Planification du déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="45931-103">Planning to Deploy MBAM 1.0</span></span>


<span data-ttu-id="45931-104">Vous devez prendre en considération un certain nombre de configurations et de configurations de déploiement différentes pour pouvoir créer votre plan de déploiement d’MBAM (Microsoft BitLocker Administration and Analysis 1,0).</span><span class="sxs-lookup"><span data-stu-id="45931-104">You should consider a number of different deployment configurations and prerequisites before you create your Microsoft BitLocker Administration and Monitoring (MBAM) 1.0 deployment plan.</span></span> <span data-ttu-id="45931-105">Cette section contient des informations qui vous aideront à collecter les informations nécessaires pour formuler un plan de déploiement qui répond le mieux à vos besoins professionnels.</span><span class="sxs-lookup"><span data-stu-id="45931-105">This section includes information that can help you gather the information that you must have to formulate a deployment plan that best meets your business requirements.</span></span>

## <span data-ttu-id="45931-106">Examiner les configurations prises en charge par MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="45931-106">Review the MBAM 1.0 supported configurations</span></span>


<span data-ttu-id="45931-107">Après avoir préparé votre environnement informatique pour l’installation du client MBAM et de la fonctionnalité serveur, assurez-vous d’examiner les informations de configurations prises en charge pour MBAM pour vérifier que les ordinateurs sur lesquels vous installez MBAM répondent à la configuration minimale requise du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="45931-107">After you prepare your computing environment for the MBAM Client and Server feature installation, make sure that you review the Supported Configurations information for MBAM to confirm that the computers on which you install MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="45931-108">Pour plus d’informations sur les conditions préalables pour le déploiement d’MBAM, voir [conditions préalables pour le déploiement d’MBAM 1,0](mbam-10-deployment-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="45931-108">For more information about MBAM deployment prerequisites, see [MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md).</span></span>

[<span data-ttu-id="45931-109">Configurations prises en charge par MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="45931-109">MBAM 1.0 Supported Configurations</span></span>](mbam-10-supported-configurations.md)

## <span data-ttu-id="45931-110">Planifier le déploiement du serveur et du client MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="45931-110">Plan for MBAM 1.0 Server and Client deployment</span></span>


<span data-ttu-id="45931-111">L’infrastructure du serveur MBAM dépend d’un ensemble de fonctionnalités serveur qui peuvent être installées sur un ou plusieurs ordinateurs serveur, en fonction des besoins de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="45931-111">The MBAM server infrastructure depends on a set of server features that can be installed on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="45931-112">Ces fonctionnalités peuvent être installées sur un serveur unique ou distribuées sur plusieurs serveurs.</span><span class="sxs-lookup"><span data-stu-id="45931-112">These features can be installed on a single server or distributed across multiple servers.</span></span>

<span data-ttu-id="45931-113">Le client MBAM permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="45931-113">The MBAM Client enables administrators to enforce and monitor the BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="45931-114">Le client BitLocker peut être intégré à une organisation en déployant le client via des outils tels que les services de domaine Active Directory (AD FS) ou en chiffrant directement les ordinateurs clients dans le cadre du processus d’imagerie initial.</span><span class="sxs-lookup"><span data-stu-id="45931-114">The BitLocker client can be integrated into an organization by deploying the client through tools like Active Directory Domain Services or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="45931-115">Avec MBAM, vous pouvez chiffrer un ordinateur de votre organisation avant que l’utilisateur final ne reçoive l’ordinateur ou après, à l’aide d’une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="45931-115">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer or afterwards, by using Group Policy.</span></span> <span data-ttu-id="45931-116">Vous pouvez appliquer l’une ou l’autre des méthodes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="45931-116">You can use one or both methods in your organization.</span></span> <span data-ttu-id="45931-117">Si vous choisissez d’utiliser les deux méthodes, vous pouvez améliorer la conformité, la création de rapports et la prise en charge de la récupération de clés.</span><span class="sxs-lookup"><span data-stu-id="45931-117">If you choose to use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

[<span data-ttu-id="45931-118">Planification du déploiement de serveursMBAM1.0</span><span class="sxs-lookup"><span data-stu-id="45931-118">Planning for MBAM 1.0 Server Deployment</span></span>](planning-for-mbam-10-server-deployment.md)

[<span data-ttu-id="45931-119">Planification du déploiement de clients MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="45931-119">Planning for MBAM 1.0 Client Deployment</span></span>](planning-for-mbam-10-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="45931-120">Autres ressources pour la planification de MBAM</span><span class="sxs-lookup"><span data-stu-id="45931-120">Other resources for MBAM planning</span></span>


-   [<span data-ttu-id="45931-121">Planification de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="45931-121">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

 

 





