---
title: Fichier journal d'Application Virtualization Client
description: Fichier journal d'Application Virtualization Client
author: dansimp
ms.assetid: ac4b3e4a-a220-4c06-bd60-af7dc318b3a9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 52908aa583d3d673b8a229df14e56f1c71633ef4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806622"
---
# Fichier journal d'Application Virtualization Client


Le fichier journal pour le client Application Virtualization (App-V) capture des informations détaillées sur les opérations et les conditions d’erreur. Vous pouvez l’utiliser lorsque vous vérifiez la fonctionnalité et que vous rencontrez des problèmes.

Lorsque le client App-V est installé pour la première fois, le fichier journal est créé par défaut dans l’emplacement indiqué dans le tableau suivant. L’emplacement du fichier journal est nouveau pour la virtualisation des applications (App-V) 4,5, même si l’emplacement ne sera pas modifié si le client est mis à niveau à partir d’une version antérieure.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de fichier journal</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>sftlog.txt</strong></p></td>
<td align="left"><p>Fournit des informations générales sur les erreurs et les opérations du client App-V. Utilisez ce journal comme point de départ pour la résolution des erreurs clientes App-V.</p>
<p>Emplacement du fichier journal pour le client de bureau ou le client pour les services Bureau à distance (anciennement services Terminal Server):</p>
<ul>
<li><p><em>C:\Documents and Settings\All Users\Application Data\Microsoft\Application Virtualization client </em> : WindowsXP, Windows Server 2003</p></li>
<li><p><em>Client de virtualisation C:\ProgramData\Microsoft\Application </em> : Windows Vista, Windows Server 2008</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Référence d'Application Virtualization Client](application-virtualization-client-reference.md)

 

 





