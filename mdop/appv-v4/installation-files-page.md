---
title: Page Fichiers d'installation
description: Page Fichiers d'installation
author: dansimp
ms.assetid: b0aad26f-b143-4f09-87a1-9f016a23cb62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 08a2e7318271503f072298ca137a1e65e16c0178
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806669"
---
# Page Fichiers d'installation


Utilisez la page **fichiers d’installation** pour spécifier les fichiers d’installation utilisés pour créer le package d’application virtuel spécifié dans la page Sélectionner un **package** de cet Assistant. Si vous avez créé un package d’application virtuel contenant plusieurs applications, vous devez copier tous les fichiers d’installation requis vers un dossier sur l’ordinateur exécutant le Sequencer Microsoft Application Virtualization.

Cette page contient les éléments suivants:

<a href="" id="original-installation-files"></a>**Fichiers d’installation d’origine**  
Cliquez sur **Parcourir** pour spécifier les fichiers d’installation utilisés à l’origine pour créer le package d’application virtuel. Le répertoire parent que vous spécifiez doit être enregistré localement sur l’ordinateur exécutant le Sequencer et doit contenir tous les fichiers d’installation requis ou les sous-dossiers contenant les fichiers d’installation. Les fichiers d’installation peuvent être contenus dans le dossier parent ou dans un sous-dossier du dossier parent spécifié.

<a href="" id="files-installed-on-local-system"></a>**Fichiers installés sur le système local**  
Cliquez sur **Parcourir** pour spécifier les fichiers d’installation installés localement sur l’ordinateur exécutant le Sequencer. Vous ne pouvez sélectionner cette option que si les fichiers d’installation de l’application ont été installés à l’emplacement par défaut de l’application.

**Remarques**  L’emplacement d’installation par défaut que vous fournissez dépend des conditions suivantes:

 

-   Racine du package spécifié lors de la création du package.

-   Emplacement d’installation spécifié dans le programme d’installation Windows lors de la création du package.

-   Le chemin d’installation de l’application par défaut.

Par exemple, si la racine du package spécifiée est **Q:\\Office12** et au cours de l’installation, l’emplacement d’installation par défaut est passé de **C:\\Program Files\\Office12** à **Q:\\Office12**, puis le chemin d’accès spécifié lors de la mise en attente doit être **C:\\Program Files\\Office 12**.

Si la racine du package spécifiée est **Q:\\Microsoft** et au cours de l’installation, l’emplacement d’installation par défaut est changé de **C:\\Program Files\\Office12** en **Q:\\Microsoft\\Office12**, puis le chemin d’accès spécifié lors de la mise en attente doit être **C:\\Program Files**.

Lorsque vous créez un package à l’aide d’un accélérateur de package, chaque fichier dans le package, par exemple **Q:\\Office12\\file.txt** est disponible sur l’ordinateur local en remplaçant le **Q:\\Office12** racine du package par l’emplacement par défaut spécifié lors de la création de l’accélérateur de package (par exemple, **C:\\Program Files\\Office12**). Dans l’exemple précédent, le fichier doit se trouver dans **C:\\Program Files\\Office12\\file.txt**.

## Rubriques connexes


[Assistant Créer un accélérateur de package (AppV4.6SP1)](create-package-accelerator-wizard--appv-46-sp1-.md)

 

 





