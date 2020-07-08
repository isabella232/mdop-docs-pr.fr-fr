---
title: Procédure pour modifier les systèmes d'exploitation associés à un fichier Windows Installer existant
description: Procédure pour modifier les systèmes d'exploitation associés à un fichier Windows Installer existant
author: dansimp
ms.assetid: 0633f7e2-aebf-4e00-be02-35bc59dec420
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63184852f996cbe09b476f456f7c2b509549f4fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806913"
---
# Procédure pour modifier les systèmes d'exploitation associés à un fichier Windows Installer existant


Utilisez la procédure suivante pour modifier les versions de système d’exploitation associées à un fichier Windows Installer (**MSI**) existant qui a été créé à l’aide du Sequencer App-V.

**Pour modifier les systèmes d’exploitation d’un fichier Windows Installer existant**

1.  Installez le Sequencer App-V sur un ordinateur de votre environnement sur lequel seul le système d’exploitation est installé. Vous pouvez également installer le Sequencer sur un ordinateur exécutant un environnement virtuel (par exemple, Microsoft Virtual PC). Cette méthode est utile, car il est plus facile de conserver un environnement de séquençage net que vous pouvez réutiliser avec une configuration supplémentaire minimum. Pour plus d’informations sur l’installation de Sequencer App-V, voir [Comment installer le Sequencer](how-to-install-the-sequencer.md).

2.  Copiez l’intégralité du package d’application virtuel contenant le fichier Windows Installer que vous voulez modifier sur l’ordinateur exécutant le Sequencer.

3.  Pour modifier le fichier du programme d’installation Windows, ouvrez la console de Sequencer, sélectionnez **package**  /  **Open**, puis naviguez jusqu’à l’emplacement dans lequel le package d’application virtuel associé au fichier d’installation Windows est enregistré.

4.  Pour ajouter ou supprimer des systèmes d’exploitation, sélectionnez l’onglet **déploiement** dans la console de Sequencer. Pour spécifier d’autres systèmes d’exploitation qui seront associés au fichier du programme d’installation Windows, sélectionnez le système d’exploitation de votre choix, puis cliquez sur la flèche qui pointe vers le contrôle de liste du système d’exploitation **sélectionné** .

    Pour supprimer une association de système d’exploitation, sélectionnez le système d’exploitation que vous voulez supprimer, puis cliquez sur la flèche qui pointe vers le contrôle de liste de systèmes d’exploitation **disponibles** .

5.  Pour créer un nouveau programme d’installation Windows qui sera associé au package d’application virtuelle, sélectionnez **générer le package Microsoft Windows Installer (MSI)**. Vous pouvez également sélectionner **Outils**  /  **créer**un fichier msi.

    **Remarques**  Si vous sélectionnez **Outils** / **création de MSI** pour créer un nouveau fichier Windows Installer, vous pouvez ignorer l' **étape 6** de cette procédure.

     

6.  Pour enregistrer le package d’application virtuelle, sélectionnez Enregistrer le **package**  /  **Save**.

## Rubriques connexes


[Tâches pour Application Virtualization Sequencer](tasks-for-the-application-virtualization-sequencer.md)

 

 





