---
title: Vérifier les liens objet de stratégie de groupe
description: Vérifier les liens objet de stratégie de groupe
author: dansimp
ms.assetid: 3aaba9da-f0aa-466f-bd1c-49f11d00ea54
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3884a6f3852986cf02e499af59bb56fcaf404ef8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807470"
---
# Vérifier les liens objet de stratégie de groupe


Vous pouvez afficher un diagramme qui indique l’emplacement d’un objet de stratégie de groupe ou d’objets de stratégie de groupe que vous sélectionnez et qui sont liés à des unités d’organisation. Les diagrammes de liens d’objets de stratégie de groupe sont mis à jour chaque fois que l’objet de stratégie de groupe est contrôlé, importé ou archivé.

Un compte d’utilisateur disposant du rôle de relecteur, d’éditeur, d’approbateur ou d’un administrateur AGPM (contrôle total) ou des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

## Examen des liens d’objets de stratégie de groupe


-   [Pour un ou plusieurs objets de stratégie de groupe](#bkmk-gpos)

-   [Pour une ou plusieurs versions d’un objet de stratégie de groupe](#bkmk-gpo-versions)

### <a href="" id="bkmk-gpos"></a>

**Pour afficher les liens d’objets de stratégie de groupe pour un ou plusieurs objets de stratégie de groupe**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé**, **en attente**ou **Corbeille** pour afficher les objets de stratégie de groupe.

3.  Sélectionnez un ou plusieurs objets de stratégie de groupe pour lesquels afficher les liens, cliquez avec le bouton droit sur un objet de stratégie de groupe sélectionné, cliquez sur **paramètres**, puis cliquez sur **liens d’objets de stratégie** de groupe pour afficher un diagramme de domaines et d’unités d’organisation avec des liens vers les objets de stratégie de groupe sélectionnés.

### <a href="" id="bkmk-gpo-versions"></a>

**Pour afficher les liens d’objets de stratégie de groupe pour une ou plusieurs versions d’un objet de stratégie de groupe**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôle** ou **Corbeille** pour afficher les objets de stratégie de groupe.

3.  Double-cliquez sur l’objet de stratégie de groupe pour afficher son historique.

4.  Cliquez avec le bouton droit sur la version de l’objet de stratégie de groupe dont vous souhaitez examiner les paramètres, cliquez sur **paramètres**, puis sur **rapport HTML** ou **État XML** pour afficher un récapitulatif des paramètres de l’objet de stratégie de groupe.

### Autres éléments à prendre en considération

-   Par défaut, vous devez être un réviseur, un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure. En particulier, vous devez disposer du **contenu de liste** et des autorisations de **paramètres** pour l’objet GPO. Par ailleurs, pour afficher la liste des objets de stratégie de groupe, vous devez disposer de l’autorisation **contenu de liste** pour le domaine.

### Références supplémentaires

-   [Exécution de tâches de réviseur](performing-reviewer-tasks-agpm40.md)

 

 





