---
title: Comment installer le Sequencer (App-V 4,6 SP1)
description: Comment installer le Sequencer (App-V 4,6 SP1)
author: dansimp
ms.assetid: fe8eb876-28fb-46ae-b592-da055107e639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 611564e861d65dcd357c58732fb60dab21c05abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807041"
---
# Comment installer le Sequencer (App-V 4,6 SP1)


Le Sequencer Microsoft Application Virtualization (App-V) vérifie et enregistre le processus d’installation et de configuration pour les applications, afin que l’application puisse être exécutée en tant qu’application virtuelle. Vous devriez installer le Sequencer App-V sur un ordinateur sur lequel seul le système d’exploitation est installé. Vous pouvez également installer le Sequencer sur un ordinateur exécutant un environnement virtuel (par exemple, un ordinateur virtuel). Cette méthode est utile, car il est plus facile de conserver un environnement de séquençage net que vous pouvez réutiliser avec une configuration supplémentaire minimum.

Vous devez disposer d’informations d’identification d’administrateur sur l’ordinateur que vous utilisez pour séquencer l’application, et l’ordinateur ne doit pas exécuter de version du client App-V. La création d’une application virtuelle à l’aide du Sequencer App-V nécessite plusieurs opérations, donc il est important que vous installiez le Sequencer sur un ordinateur qui répond ou dépasse la [configuration logicielle requise pour la configuration matérielle et logicielle requise](application-virtualization-sequencer-hardware-and-software-requirements.md)pour le Sequencer.

**Remarque**  
L’exécution du Sequencer App-V en mode sans échec n’est pas prise en charge.



**Pour installer le Sequencer Microsoft Application Virtualization**

1.  Copiez les fichiers d’installation de Microsoft Application Virtualization Sequencer sur l’ordinateur sur lequel vous voulez l’installer.

2.  Pour démarrer l’Assistant Installation de Microsoft Application Virtualization Sequencer, double-cliquez sur **Setup.exe**. Si le **package redistribuable Microsoft Visual C++ SP1 (x86)** n’est pas détecté avant l’installation, cliquez sur **installer** pour installer la prérequis requise.

3.  Dans la page **Bienvenue** , cliquez sur **suivant**pour continuer l’installation.

4.  Dans la page **contrat de licence** , pour accepter les conditions du contrat de licence, cliquez sur **J’accepte les termes du contrat**de licence, puis cliquez sur **suivant**.

5.  Dans la page **dossier de destination** , pour accepter le dossier d’installation par défaut, cliquez sur **suivant**. Pour spécifier un autre dossier de destination, cliquez sur **modifier** , puis spécifiez le dossier d’installation qui sera utilisé pour l’installation. Cliquez sur **Suivant**.

6.  Sur la page **lecteur virtuel** , pour configurer le lecteur par défaut de la virtualisation d’application **Q:\\** (par défaut) le lecteur d’exécution des applications séquencées, cliquez sur **suivant**. Si vous voulez spécifier une autre lettre de lecteur, sélectionnez la lettre de lecteur de votre choix dans la liste, puis cliquez sur **Next (suivant**).

    **Important**  
    La lettre du lecteur de virtualisation des applications spécifiée avec cette étape est la lettre du lecteur à partir de laquelle les applications virtuelles seront exécutées sur les ordinateurs cibles. La lettre de lecteur spécifiée doit être disponible et non actuellement utilisée sur les ordinateurs exécutant le client App-V. Si le lecteur spécifié est déjà utilisé, l’application virtuelle échoue sur l’ordinateur cible.



7.  Dans la page **êtes-vous prêt à installer le programme** , cliquez sur **installer**pour lancer l’installation.

8.  Dans la page **Assistant InstallShield terminé** , pour fermer l’Assistant Installation et ouvrir le Sequencer App-V, cliquez sur **Terminer**. Pour fermer l’Assistant Installation sans ouvrir le Sequencer, désactivez **lancer le programme**, puis cliquez sur **Terminer**.

    **Remarque**  
    Si vous avez installé le Sequencer App-V sur un ordinateur exécutant un environnement virtuel (par exemple, une machine virtuelle), vous devez prendre une photo. Après avoir séquencé une application, vous pouvez revenir à cette image pour effectuer une séquence de l’application suivante.



~~~
When you uninstall the Sequencer, the following registry keys are not removed from the computer that the Sequencer was installed on. Additionally, you must restart the computer after you have uninstalled the Sequencer so that all associated drivers can be stopped and the operation can be completed.

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey**
~~~

## Rubriques connexes


[Configuration d'Application Virtualization Sequencer (App-V4.6 SP1)](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)









