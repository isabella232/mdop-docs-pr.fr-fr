---
title: Configuration des rapports MBAM2.5
description: Configuration des rapports MBAM2.5
author: dansimp
ms.assetid: ec462879-0253-4d9c-83c7-a9bcad479725
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b372bd6bc38a3729aef43354ecf19b2619b7856
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811862"
---
# Configuration des rapports MBAM2.5


Cet article explique comment configurer la fonctionnalité de rapports 2,5 d’administration et de surveillance de Microsoft BitLocker (MBAM) à l’aide des éléments suivants:

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
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Architecture de hautniveau pour MBAM2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Passez en revue les configurations prises en charge pour MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurations prises en charge par MBAM2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Remplissez les conditions préalables requises sur chaque serveur.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">MBAM 2,5 requis par le serveur qui ne s’appliquent qu’à la topologie d’intégration de Configuration Manager </a> (le cas échéant)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous envisagez de configurer une fonctionnalité de MBAM Server.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installation du logiciel serveur MBAM2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Passez en revue la configuration requise pour l’utilisation de Windows PowerShell Si vous envisagez d’utiliser des cmdlets Windows PowerShell pour configurer les fonctionnalités du serveur MBAM.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Pour configurer les rapports à l’aide de Windows PowerShell**

1.  Avant de commencer la configuration, reportez-vous à la rubrique [Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) pour consulter les conditions préalables à l’utilisation de Windows PowerShell.

2.  Utilisez l’applet de cmdlet Windows PowerShell **Enable-MbamReport** pour configurer les rapports. Pour obtenir des informations sur cette applet de cmdlet Windows PowerShell, tapez **Get-Help-MbamReport**.

**Pour configurer les rapports à l’aide de l’Assistant**

1. Sur le serveur sur lequel vous voulez configurer les rapports, démarrez l’Assistant **configuration de MBAM Server** . Vous pouvez sélectionner **MBAM de configuration de serveur** dans le menu **Démarrer** pour ouvrir l’Assistant.

2. Cliquez sur **ajouter de nouvelles fonctionnalités**, sélectionnez **rapports**, puis cliquez sur **suivant**. L’Assistant vérifie que toutes les conditions préalables pour les rapports sont remplies.

3. Cliquez sur **Suivant** pour poursuivre.

4. À l’aide des descriptions suivantes, entrez les valeurs de champ dans l’Assistant:

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
   <td align="left"><p><strong>Instance de SQL Server Reporting Services</strong></p></td>
   <td align="left"><p>Instance de SQL Server Reporting Services où les rapports seront configurés.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Groupe de domaine de rôle de rapport</strong></p></td>
   <td align="left"><p>Nom du groupe d’utilisateurs du domaine dont les membres ont le droit d’accéder aux rapports sur le serveur d’administration et de surveillance.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Nom SQL Server</strong></p></td>
   <td align="left"><p>Nom du serveur sur lequel la base de données d’audit et de conformité est configurée.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Instance de base de données SQL Server</strong></p></td>
   <td align="left"><p>Nom de l’instance de SQL Server (par exemple, <em> MSSQLSERVER </em> ) où la base de données d’audit et de conformité est configurée.</p>
   <div class="alert">
   <strong>Remarque</strong><br/><p>Vous devez ajouter une exception sur l’ordinateur rapports pour activer le trafic entrant sur le port du serveur de création de rapports (le port par défaut est 80).</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Nom de la base de données</strong></p></td>
   <td align="left"><p>Nom de la base de données d’audit et de conformité. Par défaut, il s’agit du nom de la base de données <strong> MBAM </strong> , même si vous pouvez en modifier le nom lorsque vous configurez la base de données d’audit et de conformité.</p>
   <div class="alert">
   <strong>Remarque</strong><br/><p>Si vous effectuez une mise à niveau à partir d’une version précédente de MBAM, vous devez utiliser le même nom de base de données que le nom utilisé dans votre ancien déploiement.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Vérification de la conformité et de la base de données du compte de domaine</strong></p></td>
   <td align="left"><p>Compte d’utilisateur et mot de passe de domaine pour accéder à la base de données d’audit et de conformité.</p>
   <p>Si la valeur que vous entrez dans le <strong> champ d’utilisateur ou de groupe d’accès en lecture seule </strong> de la <strong> page configurer des bases de données </strong> est un utilisateur, vous devez entrer cette même valeur dans ce champ.</p>
   <p>Si la valeur que vous entrez dans le <strong> champ d’utilisateur ou de groupe d’accès en lecture seule </strong> de la <strong> page Configurer les bases de données </strong> est un groupe, la valeur que vous entrez dans ce champ doit être membre du groupe.</p>
   <p>Configurez le mot de passe de ce compte pour qu’il n’expire jamais. Le compte d’utilisateur doit être en mesure d’accéder à toutes les données disponibles pour le groupe utilisateurs de reports MBAM.</p></td>
   </tr>
   </tbody>
   </table>



5. Lorsque vous avez terminé, cliquez sur **suivant**.

   L’Assistant vérifie que toutes les conditions préalables pour la fonctionnalité rapports sont remplies.

6. Cliquez sur **Suivant** pour poursuivre.

7. Dans la page **Résumé** , passez en revue les fonctionnalités qui seront ajoutées.

   **Remarque**  
   Pour créer un script Windows PowerShell des entrées que vous venez de créer, cliquez sur **Exporter le script PowerShell**, puis enregistrez le script.



8. Cliquez sur **Ajouter** pour ajouter les rapports sur le serveur, puis cliquez sur **Fermer**.



## Rubriques connexes


[Journaux des événements serveur](server-event-logs.md)

[Configuration des composants du serveur MBAM2.5](configuring-the-mbam-25-server-features.md)

[Comment configurer les applications Web MBAM2.5](how-to-configure-the-mbam-25-web-applications.md)

[Validation de la configuration des composants serveur de MBAM2.5](validating-the-mbam-25-server-feature-configuration.md)


## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






