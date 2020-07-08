---
title: Paramètres de connexion du serveur AGPM
description: Paramètres de connexion du serveur AGPM
author: dansimp
ms.assetid: faf78e5b-2b0d-4069-9b8c-910add892200
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63163de0a1adf744e6d442b8073e5b32352ed67
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804663"
---
# Paramètres de connexion du serveur AGPM


Vous pouvez utiliser les paramètres de modèle d’administration pour la gestion avancée de la stratégie de groupe pour configurer de manière centralisée les connexions serveur AGPM pour les administrateurs de stratégie de groupe pour lesquels un objet de stratégie de groupe avec ces paramètres est appliqué.

Les paramètres suivants sont disponibles sous User Configuration\\Administrative Templates\\Windows Components\\AGPM lors de la modification d’un objet de stratégie de groupe. Si ce chemin d’accès n’est pas visible, cliquez avec le bouton droit sur **modèles d’administration**, puis ajoutez le modèle AGPM. admx ou AGPM. adm.

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
<td align="left"><p><strong>Serveur AGPM (tous les domaines)</strong></p></td>
<td align="left"><p>Si cette option est activée, vous configurez de manière centralisée une connexion de serveur AGPM pour une utilisation par tous les domaines et désactive les paramètres sous l' <strong> onglet serveur AGPM </strong> pour les administrateurs de stratégie de groupe. Pour plusieurs serveurs AGPM, configurez ce paramètre avec un serveur par défaut, puis configurez le <strong> paramètre serveur AGPM </strong> dans le modèle d’administration pour remplacer ce serveur par d’autres domaines.</p>
<p>Si elle est désactivée ou n’est pas configurée, les administrateurs de stratégie de groupe doivent sélectionner le serveur AGPM à afficher pour chaque domaine sous l' <strong> onglet serveur AGPM </strong> dans AGPM.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Serveur AGPM</strong></p></td>
<td align="left"><p>Si ce paramètre est activé, il configure de manière centralisée plusieurs serveurs AGPM spécifiques au domaine, <strong> en remplaçant le paramètre serveur AGPM (tous les domaines) </strong> dans le modèle d’administration. Si votre environnement nécessite uniquement un serveur AGPM unique, utilisez uniquement le <strong> paramètre serveur AGPM (tous les domaines) du </strong> modèle d’administration.</p>
<p>Si ce paramètre est désactivé ou n’est pas configuré, le <strong> paramètre serveur AGPM (tous les domaines) du </strong> modèle d’administration configure la connexion au serveur AGPM.</p></td>
</tr>
</tbody>
</table>

 

### Références supplémentaires

-   [Paramètres de modèles d'administration](administrative-template-settings.md)

-   [Exécution de tâches d'administrateur AGPM](performing-agpm-administrator-tasks.md)

 

 





