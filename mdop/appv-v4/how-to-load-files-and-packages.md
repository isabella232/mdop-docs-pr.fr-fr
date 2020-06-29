---
title: Procédure pour charger des fichiers et des packages
description: Procédure pour charger des fichiers et des packages
author: dansimp
ms.assetid: f86f5bf1-99a4-44d7-ae2f-e6049c482f68
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9427fd8089ec9c22d7d379b15ae94bf421ca2d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807026"
---
# Procédure pour charger des fichiers et des packages


Vous pouvez utiliser la procédure suivante pour charger des fichiers et des packages sur des serveurs de virtualisation des applications.

**Remarques**  Pendant le processus d’installation, vous avez spécifié l’emplacement du répertoire \\Content sur la page de **chemin d’accès au contenu** . Ce répertoire doit être créé et configuré comme partage de fichiers standard avant de pointer sur son emplacement.

 

**Pour charger des fichiers et des packages**

1.  Sur l’ordinateur à partir duquel vous allez diffuser des applications, accédez à l’emplacement que vous avez spécifié pour le répertoire \\Content. Le cas échéant, créez le répertoire et configurez-le en tant que partage de fichiers standard.

2.  Déplacez les fichiers SFT pour les applications virtuelles et les packages vers le répertoire \\Content Pour que les fichiers SFT restent organisés et éviter toute confusion, placez les applications et les packages dans des sous-dossiers spécifiques.

3.  Chargez les applications et packages conformément aux exigences de votre scénario et de votre configuration, en prenant en compte les conditions suivantes:

    -   Si vos applications et packages sont stockés sur un serveur de gestion des applications (App-V), chargez-les via la console de gestion. Pour plus d’informations, voir [Comment charger ou décharger une application](how-to-load-or-unload-an-application.md) , ou [charger des applications virtuelles à partir de la zone de notification du Bureau](how-to-load-virtual-applications-from-the-desktop-notification-area.md).

    -   Si vos applications sont stockées sur un serveur de streaming d’application-V, un serveur Web ou un ordinateur configuré en tant que serveur de fichiers, les applications peuvent être chargées automatiquement.

        **Remarques**  Le serveur de streaming App-V interroge automatiquement le répertoire \\Content des applications et des packages et place ces informations dans la mémoire RAM pour les demandes d’applications de service.

        Les clients App-V doivent être correctement configurés pour récupérer des applications et des packages à partir de serveurs Web et de serveurs de fichiers. Pour plus d’informations, reportez-vous [à configuration du client pour la récupération de package d’application](how-to-configure-the-client-for-application-package-retrieval.md).

         

## Rubriques connexes


[Application Virtualization Server](application-virtualization-server.md)

 

 





