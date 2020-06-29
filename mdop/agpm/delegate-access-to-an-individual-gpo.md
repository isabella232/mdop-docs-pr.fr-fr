---
title: Déléguer l'accès à un objet de stratégie de groupe individuel
description: Déléguer l'accès à un objet de stratégie de groupe individuel
author: dansimp
ms.assetid: b2a7d550-14bf-4b41-b6e4-2cc091eedd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5d2ae8c6ef52eae39feb67b9df42e84f523300
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807625"
---
# Déléguer l'accès à un objet de stratégie de groupe individuel


En tant qu’administrateur d’AGPM (contrôle total), vous pouvez déléguer la gestion d’un objet de stratégie de groupe contrôlé (GPO), de sorte que les groupes et les éditeurs sélectionnés puissent le modifier, les réviseurs peuvent le réviser et les approbateurs peuvent l’approuver.

Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’approbateur qui a créé l’objet de stratégie de groupe ou un compte d’utilisateur disposant des autorisations nécessaires dans la gestion avancée de la stratégie de groupe est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour déléguer la gestion d’un objet de stratégie de groupe contrôlé**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **Sommaire** du volet Détails, cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés, puis cliquez sur l’objet de stratégie de groupe à déléguer.

3.  Cliquez sur le bouton **Ajouter** , sélectionnez les utilisateurs ou les groupes auxquels vous avez accès autorisé, puis cliquez sur **OK**.

4.  Pour personnaliser les autorisations pour chaque utilisateur ou groupe, cliquez sur le bouton **avancé** sous l’onglet **Sommaire** et activez les cases à cocher autorisations de rôle pour autoriser ou refuser. (Pour un contrôle plus détaillé, cliquez sur **Options avancées** dans la boîte de dialogue **autorisations** .)

5.  Cliquez sur **appliquer**, puis sur **OK** dans la boîte de dialogue **autorisations** .

### Autres éléments à prendre en considération

-   Par défaut, vous devez être l’approbateur qui a créé ou contrôlé l’objet de stratégie de groupe ou un administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer de l’autorisation **contenu de liste** pour le domaine et modifier les autorisations de **sécurité** pour l’objet de stratégie de groupe.

-   Pour déléguer l’accès en lecture aux administrateurs de stratégie de groupe qui utilisent AGPM, vous devez leur attribuer le contenu de la **liste** et les autorisations de **paramètres de lecture** . Cela leur permet d’afficher des objets de stratégie de groupe dans l’onglet **contenu** d’AGPM. Définissez l’autorisation à appliquer à **cet objet et aux objets imbriqués**. D’autres autorisations doivent être déléguées explicitement.

-   Les éditeurs doivent disposer d’une autorisation de **lecture** pour la copie déployée d’un objet de stratégie de groupe pour tirer pleinement parti de l’installation de logiciels de stratégie de groupe.

-   L’appartenance au groupe de propriétaires de la stratégie de groupe doit être restreinte afin qu’elle ne soit pas utilisée pour contourner la gestion d’accès d’AGPM aux objets de stratégie de groupe. (Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)

### Références supplémentaires

-   [Exécution de tâches d'administrateur AGPM](performing-agpm-administrator-tasks.md)

 

 





