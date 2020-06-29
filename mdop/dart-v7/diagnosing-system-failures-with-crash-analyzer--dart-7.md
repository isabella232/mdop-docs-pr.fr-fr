---
title: Diagnostic d'échecs du système avec l'Analyseur d'incident
description: Diagnostic d'échecs du système avec l'Analyseur d'incident
author: dansimp
ms.assetid: 170d40ef-4edb-4a32-a349-c285c0ea5e56
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c5f8b7e189de024d7ceb84f8cfc151dc82d56ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809972"
---
# Diagnostic d'échecs du système avec l'Analyseur d'incident


L’analyseur de blocage dans Microsoft Diagnostics and Recovery Tools Tools (DaRT) 7 vous permet de déboguer un fichier de vidage sur incident sur un ordinateur exécutant Windows, puis de diagnostiquer les erreurs d’ordinateur associées. L’analyseur de blocage utilise les outils de débogage de Microsoft pour Windows afin d’examiner un fichier de vidage sur incident pour le pilote qui provoquait l’échec de l’ordinateur.

## Exécuter l’analyseur d’incidents sur un ordinateur d’utilisateur final


En règle générale, vous exécutez l’analyse crash à partir de la fenêtre de l’ensemble de diagnostics et de récupération sur un ordinateur d’utilisateur final qui rencontre des problèmes. L’analyseur de blocage tente de rechercher les outils de débogage pour Windows sur l’ordinateur qui rencontre le problème. Si la boîte de dialogue chemin d’accès au répertoire est vide, vous devez entrer l’emplacement des outils de débogage pour Windows (vous pouvez télécharger les fichiers à partir de Microsoft). Vous devez également indiquer un chemin d’accès à l’endroit où se trouvent les fichiers de symboles.

Si vous avez inclus les outils de débogage de Microsoft pour Windows et les fichiers de symboles lors de la création de l’image de récupération DaRT, ils doivent être disponibles lorsque vous exécutez l’analyseur d’incidents sur l’ordinateur qui rencontre le problème.

[Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final](how-to-run-the-crash-analyzer-on-an-end-user-computer-dart-7.md)

## Exécution de l’analyseur d’incident en mode autonome sur un ordinateur autre qu’un ordinateur d’utilisateur final


L’analyseur de blocage tente de rechercher les outils de débogage pour Windows sur l’ordinateur qui rencontre le problème. Si la boîte de dialogue chemin d’accès au répertoire est vide, vous devez entrer l’emplacement des outils de débogage pour Windows (vous pouvez télécharger les fichiers à partir de Microsoft). Vous devez également indiquer un chemin d’accès à l’endroit où se trouvent les fichiers de symboles.

Si vous n’avez pas inclus les outils de débogage de Microsoft pour Windows et les fichiers de symboles lors de la création de l’image de récupération DaRT ou si des problèmes de taille de disque ou de connectivité réseau vous empêchent de les obtenir, vous pouvez copier le fichier de vidage à partir du problème et l’analyser sur un ordinateur sur lequel est installée la version autonome d’crash Analyzer. comme l’ordinateur d’un administrateur du support technique.

[Procédure pour exécuter l'Analyseur d'incident en mode autonome sur un ordinateur autre qu'un ordinateur d'utilisateur final](how-to-run-the-crash-analyzer-in-stand-alone-mode-on-a-computer-other-than-an-end-user-computer-dart-7.md)

## S’assurer que l’analyseur d’incidents peut accéder aux fichiers de symboles


En général, les informations de débogage sont stockées dans un fichier de symboles différent du fichier exécutable. Vous devez avoir accès aux informations de symbole lors du débogage d’une application qui a cessé de répondre (par exemple, si elle a été bloquée).

Les fichiers de symboles sont automatiquement téléchargés lors de l’exécution de l’analyseur d’incidents. Si votre ordinateur n’est pas connecté à Internet ou si le réseau nécessite que l’ordinateur accède à un serveur proxy HTTP, les fichiers de symboles ne peuvent pas être téléchargés.

[Procédure pour s'assurer que l'Analyseur d'incident puisse accéder aux fichiers de symboles](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md)

## Autres ressources pour diagnostiquer les échecs système avec l’analyseur d’incidents


[Opérations de DaRT7.0](operations-for-dart-70-new-ia.md)

 

 





