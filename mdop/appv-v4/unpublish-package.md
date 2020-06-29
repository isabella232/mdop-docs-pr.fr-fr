---
title: UNPUBLISH PACKAGE
description: UNPUBLISH PACKAGE
author: dansimp
ms.assetid: 1651427c-72a5-4701-bb57-71e14a7a3803
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7704fb3ed03be4864a837767d9e890d28b63f175
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806185"
---
# UNPUBLISH PACKAGE


Vous permet de supprimer les raccourcis et les types de fichiers pour l’ensemble d’un package.

`SFTMIME UNPUBLISH PACKAGE:package-name [/CLEAR] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Nom du package.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CLEAR</p></td>
<td align="left"><p>Le cas échéant, les paramètres utilisateur sont également supprimés. (Pour plus d’informations, consultez la note important plus loin dans cette rubrique.)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Le cas échéant, le package sera annulé pour tous les utilisateurs de cet ordinateur.</p></td>
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

 

**Important**  Avant d’exécuter la commande **annuler la publication** d’un package, le package doit déjà avoir été ajouté au client de virtualisation d’applications.

Pour utiliser **Global**, la publication d’un **package** doit être exécutée en tant qu’administrateur local. dans le cas contraire, seule une autorisation **ClearApp** est nécessaire.

L’utilisation de la fonction de suppression de **package** avec l’option **Global** entraîne la suppression de tous les types de fichiers globaux et raccourcis du package. **Clear** n’est pas applicable.

L’utilisation de l’option annuler la publication d’un **package** sans **Global** entraîne celle de l’utilisateur et du type de fichier pour le package et, si la valeur est définie sur **Effacer** , supprime également les paramètres d’utilisateur et arrête les chargements en arrière-plan dans le contexte de l’utilisateur

L’annulation de la publication d’un **package** fonctionne sur les applications provenant du même nom de package ou du GUID utilisé en tant qu’ID source pour l' **Ajout**, la **modification**et la publication d’un **package**.

L’annulation de la publication d’un **package** efface toujours l’ensemble des paramètres utilisateur, des raccourcis et des types de fichiers, quelle que soit l’utilisation du commutateur/Clear.

 

## Rubriques connexes


[Référence de commande SFTMIME](sftmime--command-reference.md)

 

 





