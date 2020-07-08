---
title: Paramètres de ligne de commande de Sequencer
description: Paramètres de ligne de commande de Sequencer
author: dansimp
ms.assetid: 28fb875a-c302-4d95-b2e0-8dc0c5dbb0f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ecfa269de04cf3dcba30cbb4a40f9176f03f6571
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806353"
---
# Paramètres de ligne de commande de Sequencer


Vous pouvez utiliser les paramètres de Sequencer d’application Virtualization suivants (App-V) pour séquencer une application et mettre à niveau une application virtuelle existante à l’aide d’une ligne de commande. Pour plus d’informations sur le séquençage d’une application à l’aide d’une ligne de commande, voir [Comment séquencer une nouvelle application à l’aide de la ligne de commande](how-to-sequence-a-new-application-by-using-the-command-line.md).

## Paramètres de ligne de commande de Sequencer


<a href="" id="-help-or---"></a>**/HELP ou/?**  
Affiche des informations sur les paramètres disponibles pour l’utilisation de la ligne de commande pour la séquence des applications.

<a href="" id="-installpackage-or--i"></a>**/INSTALLPACKAGE ou/I**  
Spécifie le programme d’installation Windows ou un fichier de commandes qui sera utilisé pour installer une application de manière à ce qu’elle puisse être séquencée.

<a href="" id="-installpath-or--p"></a>**/INSTALLPATH ou/P**  
Spécifie le répertoire racine du package pour une application.

<a href="" id="-outputfile-or--o"></a>**/OUTPUTFILE ou/O**  
Spécifie le chemin d’accès et le nom de fichier du fichier SPRJ qui sera généré.

<a href="" id="-fullload-or--f"></a>**/FULLLOAD ou/F**  
Spécifie si tous les fichiers doivent figurer dans le bloc de fonctionnalités principal. Si le paramètre **/FULLLOAD** est spécifié sur la ligne de commande, toutes les données d’application associées sont ajoutées au bloc de fonctionnalités principal. Si le paramètre **/FULLLOAD** n’est pas spécifié sur la ligne de commande, aucune des données d’application associées n’est ajoutée au bloc de fonctionnalités principal.

<a href="" id="-packagename-or--k"></a>**/PACKAGENAME ou/K**  
Spécifie le nom du package qui sera affecté à l’application séquencée.

<a href="" id="-blocksize"></a>**/BLOCKSIZE**  
Spécifie la taille de bloc de fichiers SFT qui sera utilisée pour diffuser le package sur les ordinateurs clients. Vous pouvez sélectionner l’une des valeurs suivantes:

-   4 KO

-   16 KO

-   32 KO

-   64 KO

Vous devez prendre en considération la taille du fichier SFT lorsque vous spécifiez la taille du bloc. Le flux d’un fichier dont la taille de blocs est plus petite prend plus de temps sur le réseau, mais nécessite moins de bande passante. Les fichiers de tailles de blocs plus grandes utilisent davantage de bande passante réseau.

<a href="" id="-compression"></a>**/COMPRESSION**  
Spécifie la méthode permettant de compresser le fichier SFT qui sera transmis au client.

<a href="" id="-msi-or--m"></a>**/MSI ou/M**  
Indique si un programme d’installation Windows pour l’application séquencée doit être créé.

<a href="" id="-default"></a>**/DEFAULT**  
Spécifie le fichier SPRJ par défaut qui sera utilisé lors de la création d’un package d’application virtuel. Ce fichier est utilisé comme modèle. sprj lorsque l’application est séquencée pour la première fois.

<a href="" id="-upgrade"></a>**/UPGRADE**  
Spécifie le chemin d’accès et le nom de fichier du fichier SPRJ qui sera mis à niveau.

<a href="" id="-decodepath"></a>**/DECODEPATH**  
Spécifie le répertoire sur l’ordinateur de séquençage dans lequel les fichiers associés au package d’application séquencé sont installés. Lorsque vous spécifiez le répertoire, utilisez l’un des formats suivants:

-   /DECODEPATH: Q:

-   /decodepath:Q:.

-   /decodepath:"Q:."

-   /DECODEPATH: "Q:"

## Rubriques connexes


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

[Codes des erreurs de ligne de commande de Sequencer](sequencer-command-line-error-codes.md)

 

 





