---
title: Liste de contrôle de la planification de MBAM2.5
description: Liste de contrôle de la planification de MBAM2.5
author: dansimp
ms.assetid: ffe11eb8-44db-4886-8300-6dffec8bcfa4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 505f2890d67f36056ab5bb87df2a894473cd3306
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811819"
---
# Liste de contrôle de la planification de MBAM2.5


Vous pouvez utiliser les listes de vérification suivantes pour vous aider à préparer votre environnement informatique pour le déploiement de Microsoft BitLocker administration et de la surveillance (MBAM). Les listes de vérification fournissent une liste de haut niveau des éléments à prendre en compte lors de la planification du déploiement. Il existe des listes de vérification distinctes pour la topologie autonome et la topologie d’intégration de Configuration Manager. Vous souhaiterez peut-être copier la liste de vérification souhaitée dans une feuille de calcul et la personnaliser pour votre utilisation.

**Liste de contrôle de planification pour un déploiement MBAM**

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
<td align="left"><p>Passez &quot; en revue les &quot; informations de mise en route pour comprendre le produit avant de commencer la planification du déploiement.</p></td>
<td align="left"><p><a href="getting-started-with-mbam-25.md" data-raw-source="[Getting Started with MBAM 2.5](getting-started-with-mbam-25.md)">Prise en main de MBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Passez en revue l’architecture de haut niveau recommandée pour un déploiement MBAM. Vous voudrez peut-être également consulter une illustration et une description des différents composants (bases de données, sites Web, rapports) d’un déploiement MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Architecture de hautniveau pour MBAM2.5</a></p>
<p><a href="illustrated-features-of-an-mbam-25-deployment.md" data-raw-source="[Illustrated Features of an MBAM 2.5 Deployment](illustrated-features-of-an-mbam-25-deployment.md)">Illustration des composants d'un déploiement de MBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Passez en revue et remplissez les conditions préalables pour les topologies d’intégration de configuration autonome et de configuration de MBAM.</p></td>
<td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Si vous envisagez d’utiliser la topologie d’intégration de Configuration Manager, remplissez les conditions préalables supplémentaires qui s’appliquent uniquement à cette topologie.</p></td>
<td align="left"><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Reportez-vous aux conditions préalables sur MBAM 2,5 pour le client MBAM.</p></td>
<td align="left"><p><a href="prerequisites-for-mbam-25-clients.md" data-raw-source="[Prerequisites for MBAM 2.5 Clients](prerequisites-for-mbam-25-clients.md)">Conditions préalables pour les clients MBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planifiez et configurez les exigences de stratégie de groupe MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)">Planification des exigences en matière de stratégie de groupe MBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planifiez et créez les groupes de sécurité ActiveDirectoryDomainServices nécessaires.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-groups-and-accounts.md" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md)">Planification des comptes et groupes MBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planifiez le mode de sécurisation des sites Web MBAM.</p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md)">Planification de la sécurisation des sites web MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Passez en revue les configurations prises en charge par MBAM pour vous assurer que votre matériel répond à la configuration système requise pour l’installation.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurations prises en charge par MBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Passez en revue les éléments à prendre en compte pour déployer les fonctionnalités du serveur MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-server-deployment.md" data-raw-source="[Planning for MBAM 2.5 Server Deployment](planning-for-mbam-25-server-deployment.md)">Planification du déploiement de serveursMBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Prenez connaissance des considérations relatives au déploiement du client MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-client-deployment.md" data-raw-source="[Planning for MBAM 2.5 Client Deployment](planning-for-mbam-25-client-deployment.md)">Planification du déploiement de clients MBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Passez en revue la configuration requise et les étapes de déploiement d’MBAM dans une configuration très disponible.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-high-availability.md" data-raw-source="[Planning for MBAM 2.5 High Availability](planning-for-mbam-25-high-availability.md)">Planification de la haute disponibilité de MBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Passez en revue les considérations en matière de sécurité MBAM relatives au module de plateforme sécurisée, aux fichiers journaux et au chiffrement de données transparent.</p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)">Considérations relatives à la sécurité pour MBAM2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Vous pouvez également consulter la procédure d’évaluation de MBAM dans un environnement de test.</p></td>
<td align="left"><p><a href="evaluating-mbam-25-in-a-test-environment.md" data-raw-source="[Evaluating MBAM 2.5 in a Test Environment](evaluating-mbam-25-in-a-test-environment.md)">Évaluation de MBAM2.5 dans un environnement de test</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 


## Rubriques connexes


[Planification de MBAM2.5](planning-for-mbam-25.md)

 

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




