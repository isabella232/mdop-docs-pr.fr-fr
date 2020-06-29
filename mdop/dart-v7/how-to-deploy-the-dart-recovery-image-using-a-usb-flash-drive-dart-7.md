---
title: Procédure pour déployer l'image de récupération DaRT à l'aide d'une clé USB
description: Procédure pour déployer l'image de récupération DaRT à l'aide d'une clé USB
author: dansimp
ms.assetid: 5b7aa843-731e-47e7-b5f9-48d08da732d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1228c9cb5f870162f285d726d48721dde1185107
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810092"
---
# <span data-ttu-id="fcec4-103">Procédure pour déployer l'image de récupération DaRT à l'aide d'une clé USB</span><span class="sxs-lookup"><span data-stu-id="fcec4-103">How to Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>


<span data-ttu-id="fcec4-104">Lorsque vous avez fini d’exécuter l' **Assistant image de récupération DART**, vous pouvez utiliser l’outil sur <https://go.microsoft.com/fwlink/?LinkId=218888> pour copier le fichier image ISO sur un disque mémoire flash USB (UFD).</span><span class="sxs-lookup"><span data-stu-id="fcec4-104">After you have finished running the **DaRT Recovery Image Wizard**, you can use the tool at <https://go.microsoft.com/fwlink/?LinkId=218888> to copy the ISO image file to a USB flash drive (UFD).</span></span>

<span data-ttu-id="fcec4-105">Vous pouvez également copier manuellement le fichier image ISO sur un disque UFD en suivant les étapes décrites dans cette section.</span><span class="sxs-lookup"><span data-stu-id="fcec4-105">You can also manually copy the ISO image file to a UFD by following the steps provided in this section.</span></span>

**<span data-ttu-id="fcec4-106">Pour enregistrer l’image de récupération DaRT sur une clé USB</span><span class="sxs-lookup"><span data-stu-id="fcec4-106">To save the DaRT recovery image to a USB flash drive</span></span>**

1.  <span data-ttu-id="fcec4-107">Mettre en forme la clé USB.</span><span class="sxs-lookup"><span data-stu-id="fcec4-107">Format the USB flash drive.</span></span>

    1.  <span data-ttu-id="fcec4-108">À partir d’un système d’exploitation valide ou d’une session WindowsPE, insérez votre UFD.</span><span class="sxs-lookup"><span data-stu-id="fcec4-108">From a running valid operating system or WindowsPE session, insert your UFD.</span></span>

    2.  <span data-ttu-id="fcec4-109">À l’invite de commandes avec des autorisations d’administrateur, tapez **diskpart** , puis tapez **List Disk**.</span><span class="sxs-lookup"><span data-stu-id="fcec4-109">At the command prompt with administrator permissions, type **DISKPART** and then type **LIST DISK**.</span></span>

        <span data-ttu-id="fcec4-110">La fenêtre d’invite de commandes affiche le numéro de disque de votre UFD (par exemple, **Disk 1**).</span><span class="sxs-lookup"><span data-stu-id="fcec4-110">The Command Prompt window displays the disk number of your UFD, for example **DISK 1**.</span></span>

    3.  <span data-ttu-id="fcec4-111">Entrez les commandes suivantes une à la fois à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="fcec4-111">Enter the following commands one at a time at the command prompt.</span></span>

        ``` syntax
        SELECT DISK 1
        CLEAN
        CREATE PARTITION PRIMARY
        SELECT PARTITION 1
        ACTIVE
        FORMAT FS=NTFS
        ASSIGN
        EXIT
        ```

        <span data-ttu-id="fcec4-112">**Remarques**  L’exemple de code précédent suppose que Disk1 est le UFD.</span><span class="sxs-lookup"><span data-stu-id="fcec4-112">**Note** The previous code example assumes Disk1 is the UFD.</span></span> <span data-ttu-id="fcec4-113">Le cas échéant, remplacez le disque 1 par le numéro de votre disque.</span><span class="sxs-lookup"><span data-stu-id="fcec4-113">If it is necessary, replace DISK 1 with your disk number.</span></span>

         

2.  <span data-ttu-id="fcec4-114">À l’aide de la méthode de montage préférée d’une image par votre entreprise, montez le fichier image ISO que vous avez créé dans la boîte de dialogue **créer une image de démarrage** de l' **Assistant image de récupération DART**.</span><span class="sxs-lookup"><span data-stu-id="fcec4-114">By using your company’s preferred method of mounting an image, mount the ISO image file that you created in the **Create Startup Image** dialog box of the **DaRT Recovery Image Wizard**.</span></span> <span data-ttu-id="fcec4-115">Pour cela, il est nécessaire d’avoir une méthode disponible pour monter un fichier image.</span><span class="sxs-lookup"><span data-stu-id="fcec4-115">This requires that you have a method available to mount an image file.</span></span>

3.  <span data-ttu-id="fcec4-116">Ouvrez le fichier image ISO monté et copiez son contenu sur la clé USB mise en forme.</span><span class="sxs-lookup"><span data-stu-id="fcec4-116">Open the mounted ISO image file and copy all its contents to the formatted USB flash drive.</span></span>

    <span data-ttu-id="fcec4-117">**Remarques**  Si vous avez gravé un CD ou un DVD de l’image de récupération, vous pouvez ouvrir les fichiers sur le CD ou DVD et copier le contenu sur le UFD.</span><span class="sxs-lookup"><span data-stu-id="fcec4-117">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the contents to the UFD.</span></span> <span data-ttu-id="fcec4-118">Cela vous permet d’ignorer la nécessité de monter l’image.</span><span class="sxs-lookup"><span data-stu-id="fcec4-118">This lets you skip the need to mount the image.</span></span>

     

## <span data-ttu-id="fcec4-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fcec4-119">Related topics</span></span>


[<span data-ttu-id="fcec4-120">Déploiement de l'image de récupération DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="fcec4-120">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





