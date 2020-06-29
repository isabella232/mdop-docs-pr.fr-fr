---
title: Composants requis d'App-V5.0
description: Composants requis d'App-V5.0
author: dansimp
ms.assetid: 9756b571-c785-4ce6-a95c-d4e134e89429
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 176c9729d8c909325c6d6694e024938d9ce9df53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806007"
---
# Composants requis d'App-V5.0

Avant de commencer l’installation de Microsoft Application Virtualization (App-V) 5,0, assurez-vous d’avoir rempli les conditions préalables à l’installation du produit. Cette rubrique contient des informations pour vous aider à préparer votre environnement informatique avant de déployer les fonctionnalités de l’application-V 5,0.

> [!Important]
> **Les conditions préalables à cet article s’appliquent uniquement à l’App-V 5,0**. Pour obtenir d’autres conditions préalables applicables aux service packs App-V 5,0, consultez les pages Web suivantes:

-   [Nouveautés dans App-V5.0 SP1](whats-new-in-app-v-50-sp1.md)

-   [À propos d'App-V5.0 SP2](about-app-v-50-sp2.md)

-   [Composants requis d'App-V5.0 SP3](app-v-50-sp3-prerequisites.md)

Le tableau suivant répertorie les informations prérequises relatives aux systèmes d’exploitation spécifiques.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Systèmes d’exploitation</th>
<th align="left">Description requise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ordinateurs en cours d’exécution:</p>
<ul>
<li><p>Windows8</p></li>
<li><p>Windows Server2012</p></li>
</ul></td>
<td align="left"><p>Les conditions préalables suivantes sont déjà installées:</p>
<ul>
<li><p>Microsoft .NET Framework 4,5 – vous n’avez pas besoin de Microsoft .NET Framework 4</p></li>
<li><p>Windows PowerShell 3,0</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Ordinateurs en cours d’exécution:</p>
<ul>
<li><p>Windows7</p></li>
<li><p>WindowsServer2008</p></li>
</ul></td>
<td align="left"><p>Vous pouvez télécharger la base de connaissances suivante:</p>
<p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[Microsoft Security Advisory: Insecure library loading could allow remote code execution](https://support.microsoft.com/kb/2533623)">Avis de sécurité Microsoft: le chargement de la bibliothèque insécurisée peut permettre l’exécution du code distant</a></p>
<p>Assurez-vous de rechercher les Ko suivants qui ont été remplacés par le reste, et notez que certaines de nos Ko peuvent nécessiter la désinstallation des mises à jour précédentes.</p></td>
</tr>
</tbody>
</table>

## Conditions préalables à l’installation de App-V 5,0

> [!Note]  
> Les composants requis suivants sont déjà installés sur les ordinateurs exécutant Windows 8.

Chacune des fonctionnalités de 5,0 App-V comporte des éléments requis spécifiques qui doivent être satisfaits pour que les fonctionnalités de l’application-V 5,0 puissent être installées correctement.

### Conditions préalables pour le client App-V 5,0

Le tableau suivant répertorie les conditions préalables à l’installation du client App-V 5,0:

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
<td align="left"><p><strong>Configuration logicielle requise</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (package complet)</p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p>
<div class="alert">
<strong>Remarque</strong><br/><p>L’installation de PowerShell 3,0 nécessite un redémarrage.</p>
</div>
<div>

</div></li>
<li><p>Télécharger et installer <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Important</strong><br/><p>Vous pouvez télécharger et installer l’article de la base de connaissances précédent. Toutefois, il a pu avoir été remplacé par une version plus récente.</p>
</div>
<div>

</div></li>
<li><p>Le programme d’installation du client (. exe) détecte s’il est nécessaire d’installer les conditions préalables suivantes:</p>
<p></p>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Packages redistribuables Visual C++ pour Visual Studio 2013</a></p>
<p>Cette condition préalable n’est nécessaire que si vous avez installé le package de correctif logiciel 4 pour la virtualisation des applications 5,0 SP2 ou version ultérieure.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=26999" data-raw-source="[The Microsoft Visual C++ 2010 Redistributable](https://www.microsoft.com/download/details.aspx?id=26999)">Microsoft Visual C++ 2010 redistribuable</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=5638" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://www.microsoft.com/download/details.aspx?id=5638)">Package redistribuable Microsoft Visual C++ 2005 SP1 (x86)</a></p></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

### Conditions préalables pour le client App-V 5,0 Bureau à distance

> [!Note]  
> Les composants requis suivants sont déjà installés sur les ordinateurs exécutant Windows Server 2012.

Le tableau suivant répertorie les conditions préalables à l’installation du client App-V 5,0 Bureau à distance:

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
<td align="left"><p><strong>Configuration logicielle requise</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft.NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft.NET Framework 4 (package complet)</a></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p>
<div class="alert">
<strong>Remarque</strong><br/><p>L’installation de PowerShell 3,0 nécessite un redémarrage.</p>
</div>
<div>

</div></li>
<li><p>Télécharger et installer <a href="https://go.microsoft.com/fwlink/?LinkId=286102" data-raw-source="[KB2533623](https://go.microsoft.com/fwlink/?LinkId=286102 )"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Important</strong><br/><p>Vous pouvez télécharger et installer l’article de la base de connaissances précédent. Toutefois, il a pu avoir été remplacé par une version plus récente.</p>
</div>
<div>

</div></li>
<li><p>Le programme d’installation du client (. exe) détecte s’il est nécessaire d’installer les conditions préalables suivantes:</p>
<p></p>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Packages redistribuables Visual C++ pour Visual Studio 2013</a></p>
<p>Cette condition préalable n’est nécessaire que si vous avez installé le package de correctif logiciel 4 pour la virtualisation des applications 5,0 SP2 ou version ultérieure.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=26999" data-raw-source="[The Microsoft Visual C++ 2010 Redistributable](https://www.microsoft.com/download/details.aspx?id=26999)">Microsoft Visual C++ 2010 redistribuable</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=5638" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://www.microsoft.com/download/details.aspx?id=5638)">Package redistribuable Microsoft Visual C++ 2005 SP1 (x86)</a></p></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

### Conditions préalables pour le Sequencer App-V 5,0

> [!Note]
> Les composants requis suivants sont déjà installés sur les ordinateurs exécutant Windows 8 et Windows Server 2012.

Le tableau suivant répertorie les conditions préalables à l’installation pour le Sequencer App-V 5,0. Dans la mesure du possible, l’ordinateur qui exécute le Sequencer doit avoir les mêmes configurations matérielle et logicielle que les ordinateurs exécutant les applications virtuelles.

> [!Note]  
> Si la configuration système requise pour une application installée localement dépasse les exigences du Sequencer, vous devez respecter les exigences de cette application. Par ailleurs, dans la mesure où le processus de séquençage exige une ressources système plus gourmandes en ressources, il est recommandé que l’ordinateur qui exécute le Sequencer dispose de suffisamment de mémoire, d’un processeur rapide et d’un disque dur rapide. Pour plus d’informations, voir [Configurations prises en charge par App-V 5,0](app-v-50-supported-configurations.md).

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
<td align="left"><p><strong>Configuration logicielle requise</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Packages redistribuables Visual C++ pour Visual Studio 2013</a></p>
<p>Cette condition préalable n’est nécessaire que si vous avez installé le package de correctif logiciel 4 pour le SP2 application 5,0.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (package complet)</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></li>
<li><p>Télécharger et installer <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p></li>
<li><p>Pour les ordinateurs exécutant Microsoft Windows Server 2008 R2 SP1, téléchargez et installez <a href="https://go.microsoft.com/fwlink/?LinkId=286102" data-raw-source="[KB2533623](https://go.microsoft.com/fwlink/?LinkId=286102 )"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Important</strong><br/><p>Vous pouvez télécharger et installer l’un des Articles de la base de connaissances précédents. Toutefois, ils peuvent avoir été remplacés par une version plus récente.</p>
</div>
<div>

</div></li>
</ul></td>
</tr>
</tbody>
</table>

### Conditions préalables pour le serveur App-V 5,0

> [!Note]
> Les composants requis suivants sont déjà installés pour les ordinateurs exécutant Windows Server 2012:

-   Microsoft .NET Framework 4,5. Cela élimine la configuration requise pour Microsoft .NET Framework 4.

-   Windows PowerShell 3,0

-   Télécharger et installer [KB2533623](https://support.microsoft.com/kb/2533623) (https://support.microsoft.com/kb/2533623)

    > [!Important]
    > Vous pouvez toujours télécharger la version antérieure de la base de connaissances. Toutefois, il a pu avoir été remplacé par une version plus récente.

Le tableau suivant répertorie les conditions préalables à l’installation du serveur App-V 5,0. Le compte que vous utilisez pour installer les composants serveur doit disposer de droits d’administrateur sur l’ordinateur sur lequel vous procédez à l’installation. Ce compte doit également être en mesure d’interroger les services d’annuaire Active Directory. Avant d’installer et de configurer les serveurs App-V 5,0, vous devez spécifier un port sur lequel chaque composant sera hébergé. Vous devez également ajouter les règles de pare-feu associées pour autoriser les demandes entrantes sur les ports spécifiés.

> [!Note]
> WebDAV (Web Distributed Authoring and Versioning) est automatiquement désactivé pour le service de gestion.

Le serveur App-V 5,0 est pris en charge pour un déploiement autonome, où tous les composants sont déployés sur le même serveur et un déploiement distribué. Selon la topologie que vous utilisez pour déployer le serveur App-V 5,0, les données nécessaires pour chaque composant seront légèrement modifiées.

> [!Important]
> L’installation du serveur App-V 5,0 sur un ordinateur qui exécute une version ou un composant antérieur de App-V n’est pas prise en charge. Par ailleurs, l’installation des composants serveur sur un ordinateur qui exécute Server Core ou un contrôleur de domaine n’est pas non plus prise en charge.

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
<td align="left"><p><strong>Serveur de gestion</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (package complet)</a></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<div class="alert">
<strong>Remarque</strong><br/><p>L’installation de PowerShell 3,0 nécessite un redémarrage.</p>
</div>
<div>

</div></li>
<li><p>Windows Web Server avec le rôle IIS activé, ainsi que les fonctionnalités suivantes: <strong> fonctionnalités http communes </strong> (contenu statique et document par défaut), <strong> développement d’application </strong> (ASP.net, extensibilité .net, extensions ISAPI et filtres ISAPI), <strong> sécurité </strong> (authentification Windows, filtrage de requête), <strong> outils </strong> de gestion (IIS Management Console).</p></li>
<li><p>Télécharger et installer <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Important</strong><br/><p>Vous pouvez toujours télécharger la version antérieure de la base de connaissances. Toutefois, il a pu avoir été remplacé par une version plus récente.</p>
</div>
<div>

</div></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=13523" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x64)](https://www.microsoft.com/download/details.aspx?id=13523)">Package redistribuable Microsoft Visual C++ 2010 SP1 (x64)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Package redistribuable Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
<li><p>64 ASP.NET.</p></li>
</ul>
<p>Les composants serveur App-V 5,0 sont dépendants, mais ils présentent des exigences différentes et des options d’installation qui doivent être déployées. Utilisez les informations suivantes pour préparer votre environnement pour l’exécution du serveur de gestion App-V 5,0.</p>
<ul>
<li><p>Emplacement d’installation-par défaut ce composant sera installé sur: <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Emplacement de la base de données de gestion App-V 5,0-nom SQL Server, nom de l’instance SQL, nom de la base de données.</p></li>
<li><p>Droits d’accès pour la console de gestion App-V 5,0-il s’agit de l’utilisateur ou du groupe qui doit être autorisé à accéder à la console de gestion à la fin du déploiement. Après le déploiement, seuls ces utilisateurs ont accès à la console de gestion tant qu’il n’y a pas d’administrateurs supplémentaires par le biais de la console de gestion.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Les groupes de sécurité et les utilisateurs uniques ne sont pas pris en charge. Vous devez spécifier un groupe AD DS.</p>
</div>
<div>

</div></li>
<li><p>Nom du site Web du service de gestion de l’application V 5,0: attribuez un nom au site Web ou utilisez le nom par défaut.</p></li>
<li><p>Liaison de port de service de gestion de l’application V 5,0-il s’agit d’un numéro de port unique qui n’est pas utilisé par un autre site Web sur l’ordinateur.</p></li>
<li><p>La prise en charge de Microsoft Silverlight – Microsoft Silverlight doit être installé avant que la console de gestion ne soit disponible. Même si ce n’est pas une obligation pour le déploiement, le serveur doit être en mesure de prendre en charge Microsoft Silverlight.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Base de données de gestion</strong></p></td>
<td align="left"><p></p>
<div class="alert">
<strong>Remarque</strong><br/><p>La base de données est requise uniquement lors de l’utilisation du serveur de gestion App-V 5,0.</p>
</div>
<div>

</div>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (package complet)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Package redistribuable Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
</ul>
<p>Les composants serveur App-V 5,0 sont dépendants, mais ils présentent des exigences différentes et des options d’installation qui doivent être déployées. Utilisez les informations suivantes pour préparer votre environnement pour l’exécution de la base de données de gestion App-V 5,0.</p>
<ul>
<li><p>Emplacement d’installation-par défaut ce composant sera installé sur <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Nom d’instance SQL Server personnalisé (le cas échéant) – le format doit être <strong> InstanceName </strong> , car l’installation suppose qu’il se trouve sur l’ordinateur local. Si vous spécifiez le nom avec le format suivant, <strong> SVR\INSTANCE </strong> ne fonctionnera pas.</p></li>
<li><p>Nom de la base de données App-V 5,0 personnalisée (le cas échéant) – vous devez spécifier un nom de base de données unique. La valeur par défaut de la base de données de gestion est <strong> AppVManagement </strong> .</p></li>
<li><p>App-V 5,0 Management Server Location: spécifie le compte d’ordinateur sur lequel est déployé le serveur de gestion. Ce paramètre doit être spécifié au format <strong> Domain\MachineAccount suivant </strong> .</p></li>
<li><p>App-V 5,0 Management Server installation administrateur-spécifie le compte qui sera utilisé pour installer le serveur de gestion App-V 5,0. Utilisez le format suivant: <strong> Domain\AdministratorLoginName </strong> .</p></li>
<li><p>Agent de service Microsoft SQL Server-configurez l’ordinateur exécutant la base de données de gestion App-V 5,0 de sorte que le service Microsoft SQL Server agent soit redémarré automatiquement. Pour plus d’informations, voir <a href="https://go.microsoft.com/fwlink/?LinkId=273725" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://go.microsoft.com/fwlink/?LinkId=273725)"> configurer SQL Server Agent pour redémarrer les services automatiquement</a></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Serveur de création de rapports</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (package complet)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Package redistribuable Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
<li><div class="alert">
<strong>Remarque</strong><br/><p>Pour vous aider à réduire le risque de transfert de données indésirables ou malveillantes sur le serveur de création de rapports, vous devez limiter l’accès au service Web de création de rapports par votre stratégie de sécurité d’entreprise.</p>
</div>
<div>

</div>
<p>Serveur Web Windows doté du rôle IIS avec les fonctionnalités suivantes: <strong> fonctionnalités http communes </strong> (contenu statique et document par défaut), <strong> développement d’application </strong> (ASP.net, extensibilité .net, extensions ISAPI et filtres ISAPI), <strong> sécurité (authentification Windows, filtrage de requête), sécurité (authentification </strong> <strong> </strong> Windows, filtrage de requête), <strong> outils </strong> de gestion (console de gestion IIS)</p></li>
<li><p>64 ASP.NET.</p></li>
<li><p>Emplacement d’installation-par défaut ce composant est installé sur <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Nom du site Web de service de création de rapports App-V 5,0: spécifie le nom du site Web ou le nom par défaut qui sera utilisé.</p></li>
<li><p>Liaison de port de service App-V 5,0: il s’agit d’un numéro de port unique qui n’est pas déjà utilisé par un autre site Web qui s’exécute sur l’ordinateur.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Base de données de création de rapports</strong></p></td>
<td align="left"><p></p>
<div class="alert">
<strong>Remarque</strong><br/><p>La base de données est requise uniquement lors de l’utilisation du serveur de création de rapports App-V 5,0.</p>
</div>
<div>

</div>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (package complet)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Package redistribuable Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
</ul>
<p>Les composants serveur App-V 5,0 sont dépendants, mais ils présentent des exigences différentes et des options d’installation qui doivent être déployées. Utilisez les informations suivantes pour préparer votre environnement pour l’exécution de la base de données de création de rapports App-V 5,0.</p>
<ul>
<li><p>Emplacement d’installation-par défaut ce composant sera installé sur <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>Nom d’instance SQL Server personnalisé (le cas échéant) – le format doit être <strong> InstanceName </strong> , car l’installation suppose qu’il se trouve sur l’ordinateur local. Si vous spécifiez le nom avec le format suivant, <strong> SVR\INSTANCE </strong> ne fonctionnera pas.</p></li>
<li><p>Nom de la base de données App-V 5,0 personnalisée (le cas échéant) – vous devez spécifier un nom de base de données unique. La valeur par défaut de la base de données de création de rapports est <strong> AppVReporting </strong> .</p></li>
<li><p>Emplacement du serveur de création de rapports App-V 5,0: spécifie le compte d’ordinateur sur lequel est déployé le serveur de rapports. Ce paramètre doit être spécifié au format <strong> Domain\MachineAccount suivant </strong> .</p></li>
<li><p>Application-V 5,0 Reporting Server installation-spécifie le compte à utiliser pour installer le serveur de création de rapports App-V 5,0. Utilisez le format suivant: <strong> Domain\AdministratorLoginName </strong> .</p></li>
<li><p>Service Microsoft SQL Server et service Microsoft SQL Server Agent: ces services doivent être associés à des comptes d’utilisateurs qui ont accès à la publicité de requête.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Serveur de publication</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (package complet)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Package redistribuable Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
<li><p>Serveur Web Windows doté du rôle IIS avec les fonctionnalités suivantes: <strong> fonctionnalités http communes </strong> (contenu statique et document par défaut), <strong> développement d’application </strong> (ASP.net, extensibilité .net, extensions ISAPI et filtres ISAPI), <strong> sécurité (authentification Windows, filtrage de requête), sécurité (authentification </strong> <strong> </strong> Windows, filtrage de requête), <strong> outils </strong> de gestion (console de gestion IIS)</p></li>
<li><p>64 ASP.NET.</p></li>
</ul>
<p>Les composants serveur App-V 5,0 sont dépendants, mais ils présentent des exigences différentes et des options d’installation qui doivent être déployées. Utilisez les informations suivantes pour préparer votre environnement pour l’exécution du serveur de publication App-V 5,0.</p>
<ul>
<li><p>Emplacement d’installation-par défaut ce composant est installé sur <strong> %ProgramFiles%\Microsoft Application Virtualization Server </strong> .</p></li>
<li><p>URL du service de gestion App-V 5,0 – spécifie l’URL du service de gestion App-V 5,0. Il s’agit du port utilisé par le serveur de publication et il doit être spécifié en utilisant le format suivant: <strong><a href="http://localhost:12345" data-raw-source="http://localhost:12345"> http://localhost:12345 </a></strong> .</p></li>
<li><p>Nom du site Web du service de publication App-V 5,0 – spécifie le nom du site Web ou le nom par défaut qui sera utilisé.</p></li>
<li><p>Liaison de port de service d’application V 5,0-il s’agit d’un numéro de port unique qui n’est pas déjà utilisé par un autre site Web qui s’exécute sur l’ordinateur.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Rubriques connexes

[Envisager de déployer App-V](planning-to-deploy-app-v.md)

[Configurations prises en charge d'App-V5.0](app-v-50-supported-configurations.md)
