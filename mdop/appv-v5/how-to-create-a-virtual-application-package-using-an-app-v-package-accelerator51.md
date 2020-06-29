---
title: Comment créer un package d'application virtuelle à l'aide d'un accélérateur de package App-V
description: Comment créer un package d'application virtuelle à l'aide d'un accélérateur de package App-V
author: dansimp
ms.assetid: eae1e4f8-f14f-4bc8-9867-052561c37297
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15376ae52a19b2d220f9ea0031f3ad5649ca487d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805604"
---
# Comment créer un package d'application virtuelle à l'aide d'un accélérateur de package App-V


**Important**  
Le Sequencer App-V 5,1 n’accorde aucun droit de licence à l’application logicielle utilisée pour créer l’accélérateur de package. Vous devez vous conformer aux termes du contrat de licence utilisateur final de l’application que vous utilisez. Il est de votre responsabilité de veiller à ce que les termes du contrat de licence de l’application logicielle vous permettent de créer un accélérateur de package avec le Sequencer App-V 5,1.



Utilisez la procédure suivante pour créer un package d’application virtuelle avec l’accélérateur de package App-V 5,1.

**Remarque**  
Avant de commencer cette procédure, copiez l’accélérateur de package requis localement vers l’ordinateur qui exécute le Sequencer App-V 5,1. Vous devez également copier tous les fichiers d’installation requis pour le package dans un répertoire local de l’ordinateur qui exécute le Sequencer. Il s’agit de l’annuaire que vous devez spécifier à l’étape 5 de cette procédure.



**Pour créer un package d’application virtuelle avec un accélérateur de package App-V 5,1**

1.  Pour démarrer le Sequencer App-v, sur l’ordinateur qui exécute le Sequencer App-v 5,1, cliquez sur **Démarrer**  /  **tous les programmes**  /  **Microsoft Application Virtualization**Microsoft  /  **Application Virtualization Sequencer**.

2.  Pour démarrer l' **Assistant Création d’un nouveau package**, cliquez sur **créer un package d’application virtuelle**. Pour créer le package, activez la case à cocher **créer un package à l’aide d’un accélérateur de package** , puis cliquez sur **suivant**.

3.  Pour spécifier l’accélérateur de package qui sera utilisé pour créer le package d’application virtuelle, cliquez sur **Parcourir** dans la page **Sélectionner un accélérateur de package** . Cliquez sur **Suivant**.

    **Important**  
    Si l’éditeur de package Accelerator ne peut pas être vérifié et ne contient pas de signature numérique valide, avant de cliquer sur **Run (exécuter**), vous devez confirmer que vous faites confiance à la source de l’accélérateur de package. Confirmez votre choix dans la boîte de dialogue **avertissement de sécurité** .



4.  Dans la page **recommandations** , passez en revue les informations d’aide sur la publication qui s’affichent dans le volet d’informations. Ces informations ont été ajoutées lors de la création de l’accélérateur de package et contiennent des recommandations sur la création et la publication du package. Pour exporter les informations d’aide dans un fichier texte (. txt), cliquez sur **Exporter** , puis spécifiez l’emplacement d’enregistrement du fichier, puis cliquez sur **suivant**.

5.  Dans la page **Sélectionner des fichiers d’installation** , cliquez sur **créer** un dossier pour créer un dossier local qui contient tous les fichiers d’installation requis pour le package, puis spécifiez l’emplacement d’enregistrement du dossier. Vous devez également spécifier un nom à attribuer au dossier. Vous devez alors copier tous les fichiers d’installation requis dans l’emplacement que vous avez spécifié. Si le dossier contenant les fichiers d’installation existe déjà sur l’ordinateur qui exécute le Sequencer, cliquez sur **Parcourir** pour sélectionner le dossier.

    Par ailleurs, si vous avez déjà copié les fichiers d’installation dans un répertoire de cet ordinateur, cliquez sur **créer un nouveau dossier**, recherchez le dossier contenant les fichiers d’installation, puis cliquez sur **suivant**.

    **Remarque**  
    Vous pouvez spécifier les types de fichiers d’installation pris en charge suivants:

    -   Fichiers Windows Installer (**. msi**)

    -   Fichiers CAB (. cab)

    -   Fichiers compressés avec une extension de nom de fichier. zip

    -   Fichiers d’application réels

    Les types de fichiers suivants ne sont pas pris en charge: fichiers **. msp** et **. exe** . Si vous spécifiez un fichier **. exe** , vous devez extraire les fichiers d’installation manuellement.



~~~
If the package accelerator requires an application to be installed before you apply the Package Accelerator, and if you have already installed the required application, select **I have installed all applications**, and then click **Next** on the **Local Installation** page.
~~~

6. Dans la page **nom du package** , spécifiez un nom qui sera associé au package. Le nom que vous spécifiez identifie le package dans la console de gestion App-V. Cliquez sur **Suivant**.

7. Dans la page **créer un package** , indiquez les commentaires qui seront associés au package. Les commentaires doivent contenir des informations d’identification sur le package que vous êtes en train de créer. Pour confirmer l’emplacement de création du package, passez en revue les informations qui s’affichent à l' **emplacement d’enregistrement**. Pour compresser le package, sélectionnez **compresser un package**. Activez la case à cocher **compresser le package** si le package est diffusé sur le réseau, ou lorsque la taille du package dépasse 4 Go.

   Pour créer le package, cliquez sur **créer**. Une fois le package créé, cliquez sur **suivant**.

8. Dans la page **configure Software** , pour permettre au Sequencer de configurer les applications contenues dans le package, sélectionnez **configure Software**. Au cours de cette étape, vous pouvez configurer les tâches associées qui doivent être achevées pour pouvoir exécuter l’application sur les ordinateurs cibles. Par exemple, vous pouvez configurer n’importe quel contrat de licence associé.

   Si vous sélectionnez **configurer le logiciel**, les éléments suivants peuvent être configurés avec le Sequencer dans le cadre de cette étape:

   -   **Chargez le package**. Le Sequencer charge les fichiers associés au package. Le décodage du package peut prendre quelques secondes à une heure.

   -   **Exécutez chaque programme**. Vous pouvez également exécuter les programmes contenus dans le package. Cette étape est utile pour effectuer toutes les tâches de configuration ou de licence associées requises pour exécuter l’application avant de déployer et d’exécuter le package sur des ordinateurs cibles. Pour exécuter tous les programmes en une seule fois, sélectionnez au moins un programme, puis cliquez sur **exécuter tout**. Pour exécuter des programmes spécifiques, sélectionnez le ou les programmes que vous souhaitez exécuter, puis cliquez sur **exécuter la sélection**. Effectuez les tâches de configuration requises, puis fermez les applications. L’exécution de tous les programmes peut prendre quelques minutes. Cliquez sur **Suivant**.

   -   **Enregistrer un package**. Le Sequencer enregistre le package.

   -   **Bloc de fonctionnalités principal**. Le Sequencer optimise le package de diffusion en reconstruisant le bloc de fonctionnalité principal.

   Si vous ne voulez pas configurer les applications, cliquez sur **ignorer cette étape**, et pour passer à l’étape 9 de cette procédure, puis cliquez sur **suivant**.

9. Dans la page **dernière étape** , après avoir examiné les informations affichées dans le volet **rapport de package d’application virtuel** , cliquez sur **Fermer**.

   Le package est désormais disponible dans le Sequencer. Pour modifier les propriétés du package, cliquez sur **modifier \ [nom du package \]**. Pour plus d’informations sur la modification d’un package, voir [Comment modifier un package d’application virtuel existant](how-to-modify-an-existing-virtual-application-package-beta.md).

   Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.1](operations-for-app-v-51.md)









