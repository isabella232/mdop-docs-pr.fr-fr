---
title: PUBLISH PACKAGE
description: PUBLISH PACKAGE
author: dansimp
ms.assetid: a33e72dd-194f-4283-8e99-4584ab13de53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00b63389986f495d9405939245a50575bae453f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806457"
---
# PUBLISH PACKAGE


Publie le contenu d’un package entier.

`SFTMIME PUBLISH PACKAGE:package-name /MANIFEST manifest-path [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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

 

**Important**  Le package doit déjà avoir été ajouté au client de virtualisation d’application et le fichier manifeste est requis.

Pour utiliser le paramètre **Global** , la commande publier le package doit être exécutée en tant qu’administrateur local. dans le cas contraire, seules les autorisations **ManageTypes** et **PublishShortcut** sont nécessaires.

La publication sans le paramètre **Global** octroie aux utilisateurs l’accès aux applications du package et publie les types de fichiers et les raccourcis répertoriés dans le manifeste dans le profil de l’utilisateur.

La publication avec le paramètre **Global** ajoute les types de fichiers et les raccourcis répertoriés dans le manifeste au profil «All Users».

Si le package n’est pas global avant l’utilisation de l’appel et du paramètre **Global** , le package est alors rendu global et disponible pour tous les utilisateurs.

 

## Rubriques connexes


[Référence de commande SFTMIME](sftmime--command-reference.md)

 

 





