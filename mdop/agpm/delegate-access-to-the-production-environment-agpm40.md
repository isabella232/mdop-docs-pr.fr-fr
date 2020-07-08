---
title: Déléguer l'accès à l'environnement de production
description: Déléguer l'accès à l'environnement de production
author: dansimp
ms.assetid: 4c670581-8c47-41ea-80eb-02846ff1ec1f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a3920a8ba5835cbbcb8a74f0af4e3ca1e1c5f43f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807622"
---
# Déléguer l'accès à l'environnement de production


Dans Advanced Group Policy Management (AGPM), vous pouvez modifier l’accès aux objets de stratégie de groupe dans l’environnement de production du domaine, en remplaçant les autorisations existantes sur ces objets. Vous pouvez configurer des autorisations au niveau du domaine pour autoriser ou empêcher les utilisateurs de modifier, de supprimer ou de modifier la sécurité des objets de stratégie de groupe dans l’environnement de production quand ils n’utilisent pas le dossier de **contrôle de modification** dans la console de gestion des stratégies de groupe (GPMC).

**Remarque**  
-   La modification de la façon dont l’accès à l’environnement de production est délégué n’a pas d’incidence sur la possibilité de lier les objets de stratégie de groupe.

-   Lorsque des objets de stratégie de groupe sont contrôlés ou déployés, l’accès pour tous les autres comptes, à l’exception de ceux portant les autorisations **lecture** et **appliquer** est supprimé

 

Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour modifier l’accès aux objets de stratégie de groupe dans l’environnement de production du domaine**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Cliquez sur l’onglet **délégation de production** .

3.  Pour ajouter des autorisations pour un utilisateur ou un groupe qui n’ont pas accès à l’environnement de production, ou pour remplacer les autorisations d’un utilisateur ou d’un groupe qui a accès:

    1.  Cliquez sur **Ajouter**, sélectionnez un utilisateur ou un groupe, puis cliquez sur **OK**.

    2.  Sélectionnez les autorisations à déléguer à un utilisateur ou à un groupe pour l’environnement de production, puis cliquez sur **OK**.

4.  Pour supprimer toutes les autorisations de l’environnement de production pour un utilisateur ou un groupe, sélectionnez l’utilisateur ou le groupe, cliquez sur **supprimer**, puis cliquez sur **OK**.

### Autres éléments à prendre en considération

-   Par défaut, vous devez être administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer des autorisations de modification de la **sécurité** pour le domaine.

-   Les autorisations pour le compte de service AGPM ne peuvent pas être modifiées sous l’onglet **délégation de production** .

-   Par défaut, les comptes suivants possèdent des autorisations pour les objets de stratégie de groupe dans l’environnement de production:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Compte</th>
    <th align="left">Autorisations par défaut pour les objets de stratégie de groupe</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>&lt;Compte de service AGPM&gt;</p></td>
    <td align="left"><p>Modifier les paramètres, supprimer ou modifier la sécurité</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Utilisateurs authentifiés</p></td>
    <td align="left"><p>Lire, appliquer</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrateurs de domaine</p></td>
    <td align="left"><p>Modifier les paramètres, supprimer ou modifier la sécurité</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrateurs d’entreprise</p></td>
    <td align="left"><p>Modifier les paramètres, supprimer ou modifier la sécurité</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Contrôleurs de domaine d’entreprise</p></td>
    <td align="left"><p>Read</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Système</p></td>
    <td align="left"><p>Modifier les paramètres, supprimer ou modifier la sécurité</p></td>
    </tr>
    </tbody>
    </table>

     

-   L’appartenance au groupe de propriétaires de la stratégie de groupe doit être restreinte, soit n’est pas utilisé pour contourner la gestion d’accès d’AGPM aux objets de stratégie de groupe. (Dans la **console de gestion des stratégies de groupe**, cliquez sur **objets de stratégie de groupe** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe, cliquez sur **délégation**, puis configurez les paramètres en fonction des besoins de votre organisation.)

### Références supplémentaires

-   [Configuration de la Gestion avancée des stratégies de groupe](configuring-advanced-group-policy-management-agpm40.md)

 

 





