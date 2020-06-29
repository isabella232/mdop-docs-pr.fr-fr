---
title: Comment déployer App-V Client
description: Comment déployer App-V Client
author: dansimp
ms.assetid: 981f57c9-56c3-45da-8261-0972bfad3e5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ea216f6b86820f752e0c0ac693470eac72cb847a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805491"
---
# Comment déployer App-V Client


Utilisez la procédure suivante pour installer le client Microsoft Application Virtualization (App-V) 5,1 et le client services Bureau à distance. Vous devez installer la version du client qui correspond au système d’exploitation de l’ordinateur cible.

<a href="" id="bkmk-clt-install-prereqs"></a>**Que faire avant de commencer**

1. Passez en revue et installez les logiciels requis:

   Installez les logiciels requis correspondant à la version d’App-V que vous installez:

   -   [À propos d'App-V5.1](about-app-v-51.md)

   -   [Composants requis d'App-V5.1](app-v-51-prerequisites.md)

2. Passez en revue la coexistence du client et les scénarios non pris en charge, comme le concernent votre installation:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Déploiement de clients App-V de coexistence</p></td>
   <td align="left"><p><a href="planning-for-the-app-v-51-sequencer-and-client-deployment.md" data-raw-source="[Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md)">Planification du déploiement d'App-V5.1 Sequencer et Client</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Scénarios d’installation non pris en charge ou limités</p></td>
   <td align="left"><p>Voir la section client dans les <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> configurations App-V 5,1 prises en charge</a></p></td>
   </tr>
   </tbody>
   </table>



3. Passez en revue les emplacements du Registre, du journal et des informations de dépannage du client:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Informations de Registre du client</p></td>
<td align="left"><ul>
<li><p>Par défaut, après avoir installé le client App-V 5,1, les informations sur le client sont stockées dans le registre dans la clé de Registre suivante:</p>
<p><strong>HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT</strong></p></li>
<li><p>Lorsque vous déployez un package virtualisé sur un ordinateur exécutant le client App-V, les données de package associées sont stockées à l’emplacement suivant:</p>
<p><strong>C: \ ProgramData \ App-V</strong></p>
<p>Toutefois, vous pouvez reconfigurer cet emplacement avec la clé de Registre suivante:</p>
<p><strong>HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT \ STREAMING \ PACKAGEINSTALLATIONROOT</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Fichiers journaux du client</p></td>
<td align="left"><ul>
<li><p>Pour les informations de fichier journal associées au client App-V 5,1, recherchez dans le journal suivant:</p>
<p><strong>Journaux d’événements/applications et journaux de services/Microsoft/AppV</strong></p></li>
<li><p>Dans App-V 5,0 SP3, certains journaux ont été consolidés et déplacés vers l’emplacement suivant:</p>
<p><strong>Journaux d’événements/applications et services journaux de Microsoft/AppV/ServiceLog</strong></p>
<p>Pour obtenir la liste des journaux déplacés, voir <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)"> à propos de App-V 5,0 SP3 </a> .</p></li>
<li><p>Les packages actuellement stockés sur des ordinateurs exécutant le client App-V 5,1 sont enregistrés à l’emplacement suivant:</p>
<p><strong>C:\ProgramData\App-V &amp; lt; ID de package &gt; &amp; lt; ID de version&gt;</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Informations de résolution des problèmes d’installation du client</p></td>
<td align="left"><p>Consultez le journal des erreurs dans le <strong> dossier% Temp% </strong> . Pour passer en revue les fichiers journaux, cliquez sur <strong> Démarrer </strong> , tapez <strong> % temp% </strong> , puis recherchez le <strong> Journal de appv_ </strong> .</p></td>
</tr>
</tbody>
</table>



**Pour installer le client App-V 5,1**

1.  Copiez le fichier d’installation du client App-V 5,1 sur l’ordinateur sur lequel il est installé. Choisissez l’une des méthodes suivantes:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Type de client</th>
    <th align="left">Fichier à utiliser</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Version standard du client</p></td>
    <td align="left"><p><strong>appv_client_setup.exe</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Version du service bureau à distance du client</p></td>
    <td align="left"><p><strong>appv_client_setup_rds.exe</strong></p></td>
    </tr>
    </tbody>
    </table>



2.  Double-cliquez sur le fichier d’installation, puis cliquez sur **installer**. Avant le début de l’installation, le programme d’installation vérifie que l’ordinateur ne contient aucune [Configuration requise pour App-V 5,1](app-v-51-prerequisites.md).

3.  Passez en revue et acceptez les termes du contrat de licence logiciel, spécifiez si vous souhaitez utiliser Microsoft Update et si vous souhaitez participer au programme d’amélioration de l’utilisation de Microsoft, puis cliquez sur **installer**.

4.  Dans la page **Configuration terminée** , cliquez sur **Fermer**.

    L’installation crée les entrées suivantes pour le client App-V dans les **programmes**:

    -   **.exe**

    -   **.msi**

    -   **module linguistique**

        **Remarque**  
        Après l’installation, seul le fichier. exe peut être désinstallé.



**Pour installer le client App-V 5,1 à l’aide d’un script**

1. Installez tous les logiciels requis requis sur les ordinateurs cibles. Apprenez [à faire avant de commencer](#bkmk-clt-install-prereqs). Si vous installez le client à l’aide d’un fichier. msi, l’installation échoue si une configuration requise est manquante.

2. Pour utiliser un script pour installer le client App-V 5,1, utilisez les paramètres suivants avec **appv\_client\_setup.exe**.

   **Remarque**  
   Le client Windows Installer (. msi) prend en charge le même ensemble de commutateurs, à l’exception du paramètre **/log** .

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p>/INSTALLDIR</p></td>
   <td align="left"><p>Spécifie le répertoire d’installation. Exemple d’utilisation: <strong> /INSTALLDIR = C:\Program Files\AppV client</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/CEIPOPTIN</p></td>
   <td align="left"><p>Permet de participer au programme d’amélioration du produit. Exemple d’utilisation: <strong> /CEIPOPTIN = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/MUOPTIN</p></td>
   <td align="left"><p>Active Microsoft Update. Exemple d’utilisation: <strong> /MUOPTIN = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/PACKAGEINSTALLATIONROOT</p></td>
   <td align="left"><p>Spécifie le répertoire dans lequel installer toutes les nouvelles applications et mises à jour. Exemple d’utilisation: <strong> /PACKAGEINSTALLATIONROOT =&#39;C:\App-V Packages&#39;</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/PACKAGESOURCEROOT</p></td>
   <td align="left"><p>Remplace l’emplacement source pour le téléchargement du contenu du package. Exemple d’utilisation: <strong> /PACKAGESOURCEROOT =&#39;<a href="http://packageStore" data-raw-source="http://packageStore"> http://packageStore </a>&#39;</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/AUTOLOAD</p></td>
   <td align="left"><p>Spécifie la façon dont les nouveaux packages sont chargés par App-V 5,1 sur un ordinateur spécifique. Les options suivantes sont activées: [1]; Chargez automatiquement tous les packages [2]; ou ne chargez pas automatiquement les packages [0]. <strong> Exemple d’utilisation:/AUTOLOAD = [0 | 1 | 2]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/SHAREDCONTENTSTOREMODE</p></td>
   <td align="left"><p>Spécifie que le contenu du package en flux ne sera pas enregistré sur le disque dur local. Exemple d’utilisation: <strong> /SHAREDCONTENTSTOREMODE = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/MIGRATIONMODE</p></td>
   <td align="left"><p>Permet au client App-V 5,1 de modifier les raccourcis et FTAs associés aux packages créés avec une version précédente. Exemple d’utilisation: <strong> /MIGRATIONMODE = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ENABLEPACKAGESCRIPTS</p></td>
   <td align="left"><p>Active les scripts qui sont définis dans le fichier manifeste de package ou les fichiers de configuration qui doivent s’exécuter. Exemple d’utilisation: <strong> /ENABLEPACKAGESCRIPTS = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/ROAMINGREGISTRYEXCLUSIONS</p></td>
   <td align="left"><p>Spécifie les chemins de Registre qui ne sont pas itinérants avec un profil utilisateur. Exemple d’utilisation: <strong> /ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ROAMINGFILEEXCLUSIONS</p></td>
   <td align="left"><p>Spécifie les chemins d’accès relatifs au fichier% UserProfile% qui ne sont pas itinérants avec un profil utilisateur&#39;s. Exemple d’utilisation: <strong> /ROAMINGFILEEXCLUSIONS &#39;ordinateur de bureau; mes images&#39;</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] PUBLISHINGSERVERNAME</p></td>
   <td align="left"><p>Affiche le nom du serveur de publication. Exemple d’utilisation: <strong> /S2PUBLISHINGSERVERNAME = MyPublishingServer</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] PUBLISHINGSERVERURL</p></td>
   <td align="left"><p>Affiche l’URL du serveur de publication. Exemple d’utilisation: <strong> /S2PUBLISHINGSERVERURL = \pubserver</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] GLOBALREFRESHENABLED-</p></td>
   <td align="left"><p>Autorise une actualisation globale de la publication. Exemple d’utilisation: <strong> /S2GLOBALREFRESHENABLED = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] GLOBALREFRESHONLOGON</p></td>
   <td align="left"><p>Lance une actualisation globale de la publication lors de la connexion d’un utilisateur. Exemple d’utilisation: <strong> /S2LOGONREFRESH = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] GLOBALREFRESHINTERVAL-</p></td>
   <td align="left"><p>Spécifie l’intervalle d’actualisation de publication, où <strong> 0 </strong> indique ne pas actualiser régulièrement. Exemple d’utilisation: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] GLOBALREFRESHINTERVALUNIT</p></td>
   <td align="left"><p>Spécifie l’unité d’intervalle (heures [0], jours [1]). Exemple d’utilisation: <strong> /S2GLOBALREFRESHINTERVALUNIT = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] USERREFRESHENABLED</p></td>
   <td align="left"><p>Active l’actualisation de la publication. Exemple d’utilisation: <strong> /S2USERREFRESHENABLED = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] USERREFRESHONLOGON</p></td>
   <td align="left"><p>Lance une actualisation de la publication des utilisateurs quand un utilisateur se connecte. Exemple d’utilisation: <strong> /S2LOGONREFRESH = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] USERREFRESHINTERVAL-</p></td>
   <td align="left"><p>Spécifie l’intervalle d’actualisation de publication, où <strong> 0 </strong> indique ne pas actualiser régulièrement. Exemple d’utilisation: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] USERREFRESHINTERVALUNIT</p></td>
   <td align="left"><p>Spécifie l’unité d’intervalle (heures [0], jours [1]). Exemple d’utilisation: <strong> /S2USERREFRESHINTERVALUNIT = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/Log</p></td>
   <td align="left"><p>Spécifie un emplacement où les informations du journal sont enregistrées. L’emplacement par défaut est% Temp%. Exemple d’utilisation: <strong> /log C:\logs\log.log</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>établit</p></td>
   <td align="left"><p>Spécifie une installation sans assistance.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/REPAIR</p></td>
   <td align="left"><p>Répare une installation précédente d’un client.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/NORESTART</p></td>
   <td align="left"><p>Empêche l’ordinateur de redémarrer après l’installation du client.</p>
   <p>Ce paramètre empêche l’ordinateur de l’utilisateur final de redémarrer après l’installation de chaque mise à jour et vous permet de planifier le redémarrage à votre convenance. Par exemple, vous pouvez installer App-V 5,1, puis installer le package de correctif Y sans redémarrer après l’installation du Service Pack. Après l’installation, vous devez redémarrer avant de commencer à utiliser App-V.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/UNINSTALL</p></td>
   <td align="left"><p>Désinstalle le client.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ACCEPTEULA</p></td>
   <td align="left"><p>Accepter le contrat de licence. Ce type de fichier est requis pour une installation sans assistance. Exemple d’utilisation: <strong> /AcceptEULA </strong> ou <strong> /ACCEPTEULA = 1 </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/LAYOUT</p></td>
   <td align="left"><p>Spécifie l’action de disposition associée. Il extrait également les fichiers Windows Installer (. msi) et script dans un dossier sans installer App-V 5,1. Aucune valeur n’est attendue.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/LAYOUTDIR</p></td>
   <td align="left"><p>Spécifie le répertoire de disposition. Nécessite une valeur de chaîne. Exemple d’utilisation: <strong> /LAYOUTDIR = «client de virtualisation C:\Application» </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/?,/h,/Help</p></td>
   <td align="left"><p>Demande des informations sur les paramètres d’installation précédents.</p></td>
   </tr>
   </tbody>
   </table>



**Pour installer le client App-V 5,1 à l’aide du fichier Windows Installer (. msi)**

1.  Installez les prérequis requis sur les ordinateurs cibles. Apprenez [à faire avant de commencer](#bkmk-clt-install-prereqs). Si une configuration requise n’est pas respectée, l’installation échoue.

2.  Assurez-vous que les ordinateurs cibles ne disposent pas de redémarrages en attente avant de procéder à l’installation du client à l’aide des fichiers App-V 5,1 Windows Installer (. msi). Les fichiers Windows Installer n’indicateur pas de redémarrage en attente.

3.  Déploiement de l’un des fichiers Windows Installer suivants sur l’ordinateur cible. Le fichier que vous spécifiez doit correspondre à la configuration de l’ordinateur cible.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Type de déploiement</th>
    <th align="left">Déployer ce fichier</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Un ordinateur exécute un système d’exploitation Microsoft Windows 32 bits</p></td>
    <td align="left"><p>appv_client_MSI_x86.msi</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Un ordinateur exécute un système d’exploitation Microsoft Windows 64 bits</p></td>
    <td align="left"><p>appv_client_MSI_x64.msi</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Vous déployez le client App-V 5,1 Remote Desktop Services</p></td>
    <td align="left"><p>appv_client_rds_MSI_x64.msi</p></td>
    </tr>
    </tbody>
    </table>



4.  En utilisant les informations figurant dans le tableau suivant, sélectionnez le module linguistique approprié **. msi** à installer en fonction de la langue souhaitée pour l’ordinateur cible. Les **xxxx** du tableau font référence aux paramètres régionaux cibles du module linguistique.

    **Ce que vous devez savoir avant de commencer:**

    -   Les modules linguistiques sont communs au client App-V 5,1 standard et à la version Service Bureau à distance du client App-V 5,1.

    -   Si vous installez le client App-V 5,1 à l’aide du fichier **. exe**, le programme d’installation déploiera uniquement le module linguistique correspondant au système d’exploitation exécuté sur l’ordinateur cible.

    -   Pour déployer des modules linguistiques supplémentaires sur un ordinateur cible, utilisez la procédure **d’installation du client App-V 5,1 à l’aide du fichier Windows Installer (. msi)**.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Type de déploiement</th>
    <th align="left">Déployer ce fichier</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Un ordinateur exécute un système d’exploitation Microsoft Windows 32 bits</p></td>
    <td align="left"><p>x86.msi appv_client_LP_xxxx_</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Un ordinateur exécute un système d’exploitation Microsoft Windows 64 bits</p></td>
    <td align="left"><p>x64.msi appv_client_LP_xxxx_</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Rubriques connexes


[Déploiement d'App-V5.1](deploying-app-v-51.md)

[À propos des paramètres de configuration du client](about-client-configuration-settings51.md)

[Désinstallation d'App-V5.1 Client](how-to-uninstall-the-app-v-51-client.md)









