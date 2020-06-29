---
title: Procédure de création d'une image de récupération limitée dans le temps
description: Procédure de création d'une image de récupération limitée dans le temps
author: dansimp
ms.assetid: d2e29cac-c24c-4239-997f-0320b8a830ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a11891753f80d41f0089311771b906865950337c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804374"
---
# Procédure de création d'une image de récupération limitée dans le temps


Vous pouvez créer une image de récupération DaRT qui ne peut être utilisée que pendant un certain nombre de jours après sa génération. Pour cela, vous devez exécuter l' **Assistant image de récupération DART** à une invite de commandes et spécifier le nombre de jours.

**Pour créer une image de récupération ayant une limite de temps**

1.  Ouvrez une invite de commandes avec des informations d’identification d’administrateur.

2.  Remplacez le répertoire par l’emplacement du programme ERDC.exe.

3.  À l’aide de la syntaxe suivante, exécutez l' **Assistant image de récupération DART**. *NumberOfDays* est un entier positif qui représente le nombre de jours pendant lesquels l’image de récupération DART sera utilisable.

    ``` syntax
    ERDC /e NumberOfDays
    ```

## Rubriques connexes


[Création de l'image de récupération DaRT7.0](creating-the-dart-70-recovery-image-dart-7.md)

 

 





