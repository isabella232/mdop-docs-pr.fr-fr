---
title: ADD PACKAGE
description: ADD PACKAGE
author: dansimp
ms.assetid: aa83928d-a234-4395-831e-2a7ef786ff53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 925349ce5bdf041b6a8768b5413692966e1cfc1e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809330"
---
# ADD PACKAGE


Ajoute un enregistrement de package. Si le package existe déjà, cette commande met à jour la configuration du package existant.

`SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                 [/OVERRIDEURL url [/AUTOLOADONREFRESH] [/AUTOLOADONLOGIN]                 [/AUTOLOADONLAUNCH] [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>PACKAGE: &lt; nom du package&gt;</p></td>
<td align="left"><p>Nom convivial et visible par l’utilisateur pour le package.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Fichier/MANIFEST-chemin&gt;</p></td>
<td align="left"><p>Chemin d’accès du fichier manifeste qui recense les applications incluses dans le package et toutes les informations de publication.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;URL/OVERRIDEURL&gt;</p></td>
<td align="left"><p>Emplacement du fichier SFT du package.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONREFRESH</p></td>
<td align="left"><p>Le chargement en arrière-plan est effectué après une actualisation de publication.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONLOGIN</p></td>
<td align="left"><p>Le chargement en arrière-plan est effectué lorsqu’un utilisateur se connecte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONLAUNCH</p></td>
<td align="left"><p>Le chargement en arrière-plan est effectué après le démarrage d’une application à partir du package par un utilisateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADTARGET cible</p></td>
<td align="left"><p>Indique quelles applications du package doivent être chargées de façon automatique.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NÉANT</p></td>
<td align="left"><p>Aucun chargement automatique ne sera effectué, malgré la présence d’indicateurs/AUTOLOADONxxx.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SES</p></td>
<td align="left"><p>Dans le cas contraire, toutes les applications du package sont chargées dans le cache, qu’elles aient été ou non déjà démarrées.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PREVUSED</p></td>
<td align="left"><p>Si un déclencheur de chargement automatique est activé, le package se charge si une application de ce package a déjà été démarrée par un utilisateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Le cas échéant, le package est disponible pour tous les utilisateurs de cet ordinateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GUI</p></td>
<td align="left"><p>Si ce paramètre est spécifié, la sortie est présentée dans une boîte de dialogue Windows.</p></td>
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

 

## Rubriques connexes


[Référence de commande SFTMIME](sftmime--command-reference.md)

 

 





