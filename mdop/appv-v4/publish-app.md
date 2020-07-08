---
title: PUBLISH APP
description: PUBLISH APP
author: dansimp
ms.assetid: f25f06a8-ca23-435b-a0c2-16a5f39b6b97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2ccb19255786ee47a8356feef14be1c4d9b4fb2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806458"
---
# PUBLISH APP


Publie le raccourci d’une application dans le menu Démarrer, le bureau ou un autre emplacement spécifié de l’utilisateur.

`SFTMIME PUBLISH APP:application                 {/DESKTOP | /START | /TARGET target-path} [/ICON icon-pathname]                 [/DISPLAY display-name] [/ARGS command-args...]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>APPLICATION: &lt; application&gt;</p></td>
<td align="left"><p>Nom et version (facultatif) de l’application.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/DESKTOP</p></td>
<td align="left"><p>Publie un raccourci vers le Bureau de l’utilisateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/START</p></td>
<td align="left"><p>Publie un raccourci vers le dossier applications de virtualisation des applications dans le dossier programmes du menu Démarrer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/TARGET &lt; target-Path&gt;</p></td>
<td align="left"><p>Le chemin d’accès absolu dans lequel le raccourci doit être publié.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Icône/Icon-chemin&gt;</p></td>
<td align="left"><p>Path ou URL du fichier d’icône.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Nom d’affichage de/Display&gt;</p></td>
<td align="left"><p>Nom d’affichage pour le raccourci.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Commande/args&gt;</p></td>
<td align="left"><p>Paramètres à transmettre à l’application.</p></td>
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

 

 





