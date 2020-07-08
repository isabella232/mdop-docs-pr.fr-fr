---
title: Architecture globale de MBAM2.5 avec la topologie Intégration Configuration Manager
description: Architecture globale de MBAM2.5 avec la topologie Intégration Configuration Manager
author: dansimp
ms.assetid: 075bafa1-792b-4c24-9d8e-5d3153e2112c
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/23/2018
ms.author: dansimp
ms.openlocfilehash: 75af2e22981d76568916c36acadbbb25648b1f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811351"
---
# Architecture de haut niveau de MBAM 2,5 avec topologie d’intégration de Configuration Manager

Cette rubrique décrit l’architecture recommandée pour le déploiement de Microsoft BitLocker administration et de la surveillance (MBAM) avec la topologie d’intégration de Configuration Manager. Cette topologie intègre MBAM à System Center Configuration Manager. Pour déployer MBAM avec la topologie autonome, voir [architecture de niveau supérieur d’MBAM 2,5 avec topologie](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)autonome.

Pour obtenir la liste des versions prises en charge pour les logiciels mentionnés dans cette rubrique, voir [Configurations prises en charge par MBAM 2,5](mbam-25-supported-configurations.md).

**Important**  Windows to Go n’est pas pris en charge pour l’installation de la topologie d’intégration de Configuration Manager lorsque vous utilisez Configuration Manager 2007.

 

## Nombre de serveurs recommandés et nombre de clients pris en charge


Le nombre de serveurs recommandés et le nombre de clients pris en charge dans un environnement de production sont les suivants:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Architecture recommandée</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nombre de serveurs et autres ordinateurs</p></td>
<td align="left"><p>Trois serveurs</p>
<p>Une station de travail</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nombre d’ordinateurs clients pris en charge</p></td>
<td align="left"><p>500 000</p></td>
</tr>
</tbody>
</table>

 

## Différences entre l’intégration de Configuration Manager et les topologies autonomes


Les principales différences entre les topologies sont les suivantes:

-   Les fonctionnalités de conformité et de création de rapports sont supprimées de MBAM et sont accessibles à partir de Configuration Manager.

-   Les rapports sont consultés à partir de la console de gestion Configuration Manager, à l’exception du rapport d’audit de récupération, que vous continuez à consulter à partir du site Web d’administration et de surveillance de MBAM.

## Architecture de niveau supérieur MBAM recommandée avec la topologie d’intégration de Configuration Manager


Le schéma et le tableau suivants décrivent l’architecture de haut niveau recommandée pour MBAM avec la topologie d’intégration de Configuration Manager. Les déploiements de forêts multiples MBAM requièrent une approbation à sens unique ou à double sens. Les approbations à sens unique requièrent que le domaine du serveur approuve le domaine client.

![mbam2\-5](images/mbam2-5-cmserver.png)

### Serveur de base de données

#### Base de données de récupération

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server et l’instance SQL Server prise en charge.

La **base de données de récupération** stocke les données de récupération collectées à partir des ordinateurs clients MBAM.

#### Base de données d’audit

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server et l’instance SQL Server prise en charge.

La **base de données d’audit** stocke les données d’activité d’audit collectées sur les ordinateurs clients ayant accédé aux données de récupération.

#### Rapports

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server et l’instance SQL Server prise en charge.

Les **rapports** fournissent des données d’audit de récupération pour les ordinateurs clients de votre entreprise. Vous pouvez afficher des rapports à partir de la console Configuration Manager ou directement à partir de SQL Server Reporting Services.

### Serveur de site principal de Configuration Manager

Fonctionnalité d’intégration de System Center Configuration Manager

-   Cette fonctionnalité est configurée sur le serveur de site principal de Configuration Manager, qui est le serveur de niveau supérieur de votre infrastructure de Configuration Manager.

-   Le **serveur Configuration Manager** collecte les informations d’inventaire matériel sur les ordinateurs clients et permet de signaler la compatibilité de BitLocker sur les ordinateurs clients.

-   Lorsque vous exécutez l’Assistant Configuration de l’administration et de la surveillance de BitLocker pour installer le logiciel de serveur, la collection d’ordinateurs pris en charge par MBAM, la planification de la configuration et les rapports sont configurées sur le serveur de site principal de Configuration Manager.

-   La **console Configuration Manager** doit être installée sur l’ordinateur sur lequel vous installez le logiciel serveur MBAM.

### Serveur d’administration et de surveillance

#### Site Web d’administration et de surveillance

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.

Le **site Web d’administration et de surveillance** permet d’effectuer les opérations suivantes:

-   Aidez les utilisateurs finaux à pouvoir accéder à leur ordinateur lorsqu’ils sont bloqués. (Cette zone du site Web est souvent appelée support technique.)

-   Affichez le rapport d’audit de récupération, qui indique l’activité de récupération pour les ordinateurs clients. D’autres rapports sont affichés dans la console Configuration Manager.

#### Portail libre-service

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.

Le **portail libre-service** est un site Web qui permet aux utilisateurs finaux sur les ordinateurs clients de se connecter de manière indépendante à un site Web pour obtenir une clé de récupération en cas de perte ou d’oubli du mot de passe BitLocker.

#### Surveiller les services Web pour ce site Web

Cette fonctionnalité est installée sur un ordinateur exécutant Windows Server.

Les **services Web de surveillance** sont utilisés par le client MBAM et les sites Web pour communiquer avec la base de données.

**Important**<br>Le service Web de surveillance n’est plus disponible dans les services d’administration et de surveillance de BitLocker (MBAM) 2,5 SP1 puisque les sites Web MBAM communiquent directement avec la base de données de récupération. 

 

### Station de travail de gestion

#### Modèles de stratégie de groupe MBAM

-   Les **modèles de stratégie de groupe MBAM** sont des paramètres de stratégie de groupe définissant les paramètres d’implémentation de MBAM, qui vous permettent de gérer le chiffrement de lecteur BitLocker.

-   Avant d’exécuter MBAM, vous devez télécharger les modèles de stratégie de groupe pour [obtenir les modèles de stratégie de groupe MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) et les copier sur un serveur ou une station de travail exécutant un système d’exploitation Windows Server ou Windows pris en charge.

    **REMARQUE**<br>La station de travail ne doit pas nécessairement être un ordinateur dédié.

     

### Client MBAM et ordinateur client Configuration Manager

#### Logiciel client MBAM

Le **client MBAM**:

-   Utilise des objets de stratégie de groupe pour appliquer le chiffrement de lecteur BitLocker sur les ordinateurs clients au sein de l’entreprise.

-   Collecte la clé de récupération BitLocker pour trois types de lecteurs de données: les lecteurs du système d’exploitation, les lecteurs de données fixes et les lecteurs de données USB.

-   Recueille des informations de récupération et des informations informatiques sur les ordinateurs clients.

#### Client Configuration Manager

Le **client Configuration Manager** permet à Configuration Manager de recueillir des données de compatibilité matérielle sur les ordinateurs clients et de signaler les informations de conformité.

 

## Différences du déploiement d’MBAM pour les versions prises en charge du gestionnaire de configurations


Lorsque vous déployez MBAM avec la topologie d’intégration de Configuration Manager, vous pouvez installer MBAM sur un serveur de site principal. Toutefois, l’installation d’MBAM fonctionne différemment pour le gestionnaire de configuration de Center2012 système et de configuration Manager2007.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version de Configuration Manager</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>System Center2012 R2 Configuration Manager</p>
<p>Gestionnaire de configuration système Center2012</p></td>
<td align="left"><p>Si vous installez MBAM sur un serveur de site principal ou un serveur d’administration centrale, MBAM effectue toutes les actions d’installation sur ce serveur de site.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager2007 R2</p>
<p>Configuration Manager2007</p></td>
<td align="left"><p>Si vous installez MBAM sur un serveur de site principal qui fait partie d’une hiérarchie de gestionnaires de configuration plus importante avec un serveur parent de site central, MBAM identifie le serveur parent du site central et effectue toutes les actions d’installation sur ce serveur parent. L’installation inclut la vérification préalable et l’installation des objets et des rapports de Configuration Manager.</p>
<p>Par exemple, si vous installez MBAM sur un serveur de site principal qui est un enfant d’un serveur parent de site central, MBAM installe tous les objets et rapports de configuration du serveur parent. Si vous installez MBAM sur le serveur parent, MBAM effectue toutes les actions d’installation sur ce serveur parent.</p></td>
</tr>
</tbody>
</table>

 

## Fonctionnement de MBAM avec Configuration Manager


L’intégration de MBAM avec Configuration Manager est basée sur un module de configuration qui installe les éléments décrits dans le tableau ci-dessous.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Éléments installés dans Configuration Manager</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Données de configuration</p></td>
<td align="left"><p>Les données de configuration installent un planning de référence, appelé «protection BitLocker», qui contient deux éléments de configuration:</p>
<ul>
<li><p>Protection des lecteurs du système d’exploitation BitLocker</p></li>
<li><p>Protection des lecteurs de données fixes BitLocker</p></li>
</ul>
<p>Le planning de référence de configuration est déployé sur la collection d’ordinateurs pris en charge par MBAM, qui est également créée lors de l’installation d’MBAM.</p>
<p>Les deux éléments de configuration fournissent la base pour évaluer l’état de conformité des ordinateurs clients. Ces informations sont capturées, stockées et évaluées dans Configuration Manager.</p>
<p>Les éléments de configuration sont basés sur les exigences en matière de conformité pour les lecteurs du système d’exploitation et les lecteurs de données fixes. Les informations requises pour les ordinateurs déployés sont collectées afin de permettre d’évaluer la conformité de ces types de lecteurs.</p>
<p>Par défaut, la ligne de base de configuration évalue l’état de conformité every12 heures et envoie les données de conformité à Configuration Manager.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Collection d’ordinateurs pris en charge par MBAM</p></td>
<td align="left"><p>MBAM crée une collection appelée MBAM d’ordinateurs pris en charge. Le planning de référence de la configuration est ciblé vers les ordinateurs clients qui se trouvent dans cette collection.</p>
<p>Il s’agit d’une collection dynamique. Par défaut, il exécute every12 heures et évalue l’appartenance, en fonction de trois critères:</p>
<ul>
<li><p>L’ordinateur est une version prise en charge du système d’exploitation Windows.</p></li>
<li><p>Il s’agit d’un ordinateur physique. Les machines virtuelles ne sont pas prises en charge.</p></li>
<li><p>Le module de plateforme sécurisée (TPM) de l’ordinateur est disponible. Une version compatible de TPM 1.2 ou version ultérieure est requise pour le son. Windows 10, Windows 8.1, Windows8 et Windows to Go ne requièrent aucun module de plateforme sécurisée.</p></li>
</ul>
<p>La collection est évaluée par rapport à tous les ordinateurs et un sous-ensemble d’ordinateurs compatibles est créé, qui sert de base à l’évaluation de la conformité et au rapport de l’intégration d’MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Rapports</p></td>
<td align="left"><p>Lorsque vous configurez MBAM à l’aide de la topologie d’intégration de Configuration Manager, vous pouvez afficher tous les rapports dans Configuration Manager, à l’exception du rapport d’audit de récupération, dont vous continuez à afficher le site Web d’administration et de surveillance MBAM. Les rapports disponibles dans Configuration Manager sont les suivants:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Rapport</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tableau de bord de conformité de BitLocker Enterprise</p></td>
<td align="left"><p>Fournit aux administrateurs informatiques trois affichages d’informations dans un seul rapport: distribution de l’état de conformité, distribution des erreurs non conforme-distribution et état de conformité par type de lecteur. Les options d’exploration du rapport permettent aux administrateurs d’effectuer un clic sur les données et d’afficher la liste des ordinateurs qui correspondent à l’état sélectionné.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Détails de la conformité à l’entreprise BitLocker</p></td>
<td align="left"><p>Permet aux administrateurs informatiques d’afficher des informations sur l’état de conformité du chiffrement BitLocker de l’entreprise et inclut l’état de conformité de chaque ordinateur. Les options d’exploration du rapport permettent aux administrateurs d’effectuer un clic sur les données et d’afficher la liste des ordinateurs qui correspondent à l’état sélectionné.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Compatibilité de l’ordinateur BitLocker</p></td>
<td align="left"><p>Permet aux administrateurs informatiques d’afficher un ordinateur individuel et de déterminer pourquoi il a été signalé avec un statut de conforme ou non conforme. Le rapport affiche également l’état de chiffrement des lecteurs du système d’exploitation et des lecteurs de données fixes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Résumé de conformité de BitLocker Enterprise</p></td>
<td align="left"><p>Permet aux administrateurs informatiques d’afficher l’état de la conformité de la stratégie MBAM au sein de l’entreprise. L’état de chaque ordinateur est évalué, et le rapport affiche un résumé de la conformité de tous les ordinateurs de l’entreprise par rapport à la stratégie. Les options d’exploration du rapport permettent aux administrateurs d’effectuer un clic sur les données et d’afficher la liste des ordinateurs qui correspondent à l’état sélectionné.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## Rubriques connexes


[Prise en main de MBAM2.5](getting-started-with-mbam-25.md)

[Architecture globale de MBAM2.5 avec la topologie autonome](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[Illustration des composants d'un déploiement de MBAM2.5](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




