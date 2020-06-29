---
title: Comment empaqueter une image MED-V
description: Comment empaqueter une image MED-V
author: dansimp
ms.assetid: e1ce2307-0f1b-4bf8-b146-e4012dc138d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a330b8feca922239691bed083767c3acc57105d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810698"
---
# Comment empaqueter une image MED-V


Une image MED-V doit être empaquetée avant d’être ajoutée à un package de déploiement ou chargée sur le serveur.

**Pour créer une image MED-V empaquetée**

1.  Cliquez sur le bouton gestion des **images** .

2.  Dans le module **images** , dans le volet **images groupées locales** , cliquez sur **nouveau**.

3.  Dans la boîte de dialogue **création d’images compactées** , sélectionnez l’image de l’ordinateur virtuel en effectuant l’une des opérations suivantes:

    -   Dans le champ **fichier image de base** , tapez le chemin d’accès complet au répertoire dans lequel se trouve l’image Microsoft Virtual PC préparée pour MED-V.

    -   Cliquez sur **Parcourir** pour accéder au répertoire dans lequel se trouve l’image Microsoft Virtual PC préparée pour MED-V.

4.  Spécifiez le nom de la nouvelle image en effectuant l’une des opérations suivantes:

    -   Dans le champ nom de l' **image** , tapez le nom souhaité.

        **Remarque**  
        Les caractères suivants ne peuvent pas être inclus dans le nom de l’image: Space " &lt; &gt; | \\ / : \* ?



~~~
    A new packed image will be created.

-   From the drop-down list, select an existing name.

    A new version of the existing image will be created.
~~~

5. Cliquez sur **OK**.

   Une nouvelle image empaquetée MED-V est créée sur votre ordinateur hôte avec les propriétés définies dans le tableau suivant.

**Remarque**  
Dans les **images compactées locales** et sur les volets **serveur** , la version la plus récente de chaque image est affichée en tant que nœud parent. Cliquez sur le nœud parent pour afficher toutes les autres versions existantes de l’image.



**Propriétés d’images compactées locales**

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
<td align="left"><p>Nom de l’image</p></td>
<td align="left"><p>Nom de l’image compactée telle qu’elle a été définie lors de la création de l’image par l’administrateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Version</p></td>
<td align="left"><p>Version de l’image affichée.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Toutes les versions précédentes sont conservées sauf si supprimées.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Taille du fichier (compressé)</p></td>
<td align="left"><p>Taille compressée physique de l’image.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Taille de l’image (non compressée)</p></td>
<td align="left"><p>Taille de l’image qui n’est pas compressée.</p></td>
</tr>
</tbody>
</table>



## Rubriques connexes


[Comment installer le client MED-V et la console de gestion MED-V](how-to-install-med-v-client-and-med-v-management-console.md)

[Utilisation de l'interface utilisateur de la console de gestion MED-V](using-the-med-v-management-console-user-interface.md)

[Création d'une image Virtual PC pour MED-V](creating-a-virtual-pc-image-for-med-v.md)









