---
title: Procédure pour mettre à niveau un package d'application séquencée à l'aide d'une ligne de commande
description: Procédure pour mettre à niveau un package d'application séquencée à l'aide d'une ligne de commande
author: dansimp
ms.assetid: 682fac46-c71d-4731-831b-81bfd5032764
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eade2ced43852419176f635918f0a6b7c3444aee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806726"
---
# Procédure pour mettre à niveau un package d'application séquencée à l'aide d'une ligne de commande


Utilisez la procédure suivante pour mettre à niveau une application virtuelle à l’aide d’une ligne de commande. Lorsque vous mettez à niveau un package d’application virtuelle existant à l’aide de la ligne de commande, la version d’origine du fichier. SFT est supprimée. Vous devez sauvegarder le fichier. SFT associé avant de mettre à niveau le package à l’aide de la ligne de commande.

**Pour mettre à niveau une application virtuelle**

1.  Sur l’ordinateur exécutant le Sequencer Application Virtualization (App-V), ouvrez l’invite de commandes, sélectionnez **Démarrer**, **exécuter**, puis tapez **cmd**. Cliquez sur **OK**.

2.  À l’invite de commandes, indiquez l’emplacement où le Sequencer App-V est installé. Par exemple, à l’invite de commandes, vous pouvez taper ce qui suit: **CD C:\\Program Files\\Microsoft**.

3.  À l’invite de commandes, tapez la commande suivante, en remplaçant le texte entre guillemets par vos valeurs:

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **Remarque**  
    Vous pouvez spécifier des paramètres supplémentaires à l’aide de la ligne de commande, en fonction de la complexité de l’application que vous effectuez la mise à niveau. Pour obtenir la liste complète des paramètres disponibles pour une utilisation avec le Sequencer App-V, voir [paramètres de ligne de commande](command-line-parameters.md).



~~~
Use the value descriptions in the following table to help you determine the actual text you will use in the preceding command.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>pathtosourceSPRJ</em></p></td>
<td align="left"><p>Specifies the directory location of the virtual application to be upgraded.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtoUpgradeInstaller</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an upgrade to the application.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodecodefolder</em></p></td>
<td align="left"><p>Specify the directory in which to unpack the SFT file.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. Appuyez sur **entrée**.

## Rubriques connexes


[Procédure pour gérer toutes les applications virtuelles à l'aide de la ligne de commande](how-to-manage-virtual-applications-using-the-command-line.md)









