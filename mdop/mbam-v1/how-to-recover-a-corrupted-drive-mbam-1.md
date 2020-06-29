---
title: Récupération d'un lecteur endommagé
description: Récupération d'un lecteur endommagé
author: dansimp
ms.assetid: 715491ae-69c0-4fae-ad3f-3bd19a0db2f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 545ff5c7e6bea29d5f89cce1cf18212b7d0e2870
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804608"
---
# <span data-ttu-id="2529d-103">Récupération d'un lecteur endommagé</span><span class="sxs-lookup"><span data-stu-id="2529d-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="2529d-104">Pour récupérer un lecteur endommagé qui a été protégé par BitLocker, un utilisateur du support technique Microsoft BitLocker (MBAM) doit créer un fichier de package de clé de récupération.</span><span class="sxs-lookup"><span data-stu-id="2529d-104">To recover a corrupted drive that has been protected by BitLocker, a Microsoft BitLocker Administration and Monitoring (MBAM) help desk user must create a recovery key package file.</span></span> <span data-ttu-id="2529d-105">Ce fichier de package peut être copié sur l’ordinateur qui contient le lecteur endommagé, puis utilisé pour récupérer le lecteur.</span><span class="sxs-lookup"><span data-stu-id="2529d-105">This package file can be copied to the computer that contains the corrupted drive and then used to recover the drive.</span></span> <span data-ttu-id="2529d-106">Pour cela, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="2529d-106">To accomplish this, use the following procedure.</span></span>

**<span data-ttu-id="2529d-107">Pour récupérer un lecteur endommagé</span><span class="sxs-lookup"><span data-stu-id="2529d-107">To Recover a Corrupted Drive</span></span>**

1.  <span data-ttu-id="2529d-108">Ouvrez le site Web d’administration MBAM.</span><span class="sxs-lookup"><span data-stu-id="2529d-108">Open the MBAM administration website.</span></span>

2.  <span data-ttu-id="2529d-109">Dans le volet de navigation, sélectionnez **récupération de lecteur** .</span><span class="sxs-lookup"><span data-stu-id="2529d-109">Select **Drive Recovery** from the navigation pane.</span></span> <span data-ttu-id="2529d-110">Entrez le nom de domaine et le nom d’utilisateur de l’utilisateur, la raison pour laquelle vous avez déverrouillé le lecteur et l’ID du mot de passe de récupération de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2529d-110">Enter the user’s domain name and user name, the reason for unlocking the drive, and the user’s recovery password ID.</span></span>

    <span data-ttu-id="2529d-111">**Remarques**  Si vous êtes membre du rôle Administrateurs du support technique, vous n’êtes pas obligé d’entrer le nom de domaine ou le nom d’utilisateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2529d-111">**Note** If you are a member of the Help Desk Administrators role, you do not have to enter the user’s domain name or user name.</span></span>

     

3.  <span data-ttu-id="2529d-112">Cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="2529d-112">Click **Submit**.</span></span> <span data-ttu-id="2529d-113">La clé de récupération s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2529d-113">The recovery key will be displayed.</span></span>

4.  <span data-ttu-id="2529d-114">Cliquez sur **Enregistrer**, puis sélectionnez **package de clé de récupération**.</span><span class="sxs-lookup"><span data-stu-id="2529d-114">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="2529d-115">Le package de clé de récupération sera créé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2529d-115">The recovery key package will be created on your computer.</span></span>

5.  <span data-ttu-id="2529d-116">Copiez le package de clé de récupération sur l’ordinateur sur lequel le lecteur est endommagé.</span><span class="sxs-lookup"><span data-stu-id="2529d-116">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

6.  <span data-ttu-id="2529d-117">Ouvrez une invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="2529d-117">Open an elevated command prompt.</span></span> <span data-ttu-id="2529d-118">Pour cela, cliquez sur **Démarrer** , puis tapez `cmd` dans la zone **Rechercher les programmes et fichiers** .</span><span class="sxs-lookup"><span data-stu-id="2529d-118">To do this, click **Start** and type `cmd` in the **Search programs and files** box.</span></span> <span data-ttu-id="2529d-119">Dans la liste résultats de la recherche, cliquez avec le bouton droit sur **cmd.exe** et sélectionnez **exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="2529d-119">In the search results list, right-click **cmd.exe** and select **Run as Administrator**.</span></span>

7.  <span data-ttu-id="2529d-120">À l’invite de commandes, tapez ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="2529d-120">At the command prompt, type the following:</span></span>

    `repair-bde <fixed drive> <corrupted drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="2529d-121">**Remarques**  Pour le &lt; lecteur fixe &gt; dans la commande, spécifiez un périphérique de stockage disponible dont l’espace disponible est supérieur ou égal à la taille des données sur le disque endommagé.</span><span class="sxs-lookup"><span data-stu-id="2529d-121">**Note** For the &lt;fixed drive&gt; in the command, specify an available storage device that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="2529d-122">Les données du lecteur endommagé sont récupérées et déplacées vers le lecteur fixe indiqué.</span><span class="sxs-lookup"><span data-stu-id="2529d-122">Data on the corrupted drive is recovered and moved to the specified fixed drive.</span></span>

     

## <span data-ttu-id="2529d-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2529d-123">Related topics</span></span>


[<span data-ttu-id="2529d-124">Gestion de BitLocker avec MBAM</span><span class="sxs-lookup"><span data-stu-id="2529d-124">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





