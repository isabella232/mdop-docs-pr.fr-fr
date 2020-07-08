---
title: Procédure pour exécuter l'Analyseur d'incident en mode autonome sur un ordinateur autre qu'un ordinateur d'utilisateur final
description: Procédure pour exécuter l'Analyseur d'incident en mode autonome sur un ordinateur autre qu'un ordinateur d'utilisateur final
author: dansimp
ms.assetid: 881d573f-2f18-4c5f-838e-2f5320179f94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6f398c56b7c631145388541b71229d69c16bf6f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809564"
---
# Procédure pour exécuter l'Analyseur d'incident en mode autonome sur un ordinateur autre qu'un ordinateur d'utilisateur final


Si vous ne parvenez pas à accéder aux outils de débogage de Microsoft pour Windows ou aux fichiers de symboles de l’ordinateur de l’utilisateur final, vous pouvez copier le fichier de vidage à partir de l’ordinateur qui rencontre un problème et l’analyser sur un ordinateur sur lequel est installée la version autonome d’crash Analyzer, telle que l’ordinateur d’un administrateur du support technique.

**Pour exécuter l’analyseur d’incident en mode indépendant**

1.  Sur un ordinateur sur lequel DaRT7 est installé, cliquez sur **Démarrer**  /  **tous les programmes**  /  **Microsoft DART 7**.

2.  Fournissez les informations requises pour les éléments suivants:

    -   Outils de débogage de Microsoft pour Windows

    -   Fichiers de symboles

        Pour plus d’informations sur les fichiers de symboles, voir [Comment s’assurer que l’analyseur d’incidents peut accéder aux fichiers de symboles](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).

    -   Fichier de vidage sur incident

        **Remarques**  Utilisez l’outil de recherche dans DaRT7 pour rechercher le fichier de vidage sur incident copié.

         

3.  L' **Analyseur de blocage** analyse le fichier de vidage sur incident et signale la cause probable du blocage. Vous pouvez afficher des informations supplémentaires sur le blocage, comme le message d’incident et la description spécifiques, les pilotes chargés au moment du blocage et la sortie complète de l’analyse.

4.  Décidez d’une stratégie appropriée pour résoudre le problème. Cela risque de désactiver ou de mettre à jour le pilote de périphérique à l’origine du blocage à l’aide du nœud **services et pilotes** de l’outil de gestion de l' **ordinateur** dans DART.

## Rubriques connexes


[Diagnostic d'échecs du système avec l'Analyseur d'incident](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





