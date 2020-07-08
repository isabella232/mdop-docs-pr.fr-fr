---
title: Fonctionnalités de l'onglet Contenu
description: Fonctionnalités de l'onglet Contenu
author: dansimp
ms.assetid: f1f4849d-bf94-47d5-ad81-0eee33abcaca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 081cffb7c2871d0e49abd229ec06773726483f2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807689"
---
# Fonctionnalités de l'onglet Contenu


Chacun des onglets secondaires de l’onglet **Sommaire** comporte deux sections: les**objets de stratégie de groupe** , **les groupes et les utilisateurs**.

## Section objets de stratégie de groupe


La section **objets de stratégie de groupe** affiche la liste filtrée d’objets de stratégie de groupe et identifie les attributs suivants pour chaque GPO. Vous pouvez utiliser la zone de **recherche** pour rechercher des objets de stratégie de groupe avec des attributs spécifiques. Pour plus d’informations, reportez-vous à [recherche et filtrage de la liste des objets de stratégie de groupe](search-and-filter-the-list-of-gpos.md).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attribut d’objet de stratégie de groupe</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Name</strong></p></td>
<td align="left"><p>Nom de l’objet de stratégie de groupe.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>État</strong></p></td>
<td align="left"><p>État de l’objet de stratégie de groupe sélectionné</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Modifié par</strong></p></td>
<td align="left"><p>Éditeur ayant archivé l’objet de stratégie de groupe et l’approbateur qui l’a déployé.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Changer la date</strong></p></td>
<td align="left"><p>S’il s’agit d’un objet de stratégie de groupe contrôlé, la date la plus récente à laquelle il a été archivé après sa modification ou son extraction pour être modifié. S’il s’agit d’un objet de stratégie de groupe non contrôlé, date de la dernière modification.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Comment</strong></p></td>
<td align="left"><p>Commentaire entré par la personne qui a archivé ou déployé un objet de stratégie de groupe au moment de sa modification. Utile pour identifier les spécificités de la version dans le cas où il est nécessaire de revenir à une version antérieure.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Version de l’ordinateur</strong></p></td>
<td align="left"><p>Version générée automatiquement de la partie configuration de l’ordinateur de l’objet de stratégie de groupe.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Version utilisateur</strong></p></td>
<td align="left"><p>Version générée automatiquement de la partie de configuration utilisateur de l’objet de stratégie de groupe.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>État de l’objet GPO</strong></p></td>
<td align="left"><p>La configuration de l’ordinateur et la configuration de l’utilisateur peuvent être gérées séparément. L’état de l’objet de stratégie de groupe indique quelles parties de l’objet de stratégie de groupe sont activées.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Filtre WMI</strong></p></td>
<td align="left"><p>Afficher les filtres WMI appliqués à cet objet GPO. Les filtres WMI sont gérés dans le <strong> dossier filtres WMI </strong> pour le domaine dans l’arborescence de la console GPMC.</p></td>
</tr>
</tbody>
</table>

 

## Section groupes et utilisateurs


Lorsqu’un objet de stratégie de groupe est sélectionné, la section **groupes et utilisateurs** affiche une liste des groupes et des utilisateurs ayant accès à cet objet. Les autorisations et l’héritage autorisés sont affichés pour chaque groupe ou utilisateur. Un administrateur AGPM peut configurer les autorisations à l’aide de rôles AGPM standard (éditeur, approbateur, réviseur et administrateur AGPM) ou d’une combinaison personnalisée d’autorisations.

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
<td align="left"><p>Ajoutez une nouvelle entrée au descripteur de sécurité. Tout utilisateur ou groupe dans Active Directory peut être ajouté.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Supprimer</strong></p></td>
<td align="left"><p>Supprimer l’entrée sélectionnée de la liste de contrôle d’accès.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Propriétés</strong></p></td>
<td align="left"><p>Afficher les propriétés de l’objet sélectionné. La page Propriétés est la même que celle affichée pour un objet dans <strong> utilisateurs et ordinateurs Active Directory </strong> .</p></td>
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

-   [Onglet Contenu](contents-tab-agpm40.md)

 

 





