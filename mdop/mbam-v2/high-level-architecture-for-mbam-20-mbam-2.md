---
title: Architecture de haut niveau pour MBAM 2.0
description: Architecture de haut niveau pour MBAM 2.0
author: dansimp
ms.assetid: 7f73dd3a-0b1f-4af6-a2f0-d0c5bc5d183a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f19480b5797362e6e4119fff9a14afd9d5a74d98
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910499"
---
# <a name="high-level-architecture-for-mbam-20"></a>Architecture de haut niveau pour MBAM 2.0


Microsoft BitLocker Administration and Monitoring (MBAM) est une solution client/serveur qui peut vous aider à simplifier l’approvisionnement et le déploiement de BitLocker, à améliorer la conformité et les rapports sur BitLocker et à réduire les coûts de support. Microsoft BitLocker Administration and Monitoring inclut les fonctionnalités décrites dans cette rubrique.

Microsoft BitLocker Administration and Monitoring peut être déployé dans la topologie autonome ou dans une topologie intégrée à Microsoft System Center Configuration Manager 2007 ou Microsoft System Center 2012 Configuration Manager. Cette rubrique décrit l’architecture de la topologie autonome. Pour plus d’informations sur le déploiement dans la topologie Configuration Manager intégrée, voir Utilisation de [MBAM avec Configuration Manager.](using-mbam-with-configuration-manager.md)

Le diagramme suivant illustre l’architecture recommandée MBAM pour un environnement de production, qui se compose de deux serveurs et d’une station de travail de gestion. Cette architecture prend en charge jusqu’à 200 000 clients MBAM. Les fonctionnalités serveur et les bases de données de l’image d’architecture sont décrites dans la section suivante et sont répertoriées sous l’ordinateur ou le serveur où nous vous recommandons de les installer.

**Remarque**  
Une architecture à serveur unique doit être utilisée uniquement dans les environnements de test.

 

![Topologie de déploiement à deux serveurs mbam 2.](images/mbam2-3-servers.gif)

## <a name="administration-and-monitoring-server"></a>Serveur d’administration et de surveillance


Les fonctionnalités suivantes sont installées sur ce serveur :

-   **Serveur d’administration et de surveillance.** La fonctionnalité Serveur d’administration et de surveillance est installée sur un serveur Windows et se compose du site web Administration et surveillance, qui inclut les rapports, le portail Help Desk et les services web de surveillance.

-   **Portail libre-service**. Le Self-Service'entreprise est installé sur un Windows serveur. Le portail Self-Service permet aux utilisateurs finaux sur les ordinateurs clients de se connecter indépendamment à un site web, où ils peuvent obtenir une clé de récupération pour récupérer un volume BitLocker verrouillé.

## <a name="database-server"></a>Serveur de base de données


Les fonctionnalités suivantes sont installées sur ce serveur :

-   **Base de données de récupération**. La base de données de récupération est installée sur un serveur Windows et une instance prise en charge de Microsoft SQL Server. Cette base de données stocke les données de récupération collectées à partir des ordinateurs clients MBAM.

-   **Base de données de conformité et d’audit.** La base de données de conformité et d’audit est installée sur Windows serveur et une instance de SQL Server. Cette base de données stocke les données de conformité pour les ordinateurs clients MBAM. Ces données sont utilisées principalement pour les rapports SQL Server Reporting Services (SSRS).

-   **Rapports de conformité et d’audit.** Les rapports de conformité et d’audit sont installés sur un serveur Windows et une instance de SQL Server prise en charge sur SQL Server Reporting Services (SSRS) est installée. Ces rapports fournissent des rapports MBAM accessibles à partir du site Web Administration et surveillance ou directement à partir du serveur SSRS.

## <a name="management-workstation"></a>Station de travail de gestion


La fonctionnalité suivante est installée sur la station de travail de gestion, qui peut être un serveur Windows ou un ordinateur client.

-   **Modèle de stratégie**. Le modèle de stratégie se compose de paramètres de stratégie de groupe qui définissent les paramètres d’implémentation MBAM pour le chiffrement de lecteur BitLocker. Vous pouvez installer le modèle de stratégie sur n’importe quel serveur ou station de travail, mais il est généralement installé sur une station de travail de gestion, qui est un serveur Windows ou un ordinateur client pris en charge. La station de travail n’a pas besoin d’être un ordinateur dédié.

## <a name="mbam-client"></a><a href="" id="---------mbam-client"></a> MBAM Client


Le client MBAM est installé sur un ordinateur Windows et présente les caractéristiques suivantes :

-   Utilise la stratégie de groupe pour appliquer le chiffrement de lecteur BitLocker des ordinateurs clients dans l’entreprise.

-   Collecte la clé de récupération pour les trois types de lecteur de données BitLocker : lecteurs de système d’exploitation, lecteurs de données fixes et lecteurs de données amovibles (USB).

-   Collecte les données de conformité de l’ordinateur et les transmet au système de rapports.

## <a name="related-topics"></a>Rubriques associées


[Prise en main de MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





