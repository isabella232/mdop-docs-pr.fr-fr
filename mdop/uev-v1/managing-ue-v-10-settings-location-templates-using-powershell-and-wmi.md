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
# Gestion des modèles d'emplacement des paramètres UE-V1.0 à l'aide de PowerShell et WMI


La virtualisation de l’utilisation de l’utilisateur Microsoft (UE-V) utilise des modèles d’emplacement des paramètres (fichiers XML) qui définissent les paramètres capturés et appliqués par la virtualisation de l’utilisation de l’utilisateur. UE-V inclut un ensemble de modèles d’emplacement des paramètres standard. Il inclut également l’outil de génération UE-V qui vous permet de créer des modèles d’emplacement des paramètres personnalisés. Une fois que vous avez créé et déployé des modèles d’emplacement des paramètres, vous pouvez gérer ces modèles en utilisant PowerShell ou WMI.

## Gérer les modèles d’emplacement des paramètres avec WMI et PowerShell


Les fonctionnalités WMI et PowerShell d’UE-V incluent la possibilité d’activer, de désactiver, de inscrire, de mettre à jour et de déregistrer les modèles d’emplacement des paramètres. L’utilisation de ces fonctionnalités vous permet d’automatiser le processus d’inscription, de mise à jour ou de suppression de l’enregistrement de modèles auprès de l’agent UE-V. Vous pouvez également enregistrer des modèles manuellement à l’aide des commandes WMI et PowerShell. L’utilisation de ces fonctionnalités conjointement à une solution de distribution de logiciels électronique, une stratégie de groupe ou un autre mode de déploiement automatisé, tel qu’un script, vous permet d’automatiser davantage ce processus.

Vous devez disposer des autorisations d’administrateur pour mettre à jour, inscrire ou annuler l’enregistrement d’un modèle d’emplacement des paramètres. Les autorisations d’administrateur ne sont pas requises pour activer ou désactiver des modèles.

**Pour gérer les modèles d’emplacement des paramètres avec PowerShell**

1.  Utilisez un compte disposant de droits d’administrateur pour ouvrir une fenêtre Windows PowerShell. Pour importer le module **Microsoft UE-V PowerShell** , tapez la commande suivante à l’invite de commandes PowerShell.

    ``` syntax
    Import-module UEV
    ```

2.  Utilisez les applets de commande PowerShell suivantes pour inscrire et gérer les modèles d’emplacement des paramètres UE-V.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Commande PowerShell</strong></th>
    <th align="left"><strong>Description</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Get-UevTemplate</p></td>
    <td align="left"><p>Répertorie tous les modèles d’emplacements des paramètres enregistrés sur l’ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Register-UevTemplate</p></td>
    <td align="left"><p>Inscrit un modèle d’emplacement des paramètres avec UE-V. Une fois qu’un modèle est enregistré, UE-V va synchroniser les paramètres définis dans le modèle entre les ordinateurs sur lesquels le modèle est enregistré.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Unregister-UevTemplate</p></td>
    <td align="left"><p>Annule l’inscription d’un modèle d’emplacement des paramètres avec UE-V. Dès qu’aucun modèle n’est enregistré, UE-V ne synchronise plus les paramètres définis dans le modèle entre les ordinateurs.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Update-UevTemplate</p></td>
    <td align="left"><p>Met à jour un modèle d’emplacement des paramètres avec une version plus récente du modèle. Le nouveau modèle doit avoir une version ultérieure à celle existante.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Disable-UevTemplate</p></td>
    <td align="left"><p>Désactive un modèle d’emplacement des paramètres pour l’utilisateur actuel de l’ordinateur.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Enable-UevTemplate</p></td>
    <td align="left"><p>Active un modèle d’emplacement des paramètres pour l’utilisateur actuel de l’ordinateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Test-UevTemplate</p></td>
    <td align="left"><p>Détermine si un modèle d’emplacement des paramètres donné est conforme à son schéma XML.</p></td>
    </tr>
    </tbody>
    </table>

     

Les fonctionnalités PowerShell d’UE-V vous permettent de gérer un groupe de modèles de paramètres déployés dans votre entreprise. Pour gérer un groupe de modèles à l’aide de PowerShell, procédez comme suit.

**Pour gérer un groupe de modèles d’emplacement des paramètres avec PowerShell**

1.  Modifiez ou mettez à jour les modèles d’emplacement des paramètres souhaités.

2.  Déployez les modèles d’emplacement des paramètres souhaités dans un dossier accessible à partir de l’ordinateur local.

3.  Sur l’ordinateur local, ouvrez une fenêtre Windows PowerShell avec des droits d’administrateur.

4.  Importez le module Microsoft UE-V PowerShell en entrant la commande suivante.

    ``` syntax
    Import-module UEV
    ```

5.  Annulez l’enregistrement de toutes les versions inscrites des modèles en entrant la commande suivante.

    ``` syntax
    Get-UevTemplate | Unregister-UevTemplate
    ```

    Le fichier est alors annulé sur tous les modèles actifs de l’ordinateur.

6.  Enregistrez les modèles mis à jour en entrant la commande suivante.

    ``` syntax
    Register-UevTemplate <path to template folder>\*.xml
    ```

    Les modèles d’emplacement des paramètres sont enregistrés dans le dossier de modèles spécifié.

La virtualisation de l’interface utilisateur fournit l’ensemble des commandes WMI suivantes. Les administrateurs peuvent utiliser ces interfaces pour gérer les modèles d’emplacement des paramètres à partir de Windows PowerShell et automatiser les tâches d’administration des modèles.

**Pour gérer les modèles d’emplacement des paramètres avec WMI**

1.  Utilisez un compte disposant de droits d’administrateur pour ouvrir une fenêtre Windows PowerShell.

2.  Utilisez les commandes WMI suivantes pour inscrire et gérer les modèles d’emplacement des paramètres UE-V.

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
    <td align="left"><p>Get-WmiObject-namespace root\Microsoft\UEV SettingsLocationTemplate | Select-Object TemplateId, Nom_modèle, TemplateVersion, activé | Format-table-dimensionnement automatique</p></td>
    <td align="left"><p>Répertorie tous les modèles d’emplacements des paramètres enregistrés pour l’ordinateur.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-nom Register--chemin de modèle-ArgumentList &lt;&gt;</p></td>
    <td align="left"><p>Inscrit un modèle d’emplacement des paramètres avec UE-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-SettingsLocationTemplate-nom UnregisterByTemplateId-ID de &lt; modèle-argumentlist&gt;</p></td>
    <td align="left"><p>Annule l’inscription d’un modèle d’emplacement des paramètres avec UE-V. Dès qu’aucun modèle n’est enregistré, UE-V ne synchronise plus les paramètres définis dans le modèle entre les ordinateurs.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-SettingsLocationTemplate-nom EnableByTemplateId-ID de &lt; modèle-argumentlist&gt;</p></td>
    <td align="left"><p>Active un modèle d’emplacement des paramètres avec UE-V</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-SettingsLocationTemplate-nom DisableByTemplateId-ID de &lt; modèle-argumentlist&gt;</p></td>
    <td align="left"><p>Désactive un modèle d’emplacement des paramètres avec UE-V</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-nom &lt;&gt;</p></td>
    <td align="left"><p>Met à jour un modèle d’emplacement des paramètres avec UE-V. Le nouveau modèle doit avoir une version supérieure à la version existante.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class SettingsLocationTemplate-nom Validate- &lt; argumentlist&gt;</p></td>
    <td align="left"><p>Détermine si un modèle d’emplacement des paramètres donné est conforme à son schéma XML.</p></td>
    </tr>
    </tbody>
    </table>

     

**Déploiement de l’agent UE-V avec PowerShell**

1.  Copiez le fichier du programme d’installation d’UE-V dans un partage réseau accessible.

    **Remarques**  Utilisez AgentSetup.exe pour déployer à la fois les versions 32 bits et 64 bits de l’agent UE-V. Les versions des fichiers du programme d’installation Windows, AgentSetupx86.msi et les AgentSetupx64.msi, sont disponibles pour chaque architecture. Pour désinstaller l’agent UE-V ultérieurement à l’aide du fichier d’installation, vous devez utiliser le même type de fichier.

     

2.  Utilisez l’une des commandes PowerShell suivantes pour installer l’agent.

    `& AgentSetup.exe /quiet /norestart /log "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

    `& msiexec.exe /i "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log" SettingsStoragePath=\\server\settingsshare\%username%`

## Rubriques connexes


[Gestion de l'agent UE-V1.0 et des packages avec PowerShell et WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

[Administration d'UE-V1.0](administering-ue-v-10.md)

[Opérations d'UE-V1.0](operations-for-ue-v-10.md)

 

 





