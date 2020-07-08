---
title: À propos de DaRT8.0
description: À propos de DaRT8.0
author: dansimp
ms.assetid: ce91efd6-7d78-44cb-bb8f-1f43f768ebaa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e70816425dc4775b11596b91d7b5c0045830c6ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808663"
---
# À propos de DaRT8.0


Microsoft Diagnostics and Recovery Tools (DaRT) 8,0 vous aide à résoudre les problèmes liés à l’ordinateur Windows. Cela inclut les ordinateurs qui ne peuvent pas être démarrés. DaRT 8,0 est un puissant outil d’outils qui étend l’environnement de récupération Windows (WinRE). À l’aide de DaRT, vous pouvez analyser un problème pour en déterminer la cause, par exemple, en inspectant le journal des événements ou le Registre du système de l’ordinateur. Le DaRT prend en charge la récupération des disques durs de base qui contiennent des partitions (par exemple, partitions principales et lecteurs logiques) et prend en charge la récupération des volumes.

**Remarques**  Le DaRT ne prend pas en charge la récupération des disques dynamiques.

 

Le DaRT fournit également des outils pour vous aider à résoudre un problème dès que vous déterminez la cause du problème. Par exemple, vous pouvez utiliser les outils dans DaRT pour désactiver un pilote de périphérique défectueux, supprimer les correctifs, restaurer des fichiers supprimés et analyser l’ordinateur à la recherche de logiciels malveillants, même si vous ne pouvez pas démarrer le système d’exploitation Windows installé.

Le DaRT peut vous aider à récupérer rapidement des ordinateurs qui exécutent des versions 32 bits ou 64 bits de Windows 8, généralement plus longtemps que nécessaire pour réutiliser l’ordinateur.

Les fonctionnalités de DaRT vous permettent de créer une image de récupération. L’image de récupération démarre l’environnement de récupération Windows, à partir duquel vous pouvez démarrer la fenêtre du **jeu d’outils de diagnostics et de récupération** et accéder aux outils Dart.

Utilisez l' **Assistant image de récupération DART** pour créer l’image de récupération Dart. Par défaut, l’Assistant crée un fichier image ISO (International Organization for Standardization) et un fichier WIM (Windows Imaging Format) et vous permet de graver l’image sur un CD, un DVD ou un lecteur USB. Vous pouvez déployer l’image localement sur les ordinateurs des utilisateurs finaux ou vous pouvez la déployer à partir d’une partition réseau distante ou d’une partition de récupération sur le disque dur local.

## <a href="" id="what-s-new-in-dart-8-0"></a>Nouveautés de DaRT 8,0


Le DaRT 8,0 peut vous aider à récupérer rapidement des ordinateurs qui exécutent des versions 32 bits ou 64 bits de Windows 8, généralement plus longtemps que nécessaire pour réutiliser l’ordinateur. Le DaRT 8,0 offre les nouvelles fonctionnalités suivantes.

### Créer des images DaRT à l’aide de Windows 8 ou Windows Server 2012

Le DaRT 8,0 vous permet de créer des images DaRT en utilisant Windows® 8 ou Windows Server® 2012. Pour les versions de Windows antérieures à Windows 8 et Windows Server 2012, les clients doivent continuer à utiliser les versions antérieures de DaRT.

### Générer des images 32 et 64 bits à partir d’un ordinateur

Le DaRT 8,0 vous permet de générer des images 32 bits et 64 bits à partir d’un ordinateur exécutant DaRT, qu’il s’agisse d’un ordinateur 32 ou d’un ordinateur 64. Dans DaRT7, l’image qui a été créée devait être de la même manière que celle de l’ordinateur exécutant DaRT.

### Créer une image qui prend en charge les ordinateurs équipés d’une interface BIOS ou UEFI

La prise en charge de DaRT 8.0 pour les interfaces d’interface de microprogrammes unifiées (UEFI) et de BIOS vous permet de créer une seule image qui fonctionne avec des ordinateurs dotés d’une interface.

### Utiliser une table de partitions GUID (GPT) pour partitionner

Les outils 8,0 DaRT prennent désormais en charge les disques GPT Windows 8, qui fournissent un mécanisme plus flexible pour partitionner des disques que l’ancien modèle de partitionnement d’enregistrement de démarrage principal (MBR). Les outils 8,0 de DaRT continuent de prendre en charge une partition MBR.

### Installer Windows 8 et Windows Server 2012 sur le disque dur local

Les outils 8,0 DaRT peuvent être utilisés uniquement lorsque Windows 8 et Windows Server 2012 sont installés sur le disque dur local. Pour le moment, il n’y a pas de prise en charge pour Windows to go.

### <a href="" id="-------------dart-8-0-release-notes"></a> Notes de publication de DaRT 8,0

Pour plus d’informations et pour les actualités de dernière minute qui n’ont pas été intégrées à la documentation, voir les [notes de publication de DaRT 8,0](release-notes-for-dart-80--dart-8.md).

## Obtention de la 8,0 DaRT


Cette technologie fait partie du pack d’optimisation de bureau Microsoft (MDOP). MDOP fait partie de Microsoft Software Assurance. Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Rubriques connexes


[Prise en main de DaRT8.0](getting-started-with-dart-80-dart-8.md)

[Notes de publication pour DaRT8.0](release-notes-for-dart-80--dart-8.md)

 

 





