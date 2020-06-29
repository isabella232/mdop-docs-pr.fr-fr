---
title: Procédure pour réinitialiser le cache de FileSystem
description: Procédure pour réinitialiser le cache de FileSystem
author: dansimp
ms.assetid: 7777259d-8c21-4c06-9384-9599b69f9828
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 680634d98f8aac048af605c62029a0ee6b20af03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806817"
---
# Procédure pour réinitialiser le cache de FileSystem


La réinitialisation du cache de systèmes de fichiers n’est pas un facteur qui devrait généralement être nécessaire. Néanmoins, si vous avez besoin de réinitialiser entièrement le cache de systèmes de fichiers, peut-être à des fins de dépannage, vous pouvez utiliser la procédure suivante. Des droits d’administration sont requis pour effectuer cette action.

**Pour réinitialiser le cache de systèmes de fichiers**

1.  Définissez la valeur de Registre suivante sur 0 (zéro):

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State

2.  Redémarrez l’ordinateur.

## Rubriques connexes


[Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





