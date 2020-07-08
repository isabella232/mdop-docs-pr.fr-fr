---
title: Gestion de packages App-V5.1 s'exécutant sur un ordinateur autonome à l'aide de PowerShell
description: Gestion de packages App-V5.1 s'exécutant sur un ordinateur autonome à l'aide de PowerShell
author: dansimp
ms.assetid: c3fd06f6-102f-43d1-a577-d5ced6ac537d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b454014da4e5f349af913d3fea8ea3837598a039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805335"
---
# Gestion de packages App-V5.1 s'exécutant sur un ordinateur autonome à l'aide de PowerShell


Les sections suivantes vous expliquent comment effectuer différentes tâches de gestion sur un ordinateur client autonome à l’aide de PowerShell:

-   [Pour renvoyer une liste de packages](#bkmk-return-pkgs-standalone-posh)

-   [Pour ajouter un package](#bkmk-add-pkgs-standalone-posh)

-   [Pour publier un package](#bkmk-pub-pkg-standalone-posh)

-   [Pour publier un package pour un utilisateur spécifique](#bkmk-pub-pkg-a-user-standalone-posh)

-   [Pour ajouter et publier un package](#bkmk-add-pub-pkg-standalone-posh)

-   [Pour annuler la publication d’un package existant](#bkmk-unpub-pkg-standalone-posh)

-   [Pour annuler la publication d’un package pour un utilisateur spécifique](#bkmk-unpub-pkg-specfc-use)

-   [Pour supprimer un package existant](#bkmk-remove-pkg-standalone-posh)

-   [Pour permettre uniquement aux administrateurs de publier ou de retirer des packages](#bkmk-admins-pub-pkgs)

-   [Présentation des packages en attente (UserPending et GlobalPending)](#bkmk-understd-pend-pkgs)

## <a href="" id="bkmk-return-pkgs-standalone-posh"></a>Pour renvoyer une liste de packages


Utilisez les informations suivantes pour renvoyer une liste des packages qui sont habilités à un utilisateur spécifique:

**Cmdlet**: Get-AppvClientPackage

**Paramètres**:-nom-version-PackageID-VersionId

**Exemple**: Get-AppvClientPackage – Name "ContosoApplication"-version 2

## <a href="" id="bkmk-add-pkgs-standalone-posh"></a>Pour ajouter un package


Utilisez les informations suivantes pour ajouter un package à un ordinateur.

**Important**  Cet exemple n’ajoute qu’un package. Le package n’est pas publié pour l’utilisateur ou l’ordinateur.

 

**Applet**de passe: Add-AppvClientPackage

**Exemple**: $contoso = Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV

## <a href="" id="bkmk-pub-pkg-standalone-posh"></a>Pour publier un package


Utilisez les informations suivantes pour publier un package qui a été ajouté à un utilisateur spécifique ou globalement à un utilisateur de l’ordinateur.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Méthode de publication</th>
<th align="left">Cmdlet et exemple</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Publication pour l’utilisateur</p></td>
<td align="left"><p><strong>Cmdlet </strong> : Publisher-AppvClientPackage</p>
<p><strong>Exemple </strong> : Publisher-AppvClientPackage "ContosoApplication"</p></td>
</tr>
<tr class="even">
<td align="left"><p>Publication globale</p></td>
<td align="left"><p><strong>Cmdlet </strong> : Publisher-AppvClientPackage</p>
<p><strong>Exemple </strong> : Publisher-AppvClientPackage "ContosoApplication"-Global</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-pub-pkg-a-user-standalone-posh"></a>Pour publier un package pour un utilisateur spécifique


**Remarques**  Pour utiliser ce paramètre, vous devez utiliser le correctif logiciel App-V 5,0 SP2 package 5 ou version ultérieure.

 

Un administrateur peut publier un package pour un utilisateur spécifique en spécifiant le paramètre facultatif **-UserSid** avec l’applet de la cmdlet **Publisher AppvClientPackage** , où **-UserSid** représente l’identificateur de sécurité (SID) de l’utilisateur final.

Pour utiliser ce paramètre:

-   Vous pouvez exécuter cette cmdlet à partir de la session utilisateur ou administrateur.

-   Vous devez être connecté avec des informations d’identification d’administrateur pour utiliser le paramètre.

-   L’utilisateur final doit être connecté.

-   Vous devez indiquer l’identificateur de sécurité (SID) de l’utilisateur final.

**Cmdlet**: Publisher-AppvClientPackage

**Exemple**: Publisher-AppvClientPackage "ContosoApplication"-UserSid S-1-2-34-56789012-3456789012-345678901-2345

## <a href="" id="bkmk-add-pub-pkg-standalone-posh"></a>Pour ajouter et publier un package


Utilisez les informations suivantes pour ajouter un package à un ordinateur et le publier à l’utilisateur.

**Applet**de passe: Add-AppvClientPackage

**Exemple**: Add-AppvClientPackage \\\\path\\to\\appv\\package.AppV | Publisher-AppvClientPackage

## <a href="" id="bkmk-unpub-pkg-standalone-posh"></a>Pour annuler la publication d’un package existant


Utilisez les informations suivantes pour annuler la publication d’un package ayant été autorisé à un utilisateur, mais pas de supprimer le package de l’ordinateur.

**Cmdlet**: UNPUBLISH-AppvClientPackage

**Exemple**: UNPUBLISH-AppvClientPackage "ContosoApplication"

## <a href="" id="bkmk-unpub-pkg-specfc-use"></a>Pour annuler la publication d’un package pour un utilisateur spécifique


**Remarques**  Pour utiliser ce paramètre, vous devez utiliser le correctif logiciel App-V 5,0 SP2 package 5 ou version ultérieure.

 

Un administrateur peut annuler la publication d’un package pour un utilisateur spécifique à l’aide du paramètre facultatif **-UserSid** avec l’applet de passe **UNPUBLISH-AppvClientPackage** , où **-UserSid** représente l’identificateur de sécurité (SID) de l’utilisateur final.

Pour utiliser ce paramètre:

-   Vous pouvez exécuter cette cmdlet à partir de la session utilisateur ou administrateur.

-   Vous devez être connecté avec des informations d’identification d’administrateur pour utiliser le paramètre.

-   L’utilisateur final doit être connecté.

-   Vous devez indiquer l’identificateur de sécurité (SID) de l’utilisateur final.

**Cmdlet**: UNPUBLISH-AppvClientPackage

**Exemple**: UNPUBLISH-AppvClientPackage "ContosoApplication"-UserSid S-1-2-34-56789012-3456789012-345678901-2345

## <a href="" id="bkmk-remove-pkg-standalone-posh"></a>Pour supprimer un package existant


Utilisez les informations suivantes pour supprimer un package de l’ordinateur.

**Applet**de passe: Remove-AppvClientPackage

**Exemple**: Remove-AppvClientPackage "ContosoApplication"

**Remarques**  Les applets de cmdlets App-V ont été affectées à des variables pour les exemples précédents pour plus de clarté. le devoir n’est pas une obligation. La plupart des cmdlets peuvent être combinées comme affichées dans [pour ajouter et publier un package](#bkmk-add-pub-pkg-standalone-posh). Pour un didacticiel détaillé, voir [App-V 5,0 client PowerShell Deep plongée](https://go.microsoft.com/fwlink/?LinkId=324466).

 

## <a href="" id="bkmk-admins-pub-pkgs"></a>Pour permettre uniquement aux administrateurs de publier ou de retirer des packages


**Remarques** 
 **Cette fonctionnalité est prise en charge à partir de l’App-V 5,0 SP3.**

 

Utilisez l’applet de commande et le paramètre suivants pour permettre aux administrateurs (et non aux utilisateurs finaux) de publier ou d’annuler la publication des packages:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Applet de commande</strong></p></td>
<td align="left"><p>Set-AppvClientConfiguration</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Paramètre</strong></p></td>
<td align="left"><p>-RequirePublishAsAdmin</p>
<p>Valeurs de paramètres:</p>
<ul>
<li><p>0-faux</p></li>
<li><p>1-vrai</p></li>
</ul>
<p><strong>Exemple: </strong> : Set-AppvClientConfiguration – RequirePublishAsAdmin1</p></td>
</tr>
</tbody>
</table>

 

Pour utiliser la console de gestion App-V pour définir cette configuration, reportez-vous à la rubrique [publication d’un package à l’aide de la console de gestion](how-to-publish-a-package-by-using-the-management-console-51.md).

## <a href="" id="bkmk-understd-pend-pkgs"></a>Présentation des packages en attente (UserPending et GlobalPending)


**À partir de l’App-V 5,0 SP2**: Si vous exécutez une applet de cmdlet PowerShell affectant un package en cours d’utilisation, la tâche que vous essayez d’effectuer se trouve dans un état d’attente. Par exemple, si vous tentez de publier un package alors qu’une application de ce package est utilisée, puis exécuté **Get-AppvClientPackage**, l’État en attente apparaît dans la sortie de l’applet de connexion comme suit:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Élément de sortie de l’applet de vente</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>UserPending</p></td>
<td align="left"><p>Indique si une tâche en attente est appliquée au package dans la liste d’utilisateurs:</p>
<ul>
<li><p>Vrai</p></li>
<li><p>Faux</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalPending</p></td>
<td align="left"><p>Indique si une tâche en attente dans le package répertorié est appliquée globalement à l’ordinateur:</p>
<ul>
<li><p>Vrai</p></li>
<li><p>Faux</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

La tâche en attente sera exécutée plus tard, conformément aux règles suivantes:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Type de tâche</th>
<th align="left">Règle applicable</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tâche basée sur l’utilisateur (par exemple, publication d’un package pour un utilisateur);</p></td>
<td align="left"><p>La tâche en attente sera exécutée après que l’utilisateur se déconnecte, puis se reconnecte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Une tâche basée sur le monde (par exemple, l’activation globale d’un groupe de connexions);</p></td>
<td align="left"><p>La tâche en attente sera effectuée lorsque l’ordinateur sera arrêté, puis redémarré.</p></td>
</tr>
</tbody>
</table>

 

Pour plus d’informations sur les tâches en attente, voir [à propos de App-V 5,0 SP2](about-app-v-50-sp2.md#bkmk-pkg-upgr-pendg-tasks).

Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.1](operations-for-app-v-51.md)

[Administration d'App-V5.1 à l'aide de PowerShell](administering-app-v-51-by-using-powershell.md)

 

 





