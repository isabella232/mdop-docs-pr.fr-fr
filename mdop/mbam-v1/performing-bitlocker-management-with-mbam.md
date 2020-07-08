---
title: Gestion de BitLocker avec MBAM
description: Gestion de BitLocker avec MBAM
author: dansimp
ms.assetid: 2d24390a-87bf-48b3-96a9-3882d6f2a15c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d0de3711d5b7c3696783a054ee7c7f8220b5356
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811429"
---
# Gestion de BitLocker avec MBAM


Après avoir déployé le contrôle d’administration et de surveillance de BitLocker de Microsoft (MBAM), vous pouvez configurer et utiliser MBAM pour gérer le chiffrement d’entreprise BitLocker. Cette section décrit les tâches de gestion du chiffrement à l’aide de l’installation, qui peuvent être effectuées à l’aide de MBAM.

## Réinitialiser un verrouillage du TPM avec MBAM


Un micropuce module de plateforme sécurisée (TPM) fournit des fonctions de sécurité de base. Ces fonctions sont principalement effectuées par l’utilisation de clés de chiffrement. Le module de plateforme sécurisée est généralement installé sur la carte mère d’un ordinateur, d’un ordinateur portable et communique avec le reste du système à l’aide d’un bus matériel. Les ordinateurs qui intègrent un TPM peuvent créer des clés de chiffrement qui peuvent être déchiffrées uniquement par le TPM. Un verrouillage du TPM peut se produire si un utilisateur entre un code confidentiel incorrect trop souvent. Le nombre de fois qu’un utilisateur peut entrer un code confidentiel incorrect avant que les verrouillages du TPM ne varient d’un fabricant au fabricant. Le système de données de récupération de clés sur le site Web d’administration MBAM vous permet d’obtenir un fichier de mot de passe de réinitialisation du propriétaire de TPM.

[Réinitialisation d'un verrouillage TPM](how-to-reset-a-tpm-lockout-mbam-1.md)

## Récupérer des lecteurs avec MBAM


Assurez-vous de savoir comment procéder à la récupération des données à partir de lecteurs chiffrés dans le cas d’une panne matérielle, de changements de personnel ou d’autres situations dans lesquelles les clés de chiffrement sont perdues. Les fonctionnalités de récupération de lecteur chiffrées de MBAM fournissent la capture et le stockage des données et la disponibilité des outils requis pour accéder au volume protégé par BitLocker lorsque le volume passe en mode de récupération, est déplacé ou est endommagé.

[Procédure de récupération d'un lecteur en mode de récupération](how-to-recover-a-drive-in-recovery-mode-mbam-1.md)

[Récupération d'un lecteur déplacé](how-to-recover-a-moved-drive-mbam-1.md)

[Récupération d'un lecteur endommagé](how-to-recover-a-corrupted-drive-mbam-1.md)

## Déterminer l’état de chiffrement de BitLocker des ordinateurs perdus en utilisant MBAM


Lorsque vous utilisez MBAM, vous pouvez déterminer le dernier état de chiffrement BitLocker connu des ordinateurs perdus ou volés.

[Détermination de l'état de chiffrement BitLocker d'un ordinateur perdu](how-to-determine-the-bitlocker-encryption-state-of-a-lost-computers-mbam-1.md)

## Autres ressources pour effectuer une gestion BitLocker avec MBAM


[Opérations de MBAM1.0](operations-for-mbam-10.md)

 

 





