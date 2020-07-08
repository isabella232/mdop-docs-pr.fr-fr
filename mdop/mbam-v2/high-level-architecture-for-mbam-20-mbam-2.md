---
title: Architecture de hautniveau pour MBAM2.0
description: Architecture de hautniveau pour MBAM2.0
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
ms.openlocfilehash: ddc061a1aec5141548c2d2141be38f8501d2244d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810715"
---
# Architecture de hautniveau pour MBAM2.0


Le programme d’administration et de surveillance de Microsoft BitLocker (MBAM) est une solution client/serveur qui vous permet de simplifier la mise en service et le déploiement de BitLocker, d’améliorer la conformité et la création de rapports sur BitLocker et de réduire les coûts de prise en charge. L’administration et la surveillance de Microsoft BitLocker incluent les fonctionnalités décrites dans cette rubrique.

L’administration et le suivi de BitLocker peuvent être déployés dans la topologie autonome ou dans une topologie intégrée à Microsoft System Center Configuration Manager 2007 ou MicrosoftSystemCenter2012. Cette rubrique décrit l’architecture de la topologie autonome. Pour plus d’informations sur le déploiement dans la topologie intégré de Configuration Manager, voir [utilisation de MBAM avec Configuration Manager](using-mbam-with-configuration-manager.md).

Le diagramme suivant illustre l’architecture recommandée de MBAM pour un environnement de production, qui comprend deux serveurs et une station de travail de gestion. Cette architecture prend en charge jusqu’à 200 000 clients MBAM. Les fonctionnalités de serveur et bases de données de l’architecture de l’architecture sont décrites dans la section suivante, qui s’affichent sur votre ordinateur ou serveur pour lequel nous vous recommandons de les installer.

**Remarques**  Une architecture à serveur unique doit être utilisée uniquement dans les environnements de test.

 

![MBAM 2 2-topologie de déploiement de serveur](images/mbam2-3-servers.gif)

## Serveur d’administration et de surveillance


Les fonctionnalités suivantes sont installées sur ce serveur:

-   **Serveur d’administration et de surveillance**. La fonctionnalité d’administration et de surveillance du serveur est installée sur un serveur Windows et se compose du site Web d’administration et de surveillance, qui inclut les rapports et le portail du support technique, ainsi que les services Web de surveillance.

-   **Portail libre-service**. Le portail libre-service est installé sur un serveur Windows. Le portail libre-service permet aux utilisateurs finaux sur les ordinateurs clients de se connecter de manière indépendante à un site Web, à partir duquel ils peuvent obtenir une clé de récupération pour récupérer un volume BitLocker verrouillé.

## Serveur de base de données


Les fonctionnalités suivantes sont installées sur ce serveur:

-   **Base de données de récupération**. La base de données de récupération est installée sur un serveur Windows et sur une instance de Microsoft SQLServer qui est prise en charge. Cette base de données stocke les données de récupération collectées à partir des ordinateurs clients MBAM.

-   **Base de données d’audit et de conformité**. La base de données d’audit et de conformité est installée sur un serveur Windows et sur une instance de SQLServer prise en charge. Cette base de données stocke les données de conformité pour les ordinateurs clients MBAM. Ces données sont principalement utilisées pour les rapports hébergés par SQL Server Reporting Services (SSRS).

-   **Rapports de conformité et d’audit**. Les rapports de conformité et d’audit sont installés sur un serveur Windows et une instance prise en charge de SQLServer pour lequel la fonctionnalité SQL Server Reporting Services (SSRS) est installée. Ces rapports fournissent des rapports MBAM auxquels vous pouvez accéder à partir du site Web d’administration et de surveillance ou directement à partir du serveur SSRS.

## Station de travail de gestion


La fonctionnalité suivante est installée sur la station de travail de gestion, qui peut être un ordinateur Windows Server ou un ordinateur client.

-   **Modèle de stratégie**. Le modèle de stratégie est composé de paramètres de stratégie de groupe définissant les paramètres d’implémentation de MBAM pour le chiffrement de lecteur BitLocker. Vous pouvez installer le modèle de stratégie sur n’importe quel serveur ou station de travail, mais il est généralement installé sur une station de travail de gestion (ordinateur client ou client pris en charge). La station de travail ne doit pas nécessairement être un ordinateur dédié.

## <a href="" id="---------mbam-client"></a> Client MBAM


Le client MBAM est installé sur un ordinateur Windows et il présente les caractéristiques suivantes:

-   Utilise une stratégie de groupe pour appliquer le chiffrement de lecteur BitLocker d’ordinateurs clients au sein de l’entreprise.

-   Collecte la clé de récupération pour les trois types de lecteurs de données BitLocker: lecteurs du système d’exploitation, lecteurs de données fixes et lecteurs de données amovibles (USB).

-   Collecte les données de conformité de l’ordinateur et transmet les données au système de création de rapports.

## Rubriques connexes


[Prise en main de MBAM2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





