---
title: Illustration des composants d'un déploiement de MBAM 2.5
description: Illustration des composants d'un déploiement de MBAM 2.5
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
ms.openlocfilehash: 139980fb6712b40685a41bab45610da670803afa
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910619"
---
# <a name="illustrated-features-of-an-mbam-25-deployment"></a>Illustration des composants d'un déploiement de MBAM 2.5


Cette rubrique décrit les fonctionnalités individuelles qui sont à l’origine du déploiement de Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 pour les topologies suivantes :

-   MBAM autonome

-   System Center Configuration Manager Intégration

**Important**  
Ces fonctionnalités ne représentent pas l’architecture recommandée pour le déploiement de MBAM. Utilisez ces informations uniquement comme guide pour comprendre les fonctionnalités individuelles qui sont à l’origine d’un déploiement MBAM. Voir [Architecture de haut niveau pour MBAM 2.5](high-level-architecture-for-mbam-25.md) pour l’architecture recommandée pour MBAM.



Pour obtenir la liste des versions du logiciel pris en charge mentionnées dans cette rubrique, voir CONFIGURATIONS prise en charge [par MBAM 2.5.](mbam-25-supported-configurations.md)

## <a name="mbam-stand-alone-topology"></a><a href="" id="bkmk-standalone"></a> Topologie mbam autonome


L’image et le tableau suivants expliquent les fonctionnalités d’une topologie autonome MBAM.

![mbab2\-5.](images/mbam2-5-standalonecomponents.png)

|Type de fonctionnalité|Description|Base de données|
|-|-|-|
|Base de données de récupération|Cette base de données stocke les données de récupération collectées à partir des ordinateurs clients MBAM.|Cette fonctionnalité est configurée sur un serveur exécutant Windows Server et une instance SQL Server prise en charge.|
|Base de données de conformité et d’audit|Cette base de données stocke les données de conformité, qui sont principalement utilisées pour les rapports SQL Server Reporting Services hôtes.|Cette fonctionnalité est configurée sur un serveur exécutant Windows Server et une instance SQL Server prise en charge.|
|Rapports de conformité et d’audit|||
|Service Web de rapports|Ce service web permet la communication entre le site Web d’administration et de surveillance et l’instance SQL Server où les données de rapport sont stockées.|Cette fonctionnalité est installée sur un serveur exécutant Windows Server.|
|Site web de rapports (site web d’administration et de surveillance)|Vous pouvez afficher les rapports à partir du site Web d’administration et de surveillance. Les rapports fournissent des données d’état d’audit et de conformité de récupération sur les ordinateurs clients de votre entreprise.|Cette fonctionnalité est configurée sur un serveur exécutant Windows Server.|
|SQL Server Reporting Services (SSRS)|Les rapports sont configurés dans une instance de base de données SSRS. Les rapports peuvent être consultés directement à partir du SSRS ou du site Web d’administration et de surveillance.|Cette fonctionnalité est configurée sur un serveur exécutant Windows Server et une instance SQL Server prise en charge qui exécute SSRS.|
|Self-Service Server|||
|Self-Service Web Service|Ce service web est utilisé par le client MBAM, le site web d’administration et de surveillance et le portail Self-Service pour communiquer avec la base de données de récupération.|Cette fonctionnalité est installée sur un ordinateur exécutant Windows Server.|
|Self-Service Web (portail libre-service)|Ce site web permet aux utilisateurs finaux sur les ordinateurs clients de se connectent indépendamment à un site web pour obtenir une clé de récupération s’ils perdent ou oublient leur mot de passe BitLocker.|Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.|
|Serveur d’administration et de surveillance|||
|Service Web d’administration et de surveillance|Le service Web de surveillance est utilisé par le client MBAM et les sites web pour communiquer avec les bases de données.|Cette fonctionnalité est installée sur un ordinateur exécutant Windows Server.|

**Important**  
Le service Web Self-Service n’est plus disponible dans Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1, dans lequel le client MBAM, le site web d’administration et de surveillance et le portail Self-Service communiquent directement avec la base de données de récupération.

**Important**  
Le service Web de surveillance n’est plus disponible dans Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1, car le client MBAM et les sites web communiquent directement avec la base de données de récupération.


## <a name="system-center-configuration-manager-integration-topology"></a><a href="" id="bkmk-cmintegrated"></a>System Center Configuration Manager Topologie d’intégration

L’image et le tableau suivants expliquent les fonctionnalités de la topologie System Center Configuration Manager’intégration.

![mbam2\-5.](images/mbam2-5-cmcomponents.png)

**Important**  
Le service Web Self-Service n’est plus disponible dans Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1, dans lequel le client MBAM, le site web d’administration et de surveillance et le portail Self-Service communiquent directement avec la base de données de récupération.

**Warning**  
Le service Web de surveillance n’est plus disponible dans Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1, car le client MBAM et les sites web communiquent directement avec la base de données de récupération.


|                        Type de fonctionnalité                        |                                                                                                    Description                                                                                                    |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                    Self-Service Server                     |                                                                                                                                                                                                                   |
|                  Self-Service Web Service                  |                                                 Ce service web est utilisé par le client MBAM et le portail Self-Service pour communiquer avec la base de données de récupération.                                                  |
|                    Self-Service Web                    |                          Ce site web permet aux utilisateurs finaux sur les ordinateurs clients de se connectent indépendamment à un site web pour obtenir une clé de récupération s’ils perdent ou oublient leur mot de passe BitLocker.                          |
| Rapport d’audit d’administration et de surveillance/récupération |                                                                                                                                                                                                                   |
|         Service Web d’administration et de surveillance          |                               Ce service web permet la communication entre le site Web d’administration et de surveillance et les bases de données SQL Server où les données de rapport sont stockées.                               |
|           Site web d’administration et de surveillance            | Le rapport d’audit de récupération est consulté à partir du site Web d’administration et de surveillance. Utilisez la console Configuration Manager pour afficher tous les autres rapports ou afficher les rapports directement à partir SQL Server Reporting Services. |
|                         Bases de données                          |                                                                                                                                                                                                                   |
|                     Base de données de récupération                      |                                                                 Cette base de données stocke les données de récupération collectées à partir des ordinateurs clients MBAM.                                                                  |
|                       Base de données d’audit                       |                                                                   Cette base de données stocke des informations d’audit sur les tentatives de récupération et l’activité.                                                                    |
|               Fonctionnalités de Configuration Manager               |                                                                                                                                                                                                                   |
|          Console de gestion Configuration Manager          |                                                                   Cette console est intégrée à Configuration Manager et permet d’afficher des rapports.                                                                   |
|               Rapports Configuration Manager                |                                                             Les rapports indiquent les données d’audit de conformité et de récupération pour les ordinateurs clients de votre entreprise.                                                              |
|               SQL Server Reporting Services                |                                                SSRS active les rapports MBAM. Les rapports peuvent être vus directement à partir de SSRS ou de la console Configuration Manager.                                                 |

## <a name="related-topics"></a>Rubriques associées

[Architecture de haut niveau pour MBAM 2.5](high-level-architecture-for-mbam-25.md)

[Prise en main de MBAM 2.5](getting-started-with-mbam-25.md)

## <a name="got-a-suggestion-for-mbam"></a>Vous avez une suggestion pour MBAM ?
- Ajoutez ou votez sur les suggestions [ici.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes de MBAM, utilisez le [forum TechNet MBAM.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)




