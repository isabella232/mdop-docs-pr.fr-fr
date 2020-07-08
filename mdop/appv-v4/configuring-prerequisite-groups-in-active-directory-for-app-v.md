---
title: Configuration des groupes prérequis dans Active Directory pour App-V
description: Configuration des groupes prérequis dans Active Directory pour App-V
author: dansimp
ms.assetid: 0010d534-46c0-44a3-b5c1-621b4d5e2c31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa1ab6393dee20203b715311d4e1dfdc4c22c679
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809011"
---
# Configuration des groupes prérequis dans Active Directory pour App-V


Avant d’installer le serveur de gestion Microsoft Application Virtualization (App-V), vous devez créer les objets suivants dans Active Directory. App-V utilise des groupes Active Directory pour contrôler l’accès aux applications et aux fonctions d’administration. Vous utiliserez ces groupes lors du processus d’installation du serveur et lors de la publication d’applications.

## Configuration des groupes d’éléments requis dans Active Directory pour la virtualisation des applications


Le tableau suivant répertorie les groupes Active Directory requis pour l’installation de App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Object</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Unité d’organisation (UO)</p></td>
<td align="left"><p>Créez une unité d’organisation dans Active Directory pour les groupes spécifiques requis pour App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Groupe d’administration App-V</p></td>
<td align="left"><p>Lors de l’installation du serveur de gestion App-V, vous devez sélectionner un groupe Active Directory à utiliser en tant que groupe administrateurs d’applications-V pour contrôler l’accès administratif à la console de gestion. Créer un groupe de sécurité pour les administrateurs d’application-V et ajouter à ce groupe chaque utilisateur qui a besoin d’utiliser la console de gestion. Vous ne pouvez pas créer ce groupe directement à partir du programme d’installation d’application-V Management Server.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Groupe utilisateurs d’App-V</p></td>
<td align="left"><p>App-V nécessite que chaque compte d’utilisateur qui accède aux fonctions App-V soit membre d’une stratégie de fournisseur associée à un seul groupe pour un accès général à la plateforme. Utiliser un groupe existant; par exemple, les utilisateurs du domaine, si tous les utilisateurs ont accès à l’application-V ou créent un nouveau groupe.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Groupes d’applications</p></td>
<td align="left"><p>App-V associe le droit d’utiliser une application individuelle avec un groupe Active Directory. Créez un groupe Active Directory pour chaque application et attribuez-lui des utilisateurs pour contrôler l’accès des utilisateurs aux applications.</p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[Configuration requise pour le déploiement d'Application Virtualization](application-virtualization-deployment-requirements.md)

[Procédure pour configurer les serveurs Windows Server2008 pour App-V Management Server](how-to-configure-windows-server-2008-for-app-v-management-servers.md)

 

 





