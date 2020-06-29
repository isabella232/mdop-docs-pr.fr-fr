---
title: Liste de contrôle du déploiement de MBAM2.5
description: Liste de contrôle du déploiement de MBAM2.5
author: dansimp
ms.assetid: 2ba7de17-e3a4-4798-99e0-cd1dc28c5b76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11609b3d6d44d62b032e35005e5d967ca6d4e83b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809593"
---
# Liste de contrôle du déploiement de MBAM2.5


Vous pouvez utiliser cette liste de contrôle pour vous aider lors du déploiement de Microsoft BitLocker administration et de la surveillance (MBAM) avec une topologie autonome.

**Remarque**  
Cette liste de vérification décrit les étapes recommandées et une liste générale des éléments à prendre en compte lorsque vous déployez les fonctionnalités d’administration et de surveillance de Microsoft BitLocker. Nous vous recommandons de copier cette liste de vérification dans un tableur et de la personnaliser pour votre utilisation.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Tâche</th>
<th align="left">Références</th>
<th align="left">Remarques</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Passez en revue et effectuez toutes les étapes de planification pour préparer votre environnement pour le déploiement de MBAM.</p></td>
<td align="left"><p><a href="mbam-25-planning-checklist.md" data-raw-source="[MBAM 2.5 Planning Checklist](mbam-25-planning-checklist.md)">Liste de contrôle de la planification de MBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Passez en revue les informations de configurations prises en charge pour vous assurer que MBAM prend en charge les ordinateurs client et serveur sélectionnés.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurations prises en charge par MBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Installez le logiciel serveur MBAM.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installation du logiciel serveur MBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Configurer les fonctionnalités du serveur MBAM:</p>
<ul>
<li><p>Conformité et audit de la base de données et de la base de données de récupération</p></li>
<li><p>Rapports</p></li>
<li><p>Applications Web</p></li>
<li><p>Topologie d’intégration de Configuration Manager (requis uniquement si vous exécutez MBAM avec cette topologie)</p></li>
</ul>
<div class="alert">
<strong>Remarque</strong><br/><p>Notez les noms des serveurs sur lesquels vous configurez chaque fonctionnalité. Vous utiliserez ces informations tout au long du processus de configuration.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="configuring-the-mbam-25-server-features.md" data-raw-source="[Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md)">Configuration des composants du serveur MBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Validez la configuration MBAM.</p></td>
<td align="left"><p><a href="validating-the-mbam-25-server-feature-configuration.md" data-raw-source="[Validating the MBAM 2.5 Server Feature Configuration](validating-the-mbam-25-server-feature-configuration.md)">Validation de la configuration des composants serveur de MBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Copiez le modèle de stratégie de groupe MBAM et modifiez les paramètres de stratégie de groupe.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Copie des modèles de stratégie de groupe MBAM 2,5 </a> et <a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"> modification des paramètres de stratégie de groupe MBAM 2,5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Déployez le logiciel client MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-25-client.md" data-raw-source="[Deploying the MBAM 2.5 Client](deploying-the-mbam-25-client.md)">Déploiement du client MBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>




## Rubriques connexes


[Déploiement de MBAM2.5](deploying-mbam-25.md)




## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




