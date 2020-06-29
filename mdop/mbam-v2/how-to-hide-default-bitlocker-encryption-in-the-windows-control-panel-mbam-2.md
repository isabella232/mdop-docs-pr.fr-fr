---
title: Comment masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows
description: Comment masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows
author: dansimp
ms.assetid: 6674aa51-2b5d-4e4a-8b43-2cc18d008285
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eda8fafbd7b3ebf414520354eba6def2e97f6237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810343"
---
# Comment masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows


Le système d’administration et de surveillance de BitLocker Microsoft (MBAM) propose un panneau de configuration personnalisé pour l’administration et la surveillance de l’ordinateur client par Microsoft BitLocker, appelés options de chiffrement de BitLocker. Ce panneau de configuration personnalisé peut remplacer le panneau de configuration Windows BitLocker par défaut, qui est appelé chiffrement de lecteur BitLocker. Le panneau de configuration personnalisé, qui se trouve dans le panneau de configuration, sous système et sécurité, permet aux utilisateurs de gérer leur code confidentiel et leur mot de passe, de déverrouiller les lecteurs et de masquer l’interface permettant aux administrateurs de déchiffrer un lecteur ou de suspendre ou de reprendre le chiffrement de lecteur BitLocker.

**Pour masquer le chiffrement de lecteur BitLocker par défaut dans le panneau de configuration Windows**

1.  Dans la console de gestion des stratégies de groupe (GPMC), la gestion avancée de la stratégie de groupe (AGPM) ou l’éditeur de stratégie de groupe locale sur l’ordinateur stratégies de groupe BitLocker, accédez à **Configuration utilisateur**.

2.  Cliquez ensuite sur **stratégies**, sélectionnez **modèles d’administration**, puis cliquez sur **panneau de configuration**.

3.  Double-cliquez sur **Masquer les éléments du panneau de configuration spécifiés** dans le volet **Détails** , puis sélectionnez **activé**.

4.  Cliquez sur **Afficher**, puis sur **Ajouter**et tapez **Microsoft. BitLockerDriveEncryption**. Cette stratégie masque l’outil de gestion de BitLocker Windows par défaut dans le panneau de configuration Windows, puis, dans le panneau de configuration, il permet à l’utilisateur d’ouvrir l’outil mise à jour MBAM BitLocker options dans système et sécurité.

## Rubriques connexes


[Déploiement d'objets de stratégie de groupe MBAM2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





