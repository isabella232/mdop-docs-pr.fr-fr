---
title: Mode de fonctionnement déconnecté
description: Mode de fonctionnement déconnecté
author: dansimp
ms.assetid: 3f9849ea-ba53-4c68-85d3-87a4218f59c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6e9534b93f23b17e5258ef5e2d548eb93213f2f8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808867"
---
# Mode de fonctionnement déconnecté


Les paramètres du mode de l’opération déconnectée, accessibles en cliquant avec le bouton droit sur le nœud de virtualisation de l' **application** , en sélectionnant **Propriétés**, puis en cliquant sur l’onglet **connectivité** , permettent au client de bureau virtuel d’applications ou au client pour les services Bureau à distance (anciennement services Terminal Server) d’exécuter des applications qui sont stockées dans le cache du système de fichiers

Les raisons pour lesquelles il est impossible de se connecter au serveur sont les suivantes: échec du serveur, interruption du réseau ou déconnexion du réseau. En cas d’échec, le client bascule automatiquement vers l’opération déconnectée. Après sa déconnexion, si le client a besoin de données supplémentaires du serveur pour continuer à exécuter une application ou si le délai d’expiration de l’opération déconnectée expire, le client tente de se reconnecter au serveur. Si cette tentative de connexion échoue, l’application est arrêtée.

Par défaut, l’opération hors connexion est activée et le délai d’expiration est de 90 jours. La valeur du délai d’expiration est spécifiée en tant que nombre de jours pendant lequel vous voulez limiter le mode de fonctionnement déconnecté et vous pouvez entrer une valeur comprise entre 1 et 999.

## Rubriques connexes


[Procédure pour désactiver ou modifier des paramètres de mode de fonctionnement déconnecté](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





