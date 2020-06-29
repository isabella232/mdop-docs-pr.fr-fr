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
# <span data-ttu-id="19d8a-103">Comment autoriser uniquement les administrateurs à publier des packages à l'aide d'un système ESD</span><span class="sxs-lookup"><span data-stu-id="19d8a-103">How to Enable Only Administrators to Publish Packages by Using an ESD</span></span>


<span data-ttu-id="19d8a-104">À partir de App-V 5,0 SP3, vous pouvez configurer le client App-V de façon à ce que seuls les administrateurs (pas les utilisateurs finaux) puissent publier ou annuler la publication de packages.</span><span class="sxs-lookup"><span data-stu-id="19d8a-104">Starting in App-V 5.0 SP3, you can configure the App-V client so that only administrators (not end users) can publish or unpublish packages.</span></span> <span data-ttu-id="19d8a-105">Dans les versions antérieures d’App-V, vous ne pouviez pas empêcher les utilisateurs finaux d’effectuer ces tâches.</span><span class="sxs-lookup"><span data-stu-id="19d8a-105">In earlier versions of App-V, you could not prevent end users from performing these tasks.</span></span>

**<span data-ttu-id="19d8a-106">Pour permettre uniquement aux administrateurs de publier ou de retirer des packages</span><span class="sxs-lookup"><span data-stu-id="19d8a-106">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="19d8a-107">Accédez au nœud d’objet de stratégie de groupe suivant:</span><span class="sxs-lookup"><span data-stu-id="19d8a-107">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="19d8a-108">**Configuration &gt; ordinateur Stratégies &gt; modèles d’administration &gt; système &gt; de &gt; publication d’application-V**.</span><span class="sxs-lookup"><span data-stu-id="19d8a-108">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="19d8a-109">Activez le paramètre exiger une stratégie **de groupe publier en tant qu’administrateur** .</span><span class="sxs-lookup"><span data-stu-id="19d8a-109">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="19d8a-110">Pour utiliser PowerShell pour définir cet élément, voir [Comment gérer les packages App-V 5,1 exécutés sur un ordinateur autonome à l’aide de PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span><span class="sxs-lookup"><span data-stu-id="19d8a-110">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="19d8a-111">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="19d8a-111">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="19d8a-112">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="19d8a-112">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="19d8a-113">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="19d8a-113">Got an App-V issue?</span></span>** <span data-ttu-id="19d8a-114">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="19d8a-114">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

 

 





