---
title: Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration
description: Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration
author: dansimp
ms.assetid: c08077e1-5529-468f-9370-c3b33fc258f3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 271147d0e5581f6ce49fe0b46aa83dae6ae4556b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804615"
---
# Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration


Une application du panneau de configuration Microsoft BitLocker administration et surveillance (MBAM), appelée options de chiffrement BitLocker, sera disponible sous **système et sécurité** lorsque le client MBAM est installé. Ce panneau de configuration MBAM personnalisé remplace le panneau de configuration Windows BitLocker par défaut. Le panneau de configuration MBAM vous permet de déverrouiller des lecteurs chiffrés (résolus et amovibles) et de gérer également votre code confidentiel ou votre mot de passe. Pour plus d’informations sur l’activation du panneau de configuration MBAM, voir [comment masquer le chiffrement BitLocker par défaut dans le panneau de configuration Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md).

**Remarques**  Pour le client BitLocker, les fichiers du journal d’administration et du journal opérationnel sont situés dans l’observateur d’événements, sous **applications et services consignent**  /  **Microsoft**  /  **Windows**  /  **BitLockerManagement**.

 

**Pour utiliser le panneau de configuration du client MBAM**

1.  Pour ouvrir les options de chiffrement BitLocker, cliquez sur **Démarrer**, puis sélectionnez **panneau de configuration**. Lorsque **le panneau de configuration** s’ouvre, sélectionnez **système et sécurité**.

2.  Double-cliquez sur **options de chiffrement BitLocker** pour ouvrir le panneau de configuration MBAM personnalisé. La liste de tous les disques durs de l’ordinateur s’affiche, ainsi que leur état de cryptage. Vous verrez également une option permettant de gérer votre code confidentiel ou vos mots de passe.

3.  Utilisez la liste des disques durs de l’ordinateur pour vérifier le statut de chiffrement, déverrouiller un lecteur ou demander une exemption pour la protection de BitLocker si les stratégies d’exemption des utilisateurs et des ordinateurs ont été déployées.

4.  Les non-administrateurs peuvent utiliser le panneau de configuration options de chiffrement de BitLocker pour gérer les codes confidentiels ou mots de passe. Un utilisateur peut sélectionner **gérer le code confidentiel,** puis entrer un code confidentiel actuel et un nouveau code secret. Les utilisateurs peuvent également confirmer leur nouveau code secret. La fonction de **mise à jour de l’épingle** rétablit le code confidentiel en nouveau que l’utilisateur sélectionne.

5.  Pour gérer votre mot de passe, sélectionnez **verrouiller le lecteur** et entrez votre mot de passe actuel. Dès que le lecteur est déverrouillé, sélectionnez **Réinitialiser le mot de passe** pour modifier votre mot de passe actuel.

## Rubriques connexes


[Administration des composants de MBAM1.0](administering-mbam-10-features.md)

 

 





