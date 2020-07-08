---
title: Comment créer et tester une image MED-V
description: Comment créer et tester une image MED-V
author: dansimp
ms.assetid: 40e4aba6-12cb-4794-967d-2c09dc20d808
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f7989871a695b09c987124ab02c0143082148f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812119"
---
# Comment créer et tester une image MED-V


L’administrateur MED-V crée une image MED-V pour qu’elle puisse être chargée, associée à un espace de travail MED-v, puis distribuée au client via le Web, ajoutée à un package MED-V, ou téléchargée sur le client par le biais d’un système tiers. Il est recommandé de commencer par créer une image de test et de la tester sur un client MED-V avant de la déployer.

Lors de la création d’une image MED-V, il passe par les étapes suivantes:

1.  **Image de test locale**: image de base qui peut être testée localement.

2.  **Image empaquetée locale**: après test de l’image, l’image est empaquetée tel qu’il existait avant le test. Aucune modification n’est apportée pendant le test n’est incluse dans l’image empaquetée.

3.  **Image empaquetée sur le serveur**: l’image compactée est téléchargée sur le serveur.

## Comment créer une image de test MED-V


**Pour créer une nouvelle image de test MED-V**

1.  Cliquez sur le bouton gestion des **images** .

    Le module **images** s’affiche.

    -   Le module **images** se compose des volets suivants:

        -   **Images de test locales**: images de test locales.

        -   **Images compactées locales**: toutes les images compactées sur l’ordinateur local.

        -   **Images compactées sur le serveur**: toutes les images qui ont été empaquetées et chargées sur le serveur.

    -   Dans les **images compactées locales** et sur les volets **serveur** , la version la plus récente de chaque image est affichée en tant que nœud parent. Cliquez sur le nœud parent pour afficher toutes les autres versions existantes de l’image.

2.  Dans le volet **images de test locales** , cliquez sur **nouveau**.

3.  Dans la boîte de dialogue de **création d’image de test** , sélectionnez l’image d’ordinateur virtuel que vous voulez configurer en tant qu’image de test MED-V en effectuant l’une des opérations suivantes:

    -   Dans le champ fichier **image de base** , tapez le chemin d’accès complet au répertoire dans lequel se trouve l’image Microsoft Virtual PC préparée pour MED-V.

    -   Cliquez sur **Parcourir** pour accéder au répertoire dans lequel se trouve l’image Microsoft Virtual PC préparée pour MED-V.

4.  Dans le champ nom de l' **image** , tapez ou sélectionnez le nom souhaité.

    **Remarques**  Les caractères suivants ne peuvent pas être inclus dans le nom de l’image: Space " &lt; &gt; | \\ / : \* ?

     

5.  Cliquez sur **OK**.

    Une nouvelle image de test MED-V est créée sur votre ordinateur hôte avec les propriétés définies dans le tableau suivant.

    Pour plus d’informations sur la configuration de l’image d’espace de travail MED-V, voir [Configuration des stratégies d’espace de travail MED-v](configuring-med-v-workspace-policies.md).

**Propriétés des images de test locales**

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
<td align="left"><p>Nom de l’image de test telle qu’elle a été définie lors de la création de l’image par l’administrateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Trajectoire d’image</p></td>
<td align="left"><p>Path local de l’image de test.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Générée</p></td>
<td align="left"><p>Date de création de l’image de test.</p></td>
</tr>
</tbody>
</table>

 

## Test d’une image MED-V à partir du client MED-V


Après avoir créé une image de test MED-V, utilisez la procédure suivante pour tester l’image localement.

**Pour tester une image MED-V**

1.  Cliquez sur le bouton de gestion des **stratégies** .

2.  Dans le module **stratégie** , affectez l’image de test med-v à un espace de travail MED-v en procédant comme suit:

    1.  Cliquez sur l’onglet **machine virtuelle** .

    2.  Dans le champ **image affectée** , sélectionnez l’image de test MED-V que vous avez créée. Si votre image de test ne figure pas dans la liste, cliquez sur **Actualiser**.

    3.  Dans la barre d’outils, cliquez sur **enregistrer les modifications**.

3.  Configurez les autres paramètres d’espace de travail MED-V à tester. Pour plus d’informations, reportez-vous à [Configuration des stratégies d’espace de travail MED-V](configuring-med-v-workspace-policies.md).

4.  Démarrez le client MED-V.

5.  Dans la boîte de confirmation **confirmer l’exécution du test** , cliquez sur utiliser l’image de **test**.

6.  Testez l’image de test de l’espace de travail MED-V.

    Pour plus d’informations sur le démarrage et l’exécution du client MED-V, voir [opérations du client med-v](med-v-client-operations.md).

**Remarques**  Lorsque vous testez une image, n’ouvrez pas VPC et apportez les modifications à l’image.

 

**Remarques**  Lorsque vous testez une image, aucune modification n’est enregistrée dans l’image entre les sessions; ils sont enregistrés dans un fichier temporaire distinct. Cela permet de s’assurer que lorsque l’image est empaquetée et exécutée sur l’environnement de production, il s’agit de l’image originale et claire.

 

## Rubriques connexes


[Création d'une image Virtual PC pour MED-V](creating-a-virtual-pc-image-for-med-v.md)

[Création d'un espace de travail MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Configuration de stratégies d'espace de travail MED-V](configuring-med-v-workspace-policies.md)

[Opérations du client MED-V](med-v-client-operations.md)

 

 





