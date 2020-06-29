---
title: Rechercher et filtrer la liste des objets de stratégie de groupe (GPO)
description: Rechercher et filtrer la liste des objets de stratégie de groupe (GPO)
author: dansimp
ms.assetid: 1bc58a38-033c-4aed-9eb4-c239827f5501
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5646a51a37a4ca9195fb9ef858e8c5920ca7738a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808237"
---
# Rechercher et filtrer la liste des objets de stratégie de groupe (GPO)


Dans Advanced Group Policy Management (AGPM), vous pouvez effectuer une recherche dans la liste des objets de stratégie de groupe et leurs attributs pour filtrer la liste des objets de stratégie de groupe affichés. Par exemple, vous pouvez rechercher des objets de stratégie de groupe avec un nom, un État ou un commentaire particulier. Vous pouvez également rechercher les objets de stratégie de groupe qui ont été modifiés en dernier par un administrateur de stratégie de groupe particulier ou à une date particulière.

## Exécution d’une recherche complexe


Vous pouvez effectuer une recherche complexe en utilisant l’attribut de l' *objet de stratégie de groupe format 1: chaîne de recherche 1, attribut 2: chaîne de recherche 2... chaînes de recherche dans toutes les colonnes*. La recherche n’est pas sensible à la casse.

-   **Attribut d’objet de stratégie de groupe:** Tout en-tête de colonne dans la liste d’objets de stratégie de groupe dans AGPM autre que la version de l' **ordinateur** ou la version de l' **utilisateur**. Les attributs de l’objet GPO incluent le nom de l’objet de stratégie de groupe, l’État, l’utilisateur qui a modifié le plus récemment l’objet de stratégie de groupe, la date et l’heure de la dernière modification de celui-ci, des commentaires et des filtres WMI appliqués à l’objet GPO.

-   **Chaîne de recherche:** Texte pour lequel rechercher dans la colonne spécifiée. Si une chaîne comporte des espaces, vous devez encadrer la chaîne de guillemets.

-   **Chaînes de recherche dans toutes les colonnes:** Texte pour lequel rechercher dans toutes les colonnes de la liste d’objets de stratégie de groupe dans AGPM, à l’exception de la version de l' **ordinateur** et de la **version utilisateur**. Vous pouvez inclure plusieurs chaînes séparées par des espaces. Si une chaîne comporte des espaces, vous devez encadrer la chaîne de guillemets.

Chaque attribut d’objet GPO et paire de chaînes de recherche et chaque chaîne de recherche en toutes les colonnes sont combinés à l’aide d’une opération AND logique. Le résultat est une liste de tous les objets de stratégie de groupe pour lesquels chaque attribut spécifié inclut la chaîne de recherche spécifiée et pour lequel les chaînes de recherche de toutes les colonnes apparaissent dans au moins une colonne. La recherche renvoie des correspondances partielles pour les chaînes, afin que vous puissiez entrer une partie du nom de l’objet GPO ou du nom d’utilisateur et afficher la liste de tous les objets de stratégie de groupe qui incluent ce texte dans leur nom.

Voici quelques exemples de recherche:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Description du résultat de la recherche</th>
<th align="left">Requête de recherche</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tous les objets de stratégie de groupe dont les noms incluent la sécurité du texte <strong> </strong> et l' <strong> Amérique du Nord </strong> .</p></td>
<td align="left"><p><strong>nom: </strong><strong> nom de sécurité </strong><strong> : </strong> &quot; <strong> Amérique du Nord</strong>&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tous les objets de stratégie de groupe extraits.</p></td>
<td align="left"><p><strong>État: </strong> &quot; <strong> extrait</strong>&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tous les objets de stratégie de groupe modifiés le plus récemment par l’utilisateur nommé <strong> administrateur </strong> et récemment modifiés au cours du mois précédent.</p></td>
<td align="left"><p><strong>modifié par: </strong><strong> Date de modification de l’administrateur </strong><strong> : </strong><strong> lastmonth</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Tous les objets de stratégie de groupe dans lesquels le <strong> pare-feu Word </strong> est inclus dans le commentaire le plus récent et dans lequel la sécurité du mot <strong> </strong> apparaît dans n’importe quelle colonne.</p></td>
<td align="left"><p><strong>Commentaire: </strong><strong> sécurité du pare-feu </strong><strong></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tous les objets de stratégie de groupe dont le statut est <strong> désactivé </strong> .</p></td>
<td align="left"><p><strong>État de l’objet GPO: </strong><strong> tout</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Tous les objets de stratégie de groupe qui disposent d’un filtre WMI appelé <strong> filtre WMI </strong> appliqué et dont le statut de configuration de l' <strong> utilisateur est désactivé </strong> .</p></td>
<td align="left"><p><strong>filtre WMI: </strong> &quot; <strong> mon état de GPO filtre WMI </strong> &quot; <strong> : </strong><strong> utilisateur</strong></p></td>
</tr>
</tbody>
</table>

 

## Spécification de dates


Vous pouvez rechercher des objets de stratégie de groupe modifiés à une date spécifique, à une heure spécifique ou pendant un laps de temps en utilisant les mêmes conditions spéciales disponibles lorsque vous recherchez dans Windows. Si vous entrez une date ou une heure spécifique, vous devez utiliser le format utilisé dans la colonne de **Date de modification** . Vous trouverez ci-dessous des exemples de recherches dans la colonne **Date de modification** :

-   **changer la date:****10/10/2009**

-   **modification de la date:****10/10/2009 9:00:00 AM**

-   **changer la date:****thisweek**

Vous pouvez utiliser les conditions spéciales suivantes, qui ne respectent pas la casse, lorsque vous effectuez une recherche dans la colonne **changer la date** :

-   **Aujourd’hui**

-   **Hier**

-   **ThisWeek**

-   **LastWeek**

-   **ThisMonth**

-   **LastMonth**

-   **TwoMonths**

-   **ThreeMonths**

-   **ThisYear**

-   **LastYear**

### Autres éléments à prendre en considération

-   Par défaut, vous devez être un réviseur, un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer de l’autorisation **contenu de liste** pour le domaine.

-   Pour plus d’informations sur les attributs d’objets de stratégie de groupe, voir fonctionnalités de l' [onglet contenu](contents-tab-features-agpm40.md).

### Références supplémentaires

-   [Gestion avancée des stratégies de groupe4.0](advanced-group-policy-management-40.md)

 

 





