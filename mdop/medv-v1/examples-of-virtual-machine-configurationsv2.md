---
title: Exemples de configurations d'ordinateur virtuel
description: Exemples de configurations d'ordinateur virtuel
author: dansimp
ms.assetid: 5937601e-41ab-4ca2-8fa1-3c9154710cd6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b9fc7b1f88b2b30ea149fe73a387826fdbb2a66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810644"
---
# <span data-ttu-id="c42e5-103">Exemples de configurations d'ordinateur virtuel</span><span class="sxs-lookup"><span data-stu-id="c42e5-103">Examples of Virtual Machine Configurations</span></span>


<span data-ttu-id="c42e5-104">Voici quelques exemples de configurations d’ordinateur virtuel typiques: une dans un espace de travail MED-V persistant et une dans un espace de travail revertible MED-V.</span><span class="sxs-lookup"><span data-stu-id="c42e5-104">The following are examples of typical virtual machine configurations: one in a persistent MED-V workspace and one in a revertible MED-V workspace.</span></span>

<span data-ttu-id="c42e5-105">**Remarques**  Ces exemples ne sont pas destinés à une utilisation dans tous les environnements.</span><span class="sxs-lookup"><span data-stu-id="c42e5-105">**Note** These examples are not intended for use in all environments.</span></span> <span data-ttu-id="c42e5-106">Ajustez la configuration en fonction de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="c42e5-106">Adjust the configuration according to your environment.</span></span>

 

**<span data-ttu-id="c42e5-107">Pour configurer une configuration de domaine standard dans un espace de travail MED-V permanent</span><span class="sxs-lookup"><span data-stu-id="c42e5-107">To configure a typical domain setup in a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="c42e5-108">Configurez Sysprep sur l’image de base pour créer un SID unique.</span><span class="sxs-lookup"><span data-stu-id="c42e5-108">Configure Sysprep on the base image to create a unique SID.</span></span> <span data-ttu-id="c42e5-109">Pour plus d’informations, reportez-vous à [la rubrique Création d’une image de PC virtuel pour MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).</span><span class="sxs-lookup"><span data-stu-id="c42e5-109">For more information, see [Creating a Virtual PC Image for MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).</span></span>

2.  <span data-ttu-id="c42e5-110">Dans l’onglet Configuration de l' **ordinateur virtuel** , activez la case à cocher **exécuter la configuration VM** .</span><span class="sxs-lookup"><span data-stu-id="c42e5-110">On the **VM Setup** tab, select the **Run VM Setup** check box.</span></span>

3.  <span data-ttu-id="c42e5-111">Dans la section modèle de nom de l' **ordinateur VM** , configurez le modèle du nom d’image de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c42e5-111">In the **VM Computer Name Pattern** section, configure the pattern for the machine image name.</span></span> <span data-ttu-id="c42e5-112">Pour plus d’informations, reportez-vous [à configuration des propriétés de modèle de nom d’ordinateur VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="c42e5-112">For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

4.  <span data-ttu-id="c42e5-113">Cliquez sur **éditeur de script**, puis, dans la boîte de dialogue Éditeur de script de **configuration VM** , configurez les actions suivantes:</span><span class="sxs-lookup"><span data-stu-id="c42e5-113">Click **Script Editor**, and in the **VM Setup Script Editor** dialog box, configure the following actions:</span></span>

    1.  **<span data-ttu-id="c42e5-114">Renommer ordinateur</span><span class="sxs-lookup"><span data-stu-id="c42e5-114">Rename Computer</span></span>**

    2.  **<span data-ttu-id="c42e5-115">Redémarrer Windows</span><span class="sxs-lookup"><span data-stu-id="c42e5-115">Restart Windows</span></span>**

    3.  **<span data-ttu-id="c42e5-116">Vérifier la connectivité</span><span class="sxs-lookup"><span data-stu-id="c42e5-116">Check Connectivity</span></span>**

    4.  **<span data-ttu-id="c42e5-117">Joindre un domaine</span><span class="sxs-lookup"><span data-stu-id="c42e5-117">Join Domain</span></span>**

    5.  **<span data-ttu-id="c42e5-118">Désactiver la connexion automatique</span><span class="sxs-lookup"><span data-stu-id="c42e5-118">Disable Auto-Logon</span></span>**

    <span data-ttu-id="c42e5-119">Pour plus d’informations, reportez-vous [à la rubrique Configuration d’actions de script](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="c42e5-119">For more information, see [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>

5.  <span data-ttu-id="c42e5-120">Dans le menu **stratégie** , cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="c42e5-120">On the **Policy** menu, click **Commit**.</span></span>

**<span data-ttu-id="c42e5-121">Pour configurer une configuration standard dans un espace de travail revertible</span><span class="sxs-lookup"><span data-stu-id="c42e5-121">To configure a typical setup in a revertible workspace</span></span>**

1.  <span data-ttu-id="c42e5-122">Dans l’onglet Configuration de l’ordinateur **virtuel** , activez la case à cocher **Renommer l’ordinateur virtuel en fonction de votre modèle de nom d’ordinateur** .</span><span class="sxs-lookup"><span data-stu-id="c42e5-122">On the **VM Setup** tab, select the **Rename the VM based on the computer name pattern** check box.</span></span>

2.  <span data-ttu-id="c42e5-123">Dans la section modèle de nom de l' **ordinateur VM** , configurez le modèle du nom d’image de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c42e5-123">In the **VM Computer Name Pattern** section, configure the pattern for the machine image name.</span></span> <span data-ttu-id="c42e5-124">Pour plus d’informations, reportez-vous [à configuration des propriétés de modèle de nom d’ordinateur VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="c42e5-124">For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

3.  <span data-ttu-id="c42e5-125">Dans le menu **stratégie** , cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="c42e5-125">On the **Policy** menu, click **Commit**.</span></span>

## <span data-ttu-id="c42e5-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c42e5-126">Related topics</span></span>


[<span data-ttu-id="c42e5-127">Comment configurer l'installation d'ordinateur virtuel pour un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="c42e5-127">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[<span data-ttu-id="c42e5-128">Comment configurer les propriétés du modèle de nom d'ordinateur virtuel</span><span class="sxs-lookup"><span data-stu-id="c42e5-128">How to Configure VM Computer Name Pattern Properties</span></span>](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

[<span data-ttu-id="c42e5-129">Comment configurer des actions de script</span><span class="sxs-lookup"><span data-stu-id="c42e5-129">How to Set Up Script Actions</span></span>](how-to-set-up-script-actions.md)

 

 





