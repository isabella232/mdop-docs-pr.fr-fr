---
title: Planification du déploiement de serveursMBAM2.0
description: Planification du déploiement de serveursMBAM2.0
author: dansimp
ms.assetid: b57f1a42-134f-4997-8697-7fbed08e2fc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57e6510556522dce029c958172bd89a361e06b83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804357"
---
# Planification du déploiement de serveursMBAM2.0


L’infrastructure du serveur d’administration et de surveillance de BitLocker (MBAM) Microsoft dépend d’un ensemble de fonctionnalités serveur qui peuvent être installées sur un ou plusieurs ordinateurs serveur, en fonction des besoins de l’entreprise. Si vous installez l’administration et la surveillance de BitLocker avec la topologie de Configuration Manager, consultez [planification du déploiement d’MBAM avec Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

**Remarques**  Les installations de l’administration et de l’analyse de BitLocker sur un seul serveur sont recommandées uniquement pour les environnements de test.

 

## Planification du déploiement de MBAM Server


L’infrastructure d’un déploiement MBAM Server inclut les fonctionnalités suivantes:

-   Base de données de récupération

-   Base de données d’audit et de conformité

-   Rapports de conformité et d’audit

-   Portail libre-service

-   Serveur d’administration et de surveillance

-   Modèle de stratégie de groupe MBAM

Les fonctionnalités et bases de données de MBAM Server peuvent être installées dans différentes configurations, en fonction de vos besoins en matière de modularité. Toutes les fonctionnalités de MBAM Server peuvent être installées sur un serveur unique ou distribuées sur plusieurs serveurs. Nous vous recommandons d’utiliser une configuration à deux serveurs pour les environnements de production, même si les configurations de 2 à 4 serveurs peuvent également être utilisées, en fonction de vos besoins informatiques.

Chaque fonctionnalité MBAM comporte des éléments requis spécifiques. Pour obtenir la liste complète des conditions préalables pour les fonctionnalités du serveur et la configuration matérielle et logicielle requise, voir Configuration requise pour le [déploiement d’MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md) et [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).

Outre les fonctionnalités de MBAM liées au serveur, l’application de configuration du serveur inclut un modèle de stratégie de groupe MBAM. Le modèle contient des paramètres d’objets de stratégie de groupe que vous configurez pour gérer le chiffrement de lecteur BitLocker au sein de l’entreprise. Vous pouvez installer ce modèle sur n’importe quel ordinateur qui peut exécuter la console de gestion des stratégies de groupe (GPMC) ou Advanced Group Policy Management (AGPM).

Lorsque vous planifiez le déploiement du serveur MBAM, envisagez d’utiliser des clés de récupération BitLocker dans MBAM pour une utilisation unique, après avoir expiré les clés de récupération. Pour que les clés expirent après utilisation, elles doivent être récupérées par le biais du portail du support technique ou du portail libre-service.

## Ordre de déploiement des fonctionnalités du serveur MBAM


Pour déployer les fonctionnalités MBAM sur plusieurs serveurs, vous devez installer les fonctionnalités dans l’ordre suivant:

1.  Base de données de récupération

2.  Base de données d’audit et de conformité

3.  Rapports et audit de conformité

4.  Portail libre-service

5.  Serveur d’administration et de surveillance

6.  Modèle de stratégie de groupe MBAM

**Remarques**  Assurez le suivi des noms des ordinateurs sur lesquels vous installez chaque fonctionnalité. Vous devez utiliser ces informations tout au long du processus d’installation. Vous pouvez imprimer et utiliser une liste de vérification de déploiement pour faciliter la tâche. Pour plus d’informations sur la liste de vérification de déploiement d’MBAM, voir [liste de vérification de déploiement 2,0 MBAM](mbam-20-deployment-checklist-mbam-2.md).

 

## Rubriques connexes


[Planification du déploiement de MBAM2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Déploiement de l'infrastructure de serveur MBAM2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





