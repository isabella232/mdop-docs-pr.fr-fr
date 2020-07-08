---
title: Gestion des modèles UE-V 2. x emplacements des paramètres à l’aide de Windows PowerShell et WMI
description: Gestion des modèles UE-V 2. x emplacements des paramètres à l’aide de Windows PowerShell et WMI
author: dansimp
ms.assetid: b5253050-acc3-4274-90d0-1fa4c480331d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9788ff1a11f1c70e52b75dd2187a198f5472f77f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804560"
---
# Gestion des modèles UE-V 2. x emplacements des paramètres à l’aide de Windows PowerShell et WMI


Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 et 2,1 SP1 utilisez les modèles d’emplacement des paramètres XML pour définir les paramètres de captures et d’application de la virtualisation. UE-V inclut un ensemble de modèles d’emplacement des paramètres standard. Il inclut également l’outil de génération UE-V qui vous permet de créer des modèles d’emplacement des paramètres personnalisés. Une fois que vous avez créé et déployé des modèles d’emplacement des paramètres, vous pouvez gérer ces modèles en utilisant Windows PowerShell et WMI (Windows Management Instrumentation). Pour obtenir la liste complète des cmdlets PowerShell d’UE-V, voir [référence sur l’applet de passe UE-v 2](https://go.microsoft.com/fwlink/p/?LinkId=393495) ( https://go.microsoft.com/fwlink/p/?LinkId=393495) .

## Gérer les modèles d’emplacement des paramètres UE-V 2 à l’aide de Windows PowerShell


Les fonctionnalités WMI et Windows PowerShell d’UE-V incluent la possibilité d’activer, de désactiver, de inscrire, de mettre à jour et de délivrer des modèles d’emplacement des paramètres. L’utilisation de ces fonctionnalités vous permet d’automatiser le processus d’inscription, de mise à jour ou de suppression de l’enregistrement de modèles auprès de l’agent UE-V. Vous pouvez également enregistrer des modèles manuellement à l’aide des commandes WMI et Windows PowerShell. L’utilisation de ces fonctionnalités conjointement à une solution de distribution de logiciels électronique, une stratégie de groupe ou un autre mode de déploiement automatisé, tel qu’un script, vous permet d’automatiser davantage ce processus.

Vous devez disposer des autorisations d’administrateur pour mettre à jour, inscrire ou annuler l’enregistrement d’un modèle d’emplacement des paramètres. Les autorisations d’administrateur ne sont pas requises pour activer, désactiver ou répertorier des modèles.

***<em>Pour gérer les modèles d’emplacement des paramètres à l’aide de Windows PowerShellell</em>***

1.  Utilisez un compte disposant de droits d’administrateur pour ouvrir une invite de commandes Windows PowerShell.

2.  Utilisez les applets de commande Windows PowerShell suivantes pour inscrire et gérer les modèles d’emplacement des paramètres UE-V.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Commande de Windows PowerShell</th>
    <th align="left">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate</code></p></td>
    <td align="left"><p>Répertorie tous les modèles d’emplacements des paramètres enregistrés sur l’ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate –Application &lt;string&gt;</code></p></td>
    <td align="left"><p>Répertorie tous les modèles d’emplacements des paramètres inscrits sur l’ordinateur où le nom de l’application ou du modèle contient des &lt; chaînes &gt; .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate –TemplateID &lt;string&gt;</code></p></td>
    <td align="left"><p>Répertorie tous les modèles d’emplacements des paramètres enregistrés sur l’ordinateur où l’ID du modèle contient des &lt; chaînes &gt; .</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate [-ApplicationOrTemplateID] &lt;string&gt;</code></p></td>
    <td align="left"><p>Répertorie tous les modèles d’emplacements des paramètres enregistrés sur l’ordinateur où le nom de l’application ou du modèle, ou l’ID du modèle contient des &lt; chaînes &gt; .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplateProgram [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Obtient le nom du programme et les informations de version qui dépendent de l’ID du modèle.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage</code></p></td>
    <td align="left"><p>Obtient la liste effective des applications Windows.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevAppXPackage -Computer</code></p></td>
    <td align="left"><p>Obtient la liste des applications Windows configurées pour l’ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p>Obtient la liste des applications Windows configurées pour l’utilisateur actuel.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Register-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Inscrit un modèle d’emplacement des paramètres avec UE-V en utilisant des chemins d’accès relatifs et/ou des caractères génériques dans les chemins d’accès aux fichiers. Après l’inscription d’un modèle, UE-V synchronise les paramètres définis dans le modèle entre les ordinateurs sur lesquels le modèle est enregistré.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Register-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Enregistre un ou plusieurs modèles d’emplacement des paramètres avec UE-V en utilisant des chemins littéraux, où aucun caractère ne peut être interprété comme des caractères génériques. Après l’inscription d’un modèle, UE-V synchronise les paramètres définis dans le modèle entre les ordinateurs sur lesquels le modèle est enregistré.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Unregister-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Annule l’inscription d’un modèle d’emplacement des paramètres avec UE-V. Lorsqu’un modèle est non enregistré, UE-V ne synchronise plus les paramètres définis dans le modèle entre les ordinateurs.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Unregister-UevTemplate -All</code></p></td>
    <td align="left"><p>Annule l’inscription de tous les modèles d’emplacement des paramètres avec UE-V. Lorsqu’un modèle est non enregistré, UE-V ne synchronise plus les paramètres définis dans le modèle entre les ordinateurs.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Update-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Met à jour un ou plusieurs modèles d’emplacement des paramètres avec une version plus récente du modèle. Utilisez des chemins d’accès relatifs et/ou des caractères génériques dans les chemins d’accès aux fichiers. Le nouveau modèle doit être une version plus récente que le modèle existant.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Update-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Met à jour un ou plusieurs modèles d’emplacement des paramètres avec une version plus récente du modèle. Utilisez les chemins d’accès complets aux fichiers de modèles dans lesquels aucun caractère ne peut être interprété en tant que caractères génériques. Le nouveau modèle doit être une version plus récente que le modèle existant.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Suppression d’une ou plusieurs applications Windows de la liste des applications Windows sur ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p>Supprime l’application Windows de la liste des applications Windows actuelles de l’utilisateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer -All</code></p></td>
    <td align="left"><p>Supprime toutes les applications Windows de la liste des applications Windows sur ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Suppression d’une ou plusieurs applications Windows de la liste des applications Windows actuelles de l’utilisateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] -All</code></p></td>
    <td align="left"><p>Supprime toutes les applications Windows de la liste des applications Windows actuelles de l’utilisateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Désactive un modèle d’emplacement des paramètres pour l’utilisateur actuel de l’ordinateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Disable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Désactive une ou plusieurs applications Windows dans la liste des applications Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Désactive une ou plusieurs applications Windows dans la liste des applications Windows actuelles de l’utilisateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Active un modèle d’emplacement des paramètres pour l’utilisateur actuel de l’ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Enable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Active une ou plusieurs applications Windows dans la liste des applications Windows sur ordinateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p>Active une ou plusieurs applications Windows dans la liste des applications Windows actuelles de l’utilisateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Test-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Détermine s’il s’agit d’un ou de plusieurs modèles d’emplacement des paramètres qui sont conformes au schéma XML. Peuvent utiliser des chemins d’accès relatifs et des caractères génériques.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Test-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p>Détermine s’il s’agit d’un ou de plusieurs modèles d’emplacement des paramètres qui sont conformes au schéma XML. Le chemin d’accès doit être un chemin d’accès complet au fichier de modèle, mais n’inclut pas de caractères génériques.</p></td>
    </tr>
    </tbody>
    </table>



Les fonctionnalités Windows PowerShell d’UE-V vous permettent de gérer un ensemble de modèles de paramètres déployés dans votre entreprise. Utilisez la procédure suivante pour gérer un groupe de modèles à l’aide de Windows PowerShell.

**Pour gérer un groupe de modèles d’emplacement des paramètres à l’aide de Windows PowerShell**

1.  Modifiez ou mettez à jour les modèles d’emplacement des paramètres souhaités.

2.  Si vous voulez modifier ou mettre à jour les modèles d’emplacement des paramètres, déployez ces modèles d’emplacement des paramètres dans un dossier accessible à partir de l’ordinateur local.

3.  Sur l’ordinateur local, ouvrez une fenêtre Windows PowerShell avec des droits d’administrateur.

4.  Annulez l’enregistrement de toutes les versions inscrites des modèles en entrant la commande suivante.

    ``` syntax
    Unregister-UevTemplate -All
    ```

    Cette commande supprime tous les modèles actifs de l’ordinateur.

5.  Enregistrez les modèles mis à jour en entrant la commande suivante.

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    Cette commande enregistre tous les modèles d’emplacement des paramètres situés dans le dossier de modèle spécifié.

### <a href="" id="win8applist"></a>Liste des applications Windows

En répertoriant une application Windows dans la liste des applications Windows, vous spécifiez si l’application est activée ou désactivée pour la synchronisation des paramètres. Les applications sont identifiées dans la liste par leur nom de famille de packages et si la synchronisation des paramètres doit être activée ou désactivée pour cette application. Lorsque vous utilisez ces paramètres avec le paramètre de comportement de synchronisation par défaut non répertorié, vous pouvez contrôler si les applications Windows sont synchronisées.

Pour afficher le nom de la famille de packages des applications Windows installées, à l’invite de commandes Windows PowerShell, entrez:

``` syntax
Get-AppxPackage | Sort-Object PackageFamilyName | Format-Table PackageFamilyName
```

Pour afficher une liste des applications Windows qui peuvent synchroniser les paramètres sur un ordinateur dont le nom de la famille de packages, le statut activée et la source activée, à l’invite de commandes Windows PowerShell, entrez: `Get-UevAppxPackage`

**Définitions des propriétés Get-UevAppxPackage**

<a href="" id="displayname"></a>**DisplayName**  
Nom affiché à l’utilisateur dans l’application Centre de paramètres de la société. La `DisplayName` propriété est dérivée de la `PackageFamilyName` propriété.

<a href="" id="packagefamilyname"></a>**Propriété packagefamilyname**  
Nom du package installé pour l’utilisateur actuel.

<a href="" id="enabled"></a>**Activé**  
Définit si les paramètres de l’application sont configurés pour la synchronisation.

<a href="" id="enabledsource"></a>**EnabledSource**  
L’emplacement où la configuration qui active ou désactive l’application est définie. Les valeurs possibles sont: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*et *PolicyUser*.

<a href="" id="notset"></a>**NotSet**  
La stratégie n’est pas configurée pour synchroniser cette application.

<a href="" id="localmachine"></a>**LocalMachine**  
L’État Enabled est défini dans la section ordinateur local du Registre.

<a href="" id="localuser"></a>**LocalUser**  
L’État Enabled est défini dans la section Current User du Registre.

<a href="" id="policymachine"></a>**PolicyMachine**  
L’État Enabled est défini dans la section Stratégie de la section ordinateur local du Registre.

Pour obtenir la liste des applications Windows configurées par l’utilisateur, à l’invite de commandes Windows PowerShell, entrez: `Get-UevAppxPackage –CurrentComputerUser`

Pour obtenir la liste des applications Windows configurée par l’ordinateur, à l’invite de commandes Windows PowerShell, entrez: `Get-UevAppxPackage –Computer`

Pour l’un ou l’autre paramètre, CurrentComputerUser ou ordinateur, l’applet de passe renvoie une liste des applications Windows qui sont configurées au niveau de l’ordinateur ou de l’ordinateur.

**Définitions des propriétés**

<a href="" id="displayname"></a>**DisplayName**  
Nom affiché à l’utilisateur dans l’application Centre de paramètres de la société. La `DisplayName` propriété est dérivée de la `PackageFamilyName` propriété.

<a href="" id="packagefamilyname"></a>**Propriété packagefamilyname**  
Nom du package installé pour l’utilisateur actuel.

<a href="" id="enabled"></a>**Activé**  
Définit si les paramètres de l’application sont configurés pour se synchroniser pour le commutateur spécifié ( **utilisateur** ou **ordinateur**).

<a href="" id="installed"></a>**Installé**  
True si l’application est installée sur le propriété packagefamilyname de l’utilisateur actuel.

### Gérer les modèles d’emplacement des paramètres UE-V 2 à l’aide de WMI

La virtualisation de l’interface utilisateur fournit l’ensemble des commandes WMI suivantes. Les administrateurs peuvent utiliser ces interfaces pour gérer les modèles d’emplacement des paramètres à partir de Windows PowerShell et automatiser les tâches d’administration des modèles.

**Pour gérer les modèles d’emplacement des paramètres à l’aide de WMI**

1.  Utilisez un compte disposant de droits d’administrateur pour ouvrir une fenêtre Windows PowerShell.

2.  Utilisez les commandes WMI suivantes pour inscrire et gérer les modèles d’emplacement des paramètres UE-V.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>                         Windows PowerShell command</code></th>
    <th align="left">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</code></p></td>
    <td align="left"><p>Répertorie tous les modèles d’emplacements des paramètres inscrits pour l’ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod –Namespace root\Microsoft\UEV –Class SettingsLocationTemplate –Name GetProcessInfoByTemplateId &lt;template Id&gt;</code></p></td>
    <td align="left"><p>Obtient le nom du programme et les informations de version qui dépendent du nom du modèle.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV EffectiveWindows8App</code></p></td>
    <td align="left"><p>Obtient la liste effective des applications Windows.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-WmiObject-namespace root\Microsoft\UEV MachineConfiguredWindows8App</p></td>
    <td align="left"><p>Obtient la liste des applications Windows configurées pour l’ordinateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguredWindows8App</code></p></td>
    <td align="left"><p>Obtient la liste des applications Windows configurées pour l’utilisateur actuel.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</code></p></td>
    <td align="left"><p>Inscrit un modèle d’emplacement des paramètres avec UE-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Annule l’inscription d’un modèle d’emplacement des paramètres avec UE-V. Dès qu’aucun modèle n’est enregistré, UE-V ne synchronise plus les paramètres définis dans le modèle entre les ordinateurs.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p>Met à jour un modèle d’emplacement des paramètres avec UE-V. Le nouveau modèle doit être une version plus récente que celle existante.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Suppression d’une ou plusieurs applications Windows de la liste des applications Windows sur ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Suppression d’une ou plusieurs applications Windows de la liste des applications Windows actuelles de l’utilisateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Désactive un ou plusieurs modèles d’emplacement des paramètres avec UE-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Désactive une ou plusieurs applications Windows dans la liste des applications Windows.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Désactive une ou plusieurs applications Windows dans la liste des applications Windows actuelles de l’utilisateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p>Active un modèle d’emplacement des paramètres avec UE-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Active les applications Windows dans la liste des applications Windows sur ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p>Active les applications Windows dans la liste des applications Windows actuelles de l’utilisateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p>Détermine si un modèle d’emplacement des paramètres donné est conforme à son schéma XML.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
Where a list of Package Family Names is called by the WMI command, the list must be in quotes and separated by a pipe symbol, for example, `"<package family name | package family name>"`.
~~~



### Déploiement de l’agent UE-V à l’aide de Windows PowerShell

**Déploiement d’UE-V agent à l’aide de Windows PowerShell**

1.  Copiez le package d’installation de l’agent UE-V dans un partage réseau accessible.

    **Remarque**  
    Utilisez AgentSetup.exe pour déployer à la fois les versions 32 bits et 64 bits de l’agent UE-V. Les packages Windows Installer, AgentSetupx86.msi et AgentSetupx64.msi, sont disponibles pour chaque architecture. Pour désinstaller l’agent UE-V ultérieurement à l’aide du fichier d’installation, vous devez utiliser le même type de fichier.



2.  Utilisez l’une des commandes Windows PowerShell suivantes pour installer l’agent UE-V.

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

Vous **avez une suggestion pour UE-V**? Ajoutez ou Votez en fonction [de suggestions.](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization) Vous **avez un problème UE-V**? Utiliser le [Forum de TechNet UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Rubriques connexes


[Administration d’UE-V 2. x avec Windows PowerShell et WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Administration d’UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









