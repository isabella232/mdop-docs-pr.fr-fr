---
title: Planification du déploiement de MBAM2.5
description: Planification du déploiement de MBAM2.5
author: dansimp
ms.assetid: 1343b80c-d87a-42e7-b912-e84ba997d7e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e955b426b00539aa2a4ef0b7c3a6650b05633a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811909"
---
# Planification du déploiement de MBAM2.5


Vous devez prendre en considération un certain nombre de configurations et de configurations de déploiement différentes pour pouvoir créer votre plan de déploiement pour l’administration et la surveillance de BitLocker (MBAM). Cette section contient des informations qui vous aideront à collecter les informations nécessaires pour formuler une offre de déploiement adaptée à vos besoins professionnels.

## Examiner les configurations prises en charge par MBAM 2,5


Après avoir préparé votre environnement informatique pour le déploiement de la fonctionnalité du client MBAM et du serveur, assurez-vous d’examiner les configurations prises en charge pour vérifier que les ordinateurs sur lesquels vous installez MBAM répondent à la configuration minimale requise en matière de matériel et de système d’exploitation. Pour plus d’informations sur les conditions préalables pour le déploiement d’MBAM, voir [conditions préalables pour le déploiement d’MBAM 2,5](mbam-25-deployment-prerequisites.md).

[Configurations prises en charge par MBAM2.5](mbam-25-supported-configurations.md)

## Planifier le déploiement du serveur et du client MBAM 2,5


L’infrastructure du serveur MBAM dépend d’un ensemble de fonctionnalités serveur qui peuvent être configurées sur un ou plusieurs ordinateurs serveur, en fonction des besoins de l’entreprise. Ces fonctionnalités peuvent être configurées dans une configuration distribuée sur plusieurs serveurs.

**Remarques**  Une installation MBAM sur un seul serveur est recommandée uniquement dans les environnements de laboratoire.

 

Le client MBAM permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise. Le client BitLocker peut être intégré à une organisation en déployant le client par le biais d’un système de remise de logiciels d’entreprise ou en installant le client sur des ordinateurs clients dans le cadre du processus d’image initial.

Avec MBAM, vous pouvez chiffrer un ordinateur au sein de votre organisation avant d’avoir reçu l’ordinateur, ou après une stratégie de groupe.

[Planification du déploiement de serveursMBAM2.5](planning-for-mbam-25-server-deployment.md)

[Planification du déploiement de clients MBAM2.5](planning-for-mbam-25-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a>Autres ressources pour la planification de MBAM


[Planification de MBAM2.5](planning-for-mbam-25.md)

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

 

 





