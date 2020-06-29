---
title: Déploiement du client MBAM2.0
description: Déploiement du client MBAM2.0
author: dansimp
ms.assetid: 3dd584fe-2a54-40f0-9bab-13ea74040b01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa42c8ab3adc273f0e00ba56a59f487deba89c6f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809960"
---
# <span data-ttu-id="372bb-103">Déploiement du client MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="372bb-103">Deploying the MBAM 2.0 Client</span></span>


<span data-ttu-id="372bb-104">Le client Microsoft BitLocker Administration and Analysis (MBAM) permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="372bb-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client enables administrators to enforce and monitor BitLocker drive encryption on computers in the enterprise.</span></span> <span data-ttu-id="372bb-105">Le client BitLocker peut être intégré à une organisation en déployant le client par le biais d’un système de distribution de logiciels électronique, tel que les services de domaine Active Directory (AD FS), ou en chiffrant directement les ordinateurs clients dans le cadre du processus d’imagerie initial.</span><span class="sxs-lookup"><span data-stu-id="372bb-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services, or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="372bb-106">En fonction du moment où vous déployez le client d’administration et de surveillance de BitLocker, vous pouvez activer le chiffrement BitLocker sur un ordinateur de votre organisation avant que l’utilisateur final ne reçoive l’ordinateur ou après la configuration de la stratégie de groupe et le déploiement du logiciel client MBAM à l’aide d’un système de déploiement de logiciels d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="372bb-106">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring Client, you can enable BitLocker encryption on a computer in your organization either before the end user receives the computer or afterwards by configuring Group Policy and deploying the MBAM Client software by using an enterprise software deployment system.</span></span>

## <span data-ttu-id="372bb-107">Déployer le client MBAM sur un ordinateur portable ou de bureau</span><span class="sxs-lookup"><span data-stu-id="372bb-107">Deploy the MBAM Client to Desktop or Laptop Computers</span></span>


<span data-ttu-id="372bb-108">Après avoir configuré une stratégie de groupe, vous pouvez utiliser un produit système de déploiement de logiciels d’entreprise, tel que Microsoft System Center Configuration Manager 2012 ou services de domaine Active Directory (AD FS) pour déployer les fichiers du programme d’installation du client MBAM sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="372bb-108">After configuring Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager 2012 or Active Directory Domain Services to deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="372bb-109">Vous pouvez déployer le client à 32 l’aide des fichiers MbamClientSetup.exe de MBAMClient.msi ou 64 bits, ou des fichiers 32 ou 64 bits, fournis avec le logiciel MBAM.</span><span class="sxs-lookup"><span data-stu-id="372bb-109">You can deploy the client by using either the 32-bit or 64-bit MbamClientSetup.exe files, or the 32-bit or 64-bit MBAMClient.msi files, which are provided with the MBAM software.</span></span> <span data-ttu-id="372bb-110">Pour plus d’informations sur le déploiement d’objets de stratégie de groupe MBAM, voir [déploiement d’objets de stratégie de groupe MBAM 2,0](deploying-mbam-20-group-policy-objects-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="372bb-110">For more information about deploying MBAM Group Policy Objects, see [Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md).</span></span>

[<span data-ttu-id="372bb-111">Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables</span><span class="sxs-lookup"><span data-stu-id="372bb-111">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-2.md)

## <span data-ttu-id="372bb-112">Déploiement du client MBAM dans le cadre d’un déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="372bb-112">Deploy the MBAM Client as Part of a Windows Deployment</span></span>


<span data-ttu-id="372bb-113">Dans les organisations sur lesquelles les ordinateurs sont reçus et configurés de manière centralisée, vous pouvez installer le client MBAM pour gérer le chiffrement BitLocker sur chaque ordinateur avant d’y écrire des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="372bb-113">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="372bb-114">L’avantage de ce processus est que chaque ordinateur est alors conforme au chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="372bb-114">The benefit of this process is that every computer is then BitLocker encryption compliant.</span></span> <span data-ttu-id="372bb-115">Cette méthode ne repose pas sur l’action de l’utilisateur, car l’administrateur l’a déjà crypté.</span><span class="sxs-lookup"><span data-stu-id="372bb-115">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="372bb-116">Une supposition essentielle pour ce scénario est que la stratégie de l’organisation installe une image Windows d’entreprise avant que l’ordinateur ne soit remis à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="372bb-116">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span> <span data-ttu-id="372bb-117">Si la stratégie de groupe a été configurée pour exiger un code confidentiel, les utilisateurs sont invités à définir un code confidentiel après réception de la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="372bb-117">If the Group Policy has been configured to require a PIN, users are prompted to set a PIN after they receive the Group Policy.</span></span>

[<span data-ttu-id="372bb-118">Déploiement du client MBAM dans le cadre d'un déploiement de Windows</span><span class="sxs-lookup"><span data-stu-id="372bb-118">How to Deploy the MBAM Client as Part of a Windows Deployment</span></span>](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-2.md)

## <span data-ttu-id="372bb-119">Utilisation d'une ligne de commande pour installer le client MBAM</span><span class="sxs-lookup"><span data-stu-id="372bb-119">How to Use a Command Line to Install the MBAM Client</span></span>


<span data-ttu-id="372bb-120">Cette section explique comment installer le client MBAM à l’aide d’une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="372bb-120">This section explains how to install the MBAM Client by using a command line.</span></span>

[<span data-ttu-id="372bb-121">Utilisation d'une ligne de commande pour installer le client MBAM</span><span class="sxs-lookup"><span data-stu-id="372bb-121">How to Use a Command Line to Install the MBAM Client</span></span>](how-to-use-a-command-line-to-install-the-mbam-client.md)

## <span data-ttu-id="372bb-122">Autres ressources pour le déploiement du client MBAM</span><span class="sxs-lookup"><span data-stu-id="372bb-122">Other Resources for Deploying the MBAM Client</span></span>


<span data-ttu-id="372bb-123">[Déploiement de MBAM 2,0](deploying-mbam-20-mbam-2.md)[planification pour le déploiement du client 2,0 MBAM](planning-for-mbam-20-client-deployment-mbam-2.md)</span><span class="sxs-lookup"><span data-stu-id="372bb-123">[Deploying MBAM 2.0](deploying-mbam-20-mbam-2.md)[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)</span></span>

 

 





