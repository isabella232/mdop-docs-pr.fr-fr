---
title: Migration des packages de paramètres UE-V
description: Migration des packages de paramètres UE-V
author: dansimp
ms.assetid: 93d99254-3e17-4e96-92ad-87059d8554a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0087f334e916c06e7611d2671d0b50e7d1dd916
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809816"
---
# <span data-ttu-id="8e9eb-103">Migration des packages de paramètres UE-V</span><span class="sxs-lookup"><span data-stu-id="8e9eb-103">Migrating UE-V Settings Packages</span></span>


<span data-ttu-id="8e9eb-104">Dans le cycle de vie d’un déploiement de la virtualisation de l’interface utilisateur de Microsoft (UE-V), vous devrez peut-être déplacer les packages de paramètres utilisateur lors de la migration vers un nouveau serveur ou à des fins de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-104">In the lifecycle of a Microsoft User Experience Virtualization (UE-V) deployment, you might need to relocate the user settings packages either when migrating to a new server or for backup purposes.</span></span> <span data-ttu-id="8e9eb-105">La migration des packages de paramètres peut être nécessaire dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="8e9eb-105">Migration of settings packages might be needed in the following scenarios:</span></span>

-   <span data-ttu-id="8e9eb-106">Effectuez la mise à niveau du matériel du serveur existant vers un serveur plus moderne.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-106">Upgrade of existing server hardware to a more modern server.</span></span>

-   <span data-ttu-id="8e9eb-107">Migration d’un emplacement de stockage des paramètres d’un laboratoire vers un serveur de production.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-107">Migration of a settings storage location share from a lab to a production server.</span></span>

<span data-ttu-id="8e9eb-108">Le simple fait de copier les fichiers et dossiers ne conserve pas les paramètres de sécurité et les autorisations.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-108">Simply copying the files and folders will not preserve the security settings and permissions.</span></span> <span data-ttu-id="8e9eb-109">Les étapes décrites ci-dessous permettent de copier correctement les fichiers du package de paramètres avec leurs autorisations NTFS vers un nouveau partage.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-109">The following described steps will properly copy the settings package files with their NTFS permissions to a new share.</span></span>

**<span data-ttu-id="8e9eb-110">Conservation des packages de paramètres d’UE-V lors de la migration vers un nouveau serveur</span><span class="sxs-lookup"><span data-stu-id="8e9eb-110">How to preserve UE-V settings packages when migrating to a new server</span></span>**

1.  <span data-ttu-id="8e9eb-111">Dans un nouvel emplacement sur un autre serveur, créez un nouveau dossier. par exemple, MySettings.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-111">In a new location on a different server, create a new folder; for example, MySettings.</span></span>

2.  <span data-ttu-id="8e9eb-112">Désactivez le partage pour l’ancien dossier partage sur l’ancien serveur.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-112">Disable sharing for the old folder share on the old server.</span></span>

3.  <span data-ttu-id="8e9eb-113">Déplacez les packages de paramètres existants vers le nouveau serveur avec Robocopy à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-113">Move the existing settings packages to the new server with Robocopy from the command line.</span></span> <span data-ttu-id="8e9eb-114">Exemple:</span><span class="sxs-lookup"><span data-stu-id="8e9eb-114">For example:</span></span>

    ``` syntax
    c:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    <span data-ttu-id="8e9eb-115">**Remarques**  Pour surveiller la progression de la copie, ouvrez MySettings.txt avec un lecteur de fichier journal tel que trace32.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-115">**Note** To monitor the copy progress, open MySettings.txt with a log file reader such as Trace32.</span></span>

     

4.  <span data-ttu-id="8e9eb-116">Accordez des autorisations de niveau partage au nouveau partage.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-116">Grant share-level permissions to the new share.</span></span> <span data-ttu-id="8e9eb-117">Laissez les autorisations NTFS telles qu’elles ont été définies par Robocopy.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-117">Leave the NTFS permissions as they were set by Robocopy.</span></span>

    <span data-ttu-id="8e9eb-118">Sur les ordinateurs qui exécutent l’agent UE-V, mettez à jour le paramètre de configuration SettingsStoragePath sur le chemin UNC du nouveau partage.</span><span class="sxs-lookup"><span data-stu-id="8e9eb-118">On computers that run the UE-V agent, update the SettingsStoragePath configuration setting to the UNC path of the new share.</span></span>

## <span data-ttu-id="8e9eb-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e9eb-119">Related topics</span></span>


[<span data-ttu-id="8e9eb-120">Administration d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="8e9eb-120">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="8e9eb-121">Opérations d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="8e9eb-121">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





