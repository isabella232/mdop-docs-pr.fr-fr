---
title: Exécution de tâches d'administrateur AGPM
description: Exécution de tâches d'administrateur AGPM
author: dansimp
ms.assetid: bc746f39-bdc9-4e2a-bc48-c3c7905de098
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 609b5b8b27fe24ff93e86bea7113929b1e04984d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809342"
---
# Exécution de tâches d'administrateur AGPM


Gestion de la stratégie de groupe avancée (AGPM) permet à un administrateur AGPM (contrôle total) de configurer les options à l’échelle du domaine et de déléguer les autorisations aux approbateurs, aux éditeurs, aux réviseurs et aux administrateurs d’AGPM. Par défaut, un administrateur d’AGPM est une personne disposant du contrôle total (toutes les autorisations d’AGPM) et qui peut donc effectuer des tâches associées à n’importe quel rôle.

Dans un environnement dans lequel plusieurs personnes développent des objets de stratégie de groupe, vous pouvez choisir de laisser tous les administrateurs de stratégie de groupe effectuer les mêmes tâches et disposer du même niveau d’accès. Ou bien, vous pouvez choisir de permettre aux administrateurs d’AGPM de déléguer des autorisations aux éditeurs qui peuvent modifier des objets de stratégie de groupe et aux approbateurs qui déploient les objets GPO dans l’environnement de production. Les administrateurs d’AGPM peuvent configurer les autorisations pour répondre aux besoins de votre organisation.

-   [Configuration de la gestion avancée](configuring-advanced-group-policy-management-agpm40.md)de la stratégie de groupe: configurez la connexion à un serveur AGPM et la notification par courrier électronique, déléguez l’accès aux objets de stratégie de groupe dans l’environnement de production et configurez la journalisation et le suivi

-   [Gestion de l’archive](managing-the-archive-agpm40.md): accès délégué aux objets de stratégie de groupe dans l’archive, limitez le nombre de versions de chaque GPO stockées, importez un objet GPO d’un autre domaine, puis sauvegardez et restaurez l’archive.

-   [Gestion du service AGPM](managing-the-agpm-service-agpm40.md): Arrêtez et démarrez le service AGPM ou modifiez le chemin d’archive, le compte de service AGPM ou le port sur lequel le service AGPM écoute.

-   [Déplacement du serveur et de l’archive AGPM](move-the-agpm-server-and-the-archive-agpm40.md): déplacez le service AGPM, l’archive ou les deux vers un autre serveur.

**Remarques**  Dans la mesure où le rôle d’administrateur AGPM inclut les autorisations de tous les autres rôles, un administrateur AGPM peut effectuer les tâches généralement associées à un autre rôle.

[Exécution des tâches approbateurs](performing-approver-tasks-agpm40.md), telles que la création, le déploiement et la suppression d’objets de stratégie de groupe

[Exécution de tâches d’éditeur](performing-editor-tasks-agpm40.md), telles que la modification, le changement de nom, l’étiquetage ou l’importation d’objets de stratégie de groupe, la création de modèles ou la définition d’un modèle par défaut

[Exécution des tâches de relecteur](performing-reviewer-tasks-agpm40.md), telles que la révision des paramètres et la comparaison d’objets de stratégie de groupe

 

### Autres éléments à prendre en considération

Par défaut, le rôle d’administrateur AGPM possède le contrôle total, c’est-à-dire les autorisations AGPM suivantes:

-   Contenu de la liste

-   Lire les paramètres

-   Modifier les paramètres

-   Créer un objet de stratégie de groupe

-   Déploiement d’objets de stratégie de groupe

-   Supprimer un objet de stratégie de groupe

-   Exporter un objet de stratégie de groupe

-   Importer un objet de stratégie de groupe

-   Créer un modèle

-   Modification des options

-   Modifier la sécurité

Les **options de modification** et de modification des autorisations de **sécurité** sont propres au rôle d’administrateur AGPM.

 

 





