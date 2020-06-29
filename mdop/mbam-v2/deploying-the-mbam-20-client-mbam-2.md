---
title: Déploiement du client MBAM2.0
description: Déploiement du client MBAM2.0
author: dansimp
ms.assetid: 3dd584fe-2a54-40f0-9bab-13ea74040b01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa42c8ab3adc273f0e00ba56a59f487deba89c6f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809960"
---
# Déploiement du client MBAM2.0


Le client Microsoft BitLocker Administration and Analysis (MBAM) permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise. Le client BitLocker peut être intégré à une organisation en déployant le client par le biais d’un système de distribution de logiciels électronique, tel que les services de domaine Active Directory (AD FS), ou en chiffrant directement les ordinateurs clients dans le cadre du processus d’imagerie initial.

En fonction du moment où vous déployez le client d’administration et de surveillance de BitLocker, vous pouvez activer le chiffrement BitLocker sur un ordinateur de votre organisation avant que l’utilisateur final ne reçoive l’ordinateur ou après la configuration de la stratégie de groupe et le déploiement du logiciel client MBAM à l’aide d’un système de déploiement de logiciels d’entreprise.

## Déployer le client MBAM sur un ordinateur portable ou de bureau


Après avoir configuré une stratégie de groupe, vous pouvez utiliser un produit système de déploiement de logiciels d’entreprise, tel que Microsoft System Center Configuration Manager 2012 ou services de domaine Active Directory (AD FS) pour déployer les fichiers du programme d’installation du client MBAM sur les ordinateurs cibles. Vous pouvez déployer le client à 32 l’aide des fichiers MbamClientSetup.exe de MBAMClient.msi ou 64 bits, ou des fichiers 32 ou 64 bits, fournis avec le logiciel MBAM. Pour plus d’informations sur le déploiement d’objets de stratégie de groupe MBAM, voir [déploiement d’objets de stratégie de groupe MBAM 2,0](deploying-mbam-20-group-policy-objects-mbam-2.md).

[Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-2.md)

## Déploiement du client MBAM dans le cadre d’un déploiement Windows


Dans les organisations sur lesquelles les ordinateurs sont reçus et configurés de manière centralisée, vous pouvez installer le client MBAM pour gérer le chiffrement BitLocker sur chaque ordinateur avant d’y écrire des données utilisateur. L’avantage de ce processus est que chaque ordinateur est alors conforme au chiffrement BitLocker. Cette méthode ne repose pas sur l’action de l’utilisateur, car l’administrateur l’a déjà crypté. Une supposition essentielle pour ce scénario est que la stratégie de l’organisation installe une image Windows d’entreprise avant que l’ordinateur ne soit remis à l’utilisateur. Si la stratégie de groupe a été configurée pour exiger un code confidentiel, les utilisateurs sont invités à définir un code confidentiel après réception de la stratégie de groupe.

[Déploiement du client MBAM dans le cadre d'un déploiement de Windows](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-2.md)

## Utilisation d'une ligne de commande pour installer le client MBAM


Cette section explique comment installer le client MBAM à l’aide d’une ligne de commande.

[Utilisation d'une ligne de commande pour installer le client MBAM](how-to-use-a-command-line-to-install-the-mbam-client.md)

## Autres ressources pour le déploiement du client MBAM


[Déploiement de MBAM 2,0](deploying-mbam-20-mbam-2.md)[planification pour le déploiement du client 2,0 MBAM](planning-for-mbam-20-client-deployment-mbam-2.md)

 

 





