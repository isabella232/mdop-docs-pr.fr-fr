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
# <span data-ttu-id="41fa4-103">Modification de la configuration d'un client à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="41fa4-103">How to Modify Client Configuration by Using PowerShell</span></span>


<span data-ttu-id="41fa4-104">Utilisez la procédure suivante pour configurer la configuration du client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="41fa4-104">Use the following procedure to configure the App-V 5.1 client configuration.</span></span>

**<span data-ttu-id="41fa4-105">Pour modifier la configuration du client App-V 5,1 à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="41fa4-105">To modify App-V 5.1 client configuration using PowerShell</span></span>**

1.  <span data-ttu-id="41fa4-106">Pour configurer les paramètres du client à l’aide de PowerShell, utilisez la cmdlet **Set-AppvClientConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="41fa4-106">To configure the client settings using PowerShell, use the **Set-AppvClientConfiguration** cmdlet.</span></span> <span data-ttu-id="41fa4-107">Pour plus d’informations sur l’installation de PowerShell, et une liste d’applets de vue, voir [Comment charger les applets de cmdlet PowerShell et obtenir une aide de cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).</span><span class="sxs-lookup"><span data-stu-id="41fa4-107">For more information about installing PowerShell, and a list of cmdlets see, [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).</span></span>

2.  <span data-ttu-id="41fa4-108">Pour modifier la configuration du client, ouvrez une invite de commandes PowerShell et exécutez l’applet **de commande Set-AppvClientConfiguration** avec les paramètres obligatoires suivants.</span><span class="sxs-lookup"><span data-stu-id="41fa4-108">To modify the client configuration, open a PowerShell Command prompt and run the following cmdlet **Set-AppvClientConfiguration** with any required parameters.</span></span> <span data-ttu-id="41fa4-109">Exemple:</span><span class="sxs-lookup"><span data-stu-id="41fa4-109">For example:</span></span>

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    <span data-ttu-id="41fa4-110">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="41fa4-110">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="41fa4-111">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="41fa4-111">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="41fa4-112">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="41fa4-112">Got an App-V issue?</span></span>** <span data-ttu-id="41fa4-113">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="41fa4-113">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="41fa4-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="41fa4-114">Related topics</span></span>


[<span data-ttu-id="41fa4-115">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="41fa4-115">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





