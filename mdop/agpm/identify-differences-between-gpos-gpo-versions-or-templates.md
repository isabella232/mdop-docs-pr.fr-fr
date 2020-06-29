---
title: Identifier les différences entre les objets de stratégie de groupe, les versions ou les modèles d'objet de stratégie de groupe
description: Identifier les différences entre les objets de stratégie de groupe, les versions ou les modèles d'objet de stratégie de groupe
author: dansimp
ms.assetid: 6320afc4-af81-47e8-9f4c-463ff99d5a53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fd7966c9c72b2f0d30595af55520940c779a409f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808434"
---
# <span data-ttu-id="8252e-103">Identifier les différences entre les objets de stratégie de groupe, les versions ou les modèles d'objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8252e-103">Identify Differences Between GPOs, GPO Versions, or Templates</span></span>


<span data-ttu-id="8252e-104">Vous pouvez générer des rapports de différences HTML ou XML pour analyser les différences entre les objets de stratégie de groupe (GPO), les modèles ou les différentes versions d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8252e-104">You can generate HTML-based or XML-based difference reports to analyze the differences between Group Policy objects (GPOs), templates, or different versions of a GPO.</span></span>

<span data-ttu-id="8252e-105">Un compte d’utilisateur disposant du rôle de réviseur, d’éditeur, d’approbateur ou d’administrateur AGPM (contrôle total) ou des autorisations nécessaires dans la gestion avancée des stratégies de groupe est requis pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="8252e-105">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="8252e-106">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="8252e-106">Review the details in "Additional considerations" in this topic.</span></span>

## <span data-ttu-id="8252e-107">Identification des différences entre les objets de stratégie de groupe, les versions d’objets ou les modèles</span><span class="sxs-lookup"><span data-stu-id="8252e-107">Identifying differences between GPOs, GPO versions, or templates</span></span>


-   [<span data-ttu-id="8252e-108">Entre deux objets ou modèles de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8252e-108">Between two GPOs or templates</span></span>](#bkmk-two-gpos)

-   [<span data-ttu-id="8252e-109">Entre un objet de stratégie de groupe et un modèle</span><span class="sxs-lookup"><span data-stu-id="8252e-109">Between a GPO and a template</span></span>](#bkmk-gpo-and-template)

-   [<span data-ttu-id="8252e-110">Entre deux versions d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8252e-110">Between two versions of one GPO</span></span>](#bkmk-two-versions)

-   [<span data-ttu-id="8252e-111">Entre une version d’un objet de stratégie de groupe et un modèle</span><span class="sxs-lookup"><span data-stu-id="8252e-111">Between a GPO version and a template</span></span>](#bkmk-gpo-version-and-template)

## <a href="" id="bkmk-two-gpos"></a>


**<span data-ttu-id="8252e-112">Pour identifier les différences entre deux objets ou modèles de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8252e-112">To identify differences between two GPOs or templates</span></span>**

1.  <span data-ttu-id="8252e-113">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8252e-113">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8252e-114">Dans l’onglet **contenu** du volet Détails, cliquez sur un onglet pour afficher les objets de stratégie de groupe (ou modèles, si vous comparez deux modèles).</span><span class="sxs-lookup"><span data-stu-id="8252e-114">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="8252e-115">Sélectionnez les deux objets ou modèles d’objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8252e-115">Select the two GPOs or templates.</span></span>

4.  <span data-ttu-id="8252e-116">Cliquez avec le bouton droit sur l’un des modèles ou objets de stratégie de groupe, cliquez sur **différences**, puis sur rapport **HTML** ou **État XML** pour afficher un rapport de différences résumant les paramètres des objets ou modèles de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8252e-116">Right-click one of the GPOs or templates, click **Differences**, and then click **HTML Report** or **XML Report** to display a difference report summarizing the settings of the GPOs or templates.</span></span>

### <a href="" id="bkmk-gpo-and-template"></a>

**<span data-ttu-id="8252e-117">Pour identifier les différences entre un objet de stratégie de groupe et un modèle</span><span class="sxs-lookup"><span data-stu-id="8252e-117">To identify differences between a GPO and a template</span></span>**

1.  <span data-ttu-id="8252e-118">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8252e-118">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8252e-119">Dans l’onglet **contenu** du volet Détails, cliquez sur un onglet pour afficher les objets de stratégie de groupe (ou modèles, si vous comparez deux modèles).</span><span class="sxs-lookup"><span data-stu-id="8252e-119">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="8252e-120">Cliquez avec le bouton droit sur l’objet de stratégie de groupe, cliquez sur **différences**, puis sur **modèle**.</span><span class="sxs-lookup"><span data-stu-id="8252e-120">Right-click the GPO, click **Differences**, and then click **Template**.</span></span>

4.  <span data-ttu-id="8252e-121">Sélectionnez le modèle et le type de rapport, puis cliquez sur **OK** pour afficher un rapport de différences résumant les paramètres de l’objet de stratégie de groupe et du modèle.</span><span class="sxs-lookup"><span data-stu-id="8252e-121">Select the template and type of report, and then click **OK** to display a difference report summarizing the settings of the GPO and template.</span></span>

### <a href="" id="bkmk-two-versions"></a>

**<span data-ttu-id="8252e-122">Pour identifier les différences entre deux versions d’un objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8252e-122">To identify differences between two versions of one GPO</span></span>**

1.  <span data-ttu-id="8252e-123">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8252e-123">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8252e-124">Dans l’onglet **contenu** du volet Détails, cliquez sur un onglet pour afficher les objets de stratégie de groupe (ou modèles, si vous comparez deux modèles).</span><span class="sxs-lookup"><span data-stu-id="8252e-124">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="8252e-125">Double-cliquez sur l’objet de stratégie de groupe pour afficher son historique, puis mettez en surbrillance les versions à comparer.</span><span class="sxs-lookup"><span data-stu-id="8252e-125">Double-click the GPO to display its history, and then highlight the versions to be compared.</span></span>

4.  <span data-ttu-id="8252e-126">Cliquez avec le bouton droit sur l’une des versions, cliquez sur **différences**, puis sur rapport **HTML** ou **État XML** pour afficher un rapport de différences résumant les paramètres des objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8252e-126">Right-click one of the versions, click **Differences**, and then click **HTML Report** or **XML Report** to display a difference report summarizing the settings of the GPOs.</span></span>

### <a href="" id="bkmk-gpo-version-and-template"></a>

**<span data-ttu-id="8252e-127">Pour identifier les différences entre une version d’un objet de stratégie de groupe et un modèle</span><span class="sxs-lookup"><span data-stu-id="8252e-127">To identify differences between a GPO version and a template</span></span>**

1.  <span data-ttu-id="8252e-128">Dans l’arborescence de la **console de gestion des stratégies de groupe** , cliquez sur modifier le **contrôle** dans la forêt et le domaine dans lesquels vous souhaitez gérer les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8252e-128">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="8252e-129">Dans l’onglet **contenu** du volet Détails, cliquez sur un onglet pour afficher les objets de stratégie de groupe (ou modèles, si vous comparez deux modèles).</span><span class="sxs-lookup"><span data-stu-id="8252e-129">On the **Contents** tab in the details pane, click a tab to display GPOs (or templates, if comparing two templates).</span></span>

3.  <span data-ttu-id="8252e-130">Double-cliquez sur l’objet de stratégie de groupe pour afficher son historique.</span><span class="sxs-lookup"><span data-stu-id="8252e-130">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="8252e-131">Cliquez avec le bouton droit sur la version d’objet GPO qui vous intéresse, cliquez sur **différences**, puis sur **modèle**.</span><span class="sxs-lookup"><span data-stu-id="8252e-131">Right-click the GPO version of interest, click **Differences**, and then click **Template**.</span></span>

5.  <span data-ttu-id="8252e-132">Sélectionnez le modèle et le type de rapport, puis cliquez sur **OK** pour afficher un rapport de différences résumant les paramètres de la version et du modèle de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8252e-132">Select the template and type of report, and then click **OK** to display a difference report summarizing the settings of the GPO version and template.</span></span>

## <span data-ttu-id="8252e-133">Clé pour différencier les rapports</span><span class="sxs-lookup"><span data-stu-id="8252e-133">Key to difference reports</span></span>


<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8252e-134">Symbole</span><span class="sxs-lookup"><span data-stu-id="8252e-134">Symbol</span></span></th>
<th align="left"><span data-ttu-id="8252e-135">Signification</span><span class="sxs-lookup"><span data-stu-id="8252e-135">Meaning</span></span></th>
<th align="left"><span data-ttu-id="8252e-136">Couleur</span><span class="sxs-lookup"><span data-stu-id="8252e-136">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8252e-137">None</span><span class="sxs-lookup"><span data-stu-id="8252e-137">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="8252e-138">L’élément existe avec des paramètres identiques dans les deux objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8252e-138">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="8252e-139">Varie selon le niveau</span><span class="sxs-lookup"><span data-stu-id="8252e-139">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8252e-140">[#]</span><span class="sxs-lookup"><span data-stu-id="8252e-140">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8252e-141">L’élément existe dans les deux objets de stratégie de groupe, mais avec les paramètres modifiés</span><span class="sxs-lookup"><span data-stu-id="8252e-141">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="8252e-142">Bleu</span><span class="sxs-lookup"><span data-stu-id="8252e-142">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8252e-143">[-]</span><span class="sxs-lookup"><span data-stu-id="8252e-143">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8252e-144">L’élément existe uniquement dans le premier objet GPO</span><span class="sxs-lookup"><span data-stu-id="8252e-144">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="8252e-145">Rouge</span><span class="sxs-lookup"><span data-stu-id="8252e-145">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8252e-146">[+]</span><span class="sxs-lookup"><span data-stu-id="8252e-146">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8252e-147">L’élément existe uniquement dans le second objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8252e-147">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="8252e-148">Vert</span><span class="sxs-lookup"><span data-stu-id="8252e-148">Green</span></span></p></td>
</tr>
</tbody>
</table>

 

-   <span data-ttu-id="8252e-149">Pour les éléments ayant modifié des paramètres, les paramètres modifiés sont identifiés lorsque l’élément est étendu.</span><span class="sxs-lookup"><span data-stu-id="8252e-149">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="8252e-150">La valeur de l’attribut dans chaque objet GPO est affichée dans l’ordre dans lequel les objets de stratégie de groupe sont affichés dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="8252e-150">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="8252e-151">Certaines modifications apportées aux paramètres peuvent entraîner le signalement d’un élément sous la forme de deux éléments différents (un seul présent dans le premier objet de stratégie de groupe, l’un présent uniquement dans la deuxième) plutôt qu’un élément modifié.</span><span class="sxs-lookup"><span data-stu-id="8252e-151">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second) rather than as one item that has changed.</span></span>

### <span data-ttu-id="8252e-152">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="8252e-152">Additional considerations</span></span>

-   <span data-ttu-id="8252e-153">Par défaut, vous devez être un réviseur, un éditeur, un approbateur ou un administrateur AGPM (contrôle total) pour effectuer cette procédure.</span><span class="sxs-lookup"><span data-stu-id="8252e-153">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="8252e-154">En particulier, vous devez disposer du **contenu de liste** et des autorisations de **paramètres** pour l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="8252e-154">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="8252e-155">Par ailleurs, pour afficher la liste des objets de stratégie de groupe, vous devez disposer de l’autorisation **contenu de liste** pour le domaine.</span><span class="sxs-lookup"><span data-stu-id="8252e-155">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="8252e-156">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="8252e-156">Additional references</span></span>

-   [<span data-ttu-id="8252e-157">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="8252e-157">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 





