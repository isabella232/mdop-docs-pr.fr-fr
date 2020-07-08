---
title: Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final
description: Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final
author: dansimp
ms.assetid: 40af4ead-6588-4a81-8eaa-3dc00c397e1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 943e3956609ae7e24deaca4313036445802a8f7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810194"
---
# Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final


En règle générale, vous exécutez l’analyseur de diagnostics et de récupération d’outils de diagnostics (DaRT) 7 crash Analyzer depuis la fenêtre du jeu d’outils de diagnostics et de récupération sur un ordinateur d’utilisateur final qui rencontre des problèmes. L’analyseur de blocage tente de rechercher les outils de débogage pour Windows sur l’ordinateur qui rencontre le problème. Si la boîte de dialogue chemin d’accès au répertoire est vide, vous devez entrer l’emplacement des outils de débogage pour Windows (vous pouvez télécharger les fichiers à partir de Microsoft). Vous devez également indiquer un chemin d’accès à l’endroit où se trouvent les fichiers de symboles.

**Pour ouvrir et exécuter l’analyseur d’incidents sur un ordinateur d’utilisateur final**

1.  Dans la fenêtre **jeu d’outils de diagnostics et de récupération** sur un ordinateur d’utilisateur final, cliquez sur **crash Analyzer**.

2.  Fournissez les informations requises pour les éléments suivants:

    -   Outils de débogage de Microsoft pour Windows

    -   Fichiers de symboles

        Pour plus d’informations sur les fichiers de symboles, voir [Comment s’assurer que l’analyseur d’incidents peut accéder aux fichiers de symboles](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).

    -   Fichier de vidage sur incident

        Pour déterminer l’emplacement du fichier de vidage sur incident, procédez comme suit:

        1.  Ouvrez la fenêtre de **Propriétés système** .

            Cliquez sur **Démarrer**, tapez sysdm.cpl, puis appuyez sur entrée.

        2.  Cliquez sur l’onglet **Avancé**.

        3.  Dans la zone **démarrage et récupération** , cliquez sur **paramètres**.

        **Remarques**  Si vous n’avez pas accès à la fenêtre de **Propriétés système** , vous pouvez rechercher des fichiers de vidage sur l’ordinateur de l’utilisateur final à l’aide de l’outil de **recherche** dans DART.

         

3.  L' **Analyseur de blocage** analyse le fichier de vidage sur incident et signale la cause probable du blocage. Vous pouvez afficher des informations supplémentaires sur le blocage, comme le message d’incident et la description spécifiques, les pilotes chargés au moment du blocage et la sortie complète de l’analyse.

4.  Décidez d’une stratégie appropriée pour résoudre le problème. Cela risque de désactiver ou de mettre à jour le pilote de périphérique à l’origine du blocage à l’aide du nœud **services et pilotes** de l’outil de gestion de l' **ordinateur** dans DART.

## Rubriques connexes


[Diagnostic d'échecs du système avec l'Analyseur d'incident](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





