---
title: Procédure pour charger des fichiers et des packages
description: Procédure pour charger des fichiers et des packages
author: dansimp
ms.assetid: f86f5bf1-99a4-44d7-ae2f-e6049c482f68
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9427fd8089ec9c22d7d379b15ae94bf421ca2d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807026"
---
# <span data-ttu-id="f53f1-103">Procédure pour charger des fichiers et des packages</span><span class="sxs-lookup"><span data-stu-id="f53f1-103">How to Load Files and Packages</span></span>


<span data-ttu-id="f53f1-104">Vous pouvez utiliser la procédure suivante pour charger des fichiers et des packages sur des serveurs de virtualisation des applications.</span><span class="sxs-lookup"><span data-stu-id="f53f1-104">You can use the following procedure to load files and packages on Application Virtualization Servers.</span></span>

<span data-ttu-id="f53f1-105">**Remarques**  Pendant le processus d’installation, vous avez spécifié l’emplacement du répertoire \\Content sur la page de **chemin d’accès au contenu** .</span><span class="sxs-lookup"><span data-stu-id="f53f1-105">**Note** During the installation process, you specified the location of the \\Content directory on the **Content Path** page.</span></span> <span data-ttu-id="f53f1-106">Ce répertoire doit être créé et configuré comme partage de fichiers standard avant de pointer sur son emplacement.</span><span class="sxs-lookup"><span data-stu-id="f53f1-106">This directory should be created and configured as a standard file share before you point to its location.</span></span>

 

**<span data-ttu-id="f53f1-107">Pour charger des fichiers et des packages</span><span class="sxs-lookup"><span data-stu-id="f53f1-107">To load files and packages</span></span>**

1.  <span data-ttu-id="f53f1-108">Sur l’ordinateur à partir duquel vous allez diffuser des applications, accédez à l’emplacement que vous avez spécifié pour le répertoire \\Content.</span><span class="sxs-lookup"><span data-stu-id="f53f1-108">On the computer from which you will stream applications, navigate to the location that you specified for the \\Content directory.</span></span> <span data-ttu-id="f53f1-109">Le cas échéant, créez le répertoire et configurez-le en tant que partage de fichiers standard.</span><span class="sxs-lookup"><span data-stu-id="f53f1-109">If necessary, create the directory and configure it as a standard file share.</span></span>

2.  <span data-ttu-id="f53f1-110">Déplacez les fichiers SFT pour les applications virtuelles et les packages vers le répertoire \\Content</span><span class="sxs-lookup"><span data-stu-id="f53f1-110">Move the SFT files for the virtual applications and packages to the \\Content directory.</span></span> <span data-ttu-id="f53f1-111">Pour que les fichiers SFT restent organisés et éviter toute confusion, placez les applications et les packages dans des sous-dossiers spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f53f1-111">To keep the SFT files organized and to avoid confusion, put applications and packages in dedicated subfolders.</span></span>

3.  <span data-ttu-id="f53f1-112">Chargez les applications et packages conformément aux exigences de votre scénario et de votre configuration, en prenant en compte les conditions suivantes:</span><span class="sxs-lookup"><span data-stu-id="f53f1-112">Load the applications and packages according to the requirements of your scenario and configuration, considering the following conditions:</span></span>

    -   <span data-ttu-id="f53f1-113">Si vos applications et packages sont stockés sur un serveur de gestion des applications (App-V), chargez-les via la console de gestion.</span><span class="sxs-lookup"><span data-stu-id="f53f1-113">If your applications and packages are stored on an Application Virtualization (App-V) Management Server, load them through the Management Console.</span></span> <span data-ttu-id="f53f1-114">Pour plus d’informations, voir [Comment charger ou décharger une application](how-to-load-or-unload-an-application.md) , ou [charger des applications virtuelles à partir de la zone de notification du Bureau](how-to-load-virtual-applications-from-the-desktop-notification-area.md).</span><span class="sxs-lookup"><span data-stu-id="f53f1-114">For more information, see [How to Load or Unload an Application](how-to-load-or-unload-an-application.md) or [How to Load Virtual Applications from the Desktop Notification Area](how-to-load-virtual-applications-from-the-desktop-notification-area.md).</span></span>

    -   <span data-ttu-id="f53f1-115">Si vos applications sont stockées sur un serveur de streaming d’application-V, un serveur Web ou un ordinateur configuré en tant que serveur de fichiers, les applications peuvent être chargées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f53f1-115">If your applications are stored on an App-V Streaming Server, a Web server, or a computer configured as a file server, the applications can be automatically loaded.</span></span>

        <span data-ttu-id="f53f1-116">**Remarques**  Le serveur de streaming App-V interroge automatiquement le répertoire \\Content des applications et des packages et place ces informations dans la mémoire RAM pour les demandes d’applications de service.</span><span class="sxs-lookup"><span data-stu-id="f53f1-116">**Note** The App-V Streaming Server automatically polls the \\Content directory for applications and packages and puts this information in RAM to service application requests.</span></span>

        <span data-ttu-id="f53f1-117">Les clients App-V doivent être correctement configurés pour récupérer des applications et des packages à partir de serveurs Web et de serveurs de fichiers.</span><span class="sxs-lookup"><span data-stu-id="f53f1-117">The App-V Clients must be properly configured to retrieve applications and packages from Web servers and file servers.</span></span> <span data-ttu-id="f53f1-118">Pour plus d’informations, reportez-vous [à configuration du client pour la récupération de package d’application](how-to-configure-the-client-for-application-package-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="f53f1-118">For more information, see [How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md).</span></span>

         

## <span data-ttu-id="f53f1-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f53f1-119">Related topics</span></span>


[<span data-ttu-id="f53f1-120">Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="f53f1-120">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





