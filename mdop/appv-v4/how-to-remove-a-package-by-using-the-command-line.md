---
title: Procédure de suppression d'un package à l'aide de la ligne de commande
description: Procédure de suppression d'un package à l'aide de la ligne de commande
author: dansimp
ms.assetid: 47697ec7-20e5-4258-8865-a0a710d41d5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b282830802f34bfb0670ddfdb8e2852d3559e3f7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806861"
---
# Procédure de suppression d'un package à l'aide de la ligne de commande


Vous pouvez utiliser les procédures de ligne de commande suivantes pour supprimer un package d’application virtuel du client Application Virtualization (App-V) sur un ordinateur spécifique.

**Pour supprimer un package d’application virtuel pour tous les utilisateurs**

-   Si le package a été précédemment ajouté pour tous les utilisateurs à l’aide du commutateur/GLOBAL, utilisez la commande suivante pour supprimer le package ainsi que les types de fichiers et raccourcis globaux. Vous devez disposer des droits d’administrateur. Le commutateur/GLOBAL n’est pas nécessaire dans ce cas, car la commande effectue toujours une suppression globale du package.

    `SFTMIME DELETE PACKAGE:”name”`

**Pour supprimer un package déjà ajouté pour des utilisateurs individuels**

1.  Si le package a déjà été ajouté pour des utilisateurs individuels, plusieurs options s’offrent à vous.

    Exécutez la commande suivante une fois sous le compte d’utilisateur de chaque personne à laquelle le package a été publié. Ainsi, l’utilisateur n’a pas accès aux applications s’il effectue une itinérance sur un autre ordinateur. Il supprime les paramètres de l’utilisateur, les raccourcis et les types de fichiers spécifiques du profil, et arrête les chargements en arrière-plan dans le contexte de l’utilisateur.

    `SFTMIME UNPUBLISH PACKAGE:”name”`

2.  Vous pouvez également exécuter la commande suivante sous le compte d’utilisateur de chaque personne à laquelle le package a été publié.

    `SFTMIME UNPUBLISH PACKAGE:”name”`

    Ensuite, exécutez cette commande pour le package.

    `SFTMIME DELETE PACKAGE:”name”`

    Le package est alors entièrement supprimé et les paramètres de l’utilisateur, les raccourcis et les types de fichiers sont supprimés de leur profil. Si le package est ensuite rajouté, les utilisateurs devront spécifier de nouveau leurs paramètres. Seule l’autorisation «Delete applications» (**DeleteApp**) est nécessaire pour exécuter cette commande.

3.  À la place, vous pouvez simplement exécuter la commande **supprimer le package** sans utiliser la commande annuler la **publication du package** . Dans ce cas, les types de fichiers et les raccourcis pour chaque utilisateur sont masqués plutôt que supprimés, et les paramètres de l’utilisateur sont conservés. Cela signifie que si le package est ensuite rajouté pour l’utilisateur, les types de fichiers et les raccourcis sont restaurés et les paramètres de l’utilisateur sont réappliqués.

## Rubriques connexes


[Procédure d'ajout d'un package à l'aide de la ligne de commande](how-to-add-a-package-by-using-the-command-line.md)

[Procédure pour supprimer toutes les applications virtuelles à l'aide de la ligne de commande](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

 

 





