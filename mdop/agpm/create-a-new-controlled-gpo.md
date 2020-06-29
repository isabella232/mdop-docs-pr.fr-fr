---
title: Créer un objet de stratégie de groupe contrôlé
description: Créer un objet de stratégie de groupe contrôlé
author: dansimp
ms.assetid: b43ce0f4-4519-4278-83c4-c7d5163ddd11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a64e22036bfe99e1d5012d732e3f2e081acdcca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808569"
---
# Créer un objet de stratégie de groupe contrôlé


Les nouveaux objets de stratégie de groupe créés par le biais du nœud de **contrôle de modification** seront automatiquement contrôlés, ce qui vous permettra de les gérer avec AGPM (Advanced Group Policy Management).

Un compte d’utilisateur ayant le rôle d’approbateur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour créer un nouvel objet de stratégie de groupe avec le contrôle de modification géré via AGPM**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Cliquez avec le bouton droit sur le nœud de **contrôle de modification** , puis cliquez sur **nouvel objet de stratégie de**contrôle.

3.  Dans la boîte de dialogue **nouvel objet GPO contrôlé** :

    1.  Tapez un nom pour le nouvel objet de stratégie de groupe.

    2.  Facultatif: tapez un commentaire pour le nouvel objet de stratégie de groupe à afficher dans l' **historique** de l’objet de stratégie de groupe.

    3.  Pour déployer immédiatement le nouvel objet GPO dans l’environnement de production, cliquez sur **créer en direct**. Pour créer le nouvel objet GPO hors connexion sans le déployer immédiatement, cliquez sur créer un fichier **hors connexion**.

    4.  Sélectionnez le modèle d’objet de stratégie de groupe à utiliser comme point de départ pour le nouvel objet de stratégie de groupe.

    5.  Cliquez sur **OK**.

4.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. Le nouvel objet GPO est affiché dans la liste des objets de stratégie de groupe sous l’onglet **contrôlé** .

### Autres éléments à prendre en considération

-   Par défaut, vous devez être approbateur ou administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer du **contenu de liste** et créer des autorisations d’objet de **stratégie de groupe** pour le domaine.

### Références supplémentaires

-   [Création, contrôle ou importation d'un objet de stratégie de groupe](creating-controlling-or-importing-a-gpo-approver.md)

 

 





