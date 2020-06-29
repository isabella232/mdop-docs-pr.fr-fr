---
title: Évaluation de MBAM2.0
description: Évaluation de MBAM2.0
author: dansimp
ms.assetid: bfc77eec-0fd7-4fec-9c78-6870afa87152
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7be883f44f5f09a904f619972ae3e7c35261d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810734"
---
# Évaluation de MBAM2.0


Avant de déployer l’administration et la surveillance de Microsoft BitLocker (MBAM) dans un environnement de production, vous devez l’évaluer dans un environnement de test. Les informations contenues dans cette rubrique peuvent être utilisées pour configurer l’administration et la surveillance de Microsoft BitLocker à l’aide d’une topologie autonome dans un environnement de test serveur unique à des fins d’évaluation uniquement. Une topologie sur un seul serveur n’est pas recommandée dans les environnements de production.

Pour obtenir des instructions sur le déploiement de MBAM dans un environnement de test, voir [Comment installer et configurer MBAM sur un seul serveur](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).

## Configuration de l’environnement de test


Même si vous configurez une instance de MBAM qui n’est pas de production et qu’elle évalue dans un environnement de test, vous devez vérifier que vous remplissez bien les conditions préalables et matérielles et logicielles requises. Avant de commencer l’installation, consultez la configuration requise pour le [déploiement d’MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md), les [Configurations prises en charge par MBAM 2,0](mbam-20-supported-configurations-mbam-2.md)et [la préparation de votre environnement pour MBAM 2,0](preparing-your-environment-for-mbam-20-mbam-2.md).

### Planifier un déploiement d’une évaluation MBAM

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
<td align="left"><p>Passez en revue les informations de prise en main de MBAM pour en savoir plus sur le produit avant de commencer la planification du déploiement.</p></td>
<td align="left"><p><a href="getting-started-with-mbam-20-mbam-2.md" data-raw-source="[Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)">Prise en main de MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planifiez les prérequis de déploiement d’MBAM 2,0 et préparez votre environnement informatique.</p></td>
<td align="left"><p><a href="mbam-20-deployment-prerequisites-mbam-2.md" data-raw-source="[MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md)">Conditions préalables au déploiement de MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planifiez et configurez les exigences de stratégie de groupe MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Planification des exigences en matière de stratégie de groupe MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Planifiez et créez des groupes de sécurité ActiveDirectoryDomainServices nécessaires et planifiez les exigences d’appartenance au groupe de sécurité local MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planification des rôles administrateur de MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Plan de déploiement de la fonctionnalité de déploiement de MBAM Server.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-server-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md)">Planification du déploiement de serveursMBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Plan de déploiement du déploiement du client MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)">Planification du déploiement de clients MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

### Effectuer un déploiement d’évaluation MBAM

Après avoir effectué les installations de planification et de configuration logicielles requises pour préparer votre environnement informatique pour l’installation d’MBAM, vous pouvez commencer le déploiement d’évaluation d’MBAM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Passez en revue les informations de configurations prises en charge par MBAM pour vous assurer que les ordinateurs client et serveur sélectionnés sont pris en charge pour l’installation de la fonctionnalité MBAM.</p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Configurations prises en charge par MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Exécutez le programme d’installation de MBAM pour déployer les fonctionnalités serveur MBAM sur un serveur unique à des fins d’évaluation.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)">Installation et configuration de MBAM sur un seul serveur</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ajoutez des groupes de sécurité ActiveDirectoryDomainServices, que vous avez créés lors de la phase de planification, aux groupes locaux du serveur MBAM local appropriés sur le nouveau serveur MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planification des rôles d’administrateur MBAM 2,0 </a> et <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Comment gérer les rôles d’administrateur MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Créer et déployer des objets de stratégie de groupe MBAM requis.</p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)">Déploiement d'objets de stratégie de groupe MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Déployez le logiciel client MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)">Déploiement du client MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## Configurer les ordinateurs de laboratoire pour l’évaluation de MBAM


Cette section contient des informations qui peuvent être utilisées pour accélérer la création de rapports d’État du client MBAM. Toutefois, ces modifications doivent être utilisées uniquement à des fins de test.

**Remarques**  Les informations de la section suivante décrivent comment modifier le Registre Windows. L’utilisation de l’éditeur du Registre peut être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows. Microsoft ne peut pas garantir que les problèmes résultant de l’utilisation incorrecte de l’éditeur du Registre peuvent être résolus. Utilisez l’éditeur du Registre à vos propres risques.

 

### Modifier les paramètres de fréquence des rapports d’État du client MBAM

Les fréquences de rapport d’État et de réveil du client MBAM ont une valeur minimale de 90 minutes lorsqu’elles sont définies à l’aide d’une stratégie de groupe. Vous pouvez utiliser le registre de Windows pour changer ces fréquences en une valeur inférieure sur les ordinateurs clients MBAM pour accélérer les tests.

Pour modifier les paramètres de fréquence des rapports d’État du client MBAM:

1.  Utilisez un éditeur du Registre pour accéder à **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.

2.  Modifiez les valeurs de **ClientWakeupFrequency** et **StatusReportingFrequency** sur **1** comme valeur prise en charge par le client minimum. Cette modification entraîne le rapport de chaque minute par le client MBAM.

3.  Redémarrez le **service client de gestion BitLocker**.

**Remarques**  Pour définir des valeurs dont le niveau est faible, vous devez les définir manuellement dans le registre.

 

### Modifier le délai de démarrage du service client MBAM

En plus des fréquences de création de rapports d’État et de réveil du client MBAM, il existe un délai aléatoire de maximum de 90 minutes lorsque le service d’agent client MBAM démarre sur les ordinateurs clients. Si vous ne souhaitez pas utiliser le délai aléatoire, créez une valeur **DWORD** de **NoStartupDelay** sous **HKLM\\Software\\Microsoft\\MBAM**, définissez sa valeur sur **1**, puis redémarrez le **service client de gestion BitLocker**.

## Rubriques connexes


[Prise en main de MBAM2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





