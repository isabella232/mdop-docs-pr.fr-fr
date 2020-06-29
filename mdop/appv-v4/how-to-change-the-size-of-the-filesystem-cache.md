---
title: Procédure pour modifier la taille du cache de FileSystem
description: Procédure pour modifier la taille du cache de FileSystem
author: dansimp
ms.assetid: 6ed17ba3-293b-4482-b3fa-31e5f606dad6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63c98d53ccb31e8eb64bc70d3d79b2198c506e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807333"
---
# Procédure pour modifier la taille du cache de FileSystem


Vous pouvez modifier la taille du cache de systèmes de fichiers à l’aide de la ligne de commande. Cette action nécessite une réinitialisation complète du cache et nécessite des droits d’administration.

**Pour modifier la taille du cache de systèmes de fichiers**

1.  Définissez la valeur de Registre suivante sur 0 (zéro):

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State

2.  Définissez la valeur de Registre suivante à la taille maximale du cache, en Mo, nécessaire pour contenir les packages, par exemple 8192 Mo:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize

3.  Redémarrez l’ordinateur.

## Rubriques connexes


[Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





