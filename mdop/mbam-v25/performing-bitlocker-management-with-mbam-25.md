---
title: Gestion de BitLocker avec MBAM2.5
description: Gestion de BitLocker avec MBAM2.5
author: dansimp
ms.assetid: 068f3ee0-300c-4083-ba18-7065eef997ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a0ee5802f945176914c56659e0ff7e34e93a969
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811496"
---
# <span data-ttu-id="84ece-103">Gestion de BitLocker avec MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="84ece-103">Performing BitLocker Management with MBAM 2.5</span></span>


<span data-ttu-id="84ece-104">Après avoir planifié le déploiement de la gestion et l’analyse de BitLocker (MBAM), vous pouvez le configurer et l’utiliser pour gérer le chiffrement de lecteur BitLocker au sein de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="84ece-104">After planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage BitLocker Drive Encryption across your enterprise.</span></span> <span data-ttu-id="84ece-105">Les informations contenues dans cette section décrivent les tâches de gestion du chiffrement à l’aide de la gestion des messages</span><span class="sxs-lookup"><span data-stu-id="84ece-105">The information in this section describes post-installation, day-to-day BitLocker encryption management tasks that are accomplished by using Microsoft BitLocker Administration and Monitoring.</span></span>

## <span data-ttu-id="84ece-106">Réinitialiser un verrouillage du TPM</span><span class="sxs-lookup"><span data-stu-id="84ece-106">Reset a TPM lockout</span></span>


<span data-ttu-id="84ece-107">Un module de plateforme sécurisée (TPM) est un micropuce conçu pour fournir des fonctions de sécurité de base, notamment les clés de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="84ece-107">A Trusted Platform Module (TPM) is a microchip that is designed to provide basic security-related functions, primarily involving encryption keys.</span></span> <span data-ttu-id="84ece-108">Le module de plateforme sécurisée est généralement installé sur la carte mère d’un ordinateur, et communique avec le reste du système à l’aide d’une carte de bus hôte.</span><span class="sxs-lookup"><span data-stu-id="84ece-108">The TPM is usually installed on the motherboard of a computer, and it communicates with the rest of the system by using a host bus adapter.</span></span> <span data-ttu-id="84ece-109">Sur les ordinateurs qui intègrent un module de plateforme sécurisée, vous pouvez créer des clés de chiffrement et les chiffrer pour pouvoir les déchiffrer uniquement par le TPM.</span><span class="sxs-lookup"><span data-stu-id="84ece-109">On computers that incorporate a TPM, you can create cryptographic keys and encrypt them so that they can be decrypted only by the TPM.</span></span>

<span data-ttu-id="84ece-110">Un verrouillage du TPM peut se produire si un utilisateur entre un code confidentiel incorrect trop souvent.</span><span class="sxs-lookup"><span data-stu-id="84ece-110">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="84ece-111">Le nombre de fois qu’un utilisateur peut entrer un code confidentiel incorrect avant que les verrouillages du TPM ne varient en fonction du fabricant.</span><span class="sxs-lookup"><span data-stu-id="84ece-111">The number of times that a user can enter an incorrect PIN before the TPM locks varies by manufacturer.</span></span> <span data-ttu-id="84ece-112">Vous pouvez utiliser MBAM pour accéder au système de données de récupération de clés centralisées sur le site Web d’administration et de contrôle, dans lequel vous pouvez récupérer un fichier de mot de passe de propriétaire du TPM lorsque vous fournissez un ID d’ordinateur et un identificateur d’utilisateur associé.</span><span class="sxs-lookup"><span data-stu-id="84ece-112">You can use MBAM to access the centralized key recovery data system on the Administration and Monitoring Website, where you can retrieve a TPM owner password file when you supply a computer ID and an associated user identifier.</span></span>

[<span data-ttu-id="84ece-113">Réinitialisation d'un verrouillage TPM</span><span class="sxs-lookup"><span data-stu-id="84ece-113">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-25.md)

## <span data-ttu-id="84ece-114">Récupérer des lecteurs</span><span class="sxs-lookup"><span data-stu-id="84ece-114">Recover drives</span></span>


<span data-ttu-id="84ece-115">Lorsque vous traitez le chiffrement des données, en particulier dans un environnement d’entreprise, pensez à la manière dont les données peuvent être restaurées en cas de panne matérielle, de changements de personnel ou d’autres situations dans lesquelles les clés de chiffrement peuvent être perdues.</span><span class="sxs-lookup"><span data-stu-id="84ece-115">When you are dealing with the encryption of data, especially in an enterprise environment, consider how that data can be recovered in the event of a hardware failure, changes in personnel, or other situations in which encryption keys can be lost.</span></span>

<span data-ttu-id="84ece-116">Les fonctionnalités de récupération de lecteur chiffrées dans MBAM garantissent la capture et le stockage des données et l’accès aux outils requis pour accéder au volume protégé par BitLocker lorsque le mode de récupération de BitLocker passe en mode de récupération, est déplacé ou est endommagé.</span><span class="sxs-lookup"><span data-stu-id="84ece-116">The encrypted drive recovery features in MBAM ensure that data can be captured and stored and that the required tools are available to access a BitLocker-protected volume when BitLocker goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="84ece-117">Procédure de récupération d'un lecteur en mode de récupération</span><span class="sxs-lookup"><span data-stu-id="84ece-117">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)

[<span data-ttu-id="84ece-118">Récupération d'un lecteur déplacé</span><span class="sxs-lookup"><span data-stu-id="84ece-118">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-25.md)

[<span data-ttu-id="84ece-119">Récupération d'un lecteur endommagé</span><span class="sxs-lookup"><span data-stu-id="84ece-119">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-25.md)

## <span data-ttu-id="84ece-120">Déterminer l’état de chiffrement BitLocker des ordinateurs perdus</span><span class="sxs-lookup"><span data-stu-id="84ece-120">Determine BitLocker encryption state of lost computers</span></span>


<span data-ttu-id="84ece-121">À l’aide de MBAM, vous pouvez déterminer le dernier état de chiffrement BitLocker connu des ordinateurs perdus ou volés.</span><span class="sxs-lookup"><span data-stu-id="84ece-121">By using MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="84ece-122">Détermination de l'état de chiffrement BitLocker des ordinateurs perdus</span><span class="sxs-lookup"><span data-stu-id="84ece-122">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)

## <span data-ttu-id="84ece-123">Utiliser le portail libre-service pour accéder à un ordinateur</span><span class="sxs-lookup"><span data-stu-id="84ece-123">Use the Self-Service Portal to regain access to a computer</span></span>


<span data-ttu-id="84ece-124">Si les utilisateurs finaux se bloquent pas de Windows par BitLocker, ils peuvent suivre les instructions de cette section pour obtenir une clé de récupération BitLocker afin de récupérer l’accès à leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="84ece-124">If end users get locked out of Windows by BitLocker, they can use the instructions in this section to get a BitLocker recovery key to regain access to their computer.</span></span>

[<span data-ttu-id="84ece-125">Utilisation du portail libre-service pour accéder de nouveau à un ordinateur</span><span class="sxs-lookup"><span data-stu-id="84ece-125">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>](how-to-use-the-self-service-portal-to-regain-access-to-a-computer-mbam-25.md)



## <span data-ttu-id="84ece-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="84ece-126">Related topics</span></span>


[<span data-ttu-id="84ece-127">Opérations de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="84ece-127">Operations for MBAM 2.5</span></span>](operations-for-mbam-25.md)

 

## <span data-ttu-id="84ece-128">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="84ece-128">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="84ece-129">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="84ece-129">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="84ece-130">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="84ece-130">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





