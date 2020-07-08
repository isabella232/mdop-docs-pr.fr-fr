---
title: Procédure de récupération d'un lecteur en mode de récupération
description: Procédure de récupération d'un lecteur en mode de récupération
author: dansimp
ms.assetid: e126eaf8-9ae7-40fe-a28e-dbd78d26859e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d15f33f461e60fceeed3acbce3a0c82b02b56f98
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809912"
---
# Procédure de récupération d'un lecteur en mode de récupération


Cette rubrique explique comment utiliser le site Web d’administration et de contrôle (également appelé support technique) pour obtenir un mot de passe de récupération à mettre aux utilisateurs finaux si leur lecteur protégé par BitLocker passe en mode de récupération. Les lecteurs se trouvent dans le mode de récupération si les utilisateurs perdent ou oublient leur code confidentiel ou leur mot de passe, ou si le processeur de plateforme sécurisée (TPM) détecte des modifications apportées aux fichiers du BIOS ou de démarrage d’un ordinateur.

Pour obtenir un mot de passe de récupération, utilisez la zone de **récupération de lecteur** du site Web d’administration et de surveillance. Vous devez être attribué au rôle utilisateurs du support technique MBAM ou au rôle MBAM Advanced helpdesk Users pour accéder à cette zone du site Web.

**Remarque**  
Il est possible que vous ayez attribué un nom différent aux rôles lorsque vous les avez créés. Pour plus d’informations, reportez-vous [à planification pour les comptes et groupes MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).



**Important**  
Expiration des mots de passe de récupération après une utilisation unique. Sur les lecteurs du système d’exploitation et les lecteurs de données fixes, la règle à utilisation unique est appliquée automatiquement. Sur les lecteurs amovibles, il est appliqué lors de la suppression du lecteur, puis réinséré et déverrouillé sur un ordinateur qui a activé les paramètres de stratégie de groupe pour gérer les lecteurs amovibles.



**Pour récupérer un lecteur en mode de récupération**

1.  Ouvrez un navigateur Web, puis accédez au **site Web d’administration et de surveillance**.

2.  Dans le volet gauche, sélectionnez **récupération de lecteur** pour ouvrir la page **récupérer l’accès à un lecteur chiffré** .

3.  Entrez le nom d’utilisateur et le domaine d’ouverture de session Windows de l’utilisateur final pour afficher les informations de récupération.

    **Remarque**  
    Si vous vous trouvez dans le groupe utilisateurs du support technique avancé MBAM, les champs utilisateur et ID d’utilisateur ne sont pas obligatoires.



4.  Entrez les huit premiers chiffres de l’ID de clé de récupération pour afficher une liste des clés de récupération correspondantes possibles, ou entrez l’ID de la clé de récupération complète pour obtenir la clé de récupération exacte.

5.  Dans la liste **raison de la déverrouillage du lecteur** , sélectionnez l’une des options prédéfinies, puis cliquez sur **valider**.

    MBAM renvoie la valeur suivante:

    -   Message d’erreur s’il n’existe aucun mot de passe de récupération correspondant

    -   Plusieurs correspondances possibles si l’utilisateur possède plusieurs mots de passe de récupération correspondants

    -   Le mot de passe de récupération et le package de récupération pour l’utilisateur soumis

        **Remarque**  
        Si vous récupérez un lecteur endommagé, l’option de package de récupération fournit les informations critiques de BitLocker dont il a besoin pour récupérer le lecteur.



~~~
After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

6. Pour copier le mot de passe, cliquez sur **copier la clé**, puis collez le mot de passe de récupération dans un message électronique. Vous pouvez également cliquer sur **Enregistrer** pour enregistrer le mot de passe de récupération dans un fichier.

   Lorsque l’utilisateur tape le mot de passe de récupération dans le système ou utilise le package de récupération, le lecteur est déverrouillé.



## Rubriques connexes


[Gestion de BitLocker avec MBAM2.5](performing-bitlocker-management-with-mbam-25.md)



## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





