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
# Gestion de l’agent UE-V 2. x et des packages avec Windows PowerShell et WMI


Vous pouvez utiliser WMI (Windows Management Instrumentation) et Windows PowerShell pour gérer les comportements de synchronisation et de configuration de l’interface utilisateur de Microsoft (UE-V) 2,0, 2,1 et 2,1 SP1. Pour obtenir la liste complète des cmdlets PowerShell d’UE-V, voir [référence sur l’applet de passe UE-v 2](https://go.microsoft.com/fwlink/?LinkId=393495) ( https://go.microsoft.com/fwlink/?LinkId=393495) .

**Pour déployer l’agent UE-V à l’aide de Windows PowerShell**

1.  Copiez le fichier du programme d’installation d’UE-V dans un partage réseau accessible.

    **Remarque**  
    Utilisez AgentSetup.exe pour déployer à la fois les versions 32 bits et 64 bits de l’agent UE-V. Les packages Windows Installer, AgentSetupx86.msi et AgentSetupx64.msi, sont disponibles pour chaque architecture. Pour désinstaller l’agent UE-V ultérieurement à l’aide du fichier d’installation, vous devez utiliser le même type de fichier.



2.  Utilisez l’une des commandes Windows PowerShell suivantes pour installer l’agent UE-V.

    -   `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    -   `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**Pour configurer l’agent UE-V à l’aide de Windows PowerShell**

1. Ouvrez une fenêtre Windows PowerShell. Pour gérer les paramètres d’ordinateur qui affectent tous les utilisateurs de l’ordinateur à l’aide du paramètre *ordinateur* , ouvrez la fenêtre avec un compte disposant de droits d’administrateur.

2. Utilisez les commandes Windows PowerShell suivantes pour configurer l’agent.

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
   <td align="left"><p><code>Get-UevConfiguration</code></p>
   <p></p></td>
   <td align="left"><p>Obtient les paramètres d’agent UE-V effectifs. Les paramètres spécifiques à l’utilisateur sont prioritaires sur les paramètres de l’ordinateur.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration - CurrentComputerUser</code></p>
   <p></p></td>
   <td align="left"><p>Obtient les valeurs des paramètres de l’agent UE-V pour l’utilisateur actuel uniquement.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Get-UevConfiguration -Computer</code></p></td>
   <td align="left"><p>Obtient les valeurs des paramètres de configuration de l’agent UE-V pour tous les utilisateurs de l’ordinateur.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Get-UevConfiguration -Details</code></p></td>
   <td align="left"><p>Obtient les détails pour chaque paramètre de configuration. Affiche l’emplacement de configuration du paramètre ou s’il utilise la valeur par défaut. Est affiché si le paramètre actuel est valide.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –ContactITDescription &lt;IT description&gt;</code></p></td>
   <td align="left"><p>Définit le texte qui s’affiche dans le centre de paramètres de société pour le lien aide.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -ContactITUrl &lt;string&gt;</code></p></td>
   <td align="left"><p>Définit l’URL du lien dans le Centre des paramètres de société pour le lien aide. Tout protocole d’URL peut être utilisé.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p>Configure l’agent UE-V de façon à ce qu’il ne synchronise aucune application Windows pour tous les utilisateurs de l’ordinateur.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser – EnableDontSyncWindows8AppSettings</code></p></td>
   <td align="left"><p>Configure l’agent UE-V de façon à ce qu’il ne synchronise aucune application Windows pour l’utilisateur actuel.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableFirstUseNotification</code></p></td>
   <td align="left"><p>Configure l’agent UE-V pour afficher les notifications lors du premier démarrage de l’agent pour tous les utilisateurs de l’ordinateur.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer –DisableFirstUseNotification</code></p></td>
   <td align="left"><p>Configure l’agent UE-V de façon à ne pas afficher les notifications lors de la première exécution de l’agent pour tous les utilisateurs de l’ordinateur.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSettingsImportNotify</code></p></td>
   <td align="left"><p>Configure l’agent UE-V pour informer tous les utilisateurs sur l’ordinateur lorsque la synchronisation des paramètres est retardée.</p>
   <p>Utilisez le <em> </em> paramètre DisableSettingsImportNotify pour désactiver la notification.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -EnableSettingsImportNotify</code></p></td>
   <td align="left"><p>Configure l’agent UE-V pour informer l’utilisateur actuel lorsque la synchronisation des paramètres est retardée.</p>
   <p>Utilisez le <em> </em> paramètre DisableSettingsImportNotify pour désactiver la notification.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p>Configure l’agent UE-V pour synchroniser toutes les applications Windows qui ne sont pas explicitement désactivées par la liste des applications Windows pour tous les utilisateurs de l’ordinateur. Pour plus d’informations, reportez-vous à la rubrique &quot; Get-UevAppxPackage &quot; dans <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Managing-V 2. x modèles d’emplacement des paramètres à l’aide de Windows PowerShell et WMI </a> .</p>
   <p>Utilisez le <em> </em> paramètre DisableSyncUnlistedWindows8Apps pour configurer l’agent UE-V de façon à ce qu’il synchronise uniquement les applications Windows activées explicitement par la liste des applications Windows.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser - EnableSyncUnlistedWindows8Apps</code></p></td>
   <td align="left"><p>Configure l’agent UE-V pour synchroniser toutes les applications Windows qui ne sont pas explicitement désactivées par la liste des applications Windows pour l’utilisateur actuel sur l’ordinateur. Pour plus d’informations, reportez-vous à la rubrique &quot; Get-UevAppxPackage &quot; dans <a href="managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md" data-raw-source="[Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md)"> Managing-V 2. x modèles d’emplacement des paramètres à l’aide de Windows PowerShell et WMI </a> .</p>
   <p>Utilisez le <em> </em> paramètre DisableSyncUnlistedWindows8Apps pour configurer l’agent UE-V de façon à ce qu’il synchronise uniquement les applications Windows activées explicitement par la liste des applications Windows.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration –Computer –DisableSync</code></p></td>
   <td align="left"><p>Désactive UE-V pour tous les utilisateurs de l’ordinateur.</p>
   <p>Utilisez le <em> </em> paramètre EnableSync pour activer ou réactiver.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –CurrentComputerUser -DisableSync</code></p></td>
   <td align="left"><p>Désactive UE-V pour l’utilisateur actuel sur l’ordinateur.</p>
   <p>Utilisez le <em> </em> paramètre EnableSync pour activer ou réactiver.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer –EnableTrayIcon</code></p></td>
   <td align="left"><p>Active l’icône UE-V dans la zone de notification pour tous les utilisateurs de l’ordinateur.</p>
   <p>Utilisez le <em> </em> paramètre DisableTrayIcon pour désactiver l’icône.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p>Configure l’agent UE-V pour signaler qu’une taille de fichier de package de paramètres atteint le seuil défini pour tous les utilisateurs de l’ordinateur. Définit la taille du package seuil en octets.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -MaxPackageSizeInBytes &lt;size in bytes&gt;</code></p></td>
   <td align="left"><p>Configure l’agent UE-V pour signaler l’arrivée d’un fichier de package de paramètres au seuil défini. Définit le seuil d’avertissement de taille de package pour l’utilisateur actuel.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p>Spécifie la durée en secondes avant la notification de l’utilisateur pour tous les utilisateurs de l’ordinateur.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration - CurrentComputerUser -SettingsImportNotifyDelayInSeconds</code></p></td>
   <td align="left"><p>Spécifie la durée en secondes avant l’envoi de la notification à l’utilisateur actuel.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p>Définit l’emplacement de stockage des paramètres par ordinateur pour tous les utilisateurs de l’ordinateur.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser -SettingsStoragePath &lt;path to _settings_storage_location&gt;</code></p></td>
   <td align="left"><p>Définit un emplacement de stockage des paramètres par utilisateur.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration –Computer –SettingsTemplateCatalogPath &lt;path to catalog&gt;</code></p></td>
   <td align="left"><p>Définit le chemin du catalogue de modèles de paramètres pour tous les utilisateurs de l’ordinateur.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p>Définit la méthode de synchronisation de tous les utilisateurs de l’ordinateur: SyncProvider ou aucune.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set-UevConfiguration -CurrentComputerUser  -SyncMethod &lt;sync method&gt;</code></p></td>
   <td align="left"><p>Définit la méthode de synchronisation pour l’utilisateur actuel: SyncProvider ou aucune.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Set-UevConfiguration -Computer -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p>Définit le délai d’expiration de la synchronisation en millisecondes pour tous les utilisateurs de l’ordinateur.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Set- UevConfiguration -CurrentComputerUser -SyncTimeoutInMilliseconds &lt;timeout in milliseconds&gt;</code></p></td>
   <td align="left"><p>Définissez le délai de synchronisation pour l’utilisateur actuel.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Clear-UevConfiguration –Computer -&lt;setting name&gt;</code></p></td>
   <td align="left"><p>Efface le paramètre spécifié pour tous les utilisateurs de l’ordinateur.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Clear-UevConfiguration –CurrentComputerUser -&lt;setting name&gt;</code></p></td>
   <td align="left"><p>Efface le paramètre spécifié pour l’utilisateur actuel uniquement.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><code>Export-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p>Exporte la configuration de l’ordinateur UE-V vers un fichier de migration des paramètres. L’extension de nom de fichier doit être. UEV.</p>
   <p>L' <code>Export</code> applet de passe exporte tous les paramètres d’agent UE-V qui peuvent être configurés avec le <em> </em> paramètre ordinateur.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><code>Import-UevConfiguration &lt;settings migration file&gt;</code></p></td>
   <td align="left"><p>Importe la configuration de l’ordinateur UE-V à partir d’un fichier de migration des paramètres. L’extension de nom de fichier doit être. UEV.</p></td>
   </tr>
   </tbody>
   </table>



**Pour exporter des paramètres de package UE-V et réparer des modèles UE-V à l’aide de Windows PowerShell**

1.  Ouvrez une fenêtre Windows PowerShell en tant qu’administrateur.

2.  Utilisez les commandes Windows PowerShell suivantes pour configurer l’agent.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Commande de Windows PowerShell</strong></p></td>
    <td align="left"><p><strong>Description</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Export-UevPackage MicrosoftCalculator6. pkgx</p></td>
    <td align="left"><p>Extrait les paramètres d’un fichier de Microsoft Calculator et les convertit dans un format lisible par l’utilisateur dans XML.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Réparation-UevTemplateIndex</p></td>
    <td align="left"><p>Répare l’index des modèles d’emplacement des paramètres UE-V.</p></td>
    </tr>
    </tbody>
    </table>



**Pour configurer l’agent UE-V à l’aide de WMI**

1.  La virtualisation de l’interface utilisateur fournit l’ensemble des commandes WMI suivantes. Les administrateurs peuvent utiliser cette interface pour configurer l’agent UE-V au niveau de la ligne de commande et automatiser les tâches de configuration typiques.

    Utilisez un compte disposant de droits d’administrateur pour ouvrir une fenêtre Windows PowerShell.

2.  Utilisez les commandes WMI suivantes pour configurer l’agent.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><code>Windows PowerShell command</code></th>
    <th align="left">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV Configuration</code></p>
    <p></p></td>
    <td align="left"><p>Affiche les paramètres d’agent UE-V actifs. Les paramètres spécifiques à l’utilisateur sont prioritaires sur les paramètres de l’ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p></td>
    <td align="left"><p>Affiche la configuration de l’agent UE-V définie pour un utilisateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p></td>
    <td align="left"><p>Affiche la configuration de l’agent UE-V définie pour un ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Get-WmiObject –Namespace root\Microsoft\Uev ConfigurationItem</code></p></td>
    <td align="left"><p>Affiche les détails de chaque élément de configuration.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Définit l’emplacement de stockage des paramètres par ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV UserConfiguration</code></p>
    <p><code>$config.SettingsStoragePath = &lt;path_to_settings_storage_location&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Définit un emplacement de stockage des paramètres par utilisateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncTimeoutInMilliseconds = &lt;timeout_in_milliseconds&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Définit le délai d’expiration de la synchronisation en millisecondes pour tous les utilisateurs de l’ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.MaxPackageSizeInBytes = &lt;size_in_bytes&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Configure l’agent UE-V pour signaler l’arrivée d’un seuil défini pour la taille du fichier de package de paramètres. Définissez la taille de fichier du package seuil en octets pour tous les utilisateurs de l’ordinateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.SyncMethod = &lt;sync_method&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Définit la méthode de synchronisation de tous les utilisateurs de l’ordinateur: SyncProvider ou aucune.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $true</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Pour activer un paramètre par ordinateur spécifique, effacez ce paramètre et utilisez <em> $null </em> comme valeur de paramètre. Utilisez UserConfiguration pour les paramètres par utilisateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = $false</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Pour désactiver un paramètre par ordinateur spécifique, effacez ce paramètre et utilisez <em> $null </em> comme valeur de paramètre. Utilisez la configuration utilisateur pour les paramètres par utilisateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code>$config.&lt;setting name&gt; = &lt;setting value&gt;</code></p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Met à jour un paramètre par ordinateur spécifique. Pour effacer ce paramètre, utilisez <em> $null </em> comme valeur de paramètre.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><code>$config = Get-WmiObject -Namespace root\Microsoft\UEV ComputerConfiguration</code></p>
    <p><code></code>$config. &lt; valeur du &gt;  =  &lt; paramètre Name Setting&gt;</p>
    <p><code>$config.Put()</code></p></td>
    <td align="left"><p>Met à jour un paramètre par utilisateur spécifique pour tous les utilisateurs de l’ordinateur. Pour effacer ce paramètre, utilisez <em> $null </em> comme valeur de paramètre.</p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and Windows PowerShell, the defined configuration is stored in the registry in the following locations.

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

**Pour exporter des paramètres de package UE-V et réparer des modèles UE-V à l’aide de WMI**

1.  UE-V fournit l’ensemble des commandes WMI suivantes. Les administrateurs peuvent utiliser cette interface pour exporter un package ou réparer des modèles UE-V.

2.  Utilisez les commandes WMI suivantes.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Commande WMI</th>
    <th align="left">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name ExportPackage -ArgumentList &lt;package name&gt;</code></p></td>
    <td align="left"><p>Extrait les paramètres d’un fichier de package et les convertit dans un format lisible par l’utilisateur dans XML.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><code>Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class SettingsLocationTemplate -Name RebuildIndex</code></p></td>
    <td align="left"><p>Répare l’index des modèles d’emplacement des paramètres UE-V. Doit être exécuter en tant qu’administrateur.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for UE-V**? Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **Got a UE-V issue**? Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).
~~~

## Rubriques connexes


[Administration d’UE-V 2. x avec Windows PowerShell et WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

[Administration d’UE-V 2. x](administering-ue-v-2x-new-uevv2.md)









