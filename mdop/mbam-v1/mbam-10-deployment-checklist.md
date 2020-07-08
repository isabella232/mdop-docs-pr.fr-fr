---
title: Liste de contrôle du déploiement de MBAM1.0
description: Liste de contrôle du déploiement de MBAM1.0
author: dansimp
ms.assetid: 7e00be23-36a0-4b0f-8663-3c4f2c71546d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 96725183af2cb4e3d86d3f42973452c598497773
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804302"
---
# Liste de contrôle du déploiement de MBAM1.0


Cette liste de vérification a été conçue pour faciliter le déploiement de l’administration et de la surveillance de Microsoft BitLocker (MBAM).

**Remarque**  
Cette liste de vérification souligne les étapes recommandées et fournit une liste de haut niveau des éléments à prendre en compte lorsque vous déployez les fonctionnalités de MBAM. Nous vous recommandons de copier cette liste de vérification dans un tableur et de la personnaliser en fonction de vos besoins spécifiques.



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
<td align="left"><p><a href="mbam-10-planning-checklist.md" data-raw-source="[MBAM 1.0 Planning Checklist](mbam-10-planning-checklist.md)">Liste de contrôle de la planification de MBAM1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Passez en revue les informations sur les configurations prises en charge par MBAM pour vous assurer que les ordinateurs client et serveur sélectionnés sont pris en charge pour l’installation de la fonctionnalité MBAM.</p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)">Configurations prises en charge par MBAM1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Exécutez le programme d’installation de MBAM pour déployer les fonctionnalités du serveur MBAM dans l’ordre suivant:</p>
<ol>
<li><p>Base de données de récupération et de matériel</p></li>
<li><p>Base de données état de conformité</p></li>
<li><p>Rapports et audit de conformité</p></li>
<li><p>Serveur d’administration et de surveillance</p></li>
<li><p>Modèle de stratégie de groupe MBAM</p></li>
</ol>
<div class="alert">
<strong>Remarque</strong><br/><p>Assurez le suivi des noms de chaque serveur sur lequel chaque fonctionnalité est installée. Vous utiliserez ces informations tout au long du processus d’installation.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-10-server-infrastructure.md" data-raw-source="[Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md)">Déploiement de l'infrastructure de serveur MBAM1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ajoutez des groupes de sécurité des services de domaine Active Directory créés lors de la phase de planification aux groupes d’administrateurs de fonctionnalités de serveur local MBAM appropriés sur les serveurs appropriés.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Planification des rôles d’administrateur MBAM 1,0 </a> et <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Comment gérer les rôles d’administrateur MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Créez et déployez les objets de stratégie de groupe MBAM requis.</p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)">Déploiement d'objets de stratégie de groupe MBAM1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Déployez le logiciel client MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)">Déploiement du client MBAM1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Rubriques connexes


[Déploiement de MBAM1.0](deploying-mbam-10.md)









