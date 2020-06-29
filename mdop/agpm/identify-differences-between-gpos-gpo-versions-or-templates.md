---
title: Identifier les différences entre les objets de stratégie de groupe, les versions ou les modèles d'objet de stratégie de groupe
description: Identifier les différences entre les objets de stratégie de groupe, les versions ou les modèles d'objet de stratégie de groupe
author: dansimp
ms.assetid: 6320afc4-af81-47e8-9f4c-463ff99d5a53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fd7966c9c72b2f0d30595af55520940c779a409f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808434"
---
# Identifier les différences entre les objets de stratégie de groupe, les versions ou les modèles d'objet de stratégie de groupe


Vous pouvez générer des rapports de différences HTML ou XML pour analyser les différences entre les objets de stratégie de groupe (GPO), les modèles ou les différentes versions d’un objet de stratégie de groupe.

Un compte d’utilisateur disposant du rôle de réviseur, d’éditeur, d’approbateur ou d’administrateur AGPM (contrôle total) ou des autorisations nécessaires dans la gestion avancée des stratégies de groupe est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

## Identification des différences entre les objets de stratégie de groupe, les versions d’objets ou les modèles


-   [Entre deux objets ou modèles de stratégie de groupe](#bkmk-two-gpos)

-   [Entre un objet de stratégie de groupe et un modèle](#bkmk-gpo-and-template)

-   [Entre deux versions d’un objet de stratégie de groupe](#bkmk-two-versions)

-   [Entre une version d’un objet de stratégie de groupe et un modèle](#bkmk-gpo-version-and-template)

## <a href="" id="bkmk-two-gpos"></a>


**Pour identifier les différences entre deux objets ou modèles de stratégie de groupe**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** du volet Détails, cliquez sur un onglet pour afficher les objets de stratégie de groupe (ou modèles, si vous comparez deux modèles).

3.  Sélectionnez les deux objets ou modèles d’objets de stratégie de groupe.

4.  Cliquez avec le bouton droit sur l’un des modèles ou objets de stratégie de groupe, cliquez sur **différences**, puis sur rapport **HTML** ou **État XML** pour afficher un rapport de différences résumant les paramètres des objets ou modèles de stratégie de groupe.

### <a href="" id="bkmk-gpo-and-template"></a>

**Pour identifier les différences entre un objet de stratégie de groupe et un modèle**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** du volet Détails, cliquez sur un onglet pour afficher les objets de stratégie de groupe (ou modèles, si vous comparez deux modèles).

3.  Cliquez avec le bouton droit sur l’objet de stratégie de groupe, cliquez sur **différences**, puis sur **modèle**.

4.  Sélectionnez le modèle et le type de rapport, puis cliquez sur **OK** pour afficher un rapport de différences résumant les paramètres de l’objet de stratégie de groupe et du modèle.

### <a href="" id="bkmk-two-versions"></a>

**Pour identifier les différences entre deux versions d’un objet de stratégie de groupe**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** du volet Détails, cliquez sur un onglet pour afficher les objets de stratégie de groupe (ou modèles, si vous comparez deux modèles).

3.  Double-cliquez sur l’objet de stratégie de groupe pour afficher son historique, puis mettez en surbrillance les versions à comparer.

4.  Cliquez avec le bouton droit sur l’une des versions, cliquez sur **différences**, puis sur rapport **HTML** ou **État XML** pour afficher un rapport de différences résumant les paramètres des objets de stratégie de groupe.

### <a href="" id="bkmk-gpo-version-and-template"></a>

**Pour identifier les différences entre une version d’un objet de stratégie de groupe et un modèle**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** du volet Détails, cliquez sur un onglet pour afficher les objets de stratégie de groupe (ou modèles, si vous comparez deux modèles).

3.  Double-cliquez sur l’objet de stratégie de groupe pour afficher son historique.

4.  Cliquez avec le bouton droit sur la version d’objet GPO qui vous intéresse, cliquez sur **différences**, puis sur **modèle**.

5.  Sélectionnez le modèle et le type de rapport, puis cliquez sur **OK** pour afficher un rapport de différences résumant les paramètres de la version et du modèle de l’objet de stratégie de groupe.

## Clé pour différencier les rapports


<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Symbole</th>
<th align="left">Signification</th>
<th align="left">Couleur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>None</p></td>
<td align="left"><p>L’élément existe avec des paramètres identiques dans les deux objets de stratégie de groupe</p></td>
<td align="left"><p>Varie selon le niveau</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[#]</strong></p></td>
<td align="left"><p>L’élément existe dans les deux objets de stratégie de groupe, mais avec les paramètres modifiés</p></td>
<td align="left"><p>Bleu</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>[-]</strong></p></td>
<td align="left"><p>L’élément existe uniquement dans le premier objet GPO</p></td>
<td align="left"><p>Rouge</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[+]</strong></p></td>
<td align="left"><p>L’élément existe uniquement dans le second objet de stratégie de groupe</p></td>
<td align="left"><p>Vert</p></td>
</tr>
</tbody>
</table>

 

-   Pour les éléments ayant modifié des paramètres, les paramètres modifiés sont identifiés lorsque l’élément est étendu. La valeur de l’attribut dans chaque objet GPO est affichée dans l’ordre dans lequel les objets de stratégie de groupe sont affichés dans le rapport.

-   Certaines modifications apportées aux paramètres peuvent entraîner le signalement d’un élément sous la forme de deux éléments différents (un seul présent dans le premier objet de stratégie de groupe, l’un présent uniquement dans la deuxième) plutôt qu’un élément modifié.

### Autres éléments à prendre en considération

-   Par défaut, vous devez être un réviseur, un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure. En particulier, vous devez disposer du **contenu de liste** et des autorisations de **paramètres** pour l’objet GPO. Par ailleurs, pour afficher la liste des objets de stratégie de groupe, vous devez disposer de l’autorisation **contenu de liste** pour le domaine.

### Références supplémentaires

-   [Exécution de tâches de réviseur](performing-reviewer-tasks.md)

 

 





