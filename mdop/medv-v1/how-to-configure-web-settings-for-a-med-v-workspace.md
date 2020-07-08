---
title: Comment configurer les paramètres Web pour un espace de travail MED-V
description: Comment configurer les paramètres Web pour un espace de travail MED-V
author: dansimp
ms.assetid: 9a6cd28f-7e4f-468f-830a-7b1d9abd3af3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 770d3fa9a03c9754db86ca348390d0b916de6d5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812132"
---
# Comment configurer les paramètres Web pour un espace de travail MED-V


Les sites Web qui peuvent être affichés uniquement dans les versions antérieures d’Internet Explorer et qui n’existent pas dans le système d’exploitation hôte peuvent être affichés dans les versions antérieures d’Internet Explorer dans l’espace de travail MED-V. L’utilisateur n’a pas besoin d’ouvrir un navigateur dans l’espace de travail MED-V pour afficher les sites Web spécifiés. L’utilisateur peut ouvrir un navigateur sur l’hôte et être automatiquement redirigé vers l’espace de travail MED-V et vice versa.

Les procédures suivantes vous expliquent comment créer une liste de règles de navigation Web pour un espace de travail MED-V. Tous les sites inclus dans les règles peuvent être parcourus dans l’espace de travail MED-V ou sur l’hôte, tel qu’il est défini par l’administrateur. Tous les sites non définis dans les règles sont parcourus à partir de l’environnement dans lequel ils ont été demandés. Toutefois, vous pouvez également les configurer en tant que groupe, à parcourir dans l’espace de travail MED-V ou l’hôte.

**Remarque**  
Les paramètres Web s’appliquent uniquement à Internet Explorer et à aucun autre navigateur.



Tous les paramètres Web sont configurés dans le module de **stratégie** sous l’onglet **Web** .

## Comment configurer les paramètres Web pour l’espace de travail MED-V


**Pour configurer les paramètres Web pour l’espace de travail MED-V**

1.  Cliquez sur l’espace de travail MED-V à configurer.

2.  Activez la case à cocher **Parcourir la liste des URL définies dans le tableau ci-dessous** pour rediriger l’utilisateur vers un navigateur au sein de l’espace de travail ou de l’hôte MED-V, lorsque l’utilisateur navigue vers une URL qui est conforme aux règles Web spécifiées.

3.  Cliquez sur l’une des options suivantes:

    -   **Dans l’espace de travail**, redirigez vers un navigateur dans l’espace de travail MED-V.

    -   **Dans l’hôte**, redirigez vers un navigateur sur l’hôte.

4.  Cochez la case **Parcourir toutes les autres URL** pour rediriger toutes les URL exclues des règles Web vers l’espace de travail hôte ou MED-V.

5.  Cliquez sur l’une des options suivantes:

    -   **Dans l’espace de travail**, redirigez toutes les autres URL vers un navigateur dans l’espace de travail MED-V.

    -   **Dans l’hôte**, redirigez toutes les autres URL vers un navigateur sur l’hôte.

6.  Dans le menu **stratégie** , cliquez sur **valider**.

## Comment ajouter une règle Web


**Pour ajouter une règle Web**

1.  Activez la case à cocher **Parcourir la liste des URL définies dans le tableau ci-dessous** pour activer les règles de navigation Web.

2.  Cliquez sur **Ajouter**.

    Une nouvelle règle Web est ajoutée.

3.  Configurez les propriétés de la règle Web comme décrit dans le tableau suivant.

4.  Dans le menu **stratégie** , cliquez sur **valider**.

**Propriétés Web de l’espace de travail MED-V**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propriété</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Type</p></td>
<td align="left"><ul>
<li><p><strong>Suffixe </strong> de domaine: accès à n’importe quelle adresse d’hôte se terminant par le suffixe spécifié dans la <strong> </strong> propriété Value et est défini en fonction de l’option définie dans navigation sur le <strong> Web </strong> .</p></li>
<li><p><strong>Préfixe IP </strong> : accès à toute adresse IP complète ou partielle dans la plage du préfixe spécifiée dans <strong> la </strong> propriété Value et définie en fonction de l’option définie dans navigation sur le <strong> Web </strong> .</p></li>
<li><p><strong>Toutes les adresses locales </strong> : l’accès à toutes les adresses sans &#39;. &#39; et est défini d’après l’option définie dans navigation sur le <strong> Web </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Valeur</p></td>
<td align="left"><ul>
<li><p>Si <strong> </strong> l’option suffixe de domaine est sélectionnée dans la <strong> </strong> propriété type, entrez un suffixe de domaine.</p>
<div class="alert">
<strong>Remarque</strong><br/><ul>
<li><p>Ne pas entrer &quot; * &quot; avant le suffixe.</p></li>
<li><p>Les suffixes de domaine prennent également en charge les alias.</p></li>
</ul>
</div>
<div>

</div></li>
<li><p>Si l’option préfixe IP est sélectionnée dans la <strong> </strong> propriété type, entrez une adresse IP complète ou partielle.</p></li>
</ul></td>
</tr>
</tbody>
</table>



## Comment supprimer une règle Web


**Pour supprimer une règle Web**

1.  Dans le volet **Web** , sélectionnez la règle Web à supprimer.

2.  Cliquez sur **supprimer**.

    La règle Web est supprimée.

## Rubriques connexes


[Utilisation de l'interface utilisateur de la console de gestion MED-V](using-the-med-v-management-console-user-interface.md)

[Création d'un espace de travail MED-V](creating-a-med-v-workspacemedv-10-sp1.md)









