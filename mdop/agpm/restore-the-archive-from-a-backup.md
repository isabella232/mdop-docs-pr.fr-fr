---
title: Restaurer l'archive à partir d'une sauvegarde
description: Restaurer l'archive à partir d'une sauvegarde
author: dansimp
ms.assetid: 49666337-d72c-4e44-99e4-9eb59b2355a9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b00d2e5e612e2ac43f965e4adf6175e2fd159007
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807477"
---
# Restaurer l'archive à partir d'une sauvegarde


En cas de sinistre et si l’archive de la gestion de la stratégie de groupe avancée (AGPM) est endommagée ou détruite, un administrateur AGPM (contrôle total) peut restaurer l’archive à partir d’une copie de sauvegarde préparée à l’avance, puis importer à partir de l’environnement de production les objets de stratégie de groupe qui ne figurent pas dans l’archive ou dont la version en production est plus Pour plus d’informations sur la restauration d’une sauvegarde d’archive sur un serveur différent, voir [déplacer le serveur AGPM et l’archive](move-the-agpm-server-and-the-archive.md).

Un compte d’utilisateur ayant accès au serveur AGPM (l’ordinateur sur lequel est installé le service AGPM) et au dossier qui contient l’archive est requis pour effectuer cette procédure.

**Pour restaurer l’archive à partir d’une sauvegarde**

1.  Arrêtez le service AGPM. Pour plus d’informations, reportez-vous à [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service-agpm30ops.md).

2.  Supprimez l’archive existante. Par défaut, le dossier d’archivage est%ProgramData%\\Microsoft\\AGPM, mais l’Administrateur AGPM qui a installé Microsoft Advanced Group Policy Management-Server a peut-être entré un autre emplacement lors de l’installation.

3.  Recréez le dossier archive en configurant le chemin d’archive, le compte de service AGPM, le propriétaire de l’archivage et le port d’écoute. Il n’est pas nécessaire d’utiliser les mêmes valeurs que celles utilisées lors de l’installation d’origine. Pour plus d’informations, voir [modifier le service AGPM](modify-the-agpm-service-agpm30ops.md).

4.  Copiez le contenu de la sauvegarde d’archive dans le dossier d’archivage, en copiant les sous-dossiers et les fichiers pour vous assurer que chaque sous-dossier et fichier héritent des autorisations du dossier d’archivage. Veillez à ne pas écraser le dossier d’archivage.

5.  Si vous ne savez pas si un objet GPO dans la sauvegarde d’archive est plus à jour que la copie de cet objet GPO en production, générez un rapport de différences et comparez les paramètres. Pour plus d’informations, voir [identifier les différences entre les objets de stratégie de groupe, les versions](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md)d’objets de stratégie de groupe et les modèles.

6.  Redémarrez le service AGPM. Pour plus d’informations, reportez-vous à [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service-agpm30ops.md).

### Références supplémentaires

-   [Sauvegarder l'archive](back-up-the-archive.md)

-   [Déplacer le serveur AGPM et l'archive](move-the-agpm-server-and-the-archive.md)

-   [Gestion de l'archivage](managing-the-archive.md)

 

 





