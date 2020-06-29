---
title: Comment publier un package à l’aide de la console de gestion
description: Comment publier un package à l’aide de la console de gestion
author: dansimp
ms.assetid: e34d2bcf-15ac-4a75-9dc8-79380b36a25f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b0783a05f658da5e93603e26dc7e9581d26b81f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805226"
---
# <span data-ttu-id="8d200-103">Comment publier un package à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="8d200-103">How to Publish a Package by Using the Management Console</span></span>


<span data-ttu-id="8d200-104">Utilisez la procédure suivante pour publier un package App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8d200-104">Use the following procedure to publish an App-V 5.1 package.</span></span> <span data-ttu-id="8d200-105">Dès lors que vous publiez un package, les ordinateurs exécutant le client App-V 5,1 peuvent accéder aux applications de ce package et les exécuter.</span><span class="sxs-lookup"><span data-stu-id="8d200-105">Once you publish a package, computers that are running the App-V 5.1 client can access and run the applications in that package.</span></span>

<span data-ttu-id="8d200-106">**Remarques**  La possibilité d’activer seuls les administrateurs pour publier ou annuler la publication de packages (voir ci-dessous) est prise en charge à partir de l’App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="8d200-106">**Note** The ability to enable only administrators to publish or unpublish packages (described below) is supported starting in App-V 5.0 SP3.</span></span>

 

**<span data-ttu-id="8d200-107">Pour publier un package App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="8d200-107">To publish an App-V 5.1 package</span></span>**

1.  <span data-ttu-id="8d200-108">Dans la console de gestion App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8d200-108">In the App-V 5.1 Management console.</span></span> <span data-ttu-id="8d200-109">Cliquez ou cliquez avec le bouton droit sur le nom du package à publier.</span><span class="sxs-lookup"><span data-stu-id="8d200-109">Click or right-click the name of the package to be published.</span></span> <span data-ttu-id="8d200-110">Sélectionnez **publier**.</span><span class="sxs-lookup"><span data-stu-id="8d200-110">Select **Publish**.</span></span>

2.  <span data-ttu-id="8d200-111">Examinez la colonne **État** pour vérifier que le package a été publié et qu’il est désormais disponible.</span><span class="sxs-lookup"><span data-stu-id="8d200-111">Review the **Status** column to verify that the package has been published and is now available.</span></span> <span data-ttu-id="8d200-112">Si le package est disponible, l’état **publié** est affiché.</span><span class="sxs-lookup"><span data-stu-id="8d200-112">If the package is available, the status **published** is displayed.</span></span>

    <span data-ttu-id="8d200-113">Si le package n’est pas correctement publié, l’état non **publié** s’affiche, ainsi que le texte d’erreur expliquant pourquoi le package n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="8d200-113">If the package is not published successfully, the status **unpublished** is displayed, along with error text that explains why the package is not available.</span></span>

**<span data-ttu-id="8d200-114">Pour permettre uniquement aux administrateurs de publier ou de retirer des packages</span><span class="sxs-lookup"><span data-stu-id="8d200-114">To enable only administrators to publish or unpublish packages</span></span>**

1.  <span data-ttu-id="8d200-115">Accédez au nœud d’objet de stratégie de groupe suivant:</span><span class="sxs-lookup"><span data-stu-id="8d200-115">Navigate to the following Group Policy Object node:</span></span>

    <span data-ttu-id="8d200-116">**Configuration &gt; ordinateur Stratégies &gt; modèles d’administration &gt; système &gt; de &gt; publication d’application-V**.</span><span class="sxs-lookup"><span data-stu-id="8d200-116">**Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing**.</span></span>

2.  <span data-ttu-id="8d200-117">Activez le paramètre exiger une stratégie **de groupe publier en tant qu’administrateur** .</span><span class="sxs-lookup"><span data-stu-id="8d200-117">Enable the **Require publish as administrator** Group Policy setting.</span></span>

    <span data-ttu-id="8d200-118">Pour utiliser PowerShell pour définir cet élément, voir [Comment gérer les packages App-V 5,1 exécutés sur un ordinateur autonome à l’aide de PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span><span class="sxs-lookup"><span data-stu-id="8d200-118">To alternatively use PowerShell to set this item, see [How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).</span></span>

    <span data-ttu-id="8d200-119">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="8d200-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="8d200-120">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="8d200-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="8d200-121">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="8d200-121">Got an App-V issue?</span></span>** <span data-ttu-id="8d200-122">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="8d200-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="8d200-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8d200-123">Related topics</span></span>


[<span data-ttu-id="8d200-124">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="8d200-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="8d200-125">Comment configurer l’accès aux packages à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="8d200-125">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

 

 





