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
# <span data-ttu-id="eb041-103">Exécution d'une application installée localement à l'intérieur d'un environnement virtuel en cours d'exécution avec des applications virtualisées</span><span class="sxs-lookup"><span data-stu-id="eb041-103">Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications</span></span>


<span data-ttu-id="eb041-104">Vous pouvez exécuter une application installée localement dans un environnement virtuel, en plus des applications virtuelles à l’aide de Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="eb041-104">You can run a locally installed application in a virtual environment, alongside applications that have been virtualized by using Microsoft Application Virtualization (App-V).</span></span> <span data-ttu-id="eb041-105">Vous pouvez le faire si vous:</span><span class="sxs-lookup"><span data-stu-id="eb041-105">You might want to do this if you:</span></span>

-   <span data-ttu-id="eb041-106">Vous voulez installer et exécuter une application localement sur les ordinateurs clients, mais vous souhaitez virtualiser et exécuter des plug-ins spécifiques compatibles avec cette application locale.</span><span class="sxs-lookup"><span data-stu-id="eb041-106">Want to install and run an application locally on client computers, but want to virtualize and run specific plug-ins that work with that local application.</span></span>

-   <span data-ttu-id="eb041-107">Résolvez des problèmes liés à un package client App-V et voulez ouvrir une application locale dans l’environnement virtuel App-V.</span><span class="sxs-lookup"><span data-stu-id="eb041-107">Are troubleshooting an App-V client package and want to open a local application within the App-V virtual environment.</span></span>

<span data-ttu-id="eb041-108">Pour ouvrir une application locale à l’intérieur de l’environnement virtuel App-V, utilisez l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="eb041-108">Use any of the following methods to open a local application inside the App-V virtual environment:</span></span>

-   [<span data-ttu-id="eb041-109">Clé de Registre RunVirtual</span><span class="sxs-lookup"><span data-stu-id="eb041-109">RunVirtual registry key</span></span>](#bkmk-runvirtual-regkey)

-   [<span data-ttu-id="eb041-110">Cmdlet PowerShell Get-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="eb041-110">Get-AppvClientPackage PowerShell cmdlet</span></span>](#bkmk-get-appvclientpackage-posh)

-   [<span data-ttu-id="eb041-111">Commutateur de ligne de commande/appvpid: &lt; PID&gt;</span><span class="sxs-lookup"><span data-stu-id="eb041-111">Command line switch /appvpid:&lt;PID&gt;</span></span>](#bkmk-cl-switch-appvpid)

-   [<span data-ttu-id="eb041-112">Commutateur de raccordement de ligne de commande/appvve: &lt; GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="eb041-112">Command line hook switch /appvve:&lt;GUID&gt;</span></span>](#bkmk-cl-hook-switch-appvve)

<span data-ttu-id="eb041-113">Chaque méthode effectue essentiellement la même tâche, mais certaines méthodes pourront être plus adaptées pour certaines applications que d’autres, selon que l’application virtualisée est déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="eb041-113">Each method accomplishes essentially the same task, but some methods may be better suited for some applications than others, depending on whether the virtualized application is already running.</span></span>

## <a href="" id="bkmk-runvirtual-regkey"></a><span data-ttu-id="eb041-114">Clé de Registre RunVirtual</span><span class="sxs-lookup"><span data-stu-id="eb041-114">RunVirtual registry key</span></span>


<span data-ttu-id="eb041-115">Pour ajouter une application installée localement à un package ou à l’environnement virtuel d’un groupe de connexions, vous devez ajouter une sous-clé à la `RunVirtual` clé de Registre dans l’éditeur du Registre, comme décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="eb041-115">To add a locally installed application to a package or to a connection group’s virtual environment, you add a subkey to the `RunVirtual` registry key in the Registry Editor, as described in the following sections.</span></span>

<span data-ttu-id="eb041-116">Aucun paramètre de stratégie de groupe n’est disponible pour gérer cette clé de Registre, ce qui vous permet d’utiliser System Center Configuration Manager ou un autre système de distribution de logiciels électroniques ou de modifier manuellement le registre.</span><span class="sxs-lookup"><span data-stu-id="eb041-116">There is no Group Policy setting available to manage this registry key, so you have to use System Center Configuration Manager or another electronic software distribution (ESD) system, or manually edit the registry.</span></span>

### <a href="" id="bkmk-"></a><span data-ttu-id="eb041-117">Méthodes de publication de packages prises en charge lors de l’utilisation de RunVirtual</span><span class="sxs-lookup"><span data-stu-id="eb041-117">Supported methods of publishing packages when using RunVirtual</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="eb041-118">Version App-V</span><span class="sxs-lookup"><span data-stu-id="eb041-118">App-V version</span></span></th>
<th align="left"><span data-ttu-id="eb041-119">Méthodes de publication prises en charge</span><span class="sxs-lookup"><span data-stu-id="eb041-119">Supported publishing methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="eb041-120">App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="eb041-120">App-V 5.0 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb041-121">Publié globalement ou à l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="eb041-121">Published globally or to the user</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="eb041-122">App-V 5,0 via App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="eb041-122">App-V 5.0 through App-V 5.0 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="eb041-123">Publié en tout le monde</span><span class="sxs-lookup"><span data-stu-id="eb041-123">Published globally only</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="eb041-124">Étapes de création de la sous-clé</span><span class="sxs-lookup"><span data-stu-id="eb041-124">Steps to create the subkey</span></span>

1.  <span data-ttu-id="eb041-125">En utilisant les informations figurant dans le tableau suivant, créez une nouvelle clé de registre en utilisant le nom du fichier exécutable, par exemple, **MyApp.exe**.</span><span class="sxs-lookup"><span data-stu-id="eb041-125">Using the information in the following table, create a new registry key using the name of the executable file, for example, **MyApp.exe**.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="eb041-126">Méthode de publication de package</span><span class="sxs-lookup"><span data-stu-id="eb041-126">Package publishing method</span></span></th>
    <th align="left"><span data-ttu-id="eb041-127">Emplacement de création de la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="eb041-127">Where to create the registry key</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="eb041-128">Publié dans le monde entier</span><span class="sxs-lookup"><span data-stu-id="eb041-128">Published globally</span></span></p></td>
    <td align="left"><p><span data-ttu-id="eb041-129">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\RunVirtual</span><span class="sxs-lookup"><span data-stu-id="eb041-129">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual</span></span></p>
    <p><strong><span data-ttu-id="eb041-130">Par exemple </strong> : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="eb041-130">Example</strong>: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="eb041-131">Publié pour l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="eb041-131">Published to the user</span></span></p></td>
    <td align="left"><p><span data-ttu-id="eb041-132">HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual</span><span class="sxs-lookup"><span data-stu-id="eb041-132">HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</span></span></p>
    <p><strong><span data-ttu-id="eb041-133">Par exemple </strong> : HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="eb041-133">Example</strong>: HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="eb041-134">Le groupe de connexions peut contenir les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="eb041-134">Connection group can contain:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="eb041-135">Packages publiés uniquement globalement ou uniquement à l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="eb041-135">Packages that are published just globally or just to the user</span></span></p></li>
    <li><p><span data-ttu-id="eb041-136">Packages publiés globalement et à l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="eb041-136">Packages that are published globally and to the user</span></span></p></li>
    </ul></td>
    <td align="left"><p><span data-ttu-id="eb041-137">HKEY_LOCAL_MACHINE ou HKEY_CURRENT_USER, mais toutes les conditions suivantes doivent être remplies:</span><span class="sxs-lookup"><span data-stu-id="eb041-137">Either HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER key, but all of the following must be true:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="eb041-138">Si vous voulez inclure plusieurs packages dans l’environnement virtuel, vous devez les inclure dans un groupe de connexions activé.</span><span class="sxs-lookup"><span data-stu-id="eb041-138">If you want to include multiple packages in the virtual environment, you must include them in an enabled connection group.</span></span></p></li>
    <li><p><span data-ttu-id="eb041-139">Créez une seule sous-clé pour l’un des packages du groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="eb041-139">Create only one subkey for one of the packages in the connection group.</span></span> <span data-ttu-id="eb041-140">Par exemple, si vous disposez d’un package qui est publié globalement et d’un autre package qui est publié pour l’utilisateur, vous créez une sous-clé pour l’un de ces packages, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="eb041-140">If, for example, you have one package that is published globally, and another package that is published to the user, you create a subkey for either of these packages, but not both.</span></span> <span data-ttu-id="eb041-141">Même si vous créez une sous-clé pour un seul des packages, tous les packages du groupe de connexion, en plus de l’application locale, seront disponibles dans l’environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="eb041-141">Although you create a subkey for only one of the packages, all of the packages in the connection group, plus the local application, will be available in the virtual environment.</span></span></p></li>
    <li><p><span data-ttu-id="eb041-142">La clé de création de la sous-clé doit correspondre à la méthode de publication que vous avez utilisée pour le package.</span><span class="sxs-lookup"><span data-stu-id="eb041-142">The key under which you create the subkey must match the publishing method you used for the package.</span></span></p>
    <p><span data-ttu-id="eb041-143">Par exemple, si vous avez publié le package pour l’utilisateur, vous devez créer la sous-clé sous <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code> .</span><span class="sxs-lookup"><span data-stu-id="eb041-143">For example, if you published the package to the user, you must create the subkey under <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code>.</span></span></p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

     

2.  <span data-ttu-id="eb041-144">Définissez la nouvelle valeur de la sous-clé de Registre sur PackageId et VersionId du package, en séparant les valeurs par un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="eb041-144">Set the new registry subkey’s value to the PackageId and VersionId of the package, separating the values with an underscore.</span></span>

    <span data-ttu-id="eb041-145">**Syntaxe**: &lt; PackageId &gt; \ _ &lt; VersionId&gt;</span><span class="sxs-lookup"><span data-stu-id="eb041-145">**Syntax**: &lt;PackageId&gt;\_&lt;VersionId&gt;</span></span>

    <span data-ttu-id="eb041-146">**Par exemple**: 4c909996-afc9-4352-b606-0b74542a09c1 \ _Be463724-Oct1-48f1-8604-c4bd7ca92fa</span><span class="sxs-lookup"><span data-stu-id="eb041-146">**Example**: 4c909996-afc9-4352-b606-0b74542a09c1\_be463724-Oct1-48f1-8604-c4bd7ca92fa</span></span>

    <span data-ttu-id="eb041-147">Dans l’exemple précédent, l’application produisait un fichier d’exportation du Registre (fichier. reg) comme suit:</span><span class="sxs-lookup"><span data-stu-id="eb041-147">The application in the previous example would produce a registry export file (.reg file) like the following:</span></span>

    ``` syntax
    Windows Registry Editor Version 5.00 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual] 
    @="" 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe] 
    @="aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-555555555
    ```

## <a href="" id="bkmk-get-appvclientpackage-posh"></a><span data-ttu-id="eb041-148">Cmdlet PowerShell Get-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="eb041-148">Get-AppvClientPackage PowerShell cmdlet</span></span>


<span data-ttu-id="eb041-149">Vous pouvez utiliser l’applet de passe **Start-AppVVirtualProcess** pour récupérer le nom du package, puis démarrer un processus au sein de l’environnement virtuel du package spécifié.</span><span class="sxs-lookup"><span data-stu-id="eb041-149">You can use the **Start-AppVVirtualProcess** cmdlet to retrieve the package name and then start a process within the specified package's virtual environment.</span></span> <span data-ttu-id="eb041-150">Cette méthode vous permet de lancer une commande dans le contexte d’un package App-V, que le package s’exécute actuellement ou non.</span><span class="sxs-lookup"><span data-stu-id="eb041-150">This method lets you launch any command within the context of an App-V package, regardless of whether the package is currently running.</span></span>

<span data-ttu-id="eb041-151">Utilisez l’exemple de syntaxe suivant et remplacez le nom de votre package du \*\* &lt; package &gt; \*\*:</span><span class="sxs-lookup"><span data-stu-id="eb041-151">Use the following example syntax, and substitute the name of your package for **&lt;Package&gt;**:</span></span>

`$AppVName = Get-AppvClientPackage <Package>`

`Start-AppvVirtualProcess -AppvClientObject $AppVName cmd.exe`

<span data-ttu-id="eb041-152">Si vous ne connaissez pas le nom exact de votre package, vous pouvez utiliser la commande \*\*Get-AppvClientPackage \ \*\*\* <em> \* </em> \* de la ligne de commande pour obtenir le nom de l’application, par exemple: Get-AppvClientPackage \ \* Word \ \*.</span><span class="sxs-lookup"><span data-stu-id="eb041-152">If you don’t know the exact name of your package, you can use the command line **Get-AppvClientPackage \*executable\\**<em>, where \**executable</em>* is the name of the application, for example: Get-AppvClientPackage \*Word\*.</span></span>

## <a href="" id="bkmk-cl-switch-appvpid"></a><span data-ttu-id="eb041-153">Commutateur de ligne de commande/appvpid: &lt; PID&gt;</span><span class="sxs-lookup"><span data-stu-id="eb041-153">Command line switch /appvpid:&lt;PID&gt;</span></span>


<span data-ttu-id="eb041-154">Vous pouvez appliquer le commutateur **/appvpid &lt; : &gt; PID** à n’importe quelle commande, ce qui permet à cette commande de s’exécuter dans un processus virtuel que vous sélectionnez en spécifiant son ID de processus (PID).</span><span class="sxs-lookup"><span data-stu-id="eb041-154">You can apply the **/appvpid:&lt;PID&gt;** switch to any command, which enables that command to run within a virtual process that you select by specifying its process ID (PID).</span></span> <span data-ttu-id="eb041-155">À l’aide de cette méthode, le nouvel exécutable est lancé dans le même environnement d’application que le fichier exécutable déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="eb041-155">Using this method launches the new executable in the same App-V environment as an executable that is already running.</span></span>

<span data-ttu-id="eb041-156">Exemple :</span><span class="sxs-lookup"><span data-stu-id="eb041-156">Example:</span></span> `cmd.exe /appvpid:8108`

<span data-ttu-id="eb041-157">Pour trouver l’ID de processus (PID) de votre processus App-V, exécutez la commande **tasklist.exe** à partir d’une invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="eb041-157">To find the process ID (PID) of your App-V process, run the command **tasklist.exe** from an elevated command prompt.</span></span>

## <a href="" id="bkmk-cl-hook-switch-appvve"></a><span data-ttu-id="eb041-158">Commutateur de raccordement de ligne de commande/appvve: &lt; GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="eb041-158">Command line hook switch /appvve:&lt;GUID&gt;</span></span>


<span data-ttu-id="eb041-159">Ce commutateur vous permet d’exécuter une commande locale dans l’environnement virtuel d’un package App-V.</span><span class="sxs-lookup"><span data-stu-id="eb041-159">This switch lets you run a local command within the virtual environment of an App-V package.</span></span> <span data-ttu-id="eb041-160">Contrairement au commutateur **/appvid** , où l’environnement virtuel doit déjà être en cours d’exécution, ce commutateur vous permet de démarrer l’environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="eb041-160">Unlike the **/appvid** switch, where the virtual environment must already be running, this switch enables you to start the virtual environment.</span></span>

<span data-ttu-id="eb041-161">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb041-161">Syntax:</span></span> `cmd.exe /appvve:<PACKAGEGUID_VERSIONGUID>`

<span data-ttu-id="eb041-162">Exemple :</span><span class="sxs-lookup"><span data-stu-id="eb041-162">Example:</span></span> `cmd.exe /appvve:aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-55555555`

<span data-ttu-id="eb041-163">Pour obtenir le GUID du package et le GUID de version de votre application, exécutez l’applet **de contrôle Get-AppvClientPackage** .</span><span class="sxs-lookup"><span data-stu-id="eb041-163">To get the package GUID and version GUID of your application, run the **Get-AppvClientPackage** cmdlet.</span></span> <span data-ttu-id="eb041-164">Concaténez le commutateur **/appvve** comme suit:</span><span class="sxs-lookup"><span data-stu-id="eb041-164">Concatenate the **/appvve** switch with the following:</span></span>

-   <span data-ttu-id="eb041-165">Deux-points</span><span class="sxs-lookup"><span data-stu-id="eb041-165">A colon</span></span>

-   <span data-ttu-id="eb041-166">GUID du package du package souhaité</span><span class="sxs-lookup"><span data-stu-id="eb041-166">Package GUID of the desired package</span></span>

-   <span data-ttu-id="eb041-167">Un trait de soulignement</span><span class="sxs-lookup"><span data-stu-id="eb041-167">An underscore</span></span>

-   <span data-ttu-id="eb041-168">ID de version du package souhaité</span><span class="sxs-lookup"><span data-stu-id="eb041-168">Version ID of the desired package</span></span>

<span data-ttu-id="eb041-169">Si vous ne connaissez pas le nom exact de votre package, utilisez la commande **Get-AppvClientPackage \ \* executable\\** <em> , où \*\*exécutable </em> \* est le nom de l’application, par exemple: Get-AppvClientPackage \ \* Word \ \*.</span><span class="sxs-lookup"><span data-stu-id="eb041-169">If you don’t know the exact name of your package, use the command line **Get-AppvClientPackage \*executable\\**<em>, where \**executable</em>* is the name of the application, for example: Get-AppvClientPackage \*Word\*.</span></span>

<span data-ttu-id="eb041-170">Cette méthode vous permet de lancer une commande dans le contexte d’un package App-V, que le package s’exécute actuellement ou non.</span><span class="sxs-lookup"><span data-stu-id="eb041-170">This method lets you launch any command within the context of an App-V package, regardless of whether the package is currently running.</span></span>






## <span data-ttu-id="eb041-171">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb041-171">Related topics</span></span>


[<span data-ttu-id="eb041-172">Référence technique pour App-V5.0</span><span class="sxs-lookup"><span data-stu-id="eb041-172">Technical Reference for App-V 5.0</span></span>](technical-reference-for-app-v-50.md)

 

 





