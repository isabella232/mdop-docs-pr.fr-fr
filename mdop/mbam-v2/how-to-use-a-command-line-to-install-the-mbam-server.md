---
title: Utilisation d'une ligne de commande pour installer le serveur MBAM
description: Utilisation d'une ligne de commande pour installer le serveur MBAM
author: dansimp
ms.assetid: 6ffc6d41-a793-42c2-b997-95ba47550648
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a689a2df77300300073b2731281004feac87305f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811279"
---
# Utilisation d'une ligne de commande pour installer le serveur MBAM


Vous pouvez utiliser une ligne de commande pour installer le serveur MBAM à l’aide du topologie autonome ou du gestionnaire de configuration. L’exemple de ligne de commande suivant concerne le déploiement d’MBAM sur un serveur unique, qui est une architecture qui doit être utilisée uniquement dans un environnement de test. Vous devez modifier la ligne de commande en conséquence lorsque vous déployez MBAM dans un environnement de production, qui doit avoir plusieurs serveurs.

## Ligne de commande pour le déploiement du serveur MBAM 2.0 avec la topologie autonome


Vous pouvez utiliser une ligne de commande similaire à celle ci-dessous pour installer le serveur MBAM avec la topologie autonome.

``` syntax
MbamSetup.exe /qb /l*v MaltaServerInstall.log TOPOLOGY=0 I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 ADDLOCAL=KeyDatabase,ReportsDatabase,Reports,AdministrationMonitoringServer,SelfServiceServer,PolicyTemplate,REPORTS_USERACCOUNT=[UserDomain]\[UserName1] REPORTS_USERACCOUNTPW=[UserPwd1] COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

Le tableau suivant décrit les paramètres de ligne de commande pour le déploiement du serveur MBAM avec la topologie autonome.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paramètre</th>
<th align="left">Valeur du paramètre</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TOPOLOGIE</p></td>
<td align="left"><p>0,4</p></td>
<td align="left"><p>0-topologie autonome</p></td>
</tr>
<tr class="even">
<td align="left"><p>I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</p></td>
<td align="left"><p>nommée</p></td>
<td align="left"><p>0 – n’acceptez pas le contrat de licence agreement1: acceptez le contrat de licence.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ADDLOCAL</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Fonctionnalités devant être installées sur le serveur</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Keydatabase</p></td>
<td align="left"><p>Base de données de récupération</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>ReportsDatabase</p></td>
<td align="left"><p>Base de données des rapports de conformité et d’audit</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Rapports</p></td>
<td align="left"><p>Rapports de conformité et d’audit</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>AdministrationMonitoringServer</p></td>
<td align="left"><p>Site Web d’administration et de surveillance</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>SelfServiceServer</p></td>
<td align="left"><p>Portail libre-service</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>PolicyTemplate</p></td>
<td align="left"><p>Modèle de stratégie de groupe MBAM</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTS_USERACCOUNT</p></td>
<td align="left"><p>UserDomain [UserName1]</p></td>
<td align="left"><p>Domaine et compte d’utilisateur du compte Reporting Services qui accèdent à la base de données d’audit et de conformité</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTS_USERACCOUNTPW</p></td>
<td align="left"><p>[UserPwd1]</p></td>
<td align="left"><p>Mot de passe du compte de service Reporting Services qui accède à la base de données d’audit et de conformité</p></td>
</tr>
<tr class="even">
<td align="left"><p>COMPLIDB_SQLINSTANCE</p></td>
<td align="left"><p>masque</p></td>
<td align="left"><p>Nom de l’instance SQL Server pour la base de données d’audit et de conformité: remplacez <strong> % ComputerName% </strong> par le nom de l’ordinateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RECOVERYANDHWDB_SQLINSTANCE</p></td>
<td align="left"><p>masque</p></td>
<td align="left"><p>Nom de l’instance SQL Server pour la base de données de récupération: remplacez <strong> % ComputerName% </strong> par le nom de l’ordinateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SRS_INSTANCENAME</p></td>
<td align="left"><p>masque</p></td>
<td align="left"><p>Instance SQL Server Reporting Server sur laquelle sont installés les rapports de conformité et d’audit: remplacez <strong> % ComputerName% </strong> par le nom de l’ordinateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ADMINANDMON_WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Port pour le site Web d’administration et de surveillance; «83» n’est qu’un exemple</p></td>
</tr>
<tr class="even">
<td align="left"><p>WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Port pour le site Web du portail libre-service; «83» n’est qu’un exemple</p></td>
</tr>
</tbody>
</table>

 

## Ligne de commande pour le déploiement du serveur MBAM 2.0 avec la topologie Configuration Manager


Vous pouvez utiliser une ligne de commande semblable à ce qui suit pour installer le serveur MBAM avec la topologie Configuration Manager.

``` syntax
MbamSetup.exe /qn /l*v MaltaServerInstall.log I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 TOPOLOGY=1 COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% REPORTS_USERACCOUNT=[UserDomain]\[UserName] REPORTS_USERACCOUNTPW=[UserPwd] ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

Le tableau suivant décrit les paramètres de ligne de commande pour l’installation du serveur MBAM 2.0 avec la topologie Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paramètre</th>
<th align="left">Valeur du paramètre</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TOPOLOGIE</p></td>
<td align="left"><p>1</p></td>
<td align="left"><p>1-topologie de Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</p></td>
<td align="left"><p>nommée</p></td>
<td align="left"><p>0 – n’acceptez pas le contrat de licence agreement1: acceptez le contrat de licence.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>COMPLIDB_SQLINSTANCE</p></td>
<td align="left"><p>masque</p></td>
<td align="left"><p>Nom de l’instance SQL Server pour la base de données d’audit: remplacez <strong> % ComputerName% </strong> par le nom de l’ordinateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RECOVERYANDHWDB_SQLINSTANCE</p></td>
<td align="left"><p>masque</p></td>
<td align="left"><p>Nom de l’instance SQL Server pour la base de données de récupération: remplacez <strong> % ComputerName% </strong> par le nom de l’ordinateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SRS_INSTANCENAME</p></td>
<td align="left"><p>masque</p></td>
<td align="left"><p>Instance SQL Server Reporting Server sur laquelle les rapports d’audit seront installés: remplacez% ComputerName% par le nom de l’ordinateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTS_USERACCOUNT</p></td>
<td align="left"><p>UserDomain [UserName1]</p></td>
<td align="left"><p>Domaine et compte d’utilisateur du compte Reporting Services qui accèdent à la base de données d’audit et de conformité</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTS_USERACCOUNTPW</p></td>
<td align="left"><p>[UserPwd1]</p></td>
<td align="left"><p>Mot de passe du compte de service Reporting Services qui accède à la base de données d’audit et de conformité</p></td>
</tr>
<tr class="even">
<td align="left"><p>ADMINANDMON_WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Port pour le site Web d’administration et de surveillance; «83» n’est qu’un exemple</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WEBSITE_PORT</p></td>
<td align="left"><p>83</p></td>
<td align="left"><p>Port pour le site Web du portail libre-service; «83» n’est qu’un exemple</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Déploiement de l'infrastructure de serveur MBAM2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





