---
title: Commandes d'objet de stratégie de groupe contrôlé
description: Commandes d'objet de stratégie de groupe contrôlé
author: dansimp
ms.assetid: 370d3db9-4efc-4799-983d-e29ba5f32b07
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 65e9d06beb4c36762e845e452bab497a8d3da747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808578"
---
# Commandes d'objet de stratégie de groupe contrôlé


Onglet **contrôlé** :

-   Affiche une liste des objets de stratégie de groupe gérés par Advanced Group Policy Management (AGPM).

-   Fournit un menu contextuel contenant des commandes pour gérer les objets de stratégie de groupe et afficher l’historique et les rapports pour les objets de stratégie de groupe.

-   Affiche la liste des groupes et des utilisateurs qui ont l’autorisation d’accéder à un objet de stratégie de groupe sélectionné.

Lorsque vous cliquez avec le bouton droit sur la liste d' **objets de stratégie de groupe** dans cet onglet, un menu contextuel s’affiche. Ce menu inclut les options suivantes:

## Contrôle et historique


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Commande</th>
<th align="left">Effet</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Nouvel objet de stratégie de groupe contrôlé</strong></p></td>
<td align="left"><p>Créez un nouvel objet de stratégie de groupe avec le contrôle de modification géré via AGPM et déployez-le dans l’environnement de production du domaine. Si vous n’êtes pas autorisé à créer un objet de stratégie de groupe, vous êtes invité à le faire. (Cette option s’affiche si aucun objet GPO n’est sélectionné lorsque vous cliquez avec le bouton droit dans la <strong> Liste d’objets de stratégie de groupe </strong> .)</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Historique</strong></p></td>
<td align="left"><p>Ouvrir une fenêtre répertoriant toutes les versions de l’objet de stratégie de groupe sélectionné enregistrées dans l’archive. À partir de l’historique, vous pouvez obtenir un rapport sur les paramètres d’un objet de stratégie de groupe, comparer deux versions d’un objet de stratégie de groupe, comparer un objet GPO à un modèle, ou restaurer une version antérieure d’un objet de stratégie de groupe.</p></td>
</tr>
</tbody>
</table>

 

## Rapports


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Commande</th>
<th align="left">Effet</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Paramètres</strong></p></td>
<td align="left"><p>Générer un rapport HTML ou XML affichant les paramètres de l’objet de stratégie de groupe sélectionné ou afficher les liens vers les objets ou objets de stratégie de groupe sélectionnés à partir des unités d’organisation, au moment de la dernière vérification, de l’importation ou de l’archivage des objets de stratégie de groupe.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Diffère</strong></p></td>
<td align="left"><p>Générer un rapport HTML ou XML comparant les paramètres de deux objets de stratégie de groupe sélectionnés ou dans l’objet de stratégie de groupe sélectionné et un modèle.</p></td>
</tr>
</tbody>
</table>

 

## Édition


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Commande</th>
<th align="left">Effet</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Edit</strong></p></td>
<td align="left"><p>Ouvrir la <strong> fenêtre de l’éditeur de gestion des stratégies </strong> de groupe pour modifier l’objet de stratégie de groupe sélectionné</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Vérifier</strong></p></td>
<td align="left"><p>Obtenez une copie de l’objet de stratégie de groupe sélectionné dans l’Archive pour l’édition en mode hors connexion et interdisez à quiconque de modifier l’objet de stratégie de groupe jusqu’à ce qu’il soit réintégré dans l’archive. Extraire peut être substitué par un administrateur AGPM (contrôle total).</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Date d'arrivée</strong></p></td>
<td align="left"><p>Vérifier la version modifiée de l’objet de stratégie de groupe sélectionné dans l’archive, de sorte que d’autres éditeurs autorisés puissent y apporter des modifications ou qu’un approbateur puisse déployer l’objet GPO dans l’environnement de production du domaine.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Annuler l’extraction</strong></p></td>
<td align="left"><p>Renvoi d’un objet de stratégie de groupe extraits de l’archive sans modification.</p></td>
</tr>
</tbody>
</table>

 

## Gestion des versions


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Commande</th>
<th align="left">Effet</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Importation à partir de la production</strong></p></td>
<td align="left"><p>Pour l’objet de stratégie de groupe sélectionné, copiez la version dans l’environnement de production du domaine dans l’archive.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Importer à partir d’un fichier</strong></p></td>
<td align="left"><p>Remplacer les paramètres de stratégie de l’objet de stratégie de groupe sélectionné et extrait par ceux d’un fichier de sauvegarde d’objet GPO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Delete</strong></p></td>
<td align="left"><p>Déplacer l’objet de stratégie de groupe sélectionné vers la corbeille et indiquer si vous souhaitez conserver la version déployée (le cas échéant) en production ou supprimer la version déployée en plus de la version dans l’archive. Si vous n’êtes pas autorisé à supprimer un objet de stratégie de groupe, vous êtes invité à le faire.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Déployer</strong></p></td>
<td align="left"><p>Déplacer l’objet de stratégie de groupe sélectionné archivé dans l’archive dans l’environnement de production du domaine. Le rendez-vous actif sur le réseau et écrase la version précédemment active de l’objet de stratégie de groupe s’il existait. Si vous n’êtes pas autorisé à déployer un objet de stratégie de groupe, vous serez invité à le faire.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Exporter vers</strong></p></td>
<td align="left"><p>Enregistrez l’objet de stratégie de groupe sélectionné dans un fichier de sauvegarde pour pouvoir le copier vers un autre domaine.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Label</strong></p></td>
<td align="left"><p>Marquer l’objet de stratégie de groupe sélectionné avec une étiquette descriptive (par exemple, &quot; bon &quot; ) et un commentaire de conservation des enregistrements. Les étiquettes apparaissent dans <strong> la </strong> colonne État et les commentaires dans la <strong> </strong> colonne commentaire de la <strong> </strong> fenêtre historique. Ils vous permettent d’identifier les versions antérieures d’un objet de stratégie de groupe pour pouvoir revenir en cas de problème.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Rename</strong></p></td>
<td align="left"><p>Changer le nom de l’objet de stratégie de groupe sélectionné. Si l’objet GPO a déjà été déployé, il est mis à jour dans l’environnement de production du domaine lorsque celui-ci est redéployé.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Enregistrer en tant que modèle</strong></p></td>
<td align="left"><p>Créer un nouveau modèle basé sur les paramètres de l’objet de stratégie de groupe sélectionné.</p></td>
</tr>
</tbody>
</table>

 

## Divers


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Commande</th>
<th align="left">Effet</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Actualiser</strong></p></td>
<td align="left"><p>Mettez à jour l’affichage de la console de gestion des stratégies de groupe (GPMC) pour incorporer les modifications. Certaines modifications ne sont pas visibles tant que l’affichage n’est pas actualisé.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Help</strong></p></td>
<td align="left"><p>Afficher l’aide d’AGPM.</p></td>
</tr>
</tbody>
</table>

 

### Références supplémentaires

-   [Onglet Contenu](contents-tab-agpm40.md)

-   [Exécution de tâches d'éditeur](performing-editor-tasks-agpm40.md)

-   [Exécution de tâches d'approbateur](performing-approver-tasks-agpm40.md)

-   [Exécution de tâches de réviseur](performing-reviewer-tasks-agpm40.md)

 

 





