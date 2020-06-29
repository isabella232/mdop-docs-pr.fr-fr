---
title: Procédure pour configurer le serveur IIS
description: Procédure pour configurer le serveur IIS
author: dansimp
ms.assetid: 1fcfc583-322f-4a38-90d0-e64bfa9ee3d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9fe3367698b6f387d4467afdad1b3e17211134d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807229"
---
# <span data-ttu-id="092f5-103">Procédure pour configurer le serveur IIS</span><span class="sxs-lookup"><span data-stu-id="092f5-103">How to Configure the Server for IIS</span></span>


<span data-ttu-id="092f5-104">Pour que les applications virtuelles puissent être diffusées sur le client de bureau de la virtualisation des applications et sur le client pour les services Bureau à distance (auparavant services Terminal Server), les serveurs IIS doivent être configurés.</span><span class="sxs-lookup"><span data-stu-id="092f5-104">Before virtual applications can be streamed to the Application Virtualization Desktop Client and the Client for Remote Desktop Services (formerly Terminal Services), the IIS servers must be configured.</span></span> <span data-ttu-id="092f5-105">Lorsque vous configurez les serveurs, vous configurez le répertoire de contenu dans lequel les fichiers SFT sont chargés et stockés.</span><span class="sxs-lookup"><span data-stu-id="092f5-105">When you configure the servers, you are setting up the content directory where the SFT files are loaded and stored.</span></span> <span data-ttu-id="092f5-106">Les fichiers SFT contiennent les applications virtuelles (ou applications).</span><span class="sxs-lookup"><span data-stu-id="092f5-106">The SFT files contain the virtual application (or applications).</span></span>

**<span data-ttu-id="092f5-107">Pour configurer le répertoire de contenu sur le serveur IIS</span><span class="sxs-lookup"><span data-stu-id="092f5-107">To configure the content directory on the IIS server</span></span>**

1.  <span data-ttu-id="092f5-108">Sur le serveur exécutant IIS, recherchez le répertoire que vous souhaitez utiliser comme répertoire de contenu ou créez le répertoire s’il n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="092f5-108">On the server that is running IIS, locate the directory that you want to use as the content directory, or create the directory if it does not exist.</span></span> <span data-ttu-id="092f5-109">Configurer ce répertoire comme partage de fichiers standard.</span><span class="sxs-lookup"><span data-stu-id="092f5-109">Configure this directory as a standard file share.</span></span>

2.  <span data-ttu-id="092f5-110">Sur le serveur exécutant IIS, ouvrez le **Gestionnaire des services Internet (IIS)**, puis, sous le site Web par défaut, créez un répertoire virtuel correspondant au répertoire de contenu que vous avez créé sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="092f5-110">On the server that is running IIS, open **IIS Manager**, and under the default website, create a virtual directory that corresponds to the content directory that you created on the server.</span></span> <span data-ttu-id="092f5-111">Assurez-vous que la case à cocher **lecture** est activée.</span><span class="sxs-lookup"><span data-stu-id="092f5-111">Make sure that **Read** is checked.</span></span>

3.  <span data-ttu-id="092f5-112">Donnez au répertoire virtuel nouvellement créé le **contenu**de l’alias.</span><span class="sxs-lookup"><span data-stu-id="092f5-112">Give the newly created virtual directory the alias **Content**.</span></span>

4.  <span data-ttu-id="092f5-113">Acceptez tous les autres paramètres par défaut pour ce répertoire virtuel.</span><span class="sxs-lookup"><span data-stu-id="092f5-113">Accept all other default settings for this virtual directory.</span></span>

5.  <span data-ttu-id="092f5-114">Configurez les autorisations du système de fichiers NTFS sur le répertoire de contenu et les dossiers du package sous le répertoire de contenu à l’aide des groupes de sécurité dans les services de domaine Active Directory définis précédemment.</span><span class="sxs-lookup"><span data-stu-id="092f5-114">Configure the NTFS file system permissions to the content directory and the package folders under the content directory by using the Security Groups in Active Directory Domain Services that you defined earlier.</span></span>

<span data-ttu-id="092f5-115">**Remarques**  Si vous utilisez IIS pour publier les fichiers ICO et OSD, vous devez configurer un type MIME pour OSD = TXT; dans le cas contraire, il n’utilisera pas les fichiers ICO et OSD pour les clients.</span><span class="sxs-lookup"><span data-stu-id="092f5-115">**Note** If you are using IIS to publish the ICO and OSD files, you must configure a MIME type for OSD=TXT; otherwise, IIS will not serve the ICO and OSD files to clients.</span></span> <span data-ttu-id="092f5-116">Si vous utilisez les services Internet pour publier des packages (fichiers SFT), vous devez configurer un type MIME pour SFT = Binary; dans le cas contraire, IIS ne servira pas les fichiers SFT aux clients.</span><span class="sxs-lookup"><span data-stu-id="092f5-116">If you are using IIS to publish packages (SFT files), you must configure a MIME type for SFT=Binary; otherwise, IIS will not serve the SFT files to clients.</span></span>

 

## <span data-ttu-id="092f5-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="092f5-117">Related topics</span></span>


[<span data-ttu-id="092f5-118">Scénario basé sur un serveur Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="092f5-118">Application Virtualization Server-Based Scenario</span></span>](application-virtualization-server-based-scenario.md)

[<span data-ttu-id="092f5-119">Scénario basé sur une distribution électronique de logiciels</span><span class="sxs-lookup"><span data-stu-id="092f5-119">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="092f5-120">Procédure pour configurer les serveurs Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="092f5-120">How to Configure the Application Virtualization Management Servers</span></span>](how-to-configure-the-application-virtualization-management-servers.md)

[<span data-ttu-id="092f5-121">Procédure pour configurer les serveurs Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="092f5-121">How to Configure the Application Virtualization Streaming Servers</span></span>](how-to-configure-the-application-virtualization-streaming-servers.md)

[<span data-ttu-id="092f5-122">Procédure pour configurer le serveur de fichiers</span><span class="sxs-lookup"><span data-stu-id="092f5-122">How to Configure the File Server</span></span>](how-to-configure-the-file-server.md)

 

 





