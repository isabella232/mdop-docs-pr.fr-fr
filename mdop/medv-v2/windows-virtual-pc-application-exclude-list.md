---
title: Liste d'exclusion d'applications de WindowsVirtualPC
description: Liste d'exclusion d'applications de WindowsVirtualPC
author: dansimp
ms.assetid: 7715f198-f5ed-421e-8740-0cec2ca4ece3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/28/2017
ms.openlocfilehash: 190049ce99865ef237d8d26e14a8279def7da521
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810109"
---
# Liste d'exclusion d'applications de WindowsVirtualPC


Dans certains cas, il est possible que vous ne souhaitiez pas que les applications installées dans l’espace de travail MED-V soient publiées sur le menu **Démarrer** de l’ordinateur hôte. Vous pouvez annuler la publication de ces applications en suivant les instructions de la [procédure de publication et d’annulation de la publication d’une application dans l’espace de travail MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md). Toutefois, si le programme a déjà été automatiquement mis à jour, il peut également être republié automatiquement. Ainsi, vous devrez annuler la publication de l’application.

Windows Virtual PC inclut une fonctionnalité appelée «liste d’exclusion» qui vous permet de spécifier certaines applications installées que vous ne souhaitez pas publier dans le menu **Démarrer** de l’hôte. La «liste d’exclusion» est située dans le registre invité dans la clé HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList et répertorie les applications qui ne sont pas publiées dans le menu **Démarrer** de l’hôte. Vous pouvez considérer la «liste d’exclusion» comme annuler définitivement la publication des applications spécifiées, car toutes les mises à jour automatiques des applications qui sont répertoriées n’entraînent pas leur republication automatique.

## Gestion des applications à l’aide de la liste d’exclusion dans le PC virtuel Windows


****

1.  Ouvrir l’espace de travail MED-V en plein écran.

    Pour plus d’informations sur l’ouverture de l’espace de travail MED-V en mode plein écran à l’aide du kit de tâches d’administration de MED-v, voir [affichage des configurations d’espace de travail MED-v](viewing-med-v-workspace-configurations.md#bkmk-fullscreen). Ou vous pouvez l’ouvrir manuellement en mode plein écran en cliquant sur **Démarrer**, sur **tous les programmes**, sur **PC virtuel Windows**, sur **PC virtuel Windows**, puis en double-cliquant sur l’espace de travail MED-V.

2.  Dans la fenêtre Windows Virtual PC de l’espace de travail MED-V, ouvrez l’éditeur du Registre.

    Cliquez sur **Démarrer**, sur **exécuter**, puis tapez regedit. Cliquez ensuite sur **OK**.

3.  Dans l’éditeur du Registre, recherchez la clé de Registre HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList.

4.  Créez une nouvelle valeur de Registre pour l’application installée que vous ne souhaitez pas publier sur le menu **Démarrer** de l’ordinateur hôte. Par exemple, si vous voulez annuler la publication du programme publié automatiquement Microsoft Silverlight, procédez comme suit:

    1.  Après avoir sélectionné la clé de Registre VPCVAppExcludeList, cliquez sur **modifier**, sur **nouveau**, puis sur **valeur de chaîne**.

    2.  Entrez le nom de la nouvelle valeur de registre. Par exemple, pour Microsoft Silverlight, vous pouvez entrer sllauncher.exe.

    3.  Double-cliquez sur la nouvelle valeur du Registre et entrez les données de la valeur.

        Le champ données de la valeur correspond au chemin d’accès complet de la commande dont vous voulez annuler la publication. Pour trouver le chemin d’accès complet, cliquez avec le bouton droit sur le raccourci du menu **Démarrer** de l’application que vous ne souhaitez pas publier, puis cliquez sur **Propriétés**. Le chemin d’accès complet figure dans l’onglet **raccourci** de **target**.

        Par exemple, pour le programme Microsoft Silverlight, le chemin d’accès complet peut être «C:\\Program Files\\Microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe».

        **Important**  Le cas échéant, supprimez les guillemets du chemin d’accès complet lorsque vous entrez dans le champ données de la valeur.

         

5.  Fermez l’éditeur du Registre et redémarrez l’ordinateur virtuel de l’espace de travail MED-V.

    L’application est toujours installée sur l’espace de travail MED-V, mais elle est désormais supprimée du menu **Démarrer** de l’ordinateur hôte.

Vous pouvez également republier une application exclus dans le menu **Démarrer** de l’hôte en supprimant la valeur correspondante de la clé VPCVAppExcludeList. Par exemple, pour republier Microsoft Silverlight, cliquez avec le bouton droit sur la valeur du Registre sllauncher.exe puis sélectionnez **supprimer**.

## Rubriques connexes


[Informations techniques de référence pour MED-V](technical-reference-for-med-v.md)

[Comment publier et annuler la publication d'une application sur l'espace de travail MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





