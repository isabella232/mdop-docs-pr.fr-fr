---
title: Paramètres de ligne de commande
description: Paramètres de ligne de commande
author: dansimp
ms.assetid: d90a0591-f1ce-4cb8-b244-85cc70461922
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31d6ca1215648e2519e9818817ab5cc779a746d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807893"
---
# Paramètres de ligne de commande


Pour séquencer une application et mettre à niveau un package d’application séquencé à l’invite de commandes, utilisez les paramètres de séquenceur d’applications suivants. Dans le répertoire Microsoft Application Virtualization Sequencer, entrez **SFTSequencer**, suivi du paramètre approprié.

<a href="" id="-help-or---"></a>*/Help* ou */?*  
Permet d’afficher la liste des paramètres disponibles pour le séquençage de lignes de commande.

<a href="" id="-installpackage-or--i"></a>*/INSTALLPACKAGE* ou */i*  
Permet de spécifier le programme d’installation ou un fichier de commandes que l’application doit être séquencée.

<a href="" id="-installpath-or--p"></a>*/InstallPath* ou */p*  
Utiliser pour spécifier le répertoire racine du package.

<a href="" id="-outputfile-or--o"></a>*/Outputfile* ou */o*  
Utiliser pour spécifier le chemin d’accès et le nom de fichier du fichier SPRJ qui sera généré.

**Important**  Le paramètre */outputfile* n’est pas disponible lors de l’ouverture d’un package que vous ne souhaitez pas mettre à niveau.

 

<a href="" id="-fullload-or--f"></a>*/FULLLOAD* ou */f*  
Permet de spécifier si les éléments doivent être placés dans le bloc de fonctionnalités principal.

<a href="" id="-packagename-or--k"></a>*/PackageName* ou */k*  
Utiliser pour spécifier le nom du package de l’application séquencée.

<a href="" id="-blocksize"></a>*/BLOCKSIZE*  
Spécifie la taille de bloc de fichiers SFT qui sera utilisée pour diffuser le package sur les ordinateurs clients. Vous pouvez sélectionner l’une des valeurs suivantes:

-   4 KO

-   16 KO

-   32 KO

-   64 KO

Vous devez prendre en considération la taille du fichier SFT lorsque vous spécifiez la taille du bloc. Le flux d’un fichier dont la taille de blocs est plus petite prend plus de temps sur le réseau, mais nécessite moins de bande passante. Les fichiers de tailles de blocs plus grandes utilisent davantage de bande passante réseau.

<a href="" id="-compression"></a>*/COMPRESSION*  
Utiliser pour spécifier la méthode permettant de compresser le fichier SFT lors de son flux vers le client.

<a href="" id="-msi-or--m"></a>*/MSI* ou */m*  
Permet de spécifier la génération d’un package Microsoft Windows Installer pour l’application séquencée.

<a href="" id="-default"></a>*/DEFAULT*  
Spécifie le fichier SPRJ par défaut qui sera utilisé lors de la création d’un package d’application virtuel. Ce fichier est utilisé comme modèle. sprj lorsque l’application est séquencée pour la première fois.

<a href="" id="-upgrade"></a>*/UPGRADE*  
Spécifie le chemin d’accès et le nom de fichier du fichier SPRJ qui sera mis à niveau.

<a href="" id="-decodepath"></a>*/DECODEPATH*  
Spécifie le répertoire sur l’ordinateur de séquençage dans lequel les fichiers associés au package d’application séquencé sont installés. Lorsque vous spécifiez le répertoire, utilisez l’un des formats suivants:

-   /DECODEPATH: Q:

-   /decodepath:Q:.

-   /decodepath:"Q:."

-   /DECODEPATH: "Q:"

## Rubriques connexes


[À propos de l'utilisation de la ligne de commande de Sequencer](about-using-the-sequencer-command-line.md)

[Procédure pour ouvrir une application séquencée à l'aide de la ligne de commande](how-to-open-a-sequenced-application-using-the-command-line.md)

[Procédure pour mettre à niveau un package à l'aide de la commande Ouvrir un package](how-to-upgrade-a-package-using-the-open-package-command.md)

 

 





