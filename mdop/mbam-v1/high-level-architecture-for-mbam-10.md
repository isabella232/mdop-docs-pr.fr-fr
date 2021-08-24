---
title: Architecture de haut niveau pour MBAM 1.0
description: Architecture de haut niveau pour MBAM 1.0
author: dansimp
ms.assetid: b1349196-88ed-4d6c-8a1d-998f18127b6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d06c7bd801a9dd63916d310af75e88a307e7226a
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910409"
---
# <a name="high-level-architecture-for-mbam-10"></a>Architecture de haut niveau pour MBAM 1.0


Microsoft BitLocker Administration and Monitoring (MBAM) est une solution de chiffrement de données client/serveur qui peut vous aider à simplifier l’approvisionnement et le déploiement de BitLocker, à améliorer la conformité et la reporting de BitLocker et à réduire les coûts de support. MBAM inclut les fonctionnalités décrites dans cette rubrique.

En outre, il existe une vidéo qui fournit une vue d’ensemble de l’architecture MBAM et du programme d’installation de MBAM. Pour plus d’informations, voir [Vue d’ensemble du déploiement et de l’architecture MBAM.](https://go.microsoft.com/fwlink/p/?LinkId=258392)

## <a name="architecture-overview"></a>Vue d’ensemble de l’architecture


Le diagramme suivant affiche l’architecture MBAM. La topologie de déploiement MBAM à serveur unique présente les fonctionnalités MBAM. Toutefois, cette topologie de déploiement MBAM est recommandée uniquement pour les environnements de laboratoire.

**Remarque**  
Au moins une topologie de déploiement MBAM à trois ordinateurs est recommandée pour un déploiement de production. Pour plus d’informations sur les topologies de déploiement MBAM, voir [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).

 

![Topologie de déploiement à serveur unique mbam.](images/mbam-1-server.jpg)

1.  **Serveur d’administration et de surveillance.** Le serveur d’administration et de surveillance MBAM est installé sur un serveur Windows et héberge le site web Administration et gestion de MBAM et les services web de surveillance. Le site Web Administration et gestion MBAM permet de déterminer l’état de conformité de l’entreprise, d’auditer l’activité, de gérer les fonctionnalités matérielles et d’accéder aux données de récupération, telles que les clés de récupération BitLocker. Le serveur d’administration et de surveillance se connecte aux bases de données et services suivants :

    -   Base de données matérielle et de récupération. La base de données de récupération et de matériel est installée sur un serveur Windows et prise en charge SQL Server instance. Cette base de données stocke les données de récupération et les informations matérielles collectées à partir des ordinateurs clients MBAM.

    -   Base de données de conformité et d’audit. La base de données de conformité et d’audit est installée sur un serveur Windows et prise en charge SQL Server instance. Cette base de données stocke les données de conformité pour les ordinateurs clients MBAM. Ces données sont utilisées principalement pour les rapports hébergés par SQL Server Reporting Services (SSRS).

    -   Rapports de conformité et d’audit. Les rapports de conformité et d’audit sont installés sur un serveur Windows et pris en charge SQL Server instance où la fonctionnalité SSRS est installée. Ces rapports fournissent des rapports d’administration et de surveillance de Microsoft BitLocker. Ces rapports sont accessibles à partir du site Web Administration et gestion de MBAM ou directement à partir du serveur SSRS.

2.  **Client MBAM**. Le client d’administration et de surveillance De Microsoft BitLocker effectue les tâches suivantes :

    -   Utilise la stratégie de groupe pour appliquer le chiffrement BitLocker des ordinateurs clients dans l’entreprise.

    -   Collecte la clé de récupération pour les trois types de lecteur de données BitLocker : lecteurs de système d’exploitation, lecteurs de données fixes et lecteurs de données amovibles (USB).

    -   Collecte des informations de récupération et des informations matérielles sur les ordinateurs clients.

    -   Collecte les données de conformité de l’ordinateur et les transmet au système de rapports.

3.  **Modèle de stratégie**. Le modèle de stratégie de groupe MBAM est installé sur un serveur ou un ordinateur client Windows pris en charge. Ce modèle permet de spécifier les paramètres d’implémentation MBAM pour le chiffrement de lecteur BitLocker.

## <a name="related-topics"></a>Rubriques associées


[Prise en main de MBAM 1.0](getting-started-with-mbam-10.md)

 

 





