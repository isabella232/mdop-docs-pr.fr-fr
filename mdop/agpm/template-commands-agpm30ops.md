---
title: Commandes des modèles
description: Commandes des modèles
author: dansimp
ms.assetid: 2ec11b3f-0c5c-4788-97bd-bd4bf64ba51a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7de90780caa1eb938f78597a760723f89e2e55ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808205"
---
# Commandes des modèles


Onglet **modèles** :

-   Affiche la liste des modèles disponibles que vous pouvez utiliser pour créer des objets de stratégie de groupe.

-   Fournit un menu contextuel contenant des commandes pour la création d’un objet de stratégie de groupe en fonction d’un modèle sélectionné, la gestion des modèles et l’affichage de rapports pour les modèles.

-   Affiche la liste des groupes et des utilisateurs autorisés à accéder à un modèle sélectionné.

Dans la mesure où un modèle ne peut pas être modifié, les modèles n’ont pas d’historique. Toutefois, comme toute version d’un objet de stratégie de groupe, les paramètres d’un modèle peuvent être affichés à l’aide d’un rapport de paramètres ou d’un autre objet de stratégie de groupe avec un rapport de différences.

**Remarques**  Un modèle est une version statique non modifiable d’un objet de stratégie de groupe à utiliser comme point de départ pour créer de nouveaux objets de stratégie de groupe.

 

Lorsque vous cliquez avec le bouton droit sur la liste d' **objets de stratégie de groupe** dans cet onglet, un menu contextuel s’affiche, dont les options suivantes s’appliquent.

## Contrôle


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
<td align="left"><p>Créer un nouvel objet GPO en fonction du modèle sélectionné. L’option de déploiement du nouvel objet de stratégie de groupe dans l’environnement de production est fournie. Si vous n’êtes pas autorisé à créer un objet de stratégie de groupe, vous serez invité à le faire. (Cette option s’affiche si aucun objet GPO n’est sélectionné lorsque vous cliquez avec le bouton droit dans la <strong> Liste d’objets de stratégie de groupe </strong> .)</p></td>
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
<td align="left"><p>Générer un rapport HTML ou XML affichant les paramètres dans l’objet de stratégie de groupe sélectionné.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Diffère</strong></p></td>
<td align="left"><p>Générer un rapport HTML ou XML comparant les paramètres de deux modèles d’objets de stratégie de groupe sélectionnés.</p></td>
</tr>
</tbody>
</table>

 

## Gestion des modèles


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
<td align="left"><p><strong>Définir par défaut</strong></p></td>
<td align="left"><p>Définissez le modèle sélectionné comme modèle par défaut à utiliser automatiquement lors de la création d’un objet de stratégie de groupe.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Delete</strong></p></td>
<td align="left"><p>Déplacer le modèle sélectionné vers la <strong> Corbeille </strong> . Si vous n’êtes pas autorisé à supprimer un objet de stratégie de groupe, vous serez invité à le faire.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Rename</strong></p></td>
<td align="left"><p>Changer le nom du modèle sélectionné.</p></td>
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
<td align="left"><p>Mettez à jour l’affichage de la console de gestion des stratégies de groupe pour incorporer les modifications. Certaines modifications ne sont pas visibles tant que l’affichage n’est pas actualisé.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Help</strong></p></td>
<td align="left"><p>Afficher l’aide pour la gestion avancée des stratégies de groupe (AGPM).</p></td>
</tr>
</tbody>
</table>

 

### Références supplémentaires

-   [Onglet Contenu](contents-tab-agpm30ops.md)

-   [Exécution de tâches d'éditeur](performing-editor-tasks-agpm30ops.md)

-   [Exécution de tâches de réviseur](performing-reviewer-tasks-agpm30ops.md)

 

 





