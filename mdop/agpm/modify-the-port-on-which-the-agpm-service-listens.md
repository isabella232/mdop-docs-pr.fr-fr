---
title: Modifier le port sur lequel le service AGPM écoute
description: Modifier le port sur lequel le service AGPM écoute
author: dansimp
ms.assetid: a82c6873-e916-4a04-b263-aa612cd6956b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2af79ecb9bd05acbc55083163903ae14ab44d06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808326"
---
# Modifier le port sur lequel le service AGPM écoute


Le service AGPM est un service Windows agissant en tant que proxy de sécurité, gérant l’accès client aux objets de stratégie de groupe (GPO) dans l’environnement d’archivage et de production. Par défaut, le service AGPM écoute sur le port 4600. Vous pouvez modifier ce port en modifiant le fichier d’index d’archive Advanced Group Policy Management (AGPM) pour chaque archive.

**Remarques**  Avant de modifier le port que le service AGPM écoute, il est recommandé de sauvegarder le fichier d’index d’archive AGPM (gpostate.xml). Ce fichier se trouve dans le dossier entré comme chemin d’accès d’archive au cours de l’installation de gestion de la stratégie de groupe avancée-serveur. Par défaut, cet emplacement de ce fichier est% CommonAppData% \\Microsoft\\AGPM\\gpostate.xml sur le serveur AGPM. Si vous ne savez pas quel ordinateur héberge l’archive, vous pouvez suivre la procédure de modification du chemin d’accès de l’Archive pour afficher le chemin d’accès actuel. Pour plus d’informations, voir [modifier le chemin d’accès d’archive](modify-the-archive-path.md).

 

Un compte d’utilisateur ayant accès au serveur AGPM (l’ordinateur sur lequel est installé le service AGPM) et au fichier d’index d’archive est requis pour effectuer cette procédure.

**Pour modifier le port que le service AGPM écoute**

1.  Sur l’ordinateur hébergeant l’archive, ouvrez le fichier d’index d’archive (gpostate.xml) dans un éditeur de texte.

2.  Dans le fichier, recherchez **AGPM: port = «4600»**.

3.  Remplacez **4600** par le port sur lequel le service AGPM doit écouter; Enregistrez et fermez le fichier.

4.  Sur le serveur AGPM, redémarrez le service AGPM. (Pour plus d’informations, reportez-vous à [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service.md).)

5.  Modifiez le port dans la connexion de serveur AGPM pour chaque administrateur de stratégie de groupe. (Pour plus d’informations, voir [configurer la connexion à un serveur AGPM](configure-the-agpm-server-connection.md).)

6.  Répétez cette procédure pour chaque archive et serveur AGPM.

### Références supplémentaires

-   [Gestion du service AGPM](managing-the-agpm-service.md)

 

 





