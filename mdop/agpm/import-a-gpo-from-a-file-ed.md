---
title: Importer un objet de stratégie de groupe à partir d'un fichier
description: Importer un objet de stratégie de groupe à partir d'un fichier
author: dansimp
ms.assetid: 6e901a52-1101-4fed-9f90-3819b573b378
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15704806f089bb0d8530cd84df64b0889413426
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808421"
---
# Importer un objet de stratégie de groupe à partir d'un fichier


Dans Advanced Group Policy Management (AGPM), si vous avez exporté un objet de stratégie de groupe (GPO) vers un fichier CAB, vous pouvez importer les paramètres de stratégie de cet objet GPO dans un objet de stratégie de groupe existant d’un domaine d’une autre forêt. L’importation des paramètres de stratégie dans un objet de stratégie de groupe existant remplace tous les paramètres de stratégie de cet objet. Pour plus d’informations sur l’exportation des paramètres d’objet de stratégie de groupe dans un fichier CAB, voir [exporter un objet de stratégie de groupe dans un fichier](export-a-gpo-to-a-file.md).

Un compte d’utilisateur ayant le rôle d’éditeur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.Passez en revue les détails dans «autres considérations» dans cette rubrique.

## <a href="" id="bkmk-existing"></a>


**Pour importer les paramètres de stratégie dans un objet de stratégie de groupe existant**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans le domaine dans lequel vous voulez importer les paramètres de stratégie.

2.  Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

3.  Consultez l’objet GPO de destination sur lequel vous souhaitez importer les paramètres de stratégie.

4.  Cliquez avec le bouton droit sur l’objet GPO de destination, pointez sur **Importer à partir de**, puis cliquez sur **fichier**.

5.  Suivez les instructions de l' **Assistant importation de paramètres** pour sélectionner une sauvegarde d’objet de stratégie de groupe, importez les paramètres de la stratégie de votre choix pour remplacer celles de l’objet GPO de destination et entrez un commentaire pour la piste d’audit de l’objet GPO de destination. Par défaut, l’objet GPO de destination est réintégré lorsque l’Assistant est terminé.

### Autres éléments à prendre en considération

-   Par défaut, vous devez être un éditeur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure. En particulier, vous devez disposer d’un **contenu de liste**, **modifier des paramètres**et importer des autorisations d’objets de **stratégie de groupe** pour le domaine, et l’objet de stratégie de groupe doit être extrait par vous.

-   Même si un éditeur ne peut pas importer les paramètres de stratégie dans un nouvel objet GPO lors de sa création, un éditeur peut demander la création d’un nouvel objet de stratégie de groupe, puis importer les paramètres de stratégie dans ce dernier après sa création.

### Références supplémentaires

-   [Utilisation d'un environnement de test](using-a-test-environment.md)

 

 





