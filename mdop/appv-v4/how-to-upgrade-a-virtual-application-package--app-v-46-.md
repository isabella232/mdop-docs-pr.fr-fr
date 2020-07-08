---
title: Procédure de mise à niveau d'un package d'application virtuelle (App-V 4.6)
description: Procédure de mise à niveau d'un package d'application virtuelle (App-V 4.6)
author: dansimp
ms.assetid: 3566227e-f3dc-4c32-af1f-e0211588118c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac722dc0e9ce1650f53d8dd22db5428d33cfcf13
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806714"
---
# Procédure de mise à niveau d'un package d'application virtuelle (App-V 4.6)


Suivez la procédure ci-dessous pour mettre à niveau une application virtuelle existante à l’aide du Sequencer Application Virtualization (App-V). Vous pouvez également utiliser la console de Sequencer App-V pour apporter des modifications à une application virtuelle existante sans procéder à la mise à niveau, mais vous ne pouvez pas apporter de modifications au système de fichiers de l’application virtuelle à l’aide de cette méthode, car le Sequencer App-V ne décode pas réellement le fichier. SFT associé. Pour plus d’informations sur la modification d’un package existant, voir [Comment modifier un package d’application virtuel (App-V 4,6)](how-to-modify-a-virtual-application-package--app-v-46-.md).

**Pour mettre à niveau une application virtuelle existante**

1.  Pour démarrer la console App-v du Sequencer, sur l’ordinateur exécutant le Sequencer App-v, sélectionnez **Démarrer**des  /  **programmes**  /  **Microsoft Application Virtualization**  /  **Sequencer**.

2.  Pour ouvrir le package d’application virtuelle existant et démarrer l' **Assistant de séquençage**, sélectionnez **mettre à niveau un package**. Recherchez le package que vous voulez mettre à niveau, puis cliquez sur **ouvrir**. Dans la boîte de dialogue **Rechercher un dossier** , spécifiez l’emplacement où se trouve la version mise à niveau du package. Cet emplacement spécifié doit se trouver sur le lecteur spécifié comme lecteur de virtualisation des applications, qui est généralement le lecteur Q:\\. Pour créer un dossier, sélectionnez **créer un nouveau dossier**.

    **Avertissement**  Vous devez spécifier le dossier racine de l’application virtuelle existante. Ne créez pas manuellement un sous-dossier ou la mise à niveau échouera.

     

3.  Dans la page informations sur le **package** , spécifiez le **nom du package** qui sera affecté au package mis à jour. Le nom du package est requis pour générer le fichier Windows Installer associé. Vous devez également ajouter un commentaire facultatif qui sera affecté au package et qui fournit des informations détaillées sur l’application virtuelle, par exemple un numéro de version. Pour afficher la page **Options avancées** , sélectionnez **afficher les options de surveillance avancées** , puis cliquez sur **suivant**. dans le cas contraire, passez à l’étape 5.

4.  Dans la page **Options avancées** , pour permettre à Microsoft Update de mettre à jour l’application au fur et à mesure, sélectionnez **autoriser l’exécution de Microsoft Update lors du suivi**. Si vous sélectionnez cette option, les mises à jour Microsoft peuvent être installées pendant la phase de surveillance et vous devrez accepter les mises à jour associées pour qu’elles soient installées. Pour remapper les fichiers de la bibliothèque de liens dynamiques (. dll) pris en charge de manière à ce qu’ils utilisent un espace contigu de RAM, sélectionnez **relocal DLLs**. La sélection de cette option permet d’économiser la mémoire et d’améliorer les performances. Cliquez sur **Suivant**.

5.  Dans la page d' **installation du moniteur** , lorsque vous êtes prêt à mettre à jour l’application, cliquez sur commencer l' **analyse**.

    Lorsque les mises à jour de l’application ont été appliquées, cliquez sur **ne plus surveiller**. Cliquez sur **Suivant**.

6.  Dans la page **configurer des applications** , le cas échéant, configurez les raccourcis et les associations de types de fichiers qui seront associés à l’application virtuelle. Pour ajouter une nouvelle association de type de fichier ou un raccourci, cliquez sur **Ajouter**, puis, dans la boîte de dialogue **Ajouter une application** , spécifiez le nouvel élément. Pour supprimer un raccourci ou une association de type de fichier existant, cliquez sur **supprimer**. Pour modifier un élément existant, sélectionnez-le, puis cliquez sur **modifier**. Spécifiez les configurations dans la boîte de dialogue **modifier l’application** . Cliquez sur **Save**. Cliquez sur **Suivant**.

7.  Dans la page **Launch applications (lancer des applications** ), pour démarrer l’application afin de vérifier que le package a été correctement installé et qu’il est optimisé pour la diffusion en continu, sélectionnez-le, puis cliquez sur **Démarrer**. Cette étape est utile pour configurer le mode d’exécution de l’application sur les ordinateurs cibles, et pour accepter les contrats de licence associés avant la mise à la disposition des clients App-V. Si plusieurs applications sont associées à ce package, vous pouvez sélectionner **lancer tout** pour ouvrir toutes les applications. Pour séquencer le package, cliquez sur **suivant**.

8.  Pour fermer l’Assistant séquençage, cliquez sur **Terminer**. Pour enregistrer le package mis à jour, dans la console de Sequencer, sélectionnez **fichier**  /  **Enregistrer**.

    Si vous envisagez de déployer le package mis à jour à l’aide d’un fichier Windows Installer (. msi), vous devez en créer un nouveau en procédant comme suit: dans la console de Sequencer, sélectionnez **Outils**  /  **créer MSI**. Le nouveau fichier du programme d’installation Windows sera créé et enregistré dans le répertoire où est enregistré le package d’application virtuelle mis à jour.

## Rubriques connexes


[Procédure pour séquencer une nouvelle application (App-V4.6)](how-to-sequence-a-new-application--app-v-46-.md)

 

 





