---
title: Comment autoriser uniquement les administrateurs à activer des groupes de connexion
description: Comment autoriser uniquement les administrateurs à activer des groupes de connexion
author: dansimp
ms.assetid: 42ca3157-5d85-467b-a148-09404f8f737a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 083d6386f02996d35255f90958705798f2cd5fb9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805737"
---
# Comment autoriser uniquement les administrateurs à activer des groupes de connexion


Vous pouvez configurer le client App-V de façon à ce que seuls les administrateurs (pas les utilisateurs finaux) puissent activer ou désactiver les groupes de connexion. Dans les versions antérieures d’App-V, vous ne pouviez pas empêcher les utilisateurs finaux d’effectuer ces tâches.

**Remarques** 
 **Cette fonctionnalité est prise en charge à partir de l’App-V 5,0 SP3.**

 

Appliquez l’une des méthodes suivantes pour autoriser uniquement les administrateurs à activer ou désactiver les groupes de connexion.

<table>
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
<td align="left"><p>Paramètre de la stratégie de groupe</p></td>
<td align="left"><p>Activez le paramètre de stratégie de groupe «exiger une administration en tant qu’administrateur», qui se trouve dans le nœud d’objet de stratégie de groupe suivant:</p>
<p><strong>&gt;Stratégies de Configuration ordinateur &gt; modèles d’administration application pour la &gt; &gt; publication de l’application-V &gt;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Applet de commande PowerShell</p></td>
<td align="left"><p>Exécutez l' <strong> applet de cmdlet Set-AppvClientConfiguration </strong> à l’aide du <strong> paramètre-RequirePublishAsAdmin </strong> .</p>
<p>Valeurs de paramètres:</p>
<ul>
<li><p>0-faux</p></li>
<li><p>1-vrai</p></li>
</ul>
<p><strong>Exemple: </strong> : Set-AppvClientConfiguration – RequirePublishAsAdmin1</p></td>
</tr>
</tbody>
</table>

 

Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Gestion des groupes de connexion](managing-connection-groups51.md)

 

 





