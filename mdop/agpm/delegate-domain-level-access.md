---
title: Accès au niveau du domaine de délégué
description: Accès au niveau du domaine de délégué
author: dansimp
ms.assetid: 64c8e773-38cc-4991-9ed2-5a801094d06e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7eb4c33e60b0d995e45fca6c9e91a26c30dd4a7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808530"
---
# Accès au niveau du domaine de délégué


Configurez la délégation pour votre environnement de sorte que les administrateurs de stratégie de groupe disposent de l’accès approprié et contrôlent les objets de stratégie de groupe. Il existe des autorisations de base que vous pouvez appliquer pour rendre plus efficaces le fonctionnement de la gestion de la stratégie de groupe avancée. Vous pouvez accorder des autorisations d’une manière qui répond aux besoins de votre organisation.

Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour déléguer l’accès de sorte que les utilisateurs et les groupes disposent des autorisations appropriées pour tous les objets de stratégie de groupe dans un domaine**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Cliquez sur l’onglet **délégation de domaine** , puis cliquez sur le bouton **avancé** .

3.  Dans la boîte de dialogue **autorisations** , activez la case à cocher de chaque rôle à attribuer à une personne, puis cliquez sur le bouton **avancé** .

    **Remarques**  Éditeur et approbateur incluent les autorisations de relecteur.

     

4.  Dans la boîte de dialogue **paramètres de sécurité avancés** , sélectionnez un administrateur de stratégie de groupe, puis cliquez sur **modifier**.

5.  Pour **appliquer**à, sélectionnez **cet objet et les objets imbriqués**, configurez des autorisations spéciales au-delà des rôles AGPM standard, puis cliquez sur **OK** dans la boîte de dialogue **entrée** d' **autorisation** .

6.  Dans la boîte de dialogue **paramètres de sécurité avancés** , cliquez sur **OK**.

7.  Dans la boîte de dialogue **autorisations** , cliquez sur **OK**.

### Autres éléments à prendre en considération

-   Par défaut, vous devez être administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer des autorisations de modification de la **sécurité** pour le domaine.

-   Pour déléguer l’accès en lecture aux administrateurs de stratégie de groupe qui utilisent AGPM, vous devez leur attribuer le contenu de la **liste** et les autorisations de **paramètres de lecture** . Cela leur permet d’afficher des objets de stratégie de groupe dans l’onglet **contenu** d’AGPM. Définissez l’autorisation à appliquer à **cet objet et aux objets imbriqués**. D’autres autorisations doivent être déléguées explicitement.

-   Les éditeurs doivent disposer d’une autorisation de **lecture** pour la copie déployée d’un objet de stratégie de groupe, afin de pouvoir tirer parti de l’installation de logiciels de stratégie de groupe.

-   L’appartenance au groupe de propriétaires de la stratégie de groupe doit être restreinte afin qu’elle ne soit pas utilisée pour contourner la gestion d’accès d’AGPM aux objets de stratégie de groupe. (Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)

### Références supplémentaires

-   [Exécution de tâches d'administrateur AGPM](performing-agpm-administrator-tasks.md)

 

 





