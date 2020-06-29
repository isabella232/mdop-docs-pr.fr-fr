---
title: À propos de la création de rapports d'App-V5.0
description: À propos de la création de rapports d'App-V5.0
author: dansimp
ms.assetid: 27c33dda-f017-41e3-8a78-1b681543ec4f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a29585886aa20233f49c85101cff570a098c69ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806141"
---
# À propos de la création de rapports d'App-V5.0


Microsoft Application Virtualization (App-V) 5,0 inclut une fonctionnalité de création de rapports intégrée qui vous permet de collecter des informations sur les ordinateurs exécutant le client App-V 5,0 ainsi que des informations sur l’utilisation des packages d’applications virtuelles. Vous pouvez utiliser ces informations pour générer des rapports à partir d’une base de données centralisée.

## <a href="" id="---------app-v-5-0-reporting-overview"></a> Présentation de la création de rapports App-V 5,0


La liste suivante présente le flux de travail de haut en bas pour la création de rapports dans App-V 5,0.

1.  Le serveur de création de rapports d’application Microsoft application (App-V) 5,0 comporte les conditions préalables suivantes:

    -   Rôle du serveur Web Internet Information Services (IIS)

    -   Rôle d’authentification Windows (sous **IIS/sécurité**)

    -   SQL Server installé et exécuté avec SQL Server Reporting Services (SSRS)

    Pour vérifier que SQL Server Reporting Services est en cours d’exécution, affichez- `http://localhost/Reports` le dans un navigateur Web en tant qu’administrateur sur le serveur qui héberge la création de rapports App-V 5,0. La page d’accueil de SQL Server Reporting Services doit s’afficher.

2.  Installez le serveur de rapports App-V 5,0 et la base de données associée. Pour plus d’informations sur l’installation de Report Server [, voir comment installer le serveur de création de rapports sur un ordinateur autonome et le connecter à la base de données](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md). Configurez le moment où l’ordinateur exécutant le client App-V 5,0 doit envoyer des données au serveur de rapports.

3.  Si vous n’utilisez pas un système électronique de distribution de logiciels tel que Configuration Manager pour afficher les rapports, vous pouvez définir des rapports dans SQL Server Reporting Service. Téléchargez des rapports appvshort prédéfinis à partir du centre de téléchargement à l’adresse <https://go.microsoft.com/fwlink/?LinkId=397255> .

    **Remarques**  Si vous utilisez l’intégration de Configuration Manager avec App-V 5,0, la plupart des rapports sont générés à partir de Configuration Manager plutôt que d’App-V 5,0.

     

4.  Après avoir importé le module App-V 5,0 PowerShell en `Import-Module AppvClient` tant qu’administrateur, activez le client App-v 5,0. Cet exemple de cmdlet PowerShell permet la création de rapports 5,0 App-V:

    ``` syntax
    Set-AppvClientConfiguration –reportingserverurl <url>:<port> -reportingenabled 1 – ReportingStartTime <0-23> - ReportingRandomDelay <#min>
    ```

    Pour envoyer immédiatement les données du rapport App-V 5,0, exécutez `Send-AppvClientReport` le client App-v 5,0.

    Pour plus d’informations sur l’installation du client App-V 5,0 avec la création de rapports activée, voir [à propos des paramètres de configuration du client](about-client-configuration-settings.md). Pour gérer la création de rapports App-V 5,0 avec Windows PowerShell, reportez-vous [à la rubrique activation de la création de rapports sur le client App-v 5,0 à l’aide de PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md).

5.  Après que le serveur de création de rapports a reçu les données du client App-V 5,0, il envoie les données à la base de données de création de rapports. Lorsque la base de données reçoit et traite les données du client, une réponse réussie est envoyée au serveur de création de rapports, puis une notification est envoyée au client App-V 5,0.

6.  Lorsque le client App-V 5,0 reçoit la notification de réussite, il vide le cache des données pour économiser de l’espace.

    **Remarques**  Par défaut, le cache est vidé une fois le serveur confirmant la réception des données. Vous pouvez configurer manuellement le client pour l’enregistrement du cache de données.

     

~~~
If the App-V 5.0 client device does not receive a success notification from the server, it retains data in the cache and tries to resend data at the next configured interval. Clients continue to collect data and add it to the cache.
~~~

### <a href="" id="-------------app-v-5-0-reporting-server-frequently-asked-questions"></a> Forum aux questions sur le serveur de création de rapports App-V 5,0

Le tableau suivant contient des réponses aux questions fréquemment posées sur la création de rapports App-V 5,0

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Question</th>
<th align="left">Plus d’informations</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Quelle est la fréquence d’envoi des informations de rapport à la base de données de création de rapports?</p></td>
<td align="left"><p>La fréquence dépend du mode de configuration de la tâche de création de rapports sur l’ordinateur exécutant le client App-V 5,0. Vous devez configurer la fréquence/l’intervalle d’envoi des données de rapport. Le rapport App-V 5,0 n’est pas activé par défaut.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Quelles informations sont stockées dans la base de données du serveur de rapports?</p></td>
<td align="left"><p>La liste suivante indique les éléments stockés dans la base de données de création de rapports:</p>
<ul>
<li><p>Le système d’exploitation exécuté sur l’ordinateur exécutant le client App-V 5,0: nom d’hôte, version, Service Pack, type-client/serveur, architecture du processeur.</p></li>
<li><p>Informations sur le client App-V 5,0: version.</p></li>
<li><p>Liste des packages publiés: GUID, GUID de version, nom.</p></li>
<li><p>Informations sur l’utilisation des applications: nom, version, Streaming Server, utilisateur (DOMAIN\alias), GUID de la version du package, état du lancement et temps d’arrêt.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Quel est le volume moyen d’informations envoyées au serveur de création de rapports?</p></td>
<td align="left"><p>Ça dépend. La liste suivante présente les trois ensembles de données envoyés au serveur de rapports:</p>
<ol>
<li><p>Informations sur le système d’exploitation et le client App-V 5,0. ~ 150 octets, chaque fois que les données sont envoyées.</p></li>
<li><p>Liste de packages publiée. ~ 7 Ko pour 30 Packages. Cette opération est envoyée uniquement lorsque la liste de packages est mise à jour avec une actualisation de publication, qui est exécutée fréquemment. s’il n’y a aucune modification, ces informations ne sont pas envoyées.</p></li>
<li><p>Informations sur l’utilisation des applications virtuelles: environ 0,25 Ko par événement. Le compte d’ouverture et de fermeture en tant qu’événement s’il se produit avant l’envoi des informations. Lorsque vous envoyez du courrier à l’aide d’une tâche planifiée, seules les données depuis le dernier téléchargement réussi sont envoyées au serveur. S’il s’agit d’un envoi manuel par le biais de l’applet de commande PowerShell, il existe un argument facultatif qui contrôle si les données doivent être de nouveau envoyées une nouvelle fois, car cet argument est <strong> DeleteOnSuccess </strong> .</p>
<p></p>
<p>Par exemple, si vingt applications sont ouvertes et fermées, et que les informations de rapport doivent être envoyées quotidiennement, le trafic quotidien standard devrait être de 0,15 Ko + 20 x 0,25 Ko ou à propos de 5KB/utilisateur</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>La création de rapports peut-elle être planifiée?</p></td>
<td align="left"><p>Oui. Outre l’envoi manuel de rapports à l’aide d’applets de cmdlet PowerShell ( <strong> Send-AppvClientReport </strong> ), la tâche peut être planifiée pour qu’elle se produise automatiquement. Il existe deux méthodes pour planifier le rapport:</p>
<ol>
<li><p>Utilisation des cmdlets PowerShell- <strong> Set-AppvClientConfiguration </strong> . Exemple:</p>
<p>Set-AppvClientConfiguration-ReportingEnabled 1-ReportingServerURL<a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</a></p>
<p></p>
<p>Pour obtenir la liste complète des paramètres de configuration du client, voir <a href="about-client-configuration-settings.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings.md)"> à propos des paramètres de configuration du client </a> et recherchez les entrées suivantes: <strong> ReportingEnabled </strong> , <strong> ReportingServerURL </strong> , <strong> ReportingDataCacheLimit </strong> , <strong> ReportingDataBlockSize </strong> , <strong> ReportingStartTime </strong> , <strong> ReportingRandomDelay </strong> , <strong> ReportingInterval </strong> .</p>
<p></p></li>
<li><p>À l’aide d’une stratégie de groupe. S’il est distribué à l’aide du contrôleur de domaine, les paramètres sont les mêmes que ceux indiqués précédemment.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Les paramètres de stratégie de groupe remplacent les paramètres locaux configurés à l’aide de PowerShell.</p>
</div>
<div>

</div></li>
</ol></td>
</tr>
</tbody>
</table>
 


## <a href="" id="---------app-v-5-0-client-reporting"></a> Rapports pour les clients App-V 5,0


Pour utiliser la création de rapports App-V 5,0, vous devez installer et configurer le client App-V 5,0. Une fois le client installé, utilisez la cmdlet PowerShell **Set-AppVClientConfiguration** ou le **modèle ADMX** pour configurer la création de rapports. Les applets de commande de fonctionnalité de création de rapports sont disponibles en utilisant le lien suivant et sont précédés de **rapports**. Pour obtenir la liste complète des paramètres de configuration du client, voir [à propos des paramètres de configuration du client](about-client-configuration-settings.md). La section suivante fournit des exemples de configuration de création de rapports pour les clients App-V 5,0 utilisant PowerShell.

### Configuration de la création de rapports de clients App-V à l’aide de PowerShell

Les exemples suivants montrent comment les paramètres PowerShell peuvent configurer les fonctionnalités de création de rapports du client App-V 5,0.

**Remarque**  
La tâche de configuration suivante peut également être configurée à l’aide des paramètres de stratégie de groupe dans le modèle ADMX App-V 5,0. Pour plus d’informations sur l’utilisation du modèle ADMX, voir modification de la [configuration du client App-V 5,0 à l’aide du modèle ADMX et de la stratégie de groupe](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md).
 


**Pour activer les rapports et lancer la collecte de données sur l’ordinateur exécutant le client App-V 5,0**:

`Set-AppVClientConfiguration –ReportingEnabled 1`

**Pour configurer le client de manière à envoyer automatiquement des données à un serveur de rapports spécifique**:

``` syntax
Set-AppVClientConfiguration –ReportingServerURL http://MyReportingServer:MyPort/ -ReportingStartTime 20 -ReportingInterval 1 -ReportingRandomDelay 30
```

`-ReportingInterval 1 -ReportingRandomDelay 30`

Cet exemple configure le client pour envoyer automatiquement les données de rapport à l’URL du serveur de rapports <strong> http://MyReportingServer:MyPort/ </strong> . De plus, les données de rapport seront envoyées quotidiennement entre 8:00 et 8:30 PM, en fonction du retard aléatoire généré pour la session.

**Pour limiter la taille du cache de données sur le client**:

`Set-AppvClientConfiguration –ReportingDataCacheLimit 100`

Configure la taille maximale du cache de création de rapports sur l’ordinateur exécutant le client App-V 5,0 sur 100 Mo. Si la limite du cache est atteinte avant que les données soient envoyées au serveur, le journal est restauré et les données sont écrasées si nécessaire.

**Pour configurer la taille du bloc de données transmises sur le réseau entre le client et le serveur**:

`Set-AppvClientConfiguration –ReportingDataBlockSize 10240`

Spécifie le bloc de données maximal que le client envoie à 10240 Mo.

### Types de données collectées

Le tableau suivant répertorie les types d’informations que vous pouvez collecter à l’aide de la création de rapports App-V 5,0.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Informations client</th>
<th align="left">Informations de package</th>
<th align="left">Utilisation des applications</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nom d’hôte</p></td>
<td align="left"><p>Nom du package</p></td>
<td align="left"><p>Heures de début et de fin</p></td>
</tr>
<tr class="even">
<td align="left"><p>Version du client App-V 5,0</p></td>
<td align="left"><p>Version du package</p></td>
<td align="left"><p>État d’exécution</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Architecture de processeur</p></td>
<td align="left"><p>Source du package</p></td>
<td align="left"><p>État d’arrêt</p></td>
</tr>
<tr class="even">
<td align="left"><p>Version du système d’exploitation</p></td>
<td align="left"><p>Pourcentage mis en cache</p></td>
<td align="left"><p>Nom de l’application</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Niveau de Service Pack</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Version de l’application</p></td>
</tr>
<tr class="even">
<td align="left"><p>Type de système d’exploitation</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Nom d’utilisateur</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Groupe de connexion</p></td>
</tr>
</tbody>
</table>
 


Le client recueille et enregistre les données dans un format **. xml** . Le cache des données est masqué par défaut et nécessite des droits d’administrateur pour ouvrir le fichier XML.

### Envoyer des données au serveur

Vous pouvez configurer l’ordinateur qui exécute le client App-V 5,0 pour envoyer automatiquement des données au serveur de rapports spécifié. Pour spécifier le serveur, utilisez l’applet de commande **Set-AppvClientConfiguration** avec les paramètres suivants:

-   ReportingEnabled

-   ReportingServerURL

-   ReportingStartTime

-   ReportingInterval

-   ReportingRandomDelay

Après avoir configuré les paramètres précédents, vous devez créer une tâche planifiée. La tâche planifiée contactera le serveur spécifié par le paramètre **ReportingServerURL** et lancera le transfert. Si vous voulez envoyer les données manuellement en dehors des heures prévues, utilisez l’applet de commande PowerShell suivante:

`Send-AppVClientReport –URL http://MyReportingServer:MyPort/ -DeleteOnSuccess`

Si le serveur de création de rapports a été configuré précédemment, le paramètre **– URL** peut être omis. Si les données doivent être envoyées à un autre emplacement, vous pouvez aussi spécifier une autre URL pour remplacer le **ReportingServerURL** configuré pour cette collection de données.

Le paramètre **-DeleteOnSuccess** indique que si le transfert est réussi, le cache des données est alors effacé. Si cette valeur n’est pas spécifiée, le cache ne sera pas vidé.

### Collection de données manuelle

Vous pouvez également utiliser l’applet de passe **Send-AppVClientReport** pour collecter des données manuellement. Cette solution est utile avec ou sans serveur de création de rapports existant. La liste suivante présente des informations sur la collecte de données avec ou sans serveur de rapports.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Avec un serveur de création de rapports</th>
<th align="left">Sans serveur de création de rapports</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Si vous disposez d’un serveur de création de rapports App-V 5,0, créez une tâche planifiée ou un script personnalisé. Spécifiez que le client envoie les données à l’emplacement spécifié avec la fréquence de votre choix.</p></td>
<td align="left"><p>Si vous n’avez pas de serveur de création de rapports App-V 5,0, utilisez le <strong> paramètre – URL </strong> pour envoyer les données vers un partage spécifié. Exemple:</p>
<p><code>Send-AppVClientReport –URL \Myshare\MyData\ -DeleteOnSuccess</code></p>
<p>L’exemple précédent envoie les données de rapport à <strong> l' &lt; emplacement \MyShare\MyData/Strong &gt; indiqué par le <strong> paramètre-URL </strong> . Après l’envoi des données, le cache est vidé.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>S’il s’agit d’un emplacement autre que le serveur de création de rapports, les données sont envoyées au <strong> format. XML sans </strong> traitement supplémentaire.</p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### Création de rapports

Pour récupérer des informations de rapport et créer des rapports à l’aide de App-V 5,0, vous devez utiliser l’une des méthodes suivantes:

-   **Microsoft SQL Server Reporting Services (SSRS)** -Microsoft SQL Server Reporting Services est disponible avec Microsoft SQL Server. SSRS n’est pas installé lors de l’installation de l’App-V 5,0 Reporting Server. Il doit être déployé séparément pour générer les rapports associés.

    Utilisez le lien suivant pour plus d’informations sur l’utilisation de [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596).

-   **Écriture de scripts** – vous pouvez générer des rapports en effectuant des scripts directement sur la base de données de création de rapports App-V 5,0. Exemple:

    **Procédure stockée:**

    **spProcessClientReport** est programmé pour s’exécuter sur minuit ou 12:00 AM.

    Pour exécuter la procédure stockée planifiée Microsoft SQL Server, l’agent Microsoft SQL Server doit être en cours d’exécution. Assurez-vous que l’agent Microsoft SQL Server est défini sur **démarrage automatique**. Pour plus d’informations, reportez-vous à [démarrage automatique de l’agent SQL Server (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).

    La procédure stockée est également créée lors de l’utilisation des scripts de base de données App-V 5,0.

Vous devez également vous assurer que les **connexions concomitantes** du service Web serveur de création de rapports sont définies sur une valeur que le serveur pourra gérer sans influer sur la disponibilité. Le nombre maximal de **connexions simultanées autorisées** pour le **service Web de création de rapports** est **10 000**.






## Rubriques connexes


[Déploiement du serveur App-V5.0](deploying-the-app-v-50-server.md)

[Comment installer le serveur de rapports sur un ordinateur autonome et le connecter à la base de données](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database.md)

 

 





