---
title: Gestion de l’agent UE-V 2. x et des packages avec Windows PowerShell et WMI
description: Gestion de l’agent UE-V 2. x et des packages avec Windows PowerShell et WMI
author: dansimp
ms.assetid: 56e6780b-8b2c-4717-91c8-2af63062ab75
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6a709d2c66266cf33b8e89ddd905aa0f21eb7dfe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811975"
---
# <span data-ttu-id="c54fa-103">Gestion de l’agent UE-V 2. x et des packages avec Windows PowerShell et WMI</span><span class="sxs-lookup"><span data-stu-id="c54fa-103">Managing the UE-V 2.x Agent and Packages with Windows PowerShell and WMI</span></span>


<span data-ttu-id="c54fa-104">Vous pouvez utiliser WMI (Windows Management Instrumentation) et Windows PowerShell pour gérer les comportements de synchronisation et de configuration de l’interface utilisateur de Microsoft (UE-V) 2,0, 2,1 et 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="c54fa-104">You can use Windows Management Instrumentation (WMI) and Windows PowerShell to manage Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Agent configuration and synchronization behavior.</span></span> <span data-ttu-id="c54fa-105">Pour obtenir la liste complète des cmdlets PowerShell d’UE-V, voir [référence sur l’applet de passe UE-v 2](https://go.microsoft.com/fwlink/?LinkId=393495) ( https://go.microsoft.com/fwlink/?LinkId=393495) .</span><span class="sxs-lookup"><span data-stu-id="c54fa-105">For a complete list of UE-V PowerShell cmdlets, see [UE-V 2 Cmdlet Reference](https://go.microsoft.com/fwlink/?LinkId=393495) (https://go.microsoft.com/fwlink/?LinkId=393495).</span></span>

**<span data-ttu-id="c54fa-106">Pour déployer l’agent UE-V à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c54fa-106">To deploy the UE-V Agent by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="c54fa-107">Copiez le fichier du programme d’installation d’UE-V dans un partage réseau accessible.</span><span class="sxs-lookup"><span data-stu-id="c54fa-107">Stage the UE-V installer file in an accessible network share.</span></span>

    **<span data-ttu-id="c54fa-108">Remarque</span><span class="sxs-lookup"><span data-stu-id="c54fa-108">Note</span></span>**  
    <span data-ttu-id="c54fa-109">Utilisez AgentSetup.exe pour déployer à la fois les versions 32 bits et 64 bits de l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="c54fa-109">Use AgentSetup.exe to deploy both 32-bit and 64-bit versions of the UE-V Agent.</span></span> <span data-ttu-id="c54fa-110">Les packages Windows Installer, AgentSetupx86.msi et AgentSetupx64.msi, sont disponibles pour chaque architecture.</span><span class="sxs-lookup"><span data-stu-id="c54fa-110">Windows Installer packages, AgentSetupx86.msi and AgentSetupx64.msi, are available for each architecture.</span></span> <span data-ttu-id="c54fa-111">Pour désinstaller l’agent UE-V ultérieurement à l’aide du fichier d’installation, vous devez utiliser le même type de fichier.</span><span class="sxs-lookup"><span data-stu-id="c54fa-111">To uninstall the UE-V Agent at a later time by using the installation file, you must use the same file type.</span></span>



2.  <span data-ttu-id="c54fa-112">Utilisez l’une des commandes Windows PowerShell suivantes pour installer l’agent UE-V.</span><span class="sxs-lookup"><span data-stu-id="c54fa-112">Use one of the following Windows PowerShell commands to install the UE-V Agent.</span></span>

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**<span data-ttu-id="c54fa-113">Pour configurer l’agent UE-V à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c54fa-113">To configure the UE-V Agent by using Windows PowerShell</span></span>**

1. <span data-ttu-id="c54fa-114">Ouvrez une fenêtre Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c54fa-114">Open a Windows PowerShell window.</span></span> <span data-ttu-id="c54fa-115">Pour gérer les paramètres d’ordinateur qui affectent tous les utilisateurs de l’ordinateur à l’aide du paramètre *ordinateur* , ouvrez la fenêtre avec un compte disposant de droits d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-115">To manage computer settings that affect all users of the computer by using the *Computer* parameter, open the window with an account that has administrator rights.</span></span>

2. <span data-ttu-id="c54fa-116">Utilisez les commandes Windows PowerShell suivantes pour configurer l’agent.</span><span class="sxs-lookup"><span data-stu-id="c54fa-116">Use the following Windows PowerShell commands to configure the agent.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="c54fa-117">Commande de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c54fa-117">Windows PowerShell command</span></span></th>
   <th align="left"><span data-ttu-id="c54fa-118">Description</span><span class="sxs-lookup"><span data-stu-id="c54fa-118">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration</code></p>
   <p></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-119">Obtient les paramètres d’agent UE-V effectifs.</span><span class="sxs-lookup"><span data-stu-id="c54fa-119">Gets the effective UE-V Agent settings.</span></span> <span data-ttu-id="c54fa-120">Les paramètres spécifiques à l’utilisateur sont prioritaires sur les paramètres de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-120">User-specific settings have precedence over the computer settings.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration - CurrentComputerUser</code></p>
   <p></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-121">Obtient les valeurs des paramètres de l’agent UE-V pour l’utilisateur actuel uniquement.</span><span class="sxs-lookup"><span data-stu-id="c54fa-121">Gets the UE-V Agent settings values for the current user only.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration -Computer</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-122">Obtient les valeurs des paramètres de configuration de l’agent UE-V pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-122">Gets the UE-V Agent configuration settings values for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration -Details</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-123">Obtient les détails pour chaque paramètre de configuration.</span><span class="sxs-lookup"><span data-stu-id="c54fa-123">Gets the details for each configuration setting.</span></span> <span data-ttu-id="c54fa-124">Affiche l’emplacement de configuration du paramètre ou s’il utilise la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="c54fa-124">Displays where the setting is configured or if it uses the default value.</span></span> <span data-ttu-id="c54fa-125">Est affiché si le paramètre actuel est valide.</span><span class="sxs-lookup"><span data-stu-id="c54fa-125">Is displayed if the current setting is valid.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –ContactITDescription &lt;IT description&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-126">Définit le texte qui s’affiche dans le centre de paramètres de société pour le lien aide.</span><span class="sxs-lookup"><span data-stu-id="c54fa-126">Sets the text that is displayed in the Company Settings Center for the help link.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -ContactITUrl &lt;string&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-127">Définit l’URL du lien dans le Centre des paramètres de société pour le lien aide.</span><span class="sxs-lookup"><span data-stu-id="c54fa-127">Sets the URL of the link in the Company Settings Center for the help link.</span></span> <span data-ttu-id="c54fa-128">Tout protocole d’URL peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="c54fa-128">Any URL protocol can be used.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-129">Configure l’agent UE-V de façon à ce qu’il ne synchronise aucune application Windows pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-129">Configures the UE-V Agent to not synchronize any Windows apps for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser – EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-130">Configure l’agent UE-V de façon à ce qu’il ne synchronise aucune application Windows pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="c54fa-130">Configures the UE-V Agent to not synchronize any Windows apps for the current computer user.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableFirstUseNotification</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-131">Configure l’agent UE-V pour afficher les notifications lors du premier démarrage de l’agent pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-131">Configures the UE-V Agent to display notification the first time the agent runs for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer –DisableFirstUseNotification</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-132">Configure l’agent UE-V de façon à ne pas afficher les notifications lors de la première exécution de l’agent pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-132">Configures the UE-V Agent to not display notification the first time that the agent runs for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSettingsImportNotify</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-133">Configure l’agent UE-V pour informer tous les utilisateurs sur l’ordinateur lorsque la synchronisation des paramètres est retardée.</span><span class="sxs-lookup"><span data-stu-id="c54fa-133">Configures the UE-V Agent to notify all users on the computer when settings synchronization is delayed.</span></span></p>
   <p><span data-ttu-id="c54fa-134">Utilisez le <em> </em> paramètre DisableSettingsImportNotify pour désactiver la notification.</span><span class="sxs-lookup"><span data-stu-id="c54fa-134">Use the <em>DisableSettingsImportNotify</em> parameter to disable notification.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -EnableSettingsImportNotify</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-135">Configure l’agent UE-V pour informer l’utilisateur actuel lorsque la synchronisation des paramètres est retardée.</span><span class="sxs-lookup"><span data-stu-id="c54fa-135">Configures the UE-V Agent to notify the current user when settings synchronization is delayed.</span></span></p>
   <p><span data-ttu-id="c54fa-136">Utilisez le <em> </em> paramètre DisableSettingsImportNotify pour désactiver la notification.</span><span class="sxs-lookup"><span data-stu-id="c54fa-136">Use the <em>DisableSettingsImportNotify</em> parameter to disable notification.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-137">Configure l’agent UE-V pour synchroniser toutes les applications Windows qui ne sont pas explicitement désactivées par la liste des applications Windows pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-137">Configures the UE-V Agent to synchronize all Windows apps that are not explicitly disabled by the Windows app list for all users of the computer.</span></span> <span data-ttu-id="c54fa-138">Pour plus d’informations, reportez-vous à la rubrique &quot; Get-UevAppxPackage &quot; dans <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Managing-V 2. x modèles d’emplacement des paramètres à l’aide de Windows PowerShell et WMI </a> .</span><span class="sxs-lookup"><span data-stu-id="c54fa-138">For more information, see &quot;Get-UevAppxPackage&quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</a>.</span></span></p>
   <p><span data-ttu-id="c54fa-139">Utilisez le <em> </em> paramètre DisableSyncUnlistedWindows8Apps pour configurer l’agent UE-V de façon à ce qu’il synchronise uniquement les applications Windows activées explicitement par la liste des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="c54fa-139">Use the <em>DisableSyncUnlistedWindows8Apps</em> parameter to configure the UE-V Agent to synchronize only Windows apps that are explicitly enabled by the Windows App List.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser - EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-140">Configure l’agent UE-V pour synchroniser toutes les applications Windows qui ne sont pas explicitement désactivées par la liste des applications Windows pour l’utilisateur actuel sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-140">Configures the UE-V Agent to synchronize all Windows apps that are not explicitly disabled by the Windows app list for the current user on the computer.</span></span> <span data-ttu-id="c54fa-141">Pour plus d’informations, reportez-vous à la rubrique &quot; Get-UevAppxPackage &quot; dans <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Managing-V 2. x modèles d’emplacement des paramètres à l’aide de Windows PowerShell et WMI </a> .</span><span class="sxs-lookup"><span data-stu-id="c54fa-141">For more information, see &quot;Get-UevAppxPackage&quot; in <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)">Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI</a>.</span></span></p>
   <p><span data-ttu-id="c54fa-142">Utilisez le <em> </em> paramètre DisableSyncUnlistedWindows8Apps pour configurer l’agent UE-V de façon à ce qu’il synchronise uniquement les applications Windows activées explicitement par la liste des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="c54fa-142">Use the <em>DisableSyncUnlistedWindows8Apps</em> parameter to configure the UE-V Agent to synchronize only Windows apps that are explicitly enabled by the Windows App List.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration –Computer –DisableSync</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-143">Désactive UE-V pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-143">Disables UE-V for all the users on the computer.</span></span></p>
   <p><span data-ttu-id="c54fa-144">Utilisez le <em> </em> paramètre EnableSync pour activer ou réactiver.</span><span class="sxs-lookup"><span data-stu-id="c54fa-144">Use the <em>EnableSync</em> parameter to enable or re-enable.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –CurrentComputerUser -DisableSync</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-145">Désactive UE-V pour l’utilisateur actuel sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-145">Disables UE-V for the current user on the computer.</span></span></p>
   <p><span data-ttu-id="c54fa-146">Utilisez le <em> </em> paramètre EnableSync pour activer ou réactiver.</span><span class="sxs-lookup"><span data-stu-id="c54fa-146">Use the <em>EnableSync</em> parameter to enable or re-enable.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableTrayIcon</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-147">Active l’icône UE-V dans la zone de notification pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-147">Enables the UE-V icon in the notification area for all users of the computer.</span></span></p>
   <p><span data-ttu-id="c54fa-148">Utilisez le <em> </em> paramètre DisableTrayIcon pour désactiver l’icône.</span><span class="sxs-lookup"><span data-stu-id="c54fa-148">Use the <em>DisableTrayIcon</em> parameter to disable the icon.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-149">Configure l’agent UE-V pour signaler qu’une taille de fichier de package de paramètres atteint le seuil défini pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-149">Configures the UE-V agent to report when a settings package file size reaches the defined threshold for all users on the computer.</span></span> <span data-ttu-id="c54fa-150">Définit la taille du package seuil en octets.</span><span class="sxs-lookup"><span data-stu-id="c54fa-150">Sets the threshold package size in bytes.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-151">Configure l’agent UE-V pour signaler l’arrivée d’un fichier de package de paramètres au seuil défini.</span><span class="sxs-lookup"><span data-stu-id="c54fa-151">Configures the UE-V agent to report when a settings package file size reaches the defined threshold.</span></span> <span data-ttu-id="c54fa-152">Définit le seuil d’avertissement de taille de package pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="c54fa-152">Sets the package size warning threshold for the current user.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-153">Spécifie la durée en secondes avant la notification de l’utilisateur pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-153">Specifies the time in seconds before the user is notified for all users of the computer</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-154">Spécifie la durée en secondes avant l’envoi de la notification à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="c54fa-154">Specifies the time in seconds before notification for the current user is sent.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-155">Définit l’emplacement de stockage des paramètres par ordinateur pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-155">Defines a per-computer settings storage location for all users of the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-156">Définit un emplacement de stockage des paramètres par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-156">Defines a per-user settings storage location.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-157">Définit le chemin du catalogue de modèles de paramètres pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-157">Sets the settings template catalog path for all users of the computer.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-158">Définit la méthode de synchronisation de tous les utilisateurs de l’ordinateur: SyncProvider ou aucune.</span><span class="sxs-lookup"><span data-stu-id="c54fa-158">Sets the synchronization method for all users of the computer: SyncProvider or None.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser  -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-159">Définit la méthode de synchronisation pour l’utilisateur actuel: SyncProvider ou aucune.</span><span class="sxs-lookup"><span data-stu-id="c54fa-159">Sets the synchronization method for the current user: SyncProvider or None.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-160">Définit le délai d’expiration de la synchronisation en millisecondes pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-160">Sets the synchronization time-out in milliseconds for all users of the computer</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set- UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-161">Définissez le délai de synchronisation pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="c54fa-161">Set the synchronization time-out for the current user.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Clear-UevConfiguration –Computer -&lt;setting name&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-162">Efface le paramètre spécifié pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-162">Clears the specified setting for all users on the computer.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-163">Efface le paramètre spécifié pour l’utilisateur actuel uniquement.</span><span class="sxs-lookup"><span data-stu-id="c54fa-163">Clears the specified setting for the current user only.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Export-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-164">Exporte la configuration de l’ordinateur UE-V vers un fichier de migration des paramètres.</span><span class="sxs-lookup"><span data-stu-id="c54fa-164">Exports the UE-V computer configuration to a settings migration file.</span></span> <span data-ttu-id="c54fa-165">L’extension de nom de fichier doit être. UEV.</span><span class="sxs-lookup"><span data-stu-id="c54fa-165">The file name extension must be .uev.</span></span></p>
   <p><span data-ttu-id="c54fa-166">L' <code>Export</code> applet de passe exporte tous les paramètres d’agent UE-V qui peuvent être configurés avec le <em> </em> paramètre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-166">The <code>Export</code> cmdlet exports all UE-V Agent settings that are configurable with the <em>Computer</em> parameter.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Import-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p><span data-ttu-id="c54fa-167">Importe la configuration de l’ordinateur UE-V à partir d’un fichier de migration des paramètres.</span><span class="sxs-lookup"><span data-stu-id="c54fa-167">Imports the UE-V computer configuration from a settings migration file.</span></span> <span data-ttu-id="c54fa-168">L’extension de nom de fichier doit être. UEV.</span><span class="sxs-lookup"><span data-stu-id="c54fa-168">The file name extension must be .uev.</span></span></p></td>
   </tr>
   </tbody>
   </table>



**<span data-ttu-id="c54fa-169">Pour exporter des paramètres de package UE-V et réparer des modèles UE-V à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c54fa-169">To export UE-V package settings and repair UE-V templates by using Windows PowerShell</span></span>**

1.  <span data-ttu-id="c54fa-170">Ouvrez une fenêtre Windows PowerShell en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-170">Open a Windows PowerShell window as an administrator.</span></span>

2.  <span data-ttu-id="c54fa-171">Utilisez les commandes Windows PowerShell suivantes pour configurer l’agent.</span><span class="sxs-lookup"><span data-stu-id="c54fa-171">Use the following Windows PowerShell commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="c54fa-172">Commande de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c54fa-172">Windows PowerShell command</span></span></strong></p></td>
    <td align="left"><p><strong><span data-ttu-id="c54fa-173">Description</span><span class="sxs-lookup"><span data-stu-id="c54fa-173">Description</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="c54fa-174">Export-UevPackage MicrosoftCalculator6. pkgx</span><span class="sxs-lookup"><span data-stu-id="c54fa-174">Export-UevPackage MicrosoftCalculator6.pkgx</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-175">Extrait les paramètres d’un fichier de Microsoft Calculator et les convertit dans un format lisible par l’utilisateur dans XML.</span><span class="sxs-lookup"><span data-stu-id="c54fa-175">Extracts the settings from a Microsoft Calculator package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="c54fa-176">Réparation-UevTemplateIndex</span><span class="sxs-lookup"><span data-stu-id="c54fa-176">Repair-UevTemplateIndex</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-177">Répare l’index des modèles d’emplacement des paramètres UE-V.</span><span class="sxs-lookup"><span data-stu-id="c54fa-177">Repairs the index of the UE-V settings location templates.</span></span></p></td>
    </tr>
    </tbody>
    </table>



**<span data-ttu-id="c54fa-178">Pour configurer l’agent UE-V à l’aide de WMI</span><span class="sxs-lookup"><span data-stu-id="c54fa-178">To configure the UE-V Agent by using WMI</span></span>**

1.  <span data-ttu-id="c54fa-179">La virtualisation de l’interface utilisateur fournit l’ensemble des commandes WMI suivantes.</span><span class="sxs-lookup"><span data-stu-id="c54fa-179">User Experience Virtualization provides the following set of WMI commands.</span></span> <span data-ttu-id="c54fa-180">Les administrateurs peuvent utiliser cette interface pour configurer l’agent UE-V au niveau de la ligne de commande et automatiser les tâches de configuration typiques.</span><span class="sxs-lookup"><span data-stu-id="c54fa-180">Administrators can use this interface to configure the UE-V agent at the command line and automate typical configuration tasks.</span></span>

    <span data-ttu-id="c54fa-181">Utilisez un compte disposant de droits d’administrateur pour ouvrir une fenêtre Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c54fa-181">Use an account with administrator rights to open a Windows PowerShell window.</span></span>

2.  <span data-ttu-id="c54fa-182">Utilisez les commandes WMI suivantes pour configurer l’agent.</span><span class="sxs-lookup"><span data-stu-id="c54fa-182">Use the following WMI commands to configure the agent.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>Windows PowerShell command</code></th>
    <th align="left"><span data-ttu-id="c54fa-183">Description</span><span class="sxs-lookup"><span data-stu-id="c54fa-183">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV Configuration</code></p>
    <p></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-184">Affiche les paramètres d’agent UE-V actifs.</span><span class="sxs-lookup"><span data-stu-id="c54fa-184">Displays the active UE-V Agent settings.</span></span> <span data-ttu-id="c54fa-185">Les paramètres spécifiques à l’utilisateur sont prioritaires sur les paramètres de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-185">User-specific settings have precedence over the computer settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-186">Affiche la configuration de l’agent UE-V définie pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-186">Displays the UE-V Agent configuration that is defined for a user.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-187">Affiche la configuration de l’agent UE-V définie pour un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-187">Displays the UE-V Agent configuration that is defined for a computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject –Namespace root\Microsoft\Uev ConfigurationItem</code></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-188">Affiche les détails de chaque élément de configuration.</span><span class="sxs-lookup"><span data-stu-id="c54fa-188">Displays the details for each configuration item.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><span data-ttu-id="c54fa-189">$config. Put ()</span><span class="sxs-lookup"><span data-stu-id="c54fa-189">$config.Put()</span></span></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-190">Définit l’emplacement de stockage des paramètres par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-190">Defines a per-computer settings storage location.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-191">Définit un emplacement de stockage des paramètres par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-191">Defines a per-user settings storage location.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-192">Définit le délai d’expiration de la synchronisation en millisecondes pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-192">Sets the synchronization time-out in milliseconds for all users of the computer.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-193">Configure l’agent UE-V pour signaler l’arrivée d’un seuil défini pour la taille du fichier de package de paramètres.</span><span class="sxs-lookup"><span data-stu-id="c54fa-193">Configures the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span> <span data-ttu-id="c54fa-194">Définissez la taille de fichier du package seuil en octets pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-194">Set the threshold package file size in bytes for all users of the computer.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncMethod = &lt;sync_method&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-195">Définit la méthode de synchronisation de tous les utilisateurs de l’ordinateur: SyncProvider ou aucune.</span><span class="sxs-lookup"><span data-stu-id="c54fa-195">Sets the synchronization method for all users of the computer: SyncProvider or None.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $true</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-196">Pour activer un paramètre par ordinateur spécifique, effacez ce paramètre et utilisez <em> $null </em> comme valeur de paramètre.</span><span class="sxs-lookup"><span data-stu-id="c54fa-196">To enable a specific per-computer setting, clear the setting, and use <em>$null</em> as the setting value.</span></span> <span data-ttu-id="c54fa-197">Utilisez UserConfiguration pour les paramètres par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-197">Use UserConfiguration for per-user settings.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $false</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-198">Pour désactiver un paramètre par ordinateur spécifique, effacez ce paramètre et utilisez <em> $null </em> comme valeur de paramètre.</span><span class="sxs-lookup"><span data-stu-id="c54fa-198">To disable a specific per-computer setting, clear the setting, and use <em>$null</em> as the setting value.</span></span> <span data-ttu-id="c54fa-199">Utilisez la configuration utilisateur pour les paramètres par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-199">Use User Configuration for per-user settings.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = &lt;setting value&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-200">Met à jour un paramètre par ordinateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="c54fa-200">Updates a specific per-computer setting.</span></span> <span data-ttu-id="c54fa-201">Pour effacer ce paramètre, utilisez <em> $null </em> comme valeur de paramètre.</span><span class="sxs-lookup"><span data-stu-id="c54fa-201">To clear the setting, use <em>$null</em> as the setting value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code></code><span data-ttu-id="c54fa-202">$config. &lt; valeur du &gt;  =  &lt; paramètre Name Setting&gt;</span><span class="sxs-lookup"><span data-stu-id="c54fa-202">$config.&lt;setting name&gt; = &lt;setting value&gt;</span></span></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-203">Met à jour un paramètre par utilisateur spécifique pour tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-203">Updates a specific per-user setting for all users of the computer.</span></span> <span data-ttu-id="c54fa-204">Pour effacer ce paramètre, utilisez <em> $null </em> comme valeur de paramètre.</span><span class="sxs-lookup"><span data-stu-id="c54fa-204">To clear the setting, use <em>$null</em> as the setting value.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and Windows PowerShell, the defined configuration is stored in the registry in the following locations.

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

**<span data-ttu-id="c54fa-205">Pour exporter des paramètres de package UE-V et réparer des modèles UE-V à l’aide de WMI</span><span class="sxs-lookup"><span data-stu-id="c54fa-205">To export UE-V package settings and repair UE-V templates by using WMI</span></span>**

1.  <span data-ttu-id="c54fa-206">UE-V fournit l’ensemble des commandes WMI suivantes.</span><span class="sxs-lookup"><span data-stu-id="c54fa-206">UE-V provides the following set of WMI commands.</span></span> <span data-ttu-id="c54fa-207">Les administrateurs peuvent utiliser cette interface pour exporter un package ou réparer des modèles UE-V.</span><span class="sxs-lookup"><span data-stu-id="c54fa-207">Administrators can use this interface to export a package or repair UE-V templates.</span></span>

2.  <span data-ttu-id="c54fa-208">Utilisez les commandes WMI suivantes.</span><span class="sxs-lookup"><span data-stu-id="c54fa-208">Use the following WMI commands.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="c54fa-209">Commande WMI</span><span class="sxs-lookup"><span data-stu-id="c54fa-209">WMI command</span></span></th>
    <th align="left"><span data-ttu-id="c54fa-210">Description</span><span class="sxs-lookup"><span data-stu-id="c54fa-210">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name ExportPackage -ArgumentList &lt;package name&gt;</code></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-211">Extrait les paramètres d’un fichier de package et les convertit dans un format lisible par l’utilisateur dans XML.</span><span class="sxs-lookup"><span data-stu-id="c54fa-211">Extracts the settings from a package file and converts them into a human-readable format in XML.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name RebuildIndex</code></p></td>
    <td align="left"><p><span data-ttu-id="c54fa-212">Répare l’index des modèles d’emplacement des paramètres UE-V.</span><span class="sxs-lookup"><span data-stu-id="c54fa-212">Repairs the index of the UE-V settings location templates.</span></span> <span data-ttu-id="c54fa-213">Doit être exécuter en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c54fa-213">Must be run as administrator.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for UE-V**? Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Got a UE-V issue**? Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).
~~~

## <span data-ttu-id="c54fa-214">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c54fa-214">Related topics</span></span>


[<span data-ttu-id="c54fa-215">Administration d’UE-V 2. x avec Windows PowerShell et WMI</span><span class="sxs-lookup"><span data-stu-id="c54fa-215">Administering UE-V 2.x with Windows PowerShell and WMI</span></span>](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[<span data-ttu-id="c54fa-216">Administration d’UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="c54fa-216">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)









