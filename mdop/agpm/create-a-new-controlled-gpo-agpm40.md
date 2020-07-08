---
title: Créer un objet de stratégie de groupe contrôlé
description: Créer un objet de stratégie de groupe contrôlé
author: dansimp
ms.assetid: 5ce760f6-9f05-42b4-b787-7835ab8e324e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67c6af686b9ba7254cdaf93bd2d294b2d5bbb681
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808570"
---
# Créer un objet de stratégie de groupe contrôlé


Les nouveaux objets de stratégie de groupe créés via le dossier de **contrôle de modification** seront automatiquement contrôlés, ce qui vous permet de les gérer.

Un compte d’utilisateur disposant du rôle d’approbateur ou d’administrateur AGPM (contrôle total) ou des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour créer un nouvel objet de stratégie de groupe avec le contrôle de modification géré via AGPM**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Cliquez avec le bouton droit sur **modifier le contrôle**, puis cliquez sur **nouvel objet GPO contrôlé**.

3.  Dans la boîte de dialogue **nouvel objet GPO contrôlé** :

    1.  Tapez un nom pour le nouvel objet de stratégie de groupe.

    2.  Facultatif: tapez un commentaire pour le nouvel objet de stratégie de groupe à afficher dans l' **historique** de l’objet de stratégie de groupe.

    3.  Pour déployer immédiatement le nouvel objet de stratégie de groupe dans l’environnement de production du domaine, cliquez sur **créer en direct**. Pour créer le nouvel objet GPO hors connexion sans le déployer immédiatement, cliquez sur créer un fichier **hors connexion**.

    4.  Sélectionnez le modèle d’objet de stratégie de groupe à utiliser comme point de départ pour le nouvel objet de stratégie de groupe, puis cliquez sur **OK**.

4.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. Le nouvel objet GPO est affiché dans la liste des objets de stratégie de groupe sous l’onglet **contrôlé** .

### Autres éléments à prendre en considération

-   Par défaut, vous devez être approbateur ou administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer du **contenu de liste** et créer des autorisations d’objet de **stratégie de groupe** pour le domaine.

### Références supplémentaires

-   [Création ou contrôle d'un objet de stratégie de groupe](creating-or-controlling-a-gpo-agpm40-app.md)

 

 





