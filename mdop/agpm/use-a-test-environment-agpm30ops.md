---
title: Utiliser un environnement de test
description: Utiliser un environnement de test
author: dansimp
ms.assetid: 86295084-b39e-4040-bb3f-15c3c1e99b1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1264d9fe6f922a7e61bcd069581c7bd5e39b7787
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807426"
---
# Utiliser un environnement de test


Si vous utilisez une unité d’organisation de test (UO) pour tester les objets de stratégie de groupe avant le déploiement dans l’environnement de production, vous devez disposer des autorisations nécessaires pour accéder à l’unité d’organisation test. L’utilisation d’une UO de test est facultative.

**Pour utiliser une UO de test**

1.  Dans la console de gestion des stratégies de groupe, dans la **console de gestion des stratégies de groupe**, cliquez sur objets de **stratégie de groupe** dans la forêt et le domaine dans lequel vous gérez les objets de stratégie de groupe.

2.  Cliquez sur la copie extraite de l’objet de stratégie de groupe à tester. Le nom est précédé de **\ [extrait.]**. (S’il n’apparaît pas dans la liste, cliquez sur **action**, puis sur **Actualiser**. Triez les noms par ordre alphabétique, et les objets de stratégie de groupe **\ [extraits]** apparaissent généralement en haut de la liste.)

3.  Faites glisser et déplacez l’objet GPO vers l’unité d’organisation test.

4.  Cliquez sur **OK** dans la boîte de dialogue qui vous demande si vous souhaitez créer un lien vers l’objet GPO dans l’unité d’organisation de test.

### Autres éléments à prendre en considération

-   Une fois le test terminé, l’archivage de l’objet de stratégie de groupe supprime automatiquement le lien vers la copie extraite de l’objet GPO.

### Références supplémentaires

-   [Modification d'un objet de stratégie de groupe](editing-a-gpo-agpm30ops.md)

 

 





