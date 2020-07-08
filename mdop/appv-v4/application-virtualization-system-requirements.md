---
title: Configuration système requise pour Application Virtualization
description: Configuration système requise pour Application Virtualization
author: dansimp
ms.assetid: a2798dd9-168e-45eb-8103-e12e128fae7c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c160a7532b521bb41570b419b22b9e7daaec2987
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807938"
---
# Configuration système requise pour Application Virtualization


Cette rubrique décrit la configuration matérielle et logicielle minimale requise pour le serveur de gestion Microsoft application (App-V) et le serveur de diffusion en continu.

## Gestion de la virtualisation des applications et serveurs de diffusion en continu


La liste suivante présente la configuration minimale recommandée pour le matériel et les logiciels recommandés pour le serveur de gestion des applications et le serveur de streaming App-V.

### Configuration matérielle requise

-   Processeur: Intel Pentium III, 1 GHz

-   RAM: 512 MO

-   Disque dur: 200 Mo d’espace disque disponible sans le répertoire de contenu

### Configuration logicielle requise

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Systèmed’exploitation</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Edition standard</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Édition entreprise ou édition Datacenter</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edition standard</p></td>
<td align="left"><p>Aucun Service Pack ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Édition entreprise ou édition Datacenter</p></td>
<td align="left"><p>Aucun Service Pack ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2 ¹</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ s’applique uniquement aux applications-V 4,5 SP1 et SP2.

## Magasin de données


La liste suivante présente la configuration minimale requise recommandée pour l’ordinateur qui est utilisée lors de l’installation du magasin de données sur un serveur distinct. Le magasin de données est requis uniquement pour le serveur de gestion des applications virtuelles.

### Configuration matérielle requise

-   Processeur: Intel Pentium III, 850 MHz

-   RAM: 512 MO

-   Espace disque disponible: 200 Mo d’espace disque disponible

### Configuration logicielle requise

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Systèmed’exploitation</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Edition standard</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Édition entreprise ou édition Datacenter</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edition standard</p></td>
<td align="left"><p>Aucun Service Pack ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Édition entreprise ou édition Datacenter</p></td>
<td align="left"><p>Aucun Service Pack ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2 ¹</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ s’applique uniquement aux applications-V 4,5 SP1 et SP2.

-   Base de données: Microsoft SQL Server2000 SP3a ou SP4, SQL Server2005 SP1, SP2 ou SP3, ou SQL Server 2008, sans Service Pack ou SP1 ou SQL Server 2008 R2 (32-bit ou 64 bits)

-   Composants Microsoft Data Access (MDAC 2,7)

-   Contrôleur de domaine (Active Directory Domain Services) ou contrôleur de domaine principal Windows NT 4.0 (CPD) en tant qu’autorité d’authentification centrale

## Service Web de gestion


La liste suivante répertorie les configurations matérielles recommandées minimales et logicielles requises pour le service Web de gestion des applications qui est installé sur un autre ordinateur.

### Configuration matérielle requise

-   Processeur: Intel Pentium III, 800 MHz

-   RAM: 256 MO

-   Espace disque: 50 Mo d’espace disque disponible

### Configuration logicielle requise

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Systèmed’exploitation</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Edition standard</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Édition entreprise ou édition Datacenter</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Edition standard</p></td>
<td align="left"><p>Aucun Service Pack ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Édition entreprise ou édition Datacenter</p></td>
<td align="left"><p>Aucun Service Pack ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2 ¹</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ s’applique uniquement aux applications-V 4,5 SP1 et SP2.

-   Internet Information Services (IIS) 6,0 configuré avec Microsoft ASP.NET, IIS 7

-   Microsoft .NET Framework 2.0

## Console de gestion


La liste suivante présente la configuration minimale recommandée pour le matériel et les logiciels requis pour la console de gestion application de la virtualisation lorsqu’il est installé sur un autre ordinateur.

### Configuration matérielle requise

-   Processeur: Intel Pentium III, 450 MHz

-   RAM: 256 MO

-   Espace disque disponible: 200 Mo d’espace disque disponible

### Configuration logicielle requise

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Systèmed’exploitation</th>
<th align="left">Édition</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Edition professionnelle</p></td>
<td align="left"><p>SP2 ou SP3</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Edition professionnelle, entreprise ou édition intégrale</p></td>
<td align="left"><p>Aucun service pack, SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Plus de.</p></td>
<td align="left"><p>Edition professionnelle, entreprise ou édition intégrale</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Éditions standard, édition entreprise ou édition Datacenter</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Éditions standard, édition entreprise ou édition Datacenter</p></td>
<td align="left"><p>Aucun Service Pack ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2 ¹</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

¹ s’applique uniquement aux applications-V 4,5 SP1 et SP2.

-   Microsoft Management Console (MMC 3.0 ou version ultérieure)

-   Microsoft .NET Framework 2.0 SP2 (minimum)

    **Important**  La configuration minimale requise pour .NET Framework 2,0 SP2 consiste à installer le correctif logiciel KB980850 ou les correctifs de l’application-V suivants sur l’ordinateur exécutant la console de gestion de l’application-V.

     

## Rubriques connexes


[Configuration matérielle et logicielle requise pour Application Virtualization Client](application-virtualization-client-hardware-and-software-requirements.md)

[Configuration matérielle et logicielle requise pour Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md)

[Procédure pour configurer des serveurs pour un déploiement basé sur un serveur](how-to-configure-servers-for-server-based-deployment.md)

[Procédure pour installer les serveurs et les composants système](how-to-install-the-servers-and-system-components.md)

[Procédure pour mettre à niveau les serveurs et les composants système](how-to-upgrade-the-servers-and-system-components.md)

 

 





