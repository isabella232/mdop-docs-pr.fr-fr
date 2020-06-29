---
title: Déploiement du client MBAM2.5
description: Déploiement du client MBAM2.5
author: dansimp
ms.assetid: 0a96a0ee-f280-49d9-a244-88f4147fe9fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 375af8966c8e66a58baec5065d065891187899fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811658"
---
# <span data-ttu-id="3c91b-103">Déploiement du client MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="3c91b-103">Deploying the MBAM 2.5 Client</span></span>


<span data-ttu-id="3c91b-104">Le logiciel client Microsoft BitLocker Administration and Analysis (MBAM) permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="3c91b-104">The Microsoft BitLocker Administration and Monitoring (MBAM) Client software enables administrators to enforce and monitor BitLocker Drive Encryption on computers in the enterprise.</span></span> <span data-ttu-id="3c91b-105">Le client BitLocker peut être intégré à une organisation en déployant le client par le biais d’un système de distribution de logiciels électronique, tel que les services de domaine Active Directory (AD FS), ou en chiffrant directement les ordinateurs clients dans le cadre du processus d’imagerie initial.</span><span class="sxs-lookup"><span data-stu-id="3c91b-105">The BitLocker client can be integrated into an organization by deploying the client through an electronic software distribution system, such as Active Directory Domain Services, or by directly encrypting the client computers as part of the initial imaging process.</span></span>

<span data-ttu-id="3c91b-106">En fonction du moment où vous déployez le logiciel client d’administration et de surveillance de BitLocker, vous pouvez activer le chiffrement de lecteur BitLocker sur un ordinateur de votre organisation avant que l’utilisateur final ne reçoive l’ordinateur ou après la configuration de la stratégie de groupe et le déploiement du logiciel client MBAM à l’aide d’un système de déploiement de logiciels d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="3c91b-106">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring Client software, you can enable BitLocker Drive Encryption on a computer in your organization either before the end user receives the computer or afterwards by configuring Group Policy and deploying the MBAM Client software by using an enterprise software deployment system.</span></span>

## <span data-ttu-id="3c91b-107">Déployer le client MBAM sur un ordinateur portable ou de bureau</span><span class="sxs-lookup"><span data-stu-id="3c91b-107">Deploy the MBAM Client to desktop or laptop computers</span></span>


<span data-ttu-id="3c91b-108">Après avoir configuré les paramètres de stratégie de groupe, vous pouvez utiliser un produit système de déploiement de logiciels d’entreprise tel que MicrosoftSystemCenter2012 ConfigurationManager ou les services de domaine Active Directory pour déployer les fichiers Windows Installer du client MBAM sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="3c91b-108">After configuring Group Policy settings, you can use an enterprise software deployment system product like MicrosoftSystemCenter2012 ConfigurationManager or Active Directory Domain Services to deploy the MBAM Client installation Windows Installer files to target computers.</span></span> <span data-ttu-id="3c91b-109">Vous pouvez utiliser les fichiers MbamClientSetup.exe de la 32 ou de 64 bits ou les fichiers MBAMClient.msi 32 ou 64 bits, fourni avec le logiciel client MBAM.</span><span class="sxs-lookup"><span data-stu-id="3c91b-109">You can use either the 32-bit or 64-bit MbamClientSetup.exe files or the 32-bit or 64-bit MBAMClient.msi files, which are provided with the MBAM Client software.</span></span> <span data-ttu-id="3c91b-110">Pour plus d’informations sur le déploiement des paramètres de stratégie de groupe MBAM, voir [déploiement d’objets de stratégie de groupe MBAM 2,5](deploying-mbam-25-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3c91b-110">For more information about deploying MBAM Group Policy settings, see [Deploying MBAM 2.5 Group Policy Objects](deploying-mbam-25-group-policy-objects.md).</span></span>

<span data-ttu-id="3c91b-111">**Remarques**  À partir de MBAM 2,5 SP1, un MSI distinct n’est plus inclus dans le produit MBAM.</span><span class="sxs-lookup"><span data-stu-id="3c91b-111">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="3c91b-112">Toutefois, vous pouvez extraire le MSI du fichier exécutable (. exe) qui est inclus dans le produit.</span><span class="sxs-lookup"><span data-stu-id="3c91b-112">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

 

[<span data-ttu-id="3c91b-113">Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables</span><span class="sxs-lookup"><span data-stu-id="3c91b-113">How to Deploy the MBAM Client to Desktop or Laptop Computers</span></span>](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25.md)

## <span data-ttu-id="3c91b-114">Déploiement du client MBAM dans le cadre d’un déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="3c91b-114">Deploy the MBAM Client as part of a Windows deployment</span></span>


<span data-ttu-id="3c91b-115">Dans les organisations sur lesquelles les ordinateurs sont reçus et configurés de manière centralisée, vous pouvez installer le client MBAM pour gérer le chiffrement de lecteur BitLocker sur chaque ordinateur avant d’y écrire des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c91b-115">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker Drive Encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="3c91b-116">L’avantage de ce processus est que chaque ordinateur est alors conforme à la norme de chiffrement du lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3c91b-116">The benefit of this process is that every computer is then BitLocker Drive Encryption-compliant.</span></span> <span data-ttu-id="3c91b-117">Cette méthode ne repose pas sur l’action de l’utilisateur, car l’administrateur l’a déjà crypté.</span><span class="sxs-lookup"><span data-stu-id="3c91b-117">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="3c91b-118">Une supposition essentielle pour ce scénario est que la stratégie de l’organisation installe une image Windows d’entreprise avant que l’ordinateur ne soit remis à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c91b-118">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span> <span data-ttu-id="3c91b-119">Si les paramètres de stratégie de groupe ont été configurés pour exiger un code confidentiel, les utilisateurs sont invités à définir un code confidentiel après réception de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="3c91b-119">If the Group Policy settings has been configured to require a PIN, users are prompted to set a PIN after they receive the policy.</span></span>

[<span data-ttu-id="3c91b-120">Comment activer BitLocker à l'aide de MBAM dans le cadre d'un déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="3c91b-120">How to Enable BitLocker by Using MBAM as Part of a Windows Deployment</span></span>](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

## <span data-ttu-id="3c91b-121">Déploiement du client MBAM à l’aide d’une ligne de commande</span><span class="sxs-lookup"><span data-stu-id="3c91b-121">How to deploy the MBAM Client by using a command line</span></span>


<span data-ttu-id="3c91b-122">Cette section explique comment installer le client MBAM à l’aide d’une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3c91b-122">This section explains how to install the MBAM Client by using a command line.</span></span>

[<span data-ttu-id="3c91b-123">Déploiement du client MBAM àl'aide d'une ligne de commande</span><span class="sxs-lookup"><span data-stu-id="3c91b-123">How to Deploy the MBAM Client by Using a Command Line</span></span>](how-to-deploy-the-mbam-client-by-using-a-command-line.md)

## <span data-ttu-id="3c91b-124">Autres ressources pour le déploiement du client MBAM</span><span class="sxs-lookup"><span data-stu-id="3c91b-124">Other resources for deploying the MBAM Client</span></span>


[<span data-ttu-id="3c91b-125">Déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="3c91b-125">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)



## <span data-ttu-id="3c91b-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3c91b-126">Related topics</span></span>


[<span data-ttu-id="3c91b-127">Déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="3c91b-127">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="3c91b-128">Planification de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="3c91b-128">Planning for MBAM 2.5</span></span>](planning-for-mbam-25.md)

 
## <span data-ttu-id="3c91b-129">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="3c91b-129">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="3c91b-130">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="3c91b-130">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="3c91b-131">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="3c91b-131">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





