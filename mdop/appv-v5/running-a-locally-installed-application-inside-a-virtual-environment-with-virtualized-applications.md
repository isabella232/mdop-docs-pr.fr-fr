---
title: Exécution d'une application installée localement à l'intérieur d'un environnement virtuel en cours d'exécution avec des applications virtualisées
description: Exécution d'une application installée localement à l'intérieur d'un environnement virtuel en cours d'exécution avec des applications virtualisées
author: dansimp
ms.assetid: a8affa46-f1f7-416c-8125-9595cfbfdbc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 10c0f3f3c8a1b88cf1a98fd64fe8f7f49b597a91
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804884"
---
# Exécution d'une application installée localement à l'intérieur d'un environnement virtuel en cours d'exécution avec des applications virtualisées


Vous pouvez exécuter une application installée localement dans un environnement virtuel, en plus des applications virtuelles à l’aide de Microsoft Application Virtualization (App-V). Vous pouvez le faire si vous:

-   Vous voulez installer et exécuter une application localement sur les ordinateurs clients, mais vous souhaitez virtualiser et exécuter des plug-ins spécifiques compatibles avec cette application locale.

-   Résolvez des problèmes liés à un package client App-V et voulez ouvrir une application locale dans l’environnement virtuel App-V.

Pour ouvrir une application locale à l’intérieur de l’environnement virtuel App-V, utilisez l’une des méthodes suivantes:

-   [Clé de Registre RunVirtual](#bkmk-runvirtual-regkey)

-   [Cmdlet PowerShell Get-AppvClientPackage](#bkmk-get-appvclientpackage-posh)

-   [Commutateur de ligne de commande/appvpid: &lt; PID&gt;](#bkmk-cl-switch-appvpid)

-   [Commutateur de raccordement de ligne de commande/appvve: &lt; GUID&gt;](#bkmk-cl-hook-switch-appvve)

Chaque méthode effectue essentiellement la même tâche, mais certaines méthodes pourront être plus adaptées pour certaines applications que d’autres, selon que l’application virtualisée est déjà en cours d’exécution.

## <a href="" id="bkmk-runvirtual-regkey"></a>Clé de Registre RunVirtual


Pour ajouter une application installée localement à un package ou à l’environnement virtuel d’un groupe de connexions, vous devez ajouter une sous-clé à la `RunVirtual` clé de Registre dans l’éditeur du Registre, comme décrit dans les sections suivantes.

Aucun paramètre de stratégie de groupe n’est disponible pour gérer cette clé de Registre, ce qui vous permet d’utiliser System Center Configuration Manager ou un autre système de distribution de logiciels électroniques ou de modifier manuellement le registre.

### <a href="" id="bkmk-"></a>Méthodes de publication de packages prises en charge lors de l’utilisation de RunVirtual

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version App-V</th>
<th align="left">Méthodes de publication prises en charge</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 SP3</p></td>
<td align="left"><p>Publié globalement ou à l’utilisateur</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5,0 via App-V 5,0 SP2</p></td>
<td align="left"><p>Publié en tout le monde</p></td>
</tr>
</tbody>
</table>

 

### Étapes de création de la sous-clé

1.  En utilisant les informations figurant dans le tableau suivant, créez une nouvelle clé de registre en utilisant le nom du fichier exécutable, par exemple, **MyApp.exe**.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Méthode de publication de package</th>
    <th align="left">Emplacement de création de la clé de Registre</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Publié dans le monde entier</p></td>
    <td align="left"><p>HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\RunVirtual</p>
    <p><strong>Par exemple </strong> : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Publié pour l’utilisateur</p></td>
    <td align="left"><p>HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual</p>
    <p><strong>Par exemple </strong> : HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Le groupe de connexions peut contenir les éléments suivants:</p>
    <ul>
    <li><p>Packages publiés uniquement globalement ou uniquement à l’utilisateur</p></li>
    <li><p>Packages publiés globalement et à l’utilisateur</p></li>
    </ul></td>
    <td align="left"><p>HKEY_LOCAL_MACHINE ou HKEY_CURRENT_USER, mais toutes les conditions suivantes doivent être remplies:</p>
    <ul>
    <li><p>Si vous voulez inclure plusieurs packages dans l’environnement virtuel, vous devez les inclure dans un groupe de connexions activé.</p></li>
    <li><p>Créez une seule sous-clé pour l’un des packages du groupe de connexion. Par exemple, si vous disposez d’un package qui est publié globalement et d’un autre package qui est publié pour l’utilisateur, vous créez une sous-clé pour l’un de ces packages, mais pas les deux. Même si vous créez une sous-clé pour un seul des packages, tous les packages du groupe de connexion, en plus de l’application locale, seront disponibles dans l’environnement virtuel.</p></li>
    <li><p>La clé de création de la sous-clé doit correspondre à la méthode de publication que vous avez utilisée pour le package.</p>
    <p>Par exemple, si vous avez publié le package pour l’utilisateur, vous devez créer la sous-clé sous <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code> .</p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

     

2.  Définissez la nouvelle valeur de la sous-clé de Registre sur PackageId et VersionId du package, en séparant les valeurs par un trait de soulignement.

    **Syntaxe**: &lt; PackageId &gt; \ _ &lt; VersionId&gt;

    **Par exemple**: 4c909996-afc9-4352-b606-0b74542a09c1 \ _Be463724-Oct1-48f1-8604-c4bd7ca92fa

    Dans l’exemple précédent, l’application produisait un fichier d’exportation du Registre (fichier. reg) comme suit:

    ``` syntax
    Windows Registry Editor Version 5.00 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual] 
    @="" 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe] 
    @="aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-555555555
    ```

## <a href="" id="bkmk-get-appvclientpackage-posh"></a>Cmdlet PowerShell Get-AppvClientPackage


Vous pouvez utiliser l’applet de passe **Start-AppVVirtualProcess** pour récupérer le nom du package, puis démarrer un processus au sein de l’environnement virtuel du package spécifié. Cette méthode vous permet de lancer une commande dans le contexte d’un package App-V, que le package s’exécute actuellement ou non.

Utilisez l’exemple de syntaxe suivant et remplacez le nom de votre package du ** &lt; package &gt; **:

`$AppVName = Get-AppvClientPackage <Package>`

`Start-AppvVirtualProcess -AppvClientObject $AppVName cmd.exe`

Si vous ne connaissez pas le nom exact de votre package, vous pouvez utiliser la commande **Get-AppvClientPackage \ *** <em> * </em> * de la ligne de commande pour obtenir le nom de l’application, par exemple: Get-AppvClientPackage \ * Word \ *.

## <a href="" id="bkmk-cl-switch-appvpid"></a>Commutateur de ligne de commande/appvpid: &lt; PID&gt;


Vous pouvez appliquer le commutateur **/appvpid &lt; : &gt; PID** à n’importe quelle commande, ce qui permet à cette commande de s’exécuter dans un processus virtuel que vous sélectionnez en spécifiant son ID de processus (PID). À l’aide de cette méthode, le nouvel exécutable est lancé dans le même environnement d’application que le fichier exécutable déjà en cours d’exécution.

Exemple : `cmd.exe /appvpid:8108`

Pour trouver l’ID de processus (PID) de votre processus App-V, exécutez la commande **tasklist.exe** à partir d’une invite de commandes avec élévation de privilèges.

## <a href="" id="bkmk-cl-hook-switch-appvve"></a>Commutateur de raccordement de ligne de commande/appvve: &lt; GUID&gt;


Ce commutateur vous permet d’exécuter une commande locale dans l’environnement virtuel d’un package App-V. Contrairement au commutateur **/appvid** , où l’environnement virtuel doit déjà être en cours d’exécution, ce commutateur vous permet de démarrer l’environnement virtuel.

Syntaxe `cmd.exe /appvve:<PACKAGEGUID_VERSIONGUID>`

Exemple : `cmd.exe /appvve:aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-55555555`

Pour obtenir le GUID du package et le GUID de version de votre application, exécutez l’applet **de contrôle Get-AppvClientPackage** . Concaténez le commutateur **/appvve** comme suit:

-   Deux-points

-   GUID du package du package souhaité

-   Un trait de soulignement

-   ID de version du package souhaité

Si vous ne connaissez pas le nom exact de votre package, utilisez la commande **Get-AppvClientPackage \ * executable\\** <em> , où **exécutable </em> * est le nom de l’application, par exemple: Get-AppvClientPackage \ * Word \ *.

Cette méthode vous permet de lancer une commande dans le contexte d’un package App-V, que le package s’exécute actuellement ou non.






## Rubriques connexes


[Référence technique pour App-V5.0](technical-reference-for-app-v-50.md)

 

 





