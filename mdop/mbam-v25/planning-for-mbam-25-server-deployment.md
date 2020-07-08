---
title: Planification du déploiement de serveursMBAM2.5
description: Planification du déploiement de serveursMBAM2.5
author: dansimp
ms.assetid: 88774c89-31c8-4eb8-a845-a00bbec8c870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2ecb510fab821118ce210577f9ffb83c39be050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811621"
---
# Planification du déploiement de serveursMBAM2.5


Cette rubrique répertorie les fonctionnalités que vous déployez pour les topologies autonomes et de gestionnaire de configuration MBAM et indique l’ordre dans lequel vous devez les déployer. Il existe une configuration recommandée pour chaque topologie. Toutefois, vous pouvez configurer les fonctionnalités et bases de données serveur MBAM dans différentes configurations et sur plusieurs serveurs, en fonction de vos besoins en matière d’évolutivité.

## Remarques importantes en matière de planification pour les deux topologies


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Concernant</th>
<th align="left">Détails ou objectif</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Passez en revue les éléments suivants avant de commencer le déploiement:</p>
<ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurations prises en charge par MBAM2.5</a></p></li>
</ul></td>
<td align="left"><p>Chaque fonctionnalité MBAM comporte des éléments requis spécifiques qui doivent être satisfaits avant de démarrer l’installation d’MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Les clés de récupération BitLocker dans MBAM expirent après une utilisation unique.</p></td>
<td align="left"><p>Une utilisation unique signifie que la clé de récupération a été récupérée via le site Web d’administration et de contrôle (également appelé support technique), portail libre-service ou à l’aide de l’applet de contrôle <strong> Windows PowerShell Get-MbamBitLockerRecoveryKey </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Assurez le suivi des noms des ordinateurs sur lesquels vous configurez chaque fonctionnalité. Vous utiliserez ces informations tout au long du processus de configuration.</p></td>
<td align="left"><p>Vous pouvez utiliser la <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"> liste de vérification de déploiement de MBAM 2,5 </a> à cette fin.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurez uniquement les paramètres de stratégie de groupe du nœud MDOP MBAM (gestion BitLocker). Ne modifiez pas les paramètres de stratégie de groupe du nœud BitLocker Drive Encryption.</p></td>
<td align="left"><p>Si vous modifiez les paramètres de stratégie de groupe dans le nœud BitLocker Drive Encryption, MBAM ne fonctionnera pas.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="planning-for-mbam-server-deployment---stand-alone-topology"></a>Planification du déploiement de MBAM Server-topologie autonome


Dans le cas d’une topologie autonome, il est recommandé de configurer deux serveurs pour les environnements de production, même si les configurations de trois à quatre serveurs peuvent être utilisées.

L’infrastructure de serveur pour la topologie autonome MBAM contient les fonctionnalités suivantes, qui doivent être configurées dans l’ordre indiqué:

1.  Bases de données (bases de données d’audit et de conformité)

2.  Rapports

3.  Applications Web (et leurs services Web correspondants)

    -   Site Web d’administration et de surveillance

    -   Portail libre-service

Pour obtenir une description de ces fonctionnalités, voir [architecture de niveau supérieur de MBAM 2,5 avec topologie autonome](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).

## <a href="" id="planning-for-mbam-server-deployment---configuration-manager-topology"></a>Planification du déploiement de MBAM Server – topologie de Configuration Manager


Pour la topologie d’intégration de Configuration Manager, une configuration à trois serveurs est recommandée pour les environnements de production, même si des configurations de serveurs supplémentaires peuvent être utilisées.

L’infrastructure de serveur pour la topologie du gestionnaire de configuration MBAM contient les fonctionnalités suivantes, qui doivent être configurées ou exécutées dans l’ordre indiqué:

1.  Bases de données (bases de données d’audit et de conformité)

2.  Rapports

3.  Applications Web (et leurs services Web correspondants)

    -   Site Web d’administration et de surveillance

    -   Portail libre-service

4.  Intégration de System Center Configuration Manager

Pour obtenir une description de ces fonctionnalités, voir [architecture de niveau supérieur de MBAM 2,5 avec topologie d’intégration de Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).



## Rubriques connexes


[Planification du déploiement de MBAM2.5](planning-to-deploy-mbam-25.md)

[Déploiement de l'infrastructure de serveur MBAM2.5](deploying-the-mbam-25-server-infrastructure.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





