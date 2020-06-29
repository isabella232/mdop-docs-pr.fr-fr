---
title: Procédure pour mettre à niveau un package
description: Procédure pour mettre à niveau un package
author: dansimp
ms.assetid: 831c7556-6f6c-4b3a-aefb-26889094dc1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a9b3eca2c996337d79e551784818a421f495316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806733"
---
# Procédure pour mettre à niveau un package


Le processus de mise à niveau automatique est le même que pour ajouter une version de package dans la console de gestion du serveur d’applications. Une mise à niveau automatique est effectuée lorsque vous reséquencez l’application dans un package existant. Vous pouvez ensuite ajouter cette nouvelle version à vos serveurs pour la diffusion en continu.

Lorsque vous effectuez une mise à niveau d’un package avec une nouvelle version, vous pouvez laisser la version existante en place ou la supprimer et ne conserver que la plus récente. Vous souhaiterez peut-être conserver l’ancienne version en vigueur pour la compatibilité avec les documents hérités ou pour tester la nouvelle version avant de la rendre disponible pour tous les utilisateurs.

**Pour mettre à niveau un package automatiquement**

1.  Copiez le nouveau fichier SFT dans le dossier de contenu du serveur de virtualisation des applications.

    **Remarques**  Si le reséquençage n’a pas ajouté de fonctionnalités qui ont modifié les fichiers de description de logiciel (OSD), d’icône (ICO) ou de projet de Sequencer (SPRJ), vous n’avez pas besoin de les copier. Vous pouvez inclure ces fichiers si vous souhaitez que ces fichiers affichent la même date.

     

2.  Dans le volet gauche de la console de gestion du serveur d’applications, développez **packages**.

3.  Cliquez avec le bouton droit sur le package que vous voulez mettre à niveau, puis sélectionnez **Ajouter une version**.

4.  Dans la boîte de dialogue **Ajouter une version de package** , recherchez ou tapez le chemin d’accès complet de la nouvelle version de l’application dans le chemin d' **accès complet pour le champ fichier** . Il doit s’agir d’un fichier SFT.

5.  Cliquez sur **Suivant**.

6.  La boîte de dialogue **récapitulative** montre l’emplacement du fichier et vous invite à le faire si vous ne l’avez pas déjà fait. Cliquez sur **Terminer** une fois que vous avez vérifié les informations.

    La nouvelle version est maintenant terminée et prête à être diffusée.

## Rubriques connexes


[Procédure pour gérer les packages dans Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 





