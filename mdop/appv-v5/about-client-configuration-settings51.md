---
title: À propos des paramètres de configuration du client
description: À propos des paramètres de configuration du client
author: dansimp
ms.assetid: 18bb307a-7eda-4dd6-a83e-6afaefd99470
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb547eedf63bf165b1e8f5fd024839b3c2af3e4c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806108"
---
# À propos des paramètres de configuration du client


Le client Microsoft Application Virtualization (App-V) 5,1 stocke sa configuration dans le registre. Vous pouvez recueillir des informations utiles sur le client si vous comprenez le format des données dans le registre. Vous pouvez également configurer de nombreuses actions client en modifiant des entrées de registre. Cette rubrique répertorie les paramètres de configuration du client App-V 5,1 et explique leur utilisation. Vous pouvez utiliser PowerShell pour modifier les paramètres de configuration du client. Pour plus d’informations sur l’utilisation des applications PowerShell et App-V 5,1 [, voir administration d’App-v 5,1 à l’aide de PowerShell](administering-app-v-51-by-using-powershell.md).

## <a href="" id="---------app-v-5-1-client-configuration-settings"></a> Paramètres de configuration du client App-V 5,1


Le tableau suivant contient des informations sur les paramètres de configuration du client App-V 5,1:

|Nom du paramètre | Indicateur de configuration | Description | Définir des options | Valeur de clé de Registre | Clés et valeurs de l’état de stratégie désactivé |
|-------------|------------|-------------|-----------------|--------------------|--------------------------------------|
| PackageInstallationRoot | PACKAGEINSTALLATIONROOT | Spécifie le répertoire dans lequel toutes les nouvelles applications et mises à jour sont installées. | String | Streaming\PackageInstallationRoot | Valeur de stratégie non rédigée (comme non configuré) |
| PackageSourceRoot | PACKAGESOURCEROOT | Remplace l’emplacement source pour le téléchargement du contenu du package. | String | Streaming\PackageSourceRoot | Valeur de stratégie non rédigée (comme non configuré) |
| AllowHighCostLaunch | Non disponible. |Ce paramètre détermine si les applications virtualisées sont lancées sur des ordinateurs Windows 10 connectés par le biais d’une connexion réseau limitée (par exemple, 4G). | True (activé); Faux (état désactivé) | Streaming\AllowHighCostLaunch | 0,4 |
| ReestablishmentRetries | Non disponible. | Spécifie le nombre de tentatives de nouvelle session interrompue. | Entier (0-99) | Streaming\ReestablishmentRetries | Valeur de stratégie non rédigée (comme non configuré) |
| ReestablishmentInterval | Non disponible. | Spécifie le nombre de secondes entre les tentatives de rétablissement d’une session perdue. | Entier (0-3600) | Streaming\ReestablishmentInterval | Valeur de stratégie non rédigée (comme non configuré) |
| LocationProvider | Non disponible. | Spécifie le CLSID pour une implémentation compatible de l’interface IAppvPackageLocationProvider. | String | Streaming\LocationProvider | Valeur de stratégie non rédigée (comme non configuré) |
| CertFilterForClientSsl | Non disponible. | Spécifie le chemin d’accès d’un certificat valide dans le magasin de certificats. | String | Streaming\CertFilterForClientSsl | Valeur de stratégie non rédigée (comme non configuré) |
| VerifyCertificateRevocationList | Non disponible. | Vérifie l’état de révocation des certificats de serveur avant la transmission à l’aide de HTTPs. | True (activé); Faux (état désactivé) | Streaming\VerifyCertificateRevocationList | 0,4 |
| SharedContentStoreMode | SHAREDCONTENTSTOREMODE | Spécifie que le contenu du package en flux ne sera pas enregistré sur le disque dur local. | True (activé); Faux (état désactivé) | Streaming\SharedContentStoreMode | 0,4 |
| Nom<br>**Remarques** Ce paramètre ne peut pas être modifié à l’aide de l’applet de la cmdLet **Set-AppvclientConfiguration** . Vous devez utiliser l’applet **de cmdlet Set-AppvPublishingServer** . | PUBLISHINGSERVERNAME | Affiche le nom du serveur de publication. | String | Publishing\Servers\ {serverId} \ FriendlyName | Valeur de stratégie non rédigée (comme non configuré) |
| URL<br>**Remarques** Ce paramètre ne peut pas être modifié à l’aide de l’applet de la cmdLet **Set-AppvclientConfiguration** . Vous devez utiliser l’applet **de cmdlet Set-AppvPublishingServer** . | PUBLISHINGSERVERURL | Affiche l’URL du serveur de publication. | String | Publishing\Servers\ {serverId} \ URL | Valeur de stratégie non rédigée (comme non configuré) |
| GlobalRefreshEnabled<br>**Remarques** Ce paramètre ne peut pas être modifié à l’aide de l’applet de la cmdLet **Set-AppvclientConfiguration** . Vous devez utiliser l’applet **de cmdlet Set-AppvPublishingServer** . | GLOBALREFRESHENABLED | Active l’actualisation globale de la publication (booléen) | True (activé); Faux (état désactivé) | Publishing\Servers\ {serverId} \ GlobalEnabled | Faux |
| GlobalRefreshOnLogon<br>**Remarques** Ce paramètre ne peut pas être modifié à l’aide de l’applet de la cmdLet **Set-AppvclientConfiguration** . Vous devez utiliser l’applet **de cmdlet Set-AppvPublishingServer** . | GLOBALREFRESHONLOGON | Déclenche une actualisation globale de publication lors de l’ouverture de session. Expression | True (activé); Faux (état désactivé) | Publishing\Servers\ {serverId} \ GlobalLogonRefresh | Faux |
| GlobalRefreshInterval<br>**Remarques** Ce paramètre ne peut pas être modifié à l’aide de l’applet de la cmdLet **Set-AppvclientConfiguration** . Vous devez utiliser l’applet **de cmdlet Set-AppvPublishingServer** . | GLOBALREFRESHINTERVAL | Spécifie l’intervalle d’actualisation de publication à l’aide de GlobalRefreshIntervalUnit. Pour désactiver l’actualisation du package, sélectionnez 0. | Entier (0-744) | Publishing\Servers\ {serverId} \ GlobalPeriodicRefreshInterval | 0,4 |
| GlobalRefreshIntervalUnit <br>**Remarques** Ce paramètre ne peut pas être modifié à l’aide de l’applet de la cmdLet **Set-AppvclientConfiguration** . Vous devez utiliser l’applet **de cmdlet Set-AppvPublishingServer** . | GLOBALREFRESHINTERVALUNI | Spécifie l’unité de l’intervalle (heure 0-23, jour 0-31). | 0 pour l’heure, 1 pour le jour | Publishing\Servers\ {serverId} \ GlobalPeriodicRefreshIntervalUnit | 1 |
| UserRefreshEnabled<br>**Remarques** Ce paramètre ne peut pas être modifié à l’aide de l’applet de la cmdLet **Set-AppvclientConfiguration** . Vous devez utiliser l’applet **de cmdlet Set-AppvPublishingServer** . | USERREFRESHENABLED | Active l’actualisation de la publication des utilisateurs (booléen) | True (activé); Faux (état désactivé) | Publishing\Servers\ {serverId} \ UserEnabled | Faux |
| UserRefreshOnLogon<br>**Remarques** Ce paramètre ne peut pas être modifié à l’aide de l’applet de la cmdLet **Set-AppvclientConfiguration** . Vous devez utiliser l’applet **de cmdlet Set-AppvPublishingServer** . | USERREFRESHONLOGON | Déclenche une actualisation du ONLOGON de publication par un utilisateur. Expression<br>Statistiques (avec espaces): 60 | True (activé); Faux (état désactivé) | Publishing\Servers\ {serverId} \ UserLogonRefresh | Faux |
| UserRefreshInterval<br>**Remarques** Ce paramètre ne peut pas être modifié à l’aide de l’applet de la cmdLet **Set-AppvclientConfiguration** . Vous devez utiliser l’applet **de cmdlet Set-AppvPublishingServer** . | USERREFRESHINTERVAL | Spécifie l’intervalle d’actualisation de publication à l’aide de UserRefreshIntervalUnit. Pour désactiver l’actualisation du package, sélectionnez 0. | Statistiques (avec espaces): 85<br>Entier (0-744 heures) | Publishing\Servers\ {serverId} \ UserPeriodicRefreshInterval | 0,4 |
| UserRefreshIntervalUnit<br>**Remarques** Ce paramètre ne peut pas être modifié à l’aide de l’applet de la cmdLet **Set-AppvclientConfiguration** . Vous devez utiliser l’applet **de cmdlet Set-AppvPublishingServer** . | USERREFRESHINTERVALUNIT | Spécifie l’unité de l’intervalle (heure 0-23, jour 0-31). | 0 pour l’heure, 1 pour le jour | Publishing\Servers\ {serverId} \ UserPeriodicRefreshIntervalUnit | 1 |
| MigrationMode | MIGRATIONMODE | Le mode migration permet au client App-V de modifier des raccourcis et FTA pour les packages créés à l’aide d’une version antérieure d’App-V. | True (état activé); Faux (état désactivé) | Coexistence\MigrationMode | |
| CEIPOPTIN | CEIPOPTIN | Permet à l’ordinateur exécutant le client App-V 5,1 de collecter et de renvoyer des informations d’utilisation pour nous aider à améliorer l’application. | 0 pour désactivé; 1 pour activé | LOGICIEL/Microsoft/AppV/CEIP/CEIPEnable | 0,4 | 
| EnablePackageScripts | ENABLEPACKAGESCRIPTS | Active les scripts définis dans le manifeste du package de fichiers de configuration qui doivent s’exécuter. | True (activé); Faux (état désactivé) | \Scripting\EnablePackageScripts | | 
| RoamingFileExclusions | ROAMINGFILEEXCLUSIONS | Spécifie les chemins d’accès relatifs au fichier% UserProfile% qui ne suivent pas le profil d’un utilisateur. Exemple d’utilisation:/ROAMINGFILEEXCLUSIONS = 'bureau; mes images' | | | |
| RoamingRegistryExclusions | ROAMINGREGISTRYEXCLUSIONS | Spécifie les chemins de Registre qui ne sont pas itinérants avec un profil utilisateur. Exemple d’utilisation:/ROAMINGREGISTRYEXCLUSIONS = software\\classes; software\\clients | String | Integration\RoamingRegistryExclusions | Valeur de stratégie non rédigée (comme non configuré) |
| IntegrationRootUser | Non disponible. | Spécifie l’emplacement permettant de créer des liens symboliques associés à la version actuelle d’un package publié par utilisateur. toutes les extensions d’application virtuelles, par exemple les raccourcis clavier et les associations de types de fichiers, pointent vers ce chemin. Si vous ne spécifiez pas de chemin d’accès, les liens symboliques ne seront pas utilisés lors de la publication du package. Par exemple:%localappdata%\Microsoft\AppV\Client\Integration.| String | Integration\IntegrationRootUser | Valeur de stratégie non rédigée (comme non configuré) |
|IntegrationRootGlobal | Non disponible.| Spécifie l’emplacement permettant de créer des liens symboliques associés à la version actuelle d’un package publié globalement. toutes les extensions d’application virtuelles, par exemple les raccourcis clavier et les associations de types de fichiers, pointent vers ce chemin. Si vous ne spécifiez pas de chemin d’accès, les liens symboliques ne seront pas utilisés lors de la publication du package. Par exemple:%allusersprofile%\Microsoft\AppV\Client\Integration | String | Integration\IntegrationRootGlobal | Valeur de stratégie non rédigée (comme non configuré) |
| VirtualizableExtensions | Non disponible. | Liste délimitée par des virgules des extensions de nom de fichier qui peut être utilisée pour déterminer si une application installée localement peut être exécutée dans l’environnement virtuel.<br>Lors de la création de raccourcis, de FTAs et d’autres points d’extension lors de la publication, App-V compare l’extension de nom de fichier à la liste si l’application associée au point d’extension est installée localement. Si l’extension se trouve, le paramètre de ligne de commande **RunVirtual** est ajouté et l’application s’exécute quasiment.<br>Pour plus d’informations sur le paramètre **RunVirtual** , voir [exécution d’une application installée localement dans un environnement virtuel avec des applications virtualisées](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications51.md). | String | Integration\VirtualizableExtensions | Valeur de stratégie non écrite |
| ReportingEnabled | Non disponible. | Permet au client de renvoyer des informations vers un serveur de rapports. | True (activé); Faux (état désactivé) | Reporting\EnableReporting | Faux |
| ReportingServerURL | Non disponible. | Spécifie l’emplacement sur le serveur de création de rapports où les informations client sont enregistrées. | String | Reporting\ReportingServer | Valeur de stratégie non rédigée (comme non configuré) |
| ReportingDataCacheLimit | Non disponible. | Spécifie la taille maximale en mégaoctets (Mo) du cache XML pour le stockage des informations de rapport. La taille s’applique au cache en mémoire. Lorsque la limite est atteinte, le fichier journal est restauré. Définie entre 0 et 1024. | Entier [0-1024] | Reporting\DataCacheLimit | Valeur de stratégie non rédigée (comme non configuré) |
| ReportingDataBlockSize| Non disponible. | Spécifie la taille maximale en octets à transmettre au serveur pour signaler les demandes de chargement. Vous pouvez ainsi éviter les échecs de transmission permanents lorsque le journal atteint une taille significative. Définissez entre 1024 et illimité. | Entier [1024-illimité] | Reporting\DataBlockSize | Valeur de stratégie non rédigée (comme non configuré) |
| ReportingStartTime | Non disponible. | Spécifie le temps nécessaire pour lancer le client pour envoyer des données au serveur de rapports. Vous devez spécifier un entier valide entre 0-23 correspondant à l’heure du jour. Par défaut, le **ReportingStartTime** commence à la journée en cours à 10 P. M. ou 22.<br>**Remarques** Vous devez configurer ce paramètre sur une date à laquelle les ordinateurs exécutant le client App-V 5,1 sont moins susceptibles de se déconnecter. | Entier (0 à 23) | Rapport \ StartTime | Valeur de stratégie non rédigée (comme non configuré) |
| ReportingInterval | Non disponible. | Spécifie l’intervalle de réessayer que le client doit utiliser pour renvoyer les données au serveur de rapports. | Integer | Reporting\RetryInterval | Valeur de stratégie non rédigée (comme non configuré) |
| ReportingRandomDelay | Non disponible. | Spécifie le délai maximal (en minutes) pour les données à envoyer au serveur de rapports. Lorsque la tâche planifiée est lancée, le client génère un délai aléatoire compris entre 0 et **ReportingRandomDelay** et attend la durée spécifiée avant d’envoyer des données. Cela peut vous aider à éviter les collisions sur le serveur. | Entier [0-ReportingRandomDelay] | Reporting\RandomDelay | Valeur de stratégie non rédigée (comme non configuré) |
| EnableDynamicVirtualization<br>**Important** Ce paramètre est disponible uniquement avec App-V 5,0 SP2 ou une version ultérieure. | Non disponible. | Permet aux extensions d’environnement prises en charge, aux objets d’assistance du navigateur et aux contrôles Active X d’être virtualisés et exécutés avec des applications virtuelles. | 1 (activé), 0 (désactivée) | HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization | |
| EnablePublishingRefreshUI<br>**Important** Ce paramètre est disponible uniquement avec App-V 5,0 SP2. | Non disponible. | Active la barre de progression de l’actualisation de la publication pour l’ordinateur exécutant le client App-V 5,1. | 1 (activé), 0 (désactivée) | HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing | |
| HideUI<br>**Important**  Ce paramètre est disponible uniquement avec App-V 5,0 SP2.| Non disponible. | Masque la barre de progression de l’actualisation de la publication. | 1 (activé), 0 (désactivée) | | |
| ProcessesUsingVirtualComponents | Non disponible. | Spécifie une liste de chemins de processus (qui peuvent contenir des caractères génériques), qui sont candidats à l’utilisation de la virtualisation dynamique (extensions d’environnement prises en charge, objets d’assistance du navigateur et contrôles ActiveX). Seuls les processus dont le chemin complet correspond à l’un de ces éléments peuvent utiliser la virtualisation dynamique. | String | Virtualization\ProcessesUsingVirtualComponents | Chaîne vide. |






## Rubriques connexes


[Planification du déploiement d'App-V5.1 Sequencer et Client](deploying-the-app-v-51-sequencer-and-client.md)

[Modification de la configuration d'App-V5.1 Client à l'aide du modèle ADMX et d'une stratégie de groupe](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md)

[Comment déployer App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)

 

 





