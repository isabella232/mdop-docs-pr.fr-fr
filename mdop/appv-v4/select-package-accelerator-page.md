---
title: Page Sélectionner un accélérateur de package
description: Page Sélectionner un accélérateur de package
author: dansimp
ms.assetid: 865c2702-4dfd-41ae-8cfc-3514d5f41f76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5723f8244563539c27a3fa915c1a680905e61e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806369"
---
# Page Sélectionner un accélérateur de package


Servez-vous de la page **Sélectionner l’accélérateur de package** pour sélectionner l’accélérateur de package à utiliser pour créer le package d’application virtuelle. Vous devez copier l’accélérateur de package vers un dossier sur l’ordinateur exécutant le Sequencer App-V. Pour plus d’informations, voir [à propos des accélérateurs de package App-v (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).

Exécutez uniquement les accélérateurs de package d’éditeurs approuvés. Les accélérateurs de package incluent généralement une signature numérique. Une signature numérique est une marque de sécurité électronique qui peut vous aider à indiquer l’éditeur du logiciel et si le package a été falsifié après la signature initiale de la transformation. Si vous utilisez une transformation qui a été signée numériquement par un éditeur et que l’éditeur a vérifié son identité auprès d’une autorité de certification, vous pouvez être sûr que la transformation provient d’un éditeur spécifique et qu’elle n’a pas été altérée.

Le Sequencer App-V vous avertit si l’une des conditions suivantes est vraie:

-   La transformation sélectionnée n’a pas été signée numériquement.

-   La transformation sélectionnée est signée par un éditeur qui n’a pas vérifié son identité auprès d’une autorité de certification.

-   La transformation sélectionnée a été modifiée après sa signature numérique et sa sortie.

Si l’un de ces messages s’affiche lors de l’utilisation d’un accélérateur de package, rendez-vous sur le site Web de l’éditeur accélérateurs de packages pour obtenir une version signée numériquement de la transformation.

Cette page contient les éléments suivants:

<a href="" id="browse"></a>**Parcourir**  
Cliquez sur **Parcourir** pour spécifier l’accélérateur de package à utiliser pour créer le package d’application virtuelle. Enregistrez l’accélérateur de package que vous avez spécifié localement sur l’ordinateur exécutant le Sequencer.

## Rubriques connexes


[Assistant Sequencer - Accélérateur de package (AppV4.6SP1)](sequencer-wizard---package-accelerator--appv-46-sp1-.md)

 

 





