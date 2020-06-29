---
title: Procédure pour supprimer toutes les applications virtuelles à l'aide de la ligne de commande
description: Procédure pour supprimer toutes les applications virtuelles à l'aide de la ligne de commande
author: dansimp
ms.assetid: bfe13b5c-825a-4eb1-a979-6c4b8d8b2a9c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55c809df31fa5c19f2f1a56c143d492b092156c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807146"
---
# Procédure pour supprimer toutes les applications virtuelles à l'aide de la ligne de commande


Vous pouvez utiliser la procédure suivante pour supprimer toutes les applications virtuelles d’un ordinateur spécifique.

**Remarques**  Lorsque toutes les applications sont supprimées d’un package, le client Application Virtualization (App-V) supprime également le package.

 

**Pour supprimer toutes les applications**

-   Exécutez la commande suivante pour supprimer toutes les applications du compte d’utilisateur sous lequel la commande est exécutée. Si vous exécutez la commande avec le commutateur/GLOBAL facultatif, en utilisant un compte disposant de droits d’administration, toutes les applications sont supprimées pour tous les utilisateurs.

    `SFTMIME DELETE OBJ:APP [/GLOBAL]`

    **Remarques**  Lorsque toutes les applications sont supprimées d’un package, le client Application Virtualization (App-V) supprime également le package.

     

## Rubriques connexes


[Procédure d'ajout d'un package à l'aide de la ligne de commande](how-to-add-a-package-by-using-the-command-line.md)

[Procédure de suppression d'un package à l'aide de la ligne de commande](how-to-remove-a-package-by-using-the-command-line.md)

 

 





