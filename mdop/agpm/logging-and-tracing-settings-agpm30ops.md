---
title: Paramètres Journalisation et suivi
description: Paramètres Journalisation et suivi
author: dansimp
ms.assetid: 858b6fbf-65b4-42fa-95a9-69b04e5734d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 078bda16b5fcf968d45e0c4890487471105e8c44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808369"
---
# Paramètres Journalisation et suivi


Les paramètres de modèle d’administration de Advanced Group Policy Management (AGPM) vous permettent de configurer de manière centralisée les options de journalisation et de suivi des serveurs et clients AGPM pour lesquels un objet de stratégie de groupe avec ces paramètres est appliqué.

Le paramètre suivant est disponible sous Computer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM lors de la modification d’un objet de stratégie de groupe.

**Emplacement des fichiers de suivi**:

-   Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

-   Serveur:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paramètre</th>
<th align="left">Effet</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>AGPM: configurer la journalisation</strong></p></td>
<td align="left"><p>Ce paramètre de stratégie vous permet d’activer et de configurer la journalisation pour AGPM. Ce paramètre affecte à la fois les composants client et serveur d’AGPM.</p></td>
</tr>
</tbody>
</table>

 

### Références supplémentaires

-   [Dossier Modèles d'administration](administrative-templates-folder-agpm30ops.md)

 

 





