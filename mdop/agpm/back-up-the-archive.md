---
title: Sauvegarder l'archive
description: Sauvegarder l'archive
author: dansimp
ms.assetid: 400176da-3518-4475-ad19-c96cda6ca7ba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a75099e7a6624850ee0511cf65feddf63909a0c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807814"
---
# Sauvegarder l'archive


Pour vous aider dans la restauration de l’Archive pour la gestion avancée des stratégies de groupe (AGPM) en cas de sinistre, un administrateur AGPM (contrôle total) doit sauvegarder fréquemment l’archive. Par défaut, l’archive est créée dans%ProgramData%\\Microsoft\\AGPM. Toutefois, vous pouvez spécifier un chemin d’accès différent lors de l’installation de Microsoft Advanced Group Policy-Server.

Un compte d’utilisateur ayant accès au serveur AGPM (ordinateur sur lequel est installé le service AGPM) et au dossier qui contient l’archive est requis pour effectuer cette procédure.

**Pour sauvegarder l’archive**

1.  Arrêtez le service AGPM. Pour plus d’informations, reportez-vous à [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service-agpm30ops.md).

2.  Sauvegardez le dossier d’archivage à l’aide de l’Explorateur Windows, de xcopy, de Windows Server® de sauvegarde ou d’un autre outil de sauvegarde. Assurez-vous de sauvegarder les fichiers masqués, systèmes et en lecture seule.

3.  Stockez la sauvegarde d’archive en lieu sûr.

4.  Redémarrez le service AGPM. Pour plus d’informations, reportez-vous à [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service-agpm30ops.md).

**Remarques**  Si un administrateur AGPM sauvegarde l’archive fréquemment, les objets de stratégie de groupe de la sauvegarde d’archivage ne seront pas actualisés. Pour vous assurer que la sauvegarde d’archivage est à jour, sauvegardez l’archive dans le cadre de la stratégie de sauvegarde quotidienne de votre organisation.

 

### Références supplémentaires

-   [Restaurer l'archive à partir d'une sauvegarde](restore-the-archive-from-a-backup.md)

-   [Déplacer le serveur AGPM et l'archive](move-the-agpm-server-and-the-archive.md)

-   [Gestion de l'archivage](managing-the-archive.md)

 

 





