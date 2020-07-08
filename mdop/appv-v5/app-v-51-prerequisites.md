---
title: Composants requis d'App-V5.1
description: Composants requis d'App-V5.1
author: dansimp
ms.assetid: 1bfa03c1-a4ae-45ec-8a2b-b10c2b94bfb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a74d8f8d7148cdb6c32bcafa87f479d24305af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805953"
---
# Composants requis d'App-V5.1


Avant l’installation de Microsoft Application Virtualization (App-V) 5,1, assurez-vous d’avoir installé tous les logiciels requis suivants.

Pour obtenir la liste des systèmes d’exploitation pris en charge et la configuration matérielle requise pour le serveur App-V, le Sequencer et le client, voir [configurations App-v 5,1 prises en charge](app-v-51-supported-configurations.md).

## Résumé de logiciels préinstallés sur chaque système d’exploitation


Le tableau suivant indique les logiciels déjà installés pour différents systèmes d’exploitation.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Système d’exploitation</th>
<th align="left">Description requise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Tous les logiciels requis sont déjà installés.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Tous les logiciels requis sont déjà installés.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si vous exécutez Windows 8, effectuez une mise à niveau vers Windows 8,1 avant d’utiliser App-V 5,1.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012</p></td>
<td align="left"><p>Les logiciels requis suivants sont déjà installés:</p>
<ul>
<li><p>Microsoft .NET Framework 4,5</p></li>
<li><p>Windows PowerShell 3,0</p>
<div class="alert">
<strong>Remarque</strong><br/><p>L’installation de PowerShell 3,0 nécessite un redémarrage.</p>
</div>
<div>

</div></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Le logiciel requis n’est pas déjà installé. Pour pouvoir installer App-V, vous devez l’installer.</p></td>
</tr>
</tbody>
</table>



## Logiciels requis pour App-V Server


Installez les logiciels prérequis requis pour les composants serveur App-V 5,1.

### Ce que vous devez savoir avant de commencer

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Compte pour l’installation de l’App-V Server</p></td>
<td align="left"><p>Le compte que vous utilisez pour installer les composants du serveur App-V doit avoir:</p>
<ul>
<li><p>Des droits d’administrateur sur l’ordinateur sur lequel vous installez les composants.</p></li>
<li><p>La possibilité d’interroger les services de domaine Active Directory.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Port et pare-feu</p></td>
<td align="left"><ul>
<li><p>Spécifiez un port sur lequel chaque composant sera hébergé.</p></li>
<li><p>Ajoutez les règles de pare-feu associées pour autoriser les demandes entrantes sur les ports spécifiés.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>WebDAV (Web Distributed Authoring and Versioning)</p></td>
<td align="left"><p>WebDAV est automatiquement désactivé pour le service de gestion.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scénarios de déploiement pris en charge</p></td>
<td align="left"><ul>
<li><p>Un déploiement autonome, dans lequel tous les composants sont déployés sur le même serveur.</p></li>
<li><p>Un déploiement distribué.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Scénarios de déploiement non pris en charge</p></td>
<td align="left"><ul>
<li><p>Installation d’instances côte à côte de plusieurs versions serveur App-V sur le même serveur.</p></li>
<li><p>Installation des composants App-V Server sur un ordinateur qui exécute le serveur principal ou le contrôleur de domaine.</p></li>
</ul></td>
</tr>
</tbody>
</table>



### Logiciels requis par le serveur de gestion

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Conditions préalables et configuration requise</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Version prise en charge de SQL Server</p></td>
<td align="left"><p>Pour les versions prises en charge, voir <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> configurations App-V 5,1 prises en charge </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p></td>
<td align="left"><p>L’installation de PowerShell 3,0 nécessite un redémarrage.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Télécharger et installer <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p></td>
<td align="left"><p>S’applique uniquement à Windows 7.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Packages redistribuables Visual C++ pour Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>64 ASP.NET.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Rôle du serveur Web Windows Server</p></td>
<td align="left"><p>Ce rôle doit être ajouté à un système d’exploitation serveur pris en charge pour le serveur de gestion.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Outils de gestion du serveur Web (IIS)</p></td>
<td align="left"><p>Cliquez sur <strong> scripts et outils de gestion IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Services de rôle de serveur Web</p></td>
<td align="left"><p><strong>Fonctionnalités HTTP communes:</strong></p>
<ul>
<li><p>Contenu statique</p></li>
<li><p>Document par défaut</p></li>
</ul>
<p><strong>Développement d’applications:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Extensibilité .NET</p></li>
<li><p>Extensions ISAPI</p></li>
<li><p>Filtres ISAPI</p></li>
</ul>
<p><strong>Sûreté</strong></p>
<ul>
<li><p>Authentification Windows</p></li>
<li><p>Filtrage de requête</p></li>
</ul>
<p><strong>Outils de gestion:</strong></p>
<ul>
<li><p>Console de gestion IIS</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Emplacement d’installation par défaut</p></td>
<td align="left"><p>Serveur de virtualisation des applications de%PROGRAMFILES%\Microsoft</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Emplacement de la base de données de gestion</p></td>
<td align="left"><p>Nom de la base de données SQL Server, nom de l’instance de base de données SQL Server et nom de la base de données.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Autorisations de la console de gestion et de la base de données de gestion</p></td>
<td align="left"><p>Un utilisateur ou un groupe qui peut accéder à la console de gestion et à la base de données une fois le déploiement terminé. Seuls les utilisateurs ou les groupes peuvent accéder à la console de gestion et à la base de données, sauf si d’autres administrateurs sont ajoutés à l’aide de la console de gestion.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nom du site Web du service de gestion</p></td>
<td align="left"><p>Nom du site Web de la console de gestion.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Liaison de port de service de gestion</p></td>
<td align="left"><p>Numéro de port unique pour le service de gestion. Ce port ne peut pas être utilisé par un autre processus sur l’ordinateur.</p></td>
</tr>
</tbody>
</table>



**Important**  
JavaScript doit être activé dans le navigateur qui ouvre la console de gestion Web.



### Logiciel requis pour la base de données du serveur de gestion

La base de données de gestion est requise uniquement si vous utilisez le serveur de gestion App-V 5,1.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Conditions préalables et configuration requise</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Packages redistribuables Visual C++ pour Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Emplacement d’installation par défaut</p></td>
<td align="left"><p>Serveur de virtualisation des applications de%PROGRAMFILES%\Microsoft</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nom d’instance SQL Server personnalisé (le cas échéant)</p></td>
<td align="left"><p>Format à utiliser: <strong> InstanceName</strong></p>
<p>Ce format repose sur l’hypothèse de l’installation sur l’ordinateur local.</p>
<p>Si vous spécifiez le nom avec le format <strong> SVR\INSTANCE </strong> , l’installation échoue.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nom de la base de données personnalisée (le cas échéant)</p></td>
<td align="left"><p>Nom unique de la base de données.</p>
<p>Par défaut: AppVManagement</p></td>
</tr>
<tr class="even">
<td align="left"><p>Emplacement du serveur de gestion</p></td>
<td align="left"><p>Compte d’ordinateur sur lequel est déployé le serveur de gestion.</p>
<p>Format à utiliser: Domain\MachineAccount</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administrateur d’installation du serveur de gestion</p></td>
<td align="left"><p>Compte utilisé pour installer le serveur de gestion.</p>
<p>Format à utiliser: Domain\AdministratorLoginName</p></td>
</tr>
<tr class="even">
<td align="left"><p>Agent de service Microsoft SQL Server</p></td>
<td align="left"><p>Configurez l’ordinateur de base de données de gestion de sorte que le service Microsoft SQL Server agent soit redémarré automatiquement. Pour obtenir des instructions, voir <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)"> configurer l’agent SQL Server pour redémarrer les services automatiquement </a> .</p></td>
</tr>
</tbody>
</table>



### Logiciel requis par le serveur de publication

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Conditions préalables et configuration requise</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Packages redistribuables Visual C++ pour Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>64 ASP.NET.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Rôle du serveur Web Windows Server</p></td>
<td align="left"><p>Ce rôle doit être ajouté à un système d’exploitation serveur pris en charge pour le serveur de gestion.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Outils de gestion du serveur Web (IIS)</p></td>
<td align="left"><p>Cliquez sur <strong> scripts et outils de gestion IIS </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Services de rôle de serveur Web</p></td>
<td align="left"><p><strong>Fonctionnalités HTTP communes:</strong></p>
<ul>
<li><p>Contenu statique</p></li>
<li><p>Document par défaut</p></li>
</ul>
<p><strong>Développement d’applications:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Extensibilité .NET</p></li>
<li><p>Extensions ISAPI</p></li>
<li><p>Filtres ISAPI</p></li>
</ul>
<p><strong>Sûreté</strong></p>
<ul>
<li><p>Authentification Windows</p></li>
<li><p>Filtrage de requête</p></li>
</ul>
<p><strong>Outils de gestion:</strong></p>
<ul>
<li><p>Console de gestion IIS</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Emplacement d’installation par défaut</p></td>
<td align="left"><p>Serveur de virtualisation des applications de%PROGRAMFILES%\Microsoft</p></td>
</tr>
<tr class="even">
<td align="left"><p>URL du service de gestion</p></td>
<td align="left"><p>URL du service de gestion App-V. Il s’agit du port sur lequel communiquer le serveur de publication.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Architecture d’installation</th>
<th align="left">Format à utiliser pour l’URL</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Serveur de gestion et serveur de publication installés sur le même serveur</p></td>
<td align="left"><p><a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Serveur de gestion et serveur de publication installés sur différents serveurs</p></td>
<td align="left"><p><a href="http://MyAppvServer.MyDomain.com" data-raw-source="http://MyAppvServer.MyDomain.com">http://MyAppvServer.MyDomain.com</a></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nom du site Web du service de publication</p></td>
<td align="left"><p>Nom du site Web de publication.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Liaison de port de service de publication</p></td>
<td align="left"><p>Numéro de port unique pour le service de publication. Ce port ne peut pas être utilisé par un autre processus sur l’ordinateur.</p></td>
</tr>
</tbody>
</table>



### Logiciels requis par le serveur de création de rapports

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Conditions préalables et configuration requise</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Version prise en charge de SQL Server</p></td>
<td align="left"><p>Pour les versions prises en charge, voir <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> configurations App-V 5,1 prises en charge </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Packages redistribuables Visual C++ pour Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>64 ASP.NET.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Rôle du serveur Web Windows Server</p></td>
<td align="left"><p>Ce rôle doit être ajouté à un système d’exploitation serveur pris en charge pour le serveur de gestion.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Outils de gestion du serveur Web (IIS)</p></td>
<td align="left"><p>Cliquez sur <strong> scripts et outils de gestion IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Services de rôle de serveur Web</p></td>
<td align="left"><p>Pour réduire le risque de transfert de données indésirables ou malveillantes sur le serveur de création de rapports, vous devez limiter l’accès au service Web de création de rapports par votre stratégie de sécurité d’entreprise.</p>
<p><strong>Fonctionnalités HTTP communes:</strong></p>
<ul>
<li><p>Contenu statique</p></li>
<li><p>Document par défaut</p></li>
</ul>
<p><strong>Développement d’applications:</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Extensibilité .NET</p></li>
<li><p>Extensions ISAPI</p></li>
<li><p>Filtres ISAPI</p></li>
</ul>
<p><strong>Sûreté</strong></p>
<ul>
<li><p>Authentification Windows</p></li>
<li><p>Filtrage de requête</p></li>
</ul>
<p><strong>Outils de gestion:</strong></p>
<ul>
<li><p>Console de gestion IIS</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Emplacement d’installation par défaut</p></td>
<td align="left"><p>Serveur de virtualisation des applications de%PROGRAMFILES%\Microsoft</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nom du site Web de service de création de rapports</p></td>
<td align="left"><p>Nom du site Web de création de rapports.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Liaison de port de service de création de rapports</p></td>
<td align="left"><p>Numéro de port unique pour le service de création de rapports. Ce port ne peut pas être utilisé par un autre processus sur l’ordinateur.</p></td>
</tr>
</tbody>
</table>



### Logiciel requis pour la création de rapports

La base de données de création de rapports est requise uniquement si vous utilisez le serveur de rapports App-V 5,1.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Conditions préalables et configuration requise</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Packages redistribuables Visual C++ pour Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Emplacement d’installation par défaut</p></td>
<td align="left"><p>Serveur de virtualisation des applications de%PROGRAMFILES%\Microsoft</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nom d’instance SQL Server personnalisé (le cas échéant)</p></td>
<td align="left"><p>Format à utiliser: <strong> InstanceName</strong></p>
<p>Ce format repose sur l’hypothèse de l’installation sur l’ordinateur local.</p>
<p>Si vous spécifiez le nom avec le format <strong> SVR\INSTANCE </strong> , l’installation échoue.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nom de la base de données personnalisée (le cas échéant)</p></td>
<td align="left"><p>Nom unique de la base de données.</p>
<p>Par défaut: AppVReporting</p></td>
</tr>
<tr class="even">
<td align="left"><p>Emplacement du serveur de création de rapports</p></td>
<td align="left"><p>Compte d’ordinateur sur lequel est déployé le serveur de rapports.</p>
<p>Format à utiliser: Domain\MachineAccount</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Administrateur d’installation du serveur de création de rapports</p></td>
<td align="left"><p>Compte utilisé pour installer le serveur de rapports.</p>
<p>Format à utiliser: Domain\AdministratorLoginName</p></td>
</tr>
<tr class="even">
<td align="left"><p>Service Microsoft SQL Server et agent de service Microsoft SQL Server</p></td>
<td align="left"><p>Configurez ces services à associer aux comptes d’utilisateurs qui ont accès à la requête AD DS.</p></td>
</tr>
</tbody>
</table>



## Logiciel requis pour les clients App-V


Installez les logiciels requis suivants pour le client App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prérequises</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></td>
<td align="left"><p>L’installation de PowerShell 3,0 nécessite un redémarrage.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>S’applique à Windows 7 uniquement: Télécharger et installer la Ko.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Packages redistribuables Visual C++ pour Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Logiciels requis du client de services Bureau à distance


Installez les logiciels requis suivants pour le client App-V Remote Desktop Services.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prérequises</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></td>
<td align="left"><p>L’installation de PowerShell 3,0 nécessite un redémarrage.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>S’applique à Windows 7 uniquement: Télécharger et installer la Ko.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Packages redistribuables Visual C++ pour Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Logiciels requis par le Sequencer


**Éléments à connaître avant d’installer la configuration requise:**

-   Meilleure pratique: l’ordinateur qui exécute le Sequencer doit présenter les mêmes configurations matérielle et logicielle que les ordinateurs exécutant les applications virtuelles.

-   Le processus de séquençage est gourmand en ressources; il est donc important de veiller à ce que l’ordinateur qui exécute le Sequencer dispose de suffisamment de mémoire, d’un processeur rapide et d’un disque dur rapide. La configuration requise pour les applications installées localement ne peut pas dépasser celle du Sequencer. Pour plus d’informations, voir [configurations App-V 5,1 prises en charge](app-v-51-supported-configurations.md).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prérequises</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (programme d’installation Web)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></td>
<td align="left"><p>L’installation de PowerShell 3,0 nécessite un redémarrage.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>S’applique à Windows 7 uniquement: Télécharger et installer la Ko.</p></td>
</tr>
</tbody>
</table>








## Rubriques connexes


[Planification d'App-V5.1](planning-for-app-v-51.md)

[Configurations prises en charge par App-V5.1](app-v-51-supported-configurations.md)









