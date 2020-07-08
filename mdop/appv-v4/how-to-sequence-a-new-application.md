---
title: Procédure pour séquencer une nouvelle application
description: Procédure pour séquencer une nouvelle application
author: dansimp
ms.assetid: e01e98cd-2378-478f-9739-f72c465bf79a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aab769256116e2635edbc4bcf55d212e3a2152f8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806798"
---
# Procédure pour séquencer une nouvelle application


Le Sequencer Application Virtualization (App-V) crée des applications qui peuvent être exécutées dans un environnement virtuel. Le Sequencer App-V analyse le processus d’installation et de configuration d’une application, et enregistre les informations nécessaires à l’exécution de l’application dans un environnement virtuel. Vous pouvez également utiliser le Sequencer App-V pour configurer les fichiers et configurations applicables à tous les utilisateurs, ainsi que les fichiers et configurations que les utilisateurs peuvent personnaliser. Lorsque vous séquençagez une application, vous devez enregistrer le package sur un lecteur local de l’ordinateur sur lequel vous effectuez le séquençage.

Une application séquencée n’interagit pas avec le système d’exploitation, car chaque application s’exécute dans un environnement virtuel et est isolément d’autres applications qui peuvent être installées ou exécutées sur l’ordinateur cible. Cet isolement réduit considérablement les conflits d’application et réduit le nombre requis de tests d’avant déploiement d’application.

Une fois que vous avez correctement séquencé l’application, celle-ci est disponible dans la console de Sequencer App-V. L’exécution du Sequencer App-V en mode sans échec n’est pas prise en charge.

**Pour séquencer une nouvelle application**

1.  Vous devez créer le lecteur de virtualisation des applications pour séquencer une nouvelle application virtuelle. Pour créer le lecteur de virtualisation des applications, mappez le lecteur Q:\\ à un emplacement qui peut être utilisé pour enregistrer des fichiers pendant que vous séquençagez une application. Vous devez ensuite créer des répertoires individuels pour chaque application que vous envisagez de séquentieler sur le lecteur Q:\\. Vous pouvez créer les dossiers cibles de l’application virtuelle avant de séquencer une application, ou vous pouvez la créer à l’étape 5 de cette procédure.

2.  Pour démarrer la console de Sequencer App-v, sur l’ordinateur exécutant le Sequencer App-v, sélectionnez **Démarrer**  /  **programmes**  /  **Microsoft Application Virtualization**  /  **Sequencer Microsoft application**Virtualization. Pour démarrer l' **Assistant séquençage**, sélectionnez **fichier**  /  **nouveau package**.

3.  Dans la page informations sur le **package** , spécifiez le **nom du package** qui sera affecté à l’application virtuelle. Le nom du package est requis pour générer le fichier Windows Installer associé. Vous devez également ajouter un commentaire facultatif qui sera affecté au package et qui fournit des informations détaillées sur l’application virtuelle. Pour afficher la page **Options avancées** , sélectionnez **afficher les options de surveillance avancées**. Cliquez sur **Suivant**.

    **Remarque**  
    Pour afficher la page **Options avancées** , vous devez sélectionner **afficher les options de surveillance avancée**. Si vous n’avez pas besoin de la page **Options avancées** , passez à l’étape 4.



4.  Dans la page **Options avancées** , pour spécifier la **taille du bloc** pour l’application virtuelle, sélectionnez la taille souhaitée. La taille des blocs détermine la manière dont le fichier **. SFT** sera fractionné pour diffuser le package sur le réseau sur les ordinateurs cibles. Pour permettre à Microsoft Update de mettre à jour l’application en cours de séquence; Sélectionnez **autoriser l’exécution de Microsoft Update lors de l’analyse**. Si vous sélectionnez cette option, les mises à jour Microsoft peuvent être installées pendant la phase de surveillance et vous devrez accepter les mises à jour associées pour qu’elles soient installées. Pour remapper les fichiers de la bibliothèque de liens dynamiques (. dll) pris en charge de façon à ce qu’ils utilisent un espace contigu de RAM, sélectionnez **relocal DLLs**. La sélection de cette option permet d’économiser la mémoire et d’améliorer les performances. Dans de nombreux cas, cette option n’est pas prise en charge, mais elle est utile dans les environnements dotés d’une RAM limitée, par exemple dans les scénarios Terminal Server. Cliquez sur **Suivant**.

5.  Dans la page d' **installation du moniteur** , pour surveiller l’installation d’une application, cliquez sur **commencer la surveillance**. Après avoir cliqué sur **commencer l’analyse**, spécifiez le répertoire sur le lecteur Q:\\ où l’application sera installée. Pour installer l’application dans un dossier qui n’a pas été créé, cliquez sur **créer un nouveau dossier**. Vous devez installer chaque application que vous séquencez dans un répertoire distinct.

    **Important**  
    Le nom du dossier que vous spécifiez ne doit pas comporter plus de 8 caractères.



~~~
Wait for the virtual environment to load, and then install the application so that the App-V Sequencer can monitor the process. When you have completed the installation, click **Stop Monitoring** and then click **Next**.
~~~

6. Dans la page **fichiers supplémentaires à mapper sur le système de fichiers virtuel (VFS)** , cliquez sur **Ajouter**pour spécifier d’autres fichiers à ajouter au système de fichiers virtuel (VFS). Recherchez le fichier que vous voulez ajouter, puis cliquez sur **ouvrir**. Pour effacer les fichiers existants qui ont été ajoutés, cliquez sur **Réinitialiser** , puis sur **suivant**.

7. Dans la page **configurer des applications** , configurez les raccourcis et les associations de types de fichiers qui seront associés à l’application virtuelle. Sélectionnez l’élément que vous voulez mettre à jour, puis cliquez sur **modifier les emplacements**. Spécifiez les configurations dans la boîte de dialogue **emplacements de raccourci** . Cliquez sur **OK** , puis sur **suivant**.

8. Dans la page **Launch applications (lancer des applications** ), pour démarrer l’application afin de vous assurer que le package est optimisé pour la diffusion, sélectionnez-le, puis cliquez sur **Launch**. Cette étape est utile pour configurer la manière dont l’application s’exécute au départ sur les ordinateurs cibles, et pour accepter tout contrat de licence associé avant la mise à la disposition des clients du package. S’il existe plusieurs applications associées à ce package, vous pouvez sélectionner **lancer tout** pour ouvrir toutes les applications. Pour séquencer le package, cliquez sur **suivant**.

9. Sur la page **package de séquence** , pour fermer l’Assistant, cliquez sur **Terminer**.

10. Une fois que vous avez créé le package, pour enregistrer le package, dans la console App-V du Sequencer, sélectionnez **fichier**  /  **Enregistrer** et spécifiez le nom et l’emplacement de l’enregistrement du package.

## Rubriques connexes


[Tâches pour Application Virtualization Sequencer](tasks-for-the-application-virtualization-sequencer.md)









