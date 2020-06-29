---
title: CONFIGURE PACKAGE
description: CONFIGURE PACKAGE
author: dansimp
ms.assetid: acc7eaa8-6ada-47b9-a655-2ca2537605b9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc8b315b68349cc9834316786b0bf15d4ac3c5cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807870"
---
# CONFIGURE PACKAGE


Permet à l’utilisateur de modifier un fichier de manifeste de package, une source de package, des types de déclencheurs de chargement ou la cible de charge d’un package.

`SFTMIME CONFIGURE PACKAGE:package-name [/MANIFEST manifest-path]                 [/OVERRIDEURL url] [/AUTOLOADNEVER] [/AUTOLOADONREFRESH]                 [/AUTOLOADONLOGIN] [/AUTOLOADONLAUNCH]                 [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/LOG log-pathname | /CONSOLE | /GUI]                 [/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]`

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
<td align="left"><p>/AUTOLOADNEVER</p></td>
<td align="left"><p>Le chargement en arrière-plan est désactivé pour le package.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONREFRESH</p></td>
<td align="left"><p>Le chargement en arrière-plan est effectué après une actualisation de publication.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONLOGIN</p></td>
<td align="left"><p>Le chargement en arrière-plan est effectué lorsqu’un utilisateur se connecte.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONLAUNCH</p></td>
<td align="left"><p>Le chargement en arrière-plan est effectué après le démarrage d’une application à partir du package par un utilisateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADTARGET &lt; cible&gt;</p></td>
<td align="left"><p>Indique quelles applications du package doivent être chargées de façon automatique.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NÉANT</p></td>
<td align="left"><p>Aucun chargement automatique ne sera effectué malgré la présence d’indicateurs/AUTOLOADONxxx.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SES</p></td>
<td align="left"><p>S’il s’agit d’une opération de déclenchement du déclencheur de charge, toutes les applications du package sont chargées dans le cache, qu’elles aient été ou non démarrées.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PREVUSED</p></td>
<td align="left"><p>Si un déclencheur de chargement automatique est activé, le package se charge si une application de ce package a déjà été démarrée par un utilisateur.</p></td>
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

 

Pour la version 4.6 SP2, l’option suivante a été ajoutée.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>[/NO-UPDATE-FTA-SHORTCUT {TRUE | FALSE} {/GLOBAL}]</p></td>
<td align="left"><p>Si elle a la valeur TRUE, une valeur de Registre est créée pour le package, soit par utilisateur, soit globalement si l’indicateur/GLOBAL est spécifié.</p>
<p>Si elle est définie sur FALSe, la valeur du Registre est supprimée et les associations de types de fichier (FTA) du package sont réinstallées.</p>
<p>En l’absence de spécification, le comportement normal de FTA et de publication des raccourcis est déclenché. Si vous effectuez des opérations d’actualisation de publication ultérieures sur le client App-V 4,6 SP2, les raccourcis et FTAs pour les packages qui ont ce jeu de valeurs de registre ne seront pas modifiés, et les raccourcis et FTAs ne seront pas inscrits au démarrage du système ou à la connexion de l’utilisateur, sauf si vous réinitialisez l’indicateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Fonctionne conjointement avec l’indicateur/NO-UPDATE-FTA-SHORTCUT. Si l’indicateur/GLOBAL est présent, il indique qu’une valeur de registre sera créée pour ce package pour tous les utilisateurs. Par défaut, la valeur Registry est uniquement créée pour cet utilisateur.</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Référence de commande SFTMIME](sftmime--command-reference.md)

 

 





