---
title: À propos des applications Application Virtualization
description: À propos des applications Application Virtualization
author: dansimp
ms.assetid: 3bf833b7-d172-4eef-a9e8-4b4f0c7eb15b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4eeea7a0ec4454aefcdde5196ae15ed029da45b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808166"
---
# À propos des applications Application Virtualization


Dans le cadre de la virtualisation des applications, une *application* est un programme exécutable, tel que Microsoft Visio, qui est transmis au client ou au client de bureau de la virtualisation de l’application pour les services Bureau à distance (auparavant services Terminal Server) à partir du serveur de gestion de la virtualisation des applications. Pour qu’une application puisse être transformée en flux vers un client, l’application doit être préparée en vue d’une diffusion en continu en la traitant avec le Sequencer de virtualisation de l’application.

## Gestion des applications


Vous devez ajouter des applications au système avant de pouvoir rendre les applications accessibles aux utilisateurs. La méthode la plus courante pour ajouter des applications au système consiste à les importer. Pour accéder à cette fonctionnalité, cliquez avec le bouton droit sur le nœud **applications** dans la console de gestion du serveur d’applications et sélectionnez **importer des applications**.

Vous pouvez importer plusieurs fichiers Open Software Descriptor (OSD) en même temps, ou vous pouvez importer un fichier de projet de Sequencer (SPRJ) qui peut contenir plusieurs fichiers OSD. Cette fonctionnalité vous permet de configurer les applications associées de manière similaire.

Vous pouvez également utiliser les fonctionnalités suivantes pour vous aider à gérer vos applications:

-   **Groupes d’applications**: permet de créer des groupes logiques d’applications pour une gestion simplifiée. Lorsque des modifications sont apportées à un groupe (par exemple, des autorisations d’accès), les modifications sont appliquées à toutes les applications du groupe. Les applications d’un groupe peuvent provenir de différents packages.

-   **Sélection multiple**: permet de sélectionner plusieurs applications à la fois en maintenant la touche CTRL enfoncée lorsque vous cliquez sur une application pour modifier les propriétés de l’application. Toutefois, si vous voulez conserver une relation entre les applications, vous devez créer un groupe d’applications pour contenir les applications.

-   **Copie du système entre systèmes**: permet de copier des applications d’un environnement vers un autre qui exécute la même version d’App-V en une seule étape. Par exemple, vous pouvez avoir un environnement de test d’acceptation utilisateur dans lequel vous déployez et configurez initialement des applications. Après avoir terminé votre phase de test, vous pouvez répliquer le même ensemble d’applications (y compris les autorisations) sur l’environnement de production.

## Rubriques connexes


[À propos des packages Application Virtualization](about-application-virtualization-packages.md)

[À propos d'Application Virtualization Server Management Console](about-the-application-virtualization-server-management-console.md)

[Procédure pour gérer des groupes d'applications dans Server Management Console](how-to-manage-application-groups-in-the-server-management-console.md)

[Procédure pour gérer des applications dans Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

 

 





