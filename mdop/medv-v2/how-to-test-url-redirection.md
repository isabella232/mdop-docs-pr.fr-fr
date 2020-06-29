---
title: Comment tester la redirection d'URL
description: Comment tester la redirection d'URL
author: dansimp
ms.assetid: 38d80088-da1d-4098-b27e-76f9e78f81dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d964cf9d0114d3085d7e8952eebc82486b7b76cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810560"
---
# Comment tester la redirection d'URL


Suite à l’exécution de votre test de configuration pour la première fois, vous pouvez vérifier que la fonctionnalité de redirection d’URL fonctionne normalement en effectuant les tâches suivantes.

**Important**  L’agent hôte MED-V doit être en cours d’exécution pour que la redirection d’URL fonctionne correctement.

<a href="" id="bkmk-urlredir"></a>**Pour tester la redirection d’URL**

1.  Ouvrez un navigateur Internet Explorer sur l’ordinateur hôte, puis entrez l’URL que vous avez spécifiée pour la redirection.

2.  Vérifiez que la page Web est ouverte dans Internet Explorer sur l’ordinateur virtuel invité.

3.  Répétez cette procédure pour chaque URL que vous souhaitez tester.

**Pour vérifier qu’il est possible d’ajouter ou de supprimer une URL**

1.  Ajoutez ou supprimez une URL de l’espace de travail MED-V.

    Pour plus d’informations sur la façon d’ajouter et de supprimer des URL pour la redirection dans un espace de travail MED-V, voir [gérer la redirection d’URL med-v](manage-med-v-url-redirection.md).

2.  Si vous avez ajouté une URL à la liste de redirection, répétez les étapes de la procédure [de test de redirection d’URL](#bkmk-urlredir) pour vérifier que la nouvelle URL est redirigée comme prévu.

3.  Si vous avez supprimé une URL de la liste de redirection, vérifiez qu’elle est supprimée en procédant comme suit:

    1.  Ouvrez un navigateur Internet Explorer sur l’ordinateur hôte et entrez l’URL que vous avez supprimée de la liste de redirection.

    2.  Vérifiez que l’ouverture de la page Web s’ouvre dans Internet Explorer sur l’ordinateur hôte plutôt que sur l’ordinateur virtuel invité.

        **Remarques**  Quelques secondes peuvent s’écouler avant que les modifications de redirection d’URL soient effectuées.

**Remarques**  Si vous rencontrez des problèmes lors de la vérification de vos paramètres de redirection d’URL, voir [résolution des problèmes d’opérations](operations-troubleshooting-medv2.md).

Lorsque vous avez terminé de tester la redirection d’URL dans votre espace de travail MED-V, vous pouvez tester d’autres configurations pour vérifier qu’elles fonctionnent comme prévu.

Une fois que vous avez terminé de tester votre package d’espace de travail MED-V et que vous avez vérifié son fonctionnement, vous pouvez déployer l’espace de travail MED-V dans votre entreprise.

## Rubriques connexes

[Comment tester la publication d'applications](how-to-test-application-publishing.md)

[Comment vérifier les paramètres de première installation](how-to-verify-first-time-setup-settings.md)

[Déploiement du package d'espace de travail MED-V](deploying-the-med-v-workspace-package.md)

 

 





