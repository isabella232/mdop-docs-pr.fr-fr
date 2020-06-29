---
title: Restaurer un objet de stratégie de groupe supprimé
description: Restaurer un objet de stratégie de groupe supprimé
author: dansimp
ms.assetid: e6953296-7b7d-4d1e-ad82-d4a23044cdd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2cba097ecd651a91f828901d8115a7020d6da819
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807497"
---
# Restaurer un objet de stratégie de groupe supprimé


Gestion de la stratégie de groupe avancée (AGPM) permet aux approbateurs de restaurer un objet de stratégie de groupe supprimé de la corbeille, en le renvoyant à l’archive.

Un compte d’utilisateur ayant le rôle d’éditeur, d’approbateur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans la gestion avancée des stratégies de groupe est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour restaurer un objet de stratégie de groupe supprimé**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** , cliquez sur l’onglet **Corbeille** pour afficher les objets de stratégie de groupe supprimés.

3.  Cliquez avec le bouton droit sur l’objet de stratégie de groupe à restaurer, puis cliquez sur **restaurer**.

4.  Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe, puis cliquez sur **OK**.

5.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. L’objet de stratégie de groupe est supprimé de l’onglet **Corbeille** et s’affiche sous l’onglet **contrôlé** .

**Remarques**  Si un objet de stratégie de groupe a été supprimé de l’environnement de production, sa restauration sur l’archive ne le redéploiera pas automatiquement dans l’environnement de production. Pour renvoyer l’objet GPO vers l’environnement de production, déployez l’objet GPO. Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo.md).

 

### Autres éléments à prendre en considération

-   Par défaut, vous devez être un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer du contenu de la **liste** et **modifier les paramètres**, déployer l’objet de stratégie de **groupe**ou **supprimer** des autorisations d’objet GPO pour l’objet GPO.

### Références supplémentaires

-   [Suppression, restauration ou destruction d'un objet de stratégie de groupe](deleting-restoring-or-destroying-a-gpo.md)

 

 





