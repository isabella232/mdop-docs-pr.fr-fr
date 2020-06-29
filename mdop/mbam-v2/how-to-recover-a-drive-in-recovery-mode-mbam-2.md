---
title: Procédure de récupération d'un lecteur en mode de récupération
description: Procédure de récupération d'un lecteur en mode de récupération
author: dansimp
ms.assetid: 8b792bc8-b671-4345-9d37-0208db3e5b03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d5ce509599d0eb800a71360e3be9d0fa3b33f4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810926"
---
# Procédure de récupération d'un lecteur en mode de récupération


Les fonctionnalités de récupération de lecteur chiffrées de l’administration et de la surveillance de BitLocker (MBAM) permettent de capturer et de stocker les données et la disponibilité des outils requis pour accéder au volume protégé par BitLocker lorsque BitLocker passe en mode récupération. Un volume protégé par BitLocker est intégré au mode de récupération lors de la perte ou de l’oubli d’un code confidentiel ou d’un mot de passe, ou lorsque le processeur de plateforme sécurisée détecte des modifications apportées aux fichiers du BIOS ou de démarrage d’un ordinateur.

Utilisez cette procédure pour accéder au système de données de récupération de clés centralisées, qui peut fournir un mot de passe de récupération si un ID de mot de passe de récupération et un identificateur d’utilisateur associé sont fournis.

**Important**  
L’analyse et l’administration de BitLocker utilise des clés de récupération à utilisation unique qui expirent lors de l’utilisation. L’utilisation unique d’un mot de passe de récupération est appliquée automatiquement aux lecteurs du système d’exploitation et aux disques durs fixes. Sur les lecteurs amovibles, il est appliqué lors de la suppression du lecteur, puis de nouveau l’insertion et le déverrouillage sur un ordinateur qui a activé les paramètres de stratégie de groupe pour gérer les lecteurs amovibles.



**Pour récupérer un lecteur en mode de récupération**

1.  Ouvrez un navigateur Web, puis accédez au site Web d’administration et de surveillance.

2.  Dans le volet de navigation, cliquez sur **récupération de lecteur**. La page Web «récupérer l’accès à un lecteur chiffré» s’ouvre.

3.  Entrez le domaine d’ouverture de session Windows et le nom d’utilisateur de l’utilisateur pour afficher les informations de récupération et les huit premiers chiffres de l’ID de clé de récupération pour recevoir une liste de clés de récupération correspondantes, ou l’ID de la clé de récupération complète pour recevoir la clé de récupération exacte.

4.  Sélectionnez l’une des options prédéfinies dans la liste **raison pour le verrouillage du lecteur** , puis cliquez sur **valider**.

    **Remarque**  
    Si vous êtes un utilisateur d’assistance technique avancée MBAM, les entrées de domaine et d’ID d’utilisateur ne sont pas obligatoires.



~~~
MBAM returns the following:

-   An error message if no matching recovery password is found

-   Multiple possible matches if the user has multiple matching recovery passwords

-   The recovery password and recovery package for the submitted user

    **Note**  
    If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.



After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

5. Pour copier le mot de passe, cliquez sur **copier la clé**, puis collez le mot de passe de récupération dans un message électronique. Vous pouvez également cliquer sur **Enregistrer** pour enregistrer le mot de passe de récupération dans un fichier.

   Lorsque l’utilisateur tape le mot de passe de récupération dans le système ou utilise le package de récupération, le lecteur est déverrouillé.

## Rubriques connexes


[Gestion de BitLocker avec MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)









