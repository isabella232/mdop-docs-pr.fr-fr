---
title: Planification du déploiement de clients MBAM2.0
description: Planification du déploiement de clients MBAM2.0
author: dansimp
ms.assetid: 3a92cf29-092f-4cad-bdfa-d5f6aafe554b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c3a7383188d4064247d8e493c8e6125fc24a1d2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804363"
---
# Planification du déploiement de clients MBAM2.0


En fonction du moment où vous déployez le client Microsoft BitLocker Administration and Analysis (MBAM), vous pouvez activer le chiffrement de lecteur BitLocker sur un ordinateur de votre organisation avant que l’utilisateur final ne reçoive l’ordinateur ou après. Pour le mode autonome MBAM et les topologies du gestionnaire de configuration, vous devez configurer des paramètres de stratégie de groupe pour MBAM.

Si vous utilisez la topologie autonome MBAM, nous vous recommandons d’utiliser un système de déploiement de logiciels d’entreprise pour déployer le logiciel client MBAM sur les ordinateurs des utilisateurs finaux.

Si vous déployez MBAM avec la topologie Configuration Manager, vous pouvez utiliser Configuration Manager pour déployer le logiciel client MBAM sur les ordinateurs des utilisateurs finaux. Dans Configuration Manager, l’installation MBAM crée une collection d’ordinateurs que MBAM peut gérer. Cette collection inclut les stations de travail et les appareils qui n’ont pas de module de plateforme sécurisée (TPM), mais qui exécutent Windows 8.

**Remarques**  Windows to Go n’est pas pris en charge pour les installations intégrées de Configuration Manager du MBAM si vous utilisez Configuration Manager 2007.

 

## Déploiement du client MBAM pour activer le chiffrement BitLocker après la distribution ordinateur aux utilisateurs finaux


Après avoir configuré une stratégie de groupe, vous pouvez utiliser un produit système de déploiement de logiciels d’entreprise, tel que Microsoft System Center Configuration Manager ou les services de domaine Active Directory (AD DS) pour déployer les fichiers Windows Installer de l’installation du client MBAM sur les ordinateurs cibles. Pour déployer le client MBAM, vous pouvez utiliser les fichiers MbamClientSetup.exe 32 ou 64 bits ou MBAMClient.msi, qui sont fournis avec le logiciel MBAM.

Lorsque vous déployez le client MBAM après distribution d’ordinateurs sur des ordinateurs clients, les utilisateurs finaux sont invités à chiffrer leur ordinateur. Cela permet à MBAM de collecter les données, y compris le code confidentiel et le mot de passe, puis de commencer le processus de chiffrement.

**Remarques**  Dans cette approche, les utilisateurs disposant d’ordinateurs dotés d’un processeur de TPM sont invités à activer et initialiser le processeur du TPM si la puce n’a pas été activée auparavant.

 

## Utilisation du client MBAM pour activer le chiffrement BitLocker avant la distribution d’ordinateurs aux utilisateurs finaux


Dans les organisations sur lesquelles les ordinateurs sont reçus et configurés de manière centralisée, et sur lequel ils disposent d’un processeur de TPM compatible, vous pouvez installer le client MBAM pour gérer le chiffrement de BitLocker sur chaque ordinateur avant d’y écrire des données utilisateur. L’avantage de ce processus est que tous les ordinateurs seront alors conformes au chiffrement BitLocker. Cette méthode ne repose pas sur l’action de l’utilisateur, car l’administrateur l’a déjà crypté. Une supposition essentielle pour ce scénario est que la stratégie de l’organisation installe une image Windows d’entreprise avant que l’ordinateur ne soit remis à l’utilisateur.

Si votre organisation veut utiliser le processeur du TPM pour chiffrer les ordinateurs, l’administrateur ajoute le protecteur du TPM pour chiffrer le volume du système d’exploitation de l’ordinateur. Si votre organisation veut utiliser le processeur du TPM et un protecteur de code confidentiel, l’administrateur chiffre le volume du système d’exploitation à l’aide du protecteur du module de plateforme sécurisée, puis les utilisateurs sélectionnent un code confidentiel lors de la première connexion. Si votre organisation décide d’utiliser uniquement le protecteur de punaise, l’administrateur n’a pas besoin de chiffrer le volume d’abord. Lorsque les utilisateurs ouvrent une session, l’administration et la surveillance de BitLocker vous invitent à fournir un code confidentiel, ou un code confidentiel et un mot de passe à utiliser pour les redémarrages ultérieures de l’ordinateur.

**Remarques**  L’option de protection de module de plateforme sécurisée exige que l’administrateur accepte l’invite du BIOS pour activer et initialiser le module de plateforme sécurisée avant qu’il soit remis à l’utilisateur.

 

## Rubriques connexes


[Planification du déploiement de MBAM2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Déploiement du client MBAM2.0](deploying-the-mbam-20-client-mbam-2.md)

 

 





