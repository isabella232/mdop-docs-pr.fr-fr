---
title: Procédure pour mettre à niveau un package à l'aide de la commande Ouvrir un package
description: Procédure pour mettre à niveau un package à l'aide de la commande Ouvrir un package
author: dansimp
ms.assetid: 67c10440-de8a-4547-a34b-f83206d0cc3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cca438fe90373e8f934d1d790246544cdf46fa18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806738"
---
# Procédure pour mettre à niveau un package à l'aide de la commande Ouvrir un package


Utiliser la commande ouvrir un package pour mettre à niveau ou appliquer une mise à jour à un package d’application séquencé. Lorsque vous mettez à niveau un package d’application virtuelle existant à l’aide de la ligne de commande, la version d’origine du fichier. SFT est supprimée. Il est recommandé de sauvegarder le fichier. SFT associé avant de mettre à niveau le package à l’aide de la ligne de commande.

**Pour mettre à niveau un package à l’aide de la commande ouvrir le package**

1.  Pour ouvrir le package qui sera mis à niveau, dans la console Application Virtualization (App-V), sélectionnez **fichier**, puis **ouvrez package pour la mise à niveau**. Dans la boîte de dialogue **ouvrir** , sélectionnez le package qui sera mis à niveau.

2.  Pour démarrer l’Assistant **séquençage** , sélectionnez **Outils**, **Assistant séquençage**. Suivez les étapes de l’Assistant pour enregistrer la nouvelle application séquencée, sélectionnez **fichier**, puis **Enregistrer**.

3.  Pour ajouter le numéro de version au nom du package, dans la console de Sequencer, sélectionnez **Outils**, **options**. Sélectionnez **Ajouter la version du package au nom du fichier**. Cliquez sur **OK**.

    **Important**  Il est essentiel de mettre à jour le nom du fichier avec la version du package pour terminer la mise à niveau.

     

## Rubriques connexes


[Procédure pour gérer toutes les applications virtuelles à l'aide de la ligne de commande](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





