---
title: Procédure pour créer des accélérateurs de package App-V (App-V4.6SP1)
description: Procédure pour créer des accélérateurs de package App-V (App-V4.6SP1)
author: dansimp
ms.assetid: 585e692e-cebb-48ac-93ab-b2e7eb7ae7ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eb806ccf04fcd5ae7db87c5de21e85217739fcbc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807186"
---
# Procédure pour créer des accélérateurs de package App-V (App-V4.6SP1)


Vous pouvez utiliser les accélérateurs de package App-V pour générer automatiquement un nouveau package d’application virtuel. Une fois que vous avez correctement créé un accélérateur de package, vous pouvez réutiliser et partager l’accélérateur de package. Pour plus d’informations sur les accélérateurs de package, voir [à propos des accélérateurs de package App-v (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md). La création d’accélérateurs de package App-V est une tâche avancée. Les accélérateurs de package peuvent contenir des informations relatives aux mots de passe et aux utilisateurs. Par conséquent, vous devez enregistrer les accélérateurs de package et le média d’installation associé dans un emplacement sécurisé, et vous devez signer numériquement l’accélérateur de package après l’avoir créé, afin que l’éditeur puisse être vérifié lorsque l’accélérateur de package App-V est appliqué.

Dans certains cas, pour créer l’accélérateur de package, vous devrez peut-être installer l’application localement sur l’ordinateur exécutant le Sequencer. Tout d’abord, essayez de créer l’accélérateur de package à l’aide du support d’installation, et si le nombre de fichiers manquants requis est requis, installez l’application localement sur l’ordinateur exécutant le Sequencer, puis créez l’accélérateur de package.

**Important**  
Avant de commencer la procédure suivante, vous devez effectuer les opérations suivantes:

-   Copiez le package d’application virtuel que vous devez utiliser pour créer l’accélérateur de package localement sur l’ordinateur exécutant le Sequencer.

-   Copiez tous les fichiers d’installation requis associés au package d’application virtuelle sur l’ordinateur exécutant le Sequencer.



**Important**  
Exclusion de responsabilité: le Sequencer Microsoft Application Virtualization ne vous donne aucun droit de licence pour l’application logicielle que vous utilisez pour créer un accélérateur de package. Vous devez respecter les conditions générales du contrat de licence utilisateur final pour une telle application. Il est de votre responsabilité de veiller à ce que les termes du contrat de licence de l’application logicielle vous permettent de créer un accélérateur de package à l’aide du Sequencer de la virtualisation de l’application.



**Pour créer un accélérateur de package App-V**

1.  Pour démarrer le Sequencer App-v, sur l’ordinateur exécutant le Sequencer App-v, cliquez sur **Démarrer**  /  **tout le programme**  /  **Microsoft Application Virtualization**Microsoft Application Virtualization  /  **Sequencer**.

2.  Pour démarrer l’Assistant App-v de **création de package** , dans le Sequencer App-v, cliquez sur **Outils**  /  **créer un accélérateur de package**.

3.  Dans la page **Sélectionner un package** , pour spécifier un package d’application virtuelle existant à utiliser pour créer l’accélérateur de package, cliquez sur **Parcourir**, puis recherchez le package d’application virtuelle existant (fichier. sprj).

    **Astuce**  
    Copiez les fichiers associés au package d’application virtuel que vous envisagez d’utiliser localement sur l’ordinateur exécutant le Sequencer.



~~~
Click **Next**.
~~~

4. Dans la page **fichiers d’installation** , pour spécifier le dossier contenant les fichiers d’installation que vous avez utilisés pour créer le package d’application virtuelle d’origine, cliquez sur **Parcourir**, puis sélectionnez le répertoire contenant les fichiers d’installation.

   **Astuce**  
   Copiez le dossier contenant les fichiers d’installation requis sur l’ordinateur exécutant le Sequencer.



~~~
If the application is already installed on the computer running the Sequencer, to specify the installation file, select **Files installed on local system**. To use this option, the application must already be installed in the default installation location.
~~~

5. Dans la page **collecte d’informations** , consultez les fichiers qui n’ont pas été trouvés dans l’emplacement spécifié dans la page fichiers d' **installation** de cet Assistant. Si les fichiers affichés ne sont pas obligatoires, sélectionnez **supprimer ces fichiers**, puis cliquez sur **suivant**. Si les fichiers sont requis, cliquez sur **précédent** , puis copiez les fichiers requis dans le répertoire spécifié dans la page **fichiers d’installation** .

   **Remarque**  
   Vous devez supprimer les fichiers non requis ou cliquer sur **précédent** , puis rechercher les fichiers requis pour passer à la page suivante de l’Assistant.



6. Dans la page **Sélectionner des fichiers** , passez en revue les fichiers qui ont été détectés et effacez les fichiers qui doivent être supprimés de l’accélérateur de package. Sélectionnez uniquement les fichiers nécessaires à l’exécution correcte de l’application, puis cliquez sur **suivant**.

7. Dans la page **verify applications (vérifier les applications** ), vérifiez que tous les fichiers d’installation requis pour générer le package sont affichés. Lorsque l’accélérateur de package est utilisé pour créer un nouveau package, tous les fichiers d’installation affichés dans le volet **applications** sont requis pour créer le package.

   Si nécessaire, pour ajouter d’autres fichiers du programme d’installation, cliquez sur **Ajouter**. Pour supprimer les fichiers d’installation inutiles, sélectionnez le fichier d’installation, puis cliquez sur **supprimer**. Pour modifier les propriétés associées à un programme d’installation, cliquez sur **modifier**. Les fichiers d’installation spécifiés dans cette étape seront nécessaires lorsque l’accélérateur de package sera utilisé pour créer un nouveau package d’application virtuelle. Après confirmation des informations affichées, cliquez sur **suivant**.

8. Dans la page **Sélectionner des recommandations** , pour spécifier un fichier contenant des informations sur la façon dont l’accélérateur de package s’affiche, cliquez sur **Parcourir**. Par exemple, ce fichier peut contenir des informations sur la façon dont l’ordinateur exécutant le Sequencer doit être configuré, les informations requises pour l’application pour les ordinateurs cibles et les notes générales. Vous devez fournir toutes les informations nécessaires à l’application de l’accélérateur de package. Le fichier que vous sélectionnez doit être au format texte enrichi (. rtf) ou fichier texte (. txt). Cliquez sur **Suivant**.

9. Dans la page **créer un accélérateur de package** , pour spécifier l’emplacement d’enregistrement de l’accélérateur de package, cliquez sur **Parcourir** , puis sélectionnez le répertoire.

10. Dans la page **dernière étape** , cliquez sur **Fermer**pour fermer l’Assistant Création d’un **accélérateur de package** .

   **Important**  
   Pour vous assurer que le package Accelerator est le plus sécurisé possible et que l’éditeur puisse être vérifié lors de l’application de l’accélérateur de package, vous devez toujours signer numériquement l’accélérateur de package.



## Rubriques connexes


Configuration du séquenceur de virtualisation d’application (App-V 4,6 SP1) [comment appliquer un accélérateur de package pour créer un package d’application virtuelle (App-v 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)









