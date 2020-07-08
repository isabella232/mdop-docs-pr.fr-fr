---
title: Liste de contrôle pour l'évaluation des applications cœur de métier pour UE-V1.0
description: Liste de contrôle pour l'évaluation des applications cœur de métier pour UE-V1.0
author: dansimp
ms.assetid: 3bfaab30-59f7-4099-abb1-d248ce0086b8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 133bc5d195763b7281fd8d152e153231ac4c4d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811766"
---
# Liste de contrôle pour l'évaluation des applications cœur de métier pour UE-V1.0


Pour évaluer les applications métier qui doivent être incluses dans votre déploiement UE-V, envisagez ce qui suit:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Cette application contient-elle des paramètres que l’utilisateur peut personnaliser?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Est-il important de l’itinérance de ces paramètres?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ces paramètres utilisateur sont-ils déjà gérés par une solution de gestion des applications ou de stratégie de paramètres? UE-V applique les paramètres d’application au lancement de l’application et aux paramètres Windows lors de l’ouverture de session, du déverrouillage ou des événements de connexion à distance. Si vous utilisez UE-V avec d’autres solutions de stratégie de contrôle, les utilisateurs peuvent observer une incohérence entre les paramètres errants.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Les paramètres de l’application sont-ils spécifiques de votre ordinateur? Les préférences et personnalisations apportées à l’application qui sont associées à des configurations matérielles ou spécifiques à des ordinateurs ne sont pas toujours itinérantes entre les sessions et peuvent entraîner une faible connaissance de l’application.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Est-ce que les paramètres du Windows Store se trouvent dans le dossier Program Files ou dans le répertoire de fichiers qui se trouve dans le répertoire <strong> Users </strong> \ [user name] \ <strong> AppData </strong>  \  <strong> LocalLow </strong> ? Les données d’application stockées dans l’un de ces emplacements ne doivent généralement pas être itinérantes avec l’utilisateur, car ces données sont spécifiques à l’ordinateur ou les données sont trop volumineuses pour une itinérance.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>L’application stocke-t-elle des paramètres dans un fichier qui contient d’autres données d’application qui ne doivent pas être itinérantes? UE-V synchronise les fichiers comme une seule unité. Si les paramètres sont stockés dans des fichiers qui incluent des données d’application autres que des paramètres, la synchronisation de ces données supplémentaires risque de provoquer une médiocre application.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Quelle est la taille des fichiers contenant les paramètres? Les performances de la synchronisation des paramètres peuvent être affectées par de gros fichiers. L’inclusion de fichiers volumineux peut avoir un impact sur les performances de la synchronisation des paramètres.</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Planification de méthodes de configuration d'UE-V](planning-for-ue-v-configuration-methods.md)

[Planification pour UE-V1.0](planning-for-ue-v-10.md)

 

 





