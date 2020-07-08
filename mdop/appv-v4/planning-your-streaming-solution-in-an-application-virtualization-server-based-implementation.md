---
title: Planification de votre solution de diffusion en continu dans une implémentation basée sur un serveur Application Virtualization Server
description: Planification de votre solution de diffusion en continu dans une implémentation basée sur un serveur Application Virtualization Server
author: dansimp
ms.assetid: 3a57306e-5c54-4fde-8593-fe3b788f18d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d315f554eb99fc5c05c231630eaa41d4f505535
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806478"
---
# Planification de votre solution de diffusion en continu dans une implémentation basée sur un serveur Application Virtualization Server


Si vous souhaitez utiliser des serveurs de diffusion de la virtualisation des applications conjointement avec votre implémentation basée sur le serveur de gestion des applications, vous avez le choix entre plusieurs options, tout en tirant parti de l’infrastructure déjà en place. Par exemple, si vous avez déjà des serveurs dans les succursales de votre champ, vous pouvez placer le partage d’application \\CONTENT de partage sur ces serveurs, puis configurer ces derniers pour qu’ils utilisent ce partage de contenu en tant que source de contenu de l’application. Si vous choisissez d’utiliser uniquement des serveurs de gestion de la virtualisation des applications (par exemple, vous n’avez qu’un seul bureau), les clients peuvent diffuser du contenu de ce serveur.

Les options prises en charge sont notamment l’utilisation d’un serveur de fichiers, d’un serveur IIS ou d’un serveur de diffusion de la virtualisation des applications. Vous pouvez également installer le serveur de diffusion en continu d’applications sur un serveur de fichiers ou un serveur IIS existant. Les caractéristiques de ces différentes options sont résumées dans le tableau suivant.

**Remarques**  La fonction de mise à niveau active vous permet d’ajouter une nouvelle version d’une application à un serveur d’administration d’applications ou un serveur de diffusion en continu sans affecter les utilisateurs exécutant l’application. Les clients App-V recevront automatiquement la version la plus récente de l’application à partir du serveur de gestion App-V ou du serveur de streaming lors du prochain démarrage de l’application par l’utilisateur. L’utilisation du protocole RTSP (S) est nécessaire pour cette fonctionnalité.

 

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Type de serveur</th>
<th align="left">Protocole</th>
<th align="left">Avantages</th>
<th align="left">Inconvénients</th>
<th align="left">Liens</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Serveur de fichiers</p></td>
<td align="left"><p>SMB</p></td>
<td align="left"><ul>
<li><p>Solution simple et abordable pour configurer un serveur de fichiers existant avec le partage \CONTENT</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Aucune mise à niveau active</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-file-server.md" data-raw-source="[How to Configure the File Server](how-to-configure-the-file-server.md)">Procédure pour configurer le serveur de fichiers</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Serveur IIS</p></td>
<td align="left"><p>HTTP/HTTPS</p></td>
<td align="left"><ul>
<li><p>Prend en charge la sécurité améliorée via le protocole HTTPs</p></li>
<li><p>Prend en charge la diffusion en continu sur des ordinateurs distants via Internet</p></li>
<li><p>Un seul port du pare-feu pour s’ouvrir</p></li>
<li><p>Evolutive</p></li>
<li><p>Protocole familier</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Vous devez gérer les services Internet (IIS)</p></li>
<li><p>Aucune mise à niveau active</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-server-for-iis.md" data-raw-source="[How to Configure the Server for IIS](how-to-configure-the-server-for-iis.md)">Procédure pour configurer le serveur IIS</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Serveur de streaming de la virtualisation des applications</p></td>
<td align="left"><p>RTSP/RTSP</p></td>
<td align="left"><ul>
<li><p>Mise à niveau active</p></li>
<li><p>Prend en charge la sécurité améliorée à l’aide du protocole RTSP</p></li>
<li><p>Un seul port du pare-feu pour s’ouvrir</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Double infrastructure</p></li>
<li><p>Configuration requise pour l’administration du serveur</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-streaming-servers.md" data-raw-source="[How to Configure the Application Virtualization Streaming Servers](how-to-configure-the-application-virtualization-streaming-servers.md)">Procédure pour configurer les serveurs Application Virtualization Streaming Server</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Serveur de gestion Application Virtualization</p></td>
<td align="left"><p>RTSP/RTSP</p></td>
<td align="left"><ul>
<li><p>Mise à niveau active</p></li>
<li><p>Prend en charge la sécurité améliorée à l’aide du protocole RTSP</p></li>
<li><p>Un seul port du pare-feu pour s’ouvrir</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Double infrastructure</p></li>
<li><p>Configuration requise pour l’administration du serveur</p></li>
</ul></td>
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)">Procédure pour configurer les serveurs Application Virtualization Management Server</a></p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Scénario basé sur un serveur Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Présentation des composants du système Application Virtualization](overview-of-the-application-virtualization-system-components.md)

[Publication d'applications virtuelles à l'aide de serveurs Application Virtualization Management Server](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





