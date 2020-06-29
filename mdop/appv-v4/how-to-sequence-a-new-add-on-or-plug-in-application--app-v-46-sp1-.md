---
title: Procédure pour séquencer un nouveau module complémentaire ou plug-in (App-V4.6 SP1)
description: Procédure pour séquencer un nouveau module complémentaire ou plug-in (App-V4.6 SP1)
author: dansimp
ms.assetid: 2c018215-66e5-4301-8481-159891a6b35b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5c5bc1e96ead819459cda3879127ebdaf94f0ee7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806814"
---
# Procédure pour séquencer un nouveau module complémentaire ou plug-in (App-V4.6 SP1)


Utilisez la procédure suivante pour créer un nouveau package d’application virtuelle de complément ou plug-in en utilisant le Sequencer Application Virtualization (App-V). Un module complémentaire ou une application enfichable est une application qui étend les fonctionnalités d’une application, par exemple, un plug-in pour Microsoft Excel. Pour plus d’informations sur les types d’applications que vous pouvez séquencer, voir [Comment déterminer le type d’application à séquence (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

**Important**  
Avant d’exécuter la procédure suivante, installez l’application parente localement sur l’ordinateur exécutant le Sequencer. Par exemple, si vous séquençagez un plug-in pour Microsoft Excel, installez Microsoft Excel localement sur l’ordinateur exécutant le Sequencer. Installez également l’application parente dans le même répertoire où l’application est installée sur les ordinateurs cibles. Si le plug-in ou le complément doit être utilisé avec un package d’application virtuelle existant, installez l’application sur le même lecteur d’application virtuel que celui utilisé lors de la création du package d’application virtuelle parent.



Vous pouvez également utiliser un package d’application virtuelle existant en tant qu’application parent. Pour utiliser un package d’application virtuel existant, utilisez la procédure suivante avant de séquencer le nouveau module complémentaire ou plug-in.

1.  Pour démarrer le Sequencer App-v, sur l’ordinateur exécutant le Sequencer App-v, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft Application Virtualization  /  **Sequencer**.

2.  Pour développer un package existant sur l’ordinateur exécutant le Sequencer, cliquez sur **Outils**  /  **développer le package sur le système local**.

3.  Recherchez et sélectionnez le package (fichier **. sprj** ) que vous voulez développer, puis cliquez sur **ouvrir**. Suivez la procédure ci-dessous.

**Pour séquencer une nouvelle application de complément ou d’extension**

1.  Pour démarrer le Sequencer App-v, sur l’ordinateur exécutant le Sequencer App-v, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft Application Virtualization  /  **Sequencer**.

2.  Pour démarrer l' **Assistant Création d’un nouveau package**, cliquez sur **créer un package d’application virtuelle**. Pour créer le package, sélectionnez **créer un package (par défaut)**, puis cliquez sur **suivant**.

3.  Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui peuvent entraîner l’échec de la création du package ou pour le package qui contient des données inutiles. Nous vous recommandons vivement de résoudre tous les problèmes potentiels avant de continuer. Une fois les conflits corrigés, pour mettre à jour les informations affichées, cliquez sur **Actualiser**. Lorsque vous avez résolu tous les problèmes potentiels, cliquez sur **suivant**.

    **Important**  
    Si vous avez besoin de désactiver le logiciel antivirus, analysez l’ordinateur exécutant le Sequencer pour vous assurer qu’aucun fichier non souhaité ou malveillant ne peut être ajouté au package.



4.  Dans la page **type d’application** , sélectionnez **composant additionnel ou plug-in**, puis cliquez sur **suivant**.

    Pour plus d’informations sur les types d’applications que vous pouvez séquencer, voir [Comment déterminer le type d’application à séquence (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

5.  Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de l’extension ou du plug-in. Si l’application n’a pas de fichier d’installation associé et que vous envisagez d’exécuter toutes les étapes d’installation manuellement, activez la case à cocher **activer cette option pour effectuer une installation personnalisée** , puis cliquez sur **suivant**.

6.  Dans la page Sélectionner une page **principale** , cliquez sur **Parcourir** , puis spécifiez l’application parent.

    **Important**  
    Si l’application parente que le module complémentaire ou plug-in que vous installez prend en charge n’est pas installé en local, arrêtez-le et installez l’application sur l’ordinateur exécutant le Sequencer. Par exemple, le fichier programme **Excel.exe** doit être installé en local pour un plug-in Microsoft Excel.



~~~
Click **Next**.
~~~

7. Dans la page **nom du package** , spécifiez un nom qui sera associé au package. Utilisez un nom qui permet d’identifier l’objet et la version de l’application qui sera ajoutée au package. Le nom du package s’affiche également dans la console de gestion des applications. L' **emplacement d’installation** affiche le chemin d’accès de la virtualisation de l’application, qui permet d’installer l’application. Pour modifier cet emplacement, sélectionnez **Modifier (avancé)**.

   **Important**  
   La modification du chemin d’accès de la virtualisation des applications est une tâche de configuration avancée. Vous devez pleinement comprendre les implications du changement de chemin d’accès. Pour la plupart des applications, nous vous recommandons d’utiliser le chemin par défaut.



~~~
Click **Next**.
~~~

8. Dans la page **installation** , lorsque le programme d’installation de Sequencer et d’application est prêt, installez le plug-in ou l’application de complément pour que le Sequencer puisse surveiller le processus d’installation. Procédez à l’installation à l’aide du processus d’installation de l’application. Si des fichiers d’installation supplémentaires doivent être exécutés dans le cadre de l’installation, cliquez sur **exécuter** et recherchez et exécutez les fichiers d’installation supplémentaires. Lorsque l’installation est terminée, sélectionnez J’ai **terminé d’installer**, puis cliquez sur **suivant**.

9. Dans la page **rapport d’installation** , vous pouvez consulter les informations relatives au package d’application virtuel que vous venez de créer. Pour obtenir une explication plus détaillée des informations affichées dans **informations supplémentaires**, double-cliquez sur l’événement. Après avoir consulté les informations, cliquez sur **suivant**.

10. Dans la page **personnaliser** , si vous avez terminé l’installation et la configuration de l’application virtuelle, sélectionnez **arrêter maintenant** et passez directement à l’étape 14 de cette procédure. Si vous voulez personnaliser un des éléments de la liste suivante, sélectionnez **personnaliser**.

    -   Modifier les associations de types de fichier associées à une application.

    -   Préparez le package virtuel pour la diffusion en continu. La diffusion en continu améliore son fonctionnement lorsque le package d’application virtuelle est exécuté sur les ordinateurs cibles.

    -   Spécifiez les systèmes d’exploitation qui peuvent exécuter ce package.

    Cliquez sur **Suivant**.

11. Sur la page **modifier les raccourcis** , vous pouvez éventuellement configurer les associations de types de fichier (FTA) qui seront associées aux différentes applications du package. Pour créer un FTA, dans le volet gauche, sélectionnez et développez l’application que vous voulez personnaliser, puis cliquez sur **Ajouter**. Dans la boîte de dialogue **Ajouter une association de type de fichier** , entrez les informations nécessaires pour le nouveau FTA. Sous l’application, sélectionnez **raccourcis** pour passer en revue les informations de raccourci associées à une application. Dans le volet **emplacement** , vous pouvez consulter les informations du fichier d’icône. Pour modifier une FTA existante, cliquez sur **modifier**. Pour supprimer un FTA, sélectionnez FTA, puis cliquez sur **supprimer**. Cliquez sur **Suivant**.

12. Sur la page de **diffusion** , exécutez chaque programme de manière à optimiser son exécution et son exécution plus efficacement sur les ordinateurs cibles. L’exécution de toutes les applications peut prendre quelques minutes. Après l’exécution de toutes les applications, fermez chacune d’elles, puis cliquez sur **suivant**.

   **Remarque**  
   Si vous voulez arrêter le chargement d’une application au cours de cette étape, dans la boîte de dialogue lancement de l' **application** , cliquez sur **arrêter** et sélectionnez l’une des cases à cocher, **arrêter toutes les applications** ou **arrêter cette application uniquement**.



13. Dans la page **cible du système d’exploitation** , spécifiez les systèmes d’exploitation qui peuvent exécuter ce package. Pour permettre à tous les systèmes d’exploitation pris en charge dans votre environnement d’exécuter ce package, activez la case à cocher **autoriser ce package à s’exécuter sur tous les systèmes d’exploitation** . Pour configurer ce package de sorte qu’il ne s’exécute que sur des systèmes d’exploitation spécifiques, activez la case à cocher **autoriser ce package à s’exécuter uniquement sur les systèmes d’exploitation suivants** , puis sélectionnez les systèmes d’exploitation qui peuvent exécuter ce package. Cliquez sur **Suivant**.

14. Dans la page **créer un package** , pour modifier le package sans l’enregistrer, sélectionnez **continuer pour modifier le package sans l’enregistrer à l’aide de la** case à cocher éditeur de package. La sélection de cette option permet d’ouvrir le package dans la console de Sequencer afin de pouvoir modifier le package avant son enregistrement. Cliquez sur **Suivant**.

   Pour enregistrer le package immédiatement, sélectionnez l’option **enregistrer le package**par défaut. Vous pouvez également sélectionner **Commentaires** pour ajouter des commentaires qui seront associés au package. Les commentaires sont utiles pour identifier la version et d’autres informations sur le package. L' **emplacement d’enregistrement** par défaut est également affiché. Pour modifier l’emplacement par défaut, cliquez sur **Parcourir** et spécifiez le nouvel emplacement. La taille du package non compressé s’affiche. Si la taille du package dépasse 4 Go (non comprimé) et que vous envisagez de diffuser le package sur les ordinateurs cibles, vous devez sélectionner **compresser le package**. Cliquez sur **Créer**.

15. Dans la page d' **achèvement** , une fois que vous avez examiné les informations qui s’affichent dans le volet rapport de création de **package d’application virtuelle réussie** , cliquez sur **Fermer**. Les informations qui s’affichent dans le volet **rapport de package d’application virtuel réussi** sont également disponibles dans l’annuaire indiqué à l’étape 14 de cette procédure, dans un fichier nommé **Reports.xml**.

   Le package est désormais disponible dans le Sequencer. Cliquez sur **modifier \ [nom du package \]** pour modifier les propriétés du package. Pour plus d’informations sur la modification d’un package, voir [Comment modifier un package d’application virtuel existant (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).

   **Important**  
   Une fois que vous avez créé un package d’application virtuelle, vous ne pouvez pas exécuter le package d’application virtuel sur l’ordinateur exécutant le Sequencer.



## Rubriques connexes


[Tâches pour Application Virtualization Sequencer (App-V4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Déterminer le type d’application à séquence (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









