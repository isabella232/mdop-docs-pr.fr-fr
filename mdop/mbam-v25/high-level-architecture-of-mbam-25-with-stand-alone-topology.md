---
title: Architecture globale de MBAM2.5 avec la topologie autonome
description: Architecture globale de MBAM2.5 avec la topologie autonome
author: dansimp
ms.assetid: 35f8c5f6-8be3-443d-baf0-56d68b08f3bc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 75e878e24b4675f2f2f574791d0f06ecadd0196d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811826"
---
# Architecture globale de MBAM2.5 avec la topologie autonome


Cette rubrique décrit l’architecture recommandée pour le déploiement de Microsoft BitLocker administration et de la surveillance (MBAM) avec la topologie autonome de Configuration Manager. Dans cette topologie, MBAM est déployé en tant que produit autonome. Vous pouvez également déployer MBAM avec la topologie d’intégration de Configuration Manager, qui intègre MBAM avec Configuration Manager. Pour plus d’informations, reportez-vous à la rubrique [architecture de niveau supérieur de MBAM 2,5 avec la topologie d’intégration de Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).

Pour obtenir la liste des versions prises en charge pour les logiciels mentionnés dans cette rubrique, voir [Configurations prises en charge par MBAM 2,5](mbam-25-supported-configurations.md).

**Remarques**  Nous vous recommandons d’utiliser une architecture serveur unique uniquement dans les environnements de test.

 

## Nombre de serveurs recommandés et nombre de clients pris en charge


Le nombre de serveurs recommandés et le nombre de clients pris en charge dans un environnement de production sont les suivants:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Architecture recommandée dans un environnement de production</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nombre de serveurs et autres ordinateurs</p></td>
<td align="left"><p>Deux serveurs</p>
<p>Une station de travail</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre d’ordinateurs clients pris en charge</p></td>
<td align="left"><p>500 000</p></td>
</tr>
</tbody>
</table>

 

## Architecture de niveau supérieur MBAM recommandée avec la topologie autonome


Le schéma et le tableau ci-dessous décrivent l’architecture de serveur à double niveau recommandée pour MBAM avec la topologie autonome. Les déploiements de forêts multiples MBAM requièrent une approbation à sens unique ou à double sens. Les approbations à sens unique requièrent que le domaine du serveur approuve le domaine client.

![mbam2](images/mbam2-5-2servers.png)

Fonctionnalités serveur à configurer sur le serveur de base de données de description du serveur

Base de données d’audit et de conformité

Cette fonctionnalité est configurée sur un serveur exécutant Windows Server et l’instance SQL Server prise en charge.

La **base de données d’audit et de conformité** stocke les données de conformité, qui est principalement utilisée pour les rapports hébergés par SQL Server Reporting Services.

Base de données de récupération

Cette fonctionnalité est configurée sur un serveur exécutant Windows Server et l’instance SQL Server prise en charge.

La **base de données de récupération** stocke les données de récupération collectées à partir des ordinateurs clients MBAM.

Rapports

Cette fonctionnalité est configurée sur un serveur exécutant Windows Server et l’instance SQL Server prise en charge.

Les **rapports** fournissent des données d’audit de récupération et de conformité sur les ordinateurs clients de votre entreprise. Vous pouvez accéder aux rapports à partir du site Web d’administration et de surveillance ou directement à partir de SQL Server Reporting Services.

Serveur d’administration et de surveillance

Site Web d’administration et de surveillance

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.

Le **site Web d’administration et de surveillance** permet d’effectuer les opérations suivantes:

-   Aidez les utilisateurs finaux à pouvoir accéder à leur ordinateur lorsqu’ils sont bloqués. (Cette zone du site Web est souvent appelée support technique.)

-   Affichez des rapports qui présentent l’état de conformité et l’activité de récupération pour les ordinateurs clients.

Portail libre-service

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.

Le **portail libre-service** est un site Web qui permet aux utilisateurs finaux sur les ordinateurs clients de se connecter de manière indépendante à un site Web pour obtenir une clé de récupération en cas de perte ou d’oubli du mot de passe BitLocker.

Surveiller les services Web pour ce site Web

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.

Les **services Web de surveillance** sont utilisés par le client MBAM et les sites Web pour communiquer avec la base de données.

**Important**  Le service Web de surveillance n’est plus disponible dans les services d’administration et de surveillance de BitLocker (MBAM) 2,5 SP1 puisque les sites Web MBAM communiquent directement avec la base de données de récupération.

 

Station de travail de gestion

Modèles de stratégie de groupe MBAM

-   Les modèles de stratégie de groupe MBAM sont des paramètres de stratégie de groupe définissant les paramètres d’implémentation de MBAM, qui vous permettent de gérer le chiffrement de lecteur BitLocker.

-   Avant d’exécuter MBAM, vous devez télécharger les modèles de stratégie de groupe pour [obtenir les modèles de stratégie de groupe MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) et les copier sur un serveur ou une station de travail exécutant un système d’exploitation Windows Server ou Windows pris en charge.

-   La station de travail ne doit pas nécessairement être un ordinateur dédié.

Client MBAM et ordinateur client Configuration Manager

Logiciel client MBAM

Le client MBAM:

-   Utilise des objets de stratégie de groupe pour appliquer le chiffrement de lecteur BitLocker sur les ordinateurs clients au sein de l’entreprise.

-   Collecte la clé de récupération BitLocker pour trois types de lecteurs de données: les lecteurs du système d’exploitation, les lecteurs de données fixes et les lecteurs de données USB.

-   Recueille des informations de récupération et des informations informatiques sur les ordinateurs clients.



## Rubriques connexes


[Prise en main de MBAM2.5](getting-started-with-mbam-25.md)

[Architecture globale de MBAM2.5 avec la topologie Intégration Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[Illustration des composants d'un déploiement de MBAM2.5](illustrated-features-of-an-mbam-25-deployment.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





