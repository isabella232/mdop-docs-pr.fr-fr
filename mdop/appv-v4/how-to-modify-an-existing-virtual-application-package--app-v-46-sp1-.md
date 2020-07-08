---
title: Procédure pour modifier un package d'application virtuelle existant (App-V4.6SP1)
description: Procédure pour modifier un package d'application virtuelle existant (App-V4.6SP1)
author: dansimp
ms.assetid: f43a9927-4325-4b2d-829f-3068e4e84349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f0e9d45a32afa240ce7f6fb2ee5dfbc51889c1fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806946"
---
# Procédure pour modifier un package d'application virtuelle existant (App-V4.6SP1)


Utilisez les procédures suivantes pour modifier un package d’application virtuel existant. Vous pouvez utiliser les procédures suivantes pour:

-   Mettez à jour une application qui fait partie d’un package d’application virtuel existant. Pour effectuer cette tâche, utilisez la procédure **«pour mettre à jour une application dans un package d’application existant»** dans ce document.

-   Modification des propriétés associées à un package d’application virtuelle existant. Pour effectuer cette tâche, utilisez la procédure **«pour modifier les propriétés associées à un package d’application virtuelle existant»** dans ce document.

-   Ajoutez une nouvelle application à un package d’application virtuel existant. Pour effectuer cette tâche, utilisez la procédure **«pour ajouter une nouvelle application à un package d’application virtuelle existant»** dans ce document.

Pour pouvoir modifier un package d’application virtuelle, vous devez avoir installé le Sequencer App-V. Pour plus d’informations sur l’installation de Sequencer App-V, voir [Comment installer le Sequencer (App-V 4,6 SP1)](how-to-install-the-sequencer---app-v-46-sp1-.md).

**Pour mettre à jour une application dans un package d’application virtuel existant**

1.  Pour démarrer le Sequencer App-v, sur l’ordinateur exécutant le Sequencer App-v, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft Application Virtualization  /  **Sequencer**.

2.  Dans le Sequencer App-V, cliquez sur **modifier un package d’application virtuel existant**, puis cliquez sur **suivant**.

3.  Dans la page **Sélectionner une tâche** , cliquez sur **mettre à jour l’application dans le package existant**, puis cliquez sur **suivant**.

4.  Dans la page **Sélectionner un package** , cliquez sur **Parcourir** pour localiser le package d’application virtuel contenant l’application que vous voulez mettre à jour, puis cliquez sur **suivant**.

5.  Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui pourraient entraîner l’échec de la mise à jour de l’application, ou la mise à jour de l’application qui contient des données inutiles. Nous vous recommandons vivement de résoudre tous les problèmes potentiels avant de continuer. Une fois les conflits corrigés, cliquez sur **Actualiser**pour mettre à jour les informations affichées. Lorsque vous avez résolu tous les problèmes potentiels, cliquez sur **suivant**.

    **Important**  Si vous avez besoin de désactiver le logiciel antivirus, analysez l’ordinateur exécutant le Sequencer pour vous assurer qu’aucun fichier non souhaité ou malveillant n’est ajouté au package.

     

6.  Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de la mise à jour de l’application. Si la mise à jour n’a pas de fichier d’installation associé et que vous envisagez d’exécuter toutes les étapes d’installation manuellement, activez la case à cocher **activer cette option pour effectuer une installation personnalisée** , puis cliquez sur **suivant**.

7.  Dans la page **installation** , lorsque le programme d’installation de Sequencer et d’application est prêt, installez la mise à jour de l’application afin que le Sequencer puisse surveiller le processus d’installation. Si des fichiers d’installation supplémentaires doivent être exécutés dans le cadre de l’installation, cliquez sur **exécuter** et recherchez et exécutez les fichiers d’installation supplémentaires. Lorsque l’installation est terminée, sélectionnez J’ai **terminé d’installer**. Cliquez sur **Suivant**.

    **Remarques**  Le Sequencer vérifie l’ensemble des modifications et installations apportées à l’ordinateur exécutant le Sequencer, y compris les modifications et les installations effectuées en dehors de l’Assistant de séquençage.

     

8.  Dans la page **rapport d’installation** , vous pouvez consulter les informations relatives à l’application virtuelle que vous venez de mettre à jour. Pour obtenir une explication plus détaillée des informations affichées dans **informations supplémentaires**, double-cliquez sur l’événement. Après avoir consulté les informations, cliquez sur **suivant**.

9.  Sur la page de **diffusion** , exécutez chaque programme de manière à optimiser son exécution et son exécution plus efficacement sur les ordinateurs cibles. L’exécution de toutes les applications peut prendre quelques minutes. Après l’exécution de toutes les applications, fermez chacune d’elles, puis cliquez sur **suivant**.

    **Remarques**  Si vous voulez arrêter le chargement d’une application au cours de cette étape, dans la boîte de dialogue lancement de l' **application** , cliquez sur **arrêter**, puis cliquez sur l’une des options suivantes, **arrêter toutes les applications** ou **arrêter cette application uniquement**, en fonction de ce que vous voulez faire.

     

10. Dans la page **créer un package** , pour modifier le package sans l’enregistrer, activez la case à cocher **continuer à modifier le package sans enregistrer à l’aide de l’éditeur de package** . Lorsque vous sélectionnez cette option, le package de la console de Sequencer s’ouvre pour vous permettre de modifier le package avant son enregistrement. Cliquez sur **Suivant**.

    Pour enregistrer le package immédiatement, sélectionnez l’option **enregistrer le package**par défaut. Ajoutez des **Commentaires** facultatifs qui seront associés au package. Les commentaires sont utiles pour identifier la version et d’autres informations sur le package. L' **emplacement d’enregistrement** par défaut est également affiché. Pour modifier l’emplacement par défaut, cliquez sur **Parcourir** et spécifiez le nouvel emplacement. La taille du package non compressé s’affiche. Si la taille du package dépasse 4 Go (non compressée) et que vous envisagez de diffuser le package sur les ordinateurs cibles, vous devez sélectionner **compresser le package**, puis cliquer sur **créer**.

11. Dans la page **dernière étape** , cliquez sur **Fermer** pour fermer l’Assistant. Le package est désormais disponible dans le Sequencer.

**Pour modifier les propriétés associées à un package d’application virtuelle existant**

1.  Pour démarrer le Sequencer App-v, sur l’ordinateur exécutant le Sequencer App-v, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft Application Virtualization  /  **Sequencer**.

2.  Dans le Sequencer App-V, cliquez sur **modifier un package d’application virtuel existant**, puis cliquez sur **suivant**.

3.  Dans la page **Sélectionner une tâche** , cliquez sur modifier le **package**, puis sur **suivant**.

4.  Dans la page **Sélectionner un package** , cliquez sur **Parcourir** pour localiser le package d’application virtuel contenant les propriétés de l’application que vous voulez modifier, puis cliquez sur **modifier**.

5.  Dans la console de Sequencer, vous pouvez effectuer les tâches suivantes:

    -   Afficher les propriétés du package.

    -   Afficher l’historique des modifications de package.

    -   Afficher les fichiers de package associés.

    -   Modifier les paramètres du Registre.

    -   Passez en revue les paramètres de package supplémentaires (sauf les propriétés du fichier système d’exploitation).

    -   Créer un programme d’installation Windows (MSI) associé.

    -   Modifiez le fichier OSD.

    -   Compresser et décompresser un package.

    -   Ajouter des associations de types de fichiers.

    -   Définissez l’état de la clé de Registre virtualisé (substitution ou fusion).

    -   Définir l’état de dossier virtualisé.

    -   Modifier les mappages du système de fichiers virtuel.

6.  Lorsque vous avez fini de modifier les propriétés du package, **cliquez sur**  /  **Enregistrer** pour enregistrer le package.

**Pour ajouter une nouvelle application à un package d’application virtuelle existant**

1.  Pour démarrer le Sequencer App-v, sur l’ordinateur exécutant le Sequencer App-v, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft Application Virtualization  /  **Sequencer**.

2.  Dans le Sequencer App-V, cliquez sur **modifier un package d’application virtuel existant**, puis cliquez sur **suivant**.

3.  Dans la page **Sélectionner une tâche** , cliquez sur Ajouter une **nouvelle application**, puis cliquez sur **suivant**.

4.  Dans la page **Sélectionner un package** , cliquez sur **Parcourir** pour localiser le package d’application virtuel auquel vous souhaitez ajouter l’application, puis cliquez sur **suivant**.

5.  Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui peuvent entraîner l’échec de la création du package ou pour la mise à jour contenant des données inutiles. Nous vous recommandons vivement de résoudre tous les problèmes potentiels avant de continuer. Une fois les conflits corrigés, cliquez sur **Actualiser**pour mettre à jour les informations affichées. Lorsque vous avez résolu tous les problèmes potentiels, cliquez sur **suivant**.

    **Important**  Si vous avez besoin de désactiver le logiciel antivirus, analysez l’ordinateur exécutant le Sequencer pour vous assurer qu’aucun fichier non souhaité ou malveillant ne peut être ajouté au package.

     

6.  Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de l’application. Si l’application n’a pas de fichier d’installation associé et que vous envisagez d’exécuter toutes les étapes d’installation manuellement, activez la case à cocher **activer cette option pour effectuer une installation personnalisée** , puis cliquez sur **suivant**.

7.  Dans la page **installation** , lorsque le programme d’installation de Sequencer et d’application est prêt, installez l’application afin que le Sequencer puisse surveiller le processus d’installation. Si des fichiers d’installation supplémentaires doivent être exécutés dans le cadre de l’installation, cliquez sur **exécuter**, puis recherchez et exécutez les fichiers d’installation supplémentaires. Lorsque l’installation est terminée, sélectionnez J’ai **terminé d’installer**. Cliquez sur **Suivant**. Dans la boîte de dialogue **Rechercher un dossier** , spécifiez le répertoire principal dans lequel l’application sera installée. Il doit s’agir d’un nouvel emplacement pour ne pas remplacer la version existante du package d’application virtuelle.

    **Remarques**  Toutes les modifications et les installations apportées à l’ordinateur exécutant le Sequencer sont surveillées par le Sequencer, y compris les modifications et les installations effectuées en dehors de l’Assistant de séquençage.

     

8.  Sur la page **configurer le logiciel** , exécutez éventuellement les programmes contenus dans le package. Cette étape permet de valider toutes les tâches de configuration ou de licence associées requises pour exécuter l’application avant de déployer et d’exécuter le package sur des ordinateurs cibles. Pour exécuter tous les programmes en même temps, sélectionnez au moins un programme, puis cliquez sur **exécuter tout**. Pour exécuter des programmes spécifiques, sélectionnez le ou les programmes que vous voulez exécuter, puis cliquez sur **exécuter la sélection**. Effectuez les tâches de configuration requises, puis fermez les applications. L’exécution de tous les programmes peut prendre quelques minutes. Cliquez sur **Suivant**.

9.  Dans la page **rapport d’installation** , vous pouvez consulter les informations relatives à l’application virtuelle que vous venez de mettre à jour. Pour obtenir une explication plus détaillée des informations affichées dans **informations supplémentaires**, double-cliquez sur l’événement. Après avoir consulté les informations, cliquez sur **suivant**.

10. Dans la page **personnaliser** , si vous avez terminé l’installation et la configuration de l’application virtuelle, sélectionnez **arrêter maintenant** et passez directement à l’étape 14 de cette procédure. Si vous voulez personnaliser un des éléments de la liste suivante, cliquez sur **personnaliser**.

    -   Modifier les associations de types de fichier associées à une application.

    -   Préparez le package virtuel pour la diffusion en continu. La diffusion en continu améliore son fonctionnement lorsque le package d’application virtuelle est exécuté sur les ordinateurs cibles.

    Cliquez sur **Suivant**.

11. Sur la page **modifier les raccourcis** , vous pouvez éventuellement configurer les associations de types de fichier (FTA) qui seront associées aux différentes applications du package. Pour créer un FTA, sélectionnez et développez l’application que vous voulez personnaliser dans le volet gauche, puis cliquez sur **Ajouter**. Dans la boîte de dialogue **Ajouter une association de type de fichier** , entrez les informations nécessaires pour le nouveau FTA. Pour passer en revue les informations de raccourci associées à une application, sous application, activez la case à cocher **raccourcis** , puis dans le volet **emplacement** , vous pouvez consulter les informations du fichier d’icône. Pour modifier une FTA existante, cliquez sur **modifier**. Pour supprimer un FTA, sélectionnez FTA, puis cliquez sur **supprimer**. Cliquez sur **Suivant**.

12. Sur la page de **diffusion** , exécutez chaque programme de manière à optimiser son exécution et son exécution plus efficacement sur les ordinateurs cibles. L’exécution de toutes les applications peut prendre quelques minutes. Après l’exécution de toutes les applications, fermez chacune d’elles, puis cliquez sur **suivant**.

    **Remarques**  Si vous voulez arrêter le chargement d’une application au cours de cette étape, dans la boîte de dialogue lancement de l' **application** , cliquez sur **arrêter** , puis activez la case à cocher **arrêter toutes les applications** ou **arrêter cette application uniquement** , en fonction de ce que vous voulez faire.

     

13. Dans la page **créer un package** , activez la case à cocher **continuer à modifier le package sans enregistrer à l’aide de l’éditeur de package** pour modifier le package sans l’enregistrer. Lorsque vous sélectionnez cette option, le package de la console de Sequencer s’ouvre pour vous permettre de modifier le package avant son enregistrement. Cliquez sur **Suivant**.

    Sélectionnez l’option **enregistrer le package**par défaut, pour enregistrer immédiatement le package. Ajoutez des **Commentaires** facultatifs qui seront associés au package. Les commentaires sont utiles pour identifier la version et d’autres informations sur le package. L' **emplacement d’enregistrement** par défaut est également affiché. Pour modifier l’emplacement par défaut, cliquez sur **Parcourir** et spécifiez le nouvel emplacement. La taille du package non compressé s’affiche. Si la taille du package dépasse 4 Go (non comprimé) et que vous envisagez de diffuser le package sur les ordinateurs cibles, vous devez sélectionner **compresser le package**. Cliquez sur **Créer**.

14. Sur la page **Fin**, cliquez sur **Fermer**. Le package est désormais disponible dans le Sequencer.

## Rubriques connexes


[Tâches pour Application Virtualization Sequencer (App-V4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





