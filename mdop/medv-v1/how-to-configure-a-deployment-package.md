---
title: Comment configurer un package de déploiement
description: Comment configurer un package de déploiement
author: dansimp
ms.assetid: 748272a1-6af2-476e-a3f1-87435b8e94b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aba5e91a4da92f9e51a5ccc70502658ae724d76f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811460"
---
# Comment configurer un package de déploiement


L’Assistant Création de packages vous guide dans le processus de création d’un package en créant un dossier sur votre ordinateur local et en transférant tous les fichiers d’installation requis vers le dossier unique. Le contenu du dossier peut ensuite être déplacé vers plusieurs lecteurs de médias amovibles pour distribution.

**Remarque**  
Un package unique ne peut pas contenir des fichiers d’installation pour les systèmes x86 et x64.



## Créer un package de déploiement


**Pour créer un package de déploiement**

1. Dans le module **images** , vérifiez que vous avez créé au moins une image compactée locale.

2. Dans le menu **Outils** , sélectionnez **Assistant Empaquetage**.

3. Sur la page d’accueil de l' **Assistant Packaging** , cliquez sur **suivant**.

4. Dans la page image de l' **espace de travail** , activez la case à cocher **inclure l’image dans le package** pour inclure une image dans le package.

   Le champ d' **image** est activé.

   **Remarque**  
   Une image n’est pas requise dans un paquet MED-V; le package peut être créé sans image. Dans ce cas, l’image doit être téléchargée sur le serveur pour pouvoir être téléchargée par la suite via le réseau vers le client ou déplacée vers un dossier de préinstallation d’une image.



5. Cliquez sur la liste d' **images** pour afficher toutes les images disponibles. Sélectionnez l’image à copier dans le package. Cliquez sur **Actualiser** pour actualiser la liste des images disponibles.

6. Cliquez sur **Suivant**.

7. Dans la page **paramètres d’installation de med-v** , sélectionnez le fichier d’installation de med-v en effectuant l’une des opérations suivantes:

   -   Dans le champ **fichier d’installation de MED-V** , tapez le chemin d’accès complet au répertoire dans lequel se trouve le fichier d’installation.

   -   Cliquez sur **...** pour accéder au répertoire dans lequel se trouve le fichier d’installation.

   **Remarque**  
   Ce champ est obligatoire et ne s’applique pas sans nom de fichier valide.



8. Dans le champ **adresse du serveur** , tapez le nom ou l’adresse IP du serveur.

9. Dans le champ **port du serveur** , tapez le port du serveur.

10. Sélectionnez le **serveur est accessible à l’aide** de la case à cocher HTTPS pour exiger une connexion HTTPS pour la connexion au serveur.

11. Effectuez l'une des opérations suivantes:

    -   Cliquez sur **paramètres d’installation par défaut**, puis cliquez sur **suivant** pour continuer et conserver les paramètres par défaut.

    -   Cliquez sur **paramètres d’installation personnalisés**, puis cliquez sur **suivant** pour personnaliser les paramètres d’installation.

        1.  Dans la page **paramètres personnalisés de l’installation de med-v** , dans le champ **dossier d’installation** , tapez le chemin d’accès du dossier dans lequel les fichiers MED-V seront installés sur l’ordinateur hôte.

            **Remarque**  
            Il est recommandé d’utiliser des variables dans le chemin d’accès plutôt que des constantes, qui peuvent varier d’un ordinateur à un ordinateur.

            Par exemple, utilisez *%ProgramFiles%\\MED-V* à la place de *c:\\MED-V*.



    ~~~
    2.  In the **Virtual machines images folder** field, type the path of the folder where the virtual images files will be installed on the host computer.

        **Note**  
        If you are using image pre-staging, this is the image pre-stage folder where the image is located.



    3.  In the **Minimal required RAM** field, enter the RAM required to install a MED-V package. If the user installing the MED-V package does not have the minimal required RAM, the installation will fail.

    4.  Select the **Install the MED-V management application** check box to include the MED-V management console application in the installation.

    5.  Select the **Create a shortcut to MED-V on the desktop** check box to create a shortcut to MED-V on the host's desktop.

    6.  Select the **Start automatically on computer startup** check box to start MED-V automatically on startup.

    7.  Click **Next**.
    ~~~

12. Sur la page **installations supplémentaires** , activez la case à cocher **inclure l’installation de la version du logiciel de virtualisation** pour inclure l’installation Virtual PC dans le package.

    Le champ **fichier d’installation** est activé. Tapez le chemin d’accès complet du fichier d’installation du logiciel de virtualisation ou cliquez sur **...** pour accéder au répertoire.

13. Cochez la case **inclure l’installation de la version QFE de Virtual PC** pour inclure l’installation de la mise à jour Virtual PC dans le package.

    Le champ **fichier d’installation** est activé. Tapez le chemin d’accès complet du fichier d’installation de la mise à jour Virtual PC ou cliquez sur **...** pour accéder au répertoire.

14. Cochez la case **inclure l’installation de Microsoft .net framework 2,0** pour inclure l’installation de Microsoft .net Framework 2,0 dans le package.

    Le champ **fichier d’installation** est activé. Tapez le chemin d’accès complet du fichier d’installation de Microsoft .NET Framework 2,0 ou cliquez sur **...** pour accéder au répertoire.

15. Cliquez sur **Suivant**.

16. Sur la page **Finalize** , sélectionnez l’emplacement dans lequel enregistrer le package en effectuant l’une des opérations suivantes:

    -   Dans le champ **destination du package** , tapez le chemin d’accès complet au répertoire dans lequel le package doit être enregistré.

    -   Cliquez sur **...** pour accéder au répertoire dans lequel les fichiers d’installation doivent être enregistrés.

    **Remarque**  
    La création du package peut consommer davantage d’espace que la taille réelle du package. C’est pourquoi il est recommandé de générer le package sur le disque dur. Une fois le package créé, il peut être copié sur le USB.



17. Dans le champ **nom du package** , entrez le nom du package.

18. Cliquez sur **Terminer** pour créer le package.

    Le package est créé. Cela peut prendre quelques minutes.

    Une fois le package créé, un message s’affiche pour vous signaler qu’il s’est terminé correctement.

**Remarque**  
Si vous avez enregistré tous les fichiers localement et pas directement sur le média amovible, assurez-vous de copier uniquement le contenu du dossier et non le dossier proprement dit sur le média amovible.



**Remarque**  
Le média amovible doit être suffisamment grand pour que le contenu du package n’utilise que trois quarts de la mémoire du support amovible.



**Remarque**  
Lors de la création du package, un maximum de deux fois la taille de package réelle peut être requis lorsque la build est terminée.



## Rubriques connexes


[Création d'une image MED-V](creating-a-med-v-image.md)









