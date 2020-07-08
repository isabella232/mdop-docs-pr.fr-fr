---
title: Création de l'image de récupération DaRT7.0
description: Création de l'image de récupération DaRT7.0
author: dansimp
ms.assetid: ebb2ec58-0349-469d-a23f-3f944fe4c1fa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f19ff144cac61ca7ea5a8498f67caf8a99229d77
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809863"
---
# Création de l'image de récupération DaRT7.0


Microsoft Diagnostics and Recovery Tools (DaRT) 7 inclut l' **Assistant image de récupération DART** utilisé dans Windows pour créer une image ISO (International Organization for Standardization) amorçable. Une image ISO est un fichier qui représente le contenu brut d’un CD.

## Utiliser l’Assistant image de récupération DaRT pour créer l’image de récupération


La feuille de style ISO créée par l’Assistant image de récupération DaRT contient l’image de récupération DaRT qui vous permet d’effectuer un démarrage sur un ordinateur défectueux, même si cela n’est pas le cas. Après avoir amorcé l’ordinateur dans DaRT, vous pouvez exécuter les différents outils DaRT pour essayer de diagnostiquer et de réparer l’ordinateur.

Vous pouvez enregistrer le fichier ISO sur un CD ou un DVD enregistrable, l’enregistrer sur un disque mémoire flash ou l’enregistrer dans un format que vous pouvez utiliser pour démarrer dans DaRT à partir d’une partition distante ou d’une partition de récupération. Pour plus d’informations, reportez-vous à [déploiement de l’image de récupération 7,0 de DART](deploying-the-dart-70-recovery-image-dart-7.md).

**Remarques**  Si votre ordinateur inclut un lecteur CD-RW, l’Assistant propose de graver l’image ISO sur un CD ou un DVD vierge. Si votre ordinateur n’inclut pas de lecteur pris en charge par l’Assistant, vous pouvez graver l’image ISO sur un CD ou un DVD à l’aide de la plupart des programmes qui peuvent graver un CD ou un DVD.

 

Pour créer un CD ou un DVD amorçable à partir de l’image ISO, vous devez disposer des éléments suivants:

-   Un lecteur CD-RW.

-   Un CD ou un DVD enregistrable (dans un format pris en charge par le graveur).

-   Logiciel prenant en charge le disque enregistrable et prenant en charge la gravure d’une image ISO directement sur un CD ou un DVD.

    **Important**  Testez le CD ou DVD que vous créez sur les différents types d’ordinateurs que vous envisagez de prendre en charge, car certains ordinateurs ne peuvent pas démarrer à partir de tous les types de média enregistrables.

     

Pour enregistrer l’image ISO sur un disque mémoire USB (UFD), vous devez disposer des éléments suivants:

-   UFD.

-   Programme que vous pouvez utiliser pour monter l’image ISO.

[Procédure d'utilisation de l'Assistant Image de récupération DaRT pour créer l'image de récupération](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md)

## Créer une image de récupération de type Time Limit


Vous pouvez créer une image de récupération DaRT qui ne peut être utilisée que pendant un certain nombre de jours après sa génération. Pour cela, vous devez exécuter l' **Assistant image de récupération DART** à une invite de commandes et spécifier le nombre de jours.

[Procédure de création d'une image de récupération limitée dans le temps](how-to-create-a-time-limited-recovery-image-dart-7.md)

## Autres ressources pour créer l’image de récupération DaRT7


-   [Déploiement de DaRT7.0](deploying-dart-70-new-ia.md)

 

 





