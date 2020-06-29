---
title: Comment configurer les applications Web MBAM2.5
description: Comment configurer les applications Web MBAM2.5
author: dansimp
ms.assetid: 909bf2d3-028c-4ac1-9247-171532a1eeae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0336d24f51167a00c8565ccd081f4bc5dfb2c4cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810590"
---
# Comment configurer les applications Web MBAM2.5


Cet article explique comment configurer les applications Web Microsoft BitLocker Administration and Analysis (MBAM) 2,5 pour l' [architecture de niveau supérieur recommandée pour MBAM 2,5](high-level-architecture-for-mbam-25.md) en utilisant l’une des méthodes suivantes:

-   Une applet de cmdlet Windows PowerShell

-   Assistant Configuration de MBAM Server

Les applications Web comprennent les sites Web suivants et leurs services Web correspondants:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Website</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Site Web d’administration et de surveillance</p></td>
<td align="left"><p>Site Web dans lequel les utilisateurs spécifiques peuvent afficher des rapports et aider les utilisateurs finaux à récupérer leurs ordinateurs lors de leur oubli du code confidentiel ou du mot de passe</p></td>
</tr>
<tr class="even">
<td align="left"><p>Portail libre-service</p></td>
<td align="left"><p>Site Web: les utilisateurs finaux peuvent accéder de manière indépendante à leurs ordinateurs s’ils ont oublié leur code confidentiel ou leur mot de passe.</p></td>
</tr>
</tbody>
</table>



**Avant de démarrer la configuration:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Étape</th>
<th align="left">Où obtenir des instructions</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Passez en revue l’architecture recommandée pour MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Architecture de hautniveau pour MBAM2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Passez en revue les configurations prises en charge pour MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurations prises en charge par MBAM2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Remplissez les conditions préalables requises sur chaque serveur.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Assurez-vous de configurer les services SQL ServerReporting (SSRS) pour utiliser le protocole SSL (Secure Sockets Layer) avant de configurer le site Web d’administration et de surveillance. Dans le cas contraire, la fonction rapports utilise HTTP au lieu de HTTPs.</p>
</div>
<div>

</div></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">MBAM 2,5 requis par le serveur qui ne s’appliquent qu’à la topologie d’intégration de Configuration Manager </a> (le cas échéant)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Enregistrez les noms de principal de service (SPN) pour le compte du pool d’applications pour les sites Web. Vous ne devez effectuer cette étape que si vous n’avez pas de privilèges d’administrateur dans les services de domaine Active Directory (AD DS). Si vous disposez de ces droits dans AD DS, MBAM créera les noms de services pour vous.</p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn)">Planification de la sécurisation des sites web MBAM</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous allez configurer une fonctionnalité de MBAM Server.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si vous envisagez d’installer le site Web sur un serveur et les services Web sur un autre serveur, vous pouvez les configurer uniquement à l’aide de la <strong> </strong> cmdlet Windows PowerShell Enable-MbamWebApplication. L’Assistant Configuration du serveur MBAM ne prend pas en charge la configuration de ces éléments sur des serveurs distincts.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installation du logiciel serveur MBAM2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Consultez la configuration requise pour l’utilisation de Windows PowerShell Si vous envisagez d’utiliser des cmdlets pour configurer les fonctionnalités de MBAM Server.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Pour configurer les applications Web à l’aide de Windows PowerShell**

1.  Avant de commencer la configuration, reportez-vous à la rubrique [Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) pour consulter les conditions préalables à l’utilisation de Windows PowerShell.

2.  Utilisez l’applet de ligne **Enable-MbamWebApplication** pour configurer les applications Web à l’aide de Windows PowerShell. Pour obtenir des informations sur cette cmdlet, tapez **Get-Help-MbamWebApplication**.

**Pour configurer les paramètres de toutes les applications Web à l’aide de l’Assistant**

1. Sur le serveur sur lequel vous voulez configurer les applications Web, démarrez l’Assistant Configuration de MBAM Server. Vous pouvez sélectionner **MBAM de configuration de serveur** dans le menu **Démarrer** pour ouvrir l’Assistant.

2. Cliquez sur **ajouter de nouvelles fonctionnalités**, sélectionnez **administration et analyse du site Web** et du **portail libre-service**, puis cliquez sur **suivant**. L’Assistant vérifie que toutes les conditions préalables pour les applications Web sont remplies.

3. Si la vérification de la configuration requise est réussie, cliquez sur **suivant** pour continuer. Dans le cas contraire, résolvez les conditions préalables manquantes, puis cliquez **à nouveau sur vérifier les conditions préalables**.

4. Utilisez les descriptions suivantes pour entrer les valeurs de champ dans l’Assistant.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><strong>Champ</strong></th>
   <th align="left">Description</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Certificat de sécurité</strong></p></td>
   <td align="left"><p>Sélectionnez un certificat créé précédemment pour chiffrer éventuellement la communication entre les services Web et le serveur sur lequel vous configurez les sites Web. Si vous choisissez <strong> ne pas utiliser de certificat </strong> , votre communication Web risque de ne pas être sécurisée.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Nom de l'hôte</strong></p></td>
   <td align="left"><p>Nom de l’ordinateur hôte sur lequel vous configurez les sites Web.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Chemin d’installation</strong></p></td>
   <td align="left"><p>Emplacement d’installation des sites Web.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Port</strong></p></td>
   <td align="left"><p>Numéro de port à utiliser pour la communication avec les sites Web et les services.</p>
   <div class="alert">
   <strong>Remarque</strong><br/><p>Vous devez définir une exception de pare-feu pour autoriser les communications via le port spécifié.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Compte et mot de passe du pool d’applications de service Web</strong></p></td>
   <td align="left"><p>Compte d’utilisateur de domaine et mot de passe pour le pool d’applications de service Web.</p>
   <p>Si vous entrez un nom d’utilisateur dans le <strong> champ d’utilisateur ou de groupe de domaine d’accès en lecture/écriture </strong> sur la <strong> page configurer des bases de données </strong> , vous devez entrer cette même valeur dans ce champ.</p>
   <p>Si vous entrez un nom de groupe dans le <strong> champ User ou Group (lecture/écriture </strong> ) sur la <strong> page configure databases </strong> , la valeur que vous entrez dans ce champ doit être membre du groupe.</p>
   <p>Si vous ne spécifiez pas les informations d’identification, les informations d’identification spécifiées pour une application Web précédemment activée seront utilisées. Toutes les applications Web doivent utiliser les mêmes informations d’identification de pool d’applications. Si vous spécifiez des informations d’identification différentes pour différentes applications Web, la valeur la plus récemment spécifiée est utilisée.</p>
   <div class="alert">
   <strong>Important</strong><br/><p>Pour une sécurité améliorée, définissez le compte spécifié dans les informations d’identification pour disposer de droits d’utilisateur limités. Définissez également le mot de passe du compte pour qu’il n’expire jamais.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



5. Vérifiez que le compte intégré aux services Internet (IIS _IUSRS), ou au compte du pool d’applications a été ajouté à l' **identité d’un client après l’authentification** et **que le travail en fonction du traitement par lot** est défini sur paramètres de sécurité locale.

   Pour vérifier si l’application a été ajoutée aux paramètres de sécurité locaux, ouvrez l' **éditeur de stratégie de sécurité locale**, développez le nœud **stratégies locales** , cliquez sur le nœud d' **attribution de droits d’utilisateur** , puis double-cliquez sur emprunter l’identité d' **un client après authentification** et **Connectez-vous en tant que stratégies de travail par lot** dans le volet droit.

**Pour configurer les informations de connexion des bases de données à l’aide de l’Assistant**

1.  Utilisez les descriptions de champs suivantes pour configurer les informations de connexion dans l’Assistant pour la base de données d’audit et de conformité.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Champ</th>
    <th align="left">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Nom SQL Server</strong></p></td>
    <td align="left"><p>Nom du serveur sur lequel la base de données d’audit et de conformité est configurée.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Instance de base de données SQL Server</strong></p></td>
    <td align="left"><p>Nom de l’instance SQL Server où la base de données d’audit et de conformité est configurée.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Nom de la base de données</strong></p></td>
    <td align="left"><p>Nom de la base de données d’audit et de conformité.</p></td>
    </tr>
    </tbody>
    </table>



2.  Utilisez les descriptions de champs suivantes pour configurer les informations de connexion dans l’Assistant pour la base de données de récupération.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Champ</th>
    <th align="left">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Nom SQL Server</strong></p></td>
    <td align="left"><p>Nom du serveur sur lequel la base de données de récupération est configurée.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Instance de base de données SQL Server</strong></p></td>
    <td align="left"><p>Nom de l’instance SQL Server où la base de données de récupération est configurée.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Nom de la base de données</strong></p></td>
    <td align="left"><p>Nom de la base de données de récupération.</p></td>
    </tr>
    </tbody>
    </table>



**Pour configurer les applications Web à l’aide de l’Assistant**

1. Utilisez les descriptions suivantes pour entrer les valeurs de champ dans l’Assistant afin de configurer le site Web d’administration et de surveillance.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Champ</th>
   <th align="left">Description</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Groupe de domaine de rôle de support avancé</strong></p></td>
   <td align="left"><p>Groupe d’utilisateurs de domaine dont les membres ont accès à toutes les zones du site Web d’administration et de contrôle, à l’exception de la zone rapports.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Groupe de domaine du rôle de support technique</strong></p></td>
   <td align="left"><p>Groupe d’utilisateurs de domaine dont les membres ont accès aux <strong> zones gérer le module de plateforme sécurisée </strong> et <strong> </strong> de récupération des lecteurs du site Web d’administration et de surveillance.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Utiliser System Center Configuration Manager Integration</strong></p></td>
   <td align="left"><p>Activez cette case à cocher si vous configurez MBAM avec la topologie d’intégration de Configuration Manager. L’activation de cette case à cocher permet d’afficher tous les rapports, à l’exception du rapport d’audit de récupération, dans Configuration Manager plutôt que sur le site Web d’administration et de surveillance.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Groupe de domaine de rôle de rapport</strong></p></td>
   <td align="left"><p>Groupe d’utilisateurs de domaine dont les membres disposent d’un accès en lecture seule à la zone rapports du site Web d’administration et de surveillance.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>URL SQL Server Reporting Services</strong></p></td>
   <td align="left"><p>URL du serveur SSRS sur lequel les rapports MBAM sont configurés.</p>
   <p>Exemples d’URL de rapport:</p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Type de nom d’hôte</th>
   <th align="left">Exemple</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Exemple avec nom de domaine complet</p></td>
   <td align="left"><p><a href="https://MyReportServer.Contoso.com/ReportServer" data-raw-source="https://MyReportServer.Contoso.com/ReportServer">https://MyReportServer.Contoso.com/ReportServer</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Exemple avec nom d’hôte personnalisé</p></td>
   <td align="left"><p><a href="https://MyReportServer/ReportServer" data-raw-source="https://MyReportServer/ReportServer">https://MyReportServer/ReportServer</a></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Répertoire virtuel</strong></p></td>
   <td align="left"><p>Répertoire virtuel du site Web d’administration et de surveillance. Ce nom correspond au répertoire physique du site Web sur le serveur et est ajouté au nom d’hôte du site Web, par exemple:</p>
   <p>http (s):// &lt; <em> hostname </em> &gt; : &lt; <em> port </em> &gt; /helpdesk/</p>
   <p>Si vous ne spécifiez pas de répertoire virtuel, la valeur du <strong> support technique est </strong> utilisée.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Groupe de domaines du rôle de migration des données </strong> (facultatif)</p></td>
   <td align="left"><p>Groupe d’utilisateurs de domaine dont les membres ont accès pour utiliser les applets de sélection d’information d’écriture-MBAM * pour écrire des informations de récupération via ce point de terminaison.</p></td>
   </tr>
   </tbody>
   </table>



2. Utilisez la description suivante pour entrer les valeurs de champ dans l’Assistant afin de configurer le portail libre-service.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Champ</th>
   <th align="left">Description</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Répertoire virtuel</strong></p></td>
   <td align="left"><p>Répertoire virtuel de l’application Web. Ce nom correspond au répertoire physique du site Web sur le serveur et est ajouté au nom d’hôte du site Web, par exemple:</p>
   <p>http (s):// &lt; <em> hostname </em> &gt; : &lt; <em> port </em> &gt; /selfservice/</p>
   <p>Si vous ne spécifiez pas un répertoire virtuel, la valeur <strong> selfservice </strong> est utilisée.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Nom de la société</p></td>
   <td align="left"><p>Spécifiez le nom d’une entreprise du portail libre-service, par exemple:</p>
   <p>Contoso</p>
   <p>Le nom de cette société est affiché par tous les utilisateurs du portail libre-service.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Texte de l’URL du support technique</p></td>
   <td align="left"><p>Spécifiez une instruction de texte qui redirige les utilisateurs vers le site Web du support technique de votre organisation, par exemple:</p>
   <p>Contacter le support technique ou le service informatique</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>URL du support technique</p></td>
   <td align="left"><p>Spécifiez l’URL du site Web d’assistance technique de votre organisation, par exemple:</p>
   <p>http (s):// &lt; <em> companyHelpdeskURL</em>&gt;/</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Fichier texte d’avis</p></td>
   <td align="left"><p>Dans la page d’accueil du portail libre-service, sélectionnez un fichier qui contient la notification que vous souhaitez afficher aux utilisateurs.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Ne pas afficher le texte d’avis aux utilisateurs</p></td>
   <td align="left"><p>Activez cette case à cocher pour spécifier que le texte de l’avis ne s’affiche pas aux utilisateurs.</p></td>
   </tr>
   </tbody>
   </table>



3. Lorsque vous avez terminé, cliquez sur **suivant**.

   L’Assistant vérifie que toutes les conditions préalables pour les applications Web sont remplies.

4. Cliquez sur **Suivant** pour poursuivre.

5. Dans la page **Résumé** , passez en revue les fonctionnalités qui seront ajoutées.

   **Remarque**  
   Pour créer un script Windows PowerShell pour les entrées que vous avez effectuées, cliquez sur **Exporter le script PowerShell** et enregistrez le script.



6. Cliquez sur **Ajouter** pour ajouter les applications Web au serveur, puis cliquez sur **Fermer**.

   Pour personnaliser le portail libre-service en ajoutant un texte d’avis personnalisé, le nom de votre entreprise, des pointeurs vers des informations supplémentaires, etc., voir [Personnalisation du portail libre-service pour votre organisation](customizing-the-self-service-portal-for-your-organization.md).

**Pour configurer le portail libre-service si les ordinateurs clients ne peuvent pas accéder au CDN**

1.  Déterminez si vous exécutez le service d’administration et de surveillance de BitLocker (MBAM) 2,5 SP1. Si tel est le cas, ne faites rien. Votre configuration du portail libre-service est terminée.

    **Remarque**  
    Le programme d’administration et de surveillance de BitLocker (MBAM) 2,5 SP1 installe les fichiers JavaScript dans le programme d’installation, il n’est donc pas nécessaire de se connecter au réseau de distribution de contenu Microsoft AJAX pour configurer le portail libre-service. Les étapes suivantes sont nécessaires uniquement si vous utilisez une version de Microsoft BitLocker administration et analyse (MBAM) 2,5 antérieure à SP1.



2.  Déterminez si vos ordinateurs clients ont accès au réseau de distribution de contenu (CDN) Microsoft Ajax.

    Le CDN donne au portail libre-service le besoin d’accéder à certains fichiers JavaScript. Si vous ne configurez pas le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au CDN, seul le nom de la société et le compte sous lequel l’utilisateur final s’est connecté est affiché. Aucun message d’erreur ne s’affichera.

3.  Effectuez l'une des opérations suivantes:

    -   Si vos ordinateurs clients ont accès au réseau de distribution de contenu (CDN), ne faites rien. Votre configuration du portail libre-service est terminée.

    -   Si vos ordinateurs clients n’ont pas accès au réseau de distribution de contenu (CDN), suivez les étapes décrites dans la [procédure de configuration du portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).


## Rubriques connexes


[Journaux des événements serveur](server-event-logs.md)

[Configuration des composants du serveur MBAM2.5](configuring-the-mbam-25-server-features.md)

[Comment configurer le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)

[Personnalisation du portail libre-service de votre organisation](customizing-the-self-service-portal-for-your-organization.md)

[Validation de la configuration des composants serveur de MBAM2.5](validating-the-mbam-25-server-feature-configuration.md)



## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





