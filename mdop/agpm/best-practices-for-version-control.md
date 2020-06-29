---
title: Meilleures pratiques en matière de gestion de version
description: Meilleures pratiques en matière de gestion de version
author: dansimp
ms.assetid: 89067f6a-f7ea-4dad-999d-118284cf6c5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ed91408faeb8968175976382f9dd97d45becddb5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807813"
---
# Meilleures pratiques en matière de gestion de version


Microsoft Advanced Group Policy Management (AGPM) fournit un contrôle de version pour les objets de stratégie de groupe de la même manière que Microsoft Visual SourceSafe® fournit un contrôle de version pour le code source. Les développeurs peuvent utiliser Visual SourceSafe pour gérer plusieurs versions de chaque fichier source. Les administrateurs de stratégie de groupe peuvent utiliser AGPM pour faire la même chose pour les objets de stratégie de groupe. Lorsque vous utilisez AGPM, les administrateurs de stratégie de groupe doivent tenir compte des meilleures pratiques qui s’appliquent à n’importe quel système de contrôle de version:

-   **Date et heure:** AGPM horodate chaque version d’un objet de stratégie de groupe avec la date et l’heure. Pour garantir l’exactitude de l’historique, en particulier lorsque vous modifiez les objets de stratégie de groupe sur plusieurs ordinateurs, assurez-vous que chaque ordinateur synchronise son horloge avec une source de temps faisant autorité.

-   **Archiver les objets de stratégie de groupe lorsque vous avez terminé de les modifier:** Il est courant que les éditeurs vérifient les objets de stratégie de groupe et oubliez de les archiver dans l’archive. Toutefois, cela peut empêcher d’autres administrateurs de stratégie de groupe de modifier l’objet GPO. Vérifiez toujours les objets de stratégie de groupe sur AGPM dès que vous avez terminé la modification.

-   **Enregistrer les modifications fréquemment:** Lorsque vous modifiez un objet de stratégie de groupe, enregistrez fréquemment les modifications. La plupart des éditeurs contrôlent un objet de stratégie de groupe, apporte de nombreuses modifications, puis vérifient l’objet de stratégie de groupe dans l’archive. Activez plutôt l’objet de stratégie de groupe dans l’archive, puis vérifiez-le à nouveau. Les détails peuvent être aussi petits que le contrôle de l’objet de stratégie de groupe après avoir modifié chaque paramètre (non recommandé) ou d’archiver l’objet de stratégie de groupe une fois que vous avez effectué des modifications apportées aux groupes. Le résultat est un historique mieux documenté de chaque GPO qui peut vous aider lors de la résolution des problèmes.

-   **Déployez fréquemment les objets de stratégie de groupe:** Ne laissez pas les objets de stratégie de groupe nouveaux et modifiés qui n’ont pas encore été déployés dans de grands nombres de l’archive. Au lieu de cela, le déploiement d’objets de stratégie de groupe nouveaux et modifiés est le plus rapide possible dans l’environnement de production. Le déploiement d’un grand nombre d’objets de stratégie de groupe à la fois peut mettre en péril l’environnement de production.

-   **Documentez l’objet des modifications lorsque vous archivez des objets de stratégie de groupe:** Les réviseurs peuvent comparer les versions d’un objet de stratégie de groupe pour voir les modifications spécifiques apportées entre les deux. La documentation de ces modifications spécifiques n’entraîne aucune valeur. À la place, documentez l’intention et l’objet d’une modification au lieu de documenter les réviseurs à afficher en affichant les rapports de différences. Les commentaires de version doivent ajouter de la valeur au rapport de comparaison et permettent aux réviseurs de comprendre pourquoi l’éditeur a modifié l’objet de stratégie de groupe.

-   **Testez les objets de stratégie de groupe en laboratoire avant de procéder au déploiement:** Le déploiement d’objets de stratégie de groupe dans l’environnement de production sans tests préalables est risqué. Au lieu de cela, testez les objets de stratégie de groupe dans un environnement Lab en les associant à une unité d’organisation qui contient les ordinateurs et les utilisateurs de test, puis vérifiez qu’ils fonctionnent correctement. Après vérification de chaque GPO dans le laboratoire, déployez l’objet GPO dans l’environnement de production.

### Références supplémentaires

-   [Guide des opérations de la Gestion avancée des stratégies de groupe Microsoft3.0](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





