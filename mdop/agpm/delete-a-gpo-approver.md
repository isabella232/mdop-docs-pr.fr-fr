---
title: Supprimer un objet de stratégie de groupe
description: Supprimer un objet de stratégie de groupe
author: dansimp
ms.assetid: 85fca371-5707-49c1-aa51-813fc3a58dfc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a6419943604ee5a76d305228bb7418a8525bf33
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808525"
---
# Supprimer un objet de stratégie de groupe


Advanced Group Policy Management (AGPM) permet aux approbateurs de supprimer un objet de stratégie de groupe contrôlé (GPO) et de le déplacer vers la corbeille.

Un compte d’utilisateur ayant le rôle d’approbateur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour supprimer un objet de stratégie de groupe contrôlé**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

3.  Cliquez avec le bouton droit sur l’objet de stratégie de groupe à supprimer, puis cliquez sur **supprimer**.

    -   Pour supprimer l’objet GPO de l’archive tout en laissant la version déployée de l’objet de stratégie de groupe intacte dans l’environnement de production, cliquez sur **Supprimer l’objet de stratégie de groupe à partir de l’archive uniquement (annuler le contrôle)**.

    -   Pour supprimer l’objet GPO de l’environnement d’archivage et de production, cliquez sur **Supprimer l’objet GPO de l’archive et**de la production.

4.  Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **OK**.

5.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. L’objet de stratégie de groupe est supprimé de l’onglet **contrôlé** et s’affiche sous l’onglet de la **Corbeille** , où il peut être restauré ou détruit. Si l’objet de stratégie de groupe a été supprimé uniquement de l’archive, il apparaît également sous l’onglet non **contrôlé** .

### Autres éléments à prendre en considération

-   Par défaut, vous devez être approbateur ou administrateur AGPM (contrôle total) pour supprimer un objet de stratégie de groupe déployé. Plus précisément, vous devez disposer d’autorisations de **liste** et de **Suppression d’objets** de stratégie de groupe pour l’objet GPO.

-   Par défaut, vous devez être un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour supprimer un objet GPO de l’archive. Plus précisément, vous devez disposer du contenu de la **liste** et **modifier les paramètres** ou supprimer des autorisations d' **objet** de stratégie de groupe.

-   Pour supprimer un objet GPO non contrôlé de l’environnement de production sans le contrôler d’abord, dans la **console de gestion des stratégies de groupe**, cliquez sur **forêt**, cliquez sur **domaines**, sur ** &lt; MyDomain &gt; **, puis cliquez sur objets de stratégie de **groupe**. Cliquez avec le bouton droit sur l’objet de stratégie de groupe non contrôlé, puis cliquez sur **supprimer**.

### Références supplémentaires

-   [Suppression, restauration ou destruction d'un objet de stratégie de groupe](deleting-restoring-or-destroying-a-gpo.md)

 

 





