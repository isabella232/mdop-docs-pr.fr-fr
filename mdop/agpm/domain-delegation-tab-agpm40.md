---
title: Onglet Délégation de domaine
description: Onglet Délégation de domaine
author: dansimp
ms.assetid: 5be5841e-92fb-4af6-aa68-0ae50f8d5141
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c5f3b5c3b7d8799b383ab48870fcccad0b0c3f73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807586"
---
# Onglet Délégation de domaine


L’onglet **délégation de domaine** du volet de contrôle des **modifications** fournit une liste des administrateurs de stratégie de groupe qui disposent d’un accès au niveau du domaine pour l’archive et indiquent les rôles de chacun d’eux. Par ailleurs, cet onglet permet aux administrateurs d’AGPM (contrôle total) de configurer des autorisations au niveau du domaine pour les éditeurs, approbateurs, réviseurs et autres administrateurs d’AGPM. Il existe deux sections sous l’onglet **délégation de domaine** (configuration de la notification par courrier électronique et de la délégation basée sur le rôle pour une gestion avancée de la stratégie de groupe) au niveau du domaine.

## Configuration de la notification par courrier électronique


La section notification par courrier électronique de cet onglet identifie les approbateurs qui recevront une notification lorsque les opérations seront en attente dans AGPM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paramètre</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>À partir de l’adresse de messagerie</strong></p></td>
<td align="left"><p>Alias AGPM à partir duquel la notification est envoyée aux approbateurs. Dans un environnement à plusieurs domaines, il peut s’agir du même alias dans l’environnement ou d’un alias différent pour chaque domaine.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>À l’adresse de messagerie</strong></p></td>
<td align="left"><p>Liste séparée par des virgules des adresses de courrier des approbateurs auprès desquels la notification doit être envoyée</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Serveur SMTP</strong></p></td>
<td align="left"><p>Nom du serveur de messagerie, par exemple mail.contoso.com</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nom d’utilisateur</strong></p></td>
<td align="left"><p>Utilisateur ayant accès au serveur SMTP</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Mot de passe</strong></p></td>
<td align="left"><p>Mot de passe de l’utilisateur pour l’authentification auprès du serveur SMTP</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Confirmer le mot de passe</strong></p></td>
<td align="left"><p>Confirmer le mot de passe d’un utilisateur</p></td>
</tr>
</tbody>
</table>

 

## Délégation basée sur le rôle au niveau du domaine


La section délégation basée sur le rôle de cet onglet s’affiche, et permet à un administrateur AGPM de déléguer les autorisations autorisées, refusées et héritées pour chaque groupe et utilisateur sur le domaine avec accès à l’archive. Un administrateur AGPM peut configurer les autorisations à l’échelle d’un domaine à l’aide de rôles AGPM standard (éditeur, approbateur, réviseur et administrateur AGPM) ou d’une combinaison personnalisée d’autorisations pour chaque administrateur de stratégie de groupe.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Bouton</th>
<th align="left">Effet</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Add</strong></p></td>
<td align="left"><p>Ajoutez une nouvelle entrée au descripteur de sécurité. Les administrateurs de stratégie de groupe peuvent ajouter des utilisateurs ou des groupes dans Active Directory.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Supprimer</strong></p></td>
<td align="left"><p>Supprimer les administrateurs de stratégie de groupe sélectionnés de la liste de contrôle d’accès.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Propriétés</strong></p></td>
<td align="left"><p>Afficher les propriétés pour les administrateurs de stratégie de groupe sélectionnés.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Avancé</strong></p></td>
<td align="left"><p>Ouvrez l' <strong> éditeur de liste de contrôle d’accès </strong> .</p></td>
</tr>
</tbody>
</table>

 

### Autres éléments à prendre en considération

-   Pour plus d’informations sur les rôles et les autorisations liées à des tâches spécifiques, voir les tâches d' [exécution des tâches d’administration d’AGPM](performing-agpm-administrator-tasks-agpm40.md), exécution de tâches d' [éditeur](performing-editor-tasks-agpm40.md), [exécution des tâches approbateurs](performing-approver-tasks-agpm40.md)et [exécution des tâches de relecteur](performing-reviewer-tasks-agpm40.md).

### Références supplémentaires

-   [Interface utilisateur: gestion avancée des stratégies de groupe](user-interface-advanced-group-policy-management-agpm40.md)

-   [Exécution de tâches d'administrateur AGPM](performing-agpm-administrator-tasks-agpm40.md)

 

 





