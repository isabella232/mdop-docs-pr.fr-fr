---
title: Procédure pour configurer ou désactiver la taille de base de données
description: Procédure pour configurer ou désactiver la taille de base de données
author: dansimp
ms.assetid: 4abaf349-132d-4186-8873-a0e515593b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cbb041920e2680d51b01926f144eba595fe28d05
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806757"
---
# Procédure pour configurer ou désactiver la taille de base de données


Vous pouvez utiliser les procédures suivantes dans la console de gestion du serveur d’applications pour spécifier la taille (en Mo) de l’utilisation du système de virtualisation des applications que vous voulez stocker dans la base de données.

Lorsque la taille des données stockées atteint 95% (seuil maximal) de la limite spécifiée, le système supprime 10% des données d’utilisation en laissant 85% des données. Les données d’utilisation des packages et applications seront supprimées. Lorsque la taille de la base de données augmente et qu’elle approche du filigrane le plus élevé, un message d’avertissement est envoyé au journal SQL Server pour vous informer que cette limite a été atteinte. Cet avertissement est nécessaire, car l’action de nettoyage peut affecter la sortie des rapports. Vous pouvez également décider si vous avez besoin d’augmenter la taille maximale de la base de données, de réduire le nombre de mois de données d’utilisation à conserver ou de désactiver le niveau de journalisation.

**Remarques**  Le **champ aucune limite de taille** et **conserver toutes les** options d’utilisation est fourni de sorte que vous puissiez désactiver les rapports d’utilisation et le nettoyage de la base de données. La sélection de ces éléments entraîne le nettoyage du journal de transactions de la base de données. (Toutes les transactions Microsoft SQL Server validées seront supprimées du journal de la base de données.)

 

**Pour configurer la taille de la base de données**

1.  Dans le volet gauche, cliquez avec le bouton droit sur le nœud système de virtualisation des applications, puis sélectionnez **Options système**.

2.  Sélectionnez l’onglet **base de données** .

3.  Activez la case d’option **taille maximale de la base de données (Mo)** ou **aucune taille** .

4.  Si vous choisissez de spécifier une taille de base de données, il est recommandé d’entrer un nombre compris entre 512 et 4096 Mo. La taille par défaut est 1024 Mo et si vous avez besoin d’augmenter la taille de la base de données, la valeur maximale que vous pouvez entrer est 2 147 483 647. Si vous **ne sélectionnez aucune limite de taille**, la base de données augmentera jusqu’à atteindre la limite de taille du disque.

5.  Cliquez sur **appliquer** ou **OK**.

**Pour désactiver les limites de taille de base de données**

1.  Dans le volet **étendue** , cliquez avec le bouton droit sur le nœud système de virtualisation des applications, puis sélectionnez **Options système**.

2.  Sélectionnez l’onglet **base de données** .

3.  Activez les cases d’option **aucune limite de taille** et **conserver toutes les utilisations** .

4.  Cliquez sur **appliquer** ou **OK**.

## Rubriques connexes


[Procédure pour personnaliser un système Application Virtualization dans Server Management Console](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[Procédure pour configurer ou désactiver la création de rapports d'utilisation](how-to-set-up-or-disable-usage-reporting.md)

 

 





