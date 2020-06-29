---
title: Affichage des métadonnées de publication du serveur App-V
description: Affichage des métadonnées de publication du serveur App-V
author: dansimp
ms.assetid: d5fa9eb5-647c-478d-8a4d-0ecda018bce6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97c59301678280febe23b8061c08033a88ae49c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804824"
---
# Affichage des métadonnées de publication du serveur App-V


Utilisez cette procédure pour afficher les métadonnées de publication, qui peuvent vous aider à résoudre les problèmes liés à la publication. Pour utiliser cette procédure, vous devez utiliser le serveur de gestion App-V.

Cet article contient les informations suivantes:

-   [Configuration requise pour App-V 5,1 pour afficher les métadonnées de publication](#bkmk-51-reqs-pub-meta)

-   [Syntaxe à utiliser pour afficher les métadonnées de publication](#bkmk-syntax-view-pub-meta)

-   [Valeurs de requête pour le système d’exploitation client et version](#bkmk-values-query-pub-meta)

-   [Définition des métadonnées de publication](#bkmk-whatis-pub-metadata)

## <a href="" id="bkmk-51-reqs-pub-meta"></a>Configuration requise pour App-V 5,1 pour afficher les métadonnées de publication


Dans App-V 5,1, vous devez fournir les valeurs suivantes dans l’adresse lorsque vous interrogez le serveur de publication App-V pour les métadonnées:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Valeur</th>
<th align="left">Informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>ClientVersion</strong></p></td>
<td align="left"><p>Si vous omettez le <strong> </strong> paramètre ClientVersion de la requête, les métadonnées excluent les fonctionnalités qui étaient nouvelles dans l’application-V 5,0 SP3.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Clientos</strong></p></td>
<td align="left"><p>Vous devez renseigner cette valeur uniquement si vous sélectionnez des systèmes d’exploitation de clients spécifiques lors du séquencé du package. Si vous sélectionnez la valeur par défaut (tous les systèmes d’exploitation), ne spécifiez pas cette valeur dans la requête.</p>
<p>Si vous omettez le <strong> paramètre clientos </strong> dans la requête, seuls les packages qui ont été séquencés pour prendre en charge tout système d’exploitation apparaissent dans les métadonnées.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-syntax-view-pub-meta"></a>Syntaxe de requête pour afficher les métadonnées de publication


Le tableau suivant répertorie les exemples de syntaxe et de requête.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version de App-V</th>
<th align="left">Syntaxe de requête</th>
<th align="left">Descriptions des paramètres</th>
<th align="left">Exemple</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 SP3 et App-V 5,1</p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/?ClientVersion=&lt;AppvClientVersion&gt;&amp;ClientOS=&lt;OSStringValue&gt;</code></p></td>
<td align="left"><table>
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
<td align="left"><p>&lt;PubServer&gt;</p></td>
<td align="left"><p>Nom du serveur de publication App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Port de publication #&gt;</p></td>
<td align="left"><p>Transférez le port vers le serveur de publication App-V que vous avez défini lors de la configuration du serveur de publication.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ClientVersion = &lt; AppvClientVersion&gt;</p></td>
<td align="left"><p>Version du client App-V. Pour obtenir la valeur correcte à utiliser, consultez le tableau suivant.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Clientos = &lt; OSStringValue&gt;</p></td>
<td align="left"><p>Système d’exploitation de l’ordinateur qui exécute le client App-V. Pour obtenir la valeur correcte à utiliser, consultez le tableau suivant.</p></td>
</tr>
</tbody>
</table>
<p> </p>
<p>Pour obtenir le nom du serveur de publication et le numéro de port (http:// &lt; PubServer &gt; : port de &lt; publication # &gt; ) à partir du client App-V, observez la configuration d’URL de l’applet de passe <strong> PowerShell Get-AppvPublishingServer </strong> .</p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64" data-raw-source="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;amp;clientos=WindowsClient_6.2_x64">http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64</a></code></p>
<p>Dans l’exemple suivant:</p>
<ul>
<li><p>Un Windows Server 2012 R2 nommé «pubsvr01» héberge le service de publication.</p></li>
<li><p>Le client Windows est Windows 8,1 64 bits.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5,0 via App-V 5,0 SP2</p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/ </code></p>
<div class="alert">
<strong>Remarque</strong><br/><p><strong>ClientVersion </strong> et les <strong> clients </strong> y sont uniquement pris en charge dans app-v 5,0 SP3 et app-v 5,1.</p>
</div>
<div>

</div></td>
<td align="left"><p>Voir les informations pour App-V 5,0 SP3 et App-V 5,1.</p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718" data-raw-source="http://pubsvr01:2718">http://pubsvr01:2718</a></code></p>
<p>Dans l’exemple, un Windows Server 2012 R2 nommé «pubsvr01» héberge les services de gestion et de publication.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-values-query-pub-meta"></a>Valeurs de requête pour le système d’exploitation client et version


Dans votre requête de métadonnées de publication, entrez les valeurs de chaîne correspondant au système d’exploitation du client et à la version que vous utilisez.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Système d’exploitation</th>
<th align="left">Architecture</th>
<th align="left">Valeur de chaîne d’exploitation</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsClient_10.0_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsClient_10.0_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsClient_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsClient_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsClient_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsClient_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WindowsServer2012R2</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsServer_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>WindowsServer2012R2</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsServer_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsServer_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsServer_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsClient_6.1_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsClient_6.1_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsServer_6.1_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsServer_6.1_x86</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-whatis-pub-metadata"></a>Définition des métadonnées de publication


Lors de la publication de packages sur un ordinateur exécutant le client App-V, des métadonnées sont envoyées à cet ordinateur pour indiquer les packages et groupes de connexion en cours de publication. Le client App-V effectue deux requêtes distinctes pour ce qui suit:

-   Des packages et des groupes de connexion habilités à l’ordinateur client;

-   Des packages et des groupes de connexion qui sont habilités à l’utilisateur actuel.

Le serveur de publication communique avec le serveur de gestion pour déterminer les packages et groupes de connexion disponibles pour le demandeur. Pour pouvoir générer les métadonnées, le serveur de publication doit être inscrit auprès du serveur de gestion.

Vous pouvez afficher les métadonnées de chaque requête dans un navigateur Internet à l’aide d’une requête qui se trouve dans le contexte de l’utilisateur ou de l’ordinateur en particulier.






## Rubriques connexes


[Référence technique pour App-V5.1](technical-reference-for-app-v-51.md)









