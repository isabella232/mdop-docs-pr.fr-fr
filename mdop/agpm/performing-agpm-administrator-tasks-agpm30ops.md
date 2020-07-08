---
title: Exécution de tâches d'administrateur AGPM
description: Exécution de tâches d'administrateur AGPM
author: dansimp
ms.assetid: 9678b0f4-70a5-411e-a896-afa4dc9ea6c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26b412e5b22e46af938d127751fdca1da722a8c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809347"
---
# Exécution de tâches d'administrateur AGPM


Dans Advanced Group Policy Management (AGPM), un administrateur AGPM (contrôle total) configure les autorisations à l’échelle du domaine et délègue les autorisations aux approbateurs, aux éditeurs, aux réviseurs et aux autres administrateurs d’AGPM. Par défaut, un administrateur AGPM est une personne disposant du contrôle total, toutes les autorisations d’AGPM, qui peuvent donc effectuer des tâches associées à n’importe quel rôle.

Dans un environnement dans lequel plusieurs personnes développent des objets de stratégie de groupe, vous pouvez choisir si tous les utilisateurs d’AGPM effectuent les mêmes tâches et disposent du même niveau d’accès, ou si les administrateurs AGPM délèguent des autorisations aux éditeurs qui apportent des modifications à des objets de stratégie de groupe et à des approbateurs qui déploient des objets de stratégie de groupe Les administrateurs d’AGPM peuvent configurer les autorisations pour répondre aux besoins de votre organisation.

-   [Configuration de la gestion avancée](configuring-advanced-group-policy-management.md)de la stratégie de groupe: configurez la connexion à un serveur AGPM et la notification par courrier électronique, déléguez l’accès aux objets de stratégie de groupe dans l’environnement de production et configurez la journalisation et le suivi

-   [Gestion de l’archive](managing-the-archive.md): déléguez l’accès aux objets de stratégie de groupe dans l’archive et limitez le nombre de versions de chaque GPO stockées.

-   [Gestion du service AGPM](managing-the-agpm-service-agpm30ops.md): Arrêtez et démarrez le service AGPM ou modifiez le chemin d’archive, le compte de service AGPM ou le port sur lequel le service AGPM écoute.

-   [Déplacement du serveur et de l’archive AGPM](move-the-agpm-server-and-the-archive.md): déplacez le service AGPM, l’archive ou les deux vers un autre serveur.

Par ailleurs, dans la mesure où le rôle d’administrateur AGPM inclut les autorisations de tous les autres rôles, un administrateur AGPM peut effectuer les tâches normalement associées à un autre rôle.

-   [Exécution des tâches approbateurs](performing-approver-tasks-agpm30ops.md), telles que la création, le déploiement et la suppression d’objets de stratégie de groupe

-   [Exécution de tâches d’éditeur](performing-editor-tasks-agpm30ops.md), telles que la modification, le changement de nom, l’étiquetage ou l’importation d’objets de stratégie de groupe, la création de modèles ou la définition d’un modèle par défaut

-   [Exécution des tâches de relecteur](performing-reviewer-tasks-agpm30ops.md), telles que la révision des paramètres et la comparaison d’objets de stratégie de groupe

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

 

 





