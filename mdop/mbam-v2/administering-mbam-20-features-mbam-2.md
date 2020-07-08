---
title: Administration des composants de MBAM2.0
description: Administration des composants de MBAM2.0
author: dansimp
ms.assetid: 065e0704-069e-4372-9b86-0b57dd7638dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 35bb855e185ad8e3fa6880853938074cf6185a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809996"
---
# Administration des composants de MBAM2.0


Après avoir effectué toutes les étapes de planification, puis de déploiement de Microsoft BitLocker administration et surveillance (MBAM), vous pouvez la configurer et l’utiliser pour gérer le chiffrement BitLocker au sein de l’entreprise. les informations dans cette section décrivent les tâches d’administration et de fonctionnalité de surveillance de l’installation de Microsoft BitLocker.

## Gérer les rôles d’administrateur MBAM


Une fois l’installation d’MBAM terminée pour toutes les fonctionnalités du serveur, les utilisateurs administratifs doivent y avoir accès. Il est recommandé que les administrateurs qui gèrent ou utilisent les fonctionnalités du serveur MBAM puissent être assignés aux groupes de sécurité des services de domaine Active Directory (AD FS), et ces groupes doivent être ajoutés au groupe local d’administration MBAM approprié.

[Gérer des rôles d'administrateur MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md)

## Gérer les exemptions de chiffrement BitLocker


MBAM vous permet d’accorder des exemptions de chiffrement à des utilisateurs spécifiques qui n’ont pas besoin ou veulent que leurs lecteurs soient chiffrés. L’exemption d’ordinateur est généralement utilisée lorsqu’une société dispose d’ordinateurs qui n’ont pas besoin d’être chiffrés, tels que des ordinateurs utilisés pour le développement ou les tests, ou des ordinateurs plus anciens qui ne prennent pas en charge BitLocker. Dans certains cas, la législation locale peuvent également exiger que certains ordinateurs ne soient pas chiffrés.

[Gestion des exemptions de chiffrement BitLocker d'utilisateur](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)

## Gérer les options de chiffrement BitLocker du client MBAM à l’aide du panneau de configuration


MBAM fournit un panneau de configuration personnalisé, intitulé options de chiffrement de BitLocker, qui s’affiche sous **système et sécurité**. Le panneau de configuration MBAM peut être utilisé pour déverrouiller les disques durs fixes et amovibles chiffrés et gérer également votre code confidentiel ou votre mot de passe.

**Remarques**  Ce panneau de configuration personnalisé ne remplace pas le panneau de configuration Windows BitLocker par défaut.

 

[Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-2.md)

## Autres ressources pour administrer les fonctionnalités de MBAM


[Opérations de MBAM2.0](operations-for-mbam-20-mbam-2.md)

 

 





