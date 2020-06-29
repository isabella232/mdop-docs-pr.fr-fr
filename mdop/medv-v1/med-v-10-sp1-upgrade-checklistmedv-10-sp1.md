---
title: Liste de contrôle pour la mise à niveau de MED-V1.0 SP1
description: Liste de contrôle pour la mise à niveau de MED-V1.0 SP1
author: dansimp
ms.assetid: 1a462b37-8c7a-4826-9175-0b1b701d345b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9c418eff8dfb6146204d7d9212d42e49db000fb1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812252"
---
# <span data-ttu-id="30b36-103">Liste de contrôle pour la mise à niveau de MED-V1.0 SP1</span><span class="sxs-lookup"><span data-stu-id="30b36-103">MED-V 1.0 SP1 Upgrade Checklist</span></span>


<span data-ttu-id="30b36-104">Pour procéder à la mise à niveau de Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 vers MED-V 1.0 Service Pack1 (SP1), le client doit être mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="30b36-104">To upgrade Microsoft Enterprise Desktop Virtualization (MED-V)1.0 to MED-V1.0 Service Pack1 (SP1), the client must be upgraded.</span></span> <span data-ttu-id="30b36-105">Le serveur peut éventuellement être mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="30b36-105">The server can optionally be upgraded.</span></span>

## <span data-ttu-id="30b36-106">Mise à niveau du serveur</span><span class="sxs-lookup"><span data-stu-id="30b36-106">Server Upgrade</span></span>


**<span data-ttu-id="30b36-107">Pour mettre à niveau le serveur MED-V 1.0 vers MED-V 1.0 SP1</span><span class="sxs-lookup"><span data-stu-id="30b36-107">To upgrade the MED-V1.0 server to MED-V1.0 SP1</span></span>**

1.  <span data-ttu-id="30b36-108">Sauvegardez les fichiers suivants situés dans le répertoire \* &lt; INSTALLDIR &gt; /Servers/ConfigurationServer\* :</span><span class="sxs-lookup"><span data-stu-id="30b36-108">Back up the following files that are located in the *&lt;InstallDir&gt; / Servers / ConfigurationServer* directory:</span></span>

    -   <span data-ttu-id="30b36-109">OrganizationalPolicy.XML</span><span class="sxs-lookup"><span data-stu-id="30b36-109">OrganizationalPolicy.XML</span></span>

    -   <span data-ttu-id="30b36-110">ClientPolicy.XML</span><span class="sxs-lookup"><span data-stu-id="30b36-110">ClientPolicy.XML</span></span>

    -   <span data-ttu-id="30b36-111">WorkspaceKeys.XML</span><span class="sxs-lookup"><span data-stu-id="30b36-111">WorkspaceKeys.XML</span></span>

2.  <span data-ttu-id="30b36-112">Sauvegardez le fichier \* &lt; INSTALLDIR &gt; /serveurs/ServerSettings.xml\* .</span><span class="sxs-lookup"><span data-stu-id="30b36-112">Back up the *&lt;InstallDir&gt; / Servers / ServerSettings.xml* file.</span></span>

3.  <span data-ttu-id="30b36-113">Désinstaller le serveur MED-V 1.0.</span><span class="sxs-lookup"><span data-stu-id="30b36-113">Uninstall the MED-V1.0 server.</span></span>

4.  <span data-ttu-id="30b36-114">Installez le serveur de MED-V 1.0 SP1.</span><span class="sxs-lookup"><span data-stu-id="30b36-114">Install the MED-V1.0 SP1 server.</span></span>

5.  <span data-ttu-id="30b36-115">Restaurez les fichiers de sauvegarde dans les répertoires appropriés.</span><span class="sxs-lookup"><span data-stu-id="30b36-115">Restore the backup files to the appropriate directories.</span></span>

6.  <span data-ttu-id="30b36-116">Redémarrez le service du serveur MED-V.</span><span class="sxs-lookup"><span data-stu-id="30b36-116">Restart the MED-V server service.</span></span>

<span data-ttu-id="30b36-117">**Remarques**  Si la configuration de serveur a changé par défaut, les fichiers peuvent être stockés à un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="30b36-117">**Note** If the server configuration has been changed from the default, the files might be stored in a different location.</span></span>

 

## <span data-ttu-id="30b36-118">Mise à niveau du client</span><span class="sxs-lookup"><span data-stu-id="30b36-118">Client Upgrade</span></span>


<span data-ttu-id="30b36-119">Pour mettre à niveau le client MED-V 1.0 vers MED-V 1.0 SP1, installez le fichier. msp sur un client MED-V 1.0.</span><span class="sxs-lookup"><span data-stu-id="30b36-119">To upgrade the MED-V1.0 client to MED-V1.0 SP1, install the .msp file on a MED-V1.0 client.</span></span> <span data-ttu-id="30b36-120">Le client et MED-V sont automatiquement mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="30b36-120">The client and MED-V are automatically upgraded.</span></span>

 

 





