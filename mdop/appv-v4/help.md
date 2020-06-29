---
title: HELP
description: HELP
author: dansimp
ms.assetid: 0ddb5f18-0c0a-45ea-b7c7-2d4749e3d35d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 395e6199529ccbe708aa7d1ac6673ea6f9494ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808771"
---
# HELP


Affiche des informations sur les différentes commandes SFTMIME qui peuvent être utilisées dans la virtualisation des applications (App-V).

## HELP


`SFTMIME [/? | /HELP [VERB:<verb>]]`

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
<td align="left"><p>/?,/HELP</p></td>
<td align="left"><p>Affiche les informations d’utilisation.</p></td>
</tr>
<tr class="even">
<td align="left"><p>verbal</p></td>
<td align="left"><p>Commande pour exécuter la commande, comme ajouter, ACTUALISer, aide ou supprimer.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>object</p></td>
<td align="left"><p>Ce à quoi s’applique la commande (par exemple, application: &quot; application par défaut).&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>paramètres</p></td>
<td align="left"><p>Paramètres facultatifs pour le verbe et l’objet spécifiés.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Sortie du journal sur le nom du chemin d’accès spécifié.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Affiche la sortie dans la fenêtre de la console active (par défaut).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GUI</p></td>
<td align="left"><p>Affiche les erreurs dans une boîte de dialogue (non valide pour les requêtes).</p></td>
</tr>
</tbody>
</table>

 

Pour la version 4.6, l’option suivante a été ajoutée.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/LOGU</p></td>
<td align="left"><p>Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié au format UNICODE.</p></td>
</tr>
</tbody>
</table>

 

Les verbes décrits dans le tableau suivant sont pris en charge.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>ADD</p></td>
<td align="left"><p>Ajoute une nouvelle application, un package, une association de type de fichier ou un serveur de publication au client App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CONFIGUR</p></td>
<td align="left"><p>Modification de la configuration d’une application, d’un package, d’une association de type de fichier ou d’un serveur de publication.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DELETE</p></td>
<td align="left"><p>Supprime les applications, packages, associations de types de fichiers ou serveurs.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ÉQUILIBRAGE</p></td>
<td align="left"><p>Charge un package dans le cache du système de fichiers.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DÉMARRAGE</p></td>
<td align="left"><p>Réinitialise vos paramètres personnels pour une application.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MISE</p></td>
<td align="left"><p>Déclenche une actualisation du serveur de publication.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PUBLI</p></td>
<td align="left"><p>Publie le raccourci d’une application dans le menu Démarrer de l’utilisateur, le bureau ou un autre emplacement spécifié, ou peut être utilisé pour publier le contenu d’un package entier.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ANNULER la publication</p></td>
<td align="left"><p>Supprime les raccourcis et types de fichiers pour l’ensemble d’un package.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REQUÊTE</p></td>
<td align="left"><p>Obtient la liste actuelle des applications, packages, associations de types de fichiers ou serveurs de publication.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SUPPRIME</p></td>
<td align="left"><p>Supprime vos paramètres personnels et les configurations de bureau d’une ou plusieurs applications.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DÉCHARGE</p></td>
<td align="left"><p>Décharge un package du cache du système de fichiers.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DÉVERROUILLE</p></td>
<td align="left"><p>Verrouille l’application spécifiée dans le cache du système de fichiers.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>EXPLOITER</p></td>
<td align="left"><p>Déverrouille l’application spécifiée dans le cache du système de fichiers.</p></td>
</tr>
</tbody>
</table>

 

Pour plus d’informations sur les actions précédentes, utilisez la commande suivante:

`SFTMIME /HELP VERB:verb`

Par exemple, la commande suivante affiche des informations pour le verbe ajouter:

`SFTMIME /HELP VERB:ADD`

## Rubriques connexes


[Référence de commande SFTMIME](sftmime--command-reference.md)

 

 





