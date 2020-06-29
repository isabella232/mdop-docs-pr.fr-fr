---
title: Déplacer le serveur AGPM et l'archive
description: Déplacer le serveur AGPM et l'archive
author: dansimp
ms.assetid: 13cb83c4-bb42-4e81-8660-5b7540f473d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6ae5ba9c2346caf81f5aff9f57f6b9dc97127ad1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809402"
---
# Déplacer le serveur AGPM et l'archive


Si vous remplacez le serveur AGPM et le serveur sur lequel l’archive est hébergée, vous devez déplacer le service AGPM et l’archive. Si vous le souhaitez, vous pouvez déplacer le service AGPM et l’archive séparément.

**Remarque**  
-   Le serveur AGPM est l’ordinateur qui héberge le service AGPM et l’ordinateur sur lequel est installée la gestion de stratégie de groupe avancée Microsoft – serveur.

-   Par défaut, l’archive est hébergée sur le serveur AGPM, mais vous pouvez spécifier un chemin d’accès d’archive pour l’héberger sur un autre serveur à la place.

 

Un compte d’utilisateur membre du groupe administrateurs de domaine et ayant accès à l’ancien et au nouveau serveur AGPM est requis pour effectuer cette procédure. Par ailleurs, vous devez fournir des informations d’identification pour le compte de service AGPM que le nouveau serveur AGPM doit utiliser pour effectuer cette procédure.

**Pour déplacer le service AGPM et l’archivage vers un ou plusieurs serveurs**

1.  Sauvegardez l’archive. Pour plus d’informations, voir [sauvegarder l’archive](back-up-the-archive.md).

2.  Déplacer le service AGPM:

    1.  Arrêtez le service AGPM. Pour plus d’informations, reportez-vous à [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service-agpm30ops.md).

    2.  Installez la gestion de la stratégie de groupe avancée Microsoft-serveur sur le nouveau serveur qui héberge le service AGPM. Au cours de ce processus, vous spécifiez le chemin d’accès à la nouvelle archive, l’emplacement de l’Archive par rapport au serveur AGPM. Pour plus d’informations, reportez-vous au guide détaillé pour le Guide de planification de la 3,0 stratégie de groupe Microsoft avancée ( <https://go.microsoft.com/fwlink/?LinkId=132706> ) et au Guide de planification de Microsoft Advanced Group Policy Management ( <https://go.microsoft.com/fwlink/?LinkId=141871> ).

    3.  Par le biais d’un administrateur d’AGPM (contrôle total), vous devez configurer la connexion à un serveur AGPM pour tous les administrateurs de stratégie de groupe qui utiliseront le nouveau serveur AGPM et supprimer la connexion de l’ancien serveur AGPM, ou tous les administrateurs de stratégie de groupe doivent configurer manuellement la nouvelle connexion AGPM Server et supprimer l’ancienne connexion à un serveur AGPM pour le composant logiciel AGPM. Pour plus d’informations, voir [configurer les connexions au serveur AGPM](configure-agpm-server-connections-agpm30ops.md).

        **Remarques**  Il est recommandé de désinstaller l’application gestion de la stratégie de groupe avancée Microsoft – serveur du serveur AGPM précédent. Cela permet de garantir que le service AGPM ne peut pas être redémarré involontairement sur ce serveur et risque de provoquer une confusion en cas de connexion à un serveur AGPM.

         

3.  Copiez l’archive de la sauvegarde sur le nouveau serveur qui héberge l’archive. Pour plus d’informations, voir [restaurer l’archive à partir d’une sauvegarde](restore-the-archive-from-a-backup.md).

    **Important**  Si vous avez déplacé l’archive sans déplacer le service AGPM en même temps:

    1.  Vous devez modifier la trajectoire d’archive de sorte qu’elle pointe vers le nouvel emplacement de l’Archive par rapport au serveur AGPM. Pour plus d’informations, voir [modifier le service AGPM](modify-the-agpm-service-agpm30ops.md).

    2.  Vous devez entrer à nouveau le mot de passe et le confirmer sous l’onglet **délégation de domaine** . Pour plus d’informations, voir [configurer une notification par courrier électronique](configure-e-mail-notification-agpm30ops.md).

     

### Références supplémentaires

-   [Sauvegarder l'archive](back-up-the-archive.md)

-   [Restaurer l'archive à partir d'une sauvegarde](restore-the-archive-from-a-backup.md)

-   [Configurer les connexions du serveur AGPM](configure-agpm-server-connections-agpm30ops.md)

-   [Modifier le service AGPM](modify-the-agpm-service-agpm30ops.md)

-   Guide détaillé pour la gestion avancée de la stratégie de groupe Microsoft 3,0 ( <https://go.microsoft.com/fwlink/?LinkId=132706> )

-   Guide de planification de Microsoft Advanced Group Policy Management ( <https://go.microsoft.com/fwlink/?LinkId=141871> )

-   [Exécution de tâches d'administrateur AGPM](performing-agpm-administrator-tasks-agpm30ops.md)

 

 





