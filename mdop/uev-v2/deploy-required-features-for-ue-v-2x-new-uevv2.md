---
title: Déployer les fonctionnalités UE-V2.x requises
description: Déployer les fonctionnalités UE-V2.x requises
author: dansimp
ms.assetid: 10399bb3-cc7b-4578-bc0c-2f6b597abe4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2123ec75fb151a8f5b836b9b2522a9d6090b043
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810692"
---
# Déployer les fonctionnalités UE-V2.x requises


L’ensemble des déploiements de Microsoft User performance (UE-V) 2,0, 2,1 et 2,1 SP1 nécessitent ces fonctionnalités.

-   [Déploiement d’un emplacement de stockage des paramètres](#ssl) accessible aux utilisateurs finaux.

    Il s’agit d’un partage réseau standard qui stocke et récupère les paramètres utilisateur.

-   [Choisir la méthode de configuration pour UE-V](#config)

    UE-V peut être déployé et configuré à l’aide d’outils de gestion courants tels que la stratégie de groupe, le gestionnaire de configuration ou l’infrastructure de gestion Windows et PowerShell.

-   [Déployez un agent UE-V](#agent) pour qu’il soit installé sur tous les ordinateurs qui synchronisent les paramètres.

    Ce contrôle surveille les applications inscrites et le système d’exploitation en cas de modification des paramètres et synchronise ces paramètres entre les ordinateurs.

Les rubriques de cette section expliquent comment déployer ces fonctionnalités.

## <a href="" id="ssl"></a>Déploiement d’un emplacement de stockage des paramètres UE-V


UE-V nécessite un emplacement pour le stockage des paramètres utilisateur dans les fichiers du package de paramètres. Vous pouvez configurer cet emplacement de stockage des paramètres de l’une des manières suivantes:

-   Créer votre propre emplacement de stockage des paramètres

-   Utiliser Active Directory existant pour l’emplacement de stockage des paramètres

Si vous ne créez pas d’emplacement de stockage des paramètres, l’agent UE-V utilisera par défaut Active Directory (AD).

**Remarque**  
Dans le cadre des [performances et](https://technet.microsoft.com/library/dn458932.aspx#capacity) de la planification de la capacité et de réduire les problèmes liés à la latence du réseau, vous pouvez créer des emplacements de stockage des paramètres sur les mêmes réseaux locaux sur lesquels résident les ordinateurs des utilisateurs. Nous vous recommandons d’utiliser 20 Mo d’espace disque par utilisateur pour l’emplacement de stockage des paramètres.



### Créer un emplacement de stockage des paramètres UE-V

Avant de définir l’emplacement de stockage des paramètres, vous devez créer un répertoire racine avec des autorisations en lecture/écriture pour les utilisateurs qui stockent des paramètres sur le partage. L’agent UE-V crée des dossiers spécifiques à l’utilisateur sous cet annuaire racine.

L’emplacement de stockage des paramètres est défini en définissant l’option de configuration SettingsStoragePath, que vous pouvez configurer à l’aide de l’une des méthodes suivantes:

-   Lorsque vous [déployez l’agent UE-V](#agent) par le biais d’un paramètre de ligne de commande ou d’un script de commandes

-   Par le biais des paramètres de [stratégie de groupe](https://technet.microsoft.com/library/dn458893.aspx)

-   [Module System Center Configuration](https://technet.microsoft.com/library/dn458917.aspx) pour UE-V

-   Après l’installation de l’agent UE-V, à l’aide de [Windows PowerShell ou WMI (Windows Management Instrumentation)](https://technet.microsoft.com/library/dn458937.aspx)

Le chemin d’accès doit être dans un chemin UNC (Universal Naming Convention) du serveur et le partage. Par exemple, **\\\\Server\\Settingsshare\\**. Cette option de configuration prend en charge l’utilisation de variables pour activer des scénarios de synchronisation spécifiques. Par exemple, vous pouvez utiliser les `%username%\%computername%` variables pour conserver l’interface des paramètres utilisateur finaux dans les cas suivants:

-   Utilisateurs finaux qui utilisent plusieurs ordinateurs physiques dans votre entreprise

-   Ordinateurs d’entreprise utilisés par plusieurs utilisateurs finaux

L’agent UE-V crée de manière dynamique un chemin de stockage de paramètres spécifique à l’utilisateur, avec un dossier système caché nommé `SettingsPackages` en fonction du paramètre de configuration de **SettingsStoragePath**. L’agent lit et écrit les paramètres dans cet emplacement, comme défini par les modèles d’emplacement des paramètres UE-V enregistrés.

**Les paramètres d’UE-V sont déterminés par une règle de dernier enregistrement WINS:** Si l’emplacement de stockage des paramètres est le même pour les utilisateurs disposant de plusieurs ordinateurs gérés, un agent UE-V lit et écrit à l’emplacement des paramètres indépendamment des agents qui s’exécutent sur d’autres ordinateurs. Les derniers paramètres et valeurs écrits sont ceux appliqués lorsque l’agent suivant lit à partir de l’emplacement de stockage des paramètres.

**Déploiement de l’emplacement de stockage des paramètres:** Suivez ces étapes pour définir l’emplacement de stockage des paramètres plutôt que d’utiliser votre service Active Directory existant. Vous devez limiter l’accès au partage de stockage de paramètres aux utilisateurs qui en ont besoin, comme indiqué dans les tableaux ci-dessous.

**Pour déployer le partage réseau UE-V**

1.  Créer un groupe de sécurité pour les utilisateurs d’UE-V.

2.  Créez un dossier sur l’ordinateur central dans lequel sont stockés les packages de paramètres UE-V, puis accordez aux utilisateurs d’UE-V l’accès à un dossier. L’administrateur qui prend en charge UE-V doit disposer de l’autorisation d’accès à ce dossier partagé.

3.  Définissez les autorisations de blocs de messages serveur au niveau du partage (SMB) suivantes pour le dossier emplacement de stockage des paramètres.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Compte d’utilisateur</strong></th>
    <th align="left"><strong>Autorisations recommandées</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Tout le monde</p></td>
    <td align="left"><p>Aucune autorisation</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Groupe de sécurité des utilisateurs d’UE-V</p></td>
    <td align="left"><p>Contrôle total</p></td>
    </tr>
    </tbody>
    </table>



4.  Définissez les autorisations de système de fichiers NTFS suivantes pour le dossier emplacement de stockage des paramètres.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Compte d’utilisateur</strong></th>
    <th align="left"><strong>Autorisations recommandées</strong></th>
    <th align="left"><strong>Folder</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Créateur/propriétaire</p></td>
    <td align="left"><p>Contrôle total</p></td>
    <td align="left"><p>Sous-dossiers et fichiers uniquement</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Groupe de sécurité des utilisateurs d’UE-V</p></td>
    <td align="left"><p>Afficher le dossier/lire les données, créer des dossiers/ajouter des données</p></td>
    <td align="left"><p>Ce dossier uniquement</p></td>
    </tr>
    </tbody>
    </table>



Dans cette configuration, l’agent UE-V crée et sécurise un dossier Settingspackage lorsqu’il s’exécute dans le contexte de l’utilisateur, et accorde à chaque utilisateur l’autorisation de créer des dossiers pour le stockage des paramètres. Les utilisateurs reçoivent le contrôle total de leurs dossiers Settingspackage alors que d’autres utilisateurs ne peuvent pas y accéder.

**Remarque**  
Si vous créez le partage de stockage de paramètres sur un ordinateur exécutant un système d’exploitation Windows Server, configurez UE-V pour vérifier que le groupe Administrateurs local ou l’utilisateur actuel est le propriétaire du dossier dans lequel les packages de paramètres sont stockés. Pour activer cette sécurité supplémentaire, spécifiez ce paramètre dans l’éditeur du registre de Windows Server:

1.  Ajoutez une clé de Registre **reg \ _DWORD** nommée **«RepositoryOwnerCheckEnabled»** dans **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.

2.  Définissez la valeur de la clé de Registre sur *1*.



### Utiliser Active Directory avec UE-V 2. x

Par défaut, l’agent UE-V utilise Active Directory (AD) si un emplacement de stockage des paramètres n’est pas défini. Dans ces cas, l’agent UE-V crée dynamiquement le dossier de stockage des paramètres sous la racine du répertoire de base AD de chaque utilisateur. Toutefois, si un paramètre d’annuaire personnalisé est configuré dans AD, ce répertoire est utilisé à la place.

## <a href="" id="config"></a>Choisissez la méthode de configuration pour UE-V 2. x


Vous voulez déterminer la méthode de configuration que vous utiliserez pour gérer UE-V après le déploiement, car il s’agit de la méthode de configuration que vous utilisez pour déployer l’agent UE-V. En règle générale, il s’agit de la méthode de configuration que vous utilisez déjà dans votre environnement, telle que Windows PowerShell ou Configuration Manager.

Vous pouvez configurer UE-V avant, pendant ou après l’installation d’UE-V agent, en fonction de la méthode de configuration que vous utilisez.

-   [Stratégie de groupe](https://technet.microsoft.com/library/dn458893.aspx)**:** vous pouvez utiliser votre infrastructure de stratégie de groupe existante pour configurer UE-v avant ou après le déploiement de l’agent UE-v. Le modèle ADMX de stratégie de groupe UE-V autorise la gestion centralisée des options de configuration de l’agent UE-V communes et comprend des paramètres pour configurer la synchronisation d’UE-V.

    **Installation des modèles ADMX de stratégie de groupe UE-V:** Les modèles ADMX de stratégie de groupe pour UE-V configurent les paramètres de synchronisation pour l’agent UE-V et permettent la gestion centralisée des paramètres de configuration de l’agent UE-V communs en utilisant une infrastructure de stratégie de groupe existante.

    Les systèmes d’exploitation pris en charge pour le contrôleur de domaine qui déploient les objets de stratégie de groupe sont les suivants:

    Windows Server2008R2

    Windows Server 2012 et Windows Server 2012 R2

-   [Configuration Manager](https://technet.microsoft.com/library/dn458917.aspx)**:** le Pack de configuration d’UE-V vous permet d’utiliser la fonctionnalité paramètres de conformité de System Center Configuration Manager 2012 SP1 ou une version ultérieure pour appliquer des configurations cohérentes sur les sites sur lesquels UE-V et Configuration Manager sont installés.

-   [Windows PowerShell et WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** vous pouvez utiliser des commandes par script pour Windows PowerShell et Windows Management Instrumentation (WMI) pour modifier les configurations après l’installation de l’agent UE-V.

    **Remarque**  
    La modification du Registre peut occasionner une perte de données ou l’ordinateur ne répond plus. Nous vous recommandons d’utiliser d’autres méthodes de configuration.



-   **Installation de la ligne de commande ou du script par lot:** Les paramètres utilisés lors [du déploiement de l’agent UE-v](#agent) configurent de nombreux paramètres UE-v. Les systèmes de distribution de logiciels électroniques tels que System Center 2012 Configuration Manager, utilisent ces paramètres pour configurer leurs clients lorsqu’ils déploient et installent le logiciel d’agent UE-V.

## <a href="" id="agent"></a>Déploiement de l’agent UE-V 2. x


UE-V agent est le cœur d’un déploiement UE-V et doit s’exécuter sur chaque ordinateur qui utilise UE-V pour synchroniser les paramètres de l’application et de Windows.

**Fichiers d’installation d’agent UE-V:** Dans le cas d’un fichier d’installation unique, AgentSetup.exe, l’agent UE-V est installé sur les systèmes d’exploitation 32 bits et 64 bits. De plus, AgentSetupx86.msi ou AgentSetupx64.msi des fichiers Windows Installer propres à l’architecture sont fournis, et étant donné qu’ils sont plus petits, ils peuvent rationaliser les déploiements des agents. Les [paramètres de ligne de commande du programme](#params) d’installation de AgentSetup.exe sont également pris en charge pour l’installation de Windows Installer.

**Important**  
Lors de l’installation ou de la désinstallation d’UE-V agent, vous pouvez utiliser le fichier AgentSetup.exe ou le AgentSetup &lt; arch &gt; . msi, mais pas les deux. Le même fichier doit être utilisé pour désinstaller l’agent UE-V qui a été utilisé pour installer l’agent UE-V.



### Pour déployer l’agent UE-V

Pour déployer l’agent UE-V, vous pouvez utiliser les méthodes suivantes:

-   Un système de solution de distribution de logiciels électronique (ESD), tel que Configuration Manager, capable d’installer un fichier Windows Installer (. msi).

-   Script d’installation qui fait référence au fichier Windows Installer (. msi) qui est stocké sur un partage centralisé.

-   Un programme d’installation que vous exécutez manuellement sur l’ordinateur.

Utilisez la procédure suivante pour déployer l’agent UE-V à partir d’un partage réseau.

**Pour installer et configurer l’agent UE-V à partir d’un partage réseau**

1.  Étape du fichier d’installation de l’agent UE-V AgentSetup.exe sur un partage réseau auquel les utilisateurs disposent d’une autorisation de lecture.

2.  Déploiement d’un script sur des ordinateurs utilisateurs qui installent l’agent UE-V. Le script doit spécifier l’emplacement de stockage des paramètres.

**Options de déploiement:** Veillez à utiliser le format de variable approprié lors de l’installation de l’agent UE-V. Le tableau suivant contient des exemples d’options de déploiement pour l’utilisation des fichiers AgentSetup.exe ou Windows Installer (. msi).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Type de déploiement</strong></th>
<th align="left"><strong>Description du déploiement</strong></th>
<th align="left"><strong>Exemple</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Invite de commandes</p></td>
<td align="left"><p>Lorsque vous installez l’agent UE-V à une invite de commandes, utilisez le <em> format de variable% ^ nom_utilisateur% </em> . S’il est nécessaire de disposer de guillemets en raison d’espaces dans le chemin de stockage des paramètres, utilisez un fichier de script de commandes pour le déploiement.</p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Script de commande</p></td>
<td align="left"><p>Lorsque vous installez l’agent UE-V à partir d’un fichier de script de commandes, utilisez le <em> format de variable%% nom_utilisateur%% </em> . Si vous utilisez cette méthode d’installation, vous devez ignorer la variable contenant les caractères%%. Sans ce caractère, le script développe la <em> variable username </em> au moment de l’installation, plutôt qu’au moment de l’exécution, ce qui amène UE-V à utiliser un emplacement de stockage des paramètres unique pour tous les utilisateurs.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>WindowsPowerShell</p></td>
<td align="left"><p>Lorsque vous installez l’agent UE-V à partir d’une invite Windows PowerShell ou d’un script Windows PowerShell, utilisez le <em> format de variable% nom_utilisateur% </em> .</p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Distribution de logiciel électronique, comme le déploiement du déploiement logiciel de Configuration Manager</p></td>
<td align="left"><p>Lorsque vous installez l’agent UE-V à l’aide de Configuration Manager, utilisez le <em> format de variable ^% nom_utilisateur ^% </em> .</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>



**Remarque**  
L’installation de l’agent UE-V nécessite des droits d’administrateur, et l’ordinateur doit être redémarré pour que l’agent UE-V puisse s’exécuter.



### <a href="" id="params"></a>Paramètres de ligne de commande pour le déploiement d’agent UE-V

Les paramètres de ligne de commande de l’agent UE-V sont les suivants:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Paramètre de ligne de commande</strong></th>
<th align="left"><strong>Définition</strong></th>
<th align="left"><strong>Remarques</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/Help ou/h ou/?</p></td>
<td align="left"><p>Affiche la boîte de dialogue utilisation de AgentSetup.exe.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsStoragePath</p></td>
<td align="left"><p>Indique le chemin UNC (Universal Naming Convention) qui définit l’emplacement de stockage des paramètres.</p></td>
<td align="left"><div class="alert">
<strong>Important</strong><br/><p>Vous devez spécifier un SettingsStoragePath dans UE-V 2,1 et UE-V 2,1 SP1. Vous pouvez définir la chaîne AdHomePath pour spécifier que le chemin d’accès de l’utilisateur&#39;de la page d’accueil Active Directory est utilisé. Exemple : <code>SettingsStoragePath = \share\path|AdHomePath</code>.</p>
<p>Dans UE-V 2,0, vous pouvez laisser SettingsStoragePath vide pour utiliser le chemin d’accès à la page d’accueil Active Directory.</p>
</div>
<div>

</div>
<p>les variables d’environnement% nom d’utilisateur% ou% nom_ordinateur% sont acceptées. L’écriture de script peut nécessiter des variables d’échappement.</p>
<p><strong>Par défaut </strong> : &lt; aucune&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SettingsStoragePathReg</p></td>
<td align="left"><p>Obtient la valeur SettingsStoragePath du registre lors de l’installation.</p></td>
<td align="left"><p>À l’invite de commandes, tapez l’exemple suivant pour forcer UE-V à utiliser le chemin d’accès à la page d’accueil Active Directory au lieu d’un chemin UNC spécifique.</p>
<p><code>msiexec.exe /i AgentSetupx64.msi acceptlicenseterms=true SettingsStoragePathReg=TRUE /quiet /norestart</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsTemplateCatalogPath</p></td>
<td align="left"><p>Indique le chemin UNC (Universal Naming Convention) qui définit l’emplacement dans lequel les nouveaux modèles d’emplacement des paramètres sont consultés.</p></td>
<td align="left"><p>Requis uniquement pour les modèles d’emplacement des paramètres personnalisés</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RegisterMSTemplates</p></td>
<td align="left"><p>Indique si les modèles Microsoft par défaut doivent être inscrits lors de l’installation.</p></td>
<td align="left"><p>True | Fals</p>
<p><strong>Valeur par défaut </strong> : vrai</p></td>
</tr>
<tr class="even">
<td align="left"><p>PowerSchool</p></td>
<td align="left"><p>Spécifie la méthode de synchronisation à utiliser.</p></td>
<td align="left"><p>SyncProvider | Néant</p>
<p><strong>Par défaut </strong> : SyncProvider</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncTimeoutInMilliseconds</p></td>
<td align="left"><p>Spécifie le nombre de millisecondes pendant lesquelles l’ordinateur attend avant qu’il récupère les paramètres utilisateur à partir de l’emplacement de stockage des paramètres.</p></td>
<td align="left"><p><strong>Par défaut </strong> : 2000 millisecondes</p>
<p>(attendez 2 secondes)</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncEnabled</p></td>
<td align="left"><p>Indique si la synchronisation UE-V est activée ou désactivée.</p></td>
<td align="left"><p>True | Fals</p>
<p><strong>Valeur par défaut </strong> : vrai</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxPackageSizeInBytes</p></td>
<td align="left"><p>Spécifie la taille de fichier du package de paramètres en octets lorsque l’agent UE-V signale que les fichiers dépassent le seuil.</p></td>
<td align="left"><p>&lt;papier&gt;</p>
<p><strong>Par défaut </strong> : aucun (aucun seuil d’avertissement)</p></td>
</tr>
<tr class="even">
<td align="left"><p>CEIPEnabled</p></td>
<td align="left"><p>Spécifie le paramètre de participation au programme d’amélioration du produit. S' <strong> il est défini sur true </strong> , les informations du programme d’installation sont téléchargées sur le site du programme d’amélioration du produit de Microsoft. Si <strong> elle est définie sur false </strong> , aucune information n’est téléchargée.</p></td>
<td align="left"><p>True | Fals</p>
<p><strong>Valeur par défaut </strong> : false</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Restart</p></td>
<td align="left"><p>Prend en charge le report du redémarrage de l’ordinateur après l’installation de l’agent UE-V.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>INSTALLFOLDER</p></td>
<td align="left"><p>Permet de définir un autre dossier d’installation pour l’agent UE-V ou le générateur UE-V.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>MUENABLED</p></td>
<td align="left"><p>Permet d’accepter l’option d’inclusion du programme Microsoft Update.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>ACCEPTLICENSETERMS</p></td>
<td align="left"><p>Autorise l’installation de UE-V de manière silencieuse. Cette valeur doit être définie sur <strong> true </strong> pour installer UE-v en silence, sans que l’utilisateur accepte les termes du contrat de licence UE-v. S’il est défini sur <strong> false </strong> ou vide, l’utilisateur reçoit un message d’erreur et UE-V n’est pas installé.</p></td>
<td align="left"><div class="alert">
<strong>Important</strong><br/><p>Ce paramètre est requis pour installer UE-V en silence.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Restart</p></td>
<td align="left"><p>Empêche un redémarrage obligatoire après l’installation d’UE-V agent.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Mettre à jour l’agent UE-V

Les mises à jour du logiciel de l’agent UE-V sont fournies par le biais de Microsoft Update. Vous pouvez déployer des mises à jour de l’agent UE-V à l’aide de systèmes d’infrastructure de distribution de logiciels d’entreprise.

Lors d’une mise à niveau d’agent UE-V, le groupe par défaut des modèles d’emplacement des paramètres pour les applications Microsoft courantes et les paramètres Windows peut être mis à jour.

### Mettre à niveau l’agent UE-V 2. x

L’agent UE-V 2. x introduit de nombreuses nouvelles fonctionnalités et modifie la façon dont l’agent charge le contenu sur le partage de stockage des paramètres. Le processus de mise à niveau automatise ces modifications. Pour mettre à niveau l’agent UE-V, exécutez le package d’installation de l’agent UE-V (AgentSetup.exe, AgentSetupx86.msi ou AgentSetupx64.msi) sur les ordinateurs des utilisateurs.

**Remarque**  
Lorsque vous effectuez une mise à niveau de l’agent UE-V, vous devez utiliser le même type de programme d’installation (fichier. exe ou paquet. msi) qui a installé l’agent UE-V précédent. Par exemple, utilisez le AgentSetup.exe UE-V 2 pour mettre à niveau les agents UE-V 1,0 installés à l’aide de AgentSetup.exe.



Les configurations suivantes sont conservées lors de l’exécution du programme d’installation de l’agent:

-   Emplacement de stockage des paramètres

-   Paramètres du Registre

-   Tâches planifiées (les paramètres d’intervalle sont réinitialisés à leurs valeurs par défaut)

**Remarque**  
Un ordinateur avec des modèles d’emplacement des paramètres d’UE-V 2. x qui sont inscrits dans le journal des événements UE-V 1,0.



Vous pouvez utiliser Microsoft System Center 2012 Configuration Manager ou un autre outil de distribution de logiciels d’entreprise pour automatiser et distribuer la mise à niveau de l’agent UE-V.

**Recommandations:** Nous vous recommandons d’effectuer la mise à niveau de tous les agents UE-V 1,0 dans un environnement informatique, mais cela n’est pas obligatoire. UE-V 2. x les modèles d’emplacement des paramètres peuvent interagir avec un agent UE-V 1,0, car ils partagent uniquement les paramètres à partir du chemin de stockage des paramètres. Toutefois, nous vous recommandons de déplacer les déploiements vers une version d’agent unique pour simplifier la gestion et prendre en charge UE-V.

### Réparation d’UE-V agent après une mise à niveau infructueuse

Vous risquez de rencontrer des erreurs après avoir essayé l’une des opérations suivantes:

-   Effectuer une mise à niveau d’UE-V 1,0 vers UE-V 2

-   Effectuez une mise à niveau vers une version plus récente de Windows, par exemple, de Windows 7 vers Windows 8 ou de Windows 8 vers Windows 8,1.

-   Désinstaller l’agent après la mise à niveau de l’agent UE-V

Pour résoudre les problèmes, essayez de réparer l’agent UE-V en entrant la commande suivante à l’invite de commandes sur l’ordinateur sur lequel l’agent est installé.

``` syntax
msiexec.exe /f "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log
```

Vous pouvez ensuite réessayer le processus de désinstallation ou procéder à la mise à niveau en installant la version la plus récente de l’agent UE-V.






## Rubriques connexes


[Préparer un déploiement UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Déployer UE-V 2. x pour des applications personnalisées](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)









