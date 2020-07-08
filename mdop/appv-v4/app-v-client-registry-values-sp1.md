---
title: Valeurs de Registre d'App-V Client
description: Valeurs de Registre d'App-V Client
author: dansimp
ms.assetid: 46af5209-9762-47b9-afdb-9a2947e013f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 05cd807ff9882bc478aca07abc4a28cdea83086a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808054"
---
# Valeurs de Registre d'App-V Client


Le client Microsoft Application Virtualization (App-V) enregistre sa configuration dans le registre. Vous pouvez recueillir des informations utiles sur le client si vous comprenez le format des données dans le registre. Vous pouvez également configurer de nombreuses actions client en modifiant des entrées de registre. Cette rubrique répertorie toutes les clés de Registre clientes Application Virtualization (App-V) et explique leur utilisation.

**Important**  
Sur un ordinateur exécutant un système d’exploitation 64 bits, les clés et les valeurs décrites dans les sections suivantes se trouvent sous HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.



## Clé de configuration


Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom</th>
<th align="left">Type</th>
<th align="left">Données (exemples)</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Client de bureau Microsoft Application Virtualization</p></td>
<td align="left"><p>Ne modifiez pas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Version </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>4.5.0.xxx </p></td>
<td align="left"><p>Ne modifiez pas. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>Pilotes </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>Sftfs.sys </p></td>
<td align="left"><p>Si cette valeur de clé est présente, elle contient le nom du pilote à l’origine d’une erreur d’arrêt lors du dernier démarrage de la base. Après avoir résolu l’erreur d’arrêt, vous devez supprimer cette valeur de clé pour permettre à sftlist de démarrer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>InstallPath </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>Par défaut = C:\Program Files\Microsoft Application Virtualization Client</p></td>
<td align="left"><p>L’emplacement de l’installation du client. Ne modifiez pas. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogFileName </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>Par défaut = CSIDL_COMMON_APPDATA virtualisation \Microsoft\Application Client\sftlog.txt</p></td>
<td align="left"><p>Le chemin d’accès et le nom du fichier journal du client.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si vous exécutez une version antérieure à App-V 4,6, SP1 et que vous modifiez le nom ou l’emplacement du fichier journal, vous devez redémarrer le service sftlist pour que la modification soit prise en compte.</p>
</div>
<div>

</div>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>LogMinSeverity </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Par défaut = 4, information</p></td>
<td align="left"><p>Détermine quels messages sont écrits dans le journal. La valeur indique un seuil de ce qui est enregistré, c’est-à-dire que tout est inférieur ou égal à cette valeur est consigné. Par exemple, une valeur de 0x3 (avertissement) indique que les avertissements (0x3), les erreurs (0X2) et les erreurs critiques (0x1) sont enregistrées.</p>
<p>Plage de valeurs: 0x0 = aucune, 0x1 = Critical, 0X2 = erreur, 0x3 = Warning, 0x4 = informations (par défaut), 0x5 = Verbose.</p>
<p>Le niveau du journal peut être configuré à partir de la console client Application Virtualization (App-V) et de l’invite de commandes. À l’invite de commandes, la commande sftlist.exe/Verboselog augmentera le niveau du journal sur Verbose. Pour plus d’informations sur les détails de la ligne de commande, voir</p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467">https://go.microsoft.com/fwlink/?LinkId=141467https://go.microsoft.com/fwlink/?LinkId=141467</a></p>
<p>.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogRolloverCount</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 4</p></td>
<td align="left"><p>Définit le nombre de copies de sauvegarde du fichier journal qui sont conservées lors de la réinitialisation. La plage valide est égale à 0 – 9999. La valeur par défaut est 4. La valeur 0 indique qu’il n’y a pas de copie.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LogMaxSize</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 256</p></td>
<td align="left"><p>Définit la taille maximale en mégaoctets (Mo) que le fichier journal peut augmenter avant de procéder à la réinitialisation. La taille par défaut est 256 Mo. Lorsque cette taille est atteinte, une réinitialisation du journal sera forcée lors de la tentative d’écriture suivante.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SystemEventLogLevel</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 0x4 (App-V 4,5)</p>
<p>Par défaut = 0x3 (App-V 4,6)</p></td>
<td align="left"><p>Indique le niveau de journalisation dans lequel les messages du journal sont écrits dans le journal des événements Windows. La valeur indique un seuil de ce qui est enregistré, c’est-à-dire que tout est égal ou inférieur à cette valeur est consigné. Par exemple, une valeur de 0x3 (avertissement) indique que les avertissements (0x3), les erreurs (0X2) et les erreurs critiques (0x1) sont enregistrées.</p>
<p>Plage de valeurs</p>
<p>0x0 = aucun</p>
<p>0x1 = critique</p>
<p>0X2 = erreur</p>
<p>0x3 = AVERTISSEMENT</p>
<p>0x4 = informations (par défaut)</p>
<p>0x5 = commentaires</p></td>
</tr>
<tr class="even">
<td align="left"><p>AllowIndependentFileStreaming</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 0</p></td>
<td align="left"><p>Indique si la diffusion en continu à partir du fichier sera activée quelle que soit la façon dont le client a été configuré avec le paramètre APPLICATIONSOURCEROOT. Si elle est définie sur FALSe, le transport n’active pas la diffusion en continu à partir de fichiers, même si le paramètre OSD HREF ou APPLICATIONSOURCEROOT contient un chemin d’accès au fichier.</p>
<p>0x0 = false (par défaut)</p>
<p>0x1 = vrai</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ApplicationSourceRoot</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps</p>
<p><a href="https://mainserver:443/prodapps" data-raw-source="https://mainserver:443/prodapps">https://mainserver:443/prodapps</a></p>
<p>fichier://\uncserver\share\prodapps</p>
<p>fichier://\uncserver\share</p></td>
<td align="left"><p>Permet à un administrateur ou à un système de distribution de logiciels électronique (ESD) de garantir le chargement des applications conformément au schéma de gestion de la topologie. Utilisez cette valeur de clé pour remplacer le code base OSD pour l’élément HREF (par exemple, l’emplacement source) pour une application. La racine source de l’application prend en charge les URL et les formats de chemin UNC (Universal Naming Convention).</p>
<p>Le format correct pour le chemin d’accès URL est Protocol://servername: [port] [/path] [/], où le port et le chemin d’accès sont facultatifs. Si un port n’est pas spécifié, le port par défaut du protocole est utilisé. Seule la partie protocole://Server: port de l’URL d’OSD est remplacée. </p>
<p>Le format correct pour le chemin d’accès UNC est \computername\sharefolder [dossier] [], où le dossier est facultatif. Le nom de l’ordinateur peut être un nom de domaine complet (FQDN, Fully Qualified Domain Name) ou une adresse IP, et ShareFolder peut être une lettre d’unité. Seule la partie \computername\sharefolder ou lettre de lecteur du chemin OSD est remplacée. </p></td>
</tr>
<tr class="even">
<td align="left"><p>OSDSourceRoot</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>\computername\sharefolder\resource</p>
<p>\computername\content</p>
<p>C:\foldername</p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p>Permet à un administrateur de spécifier un emplacement source pour la récupération de fichier OSD pour un package d’application séquencé lors de la publication. Les formats acceptables pour le OSDSourceRoot incluent les chemins d’accès UNC et les URL (http ou https).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IconSourceRoot</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>\computername\sharefolder\resource</p>
<p>\computername\content</p>
<p>C:\foldername</p>
<p><a href="http://computername/productivity/" data-raw-source="http://computername/productivity/">http://computername/productivity/</a></p>
<p><a href="https://computername/productivity/" data-raw-source="https://computername/productivity/">https://computername/productivity/</a></p></td>
<td align="left"><p>Permet à un administrateur de spécifier un emplacement source pour la récupération du fichier d’icône pour un package d’application séquencé lors de la publication. Les formats acceptables pour le IconSourceRoot incluent les chemins d’accès UNC et les URL (http ou https).</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoadTriggers</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 5</p></td>
<td align="left"><p>Autoload est un paramètre de configuration de la stratégie d’exécution du client qui permet d’afficher automatiquement le bloc de fonctionnalité secondaire d’une application virtualisée au client en arrière-plan. Les déclencheurs de chargement sont des indicateurs permettant d’indiquer des événements qui déclenchent le chargement automatique des applications. Autoload utilise implicitement le streaming en arrière-plan pour permettre au chargement de l’application dans le cache. Le bloc de fonctionnalité principal est chargé en premier, et les blocs de fonctionnalités restants sont chargés en arrière-plan pour permettre aux opérations au premier plan, telles que l’interaction utilisateur avec les applications, d’avoir lieu et d’offrir des performances optimales.</p>
<p>Valeurs de masque de bits:</p>
<p>(0) jamais: aucun bit n’est défini (valeur égale à 0), aucun chargement automatique ne sera effectué, car aucun déclencheur n’est défini.</p>
<p>(1) OnLaunch: le chargement s’exécute dès qu’un utilisateur démarre une application.</p>
<p>(2) OnRefresh: le chargement démarre lors de la publication de l’application. Ce problème survient chaque fois que l’enregistrement du package est ajouté ou mis à jour, par exemple, lors de l’actualisation de la publication.</p>
<p>(4) OnLogin: le chargement s’exécute dès qu’un utilisateur se connecte.</p>
<p>(5) OnLaunch et OnLogin: par défaut.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AutoLoadTarget</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 1</p></td>
<td align="left"><p>Indique ce qui sera chargé automatiquement lorsque des déclencheurs de chargement sont présents. Valeurs de masque de bits:</p>
<p>(0) aucun: pas de chargement automatique, quels que soient les déclencheurs définis.</p>
<p>(1) PreviouslyUsed (par défaut): si aucun déclencheur de chargement automatique n’est activé, chargez uniquement les packages dans lesquels au moins une application dans le package a été précédemment utilisée (c’est-à-dire démarrée ou mise en cache).</p>
<p>(2) All: si un déclencheur de chargement automatique est activé, toutes les applications du package (par package) ou tous les packages (définies pour le client) seront automatiquement chargées, qu’elles soient ou non démarrées.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RequireAuthorizationIfCached</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 1</p></td>
<td align="left"><p>Indique qu’une autorisation est toujours requise, qu’une application soit déjà en cache ou non. Valeurs possibles:</p>
<p>0 = faux: Essayez toujours de vous connecter au serveur. Si une connexion au serveur ne peut pas être établie, le client permet toujours à l’utilisateur de lancer une application qui a déjà été chargée dans le cache.</p>
<p>1 = vrai (par défaut): l’application doit toujours être autorisée au démarrage. Pour les applications RTSP transmis, le jeton d’autorisation de l’utilisateur est envoyé au serveur pour autorisation. Dans le cas des applications basées sur le fichier, les listes de contrôle d’accès de fichier déterminent si un utilisateur est susceptible d’y accéder.</p>
<p>Redémarrez le service sftlist pour que la modification soit prise en compte.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserDataDirectory </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>AppData</p></td>
<td align="left"><p>Emplacement de stockage des paramètres du cache d’icônes et de l’utilisateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalDataDirectory </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>C:\Users\Public\Documents </p></td>
<td align="left"><p>Directory à utiliser pour les données globales App-V, y compris les caches pour les fichiers OSD, les fichiers d’icônes, les informations de raccourci et les ressources SystemGuard telles que les fichiers. ini.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AllowCrashes </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0 ou 1 </p></td>
<td align="left"><p>Par défaut = 0: une valeur de 0 indique que le client tente d’intercepter les exceptions de programme interne pour permettre à d’autres applications utilisateur de se retrouver et de continuer en cas de blocage. La valeur 1 indique que le client autorise l’apparition des exceptions du programme interne afin qu’elles puissent être capturées dans un débogueur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>CoreInternalTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>60</p></td>
<td align="left"><p>Délai d’expiration en secondes pour les demandes de CPI internes entre le cœur et le front-end. Ne modifiez pas. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>DefaultSuiteCombineTime </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0,10</p></td>
<td align="left"><p>Cette valeur est utilisée pour indiquer le nombre de fois qu’un programme peut s’arrêter et ne générer aucun message d’erreur lorsqu’une autre application de la même suite est en cours d’exécution. </p></td>
</tr>
<tr class="even">
<td align="left"><p>SerializedSuiteLaunchTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Par défaut = 60000</p></td>
<td align="left"><p>Définit la durée en millisecondes au sein de laquelle le client doit patienter pendant qu’il tente de sérialiser les programmes dans la même suite. Si le client arrive à expiration, le démarrage du programme se poursuit mais il n’est pas sérialisé. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>ScriptTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>300</p></td>
<td align="left"><p>Délai d’expiration par défaut (en secondes) pour les scripts du fichier OSD si attendez = TRUE. Vous pouvez spécifier des délais d’expiration par script avec une temporisation au lieu d’attendre. Une valeur de 0 signifie qu’il n’y A pas d’attente et 0xFFFFFFFF un délai d’exécution permanent. </p></td>
</tr>
<tr class="even">
<td align="left"><p>LaunchRecordLogPath </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p></p></td>
<td align="left"><p>Si, dans le cadre de l’argument HKLM ou HKCU, cette valeur contient un chemin valide vers un fichier journal, SFTTray écrit dans ce journal lorsque les programmes démarrent, s’arrête, ne démarre pas, puis passe ou quittez le mode déconnecté.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LaunchRecordMask </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0x1A (26) consigner les erreurs de démarrage et les activités d’entrée et de sortie du mode déconnecté.</p>
<p>0x1F (31) enregistre tout le contenu.</p>
<p>0x0 (0) n’enregistre aucune information. </p></td>
<td align="left"><p>Spécifie lequel des cinq événements sont enregistrés (valeurs de masque de réaffichages):</p>
<p>1 pour le démarrage du programme</p>
<p>2 pour les erreurs d’échec de lancement</p>
<p>4 pour les arrêts</p>
<p>8 pour entrer en mode déconnecté</p>
<p>16 pour quitter le mode déconnecté afin de vous reconnecter à un serveur</p>
<p>Ajoutez n’importe quelle combinaison de ces numéros pour activer les messages correspondants. Utilise par défaut la valeur 0x1F s’il ne se trouve pas dans le registre. </p></td>
</tr>
<tr class="even">
<td align="left"><p>LaunchRecordWriteTimeout </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Par défaut = 3000</p></td>
<td align="left"><p>Spécifie en millisecondes le temps que la barre d’attente attend lors de la tentative d’écriture dans le journal d’enregistrement de lancement si un autre processus l’utilise.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ImportSearchPath </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>d:\files; C:\Documents and settings\user1\SFTs </p></td>
<td align="left"><p>Liste délimitée par des points-virgules de cinq annuaires pour lesquels rechercher des fichiers de la liste de choix mobiles avant d’inviter l’utilisateur à sélectionner un annuaire. Le caractère barre oblique inverse dans les chemins est facultatif. Cette valeur n’est pas présente par défaut et doit être définie manuellement.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserImportPath</p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>D:\SFTs\ </p></td>
<td align="left"><p>Valide uniquement sous HKCU. Dernier emplacement sur lequel l’utilisateur a été consulté lors de la recherche d’un fichier SFT pour l’importation du package. Configuré automatiquement si la valeur SFT est correctement trouvée. Il s’utilise sur les importations successives lorsque vous tentez de rechercher automatiquement des fichiers SFT.</p></td>
</tr>
</tbody>
</table>



## Clé partagée


La clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Shared contrôle les valeurs qui sont partagées entre les composants App-V. Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé partagée.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom </th>
<th align="left">Type </th>
<th align="left">Données (exemples) </th>
<th align="left">Description </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DumpPath </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>Par défaut = C:\ </p></td>
<td align="left"><p>Chemin par défaut pour créer des fichiers de vidage lors de la génération d’un minidump sur une exception. Par défaut, la valeur est C:\ en l’absence de spécification. Le programme d’installation du client définit cette clé sur le &lt; répertoire global Data \Dumps. Directory Data Virtualization. &gt; Le programme d’installation de Sequencer définit cette clé sur le répertoire d’installation. </p></td>
</tr>
<tr class="even">
<td align="left"><p>DumpPathSizeLimit </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>1000</p></td>
<td align="left"><p>Spécifie la quantité totale d’espace disque en mégaoctets qui peut être utilisée pour stocker les minidumps. Par défaut = 1000 Mo.</p></td>
</tr>
</tbody>
</table>



## Clé réseau


La clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network contrôle divers paramètres liés au réseau. Cette clé est essentiellement utilisée par l’agent de transport réseau. Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé réseau.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom </th>
<th align="left">Type </th>
<th align="left">Données (exemples) </th>
<th align="left">Description </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Online</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 1</p></td>
<td align="left"><p>Active ou désactive le mode hors connexion. Si la valeur est définie sur 0, le client ne va pas communiquer avec des serveurs de gestion ou des serveurs de publication App-V. Dans les opérations déconnectées, le client peut démarrer une application chargée même lorsqu’elle n’est pas connectée à un serveur de gestion d’applications-V. En mode hors connexion, le client ne tente pas de se connecter à un serveur de gestion ou un serveur de publication App-V. Vous devez autoriser les opérations déconnectées à travailler en mode hors connexion. La valeur par défaut est activée (en ligne) et 0 est désactivée (hors connexion).</p></td>
</tr>
<tr class="even">
<td align="left"><p>AllowDisconnectedOperation </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Par défaut = 1</p></td>
<td align="left"><p>Active ou désactive l’opération hors connexion. La valeur par défaut est activée et 0 est désactivé. Lorsque les opérations déconnectées sont activées, le client App-V peut démarrer une application chargée, même si elle n’est pas connectée à un serveur d’administration d’applications-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FastConnectTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 1 000</p></td>
<td align="left"><p>Cette valeur spécifie le délai de connexion TCP en millisecondes pour déterminer quand passer en mode opérations déconnectées. Cette valeur peut être utilisée pour remplacer la valeur par défaut ConnectTimeout de 20 secondes (délai d’expiration de la connexion App-V pour les transactions réseau) ou le délai d’expiration TCP du système d’environ 25 secondes. Cela amène le client en mode d’opérations déconnectées rapidement. Appliqué lors de la prochaine connexion.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LimitDisconnectedOperation</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 1 </p></td>
<td align="left"><p>Applicable uniquement si AllowDisconnectedOperation est activé. Cette valeur détermine s’il y a une limite de temps pour la durée pendant laquelle le client est autorisé à fonctionner dans les opérations déconnectées. 1 = Limited. 0 = illimité.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DOTimeoutMinutes</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 129600</p></td>
<td align="left"><p>Indique le nombre de minutes d’utilisation d’une application en mode de fonctionnement déconnecté.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Les valeurs valides sont comprises entre 1 et 999999 en jours exprimées en minutes (1 – 1439998560 minutes). La valeur par défaut est 90 jours ou 129 600 minutes.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Protocole</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 8</p></td>
<td align="left"><p>Protocole par défaut à utiliser (TCP ou SSL). Configurer dans la boîte de dialogue Options.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReadTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>CX3-20</p></td>
<td align="left"><p>Délai de lecture des transactions réseau, en secondes. Ne modifiez pas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>WriteTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>CX3-20</p></td>
<td align="left"><p>Notez le délai d’expiration des transactions réseau, en quelques secondes. Ne modifiez pas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ConnectTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>CX3-20</p></td>
<td align="left"><p>Délai de connexion des transactions réseau, en secondes. Ne modifiez pas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReestablishmentRetries</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>3D</p></td>
<td align="left"><p>Nombre d’occurrences d’une tentative de rétablissement d’une session interrompue.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReestablishmentInterval</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>0,15</p></td>
<td align="left"><p>Nombre de secondes d’attente entre les tentatives de rétablissement d’une session perdue.</p></td>
</tr>
</tbody>
</table>



## Clé http


La clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\Http contrôle les paramètres liés au streaming http. Cette clé est essentiellement utilisée par l’agent de transport réseau. Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé http.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom </th>
<th align="left">Type </th>
<th align="left">Données (exemples) </th>
<th align="left">Description </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>LaunchIfNotFound</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 0</p></td>
<td align="left"><p>Contrôle le comportement de la diffusion HTTP en continu lorsqu’une connexion au serveur HTTP peut être établie et que le fichier de package n’existe plus sur le serveur HTTP. Si la valeur n’existe pas ou si elle n’est pas définie sur 1, le client App-V ne vous permet pas de lancer une application qui a déjà été chargée dans le cache.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1</p></td>
<td align="left"><p>Si cette valeur est définie sur 1, le client App-V vous permet de lancer une application qui a déjà été chargée dans le cache.</p></td>
</tr>
</tbody>
</table>



## Clé de système de fichiers


Les valeurs contenues sous la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS contrôlent les paramètres du système de fichiers pour App-V. Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé AppFS.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom </th>
<th align="left">Type </th>
<th align="left">Données (exemples) </th>
<th align="left">Description </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>FileSize </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>4096</p></td>
<td align="left"><p>Taille maximale en mégaoctets du fichier cache du système de fichiers. Si vous modifiez cette valeur dans le registre, vous devez définir l’État sur 0 et redémarrer. </p></td>
</tr>
<tr class="even">
<td align="left"><p>FileName </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>C:\Users\Public\Documents\SoftGrid Client\sftfs.fsd </p></td>
<td align="left"><p>Emplacement du fichier cache du système de fichiers. Si vous modifiez cette valeur dans le registre, vous devez laisser FileSize le même et redémarrer ou définir l’État sur 0 et redémarrer. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>LettreLecteur </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>Q: </p></td>
<td align="left"><p>Lecteur sur lequel le système de fichiers App-V sera monté, s’il est disponible. Cette valeur est définie par l’écouteur ou le programme d’installation, et est lue par le système de fichiers. </p></td>
</tr>
<tr class="even">
<td align="left"><p>État </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>0x100 </p></td>
<td align="left"><p>État du système de fichiers. Définissez la valeur sur 0 et redémarrez pour effacer entièrement le cache du système de fichiers. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileSystemStorage </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>C:\Profiles\Joe\SG </p></td>
<td align="left"><p>Path pour symlinks, définie sous HKCU. Ne pas modifier (utilisez le répertoire des données sous Configuration pour le modifier). </p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalFileSystemStorage </p></td>
<td align="left"><p>String </p></td>
<td align="left"><p>C:\Users\Public\Documents\SoftGrid Client\AppFS Storage </p></td>
<td align="left"><p>Chemin pour les données du système de fichiers global. Ne modifiez pas. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxPercentToLockInCache </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Valeur par défaut = 90 </p></td>
<td align="left"><p>Spécifie le pourcentage maximal du fichier cache du système de fichiers qui peut être verrouillé. Ne modifiez pas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UnloadLeastRecentlyUsed</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 1</p></td>
<td align="left"><p>La fonctionnalité de gestion de l’espace dans le système de fichiers utilise un algorithme de dernier recours (LRU) et est activée par défaut. Si l’espace requis pour un nouveau package dépasse l’espace libre disponible dans le cache, le client App-V utilise cette fonctionnalité pour déterminer, le cas échéant, les packages existants qu’il peut supprimer du cache pour libérer de l’espace pour le nouveau package. Le client supprime le package avec la dernière date à laquelle il est consulté le plus ancien s’il est antérieur à la valeur spécifiée dans la valeur de Registre MinPkgAge. Les valeurs sont 0 (désactivées) et 1 (valeur par défaut activée).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MinPackageAge</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>1</p></td>
<td align="left"><p>Pour déterminer à quel moment le package peut être sélectionné pour ignorer, définissez cette valeur de Registre sur égal au nombre minimal de jours que vous souhaitez voir s’écouler après le dernier accès au package. Les packages utilisés plus récemment ne sont pas supprimés.</p></td>
</tr>
</tbody>
</table>



## Touche autorisations


Pour empêcher les utilisateurs d’effectuer des erreurs, les administrateurs peuvent utiliser la clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions pour contrôler l’accès à certaines actions pour les utilisateurs non administrateurs, par exemple pour empêcher les utilisateurs de décharger accidentellement des programmes. Les utilisateurs disposant de droits d’administration peuvent lui accorder une de ces autorisations. Sur les systèmes partagés, tels qu’un serveur hôte de session Bureau à distance (hôte de session Bureau à distance) (anciennement Terminal Server), veillez à accorder des autorisations supplémentaires aux utilisateurs, car certaines de ces autorisations permettent aux utilisateurs de contrôler les applications utilisées par tous les utilisateurs sur le système. Les valeurs possibles de ces paramètres sont 1 (Allow) et 0 (Disallow).

Les paramètres de touches autorisations contrôlent toutes les interfaces qui activent les actions nommées. Cela inclut la boîte de dialogue Options, SFTTray et SFTMime. Ces paramètres n’ont aucun impact sur les administrateurs. Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé autorisations.

Données de type de nom (exemples) Description ChangeFSDrive

DWORD

Par défaut = 0

La valeur 1 permet aux utilisateurs de sélectionner une autre lettre de lecteur à utiliser comme lecteur du système de fichiers.

ChangeCacheSize

DWORD

Par défaut = 0

La valeur 1 permet aux utilisateurs de modifier la taille du cache.

ChangeLogSettings

DWORD

Par défaut = 0

La valeur 1 permet aux utilisateurs de modifier le niveau du journal, de modifier son emplacement et de le réinitialiser par le biais de l’interface utilisateur.

AddApp

DWORD

Par défaut = 0

La valeur 1 permet aux utilisateurs d’ajouter explicitement des applications. Cela n’affecte pas les applications ajoutées par le biais de la mise à jour de la publication, ou empêche les utilisateurs de démarrer (et donc d’ajouter implicitement) des applications qui n’ont pas encore été ajoutées. Les valeurs sont 0 ou 1.

LoadApp 

DWORD 

0,4

Ne permet pas à un utilisateur de charger une application. Il s’agit de la valeur par défaut pour les hôtes de session Bureau à distance. Si vous êtes un utilisateur mobile, vous souhaiterez peut-être charger entièrement vos applications dans le cache pour les utiliser en mode hors connexion ou en mode hors connexion. Pour diffuser des applications à partir du serveur de gestion App-V ou du serveur de streaming App-V, vous devez être connecté à un serveur pour charger des applications.

1

Permet à un utilisateur de charger une application. Il s’agit de la valeur par défaut pour les ordinateurs de bureau Windows. 

UnloadApp 

DWORD 

0,4

Ne permet pas à un utilisateur de décharger une application. Lorsque vous chargez ou déchargez un package, toutes les applications du package sont chargées ou supprimées du cache.

1

Permet à un utilisateur de décharger une application. 

LockApp 

DWORD 

0,4

Ne permet pas à un utilisateur de verrouiller et de déverrouiller une application. Il s’agit de la valeur par défaut pour les hôtes de session Bureau à distance. Une application verrouillée ne peut pas être supprimée du cache pour libérer de l’espace pour les nouvelles applications. Pour supprimer une application verrouillée du Bureau App-V ou du client pour les services Bureau à distance (anciennement services Terminal Server), vous devez déverrouiller celle-ci.

1

Permet à un utilisateur de verrouiller et de déverrouiller une application. Il s’agit de la valeur par défaut pour les ordinateurs de bureau Windows. 

ManageTypes 

DWORD 

0,4

Ne permet pas à un utilisateur d’ajouter, de modifier ou de supprimer des associations de types de fichiers uniquement pour cet utilisateur. Il s’agit de la valeur par défaut pour les hôtes de session Bureau à distance. 

1

Permet à un utilisateur d’ajouter, de modifier et de supprimer des associations de type de fichier uniquement pour cet utilisateur et pas globalement. Il s’agit de la valeur par défaut pour les ordinateurs de bureau Windows. 

RefreshServer 

DWORD 

0,4

Ne permet pas à un utilisateur de déclencher une actualisation des paramètres MIME. Il s’agit de la valeur par défaut pour les hôtes de session Bureau à distance. 

1

Permet à un utilisateur de déclencher une actualisation des paramètres MIME. Il s’agit de la valeur par défaut pour les ordinateurs de bureau Windows. 

UpdateOSDFile

DWORD

Par défaut = 0

La valeur 1 permet à un utilisateur d’utiliser un fichier OSD modifié.

ImportApp 

DWORD 

0,4

Ne permet pas à un utilisateur d’importer des applications dans le cache. La différence entre Load et Import réside dans le fait que le client obtient le package à partir de l’emplacement actuellement configuré contenu dans l’URL d’OSD, ASR ou override. Lors de l’utilisation de l’importation, un emplacement à partir duquel obtenir le package doit être spécifié. 

1

Permet à un utilisateur d’importer des applications dans le cache. 

ChangeRefreshSettings

DWORD

Par défaut = 0

La valeur 1 permet aux utilisateurs de modifier les paramètres d’actualisation des serveurs (actualisation à la connexion et actualisation périodique). Cela ne signifie pas que l’utilisateur peut modifier les autres paramètres du serveur (chemin d’accès, hôte, etc.).

ManageServers

DWORD

Par défaut = 0

La valeur 1 permet à l’utilisateur d’ajouter, de modifier et de supprimer des serveurs, à l’exception de la modification des paramètres d’actualisation, qui est contrôlée par l’autorisation ChangeRefreshSettings.

PublishShortcut

DWORD

Par défaut = 0

La valeur 1 permet aux utilisateurs de publier des raccourcis par le biais de l’interface utilisateur. Cela n’affecte pas les raccourcis publiés lors de l’actualisation de la publication.

ViewAllApplications

DWORD

Par défaut = 0

La valeur 1 affiche toutes les applications par le biais de l’interface utilisateur; dans le cas contraire, seules les applications de l’utilisateur sont affichées.

RepairApp

DWORD

Par défaut = 1

La valeur 1 permet à l’utilisateur d’utiliser l’action de réparation sur les applications dans SFTMime ou la console de gestion du client. Lorsque vous réparez une application, vous supprimez les paramètres utilisateur personnalisés et restaurez les paramètres par défaut. Cette action ne modifie pas ou ne supprime aucun raccourci ou association de type de fichier, et ne supprime pas l’application du cache.

ClearApp

DWORD

Par défaut = 1

La valeur 1 permet à l’utilisateur d’utiliser l’action Effacer sur les applications dans SFTMime ou la console de gestion du client. Lorsque vous effacez une application de la console, vous ne pouvez plus utiliser cette application. Toutefois, l’application reste en cache et reste disponible pour les autres utilisateurs du même système. Après une actualisation de publication, les applications effacées seront de nouveau accessibles.

DeleteApp

DWORD

Par défaut = 0

La valeur 1 permet à l’utilisateur d’utiliser l’action de suppression sur les applications dans SFTMime ou la console de gestion du client. Lorsque vous supprimez une application, l’application sélectionnée ne sera plus disponible pour les utilisateurs de ce client. Les raccourcis et les associations de types de fichiers sont supprimés et l’application est supprimée du cache. Toutefois, si une autre application fait référence à des données dans le cache du système de fichiers ou des données de paramètres pour l’application sélectionnée, ces éléments ne seront pas supprimés.

Après une actualisation de publication, les applications supprimées vous sont à nouveau accessibles.

ToggleOfflineMode

DWORD

La valeur 1 permet aux utilisateurs de sélectionner l’exécution du client en mode hors connexion. En mode hors connexion, le client de virtualisation des applications peut démarrer une application chargée même lorsqu’elle n’est pas connectée à un serveur de virtualisation des applications.



## Paramètres personnalisés


La clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\CustomSettings contient des valeurs spécifiques aux composants frontaux. Tous les paramètres personnalisés sont stockés en tant que chaînes. Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé CustomSettings.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom </th>
<th align="left">Type </th>
<th align="left">Données (exemples) </th>
<th align="left">Description </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>TrayErrorDelay </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Par défaut = 30 </p></td>
<td align="left"><p>Durée en secondes pendant laquelle la zone de notification de virtualisation des applications affiche des messages d’erreur tels que le &quot; lancement a échoué &quot; . Valeur minimale de 1. </p></td>
</tr>
<tr class="even">
<td align="left"><p>TraySuccessDelay </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Par défaut = 10 </p></td>
<td align="left"><p>Durée en secondes pendant laquelle la zone de notification appvmed affiche des messages de réussite tels que &quot; Word lancé &quot; ou &quot; Excel s’arrête &quot; . Si la valeur est 0, ces messages seront supprimés. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>TrayVisibility</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 0</p></td>
<td align="left"><p>0 = afficher la barre d’État lorsque les applications virtualisées sont utilisées.</p>
<p>1 = afficher la barre d’État toujours.</p>
<p>2 = ne jamais afficher la barre d’État.</p></td>
</tr>
<tr class="even">
<td align="left"><p>TrayShowRefresh</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Lorsque la valeur est définie et définie sur 1, permet d’afficher les applications d’actualisation des éléments de menu dans le menu de la barre d’état système et est accessible à l’utilisateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TrayShowLoad</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Lorsque la valeur est définie et définie sur 1, permet à l’élément de menu de charger les applications affichées dans le menu de la barre d’état système et est accessible à l’utilisateur.</p></td>
</tr>
</tbody>
</table>



## Paramètres de création de rapports


La clé HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Reporting contient des valeurs propres à la création de rapports sur un serveur de gestion d’applications-V. Le tableau suivant fournit des informations sur les valeurs de Registre associées à la clé de création de rapports.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom </th>
<th align="left">Type </th>
<th align="left">Données (exemples) </th>
<th align="left">Description </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DataCacheLimit</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 20</p></td>
<td align="left"><p>Cette valeur spécifie la taille maximale en mégaoctets (Mo) du cache XML pour le stockage des informations de rapport. La taille s’applique au cache en mémoire. Lorsque la limite est atteinte, le fichier journal est restauré. Lors de l’ajout d’un nouvel enregistrement (en bas de la liste), un ou plusieurs des enregistrements les plus anciens (haut de la liste) seront supprimés pour pouvoir libérer de l’espace. Un message d’avertissement sera consigné dans le journal du client et dans le journal des événements la première fois que cela se produit, et il ne sera pas enregistré de nouveau tant qu’il n’a pas été correctement vidé lors de la transmission et que le journal aura été rempli de nouveau.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DataBlockSize</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Par défaut = 65536</p></td>
<td align="left"><p>Cette valeur spécifie la taille maximale en octets à transmettre au serveur en même temps lors de l’actualisation de la publication, afin d’éviter les échecs de transmission permanents lorsque le journal atteint une taille significative. La valeur par défaut est 65536. Lorsque vous transmettez des données de rapport au serveur, un bloc d’enregistrements d’application (inférieur ou égal à la taille du bloc en octets dans les données XML) est supprimé du cache et envoyé au serveur. Chaque bloc disposera des données générales du client et de la liste des packages globaux, et ces derniers ne seront pas pris en facteur dans les calculs de la taille du bloc. Il existe un potentiel pour une liste de packages extrêmement volumineux, qui engendre des échecs de transmission via des connexions à faible bande passante ou peu fiable.</p></td>
</tr>
</tbody>
</table>



## Rubriques connexes


[Référence d'Application Virtualization Client](application-virtualization-client-reference.md)









