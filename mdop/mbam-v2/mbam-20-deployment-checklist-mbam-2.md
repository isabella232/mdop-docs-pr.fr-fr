---
title: Liste de contrôle du déploiement de MBAM2.0
description: Liste de contrôle du déploiement de MBAM2.0
author: dansimp
ms.assetid: 7905d31d-f21c-4683-b9c4-95b815e08fab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d8d0ce1a3ff48d4bf2f84e61b4a578b170264a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811754"
---
# Liste de contrôle du déploiement de MBAM2.0


Cette liste de vérification peut être utilisée pour vous aider lors du déploiement de Microsoft BitLocker administration et de la surveillance (MBAM) avec une topologie autonome.

**Remarque**  
Cette liste de vérification décrit les étapes recommandées et une liste générale des éléments à prendre en compte lors du déploiement des fonctionnalités d’administration et de surveillance de Microsoft BitLocker. Il est recommandé de copier cette liste de vérification dans un tableur et de la personnaliser pour votre utilisation.



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
<td align="left"><p>Achevez la phase de planification pour préparer l’environnement informatique pour le déploiement de MBAM.</p></td>
<td align="left"><p><a href="mbam-20-planning-checklist-mbam-2.md" data-raw-source="[MBAM 2.0 Planning Checklist](mbam-20-planning-checklist-mbam-2.md)">Liste de contrôle de la planification de MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Passez en revue les informations de configurations prises en charge par MBAM pour vous assurer que les ordinateurs client et serveur sélectionnés sont pris en charge pour l’installation de la fonctionnalité MBAM.</p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Configurations prises en charge par MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Exécutez le programme d’installation de MBAM pour déployer les fonctionnalités du serveur MBAM dans l’ordre suivant:</p>
<ol>
<li><p>Base de données de récupération</p></li>
<li><p>Base de données d’audit et de conformité</p></li>
<li><p>Rapports et audit de conformité</p></li>
<li><p>Serveur libre-service</p></li>
<li><p>Serveur d’administration et de surveillance</p></li>
<li><p>Modèle de stratégie de groupe MBAM</p></li>
</ol>
<div class="alert">
<strong>Remarque</strong><br/><p>Assurez le suivi des noms de chaque serveur sur lequel chaque fonctionnalité est installée. Ces informations seront utilisées tout au long du processus d’installation.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-20-server-infrastructure-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md)">Déploiement de l'infrastructure de serveur MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ajoutez des groupes de sécurité des services de domaine Active Directory créés lors de la phase de planification aux groupes d’administrateurs de fonctionnalités de serveur local MBAM appropriés sur les serveurs appropriés.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Planification des rôles d’administrateur MBAM 2,0 </a> et <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Comment gérer les rôles d’administrateur MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Créer et déployer des objets de stratégie de groupe MBAM requis.</p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)">Déploiement d'objets de stratégie de groupe MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Déployez le logiciel client MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)">Déploiement du client MBAM2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Rubriques connexes


[Déploiement de MBAM2.0](deploying-mbam-20-mbam-2.md)









