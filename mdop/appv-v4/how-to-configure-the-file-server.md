---
title: Procédure pour configurer le serveur de fichiers
description: Procédure pour configurer le serveur de fichiers
author: dansimp
ms.assetid: 0977554c-1741-411b-85e7-7e1cd017542f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a8971ad5c9f83dec4d0c77a16f1093ef7026b5c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807245"
---
# <span data-ttu-id="4059a-103">Procédure pour configurer le serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="4059a-103">How to Configure the File Server</span></span>


<span data-ttu-id="4059a-104">Vous pouvez suivre la procédure ci-dessous pour configurer un ordinateur local utilisé en tant que partage de fichier et flux d’applications sur le client de bureau de virtualisation des applications et sur le client pour les services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="4059a-104">You can use the following procedure to configure a local computer that is used as a file share and streams applications to the Application Virtualization Desktop Client and the Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="4059a-105">Ce scénario est utilisé lorsque vous ne souhaitez pas ajouter d’infrastructure serveur supplémentaire à votre environnement matériel existant.</span><span class="sxs-lookup"><span data-stu-id="4059a-105">This scenario is used when you do not want to add an additional server infrastructure to your existing hardware environment.</span></span>

<span data-ttu-id="4059a-106">Si vous utilisez un serveur de gestion de la virtualisation des applications comme point de distribution sur le partage de fichiers installé dans les bureaux locaux, vous devez configurer ce serveur pour que les applications virtuelles puissent être diffusées sur les ordinateurs utilisés comme partages de fichiers.</span><span class="sxs-lookup"><span data-stu-id="4059a-106">If you are using an Application Virtualization Management Server as a distribution point to the file share installed in local offices, you must configure this server before virtual applications can be streamed to the computers that are used as file shares.</span></span> <span data-ttu-id="4059a-107">Lorsque vous configurez les serveurs et les partages de fichiers, vous configurez le répertoire de contenu dans lequel les fichiers SFT sont chargés et stockés.</span><span class="sxs-lookup"><span data-stu-id="4059a-107">When you configure the servers and the file shares, you are setting up the content directory where the SFT files are loaded and stored.</span></span> <span data-ttu-id="4059a-108">Les fichiers SFT contiennent les applications virtuelles (ou applications).</span><span class="sxs-lookup"><span data-stu-id="4059a-108">The SFT files contain the virtual application (or applications).</span></span>

<span data-ttu-id="4059a-109">**Important**  Pour que les applications soient correctement diffusées sur le client de bureau de la virtualisation des applications et sur le client pour les services Bureau à distance, le flux de fichiers SFT provient du répertoire de contenu du serveur sur lequel vous stockez l’application virtuelle; le fichier ICO (Icon) et l’OSD (Open Software Descriptor) peuvent être configurés pour être diffusés en continu sur un autre serveur.</span><span class="sxs-lookup"><span data-stu-id="4059a-109">**Important** For applications to stream properly to the Application Virtualization Desktop Client and the Client for Remote Desktop Services, the SFT file streams from the content directory on the server where you store the virtual application; the ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different server.</span></span>

 

**<span data-ttu-id="4059a-110">Pour configurer le serveur de fichiers de virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="4059a-110">To configure the Application Virtualization file server</span></span>**

1.  <span data-ttu-id="4059a-111">Procédez de la manière décrite ci-dessous pour configurer le serveur utilisé comme point de distribution:</span><span class="sxs-lookup"><span data-stu-id="4059a-111">Complete the following installation procedure to configure the server that is used as the distribution point:</span></span>

    [<span data-ttu-id="4059a-112">Procédure pour installer le serveur Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="4059a-112">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

    <span data-ttu-id="4059a-113">**Remarques**  Au cours de la procédure d’installation, vous spécifiez l’emplacement du répertoire \\Content sur l’écran de **chemin d’accès** .</span><span class="sxs-lookup"><span data-stu-id="4059a-113">**Note** During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

     

2.  <span data-ttu-id="4059a-114">Créez un répertoire \\Content qui correspond à l’annuaire que vous avez spécifié lors de l’installation du serveur, sur chaque ordinateur que vous utilisez en tant que partage de fichiers.</span><span class="sxs-lookup"><span data-stu-id="4059a-114">Create a \\Content directory, which corresponds to the directory you specified when you installed the server, on each computer that you are using as a file share.</span></span>

    <span data-ttu-id="4059a-115">**Important**  Configurez les clients de bureau de la virtualisation des applications pour diffuser en continu des applications à partir de l’ordinateur que vous utilisez en tant que partage de fichiers plutôt que d’un serveur de virtualisation des applications ou d’un serveur IIS.</span><span class="sxs-lookup"><span data-stu-id="4059a-115">**Important** Configure the Application Virtualization Desktop Clients to stream applications from the computer you are using as a file share rather than from an Application Virtualization Server or IIS server.</span></span>

     

3.  <span data-ttu-id="4059a-116">Lorsque le répertoire \\Content est créé, configurez-le en tant que partage de fichiers standard.</span><span class="sxs-lookup"><span data-stu-id="4059a-116">When the \\Content directory is created, configure this directory as a standard file share.</span></span>

## <span data-ttu-id="4059a-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4059a-117">Related topics</span></span>


[<span data-ttu-id="4059a-118">Scénario basé sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="4059a-118">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="4059a-119">Scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="4059a-119">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="4059a-120">Procédure pour configurer les serveurs Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="4059a-120">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="4059a-121">Procédure pour configurer les serveurs Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="4059a-121">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)

[<span data-ttu-id="4059a-122">Procédure pour configurer le serveur IIS</span><span class="sxs-lookup"><span data-stu-id="4059a-122">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)

 

 





