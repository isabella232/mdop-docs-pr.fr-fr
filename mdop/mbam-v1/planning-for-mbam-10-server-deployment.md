---
title: Planification du déploiement de serveursMBAM1.0
description: Planification du déploiement de serveursMBAM1.0
author: dansimp
ms.assetid: 3cbef284-3092-4c42-9234-2826b18ddef1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 76ff9c444ce3f9c39161341610fb0cd9a763dc6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804219"
---
# Planification du déploiement de serveursMBAM1.0


L’infrastructure du serveur d’administration et de surveillance de BitLocker (MBAM) Microsoft dépend d’un ensemble de fonctionnalités serveur qui peuvent être installées sur un ou plusieurs ordinateurs serveur, en fonction des besoins de votre entreprise.

## Planification du déploiement de MBAM Server


Les fonctionnalités MBAM suivantes représentent l’infrastructure serveur pour un déploiement de MBAM Server:

-   Base de données de récupération et de matériel

-   Base de données d’audit et de conformité

-   Rapports de conformité et d’audit

-   Serveur d’administration et de surveillance

Les fonctionnalités et bases de données de MBAM Server peuvent être installées dans différentes configurations, en fonction de vos besoins en matière de modularité. Toutes les fonctionnalités de MBAM Server peuvent être installées sur un serveur unique ou distribuées sur plusieurs serveurs. En général, nous vous recommandons d’utiliser une configuration à trois ou cinq serveurs pour les environnements de production, même si les configurations de deux ou quatre serveurs peuvent également être utilisées, en fonction de vos besoins informatiques.

**Remarques**  Pour plus d’informations sur l’évolutivité des performances des topologies de déploiement MBAM et recommandées, consultez le livre blanc sur l’évolutivité et la haute disponibilité du MBAM à l’adresse <https://go.microsoft.com/fwlink/p/?LinkId=258314> .

 

Chaque fonctionnalité MBAM comporte des éléments requis spécifiques. Pour obtenir la liste complète des conditions préalables pour les fonctionnalités du serveur et la configuration matérielle et logicielle requise, voir Configuration requise pour le [déploiement d’MBAM 1,0](mbam-10-deployment-prerequisites.md) et [Configurations prises en charge par MBAM 1,0](mbam-10-supported-configurations.md).

Outre les fonctionnalités de MBAM liées au serveur, l’application de configuration du serveur inclut un modèle de stratégie de groupe MBAM. Ce modèle peut être installé sur n’importe quel ordinateur qui peut exécuter la console de gestion des stratégies de groupe (GPMC) ou Advanced Group Policy Management (AGPM).

## Ordre de déploiement des fonctionnalités du serveur MBAM


Lorsque vous déployez les fonctionnalités du serveur MBAM, installez les fonctionnalités dans l’ordre suivant:

1.  Base de données de récupération et de matériel

2.  Base de données d’audit et de conformité

3.  Rapports et audit de conformité

4.  Serveur d’administration et de surveillance

5.  Modèle de stratégie

**Remarques**  Assurez le suivi des noms des ordinateurs sur lesquels vous installez chaque fonctionnalité. Vous utiliserez ces informations tout au long du processus d’installation. Vous pouvez imprimer et utiliser une liste de vérification de déploiement pour vous aider dans le processus d’installation. Pour plus d’informations sur la liste de vérification de déploiement d’MBAM, voir [liste de vérification de déploiement 1,0 MBAM](mbam-10-deployment-checklist.md).

 

## Rubriques connexes


[Planification du déploiement de MBAM1.0](planning-to-deploy-mbam-10.md)

[Déploiement de l'infrastructure de serveur MBAM1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





