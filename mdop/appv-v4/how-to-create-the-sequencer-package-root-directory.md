---
title: Procédure pour créer le répertoire racine de package de Sequencer
description: Procédure pour créer le répertoire racine de package de Sequencer
author: dansimp
ms.assetid: 23fe28f1-c284-43ee-b8b7-1dfbed94eea5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5150e87915202794624b6c51510e56454d2c7d36
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807178"
---
# Procédure pour créer le répertoire racine de package de Sequencer


Le répertoire racine du package est le répertoire de l’ordinateur exécutant le Sequencer App-V dans lequel les fichiers de l’application séquencée sont installés. Ce répertoire existe également virtuellement sur l’ordinateur sur lequel une application séquencée sera diffusée. Vous devez créer le répertoire racine du package avant de surveiller l’installation d’une nouvelle application.

Une fois que vous avez créé le répertoire racine du package, vous pouvez commencer à Sequencer les applications. Pour plus d’informations sur le séquençage d’une nouvelle application, voir [Comment séquencer une application](how-to-sequence-an-application.md).

**Pour créer le répertoire racine du package**

1.  Pour créer le répertoire racine du package, sur l’ordinateur exécutant le Sequencer App-V, mappez le lecteur Q:\\ à l’emplacement réseau spécifié. L’emplacement que vous spécifiez doit disposer d’un espace suffisant pour enregistrer l’application que vous séquençage.

2.  Pour créer un répertoire que vous pouvez utiliser pour une nouvelle application virtuelle, créez un dossier sur le lecteur Q:\\ et attribuez-lui un nom.

    **Important**  Le nom que vous attribuez aux fichiers d’application virtuels qui seront enregistrés dans le répertoire racine du package doit utiliser le format de noms 8,3. Les noms de fichiers ne doivent pas comporter plus de 8 caractères avec une extension de nom de fichier à trois caractères.

     

## Rubriques connexes


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

[Procédure pour modifier l'emplacement du répertoire des journaux](how-to-modify-the-log-directory-location.md)

[Procédure pour modifier l'emplacement du répertoire Scratch](how-to-modify-the-scratch-directory-location.md)

 

 





