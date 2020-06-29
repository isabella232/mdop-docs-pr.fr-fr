---
title: À propos de la puce TPM de l'ordinateur
description: À propos de la puce TPM de l'ordinateur
author: dansimp
ms.assetid: 6f1cf18c-277a-4932-886d-14202ca8d175
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6df54dc8085c398bacc508fdbbb79a30b0e4204
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810013"
---
# <span data-ttu-id="5c7a7-103">À propos de la puce TPM de l'ordinateur</span><span class="sxs-lookup"><span data-stu-id="5c7a7-103">About the Computer TPM Chip</span></span>


<span data-ttu-id="5c7a7-104">BitLocker fournit une protection supplémentaire lorsqu’il est utilisé avec un processeur de module de plateforme sécurisée (TPM).</span><span class="sxs-lookup"><span data-stu-id="5c7a7-104">BitLocker provides additional protection when it is used with a Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="5c7a7-105">Le module de plateforme sécurisée est un composant matériel qui est installé sur de nombreux ordinateurs plus récents par les fabricants d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-105">The TPM chip is a hardware component that is installed in many newer computers by the computer manufacturers.</span></span> <span data-ttu-id="5c7a7-106">Le programme d’administration et de surveillance de BitLocker utilise BitLocker, ainsi que le processeur du TPM, pour vous aider à fournir une protection supplémentaire de vos données et pour vous assurer que votre ordinateur n’a pas été falsifié.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-106">Microsoft BitLocker Administration and Monitoring (MBAM) uses BitLocker, in addition to the TPM chip, to help provide additional protection of your data and to make sure that your computer has not been tampered with.</span></span>

## <span data-ttu-id="5c7a7-107">Comment configurer votre TPM</span><span class="sxs-lookup"><span data-stu-id="5c7a7-107">How to Set Up Your TPM</span></span>


<span data-ttu-id="5c7a7-108">Lorsque vous démarrez l’Assistant chiffrement de lecteur BitLocker sur votre ordinateur, BitLocker vérifie s’il s’agit d’un processeur de TPM si votre organisation a configuré BitLocker pour utiliser un processeur de TPM.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-108">When you start the BitLocker Drive Encryption wizard on your computer, BitLocker checks for a TPM chip if your organization has configured BitLocker to use a TPM chip.</span></span> <span data-ttu-id="5c7a7-109">Si BitLocker trouve un processeur de TPM compatible, vous pouvez être invité à redémarrer votre ordinateur pour activer le processeur du TPM.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-109">If BitLocker finds a compatible TPM chip, you may be prompted to restart your computer to enable the TPM chip for use.</span></span> <span data-ttu-id="5c7a7-110">Dès que vous avez redémarré votre ordinateur, suivez les instructions pour configurer le processeur du TPM dans le BIOS (le BIOS est une couche pré-Windows de votre logiciel informatique).</span><span class="sxs-lookup"><span data-stu-id="5c7a7-110">As soon as your computer has restarted, follow the instructions to configure the TPM chip in the BIOS (the BIOS is a pre-Windows layer of your computer software).</span></span>

<span data-ttu-id="5c7a7-111">Une fois BitLocker configuré, vous pouvez accéder à des informations supplémentaires sur le processeur du TPM en ouvrant l’outil options de chiffrement BitLocker dans le panneau de configuration Windows et en sélectionnant **administration du TPM**.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-111">After BitLocker is configured, you can access additional information about the TPM chip by opening the BitLocker Encryption Options tool in the Windows Control Panel, and then selecting **TPM Administration**.</span></span>

<span data-ttu-id="5c7a7-112">**Remarques**  Vous devez disposer des informations d’identification d’administration sur votre ordinateur pour accéder à cet outil.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-112">**Note** You must have administrative credentials on your computer to access this tool.</span></span>

 

<span data-ttu-id="5c7a7-113">Dans un échec de module de plateforme sécurisée, une modification du BIOS ou certaines mises à jour Windows, BitLocker verrouille votre ordinateur et vous demandent de contacter l’assistance technique pour la déverrouiller.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-113">In a TPM failure, a change in the BIOS, or certain Windows Updates, BitLocker will lock your computer and require you to contact your Help Desk to unlock it.</span></span> <span data-ttu-id="5c7a7-114">Vous devez indiquer le nom de votre ordinateur ainsi que le domaine de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-114">You have to provide the name of your computer as well as your computer’s domain.</span></span> <span data-ttu-id="5c7a7-115">Le support technique peut vous donner un fichier de mot de passe qui peut être utilisé pour déverrouiller votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-115">Help Desk can give you a password file that can be used to unlock your computer.</span></span>

## <span data-ttu-id="5c7a7-116">Résolution des problèmes liés au TPM</span><span class="sxs-lookup"><span data-stu-id="5c7a7-116">Troubleshooting TPM Issues</span></span>


<span data-ttu-id="5c7a7-117">En cas d’échec du module de plateforme sécurisée (TPM), de changement du BIOS ou de certaines mises à jour Windows, BitLocker verrouille votre ordinateur et vous demande de contacter l’assistance technique pour le déverrouiller.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-117">If a TPM failure, change in the BIOS, or certain Windows Updates occur, BitLocker will lock your computer and require you to contact your Help Desk to unlock it.</span></span> <span data-ttu-id="5c7a7-118">Vous devez indiquer le nom de votre ordinateur ainsi que le domaine de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-118">You have to provide the name of your computer as well as your computer’s domain.</span></span> <span data-ttu-id="5c7a7-119">Le support technique peut vous donner un fichier de mot de passe que vous pouvez utiliser pour déverrouiller votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5c7a7-119">The Help Desk can give you a password file that you can use to unlock your computer.</span></span>

## <span data-ttu-id="5c7a7-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5c7a7-120">Related topics</span></span>


[<span data-ttu-id="5c7a7-121">Aider les utilisateurs finaux à gérer BitLocker</span><span class="sxs-lookup"><span data-stu-id="5c7a7-121">Helping End Users Manage BitLocker</span></span>](helping-end-users-manage-bitlocker.md)

[<span data-ttu-id="5c7a7-122">Utilisation de votre code PIN ou de votre mot de passe</span><span class="sxs-lookup"><span data-stu-id="5c7a7-122">Using Your PIN or Password</span></span>](using-your-pin-or-password.md)

 

 





