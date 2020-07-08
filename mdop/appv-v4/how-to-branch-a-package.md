---
title: Procédure pour ramifier un package
description: Procédure pour ramifier un package
author: dansimp
ms.assetid: bfe46a8a-f0ee-4a71-9e9c-64ac08aac9c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2de36fae1a09aeae4d1b7b21ebe00f683e3b3693
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807382"
---
# Procédure pour ramifier un package


Utilisez cette procédure pour modifier un package d’application séquencé existant de sorte que vous puissiez l’exécuter côte à côte avec le package d’application séquencé d’origine. Ce processus porte le nom de branchement. Lorsque vous agencez un package d’application virtuelle, vous pouvez exécuter deux versions du même package. Par exemple, vous pouvez appliquer un service pack à un package existant et l’exécuter côte à côte avec le package d’application virtuelle séquencé d’origine.

Utilisez la procédure suivante pour brancher un package d’application virtuelle séquencé.

**Pour brancher un package d’application virtuelle séquencé**

1.  Ouvrez le Sequencer Microsoft Application Virtualization (App-V). Pour spécifier le répertoire de destination qui contient le package (. sprj) sur lequel vous voulez sélectionner un **fichier**, **ouvrez**l’arborescence.

2.  Accédez au dossier qui contient l’application séquencée que vous envisagez de brancher et cliquez sur **ouvrir**.

3.  Pour enregistrer une copie du package, dans le Sequencer App-V, sélectionnez **fichier**, **Enregistrer sous**. Spécifiez un nouveau nom unique et spécifiez un nouveau répertoire racine de package unique pour la copie du package. Cliquez sur **Save**.

    **Important**  
    Vous devez spécifier un nouveau nom de package ou vous remplacerez la version existante du package.



~~~
The sequencer will automatically generate new GUID files for the new package. The version number associated with the package will also be automatically appended to the OSD file name.
~~~

4. Après avoir enregistré la nouvelle version, vous pouvez appliquer les modifications de configuration requises et enregistrer les fichiers. ICO, OSD, SFT et SPRJ pour corriger l’emplacement sur le serveur Application Virtualization (App-V).

## Rubriques connexes


[Tâches pour Application Virtualization Sequencer](tasks-for-the-application-virtualization-sequencer.md)









