---
title: Procédure pour modifier les niveaux de création de rapport de suivi et réinitialiser les fichiers journaux
description: Procédure pour modifier les niveaux de création de rapport de suivi et réinitialiser les fichiers journaux
author: dansimp
ms.assetid: 9561d6fb-b35c-491b-a355-000064583194
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7307dee0030d9c03a8107d9d0ceef2086a94df07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807350"
---
# Procédure pour modifier les niveaux de création de rapport de suivi et réinitialiser les fichiers journaux


Vous pouvez utiliser la procédure suivante pour modifier le niveau de rapport du journal à partir du nœud **virtualisation** des applications de la console de gestion des applications. Lorsque le fichier journal atteint la taille maximale (la valeur par défaut est 256 Mo), une réinitialisation est imposée lors de l’écriture suivante du journal. Une réinitialisation entraîne la création d’un nouveau fichier journal et l’ancien fichier est renommé comme sauvegarde.

**Pour modifier le niveau de rapport du journal**

1.  Cliquez avec le bouton droit sur le nœud **Application Virtualization** , puis sélectionnez **Propriétés** dans le menu contextuel.

2.  Dans l’onglet **général** de la boîte de dialogue **Propriétés** , dans la liste déroulante **niveau du journal** , sélectionnez le niveau de journal souhaité.

    **Remarques**  Si vous choisissez l’affichage **détaillé** comme niveau de journalisation, les fichiers journaux seront considérablement volumineux. Comme cela peut inhiber les performances du client, il est recommandé d’utiliser ce niveau de journal uniquement pour diagnostiquer des problèmes spécifiques.

     

3.  Dans l’onglet **général** de la boîte de dialogue **Propriétés** , dans la liste déroulante **niveau du journal système** , sélectionnez le niveau de journal souhaité.

    **Remarques**  Le paramètre **niveau du journal système** contrôle le niveau de messages envoyés au journal des événements système. Les messages enregistrés sont identiques à ceux qui sont enregistrés dans le journal des événements du client, mais qui sont stockés à un autre emplacement.

     

4.  Cliquez sur **OK** ou sur **appliquer** pour modifier le paramètre.

**Pour réinitialiser le fichier journal**

1.  Cliquez avec le bouton droit sur le nœud **Application Virtualization** , puis sélectionnez **Propriétés** dans le menu contextuel.

2.  Dans l’onglet **général** de la boîte de dialogue **Propriétés** , cliquez sur **Réinitialiser le journal** pour sauvegarder le fichier journal actuel et commencer immédiatement un nouveau fichier journal. Les fichiers journaux de sauvegarde sont stockés dans le même dossier.

3.  Cliquez sur **OK** ou sur **appliquer** pour modifier le paramètre.

## Rubriques connexes


[Procédure pour configurer le client dans Application Virtualization Client Management Console](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

[Autorisations d'accès utilisateur dans Application Virtualization Client](user-access-permissions-in-application-virtualization-client.md)

 

 





