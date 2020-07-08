---
title: Utilisation de la console de gestion d'App-V5.1 Client
description: Utilisation de la console de gestion d'App-V5.1 Client
author: dansimp
ms.assetid: be6d4e35-5701-4f9a-ba8a-bede12662cf1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63dd75395cdfef1aebae30b364f77465ba8a9882
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804842"
---
# Utilisation de la console de gestion d'App-V5.1 Client


Cette rubrique fournit des informations sur la manière de configurer et de gérer le client Microsoft Application Virtualization (App-V) 5,1.

## Modification de la configuration du client App-V 5,1


Le client App-V 5,1 a des paramètres qui peuvent être configurés pour déterminer la façon dont le client s’exécutera dans votre environnement. Vous pouvez gérer ces paramètres sur l’ordinateur qui exécute le client ou à l’aide de PowerShell ou d’une stratégie de groupe. Pour plus d’informations sur la modification du client à l’aide de PowerShell ou de la configuration de stratégie de groupe, reportez-vous [à la rubrique modification de la configuration du client à l’aide de PowerShell](how-to-modify-client-configuration-by-using-powershell51.md).

## <a href="" id="the-app-v-5-1-client-management-console-"></a>La console de gestion des clients App-V 5,1


Vous pouvez obtenir des informations sur le client App-V 5,1 ou effectuer des tâches spécifiques en utilisant la console de gestion des clients App-V 5,1. Bon nombre de tâches que vous pouvez effectuer dans la console de gestion du client à l’aide de PowerShell. Les applets de commande PowerShell associées à chaque action sont également affichées dans le tableau suivant. Pour plus d’informations sur l’utilisation de PowerShell, voir [administration d’App-V 5,1 à l’aide de PowerShell](administering-app-v-51-by-using-powershell.md).

La console de gestion du client contient les onglets principaux décrits ci-dessous.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tabulation</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Vue d'ensemble</p></td>
<td align="left"><p>L' <strong> onglet vue d’ensemble </strong> contient les éléments suivants:</p>
<ul>
<li><p>Mise à jour: utilisez la <strong> vignette mettre à jour </strong> pour actualiser une application virtualisée ou pour recevoir un nouveau package virtualisé.</p>
<p>Le <strong> dernier rafraîchissement </strong> affiche la version actuelle du package virtualisé.</p></li>
<li><p>Télécharger toutes les applications virtuelles: utilisez la <strong> </strong> vignette Télécharger pour télécharger tous les packages approvisionnés par l’utilisateur actuel.</p>
<p>(Cmdlet PowerShell associée: <strong> Mount-AppvClientPackage </strong> )</p>
<p></p></li>
<li><p>Travailler hors connexion: utilisez cette vignette pour interdire toutes les mises à jour automatiques et manuelles des applications virtuelles.</p>
<p>(Cmdlet PowerShell associée: <strong> Set-AppvPublishServer – UserRefreshEnabled – GlobalRefreshEnabled </strong> )</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Applications virtuelles</p></td>
<td align="left"><p>L' <strong> onglet applications virtuelles </strong> affiche tous les packages qui ont été publiés pour l’utilisateur. Vous pouvez également cliquer sur un package spécifique et afficher toutes les applications qui font partie de ce package. Cela permet d’afficher des informations sur les packages actuellement utilisés et la quantité de contenu de chaque package téléchargé sur l’ordinateur. Vous pouvez également démarrer et arrêter le téléchargement de packages. Par ailleurs, vous pouvez réparer l’état de l’utilisateur. Une réparation entraîne la suppression de toutes les données utilisateur associées à un package.</p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Groupes de connexions d’application</p></td>
<td align="left"><p>L' <strong> onglet groupes de connexion </strong> d’application affiche tous les groupes de connexions disponibles pour l’utilisateur actuel. Cliquez sur un groupe de connexion spécifique pour afficher tous les packages qui font partie du groupe sélectionné. Cela affiche des informations sur les groupes de connexion qui sont déjà utilisés et la quantité de contenu du groupe de connexions téléchargée sur l’ordinateur. Par ailleurs, vous pouvez démarrer et arrêter des téléchargements de groupes de connexion. Vous pouvez utiliser cette section pour lancer une réparation. Une réparation supprimera tout l’état utilisateur associé à un groupe de connexion.</p>
<p>(Cmdlets PowerShell associées: Télécharger- <strong> Mount-AppvClientConnectionGroup </strong> . Réparer- <strong> AppvClientConnectionGroup </strong> .)</p>
<p></p></td>
</tr>
</tbody>
</table>

 

[Procédure d'accès à la console de gestion du client](how-to-access-the-client-management-console51.md)

[Comment configurer le client de manière à recevoir les mises à jour des groupes de connexion et des packages à partir du serveur de publication](how-to-configure-the-client-to-receive-package-and-connection-groups-updates-from-the-publishing-server-51.md)






## Rubriques connexes


[Opérations d'App-V5.1](operations-for-app-v-51.md)

 

 





