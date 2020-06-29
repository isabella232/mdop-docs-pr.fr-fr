---
title: Comment publier un package à l’aide de la console de gestion
description: Comment publier un package à l’aide de la console de gestion
author: dansimp
ms.assetid: 7c6930fc-5c89-4519-a901-512dae155fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 832dd95edbb0f4cd6b6ae242a81859141ebcb279
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805238"
---
# Comment publier un package à l’aide de la console de gestion


Utilisez la procédure suivante pour publier un package App-V 5,0. Dès lors que vous publiez un package, les ordinateurs exécutant le client App-V 5,0 peuvent accéder aux applications de ce package et les exécuter.

**Remarques**  La possibilité d’activer seuls les administrateurs pour publier ou annuler la publication de packages (voir ci-dessous) est prise en charge à partir de l’App-V 5,0 SP3.

 

**Pour publier un package App-V 5,0**

1.  Dans la console de gestion App-V 5,0. Cliquez avec le bouton droit sur le nom du package à publier, puis sélectionnez **publier**.

2.  Examinez la colonne **État** pour vérifier que le package a été publié et qu’il est désormais disponible. Si le package est disponible, l’état **publié** est affiché.

    Si le package n’est pas correctement publié, l’état non **publié** s’affiche, ainsi que le texte d’erreur expliquant pourquoi le package n’est pas disponible.

**Pour permettre uniquement aux administrateurs de publier ou de retirer des packages**

1.  Accédez au nœud d’objet de stratégie de groupe suivant:

    **Configuration &gt; ordinateur Stratégies &gt; modèles d’administration &gt; système &gt; de &gt; publication d’application-V**.

2.  Activez le paramètre exiger une stratégie **de groupe publier en tant qu’administrateur** .

    Pour utiliser PowerShell pour définir cet élément, voir [Comment gérer les packages App-V 5,0 exécutés sur un ordinateur autonome à l’aide de PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.0](operations-for-app-v-50.md)

[Comment configurer l’accès aux packages à l’aide de la console de gestion](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

 

 





