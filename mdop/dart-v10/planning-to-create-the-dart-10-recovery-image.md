---
title: Planification pour créer l'image de récupération DaRT10
description: Planification pour créer l'image de récupération DaRT10
author: dansimp
ms.assetid: a0087d93-b88f-454b-81b2-3c7ce3718023
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 44cf052eaffd19645885618da9104e5b0a50cfd5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809678"
---
# Planification pour créer l'image de récupération DaRT10


Utilisez les informations de cette section lorsque vous envisagez de créer l’image de récupération Microsoft Diagnostics and Recovery Tools (DaRT) 10.

## Planification de la création de l’image de récupération de DaRT 10


Lorsque vous créez l’image de récupération DaRT, vous devez choisir les outils à inclure dans l’image. Pour prendre la décision, tenez compte du fait que les utilisateurs finaux peuvent avoir accès à ces outils. Si les techniciens du support technique emportent le média d’image de récupération aux ordinateurs des utilisateurs finaux pour diagnostiquer les problèmes, vous pouvez installer tous les outils sur l’image de récupération. Si vous envisagez de diagnostiquer les ordinateurs des utilisateurs finaux à distance, vous souhaiterez peut-être désactiver certains outils, tels que l’effacement de disque et l’éditeur du Registre, puis activer d’autres outils, y compris la connexion à distance.

Lorsque vous créez l’image de récupération DaRT, vous devez également indiquer si vous souhaitez inclure d’autres pilotes ou fichiers. Déterminez les emplacements des pilotes ou fichiers supplémentaires que vous voulez inclure dans l’image de récupération DaRT.

Pour plus d’informations sur les outils DaRT, voir [vue d’ensemble des outils dans DART 10](overview-of-the-tools-in-dart-10.md). Pour plus d’informations sur la création d’une image de récupération sécurisée, voir [considérations relatives à la sécurité de DART 10](security-considerations-for-dart-10.md).

## Conditions préalables à l’image de récupération


Les éléments suivants sont requis ou recommandés pour la création de l’image de récupération DaRT:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Prérequises</strong></p></td>
<td align="left"><p><strong>Détails</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Fichiers sources Windows 10</p></td>
<td align="left"><p>Requis pour créer l’image de récupération DaRT. Spécifiez le chemin d’accès d’un DVD Windows 10 ou d’un fichier source Windows 10.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Outils de débogage Windows pour votre plate-forme</p></td>
<td align="left"><p>Requis lors de l’exécution <strong> de l’analyseur </strong> d’incidents pour déterminer la cause de l’échec de l’ordinateur. Nous vous recommandons de spécifier le chemin d’accès des outils de débogage Windows au moment de la création de l’image de récupération DaRT. Vous pouvez télécharger les outils de débogage Windows suivants: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)"> Télécharger et installer les outils de débogage pour Windows </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Facultatif: fichiers de symboles Windows à utiliser avec l' <strong> analyseur d’incidents</strong></p></td>
<td align="left"><p>En général, les informations de débogage sont stockées dans un fichier de symboles différent du programme. Vous devez avoir accès aux informations de symbole lors du débogage d’une application qui a cessé de répondre (par exemple, si elle a cessé de fonctionner). Pour plus d’informations, reportez-vous à la rubrique <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)"> diagnostic des pannes système avec l’analyseur d’incidents </a> .</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes

[Planification du déploiement de DaRT10](planning-to-deploy-dart-10.md)

 

 




