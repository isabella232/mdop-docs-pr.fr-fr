---
title: Procédure pour déployer l'image de récupération DaRT sous forme de partition distante
description: Procédure pour déployer l'image de récupération DaRT sous forme de partition distante
author: dansimp
ms.assetid: 58f4a6c6-6193-42bd-a095-0de868711af9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e9a6e3a9dc25139210ae22ba767da984e9a7b86d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808652"
---
# <span data-ttu-id="5122c-103">Procédure pour déployer l'image de récupération DaRT sous forme de partition distante</span><span class="sxs-lookup"><span data-stu-id="5122c-103">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>


<span data-ttu-id="5122c-104">Lorsque vous avez terminé d’exécuter l’Assistant image de récupération de Microsoft Diagnostics et Recovery Tools (DaRT) 8,0 et créé l’image de récupération, vous pouvez extraire le fichier Boot. wim du fichier image ISO et le déployer en tant que partition distante sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="5122c-104">After you have finished running the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a remote partition on the network.</span></span>

**<span data-ttu-id="5122c-105">Pour déployer le DaRT 8,0 en tant que partition distante</span><span class="sxs-lookup"><span data-stu-id="5122c-105">To deploy DaRT 8.0 as a remote partition</span></span>**

1.  <span data-ttu-id="5122c-106">Extrayez le fichier Boot. wim du fichier image ISO DaRT.</span><span class="sxs-lookup"><span data-stu-id="5122c-106">Extract the boot.wim file from the DaRT ISO image file.</span></span>

    1.  <span data-ttu-id="5122c-107">Montez le fichier image ISO que vous avez créé dans la boîte de dialogue **créer une image de démarrage** en utilisant la méthode préférée de montage d’une image par votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="5122c-107">Mount the ISO image file that you created in the **Create Startup Image** dialog box by using your company’s preferred method of mounting an image.</span></span>

    2.  <span data-ttu-id="5122c-108">Ouvrez le fichier image ISO et copiez le fichier Boot. wim du dossier \\sources de l’image montée vers un emplacement sur votre ordinateur ou sur un lecteur externe.</span><span class="sxs-lookup"><span data-stu-id="5122c-108">Open the ISO image file and copy the boot.wim file from the \\sources folder in the mounted image to a location on your computer or on an external drive.</span></span>

        <span data-ttu-id="5122c-109">**Remarques**  Si vous avez gravé un CD ou un DVD de l’image de récupération, vous pouvez ouvrir les fichiers sur le CD-ROM ou le DVD et copier le fichier Boot. wim à partir du dossier \\sources.</span><span class="sxs-lookup"><span data-stu-id="5122c-109">**Note** If you burned a CD or DVD of the recovery image, you can open the files on the CD or DVD and copy the boot.wim file from the \\sources folder.</span></span> <span data-ttu-id="5122c-110">Cela vous permet d’ignorer la nécessité de monter l’image.</span><span class="sxs-lookup"><span data-stu-id="5122c-110">This lets you skip the need to mount the image.</span></span>

         

2.  <span data-ttu-id="5122c-111">Déployez le fichier Boot. wim sur un serveur WDS accessible à partir d’ordinateurs d’utilisateurs finaux de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="5122c-111">Deploy the boot.wim file to a WDS server that can be accessed from end-user computers in your enterprise.</span></span>

3.  <span data-ttu-id="5122c-112">Configurez le serveur WDS pour qu’il utilise le fichier Boot. wim pour DaRT en suivant les procédures de déploiement standard de WDS.</span><span class="sxs-lookup"><span data-stu-id="5122c-112">Configure the WDS server to use the boot.wim file for DaRT by following your standard WDS deployment procedures.</span></span>

<span data-ttu-id="5122c-113">Pour plus d’informations sur le déploiement de DaRT en tant que partition distante, voir [procédure pas à pas: déploiement d’une image à l’aide](https://go.microsoft.com/fwlink/?LinkId=212108) du Guide de mise en route de PXE et [Windows Deployment Services](https://go.microsoft.com/fwlink/?LinkId=212106).</span><span class="sxs-lookup"><span data-stu-id="5122c-113">For more information about how to deploy DaRT as a remote partition, see [Walkthrough: Deploy an Image by Using PXE](https://go.microsoft.com/fwlink/?LinkId=212108) and [Windows Deployment Services Getting Started Guide](https://go.microsoft.com/fwlink/?LinkId=212106).</span></span>

## <span data-ttu-id="5122c-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5122c-114">Related topics</span></span>


[<span data-ttu-id="5122c-115">Création de l'image de récupération DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="5122c-115">Creating the DaRT 8.0 Recovery Image</span></span>](creating-the-dart-80-recovery-image-dart-8.md)

[<span data-ttu-id="5122c-116">Déploiement de l'image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="5122c-116">Deploying the DaRT Recovery Image</span></span>](deploying-the-dart-recovery-image-dart-8.md)

[<span data-ttu-id="5122c-117">Planification de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="5122c-117">Planning for DaRT 8.0</span></span>](planning-for-dart-80-dart-8.md)

 

 





