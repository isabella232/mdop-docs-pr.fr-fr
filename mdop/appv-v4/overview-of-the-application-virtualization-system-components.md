---
title: Présentation des composants du système Application Virtualization
description: Présentation des composants du système Application Virtualization
author: dansimp
ms.assetid: 75d88ef7-44d8-4fa7-b7f5-9153f37e570d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cab0065b9966094da687cce2f5e94069922189fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806553"
---
# Présentation des composants du système Application Virtualization


Le tableau suivant décrit les principaux composants du système de gestion de Microsoft Application Virtualization. Pour plus d’informations sur le déploiement de ces composants système, voir [scénario basé sur un serveur de virtualisation des applications](application-virtualization-server-based-scenario.md).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Composant</th>
<th align="left">Fonction</th>
<th align="left">Informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Serveur de gestion de Microsoft Application Virtualization</p></td>
<td align="left"><p>Composant responsable de la diffusion du contenu du package et de la publication des raccourcis et des associations de types de fichiers sur le client de virtualisation des applications.</p></td>
<td align="left"><p>Le serveur de gestion des applications virtuelles prend en charge la mise à niveau active, la gestion des licences et une base de données qui peut être utilisée pour la création de rapports.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Dossier de contenu </strong></p></td>
<td align="left"><p>Emplacement des packages de virtualisation d’application pour la diffusion en continu.</p></td>
<td align="left"><p>Ce dossier peut être localisé sur un serveur de gestion de la virtualisation des applications. Le dossier peut également être placé sur un réseau de zone de stockage (SAN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization Management Console</p></td>
<td align="left"><p>Utilitaire de gestion des composants enfichables 3,0 de MMC pour l’administration de serveur Microsoft Application Virtualization.</p></td>
<td align="left"><p>Ce composant peut être installé sur le serveur Microsoft Application Virtualization Server ou situé sur une station de travail distincte qui dispose de MMC 3.0 et. .NET 2.0 installé.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Service Web de gestion de Microsoft Application Virtualization</p></td>
<td align="left"><p>Composant responsable de la communication de toutes les demandes en lecture/écriture dans le magasin de données de virtualisation des applications.</p></td>
<td align="left"><p>Ce composant peut être installé sur le serveur Microsoft Application Virtualization ou sur un autre ordinateur sur lequel IIS est installé.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Magasin de données de Microsoft Application Virtualization</p></td>
<td align="left"><p>Composant stocké dans la base de données SQL et responsable du stockage de toutes les informations liées à l’infrastructure de virtualisation des applications.</p></td>
<td align="left"><p>Ces informations incluent tous les enregistrements d’application, les affectations d’application et les groupes responsables de la gestion de l’environnement de virtualisation des applications.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Serveur de diffusion de Microsoft Application Virtualization</p></td>
<td align="left"><p>Composant responsable de l’hébergement des packages de virtualisation d’application destinés à la diffusion en continu vers les clients d’une succursale, où le lien retour vers le serveur de gestion des applications est considéré comme un réseau étendu.</p></td>
<td align="left"><p>Ce serveur est doté de la fonctionnalité de diffusion en continu uniquement et ne fournit ni la console de gestion des applications virtuelles, ni le service Web de gestion des applications.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sequencer Microsoft Application Virtualization</p></td>
<td align="left"><p>Composant utilisé pour surveiller et capturer l’installation des applications afin de créer des packages d’application virtuelle.</p></td>
<td align="left"><p>La sortie se compose des icônes de l’application, d’un fichier OSD contenant des informations de définition de package, d’un fichier de manifeste de package et du fichier SFT contenant les fichiers de contenu du programme d’application.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client Microsoft Application Virtualization</p></td>
<td align="left"><p>Composants installés sur le client de bureau de virtualisation des applications ou sur le client de virtualisation d’application pour les services Bureau à distance (anciennement services Terminal Server) et qui fournit l’environnement virtuel pour les applications virtualisées.</p></td>
<td align="left"><p>Le client de virtualisation d’applications Microsoft gère la diffusion du package dans le cache, l’actualisation de la publication, le transport et toute interaction avec les serveurs de virtualisation des applications.</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Scénario basé sur un serveur Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Planification de votre solution de diffusion en continu dans une implémentation basée sur un serveur Application Virtualization Server](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

[Publication d'applications virtuelles à l'aide de serveurs Application Virtualization Management Server](publishing-virtual-applications-using-application-virtualization-management-servers.md)

 

 





