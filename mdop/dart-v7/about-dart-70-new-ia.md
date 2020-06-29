---
title: À propos de DaRT7.0
description: À propos de DaRT7.0
author: dansimp
ms.assetid: 217ffafc-6d73-4b80-88d9-71870460d4ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cd647b2f596ce88ce38580f08422ff8f92b35c06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809857"
---
# À propos de DaRT7.0


Microsoft Diagnostics and Recovery Tools (DaRT) 7 vous aide à résoudre les problèmes liés aux ordinateurs de bureau Windows. Cela inclut les bureaux qui ne peuvent pas être démarrés. Le DaRT est un ensemble d’outils puissants qui développent l’environnement de récupération Windows (WinRE). À l’aide de DaRT, vous pouvez analyser un problème pour en déterminer la cause, par exemple, en inspectant le journal des événements ou le Registre du système de l’ordinateur.

Le DaRT fournit également des outils pour vous aider à résoudre un problème dès que vous déterminez la cause du problème. Par exemple, vous pouvez utiliser les outils dans DaRT pour désactiver un pilote de périphérique défectueux, supprimer les correctifs, restaurer des fichiers supprimés et analyser l’ordinateur à la recherche de logiciels malveillants, même si vous ne pouvez pas démarrer le système d’exploitation Windows installé.

Le DaRT peut vous aider à récupérer rapidement des ordinateurs qui exécutent des versions 32 bits ou 64 bits de Windows 7, généralement plus longtemps que nécessaire pour réutiliser l’ordinateur.

## À propos de l’image de récupération de DaRT 7


Les fonctionnalités de DaRT vous permettent de créer une image de récupération basée sur WinRE combinée à un ensemble d’outils fournis par DaRT. L’image de récupération DaRT tire parti de WinRE, à partir duquel vous pouvez accéder à la fenêtre des **outils de diagnostics et de récupération** .

Utilisez l' **Assistant image de récupération DART** pour créer l’image de récupération Dart. Par défaut, l’Assistant crée un fichier image ISO (International Organization for Standardization) sur votre ordinateur de bureau appelé DaRT70. ISO, même si vous pouvez spécifier un autre emplacement et un nom de fichier. L’Assistant vous permet également de graver l’image sur un CD ou un DVD. Une fois l’Assistant terminé, vous pouvez enregistrer l’image de récupération sur une clé USB ou l’enregistrer dans un format que vous pouvez utiliser pour créer une partition distante ou une partition de récupération.

Lorsque vous devez utiliser DaRT pour démarrer un ordinateur d’utilisateur final qui ne démarre pas, vous pouvez suivre les instructions de la [procédure de récupération d’ordinateurs locaux à l’aide de l’image de récupération DART](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).

Pour plus d’informations sur les outils dans DaRT, voir [vue d’ensemble des outils dans dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).

## <a href="" id="what-s-new-in-dart-7"></a>Nouveautés de DaRT 7


DaRT7 continue de prendre en charge tous les scénarios inclus dans les versions précédentes et il ajoute une nouvelle fonctionnalité de connexion à distance en plus de trois nouvelles options de déploiement.

### Création d’images DaRT 7

L’Assistant que vous utilisez pour créer des images ISO DaRT est désormais appelé **image de récupération DART** et prend désormais en charge une option d’activation ou de désactivation de la nouvelle fonctionnalité de connexion à distance. Connexion à distance permet à un agent du support technique d’exécuter les outils DaRT à partir d’un emplacement distant. Dans les versions précédentes, l’agent de support technique devait être présent physiquement sur l’ordinateur de l’utilisateur final pour exécuter les outils DaRT.

L’Assistant vous permet également de personnaliser le message d’accueil de la fonctionnalité de connexion à distance (le message s’affiche lorsque les utilisateurs finaux exécutent l’outil de connexion à distance). Les administrateurs informatiques peuvent également configurer le numéro de port à utiliser par la connexion à distance.

Pour plus d’informations sur l' **Assistant image de récupération DART** ou la connexion à distance, voir [création de l’Image de récupération 7,0 de DART](creating-the-dart-70-recovery-image-dart-7.md).

### Déploiement ISO de DaRT 7

Outre la gravure sur un CD ou un DVD, DaRT7 ajoute trois nouvelles options lorsque vous déployez l’ISO qui contient l’image de récupération DaRT:

-   Déploiement d’un lecteur flash USB

-   Déploiement de partitions distantes

-   Déploiement de partitions de récupération

L’option déploiement de la clé USB permet à une entreprise d’utiliser le DaRT sur des ordinateurs qui ne disposent pas de lecteurs de CD ou de DVD disponibles. Les options de récupération et de partition distante permettent aux utilisateurs finaux d’accéder facilement à l’image DaRT et d’activer la fonctionnalité de connexion à distance.

Pour plus d’informations sur le déploiement d’images de récupération DaRT, voir [déploiement de l’image de récupération 7,0 de DART](deploying-the-dart-70-recovery-image-dart-7.md).

## Rubriques connexes


[Prise en main de DaRT7.0](getting-started-with-dart-70-new-ia.md)

[Notes de publication pour DaRT7.0](release-notes-for-dart-70-new-ia.md)

 

 





