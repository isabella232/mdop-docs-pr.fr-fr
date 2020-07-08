---
title: Comment utiliser des packages facultatifs dans les groupes de connexion
description: Comment utiliser des packages facultatifs dans les groupes de connexion
author: dansimp
ms.assetid: 4d08a81b-55e5-471a-91dc-9a684fb3c9a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 64a2c0758294bfa617d3d85f888cfce3a2c0d21e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805124"
---
# Comment utiliser des packages facultatifs dans les groupes de connexion


À partir de Microsoft Application Virtualization (App-V) 5,0 SP3, vous pouvez ajouter des packages facultatifs à vos groupes de connexion pour simplifier la gestion des groupes de connexion. Le tableau suivant récapitule les tâches que vous pouvez effectuer plus facilement à l’aide des packages facultatifs, ainsi que des liens vers des instructions pour chaque tâche.

**Remarques** 
 **Les packages facultatifs sont uniquement pris en charge dans l’App-V 5,0 SP3.**

 

Avant d’utiliser des packages facultatifs, voir [Configuration requise pour l’utilisation de packages facultatifs dans les groupes de connexion](#bkmk-reqs-using-cg).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Lien vers des instructions</th>
<th align="left">Tâche</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="#bkmk-apps-plugs-optional" data-raw-source="[Use one connection group, with optional packages, for multiple users who have different packages entitled to them](#bkmk-apps-plugs-optional)">Utiliser un groupe de connexions avec des packages facultatifs pour plusieurs utilisateurs disposant d’un paquet d’accès différent</a></p></td>
<td align="left"><p>Utilisez un groupe de connexion unique pour rendre différents groupes d’applications et plug-ins disponibles pour différents utilisateurs finaux.</p>
<p>Par exemple, vous souhaitez distribuer Microsoft Office à tous les utilisateurs finaux, mais distribuer différents plug-ins à différents sous-ensembles d’utilisateurs.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="#bkmk-unpub-del-optl-pkg" data-raw-source="[Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group](#bkmk-unpub-del-optl-pkg)">Annuler la publication ou la suppression d’un package facultatif, ou annuler la publication d’un package facultatif et le republier ultérieurement sans changer le groupe de connexion</a></p></td>
<td align="left"><p>Annulez, supprimez ou republiez un package facultatif sans avoir à désactiver, supprimer, modifier, ajouter ou réactiver le groupe de connexion sur le client App-V.</p>
<p>Vous pouvez également annuler la publication du package facultatif et le republier ultérieurement sans avoir à désactiver ou republier le groupe de connexion.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-apps-plugs-optional"></a>Utiliser un groupe de connexions avec des packages facultatifs pour plusieurs utilisateurs dotés d’un package différent


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Description de la tâche</th>
<th align="left">Exécution d’une tâche</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Avec App-V 5,0 SP3</strong></p>
<p>Vous pouvez ajouter des packages facultatifs aux groupes de connexion, ce qui vous permet de fournir différentes combinaisons d’applications et de plug-ins à différents utilisateurs finaux.</p>
<p><strong>Par exemple </strong> : vous souhaitez distribuer Microsoft Office à vos utilisateurs finaux, mais activer un certain plug-in pour seulement un sous-ensemble d’utilisateurs.</p>
<p>Pour ce faire, créez un groupe de connexion contenant un package avec Office, un autre package avec les plug-ins Office, puis rendez le package de plug-ins facultatif.</p>
<p>Les utilisateurs finaux qui n’ont pas le droit d’accéder au package du plug-in pourront toujours exécuter Office.</p></td>
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
<li><p>Dans la console de gestion, sélectionnez <strong> packages </strong> pour ouvrir la page Packages.</p></li>
<li><p>Sélectionnez <strong> groupes </strong> de connexion pour afficher la bibliothèque de groupes de connexion.</p></li>
<li><p>Sélectionnez le groupe de connexion approprié dans la bibliothèque de groupes de connexion.</p></li>
<li><p>Cliquez sur <strong> modifier </strong> dans le volet packages connectés.</p></li>
<li><p>Sélectionnez <strong> facultatif </strong> en regard du nom du package.</p></li>
<li><p>Activez la case <strong> </strong> à cocher Ajouter l’accès du package aux accès au groupe. Cette étape requise ajoute au groupe de connexions les habilitations du package que vous avez configurées précédemment lorsque vous avez affecté des packages aux groupes Active Directory.</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>App-V Server-cmdlet PowerShell</p></td>
<td align="left"><p>Utilisez l’applet de commande suivante et spécifiez le <strong> paramètre-facultatif </strong> :</p>
<p><strong>Add-AppvServerConnectionGroupPackage</strong></p>
<p><strong>Syntaxe</strong></p>
<p><code>Add-AppvServerConnectionGroupPackage [-AppvServerConnectionGroup] &lt;SerializableConnectionGroup&gt; [[-AppvServerPackage] &lt;PackageVersion&gt;] [-Optional] [-Order &lt;int&gt;] [-UseAnyPackageVersion]</code></p>
<p><strong>Exemple :</strong></p>
<p><code>Add-AppvServerConnectionGroupPackage -Name &quot;Connection Group 1&quot; -PackageName &quot;Package 1&quot; -Optional</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Client App-V sur un ordinateur autonome</p></td>
<td align="left"><ol>
<li><p>Créez le document XML de groupe de connexion et affectez <strong> </strong> à l’attribut <strong> d’indicateur de package IsOptional la </strong> <strong> valeur «true».</strong></p></li>
<li><p>Utilisez les applets de commande suivantes pour ajouter et activer le groupe de connexions:</p>
<ul>
<li><p>Add-AppvClientConnectionGroup</p></li>
<li><p>Enable-AppvClientConnectionGroup</p></li>
</ul></li>
</ol>
<p><strong>Exemple de document XML de groupe de connexion avec packages facultatifs:</strong></p>
<pre class="syntax" space="preserve"><code>&lt;?xml version=&quot;1.0&quot; ?&gt;
&lt;AppConnectionGroup
   xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;
   AppConnectionGroupId=&quot;8105CCD5-244B-4BA1-8888-E321E688D2CB&quot;
   VersionId=&quot;84CE3797-F1CB-4475-A223-757918929EB4&quot;
   DisplayName=&quot;Contoso Software Connection Group&quot; &gt;
&lt;Packages&gt;
&lt;Package
   PackageId=&quot;7735d1a8-5ef9-4df9-a1cf-3aa92ef54fe7&quot;
   VersionId=&quot;ec560d6f-e62e-48eb-a9e5-7c52a8c2e149&quot;
   DisplayName=&quot;Contoso Business Manager&quot;
/&gt;

&lt;Package
   PackageId=&quot;fc6fe0f7-be3d-4643-b37d-fc3f62d4dd5c&quot;
   VersionId=&quot;c67a71cd-3542-4a48-93e8-20c643c50970&quot;
   DisplayName=&quot;Contoso Forms&quot;
   IsOptional=&quot;false&quot;
/&gt;

&lt;Package
   PackageId=&quot;8f6301a5-4348-4039-9560-b27a5bb72711&quot;
   VersionId=&quot;6c694b45-3e19-46c6-a327-d159aa39e1d2&quot;
   DisplayName=&quot;Contoso Tax&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;Package
   PackageId=&quot;89d701bc-d507-4299-b6b6-000000003472&quot;
   VersionId=&quot;*&quot;
   DisplayName=&quot;Contoso Accounts&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;/Packages&gt;
&lt;/AppConnectionGroup&gt;</code></pre></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Avec les versions antérieures à App-V 5,0 SP3</strong></p></td>
<td align="left"><p>Vous deviez créer de nombreux groupes de connexion pour rendre des applications spécifiques et des combinaisons de plug-ins accessibles à des utilisateurs spécifiques.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-unpub-del-optl-pkg"></a>Annuler la publication ou la suppression d’un package facultatif, ou annuler la publication d’un package facultatif et le republier ultérieurement sans changer le groupe de connexion


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Description de la tâche</th>
<th align="left">Exécution d’une tâche</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Avec App-V 5,0 SP3</strong></p>
<p>Vous pouvez annuler la publication, la suppression ou la republication d’un package facultatif (qui se trouve dans un groupe de connexion) sans avoir à désactiver ou réactiver le groupe de connexion sur le client App-V.</p>
<p>Vous pouvez également annuler la publication d’un package facultatif et le republier ultérieurement sans avoir à désactiver ou republier le groupe de connexion.</p>
<p><strong>Exemple </strong> : Si vous publiez un package facultatif contenant un plug-in Microsoft Office et que vous souhaitez supprimer le plug-in, vous pouvez annuler la publication du package sans avoir à désactiver le groupe de connexion.</p></td>
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
<td align="left"><ul>
<li><p>Pour annuler la publication du package: dans la console de gestion, sélectionnez électionnez la <strong> </strong> page Packages, cliquez avec le bouton droit sur le package dont vous voulez annuler la publication, puis cliquez sur <strong> annuler la publication </strong> .</p></li>
<li><p>Pour supprimer un package facultatif d’un groupe de connexions: sur la <strong> page groupes de connexions </strong> , sélectionnez le package que vous voulez supprimer, puis cliquez sur la flèche droite pour supprimer le package du volet groupe de connexions en bas à gauche.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Client App-V sur un ordinateur autonome</p></td>
<td align="left"><p>Utilisez les applets de commande existantes suivantes:</p>
<ul>
<li><p>Annuler la publication-AppvClientPackage</p></li>
<li><p>Remove-AppvClientPackage</p></li>
</ul>
<p>Pour plus d’informations, reportez-vous <a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"> à comment gérer les packages App-V 5,0 exécutés sur un ordinateur autonome à l’aide de PowerShell </a> .</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Avec les versions antérieures à App-V 5,0 SP3</strong></p></td>
<td align="left"><p>Vous deviez:</p>
<ol>
<li><p>Supprimez le groupe de connexions de chaque ordinateur client App-V sur lequel il a été activé.</p></li>
<li><p>Annulez la publication du package.</p></li>
<li><p>Supprimez le package de la définition du groupe de connexion.</p></li>
<li><p>Republiez le groupe de connexion.</p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqs-using-cg"></a>Configuration requise pour l’utilisation de packages facultatifs dans les groupes de connexion


Avant d’utiliser les packages facultatifs dans les groupes de connexion, consultez la configuration requise suivante:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Condition requise</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Les groupes de connexions doivent contenir au moins un package non facultatif.</p></td>
<td align="left"><ul>
<li><p>Vérifiez que vous respectez cette exigence, car le serveur App-V et la cmdlet PowerShell ne vérifient pas que l’exigence a été satisfaite.</p></li>
<li><p>Si vous créez par erreur un groupe de connexions qui ne contient pas au moins un package non facultatif, et que l’utilisateur final tente d’ouvrir une application empaquetée dans ce groupe de connexion, le groupe de connexion échoue.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p>Les groupes de connexion publiés par l’utilisateur peuvent contenir des packages publiés globalement ou pour l’utilisateur.</p></li>
<li><p>Les groupes de connexion à publication globale doivent contenir uniquement des packages publiés globalement.</p></li>
</ul></td>
<td align="left"><p>Les groupes de connexions à publication globale doivent contenir des packages publiés globalement pour s’assurer que les packages seront disponibles lors du démarrage de l’environnement virtuel du groupe de connexion.</p>
<p>Si vous tentez d’ajouter ou de désactiver des groupes de connexions à publication globale qui contiennent des packages publiés par l’utilisateur, le groupe de connexion échouera.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Vous devez publier tous les packages non facultatifs avant de publier le groupe de connexion contenant ces packages.</p></td>
<td align="left"><p>L’environnement virtuel d’un groupe de connexions ne peut pas démarrer si des packages non facultatifs sont manquants.</p>
<p>Le client App-V ne peut pas ajouter ou activer un groupe de connexion si des packages non facultatifs n’ont pas été publiés.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Avant d’annuler la publication d’un package publié globalement, assurez-vous que les groupes de connexion qui sont habilités à tous les utilisateurs de cet ordinateur ne nécessitent plus le package.</p></td>
<td align="left"><p>Le système ne vérifie pas si le package fait partie du groupe de connexion d’un autre utilisateur. L’annulation de la publication d’un package global le rendra indisponible pour tous les utilisateurs de cet ordinateur, assurez-vous que les groupes de connexion de chaque utilisateur ne contiennent plus le package, ou le package facultatif.</p></td>
</tr>
</tbody>
</table>

 






## Rubriques connexes


[Gestion des groupes de connexion](managing-connection-groups.md)

 

 





