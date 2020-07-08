---
title: Procédure pour modifier la taille de mémoire cache du serveur
description: Procédure pour modifier la taille de mémoire cache du serveur
author: dansimp
ms.assetid: 24e63744-21c3-458e-b137-9592f4fe785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92e56a8a28f7a00d71805b497f9e404cca65919d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807342"
---
# Procédure pour modifier la taille de mémoire cache du serveur


Vous pouvez utiliser la procédure suivante pour modifier la taille de cache pour n’importe quel serveur directement à partir de la console de gestion du serveur d’applications.

**Remarques**  Même si vous pouvez modifier la taille du cache, à moins que votre configuration n’exige d’en modifier la taille, il est recommandé de conserver les valeurs par défaut définies sur taille du cache.

 

**Pour modifier la taille du cache du serveur**

1.  Cliquez sur le nœud **groupes de serveurs** dans le volet gauche pour développer la liste des groupes de serveurs.

2.  Dans le volet **résultats** , double-cliquez sur le groupe de serveurs souhaité pour afficher la liste des serveurs du groupe.

3.  Dans le volet **résultats** , cliquez avec le bouton droit sur le serveur de votre choix, puis sélectionnez **Propriétés**.

4.  Sélectionnez l’onglet **avancé** .

5.  Entrez une valeur dans le champ **allocation de mémoire maximale** pour le cache du serveur, puis entrez une valeur pour le niveau d’avertissement de seuil dans le champ d’avertissement d' **allocation de mémoire** .

6.  Entrez une valeur dans le champ **taille de bloc maximale** . Ce nombre doit être supérieur ou égal à la taille de blocs maximale du paquetage le plus grand qui sera transmis à partir du serveur.

7.  Cliquez sur **OK**.

## Rubriques connexes


[Procédure pour modifier le port du serveur](how-to-change-the-server-port.md)

[Procédure pour gérer les serveurs dans Server Management Console](how-to-manage-servers-in-the-server-management-console.md)

 

 





