---
title: À propos de la configuration dynamique App-V 5,1
description: Vous pouvez utiliser la configuration dynamique pour personnaliser un package App-V 5,1 pour un utilisateur. Utilisez les informations suivantes pour créer ou modifier un fichier de configuration dynamique existant.
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/28/2018
ms.author: dansimp
ms.openlocfilehash: ec8a25da6e139ac329810b1e04f7097cadaa6ab4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806117"
---
# À propos de la configuration dynamique App-V 5,1 
Avec la configuration dynamique, vous pouvez modifier le fichier de configuration dynamique pour personnaliser l’exécution d’un package App-V 5,1 pour un utilisateur ou un groupe. La personnalisation de package supprime le besoin de reséquencer les packages à l’aide des paramètres souhaités.  Il permet également de rester indépendant du contenu du package et des paramètres personnalisés.

Les packages d’application virtuels contiennent un manifeste qui fournit toutes les informations fondamentales pour le package. Ces informations incluent les valeurs par défaut des paramètres du package et déterminent les paramètres du formulaire le plus basique (sans personnalisation supplémentaire). 

Lors de la création d’un package, le Sequencer génère automatiquement des fichiers de déploiement et de configuration de l’utilisateur à l’aide des données de manifeste du package. Par conséquent, ces fichiers générés reflètent les paramètres par défaut configurés lors du séquençage. Si vous appliquez ces fichiers à un package dans le formulaire généré par le Sequencer, les packages présentent les mêmes paramètres par défaut que le manifeste. 

Utilisez ces fichiers générés pour apporter des modifications, le cas échéant, qui ne modifie pas directement le package. Si vous souhaitez ajouter, supprimer ou mettre à jour les fichiers de configuration, apportez les modifications souhaitées sur les valeurs par défaut dans les informations du manifeste.

>[!TIP]
>L’ordre dans lequel les fichiers sont lus est le suivant:<ul><li>UserConfig.xml</li><li>DeploymentConfig.xml</li><li>Manifeste</li></ul><p>La première entrée représente ce qui lit en dernier. Par conséquent, son contenu est prioritaire, et tous les packages contiennent fondamentalement et fournissent des paramètres par défaut à partir du manifeste du package.<ol><li> Si vous personnalisez le fichier DeploymentConfig.xml et appliquez les paramètres personnalisés, les paramètres par défaut dans le manifeste du package sont remplacés. </li><li> S’il s’agit de la personnalisation de l' UserConfig.xml et de l’application des paramètres personnalisés, les paramètres par défaut pour la configuration de déploiement et le manifeste du package sont remplacés. </li></ol>

## Contenu du fichier de configuration utilisateur (UserConfig.xml)
Le fichier UserConfig fournit des paramètres de configuration qui s’appliquent à un utilisateur spécifique lors du déploiement du package sur un ordinateur exécutant le client App-V 5,1.  Ces paramètres n’affectent aucun autre utilisateur sur le client.

Utilisez le fichier UserConfig pour spécifier ou modifier des paramètres personnalisés pour un package:

-   Extensions intégrées au système natif par utilisateur: raccourcis, associations de types de fichiers, protocoles d’URL, AppPaths, clients logiciels et COM
-   Sous-systèmes virtuels: objets d’application, variables d’environnement, modifications du Registre, services et polices
-   Scripts (contexte utilisateur uniquement)
-   Autorité de gestion (pour contrôler la co-existence d’un package avec App-V 4,6)

### En-tête

L’en-tête d’un fichier de configuration utilisateur dynamique se présente comme suit:

```xml
<?xml version="1.0" encoding="utf-8"?><UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">
```

**PackageId** est de la même valeur qu’existe dans le fichier manifeste.


### Body

Le corps du fichier de configuration utilisateur dynamique peut inclure tous les points d’extension d’application définis dans le fichier manifeste, ainsi que les informations de configuration des applications virtuelles. Quatre sous-sections sont autorisées dans le corps de texte:

1.  **[Applications](#applications)** 
2.  **[Sous-systèmes](#subsystems)**
3.  **[UserScripts](#userscripts)**
4.  **[ManagingAuthority](#managingauthority)**

#### Applications

Toutes les extensions d’application contenues dans le fichier manifeste au sein d’un package ont un ID d’application attribué, que vous trouverez dans le fichier manifeste. L’ID d’application vous permet d’activer ou de désactiver toutes les extensions pour une application donnée au sein d’un package. L’ID de l’application doit exister dans le fichier manifeste ou n’est pas pris en compte.

```XML
<UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved"  xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">

<Applications>

<!--No new application can be defined in policy. AppV Client will ignore any application ID that is not also in the Manifest file-->

<Application Id="{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled="false">

</Application>

</Applications>

..

</UserConfiguration>
```

#### Sous-systèmes

Nouvel appextensions et autres sous-systèmes organisés en tant que sous-nœuds.

```XML
<UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">

<Subsystems>

..

</Subsystems>

..

</UserConfiguration>
```

Vous pouvez activer ou désactiver chaque sous-système à l’aide de l’attribut **Enabled** .

**Extensions** 

Quelques extensions de contrôle de sous-systèmes (sous-systèmes d’extension). Ces sous-systèmes sont des raccourcis, des associations de types de fichiers, des protocoles d’URL, des AppPaths, des clients logiciels et des COM.

Les sous-systèmes d’extension peuvent être activés ou désactivés indépendamment du contenu. Par exemple, si vous activez l’option raccourcis, le client utilise par défaut les raccourcis contenus dans le manifeste. Chaque sous-système d’extension peut contenir un \<Extensions\> nœud. Si cet élément enfant est présent, le client ignore le contenu du fichier manifeste du sous-système et n’utilise que le contenu du fichier de configuration. 

_**Exemples:**_ 

- Si vous définissez cette valeur dans le fichier de configuration de l’utilisateur ou du déploiement, le contenu du manifeste est ignoré.

  ```XML

  <Shortcuts  Enabled="true"\>

  <Extensions>

  ...

  </Extensions>

  </Shortcuts>
  ```
- Si vous définissez uniquement ce qui suit, le contenu du manifeste est intégré lors de la publication.

  ```XML

  <Shortcuts  Enabled="true"/>
  ```

- Si vous définissez ce qui suit, tous les raccourcis du manifeste sont toujours ignorés. En d’autres termes, aucun raccourci n’est intégré.

  ```XML

  <Shortcuts  Enabled="true">

     <Extensions/>

  </Shortcuts>
  ```

_**Sous-systèmes d’extension pris en charge:**_ 

Le sous-système d’extension **raccourcis** détermine quels raccourcis sont intégrés dans le système local.  

```XML

<Subsystems>

<Shortcuts Enabled="true">

  <Extensions>

    <Extension Category="AppV.Shortcut">

      <Shortcut>

        <File>[{Common Programs}]\Microsoft Contoso\Microsoft ContosoApp Filler 2010.lnk</File>

        <Target>[{PackageRoot}]\Contoso\ContosoApp.EXE</Target>


      <Icon>[{Windows}]\Installer\{90140000-0011-0000-0000-0000000FF1CE}\inficon.exe</Icon>

        <Arguments />

        <WorkingDirectory />

        <AppUserModelId>ContosoApp.Filler.3</AppUserModelId>

        <Description>Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.</Description>

        <Hotkey>0</Hotkey>

        <ShowCommand>1</ShowCommand>

      <ApplicationId>[{PackageRoot}]\Contoso\ContosoApp.EXE</ApplicationId>

      </Shortcut>

  </Extension>

  <Extension Category="AppV.Shortcut">

    <Shortcut>

    <File>[{AppData}]\Microsoft\Contoso\Recent\Templates.LNK</File>

      <Target>[{AppData}]\Microsoft\Templates</Target>

      <Icon />

      <Arguments />

      <WorkingDirectory />

      <AppUserModelId />

      <Description />

      <Hotkey>0</Hotkey>

      <ShowCommand>1</ShowCommand>

      <!-- Note the ApplicationId is optional -->

    </Shortcut>

  </Extension>

 </Extensions>

</Shortcuts>
```

Le sous-système d’extension associée aux types de **fichiers** associe des types de fichiers à des programmes pour qu’ils s’ouvrent par défaut ainsi que dans le menu contextuel. 

>[!TIP]
>Vous pouvez configurer le sous-système avec des types MIME.

```XML

<FileTypeAssociations Enabled="true">

<Extensions>

  <Extension Category="AppV.FileTypeAssociation">

    <FileTypeAssociation>

      <FileExtension MimeAssociation="true">

      <Name>.docm</Name>

      <ProgId>contosowordpad.DocumentMacroEnabled.12</ProgId>

      <PerceivedType>document</PerceivedType>

    <ContentType>application/vnd.ms-contosowordpad.document.macroEnabled.12</ContentType>

      <OpenWithList>

        <ApplicationName>wincontosowordpad.exe</ApplicationName>

      </OpenWithList>

     <OpenWithProgIds>

        <ProgId>contosowordpad.8</ProgId>

      </OpenWithProgIds>

      <ShellNew>

        <Command />

        <DataBinary />

        <DataText />

        <FileName />

        <NullFile>true</NullFile>

        <ItemName />

        <IconPath />

        <MenuText />

        <Handler />

      </ShellNew>

    </FileExtension>

    <ProgId>

       <Name>contosowordpad.DocumentMacroEnabled.12</Name>

      <DefaultIcon\>[{Windows}]\Installer\{90140000-0011-0000-0000-000000FF1CE}\contosowordpadicon.exe,15</DefaultIcon>

        <Description>Blah Blah Blah</Description>

        <FriendlyTypeName>[{FOLDERID_ProgramFilesX86}]\Microsoft Contoso 14\res.dll,9182</FriendlyTypeName>

        <InfoTip>[{FOLDERID_ProgramFilesX86}]\Microsoft Contoso 14\res.dll,1424</InfoTip>

        <EditFlags>0</EditFlags>

        <ShellCommands>

          <DefaultCommand>Open</DefaultCommand>

          <ShellCommand>

           <ApplicationId>{e56fa627-c35f-4a01-9e79-7d36aed8225a}</ApplicationId>

             <Name>Edit</Name>

             <FriendlyName>&Edit</FriendlyName>

           <CommandLine>"[{PackageRoot}]\Contoso\WINcontosowordpad.EXE" /vu "%1"</CommandLine>

          </ShellCommand>

          </ShellCommand>

          <ApplicationId>{e56fa627-c35f-4a01-9e79-7d36aed8225a}</ApplicationId>

            <Name>Open</Name>

            <FriendlyName>&Open</FriendlyName>

            <CommandLine>"[{PackageRoot}]\Contoso\WINcontosowordpad.EXE" /n "%1"</CommandLine>

            <DropTargetClassId />

            <DdeExec>

              <Application>mscontosowordpad</Application>

              <Topic>ShellSystem</Topic>

              <IfExec>[SHELLNOOP]</IfExec>

              <DdeCommand>[SetForeground][ShellNewDatabase"%1"]</DdeCommand>

            </DdeExec>

          </ShellCommand>

        </ShellCommands>

      </ProgId>

     </FileTypeAssociation>

   </Extension>

  </Extensions>

  </FileTypeAssociations>
```

Le sous-système d’extension des **protocoles d’URL** contrôle les protocoles d’URL intégrés au registre local de l’ordinateur client, par exemple, _mailto:_. 

```XML

<URLProtocols Enabled="true">

<Extensions>

<Extension Category="AppV.URLProtocol">

<URLProtocol>

  <Name>mailto</Name>

  <ApplicationURLProtocol>

  <DefaultIcon>[{ProgramFilesX86}]\MicrosoftContoso\Contoso\contosomail.EXE,-9403</DefaultIcon>

  <EditFlags>2</EditFlags>

  <Description />

  <AppUserModelId />

  <FriendlyTypeName />

  <InfoTip />

<SourceFilter />

  <ShellFolder />

  <WebNavigableCLSID />

  <ExplorerFlags>2</ExplorerFlags>

  <CLSID />

  <ShellCommands>

  <DefaultCommand>open</DefaultCommand>

  <ShellCommand>

  <ApplicationId>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationId>

  <Name>open</Name>

  <CommandLine>[{ProgramFilesX86}\Microsoft Contoso\Contoso\contosomail.EXE" -c OEP.Note /m "%1"</CommandLine>

  <DropTargetClassId />

  <FriendlyName />

  <Extended>0</Extended>

  <LegacyDisable>0</LegacyDisable>

  <SuppressionPolicy>2</SuppressionPolicy>

   <DdeExec>

  <NoActivateHandler />

  <Application>contosomail</Application>

  <Topic>ShellSystem</Topic>

  <IfExec>[SHELLNOOP]</IfExec>

  <DdeCommand>[SetForeground][ShellNewDatabase "%1"]</DdeCommand>

  </DdeExec>

  </ShellCommand>

  </ShellCommands>

  </ApplicationURLProtocol>

  </URLProtocol>

  </Extension>

  </Extension>

  </URLProtocols>
```

Le sous-système d’extension des **clients logiciels** permet à l’application de s’inscrire en tant que client de messagerie, lecteur de News, lecteur multimédia et rend l’application visible dans l’interface utilisateur définir l’accès au programme et aux paramètres par défaut de l’ordinateur. Dans la plupart des cas, vous ne devez l’activer et la désactiver. Il existe également un contrôle permettant d’activer et de désactiver le client de messagerie de manière spécifique si vous souhaitez que les autres clients restent activés, à l’exception de ce client.

```XML

<SoftwareClients Enabled="true">

  <ClientConfiguration EmailEnabled="false" />

</SoftwareClients>
```

Le sous-système d’extension **AppPaths** ouvre les applications inscrites dans le chemin d’une application. Par exemple, si contoso.exe a un nom appPath de _MonApp_, les utilisateurs peuvent taper _MonApp_ dans le menu exécuter, en ouvrant contoso.exe.

```XML

<AppPaths Enabled="true">

<Extensions>

<Extension Category="AppV.AppPath">

<AppPath>

  <ApplicationId>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationId>

  <Name>contosomail.exe</Name>

  <ApplicationPath>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationPath>

  <PATHEnvironmentVariablePrefix />

  <CanAcceptUrl>false</CanAcceptUrl>

  <SaveUrl />

</AppPath>

</Extension>

</Extensions>

</AppPaths>
```

Le sous-système d’extensions **com** permet à une application d’être inscrite aux serveurs com locaux. Le mode peut être:

-   Avec
-   Identifié 
-   Désactivé

```XML

<COM Mode="Isolated"/>
```

**Objets de noyau virtuel**

```XML

<Objects Enabled="false" />
```

Le **Registre virtuel** définit un registre dans le registre virtuel dans HKCU.

```XML

<Registry Enabled="true">

<Include>

<Key Path="\REGISTRY\USER\[{AppVCurrentUserSID}]\Software\ABC">

<Value Type="REG_SZ" Name="Bar" Data="NewValue" />

 </Key>

  <Key Path="\REGISTRY\USER\[{AppVCurrentUserSID}]\Software\EmptyKey" />

 </Include>

<Delete>

</Registry>
```

**Système de fichiers virtuel**

```XML

    <FileSystem Enabled="true" />
```

**Polices virtuelles**

```XML

      <Fonts Enabled="false" />
```

**Variables d’environnement virtuel**

```XML

<EnvironmentVariables Enabled="true">

<Include>

       <Variable Name="UserPath" Value="%path%;%UserProfile%" />

       <Variable Name="UserLib" Value="%UserProfile%\ABC" />

       </Include>

      <Delete>

       <Variable Name="lib" />

        </Delete>

        </EnvironmentVariables>
```

**Services virtuels**

```XML

      <Services Enabled="false" />
```

#### UserScripts

Utilisez UserScripts pour configurer ou modifier l’environnement virtuel.  Vous pouvez également exécuter des scripts au moment du déploiement ou pour nettoyer l’environnement une fois l’application arrêtée. Pour voir un exemple de script, reportez-vous au fichier de configuration utilisateur généré par le Sequencer. La section scripts ci-dessous fournit des informations supplémentaires sur les différents déclencheurs qui peuvent être utilisés.

#### ManagingAuthority

Utilisez ManagingAuthority lorsque deux versions de votre package sont co-exister sur le même ordinateur, l’une ayant été déployée vers App-V 4,6 et une autre déployée sur App-V 5,0. Pour permettre à App-V vNext de prendre en charge les points d’extension 4,6 App-V pour le package nommé, entrez ce qui suit dans le fichier UserConfig (où PackageName est le GUID du package dans App-V 4,6:

```XML

<ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName="032630c0-b8e2-417c-acef-76fc5297fe81" />
```

## Fichier de configuration de déploiement (DeploymentConfig.xml)

Le fichier DeploymentConfig fournit des paramètres de configuration pour le contexte de l’ordinateur et le contexte de l’utilisateur, en fournissant les mêmes fonctionnalités que celles indiquées dans le fichier UserConfig. Le paramètre est appliqué lors du déploiement du package sur un ordinateur exécutant le client App-V 5,1.

Utilisez le fichier DeploymentConfig pour spécifier ou modifier des paramètres personnalisés pour un package:

- Tous les paramètres de UserConfig
- Extensions qui ne peuvent être appliquées globalement que par tous les utilisateurs
- Sous-systèmes virtuels pour emplacements d’ordinateur globaux (par exemple, registre)
- URL de la source de produit
- Scripts (contexte de l’ordinateur uniquement)
- Contrôles pour arrêter les processus enfants

### En-tête

L’en-tête d’un fichier de configuration de déploiement dynamique ressemble à ceci:

```XML
<?xml version="1.0" encoding="utf-8"?><DeploymentConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/deploymentconfiguration">
```

**PackageId** est de la même valeur qu’existe dans le fichier manifeste.

### Body

Le corps du fichier de configuration de déploiement dynamique comprend deux sections:

- **UserConfiguration:** permet d’autoriser le même contenu que le fichier de configuration utilisateur décrit dans la section précédente.  Lors de la publication du package pour un utilisateur, tous les paramètres de configuration nouvel appextensions de cette section remplacent les paramètres correspondants dans le manifeste au sein du package, sauf si vous fournissez un fichier de configuration utilisateur. Si vous fournissez également un fichier UserConfig, il est utilisé à la place des paramètres utilisateur dans le fichier de configuration de déploiement. Si vous publiez le package globalement, seul le contenu du fichier de configuration de déploiement s’utilisera en association avec le manifeste. Pour plus d’informations, consultez la section [contenu du fichier de configuration utilisateur (UserConfig.xml)](#user-configuration-file-contents-userconfigxml).

- **MachineConfiguration:** contient des informations qui peuvent être configurées uniquement pour la totalité d’un ordinateur, et non pour un utilisateur spécifique de l’ordinateur. Par exemple, HKEY_LOCAL_MACHINE clés de Registre dans le VFS.

```XML

<DeploymentConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/deploymentconfiguration">

<UserConfiguration>

...

</UserConfiguration>

<MachineConfiguration>

...

</MachineConfiguration>

...

</MachineConfiguration>

</DeploymentConfiguration>
```

### UserConfiguration

Pour plus d’informations sur les paramètres fournis pour cette section, voir le [contenu du fichier de configuration utilisateur (UserConfig.xml)](#user-configuration-file-contents-userconfigxml) . 

### MachineConfiguration

Utilisez la section MachineConfiguration pour configurer des informations pour l’intégralité d’un ordinateur; pas pour un utilisateur spécifique de l’ordinateur. Par exemple, HKEY_LOCAL_MACHINE clés de Registre du Registre virtuel. Quatre sous-sections sont autorisées dans cet élément:

1.  **[Sous-systèmes](#subsystems-1)**
2.  **[ProductSourceURLOptOut](#productsourceurloptout)**
3.  **[MachineScripts](#machinescripts)**
4.  **[TerminateChildProcess](#terminatechildprocess)**

#### Sous-systèmes

Nouvel appextensions et autres sous-systèmes organisés en tant que sous-nœuds.

```XML

<MachineConfiguration>

  <Subsystems>

  …

  </Subsystems>

…

</MachineConfiguration>
```

Vous pouvez activer ou désactiver chaque sous-système à l’aide de l’attribut **Enabled** .

**Extensions** 

Quelques extensions de contrôle de sous-systèmes (sous-systèmes d’extension). Le sous-système est une fonctionnalité d’application utilisée par les programmes par défaut. Pour ce type d’extension, le package doit être publié globalement pour intégration dans le système local. Les mêmes règles relatives aux contrôles et aux paramètres qui s’appliquent aux extensions dans la configuration utilisateur s’appliquent également à celles de la section MachineConfiguration.

**Fonctionnalités d’application**: utilisé par les programmes par défaut qui permettent à une application de s’enregistrer comme suit:

- Capable d’ouvrir des extensions de fichier spécifiques
- Une offre pour le menu Démarrer-emplacement du navigateur Internet
- Capable d’ouvrir des types MIME Windows spécifiques

Par ailleurs, cette extension rend l’application virtuelle visible dans l’interface utilisateur définir les programmes par défaut.

```XML

<ApplicationCapabilities Enabled="true">

  <Extensions>

   <Extension Category="AppV.ApplicationCapabilities">

    <ApplicationCapabilities>


   <ApplicationId>[{PackageRoot}]\LitView\LitViewBrowser.exe</ApplicationId>

     <Reference>

      <Name>LitView Browser</Name>

      <Path>SOFTWARE\LitView\Browser\Capabilities</Path>

     </Reference>

   <CapabilityGroup>

    <Capabilities>


   <Name>@[{ProgramFilesX86}]\LitView\LitViewBrowser.exe,-12345</Name>


   <Description>@[{ProgramFilesX86}]\LitView\LitViewBrowser.exe,-12346</Description>

     <Hidden>0</Hidden>

     <EMailSoftwareClient>Lit View E-Mail Client</EMailSoftwareClient>

     <FileAssociationList>

      <FileAssociation Extension=".htm" ProgID="LitViewHTML" />

      <FileAssociation Extension=".html" ProgID="LitViewHTML" />

      <FileAssociation Extension=".shtml" ProgID="LitViewHTML" />

     </FileAssociationList>

     <MIMEAssociationList>

      <MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" />

      <MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" />

     </MIMEAssociationList>

    <URLAssociationList>

      <URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" />

     </URLAssociationList>

     </Capabilities>

  </CapabilityGroup>

   </ApplicationCapabilities>

  </Extension>

</Extensions>

</ApplicationCapabilities>
```

_**Sous-systèmes d’extension pris en charge:**_ 

Le sous-système d’extension **du Registre virtuel** de l’ordinateur de l’entreprise définit une clé de Registre dans le registre virtuel dans HKEY_LOCAL_MACHINE.

```XML

<Registry>

<Include>

  <Key Path="\REGISTRY\\Machine\Software\ABC">

    <Value Type="REG_SZ" Name="Bar" Data="Baz" />

   </Key>

  <Key Path="\REGISTRY\Machine\Software\EmptyKey" />

 </Include>

<Delete>

</Registry>
```

**Objets de noyau virtuel de l’ordinateur**

```XML

<Objects>

<NotIsolate>

   <Object Name="testObject" />

 </NotIsolate>

</Objects>
```

#### ProductSourceURLOptOut

Utilisez ProductSourceURLOptOut pour indiquer que l’URL du package peut être modifiée globalement via _PackageSourceRoot_ (pour prendre en charge les scénarios de succursales). Les modifications sont prises en compte lors du prochain lancement. 

```XML

<MachineConfiguration>

  ... 

  <ProductSourceURLOptOut Enabled="true" />

  ...

</MachineConfiguration>
```

#### MachineScripts

Le package peut être configuré pour exécuter des scripts au moment du déploiement, de la publication ou de la suppression. Pour voir un exemple de script, reportez-vous au fichier de configuration de déploiement généré par le Sequencer. 

La section scripts ci-dessous fournit des informations supplémentaires sur les différents déclencheurs qui peuvent être utilisés.

#### TerminateChildProcess

Le processus exécutable de l’application peut être spécifié, dont le processus enfant est arrêté au moment où le processus exe de l’application s’arrête.

```XML

<MachineConfiguration>

  ...   

  <TerminateChildProcesses>

    <Application Path="[{PackageRoot}]\Contoso\ContosoApp.EXE" />

    <Application Path="[{PackageRoot}]\LitView\LitViewBrowser.exe" />

    <Application Path="[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE" />

  </TerminateChildProcesses>

  ...

</MachineConfiguration>
```



## Scripts

Le tableau suivant décrit les différents événements de script et le contexte dans lequel ils peuvent être exécutés.

| Temps d’exécution du script       | Peuvent être spécifiées dans la configuration de déploiement | Peuvent être spécifiés dans la configuration de l’utilisateur | Peut s’exécuter dans l’environnement virtuel du package | Peut être exécuté dans le contexte d’une application spécifique. | S’exécute dans le contexte système/utilisateur (configuration du déploiement, configuration de l’utilisateur). |
|-----------------------------|----------------------------------------------|----------------------------------------|---------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------|
| AddPackage                  | X                                            |                                        |                                                   |                                                     | (SYSTÈME, NO/A)                                                               |
| PublishPackage              | X                                            | X                                      |                                                   |                                                     | (Système, utilisateur)                                                              |
| UnpublishPackage            | X                                            | X                                      |                                                   |                                                     | (Système, utilisateur)                                                              |
| RemovePackage               | X                                            |                                        |                                                   |                                                     | (SYSTÈME, NO/A)                                                               |
| StartProcess                | X                                            | X                                      | X                                                 | X                                                   | (Utilisateur, utilisateur)                                                                |
| ExitProcess                 | X                                            | X                                      |                                                   | X                                                   | (Utilisateur, utilisateur)                                                                |
| StartVirtualEnvironment     | X                                            | X                                      | X                                                 |                                                     | (Utilisateur, utilisateur)                                                                |
| TerminateVirtualEnvironment | X                                            | X                                      |                                                   |                                                     | (Utilisateur, utilisateur)                                                                |

### Utilisation de plusieurs scripts sur un seul déclencheur d’événements

App-V 5,1 prend en charge l’utilisation de plusieurs scripts sur un seul déclencheur d’événements pour les packages App-V, y compris les packages que vous convertissez de App-V 4,6 vers App-V 5,0 ou version ultérieure. Pour activer l’utilisation de plusieurs scripts, App-V 5,1 utilise une application de lancement de script, nommée ScriptRunner.exe, installée dans le cadre de l’installation du client App-V.

### Utiliser plusieurs scripts sur un seul déclencheur d’événements

Pour chaque script que vous souhaitez exécuter, transmettez ce script en tant qu’argument à l’application ScriptRunner.exe. L’application exécute ensuite chaque script séparément, ainsi que les arguments que vous spécifiez pour chaque script. Utilisez un seul script (ScriptRunner.exe) par déclencheur.

> [!NOTE]
> 
> Nous vous conseillons d’exécuter la ligne à plusieurs scripts à partir d’une invite de commandes pour vous assurer que tous les arguments sont construits correctement avant de les ajouter au fichier de configuration du déploiement.

### Exemples de descriptions de scripts et de paramètres

À l’aide de l’exemple de fichier et de tableau suivant, modifiez le fichier de déploiement ou de configuration utilisateur pour ajouter les scripts que vous souhaitez exécuter.

```XML
<MachineScripts>
 <AddPackage>
   <Path>ScriptRunner.exe</Path>
   <Arguments>
   -appvscript script1.exe arg1 arg2 –appvscriptrunnerparameters –wait –timeout=10
   -appvscript script2.vbs arg1 arg2
   -appvscript script3.bat arg1 arg2 –appvscriptrunnerparameters –wait –timeout=30 –rollbackonerror
   </Arguments>
   <Wait timeout=”40” RollbackOnError=”true”/>
 </AddPackage>
</MachineScripts>
```


**Dans l’exemple de fichier, les paramètres sont les suivants:**

#### \<AddPackage\>

Nom du déclencheur d’événements pour lequel vous exécutez un script, par exemple en ajoutant un package ou en publiant un package.

#### \<Path\>ScriptRunner.exe\</Path\>

Application de lancement de script installée dans le cadre de l’installation du client App-V.

> [!NOTE]
> 
> Même si ScriptRunner.exe est installé dans le cadre du client App-V, l’emplacement du client App-V doit être dans% path% ou ScriptRunner ne sera pas exécuté. ScriptRunner.exe se trouve généralement dans le Virtualizationfolder C:FilesApplication.

#### \<Arguments\>

`-appvscript` -Jeton qui représente le script réel que vous souhaitez exécuter.

`script1.exe` – Nom du script que vous souhaitez exécuter.

`arg1 arg2` -Arguments pour le script que vous souhaitez exécuter.

`-appvscriptrunnerparameters` -Jeton qui représente les options d’exécution pour script1.exe.

`-wait` -Jeton qui informe l’exécution de script1.exe pour qu’il se termine avant de passer au script suivant.

`-timeout=x` -Jeton qui informe ScriptRunner de sorte qu’il cesse d’exécuter le script actuel après un nombre x de secondes. Tous les autres scripts spécifiés s’exécutent toujours.

`-rollbackonerror` -Jeton qui informe ScriptRunner d’arrêter l’exécution de tous les scripts qui n’ont pas encore été exécutés et de restaurer une erreur sur le client App-V.

#### \<Wait timeout=”40” RollbackOnError=”true”/\>

Attend la fin globale d' ScriptRunner.exe.

Définissez la valeur du délai d’expiration du canal global de sorte qu’elle soit supérieure ou égale à la somme des valeurs de délai d’expiration des différents scripts.

Si un script individuel a signalé une erreur et rollbackonerror a la valeur true, ScriptRunner signalerait l’erreur à un client App-V.

ScriptRunner exécute tout script dont le type de fichier est associé à une application installée sur l’ordinateur. Si l’application associée est manquante ou si le type de fichier du script n’est pas associé à une application sur l’ordinateur, le script ne s’exécute pas.

### Créer un fichier de configuration dynamique à l’aide d’un fichier manifeste App-V 5,1

Vous pouvez créer le fichier de configuration dynamique en utilisant l’une des trois méthodes suivantes: manuellement, à l’aide de la console de gestion App-V 5,1 ou du séquençage d’un package, qui génère deux exemples de fichiers. Pour plus d’informations sur la création du fichier à l’aide de la console de gestion de l’application-V 5,1, voir [créer un fichier de configuration personnalisé à l’aide de la console de gestion App-v 5,1](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md).

Pour créer le fichier manuellement, les informations ci-dessus dans les sections précédentes peuvent être combinées dans un seul fichier. Nous vous recommandons d’utiliser des fichiers générés par le Sequencer.



- Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)
- Pour les problèmes liés à l’application V, utilisez le [Forum TechNet App-v](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes

- [Comment appliquer le fichier de configuration du déploiement à l'aide de PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)

- [Comment appliquer le fichier de configuration utilisateur à l'aide de PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell51.md)

- [Opérations d'App-V5.1](operations-for-app-v-51.md)

---
