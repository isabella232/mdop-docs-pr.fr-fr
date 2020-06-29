---
title: Comment modifier une application publiée avec des paramètres avancés
description: Comment modifier une application publiée avec des paramètres avancés
author: dansimp
ms.assetid: 06a79049-9ce9-490f-aad7-fd4fdf185590
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 843aebb38f54959f209e742b398e3979acac3334
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812090"
---
# Comment modifier une application publiée avec des paramètres avancés


Après avoir ajouté et configuré une application publiée, l’application publiée peut être modifiée et des paramètres avancés supplémentaires peuvent être configurés.

**Pour modifier une application publiée avec paramètres avancés**

1.  Dans le volet **applications** , ajoutez et configurez une application publiée.

2.  Sélectionnez l’application publiée à modifier.

3.  Cliquez sur **Modifier**.

4.  Dans la boîte de dialogue **application publiée** , configurez les paramètres comme décrit dans le tableau suivant.

5.  Cliquez sur **OK**.

6.  Dans le menu **stratégie** , cliquez sur **valider**.

**Modification des propriétés de l’application publiée**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriété</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nom d’affichage</p></td>
<td align="left"><p>Nom du raccourci dans le menu Démarrer de l'&#39;utilisateur.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Le nom d’affichage n’est <strong> pas sensible à la </strong> casse.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Description</p></td>
<td align="left"><p>Description du menu publié.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Commencer à</p></td>
<td align="left"><p>Répertoire à partir duquel démarrer l’application.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>La trajectoire n’a pas besoin d’inclure de guillemets.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Ligne de commande</p></td>
<td align="left"><p>Commande d’exécution de l’application à partir de l’espace de travail MED-V.</p>
<p>Le chemin d’accès complet est requis et les paramètres peuvent être transmis à l’application de la même manière que dans toute autre commande Windows.</p>
<p>Dans une configuration de domaine, un lecteur partagé existe généralement sur le serveur sur lequel les ordinateurs de domaine sont mappés. Le répertoire doit être mappé ici, et s’il s’agit d’un dossier qui requiert une authentification utilisateur, la <strong> case à cocher utiliser les informations d’identification MED-V pour exécuter cette application </strong> doit être activée.</p>
<p>Dans un espace de travail de revertible MED-V, vous pouvez mapper un lecteur réseau avec la syntaxe MapNetworkDrive: &quot; <em> MapNetworkDrive &lt; &gt; &lt; Path, &gt; </em> &quot; par exemple &quot; <em> MapNetworkDrive t: \tux\data </em> &quot; .</p>
<p>Par exemple, pour publier l’Explorateur Windows, utilisez la syntaxe suivante: &quot; <em> c: &amp; quote ou &quot; c:\Windows </em> &quot; .</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Pour utiliser une résolution de nom, vous devez effectuer l’une des opérations suivantes:</p>
</div>
<div>

</div>
<ul>
<li><p>Configurez le DNS dans l’image de base de l’espace de travail MED-V.</p></li>
<li><p>Vérifiez que la résolution DNS est définie dans l’hôte et configurez-la pour utiliser le DNS hôte.</p></li>
<li><p>Utilisez l’adresse IP pour définir le lecteur réseau.</p></li>
</ul>
<div class="alert">
<strong>Remarque</strong><br/><p>Si le chemin d’accès comporte des espaces, le chemin d’accès complet doit être placé entre guillemets.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Remarque</strong><br/><p>Le chemin d’accès ne doit pas se terminer par une barre oblique inverse ().</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Ajouter un raccourci dans le menu Démarrer de Windows</p></td>
<td align="left"><p>Activez cette case à cocher pour créer un raccourci pour l’application dans le menu Démarrer de l’utilisateur&#39;.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Lancer l’application lorsque l’espace de travail est démarré</p></td>
<td align="left"><p>Activez cette case à cocher pour exécuter l’application automatiquement lors du démarrage de l’espace de travail MED-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utiliser les informations d’identification MED-V pour exécuter cette application</p></td>
<td align="left"><p>Activez cette case à cocher pour authentifier les applications qui demandent un nom d’utilisateur et un mot de passe à l’aide des informations d’identification MED-V au lieu des informations d’identification définies pour l’application.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Dans le cadre de l’utilisation de l’authentification unique, la ligne de commande doit être <strong>C:\Windows\Explorer.exe &quot; chemin de dossier &quot; </strong> . Dans le cas contraire, la ligne de commande doit être &quot; <strong> chemin d’accès au dossier </strong> &quot; .</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Rubriques connexes


[Comment configurer des applications publiées](how-to-configure-published-applicationsmedvv2.md)









