---
title: Procédure pour modifier un fichier OSD
description: Procédure pour modifier un fichier OSD
author: dansimp
ms.assetid: 0d126ba7-72fb-42ce-982e-90ed01a852c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4a0ff4a8efe1fa177f6847c344add94bca3648cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807106"
---
# <span data-ttu-id="58f33-103">Procédure pour modifier un fichier OSD</span><span class="sxs-lookup"><span data-stu-id="58f33-103">How to Edit an OSD File</span></span>


<span data-ttu-id="58f33-104">Utilisez les procédures suivantes pour modifier un fichier d’OSD (Open Software Descriptor) de package d’application séquencé en ajoutant ou en supprimant un élément ou un attribut.</span><span class="sxs-lookup"><span data-stu-id="58f33-104">Use the following procedures to modify a sequenced application package's Open Software Descriptor (OSD) file by adding or deleting an element or an attribute.</span></span>

<span data-ttu-id="58f33-105">**Remarques**  Certains éléments n’ayant pas d’attribut, il n’est pas possible d’ajouter un attribut à chaque élément.</span><span class="sxs-lookup"><span data-stu-id="58f33-105">**Note** Some elements do not have an attribute, so it is not possible to add an attribute to every element.</span></span>

 

<span data-ttu-id="58f33-106">**Important**  Si vous utilisez l’éditeur OSD pour modifier le nom de fichier. SFT, l’attribut HREF de l’élément code base du fichier OSD, vous devez utiliser la commande **Enregistrer sous** pour enregistrer la modification apportée aux fichiers de projet.</span><span class="sxs-lookup"><span data-stu-id="58f33-106">**Important** If you use the OSD editor to change the .sft file name, the HREF attribute of the CODEBASE element in the OSD file, you must use the **Save As** command to save the change to the project files.</span></span>

 

**<span data-ttu-id="58f33-107">Pour ajouter un élément</span><span class="sxs-lookup"><span data-stu-id="58f33-107">To add an element</span></span>**

1.  <span data-ttu-id="58f33-108">Cliquez sur l’onglet **fichier OSD** .</span><span class="sxs-lookup"><span data-stu-id="58f33-108">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="58f33-109">Dans le volet de navigation, sélectionnez le fichier OSD de package d’application séquencé que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="58f33-109">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="58f33-110">Dans le volet de navigation, cliquez avec le bouton droit sur l’élément que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="58f33-110">In the navigation pane, right-click the element that you want to modify.</span></span> <span data-ttu-id="58f33-111">Dans le menu, sélectionnez **élément** , puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="58f33-111">On the menu, select **Element** and select **Add**.</span></span>

4.  <span data-ttu-id="58f33-112">Dans le menu, sélectionnez l’élément que vous voulez ajouter (par exemple, **code base**).</span><span class="sxs-lookup"><span data-stu-id="58f33-112">From the menu, select the element you want to add—for example, **Codebase**.</span></span>

5.  <span data-ttu-id="58f33-113">Dans le menu **fichier** , sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="58f33-113">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="58f33-114">Pour supprimer un élément</span><span class="sxs-lookup"><span data-stu-id="58f33-114">To delete an element</span></span>**

1.  <span data-ttu-id="58f33-115">Cliquez sur l’onglet **fichier OSD** .</span><span class="sxs-lookup"><span data-stu-id="58f33-115">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="58f33-116">Dans le volet de navigation, sélectionnez le fichier OSD de package d’application séquencé que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="58f33-116">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="58f33-117">Dans le volet de navigation, cliquez avec le bouton droit sur l’élément que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="58f33-117">In the navigation pane, right-click the element that you want to delete.</span></span> <span data-ttu-id="58f33-118">Dans le menu, sélectionnez **élément** , puis choisissez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="58f33-118">On the menu, select **Element** and select **Delete**.</span></span>

4.  <span data-ttu-id="58f33-119">Dans le menu **fichier** , sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="58f33-119">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="58f33-120">Pour ajouter un attribut</span><span class="sxs-lookup"><span data-stu-id="58f33-120">To add an attribute</span></span>**

1.  <span data-ttu-id="58f33-121">Cliquez sur l’onglet **fichier OSD** .</span><span class="sxs-lookup"><span data-stu-id="58f33-121">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="58f33-122">Dans le volet de navigation, sélectionnez le fichier OSD de package d’application séquencé que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="58f33-122">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="58f33-123">Dans le volet gauche, cliquez avec le bouton droit sur l’élément auquel vous voulez ajouter un attribut.</span><span class="sxs-lookup"><span data-stu-id="58f33-123">In the left pane, right-click the element to which you want to add an attribute.</span></span> <span data-ttu-id="58f33-124">Dans le menu, sélectionnez **attribut** , puis sélectionnez **Ajouter**, puis choisissez l’un des attributs disponibles dans la liste.</span><span class="sxs-lookup"><span data-stu-id="58f33-124">On the menu, select **Attribute** and select **Add**, choosing from the listed available attributes.</span></span>

4.  <span data-ttu-id="58f33-125">Dans le menu **fichier** , sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="58f33-125">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="58f33-126">Pour supprimer un attribut</span><span class="sxs-lookup"><span data-stu-id="58f33-126">To delete an attribute</span></span>**

1.  <span data-ttu-id="58f33-127">Cliquez sur l’onglet **fichier OSD** .</span><span class="sxs-lookup"><span data-stu-id="58f33-127">Click the **OSD File** tab.</span></span>

2.  <span data-ttu-id="58f33-128">Dans le volet de navigation, sélectionnez le fichier OSD de package d’application séquencé que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="58f33-128">In the navigation pane, select the sequenced application package's OSD file you want to modify.</span></span>

3.  <span data-ttu-id="58f33-129">Dans le volet de navigation, cliquez avec le bouton droit sur l’élément à partir duquel vous voulez supprimer un attribut.</span><span class="sxs-lookup"><span data-stu-id="58f33-129">In the navigation pane, right-click the element from which you want to delete an attribute.</span></span> <span data-ttu-id="58f33-130">Dans le menu, sélectionnez **attribut** , puis **supprimer**et sélectionnez l’attribut que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="58f33-130">On the menu, select **Attribute** and then select **Delete**, choosing the attribute you wish to delete.</span></span>

4.  <span data-ttu-id="58f33-131">Dans le menu **fichier** , sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="58f33-131">From the **File** menu, select **Save**.</span></span>

## <span data-ttu-id="58f33-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="58f33-132">Related topics</span></span>


[<span data-ttu-id="58f33-133">À propos de l'onglet OSD</span><span class="sxs-lookup"><span data-stu-id="58f33-133">About the OSD Tab</span></span>](about-the-osd-tab.md)

[<span data-ttu-id="58f33-134">Procédure pour modifier un fichier OSD à l'aide d'un éditeur de texte</span><span class="sxs-lookup"><span data-stu-id="58f33-134">How to Edit an OSD File Using a Text Editor</span></span>](how-to-edit-an-osd-file-using-a-text-editor.md)

[<span data-ttu-id="58f33-135">Éléments du fichier OSD</span><span class="sxs-lookup"><span data-stu-id="58f33-135">OSD File Elements</span></span>](osd-file-elements.md)

[<span data-ttu-id="58f33-136">Console Sequencer</span><span class="sxs-lookup"><span data-stu-id="58f33-136">Sequencer Console</span></span>](sequencer-console.md)

 

 





