---
title: Mise à jour de MED-V2.0
description: Mise à jour de MED-V2.0
author: dansimp
ms.assetid: beea2f54-42d7-4a17-98e0-d243a8562265
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 62e8987ec511783422b8dd336dd4f3be2008c9b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810133"
---
# Mise à jour de MED-V2.0


Contribuez à sécuriser votre système en appliquant les mises à jour de sécurité appropriées pour Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Mise à jour de MED-V


Vous pouvez mettre à jour MED-V de manière interactive, par l’utilisateur final ou en silence à l’aide d’un système de distribution de logiciels électronique. L’installation de l’agent hôte MED-V met à niveau l’agent hôte MED-V, puis met à jour l’espace de travail MED-V si nécessaire. L’agent d’hébergement MED-V et l’agent invité se synchronisent. Si des applications sont exécutées à partir de l’espace de travail MED-V alors que l’agent hôte MED-V est en cours de mise à jour, le redémarrage de l’ordinateur hôte est requis pour achever la mise à jour. Si aucune application n’est en cours d’exécution, MED-V est redémarré automatiquement et la mise à niveau est terminée sans redémarrage de l’ordinateur hôte.

Si vous effectuez une mise à jour de MED-V à l’aide d’un système de distribution de logiciels électronique, vous pouvez contrôler le comportement de redémarrage. Pour cela, supprimez le redémarrage en tapant **REBOOT = «ReallySuppress»** à l’invite de commandes lors de l’installation d' MED-V\_HostAgent\_Setup.exe. Ensuite, configurez le système de distribution de logiciels électronique pour capturer le code de retour 3010 (qui indique qu’un redémarrage est requis) et exécutez le comportement de redémarrage.

## Rubriques connexes


[Informations techniques de référence pour MED-V](technical-reference-for-med-v.md)

 

 





