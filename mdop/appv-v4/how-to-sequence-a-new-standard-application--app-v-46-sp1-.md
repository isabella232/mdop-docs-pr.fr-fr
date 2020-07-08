---
title: Procédure pour séquencer une nouvelle application standard (App-V4.6SP1
description: Procédure pour séquencer une nouvelle application standard (App-V4.6SP1
author: dansimp
ms.assetid: c4a2eb33-def8-4535-b93a-3d2de21ce29f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 47c93b4880d0095c87a98292fda743acc1659e81
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806797"
---
# Procédure pour séquencer une nouvelle application standard (App-V4.6SP1


Utilisez la procédure suivante pour créer un nouveau package d’application virtuelle standard à l’aide du séquenceur Application Virtualization (App-V). Cette procédure s’applique à la plupart des applications que vous séquencez. Pour plus d’informations sur les types d’applications que vous pouvez séquencer, voir [Comment déterminer le type d’application à séquence (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md). Vous devez exécuter le Sequencer (**SFTSequencer.exe**) à l’aide d’un compte qui dispose de privilèges d’administrateur en raison des changements apportés par le Sequencer au système local. Ces modifications peuvent inclure l’écriture de fichiers dans le répertoire **C:\\Program Files** , l’apport de modifications du Registre, le démarrage et l’arrêt de services, la mise à jour des descripteurs de sécurité pour les fichiers et la modification des autorisations.

**Important**  
Lors du séquençage, si l’ordinateur exécutant le Sequencer exécute Windows Vista ou Windows 7 et qu’un redémarrage est lancé hors de l’environnement virtuel (par exemple, **Démarrer**l'  /  **arrêt**, vous devez cliquer sur **Annuler** lorsque vous êtes invité à fermer le programme qui empêche Windows Vista ou Windows d’arrêter). Si vous cliquez sur **forcer l’arrêt**, la création du package échoue. Lorsque vous cliquez sur **Annuler**, le Sequencer enregistre correctement le redémarrage lorsque l’application est en cours de séquence.



**Remarque**  
L’exécution du Sequencer App-V en mode sans échec n’est pas prise en charge.



**Pour séquencer une nouvelle application standard**

1.  Pour démarrer le Sequencer App-v, sur l’ordinateur exécutant le Sequencer App-v, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft Application Virtualization  /  **Sequencer**.

2.  Pour démarrer l' **Assistant Création d’un nouveau package**, cliquez sur **créer un package d’application virtuelle**. Pour créer le package, sélectionnez **créer un package (par défaut)**, puis cliquez sur **suivant**.

3.  Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui pourraient entraîner l’échec de la création du package ou pour le package qui contient des données inutiles. Nous vous recommandons vivement de résoudre tous les problèmes potentiels avant de continuer. Une fois les conflits corrigés, cliquez sur **Actualiser**pour mettre à jour les informations affichées. Lorsque vous avez résolu tous les problèmes potentiels, cliquez sur **suivant**.

    **Important**  
    Si vous avez besoin de désactiver le logiciel antivirus, analysez l’ordinateur exécutant le Sequencer pour vous assurer qu’aucun fichier non souhaité ou malveillant ne peut être ajouté au package.



4.  Dans la page **type d’application** , activez la case à cocher **application standard (par défaut)** , puis cliquez sur **suivant**.

    Pour plus d’informations sur les types d’applications que vous pouvez séquencer, voir [Comment déterminer le type d’application à séquence (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md).

5.  Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de l’application. Si l’application n’a pas de fichier de programme d’installation associé et que vous envisagez d’exécuter toutes les étapes d’installation manuellement, activez la case à cocher **effectuer une installation personnalisée** , puis cliquez sur **suivant**.

6.  Dans la page **nom du package** , spécifiez un nom qui sera associé au package. Ce nom permet d’identifier l’objet et la version de l’application qui sont ajoutés au package. Le nom du package s’affiche également dans la console de gestion App-V. Le **répertoire principal de l’application virtuelle** affiche le chemin d’accès de la virtualisation d’application sur lequel l’application sera installée sur les ordinateurs cibles. Pour modifier cet emplacement, sélectionnez **Modifier (avancé)**.

    **Important**  
    La modification du chemin d’accès de la virtualisation des applications est une tâche de configuration avancée. Vous devez pleinement comprendre les implications du changement de chemin d’accès. Pour la plupart des applications, le chemin d’accès par défaut est recommandé.



~~~
Click **Next**.
~~~

7. Dans la page **installation** , lorsque le programme d’installation de Sequencer et d’application est prêt, installez l’application afin que le Sequencer puisse surveiller le processus d’installation. Procédez à l’installation à l’aide du processus d’installation de l’application. Si des fichiers d’installation supplémentaires doivent être exécutés dans le cadre de l’installation, cliquez sur **exécuter** pour rechercher et exécuter les fichiers d’installation supplémentaires. Lorsque l’installation est terminée, sélectionnez J’ai **terminé d’installer**. Cliquez sur **Suivant**.

8. Dans la page **installation** , attendez que le Sequencer configure le package d’application virtuelle.

9. Sur la page **configurer le logiciel** , exécutez éventuellement les programmes contenus dans le package. Cette étape permet de valider toutes les tâches de configuration ou de licence associées requises pour exécuter l’application avant de déployer et d’exécuter le package sur des ordinateurs cibles. Pour exécuter tous les programmes en une seule fois, sélectionnez au moins un programme, puis cliquez sur **exécuter tout**. Pour exécuter des programmes spécifiques, sélectionnez le ou les programmes que vous voulez exécuter, puis cliquez sur **exécuter la sélection**. Effectuez les tâches de configuration requises, puis fermez les applications. L’exécution de tous les programmes peut prendre quelques minutes. Cliquez sur **Suivant**.

10. Dans la page **rapport d’installation** , vous pouvez consulter les informations relatives au package d’application virtuel que vous venez de créer. Pour obtenir une explication plus détaillée des informations affichées dans **informations supplémentaires**, double-cliquez sur l’événement. Après avoir consulté les informations, cliquez sur **suivant**.

11. Dans la page **personnaliser** , si vous avez terminé l’installation et la configuration de l’application virtuelle, sélectionnez **arrêter maintenant** et passez directement à l’étape 15 de cette procédure. Si vous voulez personnaliser un des éléments de la liste suivante, sélectionnez **personnaliser**.

    -   Modifiez les associations de types de fichiers et les icônes associées à une application.

    -   Préparez le package virtuel pour la diffusion en continu. La diffusion en continu améliore son fonctionnement lorsque le package d’application virtuelle est exécuté sur les ordinateurs cibles.

    -   Spécifiez les systèmes d’exploitation qui peuvent exécuter ce package.

    Cliquez sur **Suivant**.

12. Sur la page **modifier les raccourcis** , vous pouvez éventuellement configurer les types de fichiers (FTA) et les emplacements de raccourci qui seront associés aux différentes applications du package. Pour créer un FTA, dans le volet gauche, sélectionnez et développez l’application que vous voulez personnaliser, puis cliquez sur **Ajouter**. Dans la boîte de dialogue **Ajouter une association de type de fichier** , entrez les informations nécessaires pour le nouveau FTA. Pour passer en revue les informations de raccourci associées à une application, dans l’application, sélectionnez **raccourcis**, puis, dans le volet **emplacement** , vous pouvez modifier les informations du fichier d’icône. Pour modifier une FTA existante, cliquez sur **modifier**. Pour supprimer un FTA, sélectionnez FTA, puis cliquez sur **supprimer**. Cliquez sur **Suivant**.

13. Sur la page de **diffusion** , exécutez chaque programme de manière à optimiser son exécution et son exécution plus efficacement sur les ordinateurs cibles. L’exécution de toutes les applications peut prendre quelques minutes. Après l’exécution de toutes les applications, fermez chacune d’elles, puis cliquez sur **suivant**.

   **Remarque**  
   Si vous voulez arrêter le chargement d’une application au cours de cette étape, dans la boîte de dialogue lancement de l' **application** , cliquez sur **arrêter**, puis sélectionnez l’une des cases à cocher, **arrêter toutes les applications** ou **arrêter cette application uniquement**, en fonction de ce que vous voulez faire.



14. Dans la page **cible du système d’exploitation** , spécifiez les systèmes d’exploitation qui peuvent exécuter ce package. Pour permettre à tous les systèmes d’exploitation pris en charge dans votre environnement d’exécuter ce package, sélectionnez **permettre l’exécution de ce package sur tout système d’exploitation**. Pour configurer ce package de sorte qu’il ne s’exécute que sur des systèmes d’exploitation spécifiques, sélectionnez **autoriser ce package à s’exécuter uniquement sur les systèmes d’exploitation suivants** et spécifiez les systèmes d’exploitation qui peuvent exécuter ce package. Cliquez sur **Suivant**.

   **Important**  
   Les systèmes d’exploitation spécifiés au cours de cette étape reflètent les systèmes d’exploitation sur les ordinateurs cibles activés pour exécuter le package. Vous devez vous assurer que les systèmes d’exploitation spécifiés sont pris en charge par l’application que vous séquençage.



15. Dans la page **créer un package** , pour modifier le package sans l’enregistrer, sélectionnez **continuer pour modifier le package sans l’enregistrer à l’aide de l’éditeur de package**. La sélection de cette option permet d’ouvrir le package dans la console de Sequencer afin de pouvoir modifier le package avant son enregistrement. Cliquez sur **Suivant**.

   Pour enregistrer le package immédiatement, sélectionnez l’option **enregistrer le package**par défaut. Ajoutez des **Commentaires** facultatifs qui seront associés au package. Les commentaires sont utiles pour identifier la version et d’autres informations sur le package. L' **emplacement d’enregistrement** par défaut est également affiché. Pour modifier l’emplacement par défaut, cliquez sur **Parcourir** et spécifiez le nouvel emplacement. La taille du package non compressé s’affiche. Si la taille du package dépasse 4 Go (non comprimé) et que vous envisagez de diffuser le package sur les ordinateurs cibles, vous devez sélectionner **compresser le package**. Cliquez sur **Créer**.

16. Dans la page **dernière étape** , après avoir consulté les informations affichées dans le volet **rapport de package d’application virtuel** , cliquez sur **Fermer**. Les informations qui s’affichent dans le volet **rapport de package d’application virtuel** sont également disponibles dans l’annuaire indiqué à l’étape 15 de cette procédure, dans un fichier nommé **Report.xml**.

    Le package est désormais disponible dans le Sequencer. Pour modifier les propriétés du package, cliquez sur **modifier \ [nom du package \]**. Pour plus d’informations sur la modification d’un package, voir [Comment modifier un package d’application virtuel existant (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md)

    **Important**  
    Une fois que vous avez créé un package d’application virtuelle, vous ne pouvez pas exécuter le package d’application virtuel sur l’ordinateur exécutant le Sequencer.



## Rubriques connexes


[Tâches pour Application Virtualization Sequencer (App-V4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Déterminer le type d’application à séquence (App-V 4,6 SP1)](how-to-determine-which-type-of-application-to-sequence---app-v-46-sp1-.md)









