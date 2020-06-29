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
# <span data-ttu-id="bd3a1-103">Gestion des modèles UE-V 2. x emplacements des paramètres à l’aide de Windows PowerShell et WMI</span><span class="sxs-lookup"><span data-stu-id="bd3a1-103">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</span></span>


<span data-ttu-id="bd3a1-104">Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 et 2,1 SP1 utilisez les modèles d’emplacement des paramètres XML pour définir les paramètres de captures et d’application de la virtualisation.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 use XML settings location templates to define the settings that User Experience Virtualization captures and applies.</span></span> <span data-ttu-id="bd3a1-105">UE-V inclut un ensemble de modèles d’emplacement des paramètres standard.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-105">UE-V includes a set of standard settings location templates.</span></span> <span data-ttu-id="bd3a1-106">Il inclut également l’outil de génération UE-V qui vous permet de créer des modèles d’emplacement des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-106">It also includes the UE-V Generator tool that enables you to create custom settings location templates.</span></span> <span data-ttu-id="bd3a1-107">Une fois que vous avez créé et déployé des modèles d’emplacement des paramètres, vous pouvez gérer ces modèles en utilisant Windows PowerShell et WMI (Windows Management Instrumentation).</span><span class="sxs-lookup"><span data-stu-id="bd3a1-107">After you create and deploy settings location templates, you can manage those templates by using Windows PowerShell and the Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="bd3a1-108">Pour obtenir la liste complète des cmdlets PowerShell d’UE-V, voir [référence sur l’applet de passe UE-v 2](https://go.microsoft.com/fwlink/p/?LinkId=393495) ( https://go.microsoft.com/fwlink/p/?LinkId=393495) .</span><span class="sxs-lookup"><span data-stu-id="bd3a1-108">For a complete list of UE-V PowerShell cmdlets, see [UE-V 2 Cmdlet Reference](https://go.microsoft.com/fwlink/p/?LinkId=393495) (https://go.microsoft.com/fwlink/p/?LinkId=393495).</span></span>

## <span data-ttu-id="bd3a1-109">Gérer les modèles d’emplacement des paramètres UE-V 2 à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd3a1-109">Manage UE-V 2 settings location templates by using Windows PowerShell</span></span>


<span data-ttu-id="bd3a1-110">Les fonctionnalités WMI et Windows PowerShell d’UE-V incluent la possibilité d’activer, de désactiver, de inscrire, de mettre à jour et de délivrer des modèles d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-110">The WMI and Windows PowerShell features of UE-V include the ability to enable, disable, register, update, and unregister settings location templates.</span></span> <span data-ttu-id="bd3a1-111">L’utilisation de ces fonctionnalités vous permet d’automatiser le processus d’inscription, de mise à jour ou de suppression de l’enregistrement de modèles auprès de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-111">By using these features, you can automate the process of registering, updating, or unregistering templates with the UE-V Agent.</span></span> <span data-ttu-id="bd3a1-112">Vous pouvez également enregistrer des modèles manuellement à l’aide des commandes WMI et Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-112">You can also manually register templates by using WMI and Windows PowerShell commands.</span></span> <span data-ttu-id="bd3a1-113">L’utilisation de ces fonctionnalités conjointement à une solution de distribution de logiciels électronique, une stratégie de groupe ou un autre mode de déploiement automatisé, tel qu’un script, vous permet d’automatiser davantage ce processus.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-113">By using these features in conjunction with an electronic software distribution solution, Group Policy, or another automated deployment method such as a script, you can further automate that process.</span></span>

<span data-ttu-id="bd3a1-114">Vous devez disposer des autorisations d’administrateur pour mettre à jour, inscrire ou annuler l’enregistrement d’un modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-114">You must have administrator permissions to update, register, or unregister a settings location template.</span></span> <span data-ttu-id="bd3a1-115">Les autorisations d’administrateur ne sont pas requises pour activer, désactiver ou répertorier des modèles.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-115">Administrator permissions are not required to enable, disable, or list templates.</span></span>

***<em><span data-ttu-id="bd3a1-116">Pour gérer les modèles d’emplacement des paramètres à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd3a1-116">To manage settings location templates by using Windows PowerShell</span></span>ell</em>***

1.  <span data-ttu-id="bd3a1-117">Utilisez un compte disposant de droits d’administrateur pour ouvrir une invite de commandes Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-117">Use an account with administrator rights to open a Windows PowerShell command prompt.</span></span>

2.  <span data-ttu-id="bd3a1-118">Utilisez les applets de commande Windows PowerShell suivantes pour inscrire et gérer les modèles d’emplacement des paramètres UE-V.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-118">Use the following Windows PowerShell cmdlets to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="bd3a1-119">Commande de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd3a1-119">Windows PowerShell command</span></span></th>
    <th align="left"><span data-ttu-id="bd3a1-120">Description</span><span class="sxs-lookup"><span data-stu-id="bd3a1-120">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-121">Répertorie tous les modèles d’emplacements des paramètres enregistrés sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-121">Lists all the settings location templates that are registered on the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate –Application &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-122">Répertorie tous les modèles d’emplacements des paramètres inscrits sur l’ordinateur où le nom de l’application ou du modèle contient des &lt; chaînes &gt; .</span><span class="sxs-lookup"><span data-stu-id="bd3a1-122">Lists all the settings location templates that are registered on the computer where the application name or template name contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplate –TemplateID &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-123">Répertorie tous les modèles d’emplacements des paramètres enregistrés sur l’ordinateur où l’ID du modèle contient des &lt; chaînes &gt; .</span><span class="sxs-lookup"><span data-stu-id="bd3a1-123">Lists all the settings location templates that are registered on the computer where the template ID contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevTemplate [-ApplicationOrTemplateID] &lt;string&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-124">Répertorie tous les modèles d’emplacements des paramètres enregistrés sur l’ordinateur où le nom de l’application ou du modèle, ou l’ID du modèle contient des &lt; chaînes &gt; .</span><span class="sxs-lookup"><span data-stu-id="bd3a1-124">Lists all the settings location templates that are registered on the computer where the application or template name, or template ID contains &lt;string&gt;.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevTemplateProgram [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-125">Obtient le nom du programme et les informations de version qui dépendent de l’ID du modèle.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-125">Gets the name of the program and version information, which depend on the template ID.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-126">Obtient la liste effective des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-126">Gets the effective list of Windows apps.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-UevAppXPackage -Computer</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-127">Obtient la liste des applications Windows configurées pour l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-127">Gets the list of Windows apps that are configured for the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-128">Obtient la liste des applications Windows configurées pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-128">Gets the list of Windows apps that are configured for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Register-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-129">Inscrit un modèle d’emplacement des paramètres avec UE-V en utilisant des chemins d’accès relatifs et/ou des caractères génériques dans les chemins d’accès aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-129">Registers one or more settings location template with UE-V by using relative paths and/or wildcard characters in file paths.</span></span> <span data-ttu-id="bd3a1-130">Après l’inscription d’un modèle, UE-V synchronise les paramètres définis dans le modèle entre les ordinateurs sur lesquels le modèle est enregistré.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-130">After a template is registered, UE-V synchronizes the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Register-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-131">Enregistre un ou plusieurs modèles d’emplacement des paramètres avec UE-V en utilisant des chemins littéraux, où aucun caractère ne peut être interprété comme des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-131">Registers one or more settings location template with UE-V by using literal paths, where no characters can be interpreted as wildcard characters.</span></span> <span data-ttu-id="bd3a1-132">Après l’inscription d’un modèle, UE-V synchronise les paramètres définis dans le modèle entre les ordinateurs sur lesquels le modèle est enregistré.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-132">After a template is registered, UE-V synchronizes the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Unregister-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-133">Annule l’inscription d’un modèle d’emplacement des paramètres avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-133">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="bd3a1-134">Lorsqu’un modèle est non enregistré, UE-V ne synchronise plus les paramètres définis dans le modèle entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-134">When a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Unregister-UevTemplate -All</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-135">Annule l’inscription de tous les modèles d’emplacement des paramètres avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-135">Unregisters all settings location templates with UE-V.</span></span> <span data-ttu-id="bd3a1-136">Lorsqu’un modèle est non enregistré, UE-V ne synchronise plus les paramètres définis dans le modèle entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-136">When a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Update-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-137">Met à jour un ou plusieurs modèles d’emplacement des paramètres avec une version plus récente du modèle.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-137">Updates one or more settings location templates with a more recent version of the template.</span></span> <span data-ttu-id="bd3a1-138">Utilisez des chemins d’accès relatifs et/ou des caractères génériques dans les chemins d’accès aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-138">Use relative paths and/or wildcard characters in the file paths.</span></span> <span data-ttu-id="bd3a1-139">Le nouveau modèle doit être une version plus récente que le modèle existant.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-139">The new template should be a newer version than the existing template.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Update-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-140">Met à jour un ou plusieurs modèles d’emplacement des paramètres avec une version plus récente du modèle.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-140">Updates one or more settings location templates with a more recent version of the template.</span></span> <span data-ttu-id="bd3a1-141">Utilisez les chemins d’accès complets aux fichiers de modèles dans lesquels aucun caractère ne peut être interprété en tant que caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-141">Use full paths to template files, where no characters can be interpreted as wildcard characters.</span></span> <span data-ttu-id="bd3a1-142">Le nouveau modèle doit être une version plus récente que le modèle existant.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-142">The new template should be a newer version than the existing template.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-143">Suppression d’une ou plusieurs applications Windows de la liste des applications Windows sur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-143">Removes one or more Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage -CurrentComputerUser</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-144">Supprime l’application Windows de la liste des applications Windows actuelles de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-144">Removes Windows app from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage –Computer -All</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-145">Supprime toutes les applications Windows de la liste des applications Windows sur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-145">Removes all Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-146">Suppression d’une ou plusieurs applications Windows de la liste des applications Windows actuelles de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-146">Removes one or more Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Clear-UevAppXPackage [–CurrentComputerUser] -All</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-147">Supprime toutes les applications Windows de la liste des applications Windows actuelles de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-147">Removes all Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-148">Désactive un modèle d’emplacement des paramètres pour l’utilisateur actuel de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-148">Disables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Disable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-149">Désactive une ou plusieurs applications Windows dans la liste des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-149">Disables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Disable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-150">Désactive une ou plusieurs applications Windows dans la liste des applications Windows actuelles de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-150">Disables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevTemplate [-ID] &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-151">Active un modèle d’emplacement des paramètres pour l’utilisateur actuel de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-151">Enables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Enable-UevAppXPackage –Computer [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-152">Active une ou plusieurs applications Windows dans la liste des applications Windows sur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-152">Enables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Enable-UevAppXPackage [–CurrentComputerUser] [-PackageFamilyName] &lt;package family name&gt;[,&lt;package family name&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-153">Active une ou plusieurs applications Windows dans la liste des applications Windows actuelles de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-153">Enables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Test-UevTemplate [-Path] &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-154">Détermine s’il s’agit d’un ou de plusieurs modèles d’emplacement des paramètres qui sont conformes au schéma XML.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-154">Determines whether one or more settings location templates comply with its XML schema.</span></span> <span data-ttu-id="bd3a1-155">Peuvent utiliser des chemins d’accès relatifs et des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-155">Can use relative paths and wildcard characters.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Test-UevTemplate –LiteralPath &lt;template file path&gt;[,&lt;template file path&gt;]</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-156">Détermine s’il s’agit d’un ou de plusieurs modèles d’emplacement des paramètres qui sont conformes au schéma XML.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-156">Determines whether one or more settings location templates comply with its XML schema.</span></span> <span data-ttu-id="bd3a1-157">Le chemin d’accès doit être un chemin d’accès complet au fichier de modèle, mais n’inclut pas de caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-157">The path must be a full path to the template file, but does not include wildcard characters.</span></span></p></td>
    </tr>
    </tbody>
    </table>



<span data-ttu-id="bd3a1-158">Les fonctionnalités Windows PowerShell d’UE-V vous permettent de gérer un ensemble de modèles de paramètres déployés dans votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-158">The UE-V Windows PowerShell features enable you to manage a group of settings templates that are deployed in your enterprise.</span></span> <span data-ttu-id="bd3a1-159">Utilisez la procédure suivante pour gérer un groupe de modèles à l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-159">Use the following procedure to manage a group of templates by using Windows PowerShell.</span></span>

**<span data-ttu-id="bd3a1-160">Pour gérer un groupe de modèles d’emplacement des paramètres à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd3a1-160">To manage a group of settings location templates by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="bd3a1-161">Modifiez ou mettez à jour les modèles d’emplacement des paramètres souhaités.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-161">Modify or update the desired settings location templates.</span></span>

2.  <span data-ttu-id="bd3a1-162">Si vous voulez modifier ou mettre à jour les modèles d’emplacement des paramètres, déployez ces modèles d’emplacement des paramètres dans un dossier accessible à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-162">If you want to modify or update the settings location templates, deploy those settings location templates to a folder that is accessible to the local computer.</span></span>

3.  <span data-ttu-id="bd3a1-163">Sur l’ordinateur local, ouvrez une fenêtre Windows PowerShell avec des droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-163">On the local computer, open a Windows PowerShell window with administrator rights.</span></span>

4.  <span data-ttu-id="bd3a1-164">Annulez l’enregistrement de toutes les versions inscrites des modèles en entrant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-164">Unregister all the previously registered versions of the templates by typing the following command.</span></span>

    ``` syntax
    Unregister-UevTemplate -All
    ```

    <span data-ttu-id="bd3a1-165">Cette commande supprime tous les modèles actifs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-165">This command unregisters all active templates on the computer.</span></span>

5.  <span data-ttu-id="bd3a1-166">Enregistrez les modèles mis à jour en entrant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-166">Register the updated templates by typing the following command.</span></span>

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    <span data-ttu-id="bd3a1-167">Cette commande enregistre tous les modèles d’emplacement des paramètres situés dans le dossier de modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-167">This command registers all of the settings location templates that are located in the specified template folder.</span></span>

### <a href="" id="win8applist"></a><span data-ttu-id="bd3a1-168">Liste des applications Windows</span><span class="sxs-lookup"><span data-stu-id="bd3a1-168">Windows app list</span></span>

<span data-ttu-id="bd3a1-169">En répertoriant une application Windows dans la liste des applications Windows, vous spécifiez si l’application est activée ou désactivée pour la synchronisation des paramètres.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-169">By listing a Windows app in the Windows app list, you specify whether that app is enabled or disabled for settings synchronization.</span></span> <span data-ttu-id="bd3a1-170">Les applications sont identifiées dans la liste par leur nom de famille de packages et si la synchronisation des paramètres doit être activée ou désactivée pour cette application.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-170">Apps are identified in the list by their Package Family name and whether settings synchronization should be enabled or disabled for that app.</span></span> <span data-ttu-id="bd3a1-171">Lorsque vous utilisez ces paramètres avec le paramètre de comportement de synchronisation par défaut non répertorié, vous pouvez contrôler si les applications Windows sont synchronisées.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-171">When you use these settings along with the Unlisted Default Sync Behavior setting, you can control whether Windows apps are synchronized.</span></span>

<span data-ttu-id="bd3a1-172">Pour afficher le nom de la famille de packages des applications Windows installées, à l’invite de commandes Windows PowerShell, entrez:</span><span class="sxs-lookup"><span data-stu-id="bd3a1-172">To display the Package Family Name of installed Windows apps, at a Windows PowerShell command prompt, enter:</span></span>

``` syntax
Get-AppxPackage | Sort-Object PackageFamilyName | Format-Table PackageFamilyName
```

<span data-ttu-id="bd3a1-173">Pour afficher une liste des applications Windows qui peuvent synchroniser les paramètres sur un ordinateur dont le nom de la famille de packages, le statut activée et la source activée, à l’invite de commandes Windows PowerShell, entrez:</span><span class="sxs-lookup"><span data-stu-id="bd3a1-173">To display a list of Windows apps that can synchronize settings on a computer with their package family name, enabled status, and enabled source, at a Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage`

**<span data-ttu-id="bd3a1-174">Définitions des propriétés Get-UevAppxPackage</span><span class="sxs-lookup"><span data-stu-id="bd3a1-174">Definitions of Get-UevAppxPackage properties</span></span>**

<a href="" id="displayname"></a>**<span data-ttu-id="bd3a1-175">DisplayName</span><span class="sxs-lookup"><span data-stu-id="bd3a1-175">DisplayName</span></span>**  
<span data-ttu-id="bd3a1-176">Nom affiché à l’utilisateur dans l’application Centre de paramètres de la société.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-176">The name that is displayed to the user in the Company Settings Center application.</span></span> <span data-ttu-id="bd3a1-177">La `DisplayName` propriété est dérivée de la `PackageFamilyName` propriété.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-177">The `DisplayName` property is derived from the `PackageFamilyName` property.</span></span>

<a href="" id="packagefamilyname"></a>**<span data-ttu-id="bd3a1-178">Propriété packagefamilyname</span><span class="sxs-lookup"><span data-stu-id="bd3a1-178">PackageFamilyName</span></span>**  
<span data-ttu-id="bd3a1-179">Nom du package installé pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-179">The name of the package that is installed for the current user.</span></span>

<a href="" id="enabled"></a>**<span data-ttu-id="bd3a1-180">Activé</span><span class="sxs-lookup"><span data-stu-id="bd3a1-180">Enabled</span></span>**  
<span data-ttu-id="bd3a1-181">Définit si les paramètres de l’application sont configurés pour la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-181">Defines whether the settings for the app are configured to synchronize.</span></span>

<a href="" id="enabledsource"></a>**<span data-ttu-id="bd3a1-182">EnabledSource</span><span class="sxs-lookup"><span data-stu-id="bd3a1-182">EnabledSource</span></span>**  
<span data-ttu-id="bd3a1-183">L’emplacement où la configuration qui active ou désactive l’application est définie.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-183">The location where the configuration that enables or disables the app is set.</span></span> <span data-ttu-id="bd3a1-184">Les valeurs possibles sont: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*et *PolicyUser*.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-184">Possible values are: *NotSet*, *LocalMachine*, *LocalUser*, *PolicyMachine*, and *PolicyUser*.</span></span>

<a href="" id="notset"></a>**<span data-ttu-id="bd3a1-185">NotSet</span><span class="sxs-lookup"><span data-stu-id="bd3a1-185">NotSet</span></span>**  
<span data-ttu-id="bd3a1-186">La stratégie n’est pas configurée pour synchroniser cette application.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-186">The policy is not configured to synchronize this app.</span></span>

<a href="" id="localmachine"></a>**<span data-ttu-id="bd3a1-187">LocalMachine</span><span class="sxs-lookup"><span data-stu-id="bd3a1-187">LocalMachine</span></span>**  
<span data-ttu-id="bd3a1-188">L’État Enabled est défini dans la section ordinateur local du Registre.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-188">The enabled state is set in the local computer section of the registry.</span></span>

<a href="" id="localuser"></a>**<span data-ttu-id="bd3a1-189">LocalUser</span><span class="sxs-lookup"><span data-stu-id="bd3a1-189">LocalUser</span></span>**  
<span data-ttu-id="bd3a1-190">L’État Enabled est défini dans la section Current User du Registre.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-190">The enabled state is set in the current user section of the registry.</span></span>

<a href="" id="policymachine"></a>**<span data-ttu-id="bd3a1-191">PolicyMachine</span><span class="sxs-lookup"><span data-stu-id="bd3a1-191">PolicyMachine</span></span>**  
<span data-ttu-id="bd3a1-192">L’État Enabled est défini dans la section Stratégie de la section ordinateur local du Registre.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-192">The enabled state is set in the policy section of the local computer section of the registry.</span></span>

<span data-ttu-id="bd3a1-193">Pour obtenir la liste des applications Windows configurées par l’utilisateur, à l’invite de commandes Windows PowerShell, entrez:</span><span class="sxs-lookup"><span data-stu-id="bd3a1-193">To get the user-configured list of Windows apps, at the Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage –CurrentComputerUser`

<span data-ttu-id="bd3a1-194">Pour obtenir la liste des applications Windows configurée par l’ordinateur, à l’invite de commandes Windows PowerShell, entrez:</span><span class="sxs-lookup"><span data-stu-id="bd3a1-194">To get the computer-configured list of Windows apps, at the Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage –Computer`

<span data-ttu-id="bd3a1-195">Pour l’un ou l’autre paramètre, CurrentComputerUser ou ordinateur, l’applet de passe renvoie une liste des applications Windows qui sont configurées au niveau de l’ordinateur ou de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-195">For either parameter, CurrentComputerUser or Computer, the cmdlet returns a list of the Windows apps that are configured at the user or at the computer level.</span></span>

**<span data-ttu-id="bd3a1-196">Définitions des propriétés</span><span class="sxs-lookup"><span data-stu-id="bd3a1-196">Definitions of properties</span></span>**

<a href="" id="displayname"></a>**<span data-ttu-id="bd3a1-197">DisplayName</span><span class="sxs-lookup"><span data-stu-id="bd3a1-197">DisplayName</span></span>**  
<span data-ttu-id="bd3a1-198">Nom affiché à l’utilisateur dans l’application Centre de paramètres de la société.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-198">The name that is displayed to the user in the Company Settings Center application.</span></span> <span data-ttu-id="bd3a1-199">La `DisplayName` propriété est dérivée de la `PackageFamilyName` propriété.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-199">The `DisplayName` property is derived from the `PackageFamilyName` property.</span></span>

<a href="" id="packagefamilyname"></a>**<span data-ttu-id="bd3a1-200">Propriété packagefamilyname</span><span class="sxs-lookup"><span data-stu-id="bd3a1-200">PackageFamilyName</span></span>**  
<span data-ttu-id="bd3a1-201">Nom du package installé pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-201">The name of the package that is installed for the current user.</span></span>

<a href="" id="enabled"></a>**<span data-ttu-id="bd3a1-202">Activé</span><span class="sxs-lookup"><span data-stu-id="bd3a1-202">Enabled</span></span>**  
<span data-ttu-id="bd3a1-203">Définit si les paramètres de l’application sont configurés pour se synchroniser pour le commutateur spécifié ( **utilisateur** ou **ordinateur**).</span><span class="sxs-lookup"><span data-stu-id="bd3a1-203">Defines whether the settings for the app are configured to synchronize for the specified switch, that is, **user** or **computer**.</span></span>

<a href="" id="installed"></a>**<span data-ttu-id="bd3a1-204">Installé</span><span class="sxs-lookup"><span data-stu-id="bd3a1-204">Installed</span></span>**  
<span data-ttu-id="bd3a1-205">True si l’application est installée sur le propriété packagefamilyname de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-205">True if the app, that is, the PackageFamilyName is installed for the current user.</span></span>

### <span data-ttu-id="bd3a1-206">Gérer les modèles d’emplacement des paramètres UE-V 2 à l’aide de WMI</span><span class="sxs-lookup"><span data-stu-id="bd3a1-206">Manage UE-V 2 settings location templates by using WMI</span></span>

<span data-ttu-id="bd3a1-207">La virtualisation de l’interface utilisateur fournit l’ensemble des commandes WMI suivantes.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-207">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="bd3a1-208">Les administrateurs peuvent utiliser ces interfaces pour gérer les modèles d’emplacement des paramètres à partir de Windows PowerShell et automatiser les tâches d’administration des modèles.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-208">Administrators can use these interfaces to manage settings location templates from Windows PowerShell and automate template administrative tasks.</span></span>

**<span data-ttu-id="bd3a1-209">Pour gérer les modèles d’emplacement des paramètres à l’aide de WMI</span><span class="sxs-lookup"><span data-stu-id="bd3a1-209">To manage settings location templates by using WMI</span></span>**

1.  <span data-ttu-id="bd3a1-210">Utilisez un compte disposant de droits d’administrateur pour ouvrir une fenêtre Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-210">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="bd3a1-211">Utilisez les commandes WMI suivantes pour inscrire et gérer les modèles d’emplacement des paramètres UE-V.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-211">Use the following WMI commands to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>                         Windows PowerShell command</code></th>
    <th align="left"><span data-ttu-id="bd3a1-212">Description</span><span class="sxs-lookup"><span data-stu-id="bd3a1-212">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-213">Répertorie tous les modèles d’emplacements des paramètres inscrits pour l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-213">Lists all the settings location templates that are registered for the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod –Namespace root\Microsoft\UEV –Class SettingsLocationTemplate –Name GetProcessInfoByTemplateId &lt;template Id&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-214">Obtient le nom du programme et les informations de version qui dépendent du nom du modèle.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-214">Gets the name of the program and version information, which depends on the template name.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV EffectiveWindows8App</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-215">Obtient la liste effective des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-215">Gets the effective list of Windows apps.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="bd3a1-216">Get-WmiObject-namespace root\Microsoft\UEV MachineConfiguredWindows8App</span><span class="sxs-lookup"><span data-stu-id="bd3a1-216">Get-WmiObject -Namespace root\Microsoft\UEV MachineConfiguredWindows8App</span></span></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-217">Obtient la liste des applications Windows configurées pour l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-217">Gets the list of Windows apps that are configured for the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguredWindows8App</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-218">Obtient la liste des applications Windows configurées pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-218">Gets the list of Windows apps that are configured for the current user.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-219">Inscrit un modèle d’emplacement des paramètres avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-219">Registers a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-220">Annule l’inscription d’un modèle d’emplacement des paramètres avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-220">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="bd3a1-221">Dès qu’aucun modèle n’est enregistré, UE-V ne synchronise plus les paramètres définis dans le modèle entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-221">As soon as a template is unregistered, UE-V no longer synchronizes the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-222">Met à jour un modèle d’emplacement des paramètres avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-222">Updates a settings location template with UE-V.</span></span> <span data-ttu-id="bd3a1-223">Le nouveau modèle doit être une version plus récente que celle existante.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-223">The new template should be a newer version than the existing one.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-224">Suppression d’une ou plusieurs applications Windows de la liste des applications Windows sur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-224">Removes one or more Windows apps from the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name RemoveApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-225">Suppression d’une ou plusieurs applications Windows de la liste des applications Windows actuelles de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-225">Removes one or more Windows apps from the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-226">Désactive un ou plusieurs modèles d’emplacement des paramètres avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-226">Disables one or more settings location templates with UE-V.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-227">Désactive une ou plusieurs applications Windows dans la liste des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-227">Disables one or more Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name DisableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-228">Désactive une ou plusieurs applications Windows dans la liste des applications Windows actuelles de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-228">Disables one or more Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-229">Active un modèle d’emplacement des paramètres avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-229">Enables a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class MachineConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-230">Active les applications Windows dans la liste des applications Windows sur ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-230">Enables Windows apps in the computer Windows app list.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserConfiguredWindows8App -Name EnableApp -ArgumentList &lt;package family name | package family name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-231">Active les applications Windows dans la liste des applications Windows actuelles de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-231">Enables Windows apps in the current user Windows app list.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="bd3a1-232">Détermine si un modèle d’emplacement des paramètres donné est conforme à son schéma XML.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-232">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
Where a list of Package Family Names is called by the WMI command, the list must be in quotes and separated by a pipe symbol, for example, `"<package family name | package family name>"`.
~~~



### <span data-ttu-id="bd3a1-233">Déploiement de l’agent UE-V à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd3a1-233">Deploying the UE-V Agent using Windows PowerShell</span></span>

**<span data-ttu-id="bd3a1-234">Déploiement d’UE-V agent à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd3a1-234">How to deploy the UE-V Agent by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="bd3a1-235">Copiez le package d’installation de l’agent UE-V dans un partage réseau accessible.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-235">Stage the UE-V Agent installation package in an accessible network share.</span></span>

    **<span data-ttu-id="bd3a1-236">Remarque</span><span class="sxs-lookup"><span data-stu-id="bd3a1-236">Note</span></span>**  
    <span data-ttu-id="bd3a1-237">Utilisez AgentSetup.exe pour déployer à la fois les versions 32 bits et 64 bits de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-237">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="bd3a1-238">Les packages Windows Installer, AgentSetupx86.msi et AgentSetupx64.msi, sont disponibles pour chaque architecture.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-238">The Windows Installer packages, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="bd3a1-239">Pour désinstaller l’agent UE-V ultérieurement à l’aide du fichier d’installation, vous devez utiliser le même type de fichier.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-239">To uninstall the UE-V Agent at a later time by using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="bd3a1-240">Utilisez l’une des commandes Windows PowerShell suivantes pour installer l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-240">Use one of the following Windows PowerShell commands to install the UE-V Agent.</span></span>

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

<span data-ttu-id="bd3a1-241">Vous **avez une suggestion pour UE-V**?</span><span class="sxs-lookup"><span data-stu-id="bd3a1-241">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="bd3a1-242">Ajoutez ou Votez en fonction [de suggestions.](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization)</span><span class="sxs-lookup"><span data-stu-id="bd3a1-242">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="bd3a1-243">Vous **avez un problème UE-V**?</span><span class="sxs-lookup"><span data-stu-id="bd3a1-243">**Got a UE-V issue**?</span></span> <span data-ttu-id="bd3a1-244">Utiliser le [Forum de TechNet UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="bd3a1-244">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="bd3a1-245">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bd3a1-245">Related topics</span></span>


[<span data-ttu-id="bd3a1-246">Administration d’UE-V 2. x avec Windows PowerShell et WMI</span><span class="sxs-lookup"><span data-stu-id="bd3a1-246">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="bd3a1-247">Administration d’UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="bd3a1-247">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









