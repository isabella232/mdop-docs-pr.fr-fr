---
title: Comment configurer l'intégration de MBAM2.5 à System Center Configuration Manager
description: Comment configurer l'intégration de MBAM2.5 à System Center Configuration Manager
author: dansimp
ms.assetid: 2b8a4c13-1dad-41e8-89ac-6889c5f7e051
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c6fb0a0b06399baf1dc6493a40d17e76a51741f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804231"
---
# Comment configurer l'intégration de MBAM2.5 à System Center Configuration Manager


Cet article explique comment configurer l’administration et la surveillance de l’utilisation de Microsoft BitLocker (MBAM) pour utiliser la topologie d’intégration de System Center Configuration Manager, qui intègre MBAM avec Configuration Manager.

Les instructions expliquent comment configurer l’intégration de Configuration Manager à l’aide des éléments suivants:

-   Une applet de cmdlet Windows PowerShell

-   Assistant Configuration de MBAM Server

Les instructions sont basées sur l’architecture recommandée dans [architecture de haut niveau pour MBAM 2,5](high-level-architecture-for-mbam-25.md).

**Avant de démarrer la configuration:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Étape</th>
<th align="left">Où obtenir des instructions</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Passez en revue l’architecture recommandée pour MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md" data-raw-source="[High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)">Architecture globale de MBAM2.5 avec la topologie Intégration Configuration Manager</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Passez en revue les configurations prises en charge pour MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurations prises en charge par MBAM2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Remplissez les conditions préalables requises sur chaque serveur.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous allez configurer une fonctionnalité de MBAM Server.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Pour cette topologie, vous devez installer la console Configuration Manager sur l’ordinateur sur lequel vous installez le logiciel serveur MBAM.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installation du logiciel serveur MBAM2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Passez en revue la configuration requise pour Windows PowerShell (s’applique uniquement si vous envisagez d’utiliser des cmdlets Windows PowerShell pour configurer MBAM).</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Pour configurer l’intégration de Configuration Manager à l’aide de Windows PowerShell**

1.  Avant de commencer la configuration, reportez-vous à la rubrique [Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) pour consulter les conditions préalables à l’utilisation de Windows PowerShell.

2.  Utilisez l’applet de cmdlet Windows PowerShell **Enable-MbamCMIntegration** pour configurer les rapports. Pour obtenir des informations sur cette cmdlet, tapez **Get-Help-MbamCMIntegration**.

**Pour configurer l’intégration de System Center Configuration Manager à l’aide de l’Assistant**

1.  Sur le serveur sur lequel vous voulez configurer la fonctionnalité d’intégration de System Center Configuration Manager, démarrez l’Assistant Configuration de MBAM Server. Vous pouvez sélectionner **MBAM de configuration de serveur** dans le menu **Démarrer** pour ouvrir l’Assistant.

2.  Cliquez sur **ajouter de nouvelles fonctionnalités**, sélectionnez **intégration de System Center Configuration Manager**, puis cliquez sur **suivant**.

    L’Assistant vérifie que toutes les conditions préalables pour l’intégration de Configuration Manager sont remplies.

3.  Si la vérification de la configuration requise est réussie, cliquez sur **suivant** pour continuer. Dans le cas contraire, résolvez les conditions préalables manquantes, puis cliquez **à nouveau sur vérifier les conditions préalables**.

4.  Utilisez les descriptions suivantes pour entrer les valeurs de champ dans l’Assistant:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Champ</th>
    <th align="left">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Serveur SQL Server Reporting Services</strong></p></td>
    <td align="left"><p>Nom de domaine complet (FQDN) du serveur doté du rôle de point de service de création de rapports. Il s’agit du serveur sur lequel sont déployés les rapports du gestionnaire de configuration MBAM.</p>
    <p>Si vous ne spécifiez pas de serveur, les rapports du gestionnaire de configuration seront déployés sur le serveur local.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Instance de SQL Server Reporting Services</strong></p></td>
    <td align="left"><p>Nom de l’instance SQL Server Reporting Services (SSRS) dans laquelle les rapports Configuration Manager sont déployés.</p>
    <p>Si vous ne spécifiez pas d’instance, les rapports du gestionnaire de configuration seront déployés sur le nom d’instance SSRS par défaut. La valeur que vous entrez est ignorée si le serveur a installé le gestionnaire de configuration de System Center 2012.</p></td>
    </tr>
    </tbody>
    </table>



5.  Dans la page **Résumé** , passez en revue les fonctionnalités qui seront ajoutées.

    **Remarque**  
    Pour créer un script Windows PowerShell des entrées que vous venez de créer, cliquez sur **Exporter le script PowerShell** et enregistrez le script.



6.  Cliquez sur **Ajouter** pour ajouter la fonctionnalité d’intégration de Configuration Manager au serveur, puis cliquez sur **Fermer**.



## Rubriques connexes


[Configuration des composants du serveur MBAM2.5](configuring-the-mbam-25-server-features.md)

[Validation de la configuration des composants serveur de MBAM2.5](validating-the-mbam-25-server-feature-configuration.md)


## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






