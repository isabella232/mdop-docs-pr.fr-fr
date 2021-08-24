---
title: Déploiement de l'infrastructure de serveur MBAM 1.0
description: Déploiement de l'infrastructure de serveur MBAM 1.0
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
ms.openlocfilehash: 63099d425b51bfde52eac59771007b1c765acf05
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910419"
---
# <a name="deploying-the-mbam-10-server-infrastructure"></a>Déploiement de l'infrastructure de serveur MBAM 1.0


Vous pouvez installer les fonctionnalités du serveur MBAM (Microsoft BitLocker Administration and Monitoring) dans différentes configurations à l’aide d’un à cinq serveurs. En règle générale, vous devez utiliser une configuration de trois à cinq serveurs pour les environnements de production, en fonction de vos besoins en évolutivité. Pour plus d’informations sur l’évolutivité des performances de MBAM et des topologies de déploiement recommandées, voir le livre blanc sur l’évolutivité et [High-Availability MBAM.](https://go.microsoft.com/fwlink/p/?LinkId=258314)

## <a name="deploy-all-mbam-10-on-a-single-server"></a>Déployer tous les MBAM 1.0 sur un seul serveur


Dans cette configuration, toutes les fonctionnalités MBAM sont installées sur un seul serveur. Cette topologie de déploiement pour l’infrastructure serveur MBAM prendra en charge jusqu’à 21 000 ordinateurs clients MBAM.

**Important**  
Cette configuration est prise en charge, mais nous la recommandons uniquement pour les tests.

 

Les procédures de cette section décrivent l’installation complète des fonctionnalités MBAM sur un seul serveur.

[Installation et configuration de MBAM sur un seul serveur](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## <a name="deploy-mbam-10-on-distributed-servers"></a>Déployer MBAM 1.0 sur des serveurs distribués


Les fonctionnalités MBAM peuvent être installées dans différentes configurations, en fonction de vos besoins en évolutivité. Pour plus d’informations sur la planification du déploiement des fonctionnalités serveur MBAM, voir [Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md).

Les procédures de cette section décrivent l’installation complète des fonctionnalités MBAM sur des serveurs distribués.

### <a name="three-computer-configuration"></a>Configuration à trois ordinateurs

Le diagramme suivant montre la topologie de déploiement à trois ordinateurs pour MBAM. Nous recommandons cette topologie pour les environnements de production qui peuvent prendre en charge jusqu’à 55 000 clients MBAM.

![Topologie de déploiement d’ordinateur mbam 3.](images/mbam-3-server.jpg)

Dans cette configuration, les fonctionnalités MBAM sont installées dans la configuration suivante :

1.  La base de données de récupération et matérielle, la base de données de conformité et d’audit, ainsi que les rapports de conformité et d’audit sont installés sur un serveur.

2.  La fonctionnalité Serveur d’administration et de surveillance est installée sur un serveur.

3.  Le modèle de stratégie de groupe MBAM est installé sur un ordinateur capable de modifier les objets de stratégie de groupe (GPO).

### <a name="four-computer-configuration"></a>Configuration à quatre ordinateurs

Le diagramme suivant montre la topologie de déploiement à quatre ordinateurs pour MBAM. Nous vous recommandons cette topologie pour les environnements de production qui peuvent prendre en charge jusqu’à 110 000 clients MBAM.

![Topologie de déploiement d’ordinateur mbam 4.](images/mbam-4-computer.jpg)

Dans cette configuration, les fonctionnalités MBAM sont installées dans la configuration suivante :

1.  La base de données de récupération et matérielle, la base de données de conformité et d’audit, ainsi que les rapports de conformité et d’audit sont installés sur un serveur.

2.  La fonctionnalité Serveur d’administration et de surveillance est installée sur un serveur configuré dans un cluster de serveurs d’équilibrage de charge réseau (NLB).

3.  Le modèle de stratégie de groupe MBAM est installé sur un ordinateur capable de modifier les objets de stratégie de groupe.

### <a name="five-computer-configuration"></a>Configuration à cinq ordinateurs

Le diagramme suivant montre la topologie de déploiement à cinq ordinateurs pour MBAM. Nous recommandons cette topologie pour les environnements de production qui peuvent prendre en charge jusqu’à 135 000 clients MBAM.

![Topologie de déploiement d’ordinateur mbam 5.](images/mbam-5-computer.jpg)

Dans cette configuration, les fonctionnalités MBAM sont installées dans la configuration suivante :

1.  La base de données de récupération et matérielle est installée sur un serveur.

2.  La base de données de conformité et d’audit, ainsi que les rapports de conformité et d’audit sont installés sur un serveur.

3.  La fonctionnalité Serveur d’administration et de surveillance est installée sur un serveur configuré dans un cluster de serveurs d’équilibrage de charge réseau (NLB).

4.  Le modèle de stratégie de groupe MBAM est installé sur un ordinateur capable de modifier les objets de stratégie de groupe.

[Installation et configuration de MBAM sur des serveurs distribués](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[Configurer l'équilibrage de la charge réseau pour MBAM](how-to-configure-network-load-balancing-for-mbam.md)

## <a name="other-resources-for-mbam-10-server-features-deployment"></a>Autres ressources pour le déploiement des fonctionnalités de MBAM 1.0 Server


[Déploiement de MBAM 1.0](deploying-mbam-10.md)

 

 





