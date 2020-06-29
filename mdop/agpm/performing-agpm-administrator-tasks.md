---
title: Exécution de tâches d'administrateur AGPM
description: Exécution de tâches d'administrateur AGPM
author: dansimp
ms.assetid: 32e694a7-be64-4943-bce2-2a3a15e5341f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0daa8df93a88ed155e9f894011d4dd835761948b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808322"
---
# Exécution de tâches d'administrateur AGPM


Un administrateur AGPM (contrôle total) configure les autorisations à l’échelle du domaine et délègue les autorisations aux approbateurs, éditeurs, réviseurs et autres administrateurs d’AGPM. Par défaut, un administrateur AGPM est une personne disposant du contrôle total (toutes les autorisations de gestion de la stratégie de groupe avancées \ [AGPM \]) et peut également effectuer des tâches associées à n’importe quel rôle.

Dans un environnement dans lequel plusieurs personnes développent des objets de stratégie de groupe, vous pouvez choisir si tous les utilisateurs de gestion de la stratégie de groupe avancés (AGPM) effectuent les mêmes tâches et disposent du même niveau d’accès, ou si les administrateurs d’AGPM délèguent des autorisations aux éditeurs qui apportent des modifications à des objets de stratégie de groupe et à l’environnement de production. Les administrateurs d’AGPM peuvent configurer les autorisations pour répondre aux besoins de votre organisation.

-   [Configurer la connexion au serveur AGPM](configure-the-agpm-server-connection.md)

-   [Configurer la notification par courrier électronique](configure-e-mail-notification.md)

-   [Accès au niveau du domaine de délégué](delegate-domain-level-access.md)

-   [Déléguer l'accès à un objet de stratégie de groupe individuel](delegate-access-to-an-individual-gpo.md)

-   [Configurer la journalisation et suivi](configure-logging-and-tracing.md)

-   [Gestion du service AGPM](managing-the-agpm-service.md)

    -   [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service.md)

    -   [Modifier le chemin d'accès de l'archive](modify-the-archive-path.md)

    -   [Modifier le compte du service AGPM](modify-the-agpm-service-account.md)

    -   [Modifier le port sur lequel le service AGPM écoute](modify-the-port-on-which-the-agpm-service-listens.md)

Par ailleurs, dans la mesure où le rôle d’administrateur AGPM inclut les autorisations de tous les autres rôles, un administrateur AGPM peut effectuer les tâches normalement associées à un autre rôle.

-   [Exécution des tâches approbateurs](performing-approver-tasks.md), telles que la création, le déploiement et la suppression d’objets de stratégie de groupe

-   [Exécution de tâches d’éditeur](performing-editor-tasks.md), telles que la modification, le changement de nom, l’étiquetage ou l’importation d’objets de stratégie de groupe, la création de modèles ou la définition d’un modèle par défaut

-   [Exécution des tâches de relecteur](performing-reviewer-tasks.md), telles que la révision des paramètres et la comparaison d’objets de stratégie de groupe

### Autres éléments à prendre en considération

Par défaut, le rôle d’administrateur AGPM possède le contrôle total, c’est-à-dire les autorisations AGPM suivantes:

-   Contenu de la liste

-   Lire les paramètres

-   Modifier les paramètres

-   Créer un objet de stratégie de groupe

-   Déploiement d’objets de stratégie de groupe

-   Supprimer un objet de stratégie de groupe

-   Modification des options

-   Modifier la sécurité

-   Créer un modèle

Les **options de modification** et de modification des autorisations de **sécurité** sont propres au rôle d’administrateur AGPM.

 

 





