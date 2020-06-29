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
# <span data-ttu-id="a14fe-103">Comment publier un package à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="a14fe-103">How to Publish a Package by Using the Management Console</span></span>


<span data-ttu-id="a14fe-104">Utilisez la procédure suivante pour publier un package App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a14fe-104">Use the following procedure to publish an App-V 5.0 package.</span></span> <span data-ttu-id="a14fe-105">Dès lors que vous publiez un package, les ordinateurs exécutant le client App-V 5,0 peuvent accéder aux applications de ce package et les exécuter.</span><span class="sxs-lookup"><span data-stu-id="a14fe-105">Once you publish a package, computers that are running the App-V 5.0 client can access and run the applications in that package.</span></span>

<span data-ttu-id="a14fe-106">**Remarques**  La possibilité d’activer seuls les administrateurs pour publier ou annuler la publication de packages (voir ci-dessous) est prise en charge à partir de l’App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="a14fe-106">**Note** The ability to enable only administrators to publish or unpublish packages (described below) is supported starting in App-V 5.0 SP3.</span></span>

 

**<span data-ttu-id="a14fe-107">Pour publier un package App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a14fe-107">To publish an App-V 5.0 package</span></span>**

1.  <span data-ttu-id="a14fe-108">Dans la console de gestion App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a14fe-108">In the App-V 5.0 Management console.</span></span> <span data-ttu-id="a14fe-109">Cliquez avec le bouton droit sur le nom du package à publier, puis sélectionnez **publier**.</span><span class="sxs-lookup"><span data-stu-id="a14fe-109">right-click the name of the package to be published, and select **Publish**.</span></span>

2.  <span data-ttu-id="a14fe-110">Examinez la colonne **État** pour vérifier que le package a été publié et qu’il est désormais disponible.</span><span class="sxs-lookup"><span data-stu-id="a14fe-110">Review the **Status** column to verify that the package has been published and is now available.</span></span> <span data-ttu-id="a14fe-111">Si le package est disponible, l’état **publié** est affiché.</span><span class="sxs-lookup"><span data-stu-id="a14fe-111">If the package is available, the status **published** is displayed.</span></span>

    <span data-ttu-id="a14fe-112">Si le package n’est pas correctement publié, l’état non **publié** s’affiche, ainsi que le texte d’erreur expliquant pourquoi le package n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="a14fe-112">If the package is not published successfully, the status **unpublished** is displayed, along with error text that explains why the package is not available.</span></span>

**<span data-ttu-id="a14fe-113">Pour permettre uniquement aux administrateurs de publier ou de retirer des packages</span><span class="sxs-lookup"><span data-stu-id="a14fe-113">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="a14fe-114">Accédez au nœud d’objet de stratégie de groupe suivant:</span><span class="sxs-lookup"><span data-stu-id="a14fe-114">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="a14fe-115">**Configuration &gt; ordinateur Stratégies &gt; modèles d’administration &gt; système &gt; de &gt; publication d’application-V**.</span><span class="sxs-lookup"><span data-stu-id="a14fe-115">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="a14fe-116">Activez le paramètre exiger une stratégie **de groupe publier en tant qu’administrateur** .</span><span class="sxs-lookup"><span data-stu-id="a14fe-116">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="a14fe-117">Pour utiliser PowerShell pour définir cet élément, voir [Comment gérer les packages App-V 5,0 exécutés sur un ordinateur autonome à l’aide de PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span><span class="sxs-lookup"><span data-stu-id="a14fe-117">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="a14fe-118">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="a14fe-118">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="a14fe-119">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="a14fe-119">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="a14fe-120">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="a14fe-120">Got an App-V issue?</span></span>** <span data-ttu-id="a14fe-121">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="a14fe-121">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a14fe-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a14fe-122">Related topics</span></span>


[<span data-ttu-id="a14fe-123">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="a14fe-123">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="a14fe-124">Comment configurer l’accès aux packages à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="a14fe-124">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

 

 





