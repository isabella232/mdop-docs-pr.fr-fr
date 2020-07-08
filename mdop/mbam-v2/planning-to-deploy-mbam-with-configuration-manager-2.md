---
title: Planification du déploiement de MBAM avec Configuration Manager
description: Planification du déploiement de MBAM avec Configuration Manager
author: dansimp
ms.assetid: fb768306-48c2-40b4-ac4e-c279db987391
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e8588ce03c86a8a5138d591327e5f95503dce5ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811268"
---
# Planification du déploiement de MBAM avec Configuration Manager


Pour déployer MBAM avec la topologie Configuration Manager, il est recommandé d’utiliser une architecture à trois serveurs qui prend en charge les clients 200 000. Utilisez un serveur distinct pour exécuter Configuration Manager, puis installez les fonctionnalités d’administration et de surveillance de base sur deux serveurs, comme indiqué dans l’image d’architecture de la rubrique [mise en route de l’utilisation de MBAM avec Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).

**Important**  
Windows to Go n’est pas pris en charge lorsque vous installez la topologie intégrée de MBAM avec Configuration Manager 2007.



## Prérequis de déploiement pour l’installation d’MBAM avec Configuration Manager


Vérifiez que vous remplissez les conditions préalables suivantes avant d’installer MBAM avec Configuration Manager:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prérequises</th>
<th align="left">Informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Assurez-vous que le serveur Configuration Manager est un site principal dans le système Configuration Manager.</p></td>
<td align="left"><p>N/A</p></td>
</tr>
<tr class="even">
<td align="left"><p>Activez l’agent client d’inventaire matériel sur le serveur Configuration Manager.</p></td>
<td align="left"><p>Pour Configuration Manager 2007, voir <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> Comment configurer l’inventaire matériel d’un site </a> .</p>
<p>Pour le gestionnaire de configuration de System Center 2012, voir <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> Comment configurer l’inventaire matériel dans Configuration Manager </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Activez l’agent de gestion de la configuration (DCM) souhaité ou les paramètres de conformité, en fonction de la version de Configuration Manager que vous utilisez.</p></td>
<td align="left"><p>Pour Configuration Manager 2007, activez les propriétés de l' <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> agent client de gestion de la configuration souhaitées </a> .</p>
<p>Pour System Center 2012 Configuration Manager, consultez <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> la rubrique Configuration des paramètres de conformité dans Configuration Manager </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Définissez un point Report services dans Configuration Manager. Requis pour les services de rapport SQL Server.</p></td>
<td align="left"><p>Pour Configuration Manager 2007, voir <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> création d’un point de Reporting Services pour SQL Reporting Services </a> .</p>
<p>Pour le gestionnaire de configuration de System Center 2012, voir la configuration <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> requise pour la création de rapports dans Configuration Manager </a> .</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------configuration-manager-supported-versions"></a> Versions prises en charge par Configuration Manager


MBAM prend en charge les versions suivantes de Configuration Manager:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version prise en charge</th>
<th align="left">Service Pack</th>
<th align="left">Architecture système</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft System Center Configuration Manager 2007 R2</p></td>
<td align="left"><p>SP1 ou version ultérieure</p></td>
<td align="left"><p>64 bits</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Même si Configuration Manager 2007 est 32 bits, vous devez l’installer et SQL Server sur un système d’exploitation 64 bits afin de correspondre au logiciel MBAM 64.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Gestionnaire de configuration de Microsoft System Center 2012</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
</tr>
</tbody>
</table>



Pour obtenir la liste des configurations prises en charge pour le serveur Configuration Manager, consultez la page Web appropriée pour la version de Configuration Manager que vous utilisez. MBAM ne possède aucune configuration système supplémentaire pour le serveur Configuration Manager.

## <a href="" id="---------mbam-and-sql-server-system-requirements"></a> Configuration système requise pour MBAM et SQL Server


Les configurations prises en charge et la configuration système requise pour les serveurs MBAM et SQL Server pour la topologie de Configuration Manager sont les mêmes que celles de la topologie autonome. Pour la configuration système autonome requise, voir [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md). Pour le serveur MBAM et le processeur SQL Server, la RAM et l’espace disque requis pour la topologie Configuration Manager, consultez les sections suivantes.

## MBAM, RAM et espace disque requis pour MBAM


Le tableau suivant répertorie les conditions requises processeur de serveur, RAM et espace disque pour les serveurs MBAM lorsque vous utilisez la topologie d’intégration de Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Composant matériel</th>
<th align="left">Configuration minimale</th>
<th align="left">Configuration recommandée</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Processeur</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz ou supérieur</p></td>
</tr>
<tr class="even">
<td align="left"><p>Mémoire vive (RAM)</p></td>
<td align="left"><p>4 Go</p></td>
<td align="left"><p>8 GO</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espace disque disponible</p></td>
<td align="left"><p>1 Go</p></td>
<td align="left"><p>2 Go</p></td>
</tr>
</tbody>
</table>



## Configuration requise pour le processeur SQL Server, la RAM et l’espace disque


Le tableau suivant répertorie les exigences relatives au processeur du serveur, à la RAM et à l’espace disque pour l’ordinateur SQL Server lorsque vous utilisez la topologie d’intégration de Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Composant matériel</th>
<th align="left">Configuration minimale</th>
<th align="left">Configuration recommandée</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Processeur</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz ou supérieur</p></td>
</tr>
<tr class="even">
<td align="left"><p>Mémoire vive (RAM)</p></td>
<td align="left"><p>4 Go</p></td>
<td align="left"><p>8 GO</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Espace disque disponible</p></td>
<td align="left"><p>5 GO</p></td>
<td align="left"><p>5 Go minimum</p></td>
</tr>
</tbody>
</table>



## Autorisations requises pour installer le serveur MBAM


Pour installer MBAM avec Configuration Manager, vous devez disposer d’un utilisateur administratif dans Configuration Manager ayant un rôle de sécurité avec les autorisations minimales indiquées dans le tableau suivant. Le tableau ci-dessous indique également les droits dont vous avez besoin au-delà des droits d’administrateur d’ordinateur de base pour installer le serveur MBAM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Autorisations</th>
<th align="left">Fonctionnalité du serveur MBAM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Rôles de serveurs de connexion d’instances SQL:-dbcreator-processadmin</p></td>
<td align="left"><p>- Base de données de récupération-base de données d’audit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Droits d’instance SQL Server Reporting Services:-créer des dossiers-publier des rapports</p></td>
<td align="left"><p>- Intégration de System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



**System Center2012 Configuration Manager**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Autorisations</th>
<th align="left">Fonctionnalité serveur Configuration Manager</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Droits de site Configuration Manager:-lecture</p></td>
<td align="left"><p>Intégration de System Center Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>Droits de collection de Configuration Manager:-création-suppression-lecture-modification-déploiement des éléments de configuration</p></td>
<td align="left"><p>Intégration de System Center Configuration Manager</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuration des éléments de configuration de Configuration Manager:-création-suppression-lecture</p></td>
<td align="left"><p>Intégration de System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



**Gestionnaire de configuration 2007**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Autorisations</th>
<th align="left">Fonctionnalité serveur Configuration Manager</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Droits de site Configuration Manager:-lecture</p></td>
<td align="left"><p>Intégration de System Center Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>Droits de collection de Configuration Manager:-création-suppression-lecture-ReadResource</p></td>
<td align="left"><p>Intégration de System Center Configuration Manager</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuration des éléments de configuration de Configuration Manager:-création-suppression-lecture/distribution</p></td>
<td align="left"><p>Intégration de System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



## Ordre de déploiement des fonctionnalités MBAM pour la topologie de Configuration Manager


Lors du déploiement de MBAM sur le serveur Configuration Manager, vous devez effectuer les tâches de déploiement dans l’ordre suivant:

1.  Modifiez le fichier Configuration. mof sur le serveur Configuration Manager.

2.  Créez ou modifiez le serveur SMS \ _def. mof.

3.  Installation de MBAM sur le serveur Configuration Manager.

4.  Installation de la base de données de récupération et de la base de données d’audit sur le serveur de base de données.

5.  Installez les fonctionnalités de MBAM sur le serveur d’administration et de surveillance.

## Liste de contrôle de planification pour l’installation d’MBAM avec Configuration Manager


Cette liste de vérification décrit les étapes recommandées et une liste générale des éléments à prendre en compte lors de la planification d’un déploiement de l’administration et de la surveillance de Microsoft BitLocker avec Configuration Manager. Il est recommandé de copier cette liste de vérification dans un tableur et de la personnaliser pour votre utilisation.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Tâche</th>
<th align="left">Références</th>
<th align="left">Remarques</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Passez en revue les informations de mise en route, qui décrivent comment Configuration Manager fonctionne avec MBAM et montre l’architecture de haut niveau recommandée.</p></td>
<td align="left"><p><a href="getting-started---using-mbam-with-configuration-manager.md" data-raw-source="[Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)">Prise en main - Utilisation de MBAM avec Configuration Manager</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Passez en revue les informations de planification qui décrivent les prérequis de déploiement, les configurations prises en charge, les autorisations requises et l’ordre de déploiement pour chaque fonctionnalité.</p></td>
<td align="left"><p>Planification du déploiement de MBAM avec Configuration Manager</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planifiez et configurez les exigences de stratégie de groupe MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Planification des exigences en matière de stratégie de groupe MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Prévoyez et créez des groupes de sécurité de services de domaine Active Directory requis et planifiez les exigences d’appartenance au groupe de sécurité local MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planification des rôles administrateur de MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Plan de déploiement du déploiement du client MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)">Planification du déploiement de clients MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Rubriques connexes


[Utilisation de MBAM avec Configuration Manager](using-mbam-with-configuration-manager.md)









