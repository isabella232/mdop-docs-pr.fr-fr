---
title: Déploiement de Microsoft Office2010 à l'aide d'App-V
description: Déploiement de Microsoft Office2010 à l'aide d'App-V
author: dansimp
ms.assetid: 0a9e496e-82a1-4dc0-a496-7b21eaa00f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 303a44d921e40a411a4c4ea4622f06a76b8ed9c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805875"
---
# Déploiement de Microsoft Office2010 à l'aide d'App-V


Vous pouvez créer des packages Office 2010 pour la virtualisation des applications 5,0 en utilisant l’une des méthodes suivantes:

-   Sequencer Application Virtualization (App-V)

-   Accélérateur de package Application Virtualization (App-V)

## Prise en charge de App-V pour Office 2010


Le tableau suivant indique les versions d’App-V, les méthodes de création de packages Office, les licences prises en charge et les déploiements pris en charge pour Office 2010.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Élément pris en charge</th>
<th align="left">Niveau de prise en charge</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Versions d’App-V prises en charge</p></td>
<td align="left"><ul>
<li><p>4,6</p></li>
<li><p>5.0</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Création de package</p></td>
<td align="left"><ul>
<li><p>Séquençage</p></li>
<li><p>Package Accelerator</p></li>
<li><p>Kit de déploiement Office</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Licences prises en charge</p></td>
<td align="left"><p>Gestion des licences en volume</p></td>
</tr>
<tr class="even">
<td align="left"><p>Déploiements pris en charge</p></td>
<td align="left"><ul>
<li><p>Bureau</p></li>
<li><p>VDI personnel</p></li>
<li><p>RDS</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## Création d’une application Office 2010-V 5,0 à l’aide du Sequencer


Le séquençage d’Office 2010 est l’une des principales méthodes de création d’un package Office 2010 sur App-V 5,0. Microsoft a fourni une recette détaillée par le biais d’un article de la base de connaissances. Pour créer un package 2010 Office sur App-V 5,0, voir les liens suivants pour obtenir des instructions détaillées:

[Comment séquencer Microsoft Office 2010 dans Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## Créer des packages App-V 5,0 Office 2010 à l’aide des accélérateurs de package


Les packages App-V 5,0 d’Office 2010 peuvent être créés via accélérateurs de package. Microsoft a fourni des accélérateurs de package pour la création d’Office 2010 sur Windows 8 et Windows 7. Pour créer des packages Office 2010 sur App-V à l’aide d’accélérateurs de package, reportez-vous aux pages suivantes pour accéder à l’accélérateur de package approprié:

-   [App-V 5,0 package Accelerator pour Office professionnel plus 2010 – Windows 8](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [App-V 5,0 package Accelerator pour Office professionnel plus 2010-Windows 7](https://go.microsoft.com/fwlink/p/?LinkId=330678)

Pour obtenir des instructions détaillées sur la création de packages d’applications virtuelles à l’aide des accélérateurs de package App-V, voir [créer un package d’application virtuelle à l’aide d’un accélérateur de package App-v](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md).

## Déploiement du package Microsoft Office pour App-V 5,0


Vous pouvez déployer les packages Office 2010 à l’aide de l’une des méthodes de déploiement d’App-V suivantes:

-   SystemCenterConfigurationManager

-   App-V Server

-   Commandes PowerShell autonomes

## Gestion et personnalisation des packages App-V pour Office


Les packages 2010 Office peuvent être gérés comme n’importe quel autre package App-V 5,0 par le biais de mécanismes de gestion des packages connus. Aucune instruction spéciale n’est nécessaire (par exemple, pour ajouter, publier, annuler ou supprimer des packages Office).

## Intégration de Microsoft Office à Windows


Le tableau suivant répertorie la liste complète des points d’intégration pris en charge pour Office 2010.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Point d’extension</th>
<th align="left">Description</th>
<th align="left">Office 2010</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Plug-in Lync Meeting join pour Firefox et chrome</p></td>
<td align="left"><p>Les utilisateurs peuvent participer à des réunions Lync depuis Firefox et chrome</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Envoyés vers le pilote d’impression OneNote</p></td>
<td align="left"><p>L’utilisateur peut imprimer dans OneNote</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Notes liées OneNote</p></td>
<td align="left"><p>Notes liées OneNote</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Envoyer vers le complément OneNote sur le Web Explorer</p></td>
<td align="left"><p>L’utilisateur peut envoyer à OneNote à partir d’Internet Explorer</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Exception de pare-feu pour Lync et Outlook</p></td>
<td align="left"><p>Exception de pare-feu pour Lync et Outlook</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Client MAPI</p></td>
<td align="left"><p>Les applications et les compléments natifs peuvent interagir avec les applications virtuelles Outlook via MAPI</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Plug-in SharePoint pour Firefox</p></td>
<td align="left"><p>Les utilisateurs peuvent utiliser les fonctionnalités SharePoint dans Firefox</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Applet panneau de configuration de la messagerie</p></td>
<td align="left"><p>L’utilisateur obtient l’applet panneau de configuration de la messagerie dans Outlook</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Assemblys d’interopérabilité principaux</p></td>
<td align="left"><p>Compléments gérés par le support</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestionnaire de cache de documents Office</p></td>
<td align="left"><p>Autorise le cache de documents pour les applications Office</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestionnaire de recherche du protocole Outlook</p></td>
<td align="left"><p>L’utilisateur peut effectuer une recherche dans Outlook</p></td>
<td align="left"><p>Oui</p></td>
</tr>
<tr class="even">
<td align="left"><p>Contrôles Active X:</p></td>
<td align="left"><p>Pour plus d’informations sur les contrôles ActiveX, voir informations de référence sur les <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> API de contrôles ActiveX </a> .</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Groove. SiteClient</p></td>
<td align="left"><p>Contrôle Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   PortalConnect.PersonalSite</p></td>
<td align="left"><p>Contrôle Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. openDocuments</p></td>
<td align="left"><p>Contrôle Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ExportDatabase</p></td>
<td align="left"><p>Contrôle Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. SpreadSheetLauncher</p></td>
<td align="left"><p>Contrôle Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. StssyncHander</p></td>
<td align="left"><p>Contrôle Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. DragUploadCtl</p></td>
<td align="left"><p>Contrôle Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. DragDownloadCtl</p></td>
<td align="left"><p>Contrôle Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. OpenXMLDocuments</p></td>
<td align="left"><p>Contrôle Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ClipboardCtl</p></td>
<td align="left"><p>Contrôle Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   WinProj. Activator</p></td>
<td align="left"><p>Contrôle Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   Nom. NameCtrl</p></td>
<td align="left"><p>Contrôle Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   STSUPld.CopyCtl</p></td>
<td align="left"><p>Contrôle Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   CommunicatorMeetingJoinAx.JoinManager</p></td>
<td align="left"><p>Contrôle Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   LISTNET. Listnet</p></td>
<td align="left"><p>Contrôle Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   Programme d’assistance du navigateur OneDrive Pro</p></td>
<td align="left"><p>Contrôle ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Superpositions d’icônes OneDrive Pro</p></td>
<td align="left"><p>Icônes de l’interface utilisateur de l’Explorateur Windows lorsque les utilisateurs regardent les dossiers OneDrive Pro</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## Ressources supplémentaires


**Office 2013 App-V 5,0 packages 5,0 ressources supplémentaires**

[Scénarios pris en charge pour le déploiement de Microsoft Office en tant que package App-V séquencé](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**Packages App-V 5,0 dans Office 2010**

[Kit de séquençage Microsoft Office 2010 pour Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[Problèmes connus lors de la création ou de l’utilisation d’un package App-V 5,0 Office 2010](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[Comment séquencer Microsoft Office 2010 dans Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**Groupes de connexion**

[Déploiement de groupes de connexion dans Microsoft App-V v5](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[Gestion des groupes de connexion](managing-connection-groups.md)

**Configuration dynamique**

[À propos de la configuration dynamique d'App-V5.0](about-app-v-50-dynamic-configuration.md)






 

 





