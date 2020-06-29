---
title: Scénarios de serveur accessible sur Internet pour les réseaux de périmètre
description: Scénarios de serveur accessible sur Internet pour les réseaux de périmètre
author: dansimp
ms.assetid: 8a4da6e6-82c7-49e5-b9b1-1666cba02f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fcb04e651341fa107c358eaabbd7992d7ea155ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806645"
---
# Scénarios de serveur accessible sur Internet pour les réseaux de périmètre


App-V 4.5 prend en charge les scénarios de serveur Internet, dans lesquels les utilisateurs qui ne sont pas connectés au réseau d’entreprise ou qui se déconnectent du réseau peuvent continuer à utiliser App-V. Comme indiqué dans l’illustration suivante, seules les protocoles sécurisés sur Internet (RTSP et HTTPs) sont pris en charge.

![diagramme de positionnement de pare-feu App-v](images/appvfirewalls.gif)

Vous pouvez configurer une solution Internet à l’aide d’un serveur ISA sur lequel l’infrastructure App-V se trouve sur le réseau interne comme suit:

-   Créez une règle de publication Web pour le serveur IIS qui héberge les fichiers ICO et OSD (et éventuellement les packages de diffusion en continu) situés sur le réseau interne. Des étapes détaillées sont disponibles à l’adresse <https://go.microsoft.com/fwlink/?LinkId=151982> .

-   Créer une règle de publication de serveur pour le serveur de gestion des applications (RTSP). Des étapes détaillées sont disponibles à l’adresse [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .

Comme le montre l’illustration ci-dessous, si l’infrastructure a implémenté d’autres pare-feu entre le client et le serveur ISA ou entre le serveur ISA et le réseau interne, vous devez créer des règles de pare-feu RTSP (TCP 322) et HTTPs (TCP 443) pour prendre en charge le flux de trafic. De plus, si des pare-feu sont implémentés entre le serveur ISA et le réseau interne, le trafic par défaut requis pour les membres du domaine doit être autorisé à effectuer un tunnel via le pare-feu (DNS, LDAP, Kerberos, SMB/CIFS).

![diagramme de pare-feu du réseau de périmètre App-v](images/appvperimeternetworkfirewall.gif)

Étant donné que les solutions de pare-feu varient d’un environnement à un environnement, les recommandations fournies dans cette rubrique décrivent le trafic requis pour configurer un environnement App-V dans le réseau de périmètre. Ces informations incluent également les serveurs réseau internes recommandés.

Placez les serveurs suivants dans le réseau de périmètre:

-   Serveur de gestion App-V

-   Serveur IIS pour la publication et la diffusion en continu

**Remarques**  Il est recommandé de placer le serveur de gestion et le serveur IIS sur des ordinateurs séparés.

 

Placez les serveurs suivants sur le réseau interne:

-   Serveur de contenu

-   Magasin de données (SQL Server)

-   Contrôleur de domaine Active Directory

## Exigences en matière de trafic


Les tableaux suivants répertorient les exigences en matière de trafic pour la communication à partir d’Internet et du réseau de périmètre, et du réseau de périmètre au réseau interne.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Exigences en matière de trafic entre Internet et le réseau de périmètre</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>RTSP (actualisation de publication et packages de diffusion en continu)</p></td>
<td align="left"><p>TCP 322 par défaut; vous pouvez le modifier dans le serveur de gestion App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>HTTPs (publication des fichiers. ICO et OSD et des packages de diffusion en continu)</p></td>
<td align="left"><p>TCP 443 par défaut; ce problème peut être modifié dans la configuration IIS.</p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Exigences en matière de trafic du réseau de périmètre vers réseau interne</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQLServer</p></td>
<td align="left"><p>TCP 1433 est la valeur par défaut, mais elle peut être configurée dans SQL Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SMB/CIFS</p></td>
<td align="left"><p>Si le répertoire de contenu se trouve à distance à partir du ou du serveur de gestion ou du serveur IIS (recommandé).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kerberos</p></td>
<td align="left"><p>TCP et UDP 88</p></td>
</tr>
<tr class="even">
<td align="left"><p>LDAP</p></td>
<td align="left"><p>TCP et UDP 389</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DNS</p></td>
<td align="left"><p>Pour la résolution de noms des ressources internes (qui peuvent être éliminées lors de l’utilisation du fichier hôte sur les serveurs de réseau de périmètre);</p></td>
</tr>
</tbody>
</table>

 

 

 





