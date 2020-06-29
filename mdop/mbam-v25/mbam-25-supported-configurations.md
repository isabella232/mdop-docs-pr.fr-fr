---
title: Configurations prises en charge par MBAM2.5
description: Configurations prises en charge par MBAM2.5
author: dansimp
ms.assetid: ce689aff-9a55-4ae7-a968-23c7bda9b4d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 10/24/2018
ms.openlocfilehash: 262cd8c259dc37b291cdaf02caf0e20b7515d38b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810229"
---
# Configurations prises en charge par MBAM2.5


Vous pouvez exécuter l’outil d’administration et de surveillance de BitLocker (MBAM) 2,5 dans une topologie autonome ou dans une topologie d’intégration de Configuration Manager intégrant MBAM avec System Center Configuration Manager. Si vous utilisez la configuration recommandée pour une topologie dans un environnement de production, MBAM prend en charge jusqu’à 500 000 MBAM clients. Pour plus d’informations sur l’architecture et les fonctionnalités recommandées qui sont configurées sur chaque serveur pour chaque topologie, voir [architecture de haut niveau pour MBAM 2,5](high-level-architecture-for-mbam-25.md).

Pour les configurations supplémentaires qui sont spécifiques au topologie d’intégration de Configuration Manager, voir [versions de Configuration Manager prises en charge par MBAM](#bkmk-cm-ramreqs).

**Remarque**  
Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975). Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).



## Langues prises en charge par MBAM


Les tableaux suivants illustrent les langues prises en charge pour le client MBAM (y compris le portail libre-service) et le serveur MBAM dans MBAM 2,5 et MBAM 2,5 SP1.

**Langues prises en charge dans MBAM 2,5 SP1:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Langues client</th>
<th align="left">Langues du serveur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tchèque (République tchèque) CS-CZ</p>
<p>Danois (Danemark) da-DK</p>
<p>Néerlandais (Pays-Bas) NL-NL</p>
<p>Anglais (États-Unis) en-US</p>
<p>FI (Finlande)-FI</p>
<p>Français (France) fr-FR</p>
<p>Allemand (Allemagne) de-DE</p>
<p>Grec (Grèce) El-GR</p>
<p>Hongrois (Hongrie) HU-HU</p>
<p>IT Italien (Italie)-IT</p>
<p>Japonais (Japon) ja-JP</p>
<p>Coréen (Corée) ko-KR</p>
<p>Norvégien, Bokmål (Norvège) NB-non</p>
<p>Polonais (Pologne) PL-PL</p>
<p>Portugais (Brésil) pt-BR</p>
<p>Portugais (Portugal) pt-PT</p>
<p>Russe (Russie) ru-RU</p>
<p>Slovaque (Slovaquie) SK-SK</p>
<p>Espagnol (Espagne) es-ES</p>
<p>Suédois (Suède) sv-SE</p>
<p>Turc (Turquie) TR-TR</p>
<p>Slovène (Slovénie) SL-SI</p>
<p>Chinois simplifié (RPC) zh-NC</p>
<p>Chinois traditionnel (Taïwan) zh-TW</p></td>
<td align="left"><ul>
<li><p>Anglais (États-Unis) en-US</p></li>
<li><p>Français (France) fr-FR</p></li>
<li><p>Allemand (Allemagne) de-DE</p></li>
<li><p>IT Italien (Italie)-IT</p></li>
<li><p>Japonais (Japon) ja-JP</p></li>
<li><p>Coréen (Corée) ko-KR</p></li>
<li><p>Portugais (Brésil) pt-BR</p></li>
<li><p>Russe (Russie) ru-RU</p></li>
<li><p>Espagnol (Espagne) es-ES</p></li>
<li><p>Chinois simplifié (RPC) zh-NC</p></li>
<li><p>Chinois traditionnel (Taïwan) zh-TW</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Langues prises en charge dans MBAM 2,5:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Langues client</th>
<th align="left">Langues du serveur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p>Anglais (États-Unis) en-US</p></li>
<li><p>Français (France) fr-FR</p></li>
<li><p>Allemand (Allemagne) de-DE</p></li>
<li><p>IT Italien (Italie)-IT</p></li>
<li><p>Japonais (Japon) ja-JP</p></li>
<li><p>Coréen (Corée) ko-KR</p></li>
<li><p>Portugais (Brésil) pt-BR</p></li>
<li><p>Russe (Russie) ru-RU</p></li>
<li><p>Espagnol (Espagne) es-ES</p></li>
<li><p>Chinois simplifié (RPC) zh-NC</p></li>
<li><p>Chinois traditionnel (Taïwan) zh-TW</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Anglais (États-Unis) en-US</p></li>
<li><p>Français (France) fr-FR</p></li>
<li><p>Allemand (Allemagne) de-DE</p></li>
<li><p>IT Italien (Italie)-IT</p></li>
<li><p>Japonais (Japon) ja-JP</p></li>
<li><p>Coréen (Corée) ko-KR</p></li>
<li><p>Portugais (Brésil) pt-BR</p></li>
<li><p>Russe (Russie) ru-RU</p></li>
<li><p>Espagnol (Espagne) es-ES</p></li>
<li><p>Chinois simplifié (RPC) zh-NC</p></li>
<li><p>Chinois traditionnel (Taïwan) zh-TW</p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-server-system-requirements"></a> Configuration système requise pour MBAM Server


### Configuration requise pour le système d’exploitation MBAM

Nous vous recommandons vivement d’exécuter le client MBAM et MBAM Server sur la même ligne de systèmes d’exploitation. Par exemple, Windows 10 avec Windows Server 2016, Windows 8,1 avec Windows Server 2012 R2, et ainsi de suite.

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de MBAM Server.

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
<td align="left"><p>Windows Server2016</p></td>
<td align="left"><p>Standard ou Datacenter</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>WindowsServer2012R2</p></td>
<td align="left"><p>Standard ou Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012</p></td>
<td align="left"><p>Standard ou Datacenter</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard, entreprise ou centre de</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



Le domaine d’entreprise doit contenir au moins un contrôleur de domaine Windows Server 2008 (ou version ultérieure).

### <a href="" id="bkmk-stand-alone-ramreqs"></a>Configuration requise pour le processeur du serveur MBAM, la RAM et l’espace disque-topologie autonome

Ces exigences concernent la topologie autonome MBAM. Pour connaître la configuration requise pour la topologie d’intégration de Configuration Manager, voir Configuration requise pour le [processeur du serveur MBAM, la RAM et l’espace disque-topologie d’intégration de Configuration Manager](#bkmk-cm-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Élément matériel</th>
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



### <a href="" id="bkmk-cm-ramreqs"></a>Configurations requises pour le processeur du serveur MBAM, la RAM et l’espace disque-topologie d’intégration de Configuration Manager

Le tableau suivant répertorie les conditions requises processeur de serveur, RAM et espace disque pour les serveurs MBAM lorsque vous utilisez la topologie d’intégration de Configuration Manager. Pour connaître la configuration requise pour la topologie autonome, voir [Configuration requise pour le processeur MBAM, la RAM et l’espace disque-topologie autonome](#bkmk-stand-alone-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Élément matériel</th>
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
<td align="left"><p>4 Go</p></td>
<td align="left"><p>8 GO</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espace disque disponible</p></td>
<td align="left"><p>1 Go</p></td>
<td align="left"><p>2 Go</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-cmversions"></a>Versions du gestionnaire de configurations prises en charge par MBAM

MBAM prend en charge les versions suivantes de Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version prise en charge</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager (branche actuelle), versions allant jusqu’à 1902</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>

<tr class="odd">
<td align="left"><p>Microsoft System Center Configuration Manager 1806</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager (LTSB-version 1606)</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestionnaire de configuration de Microsoft System Center 2012</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft System Center Configuration Manager 2007 R2 ou version ultérieure</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p>

&gt;<strong>Remarque </strong> bien que Configuration Manager 2007 R2 soit 32 bits, vous devez l’installer et SQL Server sur un système d’exploitation 64 bits afin de correspondre au logiciel MBAM 64.
</td>
</tr>
</tbody>
</table>



Pour obtenir la liste des configurations prises en charge pour le serveur Configuration Manager, consultez la documentation TechNet appropriée pour la version de Configuration Manager que vous utilisez. MBAM ne possède aucune configuration système supplémentaire pour le serveur Configuration Manager.

### <a href="" id="sql-server-database-requirements-"></a>Configuration requise pour la base de données SQL Server

Le tableau suivant répertorie les versions de Microsoft SQL Server prises en charge pour les fonctionnalités du serveur MBAM, notamment la base de données de récupération, la base de données d’audit et de conformité, et la fonctionnalité rapports. Les versions requises s’appliquent aux topologies d’intégration autonomes et de Configuration Manager.

Vous devez installer SQL Server à l’aide du **SQL \ _Latin1 \ _General \ _CP1 \ _CI \ _AS** collation.

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
<td align="left"><p>Microsoft SQL Server 2017</p></td>
<td align="left"><p>Standard, entreprise ou centre de</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td><br/><tr class="even">
<td align="left"><p>MicrosoftSQLServer2016</p></td>
<td align="left"><p>Standard, entreprise ou centre de</p></td>
<td align="left"><p>SP1</p></td>
<a href="https://www.microsoft.com/download/details.aspx?id=54967" data-raw-source="https://www.microsoft.com/download/details.aspx?id=54967">https://www.microsoft.com/download/details.aspx?id=54967</a><td align="left"><p>64 bits</p></td>
<tr class="odd">
<td align="left"><p>MicrosoftSQLServer2014</p></td>
<td align="left"><p>Standard, entreprise ou centre de</p></td>
<td align="left"><p>SP1, SP2</p></td>
<td align="left"><p>64 bits</p></td>
<tr class="odd">
<td align="left"><p>MicrosoftSQLServer 2012</p></td>
<td align="left"><p>Standard, entreprise ou centre de</p></td>
<td align="left"><p>3</p></td>
<td align="left"><p>64 bits</p></td>
<tr class="even">
<td align="left"><p>Microsoft SQL Server 2008 R2</p></td>
<td align="left"><p>Standard ou Entreprise</p></td>
<td align="left"><p>3</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

**Remarque**  
Pour prendre en charge SQL 2016, vous devez installer le version de service de mars 2017 pour MDOP https://www.microsoft.com/download/details.aspx?id=54967 et prendre en charge sql 2017 vous devez installer la version de maintenance de juillet 2018 pour MDOP https://www.microsoft.com/download/details.aspx?id=57157 . En règle générale, restez en mesure d’utiliser la mise à jour de maintenance la plus récente, car elle inclut également toutes les ainsi correctifs et nouvelles fonctionnalités.


### <a href="" id="bkmk-sql-stand-alone-ramreqs"></a>Configuration requise pour le processeur SQL Server, la RAM et l’espace disque-topologie autonome

Le tableau suivant répertorie les exigences relatives au processeur, à la RAM et à l’espace disque recommandés pour l’ordinateur SQL Server lors de l’utilisation de la topologie autonome. Utilisez ces exigences comme guide. Vos exigences spécifiques varient en fonction du nombre d’ordinateurs clients que vous prenez en charge au sein de votre entreprise. Pour consulter la configuration requise pour la topologie d’intégration de Configuration Manager, voir Configuration requise pour le [processeur SQL Server, la RAM et l’espace disque-topologie d’intégration de Configuration Manager](#bkmk-cm-sql-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Élément matériel</th>
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



### <a href="" id="bkmk-cm-sql-ramreqs"></a>Configuration requise pour le processeur SQL Server, la RAM et l’espace disque-topologie d’intégration de Configuration Manager

Le tableau suivant répertorie les exigences relatives au processeur, à la RAM et à l’espace disque pour l’ordinateur Microsoft SQL Server lors de l’utilisation de la topologie d’intégration de Configuration Manager, voir [topologie autonome du processeur SQL Server, de la RAM et de l’espace disque](#bkmk-sql-stand-alone-ramreqs).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Élément matériel</th>
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
<td align="left"><p>4 Go</p></td>
<td align="left"><p>8 GO</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espace disque disponible</p></td>
<td align="left"><p>5 GO</p></td>
<td align="left"><p>5 GO</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------mbam-client-system-requirements"></a> Configuration système requise pour le client MBAM


### Configuration requise du système d’exploitation client

Nous vous recommandons vivement d’exécuter le client MBAM et MBAM Server sur la même ligne de systèmes d’exploitation. Par exemple, Windows 10 avec Windows Server 2016, Windows 8,1 avec Windows Server 2012 R2, et ainsi de suite.

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client MBAM. Les mêmes exigences s’appliquent aux topologies d’intégration autonome et Configuration Manager.

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
<tr class="even">
    <td align="left"><p>Windows 10 IoT</p></td>
    <td align="left"><p>Enterprise</p></td>
    <td align="left"><p></p></td>
    <td align="left"><p>32bits ou 64bits</p></td>
</tr><br/><tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Entreprise ou intégrale</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>WindowsToGo</p></td>
<td align="left"><p>Windows 8,1 et Windows 10 entreprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
</tbody>
</table>



### <a href="" id="client-ram-requirements-"></a>Configuration requise pour le client RAM

Il n’existe aucune exigence de RAM spécifique à l’installation du client MBAM.

## <a href="" id="---------mbam-group-policy-system-requirements"></a> Configuration système requise pour la stratégie de groupe MBAM


Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de modèles de stratégie de groupe MBAM.

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
 <tr class="even">
      <td align="left"><p>Windows 10 IoT</p></td>
      <td align="left"><p>Enterprise</p></td>
      <td align="left"><p></p></td>
      <td align="left"><p>32bits ou 64bits</p></td>
 </tr>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Enterprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Entreprise ou intégrale</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>WindowsServer2012R2</p></td>
<td align="left"><p>Standard ou Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012</p></td>
<td align="left"><p>Standard ou Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard, entreprise ou centre de</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>

## MBAM dans Azure IaaS

Le serveur MBAM peut être déployé dans Azure infrastructure en tant que service (IaaS) sur les versions de système d’exploitation prises en charge répertoriées ci-dessus, qui se connectent à un annuaire actif hébergé sur un site ou un Active Directory également hébergé dans Azure IaaS.  La documentation relative à la configuration et à la configuration d’Active Directory sur Azure IaaS est disponible [ici](https://msdn.microsoft.com/library/azure/jj156090.aspx).

Le client MBAM n’est pas pris en charge sur les machines virtuelles et n’est pas non plus pris en charge sur Azure IaaS.


## Service Releases 

- [Correctif 2016 d’avril](https://support.microsoft.com/help/3144445/april-2016-hotfix-rollup-for-microsoft-desktop-optimization-pack)
- [2016 septembre](https://support.microsoft.com/ms-my/help/3168628/september-2016-servicing-release-for-microsoft-desktop-optimization-pa)
- [Décembre2016](https://support.microsoft.com/help/3198158/december-2016-servicing-release-for-microsoft-desktop-optimization-pac)
- [Mars2017](https://support.microsoft.com/en-ie/help/4014009/march-2017-servicing-release-for-microsoft-desktop-optimization-pack) 
- [Juin2017](https://support.microsoft.com/af-za/help/4018510/june-2017-servicing-release-for-microsoft-desktop-optimization-pack)
- [Septembre2017](https://support.microsoft.com/en-ie/help/4041137/september-2017-servicing-release-for-microsoft-desktop-optimization)
- [Mars2018](https://support.microsoft.com/help/4074878/march-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [2018 juillet](https://support.microsoft.com/help/4340040/july-2018-servicing-release-for-microsoft-desktop-optimization-pack)
- [2019](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack)

## Rubriques connexes


[Planification du déploiement de MBAM2.5](planning-to-deploy-mbam-25.md)

[Préparation de votre environnement pour MBAM2.5](preparing-your-environment-for-mbam-25.md)




## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




