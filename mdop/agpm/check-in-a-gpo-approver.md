---
title: Enregistrer un objet de stratégie de groupe
description: Enregistrer un objet de stratégie de groupe
author: dansimp
ms.assetid: e428cfff-651f-4903-bf01-d742714d2fa9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6adbcfa1c2b0d79389bc16dd1dde5afc0a4ec4a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807790"
---
# Enregistrer un objet de stratégie de groupe


En règle générale, les éditeurs doivent vérifier les objets de stratégie de groupe qu’ils ont modifiés lorsque leurs modifications sont terminées. (Pour plus d’informations, voir [modifier un objet GPO hors connexion](edit-a-gpo-offline.md).) Toutefois, si l’éditeur n’est pas disponible, un approbateur peut également archiver un objet GPO.

Un compte d’utilisateur ayant le rôle d’éditeur, d’approbateur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans la gestion avancée des stratégies de groupe est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour archiver un objet de stratégie de groupe qui a été extrait par un éditeur**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** du volet Détails, cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

    -   Pour annuler les modifications apportées par l’éditeur, cliquez avec le bouton droit sur l’objet, cliquez sur **Annuler l’extraction**, puis sur **Oui** pour confirmer.

    -   Pour conserver les modifications apportées par l’éditeur, cliquez avec le bouton droit sur l’objet, puis cliquez sur **Archiver**.

3.  Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **OK**.

4.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **Archivé**.

### Autres éléments à prendre en considération

-   Par défaut, vous devez être un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer du contenu de la **liste** et **modifier les paramètres** ou les autorisations de l’objet de **stratégie** de groupe pour l’objet GPO. Si vous n’êtes pas un approbateur ou un administrateur AGPM (ou un autre administrateur de stratégie de groupe ayant une autorisation de **déploiement d’objets** de stratégie de groupe), vous devez être l’éditeur qui a extrait l’objet de stratégie de groupe.

### Références supplémentaires

-   [Exécution de tâches d'approbateur](performing-approver-tasks.md)

-   [Modifier un objet de stratégie de groupe hors connexion](edit-a-gpo-offline.md)

 

 





