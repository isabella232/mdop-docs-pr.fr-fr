---
title: Nouveautés d'AGPM4.0SP3
description: Nouveautés d'AGPM4.0SP3
author: dansimp
ms.assetid: df495d55-9fbf-4f7e-a7af-3905f4f8790e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: a98bda82fab561113522382b4de6539a9dc23d0c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808178"
---
# Nouveautés d'AGPM4.0SP3


Ce contenu décrit les améliorations et les configurations prises en charge pour Microsoft Advanced Group Policy Management (AGPM) 4.0 Service Pack3 (SP3). S’il existe une différence entre ce contenu et une autre documentation AGPM, considérez ce contenu faisant autorité et supposez qu’il remplace l’autre documentation.

## <a href="" id="what-s-new"></a>Nouveautés


Le SP3 d’AGPM 4.0 prend en charge les fonctionnalités et fonctionnalités suivantes.

### Prise en charge de Windows 10

Le SP3 d’AGPM 4.0 ajoute une prise en charge pour les systèmes d’exploitation Windows 10 et Windows Server 2016.

### Prise en charge de PowerShell

Le SP3 d’AGPM 4.0 ajoute une prise en charge des cmdlets PowerShell. Pour obtenir la liste des applets de service disponibles dans AGPM 4.0 SP3, y compris les descriptions et la syntaxe, voir [automatisation du pack d’optimisation du bureau Microsoft avec Windows PowerShell](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps).

### Commentaires des clients et ROLLUP de HotFix

Le SP3 d’AGPM 4,0 inclut un cumul de tous les correctifs de la gestion de la stratégie de groupe Microsoft avancée 4,0 SP2 ainsi que des solutions aux problèmes rencontrés depuis AGPM 4,0 SP2.

### Possibilité d’effectuer la mise à niveau vers AGPM 4.0 SP3 sans entrer de nouveau les paramètres de configuration

Vous pouvez mettre à niveau le client AGPM ou le serveur AGPM vers AGPM 4.0 SP3 sans être invité à entrer de nouveau les paramètres de configuration (appelé mise à niveau intelligente) uniquement dans AGPM 4.0 et les versions ultérieures, comme indiqué dans le tableau suivant. Si vous effectuez une mise à niveau vers AGPM 4.0 SP3 à partir d’autres versions d’AGPM, comme indiqué dans le tableau ci-dessous, vous devez utiliser la mise à niveau classique, qui nécessite d’entrer de nouveau les paramètres de configuration. Étant donné que chaque version d’AGPM est associée à un système d’exploitation spécifique, voir [choisir la version d’AGPM à installer](https://go.microsoft.com/fwlink/?LinkId=254350) et vérifier que vous effectuez une mise à niveau de votre système d’exploitation le cas échéant avant de procéder à la mise à niveau d’AGPM.

**Mises à jour d’AGPM 4,0 SP3 prises en charge**

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Version d’AGPM à partir de laquelle vous pouvez effectuer la mise à niveau</strong></p></td>
<td align="left"><p><strong>2,5</strong></p></td>
<td align="left"><p><strong>3,0</strong></p></td>
<td align="left"><p><strong>4,0</strong></p></td>
<td align="left"><p><strong>4,0 SP1</strong></p></td>
<td align="left"><p><strong>4,0 SP2</strong></p></td>
<td align="left"><p><strong>4,0 SP3</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2,5</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Mise à niveau classique</p></td>
<td align="left"><p>Mise à niveau classique</p></td>
<td align="left"><p>L’installation est bloquée.</p></td>
<td align="left"><p>L’installation est bloquée.</p></td>
<td align="left"><p>L’installation est bloquée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3,0</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Mise à niveau classique</p></td>
<td align="left"><p>L’installation est bloquée.</p></td>
<td align="left"><p>L’installation est bloquée.</p></td>
<td align="left"><p>L’installation est bloquée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Mise à niveau intelligente</p></td>
<td align="left"><p>Mise à niveau intelligente</p></td>
<td align="left"><p>Mise à niveau intelligente</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4,0 SP1</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Mise à niveau intelligente</p></td>
<td align="left"><p>Mise à niveau intelligente</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0 SP2</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Mise à niveau intelligente</p></td>
</tr>
</tbody>
</table>

 

## Configurations prises en charge


AGPM 4.0 SP3 prend en charge les configurations figurant dans le tableau suivant. Bien qu’AGPM prenne en charge des configurations mixtes, nous vous recommandons vivement d’exécuter le client AGPM et le serveur AGPM sur la même ligne de système d’exploitation (par exemple, Windows 10 avec Windows Server 2016, Windows 8,1 avec Windows Server 2012 R2, etc.).

**Systèmes d’exploitation et systèmes d’exploitation pris en charge par AGPM 4.0 SP3**

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
<td align="left"><p>Windows10</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 ou Windows 8.1</p></td>
<td align="left"><p>Windows Server2012</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Windows Server 2008 ou Vista avec Service Pack 1 (SP1)</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Non pris en charge</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 ou Windows.</p></td>
</tr>
</tbody>
</table>

 

## Conditions préalables à l’installation d’AGPM 4.0 SP3

Le tableau suivant décrit le comportement d’AGPM 4.0 SP3 du client et du serveur lorsque .NET Framework 4.5.1, PowerShell 3,0 ou la console GPMC dans les outils d’administration de serveur distant est manquant.

| Client AGPM            |                                                                                                 |                                                                            | Serveur AGPM                                                                     |                                                                                                 |                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Système d’exploitation       | .NET Framework                                                                                  | PowerShell                                                                 | Outils d'administration de serveur distant                                              | .NET Framework                                                                                  | Outils d'administration de serveur distant                                              |
| Windows 10             | Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation. | Si PowerShell 3,0 n’est pas installé, le programme d’installation bloque l’installation. | Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation. | Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation. | Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation. |
| Windows 8.1            | Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation. | Si PowerShell 3,0 n’est pas installé, le programme d’installation bloque l’installation. | Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation. | Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation. | Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation. |
| WindowsServer2012R2 | Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation. | Si PowerShell 3,0 n’est pas installé, le programme d’installation bloque l’installation. | Si la console GPMC n’est pas activée, le programme d’installation l’active au cours de l’installation.   | Si .NET Framework 4.5.1 n’est pas activé ou installé, le programme d’installation bloque l’installation. | Si la console GPMC n’est pas activée, le programme d’installation l’active au cours de l’installation.   |

 

## Obtention de technologies MDOP


Le pack d’optimisation du Bureau d’AGPM 4,0 est un composant de l’application MDOP 2015. MDOP fait partie de Microsoft Software Assurance. Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Rubriques connexes


[Gestion avancée des stratégies de groupe](index.md)

[Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP3](release-notes-for-microsoft-advanced-group-policy-management-40-sp3.md)

[Choix de la version d'AGPM à installer](choosing-which-version-of-agpm-to-install.md)

 

 





