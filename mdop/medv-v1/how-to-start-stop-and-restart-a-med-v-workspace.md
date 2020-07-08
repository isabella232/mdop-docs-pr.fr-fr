---
title: Comment démarrer, arrêter et redémarrer un espace de travail MED-V
description: Comment démarrer, arrêter et redémarrer un espace de travail MED-V
author: dansimp
ms.assetid: 54ce139c-8f32-499e-944b-72f123ebfd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2739ace085a4d57d333daf7872e01a7712a7fbd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811327"
---
# Comment démarrer, arrêter et redémarrer un espace de travail MED-V


**Pour créer un espace de travail MED-V**

1.  Dans la zone de notification, cliquez avec le bouton droit sur l’icône MED-V.

2.  Dans le sous-menu, cliquez sur **Démarrer l’espace de travail**.

    -   S’il existe plusieurs espaces de travail MED-V en cours d’exécution sur l’ordinateur, la fenêtre **de sélection de l’espace de travail** s’affiche.

        1.  Sélectionnez un espace de travail MED-V.

        2.  Activez la case à cocher **Démarrer l’espace de travail sélectionné sans m’avertir** pour ignorer cette fenêtre la prochaine fois que le client est démarré et l’ouverture automatique de l’espace de travail MED-V sélectionné.

        3.  Cliquez sur **OK**.

    La fenêtre **Démarrer l’authentification de l’espace de travail** s’affiche.

    -   S’il existe plusieurs espaces de travail MED-V sur l’ordinateur et que vous avez choisi d’utiliser un espace de travail MED-V, la fenêtre affichée dans la figure ci-dessous s’affiche.

        ![](images/medv-logon.gif)

    -   S’il n’y a qu’un seul espace de travail MED-V sur l’ordinateur, l’option «démarrer le dernier espace de travail utilisé» n’est pas disponible.

3.  Entrez les informations d’identification de l’utilisateur de votre domaine.

    **Remarques**  Lors du premier démarrage d’un espace de travail MED-V, le nom d’utilisateur doit présenter le format suivant: nom de &lt; domaine nom d' &gt; \\ &lt; utilisateur &gt; .

     

4.  Sélectionnez **enregistrer mon mot** de passe pour enregistrer votre mot de passe entre les sessions.

    **Remarques**  Pour activer la fonctionnalité enregistrer le mot de passe, l’attribut EnableSavePassword doit être défini sur true dans le fichier ClientSettings.xml. Le fichier se trouve dans le dossier *Servers\\Configuration Server\\* .

     

5.  Décochez la case **Démarrer le dernier espace de travail utilisé** pour choisir un autre espace de travail MED-V.

6.  Cliquez sur **OK**.

    Plusieurs écrans de statut apparaissent en fonction de la configuration de l’espace de travail MED-V.

    L’écran **de démarrage** s’affiche.

**Pour redémarrer une version d’un espace de travail MED-V**

1.  Lorsque le client est en cours d’exécution, dans la zone de notification, cliquez avec le bouton droit sur l’icône MED-V.

2.  Dans le sous-menu, cliquez sur **redémarrer l’espace de travail**.

    L’espace de travail MED-V est redémarré.

    -   Dans un espace de travail MED-V permanent, l’ordinateur virtuel est arrêté, puis redémarré.

    -   Dans un espace de travail MED-V revertible, l’ordinateur virtuel ne s’arrête pas réellement; au lieu de cela, il revient à son état d’origine.

**Pour mettre fin à un espace de travail MED-V**

1.  Dans la zone de notification, cliquez avec le bouton droit sur l’icône MED-V.

2.  Dans le sous-menu, cliquez sur **arrêter l’espace de travail**.

    L’espace de travail MED-V est arrêté.

## Rubriques connexes


[Comment démarrer et quitter le client MED-V](how-to-start-and-exit-the-med-v-client.md)

 

 





