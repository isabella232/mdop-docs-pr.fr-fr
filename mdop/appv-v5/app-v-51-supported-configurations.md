---
title: Configurations prises en charge par App-V5.1
description: Configurations prises en charge par App-V5.1
author: dansimp
ms.assetid: 8b8db63b-f71c-4ae9-80e7-a6752334e1f6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/02/2020
ms.openlocfilehash: fbda364de66b1f7b8730dca38f864a84f7848e58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805941"
---
# Configurations prises en charge par App-V5.1

>S’applique à: Windows 10, version 1607; Windows Server 2019; Windows Server 2016; Windows Server 2012 R2; Windows Server 2012; Windows Server 2008 R2 (mise à jour de sécurité étendue)

Cette rubrique spécifie la configuration requise pour l’installation et l’exécution de Microsoft Application Virtualization (App-V) 5,1 dans votre environnement.

## Configuration système requise pour App-V Server

Cette section répertorie le système d’exploitation et la configuration matérielle requise pour tous les composants App-V Server.

### Scénarios App-V 5,1 Server non pris en charge

Le serveur App-V 5,1 ne prend pas en charge les scénarios suivants:

-   Déploiement sur un ordinateur exécutant Microsoft Windows Server Core.

-   Déploiement sur un ordinateur qui exécute une version antérieure des composants serveur App-V 5,1. Vous pouvez installer l’application-V 5,1 côte à côte avec l’App-V 4.5 Lightweight Streaming Server (LWS) uniquement. Le déploiement d’App-V côte à côte avec le serveur de gestion des services d’application (HWS) App-V 4,5 n’est pas pris en charge.

-   Déploiement sur un ordinateur qui exécute Microsoft SQL Server Express Edition.

-   Déploiement sur un contrôleur de domaine.

-   Chemins courts. Si vous envisagez d’utiliser un chemin court, vous devez créer un nouveau volume.

### Configuration requise pour le système d’exploitation de Management Server

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation d’App-V 5,1 Management Server.

> [!NOTE]
> Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975). Pour plus d’informations, consultez le [Forum aux questions sur la politique de support du support technique Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976) .

 | Systèmed’exploitation                 | Service Pack | Architecture système |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bits       |
| Microsoft Windows Server 2016    |              |        64 bits       |
| Microsoft Windows Server 2012 R2 |              |        64 bits       |
| Microsoft Windows Server 2012    |              |        64 bits       |
| [Mise à jour de sécurité étendue](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2|      SP1     |        64 bits       |
 

**Important**  Le déploiement du rôle serveur de gestion sur un ordinateur sur lequel le partage de bureau à distance est activé n’est pas pris en charge.

 

### <a href="" id="management-server-hardware-requirements-"></a>Configuration matérielle requise pour le serveur de gestion

-   Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)

-   RAM: 1 Go de RAM (64 bits)

-   Disque dur: 200 Mo d’espace disque disponible sans le répertoire de contenu

### Exigences de base de données du serveur de gestion

Le tableau suivant répertorie les versions de SQL Server prises en charge pour l’installation de la base de données de gestion App-V 5,1.

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
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2019</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>

<tr class="odd">
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftSQLServer2016</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MicrosoftSQLServer2014</p></td>
<td align="left"><p>SP2</p></td>
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

Pour plus d’informations sur les fichiers de configuration utilisateur avec SQL Server 2016 ou une version ultérieure, voir l' [article de support technique](https://support.microsoft.com/help/4548751/app-v-server-publishing-might-fail-when-you-apply-user-configuration-f).

### Configuration requise du système d’exploitation du serveur de publication

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de serveur de publication 5,1 App-V.

| Systèmed’exploitation                 | Service Pack | Architecture système |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bits       |
| Microsoft Windows Server 2016    |              |        64 bits       |
| Microsoft Windows Server 2012 R2 |              |        64 bits       |
| Microsoft Windows Server 2012    |              |        64 bits       |
| [Mise à jour de sécurité étendue](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2 |      SP1     |        64 bits       |

### <a href="" id="publishing-server-hardware-requirements-"></a>Configuration matérielle requise pour le serveur de publication

App-V n’ajoute aucune configuration requise supplémentaire au-delà de celles de Windows Server.

-   Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)

-   RAM: 2 Go de RAM (64 bits)

-   Disque dur: 200 Mo d’espace disque disponible sans le répertoire de contenu

### Configuration requise pour le système d’exploitation du serveur de rapports

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de serveur de création de rapports App-V 5,1.

| Systèmed’exploitation                 | Service Pack | Architecture système |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bits       |
| Microsoft Windows Server 2016    |              |        64 bits       |
| Microsoft Windows Server 2012 R2 |              |        64 bits       |
| Microsoft Windows Server 2012    |              |        64 bits       |
| [Mise à jour de sécurité étendue](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2 |      SP1     |        64 bits       |

### <a href="" id="reporting-server-hardware-requirements-"></a>Configuration matérielle requise pour le serveur de création de rapports

App-V n’ajoute aucune configuration requise supplémentaire au-delà de celles de Windows Server.

-   Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)

-   RAM: 2 Go de RAM (64 bits)

-   Espace disque disponible: 200 Mo d’espace disque disponible

### Configuration requise pour la base de données serveur de rapport

Le tableau suivant répertorie les versions de SQL Server prises en charge pour l’installation de la base de données de création de rapports App-V 5,1.

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
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftSQLServer2016</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MicrosoftSQLServer2014</p></td>
<td align="left"><p>SP2</p></td>
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

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client App-V 5,1.

> [!NOTE]
> Dans le cadre de la mise à jour anniversaire Windows 10 (c’est-à-dire la version 1607), le client App-V est en cours de blocage de l’installation de toute version antérieure du client App-V.

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
<td align="left"><p>Microsoft Windows 10 (version antérieure à 1607)</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8.1</p></td>
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

-   Le client App-V 5,1 Bureau à distance est uniquement pris en charge pour les serveurs RDS

### <a href="" id="app-v-client-hardware-requirements-"></a>Configuration matérielle requise pour le client App-V

La liste suivante présente la configuration matérielle prise en charge pour l’installation du client App-V 5,1.

-   Processeur: 1,4 GHz ou supérieur 32 bits (x86) ou processeur 64 bits (x64)

-   RAM: 1 Go (32 bits) ou 2 Go (64 bits)

-   Disque: 100 Mo pour l’installation, sans compter l’espace disque utilisé par les applications virtualisées.

## Configuration système requise pour le client Bureau à distance


Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client App-V 5,1 Desktop Services (RDS).

| Systèmed’exploitation                 | Service Pack | Architecture système |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bits       |
| Microsoft Windows Server 2016    |              |        64 bits       |
| Microsoft Windows Server 2012 R2 |              |        64 bits       |
| Microsoft Windows Server 2012    |              |        64 bits       |
| [Mise à jour de sécurité étendue](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2 |      SP1     |        64 bits       |

### Configuration matérielle requise pour le client Bureau à distance

App-V n’ajoute aucune configuration requise supplémentaire au-delà de celles de Windows Server.

-   Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)

-   RAM: 2 Go de RAM (64 bits)

-   Espace disque disponible: 200 Mo d’espace disque disponible

## Configuration requise pour le Sequencer

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de Sequencer App-V 5,1.

| Systèmed’exploitation                 | Service Pack | Architecture système |
|----------------------------------|--------------|---------------------|
| Microsoft Windows Server 2019    |              |        64 bits       |
| Microsoft Windows Server 2016    |              |        64 bits       |
| Microsoft Windows Server 2012 R2 |              |        64 bits       |
| Microsoft Windows Server 2012    |              |        64 bits       |
| [Mise à jour de sécurité étendue](https://www.microsoft.com/windows-server/extended-security-updates) Microsoft Windows Server 2008 R2 |      SP1     |        64 bits       |
| Microsoft Windows 10             |              | 32bits et 64bits   |
| Microsoft Windows 8,1            |              | 32bits et 64bits   |
| Microsoft Windows 7              |      SP1     | 32bits et 64bits   |

### Configuration matérielle requise pour le Sequencer

Pour connaître la configuration matérielle requise, voir la documentation de Windows ou Windows Server. App-V n’ajoute aucune configuration matérielle supplémentaire.

## <a href="" id="bkmk-supp-ver-sccm"></a>Versions prises en charge de System Center Configuration Manager

Le client App-V prend en charge les versions suivantes de System Center Configuration Manager:

-   MicrosoftSystemCenter2012 ConfigurationManager

-   System Center2012R2 Configuration Manager

-   System Center2012R2 ConfigurationManagerSP1

Les matrices de version de l’application-V et System Center Configuration Manager suivantes montrent toutes les combinaisons officiellement prises en charge par App-V et Configuration Manager.

> [!NOTE]
> La prise en charge standard de l’application-V 4,5 et 4,6 a été fermée.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version App-V</th>
<th align="left">System Center Configuration Manager 2007</th>
<th align="left">SystemCenter2012 ConfigurationManager</th>
<th align="left">SystemCenter2012 ConfigurationManagerSP1</th>
<th align="left">System Center2012R2 Configuration Manager</th>
<th align="left">System Center2012R2 ConfigurationManagerSP1</th>
<th align="left">SystemCenter2012 ConfigurationManagerSP2</th>
<th align="left">System Center Configuration Manager version 1511</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 SP3</p></td>
<td align="left"><p>MSI-wrapper uniquement</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>2012 SP1 CU4</p></td>
<td align="left"><p>2012 R2 CU1</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5.1</p></td>
<td align="left"><p>MSI-wrapper uniquement</p></td>
<td align="left"><p>Non</p></td>
<td align="left"><p>2012 SP1 CU4</p></td>
<td align="left"><p>2012 R2 CU1</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Oui</p></td>
</tr>
</tbody>
</table>

 

Pour plus d’informations sur l’intégration de Configuration Manager à l’application-V, voir [planification de l’intégration d’App-v à la Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).

## Rubriques connexes

[Envisager de déployer App-V](planning-to-deploy-app-v51.md)

[Composants requis d'App-V5.1](app-v-51-prerequisites.md)
