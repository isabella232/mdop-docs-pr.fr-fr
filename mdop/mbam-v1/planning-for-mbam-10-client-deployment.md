---
title: Planification du déploiement de clients MBAM1.0
description: Planification du déploiement de clients MBAM1.0
author: dansimp
ms.assetid: 3af2e7f3-134b-4ab9-9847-b07474ca6ac3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d58d6420febd2da9ee9cd4074fc8b5870285b0b4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811418"
---
# <span data-ttu-id="2bc5e-103">Planification du déploiement de clients MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="2bc5e-103">Planning for MBAM 1.0 Client Deployment</span></span>


<span data-ttu-id="2bc5e-104">Selon la manière dont vous déployez le client Microsoft BitLocker Administration and Analysis (MBAM), vous pouvez activer le chiffrement BitLocker sur un ordinateur de votre organisation avant que l’utilisateur final ne reçoive l’ordinateur ou après.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client, you can enable BitLocker encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="2bc5e-105">Pour activer le chiffrement BitLocker après que l’utilisateur final a reçu l’ordinateur, configurez une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-105">To enable BitLocker encryption after the end user receives the computer, configure Group Policy.</span></span> <span data-ttu-id="2bc5e-106">Pour activer le chiffrement BitLocker avant la réception de l’ordinateur par l’utilisateur final, déployez le logiciel client MBAM à l’aide d’un système de déploiement de logiciels d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-106">To enable BitLocker encryption before the end user receives the computer, deploy the MBAM Client software by using an enterprise software deployment system.</span></span>

<span data-ttu-id="2bc5e-107">Vous pouvez appliquer l’une ou l’autre des méthodes au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-107">You can use one or both methods in your organization.</span></span> <span data-ttu-id="2bc5e-108">Si vous utilisez les deux méthodes, vous pouvez améliorer la conformité, la création de rapports et la prise en charge des récupérations de clés.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-108">If you use both methods, you can improve compliance, reporting, and key recovery support.</span></span>

<span data-ttu-id="2bc5e-109">**Remarques**  Pour vérifier la configuration système requise pour le client MBAM, voir [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="2bc5e-109">**Note** To review the MBAM Client system requirements, see [MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md).</span></span>

 

## <span data-ttu-id="2bc5e-110">Déploiement du client MBAM pour activer le chiffrement BitLocker après la distribution ordinateur aux utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="2bc5e-110">Deploying the MBAM Client to enable BitLocker encryption after computer distribution to end users</span></span>


<span data-ttu-id="2bc5e-111">Après avoir configuré la stratégie de groupe, vous pouvez utiliser un produit système de déploiement de logiciels d’entreprise, tel que Microsoft System Center Configuration Manager 2012 ou services de domaine Active Directory, pour déployer les fichiers Windows Installer du client MBAM sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-111">After you configure the Group Policy, you can use an enterprise software deployment system product, such as Microsoft System Center Configuration Manager 2012 or Active Directory Domain Services, to deploy the MBAM Client installation Windows Installer files to the target computers.</span></span> <span data-ttu-id="2bc5e-112">Les deux fichiers du programme d’installation du client MBAM sont MBAMClient-64bit.msi et MBAMClient-32bit.msi fournis avec le logiciel MBAM.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-112">The two MBAM Client installation Windows Installer files are MBAMClient-64bit.msi and MBAMClient-32bit.msi, which are provided with the MBAM software.</span></span> <span data-ttu-id="2bc5e-113">Pour plus d’informations sur le déploiement d’objets de stratégie de groupe MBAM, voir [déploiement d’objets de stratégie de groupe MBAM 1,0](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2bc5e-113">For more information about how to deploy MBAM Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

<span data-ttu-id="2bc5e-114">Lorsque vous déployez le client MBAM, après avoir distribué les ordinateurs aux utilisateurs finaux, les utilisateurs finaux sont invités à chiffrer leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-114">When you deploy the MBAM Client, after you distribute the computers to end users, the end users are prompted to encrypt their computers.</span></span> <span data-ttu-id="2bc5e-115">Cela permet à MBAM de collecter les données, d’inclure le code confidentiel et le mot de passe, puis de commencer le processus de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-115">This lets MBAM collect the data, to include the PIN and password, and then begin the encryption process.</span></span>

<span data-ttu-id="2bc5e-116">**Remarques**  Dans le cas présent, l’utilisateur est invité à activer et initialiser le processeur du module de plateforme sécurisée, s’il n’a pas encore été activé.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-116">**Note** In this approach, users are prompted to activate and initialize the Trusted Platform Module (TPM) chip, if it has not been previously activated.</span></span>

 

## <span data-ttu-id="2bc5e-117">Utilisation du client MBAM pour activer le chiffrement BitLocker avant la distribution d’ordinateurs aux utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="2bc5e-117">Using the MBAM Client to enable BitLocker encryption before computer distribution to end users</span></span>


<span data-ttu-id="2bc5e-118">Dans les organisations sur lesquelles les ordinateurs sont reçus et configurés de manière centralisée, vous pouvez installer le client MBAM pour gérer le chiffrement BitLocker sur chaque ordinateur avant d’écrire des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-118">In organizations where computers are received and configured centrally, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written on it.</span></span> <span data-ttu-id="2bc5e-119">L’avantage de ce processus est que tous les ordinateurs seront alors conformes au chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-119">The benefit of this process is that every computer will then be compliant with the BitLocker encryption.</span></span> <span data-ttu-id="2bc5e-120">Cette méthode ne repose pas sur l’action de l’utilisateur, car l’administrateur l’a déjà crypté.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-120">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="2bc5e-121">Une supposition essentielle pour ce scénario est que la stratégie de l’organisation installe une image Windows d’entreprise avant que l’ordinateur ne soit remis à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

<span data-ttu-id="2bc5e-122">Si votre organisation souhaite utiliser le module de plateforme sécurisée pour chiffrer les ordinateurs, l’administrateur doit chiffrer le volume du système d’exploitation de l’ordinateur avec le protecteur de module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-122">If your organization wants to use (TPM) to encrypt computers, the administrator must encrypt the operating system volume of the computer with TPM protector.</span></span> <span data-ttu-id="2bc5e-123">Si votre organisation veut utiliser le processeur du TPM et un protecteur de code confidentiel, l’administrateur doit chiffrer le volume du système avec le protecteur de TPM, puis les utilisateurs sélectionner un code confidentiel lors de la première connexion.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-123">If your organization wants to use the TPM chip and a PIN protector, the administrator must encrypt the system volume with the TPM protector, and then the users select a PIN the first time they log on.</span></span> <span data-ttu-id="2bc5e-124">Si votre organisation décide d’utiliser uniquement le protecteur de punaise, l’administrateur n’a pas besoin de chiffrer le volume d’abord.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-124">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="2bc5e-125">Lorsque l’utilisateur se connecte sur son ordinateur, MBAM lui demande de fournir un code confidentiel ou un code confidentiel et un mot de passe qu’il utilisera lors du redémarrage de son ordinateur ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-125">When users log on their computers, MBAM prompts them to provide a PIN or a PIN and a password that they will use when they restart their computer later.</span></span>

<span data-ttu-id="2bc5e-126">**Remarques**  L’une des options de protection de module de plateforme sécurisée doit permettre à l’administrateur d’accepter l’invite du BIOS pour activer et initialiser le TPM avant de l’envoyer à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2bc5e-126">**Note** The TPM protector option requires for the administrator to accept the BIOS prompt to activate and initialize the TPM before delivering the computer to the user.</span></span>

 

## <span data-ttu-id="2bc5e-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2bc5e-127">Related topics</span></span>


[<span data-ttu-id="2bc5e-128">Planification du déploiement de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="2bc5e-128">Planning to Deploy MBAM 1.0</span></span>](planning-to-deploy-mbam-10.md)

[<span data-ttu-id="2bc5e-129">Déploiement du client MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="2bc5e-129">Deploying the MBAM 1.0 Client</span></span>](deploying-the-mbam-10-client.md)

 

 





