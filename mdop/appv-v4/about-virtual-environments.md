---
title: À propos des environnements virtuels
description: À propos des environnements virtuels
author: dansimp
ms.assetid: e03a8c72-56c1-4ae9-aa45-0283c50a154c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15f3ae29ae8d5586f83baa98ea6821e09ae5c305
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809329"
---
# À propos des environnements virtuels


Les applications virtuelles s’exécutent en environnement virtuel. Les environnements virtuels permettent à chaque application de s’exécuter sur un ordinateur de bureau, un ordinateur portable ou un serveur hôte de session Bureau à distance. Chaque application possède ses propres informations de configuration dans l’environnement virtuel. Par conséquent, de nombreuses applications sont exécutées côte à côte avec d’autres applications sur le même ordinateur sans aucun conflit.

Les applications virtuelles s’exécutent en local, de sorte qu’elles s’exécutent avec les performances complètes, les fonctionnalités et l’accès aux services locaux que vous attendez d’une application installée en local.

Dans la mesure où chaque application s’exécute dans un environnement virtuel, les problèmes suivants sont réduits:

-   Conflits d’application: dans les environnements qui n’utilisent pas la virtualisation de l’application, vous devez tester soigneusement chaque application pour vérifier qu’elle n’interfère pas avec d’autres applications installées.

-   Tests de régression: dans la mesure où l’application ne modifie pas le système d’exploitation sous-jacent, le test de régression de longue durée est éliminé.

-   Incompatibilités de version: différentes versions d’une même application peuvent être exécutées simultanément sur le même ordinateur.

-   Accès multi-utilisateurs: les applications qui ne sont pas exécutées en mode multiutilisateur et qui ne peuvent pas être exécutées au sein d’un hôte RDSession, peuvent désormais le faire et fonctionner correctement pour plusieurs utilisateurs sur un seul hôte RDSession.

-   Problèmes de location mutualisée: deux instances de la même application qui utilisent des configurations différentes peuvent être exécutées sur le même ordinateur en même temps.

-   Les silos de serveurs: le nombre de batteries de serveurs distinctes est éliminé.

Les environnements virtuels incluent un registre virtuel pour chaque application. Les paramètres de Registre créés par une application ne sont pas visibles par d’autres applications ou utilitaires tels que Regedit. Au lieu de copier l’intégralité du Registre, le registre virtuel utilise une méthode de *superposition* . Les éléments du registre client peuvent être lus par l’application tant qu’une copie virtuelle de cet élément de Registre n’est pas incluse dans le registre virtuel. Toutes les écritures apportées à l’application du Registre sont contenues dans le registre virtuel.

Les environnements virtuels incluent également un système de fichiers virtuel et d’autres composants virtuels, notamment les services virtuels et le COM virtuel.

## Rubriques connexes


[Vue d'ensemble d'Application Virtualization Client Management Console](application-virtualization-client-management-console-overview.md)

 

 





