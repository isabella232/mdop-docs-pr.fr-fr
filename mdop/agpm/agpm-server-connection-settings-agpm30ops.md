---
title: Paramètres de connexion du serveur AGPM
description: Paramètres de connexion du serveur AGPM
author: dansimp
ms.assetid: 5f03e397-b868-4c49-9cbf-a5f5d0ddcc39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9ee1e67eb2c565bcf833314d82cdf611e2caa85
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804639"
---
# Paramètres de connexion du serveur AGPM


Vous pouvez utiliser les paramètres de modèle d’administration pour la gestion avancée de la stratégie de groupe pour configurer de manière centralisée les connexions serveur AGPM pour les administrateurs de stratégie de groupe pour lesquels un objet de stratégie de groupe avec ces paramètres est appliqué.

Les paramètres suivants sont disponibles sous User Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM lors de la modification d’un objet de stratégie de groupe.

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
<td align="left"><p><strong>AGPM: spécifier le serveur AGPM par défaut (tous les domaines)</strong></p></td>
<td align="left"><p>Ce paramètre de stratégie vous permet de spécifier un serveur AGPM par défaut pour tous les domaines. Ce paramètre est utilisé uniquement par les clients AGPM et limite les administrateurs de stratégie de groupe à la connexion à une autre archive. Vous pouvez remplacer cette valeur par défaut pour des domaines individuels à l’aide du <strong> paramètre AGPM: spécifier les serveurs AGPM </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>AGPM: spécifier les serveurs AGPM</strong></p></td>
<td align="left"><p>Ce paramètre de stratégie vous permet de spécifier les serveurs AGPM pour des domaines individuels. Ce paramètre est utilisé uniquement par les clients AGPM et limite les administrateurs de stratégie de groupe à la connexion à une autre Archive pour le domaine spécifié. Pour spécifier un serveur AGPM par défaut, utilisez le <strong> paramètre AGPM: spécifiez le serveur AGPM par défaut (tous les domaines), </strong> puis utilisez ce paramètre de stratégie pour remplacer la valeur par défaut pour chaque domaine.</p></td>
</tr>
</tbody>
</table>

 

### Références supplémentaires

-   [Dossier Modèles d'administration](administrative-templates-folder-agpm30ops.md)

-   [Exécution de tâches d'administrateur AGPM](performing-agpm-administrator-tasks-agpm30ops.md)

 

 





