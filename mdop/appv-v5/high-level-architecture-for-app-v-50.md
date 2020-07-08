---
title: Architecture de haut niveau pour App-V5.0
description: Architecture de haut niveau pour App-V5.0
author: dansimp
ms.assetid: fdf8b841-918f-4672-b352-0f2b9519581b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0ec105ffcc3213e488615603484b2de6bafce4d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805815"
---
# Architecture de haut niveau pour App-V5.0


Utilisez les informations suivantes pour vous simplifier le déploiement de Microsoft Application Virtualization (App-V) 5,0.

## Présentation de l’architecture


Une implémentation standard d’App-V 5,0 se compose des éléments suivants.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Élément</th>
<th align="left">Informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Serveur de gestion App-V 5,0</p></td>
<td align="left"><p>Le serveur de gestion App-V 5,0 fournit une fonctionnalité de gestion générale de l’infrastructure App-V 5,0. De plus, vous pouvez installer plusieurs instances du serveur de gestion dans votre environnement, qui offre les avantages suivants:</p>
<ul>
<li><p>Tolérance de panne et haute disponibilité: l’installation et la configuration du serveur de gestion App-V 5,0 sur deux ordinateurs séparés peuvent être utiles lorsque l’un des serveurs est indisponible ou hors connexion.</p>
<p>Vous pouvez également améliorer la disponibilité de l’application-V 5,0 en installant le serveur de gestion sur plusieurs ordinateurs. Dans ce scénario, un équilibreur de charge réseau doit également être considéré de sorte que les requêtes serveur soient équilibrées.</p></li>
<li><p>Extensibilité: vous pouvez ajouter d’autres serveurs de gestion nécessaires à la prise en charge d’une forte charge, par exemple pour installer plusieurs serveurs derrière un équilibreur de charge.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Serveur de publication 5,0 App-V</p></td>
<td align="left"><p>Le serveur de publication App-V 5,0 fournit des fonctionnalités pour l’hébergement et la diffusion en continu d’applications virtuelles. Le serveur de publication ne nécessite pas de connexion de base de données et prend en charge les protocoles suivants:</p>
<ul>
<li><p>HTTP et HTTPs</p></li>
</ul>
<p>Vous pouvez également améliorer la disponibilité de l’application-V 5,0 en installant le serveur de publication sur plusieurs ordinateurs. Un équilibrage de charge réseau doit également être considéré de sorte que les requêtes serveur soient équilibrées.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Serveur de création de rapports App-V 5,0</p></td>
<td align="left"><p>Le serveur de création de rapports App-V 5,0 permet aux utilisateurs autorisés d’exécuter et d’afficher des rapports App-V 5,0 et des rapports ad hoc existants qui leur permettent de gérer l’infrastructure App-V 5,0. Le serveur de création de rapports nécessite une connexion à la base de données de création de rapports App-V 5,0. Vous pouvez également améliorer la disponibilité de l’application-V 5,0 en installant le serveur de création de rapports sur plusieurs ordinateurs. Un équilibrage de charge réseau doit également être considéré de sorte que les requêtes serveur soient équilibrées.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client App-V 5,0</p></td>
<td align="left"><p>Le client App-V 5,0 permet aux packages créés à l’aide de App-V 5,0 de s’exécuter sur des ordinateurs cibles.</p></td>
</tr>
</tbody>
</table>

 

**Remarques**  Si vous utilisez App-V 5,0 avec la distribution de logiciels électroniques (ESD), vous n’êtes pas tenu d’utiliser le serveur de gestion App-V 5,0, mais vous pouvez toujours utiliser la fonctionnalité de création de rapports et de streaming de App-V 5,0.

 






## Rubriques connexes


[Prise en main de l'application App-V5.0](getting-started-with-app-v-50--rtm.md)

 

 





