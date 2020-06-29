---
title: Comment installer l'agent hôte MED-V manuellement
description: Comment installer l'agent hôte MED-V manuellement
author: dansimp
ms.assetid: 4becc90b-6481-4e1f-a4d3-aec74c8821ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a7fb44b23a390cf394af2331152955afc2d8eba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804572"
---
# Comment installer l'agent hôte MED-V manuellement


Il existe deux composants distincts mais liés à la solution 2,0 de Microsoft Enterprise Desktop Virtualization (MED-V): agent d’hébergement et agent invité MED-V. L’agent hôte réside sur l’ordinateur hôte (l’ordinateur de l’utilisateur exécutant Windows 7) et fournit un canal permettant de communiquer avec l’invité MED-V (l’ordinateur virtuel MED-V qui s’exécute sur l’ordinateur hôte). Il fournit également certaines fonctionnalités associées à MED-V, comme la publication d’applications.

En règle générale, vous déployez et installez l’agent d’hébergement MED-V en utilisant la méthode de mise en service préférée de votre entreprise. Néanmoins, avant de déployer MED-V au sein de votre entreprise, vous préférerez peut-être installer l’agent hôte localement pour le test. Cette section fournit des instructions pas à pas pour l’installation manuelle de l’agent hôte MED-V.

**Remarques**  L’agent d’invité MED-V est automatiquement installé lors de la première configuration.

 

**Important**  Fermez Internet Explorer avant d’installer l’agent d’hébergement MED-V, sinon des conflits peuvent se produire plus tard avec la redirection d’URL. Vous pouvez également le faire en spécifiant un redémarrage de l’ordinateur lors d’une distribution.

 

**Pour installer l’agent hôte MED-V**

1.  Recherchez les fichiers d’installation de MED-V que vous avez reçus dans le cadre de votre téléchargement de logiciels.

2.  Double-cliquez sur le fichier d’installation MED-V \ _HostAgent \ _Setup.

    L’Assistant de configuration de l' **agent d’hébergement MED-V de Microsoft Enterprise Desktop Virtualization** s’ouvre. Cliquez sur **Suivant** pour poursuivre.

3.  Acceptez les termes du contrat de licence logiciel Microsoft, puis cliquez sur **suivant**.

4.  Sélectionnez le dossier de destination pour l’installation de l’agent hôte MED-V. Cliquez sur **Suivant**.

5.  Pour commencer l’installation de l’agent hôte, cliquez sur **installer**.

6.  Une fois l’installation terminée, cliquez sur **Terminer** pour fermer l’Assistant.

    Pour vérifier que l’installation de l’agent hôte a réussi, cliquez sur **Démarrer**, sur **tous les programmes**, sur **virtualisation du bureau Microsoft entreprise**, puis sur **agent hôte MED-V**.

**Remarques**  Tant qu’un espace de travail MED-V n’est pas installé, l’agent hôte MED-V peut être démarré et exécuté, mais ne fournit aucune fonctionnalité.

 

## Rubriques connexes


[Déploiement des composants de MED-V via un système de distribution électronique de logiciels](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md)

[Comment installer le Gestionnaire de package de l'espace de travail MED-V](how-to-install-the-med-v-workspace-packager.md)

[Comment désinstaller les composants de MED-V](how-to-uninstall-the-med-v-components.md)

 

 





