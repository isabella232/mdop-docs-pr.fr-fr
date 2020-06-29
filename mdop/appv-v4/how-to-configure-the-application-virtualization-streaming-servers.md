---
title: Procédure pour configurer les serveurs Application Virtualization Streaming Server
description: Procédure pour configurer les serveurs Application Virtualization Streaming Server
author: dansimp
ms.assetid: 3e2dde35-9d72-40ba-9fdf-d0338bd4d561
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0ec5497b010d18bcba60e81e96cbe6334c27fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807261"
---
# <span data-ttu-id="ee256-103">Procédure pour configurer les serveurs Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="ee256-103">How to Configure the Application Virtualization Streaming Servers</span></span>


<span data-ttu-id="ee256-104">Pour que les applications virtuelles puissent être diffusées sur le client de bureau de la virtualisation des applications ou sur le client pour les services Bureau à distance,</span><span class="sxs-lookup"><span data-stu-id="ee256-104">Before virtual applications can be streamed to the Application Virtualization Desktop Client or the Client for Remote Desktop Services (formerly Terminal Services), the Application Virtualization Streaming Servers must be configured.</span></span> <span data-ttu-id="ee256-105">Lorsque vous configurez les serveurs, vous configurez le *Répertoire de contenu* dans lequel les fichiers SFT sont chargés et stockés.</span><span class="sxs-lookup"><span data-stu-id="ee256-105">When you configure the servers, you are setting up the *content directory* where the SFT files are loaded and stored.</span></span> <span data-ttu-id="ee256-106">Les fichiers SFT contiennent les applications virtuelles (ou applications).</span><span class="sxs-lookup"><span data-stu-id="ee256-106">The SFT files contain the virtual application (or applications).</span></span>

<span data-ttu-id="ee256-107">**Important**  Les serveurs de virtualisation des applications diffusent des fichiers SFT au client de bureau et au client pour les services Bureau à distance en utilisant uniquement les protocoles RTSP ou RTSP.</span><span class="sxs-lookup"><span data-stu-id="ee256-107">**Important** Application Virtualization Servers stream SFT files to the Desktop Client and the Client for Remote Desktop Services using only RTSP or RTSPS protocols.</span></span> <span data-ttu-id="ee256-108">Il est possible de configurer le fichier ICO (icône) et l’OSD (Open Software Descriptor) sur un autre fichier ou serveur HTTP.</span><span class="sxs-lookup"><span data-stu-id="ee256-108">The ICO (icon) file and the OSD (open software descriptor) file can be configured to stream from a different file or HTTP server.</span></span>

 

**<span data-ttu-id="ee256-109">Pour configurer les serveurs de streaming de la virtualisation des applications</span><span class="sxs-lookup"><span data-stu-id="ee256-109">To configure the Application Virtualization Streaming Servers</span></span>**

1.  <span data-ttu-id="ee256-110">Terminez la procédure d’installation du serveur de diffusion de contenu de l’application.</span><span class="sxs-lookup"><span data-stu-id="ee256-110">Complete the installation procedure for the Application Virtualization Streaming Server.</span></span> <span data-ttu-id="ee256-111">Au cours de la procédure d’installation, vous spécifiez l’emplacement du répertoire \\Content sur l’écran de **chemin d’accès** .</span><span class="sxs-lookup"><span data-stu-id="ee256-111">During the installation procedure, you specify the location of the \\Content directory on the **Content Path** screen.</span></span>

2.  <span data-ttu-id="ee256-112">Naviguez jusqu’à l’emplacement que vous avez spécifié pour le répertoire \\Content et, si nécessaire, créez le répertoire.</span><span class="sxs-lookup"><span data-stu-id="ee256-112">Navigate to the location that you specified for the \\Content directory, and if you have to, create the directory.</span></span>

3.  <span data-ttu-id="ee256-113">Lorsque le répertoire de contenu est créé, configurez-le en tant que partage de fichiers standard.</span><span class="sxs-lookup"><span data-stu-id="ee256-113">When the Content directory is created, configure this directory as a standard file share.</span></span>

4.  <span data-ttu-id="ee256-114">Configurez les autorisations du système de fichiers NTFS sur le répertoire de contenu et les dossiers du package sous le répertoire de contenu.</span><span class="sxs-lookup"><span data-stu-id="ee256-114">Configure the NTFS file system permissions to the Content directory and the package folders under the Content directory.</span></span> <span data-ttu-id="ee256-115">Dans les services de domaine Active Directory, vous devez utiliser des groupes de sécurité qui définissent les utilisateurs qui peuvent accéder à chaque application.</span><span class="sxs-lookup"><span data-stu-id="ee256-115">You should use Security Groups in Active Directory Domain Services that define which users can access each application.</span></span>

## <span data-ttu-id="ee256-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ee256-116">Related topics</span></span>


[<span data-ttu-id="ee256-117">Scénario basé sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="ee256-117">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="ee256-118">Scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="ee256-118">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="ee256-119">Procédure pour configurer les serveurs Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="ee256-119">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="ee256-120">Procédure pour configurer le serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="ee256-120">How to Configure the File Server</span></span>](how-to-configure-the-file-server.md)

[<span data-ttu-id="ee256-121">Procédure pour configurer le serveur IIS</span><span class="sxs-lookup"><span data-stu-id="ee256-121">How to Configure the Server for IIS</span></span>](how-to-configure-the-server-for-iis.md)

 

 





