---
title: Comment appliquer un accélérateur de package pour créer un package d’application virtuelle (App-V 4,6 SP1)
description: Comment appliquer un accélérateur de package pour créer un package d’application virtuelle (App-V 4,6 SP1)
author: dansimp
ms.assetid: ca0bd514-2bbf-4130-8c77-98d991cbe016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce6960fb95cce7f5e0eeb111412f27f945b0c1a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808723"
---
# Comment appliquer un accélérateur de package pour créer un package d’application virtuelle (App-V 4,6 SP1)


Vous pouvez utiliser les accélérateurs de package App-V pour générer automatiquement un nouveau package d’application virtuel. Pour plus d’informations sur les accélérateurs de package, voir [à propos des accélérateurs de package App-v (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).

**Important**  
Exclusion de responsabilité: le Sequencer de la virtualisation de l’application ne vous donne aucun droit de licence pour l’application logicielle que vous utilisez pour créer un accélérateur de package. Vous devez respecter les conditions générales du contrat de licence utilisateur final pour une telle application. Il est de votre responsabilité de veiller à ce que les termes du contrat de licence de l’application logicielle vous permettent de créer un accélérateur de package à l’aide du Sequencer de la virtualisation de l’application.



**Remarque**  
Avant de commencer cette procédure, copiez l’accélérateur de package requis localement vers l’ordinateur exécutant le Sequencer App-V. Vous devez également copier tous les fichiers d’installation requis pour le package dans un répertoire local sur l’ordinateur exécutant le Sequencer. Il s’agit de l’annuaire que vous devez spécifier à l’étape 5 de cette procédure.



Utilisez la procédure suivante pour créer un package d’application virtuelle à l’aide d’un accélérateur de package.

**Pour créer un package d’application virtuelle à l’aide d’un accélérateur de package App-V**

1. Pour démarrer le Sequencer App-v, sur l’ordinateur exécutant le Sequencer App-v, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft Application Virtualization  /  **Sequencer**.

2. Pour démarrer l' **Assistant Création d’un nouveau package**, cliquez sur **créer un package d’application virtuelle**. Pour créer le package, activez la case à cocher **créer un package à l’aide d’un accélérateur de package** , puis cliquez sur **suivant**.

3. Dans la page **Sélectionner l’accélérateur de package** , pour spécifier l’accélérateur de package à utiliser pour créer le package d’application virtuelle, cliquez sur **Parcourir** pour Rechercher l’accélérateur de package que vous voulez utiliser. Cliquez sur **Suivant**.

   **Important**  
   Si l’éditeur de package Accelerator ne peut pas être vérifié et ne contient pas de signature numérique valide, dans la boîte de dialogue **avertissement de sécurité** , vous devez confirmer que vous faites confiance à la source de l’accélérateur de package avant de cliquer sur **exécuter**.



4. Dans la page **recommandations** , passez en revue les informations d’instructions de publication affichées dans le volet d’informations. Les informations affichées étaient ajoutées lors de la création de l’accélérateur de package et contiennent des informations sur la création et la publication du package. Pour exporter les informations d’aide dans un fichier texte (. txt), cliquez sur **Exporter** , puis spécifiez l’emplacement d’enregistrement du fichier, puis cliquez sur **suivant**.

5. Dans la page **Sélectionner des fichiers d’installation** , pour créer un dossier local qui contient tous les fichiers d’installation requis pour le package, cliquez sur créer un **dossier** , puis spécifiez l’emplacement d’enregistrement du dossier. Vous devez également spécifier un nom à attribuer au dossier. Vous devez alors copier tous les fichiers d’installation requis dans l’emplacement que vous avez spécifié. Si le dossier contenant les fichiers d’installation existe déjà sur l’ordinateur exécutant le Sequencer, cliquez sur **Parcourir** pour sélectionner le dossier.

   Par ailleurs, si vous avez déjà copié les fichiers d’installation dans un répertoire de cet ordinateur, cliquez sur **créer un nouveau dossier**, recherchez le dossier contenant les fichiers d’installation, puis cliquez sur **suivant**.

   **Remarque**  
   Vous pouvez spécifier les types de fichiers d’installation pris en charge suivants:

   -   Fichiers du programme d’installation Windows (**. msi**

   -   fichiers. cab

   -   Fichiers compressés avec une extension de nom de fichier. zip

   -   Fichiers d’application réels

   Les types de fichiers suivants ne sont pas pris en charge: fichiers **. msp** et <strong> . exe </strong> . Si vous spécifiez un fichier **. exe** , vous devez extraire les fichiers d’installation manuellement.



~~~
If the Package Accelerator requires an application be installed prior to applying the Package Accelerator and you have installed the application, on the **Local Installation** page, select the check box **I have installed all applications**, and then click **Next**.
~~~

6. Dans la page **nom du package** , spécifiez un nom qui sera associé au package. Le nom indiqué identifie le package dans la console de gestion de l’application-V. Cliquez sur **Suivant**.

7. Dans la page **créer un package** , indiquez les commentaires qui seront associés au package. Les commentaires doivent contenir des informations d’identification sur le package que vous créez. Pour confirmer l’emplacement de création du package, passez en revue les informations affichées dans la **zone enregistrement**. Pour compresser le package, sélectionnez **compresser un package**. Activez la case à cocher **compresser le package** si le package est diffusé sur le réseau, ou lorsque la taille du package dépasse 4 Go.

   Pour créer le package, cliquez sur **créer**. Lorsque le package a été créé, cliquez sur **suivant**.

8. Dans la page **configure Software** , pour permettre au Sequencer de configurer les applications contenues dans le package, sélectionnez **configure Software**. Cette étape est utile pour la configuration des tâches associées qui doivent être achevées pour exécuter l’application sur des ordinateurs cibles, par exemple pour configurer tous les contrats de licence associés.

   Si vous sélectionnez **configurer le logiciel**, les éléments suivants sont configurés par le Sequencer dans le cadre de cette étape:

   -   **Chargez le package**. Le Sequencer charge les fichiers associés au package. Le décodage du package peut prendre quelques secondes à une heure.

   -   **Exécutez chaque programme**. Vous pouvez également exécuter les programmes contenus dans le package. Cette étape est utile pour effectuer toutes les tâches de configuration ou de licence associées requises pour exécuter l’application avant de déployer et d’exécuter le package sur des ordinateurs cibles. Pour exécuter tous les programmes en une seule fois, sélectionnez au moins un programme, puis cliquez sur **exécuter tout**. Pour exécuter des programmes spécifiques, sélectionnez le ou les programmes que vous voulez exécuter, puis cliquez sur **exécuter la sélection**. Effectuez les tâches de configuration requises, puis fermez les applications. L’exécution de tous les programmes peut prendre quelques minutes. Cliquez sur **Suivant**.

   -   **Enregistrer un package**. Le Sequencer enregistre le package.

   -   **Bloc de fonctionnalités principal**. Le Sequencer optimise le package de diffusion en reconstruisant le bloc de fonctionnalité principal.

   Si vous ne voulez pas configurer les applications, cliquez sur **ignorer cette étape**, et pour passer à l’étape 9 de cette procédure, puis cliquez sur **suivant**.

9. Dans la page **dernière étape** , après avoir consulté les informations affichées dans le volet **rapport de package d’application virtuel** , cliquez sur **Fermer**.

   Le package est désormais disponible dans le Sequencer. Pour modifier les propriétés du package, cliquez sur **modifier \ [nom du package \]**. Pour plus d’informations sur la modification d’un package, voir [Comment modifier un package d’application virtuel existant (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).

## Rubriques connexes


[Configuration d'Application Virtualization Sequencer (App-V4.6 SP1)](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Procédure pour créer des accélérateurs de package App-V (App-V4.6SP1)](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)









