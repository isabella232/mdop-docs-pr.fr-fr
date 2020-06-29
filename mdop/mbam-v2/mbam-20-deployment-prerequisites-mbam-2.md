---
title: Conditions préalables au déploiement de MBAM2.0
description: Conditions préalables au déploiement de MBAM2.0
author: dansimp
ms.assetid: 57d1c2bb-5ea3-457e-badd-dd9206ff0f20
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ef7ee64a3661009f18e0963d738c57a59885cb20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811501"
---
# Conditions préalables au déploiement de MBAM2.0


Avant de démarrer le programme d’installation de Microsoft BitLocker (MBAM), vous devez vérifier que vous remplissez les conditions préalables à l’installation du produit. Cette section contient des informations pour vous aider à planifier votre environnement informatique avant de déployer Microsoft BitLocker administration et de surveiller les fonctionnalités et clients du serveur. Si vous installez MBAM avec Configuration Manager, reportez-vous à la section [planification du déploiement d’MBAM avec Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) pour obtenir d’autres conditions préalables.

## Conditions préalables à l’installation pour les fonctionnalités du serveur MBAM


Chacune des fonctionnalités du serveur MBAM comporte des éléments requis spécifiques qui doivent être satisfaits pour que les fonctionnalités MBAM puissent être installées avec succès. Le programme d’installation de MBAM vérifie que toutes les conditions préalables sont remplies avant le démarrage de l’installation.

### Conditions préalables pour le serveur d’administration et de surveillance

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
<td align="left"><p><strong>Rôle du serveur Web Windows Server</strong></p></td>
<td align="left"><p>Ce rôle doit être ajouté à un système d’exploitation serveur pris en charge pour la fonctionnalité d’administration et de surveillance du serveur.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Outils de gestion du serveur Web (IIS)</strong></p></td>
<td align="left"><p>Sélectionnez <strong> scripts et outils de gestion IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Certificat SSL</strong></p></td>
<td align="left"><p>Facultatif. Pour sécuriser les communications entre les clients et les services Web, vous devez obtenir et installer un certificat signé par une autorité de sécurité approuvée.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Services de rôle de serveur Web</strong></p></td>
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
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Fonctionnalités de Windows Server</strong></p></td>
<td align="left"><p><strong>Fonctionnalités de .NET Framework 3.5.1:</strong></p>
<ul>
<li><p>.NET Framework 3.5.1</p></li>
<li><p>Activation WCF</p>
<ul>
<li><p>Activation HTTP</p></li>
<li><p>Activation non HTTP</p></li>
</ul></li>
</ul>
<p><strong>Service d’activation de processus Windows:</strong></p>
<ul>
<li><p>Modèle de processus</p></li>
<li><p>Environnement .NET</p></li>
<li><p>API de configuration</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Remarque**  
Pour obtenir la liste des systèmes d’exploitation pris en charge, voir [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).



### Conditions préalables pour les rapports de conformité et d’audit

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
<td align="left"><p>Version prise en charge de SQL Server</p>
<p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,0.</p></td>
<td align="left"><p>Installez SQL Server avec:</p>
<ul>
<li><p>Assemblage SQL_Latin1_General_CP1_CI_AS</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server Reporting Services (SSRS)</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Droits d’instance SSRS: requis pour l’installation de rapports uniquement si vous installez des bases de données sur un serveur distinct des rapports.</p></td>
<td align="left"><p>Droits d’instance requis:</p>
<ul>
<li><p>Créer des dossiers</p></li>
<li><p>Publier des rapports</p></li>
</ul>
<p>SSRS doit être installé et exécuté lors de l’installation de MBAM Server. Configurez le mode «natif» dans le mode «natif» et non le mode «SharePoint» non configuré.</p></td>
</tr>
</tbody>
</table>



### Conditions préalables pour la base de données de récupération

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
<td align="left"><p>Version prise en charge de SQL Server</p>
<p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,0.</p></td>
<td align="left"><p>Installez SQL Server avec:</p>
<ul>
<li><p>Assemblage SQL_Latin1_General_CP1_CI_AS</p></li>
<li><p>Outils de gestion SQL Server</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Autorisations SQL Server requises</p></td>
<td align="left"><p>Autorisations requises:</p>
<ul>
<li><p>Rôles de serveurs de connexion d’instances SQL:</p>
<ul>
<li><p>rôles</p></li>
<li><p>processadmin</p></li>
</ul></li>
<li><p>Droits d’instance de SQL Server Reporting Services:</p>
<ul>
<li><p>Créer des dossiers</p></li>
<li><p>Publier des rapports</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Fonctionnalité facultative-installation du chiffrement de données (TDE) en option disponible dans SQL Server</p></td>
<td align="left"><p>La TDE SQL Server vous permet de chiffrer et de déchiffrer les données et les fichiers journaux en temps réel, ce qui peut vous aider à vous conformer à de nombreux lois, règlements et directives établis dans divers secteurs d’utilisation.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>TDE exécute le déchiffrement en temps réel des informations de la base de données, ce qui signifie que si le compte sous lequel vous vous êtes connecté dispose de l’autorisation de la base de données pendant que vous consultez les informations de la clé de récupération dans les tables SQL Server, les informations de la clé de récupération sont affichées.</p>
</div>
<div>

</div>
<p>En savoir plus sur TDE: MBAM des considérations en matière de <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> sécurité 2,0 </a> .</p></td>
</tr>
</tbody>
</table>



### Conditions préalables pour la base de données d’audit et de conformité

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
<td align="left"><p>Version prise en charge de SQL Server</p>
<p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,0.</p></td>
<td align="left"><p>Installez SQL Server avec:</p>
<ul>
<li><p>Assemblage SQL_Latin1_General_CP1_CI_AS</p></li>
<li><p>Outils de gestion SQL Server</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Autorisations SQL Server requises</p></td>
<td align="left"><p>Autorisations requises:</p>
<ul>
<li><p>Rôles de serveurs de connexion d’instances SQL:</p>
<ul>
<li><p>rôles</p></li>
<li><p>processadmin</p></li>
</ul></li>
<li><p>Droits d’instance de SQL Server Reporting Services:</p>
<ul>
<li><p>Créer des dossiers</p></li>
<li><p>Publier des rapports</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Fonctionnalité facultative d’installation du chiffrement de données (TDE) dans SQL Server.</p></td>
<td align="left"><p>La TDE SQL Server vous permet de chiffrer et de déchiffrer les données et les fichiers journaux en temps réel, ce qui peut vous aider à vous conformer à de nombreux lois, règlements et directives établis dans divers secteurs d’utilisation.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>TDE exécute le déchiffrement en temps réel des informations de la base de données, ce qui signifie que si le compte sous lequel vous vous êtes connecté dispose de l’autorisation de la base de données pendant que vous consultez les informations de la clé de récupération dans les tables SQL Server, les informations de la clé de récupération sont affichées.</p>
</div>
<div>

</div>
<p>En savoir plus sur TDE: MBAM des considérations en matière de <a href="mbam-20-security-considerations-mbam-2.md" data-raw-source="[MBAM 2.0 Security Considerations](mbam-20-security-considerations-mbam-2.md)"> sécurité 2,0</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Les services du moteur de base de données SQL Server doivent être installés et exécutés lors de l’installation de MBAM Server.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Le service de l’agent SQL Server doit être en cours d’exécution et configuré pour démarrer automatiquement sur les instances sélectionnées de SQL Server.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Conditions préalables pour le portail libre-service

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
<td align="left"><p>Version prise en charge de Windows Server</p>
<p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,0.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 2,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392270" data-raw-source="[ASP.NET MVC 2 download](https://go.microsoft.com/fwlink/?LinkId=392270)">Télécharger ASP.NET MVC 2</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Outils de gestion IIS de service Web</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Conditions préalables pour les clients MBAM


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
<td align="left"><p><strong>Les clients Windows 7 </strong> - doivent disposer d’une fonctionnalité de module de plateforme sécurisée (TPM) uniquement.</p></td>
<td align="left"><p>La version du module de plateforme sécurisée doit être 1,2 ou une version ultérieure.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Le processeur du TPM doit être activé dans le BIOS et être Resettable du système d’exploitation.</p></td>
<td align="left"><p>Pour plus d’informations, consultez la documentation relative au BIOS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Clients Windows 8 uniquement </strong> : pour permettre à MBAM de stocker et de gérer les clés de récupération du module de plateforme sécurisée: la mise en service automatique du module de plateforme sécurisée doit être désactivée, et MBAM doit être défini en tant que propriétaire du TPM avant le déploiement d’MBAM. Pour désactiver la mise en service automatique du module de plateforme sécurisée, voir <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</p>
<ul>
<li><p>La mise en service automatique du module de plateforme sécurisée doit être désactivée.</p></li>
<li><p>MBAM doit être défini en tant que propriétaire du TPM avant le déploiement d’MBAM.</p></li>
</ul></td>
<td align="left"><p>Pour désactiver la mise en service automatique du module de plateforme sécurisée, voir <a href="https://go.microsoft.com/fwlink/?LinkId=286468" data-raw-source="[Disable-TpmAutoProvisioning](https://go.microsoft.com/fwlink/?LinkId=286468)"> Disable-TpmAutoProvisioning </a> .</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Assurez-vous que le clavier, la vidéo ou la souris sont directement connectés et ne sont pas gérés par le biais d’un clavier, d’une vidéo ou d’un commutateur de souris (KVM). Un commutateur KVM peut interférer avec la capacité de l’ordinateur à détecter la présence physique du matériel.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Rubriques connexes


[Planification du déploiement de MBAM2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Configurations prises en charge par MBAM2.0](mbam-20-supported-configurations-mbam-2.md)









