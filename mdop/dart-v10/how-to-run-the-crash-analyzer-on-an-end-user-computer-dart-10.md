---
title: Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final
description: Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final
author: dansimp
ms.assetid: 10334800-ff8e-43ac-a9c2-d28807473ec2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4abf1ba2ae1a0cb1dfb129c1f5a26e11f5045290
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809492"
---
# Procédure pour exécuter l'Analyseur d'incident sur l'ordinateur d'un utilisateur final


Pour exécuter l' **analyseur d’incidents** à partir de la fenêtre du **jeu d’outils de diagnostics et de récupération** sur un ordinateur d’utilisateur final rencontrant des problèmes, vous devez disposer des outils de débogage Microsoft pour Windows et des fichiers de symboles installés. Pour télécharger les outils de débogage Windows, voir [outils de débogage pour Windows](https://go.microsoft.com/fwlink/?LinkId=266248).

**Pour exécuter l’analyseur d’incidents sur un ordinateur d’utilisateur final**

1.  Dans la fenêtre **jeu d’outils de diagnostics et de récupération** sur un ordinateur d’utilisateur final, cliquez sur **crash Analyzer**.

2.  Fournissez les informations requises pour les outils de débogage de Microsoft pour Windows.

3.  Fournissez les informations requises pour les fichiers de symboles. Pour plus d’informations sur les fichiers de symboles, voir [Comment s’assurer que l’analyseur d’incidents peut accéder aux fichiers de symboles](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-10.md).

4.  Fournissez les informations requises pour un fichier de vidage de mémoire. Pour déterminer l’emplacement du fichier de vidage de mémoire:

    1.  Ouvrez la fenêtre de **Propriétés système** .

    2.  Cliquez sur **Démarrer**, tapez **sysdm.cpl**, puis appuyez sur **entrée**.

    3.  Cliquez sur l’onglet **Avancé**.

    4.  Dans la zone **démarrage et récupération** , cliquez sur **paramètres**.

        Si vous n’avez pas accès à la fenêtre de **Propriétés système** , vous pouvez rechercher des fichiers de vidage sur l’ordinateur de l’utilisateur final à l’aide de l’outil de **recherche** dans Microsoft Diagnostics and Recovery Tools (DART) 10.

    Le **crash Analyzer** analyse le fichier de vidage de la mémoire et signale la cause probable du problème. Vous pouvez afficher des informations supplémentaires sur l’échec, par exemple le message de vidage de mémoire et la description spécifiques, les pilotes chargés au moment de l’échec et la sortie complète de l’analyse.

5.  Identifiez la stratégie appropriée pour résoudre le problème. La stratégie est susceptible de nécessiter la désactivation ou la mise à jour du pilote de périphérique à l’origine de l’échec à l’aide du nœud **services et pilotes** de l’outil de gestion de l' **ordinateur** dans DART 10.

## Rubriques connexes


[Diagnostic d'échecs du système avec l'Analyseur d'incident](diagnosing-system-failures-with-crash-analyzer-dart-10.md)

[Opérations de DaRT10](operations-for-dart-10.md)

 

 





