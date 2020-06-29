---
title: Comment séquencer un package à l’aide de PowerShell
description: Comment séquencer un package à l’aide de PowerShell
author: dansimp
ms.assetid: b41feed9-d1c5-48a3-940c-9a21d594f4f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bbb9641ba75eda4d190892fa2bd0043c92ed9006
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805173"
---
# Comment séquencer un package à l’aide de PowerShell


Utilisez la procédure suivante pour créer un package App-V 5,0 à l’aide de PowerShell.

**Remarques**  Avant d’utiliser cette procédure, vous devez copier les fichiers du programme d’installation associé sur l’ordinateur exécutant le Sequencer et vous avez lu et compris la section de Sequencer de [planification pour le déploiement du client et du Sequencer App-V 5,0](planning-for-the-app-v-50-sequencer-and-client-deployment.md).

 

**Pour créer une nouvelle application virtuelle à l’aide de PowerShell**

1.  Installez le Sequencer App-V 5,0. Pour plus d’informations sur l’installation de Sequencer, voir [Comment installer le Sequencer](how-to-install-the-sequencer-beta-gb18030.md).

2.  Pour ouvrir une console PowerShell, cliquez sur **Démarrer** et tapez **PowerShell**. Cliquez avec le bouton droit sur **Windows PowerShell**, puis sélectionnez **Exécuter en tant qu’administrateur**.

3.  À l’aide de la console PowerShell, tapez ce qui suit: **import-module appvsequencer**.

4.  Pour créer un package, utilisez l’applet **de nouvelle applet de nouveau-AppvSequencerPackage** . Les paramètres suivants sont nécessaires pour créer un package:

    -   **Nom** : spécifie le nom du package.

    -   **PrimaryVirtualApplicationDirectory** : spécifie le chemin d’accès du répertoire qui sera utilisé pour installer l’application. Ce chemin doit exister.

    -   **Programme d’installation** : spécifie le chemin d’accès au programme d’installation d’applications associé.

    -   **Path** -spécifie le répertoire de sortie du package.

    Exemple:

    **New-AppvSequencerPackage-nom &lt; du package &gt; -PrimaryVirtualApplicationDirectory chemin d’accès &lt; au programme d’installation racine du package vers le &gt; &lt; répertoire exécutable du programme d’installation &gt; -OutputPath &lt; du chemin de sortie&gt;**

    Attendez que le Sequencer crée le package. La création d’un package à l’aide de PowerShell peut prendre du temps. Si le package n’a pas été créé correctement, une erreur est retournée.

    La liste suivante présente des paramètres facultatifs supplémentaires qui peuvent être utilisés avec l’applet **de commande New-AppvSequencerPackage** :

    -   AcceleratorFilePath: spécifie le chemin d’accès au fichier Accelerator. cab pour générer un package.

    -   InstalledFilesPath: spécifie le chemin d’accès de l’emplacement vers lequel les fichiers locaux installés de l’application sont enregistrés.

    -   InstallMediaPath: spécifie le chemin d’accès du support d’installation.

    -   TemplateFilePath: spécifie le chemin d’accès d’un fichier de modèle si vous souhaitez personnaliser le processus de séquençage.

    -   FullLoad: indique que le package doit être entièrement téléchargé sur l’ordinateur exécutant l’application-V 5,0 pour pouvoir être ouvert.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Administration d'App-V à l'aide de PowerShell](administering-app-v-by-using-powershell.md)

 

 





