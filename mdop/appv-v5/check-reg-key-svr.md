---
title: Vérifier les clés de Registre avant d'installer App-V5.x Server
description: Vérifier les clés de Registre avant d'installer App-V5.x Server
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.openlocfilehash: 9fe5a1b37d0fb5208d138939bb2fc79c89171fb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805929"
---
# Vérifier les clés de Registre avant d'installer App-V5.x Server

Si vous procédez à la mise à niveau de l’application-V Server du correctif logiciel pour App-V 5,0 SP1 ou version ultérieure, suivez les étapes décrites dans cette section avant d’installer l’App-V 5. x Server.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Lorsque cette étape est nécessaire</strong></p></td>
<td align="left"><p>Vous procédez à la mise à niveau de App-V 5,0 SP1 avec les packages de correctifs suivants que vous avez installés à l’aide d’un fichier. msp.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Quels composants nécessitent cette étape</strong></p></td>
<td align="left"><p>Uniquement les composants serveur App-V que vous effectuez une mise à niveau.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Lorsque vous devez effectuer cette étape</strong></p></td>
<td align="left"><p>Avant de mettre à niveau l’application-V Server vers App-V 5. x</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Ce que vous devez faire</strong></p></td>
<td align="left"><p>À l’aide des informations contenues dans les tableaux ci-dessous, vous devez mettre à jour chaque valeur de clé de registre en <code>HKLM\Software\Microsoft\AppV\Server</code> fonction de la valeur que vous avez fournie lors de votre installation de serveur d’origine. Cette étape restaure les valeurs de Registre susceptibles d’avoir été supprimées lors de l’installation des packages de correctifs App-V 5,0 SP1.</p></td>
</tr>
</tbody>
</table>

 

**Clé ManagementDatabase**

Si vous installez la base de données de gestion, définissez les clés de Registre suivantes `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la clé</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>Indique si un compte d’accès public est requis pour accéder aux bases de données de gestion non locales. La valeur est définie sur «1» s’il est requis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_NAME</p></td>
<td align="left"><p>Nom de la base de données de gestion.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Compte utilisé pour l’accès en lecture (public) à la base de données de gestion.</p>
<p>Utilisé lorsque <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> est défini sur 1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>ID de sécurité (SID) du compte utilisé pour l’accès en lecture (public) à la base de données de gestion.</p>
<p>Utilisé lorsque <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> est défini sur 1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instance SQL Server de la base de données de gestion.</p>
<p>Si la valeur est vide, l’instance de base de données par défaut est utilisée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Compte utilisé pour l’accès en écriture (administrateur) à la base de données de gestion.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>ID de sécurité (SID) du compte utilisé pour l’accès en écriture (administrateur) à la base de données de gestion.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>Compte d’ordinateur distant du serveur de gestion (domaine\compte).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>Connexion administrateur d’installation pour le serveur de gestion (domaine\compte).</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>Valeurs valides:</p>
<ul>
<li><p><strong>1 </strong> – le service de gestion est sur l’ordinateur local, c’est-à-dire MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT est vide.</p></li>
<li><p><strong>0 </strong> - le service de gestion est sur un ordinateur différent de l’ordinateur local.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Clé ManagementService**

Si vous installez le serveur de gestion, définissez les clés de Registre suivantes `HKLM\Software\Microsoft\AppV\Server\ManagementService` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la clé</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MANAGEMENT_ADMINACCOUNT</p></td>
<td align="left"><p>Le compte ou le groupe AD DS (Active Directory Domain Services) qui est autorisé à gérer App-V (domaine\compte).</p></td>
</tr>
<tr class="even">
<td align="left"><p>MANAGEMENT_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instance SQL Server qui contient la base de données de gestion.</p>
<p>Si la valeur est vide, l’instance de base de données par défaut est utilisée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MANAGEMENT_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>Nom du serveur SQL distant doté de la base de données de gestion.</p>
<p>Si la valeur est vide, l’ordinateur local est utilisé.</p></td>
</tr>
</tbody>
</table>

 

**Clé ReportingDatabase**

Si vous installez la base de données de création de rapports, définissez ces clés de Registre sous `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la clé</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</p></td>
<td align="left"><p>Indique si un compte d’accès public est requis pour accéder aux bases de données de création de rapports non locales. La valeur est définie sur «1» s’il est requis.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_NAME</p></td>
<td align="left"><p>Nom de la base de données de création de rapports.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</p></td>
<td align="left"><p>Compte utilisé pour l’accès en lecture (public) à la base de données de création de rapports.</p>
<p>Utilisé lorsque <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> est défini sur 1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p>ID de sécurité (SID) du compte utilisé pour l’accès en lecture (public) à la base de données de création de rapports.</p>
<p>Utilisé lorsque <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> est défini sur 1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instance SQL Server de la base de données de création de rapports.</p>
<p>Si la valeur est vide, l’instance de base de données par défaut est utilisée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
<td align="left"><p>Compte d’ordinateur distant du serveur de rapports (domaine\compte).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
<td align="left"><p>Connexion administrateur d’installation pour le serveur de rapports (domaine\compte).</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_SERVER_MACHINE_USE_LOCAL</p></td>
<td align="left"><p>Valeurs valides:</p>
<ul>
<li><p><strong>1 </strong> – le service de création de rapports est sur l’ordinateur local, c’est-à-dire REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT est vide.</p></li>
<li><p><strong>0 </strong> - le service de création de rapports est sur un ordinateur différent de l’ordinateur local.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Clé ReportingService**

Si vous installez le serveur de création de rapports, définissez ces clés de Registre sous `HKLM\Software\Microsoft\AppV\Server\ReportingService` .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom de la clé</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>REPORTING_DB_SQL_INSTANCE</p></td>
<td align="left"><p>Instance SQL Server de la base de données de création de rapports.</p>
<p>Si la valeur est vide, l’instance de base de données par défaut est utilisée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>REPORTING_DB_SQL_SERVER_NAME</p></td>
<td align="left"><p>Nom du serveur SQL distant avec la base de données de création de rapports.</p>
<p>Si la valeur est vide, l’ordinateur local est utilisé.</p></td>
</tr>
</tbody>
</table>

