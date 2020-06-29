---
title: Diagnostic d'échecs du système avec l'Analyseur d'incident
description: Diagnostic d'échecs du système avec l'Analyseur d'incident
author: dansimp
ms.assetid: ce3d3186-54fb-45b2-b5ce-9bb7841db28f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: abb9d1ec99236199e0866a3b23219dd412bc9da6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810619"
---
# Diagnostic d'échecs du système avec l'Analyseur d'incident


L' **Analyseur de blocage** dans Microsoft Diagnostics and Recovery Tools (DaRT) 8,0 vous permet de déboguer un fichier de vidage de mémoire sur un ordinateur exécutant Windows, puis de diagnostiquer les erreurs d’ordinateur associées. L' **Analyseur de blocage** utilise les outils de débogage de Microsoft pour Windows afin d’examiner un fichier de vidage de mémoire pour le pilote ayant entraîné l’échec de l’ordinateur. Vous pouvez exécuter l’analyseur d’incident sur un ordinateur d’utilisateur final ou en mode autonome sur un ordinateur autre qu’un ordinateur d’utilisateur final.

## Exécuter l’analyseur d’incidents sur un ordinateur d’utilisateur final


En règle générale, vous exécutez l' **analyse crash** à partir de la fenêtre du **jeu d’outils de diagnostics et de récupération** sur un ordinateur d’utilisateur final qui rencontre le problème. L' **Analyseur de blocage** tente de rechercher les outils de débogage pour Windows sur l’ordinateur qui rencontre le problème. Si la boîte de dialogue chemin d’accès au répertoire est vide, vous devez entrer l’emplacement ou accéder à l’emplacement des outils de débogage pour Windows (vous pouvez télécharger les fichiers à partir de Microsoft). Vous devez également indiquer un chemin d’accès à l’endroit où se trouvent les fichiers de symboles.

Si vous avez inclus les outils de débogage de Microsoft pour Windows et les fichiers de symboles lors de la création de l’image de récupération 8,0 de DaRT, les outils et fichiers de symboles doivent être disponibles lorsque vous exécutez l' **analyseur d’incidents** sur l’ordinateur qui rencontre le problème. Si vous ne l’avez pas inclus dans l’image de récupération DaRT, ou si les problèmes de taille de disque ou de connectivité réseau vous empêchent de les obtenir, vous pouvez également exécuter l’analyseur d’incident en mode autonome sur un ordinateur autre que l’ordinateur de l’utilisateur final, comme décrit dans la section suivante.

[Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-8.md)

## <a href="" id="run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-s-computer"></a>Exécution de l’analyseur d’incident en mode autonome sur un ordinateur autre que l’ordinateur d’un utilisateur final


Même si vous exécutez généralement **crash Analyzer** sur l’ordinateur de l’utilisateur final qui rencontre le problème, vous pouvez également exécuter l’analyseur d’incident en mode autonome, sur un ordinateur autre qu’un ordinateur d’utilisateur final. Vous pouvez opter pour cette option si vous n’avez pas inclus les outils de débogage Windows dans l’image de récupération DaRT ou si les problèmes de taille de disque ou de connectivité réseau vous empêchent d’obtenir les outils de débogage. Dans ce cas, vous pouvez copier le fichier de vidage à partir du problème et l’analyser sur un ordinateur sur lequel est installée la version autonome d' **crash Analyzer** , par exemple sur un ordinateur de l’agent de support technique.

[Procédure pour exécuter l'Analyseur d'incident en mode autonome sur un ordinateur autre qu'un ordinateur d'utilisateur final](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-8.md)

## Comment s’assurer que l’analyseur d’incidents peut accéder aux fichiers de symboles


Pour déboguer des applications qui ont cessé de répondre, vous devez accéder au fichier de symboles, qui est distinct du programme. Bien que les fichiers de symboles soient automatiquement téléchargés lors de l’exécution de l’analyseur d’incidents, il peut arriver que le problème ne soit pas possible d’accéder à Internet. Il existe plusieurs façons de vérifier que vous avez garanti l’accès aux fichiers de symboles.

[Procédure pour s'assurer que l'Analyseur d'incident puisse accéder aux fichiers de symboles](how-to-ensure-that-crash-analyzer-can-access-symbol-files.md)

## Autres ressources pour diagnostiquer les échecs système avec l’analyseur d’incidents


[Opérations de DaRT8.0](operations-for-dart-80-dart-8.md)

 

 





