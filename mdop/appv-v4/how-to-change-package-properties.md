---
title: Procédure pour modifier les propriétés du package
description: Procédure pour modifier les propriétés du package
author: dansimp
ms.assetid: 6050916a-d4fe-4dac-8f2a-47308dbbf481
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2427a2651f3941f967c171ae7854facc62b4aa9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807349"
---
# Procédure pour modifier les propriétés du package


Vous pouvez utiliser les procédures suivantes pour modifier le nom du package de virtualisation des applications et les commentaires qui lui sont associés.

Si c’est la première fois que le package a été créé, vous pouvez également modifier la taille du bloc de paramètre de séquençage, qui détermine la façon dont un package d’application séquencé est transmis à partir d’un serveur de virtualisation des applications vers un client de bureau de la virtualisation d’applications.

**Remarques**  Lorsque vous sélectionnez une taille de bloc, tenez compte de la taille du fichier SFT et de la bande passante réseau. Le flux d’un fichier dont la taille de blocs est plus petite prend plus de temps sur le réseau, mais il est plus gourmand en bande passante. Les fichiers de tailles de blocs plus grandes peuvent être plus rapides, mais ils utilisent plus de bande passante réseau. Dans le cadre de l’expérimentation, vous pouvez découvrir la taille maximale de bloc pour les applications en continu sur votre réseau.

 

Le reste des propriétés de package sous l’onglet **Propriétés** est généré automatiquement et ne peut pas être modifié sous cet onglet.

**Pour modifier le nom ou les commentaires du package**

1.  Cliquez sur l’onglet **Propriétés** .

2.  Dans la zone de texte **nom du package** , entrez ou modifiez le nom unique utilisé pour le package, qui peut contenir plusieurs applications.

3.  Dans la zone de texte **Commentaires** , vous pouvez entrer ou modifier des commentaires. La meilleure pratique recommandée consiste à fournir des informations détaillées sur le package et le séquençage.

4.  Dans le menu **fichier** , sélectionnez **Enregistrer**.

**Pour modifier la taille du bloc**

1.  Cliquez sur l’onglet **Propriétés** .

2.  Dans la liste déroulante **taille de bloc** , sélectionnez **4 Ko**, **16 ko**, **32 Ko**ou **64 Ko**.

3.  Dans le menu **fichier** , sélectionnez **Enregistrer**.

## Rubriques connexes


[À propos de l'onglet Propriétés](about-the-properties-tab.md)

[Console Sequencer](sequencer-console.md)

 

 





