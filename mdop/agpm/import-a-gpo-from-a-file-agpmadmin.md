---
title: Importer un objet de stratégie de groupe à partir d'un fichier
description: Importer un objet de stratégie de groupe à partir d'un fichier
author: dansimp
ms.assetid: 2cbcda72-4de3-47ad-aaf8-4fc7341d5a00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 04819dacac8df73f0a61cace0dab8b9fa79b7307
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808433"
---
# Importer un objet de stratégie de groupe à partir d'un fichier


Dans Advanced Group Policy Management (AGPM), si vous êtes un administrateur AGPM (contrôle total) et si vous avez exporté un objet de stratégie de groupe (GPO) vers un fichier CAB, vous pouvez importer les paramètres de stratégie de cet objet GPO dans un nouvel objet de stratégie de groupe ou un objet de stratégie de groupe existant dans un domaine d’une autre forêt. Pour plus d’informations sur l’exportation des paramètres d’objet de stratégie de groupe dans un fichier CAB, voir [exporter un objet de stratégie de groupe dans un fichier](export-a-gpo-to-a-file.md).

Un compte d’utilisateur ayant le rôle d’administrateur AGPM ou les autorisations nécessaires dans AGPM est requis pour importer les paramètres de stratégie dans un nouvel objet de stratégie de groupe contrôlé. Un compte d’utilisateur possédant le rôle d’administrateur de l’éditeur ou d’AGPM ou les autorisations nécessaires dans AGPM est requis pour importer les paramètres de stratégie dans un objet de stratégie de groupe existant. Passez en revue les détails dans «autres considérations» dans cette rubrique.

## Importation des paramètres de stratégie à partir d’un fichier


Lorsque vous importez des paramètres de stratégie à partir d’un fichier, vous pouvez les importer dans un nouvel objet de stratégie de groupe ou un objet de stratégie de groupe existant. Toutefois, si vous importez des paramètres de stratégie dans un objet de stratégie de groupe existant, tous les paramètres de stratégie qu’il contient sont remplacés.

-   [Importer les paramètres de stratégie dans un nouvel objet de stratégie de groupe contrôlé](#bkmk-new)

-   [Importer les paramètres de stratégie dans un objet de stratégie de groupe existant](#bkmk-existing)

### <a href="" id="bkmk-new"></a>

**Pour importer les paramètres de stratégie dans un nouvel objet de stratégie de groupe contrôlé**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans le domaine dans lequel vous voulez importer les paramètres de stratégie.

2.  Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

3.  Créer un objet de stratégie de groupe contrôlé. Dans la boîte de dialogue **nouvel objet GPO contrôlé** , cliquez sur **Importer** , puis sur **Assistant lancement**. Pour plus d’informations sur la création d’un objet de stratégie de groupe, voir [créer un objet de stratégie de groupe contrôlé](create-a-new-controlled-gpo-agpm40.md).

4.  Suivez les instructions de l' **Assistant importation de paramètres** pour sélectionner une sauvegarde de l’objet de stratégie de groupe, importer les paramètres de stratégie de celle-ci pour le nouvel objet de stratégie de groupe et entrer un commentaire pour la trace d’audit du nouvel objet de stratégie de groupe.

### <a href="" id="bkmk-existing"></a>

**Pour importer les paramètres de stratégie dans un objet de stratégie de groupe existant**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans le domaine dans lequel vous voulez importer les paramètres de stratégie.

2.  Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

3.  Consultez l’objet GPO de destination sur lequel vous souhaitez importer les paramètres de stratégie.

4.  Cliquez avec le bouton droit sur l’objet GPO de destination, pointez sur **Importer à partir de**, puis cliquez sur **fichier**.

5.  Suivez les instructions de l' **Assistant importation de paramètres** pour sélectionner une sauvegarde d’objet de stratégie de groupe, importez les paramètres de la stratégie de votre choix pour remplacer celles de l’objet GPO de destination et entrez un commentaire pour la piste d’audit de l’objet GPO de destination. Par défaut, l’objet GPO de destination est réintégré lorsque l’Assistant est terminé.

### Autres éléments à prendre en considération

-   Pour importer les paramètres de stratégie dans un nouvel objet de stratégie de groupe, vous devez disposer d’un **contenu de liste**, d’importer un **objet de stratégie**de groupe et de créer des autorisations d' **objet GPO** pour le domaine. Par défaut, vous devez être administrateur d’AGPM pour effectuer cette procédure.

-   Pour importer les paramètres de stratégie d’un objet de stratégie de groupe existant, vous devez disposer d’un **contenu de liste**, **modifier des paramètres**et importer des autorisations d' **objets** de stratégie de groupe pour le domaine et l’objet de stratégie de groupe doit être extrait par vous. Par défaut, vous devez être un éditeur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.

### Références supplémentaires

-   [Gestion de l'archivage](managing-the-archive-agpm40.md)

 

 





