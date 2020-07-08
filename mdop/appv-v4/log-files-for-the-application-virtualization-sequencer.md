---
title: Fichiers journaux d'Application Virtualization Sequencer
description: Fichiers journaux d'Application Virtualization Sequencer
author: dansimp
ms.assetid: 1a296544-eab4-46f9-82ce-3136f8b578af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8cdf9dbc78ccdd03df5903ef4d42990099a2c53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806618"
---
# Fichiers journaux d'Application Virtualization Sequencer


Les fichiers journaux pour le Sequencer Application Virtualization (App-V) fournissent des informations détaillées sur les applications de séquençage, et peuvent être utiles lorsque vous vérifiez la fonctionnalité ou que vous rencontrez des problèmes.

Le tableau suivant fournit des informations sur les fichiers journaux et leurs emplacements par défaut, qui sont créés lors de l’utilisation du Sequencer.

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
<td align="left"><p><strong>sft-seq-log.txt</strong></p></td>
<td align="left"><p>Fournit des informations générales sur le séquençage d’une application. Utilisez ce journal comme point de départ pour la résolution des erreurs de Sequencer.</p>
<p>Emplacement du fichier journal: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</em></p>
<p>[Valeur du jeton de modèle] Emplacement du fichier journal App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [valeur de jeton de modèle]</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>sftbt.txt</strong></p></td>
<td align="left"><p>Fournit des informations sur les tâches de redémarrage de l’ordinateur qui se produisent lors du redémarrage simulé du Sequencer.</p>
<p>Emplacement du fichier journal: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</em></p>
<p>[Valeur du jeton de modèle] Emplacement du fichier journal App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [valeur de jeton de modèle]</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>SftCallBack.txt</strong></p></td>
<td align="left"><p>Fournit des informations générales sur les processus utilisés lors du séquençage.</p>
<p>Emplacement du fichier journal: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</em></p>
<p>[Valeur du jeton de modèle] Emplacement du fichier journal App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [valeur de jeton de modèle]</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Référence d'Application Virtualization Sequencer](application-virtualization-sequencer-reference.md)

 

 





