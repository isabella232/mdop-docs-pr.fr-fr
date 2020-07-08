---
title: Procédure pour configurer ou désactiver la création de rapports d'utilisation
description: Procédure pour configurer ou désactiver la création de rapports d'utilisation
author: dansimp
ms.assetid: 8587003a-128d-4b5d-ac70-5b9eddddd3dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f8f6c44d4060581f1ebe435875bc2f105cb93d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806750"
---
# Procédure pour configurer ou désactiver la création de rapports d'utilisation


Vous pouvez utiliser les procédures suivantes dans la console de gestion du serveur d’applications pour spécifier la durée (en mois) des informations d’utilisation du système de virtualisation des applications que vous voulez stocker dans la base de données.

**Remarques**  Pour stocker les informations d’utilisation, vous devez activer la case à cocher **journalisation des informations d’utilisation** sous l’onglet **pipeline du fournisseur** . Pour afficher cet onglet, cliquez avec le bouton droit sur la stratégie du fournisseur dans le volet de **résultats stratégies du fournisseur** , puis sélectionnez **Propriétés**.

 

**Pour configurer la création de rapports d’utilisation**

1.  Dans le volet gauche, cliquez avec le bouton droit sur le nœud système de virtualisation des applications, puis sélectionnez **Options système**.

2.  Sélectionnez l’onglet **base de données** .

3.  Sélectionnez la case **d’option conserver l’utilisation pour (mois)** ou **conserver tout l’utilisation** .

4.  Si vous choisissez de spécifier la durée d’utilisation en mois, entrez un nombre compris entre 1 et 120 (la valeur par défaut est 6 mois). Si vous sélectionnez **conserver toute l’utilisation**, la base de données s’étire jusqu’à ce qu’elle atteigne la taille limite spécifiée.

5.  Cliquez sur **appliquer** ou **OK**.

**Pour désactiver la création de rapports d’utilisation**

1.  Cliquez sur le nœud **stratégies du fournisseur** .

2.  Cliquez avec le bouton droit sur **stratégie du fournisseur** , puis sélectionnez **Propriétés**.

3.  Sélectionnez l’onglet **pipeline du fournisseur** .

4.  Décochez la case **journaliser les informations d’utilisation** .

5.  Cliquez sur **appliquer** ou **OK**.

## Rubriques connexes


[Procédure pour personnaliser un système Application Virtualization dans Server Management Console](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[Procédure pour configurer ou désactiver la taille de base de données](how-to-set-up-or-disable-database-size.md)

 

 





