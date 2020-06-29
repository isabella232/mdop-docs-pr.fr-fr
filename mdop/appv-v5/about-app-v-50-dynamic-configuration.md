---
title: À propos de la configuration dynamique d'App-V5.0
description: À propos de la configuration dynamique d'App-V5.0
author: dansimp
ms.assetid: 88afaca1-68c5-45c4-a074-9371c56b5804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0294a60570d6dea99193c8bd411639c4888ae6b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806145"
---
# À propos de la configuration dynamique d'App-V5.0


Vous pouvez utiliser la configuration dynamique pour personnaliser un package App-V 5,0 pour un utilisateur. Utilisez les informations suivantes pour créer ou modifier un fichier de configuration dynamique existant.

Lorsque vous modifiez le fichier de configuration dynamique, il personnalise la façon dont un utilisateur ou un groupe peut exécuter un package App-V 5,0. Cela permet de fournir une méthode plus pratique pour la personnalisation du package en supprimant la nécessité de réorganiser les packages à l’aide des paramètres souhaités et permet de maintenir le contenu du package et les paramètres personnalisés indépendants.

## Avancé: configuration dynamique


Les packages d’application virtuels contiennent un manifeste qui fournit toutes les informations fondamentales pour le package. Ces informations incluent les valeurs par défaut des paramètres du package et déterminent les paramètres du formulaire le plus basique (sans personnalisation supplémentaire). Si vous voulez ajuster ces valeurs par défaut pour un utilisateur ou un groupe particulier, vous pouvez créer et modifier les fichiers suivants:

-   Fichier de configuration de l’utilisateur

-   Fichier de configuration de déploiement

Les fichiers. xml précédents spécifient les paramètres du package et permettent la personnalisation des packages sans affecter directement les packages. Lors de la création d’un package, le Sequencer génère automatiquement les fichiers de déploiement par défaut et de configuration de l’utilisateur à l’aide des données de manifeste du package. C’est la raison pour laquelle ces fichiers de configuration génèrent automatiquement des paramètres par défaut que le package de la part de l’utilisation de la configuration au cours de la séquence. Si vous appliquez ces fichiers de configuration à un package dans le formulaire généré par le Sequencer, les packages présentent les mêmes paramètres par défaut que le manifeste. Cela vous permet d’accéder à un modèle spécifique au package pour commencer si l’un des paramètres par défaut doit être modifié.

**Remarques**  Les informations suivantes peuvent uniquement être utilisées pour modifier les fichiers de configuration générés par Sequencer afin de personnaliser les packages pour répondre à des exigences spécifiques en matière d’utilisateur ou de groupe.

 

### Contenu du fichier de configuration dynamique

Tous les ajouts, suppressions et mises à jour des fichiers de configuration doivent être effectués en relation avec les valeurs par défaut spécifiées par les informations de manifeste du package. Consultez le tableau suivant:

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Fichier de configuration de l’utilisateur. Xml</p></td>
</tr>
<tr class="even">
<td align="left"><p>Fichier Configuration. XML de déploiement</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manifeste du package</p></td>
</tr>
</tbody>
</table>

 

Le tableau précédent représente la façon dont les fichiers sont lus. La première entrée représente ce qui sera lu en dernier, par conséquent, son contenu est prioritaire. Par conséquent, tous les packages contiennent fondamentalement et fournissent des paramètres par défaut à partir du manifeste du package. Si un fichier de configuration de déploiement. XML avec des paramètres personnalisés est appliqué, il remplace les valeurs par défaut de manifeste de package. Si un fichier de configuration utilisateur. XML avec des paramètres personnalisés est appliqué avant cela, la configuration du déploiement et les valeurs par défaut du manifeste du package sont ignorées.

La liste suivante présente des informations supplémentaires sur les deux types de fichiers:

-   **Fichier de configuration utilisateur (UserConfig)** : permet de spécifier ou de modifier des paramètres personnalisés pour un package. Ces paramètres seront appliqués pour un utilisateur spécifique lorsque le package est déployé sur un ordinateur exécutant le client App-V 5,0.

-   **Fichier de configuration de déploiement (DeploymentConfig)** : permet de spécifier ou de modifier les paramètres par défaut d’un package. Ces paramètres s’appliquent à tous les utilisateurs lors du déploiement d’un package sur un ordinateur exécutant le client App-V 5,0.

Pour personnaliser les paramètres d’un package pour un ensemble spécifique d’utilisateurs sur un ordinateur ou pour apporter des modifications qui seront appliquées aux emplacements des utilisateurs locaux tels que HKCU, le fichier UserConfig doit être utilisé. Pour modifier les paramètres par défaut d’un package pour tous les utilisateurs sur un ordinateur ou pour apporter des modifications qui seront appliquées aux emplacements globaux tels que HKEY \ _LOCAL \ _MACHINE et le dossier All Users, le fichier DeploymentConfig doit être utilisé.

Le fichier UserConfig fournit des paramètres de configuration qui peuvent être appliqués à un utilisateur unique sans affecter d’autres utilisateurs sur un client:

-   Extensions intégrées au système natif par utilisateur:-raccourcis, associations de types de fichiers, protocoles d’URL, AppPaths, clients logiciels et COM

-   Sous-systèmes virtuels:-objets d’application, variables d’environnement, modifications du Registre, services et polices

-   Scripts (contexte utilisateur uniquement)

-   Autorité de gestion (pour contrôler la co-existence d’un package avec App-V 4,6)

Le fichier DeploymentConfig fournit des paramètres de configuration dans deux sections, l’un pour le contexte de l’ordinateur et l’autre relatif au contexte de l’utilisateur, qui fournit les mêmes fonctionnalités que celles indiquées dans la liste UserConfig ci-dessus:

-   Tous les paramètres de UserConfig ci-dessus.

-   Extensions qui ne peuvent être appliquées globalement que par tous les utilisateurs

-   Les sous-systèmes virtuels qui peuvent être configurés pour les emplacements globaux de l’ordinateur (par exemple, registre)

-   URL de la source de produit

-   Scripts (contexte de l’ordinateur uniquement)

-   Contrôles pour arrêter les processus enfants

### Structure de fichier

La structure du fichier de configuration dynamique App-V 5,0 est expliquée dans la section suivante.

### Fichier de configuration utilisateur dynamique

**Header** : l’en-tête d’un fichier de configuration utilisateur dynamique se présente comme suit:

&lt;? XML version = "1.0" Encoding = "UTF-8"? &gt; &lt; UserConfiguration **PackageId**= "1F8488bf-2257-46B4-B27F-09c9dbaae707" DisplayName = "réservé" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

**PackageId** est de la même valeur qu’existe dans le fichier manifeste.

**Corps** -le corps du fichier de configuration de l’utilisateur dynamique peut inclure tous les points d’extension d’application définis dans le fichier manifeste ainsi que les informations de configuration des applications virtuelles. Quatre sous-sections sont autorisées dans le corps de texte:

1. **Applications** : toutes les extensions d’application contenues dans le fichier manifeste au sein d’un package sont affectées avec un ID d’application, qui est également défini dans le fichier manifeste. Cela vous permet d’activer ou de désactiver toutes les extensions pour une application donnée au sein d’un package. L' **ID d’application** doit exister dans le fichier manifeste ou être ignoré.

   &lt;UserConfiguration **PackageId**= "1F8488bf-2257-46B4-B27F-09c9dbaae707" DisplayName = "réservé" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

   &lt;Applications&gt;

   &lt;!--Aucune nouvelle application ne peut être définie dans Policy. Le client AppV ignorera tout ID d’application qui n’est pas également présent dans le fichier manifeste:&gt;

   &lt;ID d’application = "{a56fa627-c35f-4A01-9e79-7d36aed8225a}" enabled = "false"&gt;

   &lt;/Application&gt;

   &lt;/Applications&gt;

   …

   &lt;/UserConfiguration&gt;

2. Les sous- **systèmes** -nouvel appextensions et les autres sous-systèmes sont organisés en tant que sous-nœuds dans les sous &lt; -systèmes &gt; :

   &lt;UserConfiguration **PackageId**= "1F8488bf-2257-46B4-B27F-09c9dbaae707" DisplayName = "réservé" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

   &lt;Sous-systèmes&gt;

   ..

   &lt;/Subsystems&gt;

   ..

   &lt;/UserConfiguration&gt;

   Chaque sous-système peut être activé/désactivé à l’aide de l’attribut «**activé**». Vous trouverez ci-dessous les divers exemples de sous-systèmes et d’utilisation.

   **Variable**

   Quelques extensions de contrôle de sous-systèmes (sous-systèmes d’extension). Ces sous-systèmes sont: des raccourcis clavier, des associations de types de fichiers, des protocoles d’URL, des AppPaths, des clients logiciels et des COM

   Les sous-systèmes d’extension peuvent être activés ou désactivés indépendamment du contenu.  Par conséquent, si des raccourcis sont activés, le client utilisera par défaut les raccourcis contenus dans le manifeste. Chaque sous-système d’extension peut contenir un &lt; &gt; nœud extensions. Si cet élément enfant est présent, le client ignore le contenu du fichier manifeste du sous-système et utilise uniquement le contenu du fichier de configuration.

   Exemple utilisant le sous-système de raccourcis:

   1.  Si l’utilisateur a défini cette valeur dans le fichier de configuration du déploiement ou du fichier dynamique:

                                    **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions&gt;**

                                                 ...

                                                **&lt;/Extensions&gt;**

                                    **&lt;/Shortcuts&gt;**

                         Content in the manifest will be ignored.   

   2.  Si l’utilisateur a défini uniquement ce qui suit:

                                   **&lt;Shortcuts  Enabled="true"/&gt;**

                         Then the content in the Manifest will be integrated during publishing.

   3.  Si l’utilisateur définit ce qui suit:

                                  **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions/&gt;**

                                    **&lt;/Shortcuts&gt;**

   Tous les raccourcis du manifeste seront tout de même ignorés. Aucun raccourci n’est intégré.

   Les sous-systèmes d’extension pris en charge sont les suivants:

   **Raccourcis clavier:** Ce contrôle contrôle les raccourcis qui seront intégrés au système local. Vous trouverez ci-dessous un exemple avec 2 raccourcis:

   &lt;Sous-systèmes&gt;

   &lt;Raccourcis activés: "vrai"&gt;

     &lt;Extensions&gt;

       &lt;Extension Category="AppV.Shortcut"&gt;

         &lt;Shortcut&gt;

           &lt;File&gt;\[{Common Programs}\]\\Microsoft Contoso\\Microsoft ContosoApp Filler 2010.lnk&lt;/File&gt;

           &lt;Target&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/Target&gt;

           &lt;Icon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\inficon.exe&lt;/Icon&gt;

           &lt;Arguments /&gt;

           &lt;WorkingDirectory /&gt;

           &lt;AppUserModelId&gt;ContosoApp.Filler.3&lt;/AppUserModelId&gt;

           &lt;Description&gt;Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.&lt;/Description&gt;

           &lt;Hotkey&gt;0&lt;/Hotkey&gt;

           &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

           &lt;ApplicationId&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/ApplicationId&gt;

         &lt;/Shortcut&gt;

     &lt;/Extension&gt;

     &lt;Extension catégorie = "AppV. Shortcut"&gt;

       &lt;Shortcut&gt;

         &lt;File&gt;\[{AppData}\]\\Microsoft\\Contoso\\Recent\\Templates.LNK&lt;/File&gt;

         &lt;Target&gt;\[{AppData}\]\\Microsoft\\Templates&lt;/Target&gt;

         &lt;Icon /&gt;

         &lt;Arguments /&gt;

         &lt;WorkingDirectory /&gt;

         &lt;AppUserModelId /&gt;

         &lt;Description /&gt;

         &lt;Hotkey&gt;0&lt;/Hotkey&gt;

         &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

         &lt;!-- Note the ApplicationId is optional --&gt;

       &lt;/Shortcut&gt;

     &lt;/Extension&gt;

    &lt;/Extensions&gt;

   &lt;/Shortcuts&gt;

   **Associations de types de fichiers:** Associe des types de fichiers à des programmes pour s’ouvrir par défaut et configure le menu contextuel. (Le type MIME peut également être configuré à l’aide de ce susbsystem). L’exemple d’association de type de fichier est le suivant:

   &lt;FileTypeAssociations activé = "vrai"&gt;

   &lt;Extensions&gt;

     &lt;Extension category = "AppV. FileTypeAssociation"&gt;

       &lt;FileTypeAssociation&gt;

         &lt;FileExtension MimeAssociation="true"&gt;

         &lt;Name&gt;.docm&lt;/Name&gt;

         &lt;ProgId&gt;contosowordpad.DocumentMacroEnabled.12&lt;/ProgId&gt;

         &lt;PerceivedType&gt;document&lt;/PerceivedType&gt;

         &lt;ContentType&gt;application/vnd.ms-contosowordpad.document.macroEnabled.12&lt;/ContentType&gt;

         &lt;OpenWithList&gt;

           &lt;ApplicationName&gt;wincontosowordpad.exe&lt;/ApplicationName&gt;

         &lt;/OpenWithList&gt;

        &lt;OpenWithProgIds&gt;

           &lt;ProgId&gt;contosowordpad.8&lt;/ProgId&gt;

         &lt;/OpenWithProgIds&gt;

         &lt;ShellNew&gt;

           &lt;Command /&gt;

           &lt;DataBinary /&gt;

           &lt;DataText /&gt;

           &lt;FileName /&gt;

           &lt;NullFile&gt;true&lt;/NullFile&gt;

           &lt;ItemName /&gt;

           &lt;IconPath /&gt;

           &lt;MenuText /&gt;

           &lt;Handler /&gt;

         &lt;/ShellNew&gt;

       &lt;/FileExtension&gt;

       &lt;ProgId&gt;

          &lt;Name&gt;contosowordpad.DocumentMacroEnabled.12&lt;/Name&gt;

           &lt;DefaultIcon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\contosowordpadicon.exe,15&lt;/DefaultIcon&gt;

           &lt;Description&gt;Blah Blah Blah&lt;/Description&gt;

           &lt;FriendlyTypeName&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,9182&lt;/FriendlyTypeName&gt;

           &lt;InfoTip&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,1424&lt;/InfoTip&gt;

           &lt;EditFlags&gt;0&lt;/EditFlags&gt;

           &lt;ShellCommands&gt;

             &lt;DefaultCommand&gt;Open&lt;/DefaultCommand&gt;

             &lt;ShellCommand&gt;

                &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

                &lt;Name&gt;Edit&lt;/Name&gt;

                &lt;FriendlyName&gt;&Edit&lt;/FriendlyName&gt;

                &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /vu "%1"&lt;/CommandLine&gt;

             &lt;/ShellCommand&gt;

             &lt;/ShellCommand&gt;

               &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

               &lt;Name&gt;Open&lt;/Name&gt;

               &lt;FriendlyName&gt;&Open&lt;/FriendlyName&gt;

               &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /n "%1"&lt;/CommandLine&gt;

               &lt;DropTargetClassId /&gt;

               &lt;DdeExec&gt;

                 &lt;Application&gt;mscontosowordpad&lt;/Application&gt;

                 &lt;Topic&gt;ShellSystem&lt;/Topic&gt;

                 &lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;

                 &lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;

               &lt;/DdeExec&gt;

             &lt;/ShellCommand&gt;

           &lt;/ShellCommands&gt;

         &lt;/ProgId&gt;

        &lt;/FileTypeAssociation&gt;

      &lt;/Extension&gt;

     &lt;/Extensions&gt;

     &lt;/FileTypeAssociations&gt;

   **Protocoles d’URL**: cette commande contrôle les protocoles d’URL intégrés au registre local de l’ordinateur client (par exemple, «mailto:»).

   &lt;URLProtocols activé = "vrai"&gt;

   &lt;Extensions&gt;

   &lt;Extension category = "AppV. URLProtocol"&gt;

   &lt;URLProtocol&gt;

     &lt;Nom &gt; mailto &lt; /Name&gt;

     &lt;ApplicationURLProtocol&gt;

     &lt;DefaultIcon &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403 &lt; /DefaultIcon&gt;

     &lt;EditFlags &gt; 2 &lt; /EditFlags&gt;

     &lt;Description&gt;

     &lt;Ayant&gt;

     &lt;FriendlyTypeName /&gt;

     &lt;Info&gt;

   &lt;SourceFilter /&gt;

     &lt;ShellFolder /&gt;

     &lt;WebNavigableCLSID /&gt;

     &lt;ExplorerFlags &gt; 2 &lt; /ExplorerFlags&gt;

     &lt;CLSID&gt;

     &lt;ShellCommands&gt;

     &lt;DefaultCommand &gt; ouvrir &lt; /DefaultCommand&gt;

     &lt;ShellCommand&gt;

     &lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationId&gt;

     &lt;Nom &gt; ouvert &lt; /Name&gt;

     &lt;CommandLine &gt; \ [{ProgramFilesX86} \\Microsoft Contoso\\Contoso\\contosomail.EXE "-c OEP. Remarque/m "%1" &lt; /CommandLine&gt;

     &lt;DropTargetClassId /&gt;

     &lt;FriendlyName&gt;

     &lt;Étendu &gt; 0 &lt; /Extended&gt;

     &lt;LegacyDisable &gt; 0 &lt; /LegacyDisable&gt;

     &lt;SuppressionPolicy &gt; 2 &lt; /SuppressionPolicy&gt;

      &lt;DdeExec&gt;

     &lt;NoActivateHandler /&gt;

     &lt;Application &gt; ContosoMail &lt; /application&gt;

     &lt;Rubrique &gt; ShellSystem &lt; /topic&gt;

     &lt;IfExec &gt; \ [SHELLNOOP \] &lt; /IfExec&gt;

     &lt;DdeCommand &gt; \ [SetForeground \] \ [ShellNewDatabase "%1" \] &lt; /DdeCommand&gt;

     &lt;/DdeExec&gt;

     &lt;/ShellCommand&gt;

     &lt;/ShellCommands&gt;

     &lt;/ApplicationURLProtocol&gt;

     &lt;/URLProtocol&gt;

     &lt;/Extension&gt;

     &lt;/Extension&gt;

     &lt;/URLProtocols&gt;

   **Clients logiciels**: permet à l’application de s’inscrire en tant que client de messagerie, lecteur de News, lecteur multimédia et rend l’application visible dans l’interface utilisateur définir l’accès aux programmes et aux paramètres de l’ordinateur. Dans la plupart des cas, vous devez seulement les activer et les désactiver. Il existe également un contrôle permettant d’activer et de désactiver le client de messagerie de manière spécifique si vous souhaitez que les autres clients restent activés, à l’exception de ce client.

   &lt;SoftwareClients activé = "vrai"&gt;

     &lt;ClientConfiguration EmailEnabled = "false"/&gt;

   &lt;/SoftwareClients&gt;

   AppPaths:-si une application par exemple contoso.exe est inscrite à l’aide d’un nom appPath de «MyApp», elle permet de taper «MyApp» sous le menu Exécuter et il ouvre contoso.exe.

   &lt;AppPaths activé = "vrai"&gt;

   &lt;Extensions&gt;

   &lt;Extension category = "AppV. AppPath"&gt;

   &lt;AppPath&gt;

     &lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationId&gt;

     &lt;Nom &gt;contosomail.exe&lt; /nom&gt;

     &lt;ApplicationPath &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationPath&gt;

     &lt;PATHEnvironmentVariablePrefix /&gt;

     &lt;CanAcceptUrl &gt; false &lt; /CanAcceptUrl&gt;

     &lt;SaveUrl /&gt;

   &lt;/AppPath&gt;

   &lt;/Extension&gt;

   &lt;/Extensions&gt;

   &lt;/AppPaths&gt;

   **Com**: permet à une application de s’inscrire aux serveurs com locaux. Le mode peut être intégré, isolé ou désactivé. Lorsque isol.

   &lt;Mode COM = "isolé"/&gt;

   **Autres paramètres**:

   Outre les extensions, il est possible d’activer/de désactiver et de modifier d’autres sous-systèmes:

   **Objets de noyau virtuel**:

   &lt;Objets activés = "faux"/&gt;

   **Registre virtuel**: utilisé si vous voulez définir un registre dans le registre virtuel dans HKCU

   &lt;Registry Enabled = "true"&gt;

   &lt;Agir&gt;

   &lt;Chemin clé = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\ABC"&gt;

   &lt;Type de valeur = «REG \ _SZ» Name = «bar» Data = «NewValue»/&gt;

    &lt;/Key&gt;

     &lt;Chemin clé = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\EmptyKey"/&gt;

    &lt;/Include&gt;

   &lt;Annuler&gt;

     &lt;/Registry&gt;

   **Système de fichiers virtuel**

         &lt;FileSystem Enabled="true" /&gt;

   **Polices virtuelles**

         &lt;Fonts Enabled="false" /&gt;

   **Variables d’environnement virtuel**

   &lt;EnvironmentVariables activé = "vrai"&gt;

   &lt;Agir&gt;

          &lt;Variable Name="UserPath" Value="%path%;%UserProfile%" /&gt;

          &lt;Variable Name="UserLib" Value="%UserProfile%\\ABC" /&gt;

          &lt;/Include&gt;

         &lt;Delete&gt;

          &lt;Variable Name="lib" /&gt;

           &lt;/Delete&gt;

           &lt;/EnvironmentVariables&gt;

   **Services virtuels**

         &lt;Services Enabled="false" /&gt;

3. **Userscripts** : les scripts peuvent être utilisés pour configurer ou altérer l’environnement virtuel, ainsi que pour exécuter des scripts au moment du déploiement ou de la suppression, avant qu’une application s’exécute, ou qu’elle puisse être utilisée pour «nettoyer» l’environnement après l’arrêt de l’application. Pour voir un exemple de script, veuillez vous référer au fichier de configuration de l’utilisateur qui est généré par le Sequencer. La section scripts ci-dessous fournit des informations supplémentaires sur les différents déclencheurs qui peuvent être utilisés.

4. **ManagingAuthority** -peut être utilisé lorsque 2 versions de votre package sont coexistantes sur le même ordinateur, l’une ayant été déployée vers App-v 4,6 et l’autre déployée sur app-v 5,0. Pour permettre à App-V vNext de prendre en charge les points d’extension 4,6 App-V pour le package nommé, entrez ce qui suit dans le fichier UserConfig (où PackageName est le GUID du package dans App-V 4,6:

   &lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = "032630c0-B8E2-417C-ACEF-76fc5297fe81"/&gt;

### Fichier de configuration du déploiement dynamique

**Header** : l’en-tête d’un fichier de configuration de déploiement est le suivant:

&lt;? XML version = "1.0" Encoding = "UTF-8"? &gt; &lt; DeploymentConfiguration **PackageId**= "1F8488bf-2257-46B4-B27F-09c9dbaae707" DisplayName = "réservé" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;

**PackageId** est de la même valeur qu’existe dans le fichier manifeste.

**Corps** -le corps du fichier de configuration de déploiement comporte deux sections:

-   Section Configuration utilisateur: autorise le même contenu que le fichier de configuration utilisateur décrit dans la section précédente. Lorsque le package est publié par un utilisateur, tous les paramètres de configuration nouvel appextensions de cette section remplacent les paramètres correspondants dans le manifeste du package, sauf si un fichier de configuration utilisateur est également fourni. Si un fichier UserConfig est également fourni, il est utilisé à la place des paramètres utilisateur dans le fichier de configuration de déploiement. Si le package est publié globalement, seul le contenu du fichier de configuration de déploiement sera utilisé en combinaison avec le manifeste.

-   Section Configuration de l’ordinateur: contient des informations qui peuvent être configurées uniquement pour la totalité d’un ordinateur, et non pour un utilisateur spécifique de l’ordinateur. Par exemple, HKEY \ _LOCAL \ _MACHINE clés de Registre dans le VFS.

&lt;DeploymentConfiguration **PackageId**= "1F8488bf-2257-46B4-B27F-09c9dbaae707" DisplayName = "réservé" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;

&lt;UserConfiguration&gt;

  ..

&lt;/UserConfiguration&gt;

&lt;MachineConfiguration&gt;

..

&lt;/MachineConfiguration&gt;

..

&lt;/MachineConfiguration&gt;

&lt;/DeploymentConfiguration&gt;

**Configuration utilisateur** -utilisez la section précédente du **fichier de configuration utilisateur dynamique** pour plus d’informations sur les paramètres fournis dans la section Configuration de l’utilisateur du fichier de configuration du déploiement.

Configuration de l’ordinateur: la section Configuration de l’ordinateur du fichier de configuration du déploiement permet de configurer des informations qui ne peuvent être définies que sur un ordinateur entier, et non pour un utilisateur spécifique de l’ordinateur. Par exemple, HKEY \ _LOCAL \ _MACHINE clés de Registre dans le registre virtuel. Quatre sous-sections sont autorisées dans cet élément.

1.  Les sous- **systèmes** -nouvel appextensions et les autres sous-systèmes sont organisés en tant que sous-nœuds dans les sous &lt; -systèmes &gt; :

    &lt;MachineConfiguration&gt;

      &lt;Sous-systèmes&gt;

      ..

      &lt;/Subsystems&gt;

    ..

    &lt;/MachineConfiguration&gt;

    La section suivante présente les différents exemples d’utilisation et de sous-systèmes.

    **Extensions**:

    Certaines extensions de contrôle de sous-systèmes (sous-systèmes d’extension) qui ne peuvent être appliquées que par tous les utilisateurs. Le sous-système est une fonctionnalité de l’application. Dans la mesure où cela peut s’appliquer uniquement à tous les utilisateurs, le package doit être publié globalement pour que ce type d’extension soit intégré au système local. Les mêmes règles relatives aux contrôles et aux paramètres qui s’appliquent aux extensions de configuration utilisateur s’appliquent également à celles de la section MachineConfiguration.

    **Fonctionnalités**de l’application: utilisée par défaut dans l’interface du système d’exploitation Windows. Permet à une application de s’enregistrer en tant qu’il est en mesure d’ouvrir certaines extensions de fichier (par exemple, pour le menu Démarrer, emplacement du navigateur Internet, capable d’ouvrir certains types MIME Windows).Par ailleurs, cette extension rend l’application virtuelle visible dans l’interface utilisateur définir les programmes par défaut.

    &lt;ApplicationCapabilities activé = "vrai"&gt;

      &lt;Extensions&gt;

       &lt;Extension category = "AppV. ApplicationCapabilities"&gt;

        &lt;ApplicationCapabilities&gt;

         &lt;ApplicationId&gt;\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe&lt;/ApplicationId&gt;

         &lt;Reference&gt;

          &lt;Name&gt;LitView Browser&lt;/Name&gt;

          &lt;Path&gt;SOFTWARE\\LitView\\Browser\\Capabilities&lt;/Path&gt;

         &lt;/Reference&gt;

       &lt;CapabilityGroup&gt;

        &lt;Capabilities&gt;

         &lt;Name&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12345&lt;/Name&gt;

         &lt;Description&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12346&lt;/Description&gt;

         &lt;Hidden&gt;0&lt;/Hidden&gt;

         &lt;EMailSoftwareClient&gt;Lit View E-Mail Client&lt;/EMailSoftwareClient&gt;

         &lt;FileAssociationList&gt;

          &lt;FileAssociation Extension=".htm" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".html" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".shtml" ProgID="LitViewHTML" /&gt;

         &lt;/FileAssociationList&gt;

         &lt;MIMEAssociationList&gt;

          &lt;MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" /&gt;

          &lt;MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" /&gt;

         &lt;/MIMEAssociationList&gt;

        &lt;URLAssociationList&gt;

          &lt;URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" /&gt;

         &lt;/URLAssociationList&gt;

         &lt;/Capabilities&gt;

      &lt;/CapabilityGroup&gt;

       &lt;/ApplicationCapabilities&gt;

      &lt;/Extension&gt;

    &lt;/Extensions&gt;

    &lt;/ApplicationCapabilities&gt;

    **Autres paramètres**:

    Outre les extensions, d’autres sous-systèmes peuvent être modifiés:

    **Registre virtuel d’ordinateur**à l’échelle: utilisé lorsque vous voulez définir une clé de Registre dans le registre virtuel dans HKEY \ _Local \ _Machine

    &lt;Registry&gt;

    &lt;Agir&gt;

      &lt;Chemin clé = «\\REGISTRY\\Machine\\Software\\ABC»&gt;

        &lt;Value Type="REG\_SZ" Name="Bar" Data="Baz" /&gt;

       &lt;/Key&gt;

      &lt;Clé path = "\\REGISTRY\\Machine\\Software\\EmptyKey"/&gt;

     &lt;/Include&gt;

    &lt;Annuler&gt;

    &lt;/Registry&gt;

    **Objets de noyau virtuel de l’ordinateur**

    &lt;Objets&gt;

    &lt;NotIsolate&gt;

       &lt;Nom de l’objet = "testObject"/&gt;

     &lt;/NotIsolate&gt;

    &lt;/Objects&gt;

2.  **ProductSourceURLOptOut**: indique si l’URL du package peut être modifiée globalement via PackageSourceRoot (pour prendre en charge les scénarios de succursales). La valeur par défaut est false et la modification du paramètre est appliquée au prochain lancement.  

    &lt;MachineConfiguration&gt;

      .. 

      &lt;ProductSourceURLOptOut activé = "vrai"/&gt;

      ..

    &lt;/MachineConfiguration&gt;

3.  **MachineScripts** : package peut être configuré pour exécuter des scripts au moment du déploiement, de la publication ou de la suppression. Veuillez référencer un exemple de fichier de configuration de déploiement généré par le Sequencer pour voir un exemple de script. La section scripts ci-dessous fournit des informations supplémentaires sur les différents déclencheurs qui peuvent être utilisés.

4.  **TerminateChildProcess**:-un exécutable de l’application peut être spécifié, dont le processus enfant va être arrêté lorsque le processus exe de l’application est arrêté.

    &lt;MachineConfiguration&gt;

      ..   

      &lt;TerminateChildProcesses&gt;

        &lt;Application Path="\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE" /&gt;

        &lt;Application Path="\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe" /&gt;

        &lt;Application Path="\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE" /&gt;

      &lt;/TerminateChildProcesses&gt;

      ..

    &lt;/MachineConfiguration&gt;

### Scripts

Le tableau suivant décrit les différents événements de script et le contexte dans lequel ils peuvent être exécutés.

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
<th align="left">Temps d’exécution du script</th>
<th align="left">Peuvent être spécifiées dans la configuration de déploiement</th>
<th align="left">Peuvent être spécifiés dans la configuration de l’utilisateur</th>
<th align="left">Peut s’exécuter dans l’environnement virtuel du package</th>
<th align="left">Peut être exécuté dans le contexte d’une application spécifique.</th>
<th align="left">S’exécute dans le contexte système/utilisateur (configuration du déploiement, configuration de l’utilisateur).</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AddPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(SYSTÈME, NO/A)</p></td>
</tr>
<tr class="even">
<td align="left"><p>PublishPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Système, utilisateur)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UnpublishPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Système, utilisateur)</p></td>
</tr>
<tr class="even">
<td align="left"><p>RemovePackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(SYSTÈME, NO/A)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartProcess</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>(Utilisateur, utilisateur)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ExitProcess</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>(Utilisateur, utilisateur)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartVirtualEnvironment</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Utilisateur, utilisateur)</p></td>
</tr>
<tr class="even">
<td align="left"><p>TerminateVirtualEnvironment</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Utilisateur, utilisateur)</p></td>
</tr>
</tbody>
</table>

 

### Créer un fichier de configuration dynamique à l’aide d’un fichier manifeste App-V 5,0

Vous pouvez créer le fichier de configuration dynamique à l’aide de l’une des trois méthodes suivantes: manuellement, à l’aide de la console de gestion App-V 5,0 ou du séquençage d’un package, qui est généré avec 2 exemples de fichiers.

Pour plus d’informations sur la création du fichier à l’aide de la console de gestion de l’application-V 5,0, voir [créer un fichier de configuration personnalisé à l’aide de la console de gestion App-v 5,0](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).

Pour créer le fichier manuellement, les informations ci-dessus dans les sections précédentes peuvent être combinées dans un seul fichier. Nous vous recommandons d’utiliser des fichiers générés par le Sequencer.






## Rubriques connexes


[Comment appliquer le fichier de configuration du déploiement à l'aide de PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

[Comment appliquer le fichier de configuration utilisateur à l'aide de PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell.md)

[Opérations d'App-V5.0](operations-for-app-v-50.md)

 

 





