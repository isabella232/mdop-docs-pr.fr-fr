---
title: À propos des paramètres de configuration du client
description: À propos des paramètres de configuration du client
author: dansimp
ms.assetid: cc7ae28c-b2ac-4f68-b992-5ccdbd5316a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 289f5b35ac223d488152ff7ee1f42b1cf50341df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806103"
---
# À propos des paramètres de configuration du client


Le client Microsoft Application Virtualization (App-V) 5,0 stocke sa configuration dans le registre. Vous pouvez recueillir des informations utiles sur le client si vous comprenez le format des données dans le registre. Vous pouvez également configurer de nombreuses actions client en modifiant des entrées de registre. Cette rubrique répertorie les paramètres de configuration du client App-V 5,0 et explique leur utilisation. Vous pouvez utiliser PowerShell pour modifier les paramètres de configuration du client. Pour plus d’informations sur l’utilisation des applications PowerShell et App-V 5,0, voir [administration de l’application-v à l’aide de PowerShell](administering-app-v-by-using-powershell.md).

## <a href="" id="---------app-v-5-0-client-configuration-settings"></a> Paramètres de configuration du client App-V 5,0


Le tableau suivant contient des informations sur les paramètres de configuration du client App-V 5,0:

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom du paramètre</th>
<th align="left">Indicateur de configuration</th>
<th align="left">Description</th>
<th align="left">Définir des options</th>
<th align="left">Valeur de clé de Registre</th>
<th align="left">Clés et valeurs de l’état de stratégie désactivé</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>PACKAGEINSTALLATIONROOT</p></td>
<td align="left"><p>Spécifie le répertoire dans lequel toutes les nouvelles applications et mises à jour sont installées.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Streaming\PackageInstallationRoot</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>PACKAGESOURCEROOT</p></td>
<td align="left"><p>Remplace l’emplacement source pour le téléchargement du contenu du package.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Streaming\PackageSourceRoot</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AllowHighCostLaunch</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Ce paramètre détermine si les applications virtualisées sont lancées sur des ordinateurs Windows 8 connectés par le biais d’une connexion réseau limitée (par exemple, 4G).</p></td>
<td align="left"><p>True (activé); Faux (état désactivé)</p></td>
<td align="left"><p>Streaming\AllowHighCostLaunch</p></td>
<td align="left"><p>0,4</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReestablishmentRetries</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Spécifie le nombre de tentatives de nouvelle session interrompue.</p></td>
<td align="left"><p>Entier (0-99)</p></td>
<td align="left"><p>Streaming\ReestablishmentRetries</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReestablishmentInterval</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Spécifie le nombre de secondes entre les tentatives de rétablissement d’une session perdue.</p></td>
<td align="left"><p>Entier (0-3600)</p></td>
<td align="left"><p>Streaming\ReestablishmentInterval</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoad</p></td>
<td align="left"><p>AUTOLOAD</p></td>
<td align="left"><p>Spécifie la façon dont les nouveaux packages doivent être chargés automatiquement par l’application-V sur un ordinateur spécifique.</p></td>
<td align="left"><p>(0x0) aucun; (0x1) précédemment utilisée; (0X2) tous</p></td>
<td align="left"><p>Streaming\AutoLoad</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocationProvider</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Spécifie le CLSID pour une implémentation compatible de l’interface IAppvPackageLocationProvider.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Streaming\LocationProvider</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="even">
<td align="left"><p>CertFilterForClientSsl</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Spécifie le chemin d’accès d’un certificat valide dans le magasin de certificats.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Streaming\CertFilterForClientSsl</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VerifyCertificateRevocationList</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Vérifie l’état de révocation des certificats de serveur avant la transmission à l’aide de HTTPs.</p></td>
<td align="left"><p>True (activé); Faux (état désactivé)</p></td>
<td align="left"><p>Streaming\VerifyCertificateRevocationList</p></td>
<td align="left"><p>0,4</p></td>
</tr>
<tr class="even">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>SHAREDCONTENTSTOREMODE</p></td>
<td align="left"><p>Spécifie que le contenu du package en flux ne sera pas enregistré sur le disque dur local.</p></td>
<td align="left"><p>True (activé); Faux (état désactivé)</p></td>
<td align="left"><p>Streaming\SharedContentStoreMode</p></td>
<td align="left"><p>0,4</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nom</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> . Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>PUBLISHINGSERVERNAME</p></td>
<td align="left"><p>Affiche le nom du serveur de publication.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ FriendlyName</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="even">
<td align="left"><p>URL</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> . Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>PUBLISHINGSERVERURL</p></td>
<td align="left"><p>Affiche l’URL du serveur de publication.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ URL</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GlobalRefreshEnabled</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> . Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHENABLED</p></td>
<td align="left"><p>Active l’actualisation globale de la publication (booléen)</p></td>
<td align="left"><p>True (activé); Faux (état désactivé)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ GlobalEnabled</p></td>
<td align="left"><p>Faux</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalRefreshOnLogon</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> . Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHONLOGON</p></td>
<td align="left"><p>Déclenche une actualisation globale de publication lors de l’ouverture de session. Expression</p></td>
<td align="left"><p>True (activé); Faux (état désactivé)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ GlobalLogonRefresh</p></td>
<td align="left"><p>Faux</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GlobalRefreshInterval</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> . Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHINTERVAL  </p></td>
<td align="left"><p>Spécifie l’intervalle d’actualisation de publication à l’aide de GlobalRefreshIntervalUnit. Pour désactiver l’actualisation du package, sélectionnez 0.</p></td>
<td align="left"><p>Entier (0-744</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ GlobalPeriodicRefreshInterval</p></td>
<td align="left"><p>0,4</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalRefreshIntervalUnit</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> . Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHINTERVALUNI</p></td>
<td align="left"><p>Spécifie l’unité de l’intervalle (heure 0-23, jour 0-31). </p></td>
<td align="left"><p>0 pour l’heure, 1 pour le jour</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ GlobalPeriodicRefreshIntervalUnit</p></td>
<td align="left"><p>1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserRefreshEnabled</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> . Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHENABLED </p></td>
<td align="left"><p>Active l’actualisation de la publication des utilisateurs (booléen)</p></td>
<td align="left"><p>True (activé); Faux (état désactivé)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ UserEnabled</p></td>
<td align="left"><p>Faux</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserRefreshOnLogon</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> . Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHONLOGON</p></td>
<td align="left"><p>Déclenche une actualisation du ONLOGON de publication par un utilisateur. Expression</p>
<p>Statistiques (avec espaces): 60</p></td>
<td align="left"><p>True (activé); Faux (état désactivé)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ UserLogonRefresh</p></td>
<td align="left"><p>Faux</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserRefreshInterval</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> . Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHINTERVAL     </p></td>
<td align="left"><p>Spécifie l’intervalle d’actualisation de publication à l’aide de UserRefreshIntervalUnit. Pour désactiver l’actualisation du package, sélectionnez 0.</p>
<p>Statistiques (avec espaces): 85</p></td>
<td align="left"><p>Entier (0-744 heures)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ UserPeriodicRefreshInterval</p></td>
<td align="left"><p>0,4</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserRefreshIntervalUnit</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> . Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHINTERVALUNIT  </p></td>
<td align="left"><p>Spécifie l’unité de l’intervalle (heure 0-23, jour 0-31). </p></td>
<td align="left"><p>0 pour l’heure, 1 pour le jour</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ UserPeriodicRefreshIntervalUnit</p></td>
<td align="left"><p>1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MigrationMode</p></td>
<td align="left"><p>MIGRATIONMODE</p></td>
<td align="left"><p>Le mode migration permet au client App-V de modifier des raccourcis et FTA pour les packages créés à l’aide d’une version antérieure d’App-V.</p></td>
<td align="left"><p>True (état activé); Faux (état désactivé)</p></td>
<td align="left"><p>Coexistence\MigrationMode</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>CEIPOPTIN</p></td>
<td align="left"><p>CEIPOPTIN</p></td>
<td align="left"><p>Permet à l’ordinateur exécutant le client App-V 5,0 de collecter et de renvoyer des informations d’utilisation pour nous aider à améliorer l’application.</p></td>
<td align="left"><p>0 pour désactivé; 1 pour activé</p></td>
<td align="left"><p>LOGICIEL/Microsoft/AppV/CEIP/CEIPEnable</p></td>
<td align="left"><p>0,4</p></td>
</tr>
<tr class="odd">
<td align="left"><p>EnablePackageScripts</p></td>
<td align="left"><p>ENABLEPACKAGESCRIPTS</p></td>
<td align="left"><p>Active les scripts définis dans le manifeste du package de fichiers de configuration qui doivent s’exécuter.</p></td>
<td align="left"><p>True (activé); Faux (état désactivé)</p></td>
<td align="left"><p>\Scripting\EnablePackageScripts</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>RoamingFileExclusions</p></td>
<td align="left"><p>ROAMINGFILEEXCLUSIONS</p></td>
<td align="left"><p>Spécifie les chemins d’accès relatifs au fichier% UserProfile% qui ne sont pas itinérants avec un profil utilisateur&#39;s. Exemple d’utilisation:/ROAMINGFILEEXCLUSIONS =&#39;Bureau; mes images&#39;</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>RoamingRegistryExclusions</p></td>
<td align="left"><p>ROAMINGREGISTRYEXCLUSIONS</p></td>
<td align="left"><p>Spécifie les chemins de Registre qui ne sont pas itinérants avec un profil utilisateur. Exemple d’utilisation:/ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Integration\RoamingRegistryExclusions</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="even">
<td align="left"><p>IntegrationRootUser</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Spécifie l’emplacement permettant de créer des liens symboliques associés à la version actuelle d’un package publié par utilisateur. toutes les extensions d’application virtuelles, par exemple les raccourcis clavier et les associations de types de fichiers, pointent vers ce chemin. Si vous ne spécifiez pas de chemin d’accès, les liens symboliques ne seront pas utilisés lors de la publication du package. Par exemple:%localappdata%\Microsoft\AppV\Client\Integration.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Integration\IntegrationRootUser</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IntegrationRootGlobal</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Spécifie l’emplacement permettant de créer des liens symboliques associés à la version actuelle d’un package publié globalement. toutes les extensions d’application virtuelles, par exemple les raccourcis clavier et les associations de types de fichiers, pointent vers ce chemin. Si vous ne spécifiez pas de chemin d’accès, les liens symboliques ne seront pas utilisés lors de la publication du package. Par exemple:%allusersprofile%\Microsoft\AppV\Client\Integration</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Integration\IntegrationRootGlobal</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="even">
<td align="left"><p>VirtualizableExtensions</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Liste délimitée par des virgules des extensions de nom de fichier qui peut être utilisée pour déterminer si une application installée localement peut être exécutée dans l’environnement virtuel.</p>
<p>Lors de la création de raccourcis, de FTAs et d’autres points d’extension lors de la publication, App-V compare l’extension de nom de fichier à la liste si l’application associée au point d’extension est installée localement. Si l’extension se trouve, le <strong> paramètre de ligne de commande RunVirtual est </strong> ajouté et l’application s’exécute quasiment.</p>
<p>Pour plus d’informations sur <strong> le </strong> paramètre RunVirtual, voir <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)"> exécution d’une application installée localement dans un environnement virtuel avec des applications virtualisées </a> .</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Integration\VirtualizableExtensions</p></td>
<td align="left"><p>Valeur de stratégie non écrite</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingEnabled</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Permet au client de renvoyer des informations vers un serveur de rapports.</p></td>
<td align="left"><p>True (activé); Faux (état désactivé)</p></td>
<td align="left"><p>Reporting\EnableReporting</p></td>
<td align="left"><p>Faux</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingServerURL</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Spécifie l’emplacement sur le serveur de création de rapports où les informations client sont enregistrées.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Reporting\ReportingServer</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingDataCacheLimit</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Spécifie la taille maximale en mégaoctets (Mo) du cache XML pour le stockage des informations de rapport. La taille s’applique au cache en mémoire. Lorsque la limite est atteinte, le fichier journal est restauré. Définie entre 0 et 1024.</p></td>
<td align="left"><p>Entier [0-1024]</p></td>
<td align="left"><p>Reporting\DataCacheLimit</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingDataBlockSize</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Spécifie la taille maximale en octets à transmettre au serveur pour signaler les demandes de chargement. Vous pouvez ainsi éviter les échecs de transmission permanents lorsque le journal atteint une taille significative. Définissez entre 1024 et illimité.</p></td>
<td align="left"><p>Entier [1024-illimité]</p></td>
<td align="left"><p>Reporting\DataBlockSize</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingStartTime</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Spécifie le temps nécessaire pour lancer le client pour envoyer des données au serveur de rapports. Vous devez spécifier un entier valide entre 0-23 correspondant à l’heure du jour. Par défaut, le <strong> ReportingStartTime </strong> commence à la journée en cours à 10 P. M. ou 22.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Vous devez configurer ce paramètre sur une date à laquelle les ordinateurs exécutant le client App-V 5,0 sont moins susceptibles de se déconnecter.</p>
</div>
<div>

</div></td>
<td align="left"><p>Entier (0 à 23)</p></td>
<td align="left"><p>Rapport \ StartTime</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingInterval</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Spécifie l’intervalle de réessayer que le client doit utiliser pour renvoyer les données au serveur de rapports.</p></td>
<td align="left"><p>Integer</p></td>
<td align="left"><p>Reporting\RetryInterval</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingRandomDelay</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Spécifie le délai maximal (en minutes) pour les données à envoyer au serveur de rapports. Lorsque la tâche planifiée est lancée, le client génère un délai aléatoire compris entre 0 et <strong> ReportingRandomDelay </strong> et attend la durée spécifiée avant d’envoyer des données. Cela peut vous aider à éviter les collisions sur le serveur.</p></td>
<td align="left"><p>Entier [0-ReportingRandomDelay]</p></td>
<td align="left"><p>Reporting\RandomDelay</p></td>
<td align="left"><p>Valeur de stratégie non rédigée (comme non configuré)</p></td>
</tr>
<tr class="even">
<td align="left"><p>EnableDynamicVirtualization</p>
<div class="alert">
<strong>Important</strong><br/><p>Ce paramètre est disponible uniquement avec App-V 5,0 SP2 ou une version ultérieure.</p>
</div>
<div>

</div></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Permet aux extensions d’environnement prises en charge, aux objets d’assistance du navigateur et aux contrôles Active X d’être virtualisés et exécutés avec des applications virtuelles.</p></td>
<td align="left"><p>1 (activé), 0 (désactivée)</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>EnablePublishingRefreshUI</p>
<div class="alert">
<strong>Important</strong><br/><p>Ce paramètre est disponible uniquement avec App-V 5,0 SP2.</p>
</div>
<div>

</div></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Active la barre de progression de l’actualisation de la publication pour l’ordinateur exécutant le client App-V 5,0.</p></td>
<td align="left"><p>1 (activé), 0 (désactivée)</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>HideUI</p>
<div class="alert">
<strong>Important</strong><br/><p>Ce paramètre est disponible uniquement avec App-V 5,0 SP2.</p>
</div>
<div>

</div></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Masque la barre de progression de l’actualisation de la publication.</p></td>
<td align="left"><p>1 (activé), 0 (désactivée)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProcessesUsingVirtualComponents</p></td>
<td align="left"><p>Non disponible.</p></td>
<td align="left"><p>Spécifie une liste de chemins de processus (qui peuvent contenir des caractères génériques), qui sont candidats à l’utilisation de la virtualisation dynamique (extensions d’environnement prises en charge, objets d’assistance du navigateur et contrôles ActiveX). Seuls les processus dont le chemin complet correspond à l’un de ces éléments peuvent utiliser la virtualisation dynamique.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Virtualization\ProcessesUsingVirtualComponents</p></td>
<td align="left"><p>Chaîne vide.</p></td>
</tr>
</tbody>
</table>








## Rubriques connexes


[Déploiement d'App-V5.0 Sequencer et Client](deploying-the-app-v-50-sequencer-and-client.md)

[Modification de la configuration d'App-V5.0 Client à l'aide du modèle ADMX et d'une stratégie de groupe](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

[Comment déployer App-V Client](how-to-deploy-the-app-v-client-gb18030.md)









