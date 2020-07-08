---
title: Demander la création d'un objet de stratégie de groupe contrôlé
description: Demander la création d'un objet de stratégie de groupe contrôlé
author: dansimp
ms.assetid: e1875d81-8553-42ee-8f3a-023d6ced86ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7994e1af80c0ae32940d52955f7e5f773d1ee6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808257"
---
# Demander la création d'un objet de stratégie de groupe contrôlé


Si vous n’êtes pas un approbateur ou un administrateur AGPM (contrôle total), vous devez demander la création d’un objet de stratégie de groupe (objet de stratégie de groupe) s’il doit être géré à l’aide d’AGPM (Advanced Group Policy Management).

Un compte d’utilisateur disposant de l’éditeur ou du rôle de réviseur ou des autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour créer un nouvel objet de stratégie de groupe avec le contrôle de modification géré via AGPM**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Cliquez avec le bouton droit sur le nœud de **contrôle de modification** , puis cliquez sur **nouvel objet de stratégie de**contrôle.

3.  Si vous n’avez pas l’autorisation spéciale pour créer des objets de stratégie de groupe, vous devez en créer une. Dans la boîte de dialogue **nouvel objet GPO contrôlé** :

    1.  Pour recevoir une copie de la demande, entrez votre adresse de messagerie dans le champ **CC** .

    2.  Tapez un nom pour le nouvel objet de stratégie de groupe.

    3.  Facultatif: tapez un commentaire pour le nouvel objet de stratégie de groupe.

    4.  Pour déployer le nouvel objet GPO dans l’environnement de production immédiatement après approbation, cliquez sur **créer en direct**. Pour créer le nouvel objet GPO hors connexion sans le déployer immédiatement après approbation, cliquez sur créer un fichier **hors connexion**.

    5.  Sélectionnez le modèle d’objet de stratégie de groupe à utiliser comme point de départ pour le nouvel objet de stratégie de groupe.

    6.  Cliquez sur **Envoyer**.

4.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. Le nouvel objet GPO est affiché dans la liste des objets de stratégie de groupe de l’onglet **en attente** . Lorsqu’un approbateur a approuvé votre demande, l’objet de stratégie de groupe est déplacé vers l’onglet **contrôlé** .

### Autres éléments à prendre en considération

-   Par défaut, vous devez être un éditeur ou un relecteur pour effectuer cette procédure. Plus précisément, vous devez disposer de l’autorisation **contenu de liste** pour le domaine.

-   Pour annuler votre demande avant qu’elle ne soit approuvée, cliquez sur l’onglet **en attente** . Cliquez avec le bouton droit sur l’objet, puis cliquez sur **retirer**. L’objet GPO sera détruit.

### Références supplémentaires

-   [Création, contrôle ou importation d'un objet de stratégie de groupe](creating-controlling-or-importing-a-gpo-editor.md)

 

 





