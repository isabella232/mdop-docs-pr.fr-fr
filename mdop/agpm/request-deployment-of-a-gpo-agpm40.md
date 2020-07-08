---
title: Demander le déploiement d'un objet de stratégie de groupe
description: Demander le déploiement d'un objet de stratégie de groupe
author: dansimp
ms.assetid: 5783cfd0-bd93-46b4-8fa0-684bd39aa8fc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 46e9cc0fc12962dbdd7758c429a20fdd7c55b3cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808285"
---
# Demander le déploiement d'un objet de stratégie de groupe


Une fois que vous avez modifié et archivé un objet de stratégie de groupe, vous devez le déployer pour qu’il prenne effet dans l’environnement de production.

Un compte d’utilisateur ayant le rôle d’éditeur ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour demander le déploiement d’un objet de stratégie de groupe dans l’environnement de production du domaine**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

3.  Cliquez avec le bouton droit sur l’objet de stratégie de groupe à déployer, puis cliquez sur **déployer**.

4.  À moins que vous ne soyez un approbateur ou un administrateur AGPM ou que vous ne disposiez pas des autorisations spéciales pour déployer des objets de stratégie de groupe, vous devez demander un déploiement. Pour recevoir une copie de la demande, tapez votre adresse de messagerie dans le champ **CC** . Tapez un commentaire à afficher dans l' **historique** de l’objet de stratégie de groupe, puis cliquez sur **valider**.

5.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. L’objet de stratégie de groupe est affiché dans la liste des objets de stratégie de groupe de l’onglet **en attente** . Lorsqu’un approbateur a approuvé votre demande, l’objet GPO est déplacé de l’onglet **en attente** vers l’onglet **contrôlé** et sera déployé.

### Autres éléments à prendre en considération

-   Par défaut, vous devez être un éditeur pour effectuer cette procédure. Plus précisément, vous devez disposer du **contenu de liste** et des autorisations de **modification des paramètres** pour l’objet de stratégie de groupe.

-   Pour annuler votre demande avant qu’elle ne soit approuvée, cliquez sur l’onglet **en attente** . Cliquez avec le bouton droit sur l’objet, puis cliquez sur **retirer**. L’objet GPO sera renvoyé à l’onglet **contrôlé** .

### Références supplémentaires

-   [Exécution de tâches d'éditeur](performing-editor-tasks-agpm40.md)

 

 





