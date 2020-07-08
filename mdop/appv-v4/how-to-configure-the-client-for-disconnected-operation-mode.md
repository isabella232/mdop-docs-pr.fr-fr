---
title: Procédure pour configurer le client en mode de fonctionnement hors connexion
description: Procédure pour configurer le client en mode de fonctionnement hors connexion
author: dansimp
ms.assetid: 3b48464a-b8b4-494b-93e3-9a6d9bd74652
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1c917d87996a26b330551deb04b1828c31fd3c73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807258"
---
# Procédure pour configurer le client en mode de fonctionnement hors connexion


Le mode de fonctionnement déconnecté permet au client de bureau App-V (App-V) ou au client de virtualisation des applications (App-V) d’exécuter des applications qui sont stockées dans le cache du système de fichiers du client lorsque le client ne peut pas se connecter au serveur de gestion App-V.

**Important**  Dans une grande organisation où de multiples serveurs de session Bureau à distance (hôtes de session de bureau à distance) sont liés dans une batterie de serveurs pour prendre en charge de nombreux utilisateurs, le recours à un serveur d’administration d’application unique pour la prise en charge de la batterie représente un point de défaillance unique. Pour garantir une haute disponibilité à la prise en charge de la batterie d’hébergement RDSession, envisagez de lier deux ou plusieurs serveurs d’administration d’applications-V pour utiliser la même base de données.

 

**Pour activer le mode de fonctionnement déconnecté**

-   Définissez la valeur de clé de Registre suivante sur 1 pour activer le mode de fonctionnement hors connexion:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation

**Pour définir un délai d’utilisation du mode de fonctionnement déconnecté**

1.  Attribuez la valeur 1 à la clé de Registre suivante:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation

2.  Définissez la valeur de clé de Registre suivante sur le nombre de minutes pendant lequel vous voulez limiter le mode de fonctionnement déconnecté. La plage de valeurs valide est 1 – 999999. La valeur par défaut est 90 jours ou 129 600 minutes.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes

**Pour configurer le client pour les services Bureau à distance pour le mode de fonctionnement déconnecté**

1.  Définissez la valeur de clé de Registre suivante sur 1 pour activer le mode de fonctionnement hors connexion:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation

2.  Définissez la valeur de clé de Registre suivante sur 0 (zéro) pour autoriser l’utilisation illimitée du mode de fonctionnement hors connexion:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation

3.  Assurez-vous que tous les packages sont préchargés dans le cache pour améliorer les performances.

## Rubriques connexes


[Mode de fonctionnement déconnecté](disconnected-operation-mode.md)

[Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





