---
title: Vue d'ensemble de la Gestion avancée des stratégies de groupe
description: Vue d'ensemble de la Gestion avancée des stratégies de groupe
author: dansimp
ms.assetid: 028de9dd-848b-42bc-a982-65ba5c433772
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38396de6bd8bdace72d3add1bba09769ae26de32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809383"
---
# Vue d'ensemble de la Gestion avancée des stratégies de groupe


Vous pouvez utiliser la gestion de la stratégie de groupe avancée (AGPM) pour étendre les fonctionnalités de la console de gestion des stratégies de groupe (GPMC), en fournissant un contrôle complet et une gestion améliorée pour les objets de stratégie de groupe.

## Développement d’objets de stratégie de groupe avec le contrôle des modifications


Avec AGPM, vous pouvez stocker une copie de chaque GPO dans une archive centrale de sorte que les administrateurs de stratégie de groupe puissent l’afficher et le modifier sans préjudice de la version déployée de l’objet GPO. Par ailleurs, AGPM stocke une copie de chaque version de chaque GPO contrôlé dans l’archive, afin que vous puissiez revenir à une version antérieure si nécessaire.

Les termes «archiver» et «extraire» sont utilisés de la même manière que dans une bibliothèque (ou dans des applications qui fournissent un contrôle de modification, le contrôle de version ou le contrôle de code source pour le développement de programmation). Pour utiliser un classeur qui se trouve dans une bibliothèque, vous devez le faire à partir de la bibliothèque. Personne d’autre ne peut l’utiliser pendant l’extraction. Lorsque vous avez terminé d’utiliser le livre, vous le recochez dans la bibliothèque, afin que d’autres personnes puissent l’utiliser.

Lors du développement d’objets de stratégie de groupe avec AGPM:

1.  Créer un objet de stratégie de groupe contrôlé ou un contrôle d’objet de stratégie de groupe précédemment non contrôlé.

2.  Consultez l’objet de stratégie de groupe pour vous permettre de le modifier.

3.  Modifiez l’objet de stratégie de groupe.

4.  Archivez l’objet GPO modifié pour permettre aux autres utilisateurs de le modifier ou de le déployer.

5.  Passez en revue les modifications.

6.  Déploiement de l’objet de stratégie de groupe dans l’environnement de production.

## Délégation basée sur les rôles


AGPM fournit une délégation basée sur les rôles complète et facile à utiliser. Les autorisations au niveau du domaine permettent aux administrateurs d’AGPM de fournir l’accès à des domaines individuels sans permettre l’accès à d’autres domaines. La délégation basée sur les objets de stratégie de groupe permet aux administrateurs d’AGPM d’autoriser l’accès à des objets GPO spécifiques.

Dans AGPM, il existe des rôles spécifiquement définis: Administrateur AGPM (contrôle total), approbateur, éditeur et relecteur. Le rôle d’administrateur AGPM inclut les autorisations pour tous les autres rôles. Par défaut, seuls les approbateurs ont la possibilité de déployer des objets de stratégie de groupe dans l’environnement de production, en protégeant l’environnement contre les erreurs fortuites par des éditeurs moins expérimentés. Par défaut, tous les rôles incluent le rôle de réviseur et par conséquent la possibilité d’afficher les paramètres de l’objet de stratégie de groupe dans les États. Néanmoins, AGPM fournit à un administrateur AGPM la possibilité de personnaliser l’accès à l’objet de stratégie de groupe pour l’adapter aux besoins de votre organisation.

## Délégation dans un environnement d’administration de stratégie de groupe multiples


Dans un environnement dans lequel plusieurs personnes apportent des modifications à des objets de stratégie de groupe, un administrateur AGPM délègue l’autorisation aux réviseurs, aux approbateurs et aux réviseurs en tant que groupes ou personnes. Pour un processus de développement d’objet GPO standard pour un éditeur et un approbateur, voir [liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe](checklist-create-edit-and-deploy-a-gpo.md).

### Références supplémentaires

-   [Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe](checklist-create-edit-and-deploy-a-gpo.md)

-   [Exécution de tâches d'administrateur AGPM](performing-agpm-administrator-tasks.md)

-   [Exécution de tâches d'éditeur](performing-editor-tasks.md)

-   [Exécution de tâches d'approbateur](performing-approver-tasks.md)

-   [Exécution de tâches de réviseur](performing-reviewer-tasks.md)

-   [Résolution des problèmes de la Gestion avancée des stratégies de groupe](troubleshooting-advanced-group-policy-management.md)

-   [Interface utilisateur: gestion avancée des stratégies de groupe](user-interface-advanced-group-policy-management.md)

 

 





