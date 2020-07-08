---
title: Modification de la configuration d'un client à l'aide de PowerShell
description: Modification de la configuration d'un client à l'aide de PowerShell
author: dansimp
ms.assetid: 53ccb2cf-ef81-4310-a853-efcb395f006e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d3173944abfe2c2b3d30aa9654dae81f204a32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805269"
---
# Modification de la configuration d'un client à l'aide de PowerShell


Utilisez la procédure suivante pour configurer la configuration du client App-V 5,0.

**Pour modifier la configuration du client App-V 5,0 à l’aide de PowerShell**

1.  Pour configurer les paramètres du client à l’aide de PowerShell, utilisez la cmdlet **Set-AppvClientConfiguration** .

2.  Pour modifier la configuration du client, ouvrez une invite de commandes PowerShell et exécutez l’applet **de commande Set-AppvClientConfiguration** avec les paramètres obligatoires suivants. Exemple:

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.0](operations-for-app-v-50.md)

 

 





