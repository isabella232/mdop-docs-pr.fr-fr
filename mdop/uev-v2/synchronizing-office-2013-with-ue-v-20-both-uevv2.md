---
title: Synchronisation d’Office 2013 avec UE-V 2,0
description: Synchronisation d’Office 2013 avec UE-V 2,0
author: dansimp
ms.assetid: c46feb6d-28a8-4799-888d-053531dc5842
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9b079d3f21e6ced689fa2101f5321fa9b1406c8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812024"
---
# Synchronisation d’Office 2013 avec UE-V 2,0


Microsoft User Interface Virtualization (UE-V) 2,0 prend en charge la synchronisation du paramètre d’application Microsoft Office 2013 à l’aide d’un modèle disponible dans la Galerie de modèles UE-V. Dans le cadre de la prise en charge de UE-V 2 et de la prise en charge de App-v 5,0 SP2 d’Office 2013 professionnel plus, vous bénéficiez de la même expérience sur une instance virtualisée d’Office 2013 à partir d’un appareil compatible avec UE-V ou de bureau virtualisé.

Pour activer la prise en charge des paramètres d’application UE-V d’Office 2013, vous pouvez télécharger des modèles d’Office 2013 officiels UE-V à partir de la [Galerie de modèles Microsoft User Interface Virtualization (UE-v) 2](https://go.microsoft.com/fwlink/p/?LinkId=246589). Cette ressource fournit des modèles d’emplacement des paramètres UE-V et des paramètres développés par la communauté.

## Prise en charge de Microsoft Office dans UE-V


UE-V 1,0 et UE-V 2 incluent les modèles d’emplacement des paramètres pour Microsoft Office 2010. Ces modèles sont distribués et inscrits dans le cadre du processus d’installation de l’agent UE-V. Ces modèles permettent de synchroniser l’interface utilisateur d’Office entre les appareils. Les modèles UE-V pour Office 2013 fournissent une interface de paramètres très similaire aux modèles pour Office 2010. Les paramètres de Microsoft Office 2013 qui sont déplacés par l’utilisateur d’Office 365 ne sont pas inclus dans ces paramètres. Pour obtenir la liste des paramètres spécifiques d’Office 365, voir [vue d’ensemble des paramètres utilisateur et itinérance pour office 2013](https://go.microsoft.com/fwlink/p/?LinkId=391220).

## Paramètres 2013 d’Office synchronisés


Les tableaux suivants contiennent les détails relatifs à la prise en charge d’Office 2013 dans UE-V:

### Modèles UE-V pris en charge pour Microsoft Office

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Modèles Office 2013 (UE-V 2,0 disponibles sur le site UE-V Gallery):</th>
<th align="left">Modèles Office 2010 (UE-V 1,0 &amp; 1,0 SP1):</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MicrosoftOffice2013Win32.xml</p>
<p>MicrosoftOffice2013Win64.xml</p>
<p>MicrosoftLync2013Win32.xml</p>
<p>MicrosoftLync2013Win64.xml</p></td>
<td align="left"><p>MicrosoftOffice2010Win32.xml</p>
<p>MicrosoftOffice2010Win64.xml</p>
<p>MicrosoftLync2010.xml</p>
<p></p></td>
</tr>
</tbody>
</table>

 

### Applications Microsoft Office prises en charge par les modèles UE-V

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Access 2013</p>
<p>Microsoft Lync 2013</p>
<p>Microsoft Excel 2013</p>
<p>Microsoft InfoPath 2013</p>
<p>Microsoft OneNote 2013</p>
<p>Microsoft Outlook 2013</p>
<p>Microsoft PowerPoint 2013</p>
<p>Microsoft Project 2013</p>
<p>Microsoft Publisher 2013</p>
<p>Microsoft SharePoint Designer 2013</p>
<p>Microsoft Visio 2013</p>
<p>Microsoft Word 2013</p>
<p>Gestionnaire de téléchargement Microsoft Office</p></td>
<td align="left"><p>Microsoft Access 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft SharePoint Designer 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft Word 2010</p>
<p></p></td>
</tr>
</tbody>
</table>

 

## Déploiement des modèles Office 2013


Vous pouvez déployer le modèle d’emplacement des paramètres UE-V avec les méthodes suivantes:

-   **Inscription du modèle via PowerShell**. Si vous utilisez Windows PowerShell pour gérer les ordinateurs, exécutez la commande Windows PowerShell suivante ouverte en tant qu’administrateur pour inscrire ce modèle d’emplacement des paramètres:

    ``` syntax
    Register-UevTemplate -Path <Path_to_Template>
    ```

    Pour plus d’informations sur UE-V et Windows PowerShell, reportez-vous à la rubrique [gestion des modèles d’emplacement des paramètres UE-v 2. x utilisant Windows PowerShell et WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).

-   **Inscription du modèle via le chemin du catalogue du modèle**. Si vous utilisez le chemin du catalogue de modèles de paramètres pour gérer les modèles sur les ordinateurs des utilisateurs, copiez le modèle 2013 Office dans le dossier défini dans l’agent UE-V. Lors de la prochaine exécution de la tâche planifiée de mise à jour automatique de modèle (ApplySettingsCatalog.exe), le modèle d’emplacement des paramètres est enregistré sur l’appareil. Pour plus d’informations, reportez-vous à [déploiement du catalogue de modèles de paramètres pour UE-V 2](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue).

-   **Inscription du modèle via Configuration Manager**. Si vous utilisez Configuration Manager pour gérer vos modèles de stockage de paramètres UE-V, recréez le modèle de fichier CAB de référence, importez-le dans Configuration Manager, puis déployez le planning de référence sur vos clients. Pour plus d’informations, reportez-vous aux recommandations fournies dans la documentation relative au [Pack de configuration de System Center 2012 pour l’utilisation de Microsoft User-virtualisation 2](https://go.microsoft.com/fwlink/?LinkId=317263).






 

 





