---
title: Gestion de BitLocker avec MBAM
description: Gestion de BitLocker avec MBAM
author: dansimp
ms.assetid: 9bfc6c67-f12c-4daa-8f08-5884fb47443c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d261ec4fa789cd331209afe1c2f1858d627209a3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811790"
---
# Gestion de BitLocker avec MBAM


Après avoir planifié le déploiement de Microsoft BitLocker et de l’analyse, vous pouvez le configurer et l’utiliser pour gérer le chiffrement d’entreprise BitLocker. Les informations contenues dans cette section décrivent les tâches de gestion du chiffrement à l’aide du chiffrement de BitLocker qui sont accomplies à l’aide de l’administration et de la surveillance de Microsoft BitLocker.

## Réinitialiser un verrouillage du TPM à l’aide de MBAM


Un module de plateforme sécurisée (TPM) est un micropuce conçu pour fournir des fonctions de sécurité de base, notamment les clés de chiffrement. Le module de plateforme sécurisée est généralement installé sur la carte de réseau d’un ordinateur ou d’un ordinateur portable et communique avec le reste du système à l’aide d’un bus matériel. Les ordinateurs qui intègrent un TPM ont la possibilité de créer des clés de chiffrement et de les chiffrer de sorte qu’ils puissent être déchiffrés uniquement par le TPM.

Un verrouillage du TPM peut se produire si un utilisateur entre un code confidentiel incorrect trop souvent. Le nombre de fois qu’un utilisateur peut entrer un code confidentiel incorrect avant que les verrouillages du TPM ne varient d’un fabricant au fabricant. Vous pouvez utiliser MBAM pour accéder au système de données de récupération de clés centralisées sur le site Web d’administration et de contrôle, dans lequel vous pouvez récupérer un fichier de mot de passe de propriétaire du TPM lorsque vous fournissez un ID d’ordinateur et un identificateur d’utilisateur associé.

[Réinitialisation d'un verrouillage TPM](how-to-reset-a-tpm-lockout-mbam-2.md)

## Récupérer des lecteurs avec MBAM


Lorsque vous traitez le chiffrement des données, en particulier dans un environnement d’entreprise, pensez à la manière dont les données peuvent être restaurées en cas de panne matérielle, de changements de personnel ou d’autres situations dans lesquelles les clés de chiffrement peuvent être perdues.

Les fonctionnalités de récupération de lecteur chiffrées de MBAM garantissent la capture et le stockage des données et l’accès aux outils requis pour accéder au volume protégé par BitLocker lorsque le mode de récupération de BitLocker passe en mode de récupération, est déplacé ou est endommagé.

[Procédure de récupération d'un lecteur en mode de récupération](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

[Récupération d'un lecteur déplacé](how-to-recover-a-moved-drive-mbam-2.md)

[Récupération d'un lecteur endommagé](how-to-recover-a-corrupted-drive-mbam-2.md)

## Déterminer l’état de chiffrement de BitLocker des ordinateurs perdus en utilisant MBAM


À l’aide de MBAM, vous pouvez déterminer le dernier état de chiffrement BitLocker connu des ordinateurs perdus ou volés.

[Détermination de l'état de chiffrement BitLocker des ordinateurs perdus](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

## Utiliser le portail libre-service pour accéder à un ordinateur


Si les utilisateurs finaux se bloquent pas de Windows par BitLocker, ils peuvent suivre les instructions de cette section pour obtenir une clé de récupération BitLocker afin de récupérer l’accès à leur ordinateur.

[Utilisation du portail libre-service pour accéder de nouveau à un ordinateur](how-to-use-the-self-service-portal-to-regain-access-to-a-computer.md)

## Autres ressources pour effectuer une gestion BitLocker avec MBAM


[Opérations de MBAM2.0](operations-for-mbam-20-mbam-2.md)

 

 





