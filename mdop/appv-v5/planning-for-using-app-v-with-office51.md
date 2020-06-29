---
title: Planification de l'utilisation d'App-V avec Office
description: Planification de l'utilisation d'App-V avec Office
author: dansimp
ms.assetid: e7a19b43-1746-469f-bad6-8e75cf4b3f67
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/16/2017
ms.openlocfilehash: ae225db3c47faca5fba790fb9963bfd4dc2c66b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804957"
---
# Planification de l'utilisation d'App-V avec Office


Utilisez les informations suivantes pour planifier le déploiement d’Office à l’aide de Microsoft Application Virtualization (App-V) 5,1. Cet article inclut les éléments suivants:

-   [Prise en charge de App-V pour les modules linguistiques](#bkmk-lang-pack)

-   [Versions prises en charge de Microsoft Office](#bkmk-office-vers-supp-appv)

-   [Planification de l’utilisation de App-V avec les versions coexistantes d’Office](#bkmk-plan-coexisting)

-   [Intégration d’Office à Windows lorsque vous déployez utiliser App-V pour déployer Office](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a>Prise en charge de App-V pour les modules linguistiques


Vous pouvez utiliser le Sequencer App-V 5,1 pour créer des packages de plug-in pour les modules linguistiques, les packs linguistiques LIP, les outils de vérification linguistique et les langues d’info-bulles. Vous pouvez ensuite inclure les packages de plug-in dans un groupe de connexion, ainsi que le package 2013 Office que vous créez à l’aide du kit de développement logiciel de déploiement d’Office. Les applications Office et les modules linguistiques enfichables interagissent en toute transparence dans le même groupe de connexion, de la même manière que sur les autres packages regroupés dans un groupe de connexion.

>**Remarques**  Microsoft Visio et Microsoft Project ne prennent pas en charge le module linguistique thaï.

 

## <a href="" id="bkmk-office-vers-supp-appv"></a>Versions prises en charge de Microsoft Office

Voir [ID de produit Microsoft Office prises en charge par l’application-V](https://support.microsoft.com/help/2842297/product-ids-that-are-supported-by-the-office-deployment-tool-for-click) pour obtenir la liste des produits Office pris en charge.
>**Note** &nbsp; Remarques &nbsp; Vous devez utiliser l’outil déploiement d’Office pour créer des packages App-V pour les applications Microsoft 365 pour les entreprises. La création de packages pour les versions avec licence en volume d’Office professionnel plus ou d’Office standard n’est pas prise en charge. Vous ne pouvez pas utiliser le Sequencer App-V.

 

## <a href="" id="bkmk-plan-coexisting"></a>Planification de l’utilisation de App-V avec les versions coexistantes d’Office


Vous pouvez installer plusieurs versions de Microsoft Office côte à côte sur le même ordinateur en utilisant «coexistence Microsoft Office». Vous pouvez implémenter la coexistence d’Office à l’aide de combinaisons de toutes les principales versions d’Office et de méthodes d’installation, le cas échéant, à l’aide de la version Windows Installer (MSi) d’Office, d’Office «démarrer en un clic» et d’App-V 5,1. Toutefois, l’utilisation de la coexistence Office n’est pas recommandée par Microsoft.

Pour éviter les problèmes de compatibilité, nous vous conseillons de ne pas avoir de coexistence d’Office. Toutefois, lorsque vous effectuez une migration vers une version plus récente d’Office, des problèmes peuvent entraîner des problèmes qui ne peuvent pas être résolus, de sorte que vous pouvez implémenter une coexistence temporaire pour faciliter la migration vers la dernière version du produit. L’utilisation de la coexistence Office sur une base longue n’est jamais recommandée, et votre organisation doit être disposant d’un forfait pour une transition complète immédiate.

### Avant de mettre en œuvre la coexistence d’Office

Avant d’implémenter la coexistence d’Office, consultez la documentation Office suivante. Choisissez l’article qui correspond à la version la plus récente d’Office pour laquelle vous envisagez d’implémenter une coexistence.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version d’Office</th>
<th align="left">Lien vers des conseils</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Office 2013</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)">Informations sur l’utilisation des suites et programmes Office 2013 (déploiement MSI) sur un ordinateur exécutant une autre version d’Office</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 2010</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)">Informations sur l’utilisation des suites et des programmes Office 2010 sur un ordinateur exécutant une autre version d’Office</a></p></td>
</tr>
</tbody>
</table>

 

La documentation Office fournit des instructions détaillées sur la coexistence pour les installations d’Office basées sur Windows Installer (MSi) et démarrer en un clic. Ce sujet App-V sur la coexistence complète les recommandations d’Office avec des informations plus spécifiques aux déploiements d’application-V.

### Scénarios de coexistence pour Office pris en charge

Les tableaux suivants résument les scénarios de coexistence pris en charge. Celles-ci sont organisées en fonction de la version et de la méthode de déploiement que vous démarrez avec et de la version et de la méthode de déploiement vers laquelle vous effectuez la migration. Veillez à tester complètement toutes les solutions de coexistence avant de les déployer auprès d’un public de production.

>**Remarques**  Microsoft ne prend pas en charge l’utilisation de plusieurs versions d’Office dans les environnements Windows Server pour lesquels le service de rôle hôte de session Bureau à distance est activé. Pour exécuter des scénarios de coexistence Office, vous devez désactiver ce service de rôle.

 

### Intégrations Windows & coexistence d’Office

Les méthodes d’installation de Windows Installer et d’Office «démarrer en un clic» s’intègrent à certains points du système d’exploitation Windows sous-jacent. Lorsque vous utilisez la coexistence, les intégrations de système d’exploitation courantes entre deux versions d’Office peuvent entrer en conflit et provoquer des problèmes de compatibilité et d’utilisation de l’utilisateur. Avec App-V, vous pouvez effectuer une séquence de certaines versions d’Office afin d’exclure les intégrations, ce qui a pour effet d’isoler celles-ci du système d’exploitation.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Mode dans lequel App-V peut séquencer cette version d’Office</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Office 2007</p></td>
<td align="left"><p>Toujours non intégré. App-V n’offre aucune intégration du système d’exploitation à une version virtualisée d’Office 2007.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 2010</p></td>
<td align="left"><p>Modes intégrés et non intégrés.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Office 2013</p></td>
<td align="left"><p>Toujours intégré. Les intégrations du système d’exploitation Windows ne peuvent pas être désactivées.</p></td>
</tr>
</tbody>
</table>

 

Microsoft vous recommande de déployer la coexistence d’Office avec une seule instance Office intégrée. Par exemple, si vous utilisez App-V pour déployer Office 2010 et Office 2013, vous devez effectuer une séquence d’Office 2010 en mode non intégré. Pour plus d’informations sur le séquençage d’Office dans le mode non-intégration (isolé), voir [Comment séquencé Microsoft Office 2010 dans Microsoft application virtualization 5,0](https://support.microsoft.com/kb/2830069).

### Limitations connues des scénarios de coexistence d’Office

Les sections suivantes décrivent certains problèmes que vous pouvez rencontrer lors de l’utilisation de App-V pour implémenter la coexistence avec Office.

### Limitations communes aux scénarios de coexistence pour Windows Installer et démarrer en un clic et App-V pour Office

Les limitations suivantes peuvent se produire lorsque vous installez les versions suivantes d’Office sur le même ordinateur:

-   Office 2010 à l’aide de la version Windows Installer

-   Office 2013 à l’aide de App-V

Après avoir publié Office 2013 en utilisant App-V côte à côte avec une version antérieure de la version d’Office 2010 basée sur Windows Installer, il est possible que le programme d’installation Windows démarre. En effet, la version Windows Installer ou «démarrer en un clic» d’Office 2010 tente de s’inscrire automatiquement à l’ordinateur.

Pour ignorer l’opération d’inscription automatique pour Word 2010 natif, procédez comme suit:

1.  Quittez Word 2010.

2.  Démarrez l’éditeur du registre en procédant comme suit:

    -   Dans Windows 7: cliquez sur **Démarrer**, tapez **regedit** dans la zone démarrer la recherche, puis appuyez sur entrée.

    -   Dans Windows 8,1 ou Windows 10, tapez **regedit** , puis appuyez sur entrée dans la page de démarrage, puis appuyez sur entrée.

    Si vous êtes invité à entrer un mot de passe d’administrateur ou une confirmation, tapez le mot de passe ou cliquez sur **Continuer**.

3.  Recherchez et sélectionnez la sous-clé de Registre suivante:

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  Dans le menu **édition** , cliquez sur **nouveau**, puis cliquez sur **valeur DWORD**.

5.  Tapez **NoReReg**, puis appuyez sur entrée.

6.  Cliquez avec le bouton droit sur **NoReReg** , puis cliquez sur **modifier**.

7.  Dans la zone **ValueData** , tapez **1**, puis cliquez sur **OK**.

8.  Dans le menu fichier, cliquez sur **quitter** pour fermer l’éditeur du Registre.

## <a href="" id="bkmk-office-integration-win"></a>Intégration d’Office à Windows lors de l’utilisation de App-V pour le déploiement d’Office


Lorsque vous déployez Office 2013 à l’aide de App-V, Office est totalement intégré au système d’exploitation, qui fournit aux utilisateurs finaux les mêmes fonctionnalités qu’Office lorsque celui-ci est déployé sans App-V.

Le package App-V pour Office 2013 prend en charge les points d’intégration suivants avec le système d’exploitation Windows:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Point d’extension</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Plug-in Lync Meeting join pour Firefox et chrome</p></td>
<td align="left"><p>Les utilisateurs peuvent participer à des réunions Lync depuis Firefox et chrome</p></td>
</tr>
<tr class="even">
<td align="left"><p>Envoyés vers le pilote d’impression OneNote</p></td>
<td align="left"><p>L’utilisateur peut imprimer dans OneNote</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Notes liées OneNote</p></td>
<td align="left"><p>Notes liées OneNote</p></td>
</tr>
<tr class="even">
<td align="left"><p>Envoyer vers le complément OneNote sur le Web Explorer</p></td>
<td align="left"><p>L’utilisateur peut envoyer à OneNote à partir d’Internet Explorer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Exception de pare-feu pour Lync et Outlook</p></td>
<td align="left"><p>Exception de pare-feu pour Lync et Outlook</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client MAPI</p></td>
<td align="left"><p>Les applications et les compléments natifs peuvent interagir avec les applications virtuelles Outlook via MAPI</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Plug-in SharePoint pour Firefox</p></td>
<td align="left"><p>Les utilisateurs peuvent utiliser les fonctionnalités SharePoint dans Firefox</p></td>
</tr>
<tr class="even">
<td align="left"><p>Applet panneau de configuration de la messagerie</p></td>
<td align="left"><p>L’utilisateur obtient l’applet panneau de configuration de la messagerie dans Outlook</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Assemblys d’interopérabilité principaux</p></td>
<td align="left"><p>Compléments gérés par le support</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestionnaire de cache de documents Office</p></td>
<td align="left"><p>Autorise le cache de documents pour les applications Office</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestionnaire de recherche du protocole Outlook</p></td>
<td align="left"><p>L’utilisateur peut effectuer une recherche dans Outlook</p></td>
</tr>
<tr class="even">
<td align="left"><p>Contrôles Active X:</p></td>
<td align="left"><p>Pour plus d’informations sur les contrôles ActiveX, voir informations de référence sur les <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> API de contrôles ActiveX </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Groove. SiteClient</p></td>
<td align="left"><p>Contrôle Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   PortalConnect.PersonalSite</p></td>
<td align="left"><p>Contrôle Active X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. openDocuments</p></td>
<td align="left"><p>Contrôle Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ExportDatabase</p></td>
<td align="left"><p>Contrôle Active X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. SpreadSheetLauncher</p></td>
<td align="left"><p>Contrôle Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. StssyncHander</p></td>
<td align="left"><p>Contrôle Active X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. DragUploadCtl</p></td>
<td align="left"><p>Contrôle Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. DragDownloadCtl</p></td>
<td align="left"><p>Contrôle Active X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. OpenXMLDocuments</p></td>
<td align="left"><p>Contrôle Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ClipboardCtl</p></td>
<td align="left"><p>Contrôle Active X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   WinProj. Activator</p></td>
<td align="left"><p>Contrôle Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   Nom. NameCtrl</p></td>
<td align="left"><p>Contrôle Active X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   STSUPld.CopyCtl</p></td>
<td align="left"><p>Contrôle Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   CommunicatorMeetingJoinAx.JoinManager</p></td>
<td align="left"><p>Contrôle Active X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   LISTNET. Listnet</p></td>
<td align="left"><p>Contrôle Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   Programme d’assistance du navigateur OneDrive Pro</p></td>
<td align="left"><p>Contrôle ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Superpositions d’icônes OneDrive Pro</p></td>
<td align="left"><p>Icônes de l’interface utilisateur de l’Explorateur Windows lorsque les utilisateurs regardent les dossiers OneDrive Pro</p></td>
</tr>
<tr class="even">
<td align="left"><p>Extensions d'environnement</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Associés</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Search</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 





