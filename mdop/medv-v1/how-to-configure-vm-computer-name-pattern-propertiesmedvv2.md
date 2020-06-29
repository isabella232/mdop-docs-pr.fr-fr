---
title: Comment configurer les propriétés du modèle de nom d'ordinateur virtuel
description: Comment configurer les propriétés du modèle de nom d'ordinateur virtuel
author: dansimp
ms.assetid: ddf79ace-8cc3-4ee6-be5a-5940b4df5c36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa171712b6624b73fb5e0756aaf56277baa4c8cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812138"
---
# <span data-ttu-id="24cf5-103">Comment configurer les propriétés du modèle de nom d'ordinateur virtuel</span><span class="sxs-lookup"><span data-stu-id="24cf5-103">How to Configure VM Computer Name Pattern Properties</span></span>


<span data-ttu-id="24cf5-104">Un modèle de nom d’ordinateur de machine virtuelle peut être attribué à la fois pour revertible et pour les espaces de travail MED-V persistants.</span><span class="sxs-lookup"><span data-stu-id="24cf5-104">A virtual machine computer name pattern can be assigned both for revertible and for persistent MED-V workspaces.</span></span>

-   <span data-ttu-id="24cf5-105">Revertible: les administrateurs peuvent affecter un nom unique à chaque instance d’espace de travail MED-V pour faire la distinction entre plusieurs ordinateurs utilisant le même espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="24cf5-105">Revertible—Administrators can assign a unique name to each revertible MED-V workspace instance to differentiate between multiple computers using the same MED-V workspace.</span></span>

-   <span data-ttu-id="24cf5-106">Permanent: dans un espace de travail MED-V persistant, les administrateurs peuvent configurer un ordinateur à renommer au cours d’un script d’installation.</span><span class="sxs-lookup"><span data-stu-id="24cf5-106">Persistent—In a persistent MED-V workspace, administrators can set a computer to be renamed during a setup script.</span></span>

## <span data-ttu-id="24cf5-107">Comment affecter un modèle de nom d’ordinateur virtuel à un espace de travail Revertible MED-V</span><span class="sxs-lookup"><span data-stu-id="24cf5-107">How to Assign a Virtual Machine Computer Name Pattern to a Revertible MED-V Workspace</span></span>


**<span data-ttu-id="24cf5-108">Pour affecter un modèle de nom d’ordinateur virtuel à un espace de travail revertible MED-V</span><span class="sxs-lookup"><span data-stu-id="24cf5-108">To assign a virtual machine computer name pattern to a revertible MED-V workspace</span></span>**

1.  <span data-ttu-id="24cf5-109">Cliquez sur l’espace de travail revertible MED-V pour le configurer.</span><span class="sxs-lookup"><span data-stu-id="24cf5-109">Click the revertible MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="24cf5-110">Dans la section **installation de REVERTIBLE VM** , activez la case à cocher **Renommer l’ordinateur virtuel en fonction de votre modèle de nom d’ordinateur** .</span><span class="sxs-lookup"><span data-stu-id="24cf5-110">In the **Revertible VM Setup** section, select the **Rename the VM based on the computer name pattern** check box.</span></span>

3.  <span data-ttu-id="24cf5-111">Dans la section modèle de nom de l' **ordinateur VM** , entrez le modèle à utiliser pour nommer les images d’machines virtuelles, à l’aide des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="24cf5-111">In the **VM Computer Name Pattern** section, enter the pattern to use for naming virtual machine images, using the following options:</span></span>

    -   <span data-ttu-id="24cf5-112">**Constante**: entrez du texte libre qui sera constant sur tous les ordinateurs qui utilisent l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="24cf5-112">**Constant**—Enter free text that will be constant on all computers using the MED-V workspace.</span></span>

    -   <span data-ttu-id="24cf5-113">**Variable**: entrez une variable, en cliquant sur **Insérer une variable**, puis effectuez l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="24cf5-113">**Variable**—Enter a variable, by clicking **Insert Variable**, and select from one of the following:</span></span>

        -   **<span data-ttu-id="24cf5-114">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="24cf5-114">User name</span></span>**

        -   **<span data-ttu-id="24cf5-115">Nom de domaine</span><span class="sxs-lookup"><span data-stu-id="24cf5-115">Domain name</span></span>**

        -   **<span data-ttu-id="24cf5-116">Nom de l'hôte</span><span class="sxs-lookup"><span data-stu-id="24cf5-116">Host name</span></span>**

        -   **<span data-ttu-id="24cf5-117">Nom de l’espace de travail</span><span class="sxs-lookup"><span data-stu-id="24cf5-117">Workspace name</span></span>**

        -   **<span data-ttu-id="24cf5-118">Nom de l’ordinateur virtuel</span><span class="sxs-lookup"><span data-stu-id="24cf5-118">Virtual machine name</span></span>**

        <span data-ttu-id="24cf5-119">La variable sélectionnée sera spécifique à l’ordinateur qui utilise l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="24cf5-119">The variable selected will be specific to the computer using the MED-V workspace.</span></span> <span data-ttu-id="24cf5-120">Par exemple, si vous sélectionnez **Domain Name (nom de domaine** ), le nom unique de chaque ordinateur inclut le nom de domaine de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="24cf5-120">For example, if **Domain name** is selected, the unique name for each computer will include the computer's domain name.</span></span>

    -   <span data-ttu-id="24cf5-121">**Caractères aléatoires**: entrez «\ #» pour chaque caractère aléatoire à inclure dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="24cf5-121">**Random characters**—Enter “\#” for each random character to include in the pattern.</span></span> <span data-ttu-id="24cf5-122">Chaque ordinateur qui utilise l’espace de travail MED-V dispose d’un suffixe de longueur spécifiée, qui est généré de manière aléatoire.</span><span class="sxs-lookup"><span data-stu-id="24cf5-122">Each computer using the MED-V workspace will have a suffix of the length specified, which is generated randomly.</span></span>

    **<span data-ttu-id="24cf5-123">Remarque</span><span class="sxs-lookup"><span data-stu-id="24cf5-123">Note</span></span>**  
    <span data-ttu-id="24cf5-124">Le nom de l’ordinateur est limité à 15 caractères.</span><span class="sxs-lookup"><span data-stu-id="24cf5-124">The computer name has a limit of 15 characters.</span></span> <span data-ttu-id="24cf5-125">Si le modèle dépasse la limite, il est tronqué.</span><span class="sxs-lookup"><span data-stu-id="24cf5-125">If the pattern exceeds the limit, it will be truncated.</span></span>



4.  <span data-ttu-id="24cf5-126">Dans le menu **stratégie** , cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="24cf5-126">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="24cf5-127">Remarque</span><span class="sxs-lookup"><span data-stu-id="24cf5-127">Note</span></span>**  
    <span data-ttu-id="24cf5-128">Un modèle de nom d’ordinateur revertible VM peut être attribué uniquement lors de l’attribution d’un **nom à l’ordinateur virtuel en fonction des modèles de nom** de l’ordinateur (dans la section Configuration de l’ordinateur **virtuel revertible** ) est coché.</span><span class="sxs-lookup"><span data-stu-id="24cf5-128">A revertible VM computer name pattern can be assigned only when **Rename the VM based on the computer name patterns** (in the **Revertible VM Setup** section) is checked.</span></span>



~~~
**Note**  
A unique computer name can be assigned only if it is configured prior to MED-V workspace setup. Changing the name will not affect MED-V workspaces that were already set up.
~~~



## <span data-ttu-id="24cf5-129">Comment affecter un modèle de nom d’ordinateur virtuel à un espace de travail MED-V permanent</span><span class="sxs-lookup"><span data-stu-id="24cf5-129">How to Assign a Virtual Machine Computer Name Pattern to a Persistent MED-V Workspace</span></span>


**<span data-ttu-id="24cf5-130">Pour affecter un modèle de nom d’ordinateur virtuel à un espace de travail MED-V permanent</span><span class="sxs-lookup"><span data-stu-id="24cf5-130">To assign a virtual machine computer name pattern to a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="24cf5-131">Cliquez sur l’espace de travail MED-V permanent à configurer.</span><span class="sxs-lookup"><span data-stu-id="24cf5-131">Click the persistent MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="24cf5-132">Dans la section **installation d’un VM persistante** , cliquez sur **éditeur de script**.</span><span class="sxs-lookup"><span data-stu-id="24cf5-132">In the **Persistent VM Setup** section, click **Script Editor**.</span></span>

3.  <span data-ttu-id="24cf5-133">Dans la boîte de dialogue **actions de script** , cliquez sur **Ajouter**, puis dans le sous-menu, cliquez sur **Renommer un ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="24cf5-133">In the **Script Actions** dialog box, click **Add**, and on the submenu, click **Rename Computer**.</span></span>

4.  <span data-ttu-id="24cf5-134">Cliquez sur **OK** pour fermer la boîte de dialogue **actions de script** .</span><span class="sxs-lookup"><span data-stu-id="24cf5-134">Click **OK** to close the **Script Actions** dialog box.</span></span>

5.  <span data-ttu-id="24cf5-135">Dans l’onglet Configuration de l’ordinateur **virtuel** , dans la section modèle de nom de l' **ordinateur VM** , entrez le modèle à utiliser pour renommer l’ordinateur, en procédant comme suit:</span><span class="sxs-lookup"><span data-stu-id="24cf5-135">On the **VM Setup** tab, in the **VM Computer Name Pattern** section, enter the pattern to use for renaming the computer, using the following:</span></span>

    -   <span data-ttu-id="24cf5-136">**Constante**: entrez le texte libre qui sera inclus dans le nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="24cf5-136">**Constant**— Enter free text that will be included in the computer name.</span></span>

    -   <span data-ttu-id="24cf5-137">**Variable**: entrez une variable, en cliquant sur **Insérer une variable**, puis effectuez l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="24cf5-137">**Variable**—Enter a variable, by clicking **Insert Variable**, and select from one of the following:</span></span>

        -   **<span data-ttu-id="24cf5-138">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="24cf5-138">User name</span></span>**

        -   **<span data-ttu-id="24cf5-139">Nom de domaine</span><span class="sxs-lookup"><span data-stu-id="24cf5-139">Domain name</span></span>**

        -   **<span data-ttu-id="24cf5-140">Nom de l'hôte</span><span class="sxs-lookup"><span data-stu-id="24cf5-140">Host name</span></span>**

        -   **<span data-ttu-id="24cf5-141">Nom de l’espace de travail</span><span class="sxs-lookup"><span data-stu-id="24cf5-141">Workspace name</span></span>**

        -   **<span data-ttu-id="24cf5-142">Nom de l’ordinateur virtuel</span><span class="sxs-lookup"><span data-stu-id="24cf5-142">Virtual machine name</span></span>**

        <span data-ttu-id="24cf5-143">Les variables sélectionnées seront spécifiques de l’ordinateur renommé.</span><span class="sxs-lookup"><span data-stu-id="24cf5-143">The variable selected will be specific to the computer that is being renamed.</span></span> <span data-ttu-id="24cf5-144">Par exemple, si le **nom de domaine** est sélectionné, le nom de l’ordinateur inclut le nom de domaine de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="24cf5-144">For example, if **Domain name** is selected, the computer name will include the computer's domain name.</span></span>

    -   <span data-ttu-id="24cf5-145">**Caractères aléatoires**: entrez «\ #» pour chaque caractère aléatoire à inclure dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="24cf5-145">**Random characters**— Enter “\#” for each random character to include in the pattern.</span></span> <span data-ttu-id="24cf5-146">L’ordinateur aura un suffixe de longueur spécifiée, qui est généré de manière aléatoire.</span><span class="sxs-lookup"><span data-stu-id="24cf5-146">The computer will have a suffix of the length specified, which is generated randomly.</span></span>

    **<span data-ttu-id="24cf5-147">Remarque</span><span class="sxs-lookup"><span data-stu-id="24cf5-147">Note</span></span>**  
    <span data-ttu-id="24cf5-148">Le nom de l’ordinateur est limité à 15 caractères.</span><span class="sxs-lookup"><span data-stu-id="24cf5-148">The computer name has a limit of 15 characters.</span></span> <span data-ttu-id="24cf5-149">Si le modèle dépasse la limite, il est tronqué.</span><span class="sxs-lookup"><span data-stu-id="24cf5-149">If the pattern exceeds the limit, it will be truncated.</span></span>



6.  <span data-ttu-id="24cf5-150">Dans le menu **stratégie** , cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="24cf5-150">On the **Policy** menu, select **Commit**.</span></span>

    **<span data-ttu-id="24cf5-151">Remarque</span><span class="sxs-lookup"><span data-stu-id="24cf5-151">Note</span></span>**  
    <span data-ttu-id="24cf5-152">L’ordinateur est renommé uniquement s’il est défini comme action dans la boîte de dialogue **actions de script** .</span><span class="sxs-lookup"><span data-stu-id="24cf5-152">The computer will be renamed only if it is set as an action in the **Script Actions** dialog box.</span></span> <span data-ttu-id="24cf5-153">Pour plus d’informations, reportez-vous [à la rubrique Configuration d’actions de script](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="24cf5-153">For detailed information, see [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>



## <span data-ttu-id="24cf5-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24cf5-154">Related topics</span></span>


[<span data-ttu-id="24cf5-155">Utilisation de l'interface utilisateur de la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="24cf5-155">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="24cf5-156">Création d'un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="24cf5-156">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="24cf5-157">Comment configurer des actions de script</span><span class="sxs-lookup"><span data-stu-id="24cf5-157">How to Set Up Script Actions</span></span>](how-to-set-up-script-actions.md)

[<span data-ttu-id="24cf5-158">Exemples de configurations d'ordinateur virtuel</span><span class="sxs-lookup"><span data-stu-id="24cf5-158">Examples of Virtual Machine Configurations</span></span>](examples-of-virtual-machine-configurationsv2.md)









