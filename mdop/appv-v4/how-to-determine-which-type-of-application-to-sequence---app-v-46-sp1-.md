---
title: Déterminer le type d’application à séquence (App-V 4,6 SP1)
description: Déterminer le type d’application à séquence (App-V 4,6 SP1)
author: dansimp
ms.assetid: 936abee2-98f1-45fb-9f0d-786e1d7464b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 001f6afa36ca28eb1b8e0cc2ccc161cef4194d24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807126"
---
# Déterminer le type d’application à séquence (App-V 4,6 SP1)


Vous pouvez séquencer trois types d’applications de base à l’aide du Sequencer Microsoft Application Virtualization (App-V).

## Pour déterminer le type d’application à séquencer


Utilisez le tableau suivant pour déterminer le type d’application que vous devez séquencer et obtenir plus d’informations sur la façon de séquencer l’application.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Type d’application</th>
<th align="left">Description</th>
<th align="left">Plus d’informations</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Standard</p></td>
<td align="left"><p>Sélectionnez cette option pour créer un package qui contient une application ou une suite d’applications. Cette option doit être sélectionnée pour la plupart des applications que vous envisagez de séquencer.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-standard-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Standard Application (App-V 4.6 SP1)](how-to-sequence-a-new-standard-application--app-v-46-sp1-.md)">Procédure pour séquencer une nouvelle application standard (App-V4.6SP1</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Module complémentaire ou plug-in</p></td>
<td align="left"><p>Sélectionnez cette option pour créer un package qui étend les fonctionnalités d’une application standard, par exemple un plug-in pour Microsoft Excel. De plus, vous pouvez utiliser les plug-ins pour les applications installées en mode natif ou un autre package lié à l’aide de la composition suite dynamique. Pour plus d’informations sur la composition de la suite dynamique, voir <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> utilisation de la composition suite dynamique </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)](how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md)">Procédure pour séquencer un nouveau module complémentaire ou plug-in (App-V4.6 SP1)</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Intergiciels</p></td>
<td align="left"><p>Sélectionnez cette option pour créer un package requis par une application standard (par exemple, Microsoft .NET Framework). Les packages middleware permettent de créer des liens vers d’autres packages à l’aide de la composition suite dynamique. Pour plus d’informations sur la composition de la suite dynamique, voir <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> utilisation de la composition suite dynamique </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Middleware Application (App-V 4.6 SP1)](how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md)">Procédure pour séquencer une nouvelle application d'intergiciel (middleware) (App-V4.6SP1)</a></p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Tâches pour Application Virtualization Sequencer (App-V4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





