---
title: Planification du déploiement de clients MBAM2.5
description: Planification du déploiement de clients MBAM2.5
author: dansimp
ms.assetid: 23c89976-af24-4753-9412-ce0ea42d1964
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ff03b58da0985b2f57308c99a9bc15f4a0554623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811489"
---
# Planification du déploiement de clients MBAM2.5


Selon la manière dont vous déployez le logiciel client Microsoft BitLocker Administration and Analysis (MBAM), vous pouvez activer le chiffrement de lecteur BitLocker sur un ordinateur de votre organisation avant que l’utilisateur final ne reçoive l’ordinateur ou après. Pour les topologies d’intégration autonomes MBAM et System Center Configuration Manager, vous devez configurer des paramètres de stratégie de groupe pour MBAM.

Si vous utilisez la topologie autonome MBAM, nous vous recommandons d’utiliser un système de déploiement de logiciels d’entreprise pour déployer le logiciel client MBAM sur les ordinateurs des utilisateurs finaux.

Si vous déployez MBAM avec la topologie d’intégration de Configuration Manager, vous pouvez utiliser Configuration Manager pour déployer le logiciel client MBAM sur les ordinateurs des utilisateurs finaux. Dans Configuration Manager, l’installation MBAM crée une collection d’ordinateurs que MBAM peut gérer. Cette collection inclut les stations de travail et les appareils qui n’ont pas de module de plateforme sécurisée (TPM), mais qui exécutent Windows 8, Windows 8,1 ou Windows 10.

**Remarques**  Windows to Go n’est pas pris en charge pour l’installation de la topologie d’intégration de Configuration Manager lorsque vous utilisez Configuration Manager 2007.

 

## Déploiement du client MBAM pour activer le chiffrement de lecteur BitLocker après la distribution d’ordinateur aux utilisateurs finaux


Après avoir configuré une stratégie de groupe, vous pouvez utiliser un produit système de déploiement de logiciels d’entreprise, tel que Microsoft System Center Configuration Manager ou les services de domaine Active Directory (AD DS) pour déployer les fichiers Windows Installer de l’installation du client MBAM sur les ordinateurs cibles. Pour déployer le client MBAM, vous pouvez utiliser 32 les fichiers MbamClientSetup.exe MBAMClient.msi ou 64 bits ou les fichiers de fournis avec le logiciel client MBAM.

**Remarques**  À partir de MBAM 2,5 SP1, un MSI distinct n’est plus inclus dans le produit MBAM. Toutefois, vous pouvez extraire le MSI du fichier exécutable (. exe) qui est inclus dans le produit.

 

Lorsque vous déployez le client MBAM après distribution d’ordinateurs sur des ordinateurs clients, les utilisateurs finaux sont invités à chiffrer leur ordinateur. Cette action permet à MBAM de collecter les données (code confidentiel et mot de passe (si nécessaire), puis de commencer le processus de chiffrement.

**Remarques**  Dans cette approche, les utilisateurs finaux disposant d’ordinateurs dotés d’un processeur de TPM sont invités à activer et initialiser le processeur du TPM si la puce n’a pas été activée auparavant.

 

## Utilisation du client MBAM pour activer le chiffrement de lecteur BitLocker avant la distribution d’ordinateurs aux utilisateurs finaux


Dans les organisations sur lesquelles les ordinateurs sont reçus et configurés de manière centralisée, et sur lequel les ordinateurs sont équipés d’un processeur de TPM compatible, vous pouvez utiliser le client MBAM pour gérer le chiffrement de lecteur BitLocker sur chaque ordinateur avant d’y écrire des données utilisateur. L’avantage de ce processus est que chaque ordinateur est alors conforme. Cette méthode ne repose pas sur l’action de l’utilisateur final, car l’administrateur l’a déjà chiffrée. Une supposition essentielle pour ce scénario est que la stratégie de l’organisation installe une image Windows d’entreprise avant que l’ordinateur ne soit remis à l’utilisateur final.

Si votre organisation veut utiliser le processeur du TPM pour chiffrer les ordinateurs, l’administrateur ajoute le protecteur du TPM pour chiffrer le volume du système d’exploitation de l’ordinateur. Si votre organisation veut utiliser le processeur du TPM et un protecteur de code confidentiel, l’administrateur chiffre le volume du système d’exploitation à l’aide du protecteur du module de plateforme sécurisée, puis les utilisateurs finaux sélectionnent un code confidentiel lors de la première connexion. Si votre organisation décide d’utiliser uniquement le protecteur de punaise, l’administrateur n’a pas besoin de chiffrer le volume d’abord. Lorsque les utilisateurs finaux se connectent, l’administration et la surveillance de BitLocker vous invitent à entrer un code confidentiel, ou un code confidentiel et un mot de passe à utiliser sur un redémarrage d’ordinateur ultérieur.

**Remarques**  Par le biais de l’option de protection de TPM, l’administrateur doit accepter l’invite du BIOS pour activer et initialiser le module de plateforme sécurisée avant que l’ordinateur ne soit remis à l’utilisateur final.

 

## Prise en charge du client MBAM pour les disques durs chiffrés


MBAM prend en charge BitLocker sur les disques durs chiffrés qui satisfont les exigences de spécification TCG pour Opal ainsi que les normes IEEE 1667. Lorsque BitLocker est activé sur ces appareils, il génère des clés et effectue des tâches de gestion sur le lecteur chiffré. Pour plus d’informations, voir [disque dur chiffré](https://technet.microsoft.com/library/hh831627.aspx) .


## Rubriques connexes


[Planification du déploiement de MBAM2.5](planning-to-deploy-mbam-25.md)

[Déploiement du client MBAM2.5](deploying-the-mbam-25-client.md)

 

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




