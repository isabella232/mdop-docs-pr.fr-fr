---
title: Nouveautés d'AGPM4.0SP1
description: Nouveautés d'AGPM4.0SP1
author: dansimp
ms.assetid: c6a3d94a-13c3-44e6-a466-c3011879999e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca1ee4a1c2eb943a25246dc31b127eaf72ff5fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807393"
---
# Nouveautés d'AGPM4.0SP1


Ce contenu «nouveautés» décrit les améliorations et les configurations prises en charge pour la gestion de la stratégie de groupe avancée Microsoft (AGPM) 4,0 SP1. S’il existe une différence entre ce contenu et toute autre documentation AGPM, ce contenu doit être considéré comme faisant autorité et doit remplacer le contenu inclus dans le produit.

## <a href="" id="what-s-new"></a>Nouveautés


AGPM 4,0 SP1 prend en charge les améliorations suivantes:

### Extensions côté client nouvelles et modifiées

Les extensions côté client de la stratégie de groupe ont été ajoutées ou modifiées pour AGPM afin de prendre en charge les nouvelles stratégies de groupe dans Windows 8 et Windows Server 2012. Ces stratégies de groupe permettent aux administrateurs de stratégie de groupe de gérer et de suivre les paramètres de stratégie de groupe spécifiques de Windows 8 qui changent entre deux objets de stratégie de groupe ou modèles. Vous pouvez également créer des objets de stratégie de groupe personnalisés avec des paramètres spécifiques de Windows 8 et configurer et enregistrer les objets de stratégie de groupe en tant que modèle. Pour afficher vos CSE, utilisez les paramètres et les rapports de différences disponibles dans le client AGPM 4,0 SP1.

Les extensions côté client nouvelles et modifiées sont les suivantes:

-   **Stratégie d’accès centralisé:** Permet aux administrateurs de stratégie de groupe de spécifier des stratégies d’accès centralisées sur des serveurs de stratégie de groupe, par exemple des serveurs de fichiers. La stratégie d’accès centralisé est une stratégie d’autorisation spécifiée par un élément d’objet de stratégie de groupe et appliquée aux cibles de stratégie pour faciliter l’accès centralisé et le contrôle des ressources. Ces stratégies d’accès centralisé doivent être configurées sur un ordinateur client de stratégie de groupe à partir d’Active Directory. Une stratégie de groupe distribue les connaissances d’une stratégie d’accès centralisé applicable aux ordinateurs qui doivent l’appliquer.

-   **Modifications de la stratégie de résolution de nom:** Permet aux administrateurs de stratégie de groupe de configurer les paramètres pour la sécurité DNS et DirectAccess sur les ordinateurs clients DNS. De nouveaux onglets pour la configuration des paramètres du serveur DNS générique et des paramètres d’encodage ont été ajoutés.

-   **Modifications des préférences de stratégie de groupe:** Ajoute une prise en charge pour la configuration et la gestion des paramètres d’Internet Explorer 10 qui ont été ajoutés pour Windows 8.

-   **Connexions d’application et de bureau distantes:** Permet aux administrateurs de stratégie de groupe de spécifier l’URL de connexion par défaut utilisée pour les connexions aux applications et au bureau à distance.

-   **Options de démarrage de Windows to Go:** Permet aux administrateurs de stratégie de groupe de configurer le démarrage de l’ordinateur pour Windows sur Go si un appareil USB contenant un espace de travail Windows to Go est connecté.

-   **Options de mise en veille prolongée de Windows to Go:** Permet aux administrateurs de stratégie de groupe de configurer l’utilisation de l’état de veille de la mise en veille (S4) lors du démarrage de l’ordinateur à partir d’un espace de travail Windows to go.

### Commentaires des clients et ROLLUP de HotFix

Le Service Pack d’AGPM 4,0 inclut un correctif cumulatif pour résoudre les problèmes détectés depuis la version d’AGPM 4,0. AGPM 4,0 SP1 contient les correctifs les plus récents pour la gestion de la stratégie de groupe Microsoft avancée 4,0 Hotfix 1.

### Les rapports et les différences indiquent les nouvelles extensions de stratégie de groupe

Les nouvelles extensions de stratégie de groupe ont été ajoutées aux rapports paramètres et différences.

### Modifications et prise en charge du programme d’installation

Les modifications et la prise en charge du programme d’installation d’AGPM 4,0 SP1 sont les suivantes:

-   Si vous installez AGPM 4,0 SP1 sur Windows 8 ou Windows Server 2012, le programme d’installation d’AGPM vérifie que les logiciels prérequis requis (console de gestion des stratégies de groupe et .NET 3,5 Framework) sont installés. Si ces éléments requis ne sont pas installés, l’installation d’AGPM 4,0 SP1 est bloquée.

-   Lors de l’installation d’AGPM 4,0 SP1, l’activation WCF, l’activation non HTTP et le service d’activation de processus Windows sont activés automatiquement.

-   Sur les systèmes d’exploitation Windows Vista, Windows 7 et Windows 8, téléchargez la version appropriée du kit de tâches d’administration du système distant pour votre système d’exploitation avant d’installer AGPM 4,0 SP1.

-   La compatibilité descendante avec les anciens systèmes d’exploitation pris en charge est prise en charge.

### Possibilité d’effectuer la mise à niveau ou la mise à jour vers AGPM 4,0 SP1 sans entrer de nouveau les paramètres de configuration

Vous pouvez mettre à niveau le client ou le serveur AGPM vers AGPM 4,0 SP1 uniquement d’AGPM 4,0 sans être invité à entrer de nouveau les paramètres de configuration (appelées «mise à niveau intelligente»), comme indiqué dans le tableau suivant. Si vous effectuez une mise à niveau vers AGPM 4,0 SP1 à partir d’autres versions d’AGPM, comme indiqué dans le tableau ci-dessous, vous devez utiliser la «mise à niveau classique» qui nécessite d’entrer de nouveau les paramètres de configuration. Dans la mesure où chaque version d’AGPM est associée à un système d’exploitation spécifique, reportez-vous à la rubrique [choix de la version d’AGPM à installer](https://go.microsoft.com/fwlink/?LinkId=254350)et veillez à mettre à niveau votre système d’exploitation, le cas échéant, avant d’effectuer une mise à niveau.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Version d’AGPM à partir de laquelle vous pouvez effectuer la mise à niveau</strong></p></td>
<td align="left"><p><strong>2,5</strong></p></td>
<td align="left"><p><strong>3,0</strong></p></td>
<td align="left"><p><strong>4,0</strong></p></td>
<td align="left"><p><strong>4,0 SP1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2,5</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Mise à niveau classique</p></td>
<td align="left"><p>Mise à niveau classique</p></td>
<td align="left"><p>L’installation est bloquée.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3,0</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Mise à niveau classique</p></td>
<td align="left"><p>L’installation est bloquée.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Non applicable</p></td>
<td align="left"><p>Mise à niveau intelligente</p></td>
</tr>
</tbody>
</table>

 

## Configurations prises en charge


AGPM prend en charge les configurations du tableau suivant. Bien qu’AGPM prenne en charge des configurations mixtes, il est fortement recommandé d’exécuter le client et le serveur AGPM sur la même famille de systèmes d’exploitation (par exemple, Windows 8 et Windows Server 2012, Windows 7 avec Windows Server 2008 R2, etc.).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Configurations prises en charge pour le serveur AGPM 4,0 SP1</strong></p></td>
<td align="left"><p><strong>Configurations prises en charge pour le client AGPM 4,0 SP1</strong></p></td>
<td align="left"><p><strong>Prise en charge d’AGPM 4,0 SP1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8 ou Windows Server 2012</p></td>
<td align="left"><p>Windows 8 ou Windows Server 2012</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2 ou Windows 7</p></td>
<td align="left"><p>Windows Server 2008 R2 ou Windows 7</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows 8</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2 ou Windows 7, Windows 8 ou Windows Server 2012</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais ne peut pas modifier les paramètres de stratégie ou les éléments de préférence qui existent uniquement dans Windows Server 2008 R2 ou Windows 7 ou Windows 8.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2008 R2 ou Windows 7, Windows 8 ou Windows Server 2012</p></td>
<td align="left"><p>Pris en charge</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Windows Server 2008 ou Windows Vista avec SP1</p></td>
<td align="left"><p>Pris en charge, mais il est impossible de signaler ou de modifier des paramètres de stratégie ou des éléments de préférence qui existent uniquement dans Windows Server 2008 R2 ou Windows 7 ou Windows 8.</p></td>
</tr>
</tbody>
</table>

 

## Conditions préalables à l’installation d’AGPM 4,0 SP1


Le tableau suivant décrit le comportement de Windows 8 d’AGPM 4,0 SP1 et des programmes d’installation du serveur lorsque .NET 3,5 ou la console de gestion des stratégies de groupe dans les outils d’administration de serveur distant.

**Client AGPM 4,0 SP1**

**Serveur AGPM Server 4,0 SP1**

**Systèmed’exploitation**

**.NET**

**Outils d'administration de serveur distant**

**.NET**

**Outils d'administration de serveur distant**

**Windows8**

Si .NET 3,5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.

Si la console de gestion des stratégies de messagerie n’est pas activée ou installée sur le système, le programme d’installation bloque celle-ci.

Si .NET 3,5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.

Si la console de gestion des stratégies de messagerie n’est pas activée ou installée sur le système, le programme d’installation bloque celle-ci.

**Windows Server2012**

Si .NET 3,5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.

Si la console de gestion des stratégies de messagerie n’est pas activée, le programme d’installation l’autorise lors de l’installation.

Si .NET 3,5 n’est pas activé ou n’est pas installé, le programme d’installation bloque l’installation.

Si la console de gestion des stratégies de messagerie n’est pas activée, le programme d’installation l’autorise lors de l’installation.

 

## Rubriques connexes


[Gestion avancée des stratégies de groupe](index.md)

[Notes de publication pour la Gestion avancée des stratégies de groupe Microsoft4.0SP1](release-notes-for-microsoft-advanced-group-policy-management-40-sp1.md)

 

 





