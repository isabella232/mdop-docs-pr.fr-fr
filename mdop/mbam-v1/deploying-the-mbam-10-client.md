---
title: Déploiement du client MBAM1.0
description: Déploiement du client MBAM1.0
author: dansimp
ms.assetid: f7ca233f-5035-4ff9-ab3a-f2453b4929d1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dee8c2f4a9b398c9f0797ada35e4c36610c755b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809635"
---
# Déploiement du client MBAM1.0


Le client Microsoft BitLocker Administration and Analysis (MBAM) permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise. Le client BitLocker peut être intégré à une organisation en déployant le client via des outils tels que les services de domaine Active Directory (AD FS) ou en chiffrant directement les ordinateurs clients dans le cadre du processus d’imagerie initial.

En fonction du moment de déploiement du client MBAM, vous pouvez activer le chiffrement BitLocker sur un ordinateur de votre organisation avant ou après la réception de l’ordinateur par l’utilisateur final. Pour contrôler ce minutage, vous devez configurer une stratégie de groupe et déployer le logiciel client MBAM à l’aide d’un système de déploiement de logiciels d’entreprise.

Vous pouvez utiliser l’une ou l’autre de ces méthodes au sein de votre organisation. Si vous utilisez les deux méthodes, vous pouvez améliorer la conformité, la création de rapports et la prise en charge des récupérations de clés.

## Déployer le client MBAM sur un ordinateur portable ou de bureau


Après avoir configuré une stratégie de groupe, vous pouvez déployer les fichiers du programme d’installation du client MBAM sur les ordinateurs cibles. Pour ce faire, vous devez utiliser un produit système de déploiement de logiciels d’entreprise, tel que Microsoft System Center 2012 Configuration Manager ou les services de domaine Active Directory. Les deux fichiers du programme d’installation du client MBAM disponibles sont MBAMClient-64bit.msi et MBAMClient-32bit.msi. Ces fichiers sont fournis avec le logiciel MBAM. Pour plus d’informations sur le déploiement d’objets de stratégie de groupe MBAM, voir [déploiement d’objets de stratégie de groupe MBAM 1,0](deploying-mbam-10-group-policy-objects.md).

[Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-1.md)

## Déploiement du client MBAM dans le cadre d’un déploiement Windows


Dans certaines organisations, de nouveaux ordinateurs sont reçus et configurés de manière centralisée. Cette situation permet aux administrateurs d’installer le client MBAM pour gérer le chiffrement BitLocker sur chaque ordinateur avant que les données de l’utilisateur ne soient écrites sur l’ordinateur. Cette approche permet de s’assurer que les ordinateurs sont correctement chiffrés, car l’administrateur effectue l’action sans recourir à une action de l’utilisateur final. Une supposition essentielle pour ce scénario est que la stratégie de l’organisation installe une image Windows d’entreprise avant que l’ordinateur ne soit remis à l’utilisateur.

[Déploiement du client MBAM dans le cadre d'un déploiement de Windows](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-1.md)

## Autres ressources pour le déploiement du client MBAM


[Déploiement de MBAM1.0](deploying-mbam-10.md)

[Planification du déploiement de clients MBAM1.0](planning-for-mbam-10-client-deployment.md)

 

 





