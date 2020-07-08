---
title: Procédure pour ajouter une version de package
description: Procédure pour ajouter une version de package
author: dansimp
ms.assetid: dbb829c1-e5cb-4a2f-bc17-9a9bb50c671c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a60252e8b43af61ad548df30a93d8fbc9bae0cb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808735"
---
# Procédure pour ajouter une version de package


Dans la console de gestion de l’application virtualisation du serveur, lorsque vous recommandez un package, vous pouvez utiliser la procédure suivante pour ajouter la nouvelle version à vos serveurs pour la diffusion en continu.

**Remarques**  Lorsque vous effectuez une mise à niveau d’un package avec une nouvelle version, vous pouvez laisser la version existante en place ou la supprimer et ne conserver que la plus récente. Vous souhaiterez peut-être conserver l’ancienne version en vigueur pour la compatibilité avec les documents hérités ou pour tester la nouvelle version avant de la rendre disponible pour tous les utilisateurs.

 

**Pour ajouter une version de package**

1.  Copiez le nouveau fichier SFT dans le dossier Content du serveur d’applications. Si le reséquençage n’a pas ajouté de modifications aux fichiers Open Software Descriptor (OSD), Icon ou Sequencer (SPRJ), vous n’avez pas besoin de les copier. Vous pouvez inclure ces fichiers si vous souhaitez que tous les fichiers affichent la même date.

2.  Dans le volet gauche de la console de gestion du serveur d’applications, développez le nœud **packages** .

3.  Cliquez avec le bouton droit sur le package que vous voulez mettre à jour, puis choisissez **Ajouter une version**.

4.  Dans la boîte de dialogue **Ajouter une version de package** , recherchez ou tapez le chemin d’accès du nouveau fichier d’application dans le champ chemin d' **accès complet du fichier de package** . Il doit s’agir d’un fichier SFT.

5.  Cliquez sur **Suivant**.

6.  La boîte de dialogue **récapitulative** montre l’emplacement du fichier et vous invite à le faire si vous ne l’avez pas déjà fait. Cliquez sur **Terminer** une fois que vous avez vérifié les informations.

    La nouvelle version est maintenant terminée et prête à être diffusée.

## Rubriques connexes


[Procédure pour supprimer un package](how-to-delete-a-packageserver.md)

[Procédure pour gérer les packages dans Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 





