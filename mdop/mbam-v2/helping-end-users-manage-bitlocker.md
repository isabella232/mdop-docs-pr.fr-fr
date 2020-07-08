---
title: Aider les utilisateurs finaux à gérer BitLocker
description: Aider les utilisateurs finaux à gérer BitLocker
author: dansimp
ms.assetid: 47776fb3-2d94-4970-b687-c35ec3dd6c64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26ef2bc33a75ff7773b75807ab0e10e5aa67b109
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810758"
---
# Aider les utilisateurs finaux à gérer BitLocker


Le contenu d’un ordinateur perdu ou volé est vulnérable aux accès non autorisés et peut présenter un risque de sécurité aux personnes et aux entreprises. Le programme d’administration et de surveillance de BitLocker utilise BitLocker pour empêcher tout accès non autorisé en verrouillant votre ordinateur pour protéger les données sensibles des utilisateurs malveillants.

## Qu’est-ce que BitLocker?


Le chiffrement de lecteur BitLocker peut offrir une protection pour les lecteurs de systèmes d’exploitation, les lecteurs de données et les lecteurs amovibles (tels qu’une clé USB) en chiffrant les lecteurs. Selon la configuration de BitLocker, les utilisateurs devront peut-être fournir une clé (un mot de passe ou un code confidentiel) pour déverrouiller les informations stockées sur les lecteurs chiffrés.

Lorsque vous ajoutez de nouveaux fichiers à un lecteur chiffré avec BitLocker, BitLocker les chiffre automatiquement. Les fichiers restent chiffrés uniquement lorsqu’ils sont stockés sur le lecteur chiffré. Les fichiers copiés sur un autre lecteur ou ordinateur sont déchiffrés. Si vous partagez des fichiers avec d’autres utilisateurs, par exemple par le biais d’un réseau, ces fichiers sont chiffrés en même temps que les utilisateurs autorisés.

Si vous chiffrez le lecteur du système d’exploitation, BitLocker vérifie l’ordinateur lors du démarrage pour toutes les conditions susceptibles de représenter un risque de sécurité (par exemple, une modification du BIOS ou des modifications apportées à un fichier de démarrage). Si un risque de sécurité potentiel est détecté, BitLocker verrouille le lecteur du système d’exploitation et nécessite une clé de récupération BitLocker spéciale pour le déverrouiller. Assurez-vous de créer cette clé de récupération lorsque vous activez BitLocker pour la première fois. Dans le cas contraire, vous risquez de perdre définitivement l’accès à vos fichiers.

Si vous chiffrez des lecteurs de données (résolus ou amovibles), vous pouvez déverrouiller un lecteur chiffré à l’aide d’un mot de passe ou d’une carte à puce, ou configurer le lecteur pour qu’il s’ouvre automatiquement lorsque vous ouvrez une session sur l’ordinateur.

En plus des mots de passe et des épingles, BitLocker peut utiliser le processeur du module de plateforme sécurisée fourni dans de nombreux ordinateurs récents. Le puce TPM est utilisée pour s’assurer que votre ordinateur n’a pas été falsifié avant que BitLocker ne déverrouille le lecteur du système d’exploitation. Pendant le processus de chiffrement, il est possible que vous deviez activer le processeur du TPM. Lorsque vous démarrez votre ordinateur, BitLocker demande à l’application de plateforme sécurisée les clés pour le lecteur et la déverrouille. Pour activer le processeur du module de plateforme sécurisée, vous devez redémarrer votre ordinateur, puis modifier un paramètre dans le BIOS, une couche pré-Windows du logiciel de votre ordinateur. Pour plus d’informations sur le TPM, voir [à propos du puce du TPM de l’ordinateur](about-the-computer-tpm-chip.md).

Une fois votre ordinateur protégé par BitLocker, il est possible que vous deviez entrer un code confidentiel ou un mot de passe chaque fois que l’ordinateur quitte la mise en veille prolongée ou démarre. Le support technique de votre entreprise ou organisation peut vous aider si vous oubliez votre code confidentiel ou votre mot de passe.

Vous pouvez désactiver la fonctionnalité BitLocker, de manière temporaire, en l’interrompant ou définitivement en déchiffrant le lecteur.

**Remarques**  Dans la mesure où BitLocker chiffre tout le lecteur et pas seulement les fichiers individuels, soyez prudent lorsque vous déplacez des données sensibles entre les lecteurs. Si vous déplacez un fichier à partir d’un lecteur protégé par BitLocker vers un lecteur non chiffré, le fichier ne sera plus chiffré.

 

## À propos de l’application options de chiffrement BitLocker


Pour déverrouiller les disques durs de votre ordinateur et gérer votre code confidentiel et vos mots de passe, utilisez l’application options de chiffrement BitLocker du panneau de configuration Windows en suivant la procédure décrite dans cet article. Vous pouvez entrer des mots de passe pour déverrouiller des lecteurs protégés et vérifier l’état de BitLocker des lecteurs connectés à l’aide de cette application.

**Pour ouvrir l’application options de chiffrement BitLocker**

1.  Cliquez sur **Démarrer**, puis sélectionnez **panneau de configuration**. Le panneau de configuration s’ouvre dans une nouvelle fenêtre.

2.  Dans **le panneau**de configuration, sélectionnez **système et sécurité**.

3.  Sélectionnez **options de chiffrement BitLocker** pour ouvrir l’application options de chiffrement BitLocker.

    Pour obtenir une description des options disponibles, reportez-vous à la section suivante.

## Options de l’application options de chiffrement BitLocker


L’application options de chiffrement BitLocker du panneau de configuration vous permet de gérer votre code confidentiel et vos mots de passe, qu’utilise BitLocker pour protéger votre ordinateur.

**Chiffrement de lecteur BitLocker – lecteurs de disque fixes:**

Dans cette section, vous pouvez afficher des informations sur les disques durs connectés à votre ordinateur et leur état actuel du chiffrement BitLocker.

-   **Gérer votre code confidentiel** : change le code confidentiel utilisé par BitLocker pour déverrouiller le lecteur de votre système d’exploitation.

-   **Gérer votre mot de passe** : modifie le mot de passe utilisé par BitLocker pour déverrouiller vos autres lecteurs internes.

**Chiffrement de lecteur BitLocker-lecteurs externes:**

Dans cette section, vous pouvez afficher des informations sur les lecteurs externes (par exemple, une clé USB) connectée à votre ordinateur, et sur son état actuel du chiffrement BitLocker.

-   **Gérer votre mot de passe** : modifie le mot de passe utilisé par BitLocker pour déverrouiller vos autres lecteurs internes.

**Avancé**

-   **Administration du TPM** : ouvre l’outil d’administration du TPM dans une fenêtre séparée. À partir de cet emplacement, vous pouvez configurer les tâches courantes de GPC et obtenir des informations sur le chipset GPC. Pour accéder à cet outil, vous devez disposer des autorisations d’administration sur votre ordinateur.

-   **Gestion des disques** : Ouvrez l’outil Gestion des disques. Vous pouvez alors afficher les informations de tous les disques durs connectés à l’ordinateur et configurer des partitions et des options de lecteur. Pour accéder à cet outil, vous devez disposer des droits d’administration sur votre ordinateur.

 

 





