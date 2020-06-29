---
title: Utilisation de votre code PIN ou de votre mot de passe
description: Utilisation de votre code PIN ou de votre mot de passe
author: dansimp
ms.assetid: 7fe2aef4-d3e0-49c8-877d-7fee13dc5b7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b8c4b894b8f3e14d2a5cfb39e744fa43874c6753
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810169"
---
# Utilisation de votre code PIN ou de votre mot de passe


BitLocker contribue à sécuriser votre ordinateur en nécessitant un code confidentiel (PIN) ou un mot de passe pour déverrouiller les informations stockées sur votre ordinateur. La configuration requise pour le code confidentiel ou le mot de passe est définie par votre organisation et dépend du type de lecteur chiffré. Les données sur les lecteurs chiffrés ne peuvent pas être affichées sans saisie du code confidentiel ou du mot de passe. Si le matériel de votre ordinateur inclut un module de plateforme sécurisée (TPM) activé, le processeur du TPM vous invite à entrer votre code confidentiel avant le démarrage de Windows sur votre ordinateur.

## À propos de votre code secret et de vos mots de passe BitLocker


Votre entreprise spécifie la complexité requise pour votre code confidentiel ou votre mot de passe. Les exigences de votre code confidentiel ou de votre mot de passe sont expliquées lors du processus de configuration de BitLocker.

Le mot de passe est utilisé pour déverrouiller les lecteurs de votre ordinateur qui ne contiennent pas le système d’exploitation. BitLocker vous demandera votre mot de passe une fois le code confidentiel demandé au démarrage. Chaque disque dur protégé par BitLocker sur votre ordinateur dispose d’un mot de passe unique. Vous ne pouvez pas déverrouiller un lecteur protégé par BitLocker tant que vous n’avez pas fourni votre mot de passe.

**Remarques**  Votre support technique est susceptible de définir le déverrouillage automatique des lecteurs. Cela évite d’avoir à entrer un code confidentiel ou un mot de passe pour afficher les informations sur les lecteurs.

 

## Déverrouille votre ordinateur si vous oubliez votre code confidentiel ou votre mot de passe


Si vous oubliez votre code confidentiel ou votre mot de passe, l’assistance technique peut vous aider à déverrouiller des lecteurs protégés par BitLocker. Pour déverrouiller un lecteur protégé par BitLocker, contactez votre support technique si vous avez besoin d’aide.

**Comment déverrouiller votre ordinateur si vous oubliez votre code confidentiel ou votre mot de passe**

1.  Lorsque vous contactez votre support technique, vous devrez lui fournir les informations suivantes:

    -   Votre nom d’utilisateur

    -   Votre domaine

    -   Les huit premiers chiffres de votre ID de clé de récupération. Il s’agit d’un code à 32 chiffres qui sera affiché par BitLocker si vous oubliez votre code confidentiel ou votre mot de passe.

        -   Si vous oubliez votre code confidentiel, vous devrez entrer les huit premiers chiffres de l’ID de la clé de récupération qui s’afficheront dans la console de récupération BitLocker. La console de récupération BitLocker est un écran antérieur à Windows qui s’affiche si vous n’entrez pas le code confidentiel approprié.

        -   Si vous oubliez votre mot de passe, recherchez l’ID de clé de récupération dans l’application panneau de configuration options de chiffrement BitLocker. Sélectionnez **déverrouiller le lecteur** , puis cliquez sur **j’ai oublié mon mot de passe**. L’application options de chiffrement BitLocker affiche alors un ID de clé de récupération que vous fournissez au support technique.

2.  Lorsque votre support technique reçoit les informations nécessaires, il vous fournira une clé de récupération sur le téléphone ou par courrier électronique.

    -   Si vous avez oublié votre code confidentiel, entrez la clé de récupération dans la console de récupération BitLocker pour déverrouiller votre ordinateur.

    -   Si vous avez oublié votre mot de passe, entrez la clé de récupération dans l’application panneau de configuration options de chiffrement BitLocker, à l’emplacement où vous avez trouvé l’ID de clé de récupération auparavant. Le disque dur protégé est alors déverrouillé.

## Modification de votre code confidentiel ou de votre mot de passe


Pour pouvoir changer le mot de passe sur un lecteur protégé par BitLocker, vous devez déverrouiller le lecteur. Dans le cas contraire, cliquez sur **déverrouiller le lecteur**, puis entrez votre mot de passe actuel. Dès que le lecteur est déverrouillé, vous pouvez sélectionner **gérer votre mot de passe** pour modifier votre mot de passe actuel.

**Modification de votre code confidentiel ou de votre mot de passe**

1.  Cliquez sur **Démarrer**, puis sélectionnez **panneau de configuration**. Le panneau de configuration s’ouvre dans une nouvelle fenêtre.

2.  Cliquez sur **système et sécurité**, puis sélectionnez **options de chiffrement BitLocker**.

    -   Pour modifier votre code confidentiel, sélectionnez **gérer votre code confidentiel**. Tapez votre nouveau code secret dans les deux champs et sélectionnez **Réinitialiser le code confidentiel**.

    -   Pour modifier votre mot de passe, sélectionnez **gérer votre mot de passe**. Entrez votre nouveau mot de passe dans les deux champs et sélectionnez **Reset Password (réinitialiser le mot de passe**).

 

 





