---
title: Tester un objet de stratégie de groupe dans une unité d'organisation distincte
description: Tester un objet de stratégie de groupe dans une unité d'organisation distincte
author: dansimp
ms.assetid: 9a9e6d22-74e6-41d8-ac2f-12a1b76ad5a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 509721fdd775c8669399549f6dcc29cb9ebaea2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807434"
---
# Tester un objet de stratégie de groupe dans une unité d'organisation distincte


Si vous utilisez une unité d’organisation de test (UO) pour tester les objets de stratégie de groupe au sein d’un même domaine avant de procéder au déploiement vers l’environnement de production, vous devez disposer des autorisations nécessaires pour accéder à l’unité d’organisation de test. L’utilisation d’une UO de test est facultative.

**Pour utiliser une UO de test**

1.  Même si l’objet de stratégie de groupe est extrait pour modification, dans la **console de gestion des stratégies de groupe**, cliquez sur objets de stratégie de **groupe** dans la forêt et dans le domaine dans lequel vous gérez les objets de stratégie de groupe.

2.  Cliquez sur la copie extraite de l’objet de stratégie de groupe à tester. Le nom est précédé de **\ [AGPM \]**. (S’il n’apparaît pas dans la liste, cliquez sur **action**, puis sur **Actualiser**. Triez les noms par ordre alphabétique, et les objets de stratégie de groupe **\ [AGPM \]** apparaissent généralement en haut de la liste.)

3.  Faites glisser l’objet GPO vers l’unité d’organisation test.

4.  Cliquez sur **OK** dans la boîte de dialogue qui vous demande si vous souhaitez créer un lien vers l’objet de stratégie de groupe dans l’unité d’organisation test.

### Autres éléments à prendre en considération

-   Une fois le test terminé, l’archivage de l’objet de stratégie de groupe supprime automatiquement le lien vers la copie extraite de l’objet GPO.

### Références supplémentaires

-   [Utilisation d'un environnement de test](using-a-test-environment.md)

 

 





