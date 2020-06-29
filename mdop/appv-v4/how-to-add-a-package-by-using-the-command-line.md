---
title: Procédure d'ajout d'un package à l'aide de la ligne de commande
description: Procédure d'ajout d'un package à l'aide de la ligne de commande
author: dansimp
ms.assetid: e75af49e-811a-407a-a7f0-6de8562b9188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab418017a075300f308d4ef4c6eceb4f623a05c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808736"
---
# Procédure d'ajout d'un package à l'aide de la ligne de commande


Les procédures suivantes répertorient les étapes nécessaires à l’ajout d’un package d’application virtuel au client Application Virtualization (App-V) sur un ordinateur spécifique.

**Pour ajouter un package d’application virtuel pour un utilisateur spécifique**

-   Exécutez la commande suivante sous le compte d’utilisateur de la personne qui doit obtenir le package. La commande ajoute et publie le package pour cet utilisateur.

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

**Pour ajouter un package d’application virtuel pour tous les utilisateurs**

-   Exécutez la commande suivante sous un compte disposant de droits d’administrateur. Le package est ajouté et publié pour tous les utilisateurs de l’ordinateur.

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

**Pour ajouter un package à l’aide d’un système de distribution de logiciels électronique**

1.  Si vous utilisez un système de distribution de logiciels électronique qui exécute les commandes sous le compte **système** de l’ordinateur, le package est publié uniquement pour ce compte, sauf si vous utilisez le commutateur/global. Exécutez la commande suivante pour ajouter et publier le package pour tous les utilisateurs sur l’ordinateur:

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

2.  

    Si vous souhaitez ajouter le package uniquement pour des utilisateurs spécifiques, exécutez la commande **Ajouter un package** , puis publiez explicitement le package pour chaque utilisateur en exécutant la commande de publication de **package** suivante sous le compte d’utilisateur de chaque personne:

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

    `SFTMIME PUBLISH PACKAGE:”name” /MANIFEST <manifest-path>`

    La publication du package sans le paramètre GLOBAL autorise l’accès de l’utilisateur aux applications du package et publie les types de fichiers et les raccourcis répertoriés dans le manifeste dans le profil de l’utilisateur. Les autorisations requises sont «gérer les associations de types de fichiers» (**ManageTypes**) et «publier des raccourcis» (**PublishShortcut**).

## Rubriques connexes


[Procédure pour supprimer toutes les applications virtuelles à l'aide de la ligne de commande](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

[Procédure de suppression d'un package à l'aide de la ligne de commande](how-to-remove-a-package-by-using-the-command-line.md)

 

 





