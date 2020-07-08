---
title: Restaurer un objet de stratégie de groupe supprimé
description: Restaurer un objet de stratégie de groupe supprimé
author: dansimp
ms.assetid: 0a131d26-a741-4a51-b612-c0bc7dbba06b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14fdf2f74f2d3db4be0db1aab7c185f5c1ab2cd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807501"
---
# Restaurer un objet de stratégie de groupe supprimé


Les approbateurs peuvent restaurer l’objet de stratégie de groupe (GPO) supprimé de la Corbeille en le renvoyant à l’archive.

Un compte d’utilisateur disposant du rôle d’approbateur ou d’administrateur AGPM (contrôle total) ou des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour restaurer un objet de stratégie de groupe supprimé**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** , cliquez sur l’onglet **Corbeille** pour afficher les objets de stratégie de groupe supprimés.

3.  Cliquez avec le bouton droit sur l’objet de stratégie de groupe à restaurer, puis cliquez sur **restaurer**.

4.  Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe, puis cliquez sur **OK**.

5.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. L’objet de stratégie de groupe est supprimé de l’onglet **Corbeille** et s’affiche sous l’onglet **contrôlé** .

**Remarques**  Si un objet de stratégie de groupe a été supprimé de l’environnement de production, sa restauration sur l’archive ne le redéploiera pas automatiquement dans l’environnement de production. Pour renvoyer l’objet GPO vers l’environnement de production, déployez l’objet GPO. Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm40.md).

 

### Autres éléments à prendre en considération

-   Par défaut, vous devez être approbateur ou administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez avoir le contenu de la **liste** et l’autorisation de **déploiement** ou de **suppression** d’un objet de stratégie de groupe pour l’objet GPO.

### Références supplémentaires

-   [Suppression, restauration ou destruction d'un objet de stratégie de groupe](deleting-restoring-or-destroying-a-gpo-agpm40.md)

 

 





