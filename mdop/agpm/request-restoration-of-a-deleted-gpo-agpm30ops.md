---
title: Demander la restauration d'un objet de stratégie de groupe supprimé
description: Demander la restauration d'un objet de stratégie de groupe supprimé
author: dansimp
ms.assetid: dcc3baea-8af7-4886-a301-98b6ac5819cd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f85620ed7d9afe676caabe4ce0f7da4fd8d5ae13
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808278"
---
# Demander la restauration d'un objet de stratégie de groupe supprimé


Sauf si vous êtes un approbateur ou un administrateur AGPM (contrôle total), vous devez demander la restauration d’un objet de stratégie de groupe (GPO) supprimé de la corbeille.

Un compte d’utilisateur ayant le rôle d’éditeur ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour demander la restauration d’un objet de stratégie de groupe supprimé**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** , cliquez sur l’onglet **Corbeille** pour afficher les objets de stratégie de groupe supprimés.

3.  Cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous voulez restaurer, puis cliquez sur **restaurer**.

4.  Sauf si vous disposez d’une autorisation spéciale pour restaurer des objets de stratégie de groupe, vous devez demander la restauration de l’objet de stratégie de groupe supprimé. Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** . Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **valider**.

5.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. L’objet de stratégie de groupe est supprimé de l’onglet **Corbeille** et s’affiche sous l’onglet **contrôlé** .

**Remarques**  Si un objet de stratégie de groupe a été supprimé de l’environnement de production, sa restauration sur l’archive ne le redéploiera pas automatiquement dans l’environnement de production. Pour renvoyer l’objet GPO vers l’environnement de production, déployez l’objet GPO. Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm30ops.md).

 

### Autres éléments à prendre en considération

-   Par défaut, vous devez être un éditeur pour effectuer cette procédure. En particulier, vous devez disposer du **contenu de liste** et de l’autorisation de **modification des paramètres** pour l’objet de stratégie de groupe.

-   Pour annuler votre demande avant qu’elle ne soit approuvée, cliquez sur l’onglet **en attente** . Cliquez avec le bouton droit sur l’objet, puis cliquez sur **retirer**. L’objet GPO sera renvoyé à l’onglet **Corbeille** .

### Références supplémentaires

-   [Suppression, restauration ou destruction d'un objet de stratégie de groupe](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 





