---
title: Procédure d'utilisation de la fonction de gestion de l'espace du cache
description: Procédure d'utilisation de la fonction de gestion de l'espace du cache
author: dansimp
ms.assetid: 60965660-c015-46a8-88ac-54cbc050fe33
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fcb9cc4bc076e1acf52fb1c03797384c45b82f7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806694"
---
# <span data-ttu-id="f2fa9-103">Procédure d'utilisation de la fonction de gestion de l'espace du cache</span><span class="sxs-lookup"><span data-stu-id="f2fa9-103">How to Use the Cache Space Management Feature</span></span>


<span data-ttu-id="f2fa9-104">La fonctionnalité de gestion de l’espace du cache de systèmes de fichiers utilise un algorithme de dernier recours (LRU) et est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-104">The FileSystem cache space management feature uses a Least Recently Used (LRU) algorithm and is enabled by default.</span></span> <span data-ttu-id="f2fa9-105">Si l’espace requis pour un nouveau package dépasse l’espace libre disponible dans le cache, le client Application Virtualization (App-V) utilise cette fonctionnalité pour déterminer, le cas échéant, les packages existants qu’il peut supprimer du cache afin de libérer de l’espace pour le nouveau package.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-105">If the space that is required for a new package would exceed the available free space in the cache, the Application Virtualization (App-V) Client uses this feature to determine which, if any, existing packages it can delete from the cache to make room for the new package.</span></span> <span data-ttu-id="f2fa9-106">Le client supprime le package avec la dernière date à laquelle il est consulté le plus ancien s’il est antérieur à la valeur spécifiée dans la valeur de Registre MinPkgAge.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-106">The client deletes the package with the oldest last-accessed date if it is older than the value specified in the MinPkgAge registry value.</span></span> <span data-ttu-id="f2fa9-107">L’utilisation de la fonctionnalité de gestion de l’espace dans le cache de systèmes de fichiers peut également vous aider à éviter des problèmes de faible encombrement du cache.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-107">Use of the FileSystem cache space management feature can also help to avoid low cache space problems.</span></span>

<span data-ttu-id="f2fa9-108">Plusieurs packages sont supprimés le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-108">More than one package is deleted if necessary.</span></span> <span data-ttu-id="f2fa9-109">Les packages verrouillés ne sont pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-109">Packages that are locked are not deleted.</span></span>

<span data-ttu-id="f2fa9-110">**Remarques**  Pour vous assurer que le cache dispose de suffisamment d’espace alloué pour tous les packages qui peuvent être déployés, utilisez le paramètre **utiliser le seuil d’espace disque libre** lorsque vous configurez le client de manière à ce que le cache puisse augmenter selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-110">**Note** To ensure that the cache has sufficient space allocated for all packages that might be deployed, use the **Use free disk space threshold** setting when you configure the client so that the cache can grow as needed.</span></span> <span data-ttu-id="f2fa9-111">Par ailleurs, vous pouvez déterminer à l’avance la quantité d’espace disque nécessaire pour le cache de l’application V et au moment de l’installation, définir la taille de cache en conséquence.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-111">Alternatively, determine in advance how much disk space will be needed for the App-V cache, and at installation time, set the cache size accordingly.</span></span>

 

<span data-ttu-id="f2fa9-112">La fonctionnalité de gestion de l’espace de cache est contrôlée par la valeur de Registre UnloadLeastRecentlyUsed.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-112">The cache space management feature is controlled by the UnloadLeastRecentlyUsed registry value.</span></span> <span data-ttu-id="f2fa9-113">Une valeur de 1 active la fonctionnalité et une valeur de 0 (zéro) désactive celle-ci.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-113">A value of 1 enables the feature, and a value of 0 (zero) disables it.</span></span>

**<span data-ttu-id="f2fa9-114">Pour activer ou désactiver la fonctionnalité de gestion de l’espace dans le cache</span><span class="sxs-lookup"><span data-stu-id="f2fa9-114">To enable or disable the cache space management feature</span></span>**

-   <span data-ttu-id="f2fa9-115">Définissez la valeur de Registre suivante sur 1 pour activer l’algorithme LRU.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-115">Set the following registry value to 1 to enable the LRU algorithm.</span></span> <span data-ttu-id="f2fa9-116">Définissez la valeur sur 0 (zéro) pour désactiver cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-116">Set it to 0 (zero) to disable the feature.</span></span>

    <span data-ttu-id="f2fa9-117">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed</span><span class="sxs-lookup"><span data-stu-id="f2fa9-117">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed</span></span>

**<span data-ttu-id="f2fa9-118">Pour contrôler les packages qui peuvent être supprimés</span><span class="sxs-lookup"><span data-stu-id="f2fa9-118">To control which packages can be discarded</span></span>**

-   <span data-ttu-id="f2fa9-119">Pour déterminer à quel moment le package peut être sélectionné pour ignorer, définissez la valeur de Registre suivante sur égale le nombre minimal de jours que vous souhaitez voir s’écouler après le dernier accès au package.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-119">To determine when the package can be selected for discard, set the following registry value to equal the minimum number of days you want to elapse since the package was last accessed.</span></span> <span data-ttu-id="f2fa9-120">Les packages utilisés plus récemment ne sont pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-120">Packages that have been used more recently are not discarded.</span></span>

    <span data-ttu-id="f2fa9-121">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge</span><span class="sxs-lookup"><span data-stu-id="f2fa9-121">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge</span></span>

    <span data-ttu-id="f2fa9-122">**Attention**  La valeur maximale de cette clé de Registre est 0x00011111.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-122">**Caution** The maximum value for this registry key is 0x00011111.</span></span> <span data-ttu-id="f2fa9-123">Des valeurs plus grandes empêchent l’opération correcte de la fonctionnalité de gestion de l’espace de cache.</span><span class="sxs-lookup"><span data-stu-id="f2fa9-123">Larger values will prevent the correct operation of the cache space management feature.</span></span>

     

## <span data-ttu-id="f2fa9-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f2fa9-124">Related topics</span></span>


[<span data-ttu-id="f2fa9-125">Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="f2fa9-125">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





