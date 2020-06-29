---
title: Planification du déploiement de clients MBAM2.5
description: Planification du déploiement de clients MBAM2.5
author: dansimp
ms.assetid: 23c89976-af24-4753-9412-ce0ea42d1964
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ff03b58da0985b2f57308c99a9bc15f4a0554623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811489"
---
# <span data-ttu-id="8618b-103">Planification du déploiement de clients MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8618b-103">Planning for MBAM 2.5 Client Deployment</span></span>


<span data-ttu-id="8618b-104">Selon la manière dont vous déployez le logiciel client Microsoft BitLocker Administration and Analysis (MBAM), vous pouvez activer le chiffrement de lecteur BitLocker sur un ordinateur de votre organisation avant que l’utilisateur final ne reçoive l’ordinateur ou après.</span><span class="sxs-lookup"><span data-stu-id="8618b-104">Depending on when you deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client software, you can enable BitLocker Drive Encryption on a computer in your organization either before the end user receives the computer or afterwards.</span></span> <span data-ttu-id="8618b-105">Pour les topologies d’intégration autonomes MBAM et System Center Configuration Manager, vous devez configurer des paramètres de stratégie de groupe pour MBAM.</span><span class="sxs-lookup"><span data-stu-id="8618b-105">For both the MBAM Stand-alone and the System Center Configuration Manager Integration topologies, you have to configure Group Policy settings for MBAM.</span></span>

<span data-ttu-id="8618b-106">Si vous utilisez la topologie autonome MBAM, nous vous recommandons d’utiliser un système de déploiement de logiciels d’entreprise pour déployer le logiciel client MBAM sur les ordinateurs des utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="8618b-106">If you are using the MBAM Stand-alone topology, we recommend that you use an enterprise software deployment system to deploy the MBAM Client software to end-user computers.</span></span>

<span data-ttu-id="8618b-107">Si vous déployez MBAM avec la topologie d’intégration de Configuration Manager, vous pouvez utiliser Configuration Manager pour déployer le logiciel client MBAM sur les ordinateurs des utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="8618b-107">If you deploy MBAM with the Configuration Manager Integration topology, you can use Configuration Manager to deploy the MBAM Client software to end-user computers.</span></span> <span data-ttu-id="8618b-108">Dans Configuration Manager, l’installation MBAM crée une collection d’ordinateurs que MBAM peut gérer.</span><span class="sxs-lookup"><span data-stu-id="8618b-108">In Configuration Manager, the MBAM installation creates a collection of computers that MBAM can manage.</span></span> <span data-ttu-id="8618b-109">Cette collection inclut les stations de travail et les appareils qui n’ont pas de module de plateforme sécurisée (TPM), mais qui exécutent Windows 8, Windows 8,1 ou Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8618b-109">This collection includes workstations and devices that do not have a Trusted Platform Module (TPM), but that are running Windows 8, Windows 8.1, or Windows 10.</span></span>

<span data-ttu-id="8618b-110">**Remarques**  Windows to Go n’est pas pris en charge pour l’installation de la topologie d’intégration de Configuration Manager lorsque vous utilisez Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="8618b-110">**Note** Windows To Go is not supported for the Configuration Manager Integration topology installation when you are using Configuration Manager 2007.</span></span>

 

## <span data-ttu-id="8618b-111">Déploiement du client MBAM pour activer le chiffrement de lecteur BitLocker après la distribution d’ordinateur aux utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="8618b-111">Deploying the MBAM Client to enable BitLocker Drive Encryption after computer distribution to end users</span></span>


<span data-ttu-id="8618b-112">Après avoir configuré une stratégie de groupe, vous pouvez utiliser un produit système de déploiement de logiciels d’entreprise, tel que Microsoft System Center Configuration Manager ou les services de domaine Active Directory (AD DS) pour déployer les fichiers Windows Installer de l’installation du client MBAM sur les ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="8618b-112">After you configure Group Policy, you can use an enterprise software deployment system product like Microsoft System Center Configuration Manager or Active Directory Domain Services (AD DS) to deploy the Windows Installer files of the MBAM Client installation to target computers.</span></span> <span data-ttu-id="8618b-113">Pour déployer le client MBAM, vous pouvez utiliser 32 les fichiers MbamClientSetup.exe MBAMClient.msi ou 64 bits ou les fichiers de fournis avec le logiciel client MBAM.</span><span class="sxs-lookup"><span data-stu-id="8618b-113">To deploy the MBAM Client, you can use either the 32-bit or 64-bit MbamClientSetup.exe files or MBAMClient.msi files, which are provided with the MBAM Client software.</span></span>

<span data-ttu-id="8618b-114">**Remarques**  À partir de MBAM 2,5 SP1, un MSI distinct n’est plus inclus dans le produit MBAM.</span><span class="sxs-lookup"><span data-stu-id="8618b-114">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="8618b-115">Toutefois, vous pouvez extraire le MSI du fichier exécutable (. exe) qui est inclus dans le produit.</span><span class="sxs-lookup"><span data-stu-id="8618b-115">However, you can extract the MSI from the executable file (.exe) that is included with the product.</span></span>

 

<span data-ttu-id="8618b-116">Lorsque vous déployez le client MBAM après distribution d’ordinateurs sur des ordinateurs clients, les utilisateurs finaux sont invités à chiffrer leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8618b-116">When you deploy the MBAM Client after you distribute computers to client computers, end users are prompted to encrypt their computer.</span></span> <span data-ttu-id="8618b-117">Cette action permet à MBAM de collecter les données (code confidentiel et mot de passe (si nécessaire), puis de commencer le processus de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="8618b-117">This action enables MBAM to collect the data, which includes the PIN and password (if required by policy), and then to begin the encryption process.</span></span>

<span data-ttu-id="8618b-118">**Remarques**  Dans cette approche, les utilisateurs finaux disposant d’ordinateurs dotés d’un processeur de TPM sont invités à activer et initialiser le processeur du TPM si la puce n’a pas été activée auparavant.</span><span class="sxs-lookup"><span data-stu-id="8618b-118">**Note** In this approach, end users who have computers with a TPM chip are prompted to activate and initialize the TPM chip if the chip has not been previously activated.</span></span>

 

## <span data-ttu-id="8618b-119">Utilisation du client MBAM pour activer le chiffrement de lecteur BitLocker avant la distribution d’ordinateurs aux utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="8618b-119">Using the MBAM Client to enable BitLocker Drive Encryption before computer distribution to end users</span></span>


<span data-ttu-id="8618b-120">Dans les organisations sur lesquelles les ordinateurs sont reçus et configurés de manière centralisée, et sur lequel les ordinateurs sont équipés d’un processeur de TPM compatible, vous pouvez utiliser le client MBAM pour gérer le chiffrement de lecteur BitLocker sur chaque ordinateur avant d’y écrire des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8618b-120">In organizations where computers are received and configured centrally, and where computers have a compliant TPM chip, you can use the MBAM Client to manage BitLocker Drive Encryption on each computer before any user data is written to it.</span></span> <span data-ttu-id="8618b-121">L’avantage de ce processus est que chaque ordinateur est alors conforme.</span><span class="sxs-lookup"><span data-stu-id="8618b-121">The benefit of this process is that every computer is then compliant.</span></span> <span data-ttu-id="8618b-122">Cette méthode ne repose pas sur l’action de l’utilisateur final, car l’administrateur l’a déjà chiffrée.</span><span class="sxs-lookup"><span data-stu-id="8618b-122">This method does not rely on end-user action because the administrator has already encrypted the computer.</span></span> <span data-ttu-id="8618b-123">Une supposition essentielle pour ce scénario est que la stratégie de l’organisation installe une image Windows d’entreprise avant que l’ordinateur ne soit remis à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="8618b-123">A key assumption for this scenario is that the policy of the organization installs a corporate Windows image before the computer is delivered to the end user.</span></span>

<span data-ttu-id="8618b-124">Si votre organisation veut utiliser le processeur du TPM pour chiffrer les ordinateurs, l’administrateur ajoute le protecteur du TPM pour chiffrer le volume du système d’exploitation de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8618b-124">If your organization wants to use the TPM chip to encrypt computers, the administrator adds the TPM protector to encrypt the operating system volume of the computer.</span></span> <span data-ttu-id="8618b-125">Si votre organisation veut utiliser le processeur du TPM et un protecteur de code confidentiel, l’administrateur chiffre le volume du système d’exploitation à l’aide du protecteur du module de plateforme sécurisée, puis les utilisateurs finaux sélectionnent un code confidentiel lors de la première connexion.</span><span class="sxs-lookup"><span data-stu-id="8618b-125">If your organization wants to use the TPM chip and a PIN protector, the administrator encrypts the operating system volume with the TPM protector, and then end users select a PIN when they log on for the first time.</span></span> <span data-ttu-id="8618b-126">Si votre organisation décide d’utiliser uniquement le protecteur de punaise, l’administrateur n’a pas besoin de chiffrer le volume d’abord.</span><span class="sxs-lookup"><span data-stu-id="8618b-126">If your organization decides to use only the PIN protector, the administrator does not have to encrypt the volume first.</span></span> <span data-ttu-id="8618b-127">Lorsque les utilisateurs finaux se connectent, l’administration et la surveillance de BitLocker vous invitent à entrer un code confidentiel, ou un code confidentiel et un mot de passe à utiliser sur un redémarrage d’ordinateur ultérieur.</span><span class="sxs-lookup"><span data-stu-id="8618b-127">When end users log on, Microsoft BitLocker Administration and Monitoring prompts them to provide a PIN, or a PIN and password to be used on later computer restarts.</span></span>

<span data-ttu-id="8618b-128">**Remarques**  Par le biais de l’option de protection de TPM, l’administrateur doit accepter l’invite du BIOS pour activer et initialiser le module de plateforme sécurisée avant que l’ordinateur ne soit remis à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="8618b-128">**Note** The TPM protector option requires the administrator to accept the BIOS prompt to activate and initialize the TPM before the computer is delivered to the end user.</span></span>

 

## <span data-ttu-id="8618b-129">Prise en charge du client MBAM pour les disques durs chiffrés</span><span class="sxs-lookup"><span data-stu-id="8618b-129">MBAM Client support for Encrypted Hard Drives</span></span>


<span data-ttu-id="8618b-130">MBAM prend en charge BitLocker sur les disques durs chiffrés qui satisfont les exigences de spécification TCG pour Opal ainsi que les normes IEEE 1667.</span><span class="sxs-lookup"><span data-stu-id="8618b-130">MBAM supports BitLocker on Encrypted Hard Drives that meet TCG specification requirements for Opal as well as IEEE 1667 standards.</span></span> <span data-ttu-id="8618b-131">Lorsque BitLocker est activé sur ces appareils, il génère des clés et effectue des tâches de gestion sur le lecteur chiffré.</span><span class="sxs-lookup"><span data-stu-id="8618b-131">When BitLocker is enabled on these devices, it will generate keys and perform management functions on the encrypted drive.</span></span> <span data-ttu-id="8618b-132">Pour plus d’informations, voir [disque dur chiffré](https://technet.microsoft.com/library/hh831627.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8618b-132">See [Encrypted Hard Drive](https://technet.microsoft.com/library/hh831627.aspx) for more information.</span></span>


## <span data-ttu-id="8618b-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8618b-133">Related topics</span></span>


[<span data-ttu-id="8618b-134">Planification du déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8618b-134">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

[<span data-ttu-id="8618b-135">Déploiement du client MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8618b-135">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

 

 
## <span data-ttu-id="8618b-136">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="8618b-136">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8618b-137">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="8618b-137">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8618b-138">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8618b-138">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




