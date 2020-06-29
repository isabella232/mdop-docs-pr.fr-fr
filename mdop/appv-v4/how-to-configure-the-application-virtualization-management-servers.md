---
title: Procédure pour configurer les serveurs Application Virtualization Management Server
description: Procédure pour configurer les serveurs Application Virtualization Management Server
author: dansimp
ms.assetid: a9f96148-bf2d-486f-98c2-23409bfb0935
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d6d54dd213efb8d5cbff5d0e730e6dc08c8d19b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807269"
---
# <span data-ttu-id="46c04-103">Procédure pour configurer les serveurs Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="46c04-103">How to Configure the Application Virtualization Management Servers</span></span>


<span data-ttu-id="46c04-104">Pour que les applications virtuelles puissent être diffusées sur le client de bureau de la virtualisation des applications ou sur le client pour les services Bureau à distance (auparavant services Terminal Server), le serveur de gestion des applications doit être configuré.</span><span class="sxs-lookup"><span data-stu-id="46c04-104">Before virtualized applications can be streamed to the Application Virtualization Desktop Client or the Client for Remote Desktop Services (formerly Terminal Services), the Application Virtualization Management Server must be configured.</span></span> <span data-ttu-id="46c04-105">Lorsque vous configurez le serveur, vous configurez le *Répertoire de contenu* dans lequel les fichiers SFT sont chargés et stockés.</span><span class="sxs-lookup"><span data-stu-id="46c04-105">When you configure the server, you are setting up the *content directory* where the SFT files are loaded and stored.</span></span> <span data-ttu-id="46c04-106">Les fichiers SFT contiennent l’application virtualisée (ou les applications).</span><span class="sxs-lookup"><span data-stu-id="46c04-106">The SFT files contain the virtualized application (or applications).</span></span>

<span data-ttu-id="46c04-107">**Important**  Les serveurs de virtualisation des applications diffusent des fichiers SFT au client de bureau et au client pour les services Bureau à distance en utilisant uniquement les protocoles RTSP ou RTSP.</span><span class="sxs-lookup"><span data-stu-id="46c04-107">**Important** Application Virtualization Servers stream SFT files to the Desktop Client and the Client for Remote Desktop Services using only RTSP or RTSPS protocols.</span></span> <span data-ttu-id="46c04-108">Il est possible de configurer le fichier ICO (icône) et l’OSD (Open Software Descriptor) sur un autre fichier ou serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="46c04-108">The ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different file or HTTP server.</span></span>

 

**<span data-ttu-id="46c04-109">Pour configurer le serveur de gestion de la virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="46c04-109">To configure the Application Virtualization Management Server</span></span>**

1.  <span data-ttu-id="46c04-110">Procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="46c04-110">Complete the following procedure:</span></span>

    [<span data-ttu-id="46c04-111">Procédure pour installer le serveur Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="46c04-111">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

    <span data-ttu-id="46c04-112">**Remarques**  Au cours de la procédure d’installation, vous spécifiez l’emplacement du répertoire \\Content sur l’écran de **chemin d’accès** .</span><span class="sxs-lookup"><span data-stu-id="46c04-112">**Note** During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

     

2.  <span data-ttu-id="46c04-113">Naviguez jusqu’à l’emplacement que vous avez spécifié pour le répertoire \\Content et, si nécessaire, créez le répertoire.</span><span class="sxs-lookup"><span data-stu-id="46c04-113">Navigate to the location that you specified for the \\Content directory, and if necessary, create the directory.</span></span>

3.  <span data-ttu-id="46c04-114">Lorsque le répertoire de contenu est créé, configurez-le en tant que partage de fichiers standard.</span><span class="sxs-lookup"><span data-stu-id="46c04-114">When the content directory is created, configure this directory as a standard file share.</span></span>

## <span data-ttu-id="46c04-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="46c04-115">Related topics</span></span>


[<span data-ttu-id="46c04-116">Scénario basé sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="46c04-116">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="46c04-117">Configuration système requise pour Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="46c04-117">Application Virtualization System Requirements</span></span>](application-virtualization-system-requirements.md)

[<span data-ttu-id="46c04-118">Scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="46c04-118">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="46c04-119">Procédure pour configurer des serveurs pour un déploiement basé sur un serveur</span><span class="sxs-lookup"><span data-stu-id="46c04-119">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

 

 





