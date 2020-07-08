---
title: Gestion des imprimantes sur un espace de travail MED-V
description: Gestion des imprimantes sur un espace de travail MED-V
author: dansimp
ms.assetid: ba0a65ad-444f-4d18-95eb-8b9fa1a3ffba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bc7a62075c95e8816a425eff89ffb992f1185d04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811562"
---
# Gestion des imprimantes sur un espace de travail MED-V


Dans la version 2,0 de Microsoft Enterprise Desktop Virtualization (MED-V), la redirection d’imprimante fournit aux utilisateurs finaux une expérience d’impression homogène entre l’ordinateur virtuel MED-V et l’ordinateur hôte.

Cette rubrique fournit des informations sur la gestion de l’impression dans un espace de travail MED-V.

## Gestion des imprimantes dans les espaces de travail MED-V


Dans la plupart des cas, MED-V gère automatiquement la redirection de l’imprimante. Après avoir configuré la première fois, MED-V identifie toutes les imprimantes réseau installées sur l’hôte, récupère les pilotes correspondants auprès du serveur d’impression réseau, et, le cas échéant, installe les pilotes pertinents dans l’espace de travail MED-V. Une fois tous les pilotes trouvés et installés, MED-V réamorce l’espace de travail MED-V. En général, une fois que l’espace de travail MED-V est redémarré, les imprimantes hôtes sont présentes et disponibles sur l’invité, en général quelques minutes.

**Remarques**  Si des applications sont exécutées sur l’espace de travail MED-V, l’utilisateur final est invité à laisser le redémarrage continuer ou à le différer jusqu’à ce qu’il soit plus tard. Si aucune application n’est en cours d’exécution, le redémarrage est automatique et n’est pas présenté à l’utilisateur final.

 

Chaque fois que l’application MED-V est redémarrée, elle vérifie si de nouvelles imprimantes sont installées sur l’hôte et, le cas échéant, récupère les pilotes correspondants à partir du serveur d’impression réseau et les installe sur l’invité. MED-V redémarre ensuite l’espace de travail MED-V comme la première fois que vous avez terminé la configuration.

**Important**  Une fois les pilotes pertinents installés sur l’invité, les imprimantes ne deviennent visibles sur l’invité qu’après le redémarrage.

 

Si un pilote est introuvable ou n’est pas installé, il doit être installé manuellement sur l’invité pour que l’imprimante réseau soit disponible pour l’utilisateur final.

La liste suivante fournit des recommandations supplémentaires:

**MED-V gère uniquement les imprimantes réseau**. Les pilotes pour les imprimantes installées localement sur l’hôte ne sont pas automatiquement installés sur l’invité.

**MED-V installe uniquement les pilotes d’imprimante s’il existe sur le serveur d’impression**. Si ce n’est pas le cas, les pilotes d’imprimante doivent être installés manuellement.

**Les imprimantes installées manuellement sur l’invité ne sont pas accessibles à l’hôte**. Par défaut, la fonction MED-V ne prend en charge que la redirection d’imprimante de l’invité vers l’hôte.

**Avertissement**  Si une imprimante est installée manuellement sur l’invité et qu’elle est installée plus tard sur l’hôte, il en résulte que l’imprimante est installée à deux reprises dans l’invité. Pour éviter ce problème, une meilleure pratique MED-V consiste à gérer la redirection de l’impression d’une manière uniquement: désactivez la redirection et l’installation manuelle de l’imprimante sur l’invité, ou activez la redirection et n’installez pas les imprimantes manuellement sur l’invité.

 

## Rubriques connexes


[Gérer les paramètres de l'espace de travail MED-V](manage-med-v-workspace-settings.md)

 

 





