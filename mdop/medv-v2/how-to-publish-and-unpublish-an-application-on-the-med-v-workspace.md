---
title: Comment publier et annuler la publication d'une application sur l'espace de travail MED-V
description: Comment publier et annuler la publication d'une application sur l'espace de travail MED-V
author: dansimp
ms.assetid: fd5a62e9-0577-44d2-ae17-61c0aef78ce8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc8f9579d800aa0e5da0d67e0cd71bcae5e912a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812047"
---
# Comment publier et annuler la publication d'une application sur l'espace de travail MED-V


Même si une application est installée dans un espace de travail MED-V, vous devrez peut-être également publier l’application avant qu’elle ne soit disponible pour l’utilisateur final. Par défaut, la plupart des applications sont publiées au moment où elles sont installées et des raccourcis sont créés et activés.

Dans certains cas, vous souhaiterez peut-être installer des applications sur l’espace de travail MED-V sans les mettre à la disposition de l’utilisateur final, par exemple, un logiciel d’analyse antivirus. De même, il peut arriver que vous souhaitiez publier une application installée sur l’espace de travail MED-V qui n’est pas disponible pour l’utilisateur final. Par exemple, il se peut que vous deviez publier une application installée si l’installation n’a pas créé automatiquement de raccourci dans le menu **Démarrer** .

**Important**  Si vous publiez une application qui ne prend pas en charge les chemins UNC, nous vous conseillons de mapper l’application sur un lecteur.

 

Vous pouvez publier ou annuler la publication d’applications dans un espace de travail MED-V en effectuant l’une des tâches suivantes:

**Pour publier ou annuler la publication d’une application installée**

1.  Pour publier une application sur un espace de travail MED-V, copiez le raccourci de l’application dans le dossier suivant de l’ordinateur virtuel:

    C:\\Documents et Settings\\All Users\\Start

    Si nécessaire, utilisez une stratégie de groupe ou un système de ESD pour déployer un script qui copie le raccourci de l’application dans le dossier du menu tous les Users\\Start.

2.  Pour annuler la publication d’une application sur un espace de travail MED-V, supprimez le raccourci de l’application dans le dossier suivant de l’ordinateur virtuel:

    C:\\Documents et Settings\\All Users\\Start

    Si nécessaire, utilisez une stratégie de groupe ou un système ESD pour déployer un script qui supprime le raccourci de l’application dans le dossier du menu tous les Users\\Start.

    **Remarques**  Souvent, le raccourci est automatiquement supprimé du menu **Démarrer** de l’ordinateur hôte lorsque vous désinstallez l’application. Toutefois, dans certains cas, par exemple pour un espace de travail MED-V configuré pour tous les utilisateurs d’un ordinateur partagé, vous devrez peut-être supprimer manuellement le raccourci dans le menu **Démarrer** après la désinstallation de l’application. Pour cela, il suffit de cliquer avec le bouton droit sur le raccourci et de sélectionner **supprimer**.

     

Pour vérifier que l’application a été publiée ou annulée, vérifiez sur l’espace de travail MED-V si le raccourci correspondant est disponible ou non.

**Remarques**  Les applications incluses dans Windows XP SP3 et situées dans le dossier du menu Démarrer de l’ordinateur virtuel ne sont pas automatiquement publiées sur l’hôte. Ils sont contrôlés par des paramètres de Registre qui bloquent la publication automatique. Pour plus d’informations, voir liste d’exclusion de l' [application Windows Virtual PC](windows-virtual-pc-application-exclude-list.md).

 

**Pour publier des éléments du panneau de configuration**

1.  Créer un raccourci sur l’ordinateur virtuel où la cible est le nom de l’élément, par exemple, C:\\WINDOWS\\system32\\appwiz.cpl.

    Le raccourci doit être créé ou déplacé vers le dossier «%ALLUSERSPROFILE%\\Start Menu\\» ou l’un de ses sous-dossiers.

    L’élément sera publié sur l’ordinateur hôte à l’emplacement correspondant dans le dossier du menu Démarrer de l’hôte.

2.  Démarrez le raccourci de l’élément dans l’hôte.

**Attention**  Lorsque vous créez le raccourci, ne spécifiez pas% SystemRoot% \\control.exe. Cette application ne sera pas publiée, car elle figure dans les paramètres de Registre qui bloquent la publication automatique.

 

**Comment MED-V gère la publication automatique d’applications**

1.  Lors de la publication d’applications, MED-V copie les raccourcis depuis l’ordinateur virtuel invité vers l’ordinateur hôte en essayant de faire correspondre la hiérarchie de dossiers qui existe dans l’invité. En procédant ainsi, MED-V copie le raccourci de l’invité vers l’hôte en procédant comme suit:

    1.  MED-V essaie de rechercher un dossier sous Démarrer Menu\\Programs sur l’ordinateur hôte portant le même nom que le dossier de l’invité sur lequel réside le raccourci.

    2.  S’il n’y a pas de dossier correspondant, MED-V tente d’accéder à un dossier dans le dossier du menu Démarrer de l’hôte portant le même nom que le dossier de l’invité dans lequel réside le raccourci.

    3.  S’il n’y a aucun dossier correspondant, MED-V copie le raccourci vers le dossier par défaut sur l’hôte, le dossier Menu\\Programs de démarrage.

2.  Exemple de processus de publication d’application:

    1.  Si le raccourci d’une application est publié dans le dossier Start Menu\\Programs\\AppShortcuts de l’invité, l’application MED-V recherche un dossier de démarrage Menu\\Programs\\ AppShortcuts et, le cas échéant, copie le raccourci vers ce dossier.

    2.  Si le dossier est introuvable, l’action MED-V recherche un dossier de démarrage dans l’ordinateur hôte et, le cas échéant, copie le raccourci vers ce dossier.

    3.  Si le dossier n’est pas trouvé, MED-V copie le raccourci dans le dossier de démarrage Menu\\Programs.

**Remarques**  Un dossier doit déjà exister dans le dossier du menu Démarrer de l’ordinateur hôte pour MED-V pour y copier le raccourci. MED-V ne crée pas le dossier s’il n’existe pas déjà.

 

## Rubriques connexes


[Installation et suppression d'une application sur l'espace de travail MED-V](installing-and-removing-an-application-on-the-med-v-workspace.md)

[Gestion des mises à jour de logiciels pour les espaces de travail MED-V](managing-software-updates-for-med-v-workspaces.md)

[Liste d'exclusion d'applications de WindowsVirtualPC](windows-virtual-pc-application-exclude-list.md)

 

 





