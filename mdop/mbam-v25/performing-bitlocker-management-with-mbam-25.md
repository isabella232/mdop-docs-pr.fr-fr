---
title: Gestion de BitLocker avec MBAM2.5
description: Gestion de BitLocker avec MBAM2.5
author: dansimp
ms.assetid: 068f3ee0-300c-4083-ba18-7065eef997ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a0ee5802f945176914c56659e0ff7e34e93a969
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811496"
---
# Gestion de BitLocker avec MBAM2.5


Après avoir planifié le déploiement de la gestion et l’analyse de BitLocker (MBAM), vous pouvez le configurer et l’utiliser pour gérer le chiffrement de lecteur BitLocker au sein de votre entreprise. Les informations contenues dans cette section décrivent les tâches de gestion du chiffrement à l’aide de la gestion des messages

## Réinitialiser un verrouillage du TPM


Un module de plateforme sécurisée (TPM) est un micropuce conçu pour fournir des fonctions de sécurité de base, notamment les clés de chiffrement. Le module de plateforme sécurisée est généralement installé sur la carte mère d’un ordinateur, et communique avec le reste du système à l’aide d’une carte de bus hôte. Sur les ordinateurs qui intègrent un module de plateforme sécurisée, vous pouvez créer des clés de chiffrement et les chiffrer pour pouvoir les déchiffrer uniquement par le TPM.

Un verrouillage du TPM peut se produire si un utilisateur entre un code confidentiel incorrect trop souvent. Le nombre de fois qu’un utilisateur peut entrer un code confidentiel incorrect avant que les verrouillages du TPM ne varient en fonction du fabricant. Vous pouvez utiliser MBAM pour accéder au système de données de récupération de clés centralisées sur le site Web d’administration et de contrôle, dans lequel vous pouvez récupérer un fichier de mot de passe de propriétaire du TPM lorsque vous fournissez un ID d’ordinateur et un identificateur d’utilisateur associé.

[Réinitialisation d'un verrouillage TPM](how-to-reset-a-tpm-lockout-mbam-25.md)

## Récupérer des lecteurs


Lorsque vous traitez le chiffrement des données, en particulier dans un environnement d’entreprise, pensez à la manière dont les données peuvent être restaurées en cas de panne matérielle, de changements de personnel ou d’autres situations dans lesquelles les clés de chiffrement peuvent être perdues.

Les fonctionnalités de récupération de lecteur chiffrées dans MBAM garantissent la capture et le stockage des données et l’accès aux outils requis pour accéder au volume protégé par BitLocker lorsque le mode de récupération de BitLocker passe en mode de récupération, est déplacé ou est endommagé.

[Procédure de récupération d'un lecteur en mode de récupération](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)

[Récupération d'un lecteur déplacé](how-to-recover-a-moved-drive-mbam-25.md)

[Récupération d'un lecteur endommagé](how-to-recover-a-corrupted-drive-mbam-25.md)

## Déterminer l’état de chiffrement BitLocker des ordinateurs perdus


À l’aide de MBAM, vous pouvez déterminer le dernier état de chiffrement BitLocker connu des ordinateurs perdus ou volés.

[Détermination de l'état de chiffrement BitLocker des ordinateurs perdus](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)

## Utiliser le portail libre-service pour accéder à un ordinateur


Si les utilisateurs finaux se bloquent pas de Windows par BitLocker, ils peuvent suivre les instructions de cette section pour obtenir une clé de récupération BitLocker afin de récupérer l’accès à leur ordinateur.

[Utilisation du portail libre-service pour accéder de nouveau à un ordinateur](how-to-use-the-self-service-portal-to-regain-access-to-a-computer-mbam-25.md)



## Rubriques connexes


[Opérations de MBAM2.5](operations-for-mbam-25.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





