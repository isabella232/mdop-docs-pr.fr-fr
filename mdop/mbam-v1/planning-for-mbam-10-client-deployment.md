---
title: Planification du déploiement de clients MBAM1.0
description: Planification du déploiement de clients MBAM1.0
author: dansimp
ms.assetid: 3af2e7f3-134b-4ab9-9847-b07474ca6ac3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d58d6420febd2da9ee9cd4074fc8b5870285b0b4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811418"
---
# Planification du déploiement de clients MBAM1.0


Selon la manière dont vous déployez le client Microsoft BitLocker Administration and Analysis (MBAM), vous pouvez activer le chiffrement BitLocker sur un ordinateur de votre organisation avant que l’utilisateur final ne reçoive l’ordinateur ou après. Pour activer le chiffrement BitLocker après que l’utilisateur final a reçu l’ordinateur, configurez une stratégie de groupe. Pour activer le chiffrement BitLocker avant la réception de l’ordinateur par l’utilisateur final, déployez le logiciel client MBAM à l’aide d’un système de déploiement de logiciels d’entreprise.

Vous pouvez appliquer l’une ou l’autre des méthodes au sein de votre organisation. Si vous utilisez les deux méthodes, vous pouvez améliorer la conformité, la création de rapports et la prise en charge des récupérations de clés.

**Remarques**  Pour vérifier la configuration système requise pour le client MBAM, voir [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).

 

## Déploiement du client MBAM pour activer le chiffrement BitLocker après la distribution ordinateur aux utilisateurs finaux


Après avoir configuré la stratégie de groupe, vous pouvez utiliser un produit système de déploiement de logiciels d’entreprise, tel que Microsoft System Center Configuration Manager 2012 ou services de domaine Active Directory, pour déployer les fichiers Windows Installer du client MBAM sur les ordinateurs cibles. Les deux fichiers du programme d’installation du client MBAM sont MBAMClient-64bit.msi et MBAMClient-32bit.msi fournis avec le logiciel MBAM. Pour plus d’informations sur le déploiement d’objets de stratégie de groupe MBAM, voir [déploiement d’objets de stratégie de groupe MBAM 1,0](deploying-mbam-10-group-policy-objects.md).

Lorsque vous déployez le client MBAM, après avoir distribué les ordinateurs aux utilisateurs finaux, les utilisateurs finaux sont invités à chiffrer leur ordinateur. Cela permet à MBAM de collecter les données, d’inclure le code confidentiel et le mot de passe, puis de commencer le processus de chiffrement.

**Remarques**  Dans le cas présent, l’utilisateur est invité à activer et initialiser le processeur du module de plateforme sécurisée, s’il n’a pas encore été activé.

 

## Utilisation du client MBAM pour activer le chiffrement BitLocker avant la distribution d’ordinateurs aux utilisateurs finaux


Dans les organisations sur lesquelles les ordinateurs sont reçus et configurés de manière centralisée, vous pouvez installer le client MBAM pour gérer le chiffrement BitLocker sur chaque ordinateur avant d’écrire des données utilisateur. L’avantage de ce processus est que tous les ordinateurs seront alors conformes au chiffrement BitLocker. Cette méthode ne repose pas sur l’action de l’utilisateur, car l’administrateur l’a déjà crypté. Une supposition essentielle pour ce scénario est que la stratégie de l’organisation installe une image Windows d’entreprise avant que l’ordinateur ne soit remis à l’utilisateur.

Si votre organisation souhaite utiliser le module de plateforme sécurisée pour chiffrer les ordinateurs, l’administrateur doit chiffrer le volume du système d’exploitation de l’ordinateur avec le protecteur de module de plateforme sécurisée. Si votre organisation veut utiliser le processeur du TPM et un protecteur de code confidentiel, l’administrateur doit chiffrer le volume du système avec le protecteur de TPM, puis les utilisateurs sélectionner un code confidentiel lors de la première connexion. Si votre organisation décide d’utiliser uniquement le protecteur de punaise, l’administrateur n’a pas besoin de chiffrer le volume d’abord. Lorsque l’utilisateur se connecte sur son ordinateur, MBAM lui demande de fournir un code confidentiel ou un code confidentiel et un mot de passe qu’il utilisera lors du redémarrage de son ordinateur ultérieurement.

**Remarques**  L’une des options de protection de module de plateforme sécurisée doit permettre à l’administrateur d’accepter l’invite du BIOS pour activer et initialiser le TPM avant de l’envoyer à l’utilisateur.

 

## Rubriques connexes


[Planification du déploiement de MBAM1.0](planning-to-deploy-mbam-10.md)

[Déploiement du client MBAM1.0](deploying-the-mbam-10-client.md)

 

 





