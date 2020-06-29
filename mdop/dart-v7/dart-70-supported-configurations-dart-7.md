---
title: Configurations prises en charge par DaRT7.0
description: Configurations prises en charge par DaRT7.0
author: dansimp
ms.assetid: e9ee87b0-3254-4625-b178-17b2f5b8f8c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b074a061c402f86769e42d873e0119ac54080c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804417"
---
# Configurations prises en charge par DaRT7.0


Votre environnement peut déjà respecter les exigences de configuration fournies ici pour pouvoir installer et exécuter Microsoft Diagnostics et Recovery Tools Tools (DaRT) 7. Il s’agit de l’image de récupération et de l’espace disque requis.

## Configuration requise pour l’image de récupération de DaRT 7


Aucune création d’image de récupération multiplateforme n’est prise en charge. Le tableau suivant spécifie le type d’image de récupération que vous devez créer et déployer dans votre entreprise:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Plateforme et version DaRT</th>
<th align="left">Exigences relatives à l’image de récupération</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>64 bits DaRT 7,0</p></td>
<td align="left"><p>Créez et utilisez une image de récupération DaRT 64 bits.</p></td>
</tr>
<tr class="even">
<td align="left"><p>32 bits DaRT 7,0</p></td>
<td align="left"><p>Créez et utilisez une image de récupération DaRT 32 bits.</p></td>
</tr>
</tbody>
</table>

 

## Configuration requise pour l’ordinateur de l’utilisateur final de DaRT 7


La fenêtre du **jeu d’outils de diagnostics et de récupération** dans DART nécessite que l’ordinateur de destination utilise l’un des systèmes d’exploitation suivants avec la quantité de mémoire système spécifiée pour DART:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Systèmed’exploitation</th>
<th align="left">Configuration système requise pour DaRT</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>D’une 64 (2 Go)</p></td>
<td align="left"><p>2,5 Go de mémoire système</p></td>
</tr>
<tr class="even">
<td align="left"><p>Le 32-bit (1 Go)</p></td>
<td align="left"><p>1,5 Go de mémoire système</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 (512 Mo)</p></td>
<td align="left"><p>1 Go de mémoire système</p></td>
</tr>
</tbody>
</table>

 

Le système DaRT dispose également de la configuration matérielle minimum suivante:

-   Un lecteur de CD ou un DVD ou un port USB

    C’est obligatoire si vous déployez DaRT au sein de votre entreprise à l’aide d’un CD, d’un DVD ou d’un lecteur USB.

-   Prise en charge du BIOS pour le démarrage de l’ordinateur à partir d’un CD ou d’un DVD, d’une clé USB ou d’une partition distante ou de récupération

## Rubriques connexes


[Planification du déploiement de DaRT7.0](planning-to-deploy-dart-70.md)

 

 





