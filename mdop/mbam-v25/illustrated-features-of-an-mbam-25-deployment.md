---
title: Illustration des composants d'un déploiement de MBAM2.5
description: Illustration des composants d'un déploiement de MBAM2.5
author: dansimp
ms.assetid: 7b5eff42-af8c-4bd0-a20a-18cc2e779f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: c3b205d4f0b4b18cf8bdbf51982b5a59e5e1b9d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804195"
---
# Illustration des composants d'un déploiement de MBAM2.5


Cette rubrique décrit les fonctionnalités individuelles qui font l’objet d’un déploiement 2,5 de Microsoft BitLocker (MBAM) pour les topologies suivantes:

-   MBAM autonome

-   Intégration de System Center Configuration Manager

**Important**  
Ces fonctionnalités ne représentent pas l’architecture recommandée pour le déploiement de MBAM. Utilisez ces informations uniquement comme guide pour comprendre les fonctionnalités individuelles qui constituent un déploiement MBAM. Voir [architecture de haut niveau pour MBAM 2,5](high-level-architecture-for-mbam-25.md) pour l’architecture recommandée de MBAM.



Pour obtenir la liste des versions prises en charge pour les logiciels mentionnés dans cette rubrique, voir [Configurations prises en charge par MBAM 2,5](mbam-25-supported-configurations.md).

## <a href="" id="bkmk-standalone"></a> Topologie autonome MBAM


L’image et le tableau suivants décrivent les fonctionnalités d’une topologie autonome MBAM.

![mbab2\-5](images/mbam2-5-standalonecomponents.png)

|Type de fonctionnalité|Description|Base de données|
|-|-|-|
|Base de données de récupération|Cette base de données stocke les données de récupération collectées à partir des ordinateurs clients MBAM.|Cette fonctionnalité est configurée sur un serveur exécutant Windows Server et une instance SQL Server prise en charge.|
|Base de données d’audit et de conformité|Cette base de données stocke les données de conformité, qui est essentiellement utilisée pour les rapports hébergés par SQL Server Reporting Services.|Cette fonctionnalité est configurée sur un serveur exécutant Windows Server et une instance SQL Server prise en charge.|
|Rapports de conformité et d’audit|||
|Service Web de création de rapports|Ce service Web permet une communication entre le site Web d’administration et de contrôle, ainsi que l’instance SQL Server où sont stockées les données de création de rapports.|Cette fonctionnalité est installée sur un serveur exécutant Windows Server.|
|Site Web de création de rapports (site Web d’administration et de surveillance)|Vous pouvez afficher les rapports à partir du site Web Administration et analyse. Les rapports fournissent des données d’audit de récupération et de conformité sur les ordinateurs clients de votre entreprise.|Cette fonctionnalité est configurée sur un serveur exécutant Windows Server.|
|SQL Server Reporting Services (SSRS)|Les rapports sont configurés dans une instance de base de données SSRS. Les rapports peuvent être consultés directement à partir de SSRS ou du site Web d’administration et de surveillance.|Cette fonctionnalité est configurée sur un serveur exécutant Windows Server et une instance SQL Server prise en charge exécutant SSRS.|
|Serveur libre-service|||
|Service Web libre-service|Ce service Web est utilisé par le client MBAM et le site Web d’administration et de surveillance et le portail libre-service pour communiquer avec la base de données de récupération.|Cette fonctionnalité est installée sur un ordinateur exécutant Windows Server.|
|Site Web libre-service (portail libre-service)|Ce site Web permet aux utilisateurs finaux sur les ordinateurs clients de se connecter de manière indépendante à un site Web pour obtenir une clé de récupération en cas de perte ou d’oubli du mot de passe BitLocker.|Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.|
|Serveur d’administration et de surveillance|||
|Service Web d’administration et de surveillance|Le service Web de surveillance est utilisé par le client MBAM et les sites Web pour communiquer avec les bases de données.|Cette fonctionnalité est installée sur un ordinateur exécutant Windows Server.|

**Important**  
Le service Web libre-service n’est plus disponible dans Microsoft BitLocker administration et surveillance (MBAM) 2,5 SP1, dans lequel le client MBAM, le site Web d’administration et de surveillance, et le portail libre-service communiquent directement avec la base de données de récupération.

**Important**  
Le service Web de surveillance n’est plus disponible dans Microsoft BitLocker administration et surveillance (MBAM) 2,5 SP1, car le client MBAM et les sites Web communiquent directement avec la base de données de récupération.


## <a href="" id="bkmk-cmintegrated"></a>Topologie d’intégration de System Center Configuration Manager

L’image et le tableau suivants décrivent les fonctionnalités de la topologie d’intégration de System Center Configuration Manager.

![mbam2\-5](images/mbam2-5-cmcomponents.png)

**Important**  
Le service Web libre-service n’est plus disponible dans Microsoft BitLocker administration et surveillance (MBAM) 2,5 SP1, dans lequel le client MBAM, le site Web d’administration et de surveillance, et le portail libre-service communiquent directement avec la base de données de récupération.

**Warning**  
Le service Web de surveillance n’est plus disponible dans Microsoft BitLocker administration et surveillance (MBAM) 2,5 SP1, car le client MBAM et les sites Web communiquent directement avec la base de données de récupération.


|                        Type de fonctionnalité                        |                                                                                                    Description                                                                                                    |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                    Serveur libre-service                     |                                                                                                                                                                                                                   |
|                  Service Web libre-service                  |                                                 Ce service Web est utilisé par le client MBAM et le portail libre-service pour communiquer avec la base de données de récupération.                                                  |
|                    Site Web libre-service                    |                          Ce site Web permet aux utilisateurs finaux sur les ordinateurs clients de se connecter de manière indépendante à un site Web pour obtenir une clé de récupération en cas de perte ou d’oubli du mot de passe BitLocker.                          |
| Rapports d’administration et de surveillance du serveur/analyse de récupération |                                                                                                                                                                                                                   |
|         Service Web d’administration et de surveillance          |                               Ce service Web permet une communication entre le site Web d’administration et de contrôle, ainsi que les bases de données SQL Server où sont stockées les données de création de rapports.                               |
|           Site Web d’administration et de surveillance            | Le rapport d’audit de récupération est affiché à partir du site Web d’administration et de surveillance. Utilisez la console Configuration Manager pour afficher tous les autres rapports, ou afficher les rapports directement à partir de SQL Server Reporting Services. |
|                         Bases de données                          |                                                                                                                                                                                                                   |
|                     Base de données de récupération                      |                                                                 Cette base de données stocke les données de récupération collectées à partir des ordinateurs clients MBAM.                                                                  |
|                       Base de données d’audit                       |                                                                   Cette base de données enregistre les informations d’audit relatives aux tentatives de récupération et à l’activité.                                                                    |
|               Fonctionnalités du gestionnaire de configuration               |                                                                                                                                                                                                                   |
|          Console de gestion Configuration Manager          |                                                                   Cette console est intégrée à Configuration Manager et permet d’afficher des rapports.                                                                   |
|               Rapports du gestionnaire de configuration                |                                                             Les rapports indiquent les données d’audit de conformité et de récupération pour les ordinateurs clients de votre entreprise.                                                              |
|               SQL Server Reporting Services                |                                                SSRS active les rapports MBAM. Les rapports peuvent être affichés directement depuis SSRS ou à partir de la console Configuration Manager.                                                 |

## Rubriques connexes

[Architecture de hautniveau pour MBAM2.5](high-level-architecture-for-mbam-25.md)

[Prise en main de MBAM2.5](getting-started-with-mbam-25.md)

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




