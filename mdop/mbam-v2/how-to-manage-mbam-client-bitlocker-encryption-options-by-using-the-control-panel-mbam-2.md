---
title: Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration
description: Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration
author: dansimp
ms.assetid: e2ff153e-5770-4a12-b79d-cda998b8a8ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a42901ac9d8a1a3527712f4cf342b5c0ca9ffdfd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810956"
---
# Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration


Une application du panneau de configuration Microsoft BitLocker d’administration et de surveillance (MBAM) Microsoft, appelée options de chiffrement BitLocker, sera disponible sous **système et sécurité** lorsque le client d’administration et de surveillance Microsoft BitLocker sera installé. Ce panneau de configuration MBAM personnalisé est un panneau de configuration supplémentaire. Cela ne remplace pas le panneau de configuration Windows BitLocker par défaut. Le panneau de configuration MBAM peut être utilisé pour déverrouiller les disques durs fixes et amovibles chiffrés et gérer également votre code confidentiel ou votre mot de passe. Pour plus d’informations sur l’activation du panneau de configuration MBAM, voir [comment masquer le chiffrement BitLocker par défaut dans le panneau de configuration Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md).

**Pour utiliser le panneau de configuration du client MBAM**

1.  Pour ouvrir les options de chiffrement BitLocker, cliquez sur **Démarrer** , puis sélectionnez **panneau de configuration**. Lorsque **le panneau de configuration** s’ouvre, sélectionnez **système et sécurité**.

2.  Double-cliquez sur **options de chiffrement BitLocker** pour ouvrir le panneau de configuration MBAM personnalisé. Vous verrez la liste de tous les disques durs de votre ordinateur et leur état de chiffrement, en plus d’une option de gestion de votre code confidentiel ou de votre mot de passe.

    La liste des disques durs de l’ordinateur peut être utilisée pour vérifier le statut de chiffrement, déverrouiller un lecteur ou demander une exemption de protection de BitLocker si les stratégies d’exemption des utilisateurs et des ordinateurs ont été déployées.

    Le panneau de configuration options de chiffrement BitLocker autorise également les utilisateurs non administrateurs à gérer leur code confidentiel ou leur mot de passe. En sélectionnant **gérer le code confidentiel**, les utilisateurs sont invités à entrer un code confidentiel actuel et un nouveau code confidentiel (en plus de confirmer le nouveau code confidentiel). Le choix de **mettre à jour le code confidentiel** entraîne la réinitialisation du code confidentiel.

    Pour gérer votre mot de passe, sélectionnez **verrouiller le lecteur** et entrez votre mot de passe actuel. Dès que le lecteur est déverrouillé, sélectionnez **Réinitialiser le mot de passe** pour modifier votre mot de passe actuel.

## Rubriques connexes


[Administration des composants de MBAM2.0](administering-mbam-20-features-mbam-2.md)

 

 





