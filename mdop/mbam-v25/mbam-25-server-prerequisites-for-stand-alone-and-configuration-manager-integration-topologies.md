---
title: Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome
description: Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome
author: dansimp
ms.assetid: 76a6047a-5c6e-42ff-af09-a6f382a69537
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9af551b1d867f61912bbf3b759574a840b0645c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811490"
---
# Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome


Avant de démarrer l’installation de l’administration et de la surveillance de BitLocker (MBAM) Microsoft, vous devez remplir les conditions préalables indiquées dans cette rubrique. Ces conditions préalables s’appliquent à la topologie autonome MBAM et System Center Configuration Manager.

Si vous déployez MBAM à l’aide de System Center Configuration Manager, vous devez renseigner des éléments requis supplémentaires, qui sont répertoriés dans [MBAM 2,5 Server Prerequisites qui ne s’appliquent qu’à la topologie d’intégration de Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).

Pour obtenir la liste des matériels et systèmes d’exploitation pris en charge pour MBAM, voir [Configurations prises en charge par MBAM 2,5](mbam-25-supported-configurations.md).

**Important**  
Si BitLocker a été utilisé sans MBAM, vous devez déchiffrer le lecteur puis effacer TPM à l’aide de TPM. msc. MBAM ne peut pas prendre la propriété de TPM si le PC client est déjà chiffré et que le mot de passe du propriétaire du TPM a été créé.



## Rôles et comptes MBAM requis


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
<td align="left"><p>Groupes créés dans les services de domaine Active Directory (AD DS)</p></td>
<td align="left"><p><a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)"> </a> Pour obtenir une description de ces groupes et comptes, voir Planification des groupes et comptes MBAM 2,5.</p></td>
</tr>
</tbody>
</table>



## Conditions préalables pour la base de données de récupération


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
<td align="left"><p>Version prise en charge de SQL Server</p></td>
<td align="left"><p>Installez Microsoft SQL Server avec SQL_Latin1_General_CP1_CI_AS collation.</p>
<p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,5.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Autorisations SQL Server requises</p></td>
<td align="left"><p>Autorisations requises:</p>
<ul>
<li><p>Rôles de serveurs de connexion d’instances SQL Server:</p>
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
<td align="left"><p>Facultatif: installation de la fonctionnalité de chiffrement de données (TDE) transparente disponible dans SQL Server</p></td>
<td align="left"><p>La TDE SQL Server vous permet de chiffrer et de déchiffrer les données et les fichiers journaux en temps réel, ce qui peut vous aider à vous conformer aux lois, réglementations et recommandations applicables à divers secteurs d’utilisation.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>TDE procède au déchiffrement en temps réel des informations de la base de données. Cela signifie que si vous affichez les informations de clé de récupération dans la base de données SQL Server et que vous êtes connecté sous un compte qui dispose des autorisations de la base de données, les informations de clé de récupération sont affichées. Pour en savoir plus sur TDE, reportez-vous à la section <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considérations relatives à la sécurité dans 2,5 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Services du moteur de base de données SQL Server</p></td>
<td align="left"><p>Les services du moteur de base de données SQL Server doivent être installés et exécutés lors de l’installation de MBAM Server.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell 3,0 ou version ultérieure</p></td>
<td align="left"><p>Il n’est pas nécessaire d’installer Windows PowerShell sur le serveur de base de données de récupération si vous utilisez Windows PowerShell pour configurer la base de données à partir d’un ordinateur distant.</p></td>
</tr>
</tbody>
</table>



## Conditions préalables pour la base de données d’audit et de conformité


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
<td align="left"><p>Version prise en charge de SQL Server</p></td>
<td align="left"><p>Installez SQL Server avec SQL_Latin1_General_CP1_CI_AS collation.</p>
<p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,5.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Autorisations SQL Server requises</p></td>
<td align="left"><p>Autorisations requises:</p>
<ul>
<li><p>Rôles de serveurs de connexion d’instances SQL Server:</p>
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
<td align="left"><p>Option facultative: installation de la fonctionnalité de chiffrement de données (TDE) transparente dans SQL Server</p></td>
<td align="left"><p>La TDE SQL Server vous permet de chiffrer et de déchiffrer les données et les fichiers journaux en temps réel, ce qui peut vous aider à vous conformer aux lois, réglementations et recommandations applicables à divers secteurs d’utilisation.</p>
<p>TDE procède au déchiffrement en temps réel des informations de la base de données. Cela signifie que si vous affichez les informations de clé de récupération dans la base de données SQL Server et que vous êtes connecté sous un compte qui dispose des autorisations de la base de données, les informations de clé de récupération sont affichées. Pour en savoir plus sur TDE, reportez-vous à la section <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considérations relatives à la sécurité dans 2,5 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Services du moteur de base de données SQL Server</p></td>
<td align="left"><p>Les services du moteur de base de données SQL Server doivent être installés et exécutés lors de l’installation de MBAM Server. Toutefois, SQL Server peut être exécuté à distance; Il n’est pas nécessaire de se trouver sur le même serveur sur lequel vous installez le logiciel serveur MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows PowerShell 3,0 ou version ultérieure</p></td>
<td align="left"><p>Pour configurer la base de données à partir d’un ordinateur distant, il n’est pas nécessaire d’installer Windows PowerShell sur le serveur de base de données de conformité et d’audit si vous utilisez Windows PowerShell.</p></td>
</tr>
</tbody>
</table>



## Conditions préalables pour les rapports


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
<td align="left"><p>Version prise en charge de SQL Server</p></td>
<td align="left"><p>Installez SQL Server avec SQL_Latin1_General_CP1_CI_AS collation.</p>
<p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,5.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SQL Server Reporting Services (SSRS)</p></td>
<td align="left"><p>SSRS doit être installé et exécuté lors de l’installation de MBAM Server.</p>
<p>Configurer SSRS en &quot; &quot; mode natif et non en mode non configuré ou &quot; SharePoint &quot; .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Droits d’instance SSRS: requis pour la configuration des rapports uniquement si vous installez des bases de données sur un serveur distinct du serveur sur lequel les rapports sont configurés.</p></td>
<td align="left"><p>Droits d’instance requis:</p>
<ul>
<li><p>Créer des dossiers</p></li>
<li><p>Publier des rapports</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows PowerShell 3,0 ou version ultérieure</p></td>
<td align="left"><p>Pour configurer la base de données à partir d’un ordinateur distant, il n’est pas nécessaire d’installer Windows PowerShell sur ce serveur de base de données si vous utilisez Windows PowerShell.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-prereqsams"></a>Conditions préalables pour le serveur d’administration et de surveillance


Le tableau suivant répertorie les conditions préalables à l’installation du serveur d’administration et de surveillance MBAM.

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
<td align="left"><p>Rôle du serveur Web Windows Server</p></td>
<td align="left"><p>Ce rôle doit être ajouté à un système d’exploitation serveur pris en charge pour la fonctionnalité d’administration et de surveillance du serveur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Outils de gestion du serveur Web (IIS)</p></td>
<td align="left"><p>Cliquez sur <strong> scripts et outils de gestion IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Certificat SSL</strong></p></td>
<td align="left"><p>Facultatif. Pour sécuriser les communications entre les ordinateurs client et les services Web, vous devez obtenir et installer un certificat qu’une autorité de sécurité fiable a signée.</p></td>
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
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Fonctionnalités de Windows Server</p></td>
<td align="left"><p><strong>Fonctionnalités de .NET Framework 4,5:</strong></p>
<ul>
<li><p><strong>.NET Framework 4,5 ou 4,6</strong></p>
<ul>
<li><p><strong>Windows Server 2016 </strong> - .net Framework 4,6 est déjà installé pour ces versions de Windows Server, mais vous devez l’activer.</p></li>  
<li><p><strong>Windows Server 2012 ou Windows Server 2012 R2 </strong> - .net Framework 4,5 est déjà installé pour ces versions de Windows Server, mais vous devez l’activer.</p></li>
<li><p><strong>Windows Server 2008 R2 </strong> - .net Framework 4,5 n’est pas inclus dans windows Server 2008 R2, vous devez donc <a href="https://go.microsoft.com/fwlink/?LinkId=392318" data-raw-source="[download Microsoft .NET Framework 4.5](https://go.microsoft.com/fwlink/?LinkId=392318)"> Télécharger Microsoft .NET Framework 4,5 </a> et l’installer séparément.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si vous effectuez une mise à niveau à partir de MBAM 2,0 ou MBAM 2,0 SP1 et que vous devez installer .NET Framework 4,5, voir <a href="release-notes-for-mbam-25.md" data-raw-source="[Release Notes for MBAM 2.5](release-notes-for-mbam-25.md)"> les notes de publication pour MBAM 2,5 </a> pour une étape supplémentaire requise pour le fonctionnement des sites Web.</p>
</div>
<div>

</div></li>
</ul></li>
<li><p><strong>Activation WCF</strong></p>
<ul>
<li><p>Activation HTTP</p></li>
<li><p>Activation non HTTP (uniquement pour Windows Server 2008, 2012 et 2012 R2)</p>
<p></p></li>
</ul></li>
<li><p><strong>Activation TCP</strong></p></li>
</ul>
<p><strong>Service d’activation de processus Windows:</strong></p>
<ul>
<li><p>Modèle de processus</p></li>
<li><p>Environnement .NET Framework</p></li>
<li><p>API de configuration</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 4,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)">Télécharger ASP.NET MVC 4</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nom de principal de service (SPN)</p></td>
<td align="left"><p>Les applications Web requièrent un SPN pour le nom d’hôte virtuel sous le compte de domaine que vous utilisez pour les pools d’applications Web.</p>
<p>Si vos droits d’administrateur vous permettent de créer des SPN dans les services de domaine Active Directory (AD FS), MBAM crée le SPN pour vous. Voir <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> setspn </a> pour plus d’informations sur les droits nécessaires à la création de SPN.</p>
<p>Si vous ne disposez pas des droits d’administration pour créer des SPN, vous devez demander à l’administrateur Active Directory de votre organisation de créer le SPN pour vous en utilisant la commande suivante.</p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p>Dans l’exemple de code, le nom d’hôte virtuel est mbamvirtual.contoso.com et le compte de domaine utilisé pour les pools d’applications Web est contoso\mbamapppooluser.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si vous configurez l’équilibrage de charge, utilisez le même compte de pool d’applications sur tous les serveurs.</p>
</div>
<div>

</div>
<p>Pour plus d’informations sur l’inscription de SPN pour les noms d’hôtes complets, NetBIOS et personnalisés, voir <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> planification de la sécurisation des sites Web MBAM </a> .</p></td>
</tr>
</tbody>
</table>



## Conditions préalables pour le portail libre-service


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
<td align="left"><p>Version prise en charge de Windows Server</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Pour plus d’MBAM, voir Configurations prises en charge </a> par les 2,5.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ASP.NET MVC 4,0</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=392271" data-raw-source="[ASP.NET MVC 4 download](https://go.microsoft.com/fwlink/?LinkId=392271)">Télécharger ASP.NET MVC 4</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Outils de gestion IIS de service Web</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Nom de principal de service (SPN)</p></td>
<td align="left"><p>Les applications Web requièrent un SPN pour le nom d’hôte virtuel sous le compte de domaine que vous utilisez pour les pools d’applications Web.</p>
<p>Si vos droits d’administrateur vous permettent de créer des SPN dans les services de domaine Active Directory (AD FS), MBAM crée le SPN pour vous. Voir <a href="https://technet.microsoft.com/library/cc731241.aspx" data-raw-source="[Setspn](https://technet.microsoft.com/library/cc731241.aspx)"> setspn </a> pour plus d’informations sur les droits nécessaires à la création de SPN.</p>
<p>Si vous ne disposez pas des droits d’administration pour créer des SPN, vous devez demander à l’administrateur Active Directory de votre organisation de créer le SPN pour vous en utilisant la commande suivante.</p>
<pre class="syntax" space="preserve"><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser
Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></pre>
<p>Dans l’exemple de code, le nom d’hôte virtuel est mbamvirtual.contoso.com et le compte de domaine utilisé pour les pools d’applications Web est contoso\mbamapppooluser.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si vous configurez l’équilibrage de charge, utilisez le même compte de pool d’applications sur tous les serveurs.</p>
</div>
<div>

</div>
<p>Pour plus d’informations sur l’inscription de SPN pour les noms d’hôtes complets, NetBIOS et personnalisés, voir <a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)"> planification de la sécurisation des sites Web MBAM </a> .</p></td>
</tr>
</tbody>
</table>



## Conditions préalables pour la station de travail de gestion


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
<td align="left"><p>Avant d’installer le client MBAM, téléchargez les modèles de stratégie de groupe MBAM à partir de la <a href="https://go.microsoft.com/fwlink/p/?LinkId=393941" data-raw-source="[How to Get MDOP Group Policy (.admx) Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941)"> section obtention de modèles de stratégie de groupe MDOP (. admx) </a> et configurez-les avec les paramètres que vous voulez implémenter dans votre entreprise pour le chiffrement de lecteur BitLocker.</p></td>
<td align="left"><p>Avant d’installer le client MBAM, procédez comme suit:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">À faire</th>
<th align="left">Où obtenir des instructions</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copier les modèles de stratégie de groupe MBAM</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Copie des modèles de stratégie de groupe MBAM2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Modifier les paramètres de stratégie de groupe</p></td>
<td align="left"><p><a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)">Modification des paramètres de stratégie de groupe MBAM2.5</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>





## Rubriques connexes


[Préparation de votre environnement pour MBAM2.5](preparing-your-environment-for-mbam-25.md)

[Planification du déploiement de MBAM2.5](planning-to-deploy-mbam-25.md)

[Configurations prises en charge par MBAM2.5](mbam-25-supported-configurations.md)




## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




