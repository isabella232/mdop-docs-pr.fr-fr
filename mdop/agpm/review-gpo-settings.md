---
title: Vérifier les paramètres de l'objet de stratégie de groupe
description: Vérifier les paramètres de l'objet de stratégie de groupe
author: dansimp
ms.assetid: e82570b2-d8ce-4bf0-8ad7-8910409f3041
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 681492f423266ce3722bb1a657ee93527c6bdd7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807465"
---
# Vérifier les paramètres de l'objet de stratégie de groupe


Vous pouvez générer des rapports HTML et XML pour vérifier les paramètres dans n’importe quelle version d’un objet de stratégie de groupe (GPO).

Un compte d’utilisateur disposant du rôle de réviseur, d’éditeur, d’approbateur ou d’administrateur AGPM (contrôle total) ou des autorisations nécessaires dans la gestion avancée des stratégies de groupe est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour vérifier les paramètres de n’importe quelle version d’un objet de stratégie de groupe**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** du volet Détails, cliquez sur un onglet pour afficher les objets de stratégie de groupe.

3.  Double-cliquez sur l’objet de stratégie de groupe pour afficher son historique.

4.  Cliquez avec le bouton droit sur la version de l’objet de stratégie de groupe dont vous souhaitez examiner les paramètres, cliquez sur **paramètres**, puis sur **rapport HTML** ou **État XML** pour afficher un récapitulatif des paramètres de l’objet de stratégie de groupe.

### Autres éléments à prendre en considération

-   Par défaut, vous devez être un réviseur, un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure. En particulier, vous devez disposer du **contenu de liste** et des autorisations de **paramètres** pour l’objet GPO. Par ailleurs, pour afficher la liste des objets de stratégie de groupe, vous devez disposer de l’autorisation **contenu de liste** pour le domaine.

### Références supplémentaires

-   [Exécution de tâches de réviseur](performing-reviewer-tasks.md)

 

 





