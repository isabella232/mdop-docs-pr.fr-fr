---
title: Architecture de haut niveau pour MBAM1.0
description: Architecture de haut niveau pour MBAM1.0
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
ms.openlocfilehash: de3529fdb565859fcc212d1a9a614ac4ef4b183e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811034"
---
# Architecture de haut niveau pour MBAM1.0


Le programme d’administration et de surveillance de BitLocker Microsoft (MBAM) est une solution de chiffrement de données client/serveur qui vous permet de simplifier la mise en service et le déploiement de BitLocker, d’améliorer la conformité et la création de rapports de BitLocker et de réduire les coûts de prise en charge. MBAM inclut les fonctionnalités décrites dans cette rubrique.

De plus, il existe une vidéo qui offre une vue d’ensemble de l’architecture MBAM et de la configuration MBAM. Pour plus d’informations, voir [vue d’ensemble de l’architecture et du déploiement MBAM](https://go.microsoft.com/fwlink/p/?LinkId=258392).

## Présentation de l’architecture


Le diagramme suivant illustre l’architecture MBAM. La topologie de déploiement MBAM à serveur unique est proposée pour présenter les fonctionnalités MBAM. Toutefois, cette topologie de déploiement MBAM est recommandée uniquement dans les environnements de laboratoire.

**Remarques**  Au moins une topologie de déploiement MBAM à trois ordinateurs est recommandée pour un déploiement en production. Pour plus d’informations sur les topologies de déploiement MBAM, voir [déploiement de l’infrastructure de serveur 1,0 MBAM](deploying-the-mbam-10-server-infrastructure.md).

 

![topologie de déploiement de serveur unique MBAM](images/mbam-1-server.jpg)

1.  **Serveur d’administration et de surveillance**. Le serveur d’administration et de surveillance MBAM est installé sur un serveur Windows et héberge le site Web d’administration et de gestion MBAM, ainsi que les services Web d’analyse. Le site Web d’administration et de gestion d’MBAM est utilisé pour déterminer l’état de la conformité d’entreprise, pour vérifier l’activité, pour gérer les fonctionnalités matérielles et pour accéder aux données de récupération, telles que les clés de récupération BitLocker. Le serveur d’administration et de surveillance se connecte aux bases de données et services suivants:

    -   Restauration et base de données matérielle. La base de données de récupération et de matériel est installée sur un serveur Windows et sur une instance SQLServer prise en charge. Cette base de données stocke les données de récupération et les informations matérielles collectées à partir des ordinateurs clients MBAM.

    -   Base de données d’audit et de conformité. La base de données d’audit et de conformité est installée sur un serveur Windows et sur une instance SQLServer prise en charge. Cette base de données stocke les données de conformité pour les ordinateurs clients MBAM. Ces données sont principalement utilisées pour les rapports hébergés par SQL Server Reporting Services (SSRS).

    -   Rapports de conformité et d’audit. Les rapports de conformité et d’audit sont installés sur un serveur Windows et une instance SQLServer prise en charge, avec la fonctionnalité SSRS installée. Ces rapports fournissent des rapports d’administration et de surveillance de Microsoft BitLocker. Vous pouvez accéder à ces rapports à partir du site Web d’administration et de gestion de MBAM, ou directement à partir du serveur SSRS.

2.  **Client MBAM**. Le client d’administration et de surveillance de Microsoft BitLocker effectue les tâches suivantes:

    -   Utilise une stratégie de groupe pour appliquer le chiffrement BitLocker d’ordinateurs clients au sein de l’entreprise.

    -   Collecte la clé de récupération pour les trois types de lecteurs de données BitLocker: lecteurs du système d’exploitation, lecteurs de données fixes et lecteurs de données amovibles (USB).

    -   Recueille des informations de récupération et des informations matérielles sur les ordinateurs clients.

    -   Collecte les données de conformité de l’ordinateur et transmet les données au système de création de rapports.

3.  **Modèle de stratégie**. Le modèle de stratégie de groupe MBAM est installé sur un ordinateur client ou serveur Windows pris en charge. Ce modèle permet de spécifier les paramètres d’implémentation de MBAM pour le chiffrement de lecteur BitLocker.

## Rubriques connexes


[Prise en main de MBAM1.0](getting-started-with-mbam-10.md)

 

 





