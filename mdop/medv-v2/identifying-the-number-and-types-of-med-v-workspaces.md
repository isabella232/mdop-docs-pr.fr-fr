---
title: Identifier le nombre et les types d'espaces de travail MED-V
description: Identifier le nombre et les types d'espaces de travail MED-V
author: dansimp
ms.assetid: 11642253-6b1f-4c4a-a11e-48d8a360e1ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e0c9ed4b0ce92d0ca752525b847405bbce90a270
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812251"
---
# Identifier le nombre et les types d'espaces de travail MED-V


MED-V crée un environnement virtuel pour exécuter des applications qui nécessitent Windows XP ou qui nécessitent une version d’Internet Explorer différente de la version de l’ordinateur hôte. Cet environnement virtuel est connu sous le nom d’espace de travail MED-V.

En fonction des exigences de compatibilité des applications auxquelles votre organisation a fait appel dans le cadre de la migration vers Windows 7, seuls certains utilisateurs ou services peuvent nécessiter des espaces de travail MED-V. Lorsque vous planifiez votre déploiement, vous devez déterminer le nombre d’espaces de travail MED-V requis au sein de votre entreprise. Vous devez également définir les exigences de chaque espace de travail MED-V.

## Identifier le nombre et les types d’espaces de travail MED-V


Identifiez les ordinateurs et groupes de votre entreprise pour lesquels vous allez créer des espaces de travail MED-V. En règle générale, il s’agit des utilisateurs qui ont besoin d’accéder à ces applications qui ne peuvent pas être migrées vers Windows 7. Identifiez les applications qui ne peuvent pas être migrées, ainsi que les utilisateurs qui ont besoin d’un espace de travail MED-V pour exécuter ces applications.

Vous pouvez également disposer d’adresses intranet qui n’ont pas encore été optimisées pour Windows 7. L’espace de travail MED-V fournit un navigateur Internet Explorer par le biais duquel les utilisateurs finaux peuvent améliorer l’accès à ces adresses Web qui ne sont pas encore prêtes pour la migration vers Windows 7. Au fur et à mesure que vous préparez et planifiez votre déploiement MED-V, vous devrez identifier et compiler une liste des adresses URL pour les rediriger vers Internet Explorer sur l’ordinateur hôte vers Internet Explorer dans l’espace de travail MED-V.

Enfin, vous devez évaluer l’espace disque requis. La plupart des espaces de travail MED-V sont de 2 gigaoctets (Go) ou plus. L’espace disque disponible sur un système peut être consommé rapidement, selon le nombre d’utilisateurs et la configuration de MED-V. Par ailleurs, le mode de distribution préféré de votre entreprise peut nécessiter un espace supplémentaire. En règle générale, vous devez libérer un minimum de 10 Go d’espace disque pour un espace de travail MED-V, mais cela peut varier considérablement en fonction de la taille de l’image.

### Calculer l’espace disque requis pour les espaces de travail MED-V

Un espace de travail MED-V nécessite une mémoire et un espace disque de l’ordinateur hôte sur lequel il est installé. Un minimum de 2 Go d’espace disque est requis sur l’hôte. L’espace disque est variable et dépend du nombre d’applications et des données de l’espace de travail MED-V d’un utilisateur.

Nous vous recommandons d’utiliser un minimum de 10 Go d’espace disque pour MED-V. Ce montant vous permet d’accéder à un espace de travail Windows XP de base et aux applications et à la redirection Web de base. Il fournit également de l’espace disponible pour le lecteur d’échange hôte. Dans une configuration de base, MED-V et un espace de travail MED-V unique, qui consomment jusqu’à 8 Go. Si vous incluez un grand nombre d’applications sur l’espace de travail MED-V ou si vous avez plusieurs utilisateurs par ordinateur, vous pouvez utiliser le calcul suivant pour déterminer plus précisément l’espace disque requis par votre environnement MED-V.

*VHD de base + (utilisateur par ordinateur x (différence disque + état enregistré))*

Pour calculer l’espace disque nécessaire, déterminez les éléments suivants:

-   **Taille du VHD de base** – disque dur virtuel utilisé pour créer l’espace de travail MED-V.

    **Important**  N’utilisez pas la taille de fichier. medv pour le calcul, car le fichier. medv est compressé.

     

-   **Utilisateurs par ordinateur** : MED-V crée un espace de travail MED-v pour chaque utilisateur sur un ordinateur; l’espace de travail MED-V utilise l’espace disque lorsque chaque utilisateur se connecte et que l’espace de travail MED-V est créé.

-   **Taille du disque de différenciation** , utilisée pour suivre la différence par rapport au disque dur virtuel de base. Cette taille varie selon que vous ajoutez des applications et des mises à jour logicielles au disque dur virtuel. Un disque de différenciation est créé pour chaque utilisateur MED-V lors du premier démarrage de MED-V.

-   **Taille du fichier d’état enregistré** , utilisé pour conserver l’État dans l’ordinateur virtuel. En règle générale, il s’agit juste d’une taille supérieure à la RAM allouée pour l’ordinateur virtuel. Par exemple, 1 Go de mémoire RAM allouée crée un fichier à propos de 1 081 000 Ko.

L’exemple suivant illustre un calcul basé sur trois utilisateurs d’un espace de travail MED-V qui dispose d’un disque dur virtuel de 2,6 Go:

*2,6 Go + (3 x (1.5 Go + 1)) = 10,1 Go*

**Remarques**  Une meilleure pratique pour MED-V consiste à calculer l’espace requis à l’aide d’un déploiement en laboratoire pour valider la configuration requise.

 

### Rechercher les fichiers pour déterminer la taille de fichier

Les emplacements suivants contiennent les fichiers correspondant aux paramètres de l’ordinateur et de l’utilisateur:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Type</th>
<th align="left">Location</th>
<th align="left">Fichiers</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>VHD de base</p></td>
<td align="left"><p>%ProgramData%\Microsoft\Medv\Workspace</p></td>
<td align="left"><p><em>InternalName </em> . vhd-où <em> InternalName </em> est le nom du disque dur virtuel que vous avez sélectionné dans le module de création de package de l’espace de travail MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Disque de différenciation</p></td>
<td align="left"><p>Machines%LocalAppData%\Microsoft\MEDV\v2\Virtual</p></td>
<td align="left"><p><em>WorkspaceName </em> . vhd</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Fichier d’état enregistré</p></td>
<td align="left"><p>Machines%LocalAppData%\Microsoft\MEDV\v2\Virtual</p></td>
<td align="left"><p><em>WorkspaceName </em> . vsv</p></td>
</tr>
</tbody>
</table>

 

### Calculer l’espace disque requis pour les espaces de travail MED-V partagés

Si vous calculez un déploiement d’espace de travail MED-V partagé sur un ordinateur unique, le nombre d’utilisateurs par ordinateur dans votre calcul est toujours «1», car MED-V ne configure qu’un seul disque de différenciation pour tous les utilisateurs.

Vous pouvez trouver le disque de différenciation et le fichier d’état enregistré pour les espaces de travail MED-V partagés dans%ProgramData%\\Microsoft\\Medv\\AllUsers.

## Rubriques connexes


[Définir et planifier votre déploiement MED-V](define-and-plan-your-med-v-deployment.md)

[Planification de MED-V](planning-for-med-v.md)

 

 





