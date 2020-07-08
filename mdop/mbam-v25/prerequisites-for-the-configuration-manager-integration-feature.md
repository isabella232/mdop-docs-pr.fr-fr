---
title: Conditions préalables pour le composant Intégration Configuration Manager
description: Conditions préalables pour le composant Intégration Configuration Manager
author: dansimp
ms.assetid: b318cbd3-b009-44b8-991b-f7364c1cae88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af7abd50f6218810dd6718f091512b48fee32652
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810901"
---
# Conditions préalables pour le composant Intégration Configuration Manager


Si vous déployez MBAM avec la topologie d’intégration System Center Configuration Manager, nous vous recommandons d’utiliser une architecture à trois serveurs, comme décrit dans [architecture de niveau supérieur d’MBAM 2,5 avec la topologie d’intégration de Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md). Cette architecture peut prendre en charge des ordinateurs clients 500 000.

**Important**  
Windows to Go n’est pas pris en charge pour l’installation de la topologie d’intégration de Configuration Manager lorsque vous utilisez Configuration Manager 2007.



## Conditions générales requises pour la fonctionnalité d’intégration de Configuration Manager


Lorsque vous installez MBAM avec Configuration Manager, les conditions préalables supplémentaires suivantes sont requises en plus de la configuration requise pour la topologie autonome.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prérequises</th>
<th align="left">Informations complémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Le serveur Configuration Manager est un site principal dans le système Configuration Manager.</p></td>
<td align="left"><p>N/A</p></td>
</tr>
<tr class="even">
<td align="left"><p>L’agent client d’inventaire matériel est sur le serveur Configuration Manager.</p></td>
<td align="left"><p>Pour le gestionnaire de configuration de System Center 2012, voir <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> Comment configurer l’inventaire matériel dans Configuration Manager </a> .</p>
<p>Pour Configuration Manager 2007, voir <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> Comment configurer l’inventaire matériel d’un site </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>L’une des options suivantes est activée, en fonction de la version de Configuration Manager que vous utilisez:</p>
<ul>
<li><p>Paramètres de conformité-(gestionnaire de configuration de System Center 2012)</p></li>
<li><p>Agent client de gestion des configurations souhaité (DCM) – (Configuration Manager 2007)</p></li>
</ul></td>
<td align="left"><p>Pour System Center 2012 Configuration Manager, consultez <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> la rubrique Configuration des paramètres de conformité dans Configuration Manager </a> .</p>
<p>Pour Configuration Manager 2007, voir <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> Propriétés de l’agent du client de gestion de configuration souhaitées </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Un point Report services est défini dans Configuration Manager. Requis pour SQL Server Reporting Services (SSRS).</p></td>
<td align="left"><p>Pour le gestionnaire de configuration de System Center 2012, voir la configuration <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> requise pour la création de rapports dans Configuration Manager </a> .</p>
<p>Pour Configuration Manager 2007, voir <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> création d’un point de Reporting Services pour SQL Reporting Services </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuration Manager 2007 nécessite Microsoft .NET Framework 2,0</p></td>
<td align="left"><p>L’agent client de gestion des configurations souhaité (DCM) dans Configuration Manager 2007 nécessite .NET Framework 2,0 pour signaler la conformité.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>L’installation de .NET Framework 3,5 installe automatiquement .NET Framework 2,0.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Autorisations requises pour installer MBAM avec Configuration Manager


Pour installer MBAM avec Configuration Manager, vous devez disposer d’un utilisateur administratif dans Configuration Manager ayant un rôle de sécurité avec les autorisations minimales indiquées dans le tableau suivant. Le tableau ci-dessous indique également les droits dont vous avez besoin au-delà des droits d’administrateur d’ordinateur de base pour installer le serveur MBAM.

**Les autorisations figurant dans le tableau ci-dessous s’appliquent aux deux versions de Configuration Manager.**

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
<td align="left"><p>Rôles de serveurs de connexion d’instances SQL Server:-dbcreator-processadmin</p></td>
<td align="left"><p>- Base de données de récupération-base de données d’audit</p></td>
</tr>
<tr class="even">
<td align="left"><p>Droits d’instance SSRS:-créer des dossiers-publier des rapports</p></td>
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



## Modifications requises pour les fichiers. mof


Pour permettre aux ordinateurs clients de signaler les détails de conformité BitLocker par le biais des rapports du gestionnaire de configuration MBAM, vous devez modifier le fichier de configuration. mof et le fichier SMS \ _def. mof pour System Center 2012 Configuration Manager et Microsoft System Center Configuration Manager 2007. Pour obtenir des instructions, consultez [la configuration requise pour le serveur MBAM 2,5 qui s’applique uniquement à la topologie d’intégration de Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).



## Rubriques connexes


[Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

[Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)



## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





