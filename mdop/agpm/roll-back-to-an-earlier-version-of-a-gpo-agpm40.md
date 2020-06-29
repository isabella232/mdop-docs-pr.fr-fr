---
title: Revenir à une version antérieure d'objet de stratégie de groupe
description: Revenir à une version antérieure d'objet de stratégie de groupe
author: dansimp
ms.assetid: 06ce9251-95e0-46d0-99c2-b9a0690e5891
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1146a8ecaf25796b9ac105ba46ea7f27b06fc8aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808241"
---
# Revenir à une version antérieure d'objet de stratégie de groupe


Un approbateur peut annuler les modifications apportées à un objet de stratégie de groupe en redéployant une version antérieure de l’objet de stratégie de groupe à partir de son historique. Le déploiement d’une version antérieure d’un objet de stratégie de groupe remplace la version de l’objet de stratégie de groupe actuellement en production.

Un compte d’utilisateur disposant du rôle d’approbateur ou d’administrateur AGPM (contrôle total) ou des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour déployer une version antérieure d’un objet de stratégie de groupe dans l’environnement de production du domaine**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

3.  Double-cliquez sur l’objet de stratégie de groupe à déployer pour afficher son **historique**.

4.  Cliquez avec le bouton droit sur la version que vous voulez déployer, cliquez sur **déployer**, puis sur **Oui**.

5.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. Dans la fenêtre **historique** , cliquez sur **Fermer**.

**Remarques**  Pour vérifier que la version qui a été redéployée correspond à la version prévue, examinez un rapport de différences pour les deux versions. Dans la fenêtre **historique** de l’objet de stratégie de groupe, sélectionnez les deux versions, puis cliquez avec le bouton droit et sélectionnez **différence** et l’état **HTML** ou **rapport XML**.

 

### Autres éléments à prendre en considération

-   Par défaut, vous devez être approbateur ou administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer du **contenu de liste** et déployer des autorisations d' **objet** de stratégie de groupe pour l’objet GPO.

### Références supplémentaires

-   [Exécution de tâches d'approbateur](performing-approver-tasks-agpm40.md)

 

 





