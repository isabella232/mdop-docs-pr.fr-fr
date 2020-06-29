---
title: Comment personnaliser les extensions d’applications virtuelles d’un groupe AD spécifique à l’aide de la console de gestion
description: Comment personnaliser les extensions d’applications virtuelles d’un groupe AD spécifique à l’aide de la console de gestion
author: dansimp
ms.assetid: 4f249ee3-cc2d-4b1e-afe5-d1cbf9cabd88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57ce4b82cc552e0a4adc2272f849111d8da0be71
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805587"
---
# <span data-ttu-id="cc81e-103">Comment personnaliser les extensions d’applications virtuelles d’un groupe AD spécifique à l’aide de la console de gestion</span><span class="sxs-lookup"><span data-stu-id="cc81e-103">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>


<span data-ttu-id="cc81e-104">Utilisez la procédure suivante pour personnaliser les extensions d’application virtuelles pour un groupe Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="cc81e-104">Use the following procedure to customize the virtual application extensions for an Active Directory (AD) group.</span></span>

**<span data-ttu-id="cc81e-105">Pour personnaliser les extensions d’applications virtuelles pour un groupe d’annonces</span><span class="sxs-lookup"><span data-stu-id="cc81e-105">To customize virtual applications extensions for an AD group</span></span>**

1.  <span data-ttu-id="cc81e-106">Pour afficher le package que vous voulez configurer, ouvrez la console de gestion App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="cc81e-106">To view the package that you want to configure, open the App-V 5.0 Management Console.</span></span> <span data-ttu-id="cc81e-107">Pour afficher la configuration affectée à un groupe d’utilisateurs donné, sélectionnez le package, cliquez avec le bouton droit sur le nom du package, puis sélectionnez **modifier l’accès Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="cc81e-107">To view the configuration that is assigned to a given user group, select the package, and right-click the package name and select **Edit active directory access**.</span></span> <span data-ttu-id="cc81e-108">Vous pouvez également sélectionner le package et cliquer sur **modifier** dans le volet accès à la **publicité** .</span><span class="sxs-lookup"><span data-stu-id="cc81e-108">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="cc81e-109">Pour personnaliser un groupe d’annonces, vous pouvez le trouver dans la liste des **entités publicitaires ayant accès**.</span><span class="sxs-lookup"><span data-stu-id="cc81e-109">To customize an AD group, you can find the group from the list of **AD Entities with Access**.</span></span> <span data-ttu-id="cc81e-110">Ensuite, à l’aide de la zone de liste déroulante du volet **configuration affectée** , sélectionnez **personnalisé**, puis cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="cc81e-110">Then, using the drop-down box in the **Assigned Configuration** pane, select **Custom**, and then click **EDIT**.</span></span>

3.  <span data-ttu-id="cc81e-111">Pour désactiver toutes les extensions pour une application donnée, décochez la case **activer**.</span><span class="sxs-lookup"><span data-stu-id="cc81e-111">To disable all extensions for a given application, clear **ENABLE**.</span></span>

    <span data-ttu-id="cc81e-112">Pour ajouter un nouveau raccourci pour l’application sélectionnée, cliquez avec le bouton droit sur l’application dans le volet **raccourcis** , puis sélectionnez **Ajouter un nouveau raccourci**.</span><span class="sxs-lookup"><span data-stu-id="cc81e-112">To add a new shortcut for the selected application, right-click the application in the **SHORTCUTS** pane, and select **Add new shortcut**.</span></span> <span data-ttu-id="cc81e-113">Pour supprimer un raccourci, cliquez avec le bouton droit sur l’application dans le volet **raccourcis** , puis sélectionnez **supprimer le raccourci**.</span><span class="sxs-lookup"><span data-stu-id="cc81e-113">To remove a shortcut, right-click the application in the **SHORTCUTS** pane, and select **Remove Shortcut**.</span></span> <span data-ttu-id="cc81e-114">Pour modifier un raccourci existant, cliquez avec le bouton droit sur l’application, puis sélectionnez **modifier le raccourci**.</span><span class="sxs-lookup"><span data-stu-id="cc81e-114">To edit an existing shortcut, right-click the application, and select **Edit Shortcut**.</span></span>

4.  <span data-ttu-id="cc81e-115">Pour afficher d’autres extensions d’application, cliquez sur **avancé**, puis cliquez sur **Exporter la configuration**.</span><span class="sxs-lookup"><span data-stu-id="cc81e-115">To view any other application extensions, click **Advanced**, and click **Export Configuration**.</span></span> <span data-ttu-id="cc81e-116">Tapez un nom de fichier, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cc81e-116">Type in a filename and click **Save**.</span></span> <span data-ttu-id="cc81e-117">Vous pouvez afficher toutes les extensions d’application associées au package à l’aide du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="cc81e-117">You can view all application extensions that are associated with the package using the configuration file.</span></span>

5.  <span data-ttu-id="cc81e-118">Pour modifier d’autres extensions d’application, vous pouvez modifier le fichier de configuration et cliquer sur **Importer et remplacer cette configuration**.</span><span class="sxs-lookup"><span data-stu-id="cc81e-118">To edit additional application extensions, modify the configuration file and click **Import and Overwrite this Configuration**.</span></span> <span data-ttu-id="cc81e-119">Sélectionnez le fichier modifié, puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="cc81e-119">Select the modified file and click **Open**.</span></span> <span data-ttu-id="cc81e-120">Dans la boîte de dialogue, cliquez sur **remplacer** pour terminer le processus.</span><span class="sxs-lookup"><span data-stu-id="cc81e-120">In the dialog, click **Overwrite** to complete the process.</span></span>

    <span data-ttu-id="cc81e-121">Vous **avez une suggestion pour App-V**?</span><span class="sxs-lookup"><span data-stu-id="cc81e-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="cc81e-122">Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)</span><span class="sxs-lookup"><span data-stu-id="cc81e-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="cc81e-123">Vous avez un problème lié à l’application-V?</span><span class="sxs-lookup"><span data-stu-id="cc81e-123">Got an App-V issue?</span></span>** <span data-ttu-id="cc81e-124">Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="cc81e-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="cc81e-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cc81e-125">Related topics</span></span>


[<span data-ttu-id="cc81e-126">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="cc81e-126">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





