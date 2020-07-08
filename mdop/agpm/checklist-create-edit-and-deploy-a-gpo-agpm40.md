---
title: 'Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe'
description: 'Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe'
author: dansimp
ms.assetid: 44631bed-16d2-4b5a-af70-17a73fb5f6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d8bea9109040aa81a20df62356ef1d307d5eac0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807773"
---
# Liste de contrôle: créer, modifier et déployer un objet de stratégie de groupe


Dans un environnement dans lequel plusieurs personnes modifient les objets de stratégie de groupe (GPO) en utilisant la gestion avancée des stratégies de groupe (AGPM), un administrateur AGPM (contrôle total) délègue les autorisations à des éditeurs, approbateurs et réviseurs en tant que groupes ou personnes. Vous trouverez ci-après un processus standard de développement d’objets de stratégie de groupe pour un éditeur et un approbateur.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche</th>
<th align="left">Référence</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>L’éditeur demande la création d’un objet de stratégie de groupe ou l’approbation d’un nouvel objet de stratégie de groupe.</p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm40.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm40.md)">Demander la création d'un objet de stratégie de groupe contrôlé</a></p>
<p><a href="create-a-new-controlled-gpo-agpm40.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md)">Créer un objet de stratégie de groupe contrôlé</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>L’Approbateur approuve la création de l’objet de stratégie de groupe s’il a été demandé par un éditeur.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)">Approuver ou rejeter une action en attente</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>L’éditeur récupère une copie de l’objet de stratégie de groupe à partir de l’archive afin que personne d’autre ne puisse modifier l’objet GPO. L’éditeur apporte des modifications à l’objet GPO, puis vérifie l’objet GPO modifié dans l’archive.</p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm40.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm40.md)">Modifier un objet de stratégie de groupe hors connexion</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Si vous développez dans une forêt de test, l’éditeur exporte l’objet GPO vers un fichier, transfère le fichier dans la forêt de production et importe le fichier. Par ailleurs, un éditeur peut lier l’objet de stratégie de groupe à une unité d’organisation qui contient des ordinateurs et des utilisateurs de test.</p></td>
<td align="left"><p><a href="using-a-test-environment.md" data-raw-source="[Using a Test Environment](using-a-test-environment.md)">Utilisation d'un environnement de test</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>L’éditeur demande le déploiement de l’objet de stratégie de groupe dans l’environnement de production du domaine.</p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm40.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm40.md)">Demander le déploiement d'un objet de stratégie de groupe</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Les réviseurs, tels que les approbateurs ou les éditeurs, analysent l’objet de stratégie de groupe.</p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm40.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md)">Exécution de tâches de réviseur</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>L’Approbateur approuve et déploie l’objet de stratégie de groupe dans l’environnement de production du domaine ou rejeter l’objet de stratégie de groupe.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)">Approuver ou rejeter une action en attente</a></p></td>
</tr>
</tbody>
</table>

 

### Références supplémentaires

[Gestion avancée des stratégies de groupe4.0](advanced-group-policy-management-40.md)

 

 





