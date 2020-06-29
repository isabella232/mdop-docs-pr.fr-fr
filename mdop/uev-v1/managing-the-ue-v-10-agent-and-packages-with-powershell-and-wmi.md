---
title: Gestion de l'agent UE-V1.0 et des packages avec PowerShell et WMI
description: Gestion de l'agent UE-V1.0 et des packages avec PowerShell et WMI
author: dansimp
ms.assetid: c8989b01-1769-4e69-82b1-4aadb261d2d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79268e3384aaaf08bdd4e9b92d74b039ce96596a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807850"
---
# <span data-ttu-id="f3613-103">Gestion de l'agent UE-V1.0 et des packages avec PowerShell et WMI</span><span class="sxs-lookup"><span data-stu-id="f3613-103">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>


<span data-ttu-id="f3613-104">Vous pouvez utiliser WMI et PowerShell pour gérer le comportement de la synchronisation et de la synchronisation de l’agent utilisateur de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f3613-104">You can use WMI and PowerShell to manage Microsoft User Experience Virtualization (UE-V) Agent configuration and synchronization behavior.</span></span>

**<span data-ttu-id="f3613-105">Déploiement de l’agent UE-V avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3613-105">How to deploy the UE-V agent with PowerShell</span></span>**

1.  <span data-ttu-id="f3613-106">Copiez le fichier du programme d’installation d’UE-V dans un partage réseau accessible.</span><span class="sxs-lookup"><span data-stu-id="f3613-106">Stage the UE-V installer file in an accessible network share.</span></span>

    **<span data-ttu-id="f3613-107">Remarque</span><span class="sxs-lookup"><span data-stu-id="f3613-107">Note</span></span>**  
    <span data-ttu-id="f3613-108">Utilisez AgentSetup.exe pour déployer à la fois les versions 32 bits et 64 bits de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="f3613-108">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="f3613-109">Les versions des fichiers du programme d’installation Windows, AgentSetupx86.msi et les AgentSetupx64.msi, sont disponibles pour chaque architecture.</span><span class="sxs-lookup"><span data-stu-id="f3613-109">Windows Installer Files versions, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="f3613-110">Pour désinstaller l’agent UE-V ultérieurement à l’aide du fichier d’installation, vous devez utiliser le même type de fichier.</span><span class="sxs-lookup"><span data-stu-id="f3613-110">To uninstall the UE-V Agent at a later time using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="f3613-111">Utilisez l’une des commandes PowerShell suivantes pour installer l’agent.</span><span class="sxs-lookup"><span data-stu-id="f3613-111">Use one of the following PowerShell commands to install the agent.</span></span>

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**<span data-ttu-id="f3613-112">Configurer l’agent UE-V avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3613-112">How to configure the UE-V Agent with PowerShell</span></span>**

1.  <span data-ttu-id="f3613-113">Utilisez un compte disposant de droits d’administrateur pour ouvrir une fenêtre PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f3613-113">Use an account with administrator rights to open a PowerShell window.</span></span> <span data-ttu-id="f3613-114">Importez le module PowerShell UE-V à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="f3613-114">Import the UE-V PowerShell module by using the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="f3613-115">Utilisez les commandes PowerShell suivantes pour configurer l’agent.</span><span class="sxs-lookup"><span data-stu-id="f3613-115">Use the following PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="f3613-116">Commande PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3613-116">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="f3613-117">Description</span><span class="sxs-lookup"><span data-stu-id="f3613-117">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-118">Get-UevConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3613-118">Get-UevConfiguration</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="f3613-119">Afficher les paramètres d’agent UE-V effectifs.</span><span class="sxs-lookup"><span data-stu-id="f3613-119">View the effective UE-V agent settings.</span></span> <span data-ttu-id="f3613-120">Les paramètres spécifiques à l’utilisateur sont prioritaires sur les paramètres de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3613-120">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-121">Get-UevConfiguration-CurrentComputerUser</span><span class="sxs-lookup"><span data-stu-id="f3613-121">Get-UevConfiguration - CurrentComputerUser</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="f3613-122">Afficher les valeurs des paramètres de l’agent UE-V pour l’utilisateur actuel uniquement.</span><span class="sxs-lookup"><span data-stu-id="f3613-122">View the UE-V agent settings values for the current user only.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-123">Get-UevConfiguration-Computer</span><span class="sxs-lookup"><span data-stu-id="f3613-123">Get-UevConfiguration -Computer</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-124">Affichez les valeurs des paramètres de configuration de l’agent UE-V pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3613-124">View the UE-V agent configuration settings values for all users on the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-125">Set-UevConfiguration-Computer-SettingsStoragePath &lt; path to _settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-125">Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-126">Définir un emplacement de stockage des paramètres par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3613-126">Define a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-127">Set-UevConfiguration-CurrentComputerUser-SettingsStoragePath &lt; path to _settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-127">Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-128">Définir un emplacement de stockage des paramètres par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f3613-128">Define a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-129">Set-UevConfiguration-Computer-SyncTimeoutInMilliseconds &lt; délai d’expiration en millisecondes&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-129">Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-130">Définissez le délai de synchronisation en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="f3613-130">Set the synchronization timeout in milliseconds</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-131">Set-UevConfiguration-CurrentComputerUser-SyncTimeoutInMilliseconds &lt; délai en millisecondes&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-131">Set-UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-132">Définissez le délai de synchronisation de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="f3613-132">Set the synchronization timeout for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-133">Set-UevConfiguration-Computer-MaxPackageSizeInBytes &lt; taille en octets&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-133">Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-134">Configurer l’agent UE-V pour signaler l’arrivée d’un seuil défini pour la taille du fichier de package de paramètres.</span><span class="sxs-lookup"><span data-stu-id="f3613-134">Configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="f3613-135">Définissez la taille du package seuil en octets.</span><span class="sxs-lookup"><span data-stu-id="f3613-135">Set the threshold package size in bytes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-136">Set-UevConfiguration-CurrentComputerUser-MaxPackageSizeInBytes &lt; taille en octets&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-136">Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-137">Définissez le seuil d’avertissement de taille de package pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="f3613-137">Set the package size warning threshold for the current user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-138">Set-UevConfiguration-Computer-SettingsTemplateCatalogPath &lt; path to Catalog&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-138">Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-139">Définissez le chemin du catalogue de modèles de paramètres.</span><span class="sxs-lookup"><span data-stu-id="f3613-139">Set the settings template catalog path.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-140">Set-UevConfiguration-Computer-PowerSchool &lt; Method Sync&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-140">Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-141">Définissez la méthode de synchronisation: OfflineFiles ou aucune.</span><span class="sxs-lookup"><span data-stu-id="f3613-141">Set the synchronization method: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-142">Set-UevConfiguration-CurrentComputerUser-PowerSchool &lt; méthode de synchronisation&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-142">Set-UevConfiguration -CurrentComputerUser -SyncMethod &lt;sync method&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-143">Définissez la méthode de synchronisation de l’utilisateur actuel: OfflineFiles ou aucune.</span><span class="sxs-lookup"><span data-stu-id="f3613-143">Set the synchronization method for the current user: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-144">Set-UEVConfiguration-Computer-EnableSettingsImportNotify</span><span class="sxs-lookup"><span data-stu-id="f3613-144">Set-UEVConfiguration -Computer –EnableSettingsImportNotify</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-145">Activez la notification de déclenchement lorsque l’importation des paramètres utilisateur est retardée.</span><span class="sxs-lookup"><span data-stu-id="f3613-145">Enable notification to occur when the import of user settings is delayed.</span></span></p>
    <p><span data-ttu-id="f3613-146">Utilisez – DisableSettingsImportNotify pour désactiver la notification.</span><span class="sxs-lookup"><span data-stu-id="f3613-146">Use –DisableSettingsImportNotify to disable notification.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-147">Set-UEVConfiguration-CurrentComputerUser-EnableSettingsImportNotify</span><span class="sxs-lookup"><span data-stu-id="f3613-147">Set-UEVConfiguration - CurrentComputerUser -EnableSettingsImportNotify</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-148">Activez la notification pour l’utilisateur actuel lorsque l’importation des paramètres utilisateur est retardée.</span><span class="sxs-lookup"><span data-stu-id="f3613-148">Enable notification for the current user when the import of user settings is delayed.</span></span></p>
    <p><span data-ttu-id="f3613-149">Utilisez – DisableSettingsImportNotify pour désactiver la notification.</span><span class="sxs-lookup"><span data-stu-id="f3613-149">Use –DisableSettingsImportNotify to disable notification.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-150">Set-UEVConfiguration-Computer-SettingsImportNotifyDelayInSeconds</span><span class="sxs-lookup"><span data-stu-id="f3613-150">Set-UEVConfiguration -Computer -SettingsImportNotifyDelayInSeconds</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-151">Spécifier la durée en secondes avant la notification de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="f3613-151">Specify the time in seconds before the user is notified</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-152">Set-UEVConfiguration-CurrentComputerUser-SettingsImportNotifyDelayInSeconds</span><span class="sxs-lookup"><span data-stu-id="f3613-152">Set-UEVConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-153">Spécifiez la durée en secondes avant la notification de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="f3613-153">Specify the time in seconds before notification for the current user.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-154">Set-UevConfiguration-Computer-DisableSync</span><span class="sxs-lookup"><span data-stu-id="f3613-154">Set-UevConfiguration –Computer –DisableSync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-155">Désactivez UE-V pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3613-155">Disable UE-V for all the users on the computer.</span></span></p>
    <p><span data-ttu-id="f3613-156">Utilisez – EnableSync pour activer ou réactiver.</span><span class="sxs-lookup"><span data-stu-id="f3613-156">Use –EnableSync to enable or re-enable.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-157">Set-UevConfiguration-CurrentComputerUser-DisableSync</span><span class="sxs-lookup"><span data-stu-id="f3613-157">Set-UevConfiguration –CurrentComputerUser -DisableSync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-158">Désactivez UE-V pour l’utilisateur actuel sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3613-158">Disable UE-V for the current user on the computer.</span></span></p>
    <p><span data-ttu-id="f3613-159">Utilisez – EnableSync pour activer ou réactiver.</span><span class="sxs-lookup"><span data-stu-id="f3613-159">Use –EnableSync to enable or re-enable.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-160">Clear-UevConfiguration – nom de l’ordinateur- &lt; paramètre&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-160">Clear-UevConfiguration –Computer -&lt;setting name&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-161">Effacez un paramètre spécifique pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3613-161">Clear a specific setting for all users on the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-162">Clear-UevConfiguration-CurrentComputerUser- &lt; Setting Name&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-162">Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-163">Effacer un paramètre spécifique pour l’utilisateur actuel uniquement.</span><span class="sxs-lookup"><span data-stu-id="f3613-163">Clear a specific setting for the current user only.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-164">Fichier de migration des paramètres d’export-UevConfiguration &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-164">Export-UevConfiguration &lt;settings migration file&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-165">Exportez la configuration d’ordinateur UE-V vers un fichier de migration des paramètres.</span><span class="sxs-lookup"><span data-stu-id="f3613-165">Export the UE-V computer configuration to a settings migration file.</span></span> <span data-ttu-id="f3613-166">L’extension du fichier doit être «. UEV».</span><span class="sxs-lookup"><span data-stu-id="f3613-166">The extension of the file must be “.uev”.</span></span></p>
    <p><span data-ttu-id="f3613-167">La cmdlet Export exporte tous les paramètres d’agent UE-V qui peuvent être configurés avec le paramètre-Computer.</span><span class="sxs-lookup"><span data-stu-id="f3613-167">The export cmdlet exports all UE-V agent settings that are configurable with the -computer parameter.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-168">Fichier de migration des paramètres d’importation-UevConfiguration &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-168">Import-UevConfiguration &lt;settings migration file&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-169">Importez la configuration d’ordinateur UE-V à partir d’un fichier de migration des paramètres (fichier. UEV).</span><span class="sxs-lookup"><span data-stu-id="f3613-169">Import the UE-V computer configuration from a settings migration file (.uev file).</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="f3613-170">Exporter les paramètres de package UE-V et réparer les modèles UE-V avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3613-170">How to export UE-V package settings and repair UE-V templates with PowerShell</span></span>**

1.  <span data-ttu-id="f3613-171">Ouvrez une fenêtre PowerShell en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="f3613-171">Open a PowerShell window as an Administrator.</span></span> <span data-ttu-id="f3613-172">Importez le module PowerShell UE-V à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="f3613-172">Import the UE-V PowerShell module with the following command.</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="f3613-173">Utilisez les commandes PowerShell suivantes pour configurer l’agent.</span><span class="sxs-lookup"><span data-stu-id="f3613-173">Use the following PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="f3613-174">Commande PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3613-174">PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="f3613-175">Description</span><span class="sxs-lookup"><span data-stu-id="f3613-175">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-176">Export-UevPackage MicrosoftCalculator6. pkgx</span><span class="sxs-lookup"><span data-stu-id="f3613-176">Export-UevPackage MicrosoftCalculator6.pkgx</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-177">Extrait les paramètres d’un fichier de Microsoft Calculator et les convertit dans un format lisible par l’utilisateur dans XML.</span><span class="sxs-lookup"><span data-stu-id="f3613-177">Extracts the settings from a Microsoft Calculator package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-178">Réparation-UevTemplateIndex</span><span class="sxs-lookup"><span data-stu-id="f3613-178">Repair-UevTemplateIndex</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-179">Répare l’index des modèles d’emplacement des paramètres UE-V.</span><span class="sxs-lookup"><span data-stu-id="f3613-179">Repairs the index of the UE-V settings location templates.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="f3613-180">Configurer l’agent UE-V avec WMI</span><span class="sxs-lookup"><span data-stu-id="f3613-180">How to configure the UE-V Agent with WMI</span></span>**

1.  <span data-ttu-id="f3613-181">La virtualisation de l’interface utilisateur fournit l’ensemble des commandes WMI suivantes.</span><span class="sxs-lookup"><span data-stu-id="f3613-181">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="f3613-182">Les administrateurs peuvent utiliser cette interface pour configurer l’agent UE-V à partir de la ligne de commande et automatiser les tâches de configuration typiques.</span><span class="sxs-lookup"><span data-stu-id="f3613-182">Administrators can use this interface to configure the UE-V agent from the command line and automate typical configuration tasks.</span></span>

    <span data-ttu-id="f3613-183">Utilisez un compte disposant de droits d’administrateur pour ouvrir une fenêtre PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f3613-183">Use an account with administrator rights to open a PowerShell window.</span></span>

2.  <span data-ttu-id="f3613-184">Utilisez les commandes WMI suivantes pour configurer l’agent.</span><span class="sxs-lookup"><span data-stu-id="f3613-184">Use the following WMI commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="f3613-185">Commande PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3613-185">PowerShell command</span></span></th>
    <th align="left"><span data-ttu-id="f3613-186">Description</span><span class="sxs-lookup"><span data-stu-id="f3613-186">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-187">Get-WmiObject-espace de noms root\Microsoft\UEV</span><span class="sxs-lookup"><span data-stu-id="f3613-187">Get-WmiObject -Namespace root\Microsoft\UEV Configuration</span></span></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="f3613-188">Afficher les paramètres d’agent UE-V actifs.</span><span class="sxs-lookup"><span data-stu-id="f3613-188">View the active UE-V agent settings.</span></span> <span data-ttu-id="f3613-189">Les paramètres spécifiques à l’utilisateur sont prioritaires sur les paramètres de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3613-189">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-190">Get-WmiObject-namespace root\Microsoft\UEV UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3613-190">Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-191">Affichez la configuration de l’agent UE-V définie pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f3613-191">View the UE-V agent configuration that is defined for user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-192">Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3613-192">Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-193">Affichez la configuration de l’agent UE-V définie pour l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3613-193">View the UE-V agent configuration that is defined for computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-194">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3613-194">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="f3613-195">$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-195">$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</span></span></p>
    <p><span data-ttu-id="f3613-196">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="f3613-196">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-197">Définir un emplacement de stockage des paramètres par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f3613-197">Define a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-198">$config = Get-WmiObject-namespace root\Microsoft\UEV UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3613-198">$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</span></span></p>
    <p><span data-ttu-id="f3613-199">$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-199">$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</span></span></p>
    <p><span data-ttu-id="f3613-200">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="f3613-200">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-201">Définir un emplacement de stockage des paramètres par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f3613-201">Define a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-202">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3613-202">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="f3613-203">$config. SyncTimeoutInMilliseconds = &lt; timeout_in_milliseconds&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-203">$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</span></span></p>
    <p><span data-ttu-id="f3613-204">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="f3613-204">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-205">Définissez le délai de synchronisation en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="f3613-205">Set the synchronization timeout in milliseconds.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-206">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3613-206">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="f3613-207">$config. MaxPackageSizeInBytes = &lt; size_in_bytes&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-207">$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</span></span></p>
    <p><span data-ttu-id="f3613-208">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="f3613-208">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-209">Configurer l’agent UE-V pour signaler l’arrivée d’un seuil défini pour la taille du fichier de package de paramètres.</span><span class="sxs-lookup"><span data-stu-id="f3613-209">Configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="f3613-210">Définissez la taille de fichier du package seuil en octets.</span><span class="sxs-lookup"><span data-stu-id="f3613-210">Set the threshold package file size in bytes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-211">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3613-211">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="f3613-212">$config. PowerSchool = &lt; sync_method&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-212">$config.SyncMethod = &lt;sync_method&gt;</span></span></p>
    <p><span data-ttu-id="f3613-213">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="f3613-213">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-214">Définissez la méthode de synchronisation: OfflineFiles ou aucune.</span><span class="sxs-lookup"><span data-stu-id="f3613-214">Set the synchronization method: OfflineFiles or None.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="f3613-215">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3613-215">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="f3613-216">$config. &lt; valeur du &gt;  =  &lt; paramètre Name Setting&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-216">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><span data-ttu-id="f3613-217">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="f3613-217">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-218">Mettre à jour un paramètre par ordinateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="f3613-218">Update a specific per-computer setting.</span></span> <span data-ttu-id="f3613-219">Pour effacer ce paramètre, utilisez $null comme valeur de paramètre.</span><span class="sxs-lookup"><span data-stu-id="f3613-219">To clear the setting, use $null as the setting value.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="f3613-220">$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3613-220">$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</span></span></p>
    <p><span data-ttu-id="f3613-221">$config. &lt; valeur du &gt;  =  &lt; paramètre Name Setting&gt;</span><span class="sxs-lookup"><span data-stu-id="f3613-221">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><span data-ttu-id="f3613-222">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="f3613-222">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="f3613-223">Mettre à jour un paramètre par utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="f3613-223">Update a specific per-user setting.</span></span> <span data-ttu-id="f3613-224">Pour effacer ce paramètre, utilisez $null comme valeur de paramètre.</span><span class="sxs-lookup"><span data-stu-id="f3613-224">To clear the setting, use $null as the setting value.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and PowerShell, the defined configuration is stored in the registry in the following locations:

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

## <span data-ttu-id="f3613-225">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3613-225">Related topics</span></span>


[<span data-ttu-id="f3613-226">Administration d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="f3613-226">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="f3613-227">Opérations d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="f3613-227">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)









