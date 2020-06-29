---
title: Procédure pour déployer l'image de récupération DaRT sous forme de partition distante
description: Procédure pour déployer l'image de récupération DaRT sous forme de partition distante
author: dansimp
ms.assetid: 757c9340-8eac-42e8-85de-4302e436713a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a3acdbf72a2c6dac0238f868c7280f1c389b1311
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810032"
---
# <span data-ttu-id="da9ef-103">Procédure pour déployer l'image de récupération DaRT sous forme de partition distante</span><span class="sxs-lookup"><span data-stu-id="da9ef-103">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="da9ef-104">Lorsque vous avez fini d’exécuter l’Assistant image de récupération DaRT et créé l’image de récupération, vous pouvez extraire le fichier Boot. wim du fichier image ISO et le déployer en tant que partition distante sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="da9ef-104">After you have finished running the DaRT Recovery Image Wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

**<span data-ttu-id="da9ef-105">Pour déployer DaRT en tant que partition distante</span><span class="sxs-lookup"><span data-stu-id="da9ef-105">To deploy DaRT as a remote partition</span></span>**

1.  <span data-ttu-id="da9ef-106">Extrayez le fichier Boot. wim du fichier image ISO DaRT.</span><span class="sxs-lookup"><span data-stu-id="da9ef-106">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="da9ef-107">Montez le fichier image ISO que vous avez créé dans la boîte de dialogue **créer une image de démarrage** en utilisant la méthode préférée de montage d’une image par votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="da9ef-107">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="da9ef-108">Ouvrez le fichier image ISO et copiez le fichier Boot. wim du dossier \\sources de l’image montée vers un emplacement sur votre ordinateur ou sur un lecteur externe.</span><span class="sxs-lookup"><span data-stu-id="da9ef-108">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="da9ef-109">**Remarques**  Si vous avez gravé un CD ou un DVD de l’image de récupération, vous pouvez ouvrir les fichiers sur le CD-ROM ou le DVD et copier le fichier Boot. wim à partir du dossier \\sources.</span><span class="sxs-lookup"><span data-stu-id="da9ef-109">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="da9ef-110">Cela vous permet d’ignorer la nécessité de monter l’image.</span><span class="sxs-lookup"><span data-stu-id="da9ef-110">This lets you skip the need to mount the image.</span></span>

         

2.  <span data-ttu-id="da9ef-111">Déployez le fichier Boot. wim sur un serveur WDS accessible à partir d’ordinateurs d’utilisateurs finaux de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="da9ef-111">Deploy the boot.wim file to a WDS server that can be accessed from end-user computers in your enterprise.</span></span>

3.  <span data-ttu-id="da9ef-112">Configurez le serveur WDS pour qu’il utilise le fichier Boot. wim pour DaRT en suivant les procédures de déploiement standard de WDS.</span><span class="sxs-lookup"><span data-stu-id="da9ef-112">Configure the WDS server to use the boot.wim file for DaRT by following your standard WDS deployment procedures.</span></span>

<span data-ttu-id="da9ef-113">Pour plus d’informations sur le déploiement de DaRT en tant que partition distante, voir les rubriques suivantes:</span><span class="sxs-lookup"><span data-stu-id="da9ef-113">For more information about how to deploy DaRT as a remote partition, see the following:</span></span>

-   [<span data-ttu-id="da9ef-114">Procédure pas à pas: déploiement d’une image à l’aide de PXE</span><span class="sxs-lookup"><span data-stu-id="da9ef-114">Walkthrough: Deploy an Image by Using PXE</span></span>](https://go.microsoft.com/fwlink/?LinkId=212108)

-   [<span data-ttu-id="da9ef-115">Guide de mise en route de services de déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="da9ef-115">Windows Deployment Services Getting Started Guide</span></span>](https://go.microsoft.com/fwlink/?LinkId=212106)

## <span data-ttu-id="da9ef-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da9ef-116">Related topics</span></span>


[<span data-ttu-id="da9ef-117">Déploiement de l'image de récupération DaRT7.0</span><span class="sxs-lookup"><span data-stu-id="da9ef-117">Deploying the DaRT 7.0 Recovery Image</span></span>](deploying-the-dart-70-recovery-image-dart-7.md)

 

 





