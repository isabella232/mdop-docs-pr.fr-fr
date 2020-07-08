---
title: Comment créer un accélérateur de package à l'aide de PowerShell
description: Comment créer un accélérateur de package à l'aide de PowerShell
author: dansimp
ms.assetid: 8e527363-d961-4153-826a-446a4ad8d980
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4270db9a5f0603cff1f33e6244a5abb517572d97
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805622"
---
# Comment créer un accélérateur de package à l'aide de PowerShell


Les accélérateurs de package App-V 5,0 séquencéssent automatiquement de grandes applications complexes. Par ailleurs, lorsque vous appliquez un accélérateur de package App-V 5,0, il n’est pas toujours nécessaire d’installer manuellement une application pour créer le package virtualisé.

**Pour créer un accélérateur de package**

1.  Installez le Sequencer App-V 5,0. Pour plus d’informations sur l’installation de Sequencer, voir [Comment installer le Sequencer](how-to-install-the-sequencer-beta-gb18030.md).

2.  Pour ouvrir une console PowerShell, cliquez sur **Démarrer** et tapez **PowerShell**. Cliquez avec le bouton droit sur **Windows PowerShell**, puis sélectionnez **Exécuter en tant qu’administrateur**. Utilisez l’applet **de nouvelle applet de nouveau-AppvPackageAccelerator** .

3.  Pour créer un accélérateur de package, assurez-vous d’avoir le package. AppV pour créer un accélérateur à partir de, les fichiers de média d’installation ou d’installation, et éventuellement un fichier Lisez-moi pour les utilisateurs de l’accélérateur à utiliser. Les paramètres suivants sont requis pour utiliser l’applet de commande du package Accelerator:

    -   **InstalledFilesPath** : spécifie le chemin d’installation de l’application.

    -   **Programme d’installation** : spécifie le chemin d’accès au support du programme d’installation de l’application.

    -   **InputPackagePath** : spécifie le chemin d’accès au package. AppV.

    -   **Path** : spécifie le répertoire de sortie du package.

    L’exemple suivant montre comment créer un accélérateur de package avec un package. AppV et le support d’installation:

    **New-AppvPackageAccelerator-InputPackagePath &lt; chemin d’accès au fichier. AppV &gt; -chemin du programme d’installation &lt; dans le répertoire exécutable du programme d’installation &gt; &lt; du chemin de sortie&gt;**

    Les paramètres facultatifs supplémentaires qui peuvent être utilisés avec l’applet **de commande New-AppvPackageAccelerator** s’affichent dans la liste suivante:

    -   **AcceleratorDescriptionFile** : spécifie le chemin d’accès aux instructions de l’accélérateur de package créé par l’utilisateur. Les instructions de l’accélérateur de package sont des fichiers de description **. txt** ou **. rtf** qui seront empaquetés avec le package créé à l’aide de l’accélérateur de package.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Administration d'App-V à l'aide de PowerShell](administering-app-v-by-using-powershell.md)

 

 





