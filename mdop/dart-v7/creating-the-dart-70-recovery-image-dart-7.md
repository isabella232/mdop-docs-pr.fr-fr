---
title: Création de l'image de récupération DaRT7.0
description: Création de l'image de récupération DaRT7.0
author: dansimp
ms.assetid: ebb2ec58-0349-469d-a23f-3f944fe4c1fa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f19ff144cac61ca7ea5a8498f67caf8a99229d77
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809863"
---
# <span data-ttu-id="78822-103">Création de l'image de récupération DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="78822-103">Creating the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="78822-104">Microsoft Diagnostics and Recovery Tools (DaRT) 7 inclut l' **Assistant image de récupération DART** utilisé dans Windows pour créer une image ISO (International Organization for Standardization) amorçable.</span><span class="sxs-lookup"><span data-stu-id="78822-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes the **DaRT Recovery Image Wizard** that is used in Windows to create a bootable International Organization for Standardization (ISO) image.</span></span> <span data-ttu-id="78822-105">Une image ISO est un fichier qui représente le contenu brut d’un CD.</span><span class="sxs-lookup"><span data-stu-id="78822-105">An ISO image is a file that represents the raw contents of a CD.</span></span>

## <span data-ttu-id="78822-106">Utiliser l’Assistant image de récupération DaRT pour créer l’image de récupération</span><span class="sxs-lookup"><span data-stu-id="78822-106">Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>


<span data-ttu-id="78822-107">La feuille de style ISO créée par l’Assistant image de récupération DaRT contient l’image de récupération DaRT qui vous permet d’effectuer un démarrage sur un ordinateur défectueux, même si cela n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="78822-107">The ISO created by the DaRT Recovery Image Wizard contains the DaRT recovery image that lets you boot into a problem computer, even if it might otherwise not start.</span></span> <span data-ttu-id="78822-108">Après avoir amorcé l’ordinateur dans DaRT, vous pouvez exécuter les différents outils DaRT pour essayer de diagnostiquer et de réparer l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="78822-108">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span>

<span data-ttu-id="78822-109">Vous pouvez enregistrer le fichier ISO sur un CD ou un DVD enregistrable, l’enregistrer sur un disque mémoire flash ou l’enregistrer dans un format que vous pouvez utiliser pour démarrer dans DaRT à partir d’une partition distante ou d’une partition de récupération.</span><span class="sxs-lookup"><span data-stu-id="78822-109">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span> <span data-ttu-id="78822-110">Pour plus d’informations, reportez-vous à [déploiement de l’image de récupération 7,0 de DART](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="78822-110">For more information, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

<span data-ttu-id="78822-111">**Remarques**  Si votre ordinateur inclut un lecteur CD-RW, l’Assistant propose de graver l’image ISO sur un CD ou un DVD vierge.</span><span class="sxs-lookup"><span data-stu-id="78822-111">**Note** If your computer includes a CD-RW drive, the wizard offers to burn the ISO image to a blank CD or DVD.</span></span> <span data-ttu-id="78822-112">Si votre ordinateur n’inclut pas de lecteur pris en charge par l’Assistant, vous pouvez graver l’image ISO sur un CD ou un DVD à l’aide de la plupart des programmes qui peuvent graver un CD ou un DVD.</span><span class="sxs-lookup"><span data-stu-id="78822-112">If your computer does not include a drive that is supported by the wizard, you can burn the ISO image onto a CD or DVD by using most programs that can burn a CD or DVD.</span></span>

 

<span data-ttu-id="78822-113">Pour créer un CD ou un DVD amorçable à partir de l’image ISO, vous devez disposer des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="78822-113">To create a bootable CD or DVD from the ISO image, you must have:</span></span>

-   <span data-ttu-id="78822-114">Un lecteur CD-RW.</span><span class="sxs-lookup"><span data-stu-id="78822-114">A CD-RW drive.</span></span>

-   <span data-ttu-id="78822-115">Un CD ou un DVD enregistrable (dans un format pris en charge par le graveur).</span><span class="sxs-lookup"><span data-stu-id="78822-115">A recordable CD or DVD (in a format supported by the recordable drive).</span></span>

-   <span data-ttu-id="78822-116">Logiciel prenant en charge le disque enregistrable et prenant en charge la gravure d’une image ISO directement sur un CD ou un DVD.</span><span class="sxs-lookup"><span data-stu-id="78822-116">Software that supports the recordable drive and supports burning an ISO image directly to CD or DVD.</span></span>

    <span data-ttu-id="78822-117">**Important**  Testez le CD ou DVD que vous créez sur les différents types d’ordinateurs que vous envisagez de prendre en charge, car certains ordinateurs ne peuvent pas démarrer à partir de tous les types de média enregistrables.</span><span class="sxs-lookup"><span data-stu-id="78822-117">**Important** Test the CD or DVD that you create on all the different kinds of computers that you intend to support because some computers cannot start from all kinds of recordable media.</span></span>

     

<span data-ttu-id="78822-118">Pour enregistrer l’image ISO sur un disque mémoire USB (UFD), vous devez disposer des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="78822-118">To save the ISO image to a USB flash drive (UFD), you must have:</span></span>

-   <span data-ttu-id="78822-119">UFD.</span><span class="sxs-lookup"><span data-stu-id="78822-119">A correctly formatted UFD.</span></span>

-   <span data-ttu-id="78822-120">Programme que vous pouvez utiliser pour monter l’image ISO.</span><span class="sxs-lookup"><span data-stu-id="78822-120">A program that you can use to mount the ISO image.</span></span>

[<span data-ttu-id="78822-121">Procédure d'utilisation de l'Assistant Image de récupération DaRT pour créer l'image de récupération</span><span class="sxs-lookup"><span data-stu-id="78822-121">How to Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md)

## <span data-ttu-id="78822-122">Créer une image de récupération de type Time Limit</span><span class="sxs-lookup"><span data-stu-id="78822-122">Create a Time Limited Recovery Image</span></span>


<span data-ttu-id="78822-123">Vous pouvez créer une image de récupération DaRT qui ne peut être utilisée que pendant un certain nombre de jours après sa génération.</span><span class="sxs-lookup"><span data-stu-id="78822-123">You can create a DaRT recovery image that can only be used for a certain number of days after it is generated.</span></span> <span data-ttu-id="78822-124">Pour cela, vous devez exécuter l' **Assistant image de récupération DART** à une invite de commandes et spécifier le nombre de jours.</span><span class="sxs-lookup"><span data-stu-id="78822-124">To do this, you must run the **DaRT Recovery Image Wizard** at a command prompt and specify the number of days.</span></span>

[<span data-ttu-id="78822-125">Procédure de création d'une image de récupération limitée dans le temps</span><span class="sxs-lookup"><span data-stu-id="78822-125">How to Create a Time Limited Recovery Image</span></span>](how-to-create-a-time-limited-recovery-image-dart-7.md)

## <span data-ttu-id="78822-126">Autres ressources pour créer l’image de récupération DaRT7</span><span class="sxs-lookup"><span data-stu-id="78822-126">Other resources for creating the DaRT7 recovery image</span></span>


-   [<span data-ttu-id="78822-127">Déploiement de DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="78822-127">Deploying DaRT 7.0</span></span>](deploying-dart-70-new-ia.md)

 

 





