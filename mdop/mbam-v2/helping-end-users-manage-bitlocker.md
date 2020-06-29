---
title: Aider les utilisateurs finaux à gérer BitLocker
description: Aider les utilisateurs finaux à gérer BitLocker
author: dansimp
ms.assetid: 47776fb3-2d94-4970-b687-c35ec3dd6c64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26ef2bc33a75ff7773b75807ab0e10e5aa67b109
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810758"
---
# <span data-ttu-id="64661-103">Aider les utilisateurs finaux à gérer BitLocker</span><span class="sxs-lookup"><span data-stu-id="64661-103">Helping End Users Manage BitLocker</span></span>


<span data-ttu-id="64661-104">Le contenu d’un ordinateur perdu ou volé est vulnérable aux accès non autorisés et peut présenter un risque de sécurité aux personnes et aux entreprises.</span><span class="sxs-lookup"><span data-stu-id="64661-104">Content on a lost or stolen computer is vulnerable to unauthorized access, which can present a security risk to both people and companies.</span></span> <span data-ttu-id="64661-105">Le programme d’administration et de surveillance de BitLocker utilise BitLocker pour empêcher tout accès non autorisé en verrouillant votre ordinateur pour protéger les données sensibles des utilisateurs malveillants.</span><span class="sxs-lookup"><span data-stu-id="64661-105">Microsoft BitLocker Administration and Monitoring (MBAM) uses BitLocker to help prevent unauthorized access by locking your computer to help protect sensitive data from malicious users.</span></span>

## <span data-ttu-id="64661-106">Qu’est-ce que BitLocker?</span><span class="sxs-lookup"><span data-stu-id="64661-106">What is BitLocker?</span></span>


<span data-ttu-id="64661-107">Le chiffrement de lecteur BitLocker peut offrir une protection pour les lecteurs de systèmes d’exploitation, les lecteurs de données et les lecteurs amovibles (tels qu’une clé USB) en chiffrant les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="64661-107">BitLocker Drive Encryption can provide protection for operating system drives, data drives, and removable drives (such as a USB thumb drive) by encrypting the drives.</span></span> <span data-ttu-id="64661-108">Selon la configuration de BitLocker, les utilisateurs devront peut-être fournir une clé (un mot de passe ou un code confidentiel) pour déverrouiller les informations stockées sur les lecteurs chiffrés.</span><span class="sxs-lookup"><span data-stu-id="64661-108">Depending on how BitLocker is configured, users may have to provide a key (a password or PIN) to unlock the information that is stored on the encrypted drives.</span></span>

<span data-ttu-id="64661-109">Lorsque vous ajoutez de nouveaux fichiers à un lecteur chiffré avec BitLocker, BitLocker les chiffre automatiquement.</span><span class="sxs-lookup"><span data-stu-id="64661-109">When you add new files to a drive that is encrypted with BitLocker, BitLocker encrypts them automatically.</span></span> <span data-ttu-id="64661-110">Les fichiers restent chiffrés uniquement lorsqu’ils sont stockés sur le lecteur chiffré.</span><span class="sxs-lookup"><span data-stu-id="64661-110">Files remain encrypted only while they are stored in the encrypted drive.</span></span> <span data-ttu-id="64661-111">Les fichiers copiés sur un autre lecteur ou ordinateur sont déchiffrés.</span><span class="sxs-lookup"><span data-stu-id="64661-111">Files that are copied to another drive or computer are decrypted.</span></span> <span data-ttu-id="64661-112">Si vous partagez des fichiers avec d’autres utilisateurs, par exemple par le biais d’un réseau, ces fichiers sont chiffrés en même temps que les utilisateurs autorisés.</span><span class="sxs-lookup"><span data-stu-id="64661-112">If you share files with other users, such as through a network, these files are encrypted while stored on the encrypted drive, but they can be accessed normally by authorized users.</span></span>

<span data-ttu-id="64661-113">Si vous chiffrez le lecteur du système d’exploitation, BitLocker vérifie l’ordinateur lors du démarrage pour toutes les conditions susceptibles de représenter un risque de sécurité (par exemple, une modification du BIOS ou des modifications apportées à un fichier de démarrage).</span><span class="sxs-lookup"><span data-stu-id="64661-113">If you encrypt the operating system drive, BitLocker checks the computer during startup for any conditions that could represent a security risk (for example, a change to the BIOS or changes to any startup files).</span></span> <span data-ttu-id="64661-114">Si un risque de sécurité potentiel est détecté, BitLocker verrouille le lecteur du système d’exploitation et nécessite une clé de récupération BitLocker spéciale pour le déverrouiller.</span><span class="sxs-lookup"><span data-stu-id="64661-114">If a potential security risk is detected, BitLocker will lock the operating system drive and require a special BitLocker recovery key to unlock it.</span></span> <span data-ttu-id="64661-115">Assurez-vous de créer cette clé de récupération lorsque vous activez BitLocker pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="64661-115">Make sure that you create this recovery key when you turn on BitLocker for the first time.</span></span> <span data-ttu-id="64661-116">Dans le cas contraire, vous risquez de perdre définitivement l’accès à vos fichiers.</span><span class="sxs-lookup"><span data-stu-id="64661-116">Otherwise, you could permanently lose access to your files.</span></span>

<span data-ttu-id="64661-117">Si vous chiffrez des lecteurs de données (résolus ou amovibles), vous pouvez déverrouiller un lecteur chiffré à l’aide d’un mot de passe ou d’une carte à puce, ou configurer le lecteur pour qu’il s’ouvre automatiquement lorsque vous ouvrez une session sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="64661-117">If you encrypt data drives (fixed or removable), you can unlock an encrypted drive with a password or a smart card, or set the drive to automatically unlock when you log on to the computer.</span></span>

<span data-ttu-id="64661-118">En plus des mots de passe et des épingles, BitLocker peut utiliser le processeur du module de plateforme sécurisée fourni dans de nombreux ordinateurs récents.</span><span class="sxs-lookup"><span data-stu-id="64661-118">In addition to passwords and PINs, BitLocker can use the Trusted Platform Module (TPM) chip that is provided in many newer computers.</span></span> <span data-ttu-id="64661-119">Le puce TPM est utilisée pour s’assurer que votre ordinateur n’a pas été falsifié avant que BitLocker ne déverrouille le lecteur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="64661-119">The TPM chip is used to ensure that your computer has not been tampered with before BitLocker will unlock the operating system drive.</span></span> <span data-ttu-id="64661-120">Pendant le processus de chiffrement, il est possible que vous deviez activer le processeur du TPM.</span><span class="sxs-lookup"><span data-stu-id="64661-120">During the encryption process, you may have to enable the TPM chip.</span></span> <span data-ttu-id="64661-121">Lorsque vous démarrez votre ordinateur, BitLocker demande à l’application de plateforme sécurisée les clés pour le lecteur et la déverrouille.</span><span class="sxs-lookup"><span data-stu-id="64661-121">When you start your computer, BitLocker asks the TPM for the keys to the drive and unlocks it.</span></span> <span data-ttu-id="64661-122">Pour activer le processeur du module de plateforme sécurisée, vous devez redémarrer votre ordinateur, puis modifier un paramètre dans le BIOS, une couche pré-Windows du logiciel de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="64661-122">To enable the TPM chip, you will have to restart your computer and then change a setting in the BIOS, a pre-Windows layer of your computer software.</span></span> <span data-ttu-id="64661-123">Pour plus d’informations sur le TPM, voir [à propos du puce du TPM de l’ordinateur](about-the-computer-tpm-chip.md).</span><span class="sxs-lookup"><span data-stu-id="64661-123">For more information about the TPM, see [About the Computer TPM Chip](about-the-computer-tpm-chip.md).</span></span>

<span data-ttu-id="64661-124">Une fois votre ordinateur protégé par BitLocker, il est possible que vous deviez entrer un code confidentiel ou un mot de passe chaque fois que l’ordinateur quitte la mise en veille prolongée ou démarre.</span><span class="sxs-lookup"><span data-stu-id="64661-124">Once your computer is protected by BitLocker, you may have to enter a PIN or password every time that the computer wakes from hibernation or starts.</span></span> <span data-ttu-id="64661-125">Le support technique de votre entreprise ou organisation peut vous aider si vous oubliez votre code confidentiel ou votre mot de passe.</span><span class="sxs-lookup"><span data-stu-id="64661-125">The Help Desk for your company or organization can help if you ever forget your PIN or password.</span></span>

<span data-ttu-id="64661-126">Vous pouvez désactiver la fonctionnalité BitLocker, de manière temporaire, en l’interrompant ou définitivement en déchiffrant le lecteur.</span><span class="sxs-lookup"><span data-stu-id="64661-126">You can turn off BitLocker, either temporarily, by suspending it, or permanently, by decrypting the drive.</span></span>

<span data-ttu-id="64661-127">**Remarques**  Dans la mesure où BitLocker chiffre tout le lecteur et pas seulement les fichiers individuels, soyez prudent lorsque vous déplacez des données sensibles entre les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="64661-127">**Note** Because BitLocker encrypts the whole drive and not just the individual files themselves, be careful when you move sensitive data between drives.</span></span> <span data-ttu-id="64661-128">Si vous déplacez un fichier à partir d’un lecteur protégé par BitLocker vers un lecteur non chiffré, le fichier ne sera plus chiffré.</span><span class="sxs-lookup"><span data-stu-id="64661-128">If you move a file from a BitLocker-protected drive to a nonencrypted drive, the file will no longer be encrypted.</span></span>

 

## <span data-ttu-id="64661-129">À propos de l’application options de chiffrement BitLocker</span><span class="sxs-lookup"><span data-stu-id="64661-129">About the BitLocker Encryption Options Application</span></span>


<span data-ttu-id="64661-130">Pour déverrouiller les disques durs de votre ordinateur et gérer votre code confidentiel et vos mots de passe, utilisez l’application options de chiffrement BitLocker du panneau de configuration Windows en suivant la procédure décrite dans cet article.</span><span class="sxs-lookup"><span data-stu-id="64661-130">To unlock hard disk drives on your computer and to manage your PIN and passwords, use the BitLocker Encryption Options application in the Windows Control Panel by following the procedure outlined here.</span></span> <span data-ttu-id="64661-131">Vous pouvez entrer des mots de passe pour déverrouiller des lecteurs protégés et vérifier l’état de BitLocker des lecteurs connectés à l’aide de cette application.</span><span class="sxs-lookup"><span data-stu-id="64661-131">You can enter passwords to unlock protected drives and can check the BitLocker status of attached drives by using this application.</span></span>

**<span data-ttu-id="64661-132">Pour ouvrir l’application options de chiffrement BitLocker</span><span class="sxs-lookup"><span data-stu-id="64661-132">To open the BitLocker Encryption Options application</span></span>**

1.  <span data-ttu-id="64661-133">Cliquez sur **Démarrer**, puis sélectionnez **panneau de configuration**.</span><span class="sxs-lookup"><span data-stu-id="64661-133">Click **Start**, and select **Control Panel**.</span></span> <span data-ttu-id="64661-134">Le panneau de configuration s’ouvre dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="64661-134">The Control Panel opens in a new window.</span></span>

2.  <span data-ttu-id="64661-135">Dans **le panneau**de configuration, sélectionnez **système et sécurité**.</span><span class="sxs-lookup"><span data-stu-id="64661-135">In **Control Panel**, select **System and Security**.</span></span>

3.  <span data-ttu-id="64661-136">Sélectionnez **options de chiffrement BitLocker** pour ouvrir l’application options de chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="64661-136">Select **BitLocker Encryption Options** to open the BitLocker Encryption Options application.</span></span>

    <span data-ttu-id="64661-137">Pour obtenir une description des options disponibles, reportez-vous à la section suivante.</span><span class="sxs-lookup"><span data-stu-id="64661-137">For a description of the available options, see the following section.</span></span>

## <span data-ttu-id="64661-138">Options de l’application options de chiffrement BitLocker</span><span class="sxs-lookup"><span data-stu-id="64661-138">Options on the BitLocker Encryption Options Application</span></span>


<span data-ttu-id="64661-139">L’application options de chiffrement BitLocker du panneau de configuration vous permet de gérer votre code confidentiel et vos mots de passe, qu’utilise BitLocker pour protéger votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="64661-139">The BitLocker Encryption Options application on Control Panel lets you manage your PIN and passwords, which BitLocker uses to protect your computer.</span></span>

**<span data-ttu-id="64661-140">Chiffrement de lecteur BitLocker – lecteurs de disque fixes:</span><span class="sxs-lookup"><span data-stu-id="64661-140">BitLocker Drive Encryption – Fixed Disk Drives:</span></span>**

<span data-ttu-id="64661-141">Dans cette section, vous pouvez afficher des informations sur les disques durs connectés à votre ordinateur et leur état actuel du chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="64661-141">In this section, you can view information about hard disk drives connected to your computer and their current BitLocker Encryption status.</span></span>

-   <span data-ttu-id="64661-142">**Gérer votre code confidentiel** : change le code confidentiel utilisé par BitLocker pour déverrouiller le lecteur de votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="64661-142">**Manage your PIN** - changes the PIN used by BitLocker to unlock your operating system drive.</span></span>

-   <span data-ttu-id="64661-143">**Gérer votre mot de passe** : modifie le mot de passe utilisé par BitLocker pour déverrouiller vos autres lecteurs internes.</span><span class="sxs-lookup"><span data-stu-id="64661-143">**Manage your password** - changes the password that is used by BitLocker to unlock your other internal drives.</span></span>

**<span data-ttu-id="64661-144">Chiffrement de lecteur BitLocker-lecteurs externes:</span><span class="sxs-lookup"><span data-stu-id="64661-144">BitLocker Drive Encryption - External Drives:</span></span>**

<span data-ttu-id="64661-145">Dans cette section, vous pouvez afficher des informations sur les lecteurs externes (par exemple, une clé USB) connectée à votre ordinateur, et sur son état actuel du chiffrement BitLocker.</span><span class="sxs-lookup"><span data-stu-id="64661-145">In this section, you can view information about external drives (such as a USB thumb drive) connected to your computer, and their current BitLocker encryption status.</span></span>

-   <span data-ttu-id="64661-146">**Gérer votre mot de passe** : modifie le mot de passe utilisé par BitLocker pour déverrouiller vos autres lecteurs internes.</span><span class="sxs-lookup"><span data-stu-id="64661-146">**Manage your password** - changes the password that is used by BitLocker to unlock your other internal drives.</span></span>

**<span data-ttu-id="64661-147">Avancé</span><span class="sxs-lookup"><span data-stu-id="64661-147">Advanced:</span></span>**

-   <span data-ttu-id="64661-148">**Administration du TPM** : ouvre l’outil d’administration du TPM dans une fenêtre séparée.</span><span class="sxs-lookup"><span data-stu-id="64661-148">**TPM Administration** - opens the TPM Administration tool in a separate window.</span></span> <span data-ttu-id="64661-149">À partir de cet emplacement, vous pouvez configurer les tâches courantes de GPC et obtenir des informations sur le chipset GPC.</span><span class="sxs-lookup"><span data-stu-id="64661-149">From here you can configure common TPM tasks and obtain information about the TPM chipset.</span></span> <span data-ttu-id="64661-150">Pour accéder à cet outil, vous devez disposer des autorisations d’administration sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="64661-150">You must have administrative permissions on your computer to access this tool.</span></span>

-   <span data-ttu-id="64661-151">**Gestion des disques** : Ouvrez l’outil Gestion des disques.</span><span class="sxs-lookup"><span data-stu-id="64661-151">**Disk Management** -open the Disk Management tool.</span></span> <span data-ttu-id="64661-152">Vous pouvez alors afficher les informations de tous les disques durs connectés à l’ordinateur et configurer des partitions et des options de lecteur.</span><span class="sxs-lookup"><span data-stu-id="64661-152">From here you can view the information for all hard drives connected to the computer and configure partitions and drive options.</span></span> <span data-ttu-id="64661-153">Pour accéder à cet outil, vous devez disposer des droits d’administration sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="64661-153">You must have administrative rights on your computer to access this tool.</span></span>

 

 





