---
title: Fenêtre Historique
description: Fenêtre Historique
author: dansimp
ms.assetid: f11f9ad9-bffe-4c56-8c46-fe9c0a8e55c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02b4336409f33d6c1f2868bceb22cb95120f2198
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808446"
---
# <span data-ttu-id="b56a5-103">Fenêtre Historique</span><span class="sxs-lookup"><span data-stu-id="b56a5-103">History Window</span></span>


<span data-ttu-id="b56a5-104">L’historique d’un objet de stratégie de groupe peut être affiché en double-cliquant sur un objet GPO ou en cliquant avec le bouton droit sur un objet de stratégie de groupe, puis en cliquant sur **historique**.</span><span class="sxs-lookup"><span data-stu-id="b56a5-104">The history of a Group Policy object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="b56a5-105">Il est également affiché dans la **console de gestion des stratégies de groupe** (GPMC) en tant qu’onglet pour chaque GPO.</span><span class="sxs-lookup"><span data-stu-id="b56a5-105">It is also displayed in the **Group Policy Management Console** (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="b56a5-106">L’historique fournit la liste de toutes les versions de l’objet de stratégie de groupe sélectionné enregistrées dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="b56a5-106">The history provides a list of all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="b56a5-107">Dans la fenêtre **historique** , vous pouvez obtenir un rapport sur les paramètres d’un objet de stratégie de groupe, comparer plusieurs versions d’un objet de stratégie de groupe ou restaurer une version précédente d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b56a5-107">From the **History** window, you can obtain a report of the settings within a GPO, compare multiple versions of a GPO, or roll back to a previous version of a GPO.</span></span>

## <span data-ttu-id="b56a5-108">Filtrage d’événements dans la fenêtre historique</span><span class="sxs-lookup"><span data-stu-id="b56a5-108">Filtering events in the History window</span></span>


<span data-ttu-id="b56a5-109">Les onglets de la fenêtre **historique** permettent de filtrer les événements affichés.</span><span class="sxs-lookup"><span data-stu-id="b56a5-109">The tabs within the **History** window filter the events displayed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b56a5-110">Eux</span><span class="sxs-lookup"><span data-stu-id="b56a5-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="b56a5-111">Filtre</span><span class="sxs-lookup"><span data-stu-id="b56a5-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b56a5-112">Afficher tout</span><span class="sxs-lookup"><span data-stu-id="b56a5-112">Show All</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b56a5-113">Affichez toutes les versions de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b56a5-113">Display all versions of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b56a5-114">Archivé</span><span class="sxs-lookup"><span data-stu-id="b56a5-114">Checked In</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b56a5-115">Afficher uniquement les versions intégrées de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b56a5-115">Display only checked-in versions of the GPO.</span></span> <span data-ttu-id="b56a5-116">La version déployée ne figure pas dans cette liste.</span><span class="sxs-lookup"><span data-stu-id="b56a5-116">The deployed version is omitted from this list.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b56a5-117">Étiquettes uniquement</span><span class="sxs-lookup"><span data-stu-id="b56a5-117">Labels Only</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b56a5-118">Afficher uniquement les objets de stratégie de groupe associés à des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="b56a5-118">Display only GPOs that have labels associated with them.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b56a5-119">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="b56a5-119">Event information</span></span>


<span data-ttu-id="b56a5-120">Des informations sont fournies pour chaque événement dans l’historique de l’objet de stratégie de groupe sélectionné.</span><span class="sxs-lookup"><span data-stu-id="b56a5-120">Information is provided for each event in the history of the selected GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b56a5-121">Caractéristique de l’objet GPO</span><span class="sxs-lookup"><span data-stu-id="b56a5-121">GPO Characteristic</span></span></th>
<th align="left"><span data-ttu-id="b56a5-122">Description</span><span class="sxs-lookup"><span data-stu-id="b56a5-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b56a5-123">Ordinateur</span><span class="sxs-lookup"><span data-stu-id="b56a5-123">Computer</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b56a5-124">Version générée automatiquement de la partie configuration de l’ordinateur de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b56a5-124">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b56a5-125">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="b56a5-125">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b56a5-126">Version générée automatiquement de la section Configuration utilisateur de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b56a5-126">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b56a5-127">Heure</span><span class="sxs-lookup"><span data-stu-id="b56a5-127">Time</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b56a5-128">Horodatage de la version de l’objet de stratégie de groupe lorsque l’action dans le champ État a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b56a5-128">Timestamp of the version of the GPO when the action in the status field was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b56a5-129">État</span><span class="sxs-lookup"><span data-stu-id="b56a5-129">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b56a5-130">État de la version sélectionnée de l’objet de stratégie de groupe:</span><span class="sxs-lookup"><span data-stu-id="b56a5-130">The state of the selected version of the GPO:</span></span></p>
<p><img src="images/36f6b687-f5cc-40d1-805f-b191d1fb1ace.gif" alt="Deployed GPO icon" /> <strong><span data-ttu-id="b56a5-131">Déploiement </strong> : cette version de l’objet de stratégie de groupe est actuellement active dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="b56a5-131">Deployed</strong>: This version of the GPO is currently live in the production environment.</span></span></p>
<p><img src="images/57b610a5-1c71-4d26-9173-d04abd495fcc.gif" alt="Checked in GPO icon" /> <strong><span data-ttu-id="b56a5-132">Archivé </strong> : cette version de l’objet de stratégie de groupe est disponible pour les éditeurs autorisés à valider et à déployer.</span><span class="sxs-lookup"><span data-stu-id="b56a5-132">Checked In</strong>: This version of the GPO is available for authorized Editors to check out for editing or for a Group Policy administrator to deploy.</span></span></p>
<p><img src="images/8e7a7c4e-809a-435a-8b29-30d797936210.gif" alt="Checked out GPO icon" /> <strong><span data-ttu-id="b56a5-133">Extrait </strong> : cette version de l’objet de stratégie de groupe est actuellement extraite par un éditeur et n’est pas disponible pour les autres éditeurs.</span><span class="sxs-lookup"><span data-stu-id="b56a5-133">Checked Out</strong>: This version of the GPO is currently checked out by an Editor and is unavailable for other Editors.</span></span> <span data-ttu-id="b56a5-134">(L’état extrait n’est pas enregistré dans le <strong> Historique </strong> sauf pour indiquer si un objet de stratégie de groupe est actuellement extrait.)</span><span class="sxs-lookup"><span data-stu-id="b56a5-134">(The checked out state is not recorded in the <strong>History</strong> except to indicate if a GPO is currently checked out.)</span></span></p>
<p><img src="images/327623bd-0842-4372-be1f-bdc4b8c3481c.gif" alt="Created GPO icon" /> <strong><span data-ttu-id="b56a5-135">Créé </strong> : identifie la date et l’heure de la création initiale de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b56a5-135">Created</strong>: Identifies the date and time of the initial creation of the GPO.</span></span></p>
<p><img src="images/8356fcdc-1279-425b-ab14-a23bcfe391da.gif" alt="Labeled GPO icon" /> <strong><span data-ttu-id="b56a5-136">Étiquette </strong> : identifie une version libellée de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b56a5-136">Labeled</strong>: Identifies a labeled version of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b56a5-137">État de l’objet GPO</span><span class="sxs-lookup"><span data-stu-id="b56a5-137">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b56a5-138">La configuration de l’ordinateur et la configuration de l’utilisateur peuvent être gérées indépendamment les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="b56a5-138">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="b56a5-139">Cet état indique les parties de l’objet GPO qui sont activées.</span><span class="sxs-lookup"><span data-stu-id="b56a5-139">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b56a5-140">Propriétaire</span><span class="sxs-lookup"><span data-stu-id="b56a5-140">Owner</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b56a5-141">Personne ayant archivé ou déployé l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b56a5-141">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b56a5-142">Comment</span><span class="sxs-lookup"><span data-stu-id="b56a5-142">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b56a5-143">Commentaire entré par le propriétaire d’un objet de stratégie de groupe au moment de la modification de cette version.</span><span class="sxs-lookup"><span data-stu-id="b56a5-143">A comment entered by the owner of a GPO at the time that this version was modified.</span></span> <span data-ttu-id="b56a5-144">Utile pour identifier les spécificités de la version dans le cas où il est nécessaire de revenir à une version précédente.</span><span class="sxs-lookup"><span data-stu-id="b56a5-144">Useful for identifying the specifics of the version in case of the need to roll back to a previous version.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b56a5-145">Rapports</span><span class="sxs-lookup"><span data-stu-id="b56a5-145">Reports</span></span>


<span data-ttu-id="b56a5-146">Selon que vous avez sélectionné une version d’un objet de stratégie de groupe ou plusieurs versions d’objets de stratégie de groupe, les boutons **paramètres** et **différences** affichent des rapports sur les paramètres de l’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="b56a5-146">Depending on whether a single GPO version or multiple GPO versions are selected, the **Settings** and **Differences** buttons display reports on GPO settings.</span></span> <span data-ttu-id="b56a5-147">Lorsque vous cliquez avec le bouton droit sur les versions de l’objet de stratégie de groupe, vous pouvez également afficher des rapports XML.</span><span class="sxs-lookup"><span data-stu-id="b56a5-147">Right-clicking GPO versions provides the option to display XML-based reports as well.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b56a5-148">Bouton</span><span class="sxs-lookup"><span data-stu-id="b56a5-148">Button</span></span></th>
<th align="left"><span data-ttu-id="b56a5-149">Effet</span><span class="sxs-lookup"><span data-stu-id="b56a5-149">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b56a5-150">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b56a5-150">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b56a5-151">Générer un rapport HTML affichant les paramètres dans la version sélectionnée de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b56a5-151">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b56a5-152">Diffère</span><span class="sxs-lookup"><span data-stu-id="b56a5-152">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b56a5-153">Générer un rapport HTML comparant les paramètres de plusieurs versions sélectionnées de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b56a5-153">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b56a5-154">Clé pour différencier les rapports</span><span class="sxs-lookup"><span data-stu-id="b56a5-154">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b56a5-155">Symbole</span><span class="sxs-lookup"><span data-stu-id="b56a5-155">Symbol</span></span></th>
<th align="left"><span data-ttu-id="b56a5-156">Signification</span><span class="sxs-lookup"><span data-stu-id="b56a5-156">Meaning</span></span></th>
<th align="left"><span data-ttu-id="b56a5-157">Couleur</span><span class="sxs-lookup"><span data-stu-id="b56a5-157">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b56a5-158">None</span><span class="sxs-lookup"><span data-stu-id="b56a5-158">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="b56a5-159">L’élément existe avec des paramètres identiques dans les deux objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="b56a5-159">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="b56a5-160">Varie selon le niveau</span><span class="sxs-lookup"><span data-stu-id="b56a5-160">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b56a5-161">[#]</span><span class="sxs-lookup"><span data-stu-id="b56a5-161">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b56a5-162">L’élément existe dans les deux objets de stratégie de groupe, mais avec les paramètres modifiés</span><span class="sxs-lookup"><span data-stu-id="b56a5-162">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="b56a5-163">Bleu</span><span class="sxs-lookup"><span data-stu-id="b56a5-163">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b56a5-164">[-]</span><span class="sxs-lookup"><span data-stu-id="b56a5-164">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b56a5-165">L’élément existe uniquement dans le premier objet GPO</span><span class="sxs-lookup"><span data-stu-id="b56a5-165">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="b56a5-166">Rouge</span><span class="sxs-lookup"><span data-stu-id="b56a5-166">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b56a5-167">[+]</span><span class="sxs-lookup"><span data-stu-id="b56a5-167">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b56a5-168">L’élément existe uniquement dans le second objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="b56a5-168">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="b56a5-169">Vert</span><span class="sxs-lookup"><span data-stu-id="b56a5-169">Green</span></span></p></td>
</tr>
</tbody>
</table>

 

-   <span data-ttu-id="b56a5-170">Pour les éléments ayant modifié des paramètres, les paramètres modifiés sont identifiés lorsque l’élément est étendu.</span><span class="sxs-lookup"><span data-stu-id="b56a5-170">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="b56a5-171">La valeur de l’attribut dans chaque objet GPO est affichée dans l’ordre dans lequel les objets de stratégie de groupe sont affichés dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="b56a5-171">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="b56a5-172">Certaines modifications apportées aux paramètres peuvent entraîner le signalement d’un élément sous la forme de deux éléments différents (un seul présent dans le premier objet de stratégie de groupe, le premier uniquement dans le second), plutôt qu’un élément modifié.</span><span class="sxs-lookup"><span data-stu-id="b56a5-172">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second), rather than as one item that has changed.</span></span>

### <span data-ttu-id="b56a5-173">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="b56a5-173">Additional references</span></span>

-   [<span data-ttu-id="b56a5-174">Onglet Contenu</span><span class="sxs-lookup"><span data-stu-id="b56a5-174">Contents Tab</span></span>](contents-tab.md)

 

 





