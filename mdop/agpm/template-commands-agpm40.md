---
title: Commandes des modèles
description: Commandes des modèles
author: dansimp
ms.assetid: 243a9b18-bf3f-44fa-94d7-5c793f7322da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2c540bf87462f501a4db5596faca43ef66ee8558
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807446"
---
# <span data-ttu-id="e1770-103">Commandes des modèles</span><span class="sxs-lookup"><span data-stu-id="e1770-103">Template Commands</span></span>


<span data-ttu-id="e1770-104">Onglet **modèles** :</span><span class="sxs-lookup"><span data-stu-id="e1770-104">The **Templates** tab:</span></span>

-   <span data-ttu-id="e1770-105">Affiche la liste des modèles disponibles que vous pouvez utiliser pour créer des objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e1770-105">Displays a list of available templates that you can use to create new Group Policy Objects (GPOs).</span></span>

-   <span data-ttu-id="e1770-106">Fournit un menu contextuel contenant des commandes pour la création d’un objet de stratégie de groupe en fonction d’un modèle sélectionné, la gestion des modèles et l’affichage de rapports pour les modèles.</span><span class="sxs-lookup"><span data-stu-id="e1770-106">Provides a shortcut menu with commands for creating a GPO based on a selected template, managing templates, and displaying reports for templates.</span></span>

-   <span data-ttu-id="e1770-107">Affiche la liste des groupes et des utilisateurs autorisés à accéder à un modèle sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e1770-107">Displays a list of the groups and users who have permission to access a selected template.</span></span>

<span data-ttu-id="e1770-108">Dans la mesure où un modèle ne peut pas être modifié, les modèles n’ont pas d’historique.</span><span class="sxs-lookup"><span data-stu-id="e1770-108">Because a template cannot be altered, templates have no history.</span></span> <span data-ttu-id="e1770-109">Toutefois, comme toute version d’un objet de stratégie de groupe, les paramètres d’un modèle peuvent être affichés à l’aide d’un rapport de paramètres ou d’un autre objet de stratégie de groupe avec un rapport de différences.</span><span class="sxs-lookup"><span data-stu-id="e1770-109">However, like any GPO version, the settings of a template can be displayed with a settings report or compared to another GPO with a difference report.</span></span>

<span data-ttu-id="e1770-110">**Remarques**  Un modèle est une version statique non modifiable d’un objet de stratégie de groupe à utiliser comme point de départ pour créer de nouveaux objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e1770-110">**Note** A template is an uneditable, static version of a GPO for use as a starting point for creating new, editable GPOs.</span></span>

 

<span data-ttu-id="e1770-111">Lorsque vous cliquez avec le bouton droit sur la liste d' **objets de stratégie de groupe** dans cet onglet, un menu contextuel s’affiche, dont les options suivantes s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="e1770-111">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu, including whichever of the following options are applicable.</span></span>

## <span data-ttu-id="e1770-112">Contrôle</span><span class="sxs-lookup"><span data-stu-id="e1770-112">Control</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e1770-113">Commande</span><span class="sxs-lookup"><span data-stu-id="e1770-113">Command</span></span></th>
<th align="left"><span data-ttu-id="e1770-114">Effet</span><span class="sxs-lookup"><span data-stu-id="e1770-114">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e1770-115">Nouvel objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="e1770-115">New Controlled GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1770-116">Créer un nouvel objet GPO en fonction du modèle sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e1770-116">Create a new GPO based on the selected template.</span></span> <span data-ttu-id="e1770-117">L’option de déploiement du nouvel objet de stratégie de groupe dans l’environnement de production du domaine est fournie.</span><span class="sxs-lookup"><span data-stu-id="e1770-117">The option to deploy the new GPO to the production environment of the domain is provided.</span></span> <span data-ttu-id="e1770-118">Si vous n’êtes pas autorisé à créer un objet de stratégie de groupe, vous serez invité à le faire.</span><span class="sxs-lookup"><span data-stu-id="e1770-118">If you do not have permission to create a GPO, you will be prompted to submit a request.</span></span> <span data-ttu-id="e1770-119">(Cette option s’affiche si aucun objet GPO n’est sélectionné lorsque vous cliquez avec le bouton droit dans la <strong> Liste d’objets de stratégie de groupe </strong> .)</span><span class="sxs-lookup"><span data-stu-id="e1770-119">(This option is displayed if no GPO is selected when right-clicking in the <strong>Group Policy Objects</strong> list.)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e1770-120">Rapports</span><span class="sxs-lookup"><span data-stu-id="e1770-120">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e1770-121">Commande</span><span class="sxs-lookup"><span data-stu-id="e1770-121">Command</span></span></th>
<th align="left"><span data-ttu-id="e1770-122">Effet</span><span class="sxs-lookup"><span data-stu-id="e1770-122">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e1770-123">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1770-123">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1770-124">Générer un rapport HTML ou XML affichant les paramètres dans l’objet de stratégie de groupe sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e1770-124">Generate an HTML-based or XML-based report displaying the settings within the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e1770-125">Diffère</span><span class="sxs-lookup"><span data-stu-id="e1770-125">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1770-126">Générer un rapport HTML ou XML comparant les paramètres de deux modèles d’objets de stratégie de groupe sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="e1770-126">Generate an HTML-based or XML-based report comparing the settings within two selected GPO templates.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e1770-127">Gestion des modèles</span><span class="sxs-lookup"><span data-stu-id="e1770-127">Template management</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e1770-128">Commande</span><span class="sxs-lookup"><span data-stu-id="e1770-128">Command</span></span></th>
<th align="left"><span data-ttu-id="e1770-129">Effet</span><span class="sxs-lookup"><span data-stu-id="e1770-129">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e1770-130">Définir par défaut</span><span class="sxs-lookup"><span data-stu-id="e1770-130">Set as Default</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1770-131">Définissez le modèle sélectionné comme modèle par défaut à utiliser automatiquement lors de la création d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="e1770-131">Set the selected template as the default to be used automatically when creating a new GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e1770-132">Delete</span><span class="sxs-lookup"><span data-stu-id="e1770-132">Delete</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1770-133">Déplacer le modèle sélectionné vers la <strong> Corbeille </strong> .</span><span class="sxs-lookup"><span data-stu-id="e1770-133">Move the selected template to the <strong>Recycle Bin</strong>.</span></span> <span data-ttu-id="e1770-134">Si vous n’êtes pas autorisé à supprimer un objet de stratégie de groupe, vous serez invité à le faire.</span><span class="sxs-lookup"><span data-stu-id="e1770-134">If you do not have permission to delete a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e1770-135">Rename</span><span class="sxs-lookup"><span data-stu-id="e1770-135">Rename</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1770-136">Changer le nom du modèle sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e1770-136">Change the name of the selected template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e1770-137">Divers</span><span class="sxs-lookup"><span data-stu-id="e1770-137">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e1770-138">Commande</span><span class="sxs-lookup"><span data-stu-id="e1770-138">Command</span></span></th>
<th align="left"><span data-ttu-id="e1770-139">Effet</span><span class="sxs-lookup"><span data-stu-id="e1770-139">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e1770-140">Actualiser</span><span class="sxs-lookup"><span data-stu-id="e1770-140">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1770-141">Mettez à jour l’affichage de la console de gestion des stratégies de groupe pour incorporer les modifications.</span><span class="sxs-lookup"><span data-stu-id="e1770-141">Update the display of the Group Policy Management Console to incorporate any changes.</span></span> <span data-ttu-id="e1770-142">Certaines modifications ne sont pas visibles tant que l’affichage n’est pas actualisé.</span><span class="sxs-lookup"><span data-stu-id="e1770-142">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e1770-143">Help</span><span class="sxs-lookup"><span data-stu-id="e1770-143">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e1770-144">Afficher l’aide pour la gestion avancée des stratégies de groupe (AGPM).</span><span class="sxs-lookup"><span data-stu-id="e1770-144">Display help for Advanced Group Policy Management (AGPM).</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="e1770-145">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1770-145">Additional references</span></span>

-   [<span data-ttu-id="e1770-146">Onglet Contenu</span><span class="sxs-lookup"><span data-stu-id="e1770-146">Contents Tab</span></span>](contents-tab-agpm40.md)

-   [<span data-ttu-id="e1770-147">Exécution de tâches d'éditeur</span><span class="sxs-lookup"><span data-stu-id="e1770-147">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="e1770-148">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="e1770-148">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





