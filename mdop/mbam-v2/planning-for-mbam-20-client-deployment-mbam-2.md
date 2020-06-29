---
title: Planification du déploiement de clients MBAM2.0
description: Planification du déploiement de clients MBAM2.0
author: dansimp
ms.assetid: 3a92cf29-092f-4cad-bdfa-d5f6aafe554b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c3a7383188d4064247d8e493c8e6125fc24a1d2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804363"
---
# <span data-ttu-id="55878-103">Planification du déploiement de clients MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="55878-103">Planning for MBAM 2.0 Client Deployment</span></span>


<span data-ttu-id="55878-104">En fonction du moment où vous déployez le client Microsoft BitLocker Administration and Analysis (MBAM), vous pouvez activer le chiffrement de lecteur BitLocker sur un ordinateur de votre organisation avant que l’utilisateur final ne reçoive l’ordinateur ou après.</span><span class="sxs-lookup"><span data-stu-id="55878-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client, you can enable BitLocker drive encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="55878-105">Pour le mode autonome MBAM et les topologies du gestionnaire de configuration, vous devez configurer des paramètres de stratégie de groupe pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="55878-105">For both the MBAM Stand-alone and the Configuration Manager topologies, you have to configure Group Policy settings for MBAM.</span></span>

<span data-ttu-id="55878-106">Si vous utilisez la topologie autonome MBAM, nous vous recommandons d’utiliser un système de déploiement de logiciels d’entreprise pour déployer le logiciel client MBAM sur les ordinateurs des utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="55878-106">If you are using the MBAM Stand-alone topology, it is recommended that you use an enterprise software deployment system to deploy the MBAM Client software to end-user computers.</span></span>

<span data-ttu-id="55878-107">Si vous déployez MBAM avec la topologie Configuration Manager, vous pouvez utiliser Configuration Manager pour déployer le logiciel client MBAM sur les ordinateurs des utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="55878-107">If you deploy MBAM with the Configuration Manager topology, you can use Configuration Manager to deploy the MBAM Client software to end-user computers.</span></span> <span data-ttu-id="55878-108">Dans Configuration Manager, l’installation MBAM crée une collection d’ordinateurs que MBAM peut gérer.</span><span class="sxs-lookup"><span data-stu-id="55878-108">In Configuration Manager, the MBAM installation creates a collection of computers that MBAM can manage.</span></span> <span data-ttu-id="55878-109">Cette collection inclut les stations de travail et les appareils qui n’ont pas de module de plateforme sécurisée (TPM), mais qui exécutent Windows 8.</span><span class="sxs-lookup"><span data-stu-id="55878-109">This collection includes workstations and devices that do not have a Trusted Platform Module (TPM), but that are running Windows 8.</span></span>

<span data-ttu-id="55878-110">**Remarques**  Windows to Go n’est pas pris en charge pour les installations intégrées de Configuration Manager du MBAM si vous utilisez Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="55878-110">**Note** Windows To Go is not supported for integrated Configuration Manager installations of MBAM if you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="55878-111">Déploiement du client MBAM pour activer le chiffrement BitLocker après la distribution ordinateur aux utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="55878-111">Deploying the MBAM Client to Enable BitLocker Encryption After Computer Distribution to End Users</span></span>


<span data-ttu-id="55878-112">Après avoir configuré une stratégie de groupe, vous pouvez utiliser un produit système de déploiement de logiciels d’entreprise, tel que Microsoft System Center Configuration Manager ou les services de domaine Active Directory (AD DS) pour déployer les fichiers Windows Installer de l’installation du client MBAM sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="55878-112">After you configure Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager or Active Directory Domain Services (AD DS) to deploy the Windows Installer files of the MBAM Client installation to target computers.</span></span> <span data-ttu-id="55878-113">Pour déployer le client MBAM, vous pouvez utiliser les fichiers MbamClientSetup.exe 32 ou 64 bits ou MBAMClient.msi, qui sont fournis avec le logiciel MBAM.</span><span class="sxs-lookup"><span data-stu-id="55878-113">To deploy the MBAM Client, you can use either the 32-bit or 64-bit MbamClientSetup.exe files or MBAMClient.msi files, which are provided with the MBAM software.</span></span>

<span data-ttu-id="55878-114">Lorsque vous déployez le client MBAM après distribution d’ordinateurs sur des ordinateurs clients, les utilisateurs finaux sont invités à chiffrer leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="55878-114">When you deploy the MBAM Client after you distribute computers to client computers, end users are prompted to encrypt their computer.</span></span> <span data-ttu-id="55878-115">Cela permet à MBAM de collecter les données, y compris le code confidentiel et le mot de passe, puis de commencer le processus de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="55878-115">This enables MBAM to collect the data, which includes the PIN and password, and then to begin the encryption process.</span></span>

<span data-ttu-id="55878-116">**Remarques**  Dans cette approche, les utilisateurs disposant d’ordinateurs dotés d’un processeur de TPM sont invités à activer et initialiser le processeur du TPM si la puce n’a pas été activée auparavant.</span><span class="sxs-lookup"><span data-stu-id="55878-116">**Note** In this approach, users who have computers with a TPM chip are prompted to activate and initialize the TPM chip if the chip has not been previously activated.</span></span>

 

## <span data-ttu-id="55878-117">Utilisation du client MBAM pour activer le chiffrement BitLocker avant la distribution d’ordinateurs aux utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="55878-117">Using the MBAM Client to Enable BitLocker Encryption Before Computer Distribution to End Users</span></span>


<span data-ttu-id="55878-118">Dans les organisations sur lesquelles les ordinateurs sont reçus et configurés de manière centralisée, et sur lequel ils disposent d’un processeur de TPM compatible, vous pouvez installer le client MBAM pour gérer le chiffrement de BitLocker sur chaque ordinateur avant d’y écrire des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55878-118">In organizations where computers are received and configured centrally, and where computers have a compliant TPM chip, you can install the MBAM Client to manage BitLocker encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="55878-119">L’avantage de ce processus est que tous les ordinateurs seront alors conformes au chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="55878-119">The benefit of this process is that every computer will then be BitLocker encryption-compliant.</span></span> <span data-ttu-id="55878-120">Cette méthode ne repose pas sur l’action de l’utilisateur, car l’administrateur l’a déjà crypté.</span><span class="sxs-lookup"><span data-stu-id="55878-120">This method does not rely on user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="55878-121">Une supposition essentielle pour ce scénario est que la stratégie de l’organisation installe une image Windows d’entreprise avant que l’ordinateur ne soit remis à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55878-121">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the user.</span></span>

<span data-ttu-id="55878-122">Si votre organisation veut utiliser le processeur du TPM pour chiffrer les ordinateurs, l’administrateur ajoute le protecteur du TPM pour chiffrer le volume du système d’exploitation de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="55878-122">If your organization wants to use the TPM chip to encrypt computers, the administrator adds the TPM protector to encrypt the operating system volume of the computer.</span></span> <span data-ttu-id="55878-123">Si votre organisation veut utiliser le processeur du TPM et un protecteur de code confidentiel, l’administrateur chiffre le volume du système d’exploitation à l’aide du protecteur du module de plateforme sécurisée, puis les utilisateurs sélectionnent un code confidentiel lors de la première connexion.</span><span class="sxs-lookup"><span data-stu-id="55878-123">If your organization wants to use the TPM chip and a PIN protector, the administrator encrypts the operating system volume with the TPM protector, and then users select a PIN when they log on for the first time.</span></span> <span data-ttu-id="55878-124">Si votre organisation décide d’utiliser uniquement le protecteur de punaise, l’administrateur n’a pas besoin de chiffrer le volume d’abord.</span><span class="sxs-lookup"><span data-stu-id="55878-124">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="55878-125">Lorsque les utilisateurs ouvrent une session, l’administration et la surveillance de BitLocker vous invitent à fournir un code confidentiel, ou un code confidentiel et un mot de passe à utiliser pour les redémarrages ultérieures de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="55878-125">When users log on, Microsoft BitLocker Administration and Monitoring prompts them to provide a PIN, or a PIN and password to be used on later computer restarts.</span></span>

<span data-ttu-id="55878-126">**Remarques**  L’option de protection de module de plateforme sécurisée exige que l’administrateur accepte l’invite du BIOS pour activer et initialiser le module de plateforme sécurisée avant qu’il soit remis à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55878-126">**Note** The TPM protector option requires the administrator to accept the BIOS prompt to activate and initialize the TPM before the computer is delivered to the user.</span></span>

 

## <span data-ttu-id="55878-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55878-127">Related topics</span></span>


[<span data-ttu-id="55878-128">Planification du déploiement de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="55878-128">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)

[<span data-ttu-id="55878-129">Déploiement du client MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="55878-129">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)

 

 





