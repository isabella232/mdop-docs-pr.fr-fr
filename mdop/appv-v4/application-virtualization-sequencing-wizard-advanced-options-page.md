---
title: Page d’options avancées de l’Assistant séquençage de la virtualisation de l’application
description: Page d’options avancées de l’Assistant séquençage de la virtualisation de l’application
author: dansimp
ms.assetid: 2c4c5d95-d55e-463d-a851-8486f6a724f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 716fa27852f1cadfebec31a267ce1b9b581b8ff7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807970"
---
# Page d’options avancées de l’Assistant séquençage de la virtualisation de l’application


Utilisez la page **Options avancées** de l’Assistant séquençage de l’application virtualisation des applications (App-V) pour spécifier des options avancées pour l’installation de l’application. La page contient les éléments décrits dans le tableau suivant.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Taille du bloc</strong></p></td>
<td align="left"><p>Utilisez cette valeur pour spécifier la taille des blocs dans lesquels le fichier SFT sera subdivisé en continu sur un réseau. Tous les blocs égaux à la taille spécifiée; Toutefois, le dernier bloc peut avoir une taille inférieure à celle spécifiée. Sélectionnez l’une des valeurs suivantes:</p>
<ul>
<li><p><strong>4 KO</strong></p></li>
<li><p><strong>16 KO</strong></p></li>
<li><p><strong>32 KO</strong></p></li>
<li><p><strong>64 KO</strong></p></li>
</ul>
<div class="alert">
<strong>Remarque</strong><br/><p>Lorsque vous sélectionnez une taille de bloc, tenez compte de la taille du fichier SFT et de la bande passante réseau. Le flux d’un fichier dont la taille de blocs est plus petite prend plus de temps sur le réseau, mais nécessite moins de bande passante. Les fichiers de tailles de blocs plus grandes peuvent être plus rapides, mais ils utilisent plus de bande passante réseau. Dans le cadre de l’expérimentation, vous pouvez découvrir la taille maximale de bloc pour les applications en continu sur votre réseau.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Activer Microsoft Update lors de l’analyse</strong></p></td>
<td align="left"><p>Autorise l’installation des mises à jour de Microsoft au cours de l’Assistant de séquençage&#39;la phase d’analyse s.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Dll de REBASE</strong></p></td>
<td align="left"><p>Permet le remappage des bibliothèques de liens dynamiques prises en charge sur un espace contigu dans la RAM, de l’économie de mémoire et des performances améliorées.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Back</strong></p></td>
<td align="left"><p>Accède à l’Assistant séquençage&#39;la page précédente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Next</strong></p></td>
<td align="left"><p>Accède à l’Assistant séquençage&#39;à la page suivante.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Annuler</strong></p></td>
<td align="left"><p>Arrêt de l’opération de l’Assistant séquençage.</p></td>
</tr>
</tbody>
</table>



\ [Valeur du jeton de modèle \]

Utilisez la page **Options avancées** de l’Assistant séquençage d’App-V pour spécifier des options avancées pour l’application que vous séquençage. Cette page contient les éléments décrits dans le tableau ci-dessous.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nom</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Autoriser l’exécution de Microsoft Update lors du suivi</strong></p></td>
<td align="left"><p>Spécifie si les mises à jour logicielles doivent être appliquées à l’application lors de la phase d’analyse du séquençage des applications. Cette option est utile si des mises à jour sont nécessaires pour terminer l’installation de l’application. Cette option n’est pas sélectionnée par défaut.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Dll de REBASE</strong></p></td>
<td align="left"><p>Permet le remappage des bibliothèques de liens dynamiques prises en charge sur un espace contigu dans la RAM. La sélection de cette option peut vous aider à gérer la mémoire et améliorer les performances de l’application. Cette option n’est pas sélectionnée par défaut.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Back</strong></p></td>
<td align="left"><p>Permet d’accéder à la page précédente de l’Assistant.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Next</strong></p></td>
<td align="left"><p>Accède à la page suivante de l’Assistant.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Annuler</strong></p></td>
<td align="left"><p>Supprime les paramètres et quitte l’Assistant.</p></td>
</tr>
</tbody>
</table>



\ [Valeur du jeton de modèle \]

## Rubriques connexes


[Assistant de séquencement](sequencing-wizard.md)









