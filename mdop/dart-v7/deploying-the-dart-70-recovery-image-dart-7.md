---
title: Déploiement de l'image de récupération DaRT7.0
description: Déploiement de l'image de récupération DaRT7.0
author: dansimp
ms.assetid: 6bba7bff-800f-44e4-bcfc-e143115607ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cef626e50bf1049529c51afca5e536b03b3d915d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804392"
---
# <span data-ttu-id="f56d4-103">Déploiement de l'image de récupération DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="f56d4-103">Deploying the DaRT 7.0 Recovery Image</span></span>


<span data-ttu-id="f56d4-104">Une fois que vous avez créé le fichier ISO (International Organization for Standardization) qui contient l’image de récupération du Microsoft Diagnostics and Recovery Tools (DaRT) 7, vous pouvez déployer l’image de récupération DaRT dans l’ensemble de votre entreprise afin qu’elle soit disponible pour les utilisateurs finaux et les agents du support technique.</span><span class="sxs-lookup"><span data-stu-id="f56d4-104">After you have created the International Organization for Standardization (ISO) file that contains the Microsoft Diagnostics and Recovery Toolset (DaRT)7 recovery image, you can deploy the DaRT recovery image throughout your enterprise so that it is available to end users and helpdesk agents.</span></span> <span data-ttu-id="f56d4-105">Il existe quatre méthodes prises en charge que vous pouvez utiliser pour déployer l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="f56d4-105">There are four supported methods that you can use to deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="f56d4-106">Gravez le fichier image ISO sur un CD ou un DVD</span><span class="sxs-lookup"><span data-stu-id="f56d4-106">Burn the ISO image file to a CD or DVD</span></span>

-   <span data-ttu-id="f56d4-107">Enregistrez le contenu du fichier image ISO sur un disque mémoire flash USB (UFD).</span><span class="sxs-lookup"><span data-stu-id="f56d4-107">Save the contents of the ISO image file to a USB Flash Drive (UFD)</span></span>

-   <span data-ttu-id="f56d4-108">Extraire le fichier Boot. wim de l’image ISO et le déployer en tant que partition distante disponible sur les ordinateurs des utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="f56d4-108">Extract the boot.wim file from the ISO image and deploy as a remote partition that is available to end-user computers</span></span>

-   <span data-ttu-id="f56d4-109">Extraire le fichier Boot. wim de l’image ISO et le déployer dans la partition de récupération d’une nouvelle installation de Windows 7</span><span class="sxs-lookup"><span data-stu-id="f56d4-109">Extract the boot.wim file from the ISO image and deploy in the recovery partition of a new Windows 7 installation</span></span>

<span data-ttu-id="f56d4-110">**Important**  L' **Assistant image de récupération DART** vous permet uniquement de graver un CD ou un DVD.</span><span class="sxs-lookup"><span data-stu-id="f56d4-110">**Important** The **DaRT Recovery Image Wizard** only provides the option to burn a CD or DVD.</span></span> <span data-ttu-id="f56d4-111">Toutes les autres méthodes d’enregistrement et de déploiement de l’image de récupération nécessitent des étapes supplémentaires qui impliquent des outils qui ne sont pas inclus dans DaRT.</span><span class="sxs-lookup"><span data-stu-id="f56d4-111">All other methods of saving and deploying the recovery image require additional steps that involve tools that are not included in DaRT.</span></span> <span data-ttu-id="f56d4-112">Des conseils et des liens pour ces autres méthodes sont fournis dans cette section.</span><span class="sxs-lookup"><span data-stu-id="f56d4-112">Some guidance and links for these other methods are provided in this section.</span></span>

 

## <span data-ttu-id="f56d4-113">Déploiement de l’image de récupération DaRT à l’aide d’un lecteur flash USB</span><span class="sxs-lookup"><span data-stu-id="f56d4-113">Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>


<span data-ttu-id="f56d4-114">Lorsque vous avez fini d’exécuter l’Assistant image de récupération DaRT, vous pouvez utiliser l’outil sur <https://go.microsoft.com/fwlink/?LinkId=218888> pour copier le fichier image ISO sur un disque mémoire flash USB (UFD).</span><span class="sxs-lookup"><span data-stu-id="f56d4-114">After you have finished running the DaRT Recovery Image Wizard, you can use the tool at <https://go.microsoft.com/fwlink/?LinkId=218888> to copy the ISO image file to a USB flash drive (UFD).</span></span>

[<span data-ttu-id="f56d4-115">Procédure pour déployer l'image de récupération DaRT à l'aide d'une clé USB</span><span class="sxs-lookup"><span data-stu-id="f56d4-115">How to Deploy the DaRT Recovery Image Using a USB Flash Drive</span></span>](how-to-deploy-the-dart-recovery-image-using-a-usb-flash-drive-dart-7.md)

## <span data-ttu-id="f56d4-116">Déploiement de l’image de récupération DaRT dans le cadre d’une partition de récupération</span><span class="sxs-lookup"><span data-stu-id="f56d4-116">Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>


<span data-ttu-id="f56d4-117">Lorsque vous avez fini d’exécuter l’Assistant image de récupération DaRT et créé l’image de récupération, vous pouvez extraire le fichier Boot. wim du fichier image ISO et le déployer en tant que partition de récupération dans une image Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f56d4-117">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 7 image.</span></span>

[<span data-ttu-id="f56d4-118">Procédure pour déployer l'image de récupération DaRT dans le cadre d'une partition de récupération</span><span class="sxs-lookup"><span data-stu-id="f56d4-118">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-7.md)

## <span data-ttu-id="f56d4-119">Déploiement de l’image de récupération DaRT en tant que partition distante</span><span class="sxs-lookup"><span data-stu-id="f56d4-119">Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="f56d4-120">Lorsque vous avez fini d’exécuter l’Assistant image de récupération DaRT et créé l’image de récupération, vous pouvez extraire le fichier Boot. wim du fichier image ISO et le déployer en tant que partition distante sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="f56d4-120">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

[<span data-ttu-id="f56d4-121">Procédure pour déployer l'image de récupération DaRT sous forme de partition distante</span><span class="sxs-lookup"><span data-stu-id="f56d4-121">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-7.md)

## <span data-ttu-id="f56d4-122">Autres ressources pour la mise à jour du déploiement de l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="f56d4-122">Other resources for maintaining Deploying the DaRT Recovery Image</span></span>


-   [<span data-ttu-id="f56d4-123">Déploiement de DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="f56d4-123">Deploying DaRT 7.0</span></span>](deploying-dart-70-new-ia.md)

 

 





