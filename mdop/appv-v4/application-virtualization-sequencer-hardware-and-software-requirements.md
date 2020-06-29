---
title: Configuration matérielle et logicielle requise pour Application Virtualization Sequencer
description: Configuration matérielle et logicielle requise pour Application Virtualization Sequencer
author: dansimp
ms.assetid: c88a1b5b-23e1-4460-afa9-a5f37e32eb05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d68afe4d4a3f6f301d38f2e86139d94319583467
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807981"
---
# Configuration matérielle et logicielle requise pour Application Virtualization Sequencer


Cette rubrique décrit la configuration matérielle et logicielle minimale recommandée pour l’ordinateur exécutant le Sequencer Microsoft Application Virtualization (App-V).

**Important**  Vous devez exécuter le Sequencer App-V (**SFTSequencer.exe**) à l’aide d’un compte qui dispose de privilèges d’administrateur en raison des changements apportés par le Sequencer au système local. Ces modifications peuvent inclure l’écriture de fichiers dans le répertoire **C:\\Program Files** , l’apport de modifications du Registre, le démarrage et l’arrêt de services, la mise à jour des descripteurs de sécurité pour les fichiers et la modification des autorisations.

 

Avant d’installer le Sequencer et après avoir séquencé chaque application, vous devez restaurer une nouvelle image de système d’exploitation sur l’ordinateur de séquençage. Pour restaurer l’ordinateur exécutant le Sequencer, vous pouvez utiliser l’une des méthodes suivantes:

-   Remettez en forme le disque dur, puis réinstallez le système d’exploitation.

-   Restaurez le disque dur sur l’ordinateur exécutant l’image de Sequencer à l’aide d’un autre logiciel d’imagerie de disque.

-   Restaurez une image de système d’exploitation virtuelle telle qu’une image Microsoft Virtual PC. L’utilisation d’un ordinateur virtuel permet à des environnements de séquençage sains d’être facilement réutilisés avec un minimum d’administration.

La liste suivante présente la configuration matérielle requise pour exécuter le Sequencer App-V.

La configuration requise est d’abord répertoriée dans Microsoft Application Virtualization (App-V) 4.6 SP2, puis dans les versions antérieures à App-V 4.6 SP2.

### <a href="" id="hardware-requirements-"></a>Configuration matérielle requise

-   Processeur: Intel Pentium III, 1 GHz (32-bit ou 64 bits). Le processus de séquençage est un processus à thread unique qui ne tire pas parti de deux processeurs.

-   Mémoire: 1 Go ou plus, 2 Go recommandés.

-   Disque dur: 40 gigaoctets (Go) d’espace disque disponible d’au moins 15 Go d’espace libre sur le disque dur. Nous vous recommandons d’avoir au moins trois fois l’espace disque disponible requis par l’application.

    **Remarques**  Le séquençage nécessite une utilisation importante du disque. Un débit de disque rapide peut réduire le temps de séquençage.

     

### Configuration logicielle requise pour App-V 4,6 SP2

La liste suivante répertorie les systèmes d’exploitation pris en charge pour exécuter le Sequencer App-V 4,6 SP2.

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
<td align="left"><p>3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Professionnel, entreprise ou intégrale</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Plus de.</p></td>
<td align="left"><p>Professionnel, entreprise ou édition intégrale</p></td>
<td align="left"><p>Aucun Service Pack ou SP1</p></td>
<td align="left"><p>x86 et x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Professionnel ou édition entreprise</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 et x64</p></td>
</tr>
</tbody>
</table>

 

**Remarques**  Le Sequencer Application Virtualization (App-V) 4,6 SP2 prend en charge les versions 32 bits et 64 bits de ces systèmes d’exploitation.

 

Vous devez configurer des ordinateurs exécutant le Sequencer avec les mêmes applications qui sont installées sur des ordinateurs ciblés.

### Configuration logicielle requise pour les versions qui précèdent App-V 4,6 SP2

La liste suivante présente les systèmes d’exploitation pris en charge pour exécuter le Sequencer pour les versions qui précèdent App-V 4,6 SP2.

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

 

Vous devez configurer des ordinateurs exécutant le Sequencer avec les mêmes applications qui sont installées sur des ordinateurs ciblés.

### Configuration logicielle requise pour les services Bureau à distance pour App-V 4,6 SP2

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
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Éditions standard, édition entreprise ou édition Datacenter</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>Aucun Service Pack ou SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p></p></td>
<td align="left"><p>x86 ou x64</p></td>
</tr>
</tbody>
</table>

 

**Remarques**  Application Virtualization (App-V) 4,6 SP2 pour les services Bureau à distance prend en charge les versions 32 bits et 64 bits de ces systèmes d’exploitation.

 

### Configuration logicielle requise pour les services Bureau à distance pour les versions qui précèdent App-V 4,6 SP2

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
<td align="left"><p>Aucun Service Pack ou SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>Aucun Service Pack ou SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

 

**Remarques**  Application Virtualization (App-V) 4,6 SP2 pour les services Bureau à distance prend en charge les versions 32 bits et 64 bits de ces systèmes d’exploitation.

 

## Rubriques connexes


[Configuration matérielle et logicielle requise pour Application Virtualization Client](application-virtualization-client-hardware-and-software-requirements.md)

[Configuration système requise pour Application Virtualization](application-virtualization-system-requirements.md)

[Procédure pour installer Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md)

[Procédure pour mettre à niveau Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)

 

 





