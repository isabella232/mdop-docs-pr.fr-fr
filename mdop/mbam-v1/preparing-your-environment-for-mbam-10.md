---
title: Préparation de votre environnement pour MBAM1.0
description: Préparation de votre environnement pour MBAM1.0
author: dansimp
ms.assetid: 915f7c3c-70ad-4a90-a434-73e7fba97ecb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a2de4e825d5c89aeabcf57d78dc856bacb03e11
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809809"
---
# Préparation de votre environnement pour MBAM1.0


Avant de commencer la configuration de l’administration et de la surveillance de BitLocker (MBAM) Microsoft, assurez-vous que vous remplissez les conditions préalables nécessaires pour installer le produit. Si vous connaissez les conditions préalables à l’avance, vous pouvez déployer efficacement le produit et activer ses fonctionnalités, qui peuvent prendre en charge les objectifs métiers de votre organisation de manière plus efficace.

## Consulter la configuration requise pour le déploiement d’MBAM 1,0


Le client MBAM et toutes les fonctionnalités du serveur MBAM possèdent des éléments requis spécifiques qui doivent être satisfaits pour pouvoir être installés correctement.

Pour garantir la réussite de l’installation de clients MBAM et de fonctionnalités de serveur MBAM, vous devez vous assurer que les ordinateurs spécifiés pour l’installation du client MBAM ou du MBAM Server sont correctement préparés pour l’installation de MBAM.

**Remarques**  La configuration de MBAM vérifie si toutes les conditions préalables sont remplies avant le début de l’installation. Si ce n’est pas le cas, cela peut échouer.

 

[Conditions préalables au déploiement de MBAM1.0](mbam-10-deployment-prerequisites.md)

## Plan pour les exigences de la stratégie de groupe MBAM 1,0


Avant que MBAM ne puisse gérer des clients au sein de l’entreprise, vous devez définir la stratégie de groupe pour les besoins de chiffrement de votre environnement.

**Important**  MBAM ne fonctionne pas avec des stratégies pour le chiffrement de lecteur BitLocker autonome. La stratégie de groupe doit être définie pour MBAM; dans le cas contraire, le chiffrement et l’application de BitLocker échouent.

 

[Planification des exigences en matière de stratégie de groupe MBAM1.0](planning-for-mbam-10-group-policy-requirements.md)

## Planifier les rôles d’administrateur MBAM 1,0


Les rôles d’administrateur MBAM sont gérés par des groupes locaux créés par MBAM, lorsque vous installez ce qui suit: le serveur d’administration et de surveillance BitLocker, la fonctionnalité de conformité et d’audit, ainsi que la base de données état de conformité et d’audit.

L’appartenance aux rôles MBAM peut être gérée plus efficacement si vous créez des groupes de sécurité dans ActiveDirectoryDomainServices, ajoutez les comptes d’administrateur appropriés à ces groupes, puis ajoutez ces groupes de sécurité aux groupes locaux MBAM. Pour plus d’informations, reportez-vous [à la rubrique gestion des rôles d’administrateur de MBAM](how-to-manage-mbam-administrator-roles-mbam-1.md).

[Planification des rôles administrateur de MBAM1.0](planning-for-mbam-10-administrator-roles.md)

## Autres ressources pour la planification de MBAM


[Planification de MBAM1.0](planning-for-mbam-10.md)

 

 





