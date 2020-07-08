---
title: Limiter les versions d'objet de stratégie de groupe stockées
description: Limiter les versions d'objet de stratégie de groupe stockées
author: dansimp
ms.assetid: da14edc5-0c36-4c54-b122-861c86b99eb1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 20a3ae60cc330c27cbd19e943ba7f071d4ec60b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808381"
---
# Limiter les versions d'objet de stratégie de groupe stockées


Par défaut, toutes les versions de chaque objet de stratégie de groupe contrôlé (GPO) sont conservées dans l’archive sur le serveur AGPM. Toutefois, vous pouvez limiter le nombre de versions conservées pour chaque objet de stratégie de groupe et supprimer les versions antérieures lorsque cette limite est dépassée. Lors de la suppression des versions d’objets de stratégie de groupe, un enregistrement de la version reste dans l’historique de l’objet de stratégie de groupe, mais la version de l’objet de stratégie de groupe est supprimée de l’archive.

Un compte d’utilisateur disposant du rôle Administrateur AGPM (contrôle total) ou des autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour limiter le nombre de versions d’objets de stratégie de groupe stockées**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans le volet Détails, cliquez sur l’onglet **serveur AGPM** .

3.  Activez les cases à cocher **Supprimer les anciennes versions de chaque GPO de la** case à cocher archiver, puis tapez le nombre maximal de versions d’objets de stratégie de groupe à stocker pour chaque objet de stratégie de groupe, sans inclure la version actuelle. Pour conserver uniquement la version actuelle, entrez 0. La valeur maximale ne doit pas être supérieure à 999.

    **Important**  Uniquement les versions d’objets de stratégie de groupe affichées sous l’onglet **versions uniques** de la fenêtre **historique** vers la limite.

     

4.  Cliquez sur le bouton **appliquer** .

### Autres éléments à prendre en considération

-   Par défaut, vous devez être administrateur AGPM (contrôle total) pour effectuer cette procédure. En particulier, vous devez disposer du **contenu de liste** et des autorisations de **modification des options** pour le domaine.

-   Vous pouvez empêcher la suppression d’une version de l’objet GPO en le marquant dans l’historique comme inéligible pour suppression. Pour cela, cliquez avec le bouton droit sur la version dans l’historique de l’objet de stratégie de groupe et cliquez sur **ne pas supprimer**.

### Références supplémentaires

-   [Gestion de l'archivage](managing-the-archive.md)

 

 





