---
title: Configurations prises en charge d'App-V5.0
description: Configurations prises en charge d'App-V5.0
author: dansimp
ms.assetid: 3787ff63-7ce7-45a8-8f01-81b4b6dced34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 60236743d2a6b418ca7f4705168a7bf064b82156
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805989"
---
# Configurations prises en charge d'App-V5.0


Cette rubrique spécifie les exigences nécessaires pour l’installation et l’exécution de Microsoft Application Virtualization (App-V) 5,0 dans votre environnement.

**Important**  
**Les configurations prises en charge dans cet article s’appliquent uniquement à l’App-V 5,0**. Pour plus d’informations sur les configurations prises en charge qui s’appliquent aux service packs 5,0 App-V, consultez les pages Web suivantes:

-   [Nouveautés dans App-V5.0 SP1](whats-new-in-app-v-50-sp1.md)

-   [À propos d'App-V5.0 SP2](about-app-v-50-sp2.md)

-   [Configurations prises en charge d'App-V5.0 SP3](app-v-50-sp3-supported-configurations.md)



## <a href="" id="---------app-v-5-0-server-system-requirements"></a> Configuration système requise pour le serveur App-V 5,0


**Important**  
Le serveur App-V 5,0 ne prend pas en charge les scénarios suivants:



-   Déploiement sur un ordinateur exécutant Microsoft Windows Server Core.

-   Déploiement sur un ordinateur qui exécute une version antérieure des composants serveur App-V 5,0.

    **Remarque**  
    Vous pouvez installer App-V 5,0 côte à côte avec le serveur App-V 4,5 Lightweight Streaming Server (LWS) uniquement. Le déploiement d’App-V 5,0 côte à côte avec le serveur de gestion des applications (HWS) App-V 4,5 n’est pas pris en charge.



-   Déploiement sur un ordinateur qui exécute Microsoft SQL Server Express Edition.

-   Déploiement distant de la base de données du serveur de gestion ou de la base de données de création de rapports. Le programme d’installation doit être exécuté directement sur l’ordinateur exécutant Microsoft SQL pour que l’installation de la base de données réussisse.

-   Déploiement sur un contrôleur de domaine.

-   Les chemins d’accès courts ne sont pas pris en charge. Si vous envisagez d’utiliser un chemin court, vous devez créer un nouveau volume.

### Configuration requise pour le système d’exploitation de Management Server

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation d’App-V 5,0 Management Server.

**Remarque**  
Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975). Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).



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
<td align="left"><p>Microsoft Windows Server 2008 (standard, entreprise, centre de connaissances ou serveur Web)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP1 ou version ultérieure</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (standard, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (standard, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



**Important**  
Le déploiement du rôle serveur de gestion sur un ordinateur sur lequel le partage de bureau à distance est activé n’est pas pris en charge.



### <a href="" id="management-server-hardware-requirements-"></a>Configuration matérielle requise pour le serveur de gestion

-   Processeur: 1,4 GHz ou plus rapide, processeur 64 bits (x64)

-   RAM: 1 Go de RAM (64 bits)

-   Disque dur: 200 Mo d’espace disque disponible, sans inclure le répertoire de contenu.

### Configuration requise du système d’exploitation du serveur de publication

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de serveur de publication 5,0 App-V.

**Remarque**  
Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975). Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).



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
<td align="left"><p>Microsoft Windows Server 2008 (standard, entreprise, centre de connaissances ou serveur Web)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (standard, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (standard, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



### <a href="" id="publishing-server-hardware-requirements-"></a>Configuration matérielle requise pour le serveur de publication

-   Processeur: 1,4 GHz ou plus rapide. processeur 64 bits (x64)

-   RAM: 2 Go de RAM (64 bits)

-   Disque dur: 200 Mo d’espace disque disponible. Répertoire de contenu non inclus

### Configuration requise pour le système d’exploitation du serveur de rapports

Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de serveur de création de rapports App-V 5,0.

**Remarque**  
Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975). Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).



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
<td align="left"><p>Microsoft Windows Server 2008 (standard, entreprise, centre de connaissances ou serveur Web)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (standard, Datacenter)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (standard, Datacenter)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



### <a href="" id="reporting-server-hardware-requirements-"></a>Configuration matérielle requise pour le serveur de création de rapports

-   Processeur: 1,4 GHz ou plus rapide. processeur 64 bits (x64)

-   RAM: 2 Go de RAM (64 bits)

-   Espace disque disponible: 200 Mo d’espace disque disponible

### <a href="" id="sql-server-database-requirements-"></a>Configuration requise pour la base de données SQL Server

Le tableau suivant répertorie les versions de SQL Server prises en charge pour la base de données et l’installation du serveur App-V 5,0.

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
<th align="left">Type de serveur App-V 5,0</th>
<th align="left">Version de SQL Server</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gestion/création de rapports</p></td>
<td align="left"><p>Microsoft SQL Server 2008</p>
<p>(Standard, entreprise, Datacenter ou édition développeur avec la fonctionnalité suivante: <strong> Services du moteur de base de données </strong> .)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestion/création de rapports</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p>
<p>(Standard, entreprise, Datacenter ou édition développeur avec la fonctionnalité suivante: <strong> Services du moteur de base de données </strong> .)</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestion/création de rapports</p></td>
<td align="left"><p>MicrosoftSQLServer 2012</p>
<p>(Standard, entreprise, Datacenter ou édition développeur avec la fonctionnalité suivante: <strong> Services du moteur de base de données </strong> .)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-client-supp-cfgs"></a> Configuration système requise pour le client App-V 5,0


Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client App-V 5,0.

**Remarque**  
Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975). Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).



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
<td align="left"><p>Microsoft Windows 7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong>Important</strong><br/><p>Windows 8,1 est uniquement pris en charge par App-V 5,0 SP2</p>
</div>
<div>

</div>
<p>Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
</tbody>
</table>



Les scénarios d’installation du client App-V suivants ne sont pas pris en charge, sauf comme indiqué:

-   Ordinateurs exécutant Windows Server

-   Ordinateurs exécutant App-V 4,6 SP1 ou versions antérieures

-   Le client App-V 5,0 Bureau à distance est uniquement pris en charge pour les serveurs RDS

### <a href="" id="client-hardware-requirements-"></a>Configuration matérielle requise pour le client

La liste suivante présente la configuration matérielle prise en charge pour l’installation du client App-V 5,0.

-   Processeur: 1,4 GHz ou supérieur 32 bits (x86) ou processeur 64 bits (x64)

-   RAM: 1 Go (32 bits) ou 2 Go (64 bits)

-   Disque: 100 Mo pour l’installation, sans compter l’espace disque utilisé par les applications virtualisées.

## <a href="" id="---------app-v-5-0-remote-desktop-client-system-requirements"></a> Configuration système requise pour le client de bureau à distance App-V 5,0


Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation du client de bureau à distance App-V 5,0.

**Remarque**  
Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975). Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).



Operating System Edition Service Pack Microsoft Windows Server 2008

R2

SP1

Microsoft Windows Server 2012

**Important**  
Windows Server 2012 R2 est uniquement pris en charge par App-V 5,0 SP2



Microsoft Windows Server 2012 (standard, Datacenter)

R2

64 bits



### <a href="" id="remote-desktop-client-hardware-requirements-"></a>Configuration matérielle requise pour le client Bureau à distance

La liste suivante présente la configuration matérielle prise en charge pour l’installation du client App-V 5,0.

-   Processeur: 1,4 GHz ou supérieur 32 bits (x86) ou processeur 64 bits (x64)

-   RAM: 1 Go (32 bits) ou 2 Go (64 bits)

-   Disque: 100 Mo pour l’installation, sans compter l’espace disque utilisé par les applications virtualisées.

## <a href="" id="---------app-v-5-0-sequencer-system-requirements"></a> Configuration requise pour le Sequencer App-V 5,0


Le tableau suivant répertorie les systèmes d’exploitation pris en charge pour l’installation de Sequencer App-V 5,0.

**Remarque**  
Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack immédiatement précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975). Pour plus d’informations sur la politique de support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).



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
<td align="left"><p>Microsoft Windows 7</p></td>
<td align="left"></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits et 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits et 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong>Important</strong><br/><p>Windows 8,1 est uniquement pris en charge par App-V 5,0 SP2</p>
</div>
<div>

</div>
<p>Windows 8.1</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits ou 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2008</p></td>
<td align="left"><p>R2</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits et 64bits</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32bits et 64bits</p></td>
</tr>
<tr class="even">
<td align="left"><div class="alert">
<strong>Important</strong><br/><p>Windows Server 2012 R2 est uniquement pris en charge par App-V 5,0 SP2</p>
</div>
<div>

</div>
<p>Microsoft Windows Server 2012</p></td>
<td align="left"><p>R2</p></td>
<td align="left"></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-supp-ver-sccm"></a>Versions prises en charge de System Center Configuration Manager


Vous pouvez utiliser Microsoft System Center 2012 Configuration Manager ou System Center 2012 R2 Configuration Manager pour gérer les applications virtuelles App-V, la création de rapports et d’autres fonctions. Le tableau suivant répertorie les versions prises en charge de Configuration Manager pour chaque version applicable d’App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version du gestionnaire de configurations prise en charge</th>
<th align="left">Version App-V</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gestionnaire de configuration de Microsoft System Center 2012</p></td>
<td align="left"><ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>System Center2012R2 Configuration Manager</p></td>
<td align="left"><ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul></td>
</tr>
</tbody>
</table>



Pour plus d’informations sur l’intégration de Configuration Manager à l’application-V, voir [planification de l’intégration d’App-v à la Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).






## Rubriques connexes


[Envisager de déployer App-V](planning-to-deploy-app-v.md)

[Composants requis d'App-V5.0](app-v-50-prerequisites.md)









