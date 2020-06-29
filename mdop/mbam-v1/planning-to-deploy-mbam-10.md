---
title: Planification du déploiement de MBAM1.0
description: Planification du déploiement de MBAM1.0
author: dansimp
ms.assetid: 30ad4304-45c6-427d-8e33-ebe8053c7871
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2ff25e705717db5086150ed08a5640335bbacb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809804"
---
# Planification du déploiement de MBAM1.0


Vous devez prendre en considération un certain nombre de configurations et de configurations de déploiement différentes pour pouvoir créer votre plan de déploiement d’MBAM (Microsoft BitLocker Administration and Analysis 1,0). Cette section contient des informations qui vous aideront à collecter les informations nécessaires pour formuler un plan de déploiement qui répond le mieux à vos besoins professionnels.

## Examiner les configurations prises en charge par MBAM 1,0


Après avoir préparé votre environnement informatique pour l’installation du client MBAM et de la fonctionnalité serveur, assurez-vous d’examiner les informations de configurations prises en charge pour MBAM pour vérifier que les ordinateurs sur lesquels vous installez MBAM répondent à la configuration minimale requise du système d’exploitation. Pour plus d’informations sur les conditions préalables pour le déploiement d’MBAM, voir [conditions préalables pour le déploiement d’MBAM 1,0](mbam-10-deployment-prerequisites.md).

[Configurations prises en charge par MBAM1.0](mbam-10-supported-configurations.md)

## Planifier le déploiement du serveur et du client MBAM 1,0


L’infrastructure du serveur MBAM dépend d’un ensemble de fonctionnalités serveur qui peuvent être installées sur un ou plusieurs ordinateurs serveur, en fonction des besoins de l’entreprise. Ces fonctionnalités peuvent être installées sur un serveur unique ou distribuées sur plusieurs serveurs.

Le client MBAM permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise. Le client BitLocker peut être intégré à une organisation en déployant le client via des outils tels que les services de domaine Active Directory (AD FS) ou en chiffrant directement les ordinateurs clients dans le cadre du processus d’imagerie initial.

Avec MBAM, vous pouvez chiffrer un ordinateur de votre organisation avant que l’utilisateur final ne reçoive l’ordinateur ou après, à l’aide d’une stratégie de groupe. Vous pouvez appliquer l’une ou l’autre des méthodes au sein de votre organisation. Si vous choisissez d’utiliser les deux méthodes, vous pouvez améliorer la conformité, la création de rapports et la prise en charge de la récupération de clés.

[Planification du déploiement de serveursMBAM1.0](planning-for-mbam-10-server-deployment.md)

[Planification du déploiement de clients MBAM1.0](planning-for-mbam-10-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a>Autres ressources pour la planification de MBAM


-   [Planification de MBAM1.0](planning-for-mbam-10.md)

 

 





