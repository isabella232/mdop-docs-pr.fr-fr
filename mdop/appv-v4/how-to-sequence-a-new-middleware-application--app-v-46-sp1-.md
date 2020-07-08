---
title: Procédure pour séquencer une nouvelle application d'intergiciel (middleware) (App-V4.6SP1)
description: Procédure pour séquencer une nouvelle application d'intergiciel (middleware) (App-V4.6SP1)
author: dansimp
ms.assetid: 304045c2-5e5e-4c91-b59e-a91fdf2500fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b26559b8f5c451d01fefe899e96a83dd388b8140
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806801"
---
# Procédure pour séquencer une nouvelle application d'intergiciel (middleware) (App-V4.6SP1)


Utilisez la procédure suivante pour créer un nouveau package d’application virtuelle du middleware à l’aide du Sequencer Application Virtualization (App-V). Une application middleware est un logiciel qui connecte des modules logiciels ou des applications. Pour plus d’informations sur les types d’applications que vous pouvez séquencer, voir [Comment déterminer le type d’application à séquence (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

Utilisez ce type de package à l’aide de la composition suite dynamique dans App-V. La composition suite dynamique vous permet de définir un package d’application virtuel comme dépendant d’un autre package d’application virtuelle. Cette dépendance permet à l’application d’interagir avec le middleware ou le plug-in dans l’environnement virtuel, en règle générale, cette interaction est empêchée. Cela est utile, car un package d’application secondaire peut être utilisé avec plusieurs autres applications principales, ce qui permet à chaque application principale de référencer le même package secondaire. Pour plus d’informations sur l’utilisation de la composition suite dynamique, voir utilisation de la [composition suite dynamique](https://go.microsoft.com/fwlink/?LinkID=203804&clcid=0x409) dans la bibliothèque technique Microsoft ( https://go.microsoft.com/fwlink/?LinkID=203804&clcid=0x409) .

**Important**  
Lors du séquençage, si l’ordinateur exécutant le Sequencer App-V exécute Windows Vista ou Windows 7 et qu’un redémarrage est lancé en dehors de l’environnement virtuel (par exemple, **Démarrer**  /  l'**arrêt**), vous devez cliquer sur **Annuler** lorsque vous êtes invité à fermer le programme qui empêche Windows de s’arrêter. Si vous cliquez sur **forcer l’arrêt**, la création du package échoue. Lorsque vous cliquez sur **Annuler**, le Sequencer App-V enregistre correctement le redémarrage lorsque l’application est en cours de séquence.



**Pour séquencer une nouvelle application middleware**

1.  Pour démarrer le Sequencer App-v, sur l’ordinateur exécutant le Sequencer App-v, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft Application Virtualization  /  **Sequencer**.

2.  Pour démarrer l' **Assistant Création d’un nouveau package**, cliquez sur **créer un package d’application virtuelle**. Pour créer le package, sélectionnez **créer un package (par défaut)**, puis cliquez sur **suivant**.

3.  Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui peuvent entraîner l’échec de la création du package ou pour le package qui contient des données inutiles. Nous vous recommandons vivement de résoudre tous les problèmes potentiels avant de continuer. Une fois les conflits corrigés, pour mettre à jour les informations affichées, cliquez sur **Actualiser**. Lorsque vous avez résolu tous les problèmes potentiels, cliquez sur **suivant**.

    **Important**  
    Si vous êtes tenu de désactiver le logiciel antivirus, vous devez analyser l’ordinateur exécutant l’application-VSequencer pour vous assurer qu’aucun fichier non souhaité ou malveillant ne peut être ajouté au package.



4.  Dans la page **type d’application** , sélectionnez **middleware**, puis cliquez sur **suivant**.

    Pour plus d’informations sur les types d’applications que vous pouvez séquencer, voir [Comment déterminer le type d’application à séquence (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

5.  Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de l’application. Si l’application n’a pas de fichier d’installation associé et que vous envisagez d’exécuter toutes les étapes d’installation manuellement, activez la case à cocher **activer cette option pour effectuer une installation personnalisée** , puis cliquez sur **suivant**.

6.  Dans la page **nom du package** , spécifiez un nom qui sera associé au package. Le nom vous permet d’identifier l’objet et la version de l’application qui sera ajoutée au package. Le nom du package s’affiche également dans la console de gestion App-V. L' **emplacement d’installation** affiche le chemin d’accès de la virtualisation de l’application, qui permet d’installer l’application. Pour modifier cet emplacement, sélectionnez **Modifier (avancé)**.

    **Important**  
    La modification du chemin d’accès de la virtualisation des applications est une tâche de configuration avancée. Vous devez pleinement comprendre les implications du changement de chemin d’accès. Pour la plupart des applications, nous vous recommandons d’utiliser le chemin par défaut.



~~~
Click **Next**.
~~~

7. Dans la page **installation** , lorsque le programme d’installation de Sequencer et de l’application middleware est prêt, installez l’application afin que le Sequencer puisse surveiller le processus d’installation. Procédez à l’installation à l’aide du processus d’installation de l’application. Si des fichiers d’installation supplémentaires doivent être exécutés dans le cadre de l’installation, cliquez sur **exécuter**pour rechercher et exécuter les fichiers d’installation supplémentaires. Lorsque l’installation est terminée, activez la case à cocher **je suis fin** de l’installation, puis cliquez sur **suivant**.

8. Dans la page **installation** , attendez que le Sequencer configure le package d’application virtuelle.

9. Dans la page **rapport d’installation** , vous pouvez consulter les informations relatives au package d’application virtuel que vous venez de créer. Pour obtenir une explication plus détaillée des informations affichées dans **informations supplémentaires**, double-cliquez sur l’événement. Après avoir consulté les informations, cliquez sur **suivant**.

10. Dans la page **cible du système d’exploitation** , spécifiez les systèmes d’exploitation qui peuvent exécuter ce package. Pour permettre à tous les systèmes d’exploitation pris en charge dans votre environnement d’exécuter ce package, activez la case à cocher **autoriser ce package à s’exécuter sur tous les systèmes d’exploitation** . Pour configurer ce package de sorte qu’il ne s’exécute que sur des systèmes d’exploitation spécifiques, activez la case à cocher **autoriser ce package à s’exécuter uniquement sur les systèmes d’exploitation suivants** et sélectionnez les systèmes d’exploitation qui peuvent exécuter ce package. Cliquez sur **Suivant**.

11. Dans la page **créer un package** , pour modifier le package sans l’enregistrer, activez la case à cocher **continuer à modifier le package sans enregistrer à l’aide de l’éditeur de package** . La sélection de cette option permet d’ouvrir le package dans la console de Sequencer afin de pouvoir modifier le package avant son enregistrement. Cliquez sur **Suivant**.

   Pour enregistrer le package immédiatement, sélectionnez la case à cocher **enregistrer le package maintenant** . Ajoutez des commentaires facultatifs dans la zone de **Commentaires** qui sera associée au package. Les commentaires sont utiles pour identifier la version et d’autres informations sur le package. L' **emplacement d’enregistrement** par défaut est également affiché. Pour modifier l’emplacement par défaut, cliquez sur **Parcourir**, puis spécifiez le nouvel emplacement. La taille du package non compressé s’affiche. Si la taille du package dépasse 4 Go (non comprimé) et que vous envisagez de diffuser le package sur les ordinateurs cibles, vous devez sélectionner **compresser le package**. Cliquez sur **Créer**.

12. Dans la page **dernière étape** , après avoir consulté les informations affichées dans le volet **rapport de package d’application virtuel** , cliquez sur **Fermer**. Les informations qui s’affichent dans le volet **rapport de package d’application virtuel** sont également disponibles dans l’annuaire indiqué à l’étape 11 de cette procédure, dans un fichier nommé **Report.xml**.

   Le package est désormais disponible dans le Sequencer. Pour modifier les propriétés du package, cliquez sur **modifier \ [nom du package \]**. Pour plus d’informations sur la modification d’un package, voir [Comment modifier un package d’application virtuel existant (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md)

   **Important**  
   Une fois que vous avez créé un package d’application virtuelle, vous ne pouvez pas exécuter le package d’application virtuel sur l’ordinateur exécutant le Sequencer.



## Rubriques connexes


[Tâches pour Application Virtualization Sequencer (App-V4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Déterminer le type d’application à séquence (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









