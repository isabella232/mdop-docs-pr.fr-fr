---
title: Procédure pour modifier le niveau de journalisation du serveur et les paramètres de base de données
description: Procédure pour modifier le niveau de journalisation du serveur et les paramètres de base de données
author: dansimp
ms.assetid: e3ebaee5-6c4c-4aa8-9766-c5aeb00f477a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bb35ac09c5e23f4847662171b68284f868e66dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807345"
---
# Procédure pour modifier le niveau de journalisation du serveur et les paramètres de base de données


Vous pouvez utiliser les procédures suivantes pour modifier le niveau de journalisation et les paramètres de journalisation de la base de données à partir de la console de gestion du serveur d’applications.

Les niveaux de journalisation suivants sont disponibles:

-   Transaction uniquement

-   Erreurs irrécupérables

-   Erreurs

-   Avertissements/Erreurs

-   Infos/avertissements/Erreurs

-   Détaillée

**Remarques**  En raison de la taille du fichier journal obtenu lors de l’utilisation du mode **détaillé** , il est recommandé de ne pas exécuter de serveurs de production avec ce niveau de jeu de journaux.

 

Les paramètres de journalisation de la base de données déterminent le type du pilote de la base de données, les informations d’accès et l’emplacement de la base de données.

**Pour modifier le niveau de journalisation pour les serveurs de gestion**

1.  Cliquez sur le nœud **groupes de serveurs** pour afficher les groupes de serveurs.

2.  Cliquez avec le bouton droit sur le groupe de serveurs, puis sélectionnez **Propriétés**.

3.  Dans la boîte de dialogue **Propriétés** , sélectionnez l’onglet **journalisation** .

4.  Dans la boîte de dialogue **Propriétés du groupe de serveurs** , sélectionnez le serveur, puis cliquez sur **modifier**.

5.  Dans la boîte de dialogue **Ajouter/modifier le module journal** , sélectionnez le niveau de journalisation dans la liste déroulante **type d’événement** .

6.  Cliquez sur **OK**.

7.  Dans la boîte de dialogue **Propriétés du groupe de serveurs** , cliquez sur **OK** ou sur **appliquer**.

**Pour modifier le niveau de journalisation pour les serveurs de diffusion en continu**

1.  Modifiez la valeur de clé de Registre suivante pour modifier le niveau de journalisation:

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel

2.  Sélectionnez l’une des valeurs suivantes pour définir le niveau de journalisation.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Valeur</th>
    <th align="left">Niveau de journalisation</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>0,4</p></td>
    <td align="left"><p>Transactions uniquement</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>1</p></td>
    <td align="left"><p>Erreurs irrécupérables</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>deuxième</p></td>
    <td align="left"><p>Erreurs</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>3D</p></td>
    <td align="left"><p>Avertissements/Erreurs</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>n°4</p></td>
    <td align="left"><p>Informations/avertissements/Erreurs</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>n°5</p></td>
    <td align="left"><p>Détaillée</p></td>
    </tr>
    </tbody>
    </table>

     

**Pour modifier les paramètres du journal de base de données**

1.  Cliquez sur le nœud **groupes de serveurs** pour afficher les groupes de serveurs.

2.  Cliquez avec le bouton droit sur le groupe de serveurs, puis sélectionnez **Propriétés**.

3.  Dans la boîte de dialogue **Propriétés** , sélectionnez l’onglet **journalisation** .

4.  Dans la boîte de dialogue **Propriétés du groupe de serveurs** , sélectionnez le serveur, puis cliquez sur **modifier**.

5.  Dans la boîte de dialogue **Ajouter/modifier le module journal** , sélectionnez un pilote de base de données dans la liste déroulante **pilote de base de données** .

6.  Entrez un **nom d’hôte DNS**.

7.  Cliquez sur la case à cocher **Déterminez dynamiquement le port** ou entrez un numéro de port dans le champ **port** .

8.  Entrez un **nom de service** dans le champ correspondant.

9.  Cliquez sur **OK**.

10. Dans la boîte de dialogue **Propriétés du groupe de serveurs** , cliquez sur **OK** ou sur **appliquer**.

## Rubriques connexes


[Procédure pour personnaliser un système Application Virtualization dans Server Management Console](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

 

 





