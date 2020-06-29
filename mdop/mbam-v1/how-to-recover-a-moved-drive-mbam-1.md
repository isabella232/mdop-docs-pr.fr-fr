---
title: Récupération d'un lecteur déplacé
description: Récupération d'un lecteur déplacé
author: dansimp
ms.assetid: 0c7199d8-9463-4f44-9af3-b70eceeaff1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e73e0878a3102d56494feb33efa69182029988c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804596"
---
# <span data-ttu-id="6e08f-103">Récupération d'un lecteur déplacé</span><span class="sxs-lookup"><span data-stu-id="6e08f-103">How to Recover a Moved Drive</span></span>


<span data-ttu-id="6e08f-104">Lorsque vous déplacez un lecteur de système d’exploitation déjà chiffré à l’aide du système d’administration et de surveillance Microsoft BitLocker (MBAM), vous devez résoudre certains problèmes.</span><span class="sxs-lookup"><span data-stu-id="6e08f-104">When you move an operating system drive that has been previously encrypted by using Microsoft BitLocker Administration and Monitoring (MBAM), you must resolve certain issues.</span></span> <span data-ttu-id="6e08f-105">Une fois qu’un code confidentiel est attaché au nouvel ordinateur, il n’accepte pas le code confidentiel de démarrage utilisé dans l’ordinateur précédent.</span><span class="sxs-lookup"><span data-stu-id="6e08f-105">After a PIN is attached to the new computer, the drive will not accept the start-up PIN that was used in previous computer.</span></span> <span data-ttu-id="6e08f-106">Le système considère que le code confidentiel n’est pas valide en raison de la modification apportée au processeur du module de plateforme sécurisée (TPM).</span><span class="sxs-lookup"><span data-stu-id="6e08f-106">The system considers the PIN to be invalid because of the change to the Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="6e08f-107">Vous devez obtenir un ID de clé de récupération pour récupérer le mot de passe de récupération pour pouvoir utiliser le lecteur déplacé.</span><span class="sxs-lookup"><span data-stu-id="6e08f-107">You must obtain a recovery key ID to retrieve the recovery password in order to use the moved drive.</span></span> <span data-ttu-id="6e08f-108">Pour cela, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="6e08f-108">To do this, use the following procedure.</span></span>

**<span data-ttu-id="6e08f-109">Pour récupérer un lecteur déplacé</span><span class="sxs-lookup"><span data-stu-id="6e08f-109">To recover a moved drive</span></span>**

1.  <span data-ttu-id="6e08f-110">Sur l’ordinateur qui contient le lecteur déplacé, démarrez en mode WinRE (Windows Recovery Environment) ou démarrez l’ordinateur à l’aide de Microsoft Diagnostics and Recovery Tools (DaRT).</span><span class="sxs-lookup"><span data-stu-id="6e08f-110">On the computer that contains the moved drive, start in Windows Recovery Environment (WinRE) mode, or start the computer by using the Microsoft Diagnostics and Recovery Toolset (DaRT).</span></span>

2.  <span data-ttu-id="6e08f-111">Une fois que l’ordinateur est démarré avec WinRE ou DaRT, MBAM considère le lecteur du système d’exploitation déplacé comme un lecteur de données.</span><span class="sxs-lookup"><span data-stu-id="6e08f-111">Once the computer has been started with WinRE or DaRT, MBAM will treat the moved operating system drive as a data drive.</span></span> <span data-ttu-id="6e08f-112">MBAM affiche alors l’ID du mot de passe de récupération du lecteur et vous demande le mot de passe de récupération.</span><span class="sxs-lookup"><span data-stu-id="6e08f-112">MBAM will then display the drive’s recovery password ID and ask for the recovery password.</span></span>

    <span data-ttu-id="6e08f-113">**Remarques**  Dans certains cas, vous serez peut-être en mesure de cliquer sur **j’ai oublié le code confidentiel** lors du processus de démarrage pour entrer le mode de récupération.</span><span class="sxs-lookup"><span data-stu-id="6e08f-113">**Note** In some cases, you might be able to click **I forget the PIN** during the startup process to enter the recovery mode.</span></span> <span data-ttu-id="6e08f-114">L’ID de la clé de récupération s’affiche également.</span><span class="sxs-lookup"><span data-stu-id="6e08f-114">This also displays the recovery key ID.</span></span>

     

3.  <span data-ttu-id="6e08f-115">Sur le site Web d’administration MBAM, utilisez l’ID de clé de récupération pour récupérer le mot de passe de récupération et déverrouillez le lecteur.</span><span class="sxs-lookup"><span data-stu-id="6e08f-115">On the MBAM administration website, use the recovery key ID to retrieve the recovery password and unlock the drive.</span></span>

4.  <span data-ttu-id="6e08f-116">Si le lecteur déplacé a été configuré de manière à utiliser un processeur de TPM sur l’ordinateur d’origine, vous devez effectuer des étapes supplémentaires après avoir déverrouillé le lecteur et terminer le processus de démarrage.</span><span class="sxs-lookup"><span data-stu-id="6e08f-116">If the moved drive was configured to use a TPM chip on the original computer, you must take additional steps after you unlock the drive and complete the start process.</span></span> <span data-ttu-id="6e08f-117">Dans le mode WinRE, ouvrez une invite de commandes et utilisez l’outil **Manage-bde** pour déchiffrer le lecteur.</span><span class="sxs-lookup"><span data-stu-id="6e08f-117">In WinRE mode, open a command prompt and use the **manage-bde** tool to decrypt the drive.</span></span> <span data-ttu-id="6e08f-118">L’utilisation de cet outil est le seul moyen de supprimer la protection du TPM-plus-PIN sans le processeur du TPM d’origine.</span><span class="sxs-lookup"><span data-stu-id="6e08f-118">The use of this tool is the only way to remove the TPM-plus-PIN protection without the original TPM chip.</span></span>

5.  <span data-ttu-id="6e08f-119">Au terme de la suppression, démarrez le système normalement.</span><span class="sxs-lookup"><span data-stu-id="6e08f-119">After the removal is complete, start the system normally.</span></span> <span data-ttu-id="6e08f-120">L’agent MBAM va mettre en œuvre la politique de chiffrer le lecteur avec le code confidentiel plus le nouveau de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6e08f-120">The MBAM agent will proceed to enforce the policy to encrypt the drive with the new computer’s TPM plus PIN.</span></span>

## <span data-ttu-id="6e08f-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6e08f-121">Related topics</span></span>


[<span data-ttu-id="6e08f-122">Gestion de BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="6e08f-122">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





