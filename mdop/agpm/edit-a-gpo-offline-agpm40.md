---
title: Modifier un objet de stratégie de groupe hors connexion
description: Modifier un objet de stratégie de groupe hors connexion
author: dansimp
ms.assetid: 9c75eb3c-d4d5-41e0-b65e-8b4464a42cd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7ba0f72d7bfa8e2c597f62f7675a754807525ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808489"
---
# Modifier un objet de stratégie de groupe hors connexion


Pour apporter des modifications à un objet de stratégie de groupe contrôlé (GPO), vous devez d’abord extraire une copie de l’objet GPO de l’archive. Personne ne peut modifier l’objet de stratégie de groupe tant qu’il n’a pas été réintégré, ce qui empêche l’introduction de modifications conflictuelles de plusieurs administrateurs de stratégie de groupe. Lorsque vous avez fini de modifier l’objet de stratégie de groupe, vous le consultez dans l’archive afin qu’il puisse être examiné et déployé dans l’environnement de production.

Un compte d’utilisateur ayant le rôle d’éditeur ou d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe, ou un compte d’utilisateur disposant des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

## Modification d’un objet de stratégie de groupe hors connexion


Pour modifier un objet de stratégie de groupe, vous pouvez extraire l’objet de stratégie de groupe à partir de l’archive, modifier l’objet de stratégie de groupe en mode hors connexion, puis vérifier l’objet GPO dans l’archive afin qu’il puisse être consulté et déployé (ou modifié par d’autres éditeurs).

-   [Extraire un objet de stratégie de groupe à partir de l’archive en vue de le modifier](#bkmk-checkout)

-   [Modification d’un objet de stratégie de groupe hors connexion](#bkmk-edit)

-   [Archiver un objet GPO dans l’archive](#bkmk-checkin)

### <a href="" id="bkmk-checkout"></a>

**Pour extraire un objet GPO de l’archive en vue de le modifier**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

3.  Cliquez avec le bouton droit sur l’objet de stratégie de groupe à modifier, puis cliquez sur **extraire**.

4.  Tapez un commentaire à afficher dans l’historique de l’objet de stratégie de groupe lors de son extraction, puis cliquez sur **OK**.

5.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est désormais identifié comme **extrait**.

### <a href="" id="bkmk-edit"></a>

**Pour modifier un objet GPO hors connexion**

1.  Dans l’onglet **contrôlé** , cliquez avec le bouton droit sur l’objet de stratégie de groupe à modifier, puis cliquez sur **modifier**.

2.  Dans la fenêtre **éditeur de gestion des stratégies de groupe** , apporter des modifications à une copie hors connexion de l’objet de stratégie de groupe.

    **Remarques**  Pour désactiver tous les paramètres de configuration de l’ordinateur ou tous les paramètres de configuration de l’utilisateur, cliquez avec le bouton droit sur l’objet dans la fenêtre **éditeur de gestion des stratégies de groupe** , puis cliquez sur **Propriétés**. Sélectionnez **Désactiver les paramètres de configuration** de l’ordinateur ou **Désactiver les paramètres de configuration** de l’utilisateur, le cas échéant.

     

3.  Lorsque vous avez terminé de modifier l’objet de stratégie de **groupe** , fermez la fenêtre Éditeur de gestion des stratégies de groupe.

### <a href="" id="bkmk-checkin"></a>

**Pour archiver un objet GPO dans l’archive**

1.  Dans l’onglet **contrôlé** :

    -   Si vous n’avez apporté aucune modification à l’objet de stratégie de groupe, cliquez avec le bouton droit sur celui-ci, puis cliquez sur **Annuler l’extraction**, puis sur **Oui** pour confirmer.

    -   Si vous avez apporté des modifications à l’objet de stratégie de groupe, cliquez avec le bouton droit sur celui-ci, puis cliquez sur **Archiver**.

2.  Tapez un commentaire à afficher dans la trace d’audit de l’objet de stratégie de groupe, puis cliquez sur **OK**.

3.  Lorsque la fenêtre de **progression** indique que l’avancement global est terminé, cliquez sur **Fermer**. Dans l’onglet **contrôlé** , l’état de l’objet de stratégie de groupe est identifié comme **Archivé**.

### Autres éléments à prendre en considération

-   Pour extraire et modifier un objet de stratégie de groupe, par défaut, vous devez être l’approbateur qui a créé ou contrôlé l’objet de stratégie de groupe, un éditeur ou un administrateur AGPM (contrôle total). Plus précisément, vous devez disposer du **contenu de liste** et des autorisations de **modification des paramètres** pour l’objet de stratégie de groupe. En outre, pour modifier l’objet de stratégie de groupe, vous devez être la personne qui a extrait l’objet de stratégie de groupe.

-   Pour archiver un objet de stratégie de groupe par défaut, vous devez être un éditeur, un approbateur ou un administrateur AGPM (contrôle total). Plus précisément, vous devez disposer du contenu de la **liste** et **modifier les paramètres** ou les autorisations de l’objet de **stratégie** de groupe pour l’objet GPO. Si vous n’êtes pas un approbateur ou un administrateur AGPM (ou un autre administrateur de stratégie de groupe ayant une autorisation de **déploiement d’objets** de stratégie de groupe), vous devez être l’éditeur qui a extrait l’objet de stratégie de groupe.

-   Lors de la modification d’un objet de stratégie de groupe, toute mise à niveau de l’installation de logiciels de stratégie de groupe d’un package dans un autre objet de stratégie de groupe doit référencer l’objet de stratégie de groupe déployé et non la copie

### Références supplémentaires

-   [Modification d'un objet de stratégie de groupe](editing-a-gpo-agpm40.md)

-   Révision d’un objet de stratégie de groupe

    -   [Vérifier les paramètres de l'objet de stratégie de groupe](review-gpo-settings-agpm40.md)

    -   [Vérifier les liens objet de stratégie de groupe](review-gpo-links-agpm40.md)

    -   [Identifier les différences entre les objets de stratégie de groupe, les versions ou les modèles d'objet de stratégie de groupe](identify-differences-between-gpos-gpo-versions-or-templates-agpm40.md)

-   Déploiement d’un objet de stratégie de groupe

    -   [Demander le déploiement d'un objet de stratégie de groupe](request-deployment-of-a-gpo-agpm40.md)

    -   [Déployer un objet de stratégie de groupe](deploy-a-gpo-agpm40.md)

 

 





