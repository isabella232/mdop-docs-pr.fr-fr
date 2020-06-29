---
title: Déléguer l'accès au niveau du domaine à l'archive
description: Déléguer l'accès au niveau du domaine à l'archive
author: dansimp
ms.assetid: d232069e-71d5-4b4d-b22e-bef11de1cfd4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01fbc4964493da6ba40382ac40671922eeffa30e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808534"
---
# Déléguer l'accès au niveau du domaine à l'archive


Configurez la délégation pour votre environnement de sorte que les administrateurs de stratégie de groupe aient l’accès approprié et contrôlent les objets de stratégie de groupe dans l’archive. Il existe des autorisations de base que vous pouvez appliquer pour rendre les opérations plus efficaces. Vous pouvez accorder des autorisations d’une manière qui répond aux besoins de votre organisation.

Un compte d’utilisateur disposant du rôle Administrateur AGPM (contrôle total) ou des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour déléguer l’accès de sorte que les utilisateurs et les groupes disposent des autorisations appropriées pour tous les objets de stratégie de groupe au sein d’un domaine**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Cliquez sur l’onglet **délégation de domaine** , puis configurez l’accès à tous les objets de stratégie de groupe du domaine:

    1.  Pour ajouter l’accès d’un utilisateur ou d’un groupe, cliquez sur le bouton **Ajouter** , sélectionnez l’utilisateur ou le groupe, puis cliquez sur **OK**. Dans la boîte de dialogue **Ajouter un groupe ou un utilisateur** , sélectionnez un rôle, puis cliquez sur **OK**.

    2.  Pour supprimer l’accès d’un utilisateur ou d’un groupe, sélectionnez-le, puis cliquez sur le bouton **supprimer** .

    3.  Pour modifier les rôles et autorisations délégués à un utilisateur ou à un groupe, sélectionnez cliquez sur le bouton **avancé** . Dans la boîte de dialogue **autorisations** , sélectionnez l’utilisateur ou le groupe, activez la case à cocher en regard de chaque rôle à attribuer à l’utilisateur ou au groupe, puis cliquez sur **OK**.

        **Remarques**  Éditeur et approbateur incluent les autorisations de relecteur.

         

### Autres éléments à prendre en considération

-   Par défaut, vous devez être administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer des autorisations de modification de la **sécurité** pour le domaine.

-   Pour déléguer l’accès en lecture aux administrateurs de stratégie de groupe qui utilisent AGPM, vous devez leur attribuer le contenu de la **liste** et les autorisations de **paramètres de lecture** . Cela leur permet d’afficher des objets de stratégie de groupe dans l’onglet **contenu** d’AGPM. D’autres autorisations doivent être déléguées explicitement.

-   Les éditeurs doivent disposer d’une autorisation de **lecture** pour la copie déployée d’un objet de stratégie de groupe, afin de pouvoir tirer parti de l’installation de logiciels de stratégie de groupe.

-   L’appartenance au groupe de propriétaires de la stratégie de groupe doit être restreinte, soit n’est pas utilisé pour contourner la gestion d’accès d’AGPM aux objets de stratégie de groupe. (Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)

### Références supplémentaires

-   [Gestion de l'archivage](managing-the-archive.md)

 

 





