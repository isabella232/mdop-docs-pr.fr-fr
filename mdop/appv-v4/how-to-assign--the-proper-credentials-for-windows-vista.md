---
title: Comment affecter les informations d’identification appropriées pour Windows Vista
description: Comment affecter les informations d’identification appropriées pour Windows Vista
author: dansimp
ms.assetid: cc11d2af-a350-4d16-ba7b-f9c1d89e14b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 111dafea505133f123cf8531a2891a452e725ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808712"
---
# Comment affecter les informations d’identification appropriées pour Windows Vista


Utilisez la procédure suivante pour configurer le client de bureau App-V pour les informations d’identification Vista appropriées.

**Remarques**  Cette procédure doit être effectuée sur tous les ordinateurs non membres du domaine. En fonction du nombre d’ordinateurs appartenant à un domaine différent dans votre environnement, il peut s’agir d’une opération laborieuse. Vous pouvez utiliser les scripts et l’interface de ligne de commande pour le gestionnaire d’informations d’identification pour aider les administrateurs à automatiser ce processus.

 

**Pour attribuer les informations d’identification appropriées pour les clients App-V exécutant Windows Vista**

1.  Pour les privilèges d’administrateur sur le client de bureau App-V exécutant Windows Vista, ouvrez le panneau de configuration des **comptes d’utilisateurs** (panneau de configuration classique).

2.  Sélectionnez **gérer vos mots de passe réseau** dans les **comptes d’utilisateurs** dans le volet tâches de gauche.

3.  Sélectionnez **Ajouter** dans l’écran **noms et mots de passe des utilisateurs enregistrés** .

4.  Dans l’écran **propriétés d’informations d’identification stockées** , entrez les informations relatives à l’infrastructure App-V:

    1.  **Connectez-vous à:** Nom externe du serveur de publication.

    2.  **Nom d’utilisateur:** Nom d’utilisateur de l’utilisateur externe sous la forme Domain\\Username.

    3.  **Mot de passe:** Mot de passe du compte d’utilisateur entré dans le champ **nom d’utilisateur** .

    4.  Laissez **type d’informations d’identification** sélectionné, puis cliquez sur **OK**.

5.  Cliquez sur **Fermer**. Les informations d’identification sont stockées dans le magasin d’informations d’identification pour une authentification correcte auprès de l’infrastructure App-V.

## Rubriques connexes


[Clients joints au domaine et non joints au domaine](domain-joined-and-non-domain-joined-clients.md)

[Comment affecter les informations d’identification appropriées pour Windows XP](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





