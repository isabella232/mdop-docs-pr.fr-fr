---
title: Comment déployer App-V Client
description: Comment déployer App-V Client
ms.author: dansimp
author: dansimp
ms.assetid: 9c4e67ae-ddaf-4e23-8c16-72d029a74a27
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/05/2018
ms.openlocfilehash: 4e246e13bf59f167eade77200afd866c6a3c41fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805490"
---
# Comment déployer App-V Client


Utilisez la procédure suivante pour installer le client Microsoft Application Virtualization (App-V) 5,0 et le client services Bureau à distance. Vous devez installer la version du client qui correspond au système d’exploitation de l’ordinateur cible.

<a href="" id="bkmk-clt-install-prereqs"></a>**Que faire avant de commencer**

1. Passez en revue et installez les logiciels requis:

   Installez les logiciels requis correspondant à la version d’App-V que vous installez:

   - [À propos d'App-V5.0 SP3](about-app-v-50-sp3.md)

   - App-V 5,0 SP1 et App-V 5,0 SP2 – aucune nouveauté requise dans ces versions

   - [Composants requis d'App-V5.0](app-v-50-prerequisites.md)

2. Passez en revue la coexistence du client et les scénarios non pris en charge, comme le concernent votre installation:


   |                                               |                                                                                                                            |
   |-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
   |      Déploiement de clients App-V de coexistence       | [Planification du déploiement d'App-V5.0 Sequencer et Client](planning-for-the-app-v-50-sequencer-and-client-deployment.md) |
   | Scénarios d’installation non pris en charge ou limités |                         [Configurations prises en charge d'App-V5.0](app-v-50-supported-configurations.md)                         |

   ---

3. Passez en revue les emplacements du Registre, du journal et des informations de dépannage du client:

#### Informations de Registre du client
<ul><li>Par défaut, après avoir installé le client App-V 5,0, les informations sur le client sont stockées dans le registre dans la clé de Registre suivante:<p><p><code>HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\APPV\CLIENT</code></li><li>Lorsque vous déployez un package virtualisé sur un ordinateur exécutant le client App-V, les données de package associées sont stockées à l’emplacement suivant:<p><p><code>C:\ProgramData\App-V</code><p><p>Toutefois, vous pouvez reconfigurer cet emplacement avec la clé de Registre suivante:<p><p><code>HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\SOFTWARE\MICROSOFT\APPV\CLIENT\STREAMING\PACKAGEINSTALLATIONROOT</code></li></ul>

#### Fichiers journaux du client                  
<ul><li>Pour les informations de fichier journal associées au client App-V 5,0, recherchez dans le journal suivant:<p><p><code>Event logs/Applications and Services Logs/Microsoft/AppV</code></li><li>Dans App-V 5,0 SP3, certains journaux ont été consolidés et déplacés vers l’emplacement suivant:<p><p><code>Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog</code><p><p>Pour obtenir la liste des journaux déplacés, voir [à propos de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</li><li>Les packages actuellement stockés sur des ordinateurs exécutant le client App-V 5,0 sont enregistrés à l’emplacement suivant:<p><p><code>C:\ProgramData\App-V\<<em>package id</em>>\<<em>version id</em>></code></li></ul>

#### Informations de résolution des problèmes d’installation du client
- Consultez le journal des erreurs dans le dossier **% temp%** . 
- Pour passer en revue les fichiers journaux, cliquez sur **Démarrer**, tapez **% temp%**, puis recherchez le **Journal de appv_**. 

## Pour installer le client App-V 5,0

1. Copiez le fichier d’installation du client App-V 5,0 sur l’ordinateur sur lequel il est installé.<p><p>Choisissez l’une des méthodes suivantes:


   |                  Type de client                  |          Fichier à utiliser          |
   |-----------------------------------------------|-------------------------------|
   |        Version standard du client         |   **appv_client_setup.exe**   |
   | Version du service bureau à distance du client | **appv_client_setup_rds.exe** |

   ---

2. Double-cliquez sur le fichier d’installation, puis cliquez sur **installer**. Avant le début de l’installation, le programme d’installation vérifie que l’ordinateur ne contient aucune [Configuration requise pour App-V 5,0](app-v-50-prerequisites.md).

3. Passez en revue et acceptez les termes du contrat de licence logiciel, spécifiez si vous souhaitez utiliser Microsoft Update et si vous souhaitez participer au programme d’amélioration de l’utilisation de Microsoft, puis cliquez sur **installer**.

4. Dans la page **Configuration terminée** , cliquez sur **Fermer**.

   L’installation crée les entrées suivantes pour le client App-V dans les **programmes**:

   -   **.exe**

   -   **.msi**

   -   **module linguistique**

   >[!NOTE]
   >Après l’installation, seul le fichier. exe peut être désinstallé.


## Pour installer le client App-V 5,0 à l’aide d’un script

1. Installez tous les logiciels requis requis sur les ordinateurs cibles. Apprenez [à faire avant de commencer](#bkmk-clt-install-prereqs). Si vous installez le client à l’aide d’un fichier. msi, l’installation échoue si une configuration requise est manquante.

2. Pour utiliser un script pour installer le client App-V 5,0, utilisez les paramètres suivants avec **appv\_client\_setup.exe**.

   >[!NOTE]
   >Le client Windows Installer (. msi) prend en charge le même ensemble de commutateurs, à l’exception du paramètre **/log** .

   |                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                     |
   |----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |           /INSTALLDIR            |                                                                                                                                                               Spécifie le répertoire d’installation. Exemple d’utilisation:<p><p>**/INSTALLDIR = C:\Program Files\AppV client**                                                                                                                                                                |
   |            /CEIPOPTIN            |                                                                                                                                                          Permet de participer au programme d’amélioration du produit. Exemple d’utilisation:<p><p>**/CEIPOPTIN = [0 \ | 1 \]**                                                                                                                                                           |
   |             /MUOPTIN             |                                                                                                                                                                                 Active Microsoft Update. Exemple d’utilisation:<p><p>**/MUOPTIN = [0 \ | 1 \]**                                                                                                                                                                                  |
   |     /PACKAGEINSTALLATIONROOT     |                                                                                                                                         Spécifie le répertoire dans lequel installer toutes les nouvelles applications et mises à jour. Exemple d’utilisation: <p><p>**/PACKAGEINSTALLATIONROOT = 'packages C:\App-V'**                                                                                                                                         |
   |        /PACKAGESOURCEROOT        |                                                                                                                                                  Remplace l’emplacement source pour le téléchargement du contenu du package. Exemple d’utilisation:<p><p>**/PACKAGESOURCEROOT = ' <http://packageStore> '**                                                                                                                                                  |
   |            /AUTOLOAD             |                                                                                           Spécifie la façon dont les nouveaux packages sont chargés par App-V 5,0 sur un ordinateur spécifique. Les options suivantes sont activées: [1]; Chargez automatiquement tous les packages [2]; ou ne chargez pas automatiquement les packages [0]. Exemple d’utilisation:<p><p>**/AUTOLOAD = [0 \ | 1 \ | 2 \]**                                                                                           |
   |     /SHAREDCONTENTSTOREMODE      |                                                                                                                                           Spécifie que le contenu du package en flux ne sera pas enregistré sur le disque dur local. Exemple d’utilisation: <p><p>**/SHAREDCONTENTSTOREMODE = [0 \ | 1 \]**                                                                                                                                            |
   |          /MIGRATIONMODE          |                                                                                                                     Permet au client App-V 5,0 de modifier les raccourcis et FTAs associés aux packages créés avec une version précédente. Exemple d’utilisation:<p><p>**/MIGRATIONMODE = [0 \ | 1 \]**                                                                                                                     |
   |      /ENABLEPACKAGESCRIPTS       |                                                                                                                                   Active les scripts qui sont définis dans le fichier manifeste de package ou les fichiers de configuration qui doivent s’exécuter. Exemple d’utilisation:<p><p>**/ENABLEPACKAGESCRIPTS = [0 \ | 1 \]**                                                                                                                                   |
   |    /ROAMINGREGISTRYEXCLUSIONS    |                                                                                                                                      Spécifie les chemins de Registre qui ne sont pas itinérants avec un profil utilisateur. Exemple d’utilisation:<p><p>**/ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients**                                                                                                                                      |
   |      /ROAMINGFILEEXCLUSIONS      |                                                                                                                                  Spécifie les chemins d’accès relatifs au fichier% UserProfile% qui ne suivent pas le profil d’un utilisateur. Exemple d’utilisation: <p><p>**/ROAMINGFILEEXCLUSIONS’bureau; mes images'**                                                                                                                                   |
   |   /S [1-5] PUBLISHINGSERVERNAME    |                                                                                                                                                           Affiche le nom du serveur de publication. Exemple d’utilisation:<p><p>**/S2PUBLISHINGSERVERNAME = MyPublishingServer**                                                                                                                                                            |
   |    /S [1-5] PUBLISHINGSERVERURL    |                                                                                                                                                                Affiche l’URL du serveur de publication. Exemple d’utilisation:<p><p>**/S2PUBLISHINGSERVERURL = \\pubserver**                                                                                                                                                                |
   |   /S [1-5] GLOBALREFRESHENABLED    |                                                                                                                                                                    Autorise une actualisation globale de la publication. Exemple d’utilisation:<p><p>**/S2GLOBALREFRESHENABLED = [0 \ | 1 \]**                                                                                                                                                                     |
   |   /S [1-5] GLOBALREFRESHONLOGON    |                                                                                                                                                             Lance une actualisation globale de la publication lors de la connexion d’un utilisateur. Exemple d’utilisation:<p><p>**/S2LOGONREFRESH = [0 \ | 1 \]**                                                                                                                                                              |
   |   /S [1-5] GLOBALREFRESHINTERVAL   |                                                                                                                                         Spécifie l’intervalle d’actualisation de publication, où **0** indique ne pas actualiser régulièrement. Exemple d’utilisation: **/S2PERIODICREFRESHINTERVAL = [0-744]**                                                                                                                                         |
   | /S [1-5] GLOBALREFRESHINTERVALUNIT |                                                                                                                                                            Spécifie l’unité d’intervalle (heures [0], jours [1]). Exemple d’utilisation:<p><p>**/S2GLOBALREFRESHINTERVALUNIT = [0 \ | 1 \]**                                                                                                                                                            |
   |    /S [1-5] USERREFRESHENABLED     |                                                                                                                                                                          Active l’actualisation de la publication. Exemple d’utilisation: **/S2USERREFRESHENABLED = [0 \ | 1 \]**                                                                                                                                                                          |
   |    /S [1-5] USERREFRESHONLOGON     |                                                                                                                                                              Lance une actualisation de la publication des utilisateurs quand un utilisateur se connecte. Exemple d’utilisation:<p><p>**/S2LOGONREFRESH = [0 \ | 1 \]**                                                                                                                                                               |
   |    /S [1-5] USERREFRESHINTERVAL    |                                                                                                                                         Spécifie l’intervalle d’actualisation de publication, où **0** indique ne pas actualiser régulièrement. Exemple d’utilisation: **/S2PERIODICREFRESHINTERVAL = [0-744]**                                                                                                                                         |
   |  /S [1-5] USERREFRESHINTERVALUNIT  |                                                                                                                                                             Spécifie l’unité d’intervalle (heures [0], jours [1]). Exemple d’utilisation:<p><p>**/S2USERREFRESHINTERVALUNIT = [0 \ | 1 \]**                                                                                                                                                             |
   |               /Log               |                                                                                                                                                Spécifie un emplacement où les informations du journal sont enregistrées. L’emplacement par défaut est% Temp%. Exemple d’utilisation:<p><p>**/log C:\logs\log.log**                                                                                                                                                |
   |                établit                |                                                                                                                                                                                                Spécifie une installation sans assistance.                                                                                                                                                                                                |
   |             /REPAIR              |                                                                                                                                                                                               Répare une installation précédente d’un client.                                                                                                                                                                                               |
   |            /NORESTART            | Empêche l’ordinateur de redémarrer après l’installation du client.<p><p>Ce paramètre empêche l’ordinateur de l’utilisateur final de redémarrer après l’installation de chaque mise à jour et vous permet de planifier le redémarrage à votre convenance. Par exemple, vous pouvez installer App-V 5,0 SPX, puis installer le package de correctifs Y sans redémarrer après l’installation du Service Pack. Après l’installation, vous devez redémarrer avant de commencer à utiliser App-V. |
   |            /UNINSTALL            |                                                                                                                                                                                                       Désinstalle le client.                                                                                                                                                                                                        |
   |           /ACCEPTEULA            |                                                                                                                                              Accepter le contrat de licence. Ce type de fichier est requis pour une installation sans assistance. Exemple d’utilisation:<p><p>**/AcceptEULA** ou **/ACCEPTEULA = 1**                                                                                                                                               |
   |             /LAYOUT              |                                                                                                                               Spécifie l’action de disposition associée. Il extrait également les fichiers Windows Installer (. msi) et script dans un dossier sans installer App-V 5,0. Aucune valeur n’est attendue.                                                                                                                                |
   |            /LAYOUTDIR            |                                                                                                                                                 Spécifie le répertoire de disposition. Nécessite une valeur de chaîne. Exemple d’utilisation:<p><p>**/LAYOUTDIR = "client de virtualisation C:\Application"**                                                                                                                                                  |
   |          /?,/h,/Help           |                                                                                                                                                                                      Demande des informations sur les paramètres d’installation précédents.                                                                                                                                                                                      |

   ---

## Pour installer le client App-V 5,0 à l’aide du fichier Windows Installer (. msi)

1. Installez les prérequis requis sur les ordinateurs cibles. Apprenez [à faire avant de commencer](#bkmk-clt-install-prereqs). Si une configuration requise n’est pas respectée, l’installation échoue.

2. Assurez-vous que les ordinateurs cibles ne disposent pas de redémarrages en attente avant de procéder à l’installation du client à l’aide des fichiers App-V 5,0 Windows Installer (. msi). Les fichiers Windows Installer n’indicateur pas de redémarrage en attente.

3. Déploiement de l’un des fichiers Windows Installer suivants sur l’ordinateur cible. Le fichier que vous spécifiez doit correspondre à la configuration de l’ordinateur cible.


   |                       Type de déploiement                        |      Déployer ce fichier       |
   |-----------------------------------------------------------------|-----------------------------|
   | Un ordinateur exécute un système d’exploitation Microsoft Windows 32 bits |   appv_client_MSI_x86.msi   |
   | Un ordinateur exécute un système d’exploitation Microsoft Windows 64 bits |   appv_client_MSI_x64.msi   |
   | Vous déployez le client App-V 5,0 Remote Desktop Services  | appv_client_rds_MSI_x64.msi |

   ---

4. En utilisant les informations figurant dans le tableau suivant, sélectionnez le module linguistique approprié **. msi** à installer en fonction de la langue souhaitée pour l’ordinateur cible. Les **xxxx** du tableau font référence aux paramètres régionaux cibles du module linguistique.

   **Ce que vous devez savoir avant de commencer:** 

   -  Les modules linguistiques sont communs au client App-V 5,0 standard et à la version Service Bureau à distance du client App-V 5,0.

   -  Si vous installez le client App-V 5,0 à l’aide du fichier **. exe**, le programme d’installation déploiera uniquement le module linguistique correspondant au système d’exploitation exécuté sur l’ordinateur cible.

   -  Pour déployer des modules linguistiques supplémentaires sur un ordinateur cible, utilisez la procédure **d’installation du client App-V 5,0 à l’aide du fichier Windows Installer (. msi)**.

   |                       Type de déploiement                        |       Déployer ce fichier       |
   |-----------------------------------------------------------------|------------------------------|
   | Un ordinateur exécute un système d’exploitation Microsoft Windows 32 bits | x86.msi appv_client_LP_xxxx_ |
   | Un ordinateur exécute un système d’exploitation Microsoft Windows 64 bits | x64.msi appv_client_LP_xxxx_ |

   ---

   Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction de [suggestions](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). <p><p>**Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Déploiement d'App-V5.0](deploying-app-v-50.md)

[À propos des paramètres de configuration du client](about-client-configuration-settings.md)

[Procédure pour désinstaller App-V5.0 Client](how-to-uninstall-the-app-v-50-client.md)
