---
title: Configurations prises en charge d'App-V5.0 SP3
description: Configurations prises en charge d'App-V5.0 SP3
author: dansimp
ms.assetid: 08ced79a-0ed3-43c3-82e7-de01c1f33e81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b5a8858c703add3dc84c7eed4f62aa97e60ec9b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805994"
---
# Configurations prises en charge d'App-V5.0 SP3


Cette rubrique spécifie la configuration requise pour l’installation et l’exécution de Microsoft Application Virtualization (App-V) 5,0 SP3 dans votre environnement.

## Configuration système requise pour App-V Server


Cette section répertorie le système d’exploitation et la configuration matérielle requise pour tous les composants App-V Server.

### Scénarios de serveur App-V 5,0 SP3 non pris en charge

Le serveur App-V 5,0 SP3 ne prend pas en charge les scénarios suivants:

-   Déploiement sur un ordinateur exécutant Microsoft Windows Server Core.

-   Déploiement sur un ordinateur qui exécute une version antérieure des composants serveur App-V 5,0 SP3. Vous pouvez installer l’application-V 5,0 SP3 côte à côte avec le serveur application-V 4.5 Lightweight Streaming Server (LWS) uniquement. Le déploiement d’App-V côte à côte avec le serveur de gestion des services d’application (HWS) App-V 4,5 n’est pas pris en charge.

-   Déploiement sur un ordinateur qui exécute Microsoft SQL Server Express Edition.

-   Déploiement distant de la base de données du serveur de gestion ou de la base de données de création de rapports. Vous devez exécuter le programme d’installation directement sur l’ordinateur exécutant Microsoft SQL Server.

-   Déploiement sur un contrôleur de domaine.

-   Chemins courts. Si vous envisagez d’utiliser un chemin court, vous devez créer un nouveau volume.

### Configuration requise pour le système d’exploitation de Management Server

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du serveur de gestion de l’application-V 5,0 SP3.

**Remarques**  Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975). Pour plus d’informations, consultez le [Forum aux questions sur la politique de support du support technique Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976) .

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Système d’exploitation</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

**Important**  Le déploiement du rôle serveur de gestion sur un ordinateur sur lequel le partage de bureau à distance est activé n’est pas pris en charge.

 

### <a href="" id="management-server-hardware-requirements-"></a>Configuration matérielle requise pour le serveur de gestion

-   Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)

-   RAM: 1 Go de RAM (64 bits)

-   Disque dur: 200 Mo d’espace disque disponible sans le répertoire de contenu

### Exigences de base de données du serveur de gestion

Le tableau suivant répertorie les versions de SQL Server prises en charge pour l’installation de la base de données de gestion App-V 5,0 SP3.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version de SQL Server</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MicrosoftSQLServer2014</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftSQLServer 2012</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>3</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
</tbody>
</table>

 

### Configuration requise du système d’exploitation du serveur de publication

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du serveur de publication App-V 5,0 SP3.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Système d’exploitation</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="publishing-server-hardware-requirements-"></a>Configuration matérielle requise pour le serveur de publication

App-V n’ajoute aucune configuration requise supplémentaire au-delà de celles de Windows Server.

-   Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)

-   RAM: 2 Go de RAM (64 bits)

-   Disque dur: 200 Mo d’espace disque disponible sans le répertoire de contenu

### Configuration requise pour le système d’exploitation du serveur de rapports

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du serveur de création de rapports App-V 5,0 SP3.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Système d’exploitation</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="reporting-server-hardware-requirements-"></a>Configuration matérielle requise pour le serveur de création de rapports

App-V n’ajoute aucune configuration requise supplémentaire au-delà de celles de Windows Server.

-   Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)

-   RAM: 2 Go de RAM (64 bits)

-   Espace disque disponible: 200 Mo d’espace disque disponible

### Configuration requise pour la base de données serveur de rapport

Le tableau suivant répertorie les versions de SQL Server prises en charge pour l’installation de la base de données de création de rapports App-V 5,0 SP3.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version de SQL Server</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MicrosoftSQLServer2014</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftSQLServer 2012</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>3</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-client-supp-cfgs"></a>Configuration système requise pour le client App-V


Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client App-V 5,0 SP3.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Système d’exploitation</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows8</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Plus de.</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
</tbody>
</table>

 

Les scénarios d’installation du client App-V suivants ne sont pas pris en charge, sauf comme indiqué:

-   Ordinateurs exécutant Windows Server

-   Ordinateurs exécutant App-V 4.6 SP1 ou une version antérieure

-   Le client App-V 5,0 SP3 service bureau à distance est uniquement pris en charge pour les serveurs RDS

### <a href="" id="app-v-client-hardware-requirements-"></a>Configuration matérielle requise pour le client App-V

La liste suivante présente la configuration matérielle prise en charge pour l’installation du client App-V 5,0 SP3.

-   Processeur: 1,4 GHz ou supérieur 32 bits (x86) ou processeur 64 bits (x64)

-   RAM: 1 Go (32 bits) ou 2 Go (64 bits)

-   Disque: 100 Mo pour l’installation, sans compter l’espace disque utilisé par les applications virtualisées.

## Configuration système requise pour le client Bureau à distance


Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client App-V 5,0 SP3 (Bureau à distance).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Système d’exploitation</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

### Configuration matérielle requise pour le client Bureau à distance

App-V n’ajoute aucune configuration requise supplémentaire au-delà de celles de Windows Server.

-   Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)

-   RAM: 2 Go de RAM (64 bits)

-   Espace disque disponible: 200 Mo d’espace disque disponible

## Configuration requise pour le Sequencer


Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de Sequencer App-V 5,0 SP3.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Système d’exploitation</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server2012 R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server2012</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits et 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows8</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits et 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits et 64bits</p></td>
</tr>
</tbody>
</table>

 

### Configuration matérielle requise pour le Sequencer

Pour connaître la configuration matérielle requise, voir la documentation de Windows ou Windows Server. App-V n’ajoute aucune configuration matérielle supplémentaire.

## <a href="" id="bkmk-supp-ver-sccm"></a>Versions prises en charge de System Center Configuration Manager


Le client App-V prend en charge les versions suivantes de System Center Configuration Manager:

-   MicrosoftSystemCenter2012 ConfigurationManager

-   System Center2012R2 Configuration Manager

-   System Center2012R2 ConfigurationManagerSP1

Pour plus d’informations sur l’intégration de Configuration Manager à l’application-V, voir [planification de l’intégration d’App-v à la Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).






## Rubriques connexes


[Envisager de déployer App-V](planning-to-deploy-app-v.md)

[Composants requis d'App-V5.0 SP3](app-v-50-sp3-prerequisites.md)

 

 





