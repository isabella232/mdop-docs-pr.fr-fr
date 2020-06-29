---
title: Gestion des modèles d'emplacement des paramètres UE-V1.0 à l'aide de PowerShell et WMI
description: Gestion des modèles d'emplacement des paramètres UE-V1.0 à l'aide de PowerShell et WMI
author: dansimp
ms.assetid: 4b911c78-a5e9-4199-bfeb-72ab764d47c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8dab0997cdfaf7c96862fcce4bc012c3edfe0c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804267"
---
# <span data-ttu-id="ebbcf-103">Gestion des modèles d'emplacement des paramètres UE-V1.0 à l'aide de PowerShell et WMI</span><span class="sxs-lookup"><span data-stu-id="ebbcf-103">Managing UE-V 1.0 Settings Location Templates Using PowerShell and WMI</span></span>


<span data-ttu-id="ebbcf-104">La virtualisation de l’utilisation de l’utilisateur Microsoft (UE-V) utilise des modèles d’emplacement des paramètres (fichiers XML) qui définissent les paramètres capturés et appliqués par la virtualisation de l’utilisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings captured and applied by User Experience Virtualization.</span></span> <span data-ttu-id="ebbcf-105">UE-V inclut un ensemble de modèles d’emplacement des paramètres standard.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-105">UE-V includes a set of standard settings location templates.</span></span> <span data-ttu-id="ebbcf-106">Il inclut également l’outil de génération UE-V qui vous permet de créer des modèles d’emplacement des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-106">It also includes the UE-V Generator tool that enables you to create custom settings location templates.</span></span> <span data-ttu-id="ebbcf-107">Une fois que vous avez créé et déployé des modèles d’emplacement des paramètres, vous pouvez gérer ces modèles en utilisant PowerShell ou WMI.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-107">After you create and deploy settings location templates you can manage those templates using PowerShell or WMI.</span></span>

## <span data-ttu-id="ebbcf-108">Gérer les modèles d’emplacement des paramètres avec WMI et PowerShell</span><span class="sxs-lookup"><span data-stu-id="ebbcf-108">Manage settings location templates with WMI and PowerShell</span></span>


<span data-ttu-id="ebbcf-109">Les fonctionnalités WMI et PowerShell d’UE-V incluent la possibilité d’activer, de désactiver, de inscrire, de mettre à jour et de déregistrer les modèles d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-109">The WMI and PowerShell features of UE-V include the ability to enable, disable, register, update, and unregister settings location templates.</span></span> <span data-ttu-id="ebbcf-110">L’utilisation de ces fonctionnalités vous permet d’automatiser le processus d’inscription, de mise à jour ou de suppression de l’enregistrement de modèles auprès de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-110">By using these features, you can automate the process of registering, updating, or unregistering templates with the UE-V agent.</span></span> <span data-ttu-id="ebbcf-111">Vous pouvez également enregistrer des modèles manuellement à l’aide des commandes WMI et PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-111">You can also manually register templates using WMI and PowerShell commands.</span></span> <span data-ttu-id="ebbcf-112">L’utilisation de ces fonctionnalités conjointement à une solution de distribution de logiciels électronique, une stratégie de groupe ou un autre mode de déploiement automatisé, tel qu’un script, vous permet d’automatiser davantage ce processus.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-112">By using these features in conjunction with an electronic software distribution solution, Group Policy, or another automated deployment method such as a script, you can further automate that process.</span></span>

<span data-ttu-id="ebbcf-113">Vous devez disposer des autorisations d’administrateur pour mettre à jour, inscrire ou annuler l’enregistrement d’un modèle d’emplacement des paramètres.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-113">You must have administrator permissions to update, register, or unregister a settings location template.</span></span> <span data-ttu-id="ebbcf-114">Les autorisations d’administrateur ne sont pas requises pour activer ou désactiver des modèles.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-114">Administrator permissions are not required to enable or disable templates.</span></span>

**<span data-ttu-id="ebbcf-115">Pour gérer les modèles d’emplacement des paramètres avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="ebbcf-115">To manage settings location templates with PowerShell</span></span>**

1.  <span data-ttu-id="ebbcf-116">Utilisez un compte disposant de droits d’administrateur pour ouvrir une fenêtre Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-116">Use an account with administrator rights to open a Windows PowerShell window.</span></span> <span data-ttu-id="ebbcf-117">Pour importer le module **Microsoft UE-V PowerShell** , tapez la commande suivante à l’invite de commandes PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-117">To import the **Microsoft UE-V PowerShell** module, type the following command at the PowerShell command prompt.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="ebbcf-118">Utilisez les applets de commande PowerShell suivantes pour inscrire et gérer les modèles d’emplacement des paramètres UE-V.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-118">Use the following PowerShell cmdlets to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="ebbcf-119">Commande PowerShell</span><span class="sxs-lookup"><span data-stu-id="ebbcf-119">PowerShell command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="ebbcf-120">Description</span><span class="sxs-lookup"><span data-stu-id="ebbcf-120">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="ebbcf-121">Get-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="ebbcf-121">Get-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ebbcf-122">Répertorie tous les modèles d’emplacements des paramètres enregistrés sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-122">Lists all the settings location templates registered on the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="ebbcf-123">Register-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="ebbcf-123">Register-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ebbcf-124">Inscrit un modèle d’emplacement des paramètres avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-124">Registers a settings location template with UE-V.</span></span> <span data-ttu-id="ebbcf-125">Une fois qu’un modèle est enregistré, UE-V va synchroniser les paramètres définis dans le modèle entre les ordinateurs sur lesquels le modèle est enregistré.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-125">Once a template is registered, UE-V will synchronize the settings that are defined in the template between computers that have the template registered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="ebbcf-126">Unregister-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="ebbcf-126">Unregister-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ebbcf-127">Annule l’inscription d’un modèle d’emplacement des paramètres avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-127">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="ebbcf-128">Dès qu’aucun modèle n’est enregistré, UE-V ne synchronise plus les paramètres définis dans le modèle entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-128">As soon as a template is unregistered, UE-V will no longer synchronize the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="ebbcf-129">Update-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="ebbcf-129">Update-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ebbcf-130">Met à jour un modèle d’emplacement des paramètres avec une version plus récente du modèle.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-130">Updates a settings location template with a more recent version of the template.</span></span> <span data-ttu-id="ebbcf-131">Le nouveau modèle doit avoir une version ultérieure à celle existante.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-131">The new template should have a version that is later than the existing one.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="ebbcf-132">Disable-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="ebbcf-132">Disable-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ebbcf-133">Désactive un modèle d’emplacement des paramètres pour l’utilisateur actuel de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-133">Disables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="ebbcf-134">Enable-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="ebbcf-134">Enable-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ebbcf-135">Active un modèle d’emplacement des paramètres pour l’utilisateur actuel de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-135">Enables a settings location template for the current user of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="ebbcf-136">Test-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="ebbcf-136">Test-UevTemplate</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ebbcf-137">Détermine si un modèle d’emplacement des paramètres donné est conforme à son schéma XML.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-137">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

<span data-ttu-id="ebbcf-138">Les fonctionnalités PowerShell d’UE-V vous permettent de gérer un groupe de modèles de paramètres déployés dans votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-138">The UE-V PowerShell features allow you to manage a group of settings templates deployed in your enterprise.</span></span> <span data-ttu-id="ebbcf-139">Pour gérer un groupe de modèles à l’aide de PowerShell, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-139">To manage a group of templates using PowerShell, do the following.</span></span>

**<span data-ttu-id="ebbcf-140">Pour gérer un groupe de modèles d’emplacement des paramètres avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="ebbcf-140">To manage a group of settings location templates with PowerShell</span></span>**

1.  <span data-ttu-id="ebbcf-141">Modifiez ou mettez à jour les modèles d’emplacement des paramètres souhaités.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-141">Modify or update the desired settings location templates.</span></span>

2.  <span data-ttu-id="ebbcf-142">Déployez les modèles d’emplacement des paramètres souhaités dans un dossier accessible à partir de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-142">Deploy the desired settings location templates to a folder accessible to the local computer.</span></span>

3.  <span data-ttu-id="ebbcf-143">Sur l’ordinateur local, ouvrez une fenêtre Windows PowerShell avec des droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-143">On the local computer, open a Windows PowerShell window with administrator rights.</span></span>

4.  <span data-ttu-id="ebbcf-144">Importez le module Microsoft UE-V PowerShell en entrant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-144">Import the Microsoft UE-V PowerShell module, by typing the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

5.  <span data-ttu-id="ebbcf-145">Annulez l’enregistrement de toutes les versions inscrites des modèles en entrant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-145">Unregister all the previously registered versions of the templates by typing the following command.</span></span>

    ``` syntax
    Get-UevTemplate | Unregister-UevTemplate
    ```

    <span data-ttu-id="ebbcf-146">Le fichier est alors annulé sur tous les modèles actifs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-146">This will unregister all active templates on the computer.</span></span>

6.  <span data-ttu-id="ebbcf-147">Enregistrez les modèles mis à jour en entrant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-147">Register the updated templates by typing the following command.</span></span>

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    <span data-ttu-id="ebbcf-148">Les modèles d’emplacement des paramètres sont enregistrés dans le dossier de modèles spécifié.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-148">This will register all of the settings location templates located in the specified template folder.</span></span>

<span data-ttu-id="ebbcf-149">La virtualisation de l’interface utilisateur fournit l’ensemble des commandes WMI suivantes.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-149">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="ebbcf-150">Les administrateurs peuvent utiliser ces interfaces pour gérer les modèles d’emplacement des paramètres à partir de Windows PowerShell et automatiser les tâches d’administration des modèles.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-150">Administrators can use these interfaces to manage settings location templates from Windows PowerShell and automate template administrative tasks.</span></span>

**<span data-ttu-id="ebbcf-151">Pour gérer les modèles d’emplacement des paramètres avec WMI</span><span class="sxs-lookup"><span data-stu-id="ebbcf-151">To manage settings location templates with WMI</span></span>**

1.  <span data-ttu-id="ebbcf-152">Utilisez un compte disposant de droits d’administrateur pour ouvrir une fenêtre Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-152">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="ebbcf-153">Utilisez les commandes WMI suivantes pour inscrire et gérer les modèles d’emplacement des paramètres UE-V.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-153">Use the following WMI commands to register and manage the UE-V settings location templates.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="ebbcf-154">Commande PowerShell</span><span class="sxs-lookup"><span data-stu-id="ebbcf-154">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="ebbcf-155">Description</span><span class="sxs-lookup"><span data-stu-id="ebbcf-155">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="ebbcf-156">Get-WmiObject-namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId, Nom_modèle, TemplateVersion, activé | Format-table-dimensionnement automatique</span><span class="sxs-lookup"><span data-stu-id="ebbcf-156">Get-WmiObject -Namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId,TemplateName, TemplateVersion,Enabled | Format-Table -Autosize</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ebbcf-157">Répertorie tous les modèles d’emplacements des paramètres enregistrés pour l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-157">Lists all the settings location templates registered for the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="ebbcf-158">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-nom Register--chemin de modèle-ArgumentList &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="ebbcf-158">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Register -ArgumentList &lt;template path &gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ebbcf-159">Inscrit un modèle d’emplacement des paramètres avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-159">Registers a settings location template with UE-V.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="ebbcf-160">Invoke-WmiMethod-namespace root\Microsoft\UEV-SettingsLocationTemplate-nom UnregisterByTemplateId-ID de &lt; modèle-argumentlist&gt;</span><span class="sxs-lookup"><span data-stu-id="ebbcf-160">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name UnregisterByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ebbcf-161">Annule l’inscription d’un modèle d’emplacement des paramètres avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-161">Unregisters a settings location template with UE-V.</span></span> <span data-ttu-id="ebbcf-162">Dès qu’aucun modèle n’est enregistré, UE-V ne synchronise plus les paramètres définis dans le modèle entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-162">As soon as a template is unregistered, UE-V will no longer synchronize the settings that are defined in the template between computers.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="ebbcf-163">Invoke-WmiMethod-namespace root\Microsoft\UEV-SettingsLocationTemplate-nom EnableByTemplateId-ID de &lt; modèle-argumentlist&gt;</span><span class="sxs-lookup"><span data-stu-id="ebbcf-163">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name EnableByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ebbcf-164">Active un modèle d’emplacement des paramètres avec UE-V</span><span class="sxs-lookup"><span data-stu-id="ebbcf-164">Enables a settings location template with UE-V</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="ebbcf-165">Invoke-WmiMethod-namespace root\Microsoft\UEV-SettingsLocationTemplate-nom DisableByTemplateId-ID de &lt; modèle-argumentlist&gt;</span><span class="sxs-lookup"><span data-stu-id="ebbcf-165">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name DisableByTemplateId -ArgumentList &lt;template ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ebbcf-166">Désactive un modèle d’emplacement des paramètres avec UE-V</span><span class="sxs-lookup"><span data-stu-id="ebbcf-166">Disables a settings location template with UE-V</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="ebbcf-167">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-nom &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="ebbcf-167">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Update -ArgumentList &lt;template path&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ebbcf-168">Met à jour un modèle d’emplacement des paramètres avec UE-V.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-168">Updates a settings location template with UE-V.</span></span> <span data-ttu-id="ebbcf-169">Le nouveau modèle doit avoir une version supérieure à la version existante.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-169">The new template should have a version that is higher than the existing one.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="ebbcf-170">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-nom Validate- &lt; argumentlist&gt;</span><span class="sxs-lookup"><span data-stu-id="ebbcf-170">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name Validate -ArgumentList &lt;template path&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="ebbcf-171">Détermine si un modèle d’emplacement des paramètres donné est conforme à son schéma XML.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-171">Determines whether a given settings location template complies with its XML schema.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="ebbcf-172">Déploiement de l’agent UE-V avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="ebbcf-172">How to deploy the UE-V agent with PowerShell</span></span>**

1.  <span data-ttu-id="ebbcf-173">Copiez le fichier du programme d’installation d’UE-V dans un partage réseau accessible.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-173">Stage the UE-V installer file in an accessible network share.</span></span>

    <span data-ttu-id="ebbcf-174">**Remarques**  Utilisez AgentSetup.exe pour déployer à la fois les versions 32 bits et 64 bits de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-174">**Note** Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="ebbcf-175">Les versions des fichiers du programme d’installation Windows, AgentSetupx86.msi et les AgentSetupx64.msi, sont disponibles pour chaque architecture.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-175">Windows Installer Files versions, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="ebbcf-176">Pour désinstaller l’agent UE-V ultérieurement à l’aide du fichier d’installation, vous devez utiliser le même type de fichier.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-176">To uninstall the UE-V Agent at a later time using the installation file, you must use the same file type.</span></span>

     

2.  <span data-ttu-id="ebbcf-177">Utilisez l’une des commandes PowerShell suivantes pour installer l’agent.</span><span class="sxs-lookup"><span data-stu-id="ebbcf-177">Use one of the following PowerShell commands to install the agent.</span></span>

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

## <span data-ttu-id="ebbcf-178">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ebbcf-178">Related topics</span></span>


[<span data-ttu-id="ebbcf-179">Gestion de l'agent UE-V1.0 et des packages avec PowerShell et WMI</span><span class="sxs-lookup"><span data-stu-id="ebbcf-179">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

[<span data-ttu-id="ebbcf-180">Administration d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="ebbcf-180">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="ebbcf-181">Opérations d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="ebbcf-181">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





