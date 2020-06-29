---
title: Planification du déploiement d'App-V5.1 avec un système de distribution électronique de logiciels
description: Planification du déploiement d'App-V5.1 avec un système de distribution électronique de logiciels
author: dansimp
ms.assetid: c26602c2-5e8d-44e6-90df-adacc593607e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fde3f0ea4f1dec72b97143b4b27dd0b32a503b15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804950"
---
# Planification du déploiement d'App-V5.1 avec un système de distribution électronique de logiciels


Si vous utilisez un système de distribution de logiciels électronique pour déployer des packages App-V, consultez les considérations de planification suivantes. Pour plus d’informations sur l’utilisation de System Center Configuration Manager pour déployer App-V, voir [Présentation de la gestion des applications dans Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).

Passez en revue les options suivantes relatives aux composants et à l’architecture qui s’appliquent lorsque vous utilisez un système de déploiement ESD pour déployer des packages App-V:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Option ou option de déploiement requise</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>La base de données de gestion et le serveur de gestion App-V n’est pas requis.</p></td>
<td align="left"><p>Ces fonctions sont gérées par la solution ESD implémentée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Vous pouvez déployer le serveur de création de rapports d’application et de la base de données de création de rapports en parallèle avec la fonction ESD.</p></td>
<td align="left"><p>Le déploiement côte à côte vous permet de recueillir des données et de générer des rapports.</p>
<p>Si vous activez le client App-V pour envoyer des informations de rapport et que vous n’utilisez pas le serveur de rapports d’applications-V, les données de rapport sont stockées dans les fichiers. XML associés.</p></td>
</tr>
</tbody>
</table>

 






## Rubriques connexes


[Envisager de déployer App-V](planning-to-deploy-app-v51.md)

 

 





