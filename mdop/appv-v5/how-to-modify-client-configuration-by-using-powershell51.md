---
title: Modification de la configuration d'un client à l'aide de PowerShell
description: Modification de la configuration d'un client à l'aide de PowerShell
author: dansimp
ms.assetid: c3a59592-bb0d-43b6-8f4e-44f3a2d5b7ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 368a0d12c12e10a623afad3f9040ae01cee6cb38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805257"
---
# Modification de la configuration d'un client à l'aide de PowerShell


Utilisez la procédure suivante pour configurer la configuration du client App-V 5,1.

**Pour modifier la configuration du client App-V 5,1 à l’aide de PowerShell**

1.  Pour configurer les paramètres du client à l’aide de PowerShell, utilisez la cmdlet **Set-AppvClientConfiguration** . Pour plus d’informations sur l’installation de PowerShell, et une liste d’applets de vue, voir [Comment charger les applets de cmdlet PowerShell et obtenir une aide de cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).

2.  Pour modifier la configuration du client, ouvrez une invite de commandes PowerShell et exécutez l’applet **de commande Set-AppvClientConfiguration** avec les paramètres obligatoires suivants. Exemple:

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.1](operations-for-app-v-51.md)

 

 





