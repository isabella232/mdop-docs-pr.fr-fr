---
title: Fenêtre Historique
description: Fenêtre Historique
author: dansimp
ms.assetid: 114f50a4-508d-4589-b006-6cd05cffe6b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81911b5103c76e267d806fb7cd8acf55811440c9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808450"
---
# Fenêtre Historique


L’historique d’un objet de stratégie de groupe peut être affiché en double-cliquant sur un objet GPO ou en cliquant avec le bouton droit sur un objet de stratégie de groupe, puis en cliquant sur **historique**. Il est également affiché dans la **console de gestion des stratégies de groupe** (GPMC) en tant qu’onglet pour chaque GPO.

L’historique fournit un enregistrement des événements pendant la durée de vie de l’objet de stratégie de groupe sélectionné. Dans la fenêtre **historique** , vous pouvez obtenir un rapport sur les paramètres au sein d’une version de l’objet de stratégie de groupe, comparer plusieurs versions d’un objet de stratégie de groupe, ou restaurer une version précédente d’un objet de stratégie de groupe.

## Filtrage d’événements dans la fenêtre historique


Les onglets de la fenêtre **historique** permettent de filtrer les États de l’historique de l’objet de stratégie de groupe.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Eux</th>
<th align="left">Filtre</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Tous les États</strong></p></td>
<td align="left"><p>Affichez tous les États de l’historique de l’objet de stratégie de groupe.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Versions uniques</strong></p></td>
<td align="left"><p>Afficher uniquement les versions uniques de l’objet de stratégie de groupe archivé dans l’archive. La version déployée dans l’environnement de production, les raccourcis vers des versions uniques et les États d’information sont omis de cette liste.</p></td>
</tr>
</tbody>
</table>



## Informations sur l’événement


Des informations sont fournies pour chaque État de l’historique de l’objet de stratégie de groupe.

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
<td align="left"><p><strong>Changer la date</strong></p></td>
<td align="left"><p>Horodatage du moment où l’action dans la <strong> </strong> colonne État a été effectuée.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>État</strong></p></td>
<td align="left"><p>État de l’historique de l’objet de stratégie de groupe.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Modifié par</strong></p></td>
<td align="left"><p>Personne ayant archivé ou déployé l’objet de stratégie de groupe.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Comment</strong></p></td>
<td align="left"><p>Commentaire entré par la personne qui a archivé ou déployé un objet de stratégie de groupe au moment de la modification de cette version. Utile pour identifier les spécificités de la version dans le cas où il est nécessaire de revenir à une version précédente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Supprimé</strong></p></td>
<td align="left"><p>Si cette version de l’objet de stratégie de groupe peut être supprimée si le nombre de versions uniques de chaque GPO conservé dans l’archive est limité.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Vous pouvez modifier la version d’un objet de stratégie de groupe en cliquant dessus avec le bouton droit, puis en cliquant sur <strong> ne pas autoriser la suppression </strong> ou <strong> autoriser la suppression </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Version de l’ordinateur</strong></p></td>
<td align="left"><p>Version générée automatiquement de la partie configuration de l’ordinateur de l’objet de stratégie de groupe.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Version utilisateur</strong></p></td>
<td align="left"><p>Version générée automatiquement de la section Configuration utilisateur de l’objet de stratégie de groupe.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>État de l’objet GPO</strong></p></td>
<td align="left"><p>La configuration de l’ordinateur et la configuration de l’utilisateur peuvent être gérées indépendamment les uns des autres. Cet état indique les parties de l’objet GPO qui sont activées.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Filtre WMI</strong></p></td>
<td align="left"><p>Afficher les filtres WMI appliqués à cet objet GPO. Les filtres WMI sont gérés dans le <strong> dossier filtres WMI </strong> pour le domaine dans l’arborescence de la console GPMC.</p></td>
</tr>
</tbody>
</table>



## Rapports


Les boutons **paramètres** et **différences** affichent des rapports sur les paramètres de l’objet de stratégie de groupe pour la ou les versions de l’objet GPO sélectionnées. Lorsque vous cliquez avec le bouton droit sur les versions de l’objet de stratégie de groupe, vous pouvez également afficher des rapports XML.

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
<td align="left"><p><strong>Paramètres</strong></p></td>
<td align="left"><p>Générer un rapport HTML affichant les paramètres dans la version sélectionnée de l’objet de stratégie de groupe.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Diffère</strong></p></td>
<td align="left"><p>Générer un rapport HTML comparant les paramètres de plusieurs versions sélectionnées de l’objet de stratégie de groupe.</p></td>
</tr>
</tbody>
</table>



### Clé pour différencier les rapports

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Symbole</th>
<th align="left">Signification</th>
<th align="left">Couleur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>None</p></td>
<td align="left"><p>L’élément existe avec des paramètres identiques dans les deux objets de stratégie de groupe</p></td>
<td align="left"><p>Varie selon le niveau</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[#]</strong></p></td>
<td align="left"><p>L’élément existe dans les deux objets de stratégie de groupe, mais avec les paramètres modifiés</p></td>
<td align="left"><p>Bleu</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>[-]</strong></p></td>
<td align="left"><p>L’élément existe uniquement dans le premier objet GPO</p></td>
<td align="left"><p>Rouge</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[+]</strong></p></td>
<td align="left"><p>L’élément existe uniquement dans le second objet de stratégie de groupe</p></td>
<td align="left"><p>Vert</p></td>
</tr>
</tbody>
</table>



-   Pour les éléments ayant modifié des paramètres, les paramètres modifiés sont identifiés lorsque l’élément est étendu. La valeur de l’attribut dans chaque objet GPO est affichée dans l’ordre dans lequel les objets de stratégie de groupe sont affichés dans le rapport.

-   Certaines modifications apportées aux paramètres peuvent entraîner le signalement d’un élément sous la forme de deux éléments différents (un seul présent dans le premier objet de stratégie de groupe, le premier uniquement dans le second), plutôt qu’un élément modifié.

### Références supplémentaires

-   [Onglet Contenu](contents-tab-agpm30ops.md)









