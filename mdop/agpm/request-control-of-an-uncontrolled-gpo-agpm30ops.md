---
title: Demander le contrôle d'un objet de stratégie de groupe non contrôlé
description: Demander le contrôle d'un objet de stratégie de groupe non contrôlé
author: dansimp
ms.assetid: b668a67a-5a2c-4f6a-8b1c-efa3ca0794d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8cf1ede496a54d6d3d211c2e3cfc23c506217ca7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807513"
---
# Demander le contrôle d'un objet de stratégie de groupe non contrôlé


Pour proposer le contrôle de modification d’un objet de stratégie de groupe existant (GPO), l’objet GPO doit être contrôlé. Si vous n’êtes pas un approbateur ou un administrateur AGPM (contrôle total), vous devez demander le contrôle de l’objet de stratégie de groupe.

Un compte d’utilisateur ayant le rôle éditeur ou réviseur ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour contrôler un objet de stratégie de groupe non contrôlé**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet non **contrôlé** pour afficher les objets de stratégie de groupe non contrôlés.

3.  Cliquez avec le bouton droit sur l’objet de stratégie de groupe à contrôler avec AGPM, puis cliquez sur **contrôle**.

4.  Si vous n’avez pas l’autorisation spéciale pour contrôler les objets de stratégie de groupe, vous devez en demander le contrôle. Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** . Tapez un commentaire à afficher dans l' **historique** de l’objet de stratégie de groupe, puis cliquez sur **valider**.

5.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. L’objet de stratégie de groupe est supprimé de la liste sous l’onglet non **contrôlé** et ajouté à l’onglet **en attente** . Lorsqu’un approbateur a approuvé votre demande, l’objet de stratégie de groupe est déplacé vers l’onglet **contrôlé** .

### Autres éléments à prendre en considération

-   Par défaut, vous devez être un éditeur ou un relecteur pour effectuer cette procédure. En particulier, vous devez disposer du **contenu de liste** et des autorisations de **paramètres** pour le domaine.

-   Pour annuler votre demande avant qu’elle ne soit approuvée, cliquez sur l’onglet **en attente** . Cliquez avec le bouton droit sur l’objet, puis cliquez sur **retirer**. L’objet GPO sera renvoyé à l’onglet non **contrôlé** .

### Références supplémentaires

-   [Création, contrôle ou importation d'un objet de stratégie de groupe](creating-controlling-or-importing-a-gpo-agpm30ops.md)

 

 





