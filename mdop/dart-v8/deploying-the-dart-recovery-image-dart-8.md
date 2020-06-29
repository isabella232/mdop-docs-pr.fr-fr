---
title: Déploiement de l'image de récupération DaRT
description: Déploiement de l'image de récupération DaRT
author: dansimp
ms.assetid: df5cb54a-be8c-4ed2-89ea-d3c67c2ef4d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e445873324f005455ba3c96319847dea8ba761ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810361"
---
# <span data-ttu-id="eb9db-103">Déploiement de l'image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="eb9db-103">Deploying the DaRT Recovery Image</span></span>


<span data-ttu-id="eb9db-104">Une fois que vous avez créé le fichier ISO (International Organization for Standardization) qui contient l’image de récupération du Microsoft Diagnostics and Recovery Tools (DaRT 8,0), vous pouvez déployer l’image de récupération de DaRT 8,0 au sein de votre entreprise afin qu’elle soit disponible aux utilisateurs finaux et aux travailleurs du support technique.</span><span class="sxs-lookup"><span data-stu-id="eb9db-104">After you have created the International Organization for Standardization (ISO) file that contains the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image, you can deploy the DaRT 8.0 recovery image throughout your enterprise so that it is available to end users and help desk workers.</span></span> <span data-ttu-id="eb9db-105">Il existe quatre méthodes prises en charge que vous pouvez utiliser pour déployer l’image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="eb9db-105">There are four supported methods that you can use to deploy the DaRT recovery image.</span></span> <span data-ttu-id="eb9db-106">Pour connaître les avantages et inconvénients de chaque méthode, voir [planification de l’enregistrement et du déploiement de l’image de récupération 8,0 de DART](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="eb9db-106">To review the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 8.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="eb9db-107">Gravez le fichier image ISO sur un CD ou un DVD à l’aide de l’Assistant image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="eb9db-107">Burn the ISO image file to a CD or DVD by using the DaRT Recovery Image wizard</span></span>

<span data-ttu-id="eb9db-108">Enregistrez le contenu du fichier image ISO sur un lecteur flash USB à l’aide de l’Assistant image de récupération DaRT.</span><span class="sxs-lookup"><span data-stu-id="eb9db-108">Save the contents of the ISO image file to a USB Flash Drive (UFD) by using the DaRT Recovery Image wizard</span></span>

<span data-ttu-id="eb9db-109">Extraire le fichier Boot. wim de l’image ISO et le déployer en tant que partition distante disponible sur les ordinateurs des utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="eb9db-109">Extract the boot.wim file from the ISO image and deploy as a remote partition that is available to end-user computers</span></span>

<span data-ttu-id="eb9db-110">Extraire le fichier Boot. wim de l’image ISO et le déployer dans la partition de récupération d’une nouvelle installation de Windows 8</span><span class="sxs-lookup"><span data-stu-id="eb9db-110">Extract the boot.wim file from the ISO image and deploy in the recovery partition of a new Windows 8 installation</span></span>

<span data-ttu-id="eb9db-111">**Important**  L' **Assistant image de récupération DART** vous permet de graver l’image sur un CD, un DVD ou un lecteur USB, mais les autres méthodes d’enregistrement et de déploiement de l’image de récupération nécessitent des étapes supplémentaires qui impliquent des outils qui ne sont pas inclus dans DART.</span><span class="sxs-lookup"><span data-stu-id="eb9db-111">**Important** The **DaRT Recovery Image Wizard** provides the option to burn the image to a CD, DVD or UFD, but the other methods of saving and deploying the recovery image require additional steps that involve tools that are not included in DaRT.</span></span> <span data-ttu-id="eb9db-112">Des conseils et des liens pour ces autres méthodes sont fournis dans cette section.</span><span class="sxs-lookup"><span data-stu-id="eb9db-112">Some guidance and links for these other methods are provided in this section.</span></span>

 

## <span data-ttu-id="eb9db-113">Déploiement de l’image de récupération DaRT dans le cadre d’une partition de récupération</span><span class="sxs-lookup"><span data-stu-id="eb9db-113">Deploy the DaRT recovery image as part of a recovery partition</span></span>


<span data-ttu-id="eb9db-114">Lorsque vous avez fini d’exécuter l’Assistant image de récupération DaRT et créé l’image de récupération, vous pouvez extraire le fichier Boot. wim du fichier image ISO et le déployer en tant que partition de récupération dans une image Windows 8.</span><span class="sxs-lookup"><span data-stu-id="eb9db-114">After you have finished running the DaRT Recovery Image wizard and created the recovery image, you can extract the boot.wim file from the ISO image file and deploy it as a recovery partition in a Windows 8 image.</span></span>

[<span data-ttu-id="eb9db-115">Procédure pour déployer l'image de récupération DaRT dans le cadre d'une partition de récupération</span><span class="sxs-lookup"><span data-stu-id="eb9db-115">How to Deploy the DaRT Recovery Image as Part of a Recovery Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-part-of-a-recovery-partition-dart-8.md)

## <span data-ttu-id="eb9db-116">Déploiement de l’image de récupération DaRT en tant que partition distante</span><span class="sxs-lookup"><span data-stu-id="eb9db-116">Deploy the DaRT recovery image as a remote partition</span></span>


<span data-ttu-id="eb9db-117">Vous pouvez héberger l’image de récupération sur un serveur de démarrage réseau central, tel que les services de déploiement Windows, et autoriser les utilisateurs ou l’équipe de support à diffuser une image sur des ordinateurs à la demande.</span><span class="sxs-lookup"><span data-stu-id="eb9db-117">You can host the recovery image on a central network boot server, such as Windows Deployment Services, and allow users or support staff to stream the image to computers on demand.</span></span>

[<span data-ttu-id="eb9db-118">Procédure pour déployer l'image de récupération DaRT sous forme de partition distante</span><span class="sxs-lookup"><span data-stu-id="eb9db-118">How to Deploy the DaRT Recovery Image as a Remote Partition</span></span>](how-to-deploy-the-dart-recovery-image-as-a-remote-partition-dart-8.md)

## <span data-ttu-id="eb9db-119">Autres ressources pour le déploiement de l’image de récupération DaRT</span><span class="sxs-lookup"><span data-stu-id="eb9db-119">Other resources for deploying the DaRT recovery image</span></span>


[<span data-ttu-id="eb9db-120">Déploiement de DaRT8.0</span><span class="sxs-lookup"><span data-stu-id="eb9db-120">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)

 

 





