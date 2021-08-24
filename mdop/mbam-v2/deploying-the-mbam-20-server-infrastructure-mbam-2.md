---
title: Déploiement de l'infrastructure de serveur MBAM 2.0
description: Déploiement de l'infrastructure de serveur MBAM 2.0
author: dansimp
ms.assetid: 52e68d94-e2b4-4b06-ae55-f900ea6cc59f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8aee322b9a1aacbf98ff8362e95e21c2dd3d289a
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910799"
---
# <a name="deploying-the-mbam-20-server-infrastructure"></a>Déploiement de l'infrastructure de serveur MBAM 2.0


Les fonctionnalités du serveur MBAM (Microsoft BitLocker Administration and Monitoring) pour la topologie autonome peuvent être installées dans différentes configurations sur au moins deux serveurs dans un environnement de production. La configuration recommandée est de deux serveurs pour un environnement de production, en fonction de vos besoins en matière d’évolutivité. Utilisez un serveur unique pour une installation MBAM uniquement dans les environnements de test. Pour plus d’informations sur la planification du déploiement des fonctionnalités de MBAM Server, voir [Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md).

Le diagramme suivant montre un exemple de la façon dont vous pouvez configurer le déploiement MBAM à deux serveurs recommandé. Cette configuration prend en charge jusqu’à 200 000 clients MBAM dans un environnement de production. Les fonctionnalités serveur et les bases de données de l’image d’architecture sont décrites dans la section suivante et sont répertoriées sous l’ordinateur ou le serveur où nous vous recommandons de les installer.

![Topologie de déploiement à deux serveurs mbam 2.](images/mbam2-3-servers.gif)

## <a name="administration-and-monitoring-server"></a>Serveur d’administration et de surveillance


Les fonctionnalités suivantes sont installées sur ce serveur :

-   **Serveur d’administration et de surveillance.** La fonctionnalité Serveur d’administration et de surveillance est installée sur un serveur Windows et se compose du site web Help Desk et des services web de surveillance.

-   **Portail libre-service**. Le Self-Service'entreprise est installé sur un Windows serveur. Le portail Self-Service permet aux utilisateurs finaux sur les ordinateurs clients de se connecter indépendamment à un site web, où ils peuvent obtenir une clé de récupération pour récupérer un volume BitLocker verrouillé.

## <a name="database-server"></a>Serveur de base de données


Les fonctionnalités suivantes sont installées sur ce serveur :

-   **Base de données de récupération**. La base de données de récupération est installée sur un serveur Windows et une instance prise en charge de Microsoft SQL Server. Cette base de données stocke les données de récupération collectées à partir des ordinateurs clients MBAM.

-   **Base de données de conformité et d’audit.** La base de données de conformité et d’audit est installée sur Windows serveur et une instance de SQL Server. Cette base de données stocke les données de conformité pour les ordinateurs clients MBAM. Ces données sont utilisées principalement pour les rapports SQL Server Reporting Services (SSRS).

-   **Rapports de conformité et d’audit.** Les rapports de conformité et d’audit sont installés sur un serveur Windows et une instance de SQL Server prise en charge sur SQL Server Reporting Services (SSRS) est installée. Ces rapports fournissent des rapports MBAM accessibles à partir du site web Help Desk ou directement à partir du serveur SSRS.

## <a name="management-workstation"></a>Station de travail de gestion


La fonctionnalité suivante est installée sur la station de travail de gestion, qui peut être un serveur Windows ou un ordinateur client.

-   **Modèle de stratégie**. Le modèle de stratégie se compose de stratégies de groupe qui définissent les paramètres d’implémentation MBAM pour le chiffrement de lecteur BitLocker. Vous pouvez installer le modèle de stratégie sur n’importe quel serveur ou station de travail, mais il est généralement installé sur une station de travail de gestion, qui est un serveur Windows ou un ordinateur client pris en charge. La station de travail n’a pas besoin d’être un ordinateur dédié.

## <a name="mbam-client"></a><a href="" id="---------mbam-client"></a> MBAM Client


Le client MBAM est installé sur un ordinateur Windows et présente les caractéristiques suivantes :

-   Utilise la stratégie de groupe pour appliquer le chiffrement de lecteur BitLocker des ordinateurs clients dans l’entreprise.

-   Collecte la clé de récupération pour les trois types de lecteur de données BitLocker : lecteurs de système d’exploitation, lecteurs de données fixes et lecteurs de données amovibles (USB).

-   Collecte les données de conformité de l’ordinateur et les transmet au système de rapports.

## <a name="other-resources-for-deploying-mbam-20-server-features"></a>Autres ressources pour le déploiement des fonctionnalités serveur MBAM 2.0


[Déploiement de MBAM 2.0](deploying-mbam-20-mbam-2.md)

 

 





