---
title: Choix de la version d'AGPM à installer
description: Choix de la version d'AGPM à installer
author: dansimp
ms.assetid: 31357d2a-bc23-4e15-93f4-0beda8ab7a7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/05/2017
ms.openlocfilehash: b09ea8161b6801c62552f1c0d0ef8455dc111e2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807770"
---
# Choix de la version d'AGPM à installer


Chaque version de MicrosoftAdvanced de gestion des stratégies de groupe (AGPM) prend en charge des versions spécifiques du système d’exploitation Windows. Nous vous recommandons vivement d’exécuter le client AGPM et le serveur AGPM sur la même ligne de systèmes d’exploitation. Par exemple, Windows 10 avec Windows Server 2016, Windows 8.1 avec Windows Server2012 R2, et ainsi de suite.

Nous vous recommandons d’installer le serveur AGPM sur la version la plus récente du système d’exploitation dans le domaine. AGPM utilise la console de gestion des stratégies de groupe (GPMC) pour sauvegarder et restaurer des objets de stratégie de groupe (GPO). Étant donné que les versions plus récentes de la console GPMC fournissent des paramètres de stratégie supplémentaires qui ne sont pas disponibles dans les versions antérieures, vous pouvez gérer d’autres paramètres de stratégie à l’aide de la version la plus récente du système d’exploitation.

Toutes les versions d’AGPM peuvent gérer uniquement les paramètres de stratégie qui ont été introduits dans la même version ou une version antérieure du système d’exploitation sur lequel AGPM s’exécute. Par exemple, si vous installez AGPM 4.0 SP2 sur Windows Server 2012, vous pouvez gérer les paramètres de stratégie qui ont été introduits dans Windows Server 2012 ou une version antérieure, mais vous ne pouvez pas gérer les paramètres de stratégie introduits plus tard, dans Windows 8.1 ou Windows Server2012 R2.

Si la version de GPMC sur votre serveur AGPM est antérieure à la version sur les ordinateurs utilisés par les administrateurs pour gérer la stratégie de groupe, le serveur AGPM ne sera pas en mesure de stocker des paramètres de stratégie qui ne sont pas disponibles dans l’ancienne version de GPMC. Consultez la feuille de calcul des paramètres de stratégie de groupe inclus dans Windows dans [Référence des paramètres de stratégie de groupe pour Windows et Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).

## AGPM 4.0 SP3


Si vous utilisez un ordinateur exécutant Windows 10 pour gérer les objets de stratégie de groupe, vous devez utiliser le SP3 d’AGPM 4,0. Vous ne pouvez pas installer les versions antérieures d’AGPM sur les ordinateurs qui exécutent le système d’exploitation Windows 10.

Le tableau 1 recense les systèmes d’exploitation sur lesquels vous pouvez installer AGPM 4.0 SP3 et les paramètres de stratégie que vous pouvez gérer à l’aide d’AGPM 4.0 SP3.

**Tableau 1: systèmes d’exploitation et paramètres de stratégie pris en charge par AGPM 4,0 SP3**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Configurations prises en charge pour le serveur AGPM</strong></th>
<th align="left"><strong>Configurations prises en charge pour le client AGPM</strong></th>
<th align="left"><strong>Prise en charge d’AGPM</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2016 ou Windows 10</p></td>
<td align="left"><p>Windows Server 2016 ou Windows 10</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2</p></td>
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Pris en charge avec les avertissements décrits dans <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"> KB 4015786</a>
</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 ou Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012 ou Windows 8,1</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Windows Server 2008 ou Vista avec Service Pack 1 (SP1)</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 ou Windows 7</p></td>
<td align="left"><p>Non pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows.</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0 SP2


Si vous utilisez des ordinateurs exécutant Windows Server2012 R2 ou Windows 8.1 pour gérer les objets de stratégie de groupe, vous devez utiliser AGPM 4.0 SP2. Vous ne pouvez pas installer les versions antérieures d’AGPM sur les ordinateurs qui exécutent ces systèmes d’exploitation.

Le tableau 1 recense les systèmes d’exploitation sur lesquels vous pouvez installer AGPM 4.0 SP2 et les paramètres de stratégie que vous pouvez gérer à l’aide d’AGPM 4.0 SP2.

**Tableau 2: systèmes d’exploitation et paramètres de stratégie pris en charge dans AGPM 4.0 SP2**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Configurations prises en charge pour le serveur AGPM</strong></th>
<th align="left"><strong>Configurations prises en charge pour le client AGPM</strong></th>
<th align="left"><strong>Prise en charge d’AGPM</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 ou Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012 ou Windows 8,1</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Windows Server 2008 ou Vista avec Service Pack 1 (SP1)</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Non pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows.</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0 SP1


Le tableau 2 répertorie les systèmes d’exploitation sur lesquels vous pouvez installer AGPM 4,0 SP1 et les paramètres de stratégie que vous pouvez gérer à l’aide d’AGPM 4.0 SP1.

**Tableau 3: les systèmes d’exploitation et les paramètres de stratégie pris en charge dans AGPM 4.0 SP1**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Configurations prises en charge pour le serveur AGPM</strong></th>
<th align="left"><strong>Configurations prises en charge pour le client AGPM</strong></th>
<th align="left"><strong>Prise en charge d’AGPM</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2012</p></td>
<td align="left"><p>Windows Server2012</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8,1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2008R2 ou une</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2008R2 ou une icône</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0


Le tableau 3 recense les systèmes d’exploitation sur lesquels vous pouvez installer AGPM 4,0 et les paramètres de stratégie que vous pouvez gérer à l’aide d’AGPM 4.0.

**Tableau 4: systèmes d’exploitation pris en charge par AGPM 4.0 et paramètres de stratégie**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Systèmes d’exploitation pris en charge pour le serveur AGPM</th>
<th align="left">Systèmes d’exploitation pris en charge pour le client AGPM</th>
<th align="left">Prise en charge d’AGPM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2008R2 ou la touche Windows</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Non pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2008R2 ou une icône</p></td>
</tr>
</tbody>
</table>

 

## Versions d’AGPM qui précèdent AGPM 4.0


Le tableau 4 répertorie les systèmes d’exploitation sur lesquels vous pouvez installer les versions d’AGPM qui précèdent AGPM 4.0. Si aucun système d’exploitation n’est répertorié, vous ne pouvez pas installer AGPM sur ce système d’exploitation.

**Tableau 5: systèmes d’exploitation pris en charge pour les versions d’AGPM qui précèdent AGPM 4.0**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Système d’exploitation</th>
<th align="left">Version d’AGPM qui peut être installée</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server 2008</p></td>
<td align="left"><p>3,0</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista avec SP1</p></td>
<td align="left"><p>3,0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Vista sans Service Pack (32)</p></td>
<td align="left"><p>2,5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 (32 bits)</p></td>
<td align="left"><p>2,5</p></td>
</tr>
</tbody>
</table>

 

## Obtention de technologies MDOP


AGPM 4,0 SP2 fait partie du pack d’optimisation de bureau de Microsoft (MDOP). MDOP fait partie de Microsoft Software Assurance. Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Rubriques connexes


[Gestion avancée des stratégies de groupe](index.md)

 

 





