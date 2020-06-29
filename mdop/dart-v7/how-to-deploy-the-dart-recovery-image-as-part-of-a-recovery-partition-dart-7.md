---
title: Procédure pour déployer l'image de récupération DaRT dans le cadre d'une partition de récupération
description: Procédure pour déployer l'image de récupération DaRT dans le cadre d'une partition de récupération
author: dansimp
ms.assetid: 462f2d08-f03b-4a07-b2d3-c69205dc6f70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e75c3f9e58d784c13003feb84001f89c4607115d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810026"
---
# <span data-ttu-id="8ffca-103">Procédure pour déployer l'image de récupération DaRT dans le cadre d'une partition de récupération</span><span class="sxs-lookup"><span data-stu-id="8ffca-103">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="8ffca-104">Lorsque vous avez fini d’exécuter l’Assistant image de récupération DaRT et créé l’image de récupération, vous pouvez extraire le fichier Boot. wim du fichier image ISO et le déployer en tant que partition de récupération dans une image Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8ffca-104">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 7 image.</span></span>

**<span data-ttu-id="8ffca-105">Pour déployer DaRT dans la partition de récupération d’une image Windows 7</span><span class="sxs-lookup"><span data-stu-id="8ffca-105">To deploy DaRT in the recovery partition of a Windows 7 image</span></span>**

1.  <span data-ttu-id="8ffca-106">Créez une partition cible dans votre image Windows 7 qui est égale ou supérieure à la taille du fichier image ISO que vous avez créé à l’aide de l' **Assistant image de récupération DART**.</span><span class="sxs-lookup"><span data-stu-id="8ffca-106">Create a target partition in your Windows 7 image that is equal to or greater than the size of the ISO image file that you created by using the **DaRT Recovery Image Wizard**.</span></span>

    <span data-ttu-id="8ffca-107">La taille minimale requise pour une partition DaRT est d’environ 300 Mo.</span><span class="sxs-lookup"><span data-stu-id="8ffca-107">The minimum size required for a DaRT partition is approximately 300MB.</span></span> <span data-ttu-id="8ffca-108">Toutefois, nous recommandons à 450MB de prendre en charge les fonctionnalités de connexion à distance dans DaRT.</span><span class="sxs-lookup"><span data-stu-id="8ffca-108">However, we recommend 450MB to accommodate for the remote connection functionality in DaRT.</span></span>

2.  <span data-ttu-id="8ffca-109">Extrayez le fichier Boot. wim du fichier image ISO DaRT.</span><span class="sxs-lookup"><span data-stu-id="8ffca-109">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="8ffca-110">Montez le fichier image ISO que vous avez créé dans la boîte de dialogue **créer une image de démarrage** en utilisant la méthode préférée de montage d’une image par votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="8ffca-110">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="8ffca-111">Ouvrez le fichier image ISO et copiez le fichier Boot. wim du dossier \\sources de l’image montée vers un emplacement sur votre ordinateur ou sur un lecteur externe.</span><span class="sxs-lookup"><span data-stu-id="8ffca-111">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="8ffca-112">**Remarques**  Si vous avez gravé un CD ou un DVD de l’image de récupération, vous pouvez ouvrir les fichiers sur le CD-ROM ou le DVD et copier le fichier Boot. wim à partir du dossier \\sources.</span><span class="sxs-lookup"><span data-stu-id="8ffca-112">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="8ffca-113">Cela vous permet d’ignorer la nécessité de monter l’image.</span><span class="sxs-lookup"><span data-stu-id="8ffca-113">This lets you skip the need to mount the image.</span></span>

         

3.  <span data-ttu-id="8ffca-114">Utilisez le fichier Boot. wim pour créer une partition de récupération démarrable en utilisant la méthode standard de votre entreprise pour créer une image Windows RE personnalisée.</span><span class="sxs-lookup"><span data-stu-id="8ffca-114">Use the boot.wim file to create a bootable recovery partition by using your company’s standard method for creating a custom Windows RE image.</span></span>

    <span data-ttu-id="8ffca-115">Pour plus d’informations sur la création et la personnalisation d’une partition de récupération, voir [Personnalisation de l’utilisation de Windows RE](https://go.microsoft.com/fwlink/?LinkId=214222).</span><span class="sxs-lookup"><span data-stu-id="8ffca-115">For more information about how to create or customize a recovery partition, see [Customizing the Windows RE Experience](https://go.microsoft.com/fwlink/?LinkId=214222).</span></span>

4.  <span data-ttu-id="8ffca-116">Remplacez la partition cible dans votre image Windows 7 par la partition de récupération.</span><span class="sxs-lookup"><span data-stu-id="8ffca-116">Replace the target partition in your Windows 7 image with the recovery partition.</span></span>

<span data-ttu-id="8ffca-117">Lorsque votre image de Windows 7 est prête, répartir l’image sur les ordinateurs de votre entreprise à l’aide du processus de déploiement d’images standard de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="8ffca-117">After your Windows 7 image is ready, distribute the image to computers in your enterprise by using your company’s standard image deployment process.</span></span> <span data-ttu-id="8ffca-118">Pour plus d’informations sur la création d’une image Windows 7, voir [création d’une image standard de Windows 7: guide étape par étape](https://go.microsoft.com/fwlink/?LinkId=212103).</span><span class="sxs-lookup"><span data-stu-id="8ffca-118">For more information about how to create a Windows 7 image, see [Building a Standard Image of Windows 7: Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=212103).</span></span>

<span data-ttu-id="8ffca-119">Pour plus d’informations sur le déploiement d’une solution de récupération pour réinstaller l’image de fabrique en cas de panne du système, voir [déployer une image de récupération du système](https://go.microsoft.com/fwlink/?LinkId=214221).</span><span class="sxs-lookup"><span data-stu-id="8ffca-119">For more information about how to deploy a recovery solution to reinstall the factory image in the event of a system failure, see [Deploy a System Recovery Image](https://go.microsoft.com/fwlink/?LinkId=214221).</span></span>

## <span data-ttu-id="8ffca-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ffca-120">Related topics</span></span>


[<span data-ttu-id="8ffca-121">Déploiement de l'image de récupération DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="8ffca-121">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





