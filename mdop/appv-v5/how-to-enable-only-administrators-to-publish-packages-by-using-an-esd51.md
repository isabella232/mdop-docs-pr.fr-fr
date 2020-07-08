---
title: Comment autoriser uniquement les administrateurs à publier des packages à l'aide d'un système ESD
description: Comment autoriser uniquement les administrateurs à publier des packages à l'aide d'un système ESD
author: dansimp
ms.assetid: bbc9fda2-fc09-4d72-8d9a-e83d2fcfe234
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22de7f62f540ceff274862c3f16b1f89d9459093
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805467"
---
# Comment autoriser uniquement les administrateurs à publier des packages à l'aide d'un système ESD


À partir de App-V 5,0 SP3, vous pouvez configurer le client App-V de façon à ce que seuls les administrateurs (pas les utilisateurs finaux) puissent publier ou annuler la publication de packages. Dans les versions antérieures d’App-V, vous ne pouviez pas empêcher les utilisateurs finaux d’effectuer ces tâches.

**Pour permettre uniquement aux administrateurs de publier ou de retirer des packages**

1.  Accédez au nœud d’objet de stratégie de groupe suivant:

    **Configuration &gt; ordinateur Stratégies &gt; modèles d’administration &gt; système &gt; de &gt; publication d’application-V**.

2.  Activez le paramètre exiger une stratégie **de groupe publier en tant qu’administrateur** .

    Pour utiliser PowerShell pour définir cet élément, voir [Comment gérer les packages App-V 5,1 exécutés sur un ordinateur autonome à l’aide de PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

 

 





