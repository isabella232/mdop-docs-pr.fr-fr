---
title: Installation et suppression d'une application sur l'espace de travail MED-V
description: Installation et suppression d'une application sur l'espace de travail MED-V
author: dansimp
ms.assetid: 24f32720-51ab-4385-adfe-4f5a65e45fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 22cb98c167b53b1b206b8b5be2ba18fc0fba4f06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812222"
---
# Installation et suppression d'une application sur l'espace de travail MED-V


Les applications qui ne sont pas compatibles avec le système d’exploitation hôte peuvent être exécutées dans l’espace de travail MED-V et être ouvertes dans l’espace de travail MED-V de la même manière que dans l’ordinateur hôte, dans le menu **Démarrer** ou à l’aide d’un raccourci localhost.

Après avoir déployé un espace de travail MED-V, vous avez accès à différentes options pour l’installation et la suppression d’applications dans l’espace de travail MED-V. Les options suivantes sont disponibles:

-   [Utilisation d’une stratégie de groupe](#bkmk-grouppolicy)

-   [Utilisation d’un système de distribution de logiciels électronique](#bkmk-esd)

-   [Utilisation de la virtualisation des applications (APP-V)](#bkmk-appv)

-   [Mise à jour de l’image principale](#bkmk-coreimage)

**Important**  Pour vous assurer qu’une application installée est automatiquement publiée sur l’hôte, installez l’application sur l’ordinateur virtuel pour **tous les utilisateurs**. Pour plus d’informations sur la publication d’applications, voir [publication et annulation de la publication d’une application dans l’espace de travail MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).

 

**Astuce**  MED-V ne prend pas en charge la redirection d’invité à hôte pour la gestion de contenu, par exemple en double-cliquant sur un document Microsoft Word dans l’espace de travail MED-V. Par conséquent, les applications requises, comme Microsoft Word, doivent être installées dans l’espace de travail MED-V pour fournir la fonctionnalité de gestion de contenu par défaut qu’un utilisateur final peut attendre.

 

## <a href="" id="bkmk-grouppolicy"></a> Ajout et suppression d’applications à l’aide d’une stratégie de groupe


Vous pouvez utiliser une stratégie de groupe et des objets de stratégie de groupe pour attribuer ou publier des applications dans l’ensemble des espaces de travail MED-V de votre entreprise. S’il s’agit d’une application attribuée, l’application s’affiche dans le menu **Démarrer** . Lorsqu’ils sélectionnent la nouvelle application pour la première fois, l’application s’installe et est prête à être utilisée. Pour les applications publiées, l’application n’apparaît pas dans le menu **Démarrer** . Il est disponible uniquement pour l’utilisateur final pour l’installation à l’aide de l’application **Ajout/suppression de programmes** du **panneau de configuration** ou en ouvrant un fichier associé à l’application.

Vous pouvez également utiliser les objets de stratégie de groupe et de stratégie de groupe de la même manière pour supprimer des applications de l’espace de travail MED-V.

Pour plus d’informations sur la façon d’ajouter et de supprimer des applications à l’aide d’une stratégie de groupe, voir [installation de logiciels de stratégie de groupe](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

## <a href="" id="bkmk-esd"></a> Ajout et suppression d’applications à l’aide d’un système ESD


Un système de distribution de logiciels électronique (ESD) est conçu pour déployer efficacement des logiciels et d’autres informations sur de nombreux ordinateurs sur des connexions réseau. Si votre organisation utilise un système de maintenance ESD pour déployer le logiciel, vous pouvez l’utiliser pour ajouter et supprimer des applications dans les espaces de travail MED-V, de la même façon que vous ajoutez et supprimez des applications sur des ordinateurs physiques.

## <a href="" id="bkmk-appv"></a> Ajout et suppression d’applications à l’aide de APP-V


Microsoft Application Virtualization (App-V) fournit la capacité d’administration de rendre les applications accessibles aux ordinateurs des utilisateurs finaux sans avoir à installer les applications directement sur ces ordinateurs. Vous souhaiterez peut-être utiliser MED-V et App-V conjointement si, par exemple, votre organisation a des applications que vous avez séquencées avec l’application-V dans Windows XP, et que le réséquençage retarderait votre migration vers Windows 7.

Vous pouvez utiliser MED-V conjointement avec App-V pour ajouter et supprimer des applications virtuelles sur un espace de travail MED-V. Pour gérer les applications de cette manière, vous devez d’abord installer l’agent App-V sur le système d’exploitation invité MED-V. Vous pouvez ensuite utiliser App-V dans l’espace de travail MED-V pour ajouter et supprimer les applications virtuelles.

Pour plus d’informations sur la façon d’installer et d’utiliser App-V, voir [virtualisation des applications](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .

**Important**  Les applications App-V que vous publiez sur l’espace de travail MED-V possèdent des associations de types de fichiers qui ne peuvent pas être redirigées de l’ordinateur hôte vers l’ordinateur virtuel invité. Toutefois, l’utilisateur final peut toujours accéder à ces types de fichiers en cliquant sur **fichier**, puis en cliquant sur **ouvrir** dans l’application publiée-V.

Pour forcer la redirection de ces associations de type de fichier, interroger l’application-V pour les associations de types de fichiers mappées en tapant le code suivant à une invite de commandes dans l’ordinateur virtuel invité: **SFTMIME/Query obj: type**. Puis mappez les associations de types de fichiers dans l’ordinateur hôte.

 

## <a href="" id="bkmk-coreimage"></a> Ajout et suppression d’applications sur l’image principale


Même si vous n’avez pas envisagé de meilleures pratiques MED-V, vous pouvez ajouter et supprimer des applications directement sur l’image principale. Après avoir ajouté ou supprimé une application, vous pouvez redéployer l’espace de travail MED-V vers votre entreprise tout comme vous l’avez déployé à l’origine.

Pour plus d’informations sur l’ajout ou la suppression d’applications sur l’image principale, voir [l’installation d’applications sur une image de PC virtuel Windows](installing-applications-on-a-windows-virtual-pc-image.md).

**Important**  Nous déconseillons cette méthode de gestion des applications. Si vous ajoutez ou supprimez des applications sur l’image principale, puis redéployez l’espace de travail MED-V vers votre entreprise, la première fois que vous devez réexécuter le programme d’installation, la première fois que vous devez réexécuter le programme d’installation, les données enregistrées sur l’ordinateur virtuel sont perdues

 

**Remarques**  Même si une application est installée dans un espace de travail MED-V, vous devrez peut-être également publier l’application avant qu’elle ne soit disponible pour l’utilisateur final. Par exemple, il se peut que vous deviez publier une application installée si l’installation n’a pas créé automatiquement de raccourci dans le menu **Démarrer** . De même, pour annuler la publication d’une application, vous devrez peut-être supprimer manuellement un raccourci du menu **Démarrer** .

Par défaut, la plupart des applications sont publiées au moment où elles sont installées, lors de la création et de l’activation automatiques de raccourcis.

 

## Rubriques connexes


[Comment tester la publication d'applications](how-to-test-application-publishing.md)

[Comment publier et annuler la publication d'une application sur l'espace de travail MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





