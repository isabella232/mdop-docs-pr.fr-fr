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
# Gestion de l'agent UE-V1.0 et des packages avec PowerShell et WMI


Vous pouvez utiliser WMI et PowerShell pour gérer le comportement de la synchronisation et de la synchronisation de l’agent utilisateur de Microsoft.

**Déploiement de l’agent UE-V avec PowerShell**

1.  Copiez le fichier du programme d’installation d’UE-V dans un partage réseau accessible.

    **Remarque**  
    Utilisez AgentSetup.exe pour déployer à la fois les versions 32 bits et 64 bits de l’agent UE-V. Les versions des fichiers du programme d’installation Windows, AgentSetupx86.msi et les AgentSetupx64.msi, sont disponibles pour chaque architecture. Pour désinstaller l’agent UE-V ultérieurement à l’aide du fichier d’installation, vous devez utiliser le même type de fichier.



2.  Utilisez l’une des commandes PowerShell suivantes pour installer l’agent.

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

**Configurer l’agent UE-V avec PowerShell**

1.  Utilisez un compte disposant de droits d’administrateur pour ouvrir une fenêtre PowerShell. Importez le module PowerShell UE-V à l’aide de la commande suivante.

    ``` syntax
    Import-module UEV
    ```

2.  Utilisez les commandes PowerShell suivantes pour configurer l’agent.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Commande PowerShell</strong></p></td>
    <td align="left"><p><strong>Description</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-UevConfiguration</p>
    <p></p></td>
    <td align="left"><p>Afficher les paramètres d’agent UE-V effectifs. Les paramètres spécifiques à l’utilisateur sont prioritaires sur les paramètres de l’ordinateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Get-UevConfiguration-CurrentComputerUser</p>
    <p></p></td>
    <td align="left"><p>Afficher les valeurs des paramètres de l’agent UE-V pour l’utilisateur actuel uniquement.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-UevConfiguration-Computer</p></td>
    <td align="left"><p>Affichez les valeurs des paramètres de configuration de l’agent UE-V pour tous les utilisateurs de l’ordinateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-Computer-SettingsStoragePath &lt; path to _settings_storage_location&gt;</p></td>
    <td align="left"><p>Définir un emplacement de stockage des paramètres par ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-SettingsStoragePath &lt; path to _settings_storage_location&gt;</p></td>
    <td align="left"><p>Définir un emplacement de stockage des paramètres par utilisateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-Computer-SyncTimeoutInMilliseconds &lt; délai d’expiration en millisecondes&gt;</p></td>
    <td align="left"><p>Définissez le délai de synchronisation en millisecondes.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-SyncTimeoutInMilliseconds &lt; délai en millisecondes&gt;</p></td>
    <td align="left"><p>Définissez le délai de synchronisation de l’utilisateur actuel.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-Computer-MaxPackageSizeInBytes &lt; taille en octets&gt;</p></td>
    <td align="left"><p>Configurer l’agent UE-V pour signaler l’arrivée d’un seuil défini pour la taille du fichier de package de paramètres. Définissez la taille du package seuil en octets.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-MaxPackageSizeInBytes &lt; taille en octets&gt;</p></td>
    <td align="left"><p>Définissez le seuil d’avertissement de taille de package pour l’utilisateur actuel.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-Computer-SettingsTemplateCatalogPath &lt; path to Catalog&gt;</p></td>
    <td align="left"><p>Définissez le chemin du catalogue de modèles de paramètres.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-Computer-PowerSchool &lt; Method Sync&gt;</p></td>
    <td align="left"><p>Définissez la méthode de synchronisation: OfflineFiles ou aucune.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-PowerSchool &lt; méthode de synchronisation&gt;</p></td>
    <td align="left"><p>Définissez la méthode de synchronisation de l’utilisateur actuel: OfflineFiles ou aucune.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UEVConfiguration-Computer-EnableSettingsImportNotify</p></td>
    <td align="left"><p>Activez la notification de déclenchement lorsque l’importation des paramètres utilisateur est retardée.</p>
    <p>Utilisez – DisableSettingsImportNotify pour désactiver la notification.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UEVConfiguration-CurrentComputerUser-EnableSettingsImportNotify</p></td>
    <td align="left"><p>Activez la notification pour l’utilisateur actuel lorsque l’importation des paramètres utilisateur est retardée.</p>
    <p>Utilisez – DisableSettingsImportNotify pour désactiver la notification.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UEVConfiguration-Computer-SettingsImportNotifyDelayInSeconds</p></td>
    <td align="left"><p>Spécifier la durée en secondes avant la notification de l’utilisateur</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UEVConfiguration-CurrentComputerUser-SettingsImportNotifyDelayInSeconds</p></td>
    <td align="left"><p>Spécifiez la durée en secondes avant la notification de l’utilisateur actuel.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Set-UevConfiguration-Computer-DisableSync</p></td>
    <td align="left"><p>Désactivez UE-V pour tous les utilisateurs de l’ordinateur.</p>
    <p>Utilisez – EnableSync pour activer ou réactiver.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Set-UevConfiguration-CurrentComputerUser-DisableSync</p></td>
    <td align="left"><p>Désactivez UE-V pour l’utilisateur actuel sur l’ordinateur.</p>
    <p>Utilisez – EnableSync pour activer ou réactiver.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Clear-UevConfiguration – nom de l’ordinateur- &lt; paramètre&gt;</p></td>
    <td align="left"><p>Effacez un paramètre spécifique pour tous les utilisateurs de l’ordinateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Clear-UevConfiguration-CurrentComputerUser- &lt; Setting Name&gt;</p></td>
    <td align="left"><p>Effacer un paramètre spécifique pour l’utilisateur actuel uniquement.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Fichier de migration des paramètres d’export-UevConfiguration &lt;&gt;</p></td>
    <td align="left"><p>Exportez la configuration d’ordinateur UE-V vers un fichier de migration des paramètres. L’extension du fichier doit être «. UEV».</p>
    <p>La cmdlet Export exporte tous les paramètres d’agent UE-V qui peuvent être configurés avec le paramètre-Computer.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Fichier de migration des paramètres d’importation-UevConfiguration &lt;&gt;</p></td>
    <td align="left"><p>Importez la configuration d’ordinateur UE-V à partir d’un fichier de migration des paramètres (fichier. UEV).</p></td>
    </tr>
    </tbody>
    </table>



**Exporter les paramètres de package UE-V et réparer les modèles UE-V avec PowerShell**

1.  Ouvrez une fenêtre PowerShell en tant qu’administrateur. Importez le module PowerShell UE-V à l’aide de la commande suivante.

    ``` syntax
    Import-module UEV
    ```

2.  Utilisez les commandes PowerShell suivantes pour configurer l’agent.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Commande PowerShell</strong></p></td>
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



**Configurer l’agent UE-V avec WMI**

1.  La virtualisation de l’interface utilisateur fournit l’ensemble des commandes WMI suivantes. Les administrateurs peuvent utiliser cette interface pour configurer l’agent UE-V à partir de la ligne de commande et automatiser les tâches de configuration typiques.

    Utilisez un compte disposant de droits d’administrateur pour ouvrir une fenêtre PowerShell.

2.  Utilisez les commandes WMI suivantes pour configurer l’agent.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Commande PowerShell</th>
    <th align="left">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Get-WmiObject-espace de noms root\Microsoft\UEV</p>
    <p></p></td>
    <td align="left"><p>Afficher les paramètres d’agent UE-V actifs. Les paramètres spécifiques à l’utilisateur sont prioritaires sur les paramètres de l’ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Get-WmiObject-namespace root\Microsoft\UEV UserConfiguration</p></td>
    <td align="left"><p>Affichez la configuration de l’agent UE-V définie pour l’utilisateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p></td>
    <td align="left"><p>Affichez la configuration de l’agent UE-V définie pour l’ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Définir un emplacement de stockage des paramètres par ordinateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV UserConfiguration</p>
    <p>$config. SettingsStoragePath = &lt; path_to_settings_storage_location&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Définir un emplacement de stockage des paramètres par utilisateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. SyncTimeoutInMilliseconds = &lt; timeout_in_milliseconds&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Définissez le délai de synchronisation en millisecondes.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. MaxPackageSizeInBytes = &lt; size_in_bytes&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Configurer l’agent UE-V pour signaler l’arrivée d’un seuil défini pour la taille du fichier de package de paramètres. Définissez la taille de fichier du package seuil en octets.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. PowerSchool = &lt; sync_method&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Définissez la méthode de synchronisation: OfflineFiles ou aucune.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. &lt; valeur du &gt;  =  &lt; paramètre Name Setting&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Mettre à jour un paramètre par ordinateur spécifique. Pour effacer ce paramètre, utilisez $null comme valeur de paramètre.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$config = Get-WmiObject-namespace root\Microsoft\UEV ComputerConfiguration</p>
    <p>$config. &lt; valeur du &gt;  =  &lt; paramètre Name Setting&gt;</p>
    <p>$config. Put ()</p></td>
    <td align="left"><p>Mettre à jour un paramètre par utilisateur spécifique. Pour effacer ce paramètre, utilisez $null comme valeur de paramètre.</p></td>
    </tr>
    </tbody>
    </table>



~~~
Upon configuration of the UE-V Agent with WMI and PowerShell, the defined configuration is stored in the registry in the following locations:

`\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\UEV\Agent\Configuration`

`\HKEY_CURRENT_USER\SOFTWARE\Microsoft\UEV\Agent\Configuration`
~~~

## Rubriques connexes


[Administration d'UE-V1.0](administering-ue-v-10.md)

[Opérations d'UE-V1.0](operations-for-ue-v-10.md)









