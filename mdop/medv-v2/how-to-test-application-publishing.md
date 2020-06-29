---
title: Comment tester la publication d'applications
description: Comment tester la publication d'applications
author: dansimp
ms.assetid: 17ba2e12-50a0-4f41-8300-f61f09db9f6c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 8dffb4f79ac89c7d419b27640f4f05364bd69e5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812041"
---
# Comment tester la publication d'applications


Suite à l’exécution de votre test de configuration pour la première fois, vous pouvez vérifier que la fonctionnalité de publication des applications fonctionne normalement en effectuant les tâches suivantes.

<a href="" id="bkmk-apppub"></a>**Pour tester la publication d’applications**

1.  Vérifiez que les applications que vous avez spécifiées pour la publication sont visibles.

    Cliquez sur **Démarrer** , puis sur **tous les programmes** et recherchez les applications spécifiées.

    Dans certains cas, vous pouvez avoir installé la même application deux fois, une fois sur l’ordinateur hôte et une fois sur l’invité. Si une application publiée qui porte le même nom est publiée au même emplacement dans le menu de **démarrage** de l’hôte, elle se distingue du raccourci de l’application hôte en ajoutant le nom de l’ordinateur virtuel au nom du raccourci. Par exemple, dans le cas d’un ordinateur virtuel appelé «MEDVHost1», une application hôte peut être «bloc-notes» et une application publiée peut être «bloc-notes (MEDVHost1)».

2.  Vérifiez que les applications fonctionnent comme prévu.

    Sur l’ordinateur hôte, démarrez les applications que vous avez publiées et vérifiez qu’elles s’ouvrent dans Windows XP SP3 sur l’invité. L’application doit s’afficher dans une fenêtre de style Windows XP sur le Bureau de l’ordinateur hôte.

3.  Le cas échéant, vérifiez que les fonctions de redirection de document comme prévu.

    Si une application publiée sur l’invité doit ouvrir un dossier sur le lecteur du système hôte, assurez-vous qu’elle peut ouvrir le dossier spécifié.

    **Important**  Comme le PC virtuel Windows ne prend pas en charge la création d’un partage à partir d’un dossier déjà partagé, la redirection ne se produit pas pour tous les documents qui s’ouvrent à partir d’un dossier partagé, tels que le dossier Mes documents qui se trouve sur le réseau. Pour plus d’informations, reportez-vous à [résolution des problèmes d’opérations](operations-troubleshooting-medv2.md).

Une fois que vous avez vérifié que les applications publiées sont installées et fonctionnent correctement, vous pouvez tester s’il est possible d’ajouter ou de supprimer des applications à partir de l’espace de travail MED-V.

**Pour vérifier qu’il est possible d’ajouter ou de supprimer une application**

1.  Ajoutez ou supprimez une application de l’espace de travail MED-V.

    Pour plus d’informations sur la façon d’ajouter et de supprimer des applications d’un espace de travail MED-V, voir [gestion des applications déployées dans les espaces de travail MED-v](managing-applications-deployed-to-med-v-workspaces.md).

2.  Si vous avez ajouté une application, répétez les étapes décrites dans la procédure [de test](#bkmk-apppub) de la publication d’applications pour vérifier que la nouvelle application fonctionne comme prévu.

3.  Si vous avez supprimé une application, cliquez sur **Démarrer** , puis sur **tous les programmes** et assurez-vous que les applications que vous avez supprimées ne sont plus répertoriées.

**Remarques**  Si vous rencontrez des problèmes lors de la vérification des paramètres de composition de votre application, voir [résolution des problèmes d’opérations](operations-troubleshooting-medv2.md).

Une fois que vous avez terminé le test de la publication d’une application, vous pouvez tester les autres configurations d’espace de travail MED-V pour vérifier qu’elles fonctionnent comme prévu.

Une fois que vous avez terminé de tester votre package d’espace de travail MED-V et que vous avez vérifié son fonctionnement, vous pouvez déployer l’espace de travail MED-V dans votre entreprise.

## Rubriques connexes

[Comment tester la redirection d'URL](how-to-test-url-redirection.md)

[Comment vérifier les paramètres de première installation](how-to-verify-first-time-setup-settings.md)

[Déploiement du package d'espace de travail MED-V](deploying-the-med-v-workspace-package.md)

 

 





