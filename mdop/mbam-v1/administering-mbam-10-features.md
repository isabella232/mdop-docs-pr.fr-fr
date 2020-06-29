---
title: Administration des composants de MBAM1.0
description: Administration des composants de MBAM1.0
author: dansimp
ms.assetid: dd9a9eff-f1ad-4af3-85d9-c19131a4ad22
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a99ac556227c0f113fb20f3aca32d21c204877b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808627"
---
# Administration des composants de MBAM1.0


Après avoir exécuté la planification et le déploiement de la planification et du déploiement de Microsoft BitLocker requis, vous pouvez configurer et utiliser MBAM pour gérer le chiffrement d’entreprise BitLocker. Les informations contenues dans cette section décrivent les tâches d’opérations relatives aux fonctionnalités de la fonctionnalité de MBAM d’installation.

## Gérer les rôles d’administrateur MBAM


Une fois l’installation d’MBAM terminée pour toutes les fonctionnalités du serveur, les utilisateurs administratifs doivent avoir accès à ces fonctionnalités serveur. Il est recommandé que les administrateurs qui gèrent ou utilisent les fonctionnalités du serveur MBAM doivent être assignés aux groupes de sécurité Active Directory, puis ces groupes doivent être ajoutés au groupe local administratif approprié MBAM.

[Gérer des rôles d'administrateur MBAM](how-to-manage-mbam-administrator-roles-mbam-1.md)

## Gérer la compatibilité du matériel


La fonctionnalité de compatibilité matérielle MBAM peut vous aider à vous assurer que seul le matériel informatique que vous spécifiez comme prenant en charge BitLocker sera crypté. Lorsque cette fonctionnalité est activée, le bit \ _admmontla chiffre uniquement les ordinateurs marqués comme compatibles.

**Important**  Lorsque cette fonctionnalité est désactivée, tous les ordinateurs sur lesquels la stratégie MBAM est déployée seront chiffrés.

 

MBAM peut collecter des informations sur la création et le modèle d’ordinateurs clients si vous déployez la stratégie de groupe «autoriser le contrôle de compatibilité matérielle». Si vous configurez cette stratégie, l’agent MBAM rapporte les informations sur la marque et le modèle de l’ordinateur au serveur MBAM lorsque le client MBAM est déployé sur un ordinateur client.

[Gérer la compatibilité matérielle](how-to-manage-hardware-compatibility-mbam-1.md)

[Gestion des exemptions de chiffrement BitLocker d'utilisateur](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)

## Gérer les exemptions de chiffrement BitLocker


MBAM peut accorder deux formes d’exemption du chiffrement BitLocker: exemption d’ordinateur et exemption d’utilisateur. L’exemption d’ordinateur est généralement utilisée lorsqu’une société dispose d’ordinateurs qui n’ont pas besoin d’être chiffrés, tels que des ordinateurs utilisés pour le développement ou les tests, ou des ordinateurs plus anciens qui ne prennent pas en charge BitLocker. Dans certains cas, la législation locale peuvent également exiger que certains ordinateurs ne soient pas chiffrés. Vous pouvez également choisir d’exempter les utilisateurs qui n’ont pas besoin ou dont leurs lecteurs sont chiffrés.

[Gérer des exemptions d'ordinateurs au chiffrement BitLocker](how-to-manage-computer-bitlocker-encryption-exemptions.md)

## Gérer les options de chiffrement BitLocker du client MBAM à l’aide du panneau de configuration


S’il est activé par le biais d’objets de stratégie de groupe (GPO), un panneau de configuration MBAM personnalisé nommé options de chiffrement BitLocker sera disponible sous **système et sécurité**. Ce panneau de configuration personnalisé remplace le panneau de configuration Windows BitLocker par défaut. Le panneau de configuration MBAM vous permet de déverrouiller des lecteurs chiffrés (résolus et amovibles) et de gérer également votre code confidentiel ou votre mot de passe.

[Gestion des options de chiffrement BitLocker du client MBAM à l'aide du Panneau de configuration](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-1.md)

## Autres ressources pour administrer les fonctionnalités de MBAM


[Opérations de MBAM1.0](operations-for-mbam-10.md)

 

 





