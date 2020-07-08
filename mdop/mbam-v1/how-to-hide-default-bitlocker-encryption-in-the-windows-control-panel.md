---
title: Masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows
description: Masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows
author: dansimp
ms.assetid: c8503743-220c-497c-9785-e2feeca484d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67a61763e556f8c3b93825220dbbd61a14b7d6f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810596"
---
# Masquer le chiffrement BitLocker par défaut dans le Panneau de configuration Windows


Le système d’administration et de surveillance de BitLocker Microsoft (MBAM) propose un panneau de configuration personnalisé pour les ordinateurs clients MBAM appelé options de chiffrement BitLocker. Ce panneau de configuration personnalisé peut remplacer le panneau de configuration Windows BitLocker par défaut qui est appelé chiffrement de lecteur BitLocker. Le panneau de configuration options de chiffrement BitLocker, situé sous système et sécurité dans le panneau de configuration Windows, permet aux utilisateurs de gérer leur code confidentiel et leurs mots de passe, de déverrouiller des lecteurs et de masquer l’interface permettant aux administrateurs de déchiffrer un lecteur ou de suspendre ou de reprendre le chiffrement BitLocker.

**Pour masquer le chiffrement BitLocker par défaut dans le panneau de configuration Windows**

1.  Naviguez jusqu’à la **Configuration utilisateur** à l’aide de la console de gestion des stratégies de groupe (GPMC), de la gestion de la stratégie de groupe avancée (AGPM) ou de l’éditeur de stratégie de groupe locale sur l’ordinateur de stratégies de groupe BitLocker.

2.  Cliquez sur **stratégies**, sélectionnez **modèles d’administration**, puis cliquez sur **panneau de configuration**.

3.  Dans le volet **Détails** , double-cliquez sur **Masquer les éléments du panneau de configuration spécifiés**, puis sélectionnez **activé**.

4.  Cliquez sur **Afficher**, **sur Ajouter...**, puis tapez Microsoft. BitLockerDriveEncryption. Ce paramètre de stratégie masque l’outil de gestion de BitLocker Windows par défaut dans le panneau de configuration Windows, et permet à l’utilisateur d’ouvrir l’outil mise à jour MBAM BitLocker options du panneau de configuration Windows.

## Rubriques connexes


[Déploiement d'objets de stratégie de groupe MBAM1.0](deploying-mbam-10-group-policy-objects.md)

 

 





