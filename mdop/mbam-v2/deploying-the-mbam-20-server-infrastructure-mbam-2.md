---
title: Déploiement de l'infrastructure de serveur MBAM2.0
description: Déploiement de l'infrastructure de serveur MBAM2.0
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
ms.openlocfilehash: 22a69fe8f6853c02a818bb026b36771cd09632f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810746"
---
# Déploiement de l'infrastructure de serveur MBAM2.0


Les fonctionnalités de serveur d’administration et de surveillance de BitLocker pour la topologie autonome peuvent être installées dans différentes configurations sur deux serveurs ou plus dans un environnement de production. La configuration recommandée consiste à deux serveurs pour un environnement de production, en fonction de vos besoins en matière d’évolutivité. Utilisez un serveur unique pour une installation MBAM uniquement dans les environnements de test. Pour plus d’informations sur la planification du déploiement de la fonctionnalité MBAM Server, voir [planification du déploiement de MBAM 2,0 Server](planning-for-mbam-20-server-deployment-mbam-2.md).

Le diagramme suivant montre un exemple de la façon dont vous pouvez configurer le déploiement recommandé sur deux serveurs MBAM. Cette configuration prend en charge jusqu’à 200 000 clients MBAM dans un environnement de production. Les fonctionnalités de serveur et bases de données de l’architecture de l’architecture sont décrites dans la section suivante, qui s’affichent sur votre ordinateur ou serveur pour lequel nous vous recommandons de les installer.

![MBAM 2 2-topologie de déploiement de serveur](images/mbam2-3-servers.gif)

## Serveur d’administration et de surveillance


Les fonctionnalités suivantes sont installées sur ce serveur:

-   **Serveur d’administration et de surveillance**. La fonctionnalité d’administration et de surveillance du serveur est installée sur un serveur Windows et se compose du site Web du support technique et des services Web de surveillance.

-   **Portail libre-service**. Le portail libre-service est installé sur un serveur Windows. Le portail libre-service permet aux utilisateurs finaux sur les ordinateurs clients de se connecter de manière indépendante à un site Web, à partir duquel ils peuvent obtenir une clé de récupération pour récupérer un volume BitLocker verrouillé.

## Serveur de base de données


Les fonctionnalités suivantes sont installées sur ce serveur:

-   **Base de données de récupération**. La base de données de récupération est installée sur un serveur Windows et sur une instance de Microsoft SQLServer qui est prise en charge. Cette base de données stocke les données de récupération collectées à partir des ordinateurs clients MBAM.

-   **Base de données d’audit et de conformité**. La base de données d’audit et de conformité est installée sur un serveur Windows et sur une instance de SQLServer prise en charge. Cette base de données stocke les données de conformité pour les ordinateurs clients MBAM. Ces données sont principalement utilisées pour les rapports hébergés par SQL Server Reporting Services (SSRS).

-   **Rapports de conformité et d’audit**. Les rapports de conformité et d’audit sont installés sur un serveur Windows et une instance prise en charge de SQLServer pour lequel la fonctionnalité SQL Server Reporting Services (SSRS) est installée. Ces rapports fournissent des rapports MBAM auxquels vous pouvez accéder à partir du site Web de l’assistance ou directement à partir du serveur SSRS.

## Station de travail de gestion


La fonctionnalité suivante est installée sur la station de travail de gestion, qui peut être un ordinateur Windows Server ou un ordinateur client.

-   **Modèle de stratégie**. Le modèle de stratégie est composé de stratégies de groupe définissant les paramètres d’implémentation de MBAM pour le chiffrement de lecteur BitLocker. Vous pouvez installer le modèle de stratégie sur n’importe quel serveur ou station de travail, mais il est généralement installé sur une station de travail de gestion (ordinateur client ou client pris en charge). La station de travail ne doit pas nécessairement être un ordinateur dédié.

## <a href="" id="---------mbam-client"></a> Client MBAM


Le client MBAM est installé sur un ordinateur Windows et il présente les caractéristiques suivantes:

-   Utilise une stratégie de groupe pour appliquer le chiffrement de lecteur BitLocker d’ordinateurs clients au sein de l’entreprise.

-   Collecte la clé de récupération pour les trois types de lecteurs de données BitLocker: lecteurs du système d’exploitation, lecteurs de données fixes et lecteurs de données amovibles (USB).

-   Collecte les données de conformité de l’ordinateur et transmet les données au système de création de rapports.

## Autres ressources pour le déploiement des fonctionnalités du serveur MBAM 2,0


[Déploiement de MBAM2.0](deploying-mbam-20-mbam-2.md)

 

 





