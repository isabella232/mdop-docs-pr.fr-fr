---
title: Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour tous les utilisateurs sur un ordinateur spécifique
description: Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour tous les utilisateurs sur un ordinateur spécifique
author: dansimp
ms.assetid: 64640b8e-de6b-4006-a33e-353d285af15e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: ce8d5cc0e79be46fd9680a3bea0236bbeb93ea83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805191"
---
# Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour tous les utilisateurs sur un ordinateur spécifique


Utilisez la procédure suivante pour rétablir les points d’extension d’un package App-V 5,1 au format de fichier App-V 4,6 à l’aide du fichier de configuration de déploiement.

**Pour rétablir un package**

1.  Assurez-vous que le package App-V 4,6 est publié pour les utilisateurs, mais que les FTAs et raccourcis ont été supposés par le package App-v 5,1 à l’aide de la méthode de migration suivante, [Comment migrer des points d’extension d’un package App-v 4,6 vers un package App-v 5,1 pour tous les utilisateurs sur un ordinateur en particulier](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md).

    Dans la section **userConfiguration** du fichier de configuration de déploiement pour le package converti, pour définir la stratégie, effectuez la mise à jour suivante vers la section **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "FALSe" PackageName = &lt; &gt; ID de package**

2.  À partir d’une invite de commandes avec élévation de privilèges, tapez:

    PS &gt; **Set-AppvClientPackage $pkg – chemin DynamicDeploymentConfiguration** &lt; au fichier de configuration de déploiement&gt;

    &gt;**Publication PS-AppVClientPackage $pkg-DynamicUserConfigurationType useDeploymentConfiguration**

3.  Effectue une actualisation de publication ou attend la prochaine actualisation de publication planifiée pour le package App-V 4,6.

    Ouvrez l’application à l’aide de FTAs ou de raccourcis. L’application doit maintenant s’ouvrir à l’aide de App-V 4,6.

    **Remarque**  
    Si vous n’avez plus besoin du package App-V 5,1, vous pouvez annuler la publication du package App-V 5,1 et les points d’extension seront automatiquement rétablis sur App-V 4,6.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Rubriques connexes


[Opérations d'App-V5.1](operations-for-app-v-51.md)









