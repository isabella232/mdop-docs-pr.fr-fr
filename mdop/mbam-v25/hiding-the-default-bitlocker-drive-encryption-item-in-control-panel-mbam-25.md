---
title: Masquage de l'élément de chiffrement de lecteur BitLocker par défaut dans le Panneau de configuration
description: Masquage de l'élément de chiffrement de lecteur BitLocker par défaut dans le Panneau de configuration
author: dansimp
ms.assetid: 6e2a9a02-a809-43a1-80a3-1b03c7192c89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af395928ca8934bfea4eeb848bbd4ee377987293
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809750"
---
# Masquage de l'élément de chiffrement de lecteur BitLocker par défaut dans le Panneau de configuration


Cette rubrique décrit comment masquer l’élément de panneau de configuration du **chiffrement de lecteurs BitLocker** , qui apparaît par défaut dans le panneau de configuration dans le cadre du système d’exploitation Windows.

**Remarques**  Le système d’administration et de surveillance de BitLocker Microsoft (MBAM) crée un élément de panneau de configuration personnalisé supplémentaire, appelé **options de chiffrement BitLocker**, qui permet aux utilisateurs finaux de gérer leur code confidentiel et leur mot de passe, d’activer BitLocker pour un lecteur et de vérifier le chiffrement.

 

Pour en savoir plus [, voir présentation des options de chiffrement de BitLocker et des éléments de chiffrement de lecteur BitLocker dans le panneau de configuration](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) :

-   Différences entre le MBAM et les éléments du panneau de configuration par défaut

-   Menu contextuel **gérer BitLocker** qui s’affiche lorsque vous cliquez avec le bouton droit sur un lecteur dans l’Explorateur Windows

**Important**  Ne modifiez pas les paramètres de stratégie de groupe du nœud **BitLocker Drive Encryption** . Si tel est le cas, MBAM ne fonctionnera pas correctement. Lorsque vous configurez les paramètres de stratégie de groupe dans le nœud **MDOP MBAM (gestion du BitLocker)** , MBAM configure automatiquement les paramètres de **chiffrement de lecteur BitLocker** pour vous.

 

**Pour masquer l’élément de chiffrement de lecteur BitLocker par défaut dans le panneau de configuration**

1.  Dans la console de gestion des stratégies de groupe (GPMC) ou dans la gestion avancée des stratégies de groupe, accédez au panneau de configuration modèles de **Configuration des utilisateurs** &gt; **Policies** &gt; **Administrative Templates** &gt; **Control Panel**.

2.  Dans le volet **Détails** , double-cliquez sur **Masquer les éléments du panneau de configuration spécifiés**, puis cliquez sur **activé**.

3.  Cliquez sur **Afficher**, puis sur **Ajouter**et tapez **Microsoft. BitLockerDriveEncryption**.



## Rubriques connexes


[Présentation des éléments Options de chiffrement BitLocker et Chiffrement de lecteur BitLocker du Panneau de configuration](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md)

[Déploiement d'objets de stratégie de groupe MBAM2.5](deploying-mbam-25-group-policy-objects.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





