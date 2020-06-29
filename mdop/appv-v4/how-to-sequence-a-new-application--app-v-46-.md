---
title: Procédure pour séquencer une nouvelle application (App-V4.6)
description: Procédure pour séquencer une nouvelle application (App-V4.6)
author: dansimp
ms.assetid: f2c398c6-9200-4be3-b502-e00386fcd150
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a36021adf45f0f4c80ab08bcabbf9f18bf6e66b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806810"
---
# Procédure pour séquencer une nouvelle application (App-V4.6)


Utilisez la procédure suivante pour créer une application virtuelle à l’aide du séquenceur Application Virtualization (App-V). Vous pouvez également utiliser le Sequencer App-V pour configurer les fichiers et configurations applicables à tous les utilisateurs, ainsi que les fichiers et configurations que les utilisateurs peuvent personnaliser. Une fois que vous avez correctement séquencé l’application, celle-ci est disponible dans le Sequencer App-V.

**Important**  
Lors du séquençage, si l’ordinateur exécutant le Sequencer exécute Windows Vista ou Windows 7 et qu’un redémarrage est lancé en dehors de l’environnement virtuel, par exemple, en cliquant sur **Démarrer**  /  **arrêter**, vous devez cliquer sur **Annuler** lorsque vous êtes invité à fermer le programme qui empêche Windows de s’arrêter. Si vous cliquez sur **forcer l’arrêt**, la création du package échoue et l’ordinateur redémarre. Lorsque vous cliquez sur **Annuler**, le Sequencer enregistre correctement le redémarrage lorsque l’application est en cours de séquence.



**Pour séquencer une nouvelle application**

1.  Pour créer le lecteur App-V, configurez le lecteur Q en tant qu’emplacement permettant d’enregistrer des fichiers pendant que vous séquençagez une application. Pour chaque application que vous envisagez de séquencer, vous devez ensuite créer des répertoires individuels. Vous pouvez créer les dossiers ciblés de l’application virtuelle avant de séquencer une application, ou vous pouvez les créer à l’étape 5 de cette procédure.

    **Remarque**  
    Le lecteur App-V que vous spécifiez doit être accessible sur des ordinateurs ciblés. Si le lecteur Q n’est pas accessible, vous pouvez choisir une autre lettre de lecteur.



2.  Pour démarrer la console de Sequencer App-v, sur l’ordinateur exécutant le Sequencer App-v, sélectionnez **Démarrer**  /  **programmes**  /  **Microsoft Application Virtualization**  /  **Sequencer Microsoft application**Virtualization. Pour démarrer l’Assistant séquençage, cliquez sur **créer un package**.

3.  Dans la page informations sur le **package** , spécifiez le **nom du package** qui sera affecté à l’application virtuelle. Le nom du package est requis pour générer le fichier Windows Installer associé. Vous devez également ajouter un commentaire facultatif qui sera affecté au package et qui fournit des informations détaillées sur l’application virtuelle. Pour afficher la page **Options avancées** , sélectionnez **afficher les options de surveillance avancées**, puis cliquez sur **suivant**. dans le cas contraire, passez à l’étape 5.

4.  Dans la page **Options avancées** , pour permettre à Microsoft Update de mettre à jour l’application au fur et à mesure, sélectionnez **autoriser l’exécution de Microsoft Update lors du suivi**. Si vous sélectionnez cette option, les mises à jour Microsoft peuvent être installées pendant la phase de surveillance, et vous devez accepter les mises à jour associées pour qu’elles soient installées. Pour remapper les fichiers de la bibliothèque de liens dynamiques (. dll) pris en charge de façon à ce qu’ils utilisent un espace contigu de RAM, sélectionnez **relocal DLLs**. La sélection de cette option permet d’économiser la mémoire et d’améliorer les performances. Dans de nombreux cas, cette option n’est pas prise en charge, mais elle est utile dans les environnements dotés d’une RAM limitée, par exemple dans les scénarios Terminal Server. Cliquez sur **Suivant**.

5.  Dans la page d' **installation du moniteur** , lorsque vous êtes prêt à installer l’application, cliquez sur commencer l' **analyse**, puis dans la boîte de dialogue **Rechercher un dossier** , spécifiez le répertoire sur le lecteur Q où l’application sera installée. Si vous n’avez pas configuré Drive Q et que vous avez utilisé une autre lettre de lecteur pour le lecteur de virtualisation des applications, sélectionnez la lettre du lecteur que vous avez spécifiée à l’étape 1 de cette procédure. Pour installer l’application dans un dossier qui n’a pas été créé sur le lecteur de virtualisation des applications, cliquez sur **créer un nouveau dossier**. Une fois le dossier spécifié, attendez que le Sequencer configure l’ordinateur pour le séquençage.

    **Important**  
    Vous devez installer chaque application que vous séquencez dans un répertoire distinct sur le lecteur d’application virtuelle, et le nom de dossier associé ne doit pas comporter plus de huit caractères.



~~~
After the computer has been configured for sequencing, install the application so that the App-V Sequencer can monitor the installation; when you are finished, click **Stop Monitoring**, and then click **Next**.
~~~

6. Dans la page **configurer des applications** , le cas échéant, configurez les raccourcis et les associations de types de fichiers qui seront associés à l’application virtuelle. Pour ajouter une nouvelle association de type de fichier ou un raccourci, cliquez sur **Ajouter**, puis, dans la boîte de dialogue **Ajouter une application** , spécifiez le nouvel élément. Pour supprimer un raccourci ou une association de type de fichier existant, cliquez sur **supprimer**. Pour modifier un élément existant, sélectionnez-le, puis cliquez sur **modifier**. Spécifiez les configurations dans la boîte de dialogue **modifier l’application** . Cliquez sur **Enregistrer**, puis sur **suivant**.

7. Dans la page **lancer des applications** , pour démarrer l’application afin de vérifier que le package a été correctement installé et qu’il est optimisé pour la diffusion en continu, sélectionnez-le, puis cliquez sur **Démarrer**. Cette étape est utile pour configurer le mode d’exécution de l’application sur des ordinateurs ciblés et pour accepter les contrats de licence associés avant que le package ne soit disponible pour les clients App-V. Si plusieurs applications sont associées à ce package, vous pouvez sélectionner **lancer tout** pour ouvrir toutes les applications. Pour séquencer le package, cliquez sur **suivant**.

8. Une fois que vous avez créé le package, dans la console App-V du Sequencer, sélectionnez **fichier**  /  **Enregistrer** et spécifiez le nom et l’emplacement du lecteur virtuel où le package sera enregistré.

   Vous pouvez éventuellement créer un fichier Windows Installer (**. msi**) associé pour installer le package d’application virtuel sur des ordinateurs ciblés. Pour créer un fichier du programme d’installation Windows, ouvrez le package dans le Sequencer et sélectionnez **Outils**  /  **créer MSI**. Le fichier du programme d’installation Windows sera créé et enregistré dans l’annuaire dans lequel le package d’application virtuelle est enregistré.

   **Important**  
   Une fois que vous avez correctement créé un package d’application virtuelle, vous ne pouvez pas exécuter le package d’application virtuel sur l’ordinateur exécutant le Sequencer.



## Rubriques connexes


[Procédure de mise à niveau d'un package d'application virtuelle (App-V 4.6)](how-to-upgrade-a-virtual-application-package--app-v-46-.md)









