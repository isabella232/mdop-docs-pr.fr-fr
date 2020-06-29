---
title: Importer un objet de stratégie de groupe de production
description: Importer un objet de stratégie de groupe de production
author: dansimp
ms.assetid: 35c2a682-ece8-4577-a083-7e3e9facfd13
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3d739a46d5ca078ec9d218c1cc1e5bd258c55601
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808417"
---
# Importer un objet de stratégie de groupe de production


Si des modifications sont apportées à un objet de stratégie de groupe contrôlé (GPO) en dehors de la gestion de la stratégie de groupe avancée (AGPM), vous pouvez importer une copie de l’objet de stratégie de groupe à partir de l’environnement de production et l’enregistrer dans l’Archive pour amener l’archive et l’environnement de production à un état cohérent. (Pour importer un objet de stratégie de groupe non contrôlé, contrôlez l’objet GPO. Voir [demander le contrôle d’un objet de stratégie de groupe non contrôlé](request-control-of-an-uncontrolled-gpo-agpm30ops.md).)

Un compte d’utilisateur ayant le rôle d’éditeur, d’approbateur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires inAGPM est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour importer un objet de stratégie de groupe à partir de l’environnement de production**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

3.  Cliquez avec le bouton droit sur l’objet de stratégie de groupe, puis cliquez sur **Importer à partir de la production**.

4.  Tapez un commentaire pour la piste d’audit de l’objet de stratégie de groupe, puis cliquez sur **OK**.

### Autres éléments à prendre en considération

-   Par défaut, vous devez être un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer du contenu de la **liste** et **modifier les paramètres**, déployer l’objet de stratégie de **groupe**ou **supprimer** des autorisations d’objet GPO pour l’objet GPO.

### Références supplémentaires

-   [Création, contrôle ou importation d'un objet de stratégie de groupe](creating-controlling-or-importing-a-gpo-agpm30ops.md)

 

 





