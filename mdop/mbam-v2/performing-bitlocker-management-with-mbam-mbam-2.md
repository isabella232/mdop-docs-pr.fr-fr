---
title: Gestion de BitLocker avec MBAM
description: Gestion de BitLocker avec MBAM
author: dansimp
ms.assetid: 9bfc6c67-f12c-4daa-8f08-5884fb47443c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d261ec4fa789cd331209afe1c2f1858d627209a3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811790"
---
# <span data-ttu-id="90b7d-103">Gestion de BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="90b7d-103">Performing BitLocker Management with MBAM</span></span>


<span data-ttu-id="90b7d-104">Après avoir planifié le déploiement de Microsoft BitLocker et de l’analyse, vous pouvez le configurer et l’utiliser pour gérer le chiffrement d’entreprise BitLocker.</span><span class="sxs-lookup"><span data-stu-id="90b7d-104">After planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="90b7d-105">Les informations contenues dans cette section décrivent les tâches de gestion du chiffrement à l’aide du chiffrement de BitLocker qui sont accomplies à l’aide de l’administration et de la surveillance de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="90b7d-105">The information in this section describes post-installation day-to-day BitLocker encryption management tasks that are accomplished by using Microsoft BitLocker Administration and Monitoring.</span></span>

## <span data-ttu-id="90b7d-106">Réinitialiser un verrouillage du TPM à l’aide de MBAM</span><span class="sxs-lookup"><span data-stu-id="90b7d-106">Reset a TPM Lockout by Using MBAM</span></span>


<span data-ttu-id="90b7d-107">Un module de plateforme sécurisée (TPM) est un micropuce conçu pour fournir des fonctions de sécurité de base, notamment les clés de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="90b7d-107">A Trusted Platform Module (TPM) is a microchip that is designed to provide basic security-related functions, primarily involving encryption keys.</span></span> <span data-ttu-id="90b7d-108">Le module de plateforme sécurisée est généralement installé sur la carte de réseau d’un ordinateur ou d’un ordinateur portable et communique avec le reste du système à l’aide d’un bus matériel.</span><span class="sxs-lookup"><span data-stu-id="90b7d-108">The TPM is usually installed on the motherboard of a computer or laptop, and communicates with the rest of the system by using a hardware bus.</span></span> <span data-ttu-id="90b7d-109">Les ordinateurs qui intègrent un TPM ont la possibilité de créer des clés de chiffrement et de les chiffrer de sorte qu’ils puissent être déchiffrés uniquement par le TPM.</span><span class="sxs-lookup"><span data-stu-id="90b7d-109">Computers that incorporate a TPM have the ability to create cryptographic keys and encrypt them so that they can be decrypted only by the TPM.</span></span>

<span data-ttu-id="90b7d-110">Un verrouillage du TPM peut se produire si un utilisateur entre un code confidentiel incorrect trop souvent.</span><span class="sxs-lookup"><span data-stu-id="90b7d-110">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="90b7d-111">Le nombre de fois qu’un utilisateur peut entrer un code confidentiel incorrect avant que les verrouillages du TPM ne varient d’un fabricant au fabricant.</span><span class="sxs-lookup"><span data-stu-id="90b7d-111">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span> <span data-ttu-id="90b7d-112">Vous pouvez utiliser MBAM pour accéder au système de données de récupération de clés centralisées sur le site Web d’administration et de contrôle, dans lequel vous pouvez récupérer un fichier de mot de passe de propriétaire du TPM lorsque vous fournissez un ID d’ordinateur et un identificateur d’utilisateur associé.</span><span class="sxs-lookup"><span data-stu-id="90b7d-112">You can use MBAM to access the centralized Key Recovery data system in the Administration and Monitoring website, where you can retrieve a TPM owner password file when you supply a computer ID and associated user identifier.</span></span>

[<span data-ttu-id="90b7d-113">Réinitialisation d'un verrouillage TPM</span><span class="sxs-lookup"><span data-stu-id="90b7d-113">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-2.md)

## <span data-ttu-id="90b7d-114">Récupérer des lecteurs avec MBAM</span><span class="sxs-lookup"><span data-stu-id="90b7d-114">Recover Drives with MBAM</span></span>


<span data-ttu-id="90b7d-115">Lorsque vous traitez le chiffrement des données, en particulier dans un environnement d’entreprise, pensez à la manière dont les données peuvent être restaurées en cas de panne matérielle, de changements de personnel ou d’autres situations dans lesquelles les clés de chiffrement peuvent être perdues.</span><span class="sxs-lookup"><span data-stu-id="90b7d-115">When you are dealing with the encryption of data, especially in an enterprise environment, consider how that data can be recovered in the event of a hardware failure, changes in personnel, or other situations in which encryption keys can be lost.</span></span>

<span data-ttu-id="90b7d-116">Les fonctionnalités de récupération de lecteur chiffrées de MBAM garantissent la capture et le stockage des données et l’accès aux outils requis pour accéder au volume protégé par BitLocker lorsque le mode de récupération de BitLocker passe en mode de récupération, est déplacé ou est endommagé.</span><span class="sxs-lookup"><span data-stu-id="90b7d-116">The encrypted drive recovery features of MBAM ensure that data can be captured and stored and that the required tools are available to access a BitLocker-protected volume when BitLocker goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="90b7d-117">Procédure de récupération d'un lecteur en mode de récupération</span><span class="sxs-lookup"><span data-stu-id="90b7d-117">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

[<span data-ttu-id="90b7d-118">Récupération d'un lecteur déplacé</span><span class="sxs-lookup"><span data-stu-id="90b7d-118">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

[<span data-ttu-id="90b7d-119">Récupération d'un lecteur endommagé</span><span class="sxs-lookup"><span data-stu-id="90b7d-119">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

## <span data-ttu-id="90b7d-120">Déterminer l’état de chiffrement de BitLocker des ordinateurs perdus en utilisant MBAM</span><span class="sxs-lookup"><span data-stu-id="90b7d-120">Determine BitLocker Encryption State of Lost Computers by Using MBAM</span></span>


<span data-ttu-id="90b7d-121">À l’aide de MBAM, vous pouvez déterminer le dernier état de chiffrement BitLocker connu des ordinateurs perdus ou volés.</span><span class="sxs-lookup"><span data-stu-id="90b7d-121">Using MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="90b7d-122">Détermination de l'état de chiffrement BitLocker des ordinateurs perdus</span><span class="sxs-lookup"><span data-stu-id="90b7d-122">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

## <span data-ttu-id="90b7d-123">Utiliser le portail libre-service pour accéder à un ordinateur</span><span class="sxs-lookup"><span data-stu-id="90b7d-123">Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="90b7d-124">Si les utilisateurs finaux se bloquent pas de Windows par BitLocker, ils peuvent suivre les instructions de cette section pour obtenir une clé de récupération BitLocker afin de récupérer l’accès à leur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="90b7d-124">If end users get locked out of Windows by BitLocker, they can use the instructions in this section to get a BitLocker recovery key to regain access to their computer.</span></span>

[<span data-ttu-id="90b7d-125">Utilisation du portail libre-service pour accéder de nouveau à un ordinateur</span><span class="sxs-lookup"><span data-stu-id="90b7d-125">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>](how-to-use-the-self-service-portal-to-regain-access-to-a-computer.md)

## <span data-ttu-id="90b7d-126">Autres ressources pour effectuer une gestion BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="90b7d-126">Other Resources for Performing BitLocker Management with MBAM</span></span>


[<span data-ttu-id="90b7d-127">Opérations de MBAM2.0</span><span class="sxs-lookup"><span data-stu-id="90b7d-127">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





