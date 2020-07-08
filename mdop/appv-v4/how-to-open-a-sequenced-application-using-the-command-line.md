---
title: Procédure pour ouvrir une application séquencée à l'aide de la ligne de commande
description: Procédure pour ouvrir une application séquencée à l'aide de la ligne de commande
author: dansimp
ms.assetid: dc23ee65-8aea-470e-bb3f-a2f2b06cb241
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c99ab6b41947fc255afa9cad5b3ed2e22e672c3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806898"
---
# Procédure pour ouvrir une application séquencée à l'aide de la ligne de commande


Vous pouvez ouvrir des packages d’application virtuelle à l’aide de la ligne de commande. Vous devez exécuter l’invite **cmd** en tant qu’administrateur.

Utilisez la procédure suivante pour ouvrir des packages d’application séquencés à l’aide de la ligne de commande.

**Pour ouvrir une application séquencée à l’aide de la ligne de commande**

1.  Pour ouvrir l’invite de commandes, cliquez sur **Démarrer**, sélectionnez **exécuter**, tapez **cmd**, puis cliquez sur **OK**.

2.  À l’invite de commandes, tapez **cd\\** et spécifiez le chemin d’accès au répertoire dans lequel le Sequencer est installé, puis appuyez sur **entrée.**

3.  À l’invite de commandes, tapez la commande suivante, en remplaçant le texte en italique par vos valeurs:

    SFTSequencer/OPEN:*"spécifie le fichier. sprj à ouvrir"*

    Appuyez sur **entrée**.

4.  Vous pouvez également spécifier les paramètres facultatifs suivants. À l’invite de commandes, tapez les commandes suivantes en remplaçant le texte en italique par vos valeurs:

    /PACKAGENAME: "*spécifie le nom du package"*

    /MSI: indique la génération d’un programme d’installation Microsoft Windows associé.

    /COMPRESS: indique si le package est compressé. Par défaut, les packages ne sont pas compressés.

    Appuyez sur **entrée**.

    **Remarques**  Si le programme d’installation ou le package Windows Installer possède une interface utilisateur graphique, il s’affiche lorsque vous spécifiez les paramètres de ligne de commande.

     

## Rubriques connexes


[Procédure pour gérer toutes les applications virtuelles à l'aide de la ligne de commande](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





