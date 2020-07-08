---
title: Créer un modèle
description: Créer un modèle
author: dansimp
ms.assetid: 6992bd55-4a4f-401f-9815-c468bac598ef
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9ad57204170fc3f49b01b571d82b00e1faf62de0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808558"
---
# Créer un modèle


La création d’un modèle vous permet d’enregistrer tous les paramètres d’une version particulière d’un objet de stratégie de groupe à utiliser comme point de départ pour la création de nouveaux objets de stratégie de groupe.

**Remarques**  Un modèle est une version statique non modifiable d’un objet de stratégie de groupe à utiliser comme point de départ pour créer de nouveaux objets de stratégie de groupe.

 

Un compte d’utilisateur ayant le rôle d’éditeur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans la gestion avancée des stratégies de groupe est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour créer un modèle sur la base d’un objet de stratégie de groupe existant**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé** ou non **contrôlé** pour afficher les objets de stratégie de groupe disponibles.

3.  Cliquez avec le bouton droit sur l’objet GPO à partir duquel vous souhaitez créer un modèle, puis cliquez sur **Enregistrer comme modèle**.

4.  Tapez un nom pour le modèle et un commentaire, puis cliquez sur **OK**.

5.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. Le nouveau modèle s’affiche sous l’onglet **modèles** .

### Autres éléments à prendre en considération

-   Par défaut, vous devez être un éditeur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer du **contenu de liste** et créer des autorisations de **modèle** pour le domaine.

-   Le changement de nom ou la suppression d’un modèle n’a pas d’incidence sur les objets de stratégie de groupe créés à partir du modèle

-   Étant donné qu’il ne peut pas être modifié, un modèle n’a pas d’historique.

### Références supplémentaires

-   [Création d'un modèle et définition d'un modèle par défaut](creating-a-template-and-setting-a-default-template.md)

-   [Demander la création d'un objet de stratégie de groupe contrôlé](request-the-creation-of-a-new-controlled-gpo.md)

 

 





