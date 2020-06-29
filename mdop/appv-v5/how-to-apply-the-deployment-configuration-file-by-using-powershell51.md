---
title: Comment appliquer le fichier de configuration du déploiement à l'aide de PowerShell
description: Comment appliquer le fichier de configuration du déploiement à l'aide de PowerShell
author: dansimp
ms.assetid: 78fe0f15-4a36-41e3-96d6-7d5aa77c1e06
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49beb7ea4afe46c9b0f1640152c786d7c6ba8663
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805730"
---
# Comment appliquer le fichier de configuration du déploiement à l'aide de PowerShell


Le fichier de configuration de déploiement dynamique est appliqué lors de l’ajout ou de la définition d’un package ou d’un ordinateur exécutant le client App-V 5,1 avant la publication du package. Le fichier configure les paramètres par défaut du package pour tous les utilisateurs sur l’ordinateur exécutant le client App-V 5,1. Cette section décrit les étapes utilisées pour utiliser un fichier de configuration de déploiement. La procédure est basée sur l’exemple suivant et suppose que les fichiers de package et de configuration suivants existent sur un ordinateur:

**c:\\Packages\\Contoso\\MyApp.appv**

**c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**

**Pour appliquer le fichier de configuration de déploiement à l’aide de PowerShell**

-   Pour spécifier un nouvel ensemble de configurations par défaut pour tous les utilisateurs qui exécutent le package sur un ordinateur en particulier, à l’aide d’une console PowerShell, tapez les informations suivantes:

    **Add-AppVClientPackage-path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**

    **Remarque**  
    Cette commande capture l’objet obtenu dans $pkg. Si le package est déjà présent sur l’ordinateur, vous pouvez utiliser l’applet de demande **Set-AppVclientPackage** pour appliquer le document de configuration de déploiement:

    **Set-AppVClientPackage-nom MonApp-chemin c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Rubriques connexes


[Opérations d'App-V5.1](operations-for-app-v-51.md)









