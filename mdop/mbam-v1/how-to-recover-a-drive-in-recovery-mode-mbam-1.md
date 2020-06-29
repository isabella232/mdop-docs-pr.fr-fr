---
title: Procédure de récupération d'un lecteur en mode de récupération
description: Procédure de récupération d'un lecteur en mode de récupération
author: dansimp
ms.assetid: 09d27e4b-57fa-47c7-a004-8b876a49f27e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1151ffe7453eb8d07d2aa6dcb4c41f6b3efe6de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804614"
---
# Procédure de récupération d'un lecteur en mode de récupération


Le contrôle et l’administration de BitLocker Microsoft (MBAM) inclut des fonctionnalités de récupération de lecteur chiffrées. Ces fonctionnalités garantissent la capture et le stockage des données et la disponibilité des outils requis pour accéder au volume protégé par BitLocker lorsque BitLocker place le volume en mode de récupération. Un volume protégé par BitLocker est intégré au mode de récupération lors de la perte ou de l’oubli d’un code confidentiel ou d’un mot de passe, ou lorsque le processeur de plateforme sécurisée (TPM) détecte une modification apportée au BIOS ou aux fichiers de démarrage de l’ordinateur.

Utilisez cette procédure pour accéder au système de données de récupération de clés centralisées qui peut fournir un mot de passe de récupération lorsque l’ID du mot de passe de récupération et l’identificateur d’utilisateur associé sont fournis.

**Important**  MBAM génère des clés de récupération à utilisation unique. Dans le cadre de cette limitation, une clé de récupération ne peut être utilisée qu’une seule fois et n’est plus valide. L’utilisation unique d’un mot de passe de récupération est appliquée automatiquement aux lecteurs du système d’exploitation et aux disques durs fixes. Sur les lecteurs amovibles, la seule utilisation est appliquée lors de la suppression du lecteur, puis de l’insertion et de la désactivation sur un ordinateur qui a activé les paramètres de stratégie de groupe pour gérer les lecteurs amovibles.

 

**Pour récupérer un lecteur en mode de récupération**

1.  Ouvrez le site Web MBAM.

2.  Dans le volet de navigation, cliquez sur **récupération de lecteur**. Le bouton **récupérer l’accès à une page Web de lecteur chiffrée** s’ouvre.

3.  Entrez le domaine d’ouverture de session Windows et le nom d’utilisateur de l’utilisateur, ainsi que les huit premiers chiffres de l’ID de clé de récupération, pour recevoir la liste des clés de récupération correspondantes possibles. Vous pouvez également entrer l’ID de clé de récupération complet pour recevoir la clé de récupération exacte. Sélectionnez l’une des options prédéfinies dans la liste déroulante **raison du verrouillage du lecteur** , puis cliquez sur **valider**.

    **Remarques**  Si vous êtes un utilisateur d’assistance technique avancée MBAM, les entrées de domaine et d’ID d’utilisateur ne sont pas obligatoires.

     

4.  MBAM renvoie la valeur suivante:

    1.  Message d’erreur s’il n’existe aucun mot de passe de récupération correspondant

    2.  Plusieurs correspondances possibles si l’utilisateur possède plusieurs mots de passe de récupération correspondants

    3.  Le mot de passe de récupération et le package de récupération pour l’utilisateur soumis

        **Remarques**  Si vous récupérez un lecteur endommagé, l’option de package de récupération fournit BitLocker avec les informations critiques nécessaires à la récupération.

         

5.  Après l’extraction du mot de passe de récupération et du package de récupération, le mot de passe de récupération s’affiche. Pour copier le mot de passe, cliquez sur **copier la clé**, puis collez le mot de passe de récupération dans un message électronique ou dans un autre fichier texte pour le stockage temporaire. Pour enregistrer le mot de passe de récupération dans un fichier, cliquez sur **Enregistrer**.

6.  Lorsque l’utilisateur tape le mot de passe de récupération dans le système ou utilise le package de récupération, le lecteur est déverrouillé.

## Rubriques connexes


[Gestion de BitLocker avec MBAM](performing-bitlocker-management-with-mbam.md)

 

 





