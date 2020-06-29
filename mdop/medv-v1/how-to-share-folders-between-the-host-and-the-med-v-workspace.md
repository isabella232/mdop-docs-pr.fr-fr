---
title: Comment partager des dossiers entre l'hôte et l'espace de travail MED-V
description: Comment partager des dossiers entre l'hôte et l'espace de travail MED-V
author: dansimp
ms.assetid: 3cb295f2-c07e-4ee6-aa3c-ce4c8c45c191
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 87f315c9894cd38834413d2549e652a36c5cc16d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811345"
---
# Comment partager des dossiers entre l'hôte et l'espace de travail MED-V


Vous pouvez partager des dossiers entre l’hôte et l’espace de travail MED-V. Les dossiers partagés peuvent être stockés comme suit:

-   Un ordinateur externe sur le réseau

-   Ordinateur hôte

Les procédures suivantes vous montrent comment partager des dossiers entre l’hôte et l’espace de travail MED-V.

**Pour partager des dossiers situés sur le réseau**

1.  Configurez MED-V en mode Bureau complet.

2.  Dans gestion MED-V, sous l’onglet réseau, cliquez sur **utiliser une adresse IP différente de celle**de l’hôte.

3.  Procédez comme suit sur l’ordinateur hôte:

    1.  Dans le panneau de configuration, cliquez sur **afficher l’État et les tâches du réseau**, puis définissez **découverte réseau** sur **activé**.

    2.  Dans le menu Démarrer, cliquez avec le bouton droit sur **ordinateur**, puis cliquez sur **mapper le lecteur réseau**.

    3.  Dans la boîte de dialogue **connecter un lecteur réseau** , dans le champ **lecteur** , sélectionnez un lecteur.

        **Remarques**  Vérifiez que la même lettre de lecteur n’est pas utilisée sur les deux ordinateurs.

         

    4.  Cliquez sur **Parcourir**.

    5.  Dans la boîte de dialogue **Rechercher un dossier** , accédez au lecteur partagé, puis cliquez sur **OK**.

    6.  Cliquez sur **Terminer**.

4.  Répétez l’étape 3 dans l’espace de travail MED-V. Pointez sur le même lecteur que sur l’ordinateur hôte.

**Pour partager des dossiers situés sur l’hôte**

1.  Configurez le dossier à partager avec les autorisations appropriées.

2.  À partir de l’espace de travail MED-V, accédez à **Mes emplacements réseau** et recherchez le dossier partagé.

3.  À partir de l’espace de travail MED-V, recherchez le dossier partagé.

**Remarques**  Assurez-vous que les ordinateurs d’espace de travail hôte et MED-V se trouvent dans le même domaine ou groupe de travail.

 

 

 





