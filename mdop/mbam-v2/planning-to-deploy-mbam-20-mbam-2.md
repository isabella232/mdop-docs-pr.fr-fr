---
title: Planification du déploiement de MBAM2.0
description: Planification du déploiement de MBAM2.0
author: dansimp
ms.assetid: 2dc05fcd-aed9-4315-aeaf-92aaa9e0e955
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c7f065e52655212261dfe8b6b3f081f697142473
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811273"
---
# Planification du déploiement de MBAM2.0


Vous devez prendre en considération un certain nombre de configurations et de configurations de déploiement différentes pour pouvoir créer votre plan de déploiement pour l’administration et la surveillance de BitLocker (MBAM). Cette section contient des informations qui vous aideront à collecter les informations nécessaires pour formuler une offre de déploiement adaptée à vos besoins professionnels. Si vous installez MBAM avec la topologie Configuration Manager, consultez [planification du déploiement de MBAM avec Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) pour plus d’informations de planification.

## Examiner les configurations prises en charge par MBAM 2,0


Après avoir préparé votre environnement informatique pour l’installation de la fonctionnalité client et MBAM Server et, assurez-vous d’examiner les configurations prises en charge pour vérifier que les ordinateurs sur lesquels vous installez MBAM présentent la configuration minimale requise en matière de matériel et de système d’exploitation. Pour plus d’informations sur les conditions préalables pour le déploiement d’MBAM, voir [conditions préalables pour le déploiement d’MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md).

[Configurations prises en charge par MBAM2.0](mbam-20-supported-configurations-mbam-2.md)

## Planifier le déploiement du serveur et du client MBAM 2,0


L’infrastructure du serveur MBAM dépend d’un ensemble de fonctionnalités serveur qui peuvent être installées sur un ou plusieurs ordinateurs serveur, en fonction des besoins de l’entreprise. Ces fonctionnalités peuvent être installées dans une configuration distribuée sur plusieurs serveurs.

**Remarques**  Une installation MBAM sur un seul serveur est recommandée uniquement dans les environnements de laboratoire.

 

Le client MBAM permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise. Le client BitLocker peut être intégré au sein d’une organisation en déployant le client par le biais d’un système de distribution de logiciels d’entreprise ou en installant l’agent client sur les ordinateurs clients dans le cadre du processus d’image initial.

Avec MBAM, vous pouvez chiffrer un ordinateur au sein de votre organisation avant d’avoir reçu l’ordinateur, ou après une stratégie de groupe.

[Planification du déploiement de serveursMBAM2.0](planning-for-mbam-20-server-deployment-mbam-2.md)

[Planification du déploiement de clients MBAM2.0](planning-for-mbam-20-client-deployment-mbam-2.md)

## <a href="" id="other-resources-for-mbam-planning-"></a>Autres ressources pour la planification de MBAM


[Planification de MBAM2.0](planning-for-mbam-20-mbam-2.md)

 

 





