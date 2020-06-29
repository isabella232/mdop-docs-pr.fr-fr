---
title: Installation d'applications sur une image WindowsVirtualPC
description: Installation d'applications sur une image WindowsVirtualPC
author: dansimp
ms.assetid: 32651eff-e3c6-4ef4-947d-2beddc695eac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bf73fec0b33b37c2553dfe6f923917aa926b8e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811993"
---
# <span data-ttu-id="dc89a-103">Installation d'applications sur une image WindowsVirtualPC</span><span class="sxs-lookup"><span data-stu-id="dc89a-103">Installing Applications on a Windows Virtual PC Image</span></span>


<span data-ttu-id="dc89a-104">Une fois que vous avez créé une image de PC virtuel Windows pour une utilisation avec la version 2,0 de Microsoft Enterprise Desktop Virtualization (MED-V), vous pouvez installer d’autres composants utiles lors de l’exécution de MED-V, tel qu’un système de distribution de logiciels électroniques et un logiciel antivirus.</span><span class="sxs-lookup"><span data-stu-id="dc89a-104">After you have created a Windows Virtual PC image for use with Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you can install other components that are helpful when running MED-V, such as an electronic software distribution (ESD) system and antivirus software.</span></span>

<span data-ttu-id="dc89a-105">La section suivante fournit des informations pour vous aider à installer des logiciels sur l’image MED-V.</span><span class="sxs-lookup"><span data-stu-id="dc89a-105">The following section provides information to help you install software on the MED-V image.</span></span>

<span data-ttu-id="dc89a-106">**Attention**  Pour faciliter la gestion de l’espace de travail MED-V après le déploiement, nous vous recommandons de limiter le nombre de composants installés sur l’image MED-V aux composants requis ou utiles lors de l’utilisation de MED-V.</span><span class="sxs-lookup"><span data-stu-id="dc89a-106">**Caution** For ease of MED-V workspace management after deployment, we recommend that you limit the number of components that you install on the MED-V image to those components that are required or that are helpful when using MED-V.</span></span> <span data-ttu-id="dc89a-107">Par exemple, même si elles ne sont pas requises pour exécuter MED-V, vous pouvez installer un système ESD à utiliser ultérieurement pour l’installation d’applications sur un espace de travail et un logiciel antivirus MED-V pour la sécurité de l’image.</span><span class="sxs-lookup"><span data-stu-id="dc89a-107">For example, although they are not required to run MED-V, you can install an ESD system to use later for installing applications to a MED-V workspace and antivirus software for security on the image.</span></span>

 

**<span data-ttu-id="dc89a-108">Installation de logiciels sur une image MED-V</span><span class="sxs-lookup"><span data-stu-id="dc89a-108">Installing Software on a MED-V Image</span></span>**

1.  <span data-ttu-id="dc89a-109">S’il n’est pas en cours d’exécution, ouvrez votre machine virtuelle MED-V.</span><span class="sxs-lookup"><span data-stu-id="dc89a-109">If it is not currently running, open your MED-V virtual machine.</span></span>

    1.  <span data-ttu-id="dc89a-110">Cliquez sur **Démarrer**, sur **tous les programmes**, sur **PC virtuel Windows** , puis sur **PC virtuel Windows**.</span><span class="sxs-lookup"><span data-stu-id="dc89a-110">Click **Start**, click **All Programs**, click **Windows Virtual PC** and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="dc89a-111">Double-cliquez sur votre machine virtuelle MED-V.</span><span class="sxs-lookup"><span data-stu-id="dc89a-111">Double-click your MED-V virtual machine.</span></span>

2.  <span data-ttu-id="dc89a-112">À partir du système d’exploitation de l’ordinateur virtuel, recherchez les fichiers d’installation pour le logiciel que vous voulez installer.</span><span class="sxs-lookup"><span data-stu-id="dc89a-112">From inside the virtual machine operating system, locate the installation files for the software that you want to install.</span></span>

3.  <span data-ttu-id="dc89a-113">Suivez les instructions d’installation fournies par le fabricant du logiciel.</span><span class="sxs-lookup"><span data-stu-id="dc89a-113">Follow the installation instructions that are provided by the software vendor.</span></span>

    <span data-ttu-id="dc89a-114">**Remarques**  Une fois l’installation terminée, vous devrez peut-être fermer, puis redémarrer l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="dc89a-114">**Note** After installation is complete, you might have to close and then restart the virtual machine.</span></span>

     

<span data-ttu-id="dc89a-115">Répétez ces étapes pour tout logiciel ou application que vous souhaitez installer sur l’image MED-V.</span><span class="sxs-lookup"><span data-stu-id="dc89a-115">Repeat these steps for any software or application that you want to install on the MED-V image.</span></span> <span data-ttu-id="dc89a-116">Nous vous recommandons de limiter le nombre d’applications que vous préinstallez sur l’image.</span><span class="sxs-lookup"><span data-stu-id="dc89a-116">We recommend that you limit the number of applications that you preinstall on the image.</span></span> <span data-ttu-id="dc89a-117">Le processus recommandé pour l’installation d’applications et d’autres logiciels sur l’image consiste à préinstaller un système ESD dès maintenant et à l’utiliser ultérieurement pour déployer le logiciel sur l’image.</span><span class="sxs-lookup"><span data-stu-id="dc89a-117">The recommended process for installing applications and other software on the image is to preinstall an ESD system now and to use it later to deploy software to the image.</span></span> <span data-ttu-id="dc89a-118">Vous pouvez également utiliser une stratégie de groupe ou App-V pour ajouter ou supprimer des applications sur un espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="dc89a-118">Alternately, you can also use Group Policy or App-V to add or remove applications on a MED-V workspace.</span></span> <span data-ttu-id="dc89a-119">Pour plus d’informations, reportez-vous [à gestion des applications déployées dans les espaces de travail MED-V](managing-applications-deployed-to-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="dc89a-119">For more information, see [Managing Applications Deployed to MED-V Workspaces](managing-applications-deployed-to-med-v-workspaces.md).</span></span>

<span data-ttu-id="dc89a-120">Pour plus d’informations sur l’installation de logiciels sur une image virtuelle, voir les articles suivants:</span><span class="sxs-lookup"><span data-stu-id="dc89a-120">For more information about how to install software on a virtual image, see the following articles:</span></span>

-   <span data-ttu-id="dc89a-121">[Publier et utiliser des applications virtuelles](https://go.microsoft.com/fwlink/?LinkId=195926) ( https://go.microsoft.com/fwlink/?LinkId=195926) .</span><span class="sxs-lookup"><span data-stu-id="dc89a-121">[Publish and Use Virtual Applications](https://go.microsoft.com/fwlink/?LinkId=195926) (https://go.microsoft.com/fwlink/?LinkId=195926).</span></span>

-   <span data-ttu-id="dc89a-122">[Aide de l’application Virtual PC Windows](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .</span><span class="sxs-lookup"><span data-stu-id="dc89a-122">[Windows Virtual PC Help](https://go.microsoft.com/fwlink/?LinkId=182378) (https://go.microsoft.com/fwlink/?LinkId=182378).</span></span>

<span data-ttu-id="dc89a-123">Une fois que vous avez installé le logiciel souhaité sur l’image MED-V, votre image est prête à être empaquetée.</span><span class="sxs-lookup"><span data-stu-id="dc89a-123">After you have installed all of the software that you want on the MED-V image, your image is ready to be packaged.</span></span>

## <span data-ttu-id="dc89a-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dc89a-124">Related topics</span></span>


[<span data-ttu-id="dc89a-125">Configuration d'une image Windows Virtual PC pour MED-V</span><span class="sxs-lookup"><span data-stu-id="dc89a-125">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="dc89a-126">Préparer une image MED-V</span><span class="sxs-lookup"><span data-stu-id="dc89a-126">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)

 

 





