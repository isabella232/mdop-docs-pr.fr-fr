---
title: Procédure pour séquencer une nouvelle application à l'aide de la ligne de commande
description: Procédure pour séquencer une nouvelle application à l'aide de la ligne de commande
author: dansimp
ms.assetid: c3b5c842-6a91-4d0a-9a22-c7b8d1aeb09a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ea7b1222dc00a0a4649cb342ac1ba41338484889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806806"
---
# Procédure pour séquencer une nouvelle application à l'aide de la ligne de commande


Vous pouvez utiliser une ligne de commande pour séquencer une nouvelle application. L’utilisation d’une ligne de commande est utile lorsque vous devez créer un grand nombre d’applications virtuelles ou lorsque vous avez besoin de créer des applications séquencées sur une base récurrente.

**Important**  
Le séquençage de la ligne de commande ne peut être utilisé que pour le séquençage par défaut. Si vous devez modifier les paramètres d’installation par défaut de l’application que vous séquençage, vous devez modifier manuellement l’application virtuelle ou la mettre à jour à l’aide du Sequencer Application Virtualization (App-V). Pour plus d’informations sur la mise à jour d’une application virtuelle à l’aide du Sequencer App-V, voir [Comment mettre à niveau une application virtuelle existante](how-to-upgrade-an-existing-virtual-application.md).



Utilisez la procédure suivante pour créer une application virtuelle à l’aide de la ligne de commande.

**Pour séquencer une application à l’aide de la ligne de commande**

1.  Sur l’ordinateur exécutant le Sequencer App-V, ouvrez l’invite de commandes en sélectionnant **Démarrer**, **exécuter**, puis tapez **cmd**. Cliquez sur **OK**.

2.  Utilisez l’invite de commandes pour spécifier l’emplacement où le Sequencer App-V est installé. Par exemple, à l’invite de commandes, vous pouvez taper ce qui suit: **CD C:\\Program Files\\Microsoft**.

3.  À l’invite de commandes, tapez la commande suivante, en remplaçant le texte entre guillemets par vos valeurs:

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **Remarque**  
    Vous pouvez spécifier des paramètres supplémentaires à l’aide de la ligne de commande, en fonction de la complexité de l’application que vous séquençage. Pour obtenir la liste complète des paramètres disponibles pour une utilisation avec le Sequencer App-V, voir [paramètres de ligne de commande du Sequencer](sequencer-command-line-parameters.md).



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
<td align="left"><p><em>pathtoMSI</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtopackageroot</em></p></td>
<td align="left"><p>Specify the package root directory.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. Appuyez sur **entrée**.

## Rubriques connexes


[Comment créer ou mettre à niveau des applications virtuelles à l’aide du Sequencer App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[Codes des erreurs de ligne de commande de Sequencer](sequencer-command-line-error-codes.md)

[Paramètres de ligne de commande de Sequencer](sequencer-command-line-parameters.md)









