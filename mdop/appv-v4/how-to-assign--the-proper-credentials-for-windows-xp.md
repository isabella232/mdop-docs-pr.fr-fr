---
title: Comment affecter les informations d’identification appropriées pour Windows XP
description: Comment affecter les informations d’identification appropriées pour Windows XP
author: dansimp
ms.assetid: cddbd556-d8f9-4981-a947-6e8e3f552b70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81581b75a9b7d5ce35e1c50fd01e0b7bbd3f7ef5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807861"
---
# Comment affecter les informations d’identification appropriées pour Windows XP


Utilisez la procédure suivante pour configurer le client de bureau App-V pour les informations d’identification WindowsXP appropriées.

**Remarques**  Après avoir terminé cette procédure, le client sans domaine joint peut effectuer une actualisation de publication sans être joint à un domaine.

 

**Pour attribuer les informations d’identification appropriées pour les clients App-V exécutant WindowsXP**

1.  Si vous disposez de privilèges d’administrateur sur le client App-V exécutant WindowsXP, ouvrez le panneau de configuration des **comptes d’utilisateurs** (panneau de configuration classique).

2.  Cliquez sur l' **onglet Avancé**, puis sélectionnez **gérer les mots de passe**.

3.  Dans l’écran **noms d’utilisateur et mots de passe enregistrés** , cliquez sur **Ajouter**.

4.  Dans l’écran de **Propriétés informations de connexion** , renseignez les champs suivants avec les informations de l’infrastructure App-V:

    1.  **Serveur:** Nom du nom externe du serveur de publication.

    2.  **Nom d’utilisateur:** Nom d’utilisateur de l’utilisateur externe sous la forme Domain\\username.

    3.  **Mot de passe:** Mot de passe du compte d’utilisateur entré dans le champ **nom d’utilisateur** .

5.  Cliquez sur **OK**. Les informations d’identification seront stockées sur le client.

## Rubriques connexes


[Clients joints au domaine et non joints au domaine](domain-joined-and-non-domain-joined-clients.md)

[Comment affecter les informations d’identification appropriées pour Windows Vista](how-to-assign--the-proper-credentials-for-windows-vista.md)

 

 





