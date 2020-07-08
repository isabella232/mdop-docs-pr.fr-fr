---
title: Comment configurer les propriétés du modèle de nom d'ordinateur virtuel
description: Comment configurer les propriétés du modèle de nom d'ordinateur virtuel
author: dansimp
ms.assetid: ddf79ace-8cc3-4ee6-be5a-5940b4df5c36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa171712b6624b73fb5e0756aaf56277baa4c8cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812138"
---
# Comment configurer les propriétés du modèle de nom d'ordinateur virtuel


Un modèle de nom d’ordinateur de machine virtuelle peut être attribué à la fois pour revertible et pour les espaces de travail MED-V persistants.

-   Revertible: les administrateurs peuvent affecter un nom unique à chaque instance d’espace de travail MED-V pour faire la distinction entre plusieurs ordinateurs utilisant le même espace de travail MED-V.

-   Permanent: dans un espace de travail MED-V persistant, les administrateurs peuvent configurer un ordinateur à renommer au cours d’un script d’installation.

## Comment affecter un modèle de nom d’ordinateur virtuel à un espace de travail Revertible MED-V


**Pour affecter un modèle de nom d’ordinateur virtuel à un espace de travail revertible MED-V**

1.  Cliquez sur l’espace de travail revertible MED-V pour le configurer.

2.  Dans la section **installation de REVERTIBLE VM** , activez la case à cocher **Renommer l’ordinateur virtuel en fonction de votre modèle de nom d’ordinateur** .

3.  Dans la section modèle de nom de l' **ordinateur VM** , entrez le modèle à utiliser pour nommer les images d’machines virtuelles, à l’aide des options suivantes:

    -   **Constante**: entrez du texte libre qui sera constant sur tous les ordinateurs qui utilisent l’espace de travail MED-V.

    -   **Variable**: entrez une variable, en cliquant sur **Insérer une variable**, puis effectuez l’une des opérations suivantes:

        -   **Nom d’utilisateur**

        -   **Nom de domaine**

        -   **Nom de l'hôte**

        -   **Nom de l’espace de travail**

        -   **Nom de l’ordinateur virtuel**

        La variable sélectionnée sera spécifique à l’ordinateur qui utilise l’espace de travail MED-V. Par exemple, si vous sélectionnez **Domain Name (nom de domaine** ), le nom unique de chaque ordinateur inclut le nom de domaine de l’ordinateur.

    -   **Caractères aléatoires**: entrez «\ #» pour chaque caractère aléatoire à inclure dans le modèle. Chaque ordinateur qui utilise l’espace de travail MED-V dispose d’un suffixe de longueur spécifiée, qui est généré de manière aléatoire.

    **Remarque**  
    Le nom de l’ordinateur est limité à 15 caractères. Si le modèle dépasse la limite, il est tronqué.



4.  Dans le menu **stratégie** , cliquez sur **valider**.

    **Remarque**  
    Un modèle de nom d’ordinateur revertible VM peut être attribué uniquement lors de l’attribution d’un **nom à l’ordinateur virtuel en fonction des modèles de nom** de l’ordinateur (dans la section Configuration de l’ordinateur **virtuel revertible** ) est coché.



~~~
**Note**  
A unique computer name can be assigned only if it is configured prior to MED-V workspace setup. Changing the name will not affect MED-V workspaces that were already set up.
~~~



## Comment affecter un modèle de nom d’ordinateur virtuel à un espace de travail MED-V permanent


**Pour affecter un modèle de nom d’ordinateur virtuel à un espace de travail MED-V permanent**

1.  Cliquez sur l’espace de travail MED-V permanent à configurer.

2.  Dans la section **installation d’un VM persistante** , cliquez sur **éditeur de script**.

3.  Dans la boîte de dialogue **actions de script** , cliquez sur **Ajouter**, puis dans le sous-menu, cliquez sur **Renommer un ordinateur**.

4.  Cliquez sur **OK** pour fermer la boîte de dialogue **actions de script** .

5.  Dans l’onglet Configuration de l’ordinateur **virtuel** , dans la section modèle de nom de l' **ordinateur VM** , entrez le modèle à utiliser pour renommer l’ordinateur, en procédant comme suit:

    -   **Constante**: entrez le texte libre qui sera inclus dans le nom de l’ordinateur.

    -   **Variable**: entrez une variable, en cliquant sur **Insérer une variable**, puis effectuez l’une des opérations suivantes:

        -   **Nom d’utilisateur**

        -   **Nom de domaine**

        -   **Nom de l'hôte**

        -   **Nom de l’espace de travail**

        -   **Nom de l’ordinateur virtuel**

        Les variables sélectionnées seront spécifiques de l’ordinateur renommé. Par exemple, si le **nom de domaine** est sélectionné, le nom de l’ordinateur inclut le nom de domaine de l’ordinateur.

    -   **Caractères aléatoires**: entrez «\ #» pour chaque caractère aléatoire à inclure dans le modèle. L’ordinateur aura un suffixe de longueur spécifiée, qui est généré de manière aléatoire.

    **Remarque**  
    Le nom de l’ordinateur est limité à 15 caractères. Si le modèle dépasse la limite, il est tronqué.



6.  Dans le menu **stratégie** , cliquez sur **valider**.

    **Remarque**  
    L’ordinateur est renommé uniquement s’il est défini comme action dans la boîte de dialogue **actions de script** . Pour plus d’informations, reportez-vous [à la rubrique Configuration d’actions de script](how-to-set-up-script-actions.md).



## Rubriques connexes


[Utilisation de l'interface utilisateur de la console de gestion MED-V](using-the-med-v-management-console-user-interface.md)

[Création d'un espace de travail MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Comment configurer des actions de script](how-to-set-up-script-actions.md)

[Exemples de configurations d'ordinateur virtuel](examples-of-virtual-machine-configurationsv2.md)









