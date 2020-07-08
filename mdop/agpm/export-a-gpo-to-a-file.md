---
title: Exporter un objet de stratégie de groupe dans un fichier
description: Exporter un objet de stratégie de groupe dans un fichier
author: dansimp
ms.assetid: 0d01b1f7-a6a4-4d0d-9aa7-2d6f1ae93d9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4622930cb0e5b439649cc0445ae2b3d02d7d3224
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808473"
---
# Exporter un objet de stratégie de groupe dans un fichier


Vous pouvez exporter un objet de stratégie de groupe contrôlé (GPO) vers un fichier CAB de sorte que vous puissiez le copier dans un domaine d’une autre forêt et importer l’objet GPO dans Advanced Group Policy Management (AGPM) dans ce domaine. Pour plus d’informations sur l’importation des paramètres de l’objet de stratégie de groupe dans un objet GPO nouveau ou existant, voir [Importer un objet GPO à partir d’un fichier](import-a-gpo-from-a-file-ed.md).

Un compte d’utilisateur ayant le rôle d’éditeur ou d’administrateur AGPM (contrôle total) ou les autorisations nécessaires dans Advanced Group Policy Management (AGPM) est requis pour effectuer cette procédure.Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour exporter un objet de stratégie de groupe dans un fichier**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.

2.  Dans l’onglet **contenu** , cliquez sur l’onglet **contrôlé** pour afficher les objets de stratégie de groupe contrôlés.

3.  Cliquez avec le bouton droit sur l’objet de stratégie de groupe, puis cliquez sur **Exporter vers**.

4.  Entrez un nom de fichier pour le fichier dans lequel vous voulez exporter l’objet de stratégie de groupe, puis cliquez sur **Exporter**. Si le fichier n’existe pas, il est créé. S’il existe déjà, il est remplacé.

### Autres éléments à prendre en considération

-   Par défaut, vous devez être un éditeur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure. Plus précisément, vous devez disposer d’autorisations de **liste**, de **paramètres de lecture**et d' **exportation d’objets** de stratégie de groupe.

### Références supplémentaires

-   [Utilisation d'un environnement de test](using-a-test-environment.md)

 

 





