---
title: Architecture globale de MBAM 2.5 avec la topologie Intégration Configuration Manager
description: Architecture globale de MBAM 2.5 avec la topologie Intégration Configuration Manager
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
ms.openlocfilehash: a0f9349391794100a670e382bb18d0713f4b5b60
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910719"
---
# <a name="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology"></a>Architecture de haut niveau de MBAM 2.5 avec topologie d’intégration Configuration Manager

Cette rubrique décrit l’architecture recommandée pour le déploiement de Microsoft BitLocker Administration and Monitoring (MBAM) avec la topologie d’intégration Configuration Manager. Cette topologie intègre MBAM à System Center Configuration Manager. Pour déployer MBAM avec la topologie autonome, voir Architecture de haut niveau de [MBAM 2.5](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)avec topologie autonome.

Pour obtenir la liste des versions du logiciel pris en charge mentionnées dans cette rubrique, voir CONFIGURATIONS prise en charge [par MBAM 2.5.](mbam-25-supported-configurations.md)

**Important**  
Windows To Go n’est pas pris en charge pour l’installation de la topologie Intégration de Configuration Manager lorsque vous utilisez Configuration Manager 2007.

 

## <a name="recommended-number-of-servers-and-supported-number-of-clients"></a>Nombre recommandé de serveurs et nombre de clients pris en charge


Le nombre recommandé de serveurs et le nombre de clients pris en charge dans un environnement de production sont les suivants :

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
<td align="left"><p>500,000</p></td>
</tr>
</tbody>
</table>

 

## <a name="differences-between-configuration-manager-integration-and-stand-alone-topologies"></a>Différences entre l’intégration de Configuration Manager et les topologies autonomes


Les principales différences entre les topologies sont :

-   Les fonctionnalités de conformité et de rapport sont supprimées de MBAM et sont accessibles à partir de Configuration Manager.

-   Les rapports sont consultés à partir de la console de gestion Configuration Manager, à l’exception du rapport d’audit de récupération, que vous continuez à consulter à partir du site Web d’administration et de surveillance de MBAM.

## <a name="recommended-mbam-high-level-architecture-with-the-configuration-manager-integration-topology"></a>Architecture de haut niveau MBAM recommandée avec la topologie d’intégration Configuration Manager


Le diagramme et le tableau suivants décrivent l’architecture de haut niveau recommandée pour MBAM avec la topologie d’intégration Configuration Manager. Les déploiements MBAM à forêts multiples nécessitent une confiance à sens simple ou double. Les confiances à sens seul nécessitent que le domaine serveur l’truste au domaine client.

![mbam2\-5.](images/mbam2-5-cmserver.png)

### <a name="database-server"></a>Serveur de base de données

#### <a name="recovery-database"></a>Base de données de récupération

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server et prise en charge SQL Server instance.

La base **de données de** récupération stocke les données de récupération collectées à partir des ordinateurs clients MBAM.

#### <a name="audit-database"></a>Base de données d’audit

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server et prise en charge SQL Server instance.

La base **de données d’audit** stocke les données d’activité d’audit collectées sur les ordinateurs clients qui ont accédé aux données de récupération.

#### <a name="reports"></a>Rapports

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server et prise en charge SQL Server instance.

Les **rapports fournissent** des données d’audit de récupération pour les ordinateurs clients de votre entreprise. Vous pouvez afficher les rapports à partir de la console Configuration Manager ou directement à partir SQL Server Reporting Services.

### <a name="configuration-manager-primary-site-server"></a>Serveur de site principal Configuration Manager

System Center Configuration Manager Fonctionnalité d’intégration

-   Cette fonctionnalité est configurée sur le serveur de site principal Configuration Manager, qui est le serveur de niveau supérieur dans votre infrastructure Configuration Manager.

-   Le **serveur Configuration Manager collecte** les informations d’inventaire matériel des ordinateurs clients et est utilisé pour signaler la conformité BitLocker des ordinateurs clients.

-   Lorsque vous exécutez l’Assistant Administration et surveillance de Microsoft BitLocker pour installer le logiciel serveur, la collection Ordinateurs pris en charge par MBAM, la ligne de base de configuration et les rapports sont configurés sur le serveur de site principal Configuration Manager.

-   La **console Configuration Manager doit** être installée sur l’ordinateur sur lequel vous installez le logiciel MBAM Server.

### <a name="administration-and-monitoring-server"></a>Serveur d’administration et de surveillance

#### <a name="administration-and-monitoring-website"></a>Site web d’administration et de surveillance

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.

Le site **Web d’administration et de** surveillance est utilisé pour :

-   Aidez les utilisateurs finaux à reprendre l’accès à leurs ordinateurs lorsqu’ils sont verrouillés. (Cette zone du site Web est communément appelée Help Desk.)

-   Consultez le rapport d’audit de récupération, qui indique l’activité de récupération pour les ordinateurs clients. D’autres rapports sont vus à partir de la console Configuration Manager.

#### <a name="self-service-portal"></a>Portail libre-service

Cette fonctionnalité est configurée sur un ordinateur exécutant Windows Server.

Le **portail libre-service** est un site web qui permet aux utilisateurs finaux sur des ordinateurs clients de se connecter indépendamment à un site web pour obtenir une clé de récupération s’ils perdent ou oublient leur mot de passe BitLocker.

#### <a name="monitoring-web-services-for-this-website"></a>Surveillance des services web pour ce site web

Cette fonctionnalité est installée sur un ordinateur exécutant Windows Server.

Les **services web de surveillance** sont utilisés par le client MBAM et les sites web pour communiquer avec la base de données.

**Important**<br>Le service Web de surveillance n’est plus disponible dans Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1, car les sites web MBAM communiquent directement avec la base de données de récupération. 

 

### <a name="management-workstation"></a>Station de travail de gestion

#### <a name="mbam-group-policy-templates"></a>Modèles de stratégie de groupe MBAM

-   Les **modèles de stratégie** de groupe MBAM sont des paramètres de stratégie de groupe qui définissent les paramètres d’implémentation de MBAM, qui vous permettent de gérer le chiffrement de lecteur BitLocker.

-   Avant d’exécuter MBAM, vous devez télécharger les modèles de stratégie de groupe à partir de la page Comment obtenir des modèles de stratégie de groupe [MDOP (.admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) et les copier sur un serveur ou une station de travail qui exécute un système d’exploitation Windows Server ou Windows pris en charge.

    **REMARQUE**<br>La station de travail n’a pas besoin d’être un ordinateur dédié.

     

### <a name="mbam-client-and-configuration-manager-client-computer"></a>Ordinateur client MBAM et client Configuration Manager

#### <a name="mbam-client-software"></a>Logiciel client MBAM

Le **client MBAM**:

-   Utilise des objets de stratégie de groupe pour appliquer le chiffrement de lecteur BitLocker sur les ordinateurs clients de l’entreprise.

-   Collecte la clé de récupération BitLocker pour trois types de lecteurs de données : lecteurs de système d’exploitation, lecteurs de données fixes et lecteurs de données amovibles (USB).

-   Collecte les informations de récupération et les informations d’ordinateur sur les ordinateurs clients.

#### <a name="configuration-manager-client"></a>Client Configuration Manager

Le **client Configuration Manager permet** à Configuration Manager de collecter des données de compatibilité matérielle sur les ordinateurs clients et de signaler des informations de conformité.

 

## <a name="differences-in-mbam-deployment-for-supported-configuration-manager-versions"></a>Différences dans le déploiement MBAM pour les versions de Configuration Manager prise en charge


Lorsque vous déployez MBAM avec la topologie Intégration de Configuration Manager, vous pouvez installer MBAM sur un serveur de site principal. Toutefois, l’installation de MBAM fonctionne différemment pour System Center 2012 Configuration Manager et Configuration Manager 2007.

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
<td align="left"><p>System Center2012R2 Configuration Manager</p>
<p>System Center2012 Configuration Manager</p></td>
<td align="left"><p>Si vous installez MBAM sur un serveur de site principal ou sur un serveur d’administration centrale, MBAM effectue toutes les actions d’installation sur ce serveur de site.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager 2007 R2</p>
<p>Gestionnaire de configuration 2007</p></td>
<td align="left"><p>Si vous installez MBAM sur un serveur de site principal qui fait partie d’une hiérarchie Configuration Manager plus importante avec un serveur parent de site central, MBAM identifie le serveur parent du site central et effectue toutes les actions d’installation sur ce serveur parent. L’installation inclut la vérification des conditions préalables et l’installation des objets et des rapports Configuration Manager.</p>
<p>Par exemple, si vous installez MBAM sur un serveur de site principal qui est un enfant d’un serveur parent de site central, MBAM installe tous les objets et rapports Configuration Manager sur le serveur parent. Si vous installez MBAM sur le serveur parent, MBAM effectue toutes les actions d’installation sur ce serveur parent.</p></td>
</tr>
</tbody>
</table>

 

## <a name="how-mbam-works-with-configuration-manager"></a>Fonctionnement de MBAM avec Configuration Manager


L’intégration de MBAM avec Configuration Manager est basée sur un pack de configuration qui installe les éléments décrits dans le tableau suivant.

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
<td align="left"><p>Les données de configuration installent une ligne de base de configuration, appelée « BitLocker Protection », qui contient deux éléments de configuration :</p>
<ul>
<li><p>BitLocker Operating System Drive Protection</p></li>
<li><p>Protection des lecteurs de données fixes BitLocker</p></li>
</ul>
<p>La ligne de base de configuration est déployée sur la collection MbaM Supported Computers, qui est également créée lors de l’installation de MBAM.</p>
<p>Les deux éléments de configuration fournissent la base pour évaluer l’état de conformité des ordinateurs clients. Ces informations sont capturées, stockées et évaluées dans Configuration Manager.</p>
<p>Les éléments de configuration sont basés sur les exigences de conformité des lecteurs de système d’exploitation et des lecteurs de données fixes. Les détails requis pour les ordinateurs déployés sont collectés afin que la conformité de ces types de disques puisse être évaluée.</p>
<p>Par défaut, la ligne de base de configuration évalue l’état de conformité toutes les 12 heures et envoie les données de conformité à Configuration Manager.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Collection d’ordinateurs pris en charge par MBAM</p></td>
<td align="left"><p>MBAM crée une collection appelée Ordinateurs pris en charge par MBAM. La ligne de base de configuration est destinée aux ordinateurs clients qui font partie de cette collection.</p>
<p>Il s’agit d’une collection dynamique. Par défaut, il s’exécute toutes les 12 heures et évalue l’appartenance en fonction de trois critères :</p>
<ul>
<li><p>L’ordinateur est une version prise en charge du Windows d’exploitation.</p></li>
<li><p>L’ordinateur est un ordinateur physique. Les machines virtuelles ne sont pas pris en charge.</p></li>
<li><p>L’ordinateur dispose d’un module de plateforme fiable (TPM) qui est disponible. Une version compatible du TPM 1.2 ou version ultérieure est requise pour Windows 7. Windows 10, Windows8.1, Windows 8 et Windows To Go ne nécessitent pas de TPM.</p></li>
</ul>
<p>La collection est évaluée par rapport à tous les ordinateurs et un sous-ensemble d’ordinateurs compatibles est créé, ce qui fournit la base pour l’évaluation de la conformité et la création de rapports pour l’intégration MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Rapports</p></td>
<td align="left"><p>Lorsque vous configurez MBAM avec la topologie d’intégration Configuration Manager, vous affichez tous les rapports dans Configuration Manager, à l’exception du rapport d’audit de récupération, que vous continuez à consulter dans le site Web d’administration et de surveillance de MBAM. Les rapports disponibles dans Configuration Manager sont :</p>
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
<td align="left"><p>BitLocker Entreprise Tableau de bord de conformité</p></td>
<td align="left"><p>Donne aux administrateurs informatiques trois vues d’informations dans un seul rapport : Distribution de l’état de conformité, Non conforme – Distribution des erreurs et Distribution de l’état de conformité par type de lecteur. Les options d’analyse du rapport vous permet aux administrateurs informatiques de cliquer sur les données et d’afficher la liste des ordinateurs qui correspondent à l’état sélectionné.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker Entreprise Détails de conformité</p></td>
<td align="left"><p>Permet aux administrateurs informatiques d’afficher des informations sur l’état de conformité de chiffrement BitLocker de l’entreprise et inclut l’état de conformité pour chaque ordinateur. Les options d’analyse du rapport vous permet aux administrateurs informatiques de cliquer sur les données et d’afficher la liste des ordinateurs qui correspondent à l’état sélectionné.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformité de l’ordinateur BitLocker</p></td>
<td align="left"><p>Permet aux administrateurs informatiques d’afficher un ordinateur individuel et de déterminer pourquoi il a été signalé avec un état conforme ou non conforme. Le rapport affiche également l’état de chiffrement des lecteurs de système d’exploitation et des lecteurs de données fixes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker Entreprise Résumé de la conformité</p></td>
<td align="left"><p>Permet aux administrateurs informatiques d’afficher l’état de conformité des stratégies MBAM dans l’entreprise. L’état de chaque ordinateur est évalué et le rapport affiche un résumé de la conformité de tous les ordinateurs de l’entreprise par rapport à la stratégie. Les options d’analyse du rapport vous permet aux administrateurs informatiques de cliquer sur les données et d’afficher la liste des ordinateurs qui correspondent à l’état sélectionné.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## <a name="related-topics"></a>Rubriques associées


[Prise en main de MBAM 2.5](getting-started-with-mbam-25.md)

[Architecture globale de MBAM 2.5 avec la topologie autonome](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[Illustration des composants d'un déploiement de MBAM 2.5](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## <a name="got-a-suggestion-for-mbam"></a>Vous avez une suggestion pour MBAM ?
- Ajoutez ou votez sur les suggestions [ici.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes de MBAM, utilisez le [forum TechNet MBAM.](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam)




