---
title: Composants supplémentaires d'un package d'application virtuelle
description: Composants supplémentaires d'un package d'application virtuelle
author: dansimp
ms.assetid: 476b0f40-ebd6-4296-92fa-61fa9495c03c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d30c2c6561b0d2c08fd75e0c977bf4590d7e6688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806162"
---
# Composants supplémentaires d'un package d'application virtuelle


Le Sequencer App-V a détecté un répertoire qui contient les exécutables 64 bits et 32 bits et/ou les fichiers de bibliothèque de liens dynamiques (. dll) qui varient en fonction du même assemblage côte à côte. En règle générale, le Sequencer crée des assemblys côte à côte privés pour tous les assemblys publics utilisés par le package. Néanmoins, il n’est pas possible de créer des versions 32 bits et 64 bits des assemblys privés dans le même annuaire.

Si le Sequencer détecte un conflit unique, il effectue les actions suivantes:

-   Supprimez tous les assemblys privés 64 bits existants dans l’intégralité du package, qu’il s’agisse d’un conflit ou non.

-   Créer uniquement des versions 32 bits des assemblys côte à côte privés.

Vous devez installer en natif les versions publiques de tous les assemblys 64 bits requis sur l’ordinateur exécutant le Sequencer et sur tous les ordinateurs clients App-V.

Pour localiser les assemblys publics existants requis, ouvrez le répertoire où le package est enregistré et recherchez-le dans le dossier **VFS** . Par exemple, si la racine du package est **Q:\\MyApp**, lors de l’ordre de l’application, recherchez dans **Q:\\MyApp\\VFS\\CSIDL\ _Windows \\winsxs\\manifests** et repérez tous les assemblys publics existants. Les versions 64 bits de ces fichiers commencent toujours par le texte suivant au début du nom du manifeste: **amd64...**. Le nom exact et la version de l’assembly se trouvent dans le fichier manifeste associé.

Pour télécharger et installer la version correcte des éléments requis, utilisez l’un des liens suivants:

-   [Package redistribuable 2005 Microsoft Visual C++ (x64)](https://go.microsoft.com/fwlink/?LinkId=152697)

-   [Package redistribuable Microsoft Visual C++ 2005 SP1 (x64)](https://go.microsoft.com/fwlink/?LinkId=152698)

-   [Package redistribuable 2008 Microsoft Visual C++ (x64)](https://go.microsoft.com/fwlink/?LinkId=152699)

-   [Package redistribuable Microsoft Visual C++ 2008 SP1 (x64)](https://go.microsoft.com/fwlink/?LinkId=152700)

 

 





