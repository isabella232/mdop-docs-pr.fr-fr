---
title: Récupération d'un lecteur endommagé
description: Récupération d'un lecteur endommagé
author: dansimp
ms.assetid: 715491ae-69c0-4fae-ad3f-3bd19a0db2f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 545ff5c7e6bea29d5f89cce1cf18212b7d0e2870
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804608"
---
# Récupération d'un lecteur endommagé


Pour récupérer un lecteur endommagé qui a été protégé par BitLocker, un utilisateur du support technique Microsoft BitLocker (MBAM) doit créer un fichier de package de clé de récupération. Ce fichier de package peut être copié sur l’ordinateur qui contient le lecteur endommagé, puis utilisé pour récupérer le lecteur. Pour cela, procédez comme suit.

**Pour récupérer un lecteur endommagé**

1.  Ouvrez le site Web d’administration MBAM.

2.  Dans le volet de navigation, sélectionnez **récupération de lecteur** . Entrez le nom de domaine et le nom d’utilisateur de l’utilisateur, la raison pour laquelle vous avez déverrouillé le lecteur et l’ID du mot de passe de récupération de l’utilisateur.

    **Remarques**  Si vous êtes membre du rôle Administrateurs du support technique, vous n’êtes pas obligé d’entrer le nom de domaine ou le nom d’utilisateur de l’utilisateur.

     

3.  Cliquez sur **Envoyer**. La clé de récupération s’affiche.

4.  Cliquez sur **Enregistrer**, puis sélectionnez **package de clé de récupération**. Le package de clé de récupération sera créé sur votre ordinateur.

5.  Copiez le package de clé de récupération sur l’ordinateur sur lequel le lecteur est endommagé.

6.  Ouvrez une invite de commandes avec élévation de privilèges. Pour cela, cliquez sur **Démarrer** , puis tapez `cmd` dans la zone **Rechercher les programmes et fichiers** . Dans la liste résultats de la recherche, cliquez avec le bouton droit sur **cmd.exe** et sélectionnez **exécuter en tant qu’administrateur**.

7.  À l’invite de commandes, tapez ce qui suit:

    `repair-bde <fixed drive> <corrupted drive> -kp <location of keypackage> -rp <recovery password>`

    **Remarques**  Pour le &lt; lecteur fixe &gt; dans la commande, spécifiez un périphérique de stockage disponible dont l’espace disponible est supérieur ou égal à la taille des données sur le disque endommagé. Les données du lecteur endommagé sont récupérées et déplacées vers le lecteur fixe indiqué.

     

## Rubriques connexes


[Gestion de BitLocker avec MBAM](performing-bitlocker-management-with-mbam.md)

 

 





