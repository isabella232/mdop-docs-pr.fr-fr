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
ms.openlocfilehash: 7415cf7a97edc646653df552723667bac8d25fdc
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910689"
---
# <a name="internet-facing-server-scenarios-for-perimeter-networks"></a>Scénarios de serveur accessible sur Internet pour les réseaux de périmètre


App-V 4.5 prend en charge les scénarios de serveur connecté à Internet, dans lesquels les utilisateurs qui ne sont pas connectés au réseau d’entreprise ou qui se déconnectent du réseau peuvent toujours utiliser App-V. Comme indiqué dans l’illustration suivante, seule l’utilisation de protocoles sécurisés sur Internet (RTSPS et HTTPS) est prise en charge.

![Diagramme de positionnement du pare-feu app-v.](images/appvfirewalls.gif)

Vous pouvez configurer une solution internet, à l’aide d’un serveur ISA, où l’infrastructure App-V se trouve sur le réseau interne des manières suivantes :

-   Créez une règle de publication Web pour le serveur IIS qui héberge les fichiers ICO et OSD (et éventuellement les packages pour la diffusion en continu) situés sur le réseau interne. Les étapes détaillées sont fournies dans <https://go.microsoft.com/fwlink/?LinkId=151982> .

-   Créez une règle de publication de serveur pour app-V Web Management Server (RTSPS). Les étapes détaillées sont fournies dans [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .

Comme illustré ci-après, si l’infrastructure a implémenté d’autres pare-feu entre le client et le serveur ISA ou entre le serveur ISA et le réseau interne, les règles de pare-feu RTSPS (TCP 322) et HTTPS (TCP 443) doivent être créées pour prendre en charge le flux de trafic. En outre, si des pare-feu ont été implémentés entre le serveur ISA et le réseau interne, le trafic par défaut requis pour les membres du domaine doit être autorisé à traverser le pare-feu (DNS, LDAP, Kerberos, SMB/CIFS).

![Diagramme du pare-feu du réseau de périmètre app-v.](images/appvperimeternetworkfirewall.gif)

Étant donné que les solutions de pare-feu varient d’un environnement à l’autre, les instructions fournies dans cette rubrique décrivent le trafic qui serait nécessaire pour configurer un environnement App-V internet dans le réseau de périmètre. Ces informations incluent également les serveurs réseau internes recommandés.

Placez les serveurs suivants dans le réseau de périmètre :

-   App-V Management Server

-   Serveur IIS pour la publication et la diffusion en continu

**Remarque**  
Il est préférable de placer le serveur de gestion et le serveur IIS sur des ordinateurs distincts.

 

Placez les serveurs suivants dans le réseau interne :

-   Serveur de contenu

-   Magasin de données (SQL Server)

-   Contrôleur de domaine Active Directory

## <a name="traffic-requirements"></a>Exigences en matière de trafic


Les tableaux suivants listent les exigences de trafic pour les communications à partir d’Internet et du réseau de périmètre, ainsi que du réseau de périmètre vers le réseau interne.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Exigences en matière de trafic d’Internet vers le réseau de périmètre</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>RTSPS (publication de packages d’actualisation et de diffusion en continu)</p></td>
<td align="left"><p>TCP 322 par défaut ; Cela peut être modifié dans App-V Management Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>HTTPS (publication de fichiers ICO et OSD et packages de diffusion en continu)</p></td>
<td align="left"><p>TCP 443 par défaut ; Cela peut être modifié dans la configuration IIS.</p></td>
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
<th align="left">Exigences en matière de trafic entre le réseau de périmètre et le réseau interne</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQLServer</p></td>
<td align="left"><p>TCP 1433 est la valeur par défaut, mais peut être configuré dans SQL Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SMB/CIFS</p></td>
<td align="left"><p>Si le répertoire de contenu se trouve à distance à partir du(s) serveur(s) de gestion ou du serveur IIS (recommandé).</p></td>
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
<td align="left"><p>Pour la résolution des noms des ressources internes (peut être éliminé avec l’utilisation du fichier de l’hôte sur les serveurs réseau de périmètre)</p></td>
</tr>
</tbody>
</table>

 

 

 





