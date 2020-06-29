---
title: Déploiement du client MBAM1.0
description: Déploiement du client MBAM1.0
author: dansimp
ms.assetid: f7ca233f-5035-4ff9-ab3a-f2453b4929d1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dee8c2f4a9b398c9f0797ada35e4c36610c755b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809635"
---
# <span data-ttu-id="1e250-103">Déploiement du client MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="1e250-103">Deploying the MBAM 1.0 Client</span></span>


<span data-ttu-id="1e250-104">Le client Microsoft BitLocker Administration and Analysis (MBAM) permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="1e250-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="1e250-105">Le client BitLocker peut être intégré à une organisation en déployant le client via des outils tels que les services de domaine Active Directory (AD FS) ou en chiffrant directement les ordinateurs clients dans le cadre du processus d’imagerie initial.</span><span class="sxs-lookup"><span data-stu-id="1e250-105">The BitLocker client can be integrated into an organization by deploying the client through tools like Active Directory Domain Services or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="1e250-106">En fonction du moment de déploiement du client MBAM, vous pouvez activer le chiffrement BitLocker sur un ordinateur de votre organisation avant ou après la réception de l’ordinateur par l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="1e250-106">Depending on when you deploy the MBAM Client, you can enable BitLocker encryption on a computer in your organization either before or after the end user receives the computer.</span></span> <span data-ttu-id="1e250-107">Pour contrôler ce minutage, vous devez configurer une stratégie de groupe et déployer le logiciel client MBAM à l’aide d’un système de déploiement de logiciels d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="1e250-107">To control this timing, you configure Group Policy and deploy the MBAM Client software by using an enterprise software deployment system.</span></span>

<span data-ttu-id="1e250-108">Vous pouvez utiliser l’une ou l’autre de ces méthodes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1e250-108">You can use either or both of these methods in your organization.</span></span> <span data-ttu-id="1e250-109">Si vous utilisez les deux méthodes, vous pouvez améliorer la conformité, la création de rapports et la prise en charge des récupérations de clés.</span><span class="sxs-lookup"><span data-stu-id="1e250-109">If you use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

## <span data-ttu-id="1e250-110">Déployer le client MBAM sur un ordinateur portable ou de bureau</span><span class="sxs-lookup"><span data-stu-id="1e250-110">Deploy the MBAM Client to desktop or laptop computers</span></span>


<span data-ttu-id="1e250-111">Après avoir configuré une stratégie de groupe, vous pouvez déployer les fichiers du programme d’installation du client MBAM sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="1e250-111">After you have configured Group Policy, you can deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="1e250-112">Pour ce faire, vous devez utiliser un produit système de déploiement de logiciels d’entreprise, tel que Microsoft System Center 2012 Configuration Manager ou les services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1e250-112">You can do this by use of an enterprise software deployment system product like Microsoft System Center 2012 Configuration Manager or Active Directory Domain Services.</span></span> <span data-ttu-id="1e250-113">Les deux fichiers du programme d’installation du client MBAM disponibles sont MBAMClient-64bit.msi et MBAMClient-32bit.msi.</span><span class="sxs-lookup"><span data-stu-id="1e250-113">The two available MBAM Client installation Windows Installer files are MBAMClient-64bit.msi and MBAMClient-32bit.msi.</span></span> <span data-ttu-id="1e250-114">Ces fichiers sont fournis avec le logiciel MBAM.</span><span class="sxs-lookup"><span data-stu-id="1e250-114">These files are provided with the MBAM software.</span></span> <span data-ttu-id="1e250-115">Pour plus d’informations sur le déploiement d’objets de stratégie de groupe MBAM, voir [déploiement d’objets de stratégie de groupe MBAM 1,0](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="1e250-115">For more information about how to deploy MBAM Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

[<span data-ttu-id="1e250-116">Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables</span><span class="sxs-lookup"><span data-stu-id="1e250-116">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-1.md)

## <span data-ttu-id="1e250-117">Déploiement du client MBAM dans le cadre d’un déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="1e250-117">Deploy the MBAM Client as part of a Windows deployment</span></span>


<span data-ttu-id="1e250-118">Dans certaines organisations, de nouveaux ordinateurs sont reçus et configurés de manière centralisée.</span><span class="sxs-lookup"><span data-stu-id="1e250-118">In some organizations, new computers are received and configured centrally.</span></span> <span data-ttu-id="1e250-119">Cette situation permet aux administrateurs d’installer le client MBAM pour gérer le chiffrement BitLocker sur chaque ordinateur avant que les données de l’utilisateur ne soient écrites sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1e250-119">This situation enables administrators to install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to the computer.</span></span> <span data-ttu-id="1e250-120">Cette approche permet de s’assurer que les ordinateurs sont correctement chiffrés, car l’administrateur effectue l’action sans recourir à une action de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="1e250-120">This approach helps to ensure that computers are properly encrypted because the administrator performs the action without reliance on end-user action.</span></span> <span data-ttu-id="1e250-121">Une supposition essentielle pour ce scénario est que la stratégie de l’organisation installe une image Windows d’entreprise avant que l’ordinateur ne soit remis à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1e250-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

[<span data-ttu-id="1e250-122">Déploiement du client MBAM dans le cadre d'un déploiement de Windows</span><span class="sxs-lookup"><span data-stu-id="1e250-122">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-1.md)

## <span data-ttu-id="1e250-123">Autres ressources pour le déploiement du client MBAM</span><span class="sxs-lookup"><span data-stu-id="1e250-123">Other resources for deploying the MBAM Client</span></span>


[<span data-ttu-id="1e250-124">Déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="1e250-124">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

[<span data-ttu-id="1e250-125">Planification du déploiement de clients MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="1e250-125">Planning for MBAM 1.0 Client Deployment</span></span>](planning-for-mbam-10-client-deployment.md)

 

 





