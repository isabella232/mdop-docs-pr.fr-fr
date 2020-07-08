---
title: Procédure pour modifier un fichier OSD à l'aide d'un éditeur de texte
description: Procédure pour modifier un fichier OSD à l'aide d'un éditeur de texte
author: dansimp
ms.assetid: f4263a1b-824f-49b9-8060-b8229c9d9960
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c83547b38cee7e91e8348689583e0542a88dab83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807109"
---
# Procédure pour modifier un fichier OSD à l'aide d'un éditeur de texte


Utilisez la procédure suivante pour modifier un fichier d’OSD (Open Software Descriptor) à l’aide d’un éditeur de texte.

**Pour modifier un fichier OSD à l’aide d’un éditeur de texte**

1.  Ouvrez le fichier OSD à l’aide d’un éditeur de texte XML ou ASCII, par exemple le bloc-notes Microsoft.

    **Remarques**  Avant de modifier le fichier OSD, lisez le schéma prescrit par le fichier XSD figurant dans le répertoire d’installation. Il est possible que l’échec de la suivi de ce schéma génère des erreurs qui empêchent le démarrage correct d’une application séquencée.

     

2.  Modifiez le fichier OSD en utilisant votre éditeur de texte XML ou ASCII de votre choix, en adhérant au schéma prescrit et aux instructions suivantes:

    1.  Assurez-vous que les éléments nommés sont imbriqués dans l' &lt; &gt; élément racine SOFTPKG.

    2.  Vérifiez que les noms d’éléments sont en majuscules.

    3.  Sachez que les valeurs d’attribut respectent la casse.

    4.  Tapez soigneusement et observez les spécifications XML.

## Rubriques connexes


[À propos de l'onglet OSD](about-the-osd-tab.md)

[Procédure pour modifier un fichier OSD](how-to-edit-an-osd-file.md)

[Éléments du fichier OSD](osd-file-elements.md)

 

 





