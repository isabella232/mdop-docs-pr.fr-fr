---
title: Configurations prises en charge par MBAM2.0
description: Configurations prises en charge par MBAM2.0
author: dansimp
ms.assetid: dca63391-39fe-4273-a570-76d0a2f8a0fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8f314adcf818c1bdb17b0b239a7469f97fa849e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810236"
---
# Configurations prises en charge par MBAM2.0


Cette rubrique spécifie la configuration requise pour l’installation et l’exécution de Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 dans votre environnement via la topologie autonome. Pour les configurations prises en charge qui s’appliquent aux versions ultérieures, consultez la documentation de la version en vigueur.

Si vous envisagez d’installer MBAM 2,0 à l’aide de la topologie de Configuration Manager et que vous souhaitez consulter une liste de la configuration système requise, voir [planification du déploiement d’MBAM avec Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

La configuration recommandée pour l’exécution de MBAM dans un environnement de production consiste à utiliser deux serveurs, en fonction de vos besoins en matière d’évolutivité. Cette configuration prend en charge jusqu’à 200 000 clients MBAM. Pour obtenir une image et des descriptions de l’infrastructure de serveur MBAM autonome, voir [architecture de haut niveau pour MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).

**Remarques**  Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975). Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).

 

## <a href="" id="---------mbam-server-system-requirements"></a> Configuration système requise pour MBAM Server


### Configuration requise du système d’exploitation serveur

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du serveur d’administration et de surveillance de BitLocker.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Système d’exploitation</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsServer2008 R2</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>WindowsServer2012</p></td>
<td align="left"><p>Edition standard ou Datacenter</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

**Remarques**  Il n’y a pas de prise en charge pour l’installation des services ou des rapports MBAM sur un ordinateur contrôleur de domaine.

 

### <a href="" id="server-processor--ram--and-disk-space-requirements-"></a>Exigences relatives au processeur du serveur, à la RAM et à l’espace disque

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Composant matériel</th>
<th align="left">Configuration minimale</th>
<th align="left">Configuration recommandée</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Processeur</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz ou supérieur</p></td>
</tr>
<tr class="even">
<td align="left"><p>Mémoire vive (RAM)</p></td>
<td align="left"><p>8 GO</p></td>
<td align="left"><p>12 GO</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espace disque disponible</p></td>
<td align="left"><p>1 Go</p></td>
<td align="left"><p>2 Go</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="sql-server-database-requirements-"></a>Configuration requise pour la base de données SQLServer

Le tableau suivant répertorie les versions de SQLServer qui sont prises en charge pour l’installation de la fonctionnalité serveur d’administration et de surveillance, qui inclut la base de données de récupération, la base de données d’audit et de conformité, ainsi que les rapports d’audit et de conformité. Les bases de données requièrent également l’installation des outils de gestion SQL Server.

**Remarques**  MBAM ne prend pas en charge les groupes de disponibilité ou de mise en miroir SQL. Pour installer les bases de données, vous devez exécuter l’installation MBAM Server sur un serveur SQL autonome.

 

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version de SQL Server</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MicrosoftSQLServer2008 R2</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftSQLServer2012</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Composant matériel</th>
<th align="left">Configuration minimale</th>
<th align="left">Configuration recommandée</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Processeur</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz ou supérieur</p></td>
</tr>
<tr class="even">
<td align="left"><p>Mémoire vive (RAM)</p></td>
<td align="left"><p>8 GO</p></td>
<td align="left"><p>12 GO</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espace disque disponible</p></td>
<td align="left"><p>5 GO</p></td>
<td align="left"><p>5 Go minimum</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-client-system-requirements"></a> Configuration système requise pour le client MBAM


### Configuration requise du système d’exploitation client

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client de gestion et de contrôle BitLocker de Microsoft.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Système d’exploitation</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Plus de.</p></td>
<td align="left"><p>Edition entreprise ou édition intégrale</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Édition Entreprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WindowsToGo</p></td>
<td align="left"><p>Windows 8 entreprise Edition</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="client-ram-requirements-"></a>Configuration requise pour le client RAM

Il n’existe aucune exigence de mémoire RAM spécifique à l’installation du client d’administration et de surveillance de Microsoft BitLocker.

## <a href="" id="---------mbam-group-policy-system-requirements"></a> Configuration système requise pour la stratégie de groupe MBAM


Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de l’administration et du modèle de stratégie de groupe Microsoft BitLocker.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Système d’exploitation</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Plus de.</p></td>
<td align="left"><p>Edition entreprise ou édition intégrale</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Édition Entreprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012</p></td>
<td align="left"><p>Edition standard ou Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Planification du déploiement de MBAM2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Conditions préalables au déploiement de MBAM2.0](mbam-20-deployment-prerequisites-mbam-2.md)

 

 





