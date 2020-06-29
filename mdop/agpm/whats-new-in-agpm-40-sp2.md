---
title: Nouveautés d'AGPM4.0SP2
description: Nouveautés d'AGPM4.0SP2
author: dansimp
ms.assetid: 5c0dcab4-f27d-4153-8b8e-b280b080be51
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56369207780cf0795f16eda91f249a26270c4b47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807390"
---
# Nouveautés d'AGPM4.0SP2


Ce contenu décrit les améliorations et les configurations prises en charge pour Microsoft Advanced Group Policy Management (AGPM) 4.0 Service Pack 2 (SP2). S’il existe une différence entre ce contenu et une autre documentation AGPM, considérez ce contenu faisant autorité et supposez qu’il remplace l’autre documentation.

## <a href="" id="what-s-new"></a>Nouveautés


AGPM 4.0 SP2 prend en charge les fonctionnalités et fonctionnalités suivantes.

### Prise en charge de Windows 8.1 et Windows Server2012 R2

Le SP2 pour AGPM 4.0 ajoute une prise en charge pour les systèmes d’exploitation Windows 8.1 et Windows Server2012 R2.

### Extensions côté client nouvelles et modifiées

Les extensions côté client de la stratégie de groupe ont été ajoutées ou modifiées pour que AGPM prenne en charge les nouveaux paramètres de stratégie dans Windows 8.1. Ces paramètres de stratégie permettent aux administrateurs de stratégie de groupe de gérer et de suivre les paramètres de stratégie spécifiques de Windows 8.1 qui changent entre deux objets de stratégie de groupe ou modèles. Pour afficher vos extensions côté client, utilisez les paramètres et rapports de différences disponibles dans le client AGPM.

Les extensions côté client nouvelles et modifiées sont les suivantes:

-   **Spécifiez les paramètres des dossiers de tâches**. Si vous activez ce paramètre de stratégie, l’administrateur informatique peut configurer la création automatique de dossiers de bureau. La fonctionnalité dossiers de travail permet aux utilisateurs finaux de synchroniser des fichiers à partir de leurs appareils de bureau Windows sur leurs autres appareils. Utilisez ce paramètre de stratégie pour créer une relation de synchronisation sur les appareils de l’utilisateur final et configurer l’identification du serveur de fichiers qui stocke les dossiers de tâches de l’utilisateur. Si vous activez la case à cocher **synchronisation automatique** , le partenariat de synchronisation sera créé sans entrée utilisateur, et les données commenceront automatiquement à se synchroniser avec l’appareil de l’utilisateur. Si vous n’activez pas la case à cocher **synchronisation automatique** , les utilisateurs doivent fournir des informations pour lancer la synchronisation.

-   **Forcez la configuration automatique pour tous les utilisateurs**. Si vous activez ce paramètre de stratégie, l’administrateur informatique peut déterminer s’il est possible de créer le partenariat dossiers de tâches automatiquement sur les appareils finaux sans entrée d’utilisateurs finaux. Si vous activez ce paramètre de stratégie, la synchronisation est configurée en fonction de la manière dont vous configurez le paramètre spécifier une stratégie de paramètre **dossiers de tâches** . Si vous définissez le **paramètre forcer la configuration automatique pour tous les utilisateurs** sur **désactivé** ou **non configuré**, le partenariat dossiers de tâches sera configuré en fonction de la manière dont vous définissez l’option de **mise en service automatique** dans le paramètre spécifier une stratégie de **dossiers de tâches** .

Pour plus d’informations sur la fonction dossiers de tâches, voir [vue d’ensemble des dossiers de tâches](https://go.microsoft.com/fwlink/?LinkId=330444).

### Commentaires des clients et ROLLUP de HotFix

Le SP2 pour AGPM 4.0 inclut un correctif cumulatif des correctifs pour résoudre les problèmes rencontrés depuis la version d’AGPM 4.0 Service Pack1 (SP1). Le SP2 pour AGPM 4.0 contient les derniers correctifs pour le Service Pack d’administration de la stratégie de groupe Microsoft Advanced Hotfix1. Pour plus d’informations, voir l’article de la base de connaissances [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)).

### Nouvelles extensions de stratégie de groupe dans les rapports et les différences

Les nouvelles extensions de stratégie de groupe ont été ajoutées aux rapports paramètres et différences.

### Modifications et prise en charge du programme d’installation

Les modifications et la prise en charge du programme d’installation d’AGPM 4.0 SP2 sont les suivantes:

-   Si vous installez AGPM 4.0 SP2 sur le système d’exploitation Windows 8 ou Windows Server 2012 ou les systèmes d’exploitation plus récents, le programme d’installation d’AGPM vérifie que les logiciels requis préalablement requis (console de gestion des stratégies de groupe (GPMC) et Microsoft .NET Framework 3.5) sont installés. Si ce logiciel requis n’est pas installé, l’installation d’AGPM 4.0 SP2 est bloquée.

-   Lorsque vous installez le serveur AGPM, l’activation WCF, l’activation non HTTP et le service d’activation de processus Windows sont activés automatiquement.

-   Sur le système d’exploitation du client Vista et les systèmes d’exploitation plus récents, téléchargez la version appropriée des outils d’administration du système distant pour votre système d’exploitation avant d’installer AGPM 4.0 SP2.

-   Le SP2 pour AGPM 4.0 prend en charge la compatibilité descendante avec les anciens systèmes d’exploitation pris en charge.

### Possibilité de procéder à la mise à niveau vers AGPM 4.0 SP2 sans avoir à entrer les paramètres de configuration

Vous pouvez mettre à niveau le client AGPM ou le serveur AGPM vers AGPM 4.0 SP2 sans être invité à entrer de nouveau les paramètres de configuration (appelé mise à niveau intelligente) uniquement à partir d’AGPM 4.0, comme indiqué dans le tableau suivant. Si vous effectuez une mise à niveau vers AGPM 4.0 SP2 à partir d’autres versions d’AGPM, comme indiqué dans le tableau ci-dessous, vous devez utiliser la mise à niveau classique, qui nécessite d’entrer de nouveau les paramètres de configuration. Étant donné que chaque version d’AGPM est associée à un système d’exploitation spécifique, voir [choisir la version d’AGPM à installer](https://go.microsoft.com/fwlink/?LinkId=254350) et vérifier que vous effectuez une mise à niveau de votre système d’exploitation le cas échéant avant de procéder à la mise à niveau d’AGPM.

**Mises à jour d’AGPM 4,0 SP2 prises en charge**

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Version d’AGPM à partir de laquelle vous pouvez effectuer la mise à niveau</strong></p></td>
<td align="left"><p><strong>2,5</strong></p></td>
<td align="left"><p><strong>3,0</strong></p></td>
<td align="left"><p><strong>4,0</strong></p></td>
<td align="left"><p><strong>4,0 SP1</strong></p></td>
<td align="left"><p><strong>4,0 SP2</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2,5</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Mise à niveau classique</p></td>
<td align="left"><p>Mise à niveau classique</p></td>
<td align="left"><p>L’installation est bloquée.</p></td>
<td align="left"><p>L’installation est bloquée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3,0</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Mise à niveau classique</p></td>
<td align="left"><p>L’installation est bloquée.</p></td>
<td align="left"><p>L’installation est bloquée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Mise à niveau intelligente</p></td>
<td align="left"><p>Mise à niveau intelligente</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4,0 SP1</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Mise à niveau intelligente</p></td>
</tr>
</tbody>
</table>

 

## Configurations prises en charge


Le SP2 pour AGPM 4.0 prend en charge les configurations du tableau suivant. Bien qu’AGPM prenne en charge des configurations mixtes, nous vous recommandons vivement d’exécuter le client AGPM et le serveur AGPM sur la même ligne de système d’exploitation (par exemple, Windows 8.1 avec Windows Server2012 R2, Windows 8 avec Windows Server 2012, etc.).

**Systèmes d’exploitation et systèmes d’exploitation pris en charge par AGPM 4.0 SP2**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Configurations prises en charge pour le serveur AGPM</strong></th>
<th align="left"><strong>Configurations prises en charge pour le client AGPM</strong></th>
<th align="left"><strong>Prise en charge d’AGPM</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 ou Windows 8.1</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012, Windows 8.1 ou Windows 8</p></td>
<td align="left"><p>Windows Server 2012 ou Windows 8</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Windows Server2008R2 ou Windows.</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8.1 ou Windows 8</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 ou Windows 7</p></td>
<td align="left"><p>Windows Server 2008 ou Vista avec Service Pack 1 (SP1)</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 ou Windows 7.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 ou Windows 7</p></td>
<td align="left"><p>Non pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 ou Windows 7.</p></td>
</tr>
</tbody>
</table>

 

## Conditions préalables à l’installation d’AGPM 4.0 SP2


Le tableau suivant décrit le comportement d’AGPM 4.0 SP2 et des programmes d’installation du serveur sur Windows 8.1 lorsque .NET Framework 3.5 ou la console GPMC dans les outils d’administration de serveur distant est manquant.

**Client AGPM**

**Serveur AGPM**

**Système d’exploitation**

**.NET Framework**

**Outils d'administration de serveur distant**

**.NET Framework**

**Outils d'administration de serveur distant**

**Windows 8.1**

Si .NET Framework 3.5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.

Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation.

Si .NET Framework 3.5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.

Si la console GPMC n’est pas activée ou installée, le programme d’installation bloque l’installation.

**Windows Server2012 R2**

Si .NET Framework 3.5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.

Si la console GPMC n’est pas activée, le programme d’installation l’active au cours de l’installation.

Si .NET Framework 3.5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.

Si la console GPMC n’est pas activée, le programme d’installation l’active au cours de l’installation.

 

## Obtention de technologies MDOP


AGPM 4,0 SP2 fait partie du pack d’optimisation de bureau de Microsoft (MDOP). MDOP fait partie de Microsoft Software Assurance. Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Rubriques connexes


[Gestion avancée des stratégies de groupe](index.md)

[Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP2](release-notes-for-microsoft-advanced-group-policy-management-40-sp2.md)

[Choix de la version d'AGPM à installer](choosing-which-version-of-agpm-to-install.md)

 

 





