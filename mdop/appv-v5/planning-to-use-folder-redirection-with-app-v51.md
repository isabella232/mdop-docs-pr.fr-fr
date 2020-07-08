---
title: Envisager l'utilisation de la redirection des dossiers avec App-V
description: Envisager l'utilisation de la redirection des dossiers avec App-V
author: dansimp
ms.assetid: 6bea9a8f-a915-4d7d-be67-ef1cca1398ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 507aef186579da0efdb3af7b6e1088a5e725ad70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804938"
---
# Envisager l'utilisation de la redirection des dossiers avec App-V


Microsoft Application Virtualization (App-V) 5,1 prend en charge l’utilisation de la redirection de dossiers, une fonctionnalité qui permet aux utilisateurs et aux administrateurs de rediriger le chemin d’accès d’un dossier vers un nouvel emplacement.

Cette rubrique contient les sections suivantes:

-   [Configuration requise pour l’utilisation de la redirection de dossiers](#bkmk-folder-redir-reqs)

-   [Configuration de la redirection de dossiers pour une utilisation avec App-V](#bkmk-folder-redir-cfg)

-   [Fonctionnement de la redirection de dossiers avec App-V](#bkmk-folder-redir-works)

-   [Présentation de la redirection de dossiers](#bkmk-folder-redir-overview)

## <a href="" id="bkmk-folder-redir-reqs"></a>Configurations requises et scénarios non pris en charge pour l’utilisation de la redirection de dossiers


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Configuration requise</p></td>
<td align="left"><p>Pour utiliser la redirection de dossiers% AppData%, vous devez effectuer les opérations suivantes:</p>
<ul>
<li><p>Disposent d’un package App-V doté d’un dossier de système de fichiers virtuel AppData (VFS).</p></li>
<li><p>Activez la redirection de dossier et redirigez les dossiers des utilisateurs vers un dossier partagé, généralement un dossier réseau.</p></li>
<li><p>Accédez à l’un ou l’autre des éléments suivants:</p>
<ul>
<li><p>Fichiers sous%appdata%\Microsoft\AppV\Client\Catalog</p></li>
<li><p>Paramètres du Registre sous HKEY_CURRENT_USER \Software\Microsoft\AppV\Client\Packages</p>
<p>Pour plus d’informations, consultez la rubrique <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)"> publication d’applications et interactions client </a> .</p></li>
</ul></li>
<li><p>Vérifiez que les dossiers suivants sont disponibles pour chaque utilisateur qui se connecte à l’ordinateur exécutant le client App-V 5,0 SP2 ou version ultérieure:</p>
<ul>
<li><p>% AppData% est configuré sur l’emplacement réseau souhaité (avec ou sans <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)"> prise en charge des fichiers hors connexion </a> ).</p></li>
<li><p>% LocalAppData% est configuré dans le dossier local souhaité.</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Scénarios non pris en charge</p></td>
<td align="left"><ul>
<li><p>Configuration de% LocalAppData% en tant que lecteur réseau.</p></li>
<li><p>Redirection du menu Démarrer vers un dossier unique pour plusieurs utilisateurs.</p></li>
<li><p>En cas d’itinérance (% AppData%) est redirigé vers un partage réseau qui n’est pas disponible, les applications App-V ne peuvent pas se lancer comme suit:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version App-V</th>
<th align="left">Description du scénario</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Dans l’App-V 5,0 via App-V 5,0 SP2 plus de correctifs</p></td>
<td align="left"><p>Ce problème survient, que l’activation des fichiers hors connexion soit activée ou non.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dans l’App-V 5,0 SP3 et versions ultérieures</p></td>
<td align="left"><p>Si le partage réseau non disponible a été activé pour les fichiers en mode hors connexion, l’application application-V s’exécutera correctement.</p></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-cfg"></a>Configuration de la redirection de dossiers pour une utilisation avec App-V


La redirection de dossiers peut être appliquée à différents dossiers tels que le bureau, mes documents, mes images, etc. Toutefois, le seul dossier ayant un impact sur l’utilisation des applications App-V est le dossier AppData itinérance de l’utilisateur (% AppData%). Vous pouvez appliquer la redirection de dossiers à n’importe quel autre dossier pris en charge sans impact sur App-V.

## <a href="" id="bkmk-folder-redir-works"></a>Fonctionnement de la redirection de dossiers avec App-V


Le tableau suivant décrit le fonctionnement de la redirection de dossier lorsque% AppData% est redirigé vers un réseau et lorsque vous remplissez les conditions mentionnées plus haut dans cet article.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">État de l’environnement virtuel</th>
<th align="left">Action qui se produit</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Au démarrage de l’environnement virtuel</p></td>
<td align="left"><p>Le dossier de système de fichiers virtuel (VFS) est mappé au dossier AppData Local (% LocalAppData%) au lieu de se répartir sur le dossier AppData itinérance de l’utilisateur (% AppData%).</p>
<ul>
<li><p>LocalAppData contient un cache local du dossier AppData errant de l’utilisateur pour le package en cours d’utilisation. Le cache local se trouve sous les éléments suivants:</p>
<p><code>%LocalAppData%\Microsoft\AppV\Client\VFS\PackageGUID\AppData</code></p></li>
<li><p>Les données les plus récentes du dossier d’itinérance de l’utilisateur sont copiées dans et remplacent les données actuellement présentes dans le cache local.</p></li>
<li><p>Lorsque l’environnement virtuel est en cours d’exécution, les données continuent d’être enregistrées dans le cache local. Les données ne sont fournies qu’à partir de% LocalAppData% et ne sont pas déplacées ou synchronisées avec% AppData% tant que l’utilisateur final n’a pas arrêté l’ordinateur.</p></li>
<li><p>Les entrées du dossier AppData sont créées à l’aide du contexte de l’utilisateur et non du contexte du système.</p></li>
</ul>
<div class="alert">
<strong>Remarque</strong><br/><p>La redirection de dossiers du client App-V ne peut pas déplacer les fichiers de% AppData% vers% LocalAppData%. Consultez <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)"> les notes de publication pour App-V 5,0 SP2 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Lorsque l’environnement virtuel s’arrête</p></td>
<td align="left"><p>Les données mises en cache locales dans AppData (itinérance) sont représentées et copiées dans le dossier AppData «Real» dans% AppData%. Un horodatage, qui indique le dernier chargement connu, est enregistré en même temps que la clé de Registre sous:</p>
<p><code>HKCU\Software\Microsoft\AppV\Client\Packages&amp;lt;PACKAGE_GUID&gt;\AppDataTime</code></p>
<p>Pour fournir la redondance, App-V conserve les trois copies les plus récentes des données comprimées sous% AppData%.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-overview"></a>Présentation de la redirection de dossiers


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Objectif</p></td>
<td align="left"><p>Permet aux utilisateurs finaux de travailler avec des fichiers qui ont été redirigés vers un autre dossier, comme si les fichiers existaient déjà sur le lecteur local.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Description</p></td>
<td align="left"><p>La redirection de dossiers permet aux utilisateurs et aux administrateurs de rediriger le chemin d’accès d’un dossier vers un emplacement réseau. Les documents figurant dans le dossier sont accessibles à l’utilisateur à partir de n’importe quel ordinateur du réseau.</p>
<ul>
<li><p>La redirection de dossiers permet aux utilisateurs et aux administrateurs de rediriger le chemin d’accès d’un dossier vers un emplacement réseau. Les documents figurant dans le dossier sont accessibles à l’utilisateur à partir de n’importe quel ordinateur du réseau.</p></li>
<li><p>Le nouvel emplacement peut être un dossier sur l’ordinateur local ou un dossier sur un réseau partagé.</p></li>
<li><p>La redirection de dossier met à jour les fichiers immédiatement, tandis que les données d’itinérance sont généralement synchronisées lorsque l’utilisateur se connecte ou se déconnecte.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Exemple d’utilisation</p></td>
<td align="left"><p>Vous pouvez rediriger le dossier documents, qui est généralement stocké sur le disque dur local de l’ordinateur&#39;, à un emplacement réseau. L’utilisateur peut accéder aux documents du dossier à partir de n’importe quel ordinateur du réseau.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ressources complémentaires</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/cc778976.aspx" data-raw-source="[Folder redirection overview](https://technet.microsoft.com/library/cc778976.aspx)">Présentation de la redirection de dossiers</a></p></td>
</tr>
</tbody>
</table>
















