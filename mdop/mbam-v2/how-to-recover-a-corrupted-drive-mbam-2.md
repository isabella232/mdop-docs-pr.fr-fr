---
title: Récupération d'un lecteur endommagé
description: Récupération d'un lecteur endommagé
author: dansimp
ms.assetid: b0457a00-f72e-4ad8-ab3b-7701851ca87e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5bbd4c2a1f5ef3fde78a9f72c1f77ccb0cdea377
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809617"
---
# <span data-ttu-id="32c46-103">Récupération d'un lecteur endommagé</span><span class="sxs-lookup"><span data-stu-id="32c46-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="32c46-104">Pour récupérer un lecteur endommagé protégé par BitLocker, un utilisateur du support technique Microsoft BitLocker (MBAM) doit créer un fichier de package de clé de récupération.</span><span class="sxs-lookup"><span data-stu-id="32c46-104">To recover a corrupted drive protected by BitLocker, a Microsoft BitLocker Administration and Monitoring (MBAM) Help Desk user will need to create a recovery key package file.</span></span> <span data-ttu-id="32c46-105">Ce fichier de package peut alors être copié sur l’ordinateur qui contient le lecteur endommagé, puis utilisé pour récupérer le lecteur.</span><span class="sxs-lookup"><span data-stu-id="32c46-105">This package file can then be copied to the computer that contains the corrupted drive, and then used to recover the drive.</span></span> <span data-ttu-id="32c46-106">Suivez la procédure ci-dessous pour obtenir la procédure à suivre.</span><span class="sxs-lookup"><span data-stu-id="32c46-106">Use the following procedure for the steps needed to do this.</span></span>

<span data-ttu-id="32c46-107">**Important**  Pour éviter une perte de données potentielle, il est vivement recommandé de lire l’aide «réparation-BDE» et de comprendre clairement comment utiliser la commande avant d’exécuter les instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="32c46-107">**Important** To avoid a potential loss of data, it is strongly recommended that you read the “repair-bde” help and clearly understand how to use the command before completing the following instructions.</span></span>

 

**<span data-ttu-id="32c46-108">Pour récupérer un lecteur endommagé</span><span class="sxs-lookup"><span data-stu-id="32c46-108">To recover a corrupted drive</span></span>**

1.  <span data-ttu-id="32c46-109">Pour créer le package de clé de récupération nécessaire pour récupérer un lecteur endommagé, démarrez un navigateur Web et ouvrez le site Web d’administration et de contrôle MBAM.</span><span class="sxs-lookup"><span data-stu-id="32c46-109">To create the recovery key package necessary to recover a corrupted drive, start a web browser and open the MBAM Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="32c46-110">Dans le volet de navigation gauche, sélectionnez **récupération de lecteur** .</span><span class="sxs-lookup"><span data-stu-id="32c46-110">Select **Drive Recovery** from the left navigation pane.</span></span> <span data-ttu-id="32c46-111">Entrez le nom de domaine, le nom d’utilisateur, la raison pour le déverrouillage du lecteur et l’ID du mot de passe de récupération de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="32c46-111">Enter the user’s domain name, user name, reason for unlocking the drive, and the user’s recovery password ID.</span></span>

    <span data-ttu-id="32c46-112">**Remarques**  Si vous êtes membre du rôle Administrateurs du support technique, vous n’êtes pas obligé d’entrer le nom de domaine ou le nom d’utilisateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="32c46-112">**Note** If you are a member of the Help Desk Administrators role, you do not have to enter the user’s domain name or user name.</span></span>

     

3.  <span data-ttu-id="32c46-113">Cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="32c46-113">Click **Submit**.</span></span> <span data-ttu-id="32c46-114">La clé de récupération s’affiche.</span><span class="sxs-lookup"><span data-stu-id="32c46-114">The recovery key will be displayed.</span></span>

4.  <span data-ttu-id="32c46-115">Cliquez sur **Enregistrer**, puis sélectionnez **package de clé de récupération**.</span><span class="sxs-lookup"><span data-stu-id="32c46-115">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="32c46-116">Le package de clé de récupération sera créé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="32c46-116">The recovery key package will be created on your computer.</span></span>

5.  <span data-ttu-id="32c46-117">Copiez le package de clé de récupération sur l’ordinateur sur lequel le lecteur est endommagé.</span><span class="sxs-lookup"><span data-stu-id="32c46-117">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

6.  <span data-ttu-id="32c46-118">Ouvrez une invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="32c46-118">Open an elevated command prompt.</span></span> <span data-ttu-id="32c46-119">Pour cela, cliquez sur **Démarrer** , puis tapez `cmd` dans la **zone Rechercher les programmes et fichiers**.</span><span class="sxs-lookup"><span data-stu-id="32c46-119">To do this, click **Start** and type `cmd` in the **Search programs and files box**.</span></span> <span data-ttu-id="32c46-120">Cliquez avec le bouton droit sur **cmd.exe** et sélectionnez **exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="32c46-120">Right-click **cmd.exe** and select **Run as Administrator**.</span></span>

7.  <span data-ttu-id="32c46-121">À l’invite de commandes, tapez ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="32c46-121">At the command prompt, type the following:</span></span>

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="32c46-122">**Remarques**  Remplacez &lt; un lecteur fixe &gt; par un disque dur disponible dont l’espace disponible est supérieur ou égal à celui des données sur le disque endommagé.</span><span class="sxs-lookup"><span data-stu-id="32c46-122">**Note** Replace &lt;fixed drive&gt; with an available hard disk drive that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="32c46-123">Les données du lecteur endommagé sont récupérées et déplacées sur le disque dur spécifié.</span><span class="sxs-lookup"><span data-stu-id="32c46-123">Data on the corrupted drive is recovered and moved to the specified hard disk drive.</span></span>

     

## <span data-ttu-id="32c46-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="32c46-124">Related topics</span></span>


[<span data-ttu-id="32c46-125">Gestion de BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="32c46-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





