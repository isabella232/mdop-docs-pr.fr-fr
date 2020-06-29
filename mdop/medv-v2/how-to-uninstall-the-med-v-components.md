---
title: Comment désinstaller les composants de MED-V
description: Comment désinstaller les composants de MED-V
author: dansimp
ms.assetid: c121dd27-6b2f-4d41-a21a-c6e8608c5c41
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 514ec8227b858b34289ca2330f7cfb038bc4f00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804669"
---
# Comment désinstaller les composants de MED-V


Dans certains cas, vous voudrez peut-être désinstaller tout ou partie des composants 2,0 de Microsoft Enterprise Desktop Virtualization (MED-V) de votre entreprise. Par exemple, vous avez résolu tous les problèmes de compatibilité du système d’exploitation des applications ou vous voulez déployer un autre espace de travail MED-V dans votre entreprise.

En règle générale, vous pouvez configurer votre système de distribution de logiciels électroniques pour désinstaller les composants MED-V à l’aide d’un programme d’installation Windows. Vous pouvez également désinstaller les composants MED-V manuellement.

**Important**  Avant de désinstaller l’agent hôte MED-V, vous devez d’abord désinstaller les espaces de travail MED-V installés.

 

Pour désinstaller les composants MED-V de votre entreprise, procédez comme suit.

**Pour désinstaller MED-V à l’aide d’un système de distribution de logiciels électronique**

1.  Utilisez votre système ESD pour distribuer un script qui appelle le programme exécutable uninstall.exe pour chaque espace de travail MED-V que vous voulez désinstaller. Le fichier se trouve sur C:\\ProgramData\\Microsoft\\Medv\\Workspace. Vous pouvez définir un indicateur pour exécuter le programme de désinstallation du programme exécutable en silence de sorte que les utilisateurs finaux ne connaissent pas la désinstallation.

2.  Créer un package pour distribuer le fichier d’installation de l’agent hôte MED-V sur chaque ordinateur sur lequel un espace de travail MED-V a été désinstallé. Configurez le package pour exécuter la désinstallation en mode silencieux.

Le client ESD reconnaît lorsque les nouveaux packages sont disponibles et commence à désinstaller les packages conformément à la définition et aux exigences.

**Pour désinstaller manuellement un espace de travail MED-V**

1.  Sur l’ordinateur hôte, cliquez sur **Démarrer**, sur **panneau de configuration**, puis sur **programmes et fonctionnalités**.

2.  Dans la fenêtre **programmes et fonctionnalités** , sélectionnez l’espace de travail MED-V que vous voulez supprimer, puis cliquez sur **désinstaller**. (L’espace de travail MED-V est nommé «MED-V Workspace- &lt; *espace de travail \ _name* &gt; "). L' &lt; Assistant *de configuration de l’espace de travail \ _name* &gt; **Setup Wizard** s’ouvre.

3.  Dans l' **Assistant Configuration**, cliquez sur **suivant**, puis sur **supprimer**.

4.  Si vous le souhaitez, activez la case à cocher pour supprimer le disque dur virtuel maître et les disques de différenciation créés par MED-V. Cette opération n’est pas obligatoire, mais libère de l’espace disque après la désinstallation.

5.  Cliquez sur **supprimer**.

    **Remarques**  Si MED-V est en cours d’exécution, une boîte de dialogue s’affiche et vous demande si vous souhaitez l’arrêter. Cliquez sur **Oui** pour continuer la désinstallation. Cliquez sur **non** pour annuler la désinstallation.

     

Vous pouvez également supprimer un espace de travail MED-V en exécutant le `uninstall.exe` fichier qui se trouve généralement sur C:\\ProgramData\\Microsoft\\Medv\\Workspace.

**Pour désinstaller manuellement l’agent hôte MED-V**

1.  Sur l’ordinateur hôte de Windows 7, cliquez sur **Démarrer**, sur **panneau de configuration**, puis sur **programmes et fonctionnalités**.

2.  Dans la fenêtre **programmes et fonctionnalités** , sélectionnez **agent d’hébergement MED-V**, puis cliquez sur **désinstaller**.

    Le programme d’installation de Windows supprime l’agent hôte MED-V.

    **Remarques**  Si vous essayez de désinstaller l’agent hôte MED-V avant de désinstaller l’espace de travail MED-V, une boîte de dialogue s’affiche pour indiquer que vous devez d’abord désinstaller l’espace de travail MED-V. Cliquez sur **OK** pour continuer.

     

**Pour désinstaller manuellement le module de création de package de l’espace de travail MED-V**

1.  Sur l’ordinateur hôte, cliquez sur **Démarrer**, sur **panneau de configuration**, puis sur **programmes et fonctionnalités**.

2.  Dans la fenêtre **programmes et fonctionnalités** , sélectionnez **Gestionnaire de package d’espace de travail MED-V**, puis cliquez sur **désinstaller**.

    Le programme d’installation de Windows supprime le module de création de package de l’espace de travail MED-V.

    **Remarques**  Vous pouvez désinstaller le module de création de package de l’espace de travail MED-V à tout moment sans affecter les espaces de travail MED-V déployés.

     

## Rubriques connexes


[Déployer les composants MED-V](deploy-the-med-v-components.md)

 

 





