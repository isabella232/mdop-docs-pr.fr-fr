---
title: Planification pour créer l'image de récupération DaRT7.0
description: Planification pour créer l'image de récupération DaRT7.0
author: dansimp
ms.assetid: e5d49bee-ae4e-467b-9976-c1203f6355f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c370d2a69ec8ccea217696045e64e9a0ae724815
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808693"
---
# Planification pour créer l'image de récupération DaRT7.0


Utilisez les informations fournies dans cette section lorsque vous planifiez la création de l’image de récupération du jeu d’outils de diagnostics et de récupération Microsoft (DaRT) 7.

## Planification de la création de l’image de récupération de DaRT 7


Lorsque vous créez l’image de récupération DaRT, vous devez choisir les outils à inclure dans l’image. Lorsque vous prenez cette décision, rappelez-vous que les utilisateurs finaux peuvent avoir accès occasionnellement aux différents outils DaRT. Pour plus d’informations sur les outils DaRT, voir [vue d’ensemble des outils dans dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md). Pour plus d’informations sur la création d’une image de récupération sécurisée, voir [considérations relatives à la sécurité de DaRT 7,0](security-considerations-for-dart-70-dart-7.md).

Lorsque vous créez l’image de récupération DaRT, vous devez également indiquer si vous souhaitez inclure d’autres pilotes ou fichiers. Déterminez les emplacements des pilotes ou fichiers supplémentaires que vous voulez inclure dans l’image de récupération DaRT.

## Conditions préalables


Les éléments suivants sont requis ou recommandés pour la création de l’image de récupération DaRT:

-   Fichiers sources de Windows 7

    Vous devez indiquer le chemin d’accès d’un DVD Windows 7 ou d’un fichier source Windows 7. Les fichiers sources de Windows 7 sont requis pour créer l’image de récupération DaRT.

-   Outils de débogage Windows pour votre plate-forme

    Les outils de débogage de Windows sont requis lorsque vous exécutez l' **analyseur d’incidents** pour déterminer la cause du blocage sur un ordinateur. Nous vous recommandons de spécifier le chemin d’accès des outils de débogage Windows au moment de la création de l’image de récupération DaRT. Le cas échéant, vous pouvez télécharger les outils de débogage Windows suivants: [Télécharger et installer les outils de débogage pour Windows](https://go.microsoft.com/fwlink/?LinkId=99934).

-   Facultatif: définitions des **nettoyeurs de systèmes autonomes**

    Les définitions les plus récentes pour le **nettoyeur système autonome** sont nécessaires lorsque vous exécutez cet outil. Même si vous pouvez télécharger les définitions lors de l’exécution du **nettoyeur de systèmes autonome**, nous vous recommandons de télécharger les définitions les plus récentes au moment où vous créez l’image de récupération Dart. De cette manière, vous pouvez toujours exécuter l’outil avec les définitions les plus récentes même si le problème ne se connecte pas à l’ordinateur.

-   Facultatif: fichiers de symboles Windows à utiliser avec l' **analyseur d’incidents**

    En général, les informations de débogage sont stockées dans un fichier de symboles différent du fichier exécutable. Vous devez avoir accès aux informations de symbole lors du débogage d’une application qui a cessé de répondre (par exemple, si elle a été bloquée). Pour plus d’informations, reportez-vous à la rubrique [diagnostic des pannes système avec l’analyseur d’incidents](diagnosing-system-failures-with-crash-analyzer--dart-7.md).

## Rubriques connexes


[Planification du déploiement de DaRT7.0](planning-to-deploy-dart-70.md)

 

 





