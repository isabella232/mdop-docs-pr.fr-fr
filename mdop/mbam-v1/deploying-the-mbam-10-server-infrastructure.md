---
title: Déploiement de l'infrastructure de serveur MBAM1.0
description: Déploiement de l'infrastructure de serveur MBAM1.0
author: dansimp
ms.assetid: 90529379-b70e-4c92-b188-3d7aaf1844af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de136db557233a097d95f47ef0a1bba5996798c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810998"
---
# Déploiement de l'infrastructure de serveur MBAM1.0


Vous pouvez installer les fonctionnalités serveur d’administration et de surveillance de BitLocker (MBAM) de Microsoft dans différentes configurations en utilisant un à cinq serveurs. En règle générale, vous devez utiliser une configuration de trois à cinq serveurs pour les environnements de production, en fonction de vos besoins en matière de modularité. Pour plus d’informations sur l’évolutivité des performances des topologies de déploiement MBAM et recommandées, consultez le livre blanc sur l' [évolutivité et la haute disponibilité du MBAM](https://go.microsoft.com/fwlink/p/?LinkId=258314).

## Déploiement de tous les 1,0 MBAM sur un serveur unique


Dans cette configuration, toutes les fonctionnalités de MBAM sont installées sur un seul serveur. Cette topologie de déploiement pour l’infrastructure de serveur MBAM prend en charge jusqu’à 21 000 ordinateurs client MBAM.

**Important**  Cette configuration est prise en charge, mais nous vous recommandons de la tester uniquement.

 

Les procédures dans cette section décrivent l’installation complète des fonctionnalités MBAM sur un serveur unique.

[Installation et configuration de MBAM sur un seul serveur](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## Déploiement de MBAM 1,0 sur des serveurs distribués


Les fonctionnalités de MBAM peuvent être installées dans différentes configurations, en fonction de vos besoins en matière de modularité. Pour plus d’informations sur la planification du déploiement de fonctionnalités MBAM Server, voir [planification du déploiement de MBAM 1,0 Server](planning-for-mbam-10-server-deployment.md).

Les procédures dans cette section décrivent l’installation complète des fonctionnalités MBAM sur les serveurs distribués.

### Configuration à trois ordinateurs

Le diagramme suivant montre la topologie de déploiement à trois ordinateurs pour MBAM. Nous vous recommandons d’utiliser cette topologie pour les environnements de production qui prennent en charge jusqu’aux clients MBAM 55 000.

![MBAM trois topologie de déploiement d’ordinateur](images/mbam-3-server.jpg)

Dans cette configuration, les fonctionnalités de MBAM sont installées dans la configuration suivante:

1.  Les rapports de conformité et de base de données matérielle, de conformité et d’audit sont installés sur un serveur.

2.  La fonctionnalité d’administration et de surveillance du serveur est installée sur un serveur.

3.  MBAM modèle de stratégie de groupe est installé sur un ordinateur capable de modifier des objets de stratégie de groupe.

### Configuration à quatre ordinateurs

Le diagramme ci-après présente la topologie de déploiement à quatre ordinateurs pour MBAM. Nous vous recommandons d’utiliser cette topologie pour les environnements de production qui prennent en charge jusqu’aux clients MBAM 110 000.

![MBAM 4 topologie de déploiement d’ordinateur.](images/mbam-4-computer.jpg)

Dans cette configuration, les fonctionnalités de MBAM sont installées dans la configuration suivante:

1.  Les rapports de conformité et de base de données matérielle, de conformité et d’audit sont installés sur un serveur.

2.  La fonctionnalité d’administration et de surveillance du serveur est installée sur un serveur configuré dans un cluster de serveurs de l’équilibrage de charge réseau.

3.  MBAM modèle de stratégie de groupe est installé sur un ordinateur capable de modifier les objets de stratégie de groupe.

### Configuration de cinq ordinateurs

Le diagramme suivant présente la topologie de déploiement à cinq ordinateurs pour MBAM. Nous vous recommandons d’utiliser cette topologie pour les environnements de production qui prennent en charge jusqu’aux clients MBAM 135 000.

![MBAM cinq topologie de déploiement d’ordinateur.](images/mbam-5-computer.jpg)

Dans cette configuration, les fonctionnalités de MBAM sont installées dans la configuration suivante:

1.  La base de données de récupération et de matériel est installée sur un serveur.

2.  Les rapports de conformité et d’audit sont installés sur un serveur.

3.  La fonctionnalité d’administration et de surveillance du serveur est installée sur un serveur configuré dans un cluster de serveurs de l’équilibrage de charge réseau.

4.  MBAM modèle de stratégie de groupe est installé sur un ordinateur capable de modifier des objets de stratégie de groupe.

[Installation et configuration de MBAM sur des serveurs distribués](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[Configurer l'équilibrage de la charge réseau pour MBAM](how-to-configure-network-load-balancing-for-mbam.md)

## Autres ressources pour le déploiement de fonctionnalités MBAM 1,0 Server


[Déploiement de MBAM1.0](deploying-mbam-10.md)

 

 





