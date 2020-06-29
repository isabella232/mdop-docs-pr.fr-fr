---
title: Comment modifier un package d'application virtuelle existant
description: Comment modifier un package d'application virtuelle existant
author: dansimp
ms.assetid: 6cdeec00-e4fe-4210-b4c7-6ca1ac643ddd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 95963610c8b725412f6d516ee22b1c2f4e186df6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805298"
---
# Comment modifier un package d'application virtuelle existant


Cette rubrique explique comment effectuer les opérations suivantes:

-   [Mettre à jour une application dans un package d’application virtuel existant](#bkmk-update-app-in-pkg)

-   [Modifier les propriétés associées à un package d’application virtuelle existant](#bkmk-chg-props-in-pkg)

-   [Ajouter une nouvelle application à un package d’application virtuelle existant](#bkmk-add-app-to-pkg)

**Avant de mettre à jour un package:**

-   Vérifiez que vous avez installé le Sequencer Microsoft Application Virtualization (App-V), requis pour la modification d’un package d’application virtuel. Pour installer le Sequencer App-V, voir [Comment installer le Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).

-   Enregistrez le fichier. AppV dans un emplacement sécurisé et faites toujours confiance à la source avant d’essayer d’ouvrir le package à des fins de modification.

-   La section gestion des autorités est supprimée par erreur du fichier de configuration de déploiement lors de la mise à jour d’un package. Avant de démarrer la mise à jour, copiez la section autorité de gestion à partir du fichier de configuration de déploiement existant, puis collez la section copiée dans le nouveau fichier de configuration une fois la conversion terminée.

-   Si vous cliquez sur **modifier un package d’application virtuel existant** dans le Sequencer pour modifier un package, mais que vous n’effectuez aucune modification et que vous fermez le package, le comportement de diffusion du package est modifié. Le bloc de fonctionnalité principal est supprimé du fichier StreamMap.xml, et tous les fichiers qui ont été répertoriés dans le bloc de fonctionnalité de publication ont été supprimés. Les utilisateurs qui reçoivent l’interface de package modifiée dont le package est défectueux, quelle que soit la façon dont le package d’origine a été configuré.

<a href="" id="bkmk-update-app-in-pkg"></a>**Mettre à jour une application dans un package d’application virtuel existant**

1.  Sur l’ordinateur qui exécute le Sequencer, cliquez sur **tous les programmes**, pointez sur **virtualisation des applications**, puis cliquez sur **Sequencer Microsoft Application Virtualization**.

2.  Dans le Sequencer App-V, cliquez sur **modifier un package d’application virtuel existant** &gt; **Next**.

3.  Dans la page **Sélectionner une tâche** , cliquez sur **mettre à jour l’application dans le package existant** &gt; **Next**.

4.  Dans la page **Sélectionner un package** , cliquez sur **Parcourir** pour rechercher le package d’application virtuel qui contient l’application à mettre à jour, puis cliquez sur **suivant**.

5.  Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui pourraient entraîner l’échec de la mise à jour de l’application, ou le fait que l’application mise à jour contient des données inutiles. Résolvez tous les problèmes potentiels avant de continuer. Après avoir effectué des corrections et résolu les problèmes potentiels, cliquez sur **Actualiser** &gt; **suivant**.

    **Important**  Si vous êtes tenu de désactiver le logiciel antivirus, analysez d’abord l’ordinateur qui exécute le Sequencer pour vérifier qu’aucun fichier non souhaité ou malveillant n’est ajouté au package.

6.  Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de la mise à jour de l’application. Si la mise à jour n’a pas de fichier de programme d’installation associé et si vous envisagez d’exécuter toutes les étapes d’installation manuellement, activez la case à cocher **activer cette option pour effectuer une installation personnalisée** , puis cliquez sur **suivant**.

7.  Dans la page **installation** , lorsque le programme de séquence et d’installation de l’application est prêt, vous pouvez continuer à installer la mise à jour de l’application afin que le Sequencer puisse surveiller le processus d’installation. Si des fichiers d’installation supplémentaires doivent être exécutés dans le cadre de l’installation, cliquez sur **exécuter**, puis recherchez et exécutez les fichiers d’installation supplémentaires. Lorsque l’installation est terminée, sélectionnez J’ai **terminé d’installer**. Cliquez sur **Suivant**.

    **Remarques**  Le Sequencer contrôle toutes les modifications et les installations qui se produisent sur l’ordinateur qui exécute le Sequencer. Cela inclut les modifications et installations effectuées en dehors de l’Assistant séquençage.

8.  Dans la page **rapport d’installation** , vous pouvez consulter des informations sur l’application virtuelle mise à jour. Dans **informations supplémentaires**, double-cliquez sur l’événement pour obtenir des informations plus détaillées. Pour continuer, cliquez sur **suivant**.

9.  Sur la page de **diffusion** , exécutez chaque programme de manière à optimiser son exécution et son exécution plus efficacement sur les ordinateurs cibles. L’exécution de toutes les applications peut prendre quelques minutes. Après l’exécution de toutes les applications, fermez chacune d’elles, puis cliquez sur **suivant**.

    **Remarques**  Vous pouvez empêcher le chargement d’une application au cours de cette étape. Dans la boîte de dialogue lancement de l' **application** , cliquez sur **arrêter**, puis sélectionnez **arrêter toutes les applications** ou **arrêter cette application uniquement**.   

10. Dans la page **créer un package** , pour modifier le package sans l’enregistrer, activez la case à cocher pour **continuer à modifier le package sans l’enregistrer à l’aide de l’éditeur de package**. Lorsque vous sélectionnez cette option, le package s’ouvre dans la console App-V Sequencer dans laquelle vous pouvez modifier le package avant son enregistrement. Cliquez sur **Suivant**.

    Pour enregistrer le package immédiatement, sélectionnez l’option **enregistrer le package**par défaut. Ajoutez des **Commentaires** facultatifs à associer au package. Les commentaires sont utiles pour identifier la version de l’application et fournir d’autres informations sur le package. L' **emplacement d’enregistrement** par défaut est également affiché. Pour modifier l’emplacement par défaut, cliquez sur **Parcourir** et spécifiez le nouvel emplacement. Cliquez sur **Créer**.

11. Dans la page **dernière étape** , cliquez sur **Fermer** pour fermer l’Assistant. Le package est désormais disponible dans le Sequencer.

<a href="" id="bkmk-chg-props-in-pkg"></a>**Modifier les propriétés associées à un package d’application virtuelle existant**

1.  Sur l’ordinateur qui exécute le Sequencer, cliquez sur **tous les programmes**, pointez sur **virtualisation des applications**, puis cliquez sur **Sequencer Microsoft Application Virtualization**.

2.  Dans le Sequencer App-V, cliquez sur **modifier un package d’application virtuel existant** &gt; **Next**.

3.  Dans la page **Sélectionner une tâche** , cliquez sur modifier le **package** &gt; **suivant**.

4.  Dans la page **Sélectionner un package** , cliquez sur **Parcourir** pour localiser le package d’application virtuel contenant les propriétés de l’application à modifier, puis cliquez sur **modifier**.

5.  Dans la console de Sequencer App-V, effectuez l’une des tâches suivantes si nécessaire:

    -   Importez et exportez le fichier manifeste.

    -   Activer ou désactiver les objets d’assistance du navigateur.

    -   Importez ou exportez un fichier VFS.

    -   Importez un annuaire dans le système de fichiers virtuel.

    -   Importez et exportez des clés de Registre virtuelles.

    -   Afficher les propriétés du package.

    -   Afficher les fichiers de package associés.

    -   Modifier les paramètres du Registre.

    -   Passez en revue les paramètres de package supplémentaires (sauf les propriétés du fichier système d’exploitation).

    -   Définissez l’état de la clé de Registre virtualisé (substitution ou fusion).

    -   Définir l’état de dossier virtualisé.

    -   Ajoutez ou modifiez des raccourcis et des associations de types de fichiers.

        **Remarques**  Pour modifier les raccourcis ou les associations de types de fichiers, vous devez d’abord ouvrir le package à des fins de mise à niveau pour ajouter une nouvelle application, puis passer à la page de modification finale.

6.  Lorsque vous avez fini de modifier les propriétés du package **, cliquez sur** &gt; **Enregistrer** pour enregistrer le package.

<a href="" id="bkmk-add-app-to-pkg"></a>**Ajouter une nouvelle application à un package d’application virtuelle existant**

1.  Sur l’ordinateur qui exécute le Sequencer, cliquez sur **tous les programmes**, pointez sur **virtualisation des applications**, puis cliquez sur **Sequencer Microsoft Application Virtualization**.

2.  Dans le Sequencer App-V, cliquez sur **modifier un package d’application virtuel existant** &gt; **Next**.

3.  Dans la page **Sélectionner une tâche** , cliquez sur Ajouter une **nouvelle application** &gt; **suivante**.

4.  Dans la page **Sélectionner un package** , cliquez sur **Parcourir** pour localiser le package d’application virtuel auquel vous allez ajouter l’application, puis cliquez sur **suivant**.

5.  Sur la page **préparer l’ordinateur** , passez en revue les problèmes qui pourraient entraîner l’échec de la création du package ou entraînent l’affichage des données inutiles dans le package modifié. Résolvez tous les problèmes potentiels avant de continuer. Après avoir effectué des corrections et résolu les problèmes potentiels, cliquez sur **Actualiser** &gt; **suivant**.

    **Important**  Si vous êtes tenu de désactiver le logiciel antivirus, analysez d’abord l’ordinateur qui exécute le Sequencer pour vous assurer qu’aucun fichier non souhaité ou malveillant ne peut être ajouté au package.

6.  Dans la page **Sélectionner le programme d’installation** , cliquez sur **Parcourir** , puis spécifiez le fichier d’installation de l’application. Si l’application n’a pas de fichier d’installation associé et que vous envisagez d’exécuter toutes les étapes d’installation manuellement, activez la case à cocher **activer cette option pour effectuer une installation personnalisée** , puis cliquez sur **suivant**.

7.  Dans la page **installation** , lorsque le programme d’installation de Sequencer et d’application est prêt, installez l’application afin que le Sequencer puisse surveiller le processus d’installation. Si des fichiers d’installation supplémentaires doivent être exécutés dans le cadre de l’installation, cliquez sur **exécuter**, puis recherchez et exécutez les fichiers d’installation supplémentaires. Une fois l’installation terminée, sélectionnez l’option **j’ai terminé d’installer** &gt; **Next**. Dans la boîte de dialogue **Rechercher un dossier** , spécifiez le répertoire principal dans lequel l’application sera installée. Assurez-vous qu’il s’agit d’un nouvel emplacement dans lequel vous ne pouvez pas remplacer la version existante du package d’application virtuelle.

    **Remarques**  Le Sequencer contrôle toutes les modifications et les installations qui se produisent sur l’ordinateur qui exécute le Sequencer. Cela inclut les modifications et installations effectuées en dehors de l’Assistant séquençage.

8.  Sur la page **configurer le logiciel** , exécutez éventuellement les programmes contenus dans le package. Cette étape effectue toutes les tâches de configuration ou de licence associées requises pour exécuter l’application avant de déployer et d’exécuter le package sur des ordinateurs cibles. Pour exécuter tous les programmes en même temps, sélectionnez au moins un programme, puis cliquez sur **exécuter tout**. Pour exécuter des programmes spécifiques, sélectionnez le ou les programmes que vous voulez exécuter, puis cliquez sur **exécuter la sélection**. Effectuez les tâches de configuration requises, puis fermez les applications. L’exécution de tous les programmes peut prendre quelques minutes. Cliquez sur **Suivant**.

9.  Dans la page **rapport d’installation** , vous pouvez consulter des informations sur l’application virtuelle mise à jour. Dans **informations supplémentaires**, double-cliquez sur l’événement pour obtenir des informations plus détaillées, puis cliquez sur **suivant** pour ouvrir la page de **personnalisation** .

10. Si vous avez terminé l’installation et la configuration de l’application virtuelle, sélectionnez **arrêter maintenant** et passez directement à l’étape 13 de cette procédure. Si vous voulez effectuer la personnalisation décrite suivante, cliquez sur **personnaliser**.

    Si vous personnalisez, préparez le package virtuel pour la diffusion en continu, puis cliquez sur **suivant**. La diffusion en continu améliore son fonctionnement lorsque le package d’application virtuelle est exécuté sur les ordinateurs cibles.

11. Sur la page de **diffusion** , exécutez chaque programme de manière à optimiser son exécution et son exécution plus efficacement sur les ordinateurs cibles. L’exécution de toutes les applications peut prendre quelques minutes. Après l’exécution de toutes les applications, fermez chacune d’elles, puis cliquez sur **suivant**.

    **Remarques**  Vous pouvez empêcher le chargement d’une application au cours de cette étape. Dans la boîte de dialogue lancement de l' **application** , cliquez sur **arrêter** , puis sélectionnez **arrêter toutes les applications** ou **arrêter cette application uniquement**.

12. Dans la page **créer un package** , pour modifier le package sans l’enregistrer, activez la case à cocher **continuer à modifier le package sans enregistrer à l’aide de l’éditeur de package** . Lorsque vous sélectionnez cette option, le package est ouvert dans la console App-V du Sequencer, où vous pouvez modifier le package avant de l’enregistrer. Cliquez sur **Suivant**.

    Pour enregistrer le package immédiatement, sélectionnez l’option **enregistrer le package**par défaut. Ajoutez des **Commentaires** facultatifs à associer au package. Les commentaires sont utiles pour fournir des versions d’application et d’autres informations sur le package. L' **emplacement d’enregistrement** par défaut est également affiché. Pour modifier l’emplacement par défaut, cliquez sur **Parcourir** et spécifiez le nouvel emplacement. La taille du package non compressé s’affiche. Cliquez sur **Créer**.

13. Sur la page **Fin**, cliquez sur **Fermer**. Le package est désormais disponible dans le Sequencer.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes

[Opérations d'App-V5.1](operations-for-app-v-51.md)

 

 





