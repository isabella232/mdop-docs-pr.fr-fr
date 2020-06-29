---
title: Configuration des composants du serveur MBAM2.5
description: Configuration des composants du serveur MBAM2.5
author: dansimp
ms.assetid: 894d1080-5f13-48f7-8fde-82f8d440a4ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e6ba2fc49086acf698f61b9997505c8fa884c0eb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809726"
---
# Configuration des composants du serveur MBAM2.5


Utilisez ces informations comme point de départ pour la configuration des fonctionnalités serveur d’administration et de surveillance de BitLocker (MBAM) 2,5 après [l’installation du logiciel MBAM 2,5 Server](installing-the-mbam-25-server-software.md). Vous pouvez utiliser deux méthodes pour configurer MBAM:

-   Assistant Configuration de MBAM Server

-   Cmdlets Windows PowerShell

## Avant de commencer à configurer les fonctionnalités de MBAM Server


Passez en revue et suivez les étapes ci-dessous avant de commencer à configurer les fonctionnalités du serveur MBAM:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Étape</th>
<th align="left">Où obtenir des instructions</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Passez en revue l’architecture recommandée pour MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Architecture de hautniveau pour MBAM2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Passez en revue les configurations prises en charge pour MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurations prises en charge par MBAM2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Remplissez les conditions préalables requises sur chaque serveur.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous allez configurer une fonctionnalité de MBAM Server.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installation du logiciel serveur MBAM2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Reportez-vous aux conditions préalables à l’utilisation de Windows PowerShell pour configurer les fonctionnalités du serveur MBAM (si vous utilisez cette méthode pour configurer les fonctionnalités du serveur MBAM).</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>

 

## Étapes de configuration des fonctionnalités de MBAM Server


Chaque ligne du tableau suivant décrit les fonctionnalités que vous allez configurer sur un serveur distinct, selon l' [architecture de niveau supérieur recommandée pour MBAM 2,5](high-level-architecture-for-mbam-25.md).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Fonctionnalités à installer</th>
<th align="left">Où obtenir des instructions</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configurez les bases de données.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Comment configurer les bases de données MBAM2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurez les rapports.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Configuration des rapports MBAM2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurez les applications Web.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Comment configurer les applications Web MBAM2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurer l’intégration de System Center Configuration Manager (le cas échéant).</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">Comment configurer l'intégration de MBAM2.5 à System Center Configuration Manager</a></p></td>
</tr>
</tbody>
</table>

 

Pour obtenir la liste des événements sur la configuration des fonctionnalités de MBAM Server, voir [journaux des événements serveur](server-event-logs.md).



## Rubriques connexes


Configuration des composants du serveur MBAM2.5
 

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




