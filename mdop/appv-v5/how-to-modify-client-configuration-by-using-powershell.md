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
# <span data-ttu-id="f93fc-103">Modification de la configuration d'un client à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="f93fc-103">How to Modify Client Configuration by Using PowerShell</span></span>


<span data-ttu-id="f93fc-104">Utilisez la procédure suivante pour configurer la configuration du client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f93fc-104">Use the following procedure to configure the App-V 5.0 client configuration.</span></span>

**<span data-ttu-id="f93fc-105">Pour modifier la configuration du client App-V 5,0 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="f93fc-105">To modify App-V 5.0 client configuration using PowerShell</span></span>**

1.  <span data-ttu-id="f93fc-106">Pour configurer les paramètres du client à l’aide de PowerShell, utilisez la cmdlet **Set-AppvClientConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="f93fc-106">To configure the client settings using PowerShell, use the **Set-AppvClientConfiguration** cmdlet.</span></span>

2.  <span data-ttu-id="f93fc-107">Pour modifier la configuration du client, ouvrez une invite de commandes PowerShell et exécutez l’applet **de commande Set-AppvClientConfiguration** avec les paramètres obligatoires suivants.</span><span class="sxs-lookup"><span data-stu-id="f93fc-107">To modify the client configuration, open a PowerShell Command prompt and run the following cmdlet **Set-AppvClientConfiguration** with any required parameters.</span></span> <span data-ttu-id="f93fc-108">Exemple:</span><span class="sxs-lookup"><span data-stu-id="f93fc-108">For example:</span></span>

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    <span data-ttu-id="f93fc-109">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="f93fc-109">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f93fc-110">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="f93fc-110">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f93fc-111">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="f93fc-111">Got an App-V issue?</span></span>** <span data-ttu-id="f93fc-112">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f93fc-112">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f93fc-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f93fc-113">Related topics</span></span>


[<span data-ttu-id="f93fc-114">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="f93fc-114">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





