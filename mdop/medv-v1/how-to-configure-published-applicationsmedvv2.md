---
title: Comment configurer des applications publiées
description: Comment configurer des applications publiées
author: dansimp
ms.assetid: 43a59ff7-5d4e-49dc-84e5-1082bc4dd8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cb5736382f03e818ef10aa814a8e61044ca2b73a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810481"
---
# Comment configurer des applications publiées


Les applications qui ne sont pas compatibles avec le système d’exploitation hôte peuvent être exécutées au sein de l’espace de travail MED-V et démarrées à partir de l’espace de travail MED-V de la même manière que sur le bureau, à partir du menu Démarrer ou à partir d’un raccourci d’hôte local. Les applications sélectionnées et définies sont appelées applications publiées. Les procédures dans cette section décrivent la façon d’ajouter et de supprimer des applications publiées.

Une application peut être publiée de l’une des façons suivantes:

-   En tant qu’application: sélectionnez une application spécifique en tapant dans la ligne de commande de l’application. Seule l’application sélectionnée est publiée.

-   En tant que menu, sélectionnez un dossier qui contient plusieurs applications. Toutes les applications du dossier sont publiées et affichées sous forme de menu.

## <a href="" id="bkmk-addingapublishedapplication"></a>Comment ajouter une application publiée à un espace de travail MED-V


**Pour ajouter une application à l’espace de travail MED-V**

1.  Cliquez sur l’espace de travail MED-V à configurer.

2.  Dans le volet **applications** , dans la section **applications publiées** , cliquez sur **Ajouter** pour ajouter une nouvelle application.

3.  Configurez les propriétés de l’application comme décrit dans le tableau suivant.

4.  Dans le menu **stratégie** , cliquez sur **valider**.

    **Remarque**  
    Si vous configurez Internet Explorer en tant qu’application publiée pour vous assurer que la redirection de site Web fonctionne correctement, assurez-vous que les paramètres ne sont pas entre parenthèses.



**Propriétés de l’application publiée**

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
<td align="left"><p>Activé</p></td>
<td align="left"><p>Activez cette case à cocher pour activer l’application publiée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nom d’affichage</p></td>
<td align="left"><p>Nom du raccourci dans le menu Démarrer de l'&#39;utilisateur.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Le nom d’affichage n’est <strong> pas sensible à la </strong> casse.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Description</p></td>
<td align="left"><p>Description de l’application publiée, qui s’affiche sous la forme d’une info-bulle lorsque l’utilisateur&#39;de la souris sur le raccourci.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ligne de commande</p></td>
<td align="left"><p>Commande utilisée pour exécuter l’application à partir de l’espace de travail MED-V. Le chemin d’accès complet est requis et les paramètres peuvent être transmis à l’application de la même manière que dans toute autre commande Windows.</p>
<p>Dans un espace de travail de revertible MED-V, vous pouvez mapper un lecteur réseau avec la syntaxe MapNetworkDrive: &quot; <em> MapNetworkDrive &lt; &gt; &lt; Path, &gt; </em> &quot; par exemple &quot; <em> MapNetworkDrive t: \tux\date </em> &quot; .</p>
<p>Par exemple, pour publier l’Explorateur Windows, utilisez la syntaxe suivante: &quot; <em> &lt; /em &gt; &quot; ou &quot; <em> c:\Windows </em> .&quot;</p>
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
<td align="left"><p>Menu Démarrer</p></td>
<td align="left"><p>Activez cette case à cocher pour créer un raccourci pour l’application dans le menu Démarrer de l’utilisateur&#39;.</p></td>
</tr>
</tbody>
</table>



Toutes les applications publiées apparaissent sous la forme de raccourcis dans le menu **Démarrer** de Windows (**Démarrer &gt; toutes les &gt; applications MED-V**).

## Comment supprimer une application publiée d’un espace de travail MED-V


**Pour supprimer une application de l’espace de travail MED-V**

1.  Cliquez sur un espace de travail MED-V.

2.  Dans le volet **applications** , dans la section **applications publiées** , sélectionnez une application à supprimer.

3.  Cliquez sur **supprimer**.

    L’application est supprimée de la liste des applications publiées.

4.  Dans le menu **stratégie** , cliquez sur **valider**.

## Comment ajouter un menu publié à un espace de travail MED-V


**Pour ajouter un menu publié dans l’espace de travail MED-V**

1.  Cliquez sur l’espace de travail MED-V à configurer.

2.  Dans le volet **applications** , dans la section **menus publiés** , cliquez sur **Ajouter** pour ajouter un nouveau menu.

3.  Configurez les propriétés de menu comme décrit dans le tableau suivant.

4.  Dans le menu **stratégie** , cliquez sur **valider**.

**Propriétés du menu publié**

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
<td align="left"><p>Activé</p></td>
<td align="left"><p>Activez cette case à cocher pour activer le menu publié.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nom d’affichage</p></td>
<td align="left"><p>Nom du raccourci dans le menu Démarrer de l'&#39;utilisateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Description</p></td>
<td align="left"><p>La description, qui s’affiche sous la forme d’une info-bulle lorsque le pointeur de la souris&#39;le pointeur de la souris sur le raccourci.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dossier dans l’espace de travail</p></td>
<td align="left"><p>Sélectionnez le dossier à publier en tant que menu contenant toutes les applications dans le dossier.</p>
<p>Le texte affiché correspond au chemin d’accès relatif du dossier programmes.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>S’il est vide, tous les programmes de l’hôte seront publiés sous forme de menu.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



Tous les menus publiés apparaissent en tant que raccourcis dans le menu **Démarrer** de Windows (**Démarrez &gt; tous les programmes pour les &gt; applications MED-V**). Vous pouvez modifier le nom du raccourci dans le champ de **dossier raccourcis du menu Démarrer** .

**Remarque**  
Lorsque vous configurez deux espaces de travail MED-V, il est recommandé de configurer un autre nom pour le dossier raccourcis du menu Démarrer.



## Supprimer un menu publié d’un espace de travail MED-V


**Pour supprimer un menu publié d’un espace de travail MED-V**

1.  Cliquez sur un espace de travail MED-V.

2.  Dans le volet **applications** , dans la section **menus publiés** , sélectionnez le menu à supprimer.

3.  Cliquez sur **supprimer**.

    Le menu est supprimé de la liste des menus publiés.

4.  Dans le menu **stratégie** , cliquez sur **valider**.

## Exécution d’une application publiée à partir d’une ligne de commande sur le client


L’administrateur peut exécuter des applications publiées depuis n’importe quel emplacement, par exemple, un raccourci sur le bureau, à l’aide de la commande suivante:

``` syntax
"<Install path>\Manager\KidaroCommands.exe" /run "<published application name>" "<MED-V workspace name>"
```

**Remarque**  
L’espace de travail MED-V dans lequel l’application publiée est définie doit être en cours d’exécution.



## Rubriques connexes


[Comment modifier une application publiée avec des paramètres avancés](how-to-edit-a-published-application-with-advanced-settings.md)

[Utilisation de l'interface utilisateur de la console de gestion MED-V](using-the-med-v-management-console-user-interface.md)

[Création d'un espace de travail MED-V](creating-a-med-v-workspacemedv-10-sp1.md)









