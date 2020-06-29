---
title: Onglet Serveur AGPM
description: Onglet Serveur AGPM
author: dansimp
ms.assetid: fb3b0265-53ed-4bf6-88a4-c409f5f1bed4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 335cad07691f914884583636cef01be8dbaa0266
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807846"
---
# Onglet Serveur AGPM


L’onglet **serveur AGPM** du volet de **contrôle des modifications** vous permet de sélectionner un serveur AGPM en entrant un nom d’ordinateur et un port complets et de supprimer les versions antérieures d’objets de stratégie de groupe de l’Archive pour économiser de l’espace disque sur le serveur AGPM.

## Spécification du serveur AGPM


Le serveur AGPM sélectionné détermine le type d’archive qui s’affiche dans l’onglet **Sommaire** et à quel emplacement les paramètres de **délégation de domaine** sont appliqués. Le port par défaut pour la gestion de la stratégie de groupe avancée (AGPM) est le port 4600.

Si la connexion au serveur AGPM est configurée de façon centralisée à l’aide des paramètres de modèle d’administration, les options de cet onglet pour configurer la connexion ne sont pas disponibles. Pour plus d’informations, voir [configurer les connexions au serveur AGPM](configure-agpm-server-connections-agpm30ops.md).

## Suppression des anciennes versions de l’objet de stratégie de groupe


Par défaut, toutes les versions de chaque GPO contrôlé sont conservées dans l’archive. Toutefois, vous pouvez configurer le service AGPM pour limiter le nombre de versions conservées pour chaque objet de stratégie de groupe et supprimer automatiquement la version la plus ancienne lorsque cette limite est dépassée. Uniquement les versions d’objets de stratégie de groupe affichées sous l’onglet **versions uniques** de la fenêtre **historique** vers la limite.

**Remarques**  Le nombre maximal de versions uniques à stocker pour chaque objet de stratégie de groupe n’inclut pas la version actuelle, donc la saisie de 0 conserve uniquement la version actuelle. La limite ne doit pas être supérieure à 999 versions.

Lors de la suppression d’une version d’un objet de stratégie de groupe, un enregistrement de cette version reste dans l’historique de l’objet de stratégie de groupe, mais la version de l’objet de stratégie de groupe est supprimée de l’archive. Vous pouvez empêcher la suppression d’une version d’un objet de stratégie de groupe en le sélectionnant dans l’historique en tant que non supprimable.

 

### Références supplémentaires

-   [Interface utilisateur: gestion avancée des stratégies de groupe](user-interface-advanced-group-policy-management-agpm30ops.md)

-   [Exécution de tâches d'administrateur AGPM](performing-agpm-administrator-tasks-agpm30ops.md)

-   [Exécution de tâches de réviseur](performing-reviewer-tasks-agpm30ops.md)

 

 





