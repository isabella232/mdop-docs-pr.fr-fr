---
title: Récupération d'un lecteur endommagé
description: Récupération d'un lecteur endommagé
author: dansimp
ms.assetid: b0457a00-f72e-4ad8-ab3b-7701851ca87e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5bbd4c2a1f5ef3fde78a9f72c1f77ccb0cdea377
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809617"
---
# Récupération d'un lecteur endommagé


Pour récupérer un lecteur endommagé protégé par BitLocker, un utilisateur du support technique Microsoft BitLocker (MBAM) doit créer un fichier de package de clé de récupération. Ce fichier de package peut alors être copié sur l’ordinateur qui contient le lecteur endommagé, puis utilisé pour récupérer le lecteur. Suivez la procédure ci-dessous pour obtenir la procédure à suivre.

**Important**  Pour éviter une perte de données potentielle, il est vivement recommandé de lire l’aide «réparation-BDE» et de comprendre clairement comment utiliser la commande avant d’exécuter les instructions suivantes.

 

**Pour récupérer un lecteur endommagé**

1.  Pour créer le package de clé de récupération nécessaire pour récupérer un lecteur endommagé, démarrez un navigateur Web et ouvrez le site Web d’administration et de contrôle MBAM.

2.  Dans le volet de navigation gauche, sélectionnez **récupération de lecteur** . Entrez le nom de domaine, le nom d’utilisateur, la raison pour le déverrouillage du lecteur et l’ID du mot de passe de récupération de l’utilisateur.

    **Remarques**  Si vous êtes membre du rôle Administrateurs du support technique, vous n’êtes pas obligé d’entrer le nom de domaine ou le nom d’utilisateur de l’utilisateur.

     

3.  Cliquez sur **Envoyer**. La clé de récupération s’affiche.

4.  Cliquez sur **Enregistrer**, puis sélectionnez **package de clé de récupération**. Le package de clé de récupération sera créé sur votre ordinateur.

5.  Copiez le package de clé de récupération sur l’ordinateur sur lequel le lecteur est endommagé.

6.  Ouvrez une invite de commandes avec élévation de privilèges. Pour cela, cliquez sur **Démarrer** , puis tapez `cmd` dans la **zone Rechercher les programmes et fichiers**. Cliquez avec le bouton droit sur **cmd.exe** et sélectionnez **exécuter en tant qu’administrateur**.

7.  À l’invite de commandes, tapez ce qui suit:

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    **Remarques**  Remplacez &lt; un lecteur fixe &gt; par un disque dur disponible dont l’espace disponible est supérieur ou égal à celui des données sur le disque endommagé. Les données du lecteur endommagé sont récupérées et déplacées sur le disque dur spécifié.

     

## Rubriques connexes


[Gestion de BitLocker avec MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





