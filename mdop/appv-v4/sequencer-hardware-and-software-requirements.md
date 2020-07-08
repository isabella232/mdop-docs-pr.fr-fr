---
title: Configuration matérielle et logicielle requise pour Sequencer
description: Configuration matérielle et logicielle requise pour Sequencer
author: dansimp
ms.assetid: 36084e12-831d-452f-a4a4-45f07f9ce471
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d4e12a5803a3c9033513424826b49bc0bca5885
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806345"
---
# Configuration matérielle et logicielle requise pour Sequencer


Cette rubrique décrit la configuration matérielle et logicielle minimale recommandée pour l’ordinateur exécutant le Sequencer Microsoft Application Virtualization (App-V).

Avant d’installer le Sequencer et après avoir séquencé chaque application, vous devez restaurer une nouvelle image de système d’exploitation sur l’ordinateur de séquençage. Pour restaurer l’ordinateur exécutant le Sequencer, vous pouvez utiliser l’une des méthodes suivantes:

-   Remettez en forme le disque dur, puis réinstallez le système d’exploitation.

-   Restaurez le disque dur sur l’ordinateur exécutant l’image de Sequencer à l’aide d’un autre logiciel d’imagerie de disque.

La liste suivante présente la configuration matérielle requise pour exécuter le Sequencer App-V.

### <a href="" id="hardware-requirements-"></a>Configuration matérielle requise

-   Processeur: Intel Pentium III, 1 GHz (32-bit ou 64 bits). Le processus de séquençage est un processus à thread unique qui ne tire pas parti de deux processeurs.

-   Mémoire: 1 Go ou plus, 2 Go recommandés.

-   Disque dur: 40 gigaoctets (Go) d’espace disque disponible d’au moins 15 Go d’espace libre sur le disque dur. Nous vous recommandons d’avoir au moins trois fois l’espace disque disponible requis par l’application.

    **Remarques**  Le séquençage nécessite une utilisation importante du disque. Un débit de disque rapide peut réduire le temps de séquençage.

     

### Configuration logicielle requise

La liste suivante répertorie les systèmes d’exploitation pris en charge pour exécuter le Sequencer.

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
<td align="left"><p>Professionnel</p></td>
<td align="left"><p>SP2 ou SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Professionnel, entreprise ou intégrale</p></td>
<td align="left"><p>Aucun service pack, SP1 ou SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Le</p></td>
<td align="left"><p>Professionnel, entreprise ou édition intégrale</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

¹ pris en charge pour App-V 4,5 avec SP1 ou SP2 et App-V 4,6 uniquement

**Remarques**  Le Sequencer Application Virtualization (App-V) 4,6 prend en charge les versions 32 bits et 64 bits de ces systèmes d’exploitation.

 

Vous devez configurer des ordinateurs exécutant le Sequencer avec les mêmes applications qui sont installées sur des ordinateurs cibles.

### Configuration logicielle requise pour les services Bureau à distance

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
<td align="left"><p>Éditions standard, édition entreprise ou édition Datacenter</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Éditions standard, édition entreprise ou édition Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Standard, entreprise ou centre de</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

**Remarques**  Application Virtualization (App-V) 4,6 pour les services Bureau à distance prend en charge les versions 32 bits et 64 bits de ces systèmes d’exploitation.

 

## Rubriques connexes


[Vue d'ensemble d'Application Virtualization Sequencer](application-virtualization-sequencer-overview.md)

 

 





