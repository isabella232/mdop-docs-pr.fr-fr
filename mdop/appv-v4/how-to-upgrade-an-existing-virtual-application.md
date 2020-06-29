---
title: Procédure pour mettre à niveau une application virtuelle existante
description: Procédure pour mettre à niveau une application virtuelle existante
author: dansimp
ms.assetid: ec531576-2423-4c2c-9b9f-da74174a6858
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 71fb096c103a0bcb9913d4eea33b1259a33a54ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806710"
---
# Procédure pour mettre à niveau une application virtuelle existante


Vous pouvez mettre à niveau une application virtuelle existante vers une nouvelle version en utilisant le Sequencer Application Virtualization (App-V). Le processus de mise à niveau est similaire à la création d’une nouvelle application virtuelle. Vous devez ouvrir l’application virtuelle existante pour une mise à niveau, apporter les mises à jour nécessaires, puis enregistrer l’application virtuelle mise à jour dans un nouvel emplacement dans le répertoire racine du package.

Vous pouvez également utiliser la console de Sequencer App-V pour apporter des modifications à une application virtuelle existante sans procéder à la mise à niveau. Toutefois, vous ne pouvez pas apporter de modifications au système de fichiers de l’application virtuelle à l’aide de cette méthode, car le Sequencer App-V ne décode pas réellement le fichier. SFT associé. Par exemple, vous pouvez ouvrir une application virtuelle existante dans la console App-V du Sequencer en sélectionnant **ouvrir** dans le menu **fichier** . Vous pouvez mettre à jour le **nom du package** et les **Commentaires**associés, et apporter des modifications au système de fichiers virtuel et au registre virtuel. Vous pouvez également créer un fichier du programme d’installation Windows.

Utilisez la procédure suivante pour mettre à niveau une application virtuelle existante.

**Pour mettre à niveau une application virtuelle existante**

1.  Pour démarrer la console App-v du Sequencer, sur l’ordinateur exécutant le Sequencer App-v, sélectionnez **Démarrer**des / **programmes** / **Microsoft Application Virtualization** / **Sequencer**.

2.  Pour ouvrir l’application virtuelle existante, dans la console App-V, sélectionnez **File** / **ouverture de fichier pour la mise à niveau du package**. Utilisez la boîte **de dialogue Ouvrir pour la mise à niveau du package** pour rechercher le fichier de SPRJ associé que vous voulez ouvrir pour la mise à niveau.

3.  Pour spécifier l’emplacement de l’emplacement du décodage du package, cliquez sur **Rechercher un dossier** et spécifiez le Q:\\. Il s’agit de l’emplacement dans lequel le répertoire racine du package sera créé comme spécifié dans le fichier SFT associé. Lorsque vous créez la version mise à jour du package, celle-ci est désignée par un ajout séquentiel du nom de l’annuaire (par exemple, «**0,1**») est ajouté au nom de l’annuaire situé sur le lecteur Q:\\.

4.  Pour ouvrir l’Assistant séquençage, sélectionnez **Outils**de / **séquençage**. Dans la page informations sur le **package** , spécifiez éventuellement le nouveau **nom de package** et ajoutez des commentaires facultatifs qui seront associés à l’application virtuelle mise à jour. Cliquez sur **Suivant**.

5.  Dans la page d' **installation du moniteur** , pour commencer à surveiller la nouvelle installation, cliquez sur **commencer la surveillance**. Lorsque le chargement de l’environnement virtuel est terminé, installez la version mise à jour de l’application ou appliquez les mises à jour à l’application existante. Après avoir effectué la mise à jour de l’application virtuelle, cliquez sur **arrêter la surveillance**, puis cliquez sur **suivant**.

6.  Dans la page **fichiers supplémentaires à mapper sur le système de fichiers virtuel (VFS)** , cliquez sur **Ajouter**pour spécifier d’autres fichiers à ajouter au système de fichiers virtuel (VFS). Recherchez le fichier que vous voulez ajouter, puis cliquez sur **ouvrir**. Pour effacer les fichiers existants qui ont été ajoutés, cliquez sur **Réinitialiser**, puis sur **suivant**.

7.  Dans la page **configurer des applications** , configurez les raccourcis et les associations de types de fichiers qui seront associés à l’application virtuelle mise à jour. Sélectionnez l’élément que vous voulez mettre à jour, puis cliquez sur **modifier les emplacements**. Spécifiez les configurations dans la boîte de dialogue **emplacements de raccourci** , puis cliquez sur **suivant**.

8.  Dans la page **Launch applications (lancer des applications** ), pour démarrer l’application afin de vous assurer que le package est optimisé pour la diffusion, sélectionnez-le, puis cliquez sur **Launch**. Cette étape est utile pour configurer la manière dont l’application s’exécute au départ sur les ordinateurs cibles, et pour accepter tout contrat de licence associé avant la mise à la disposition des clients du package. S’il existe plusieurs applications associées à ce package, vous pouvez sélectionner **lancer tout** pour ouvrir toutes les applications. Pour séquencer la nouvelle version de l’application virtuelle, cliquez sur **suivant**.

9.  Pour terminer et fermer l’Assistant séquençage, sur la page **package de séquence** , cliquez sur **Terminer**.

10. Une fois que vous avez effectué la mise à jour de l’application virtuelle, dans le menu fichier, dans le menu **fichier** , sélectionnez **Enregistrer**pour enregistrer le package. Il est possible d’accéder à l’application virtuelle dans le répertoire indiqué à l’étape 3.

## Rubriques connexes


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

[Procédure pour mettre à niveau une application virtuelle à l'aide de la ligne de commande](how-to-upgrade-a-virtual-application-by-using-the-command-line.md)

 

 





