---
title: Procédure pour installer Application Virtualization Sequencer
description: Procédure pour installer Application Virtualization Sequencer
author: dansimp
ms.assetid: 89cdf60d-18b0-4204-aa9f-b402610f8f0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a6fe03f2149504b6c34c70b2b82ce2ba0b55ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807054"
---
# Procédure pour installer Application Virtualization Sequencer


Le Sequencer Microsoft Application Virtualization vérifie et enregistre le processus d’installation et de configuration pour les applications, afin que l’application puisse être exécutée en tant qu’application virtuelle. Vous devriez installer le Sequencer sur un ordinateur sur lequel seul le système d’exploitation est installé. Vous pouvez également installer le Sequencer sur un ordinateur exécutant un environnement virtuel (par exemple, Microsoft Virtual PC). Cette méthode est utile, car il est plus facile de mettre à jour un environnement d’séquençage net qui peut être réutilisé avec une configuration supplémentaire minimum.

Vous devez disposer des droits d’administrateur sur l’ordinateur que vous utilisez pour séquencer l’application, et l’ordinateur ne doit pas exécuter de version du client App-V. La création d’une application virtuelle à l’aide du Sequencer est gourmande en ressources; c’est pourquoi il est important d’installer le Sequencer sur un ordinateur qui répond ou dépasse la configuration recommandée. L’exécution du Sequencer App-V en mode sans échec n’est pas prise en charge. Pour plus d’informations sur la configuration système requise, voir [Configuration requise pour le système de virtualisation des applications](application-virtualization-system-requirements.md).

**Important**  Après avoir séquencé une application, vous devez réinstaller le système d’exploitation et le Sequencer de l’ordinateur que vous utilisez pour séquencer les applications avant de procéder à une nouvelle application.

 

**Pour installer le Sequencer Microsoft Application Virtualization**

1.  Copiez les fichiers d’installation de Microsoft Application Virtualization Sequencer sur l’ordinateur sur lequel vous voulez l’installer.

2.  Pour démarrer l’Assistant Installation de Microsoft Application Virtualization Sequencer, sélectionnez **setup.exe**. Si le **package redistribuable Microsoft Visual C++ SP1 (x86)** n’est pas détecté avant l’installation, **setup.exe** l’installera.

3.  Dans la page **Bienvenue** , cliquez sur **suivant**.

4.  Dans la page **contrat de licence** , pour accepter les conditions du contrat de licence, cliquez sur **J’accepte les conditions du contrat**de licence. Cliquez sur **Suivant**.

5.  Dans la page **dossier de destination** , pour accepter le dossier d’installation par défaut, cliquez sur **suivant**. Pour spécifier un autre dossier de destination, cliquez sur **modifier** , puis spécifiez le dossier d’installation qui sera utilisé pour l’installation. Cliquez sur **Suivant**.

6.  Dans la page **êtes-vous prêt à installer le programme** , cliquez sur **installer**pour lancer l’installation.

7.  Dans la page **Assistant InstallShield terminé** , pour fermer l’Assistant Installation et ouvrir le Sequencer, cliquez sur **Terminer**. Pour fermer l’Assistant Installation sans ouvrir le Sequencer, désactivez **l’option lancer le programme** , puis cliquez sur **Terminer**.

## Rubriques connexes


[Procédure pour mettre à niveau Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)

[Configuration requise pour le déploiement d'Application Virtualization](application-virtualization-deployment-requirements.md)

 

 





