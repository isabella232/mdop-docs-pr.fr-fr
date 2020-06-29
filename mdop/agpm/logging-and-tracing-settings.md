---
title: Paramètres Journalisation et suivi
description: Paramètres Journalisation et suivi
author: dansimp
ms.assetid: db6b43c7-fdde-4d11-b5ab-a81346e56940
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bef0f8367647aad688c2aec7586ecdaae2e22143
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808366"
---
# Paramètres Journalisation et suivi


Les paramètres de modèle d’administration de Advanced Group Policy Management (AGPM) vous permettent de configurer de manière centralisée les options de journalisation et de suivi des serveurs et clients AGPM pour lesquels un objet de stratégie de groupe avec ces paramètres est appliqué.

Le paramètre suivant est disponible sous Computer Configuration\\Administrative Templates\\Windows Components\\AGPM dans l' **éditeur d’objets de stratégie de groupe** lors de la modification d’un objet de stratégie de groupe dans la console de gestion des stratégies de groupe (GPMC). Si ce chemin d’accès n’est pas visible, cliquez avec le bouton droit sur **modèles d’administration**, puis ajoutez le modèle AGPM. admx ou AGPM. adm.

**Emplacement des fichiers de suivi**:

-   Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

-   Serveur:%CommonAppData%\\Microsoft\\AGPM\\agpmserv.log

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
<td align="left"><p><strong>Journalisation d’AGPM</strong></p></td>
<td align="left"><p>S’il est activé, ce paramètre configure si le suivi est activé et le niveau de détail. Ce paramètre affecte à la fois les composants client et serveur d’AGPM.</p>
<p>Si elle est désactivée ou n’est pas configurée, ce paramètre n’a aucun effet.</p></td>
</tr>
</tbody>
</table>

 

### Références supplémentaires

-   [Paramètres de modèles d'administration](administrative-template-settings.md)

 

 





