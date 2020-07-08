---
title: Planification du déploiement de DaRT7.0
description: Planification du déploiement de DaRT7.0
author: dansimp
ms.assetid: 05e97cdb-a8c2-46e4-9c75-a7d12fe26fe8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09725e994a95f4f93ae655402e7577e137e33f18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808682"
---
# Planification du déploiement de DaRT7.0


Il existe un certain nombre de configurations et de configurations de déploiement différentes que vous devez prendre en compte avant de créer le plan de déploiement. Cette section contient des informations qui vous aideront à collecter les informations nécessaires pour formuler un plan de déploiement qui répond le mieux à vos besoins professionnels.

Prenez en compte les points suivants lorsque vous planifiez l’installation de Microsoft Diagnostics and Recovery Tools (DaRT) 7:

-   Lors de l’installation de DaRT, vous pouvez installer toutes les fonctionnalités sur un ordinateur d’administration informatique sur lequel vous exécuterez toutes les tâches associées à l’exécution de DaRT. Ou vous pouvez installer uniquement la fonctionnalité DaRT qui crée l’image de récupération sur l’ordinateur de l’administrateur informatique. Ensuite, installez la fonctionnalité utilisée pour exécuter DaRT, telle que la **visionneuse de connexion à distance** et l' **analyseur d’incident**de DART, sur un ordinateur d’agent de support technique.

-   Pour pouvoir exécuter DaRT à distance, assurez-vous que l’ordinateur de l’agent de support technique et tous les ordinateurs qui peuvent résoudre les problèmes distants se trouvent sur le même réseau.

-   Avant de déployer le DaRT en production, vous pouvez commencer par créer un environnement de laboratoire pour le test. Un atelier de test doit inclure un minimum de deux ordinateurs, un pour agir en tant qu’administrateur informatique/agent du support technique et un pour agir en tant qu’ordinateur de l’utilisateur final. Vous pouvez ou utiliser trois ordinateurs dans votre laboratoire si vous voulez séparer les responsabilités de l’administrateur informatique de celles de l’agent de support technique.

## Examiner les configurations prises en charge


Prenez connaissance des informations sur les configurations prises en charge de Microsoft Diagnostics and Recovery Tools (DaRT) 7 prises en charge pour vérifier que les ordinateurs que vous avez sélectionnés pour l’installation d’un client ou d’une fonctionnalité répondent à la configuration minimale requise en matière de matériel et de système d’exploitation.

[Configurations prises en charge par DaRT7.0](dart-70-supported-configurations-dart-7.md)

## Plan de création de l’image de récupération DaRT


Lorsque vous créez l’image de récupération DaRT, vous devez choisir les outils à inclure dans l’image. Lorsque vous prenez cette décision, rappelez-vous que les utilisateurs finaux peuvent avoir accès occasionnellement aux différents outils DaRT. Lorsque vous créez l’image de récupération, vous devez également indiquer si vous souhaitez inclure d’autres pilotes ou fichiers. Déterminez les emplacements des pilotes ou fichiers supplémentaires que vous voulez inclure dans l’image de récupération DaRT.

Prenez en compte les conditions préalables et d’autres recommandations en matière de planification pour la création de l’image de récupération DaRT.

[Planification pour créer l'image de récupération DaRT7.0](planning-to-create-the-dart-70-recovery-image.md)

## Planifier l’enregistrement et le déploiement de l’image de récupération DaRT


Plusieurs méthodes peuvent être utilisées pour enregistrer et déployer l’image de récupération DaRT. Lorsque vous déterminez la méthode à utiliser, examinez les avantages et inconvénients de chacun d’eux. Par ailleurs, réfléchissez à la façon dont vous souhaitez utiliser DaRT au sein de votre entreprise.

**Remarques**  Vous souhaiterez peut-être utiliser plusieurs méthodes au sein de votre organisation. Par exemple, vous pouvez démarrer dans DaRT à partir d’une partition distante dans la plupart des cas, et disposer d’un lecteur flash USB dans le cas où l’ordinateur de l’utilisateur final ne peut pas se connecter au réseau.

 

[Planification de la procédure pour enregistrer et déployer l'image de récupération DaRT7.0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md)

## Autres ressources pour planifier le déploiement de DaRT


[Planification de DaRT7.0](planning-for-dart-70-new-ia.md)

 

 





