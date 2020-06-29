---
title: Procédure pour déployer l'image de récupération DaRT sous forme de partition distante
description: Procédure pour déployer l'image de récupération DaRT sous forme de partition distante
author: dansimp
ms.assetid: 06a5e250-b992-4f6a-ad74-e7715f9e96e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3cdb1313a64bacd652a5253c09f36fa792d0fa3c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804698"
---
# <span data-ttu-id="59ddb-103">Procédure pour déployer l'image de récupération DaRT sous forme de partition distante</span><span class="sxs-lookup"><span data-stu-id="59ddb-103">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="59ddb-104">Lorsque vous avez fini d’exécuter l’Assistant image de récupération Microsoft Diagnostics et Recovery Tools (DaRT) 10 et créé l’image de récupération, vous pouvez extraire le fichier Boot. wim du fichier image ISO et le déployer en tant que partition distante sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="59ddb-104">After you have finished running the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

**<span data-ttu-id="59ddb-105">Pour déployer DaRT 10 en tant que partition distante</span><span class="sxs-lookup"><span data-stu-id="59ddb-105">To deploy DaRT 10 as a remote partition</span></span>**

1.  <span data-ttu-id="59ddb-106">Extrayez le fichier Boot. wim du fichier image ISO DaRT.</span><span class="sxs-lookup"><span data-stu-id="59ddb-106">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="59ddb-107">Montez le fichier image ISO que vous avez créé dans la boîte de dialogue **créer une image de démarrage** en utilisant la méthode préférée de montage d’une image par votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="59ddb-107">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="59ddb-108">Ouvrez le fichier image ISO et copiez le fichier Boot. wim du dossier \\sources de l’image montée vers un emplacement sur votre ordinateur ou sur un lecteur externe.</span><span class="sxs-lookup"><span data-stu-id="59ddb-108">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="59ddb-109">**Remarques**  Si vous avez gravé un CD ou un DVD de l’image de récupération, vous pouvez ouvrir les fichiers sur le CD-ROM ou le DVD et copier le fichier Boot. wim à partir du dossier \\sources.</span><span class="sxs-lookup"><span data-stu-id="59ddb-109">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="59ddb-110">Cela vous permet d’ignorer la nécessité de monter l’image.</span><span class="sxs-lookup"><span data-stu-id="59ddb-110">This lets you skip the need to mount the image.</span></span>

         

2.  <span data-ttu-id="59ddb-111">Déployez le fichier Boot. wim sur un serveur WDS accessible à partir d’ordinateurs d’utilisateurs finaux de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="59ddb-111">Deploy the boot.wim file to a WDS server that can be accessed from end-user computers in your enterprise.</span></span>

3.  <span data-ttu-id="59ddb-112">Configurez le serveur WDS pour qu’il utilise le fichier Boot. wim pour DaRT en suivant les procédures de déploiement standard de WDS.</span><span class="sxs-lookup"><span data-stu-id="59ddb-112">Configure the WDS server to use the boot.wim file for DaRT by following your standard WDS deployment procedures.</span></span>

<span data-ttu-id="59ddb-113">Pour plus d’informations sur le déploiement de DaRT en tant que partition distante, voir [procédure pas à pas: déploiement d’une image à l’aide](https://go.microsoft.com/fwlink/?LinkId=212108) du Guide de mise en route de PXE et [Windows Deployment Services](https://go.microsoft.com/fwlink/?LinkId=212106).</span><span class="sxs-lookup"><span data-stu-id="59ddb-113">For more information about how to deploy DaRT as a remote partition, see [Walkthrough: Deploy an Image by Using PXE](https://go.microsoft.com/fwlink/?LinkId=212108) and [Windows Deployment Services Getting Started Guide](https://go.microsoft.com/fwlink/?LinkId=212106).</span></span>

## <span data-ttu-id="59ddb-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="59ddb-114">Related topics</span></span>


[<span data-ttu-id="59ddb-115">Création de l'image de récupération DaRT10</span><span class="sxs-lookup"><span data-stu-id="59ddb-115">Creating the DaRT 10 Recovery Image</span></span>](creating-the-dart-10-recovery-image.md)

[<span data-ttu-id="59ddb-116">Déploiement de l'image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="59ddb-116">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-10.md)

[<span data-ttu-id="59ddb-117">Planification de DaRT10</span><span class="sxs-lookup"><span data-stu-id="59ddb-117">Planning for DaRT 10</span></span>](planning-for-dart-10.md)

 

 





