---
title: Gestion de BitLocker avec MBAM
description: Gestion de BitLocker avec MBAM
author: dansimp
ms.assetid: 2d24390a-87bf-48b3-96a9-3882d6f2a15c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d0de3711d5b7c3696783a054ee7c7f8220b5356
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811429"
---
# <span data-ttu-id="45fb1-103">Gestion de BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="45fb1-103">Performing BitLocker Management with MBAM</span></span>


<span data-ttu-id="45fb1-104">Après avoir déployé le contrôle d’administration et de surveillance de BitLocker de Microsoft (MBAM), vous pouvez configurer et utiliser MBAM pour gérer le chiffrement d’entreprise BitLocker.</span><span class="sxs-lookup"><span data-stu-id="45fb1-104">After you deploy Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use MBAM to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="45fb1-105">Cette section décrit les tâches de gestion du chiffrement à l’aide de l’installation, qui peuvent être effectuées à l’aide de MBAM.</span><span class="sxs-lookup"><span data-stu-id="45fb1-105">This section describes post-installation, day-to-day BitLocker encryption management tasks that can be accomplished by using MBAM.</span></span>

## <span data-ttu-id="45fb1-106">Réinitialiser un verrouillage du TPM avec MBAM</span><span class="sxs-lookup"><span data-stu-id="45fb1-106">Reset a TPM Lockout with MBAM</span></span>


<span data-ttu-id="45fb1-107">Un micropuce module de plateforme sécurisée (TPM) fournit des fonctions de sécurité de base.</span><span class="sxs-lookup"><span data-stu-id="45fb1-107">A Trusted Platform Module (TPM) microchip provides basic security-related functions.</span></span> <span data-ttu-id="45fb1-108">Ces fonctions sont principalement effectuées par l’utilisation de clés de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="45fb1-108">These functions are accomplished primarily by the use of encryption keys.</span></span> <span data-ttu-id="45fb1-109">Le module de plateforme sécurisée est généralement installé sur la carte mère d’un ordinateur, d’un ordinateur portable et communique avec le reste du système à l’aide d’un bus matériel.</span><span class="sxs-lookup"><span data-stu-id="45fb1-109">The TPM is typically installed on the motherboard of a computer or laptop and communicates with the rest of the system by using a hardware bus.</span></span> <span data-ttu-id="45fb1-110">Les ordinateurs qui intègrent un TPM peuvent créer des clés de chiffrement qui peuvent être déchiffrées uniquement par le TPM.</span><span class="sxs-lookup"><span data-stu-id="45fb1-110">Computers that incorporate a TPM can create cryptographic keys that can be decrypted only by the TPM.</span></span> <span data-ttu-id="45fb1-111">Un verrouillage du TPM peut se produire si un utilisateur entre un code confidentiel incorrect trop souvent.</span><span class="sxs-lookup"><span data-stu-id="45fb1-111">A TPM lockout can occur if a user enters an incorrect PIN too many times.</span></span> <span data-ttu-id="45fb1-112">Le nombre de fois qu’un utilisateur peut entrer un code confidentiel incorrect avant que les verrouillages du TPM ne varient d’un fabricant au fabricant.</span><span class="sxs-lookup"><span data-stu-id="45fb1-112">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span> <span data-ttu-id="45fb1-113">Le système de données de récupération de clés sur le site Web d’administration MBAM vous permet d’obtenir un fichier de mot de passe de réinitialisation du propriétaire de TPM.</span><span class="sxs-lookup"><span data-stu-id="45fb1-113">The Key Recovery data system on the MBAM administration website enables you to obtain a reset TPM owner password file.</span></span>

[<span data-ttu-id="45fb1-114">Réinitialisation d'un verrouillage TPM</span><span class="sxs-lookup"><span data-stu-id="45fb1-114">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-1.md)

## <span data-ttu-id="45fb1-115">Récupérer des lecteurs avec MBAM</span><span class="sxs-lookup"><span data-stu-id="45fb1-115">Recover drives with MBAM</span></span>


<span data-ttu-id="45fb1-116">Assurez-vous de savoir comment procéder à la récupération des données à partir de lecteurs chiffrés dans le cas d’une panne matérielle, de changements de personnel ou d’autres situations dans lesquelles les clés de chiffrement sont perdues.</span><span class="sxs-lookup"><span data-stu-id="45fb1-116">Make sure that you know how to attempt data recovery from encrypted drives in the event of hardware failure, changes in personnel, or other situations in which encryption keys are lost.</span></span> <span data-ttu-id="45fb1-117">Les fonctionnalités de récupération de lecteur chiffrées de MBAM fournissent la capture et le stockage des données et la disponibilité des outils requis pour accéder au volume protégé par BitLocker lorsque le volume passe en mode de récupération, est déplacé ou est endommagé.</span><span class="sxs-lookup"><span data-stu-id="45fb1-117">The Encrypted Drive Recovery features of MBAM provide the capture and storage of data and availability of tools required to access a BitLocker-protected volume when the volume goes into recovery mode, is moved, or becomes corrupted.</span></span>

[<span data-ttu-id="45fb1-118">Procédure de récupération d'un lecteur en mode de récupération</span><span class="sxs-lookup"><span data-stu-id="45fb1-118">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-1.md)

[<span data-ttu-id="45fb1-119">Récupération d'un lecteur déplacé</span><span class="sxs-lookup"><span data-stu-id="45fb1-119">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-1.md)

[<span data-ttu-id="45fb1-120">Récupération d'un lecteur endommagé</span><span class="sxs-lookup"><span data-stu-id="45fb1-120">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-1.md)

## <span data-ttu-id="45fb1-121">Déterminer l’état de chiffrement de BitLocker des ordinateurs perdus en utilisant MBAM</span><span class="sxs-lookup"><span data-stu-id="45fb1-121">Determine BitLocker Encryption State of lost computers by Using MBAM</span></span>


<span data-ttu-id="45fb1-122">Lorsque vous utilisez MBAM, vous pouvez déterminer le dernier état de chiffrement BitLocker connu des ordinateurs perdus ou volés.</span><span class="sxs-lookup"><span data-stu-id="45fb1-122">When you use MBAM, you can determine the last known BitLocker encryption status of computers that were lost or stolen.</span></span>

[<span data-ttu-id="45fb1-123">Détermination de l'état de chiffrement BitLocker d'un ordinateur perdu</span><span class="sxs-lookup"><span data-stu-id="45fb1-123">How to Determine the BitLocker Encryption State of a Lost Computers</span></span>](how-to-determine-the-bitlocker-encryption-state-of-a-lost-computers-mbam-1.md)

## <span data-ttu-id="45fb1-124">Autres ressources pour effectuer une gestion BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="45fb1-124">Other resources for performing BitLocker Management with MBAM</span></span>


[<span data-ttu-id="45fb1-125">Opérations de MBAM1.0</span><span class="sxs-lookup"><span data-stu-id="45fb1-125">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





