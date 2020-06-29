---
title: Vue d'ensemble de la Gestion avancée des stratégies de groupe
description: Vue d'ensemble de la Gestion avancée des stratégies de groupe
author: dansimp
ms.assetid: 3a8d1e58-12b9-42bd-898f-6d57514dfbb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: feb43972c78ed12501e372800c1f5ec19609477a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809389"
---
# Vue d'ensemble de la Gestion avancée des stratégies de groupe


Vous pouvez utiliser la gestion de la stratégie de groupe avancée (AGPM) pour étendre les fonctionnalités de la console de gestion des stratégies de groupe (GPMC) afin de fournir un contrôle de modification complet et une gestion améliorée pour les objets de stratégie de groupe.

## Développement d’objets de stratégie de groupe avec le contrôle des modifications


Avec AGPM, vous pouvez stocker une copie de chaque GPO dans une archive centrale de sorte que les administrateurs de stratégie de groupe puissent l’afficher et le modifier sans affecter immédiatement la version déployée de l’objet GPO. Par ailleurs, AGPM stocke une copie de chaque version de chaque GPO contrôlé dans l’archive, afin que vous puissiez revenir à une version antérieure si nécessaire.

Les termes «archiver» et «extraire» sont utilisés de la même façon que dans une bibliothèque (ou dans des applications qui fournissent le contrôle de changement, le contrôle de version ou le contrôle de code source pour le développement de programmation). Pour utiliser un classeur qui se trouve dans une bibliothèque, vous devez le faire à partir de la bibliothèque. Personne d’autre ne peut l’utiliser pendant l’extraction. Lorsque vous avez terminé d’utiliser le livre, vous le recochez dans la bibliothèque, afin que d’autres personnes puissent l’utiliser.

Lorsque vous développez des objets de stratégie de groupe à l’aide d’AGPM:

1.  Créer un objet de stratégie de groupe contrôlé ou un contrôle d’objet de stratégie de groupe précédemment non contrôlé.

2.  Consultez l’objet de stratégie de groupe pour pouvoir le modifier.

3.  Modifiez l’objet de stratégie de groupe.

4.  Archivez l’objet GPO modifié pour permettre aux autres utilisateurs de le modifier ou de le déployer.

5.  Passez en revue les modifications.

6.  Déploiement de l’objet de stratégie de groupe dans l’environnement de production.

## Délégation basée sur les rôles


AGPM fournit une délégation complète et facile à utiliser basée sur les rôles pour gérer l’accès aux objets de stratégie de groupe dans l’archive. Les autorisations au niveau du domaine permettent aux administrateurs d’AGPM d’offrir un accès aux domaines individuels sans avoir accès à d’autres domaines. La délégation basée sur un ensemble d’objets permet aux administrateurs d’AGPM d’offrir un accès à des objets de stratégie de groupe spécifiques sans fournir un accès à l’échelle du domaine

Dans AGPM, il existe des rôles spécifiquement définis: Administrateur AGPM (contrôle total), approbateur, éditeur et relecteur. Le rôle d’administrateur AGPM inclut les autorisations pour tous les autres rôles. Par défaut, seuls les approbateurs ont la possibilité de déployer des objets de stratégie de groupe dans l’environnement de production, en protégeant l’environnement contre les erreurs, par des éditeurs moins expérimentés. Par défaut, tous les rôles incluent le rôle de réviseur et par conséquent la possibilité d’afficher les paramètres de l’objet de stratégie de groupe dans les États. Néanmoins, AGPM fournit à un administrateur AGPM la possibilité de personnaliser l’accès à l’objet de stratégie de groupe pour l’adapter aux besoins de votre organisation.

## Délégation dans un environnement d’administration de stratégie de groupe multiples


Dans un environnement dans lequel plusieurs personnes changent d’objets de stratégie de groupe, un administrateur d’AGPM délègue l’autorisation aux réviseurs, aux approbateurs et aux réviseurs en tant que groupes ou personnes. Pour un processus de développement d’objet GPO standard pour un éditeur et un approbateur, voir [liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md).

### Références supplémentaires

-   [Guide des opérations de la Gestion avancée des stratégies de groupe Microsoft3.0](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





