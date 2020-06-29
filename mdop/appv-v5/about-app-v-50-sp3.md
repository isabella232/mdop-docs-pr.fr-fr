---
title: À propos d'App-V5.0 SP3
description: À propos d'App-V5.0 SP3
author: dansimp
ms.assetid: 67b5268b-edc1-4027-98b0-b3937dd70a6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: bc72f3f72c2b06470287dfe4ba3ed22abcc6068b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806121"
---
# À propos d'App-V5.0 SP3


Les sections suivantes permettent de consulter des informations sur les modifications importantes qui s’appliquent à la virtualisation des applications Microsoft (App-V) 5,0 SP3:

-   [Configuration logicielle requise pour App-V 5,0 SP3 et configurations prises en charge](#bkmk-sp3-prereq-configs)

-   [Migration vers App-V 5,0 SP3](#bkmk-migrate-to-50sp3)

-   [Le fichier XML de groupe de connexion créé manuellement nécessite une mise à jour du schéma](#bkmk-update-schema-cg)

-   [Améliorations apportées aux groupes de connexion](#bkmk-cg-improvements)

-   [Les administrateurs peuvent publier et annuler la publication de packages pour un utilisateur spécifique.](#bkmk-usersid-pub-pkgs-specf-user)

-   [Autoriser uniquement les administrateurs à publier et à retirer des packages](#bkmk-admins-only-pub-unpub-pkgs)

-   [La clé de Registre RunVirtual prend en charge les packages publiés pour l’utilisateur](#bkmk-runvirtual-reg-key)

-   [Nouvelles cmdlets PowerShell et aide sur les cmdlets](#bkmk-posh-cmdlets-help)

-   [Le répertoire principal de l’application virtuelle (PVAD) est masqué, mais peut être activé.](#bkmk-pvad-hidden)

-   [ClientVersion est requis pour afficher les métadonnées de publication d’application-V](#bkmk-pub-metadata-clientversion)

-   [Les journaux des événements App-V ont été consolidés](#bkmk-event-logs-moved)

## <a href="" id="bkmk-sp3-prereq-configs"></a>Configuration logicielle requise pour App-V 5,0 SP3 et configurations prises en charge


Pour plus d’informations 5,0 sur les configurations logicielles prises en charge, voir les liens suivants:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Liens vers les composants requis et les configurations prises en charge</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-50-sp3-prerequisites.md" data-raw-source="[App-V 5.0 SP3 Prerequisites](app-v-50-sp3-prerequisites.md)">Composants requis d'App-V5.0 SP3</a></p></td>
<td align="left"><p>Logiciels requis que vous devez installer avant de démarrer l’installation App-V 5,0 SP3</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)">Configurations prises en charge d'App-V5.0 SP3</a></p></td>
<td align="left"><p>Systèmes d’exploitation pris en charge et configuration matérielle requise pour le serveur App-V, le Sequencer et les composants clients</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-migrate-to-50sp3"></a>Migration vers App-V 5,0 SP3


Utilisez les informations ci-dessous pour effectuer une mise à niveau vers App-V 5,0 SP3 à partir d’une version antérieure.

### Avant de commencer la mise à niveau

Passez en revue les informations suivantes avant de commencer la mise à niveau:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Éléments à réviser avant la mise à niveau</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Composants à mettre à niveau</p></td>
<td align="left"><ol>
<li><p>App-V Server</p></li>
<li><p>Sequencer</p></li>
<li><p>Client App-V ou App-V (service bureau à distance)</p></li>
<li><p>Groupes de connexion</p></li>
</ol>
<div class="alert">
<strong>Remarque</strong><br/><p>Pour utiliser l’interface utilisateur du client App-V, téléchargez la version existante à partir de l’application de l’interface utilisateur du <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> client Microsoft application virtualization 5,0 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Mise à niveau à partir de App-V 4. x</p></td>
<td align="left"><p>Vous devez d’abord effectuer une mise à niveau vers App-V 5,0. Vous ne pouvez pas effectuer la mise à niveau directement de App-V 4. x vers App-V 5,0 SP3.</p>
<p>Pour plus d’informations, voir:</p>
<ul>
<li><p><a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)">À propos d'App-V5.0</a> </p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)">Planification d'une migration à partir d'une version précédente d'App-V</a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Mise à niveau à partir de App-V 5,0 ou version ultérieure</p></td>
<td align="left"><p>Vous pouvez effectuer une mise à niveau vers App-V 5,0 SP3 directement à partir des versions suivantes:</p>
<ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul>
<p>Pour effectuer une mise à niveau vers App-V 5,0 SP3, suivez les étapes décrites dans les sections restantes de cet article.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modifications requises apportées aux packages et aux groupes de connexion après la mise à niveau</p></td>
<td align="left"><p>Aucune. Les packages et les groupes de connexion continuent de fonctionner comme il le fera actuellement.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a>Procédure de mise à niveau de l’infrastructure App-V

Suivez les étapes ci-dessous pour mettre à niveau chaque composant de l’infrastructure App-V vers App-V 5,0 SP3.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Étape</th>
<th align="left">Pour plus d’informations</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Étape 1: mettez à niveau le serveur App-V.</p>
<p>Si vous n’utilisez pas le serveur App-V, ignorez cette étape et passez à l’étape suivante.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Le client App-V 5,0 SP3 est compatible avec le serveur App-V 5,0 SP1.</p>
</div>
<div>

</div></td>
<td align="left"><p>Procédez comme suit: </p>
<ol>
<li><p>Consultez les <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)"> notes de publication pour App-V 5,0 SP3 </a> pour les problèmes qui peuvent affecter l’installation de l’application-v Server.</p></li>
<li><p>Effectuez l’une des opérations suivantes, selon la méthode que vous utilisez pour mettre à niveau la base de données de gestion et/ou la base de données de création de rapports, procédez comme suit:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Méthode de mise à niveau de base de données</th>
<th align="left">Étape</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Installer</p></td>
<td align="left"><p>Ignorez cette étape et passez à l’étape 3, «si vous effectuez la mise à niveau de l’application-V Server».</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scripts SQL</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Base de données de gestion</strong></p></td>
<td align="left"><p>Pour procéder à l’installation ou à la mise à niveau, voir <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> scripts SQL pour installer ou mettre à niveau la base de données du serveur de gestion de l’application-V 5,0 SP3 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Base de données de création de rapports</strong></p></td>
<td align="left"><p>Suivez les étapes décrites dans la <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> procédure de déploiement des bases de données App-V à l’aide de scripts SQL </a> .</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>
<p> </p></li>
<li><p>Si vous effectuez une mise à niveau de l’application-V Server à partir du correctif logiciel App-V 5,0 SP1 ou version ultérieure, suivez les étapes de la section <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)"> vérifier les clés de registre après l’installation de l’app-v 5,0 SP3 Server </a> .</p></li>
<li><p>Suivez les étapes décrites dans la <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> procédure de déploiement du serveur App-V 5,0 </a> .</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Étape 2: mettre à niveau le Sequencer App-V.</p></td>
<td align="left"><p>Découvrez <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> Comment installer le Sequencer </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Étape 3: mettez à niveau le client App-V ou le client RDS (App-V).</p></td>
<td align="left"><p>Découvrez <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> comment déployer le client App-V </a> .</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-check-reg-key-svr"></a>Vérifier les clés de Registre avant d’installer le serveur App-V 5,0 SP3

Étape 3 du tableau précédent.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Lorsque cette étape est nécessaire</strong></p></td>
<td align="left"><p>Vous effectuez une mise à niveau à partir de App-V SP1 avec les packages de correctifs suivants que vous avez installés à l’aide d’un fichier. msp.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Quels composants nécessitent cette étape</strong></p></td>
<td align="left"><p>Uniquement les composants serveur App-V que vous effectuez une mise à niveau.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Lorsque vous devez effectuer cette étape</strong></p></td>
<td align="left"><p>Avant de mettre à niveau l’application-V Server vers App-V 5,0 SP3</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Ce que vous devez faire</strong></p></td>
<td align="left"><p>À l’aide des informations contenues dans les tableaux ci-dessous, vous devez mettre à jour chaque valeur de clé de registre en <code>HKLM\Software\Microsoft\AppV\Server</code> fonction de la valeur que vous avez fournie lors de votre installation de serveur d’origine. Cette étape restaure les valeurs de Registre susceptibles d’avoir été supprimées lors de l’installation des packages de correctifs App-V SP1.</p></td>
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



## <a href="" id="bkmk-update-schema-cg"></a>Le fichier XML de groupe de connexion créé manuellement nécessite une mise à jour du schéma


Si vous créez manuellement le fichier XML de groupe de connexion et souhaitez utiliser les nouvelles fonctionnalités «packages facultatifs» et «utiliser les versions» décrites dans [améliorations apportées aux groupes de connexion](#bkmk-cg-improvements), vous devez spécifier le schéma suivant dans le fichier XML:

`xmlns="http://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"`

Pour des exemples et des informations supplémentaires, voir [à propos du fichier de groupe de connexion](about-the-connection-group-file.md).

## <a href="" id="bkmk-cg-improvements"></a>Améliorations apportées aux groupes de connexion


Vous pouvez gérer les groupes de connexion plus facilement en utilisant des packages facultatifs et d’autres améliorations qui ont été ajoutées dans App-V 5,0 SP3. Le tableau suivant récapitule les tâches que vous pouvez effectuer à l’aide des nouvelles fonctionnalités de groupe de connexion, ainsi que des liens vers des informations plus détaillées sur chaque tâche.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche/fonctionnalité</th>
<th align="left">Description</th>
<th align="left">Liens vers des informations complémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Permettre à un groupe de connexions d’inclure des packages facultatifs</p></td>
<td align="left"><p>L’inclusion de packages facultatifs dans un groupe de connexions vous permet de déterminer dynamiquement les applications qui seront incluses dans l’environnement virtuel du groupe de connexions, en fonction des applications auxquelles les utilisateurs sont autorisés.</p>
<p>Vous n’avez pas besoin de gérer autant de groupes de connexions, car vous pouvez mélanger des packages facultatifs et non facultatifs dans le même groupe de connexion. Le mélange de packages permet à différents groupes d’utilisateurs d’utiliser le même groupe de connexion, même si les utilisateurs ne peuvent avoir qu’un seul package en commun.</p>
<p><strong>Par exemple </strong> : vous pouvez activer un package avec Microsoft Office pour tous les utilisateurs, mais activer différents packages facultatifs, qui contiennent différents composants Office, à différents sous-ensembles d’utilisateurs.</p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">Comment utiliser des packages facultatifs dans les groupes de connexion</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Annuler la publication ou la suppression d’un package facultatif sans changer le groupe de connexion</p></td>
<td align="left"><p>Annulez ou supprimez, ou annulez ou republiez un package facultatif, qui se trouve dans un groupe de connexion, sans avoir besoin de désactiver ou réactiver le groupe de connexion sur le client App-V.</p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)">Comment utiliser des packages facultatifs dans les groupes de connexion</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Publier des groupes de connexion contenant des packages publiés par l’utilisateur et globalement publiés</p></td>
<td align="left"><p>Créer un groupe de connexion publié par l’utilisateur contenant des packages publiés par l’utilisateur et globalement publiés.</p></td>
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)">Comment créer un groupe de connexion avec des packages publiés par l’utilisateur et globalement</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Créer un groupe de connexions ignorer la version du package</p></td>
<td align="left"><p>Configurez un groupe de connexion pour accepter n’importe quelle version d’un package, qui vous permet de mettre à niveau un package sans avoir à désactiver le groupe de connexion. Par ailleurs, s’il existe un package facultatif dont la version n’est pas correcte dans le groupe de connexion, le package est ignoré et ne bloque pas la création de l’environnement virtuel du groupe de connexion.</p></td>
<td align="left"><p><a href="how-to-make-a-connection-group-ignore-the-package-version.md" data-raw-source="[How to Make a Connection Group Ignore the Package Version](how-to-make-a-connection-group-ignore-the-package-version.md)">Comment faire en sorte qu'un groupe de connexion ignore la version du package</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Limiter les capacités de publication des utilisateurs finaux</p></td>
<td align="left"><p>Activez uniquement les administrateurs (pas les utilisateurs finaux) pour publier des packages et activer les groupes de connexion.</p></td>
<td align="left"><p>Pour plus d’informations sur les groupes de connexion, voir <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)"> interdire uniquement aux administrateurs d’activer les groupes de connexion.</a></p>
<p>Pour plus d’informations sur les packages, voir les articles suivants:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Méthode</th>
<th align="left">Lien vers plus d’informations</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Console de gestion</p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)">Comment publier un package à l’aide de la console de gestion</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)">Comment gérer des groupes de connexion sur un ordinateur autonome à l'aide de PowerShell</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Système de remise de logiciels électroniques tiers</p></td>
<td align="left"><p><a href="how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md" data-raw-source="[How to Enable Only Administrators to Publish Packages by Using an ESD](how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md)">Comment autoriser uniquement les administrateurs à publier des packages à l'aide d'un système ESD</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>Activer ou désactiver un groupe de connexions pour un utilisateur spécifique</p></td>
<td align="left"><p>Les administrateurs peuvent activer ou désactiver un groupe de connexions pour un utilisateur spécifique à l’aide du <strong> paramètre facultatif-UserSid </strong> avec les applets de commande suivantes:</p>
<ul>
<li><p>Enable-AppVClientConnectionGroup</p></li>
<li><p>Disable-AppVClientConnectionGroup</p></li>
</ul></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic)">Comment gérer des groupes de connexion sur un ordinateur autonome à l'aide de PowerShell</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fusion de chemins de package identiques dans un répertoire virtuel dans les groupes de connexions</p></td>
<td align="left"><p>Si au moins deux packages d’un groupe de connexion contiennent des chemins d’accès identiques, les chemins d’accès sont fusionnés dans un répertoire virtuel unique à l’intérieur de l’environnement virtuel du groupe de connexion.</p>
<p>Cette fusion des chemins d’accès permet à une application dans un même package d’accéder aux fichiers d’un autre package.</p></td>
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp)">À propos de l’environnement virtuel du groupe de connexion</a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-usersid-pub-pkgs-specf-user"></a>Les administrateurs peuvent publier et annuler la publication de packages pour un utilisateur spécifique.


Les administrateurs peuvent utiliser les applets de commande suivantes pour publier ou annuler la publication de packages pour un utilisateur spécifique. Pour utiliser les applets de applet, entrez le paramètre **– UserSid** , suivi de l’identificateur de sécurité (SID) de l’utilisateur. Pour plus d’informations, voir:

-   [Gestion de packages App-V5.0 s'exécutant sur un ordinateur autonome à l'aide de PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-pub-pkg-a-user-standalone-posh)

-   [Gestion de packages App-V5.0 s'exécutant sur un ordinateur autonome à l'aide de PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-unpub-pkg-specfc-use)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Applet de commande</th>
<th align="left">Exemples</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Publisher-AppvClientPackage</p></td>
<td align="left"><p>Publisher-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
</tr>
<tr class="even">
<td align="left"><p>Annuler la publication-AppvClientPackage</p></td>
<td align="left"><p>Unpublish-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-admins-only-pub-unpub-pkgs"></a>Autoriser uniquement les administrateurs à publier et à retirer des packages


Vous pouvez activer uniquement les administrateurs (pas les utilisateurs finaux) pour publier et annuler la publication des packages à l’aide de l’une des méthodes suivantes:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Méthode</th>
<th align="left">Informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Paramètre de la stratégie de groupe</p></td>
<td align="left"><p>Accédez au nœud d’objet de stratégie de groupe suivant:</p>
<p><strong>&gt;Stratégies de Configuration ordinateur &gt; modèles d’administration &gt; &gt; application de la publication de l’application-V &gt; </strong> .</p>
<p>Activez le <strong> paramètre exiger une stratégie de groupe publier en tant qu’administrateur </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)">Gestion de packages App-V5.0 s'exécutant sur un ordinateur autonome à l'aide de PowerShell</a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-runvirtual-reg-key"></a>La clé de Registre RunVirtual prend en charge les packages publiés pour l’utilisateur


App-V 5,0 SP3 ajoute une prise en charge de l’utilisation de la clé de Registre **RunVirtual** avec des applications virtualisées dans des packages publiés par l’utilisateur. La clé de Registre **RunVirtual** vous permet d’exécuter une application installée localement dans un environnement virtuel, ainsi que des applications virtualisées à l’aide de App-V.

Auparavant, les applications virtualisées des packages App-V devaient être publiées globalement. Pour plus d’informations sur **RunVirtual** et sur d’autres méthodes d’exécution des applications installées en local dans un environnement virtuel avec des applications virtualisées, voir [exécution d’une application installée localement dans un environnement virtuel avec des applications virtualisées](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).

## <a href="" id="bkmk-posh-cmdlets-help"></a>Nouvelles cmdlets PowerShell et aide sur les cmdlets


Les nouvelles cmdlets PowerShell et l’aide à la mise à jour des applets de service sont inclus dans App-V 5,0 SP3. Pour télécharger les modules de cmdlet, voir [Comment charger les applets de cmdlet PowerShell et obtenir une aide pour les cmdlets](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).

### Nouvelle applet de cmdlet PowerShell Server App-V 5,0 SP3

De nouvelles cmdlets Windows PowerShell pour le serveur App-V ont été ajoutées pour vous permettre de gérer les groupes de connexion.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Applet de commande</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Add-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Ajoute un package à la fin d’un groupe de connexion&#39;liste des packages et vous permet de configurer le package en option et/ou sans version dans le groupe de connexion.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Set-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Vous permet de modifier les détails relatifs au package de groupe de connexion, par exemple, s’il est facultatif.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Remove-AppvServerConnectionGroupPackage</p></td>
<td align="left"><p>Supprime un package d’un groupe de connexion.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-get-cmdlet-help"></a>Obtenir de l’aide pour les applets de applet PowerShell

L’aide de l’applet de commande est disponible dans les formats suivants:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Format</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Module téléchargeable</p></td>
<td align="left"><p>Pour obtenir la dernière aide après le téléchargement du module de cmdlet:</p>
<ol>
<li><p>Ouvrez l’environnement d’exécution de scripts Windows PowerShell ou Windows PowerShell intégré.</p></li>
<li><p>Tapez l’une des commandes suivantes pour charger les applets de commande pour le module souhaité:</p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Composant App-V</th>
<th align="left">Commande pour taper</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V Server</p></td>
<td align="left"><p>Mise à jour-aide-module AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>Séquenceur App-V</p></td>
<td align="left"><p>Mise à jour-aide-module AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Client App-V</p></td>
<td align="left"><p>Mise à jour-aide-module AppvClient</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>Sur TechNet en tant que pages Web</p></td>
<td align="left"><p>Pour plus d’information, voir le nœud App-V sous l' <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> Automation Microsoft Desktop Optimization with Windows PowerShell </a> .</p></td>
</tr>
</tbody>
</table>



Pour plus d’informations, voir [Comment charger les applets de cmdlet PowerShell et obtenir une aide pour les cmdlets](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).

## <a href="" id="bkmk-pvad-hidden"></a>Le répertoire principal de l’application virtuelle (PVAD) est masqué, mais peut être activé.


Le répertoire principal de l’application virtuelle (PVAD) est masqué dans App-V 5,0 SP3, mais vous pouvez le réactiver en utilisant l’une des méthodes suivantes:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Méthode</th>
<th align="left">Étapes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Utiliser un paramètre de ligne de commande</p></td>
<td align="left"><p>Transmettez le <strong> paramètre-EnablePVADControl </strong> à <strong> l' </strong>Sequencer.exe.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Créer une sous-clé de Registre</p></td>
<td align="left"><ol>
<li><p>Dans l’éditeur du Registre, accédez à: <code>HKLM\SOFTWARE\Microsoft\AppV\Sequencer\Compatibility</code></p>
<div class="alert">
<strong>Remarque</strong><br/><p>S' <code>Compatibility</code> il n’existe pas, vous devez le créer.</p>
</div>
<div>

</div></li>
<li><p>Créez une valeur DWORD nommée <strong> EnablePVADControl </strong> et définissez la valeur sur <strong> 1 </strong> .</p>
<p>La valeur <strong> 0 </strong> indique que PVAD est masqué.</p></li>
</ol></td>
</tr>
</tbody>
</table>



En **savoir plus sur PVAD:** Lorsque vous utilisez le Sequencer pour créer un package, vous pouvez entrer un chemin d’installation pour le package. Dans les versions précédentes de App-V, vous deviez spécifier le répertoire de l’application virtuelle (PVAD) principal de l’application comme chemin d’accès. PVAD est le répertoire dans lequel vous devez généralement installer une application sur votre ordinateur local si vous n’utilisez pas App-V. Par exemple, si vous avez installé Office sur un ordinateur, le PVAD est généralement C:\\Program Files\\Microsoft Office\\.

## <a href="" id="bkmk-pub-metadata-clientversion"></a>ClientVersion est requis pour afficher les métadonnées de publication d’application-V


Dans App-V 5,0 SP3, vous devez fournir les valeurs suivantes dans l’adresse lorsque vous interrogez le serveur de publication App-V pour les métadonnées:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Valeur</th>
<th align="left">Informations supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>ClientVersion</strong></p></td>
<td align="left"><p>Si vous omettez le <strong> </strong> paramètre ClientVersion de la requête, les métadonnées excluent les nouvelles fonctionnalités d’App-V 5,0 SP3.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Clientos</strong></p></td>
<td align="left"><p>Vous devez renseigner cette valeur uniquement si vous sélectionnez des systèmes d’exploitation de clients spécifiques lors du séquencé du package. Si vous sélectionnez la valeur par défaut (tous les systèmes d’exploitation), ne spécifiez pas cette valeur dans la requête.</p>
<p>Si vous omettez le <strong> paramètre clientos </strong> dans la requête, seuls les packages qui ont été séquencés pour prendre en charge tout système d’exploitation apparaissent dans les métadonnées.</p></td>
</tr>
</tbody>
</table>



Pour obtenir une syntaxe et des exemples de cette requête, consultez [affichage des métadonnées de publication d’App-V Server](viewing-app-v-server-publishing-metadata.md).

## <a href="" id="bkmk-event-logs-moved"></a>Les journaux des événements App-V ont été consolidés


Les journaux d’événements suivants, précédemment situés dans **les journaux d’application et de service journaux/Microsoft/AppV/ &lt; App-V &gt; **, ont été déplacés vers **journaux des applications et services/Microsoft/AppV/ServiceLog**.

Pour afficher les journaux, sélectionnez **affichage** &gt; **afficher les journaux d’analyse et de débogage** dans l’application Observateur d’événements.

Client-client de catalogue-client d’intégration-client de catalogue-client d’orchestration-client-PackageConfig-client-client-service client-Vemgr-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary de sous-systèmes-sous-systèmes-appPath-FTA

## Obtention de technologies MDOP


App-V est un composant du pack d’optimisation du bureau Microsoft (MDOP). MDOP fait partie de Microsoft Software Assurance. Pour plus d’informations sur l’utilisation de Microsoft Software Assurance et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).






## Rubriques connexes


[Notes de publication pour App-V5.0 SP3](release-notes-for-app-v-50-sp3.md)









