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
# Procédure d'utilisation de la fonction de gestion de l'espace du cache


La fonctionnalité de gestion de l’espace du cache de systèmes de fichiers utilise un algorithme de dernier recours (LRU) et est activé par défaut. Si l’espace requis pour un nouveau package dépasse l’espace libre disponible dans le cache, le client Application Virtualization (App-V) utilise cette fonctionnalité pour déterminer, le cas échéant, les packages existants qu’il peut supprimer du cache afin de libérer de l’espace pour le nouveau package. Le client supprime le package avec la dernière date à laquelle il est consulté le plus ancien s’il est antérieur à la valeur spécifiée dans la valeur de Registre MinPkgAge. L’utilisation de la fonctionnalité de gestion de l’espace dans le cache de systèmes de fichiers peut également vous aider à éviter des problèmes de faible encombrement du cache.

Plusieurs packages sont supprimés le cas échéant. Les packages verrouillés ne sont pas supprimés.

**Remarques**  Pour vous assurer que le cache dispose de suffisamment d’espace alloué pour tous les packages qui peuvent être déployés, utilisez le paramètre **utiliser le seuil d’espace disque libre** lorsque vous configurez le client de manière à ce que le cache puisse augmenter selon les besoins. Par ailleurs, vous pouvez déterminer à l’avance la quantité d’espace disque nécessaire pour le cache de l’application V et au moment de l’installation, définir la taille de cache en conséquence.

 

La fonctionnalité de gestion de l’espace de cache est contrôlée par la valeur de Registre UnloadLeastRecentlyUsed. Une valeur de 1 active la fonctionnalité et une valeur de 0 (zéro) désactive celle-ci.

**Pour activer ou désactiver la fonctionnalité de gestion de l’espace dans le cache**

-   Définissez la valeur de Registre suivante sur 1 pour activer l’algorithme LRU. Définissez la valeur sur 0 (zéro) pour désactiver cette fonctionnalité.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed

**Pour contrôler les packages qui peuvent être supprimés**

-   Pour déterminer à quel moment le package peut être sélectionné pour ignorer, définissez la valeur de Registre suivante sur égale le nombre minimal de jours que vous souhaitez voir s’écouler après le dernier accès au package. Les packages utilisés plus récemment ne sont pas supprimés.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge

    **Attention**  La valeur maximale de cette clé de Registre est 0x00011111. Des valeurs plus grandes empêchent l’opération correcte de la fonctionnalité de gestion de l’espace de cache.

     

## Rubriques connexes


[Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





