---
title: Préparation de votre environnement pour MBAM2.0
description: Préparation de votre environnement pour MBAM2.0
author: dansimp
ms.assetid: 5fb01da9-620e-4992-9e54-2ed3fb69e6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1be989112d456064db302952d50159d00b5597a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811256"
---
# Préparation de votre environnement pour MBAM2.0


Avant de lancer le programme d’installation de Microsoft BitLocker (MBAM), vous devez vérifier que vous remplissez les conditions préalables à l’installation du produit. Lorsque vous savez ce que sont les conditions préalables, vous pouvez déployer le produit de façon efficace et activer ses fonctionnalités afin qu’il prenne en charge les objectifs métiers de votre organisation.

Si vous déployez l’administration et la surveillance de BitLocker avec Microsoft System Center Configuration Manager 2007 ou MicrosoftSystemCenter2012, voir [planification du déploiement d’MBAM avec Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

## Consulter la configuration requise pour le déploiement d’MBAM 2,0


Le client MBAM et toutes les fonctionnalités du serveur MBAM possèdent des éléments requis spécifiques qui doivent être satisfaits pour pouvoir être installés correctement.

Pour garantir la réussite de l’installation des clients MBAM et des fonctionnalités du serveur MBAM, assurez-vous que les ordinateurs spécifiés pour l’installation de la fonctionnalité du client MBAM ou MBAM du serveur sont bien préparés pour l’installation de MBAM.

**Remarques**  Le programme d’installation de MBAM vérifie que toutes les conditions préalables sont remplies avant le début de l’installation. Si toutes les conditions préalables ne sont pas remplies, le programme d’installation ne fonctionnera pas.

 

[Conditions préalables au déploiement de MBAM2.0](mbam-20-deployment-prerequisites-mbam-2.md)

## Plan pour les exigences de la stratégie de groupe MBAM 2,0


Avant que MBAM ne puisse gérer des clients au sein de l’entreprise, vous devez définir une stratégie de groupe pour les besoins de chiffrement de votre environnement.

**Important**  MBAM ne fonctionne pas avec des stratégies pour le chiffrement de lecteur BitLocker autonome. Les paramètres de stratégie de groupe doivent être définis pour MBAM ou le chiffrement et l’application de BitLocker échoueront.

 

[Planification des exigences en matière de stratégie de groupe MBAM2.0](planning-for-mbam-20-group-policy-requirements-mbam-2.md)

## Planifier les rôles d’administrateur MBAM 2,0


Les rôles d’administrateur MBAM sont gérés par des groupes locaux créés par MBAM, lorsque vous installez le serveur d’administration et de surveillance de BitLocker, que vous utilisez la fonctionnalité rapports de conformité et d’audit, ainsi que la base de données état de conformité et d’audit.

L’appartenance aux rôles d’administration et de surveillance de BitLocker peut être mieux gérée en créant des groupes de sécurité dans ActiveDirectoryDomainServices, en ajoutant les comptes d’administrateur appropriés à ces groupes, puis en ajoutant ces groupes de sécurité à l’administration de BitLocker et en surveillant les groupes locaux. Pour plus d’informations, reportez-vous [à la rubrique gestion des rôles d’administrateur de MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md).

## Autres ressources pour la planification de MBAM


[Planification de MBAM2.0](planning-for-mbam-20-mbam-2.md)

[Configurations prises en charge par MBAM2.0](mbam-20-supported-configurations-mbam-2.md)

 

 





