---
title: Création d'un espace de travail MED-V
description: Création d'un espace de travail MED-V
author: dansimp
ms.assetid: 9578bb99-8a09-44c1-b88f-538901f16ad3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 189da6b28515f0d234c8a258138a27be7a7375d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810811"
---
# <span data-ttu-id="725e0-103">Création d'un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="725e0-103">Creating a MED-V Workspace</span></span>


<span data-ttu-id="725e0-104">Un espace de travail MED-V est l’environnement de bureau dans lequel les utilisateurs finaux interagissent avec l’ordinateur virtuel fourni par MED-V.</span><span class="sxs-lookup"><span data-stu-id="725e0-104">A MED-V workspace is the desktop environment in which end users interact with the virtual machine provided by MED-V.</span></span> <span data-ttu-id="725e0-105">L’espace de travail MED-V est créé et personnalisé par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="725e0-105">The MED-V workspace is created and customized by the administrator.</span></span> <span data-ttu-id="725e0-106">Il se compose d’une image et de la stratégie, qui définit les règles et les fonctionnalités de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="725e0-106">It consists of an image and the policy, which defines the rules and functionality of the MED-V workspace.</span></span> <span data-ttu-id="725e0-107">Plusieurs espaces de travail MED-V peuvent être créés, chacun personnalisé avec ses propres configurations, paramètres et règles.</span><span class="sxs-lookup"><span data-stu-id="725e0-107">Multiple MED-V workspaces can be created, each customized with its own configuration, settings, and rules.</span></span> <span data-ttu-id="725e0-108">Un utilisateur, un groupe ou plusieurs utilisateurs ou groupes peuvent être associés à chaque espace de travail MED-V, rendant ainsi l’espace de travail MED-V disponible uniquement pour les ordinateurs des utilisateurs ou des groupes associés.</span><span class="sxs-lookup"><span data-stu-id="725e0-108">A user, group, or multiple users or groups can be associated with each MED-V workspace, thereby making the MED-V workspace available only for the associated user's or group's computers.</span></span>

## <span data-ttu-id="725e0-109">Ajouter un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="725e0-109">How to Add a MED-V Workspace</span></span>


**<span data-ttu-id="725e0-110">Pour ajouter un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="725e0-110">To add a MED-V workspace</span></span>**

1.  <span data-ttu-id="725e0-111">Cliquez sur le bouton de gestion des **stratégies** pour ouvrir le module **stratégie** .</span><span class="sxs-lookup"><span data-stu-id="725e0-111">Click the **Policy** management button to open the **Policy** module.</span></span>

    <span data-ttu-id="725e0-112">Le module de **stratégie** se compose du menu **espaces de travail** à gauche et de l’onglet **général**, **ordinateur virtuel**, **déploiement**, **applications**, **Web**, configuration de l' **ordinateur**virtuel, **réseau**et **performance** .</span><span class="sxs-lookup"><span data-stu-id="725e0-112">The **Policy** module consists of the **Workspaces** menu on the left and the **General**, **Virtual Machine**, **Deployment**, **Applications**, **Web**, **VM Setup**, **Network**, and **Performance** tabs.</span></span>

2.  <span data-ttu-id="725e0-113">Dans le menu **stratégie** , sélectionnez **nouvel espace de travail**ou cliquez sur **Ajouter** pour créer un nouvel espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="725e0-113">On the **Policy** menu, select **New Workspace**, or click **Add** to create a new MED-V workspace.</span></span>

3.  <span data-ttu-id="725e0-114">Dans l’onglet **général** , dans le champ **nom** , entrez le nom de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="725e0-114">On the **General** tab, in the **Name** field, enter the name of the MED-V workspace.</span></span>

4.  <span data-ttu-id="725e0-115">Dans le champ **Description** , entrez la description de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="725e0-115">In the **Description** field, enter a description for the MED-V workspace.</span></span>

5.  <span data-ttu-id="725e0-116">Dans le champ **informations de contact du support** technique, entrez les informations de contact du support technique.</span><span class="sxs-lookup"><span data-stu-id="725e0-116">In the **Support contact info** field, enter the contact information for technical support.</span></span>

    <span data-ttu-id="725e0-117">Pour plus d’informations sur la configuration d’un espace de travail MED-V, voir [Configuration des stratégies d’espace de travail MED-v](configuring-med-v-workspace-policies.md).</span><span class="sxs-lookup"><span data-stu-id="725e0-117">For more information about configuring a MED-V workspace, see [Configuring MED-V Workspace Policies](configuring-med-v-workspace-policies.md).</span></span>

## <span data-ttu-id="725e0-118">Comment dupliquer un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="725e0-118">How to Clone a MED-V Workspace</span></span>


<span data-ttu-id="725e0-119">Un espace de travail MED-V peut être cloné de sorte que vous puissiez créer un espace de travail MED-V identique à un espace de travail MED-V existant.</span><span class="sxs-lookup"><span data-stu-id="725e0-119">A MED-V workspace can be cloned so that you can create a MED-V workspace identical to an existing MED-V workspace.</span></span>

**<span data-ttu-id="725e0-120">Pour cloner une espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="725e0-120">To clone a MED-V workspace</span></span>**

1.  <span data-ttu-id="725e0-121">Cliquez sur l’espace de travail MED-V pour le cloner.</span><span class="sxs-lookup"><span data-stu-id="725e0-121">Click the MED-V workspace to clone.</span></span>

2.  <span data-ttu-id="725e0-122">Dans le menu **stratégie** , sélectionnez **cloner l’espace de travail**.</span><span class="sxs-lookup"><span data-stu-id="725e0-122">On the **Policy** menu, select **Clone Workspace**.</span></span>

    <span data-ttu-id="725e0-123">Un nouvel espace de travail MED-V est créé avec le nom &lt; de l’espace de travail MED-v original &gt; -2.</span><span class="sxs-lookup"><span data-stu-id="725e0-123">A new MED-V workspace is created with the name &lt;Original MED-V workspace name&gt; - 2.</span></span>

## <span data-ttu-id="725e0-124">Comment supprimer un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="725e0-124">How to Delete a MED-V Workspace</span></span>


**<span data-ttu-id="725e0-125">Pour supprimer un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="725e0-125">To delete a MED-V workspace</span></span>**

-   <span data-ttu-id="725e0-126">Dans le module **stratégie** , lorsque le volet de l’espace de travail est activé, cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="725e0-126">In the **Policy** module, while the workspace pane is in focus, click **Remove**.</span></span>

## <span data-ttu-id="725e0-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="725e0-127">Related topics</span></span>


[<span data-ttu-id="725e0-128">Utilisation de l'interface utilisateur de la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="725e0-128">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

 

 





