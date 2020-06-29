---
title: Planification du déploiement de MBAM2.5
description: Planification du déploiement de MBAM2.5
author: dansimp
ms.assetid: 1343b80c-d87a-42e7-b912-e84ba997d7e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e955b426b00539aa2a4ef0b7c3a6650b05633a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811909"
---
# <span data-ttu-id="5a792-103">Planification du déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5a792-103">Planning to Deploy MBAM 2.5</span></span>


<span data-ttu-id="5a792-104">Vous devez prendre en considération un certain nombre de configurations et de configurations de déploiement différentes pour pouvoir créer votre plan de déploiement pour l’administration et la surveillance de BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="5a792-104">You should consider a number of different deployment configurations and prerequisites before you create your deployment plan for Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="5a792-105">Cette section contient des informations qui vous aideront à collecter les informations nécessaires pour formuler une offre de déploiement adaptée à vos besoins professionnels.</span><span class="sxs-lookup"><span data-stu-id="5a792-105">This section includes information that can help you gather the necessary information to formulate a deployment plan that best meets your business requirements.</span></span>

## <span data-ttu-id="5a792-106">Examiner les configurations prises en charge par MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="5a792-106">Review the MBAM 2.5 supported configurations</span></span>


<span data-ttu-id="5a792-107">Après avoir préparé votre environnement informatique pour le déploiement de la fonctionnalité du client MBAM et du serveur, assurez-vous d’examiner les configurations prises en charge pour vérifier que les ordinateurs sur lesquels vous installez MBAM répondent à la configuration minimale requise en matière de matériel et de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5a792-107">After preparing your computing environment for the MBAM Server and Client feature deployment, make sure that you review the Supported Configurations to confirm that the computers on which you are installing MBAM meet the minimum hardware and operating system requirements.</span></span> <span data-ttu-id="5a792-108">Pour plus d’informations sur les conditions préalables pour le déploiement d’MBAM, voir [conditions préalables pour le déploiement d’MBAM 2,5](mbam-25-deployment-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="5a792-108">For more information about MBAM deployment prerequisites, see [MBAM 2.5 Deployment Prerequisites](mbam-25-deployment-prerequisites.md).</span></span>

[<span data-ttu-id="5a792-109">Configurations prises en charge par MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5a792-109">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

## <span data-ttu-id="5a792-110">Planifier le déploiement du serveur et du client MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="5a792-110">Plan for MBAM 2.5 Server and Client deployment</span></span>


<span data-ttu-id="5a792-111">L’infrastructure du serveur MBAM dépend d’un ensemble de fonctionnalités serveur qui peuvent être configurées sur un ou plusieurs ordinateurs serveur, en fonction des besoins de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="5a792-111">The MBAM Server infrastructure depends on a set of server features that can be configured on one or more server computers, based on the requirements of the enterprise.</span></span> <span data-ttu-id="5a792-112">Ces fonctionnalités peuvent être configurées dans une configuration distribuée sur plusieurs serveurs.</span><span class="sxs-lookup"><span data-stu-id="5a792-112">These features can be configured in a distributed configuration across multiple servers.</span></span>

<span data-ttu-id="5a792-113">**Remarques**  Une installation MBAM sur un seul serveur est recommandée uniquement dans les environnements de laboratoire.</span><span class="sxs-lookup"><span data-stu-id="5a792-113">**Note** An MBAM installation on a single server is recommended only for lab environments.</span></span>

 

<span data-ttu-id="5a792-114">Le client MBAM permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="5a792-114">The MBAM Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="5a792-115">Le client BitLocker peut être intégré à une organisation en déployant le client par le biais d’un système de remise de logiciels d’entreprise ou en installant le client sur des ordinateurs clients dans le cadre du processus d’image initial.</span><span class="sxs-lookup"><span data-stu-id="5a792-115">The BitLocker client can be integrated into an organization by deploying the client through an enterprise software delivery system or by installing the Client on client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="5a792-116">Avec MBAM, vous pouvez chiffrer un ordinateur au sein de votre organisation avant d’avoir reçu l’ordinateur, ou après une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5a792-116">With MBAM, you can encrypt a computer in your organization either before the end user receives the computer, or afterwards by using Group Policy.</span></span>

[<span data-ttu-id="5a792-117">Planification du déploiement de serveursMBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5a792-117">Planning for MBAM 2.5 Server Deployment</span></span>](planning-for-mbam-25-server-deployment.md)

[<span data-ttu-id="5a792-118">Planification du déploiement de clients MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5a792-118">Planning for MBAM 2.5 Client Deployment</span></span>](planning-for-mbam-25-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a><span data-ttu-id="5a792-119">Autres ressources pour la planification de MBAM</span><span class="sxs-lookup"><span data-stu-id="5a792-119">Other resources for MBAM planning</span></span>


[<span data-ttu-id="5a792-120">Planification de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="5a792-120">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

## <span data-ttu-id="5a792-121">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="5a792-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="5a792-122">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="5a792-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="5a792-123">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="5a792-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

 

 





