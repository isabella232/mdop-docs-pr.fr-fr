---
title: Comment configurer l'installation d'ordinateur virtuel pour un espace de travail MED-V
description: Comment configurer l'installation d'ordinateur virtuel pour un espace de travail MED-V
author: dansimp
ms.assetid: 50bbf58b-842c-4b63-bb93-3783903f6c7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0ba24f0e9aa5befeaf385acf06273a53feaae29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812137"
---
# <span data-ttu-id="bc319-103">Comment configurer l'installation d'ordinateur virtuel pour un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="bc319-103">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>


<span data-ttu-id="bc319-104">Tous les paramètres de configuration de l’ordinateur virtuel sont configurés dans le module de **stratégie** sous l’onglet Configuration de l' **ordinateur** virtuel.</span><span class="sxs-lookup"><span data-stu-id="bc319-104">All virtual machine setup configuration settings are configured in the **Policy** module, on the **VM Setup** tab.</span></span>

## <span data-ttu-id="bc319-105">Comment configurer la configuration de l’ordinateur virtuel pour un espace de travail MED-V permanent</span><span class="sxs-lookup"><span data-stu-id="bc319-105">How to Configure the Virtual Machine Setup for a Persistent MED-V Workspace</span></span>


**<span data-ttu-id="bc319-106">Pour configurer la configuration de l’ordinateur virtuel pour un espace de travail MED-V permanent</span><span class="sxs-lookup"><span data-stu-id="bc319-106">To configure the virtual machine setup for a persistent MED-V workspace</span></span>**

1.  <span data-ttu-id="bc319-107">Cliquez sur un espace de travail MED-V permanent à configurer.</span><span class="sxs-lookup"><span data-stu-id="bc319-107">Click a persistent MED-V workspace to be configured.</span></span>

2.  <span data-ttu-id="bc319-108">Dans la section Configuration de l' **ordinateur virtuel persistant** , configurez les propriétés comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bc319-108">In the **Persistent VM Setup** section, configure the properties as described in the following table.</span></span>

    **<span data-ttu-id="bc319-109">Remarque</span><span class="sxs-lookup"><span data-stu-id="bc319-109">Note</span></span>**  
    <span data-ttu-id="bc319-110">Les propriétés d’installation du VM persistantes sont activées uniquement pour un espace de travail MED-V permanent.</span><span class="sxs-lookup"><span data-stu-id="bc319-110">The persistent VM setup properties are enabled only for a persistent MED-V workspace.</span></span>



3.  <span data-ttu-id="bc319-111">Dans le menu **stratégie** , cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="bc319-111">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="bc319-112">Propriétés d’installation d’un VM persistant</span><span class="sxs-lookup"><span data-stu-id="bc319-112">Persistent VM Setup Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc319-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="bc319-113">Property</span></span></th>
<th align="left"><span data-ttu-id="bc319-114">Description</span><span class="sxs-lookup"><span data-stu-id="bc319-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc319-115">Exécution de la configuration VM</span><span class="sxs-lookup"><span data-stu-id="bc319-115">Run VM Setup</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc319-116">Activez cette case à cocher pour exécuter un script de configuration la première fois que l’espace de travail MED-V est exécuté.</span><span class="sxs-lookup"><span data-stu-id="bc319-116">Select this check box to run a setup script the first time the MED-V workspace is run.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc319-117">Éditeur de script</span><span class="sxs-lookup"><span data-stu-id="bc319-117">Script Editor</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc319-118">Cliquez pour configurer le script de configuration.</span><span class="sxs-lookup"><span data-stu-id="bc319-118">Click to configure the setup script.</span></span> <span data-ttu-id="bc319-119">Pour plus d’informations, reportez-vous <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)"> à la rubrique Configuration d’actions de script </a> .</span><span class="sxs-lookup"><span data-stu-id="bc319-119">For more information, see <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)">How to Set Up Script Actions</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="bc319-120">Remarque</span><span class="sxs-lookup"><span data-stu-id="bc319-120">Note</span></span></strong><br/><p><span data-ttu-id="bc319-121">Ce bouton est activé uniquement lorsque l' <strong> option exécuter le script de configuration de l’ordinateur virtuel </strong> est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="bc319-121">This button is enabled only when <strong>Run VM Setup script</strong> is selected.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc319-122">Message affiché lors de l’exécution d’un script</span><span class="sxs-lookup"><span data-stu-id="bc319-122">Message displayed when script is running</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc319-123">Message à afficher pendant l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="bc319-123">A message to be displayed while the script is running.</span></span> <span data-ttu-id="bc319-124">S’il est vide, le message par défaut s’affiche.</span><span class="sxs-lookup"><span data-stu-id="bc319-124">If left blank, the default message is displayed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="bc319-125">Remarque</span><span class="sxs-lookup"><span data-stu-id="bc319-125">Note</span></span></strong><br/><p><span data-ttu-id="bc319-126">Ce champ est activé uniquement lorsque <strong> le script de configuration de l’ordinateur virtuel </strong> est activé.</span><span class="sxs-lookup"><span data-stu-id="bc319-126">This field is enabled only when <strong>Run VM Setup script</strong> is checked.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="bc319-127">Comment configurer la configuration de l’ordinateur virtuel pour un espace de travail Revertible MED-V</span><span class="sxs-lookup"><span data-stu-id="bc319-127">How to Configure the Virtual Machine Setup for a Revertible MED-V Workspace</span></span>


**<span data-ttu-id="bc319-128">Pour configurer la configuration de l’ordinateur virtuel pour un espace de travail revertible MED-V</span><span class="sxs-lookup"><span data-stu-id="bc319-128">To configure the virtual machine setup for a revertible MED-V workspace</span></span>**

1.  <span data-ttu-id="bc319-129">Cliquez sur un espace de travail revertible MED-V à configurer.</span><span class="sxs-lookup"><span data-stu-id="bc319-129">Click a revertible MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="bc319-130">Dans la section **installation de REVERTIBLE VM** , configurez les propriétés comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bc319-130">In the **Revertible VM Setup** section, configure the properties as described in the following table.</span></span>

    **<span data-ttu-id="bc319-131">Remarque</span><span class="sxs-lookup"><span data-stu-id="bc319-131">Note</span></span>**  
    <span data-ttu-id="bc319-132">Les propriétés de l’installation de l’ordinateur virtuel revertible sont activées uniquement pour un espace de travail revertible MED-V.</span><span class="sxs-lookup"><span data-stu-id="bc319-132">The revertible VM setup properties are enabled only for a revertible MED-V workspace.</span></span>



3.  <span data-ttu-id="bc319-133">Dans le menu **stratégie** , cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="bc319-133">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="bc319-134">Propriétés de l’installation d’Revertible VM</span><span class="sxs-lookup"><span data-stu-id="bc319-134">Revertible VM Setup Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc319-135">Propriété</span><span class="sxs-lookup"><span data-stu-id="bc319-135">Property</span></span></th>
<th align="left"><span data-ttu-id="bc319-136">Description</span><span class="sxs-lookup"><span data-stu-id="bc319-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc319-137">Renommer la VM en fonction du modèle de nom de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="bc319-137">Rename the VM based on the computer name pattern</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc319-138">Activez cette case à cocher pour affecter un nom unique à chaque ordinateur à l’aide de l’espace de travail MED-V de façon à faire la différence entre plusieurs ordinateurs utilisant le même espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="bc319-138">Select this check box to assign a unique name to each computer using the MED-V workspace so that you can differentiate between multiple computers using the same MED-V workspace.</span></span></p>
<p><span data-ttu-id="bc319-139">Pour plus d’informations sur la configuration des noms d’images d’ordinateur, voir <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)"> configurer les propriétés de modèle de nom d’ordinateur VM </a> .</span><span class="sxs-lookup"><span data-stu-id="bc319-139">For more information on configuring computer image names, see <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)">How to Configure VM Computer Name Pattern Properties</a>.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="bc319-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc319-140">Related topics</span></span>


[<span data-ttu-id="bc319-141">Utilisation de l'interface utilisateur de la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="bc319-141">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="bc319-142">Création d'un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="bc319-142">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="bc319-143">Exemples de configurations d'ordinateur virtuel</span><span class="sxs-lookup"><span data-stu-id="bc319-143">Examples of Virtual Machine Configurations</span></span>](examples-of-virtual-machine-configurationsv2.md)









