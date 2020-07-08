---
title: Paramètres de visibilité des fonctionnalités
description: Paramètres de visibilité des fonctionnalités
author: dansimp
ms.assetid: 9db2ba03-fb75-4f95-9138-ec89b9fc8d01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26f19895d0a9163885779688ba7d89f6d16f2a17
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808454"
---
# Paramètres de visibilité des fonctionnalités


Les paramètres de modèle d’administration de Advanced Group Policy Management (AGPM) vous permettent de configurer de manière centralisée la visibilité des nœuds de **contrôle de modification** et de l’onglet **historique** pour les administrateurs de stratégie de groupe pour lesquels un objet de stratégie de groupe avec ces paramètres est appliqué.

Les paramètres suivants sont disponibles sous utilisateurs Configuration\\Administrative Templates\\Windows Components\\Microsoft de la console de gestion \ \ restrictions/autorisation Snap-ins\\Extension dans l' **éditeur d’objets de stratégie de groupe** lors de la modification d’un objet de stratégie de groupe dans la console de gestion des stratégies de groupe (GPMC). Si ce chemin d’accès n’est pas visible, cliquez avec le bouton droit sur **modèles d’administration**, puis ajoutez le modèle AGPM. admx ou AGPM. adm.

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
<td align="left"><p><strong>Contrôle du changement d’AGPM</strong></p></td>
<td align="left"><p>S’il est activé ou non configuré, le <strong> nœud de contrôle de modification </strong> est visible dans la console GPMC.</p>
<p>S’il est désactivé, le <strong> nœud de contrôle de modification </strong> n’est pas visible dans la console GPMC.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Extension de lien AGPM</strong></p></td>
<td align="left"><p>S’il est activé ou non configuré, un <strong> </strong> onglet historique s’affiche dans la console GPMC pour chaque objet GPO lié.</p>
<p>S’il est désactivé, l' <strong> </strong> onglet historique n’est pas visible pour les objets de stratégie de groupe liés.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Extension d’objet de stratégie de groupe AGPM</strong></p></td>
<td align="left"><p>S’il est activé ou non configuré, un <strong> </strong> onglet historique s’affiche dans la console GPMC pour chaque GPO.</p>
<p>S’il est désactivé, l' <strong> </strong> onglet historique n’est pas visible pour les objets de stratégie de groupe.</p></td>
</tr>
</tbody>
</table>

 

### Références supplémentaires

-   [Paramètres de modèles d'administration](administrative-template-settings.md)

 

 





