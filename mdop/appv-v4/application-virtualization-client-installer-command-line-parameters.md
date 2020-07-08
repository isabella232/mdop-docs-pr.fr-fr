---
title: Paramètres de ligne de commande du programme d'installation d'Application Virtualization Client
description: Paramètres de ligne de commande du programme d'installation d'Application Virtualization Client
author: dansimp
ms.assetid: 508fa404-52a5-4919-8788-2a3dfb00639b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 911d333c80060c1881c96430c1d2d0516b6a4855
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808018"
---
# Paramètres de ligne de commande du programme d'installation d'Application Virtualization Client


Le tableau suivant répertorie tous les paramètres de ligne de commande du programme d’installation du client Microsoft Application Virtualization disponibles, leurs valeurs et une brève description de chaque paramètre. Les paramètres respectent la casse et doivent être entrés en lettres minuscules. Toutes les valeurs de paramètre doivent être placées entre guillemets doubles.

**Remarque**  
-   Pour App-V version 4,6, les paramètres de ligne de commande ne peuvent pas être utilisés lors d’une mise à niveau du client.

-   Les paramètres *SWICACHESIZE* et *MINFREESPACEMB* ne peuvent pas être combinés sur la ligne de commande. Si les deux sont utilisées, le paramètre *SWICACHESIZE* est ignoré.



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paramètre</th>
<th align="left">Doubl</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>ALLOWINDEPENDENTFILESTREAMING</em></p></td>
<td align="left"><p>TRUE</p>
<p>FALSE</p></td>
<td align="left"><p>Indique si la diffusion en continu à partir du fichier sera activée quelle que soit la façon dont le client a été configuré avec le <em> </em> paramètre APPLICATIONSOURCEROOT. Si elle est définie sur FALSe, le transport n’active pas la diffusion en continu à partir de fichiers, même si le paramètre OSD HREF ou <em> APPLICATIONSOURCEROOT </em> contient un chemin d’accès au fichier.</p>
<p>Valeurs possibles:</p>
<ul>
<li><p>TRUE: une application déployée manuellement est susceptible d’être chargée à partir du disque.</p></li>
<li><p>FALSe: toutes les applications doivent provient du serveur de diffusion de contenu source.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em>APPLICATIONSOURCEROOT</em></p></td>
<td align="left"><p><em>URL RTSP:// </em> (pour la remise de package dynamique)</p>
<p><em>URL </em> ou UNC <em> file:// </em> (pour le chargement à partir d’une remise de package de fichier)</p></td>
<td align="left"><p>Pour permettre à un administrateur ou à un système de distribution de logiciels électronique de garantir le chargement de l’application conformément au schéma de gestion topologique, autorise une substitution du code base OSD pour l’élément HREF de l’application (emplacement source). Si la valeur est «», qui est la valeur par défaut, les paramètres de fichier OSD existants sont utilisés.</p>
<p>Une URL est composée de plusieurs parties:</p>
<p>&lt;protocole &gt; :// &lt; serveur &gt; : &lt; chemin de port &gt; / &lt; &gt; / &lt; ? requête &gt; &lt; #fragment&gt;</p>
<p>Un chemin d’accès UNC comporte trois parties:</p>
<p>&amp;lt; NomOrdinateur &gt; &amp; lt; partager le dossier &gt; &amp; lt; ressource&gt;</p>
<p>Si le <em> </em> paramètre APPLICATIONSOURCEROOT est spécifié sur un client, le client rompt l’URL ou le chemin UNC d’un fichier OSD dans ses parties constitutives et remplace les sections d’OSD par les <em> sections APPLICATIONSOURCEROOT correspondantes </em> .</p>
<div class="alert">
<strong>Important</strong><br/><p>Veillez à utiliser le format approprié lors de l’utilisation de file://avec un chemin UNC. Le format approprié est file:// &amp; lt; Server &gt; &amp; lt; share &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>ICONSOURCEROOT</em></p></td>
<td align="left"><p><em>UNC</em></p>
<p>URL <em> http:// </em> ou https:// <em> URL</em></p></td>
<td align="left"><p>Permet à un administrateur de spécifier un emplacement source pour la récupération d’icône pour un package d’application séquencé lors de la publication. Les racines de source d’icône prennent en charge les chemins d’accès et les URL. Si la valeur est «», qui est la valeur par défaut, les paramètres de fichier OSD existants sont utilisés.</p>
<p>Une URL est composée de plusieurs parties:</p>
<p>&lt;protocole &gt; :// &lt; serveur &gt; : &lt; chemin de port &gt; / &lt; &gt; / &lt; ? requête &gt; &lt; #fragment&gt;</p>
<p>Un chemin d’accès UNC comporte trois parties:</p>
<p>&amp;lt; NomOrdinateur &gt; &amp; lt; partager le dossier &gt; &amp; lt; ressource&gt;</p>
<div class="alert">
<strong>Important</strong><br/><p>Veillez à utiliser le format approprié lors de l’utilisation d’un chemin UNC. Les formats admissibles sont &amp; lt; Server &gt; &amp; lt; share &gt; or &lt; Drive Letter &gt; : &amp; lt; Folder &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em>OSDSOURCEROOT</em></p></td>
<td align="left"><p><em>UNC</em></p>
<p>URL <em> http:// </em> ou https:// <em> URL</em></p></td>
<td align="left"><p>Permet à un administrateur de spécifier l’emplacement source de récupération de fichier OSD pour un package d’application au cours de la publication. Les racines de source de l’OSD prennent en charge les chemins d’accès et les URL. Si la valeur est «», qui est la valeur par défaut, les paramètres de fichier OSD existants sont utilisés.</p>
<p>Une URL est composée de plusieurs parties:</p>
<p>&lt;protocole &gt; :// &lt; serveur &gt; : &lt; chemin de port &gt; / &lt; &gt; / &lt; ? requête &gt; &lt; #fragment&gt;</p>
<p>Un chemin d’accès UNC comporte trois parties:</p>
<p>&amp;lt; NomOrdinateur &gt; &amp; lt; partager le dossier &gt; &amp; lt; ressource&gt;</p>
<div class="alert">
<strong>Important</strong><br/><p>Veillez à utiliser le format approprié lors de l’utilisation d’un chemin UNC. Les formats admissibles sont &amp; lt; Server &gt; &amp; lt; share &gt; or &lt; Drive Letter &gt; : &amp; lt; Folder &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>AUTOLOADONLOGIN</em></p>
<p><em>AUTOLOADONLAUNCH</em></p>
<p><em>AUTOLOADONREFRESH</em></p></td>
<td align="left"><p>[0 | 1]</p></td>
<td align="left"><p>Déclencheurs de chargement automatique qui définissent les événements de démarrage automatique des applications. Autoload utilise implicitement le streaming en arrière-plan pour permettre au chargement de l’application dans le cache.</p>
<p>Le bloc de fonctionnalité principal sera chargé le plus rapidement possible. Les blocs de fonctionnalités restants sont chargés en arrière-plan pour permettre les opérations au premier plan, telles que l’interaction utilisateur avec les applications, de manière à obtenir une priorité et des performances optimales.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Le <em> </em> paramètre AUTOLOADTARGET détermine les applications qui sont chargées automatiquement. Par défaut, les packages qui ont été utilisés sont chargés automatiquement, sauf si <em> AUTOLOADTARGET </em> est défini.</p>
</div>
<div>

</div>
<p>Chaque paramètre affecte le comportement de chargement comme suit:</p>
<ul>
<li><p><em>AUTOLOADONLOGIN </em> — le chargement s’exécute lorsque l’utilisateur se connecte.</p></li>
<li><p><em>AUTOLOADONLAUNCH </em> — le chargement démarre lorsque l’utilisateur démarre une application.</p></li>
<li><p><em>AUTOLOADONREFRESH </em> : le chargement s’exécute à l’actualisation de la publication.</p></li>
</ul>
<p>Les trois valeurs peuvent être combinées. Dans l’exemple suivant, les déclencheurs de chargement à deux utilisateurs sont activés lors de la connexion de l’utilisateur et lors de l’actualisation de la publication.</p>
<p><em>AUTOLOADONLOGIN AUTOLOADONREFRESH</em></p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si le client est configuré à l’aide de ces valeurs lors de la première installation, ce dernier ne sera pas déclenché tant que la prochaine fois que l’utilisateur se déconnecte et se reconnecte.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em>AUTOLOADTARGET</em></p></td>
<td align="left"><p>NÉANT</p>
<p>SES</p>
<p>PREVUSED</p></td>
<td align="left"><p>Indique ce qui sera chargé automatiquement lorsque des déclencheurs de chargement sont présents.</p>
<p>Valeurs possibles:</p>
<ul>
<li><p>AUCUN: il n’y a pas de chargement automatique, quels que soient les déclencheurs définis.</p></li>
<li><p>ALL: si aucun déclencheur de charge automatique n’est activé, tous les packages sont chargés automatiquement, qu’ils aient été ou non démarrés.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Ce paramètre est configuré pour des packages individuels à l’aide du SFTMIME <strong> Ajouter un package </strong> et <strong> configurer des commandes de package </strong> . Pour plus d’informations sur ces commandes, voir informations de référence sur les <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)"> commandes SFTMIME </a> .</p>
</div>
<div>

</div></li>
<li><p>PREVUSED: si des déclencheurs de chargement automatique sont activés, chargez uniquement les packages dans lesquels au moins une application dans le package a été précédemment utilisée (c’est-à-dire lancée ou prémise en cache).</p></li>
</ul>
<div class="alert">
<strong>Remarque</strong><br/><p>Lorsque vous installez le client App-V pour utiliser un cache en lecture seule (par exemple, dans le cadre d’une implémentation de serveur VDI), vous devez définir le <em> </em> paramètre AUTOLOADTARGET sur None pour empêcher le client d’essayer de mettre à jour des applications dans le cache en lecture seule.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>DOTIMEOUTMINUTES</em></p></td>
<td align="left"><p>29600 (par défaut)</p>
<p>1 – 1439998560 minutes (plage)</p></td>
<td align="left"><p>Indique le nombre de minutes d’utilisation d’une application en mode hors connexion.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>INSTALLDIR</em></p></td>
<td align="left"><p>&lt;accès&gt;</p></td>
<td align="left"><p>Spécifie le répertoire d’installation du client App-V.</p>
<p>Exemple: INSTALLDIR = &quot; C:\Program Files\Microsoft Application Virtualization Client&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>OPTIONNEL</em></p></td>
<td align="left"><p>PROPRIÉTÉ</p>
<p>“”</p></td>
<td align="left"><p>Les composants clients de Microsoft Application Virtualization seront mis à niveau par le biais de Microsoft Update lorsque des mises à jour sont disponibles pour le grand public. L’agent Microsoft Update sur lequel sont installés les systèmes d’exploitation Windows nécessite qu’un utilisateur puisse explicitement choisir d’utiliser le service. Ce choix n’est requis qu’une seule fois pour toutes les applications sur l’appareil. Si vous avez déjà choisi Microsoft Update, les composants Microsoft Application Virtualization sur l’appareil tirent automatiquement parti du service.</p>
<p>Dans le cadre de l’installation de la ligne de commande, l’utilisation de Microsoft Update est refusée par défaut (à moins qu’une application précédente ait déjà activé l’appareil à utiliser) en raison de la configuration manuelle de Microsoft Update. Par conséquent, l’option doit être explicite pour les installations de lignes de commande. La définition du paramètre de ligne de commande <em> optin </em> sur true force la définition de l’option de mise à jour de Microsoft.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>REQUIREAUTHORIZATIONIFCACHED</em></p></td>
<td align="left"><p>TRUE</p>
<p>FALSE</p></td>
<td align="left"><p>Indique si une autorisation est toujours requise, qu’une application soit déjà en cache ou non.</p>
<p>Valeurs possibles:</p>
<ul>
<li><p>TRUE: l’application doit toujours être autorisée au démarrage. Pour les applications RTSP transmis, le jeton d’autorisation de l’utilisateur est envoyé au serveur pour autorisation. Dans le cas des applications basées sur le fichier, les listes de Contrã’le d’accès de fichier indiquent si un utilisateur est susceptible d’accéder à l’application.</p></li>
<li><p>FALSe: Essayez toujours de vous connecter au serveur. Si une connexion au serveur ne peut pas être établie, le client permet toujours à l’utilisateur de lancer une application qui a déjà été chargée dans le cache.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWICACHESIZE</em></p></td>
<td align="left"><p>Taille du cache en Mo</p></td>
<td align="left"><p>Spécifie la taille en mégaoctets du cache client. La taille par défaut est 4096 Mo et la taille maximale est 1 048 576 Mo (1 to). Le système vérifie l’espace disponible au moment de l’installation, mais l’espace n’est pas réservé.</p>
<p>Par exemple: <strong> SWICACHESIZE = &quot; 1024&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRDISPLAY</em></p></td>
<td align="left"><p>Nom d’affichage</p></td>
<td align="left"><p>Spécifie le nom affiché du serveur de publication; obligatoire lorsque <em> SWIPUBSVRHOST </em> est utilisé.</p>
<p>Par exemple: <strong> SWIPUBSVRDISPLAY = &quot; environnement de production&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRTYPE</em></p></td>
<td align="left"><p>[HTTP | RTSP</p></td>
<td align="left"><p>Spécifie le type du serveur de publication. Le type du serveur par défaut est le serveur de virtualisation des applications. Le <strong> </strong> commutateur/Secure n’est pas sensible à la casse.</p>
<ul>
<li><p>HTTP: serveur HTTP standard</p></li>
<li><p>HTTP <strong> /Secure </strong> : serveur http de sécurité améliorée</p></li>
<li><p>RTSP: serveur de virtualisation des applications</p></li>
<li><p>RTSP <strong> /Secure </strong> : serveur de virtualisation des applications de sécurité améliorée</p></li>
</ul>
<p>Par exemple: <strong> SWIPUBSVRTYPE = &quot; http/Secure&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRHOST</em></p></td>
<td align="left"><p>Adresse IP | nom d’hôte</p></td>
<td align="left"><p>Spécifie l’adresse IP du serveur de virtualisation d’applications ou le nom d’hôte du serveur résolu dans l’adresse IP du serveur&#39;s; obligatoire lorsque <em> SWIPUBSVRDISPLAY </em> est utilisé.</p>
<p>Par exemple: <strong> SWIPUBSVRHOST = &quot; SERVEUR01&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRPORT</em></p></td>
<td align="left"><p>Numéro de port</p></td>
<td align="left"><p>Spécifie le port logique qui est utilisé par le serveur de virtualisation de l’application pour détecter les demandes du client (par défaut, 554).</p>
<ul>
<li><p>Serveur HTTP standard: par défaut, 80.</p></li>
<li><p>Serveur HTTP amélioré-sécurité par défaut: 443.</p></li>
<li><p>Serveur de virtualisation des applications: par défaut = 554.</p></li>
<li><p>Serveur de virtualisation des applications de sécurité améliorée: par défaut, 322.</p></li>
</ul>
<p>Par exemple: <strong> SWIPUBSVRPORT = &quot; 443&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRPATH</em></p></td>
<td align="left"><p>Nom du chemin d’accès</p></td>
<td align="left"><p>Spécifie l’emplacement sur le serveur de publication du fichier qui définit les associations de type de fichier (par défaut =/); obligatoire lorsque la <em> </em> valeur du paramètre SWIPUBSVRTYPE est http.</p>
<p>Par exemple: <strong> SWIPUBSVRPATH = &quot; /AppVirt/appsntypes.xml&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRREFRESH</em></p></td>
<td align="left"><p>[Sur | DÉCONNECTÉ</p></td>
<td align="left"><p>Indique si le client interroge automatiquement le serveur de publication pour les associations de types de fichiers et les applications lorsque l’utilisateur se connecte au client (par défaut, le = activé).</p>
<p>Par exemple: <strong> SWIPUBSVRREFRESH = &quot; off&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIGLOBALDATA</em></p></td>
<td align="left"><p>Global Data Directory</p></td>
<td align="left"><p>Spécifie le répertoire dans lequel les données seront stockées qui ne sont pas spécifiques aux utilisateurs spécifiques (par défaut, C:\Documents and Settings\All Users\Documents).</p>
<p>Exemple: <strong> SWIGLOBALDATA = &quot; D:\Microsoft Application Virtualization Client\Global&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIUSERDATA</em></p></td>
<td align="left"><p>Répertoire de données utilisateur</p></td>
<td align="left"><p>Spécifie le répertoire dans lequel les données seront stockées qui sont spécifiques aux utilisateurs spécifiques (par défaut =% APPDATA%).</p>
<p>Exemple: <strong> SWIUSERDATA = &quot; H:\Windows\Microsoft application de virtualisation des applications&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIFSDRIVE</em></p></td>
<td align="left"><p>Lettre de lecteur préférée</p></td>
<td align="left"><p>Correspond à la lettre du lecteur que vous avez sélectionnée pour le lecteur virtuel.</p>
<p>Par exemple: <strong> SWIFSDRIVE = &quot; S&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SYSTEMEVENTLOGLEVEL</em></p></td>
<td align="left"><p>0 à 4</p></td>
<td align="left"><p>Indique le niveau de journalisation dans lequel les messages du journal sont écrits dans le journal des événements Windows. La valeur indique un seuil de ce qui est enregistré, c’est-à-dire que tout est égal ou inférieur à cette valeur est consigné. Par exemple, une valeur de 0x3 (avertissement) indique que les avertissements (0x3), les erreurs (0X2) et les erreurs critiques (0x1) sont enregistrées.</p>
<p>Valeurs possibles:</p>
<ul>
<li><p>0 = = aucun</p></li>
<li><p>1 = = critique</p></li>
<li><p>2 = = erreur</p></li>
<li><p>3 = = AVERTISSEMENT</p></li>
<li><p>4 = = informations</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em>MINFREESPACEMB</em></p></td>
<td align="left"><p>En Mo</p></td>
<td align="left"><p>Spécifie la quantité d’espace libre (en mégaoctets) qui doit être disponible sur l’hôte avant que la taille de cache ne puisse augmenter. L’exemple suivant configure le client pour vérifier qu’il s’agit d’au moins 5 Go d’espace libre sur le disque avant d’autoriser l’augmentation de la taille du cache. La valeur par défaut est 5000 Mo d’espace libre disponible sur le disque au moment de l’installation.</p>
<p>Exemple: <strong> MINFREESPACEMB = &quot; 5000 &quot; (5 Go)</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>KEEPCURRENTSETTINGS</em></p></td>
<td align="left"><p>[0 | 1]</p></td>
<td align="left"><p>Utilisé lorsque vous avez appliqué des paramètres de Registre avant de déployer un client, par exemple, à l’aide d’une stratégie de groupe. Lors du déploiement d’un client, définissez ce paramètre sur une valeur de 1 pour ne pas remplacer les paramètres du Registre.</p>
<div class="alert">
<strong>Important</strong><br/><p>Si la valeur est égale à 1, les paramètres de ligne de commande du programme d’installation du client suivants sont ignorés:</p>
<p><strong>SWICACHESIZE </strong> , <strong> MINFREESPACEMB </strong> , <strong> ALLOWINDEPENDENTFILESTREAMING </strong> , <strong> APPLICATIONSOURCEROOT </strong> , <strong> IconSourceRoot </strong> , <strong> OSDSourceRoot </strong> , <strong> SYSTEMEVENTLOGLEVEL </strong> , <strong> SWIGLOBALDATA </strong> , <strong> DOTIMEOUTMINUTES </strong> , <strong> SWIFSDRIVE </strong> , <strong> AUTOLOADTARGET </strong> , <strong> AUTOLOADTRIGGERS et </strong> <strong> SWIUSERDATA </strong> .</p>
<p>Pour plus d’informations sur la définition de ces valeurs après l’installation, voir la section «Comment configurer les paramètres du registre des clients App-V à l’aide de la ligne de commande» dans le guide des opérations d’application (App-V) <a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)"> https://go.microsoft.com/fwlink/?LinkId=122939 </a> .</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Rubriques connexes


[Procédure pour installer manuellement Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Procédure pour mettre à niveau Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)

[Référence de commande SFTMIME](sftmime--command-reference.md)









