---
title: Comment appliquer le fichier de configuration utilisateur à l'aide de PowerShell
description: Comment appliquer le fichier de configuration utilisateur à l'aide de PowerShell
author: dansimp
ms.assetid: f7d7c595-4fdd-4096-b53d-9eead111c339
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95ae5840f5eee04a29431716a956ddec7d0487aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805725"
---
# Comment appliquer le fichier de configuration utilisateur à l'aide de PowerShell


Le fichier de configuration utilisateur dynamique est appliqué lors de la publication d’un package pour un utilisateur spécifique et détermine la façon dont le package s’exécutera.

Utilisez la procédure suivante pour spécifier un fichier de configuration spécifique à l’utilisateur. La procédure suivante est basée sur l’exemple:

**c:\\Packages\\Contoso\\MyApp.appv**

**Pour appliquer un fichier de configuration utilisateur**

1.  Pour ajouter le package à l’ordinateur à l’aide de la console PowerShell, tapez la commande suivante:

    **Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.AppV**.

2.  Utilisez la commande suivante pour publier le package pour l’utilisateur et spécifier le fichier de configuration utilisateur dynamique mis à jour:

    **Publisher-AppVClientPackage $pkg-DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml**

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.0](operations-for-app-v-50.md)

 

 





