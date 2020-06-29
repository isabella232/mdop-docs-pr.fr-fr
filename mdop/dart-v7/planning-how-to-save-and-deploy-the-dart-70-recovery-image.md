---
title: Planification de la procédure pour enregistrer et déployer l'image de récupération DaRT7.0
description: Planification de la procédure pour enregistrer et déployer l'image de récupération DaRT7.0
author: dansimp
ms.assetid: d96e9363-6186-4fc3-9b83-ba15ed9694a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c292633949865d4b3f5053700f4219db3f1cf465
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809570"
---
# Planification de la procédure pour enregistrer et déployer l'image de récupération DaRT7.0


Utilisez les informations de cette section lorsque vous planifiez l’enregistrement et le déploiement de l’image de récupération du jeu d’outils de diagnostics et de récupération Microsoft (DaRT) 7.

## Planification de l’enregistrement et du déploiement de l’image de récupération DaRT


Vous pouvez enregistrer et déployer l’image de récupération DaRT en utilisant les méthodes suivantes. Lorsque vous déterminez la méthode à utiliser, examinez les avantages et inconvénients de chacun d’eux. Par ailleurs, réfléchissez à la façon dont vous souhaitez utiliser DaRT au sein de votre entreprise.

**Remarques**  Vous souhaiterez peut-être utiliser plusieurs méthodes au sein de votre organisation. Par exemple, vous pouvez démarrer dans DaRT à partir d’une partition distante dans la plupart des cas, et disposer d’un lecteur flash USB dans le cas où l’ordinateur de l’utilisateur final ne peut pas se connecter au réseau.

 

Le tableau suivant présente quelques avantages et inconvénients de chaque méthode d’utilisation de DaRT au sein de votre organisation.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Méthode de démarrage dans DaRT</th>
<th align="left">Avantages</th>
<th align="left">Inconvénients</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>À partir d’un CD ou d’un DVD</p></td>
<td align="left"><p>Prend en charge les scénarios dans lesquels l’enregistrement de démarrage principal (MBR) est endommagé et que vous ne pouvez pas accéder au disque dur. Prend également en charge les cas où il n’y a pas de connexion réseau.</p>
<p>Les utilisateurs des versions antérieures de DaRT sont les plus familiers et un CD ou un DVD peut être gravé directement depuis l' <strong> Assistant image de récupération DART </strong> .</p></td>
<td align="left"><p>Nécessite que quelqu’un ayant accès au CD ou DVD soit physiquement sur l’ordinateur de l’utilisateur final pour démarrer sur DaRT.</p></td>
</tr>
<tr class="even">
<td align="left"><p>À partir d’un lecteur flash USB (UFD)</p></td>
<td align="left"><p>Offre les mêmes avantages que le démarrage à partir d’un CD ou d’un DVD, et fournit également une assistance technique pour les ordinateurs qui n’ont pas de lecteur de CD ou de DVD.</p></td>
<td align="left"><p>Vous devez mettre en forme l’UFD avant de pouvoir l’utiliser pour démarrer sur DaRT. Il est également nécessaire que quelqu’un ayant accès au lecteur UFD soit physiquement connecté à l’ordinateur de l’utilisateur final pour démarrer dans DaRT.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>À partir d’une partition distante (réseau)</p></td>
<td align="left"><p>Vous permet d’effectuer un démarrage dans DaRT sans avoir besoin d’un CD, d’un DVD ou d’un lecteur USB. Il est également possible de mettre à jour des fichiers DaRT en toute simplicité, car il n’y a qu’un seul emplacement.</p></td>
<td align="left"><p>Ne fonctionne pas si l’ordinateur de l’utilisateur final n’est pas connecté au réseau.</p>
<p>Disponible à grande échelle pour les utilisateurs finaux et peut nécessiter des considérations en matière de sécurité lors de la création de l’image de récupération.</p></td>
</tr>
<tr class="even">
<td align="left"><p>À partir d’une partition de récupération</p></td>
<td align="left"><p>Vous permet d’effectuer un démarrage dans DaRT sans avoir besoin d’un CD, d’un DVD ou d’un UFD incluant des instances dans lesquelles il n’y a pas de connectivité réseau.</p>
<p>Par ailleurs, il est possible d’implémenter et de gérer le processus d’image Windows standard à l’aide d’outils de distribution automatisés, tels que Microsoft Endpoint Configuration Manager.</p></td>
<td align="left"><p>Lors de la mise à jour de DaRT, vous devez mettre à jour tous les ordinateurs de votre entreprise au lieu d’une seule partition (sur le réseau) ou de l’appareil (CD, DVD ou UFD).</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Planification du déploiement de DaRT7.0](planning-to-deploy-dart-70.md)

 

 





