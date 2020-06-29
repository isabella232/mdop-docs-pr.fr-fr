---
title: Récupération d'un lecteur déplacé
description: Récupération d'un lecteur déplacé
author: dansimp
ms.assetid: 0d38ce7e-bc64-473e-ae85-99b7099ca758
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 9e7e03846e0a94902b699377043237c651939a07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809899"
---
# <span data-ttu-id="3b663-103">Récupération d'un lecteur déplacé</span><span class="sxs-lookup"><span data-stu-id="3b663-103">How to Recover a Moved Drive</span></span>
<span data-ttu-id="3b663-104">Cette rubrique explique comment utiliser le site Web d’administration et de contrôle (également appelé support technique) pour récupérer un lecteur de système d’exploitation déplacé après avoir été chiffré par l’administration et la surveillance de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="3b663-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to recover an operating system drive that was moved after being encrypted by Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="3b663-105">Lorsqu’un lecteur est déplacé, il n’accepte plus le code confidentiel utilisé dans l’ordinateur précédent, car le processeur du module de plateforme sécurisée (TPM) a changé.</span><span class="sxs-lookup"><span data-stu-id="3b663-105">When a drive is moved, it no longer accepts the PIN that was used in the previous computer because the Trusted Platform Module (TPM) chip has changed.</span></span> <span data-ttu-id="3b663-106">Pour récupérer le lecteur déplacé, vous devez obtenir l’ID de clé de récupération pour récupérer le mot de passe de récupération.</span><span class="sxs-lookup"><span data-stu-id="3b663-106">To recover the moved drive, you must obtain the recovery key ID to retrieve the recovery password.</span></span>

<span data-ttu-id="3b663-107">Pour récupérer un lecteur déplacé, vous devez utiliser la zone de **récupération de lecteur** du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="3b663-107">To recover a moved drive, you must use the **Drive Recovery** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="3b663-108">Pour accéder à la zone de **récupération du lecteur** , vous devez disposer du rôle utilisateurs du support technique MBAM ou du rôle MBAM Advanced support Users.</span><span class="sxs-lookup"><span data-stu-id="3b663-108">To access the **Drive Recovery** area, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="3b663-109">Pour plus d’informations sur ces rôles, voir [planification pour les comptes et groupes MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="3b663-109">For more information about these roles, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

**<span data-ttu-id="3b663-110">Pour récupérer un lecteur déplacé</span><span class="sxs-lookup"><span data-stu-id="3b663-110">To recover a moved drive</span></span>**
1.  <span data-ttu-id="3b663-111">Sur l’ordinateur qui contient le lecteur déplacé, démarrez l’ordinateur en mode WinRE (Windows Recovery Environment) ou démarrez l’ordinateur à l’aide de Microsoft diagnostic and Recovery Tools (DaRT).</span><span class="sxs-lookup"><span data-stu-id="3b663-111">On the computer that contains the moved drive, start the computer in Windows Recovery Environment (WinRE) mode, or start the computer by using the Microsoft Diagnostic and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="3b663-112">Après le démarrage de l’ordinateur avec WinRE ou DaRT, MBAM traitera le lecteur du système d’exploitation déplacé comme un lecteur de données fixe.</span><span class="sxs-lookup"><span data-stu-id="3b663-112">After the computer has been started with WinRE or DaRT, MBAM will treat the moved operating system drive as a fixed data drive.</span></span> <span data-ttu-id="3b663-113">MBAM affiche alors l’ID du mot de passe de récupération du lecteur et vous demande le mot de passe de récupération.</span><span class="sxs-lookup"><span data-stu-id="3b663-113">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="3b663-114">**Remarques**  Dans certains cas, vous serez peut-être en mesure de cliquer sur **j’ai oublié le code confidentiel** lors du processus de démarrage, puis d’entrer le mode de récupération pour afficher l’ID de la clé de récupération.</span><span class="sxs-lookup"><span data-stu-id="3b663-114">**Note** In some cases, you may be able to click **I forgot the PIN** during the startup process, and then enter the recovery mode to display the recovery key ID.</span></span>

     

3.  <span data-ttu-id="3b663-115">Utilisez l’ID de clé de récupération pour récupérer le mot de passe de récupération et déverrouillez le lecteur à partir du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="3b663-115">Use the recovery key ID to retrieve the recovery password and unlock the drive from the Administration and Monitoring Website.</span></span> <span data-ttu-id="3b663-116">Pour obtenir des instructions, reportez-vous à la rubrique récupération d' [un lecteur en mode récupération](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="3b663-116">For instructions, see [How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md).</span></span>

    <span data-ttu-id="3b663-117">Si le lecteur déplacé a été configuré de manière à utiliser un processeur de TPM sur l’ordinateur d’origine, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="3b663-117">If the moved drive was configured to use a TPM chip on the original computer, complete the following additional steps.</span></span> <span data-ttu-id="3b663-118">Dans le cas contraire, le processus de récupération est terminé.</span><span class="sxs-lookup"><span data-stu-id="3b663-118">Otherwise, the recovery process is complete.</span></span>

4.  <span data-ttu-id="3b663-119">Après avoir déverrouillé le lecteur et terminé le processus de démarrage, ouvrez une invite de commandes en mode WinRE et utilisez la `manage-bde` commande pour déchiffrer le lecteur.</span><span class="sxs-lookup"><span data-stu-id="3b663-119">After unlocking the drive and completing the start process, open a command prompt in WinRE mode and use the `manage-bde` command to decrypt the drive.</span></span> <span data-ttu-id="3b663-120">L’utilisation de cet outil est le seul moyen de supprimer le TPM plus le protecteur de code confidentiel sans le processeur du TPM d’origine.</span><span class="sxs-lookup"><span data-stu-id="3b663-120">Using this tool is the only way to remove the TPM plus the PIN protector without the original TPM chip.</span></span> <span data-ttu-id="3b663-121">Pour plus d’informations sur la `manage-bde` commande, voir [Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567).</span><span class="sxs-lookup"><span data-stu-id="3b663-121">For information about the `manage-bde` command, see [Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567).</span></span>

5.  <span data-ttu-id="3b663-122">Lorsque la suppression est terminée, redémarrez l’ordinateur normalement.</span><span class="sxs-lookup"><span data-stu-id="3b663-122">When the removal is completed, start the computer normally.</span></span> <span data-ttu-id="3b663-123">L’agent MBAM va mettre en œuvre la stratégie pour chiffrer le disque avec le TPM et le code confidentiel du nouvel ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3b663-123">The MBAM agent will now enforce the policy to encrypt the drive with the new computer’s TPM plus the PIN.</span></span>



## <span data-ttu-id="3b663-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b663-124">Related topics</span></span>


[<span data-ttu-id="3b663-125">Gestion de BitLocker avec MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="3b663-125">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="3b663-126">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="3b663-126">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="3b663-127">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="3b663-127">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="3b663-128">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="3b663-128">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





