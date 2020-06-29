---
title: À propos de l'onglet Propriétés
description: À propos de l'onglet Propriétés
author: dansimp
ms.assetid: a6cf6f51-3778-4c8d-9632-3af4005775d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b2d6c3e01dde48fdd6701984f66610ea0333b74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808101"
---
# À propos de l'onglet Propriétés


Utilisez l’onglet **Propriétés** pour afficher des informations statistiques de base sur un package d’application séquencé. Les informations sont générées automatiquement sauf indication contraire. Cet onglet contient les éléments suivants.

## Informations de package


<a href="" id="package-name"></a>**Nom du package**  
Le nom unique utilisé pour un package d’application séquencé qui peut contenir une ou plusieurs applications (par exemple, Microsoft Office) peut être utilisé pour étiqueter un package d’application séquencé contenant des applications Microsoft Word et Microsoft Excel qui s’exécutent dans le même environnement virtuel.

<a href="" id="comments"></a>**Commentaires**  
Affiche une brève description du package logiciel qui s’affichera dans l’élément abstrait d’ouverture de fichier d’OSD. Cet élément est facultatif.

<a href="" id="package-version"></a>**Version du package**  
Version du package d’application séquencé.

<a href="" id="package-guid"></a>**GUID du package**  
Identificateur unique global (GUID) attribué automatiquement au package d’application séquencé pour le différencier des autres packages d’application séquencés qui peuvent s’exécuter sur l’ordinateur sur lequel un package d’application séquencé est en flux continu.

<a href="" id="package-version-guid"></a>**GUID de version de package**  
GUID de la version du package d’application séquencé.

<a href="" id="root-directory"></a>**Répertoire racine**  
Répertoire de l’ordinateur de séquençage dans lequel les fichiers du package d’application séquencé sont installés. Ce répertoire est également créé sur l’ordinateur sur lequel un package d’application séquencé est en flux continu. Il est recommandé de la compatibilité descendante qu’il s’agit d’un nom de répertoire de format 8,3 à la racine du lecteur Q, par exemple Q:\\MyApp.1\\.

<a href="" id="created"></a>**Générée**  
Date et heure de création du package d’application séquencé.

<a href="" id="modified"></a>**Modifié**  
Date et heure auxquelles le package d’application séquencé a été modifié pour la dernière fois.

<a href="" id="package-size"></a>**Taille du package**  
Taille du package en mégaoctets.

<a href="" id="launch-size"></a>**Taille du lancement**  
Taille en mégaoctets de la partie du fichier SFT requis pour démarrer l’application.

## Paramètres de séquençage


<a href="" id="block-size"></a>**Taille du bloc**  
Spécifie la taille des blocs de fonctionnalité principaux et secondaires dans lesquels le fichier SFT est divisé pour la diffusion en continu sur un réseau. Tous les blocs égaux à la taille spécifiée; Toutefois, le dernier bloc peut avoir une taille inférieure à celle spécifiée. Vous verrez l’une des valeurs suivantes:

-   4 KO

-   16 KO

-   32 KO

-   64 KO

**Remarques**  Après la création du package initial, la valeur taille du bloc n’est pas modifiable.

 

## Rubriques connexes


[Procédure pour modifier les propriétés du package](how-to-change-package-properties.md)

[Console Sequencer](sequencer-console.md)

 

 





