---
title: Configuration matérielle et logicielle requise pour Application Virtualization Client
description: Configuration matérielle et logicielle requise pour Application Virtualization Client
author: dansimp
ms.assetid: 8b877a2c-5721-4b22-a47f-e2838d58ab12
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5b828f59ba36099b4f6a545cd5bbcb3c72d24e3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808025"
---
# Configuration matérielle et logicielle requise pour Application Virtualization Client


Cette rubrique décrit la configuration matérielle et logicielle recommandée pour l’installation du client de bureau de virtualisation des applications et du client de virtualisation des applications pour les services Bureau à distance (anciennement services Terminal Server).

## Client de bureau de virtualisation des applications


La liste suivante présente la configuration minimale recommandée pour le matériel et les logiciels requis pour le client de bureau Virtualization. La configuration requise est d’abord répertoriée dans Microsoft Application Virtualization (App-V) 4.6 SP2, puis dans les versions antérieures à App-V 4.6 SP2.

**Remarques**  Le client de bureau App-V) ne nécessite pas de ressources processeur ou RAM supplémentaires en plus de celles requises pour le système d’exploitation hôte.

 

### Configuration matérielle requise

La configuration matérielle requise est applicable à toutes les versions.

-   Processeur — Voir la configuration système recommandée pour le système d’exploitation que vous utilisez.

-   RAM — Voir la configuration système recommandée pour le système d’exploitation que vous utilisez.

-   Disque: 30 Mo pour l’installation et 6 Go pour le cache.

### Configuration logicielle requise pour App-V 4,6 SP2

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
<th align="left">Référence SKU architecturale</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Edition professionnelle</p></td>
<td align="left"><p>3</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Edition professionnelle, entreprise ou édition intégrale</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Plus de.</p></td>
<td align="left"><p>Edition professionnelle, entreprise ou édition intégrale</p></td>
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

Les logiciels requis suivants sont installés automatiquement si vous utilisez la méthode Setup.exe. Si vous utilisez le programme d’installation de Setup.msi, les produits suivants doivent d’abord être installés.
- Package redistribuable **Microsoft Visual c++ 2005 SP1 (x86)**: pour plus d’informations sur l’installation de Microsoft visual C++ 2005 SP1 (x86), voir [microsoft Visual c++ 2005 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) ( https://go.microsoft.com/fwlink/?LinkId=119961) . Pour la version 4,5 SP2 du client App-V, téléchargez Vcredist\_x86.exe à partir de [Microsoft Visual C++ 2005 Service Pack 1 package redistribuable de la mise à jour de sécurité ATL](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360) .
  -   **Services Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)**: pour plus d’informations sur l’installation de Microsoft Core XML Services (msxml) 6,0 SP1 (x86), voir [Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) ( https://go.microsoft.com/fwlink/?LinkId=63266) .

Pour le client de bureau 4,6 de virtualisation des applications (App-V), les logiciels requis supplémentaires suivants sont installés automatiquement si vous utilisez la méthode Setup.exe. Si vous utilisez le programme d’installation de Setup.msi, vous devez également procéder à l’installation avec les autres conditions préalables indiquées.

-   Package redistribuable **Microsoft VisualC + + 2008SP1 (x86)**: pour plus d’informations sur l’installation de Microsoft VisualC + + 2008 SP1 (x86), voir [Microsoft VisualC + + 2008 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=150700) ( https://go.microsoft.com/fwlink/?LinkId=150700) .

### Configuration logicielle requise pour les versions qui précèdent App-V 4,6 SP2

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
<th align="left">Référence SKU architecturale</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Edition professionnelle</p></td>
<td align="left"><p>SP2 ou SP3</p></td>
<td align="left"><p>x86 et x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista</p></td>
<td align="left"><p>Edition professionnelle, entreprise ou édition intégrale</p></td>
<td align="left"><p>Aucun service pack, SP1 ou SP2</p></td>
<td align="left"><p>x86 et x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Le</p></td>
<td align="left"><p>Edition professionnelle, entreprise ou édition intégrale</p></td>
<td align="left"><p>Aucun Service Pack ou SP1</p></td>
<td align="left"><p>x86 et x64</p></td>
</tr>
</tbody>
</table>
¹ pris en charge pour App-V 4,5 SP1 et SP2, App-V 4,6 et 4,6 SP1 uniquement

Le client de bureau 4,6 de virtualisation des applications (App-V) prend en charge les références SKU x86 et x64 de ces systèmes d’exploitation.

Les logiciels requis suivants sont installés automatiquement si vous utilisez la méthode Setup.exe. Si vous utilisez le programme d’installation de Setup.msi, les produits suivants doivent d’abord être installés.

-   <strong>Package redistribuable Microsoft Visual C++ 2005 SP1 (x86) </strong> : pour plus d’informations sur l’installation de Microsoft Visual c++ 2005 SP1 (x86), voir <a href="https://go.microsoft.com/fwlink/?LinkId=119961" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961)"> Microsoft visual C++ 2005 SP1 (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=119961" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=119961"> https://go.microsoft.com/fwlink/?LinkId=119961 </a> ). Pour la version 4,5 SP2 du client App-V, téléchargez Vcredist_x86.exe à partir de <a href="https://go.microsoft.com/fwlink/?LinkId=169360" data-raw-source="[Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=169360)"> Microsoft Visual C++ 2005 Service Pack 1 package redistribuable de la mise à jour de sécurité ATL </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=169360" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=169360"> https://go.microsoft.com/fwlink/?LinkId=169360 </a> ).

-   <strong>Microsoft Core XML Services (MSXML) 6,0 SP1 (x86) </strong> : pour plus d’informations sur l’installation de Microsoft Core XML Services (MSXML) 6,0 SP1 (x86), voir <a href="https://go.microsoft.com/fwlink/?LinkId=63266" data-raw-source="[Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266)"> Microsoft Core XML Services (msxml) 6,0 SP1 (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=63266" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=63266"> https://go.microsoft.com/fwlink/?LinkId=63266 </a> ).

-   <strong>Rapport d’erreurs d’application Microsoft </strong> : le programme d’installation de ce logiciel est inclus dans le <strong> dossier Support\Watson du </strong> fichier d’archive auto-extractible.

Pour le client de bureau 4,6 de virtualisation des applications (App-V), les logiciels requis supplémentaires suivants sont installés automatiquement si vous utilisez la méthode Setup.exe. Si vous utilisez le programme d’installation de Setup.msi, vous devez également procéder à l’installation avec les autres conditions préalables indiquées.

-   <strong>Package redistribuable Microsoft Visual C++ 2008 SP1 (x86) </strong> : pour plus d’informations sur l’installation de Microsoft Visual c++ 2008 SP1 (x86), voir <a href="https://go.microsoft.com/fwlink/?LinkId=150700" data-raw-source="[Microsoft Visual C++ 2008 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=150700)"> Microsoft visual C++ 2008 SP1 (x86) </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=150700" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=150700"> https://go.microsoft.com/fwlink/?LinkId=150700 </a> ).

## Client de virtualisation des applications pour les services Bureau à distance

Vous trouverez ci-après les configurations matérielles et logicielles recommandées pour le client de virtualisation d’application pour les services Bureau à distance. La configuration requise est d’abord indiquée pour appv461_3, puis par la configuration requise pour les versions antérieures à App-V 4,6 SP2.

Le client Application Virtualization (App-V) pour les services Bureau à distance ne nécessite pas de ressources processeur ou RAM supplémentaires en plus de celles requises pour le système d’exploitation hôte.

### Configuration matérielle requise

La configuration matérielle requise est applicable à toutes les versions.

-   Processeur — Voir la configuration système recommandée pour le système d’exploitation que vous utilisez.

-   RAM — Voir la configuration système recommandée pour le système d’exploitation que vous utilisez. Ces exigences varient également en fonction du nombre d’utilisateurs et d’applications.

-   Disque: 30 Mo pour l’installation et 6 Go pour le cache.

### Configuration logicielle requise pour App-V 4,6 SP2

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
<th align="left">Référence SKU architecturale</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Éditions standard, édition entreprise ou édition Datacenter</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86 et x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>x86 et x64</p></td>
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
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

Les logiciels requis suivants sont installés automatiquement si vous utilisez la méthode Setup.exe. Si vous utilisez le programme d’installation de Setup.msi, les produits suivants doivent d’abord être installés.

-   Package redistribuable **Microsoft VisualC + + 2005SP1 (x86)**: pour plus d’informations sur l’installation de Microsoft VisualC + + 2005 SP1 (x86), voir [Microsoft VisualC + + 2005 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) ( https://go.microsoft.com/fwlink/?LinkId=119961) . Pour la version 4.5 SP2 du client App-V, téléchargez Vcredist\_x86.exe à partir de la [mise à jour de sécurité de Microsoft Visual C++ 2005 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=169360) (en anglais) https://go.microsoft.com/fwlink/?LinkId=169360) .

-   **Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)**: pour plus d’informations sur l’installation de Microsoft Core XML Services (MSXML) 6.0 SP1 (x86), voir [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) ( https://go.microsoft.com/fwlink/?LinkId=63266) .

-   **Rapport d’erreurs d’application Microsoft**: le programme d’installation de ce logiciel est inclus dans le dossier **Support\\Watson** du fichier d’archive auto-extractible.

Pour le client de bureau 4,6 de virtualisation des applications (App-V), les logiciels requis supplémentaires suivants sont installés automatiquement si vous utilisez la méthode Setup.exe. Si vous utilisez le programme d’installation de Setup.msi, vous devez également procéder à l’installation avec les autres conditions préalables indiquées.

-   Package redistribuable **Microsoft VisualC + + 2008SP1 (x86)**: pour plus d’informations sur l’installation de Microsoft VisualC + + 2008 SP1 (x86), voir [Microsoft VisualC + + 2008 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=150700) ( https://go.microsoft.com/fwlink/?LinkId=150700) .

### Configuration logicielle requise pour les versions qui précèdent App-V 4,6 SP2

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
<th align="left">Référence SKU architecturale</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2003</p></td>
<td align="left"><p>Éditions standard, édition entreprise ou édition Datacenter</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 et x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 R2</p></td>
<td align="left"><p>Éditions standard, édition entreprise ou édition Datacenter</p></td>
<td align="left"><p>Aucun Service Pack ou SP2</p></td>
<td align="left"><p>x86 et x64</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>SP1 ou SP2</p></td>
<td align="left"><p>x86 et x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Éditions standard, Enterprise ou Datacenter</p></td>
<td align="left"><p>Aucun Service Pack ou SP1</p></td>
<td align="left"><p>x64</p></td>
</tr>
</tbody>
</table>

Le client de virtualisation des applications (App-V) 4,6 pour les services Bureau à distance prend en charge les références SKU x86 et x64 de ces systèmes d’exploitation.

## Rubriques connexes
- [Configuration matérielle et logicielle requise pour Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md)
- [Configuration système requise pour Application Virtualization](application-virtualization-system-requirements.md)
- [Procédure pour installer le client via la ligne de commande](how-to-install-the-client-by-using-the-command-line-new.md)
- [Procédure pour installer manuellement Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)
- [Procédure pour mettre à niveau Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)
