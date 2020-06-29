---
title: ADD TYPE
description: ADD TYPE
author: dansimp
ms.assetid: 8f1d3978-9977-4851-9f46-fee6aefa3535
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d2dcfb24a32dc733aa91b5534e0011090ef12b9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809323"
---
# ADD TYPE


Ajoute l’Association de type de fichier spécifiée.

`SFTMIME ADD TYPE:file-extension /APP application [/ICON icon-pathname]                 [/DESCRIPTION type-desc] [/CONTENT-TYPE content-type] [/GLOBAL]                 [/PERCEIVED-TYPE perceived-type] [/PROGID progid]                 [/CONFIRMOPEN {YES|NO}] [/SHOWEXT {YES|NO}]                 [/NEWMENU {YES|NO}]  [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>TYPE: &lt; fichier-extension&gt;</p></td>
<td align="left"><p>L’extension de nom de fichier qui sera associée à l’application spécifiée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Application/App&gt;</p></td>
<td align="left"><p>Nom et version (facultatif) de l’application.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Icône/Icon-chemin&gt;</p></td>
<td align="left"><p>Path ou URL du fichier d’icône.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Type de type/Description-DESC&gt;</p></td>
<td align="left"><p>Nom convivial du type de fichier. Par défaut, il s’agit du &quot; fichier d’extension.&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Type de contenu/Content-type&gt;</p></td>
<td align="left"><p>Le type de contenu du fichier. Utilise par défaut la valeur &quot; application/Softricity-extension.&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Le cas échéant, le package est disponible pour tous les utilisateurs de cet ordinateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/PERCEIVED-TYPE &lt; perçu-type&gt;</p></td>
<td align="left"><p>Type perçu du fichier. Valeur par défaut est aucune.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;ProgID/ProgID&gt;</p></td>
<td align="left"><p>Identificateur programmatique pour le type de fichier. Utilise par défaut la valeur App Virt. extension. file.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONFIRMOPEN</p></td>
<td align="left"><p>Indique si les utilisateurs qui téléchargent un fichier de ce type doivent être invités à ouvrir ou enregistrer le fichier. Valeur par défaut: Oui.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SHOWEXT</p></td>
<td align="left"><p>Indique si l’extension du fichier doit toujours être affichée, même si l’utilisateur a demandé que toutes les extensions soient masquées. Par défaut, la valeur est non.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/NEWMENU</p></td>
<td align="left"><p>Indique si une entrée doit être ajoutée au menu nouveau de l’environnement <strong> </strong> . Par défaut, la valeur est non.</p></td>
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

 

 





