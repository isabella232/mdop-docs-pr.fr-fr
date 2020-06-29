---
title: Récupération d'un lecteur déplacé
description: Récupération d'un lecteur déplacé
author: dansimp
ms.assetid: 697cd78d-962c-411e-901a-2e9220ba6552
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bd0d43f2eea95fe71225a50e7fa68d4fb1c35485
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810931"
---
# <span data-ttu-id="8ee1d-103">Récupération d'un lecteur déplacé</span><span class="sxs-lookup"><span data-stu-id="8ee1d-103">How to Recover a Moved Drive</span></span>


<span data-ttu-id="8ee1d-104">Lorsque vous déplacez un lecteur de système d’exploitation qui est chiffré à l’aide de l’administration et de la surveillance de BitLocker (MBAM), le lecteur n’accepte pas le code confidentiel qui a été utilisé sur un ordinateur précédent en raison de la modification apportée au processeur du module de plateforme sécurisée (TPM).</span><span class="sxs-lookup"><span data-stu-id="8ee1d-104">When you move an operating system drive that is encrypted by using Microsoft BitLocker Administration and Monitoring (MBAM), the drive will not accept the PIN that was used in a previous computer because of the change to the Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="8ee1d-105">Pour utiliser le lecteur déplacé, vous avez besoin d’un moyen d’obtenir l’ID de clé de récupération pour récupérer le mot de passe de récupération.</span><span class="sxs-lookup"><span data-stu-id="8ee1d-105">To use the moved drive, you will need a way to obtain the recovery key ID to retrieve the recovery password.</span></span> <span data-ttu-id="8ee1d-106">Utilisez la procédure suivante pour récupérer un lecteur qui a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="8ee1d-106">Use the following procedure to recover a drive that has moved.</span></span>

**<span data-ttu-id="8ee1d-107">Pour récupérer un lecteur déplacé</span><span class="sxs-lookup"><span data-stu-id="8ee1d-107">To recover a moved drive</span></span>**

1.  <span data-ttu-id="8ee1d-108">Sur l’ordinateur qui contient le lecteur déplacé, démarrez l’ordinateur en mode WinRE (Windows Recovery Environment) ou démarrez l’ordinateur à l’aide de Microsoft diagnostic and Recovery Tools (DaRT).</span><span class="sxs-lookup"><span data-stu-id="8ee1d-108">On the computer that contains the moved drive, start the computer in Windows recovery environment (WinRE) mode, or start the computer by using the Microsoft Diagnostic and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="8ee1d-109">Une fois que l’ordinateur est démarré avec WinRE ou DaRT, l’administration et la surveillance de BitLocker utilise le lecteur du système d’exploitation déplacé comme lecteur de données.</span><span class="sxs-lookup"><span data-stu-id="8ee1d-109">Once the computer has been started with WinRE or DaRT, Microsoft BitLocker Administration and Monitoring will treat the moved operating system drive as a data drive.</span></span> <span data-ttu-id="8ee1d-110">MBAM affiche alors l’ID du mot de passe de récupération du lecteur et vous demande le mot de passe de récupération.</span><span class="sxs-lookup"><span data-stu-id="8ee1d-110">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="8ee1d-111">**Remarques**  Dans certains cas, vous serez peut-être en mesure de cliquer sur **j’ai oublié le code confidentiel** lors du processus de démarrage, puis d’entrer le mode de récupération pour afficher l’ID de la clé de récupération.</span><span class="sxs-lookup"><span data-stu-id="8ee1d-111">**Note** In some cases, you may be able to click **I forgot the PIN** during the startup process, and then enter the recovery mode to display the recovery key ID.</span></span>

     

3.  <span data-ttu-id="8ee1d-112">Utilisez l’ID de clé de récupération pour récupérer le mot de passe de récupération et déverrouillez le lecteur à partir du site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="8ee1d-112">Use the recovery key ID to retrieve the recovery password and unlock the drive from the Administration and Monitoring website.</span></span>

4.  <span data-ttu-id="8ee1d-113">Si le lecteur déplacé a été configuré de manière à utiliser un processeur de TPM sur l’ordinateur d’origine, vous devez effectuer des étapes supplémentaires après avoir déverrouillé le lecteur et terminer le processus de démarrage.</span><span class="sxs-lookup"><span data-stu-id="8ee1d-113">If the moved drive was configured to use a TPM chip on the original computer, you must take additional steps after unlocking the drive and completing the start process.</span></span> <span data-ttu-id="8ee1d-114">Dans le mode WinRE, ouvrez une invite de commandes et utilisez l’outil **Manage-bde** pour déchiffrer le lecteur.</span><span class="sxs-lookup"><span data-stu-id="8ee1d-114">In WinRE mode, open a command prompt and use the **manage-bde** tool to decrypt the drive.</span></span> <span data-ttu-id="8ee1d-115">L’utilisation de cet outil est le seul moyen de supprimer le protecteur du TPM plus code confidentiel sans le processeur du TPM d’origine.</span><span class="sxs-lookup"><span data-stu-id="8ee1d-115">Using this tool is the only way to remove the TPM plus PIN protector without the original TPM chip.</span></span>

5.  <span data-ttu-id="8ee1d-116">Lorsque la suppression est terminée, démarrez l’ordinateur normalement.</span><span class="sxs-lookup"><span data-stu-id="8ee1d-116">Once the removal is completed, start the computer normally.</span></span> <span data-ttu-id="8ee1d-117">L’agent MBAM va mettre en œuvre la stratégie pour chiffrer le lecteur avec le code confidentiel plus (TPM) de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8ee1d-117">The MBAM agent will now enforce the policy to encrypt the drive with the new computer’s TPM plus PIN.</span></span>

## <span data-ttu-id="8ee1d-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ee1d-118">Related topics</span></span>


[<span data-ttu-id="8ee1d-119">Gestion de BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="8ee1d-119">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





