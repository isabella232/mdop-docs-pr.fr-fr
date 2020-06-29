---
title: Planification de votre solution de diffusion en continu dans une implémentation de distribution électronique de logiciels
description: Planification de votre solution de diffusion en continu dans une implémentation de distribution électronique de logiciels
author: dansimp
ms.assetid: bc18772a-f169-486f-adb1-7af1a31845aa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c49d6fc0b5f8f5dee347ead3bb899ce9b0387024
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806474"
---
# Planification de votre solution de diffusion en continu dans une implémentation de distribution électronique de logiciels


Si vous décidez d’utiliser des serveurs de diffusion en conjonction avec votre système de maintenance ESD pour rendre le contenu de l’application disponible pour les ordinateurs des utilisateurs finaux, vous pouvez choisir parmi plusieurs options, tout en tirant parti de l’infrastructure qui est déjà en place. Par exemple, si votre système ESD comporte des partages de logiciels de distribution de logiciels sur des serveurs dans les succursales de votre domaine, vous pouvez placer le partage de l’application virtualisation \\CONTENT sur ces serveurs, puis configurer les clients pour qu’ils utilisent ce partage de contenu comme source de contenu de l’application. L’utilisation des options prises en charge consiste à utiliser un serveur de fichiers ou un serveur IIS. Vous pouvez également installer le serveur de diffusion en continu d’applications sur un serveur de fichiers ou un serveur IIS existant.

Le serveur de diffusion en continu d’applications prend en charge la fonctionnalité de mise à niveau active de la virtualisation des applications. La fonction de mise à niveau active vous permet d’ajouter une nouvelle version d’une application à un serveur d’administration d’applications ou un serveur de diffusion en continu sans affecter les utilisateurs exécutant l’application. Les clients App-V recevront automatiquement la version la plus récente de l’application à partir du serveur de gestion App-V ou du serveur de streaming lors du prochain démarrage de l’application par l’utilisateur. L’utilisation du protocole RTSP (S) est nécessaire pour cette fonctionnalité. Si vous choisissez de ne pas utiliser le serveur de diffusion en continu d’applications, vous devrez gérer explicitement les mises à jour de package d’application à l’aide du système ESD.

**Remarques**  L’accès aux applications est contrôlé par le biais des groupes de sécurité dans les services de domaine Active Directory (AD FS), vous devez donc planifier un processus de configuration d’un groupe de sécurité pour chaque application virtuelle et de gestion des utilisateurs ajoutés à chaque groupe. L’administrateur système de virtualisation des applications configure chaque serveur en streaming pour utiliser ces groupes Active Directory en appliquant des LCA aux répertoires de l’application sous le partage de contenu, qui contrôle l’accès aux packages en fonction de l’appartenance aux groupes Active Directory.

 

Les caractéristiques des options de streaming disponibles sont résumées dans le tableau suivant.

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
<td align="left"><p><a href="how-to-configure-the-application-virtualization-management-servers.md" data-raw-source="[How to Configure the Application Virtualization Management Servers](how-to-configure-the-application-virtualization-management-servers.md)">Procédure pour configurer les serveurs Application Virtualization Management Server</a></p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Procédure pour configurer des serveurs pour un déploiement basé sur ESD](how-to-configure-servers-for-esd-based-deployment.md)

[Vue d'ensemble de la sécurité et de la protection](security-and-protection-overview.md)

[Publication d'applications virtuelles à l'aide de la distribution électronique de logiciels](publishing-virtual-applications-using-electronic-software-distribution.md)

 

 





