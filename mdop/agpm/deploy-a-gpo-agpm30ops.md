---
title: Déployer un objet de stratégie de groupe
description: Déployer un objet de stratégie de groupe
author: dansimp
ms.assetid: 3767b722-db43-40f1-a714-bb8e38bcaa10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 71c08a3b2d4f5af5bc7f1b69f964e9bb707d889c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808497"
---
# Déployer un objet de stratégie de groupe


Un approbateur peut déployer un objet de stratégie de groupe nouveau ou modifié dans l’environnement de production. Pour plus d’informations sur le redéploiement d’une version antérieure d’un objet de stratégie de groupe, voir [restaurer une version précédente d’un objet de stratégie de groupe](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md).

Un compte d’utilisateur disposant du rôle d’approbateur ou d’administrateur AGPM (contrôle total) ou des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour déployer un objet de stratégie de groupe dans l’environnement de production**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

3.  Cliquez avec le bouton droit sur l’objet de stratégie de groupe à déployer, puis cliquez sur **déployer**.

4.  Pour examiner les liens d’objets de stratégie de groupe, cliquez sur **avancé**. Placez le pointeur de la souris sur un élément de l’arborescence pour afficher les détails.

    -   Par défaut, tous les liens vers l’objet GPO sont restaurés.

    -   Pour empêcher la restauration d’un lien, désactivez la case à cocher en regard de ce lien.

    -   Pour empêcher la restauration de tous les liens, décochez la case **restaurer les liaisons** dans la boîte de dialogue **déployer l’objet GPO** .

5.  Cliquez sur **Oui**. Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**.

**Remarques**  Pour vérifier si la version la plus récente d’un objet de stratégie de groupe a été déployée, dans l’onglet **contrôlé** , double-cliquez sur l’objet de stratégie de groupe pour afficher son **historique**. Dans l' **historique** de l’objet de stratégie de groupe, la colonne **État** indique s’il s’agit d’un objet de stratégie de groupe déployé.

 

### Autres éléments à prendre en considération

-   Par défaut, vous devez être approbateur ou administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer du **contenu de liste** et déployer des autorisations d' **objet** de stratégie de groupe pour l’objet GPO.

### Références supplémentaires

-   [Exécution de tâches d'approbateur](performing-approver-tasks-agpm30ops.md)

 

 





