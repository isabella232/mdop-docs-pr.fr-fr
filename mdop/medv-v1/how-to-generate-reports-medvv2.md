---
title: Comment générer des rapports
description: Comment générer des rapports
author: dansimp
ms.assetid: 9f8ba28e-1993-4c11-a28a-493718051e5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 930b7061d3e5e2fb9951d45b1422915836cbc00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812089"
---
# Comment générer des rapports


Les types de rapports suivants peuvent être créés par les administrateurs dans MED-V:

-   [État](#bkmk-generatingastatusreport): utilisez le rapport d’État pour passer en revue l’état actuel de tous les utilisateurs actifs et de tous les espaces de travail MED-V de chaque utilisateur sur la base d’une période de temps définie. Cela inclut l’affichage d’ordinateurs actuellement connectés au serveur ou, s’ils ne sont pas connectés, la date et l’heure de la dernière connexion au serveur, l’état de chaque ordinateur et d’autres informations pertinentes.

-   [Journal d’activité](#bkmk-generatinganactivitylogreport): ce rapport permet de passer en revue les événements provenant d’un hôte ou d’un utilisateur spécifique dans une plage de dates définie.

-   [Journal des erreurs](#bkmk-generatinganerrorlogreport): ce rapport vous permet d’afficher les erreurs provenant d’un hôte ou d’un utilisateur spécifique dans une plage de dates définie.

Les résultats du rapport peuvent être triés par n’importe quelle colonne en cliquant sur le nom de colonne approprié.

Vous pouvez regrouper les résultats d’un rapport en faisant glisser un en-tête de colonne vers le haut de l’État. Faites glisser plusieurs en-têtes de colonnes pour regrouper une colonne après l’autre.

## <a href="" id="bkmk-generatingastatusreport"></a>Génération d’un rapport d’État


**Pour générer un rapport d’État**

1.  Cliquez sur le bouton gestion des **rapports** .

2.  Dans le module **rapports** , dans le menu **types de rapports** , sélectionnez **statut**, puis cliquez sur **générer**.

    La boîte de dialogue Paramètres du rapport s’affiche.

3.  Dans la boîte de dialogue **paramètres du rapport** , dans le champ **nombre de jours** , entrez un nombre ou utilisez les flèches pour sélectionner le nombre de jours à inclure dans le rapport d’État, puis cliquez sur **OK**.

    Un rapport d’État est généré. Les paramètres du rapport sont définis dans le tableau suivant.

**Propriétés d’espace de travail MED-V du client**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriété</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Durée</p></td>
<td align="left"><p>Date et heure de l’événement.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Par défaut, les événements s’affichent dans l’ordre décroissant de dates. Néanmoins, il peut être modifié en cliquant sur la colonne heure de réception.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Nom d’utilisateur</p></td>
<td align="left"><p>Utilisateur qui a déclenché l’événement.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si l’événement s’est produit avant la connexion de l’utilisateur, le nom d’utilisateur est système.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Nom d’hôte</p></td>
<td align="left"><p>Nom de l’ordinateur hôte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nom de l’espace de travail</p></td>
<td align="left"><p>Nom de l’espace de travail MED-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espace de travail nom de l’ordinateur</p></td>
<td align="left"><p>Nom de l’ordinateur sur lequel l’espace de travail MED-V est en cours d’exécution.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Online</p></td>
<td align="left"><p>État actuel de l’ordinateur client:</p>
<ul>
<li><p><strong>Ne</strong></p></li>
<li><p><strong>Démarré à &lt; la date et heure de démarrage de l’espace de travail&gt;</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Version du client</p></td>
<td align="left"><p>Numéro de version du client.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Version de la stratégie</p></td>
<td align="left"><p>Version de stratégie utilisée actuellement par l’espace de travail MED-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nom de l’image</p></td>
<td align="left"><p>Nom de l’image.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Version d’image</p></td>
<td align="left"><p>Version d’image utilisée actuellement par l’espace de travail MED-V.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>La version de l’espace de travail MED-V peut être inconnue s’il n’a pas encore été téléchargé sur un ordinateur.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganactivitylogreport"></a>Génération d’un rapport du journal d’activité


**Pour générer un rapport du journal d’activité**

1.  Cliquez sur le bouton gestion des **rapports** .

    Le module rapports apparaît.

2.  Dans le module **rapports** , dans le menu **types de rapports** , sélectionnez journal d' **activité**, puis cliquez sur **générer**.

3.  Dans la boîte de dialogue **paramètres du rapport** , configurez un ou plusieurs des paramètres suivants:

    -   **Nombre de jours**: le nombre de jours à afficher dans l’État.

    -   **Nom d’utilisateur contient**: tout événement pour lequel le nom d’utilisateur contient le texte entré est inclus dans le rapport.

    -   **Nom d’hôte contient**: tout événement pour lequel le nom d’hôte contient le texte entré est inclus dans le rapport.

4.  Cliquez sur **OK**.

    Un rapport est généré avec les événements et les dates sélectionnés. Les paramètres du rapport sont définis dans le tableau suivant.

**Propriétés du rapport du journal d’activité**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriété</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ID d’événement</p></td>
<td align="left"><p>ID de l’événement.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gravité</p></td>
<td align="left"><p><strong>Informations, erreur, avertissement</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Catégorie</p></td>
<td align="left"><p>Module référencé par le rapport.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Description</p></td>
<td align="left"><p>Description de l’événement.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Temps reçu</p></td>
<td align="left"><p>Date et heure de réception de l’événement sur le serveur.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si le client est en mode hors connexion, le serveur reçoit les rapports lorsque le client est connecté.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Remarque</strong><br/><p>Par défaut, les événements s’affichent dans l’ordre décroissant de dates. Néanmoins, il peut être modifié en cliquant sur la <strong> colonne heure de réception </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Temps client</p></td>
<td align="left"><p>Date et heure auxquelles l’événement s’est produit en fonction de l’horloge du client.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nom d’hôte</p></td>
<td align="left"><p>Nom de l’ordinateur hôte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nom d’utilisateur</p></td>
<td align="left"><p>Utilisateur qui a déclenché l’événement.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nom de l’espace de travail</p></td>
<td align="left"><p>Nom de l’espace de travail MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Espace de travail nom de l’ordinateur</p></td>
<td align="left"><p>Nom de l’ordinateur sur lequel l’espace de travail MED-V est en cours d’exécution.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganerrorlogreport"></a>Génération d’un rapport du journal des erreurs


**Pour générer un rapport du journal des erreurs**

1.  Cliquez sur le bouton gestion des **rapports** .

2.  Dans le module **rapports** , dans le menu **types de rapports** , sélectionnez journal des **Erreurs**, puis cliquez sur **générer**.

3.  Dans la boîte de dialogue **paramètres du rapport** , configurez un ou plusieurs des paramètres suivants:

    -   **Nombre de jours**: le nombre de jours à afficher dans l’État.

    -   **Nom d’utilisateur contient**: tout événement pour lequel le nom d’utilisateur contient le texte entré est inclus dans le rapport.

    -   **Nom d’hôte contient**: tout événement pour lequel le nom d’hôte contient le texte entré est inclus dans le rapport.

4.  Cliquez sur **OK**.

    Un rapport est généré avec les événements et les dates sélectionnés. Les paramètres du rapport sont définis dans le tableau suivant.

**Propriétés du rapport du journal des erreurs**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriété</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ID d’événement</p></td>
<td align="left"><p>ID de l’événement.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Catégorie</p></td>
<td align="left"><p>Module référencé par le rapport.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Description</p></td>
<td align="left"><p>Description de l’événement.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Temps reçu</p></td>
<td align="left"><p>Date et heure de réception de l’événement sur le serveur.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si le client est en mode hors connexion, le serveur reçoit les rapports lorsque le client est connecté.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Remarque</strong><br/><p>Par défaut, les événements s’affichent dans l’ordre décroissant de dates. Néanmoins, il peut être modifié en cliquant sur la <strong> colonne heure de réception </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Temps client</p></td>
<td align="left"><p>Date et heure auxquelles l’événement s’est produit en fonction de l’horloge du client.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nom d’hôte</p></td>
<td align="left"><p>Nom de l’ordinateur hôte.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nom d’utilisateur</p></td>
<td align="left"><p>Utilisateur qui a déclenché l’événement.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nom de l’espace de travail</p></td>
<td align="left"><p>Nom de l’espace de travail MED-V.</p></td>
</tr>
</tbody>
</table>











