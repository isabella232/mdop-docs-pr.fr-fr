---
title: QUERY OBJ
description: QUERY OBJ
author: dansimp
ms.assetid: 55abf0d1-c779-4172-8357-552ab010933b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328e9feb96c70080531cbbc666d8ff1b86045ba5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806426"
---
# QUERY OBJ


Renvoie une liste délimitée par des tabulations des applications actuelles, packages, associations de types de fichiers ou serveurs de publication.

`SFTMIME QUERY OBJ:{APP|PACKAGE|TYPE|SERVER} [/SHORT] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE ]`

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
<td align="left"><p>APPLI</p></td>
<td align="left"><p>Renvoie une liste d’applications.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GESTIONNAIRE</p></td>
<td align="left"><p>Renvoie une liste de packages.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TYPE</p></td>
<td align="left"><p>Renvoie une liste des associations de types de fichiers.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SERVEURS</p></td>
<td align="left"><p>Renvoie une liste de serveurs de publication.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/SHORT</p></td>
<td align="left"><p>Sans afficher les propriétés complètes de chacune d’elles, renvoie une liste de noms d’application, de packages, d’associations ou de noms de serveurs.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Pour les applications, retourne toutes les applications connues au lieu de celles auxquelles l’utilisateur actuel a accès. Pour les packages, renvoie tous les packages connus au lieu de ceux auxquels l’utilisateur actuel a accès. Pour les associations, renvoie uniquement les associations qui s’appliquent à tous les utilisateurs, et non spécifiques à l’utilisateur. Non valide pour les serveurs.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Si ce paramètre est spécifié, la sortie est enregistrée dans le nom du chemin d’accès spécifié.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Si ce paramètre est spécifié, la sortie est présentée dans la fenêtre de la console active (par défaut).</p></td>
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

 

**Remarques**  Dans la version 4,6, une nouvelle colonne a été ajoutée à la sortie de la requête SFTMIME OBJ: APP \ [/GLOBAL\]. La dernière colonne de la sortie est une valeur numérique qui indique si une application est publiée ou non.

PUBLIÉ = 1 signifie que l’application a été publiée par une actualisation du serveur de publication, en installant l’application à l’aide d’un fichier Windows Installer (. MSI), ou en exécutant une commande SFTMIME ajouter un PACKAGE, configurer le PACKAGE ou publier le PACKAGE à l’aide d’un manifeste du package.

PUBLIÉ = 0 indique que l’application n’a pas été publiée ou qu’elle n’est plus publiée suite à l’exécution d’une opération Clear ou d’exécution d’une commande SFTMIME UNPUBLISH.

Si vous utilisez le paramètre/GLOBAL, l’État publié sera 1 pour les applications publiées globalement et 0 pour les applications qui ont été publiées sous contextes utilisateur. Sans le paramètre/GLOBAL, un État publié de 1 est retourné pour les applications publiées dans le contexte de l’utilisateur exécutant la commande, et l’État 0 est retourné pour les applications qui sont publiées globalement.

 

La commande OBJ de la requête SFTMIME peut être utilisée pour rechercher des informations sur tous les objets indiqués ci-dessus: applications, packages, associations de types de fichiers et serveurs.Pour illustrer la façon dont vous pouvez utiliser la commande SFTMIME de requête OBJ dans vos tâches d’opérations normales, l’exemple suivant illustre le processus que vous devez suivre si vous vouliez définir la valeur de paramètre OVERRIDEURL d’un package spécifique pour spécifier un nouveau chemin d’accès au contenu du package. 

1.  Pour rechercher le package que vous voulez configurer, exécutez la commande suivante:

    `SFTMIME QUERY OBJ:PACKAGE`

    Cette commande renvoie chaque nom de package détecté en tant que GUID dans la première colonne de sortie, par exemple, {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.

2.  Pour définir la valeur de paramètre OVERRIDEURL, vous utilisez la commande SFTMIME [configurer le package](configure-package.md) . Par exemple, pour définir la valeur OVERRIDEURL de ce package sur une valeur de *\\\\server\\share\\mypackage.SFT*, utilisez la commande SFTMIME configure package et attribuez-lui le GUID de package sélectionné à partir de la sortie de la commande SFTMIME de requête obj à l’étape 1, suivi du paramètre OVERRIDEURL et de sa nouvelle valeur, comme suit:

    `SFTMIME CONFIGURE PACKAGE:"{AF78ABE1-57D4-4297-89DE-C308684AEDD6}" /OVERRIDEURL "\\\\server\\share\\mypackage.sft "`

Pour la version 4.6 SP2, l’option suivante a été ajoutée.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/NO-UPDATE-FTA-SHORTCUT</p></td>
<td align="left"><p>Indique l’état actuel de l’indicateur/NO-UPDATE-FTA-SHORTCUT.</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Référence de commande SFTMIME](sftmime--command-reference.md)

 

 





