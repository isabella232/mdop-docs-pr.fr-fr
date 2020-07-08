---
title: Comment faire en sorte qu'un groupe de connexion ignore la version du package
description: Comment faire en sorte qu'un groupe de connexion ignore la version du package
author: dansimp
ms.assetid: 6ebc1bff-d190-4f4c-a6da-e09a4cca7874
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b64d1938419aef184c5df667bf71b8157de0450a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805370"
---
# Comment faire en sorte qu'un groupe de connexion ignore la version du package


Microsoft Application Virtualization (App-V) 5,0 SP3 vous permet de configurer un groupe de connexion pour utiliser n’importe quelle version d’un package, qui simplifie les mises à jour de package et réduit le nombre de groupes de connexion que vous devez créer.

Pour mettre à niveau un package dans des versions antérieures de App-V, vous devez effectuer plusieurs étapes, notamment la désactivation du groupe de connexion et la modification du fichier de définition XML du groupe de connexion.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Description de la tâche avec App-V 5,0 SP3</th>
<th align="left">Exécution d’une tâche avec App-V 5,0 SP3</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Vous pouvez configurer un groupe de connexion pour accepter n’importe quelle version d’un package, qui vous permet de mettre à niveau le package sans avoir à désactiver le groupe de connexion.</p>
<p><strong>Fonctionnement de la fonctionnalité:</strong></p>
<ul>
<li><p>Si le groupe de connexion a accès à plusieurs versions d’un package, la version la plus récente est utilisée.</p></li>
<li><p>Si le groupe de connexion contient un package facultatif présentant une version incorrecte, le package est ignoré et ne bloque pas la création de l’environnement virtuel du groupe de connexion.</p></li>
<li><p>Si le groupe de connexion contient un package non facultatif présentant une version incorrecte, l’environnement virtuel du groupe de connexions ne peut pas être créé.</p></li>
</ul></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Méthode</th>
<th align="left">Étapes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V Server-console de gestion</p></td>
<td align="left"><ol>
<li><p>Dans la console de gestion, sélectionnez <strong> packages de </strong> &gt; <strong> connexion </strong> .</p></li>
<li><p>Sélectionnez le groupe de connexion approprié dans la bibliothèque de groupes de connexion.</p></li>
<li><p>Cliquez sur <strong> modifier </strong> dans le volet packages connectés.</p></li>
<li><p>Cochez <strong> la case utiliser une version </strong> située en regard du nom du package, puis cliquez sur <strong> appliquer </strong> .</p></li>
</ol>
<p>Pour plus d’informations sur l’ajout et la mise à niveau de packages, voir <a href="how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md" data-raw-source="[How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)"> comment ajouter ou mettre à niveau des packages à l’aide de la console de gestion </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client App-V sur un ordinateur autonome</p></td>
<td align="left"><ol>
<li><p>Créez le document XML de groupe de connexion.</p></li>
<li><p>Pour mettre à niveau le package, définissez l' <strong> </strong> attribut de balise <strong> de package VersionId </strong> sur un astérisque ( <strong>*</strong> ).</p></li>
<li><p>Utilisez l’applet de commande suivante pour ajouter le groupe de connexions, puis incluez le chemin d’accès au document XML de groupe de connexion:</p>
<p><strong>Add-AppvClientConnectionGroup</strong></p></li>
<li><p>Lorsque vous mettez à niveau un package, utilisez les applets de commande suivantes pour supprimer l’ancien package, ajouter le package mis à niveau et publier le package mis à niveau:</p>
<ul>
<li><p>RemoveAppvClientPackage</p></li>
<li><p>Add-AppvClientPackage</p></li>
<li><p>Publisher-AppvClientPackage</p></li>
</ul></li>
</ol>
<p>Pour plus d’informations, voir:</p>
<ul>
<li><p>Fichier XML d’exemple, <strong> fichier XML de groupe de connexion avec packages facultatifs </strong> , dans cette section: <a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"> comment utiliser des packages facultatifs dans les groupes de connexion</a></p></li>
<li><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">Gestion de packages App-V5.0 s'exécutant sur un ordinateur autonome à l'aide de PowerShell</a></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 






## Rubriques connexes


[Gestion des groupes de connexion](managing-connection-groups.md)

 

 





