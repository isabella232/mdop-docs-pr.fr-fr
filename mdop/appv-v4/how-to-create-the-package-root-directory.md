---
title: Procédure pour créer le répertoire racine de package
description: Procédure pour créer le répertoire racine de package
author: dansimp
ms.assetid: bcfe3bd4-6c60-409a-8ffa-cc22f27194b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c9e1e7be71627d4e55eff7a4e2582a21b834876d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807182"
---
# Procédure pour créer le répertoire racine de package


Le répertoire racine du package est le répertoire de l’ordinateur exécutant le Sequencer App-V dans lequel les fichiers de l’application séquencée sont installés. Ce répertoire existe également virtuellement sur l’ordinateur sur lequel une application séquencée sera diffusée. Vous devez créer le répertoire racine du package avant de surveiller l’installation d’une nouvelle application.

Une fois que vous avez créé le répertoire racine du package, vous pouvez commencer à Sequencer les applications. Pour plus d’informations sur le séquençage d’une nouvelle application, voir [Comment installer le Sequencer](how-to-install-the-sequencer.md).

**Pour créer le répertoire racine du package**

1.  Pour créer le répertoire racine du package, sur l’ordinateur exécutant le Sequencer App-V, mappez le lecteur Q:\\ à l’emplacement réseau spécifié. L’emplacement que vous spécifiez doit disposer d’un espace suffisant pour enregistrer l’application que vous séquençage.

2.  Pour créer un répertoire que vous pouvez utiliser pour une nouvelle application virtuelle, créez un dossier sur le lecteur Q:\\ et attribuez-lui un nom.

    **Important**  Le nom que vous attribuez aux fichiers d’application virtuels qui seront enregistrés dans le répertoire racine du package doit utiliser le format de noms 8,3. Les noms de fichiers ne doivent pas comporter plus de 8 caractères avec une extension de nom de fichier à trois caractères.

     

## Rubriques connexes


[Tâches pour Application Virtualization Sequencer](tasks-for-the-application-virtualization-sequencer.md)

 

 





