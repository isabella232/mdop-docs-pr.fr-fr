---
title: Fonctionnalités courantes de l'onglet secondaire
description: Fonctionnalités courantes de l'onglet secondaire
author: dansimp
ms.assetid: 44a15c28-944c-49c1-8534-115ce1c362ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546fd4c91e060a5595b6c848015290882de933b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807766"
---
# Fonctionnalités courantes de l'onglet secondaire


Chaque onglet secondaire comporte deux sections:**objets** et **groupes de stratégie de**groupe.

## Section objets de stratégie de groupe


La section **objets de stratégie de groupe** affiche la liste filtrée d’objets de stratégie de groupe et identifie les caractéristiques suivantes pour chaque GPO:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Caractéristique de l’objet GPO</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Name</strong></p></td>
<td align="left"><p>Nom de l’objet de stratégie de groupe.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Ordinateur (COMP.)</strong></p></td>
<td align="left"><p>Version générée automatiquement de la partie configuration de l’ordinateur de l’objet de stratégie de groupe.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Utilisateur</strong></p></td>
<td align="left"><p>Version générée automatiquement de la section Configuration utilisateur de l’objet de stratégie de groupe.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>État</strong></p></td>
<td align="left"><p>État de l’objet de stratégie de groupe sélectionné:</p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong>Non contrôlé: </strong> non géré par AGPM.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>Archivé: </strong> disponible pour les éditeurs autorisés à vérifier en modification ou à un administrateur de stratégie de groupe pour procéder au déploiement.</p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong>Extrait: </strong> actuellement modifié. Non disponible pour les autres éditeurs pour le contrôle tant que l’éditeur qui l’a réintégré ou un administrateur AGPM l’a archivé.</p>
<p><img src="images/0840a6a3-54a6-4528-98a9-7b122243c1a5.gif" alt="Pending GPO icon" /> <strong>En attente: en </strong> attente d’approbation d’un administrateur de stratégie de groupe avant de créer, contrôler, déployer ou supprimer.</p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong>Supprimé: </strong> supprimé de l’archive, mais peut toujours être restauré.</p>
<p><img src="images/9b65829d-253c-4f30-9295-c816a6521ed2.gif" alt="Template icon" /> <strong>Modèle: </strong> version statique d’un objet de stratégie de groupe à utiliser comme point de départ lors de la création de nouveaux objets de stratégie de groupe.</p>
<p><img src="images/cd349b8d-c4d8-45ff-b17f-7db882502c58.gif" alt="Default template icon" /> <strong>Modèle (par défaut): </strong> par défaut, ce modèle est le point de départ utilisé lors de la création d’un objet de stratégie de groupe.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>État de l’objet GPO</strong></p></td>
<td align="left"><p>La configuration de l’ordinateur et la configuration de l’utilisateur peuvent être gérées séparément. L’état de l’objet de stratégie de groupe indique quelles parties de l’objet de stratégie de groupe sont activées.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Filtre WMI</strong></p></td>
<td align="left"><p>Afficher les filtres WMI appliqués à cet objet GPO. Les filtres WMI sont gérés par le <strong> nœud filtres WMI </strong> pour le domaine dans l’arborescence de la console GPMC.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Modifié</strong></p></td>
<td align="left"><p>S’il s’agit d’un objet de stratégie de groupe contrôlé, date la plus récente lors de sa modification ou de son extraction. S’il s’agit d’un objet de stratégie de groupe non contrôlé, date de la dernière modification.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Propriétaire</strong></p></td>
<td align="left"><p>Éditeur ayant archivé l’objet de stratégie de groupe et l’approbateur qui l’a déployé.</p></td>
</tr>
</tbody>
</table>

 

## Section groupes et utilisateurs


Lorsqu’un objet de stratégie de groupe est sélectionné, la section **groupes et utilisateurs** affiche une liste des groupes et des utilisateurs ayant accès à cet objet. Les autorisations et l’héritage autorisés sont affichés pour chaque groupe ou utilisateur. Un administrateur AGPM peut configurer les autorisations à l’aide de rôles AGPM standard (éditeur, approbateur et relecteur) ou d’une combinaison personnalisée d’autorisations.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Bouton</th>
<th align="left">Effet</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Add</strong></p></td>
<td align="left"><p>Ajoutez une nouvelle entrée au descripteur de sécurité. Tout utilisateur ou groupe dans Active Directory peut être ajouté.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Supprimer</strong></p></td>
<td align="left"><p>Supprimer l’entrée sélectionnée de la liste de contrôle d’accès.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Propriétés</strong></p></td>
<td align="left"><p>Afficher les propriétés de l’objet sélectionné. La page Propriétés est la même que celle affichée pour un objet dans <strong> utilisateurs et ordinateurs Active Directory </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Avancé</strong></p></td>
<td align="left"><p>Ouvrez l' <strong> éditeur de liste de contrôle d’accès </strong> .</p></td>
</tr>
</tbody>
</table>

 

### Autres éléments à prendre en considération

-   Pour plus d’informations sur les rôles et les autorisations liées à des tâches spécifiques, voir les tâches d' [exécution des tâches d’administration d’AGPM](performing-agpm-administrator-tasks.md), exécution de tâches d' [éditeur](performing-editor-tasks.md), [exécution des tâches approbateurs](performing-approver-tasks.md)et [exécution des tâches de relecteur](performing-reviewer-tasks.md).

### Références supplémentaires

-   [Onglet Contenu](contents-tab.md)

 

 





