---
title: Déploiement de MBAM2.0
description: Déploiement de MBAM2.0
author: dansimp
ms.assetid: 4b0eaf10-81b4-427e-9d43-eb833de935a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba4423de5306e1ca204ef3b9fd31424bb8f2630f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809977"
---
# <span data-ttu-id="f4815-103">Déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="f4815-103">Deploying MBAM 2.0</span></span>


<span data-ttu-id="f4815-104">Microsoft BitLocker administration et l’analyse (MBAM) prend en charge plusieurs configurations de déploiement différentes.</span><span class="sxs-lookup"><span data-stu-id="f4815-104">Microsoft BitLocker Administration and Monitoring (MBAM) supports a number of different deployment configurations.</span></span> <span data-ttu-id="f4815-105">Cette section contient des informations à envisager concernant le déploiement de MBAM et des procédures pas à pas pour vous aider à effectuer les tâches que vous devez effectuer à différentes étapes de votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="f4815-105">This section includes information that you should consider about the deployment of MBAM and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

<span data-ttu-id="f4815-106">Vous pouvez déployer MBAM dans une topologie autonome ou à l’aide d’une topologie intégrant MBAM à l’aide de Microsoft System Center Configuration Manager 2007 ou d’un réseau ConfigurationManager MicrosoftSystemCenter2012.</span><span class="sxs-lookup"><span data-stu-id="f4815-106">You can deploy MBAM either in a Stand-alone topology, or with a topology that integrates MBAM with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="f4815-107">Pour plus d’informations sur l’installation d’MBAM avec la topologie intégrée de Configuration Manager, voir [utilisation de MBAM avec Configuration Manager](using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="f4815-107">For information about installing MBAM with the Configuration Manager integrated topology, see [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).</span></span>

## <span data-ttu-id="f4815-108">Informations de déploiement</span><span class="sxs-lookup"><span data-stu-id="f4815-108">Deployment Information</span></span>


-   [<span data-ttu-id="f4815-109">Déploiement de l'infrastructure de serveur MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="f4815-109">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

    <span data-ttu-id="f4815-110">Cette section décrit les différentes options de topologie de déploiement MBAM et l’utilisation de la configuration MBAM pour le déploiement de fonctionnalités de MBAM Server.</span><span class="sxs-lookup"><span data-stu-id="f4815-110">This section describes the different MBAM deployment topology options and how to use MBAM Setup to deploy MBAM Server features.</span></span>

-   [<span data-ttu-id="f4815-111">Déploiement d'objets de stratégie de groupe MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="f4815-111">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

    <span data-ttu-id="f4815-112">Cette section explique comment créer et déployer des objets de stratégie de groupe MBAM requis pour gérer les clients MBAM et les stratégies de chiffrement BitLocker au sein de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f4815-112">This section describes how to create and deploy MBAM Group Policy Objects that are required for managing MBAM Clients and BitLocker encryption policies throughout the enterprise.</span></span>

-   [<span data-ttu-id="f4815-113">Déploiement du client MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="f4815-113">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

    <span data-ttu-id="f4815-114">Cette section explique comment utiliser les fichiers du programme d’installation du client MBAM pour déployer le logiciel client MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4815-114">This section describes how to use the MBAM Client Installer files to deploy the MBAM Client software.</span></span>

-   [<span data-ttu-id="f4815-115">Liste de contrôle du déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="f4815-115">MBAM 2.0 Deployment Checklist</span></span>](mbam-20-deployment-checklist-mbam-2.md)

    <span data-ttu-id="f4815-116">Cette section fournit une liste de vérification de déploiement qui peut être utilisée pour faciliter la fonction MBAM Server et le déploiement du client MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4815-116">This section provides a deployment checklist that can be used to assist in MBAM Server feature and MBAM Client deployment.</span></span>

-   [<span data-ttu-id="f4815-117">Mise à niveau des versions précédentes de MBAM</span><span class="sxs-lookup"><span data-stu-id="f4815-117">Upgrading from Previous Versions of MBAM</span></span>](upgrading-from-previous-versions-of-mbam.md)

    <span data-ttu-id="f4815-118">Cette section fournit des instructions pour la mise à niveau de MBAM à partir de versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="f4815-118">This section provides instructions for upgrading MBAM from previous versions.</span></span>

## <span data-ttu-id="f4815-119">Autres ressources pour le déploiement d’MBAM</span><span class="sxs-lookup"><span data-stu-id="f4815-119">Other Resources for Deploying MBAM</span></span>


[<span data-ttu-id="f4815-120">Guide d’administration et d’administration de Microsoft BitLocker 2</span><span class="sxs-lookup"><span data-stu-id="f4815-120">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>](index.md)

[<span data-ttu-id="f4815-121">Prise en main de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="f4815-121">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)

[<span data-ttu-id="f4815-122">Planification de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="f4815-122">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="f4815-123">Opérations de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="f4815-123">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

[<span data-ttu-id="f4815-124">Résolution des problèmes de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="f4815-124">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

 

 





