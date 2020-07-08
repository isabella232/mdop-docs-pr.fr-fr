---
title: Comment configurer les bases de données MBAM2.5
description: Comment configurer les bases de données MBAM2.5
author: dansimp
ms.assetid: 66e1c81b-f785-4398-9175-bb5f112c2a35
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c11cb58d8fd9266bd0322e4cf9aa96256b7fbb6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811867"
---
# Comment configurer les bases de données MBAM2.5


Cet article décrit la configuration de la base de données de compatibilité et d’audit de Microsoft BitLocker (MBAM 2,5) et de la base de données d’audit et de la base de données de récupération en utilisant les éléments suivants:

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
<td align="left"><p>Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous envisagez de configurer une fonctionnalité de MBAM Server.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Vous pouvez installer les bases de données sur un ordinateur distant SQL Server à l’aide de Windows PowerShell ou d’un package d’application de couche de données (DAC) exporté. Pour plus d’informations sur les packages DAC, voir <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> applications à couches de données </a> .</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installation du logiciel serveur MBAM2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Passez en revue la configuration requise pour l’utilisation de Windows PowerShell Si vous envisagez d’utiliser des cmdlets Windows PowerShell pour configurer les fonctionnalités du serveur MBAM.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Pour configurer la base de données à l’aide de Windows PowerShell**

1.  Avant de commencer la configuration, reportez-vous à la rubrique [Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) pour consulter les conditions préalables à l’utilisation de Windows PowerShell.

2.  Utilisez l’applet de cmdlet Windows PowerShell **Enable-MbamDatabase** pour configurer les bases de données. Pour obtenir des informations sur cette applet de cmdlet Windows PowerShell, tapez **Get-Help-MbamDatabase**.

**Pour configurer la conformité et la base de données d’audit à l’aide de l’Assistant**

1. Sur le serveur sur lequel vous voulez configurer les bases de données, démarrez l’Assistant **configuration de MBAM Server** . Vous pouvez sélectionner **MBAM de configuration de serveur** dans le menu **Démarrer** pour ouvrir l’Assistant.

2. Cliquez **sur Ajouter de nouvelles fonctionnalités**, sélectionnez **conformité et audit** et **base**de données d’audit, puis cliquez sur **suivant**. L’Assistant vérifie que toutes les conditions préalables pour les bases de données sont remplies.

3. Si la vérification de la configuration requise est réussie, cliquez sur **suivant** pour continuer. Dans le cas contraire, résolvez les conditions préalables manquantes, puis cliquez **à nouveau sur vérifier les conditions préalables**.

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
   <td align="left"><p><strong>Nom SQL Server</strong></p></td>
   <td align="left"><p>Nom du serveur sur lequel vous configurez la base de données d’audit et de conformité.</p>
   <div class="alert">
   <strong>Remarque</strong><br/><p>Vous devez ajouter une exception dans l’ordinateur de la base de données d’audit et de conformité pour activer le trafic entrant sur le port Microsoft SQL Server. Le numéro de port par défaut est 1433.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Instance de base de données SQL Server</strong></p></td>
   <td align="left"><p>Nom de l’instance de base de données dans laquelle les données d’audit et de conformité seront stockées. Vous devez également spécifier l’emplacement des informations de la base de données.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Nom de la base de données</strong></p></td>
   <td align="left"><p>Nom de la base de données qui stockera les données de conformité.</p>
   <div class="alert">
   <strong>Remarque</strong><br/><p>Si vous effectuez une mise à niveau à partir d’une version précédente de MBAM, vous devez utiliser le même nom de base de données que le nom utilisé dans votre ancien déploiement.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Utilisateur ou groupe d’accès en lecture/écriture</strong></p></td>
   <td align="left"><p>Utilisateur ou groupe ayant une autorisation en lecture/écriture à cette base de données pour permettre aux applications Web d’accéder aux données et rapports de cette base de données.</p>
   <p>Si vous entrez un utilisateur dans ce champ, il doit avoir la même valeur que la valeur figurant dans le <strong> champ compte de domaine du pool d’applications de service Web </strong> de la <strong> page configurer des applications Web </strong> .</p>
   <p>Si vous entrez un groupe dans ce champ, la valeur du <strong> champ compte de domaine du pool d’applications de service Web </strong> de la <strong> page configurer des applications Web </strong> doit être membre du groupe que vous entrez dans ce champ.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Utilisateur ou groupe d’accès en lecture seule</strong></p></td>
   <td align="left"><p>Nom de l’utilisateur ou du groupe disposant d’une autorisation en lecture seule sur cette base de données pour permettre aux rapports d’accéder aux données de conformité de cette base de données.</p>
   <p>Si vous entrez un utilisateur dans ce champ, il doit être le même que celui que vous avez spécifié dans le <strong> champ domaine de la base de données de conformité et d’audit </strong> de la <strong> page configurer des rapports </strong> .</p>
   <p>Si vous entrez un groupe dans ce champ, la valeur que vous spécifiez dans le <strong> champ compte de domaine de la base de données de conformité et d’audit </strong> de la <strong> page configurer des rapports </strong> doit être membre du groupe que vous spécifiez dans ce champ.</p></td>
   </tr>
   </tbody>
   </table>



5. Passez à la section suivante pour configurer la base de données de récupération.

**Pour configurer la base de données de récupération à l’aide de l’Assistant**

1. À l’aide des descriptions suivantes, entrez les valeurs de champ dans l’Assistant:

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
   <td align="left"><p><strong>Nom SQL Server</strong></p></td>
   <td align="left"><p>Nom du serveur sur lequel vous configurez la base de données de récupération.</p>
   <div class="alert">
   <strong>Remarque</strong><br/><p>Vous devez ajouter une exception sur l’ordinateur de base de données de récupération pour activer le trafic entrant sur le port Microsoft SQL Server. Le numéro de port par défaut est 1433.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Instance de base de données SQL Server</strong></p></td>
   <td align="left"><p>Nom de l’instance de base de données dans laquelle les données de récupération seront stockées. Vous devez également spécifier l’emplacement des informations de la base de données.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Nom de la base de données</strong></p></td>
   <td align="left"><p>Nom de la base de données qui stockera les données de récupération.</p>
   <div class="alert">
   <strong>Remarque</strong><br/><p>Si vous effectuez une mise à niveau à partir d’une version précédente de MBAM, vous devez utiliser le même nom de base de données que le nom utilisé dans votre ancien déploiement.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Utilisateur ou groupe d’accès en lecture/écriture</strong></p></td>
   <td align="left"><p>Utilisateur ou groupe ayant une autorisation en lecture/écriture à cette base de données pour permettre aux applications Web d’accéder aux données et rapports de cette base de données.</p>
   <p>Si vous entrez un utilisateur dans ce champ, il doit avoir la même valeur que la valeur figurant dans le <strong> champ compte de domaine du pool d’applications de service Web </strong> de la <strong> page configurer des applications Web </strong> .</p>
   <p>Si vous entrez un groupe dans ce champ, la valeur du <strong> champ compte de domaine du pool d’applications de service Web </strong> de la <strong> page configurer des applications Web </strong> doit être membre du groupe que vous entrez dans ce champ.</p></td>
   </tr>
   </tbody>
   </table>



2. Lorsque vous avez terminé, cliquez sur **suivant**.

   L’Assistant vérifie que toutes les conditions préalables pour les bases de données sont remplies.

3. Si la vérification de la configuration requise est réussie, cliquez sur **suivant** pour continuer. Dans le cas contraire, résolvez les conditions préalables manquantes, puis cliquez de nouveau sur **suivant** .

4. Dans la page **Résumé** , passez en revue les fonctionnalités qui seront ajoutées.

   **Remarque**  
   Pour créer un script Windows PowerShell des entrées que vous venez de créer, cliquez sur **Exporter le script PowerShell**, puis enregistrez le script.



5. Cliquez sur **Ajouter** pour ajouter les bases de données MBAM sur le serveur, puis cliquez sur **Fermer**.



## Rubriques connexes


[Journaux des événements serveur](server-event-logs.md)

[Configuration des composants du serveur MBAM2.5](configuring-the-mbam-25-server-features.md)

[Configuration des rapports MBAM2.5](how-to-configure-the-mbam-25-reports.md)

[Comment configurer les applications Web MBAM2.5](how-to-configure-the-mbam-25-web-applications.md)

[Validation de la configuration des composants serveur de MBAM2.5](validating-the-mbam-25-server-feature-configuration.md)



## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





