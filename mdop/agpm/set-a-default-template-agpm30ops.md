---
title: Définir un modèle par défaut
description: Définir un modèle par défaut
author: dansimp
ms.assetid: 84edbd69-451b-4c10-a898-781d4b75d09c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dec198126e98e1267589fdf252e158a0b1181b05
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808234"
---
# Définir un modèle par défaut


En tant qu’éditeur, vous pouvez spécifier lequel des modèles disponibles sera le modèle par défaut suggéré par tous les administrateurs de stratégie de groupe pour créer des objets de stratégie de groupe.

**Remarques**  Un modèle est une version statique non modifiable d’un objet de stratégie de groupe à utiliser comme point de départ pour créer de nouveaux objets de stratégie de groupe.

 

Un compte d’utilisateur ayant le rôle d’éditeur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour définir le modèle par défaut à utiliser lors de la création de nouveaux objets de stratégie de groupe**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **modèles** pour afficher les modèles disponibles.

3.  Cliquez avec le bouton droit sur le modèle que vous voulez définir par défaut, puis cliquez sur **définir par défaut**.

4.  Cliquez sur **Oui** pour confirmer.

5.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. Le modèle par défaut comporte une icône bleue et l’État est identifié comme **modèle (par défaut)** sous l’onglet **modèles** .

### Autres éléments à prendre en considération

-   Par défaut, vous devez être un éditeur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer du **contenu de liste** et créer des autorisations de **modèle** pour le domaine.

-   Après avoir défini un modèle comme modèle par défaut, ce modèle sera le premier sélectionné dans la boîte de dialogue **nouvel objet GPO contrôlé** lors de la création de nouveaux objets de stratégie de groupe par les administrateurs de stratégie de groupe. Toutefois, ils pourront sélectionner un autre modèle d’objet de stratégie de groupe, y compris un ** &lt; objet de stratégie de groupe &gt; vide**, qui n’inclut pas de paramètres.

-   Le changement de nom ou la suppression d’un modèle n’a pas d’incidence sur les objets de stratégie de groupe créés à partir du modèle

-   Étant donné qu’il ne peut pas être modifié, un modèle n’a pas d’historique.

### Références supplémentaires

-   [Création d'un modèle et définition d'un modèle par défaut](creating-a-template-and-setting-a-default-template-agpm30ops.md)

-   [Demander la création d'un objet de stratégie de groupe contrôlé](request-the-creation-of-a-new-controlled-gpo-agpm30ops.md)

 

 





