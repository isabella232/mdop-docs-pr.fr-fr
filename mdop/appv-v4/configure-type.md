---
title: CONFIGURE TYPE
description: CONFIGURE TYPE
author: dansimp
ms.assetid: 2caf9433-5449-486f-ab94-83ee8e44d7f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b70cdd1b27eba0109183f1eb9cfb42f08b3f341
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809054"
---
# CONFIGURE TYPE


Permet à l’utilisateur de modifier les paramètres d’une association de type de fichier.

`SFTMIME CONFIGURE TYPE:file-extension [/GLOBAL] [/APP application]                 [/ICON icon-pathname] [/DESCRIPTION type-desc]                 [/CONTENT-TYPE content-type] [/PERCEIVED-TYPE perceived-type]                 [/PROGID progid] [/CONFIRMOPEN {YES|NO}]                 [/SHOWEXT {YES|NO}] [/NEWMENU {YES|NO}]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Extension de nom de fichier à configurer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Application/App&gt;</p></td>
<td align="left"><p>Nom et version (facultatif) de l’application à laquelle associer ce type de fichier. Ne peut pas être spécifié avec PROGID.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Icône/Icon-chemin&gt;</p></td>
<td align="left"><p>Path ou URL du fichier d’icône.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Type de type/Description-DESC&gt;</p></td>
<td align="left"><p>Nom convivial du type de fichier.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Type de contenu/Content-type&gt;</p></td>
<td align="left"><p>Le type de contenu du fichier.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Le cas échéant, indique que l’Association qui s’applique à tous les utilisateurs doit être modifiée, et non à l’utilisateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/PERCEIVED-TYPE &lt; perçu-type&gt;</p></td>
<td align="left"><p>Type perçu du fichier.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;ProgID/ProgID&gt;</p></td>
<td align="left"><p>Indique que l’extension doit être associée à un autre type de fichier. Le type de fichier précédent n’est pas supprimé. Ne peut pas être spécifié avec l’application, l’icône, la DESCRIPTION, CONFIRMOPEN ou SHOWEXT.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONFIRMOPEN</p></td>
<td align="left"><p>Indique si les utilisateurs qui téléchargent un fichier de ce type doivent être invités à ouvrir ou enregistrer le fichier.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SHOWEXT</p></td>
<td align="left"><p>Indique si l’extension du fichier doit toujours être affichée, même si l’utilisateur a demandé que toutes les extensions soient masquées.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/NEWMENU</p></td>
<td align="left"><p>Indique si une entrée doit être ajoutée au menu nouveau de l’environnement <strong> </strong> .</p></td>
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

 

 





