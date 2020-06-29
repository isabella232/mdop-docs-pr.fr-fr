---
title: Choisir une méthode de diffusion en continu
description: Choisir une méthode de diffusion en continu
author: dansimp
ms.assetid: 50d5e0ec-7f48-4cea-8711-5882bd89153b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0acfd345ac55f11476cffe94b3a95b13c5d8f303
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808892"
---
# Choisir une méthode de diffusion en continu


Lorsque l’utilisateur double-clique pour la première fois sur l’icône placée sur un ordinateur par le biais du processus de publication, le client de virtualisation d’application obtiendra le contenu du package d’application virtuelle à partir d’un emplacement de source de flux.

**Remarques** 
 *Streaming* est le terme utilisé pour décrire le processus d’obtention de contenu à partir d’un package d’application séquencé, en commençant par le bloc de fonctionnalités principal et en obtenant des blocs supplémentaires selon les besoins.

 

En général, l’emplacement de la source est un serveur accessible à partir de l’ordinateur de l’utilisateur. Toutefois, certains systèmes de distribution électronique, tels que Microsoft Endpoint Configuration Manager, peuvent distribuer le fichier SFT sur l’ordinateur de l’utilisateur, puis diffuser le package de l’application virtuelle localement à partir du cache de l’ordinateur.

**Remarques**  Un emplacement de source de flux pour les packages virtuels peut être configuré sur un ordinateur qui n’est pas un serveur. Cette fonction est particulièrement utile dans les petites succursales qui n’ont pas de serveur.

 

Les sources de flux continu qui peuvent être utilisées pour stocker des applications séquencées sont décrites dans le tableau suivant.

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
<td align="left"><p>Fichier</p></td>
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
<li><p>Prend en charge la sécurité améliorée via le protocole HTTPs.</p></li>
<li><p>Prend en charge la diffusion en continu sur des ordinateurs distants via Internet</p></li>
<li><p>Un seul port du pare-feu pour s’ouvrir</p></li>
<li><p>Haute évolutivité</p></li>
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
<li><p>Un seul port dans le pare-feu pour s’ouvrir (RTSP uniquement)</p></li>
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


[Scénario basé sur une distribution électronique de logiciels](electronic-software-distribution-based-scenario.md)

[Présentation du scénario basé sur une distribution électronique de logiciels](electronic-software-distribution-based-scenario-overview.md)

[Choisir une méthode de publication](determine-your-publishing-method.md)

 

 





