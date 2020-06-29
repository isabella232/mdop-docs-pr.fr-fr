---
title: Fenêtre Historique
description: Fenêtre Historique
author: dansimp
ms.assetid: 114f50a4-508d-4589-b006-6cd05cffe6b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81911b5103c76e267d806fb7cd8acf55811440c9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808450"
---
# <span data-ttu-id="2ab3c-103">Fenêtre Historique</span><span class="sxs-lookup"><span data-stu-id="2ab3c-103">History Window</span></span>


<span data-ttu-id="2ab3c-104">L’historique d’un objet de stratégie de groupe peut être affiché en double-cliquant sur un objet GPO ou en cliquant avec le bouton droit sur un objet de stratégie de groupe, puis en cliquant sur **historique**.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-104">The history of a Group Policy Object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="2ab3c-105">Il est également affiché dans la **console de gestion des stratégies de groupe** (GPMC) en tant qu’onglet pour chaque GPO.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-105">It is also displayed in the **Group Policy Management Console** (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="2ab3c-106">L’historique fournit un enregistrement des événements pendant la durée de vie de l’objet de stratégie de groupe sélectionné.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-106">The history provides a record of events in the lifetime of the selected GPO.</span></span> <span data-ttu-id="2ab3c-107">Dans la fenêtre **historique** , vous pouvez obtenir un rapport sur les paramètres au sein d’une version de l’objet de stratégie de groupe, comparer plusieurs versions d’un objet de stratégie de groupe, ou restaurer une version précédente d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-107">From the **History** window, you can obtain a report of the settings within a version of the GPO, compare multiple versions of a GPO, or roll back to a previous version of a GPO.</span></span>

## <span data-ttu-id="2ab3c-108">Filtrage d’événements dans la fenêtre historique</span><span class="sxs-lookup"><span data-stu-id="2ab3c-108">Filtering events in the History window</span></span>


<span data-ttu-id="2ab3c-109">Les onglets de la fenêtre **historique** permettent de filtrer les États de l’historique de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-109">The tabs within the **History** window filter the states in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ab3c-110">Eux</span><span class="sxs-lookup"><span data-stu-id="2ab3c-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="2ab3c-111">Filtre</span><span class="sxs-lookup"><span data-stu-id="2ab3c-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2ab3c-112">Tous les États</span><span class="sxs-lookup"><span data-stu-id="2ab3c-112">All States</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-113">Affichez tous les États de l’historique de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-113">Display all states in the history of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2ab3c-114">Versions uniques</span><span class="sxs-lookup"><span data-stu-id="2ab3c-114">Unique Versions</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-115">Afficher uniquement les versions uniques de l’objet de stratégie de groupe archivé dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-115">Display only unique versions of the GPO checked into the archive.</span></span> <span data-ttu-id="2ab3c-116">La version déployée dans l’environnement de production, les raccourcis vers des versions uniques et les États d’information sont omis de cette liste.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-116">The version deployed to the production environment, shortcuts to unique versions, and informational states are omitted from this list.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="2ab3c-117">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="2ab3c-117">Event information</span></span>


<span data-ttu-id="2ab3c-118">Des informations sont fournies pour chaque État de l’historique de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-118">Information is provided for each state in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ab3c-119">Attribut d’objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2ab3c-119">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="2ab3c-120">Description</span><span class="sxs-lookup"><span data-stu-id="2ab3c-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2ab3c-121">Changer la date</span><span class="sxs-lookup"><span data-stu-id="2ab3c-121">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-122">Horodatage du moment où l’action dans la <strong> </strong> colonne État a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-122">Time stamp of when the action in the <strong>State</strong> column was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2ab3c-123">État</span><span class="sxs-lookup"><span data-stu-id="2ab3c-123">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-124">État de l’historique de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-124">A state in the history of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2ab3c-125">Modifié par</span><span class="sxs-lookup"><span data-stu-id="2ab3c-125">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-126">Personne ayant archivé ou déployé l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-126">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2ab3c-127">Comment</span><span class="sxs-lookup"><span data-stu-id="2ab3c-127">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-128">Commentaire entré par la personne qui a archivé ou déployé un objet de stratégie de groupe au moment de la modification de cette version.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-128">A comment entered by the person who checked in or deployed a GPO at the time that this version was modified.</span></span> <span data-ttu-id="2ab3c-129">Utile pour identifier les spécificités de la version dans le cas où il est nécessaire de revenir à une version précédente.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-129">Useful for identifying the specifics of the version in case of the need to roll back to a previous version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2ab3c-130">Supprimé</span><span class="sxs-lookup"><span data-stu-id="2ab3c-130">Deletable</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-131">Si cette version de l’objet de stratégie de groupe peut être supprimée si le nombre de versions uniques de chaque GPO conservé dans l’archive est limité.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-131">Whether this version of the GPO can be deleted if the number of unique versions of each GPO retained in the archive is limited.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="2ab3c-132">Remarque</span><span class="sxs-lookup"><span data-stu-id="2ab3c-132">Note</span></span></strong><br/><p><span data-ttu-id="2ab3c-133">Vous pouvez modifier la version d’un objet de stratégie de groupe en cliquant dessus avec le bouton droit, puis en cliquant sur <strong> ne pas autoriser la suppression </strong> ou <strong> autoriser la suppression </strong> .</span><span class="sxs-lookup"><span data-stu-id="2ab3c-133">You can modify whether a version of a GPO is deletable by right-clicking it and then clicking <strong>Do Not Allow Deletion</strong> or <strong>Allow Deletion</strong>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2ab3c-134">Version de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="2ab3c-134">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-135">Version générée automatiquement de la partie configuration de l’ordinateur de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-135">Automatically generated version of the Computer Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2ab3c-136">Version utilisateur</span><span class="sxs-lookup"><span data-stu-id="2ab3c-136">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-137">Version générée automatiquement de la section Configuration utilisateur de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-137">Automatically generated version of the User Configuration portion of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2ab3c-138">État de l’objet GPO</span><span class="sxs-lookup"><span data-stu-id="2ab3c-138">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-139">La configuration de l’ordinateur et la configuration de l’utilisateur peuvent être gérées indépendamment les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-139">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="2ab3c-140">Cet état indique les parties de l’objet GPO qui sont activées.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-140">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2ab3c-141">Filtre WMI</span><span class="sxs-lookup"><span data-stu-id="2ab3c-141">WMI Filter</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-142">Afficher les filtres WMI appliqués à cet objet GPO.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-142">Display any WMI filters that are applied to this GPO.</span></span> <span data-ttu-id="2ab3c-143">Les filtres WMI sont gérés dans le <strong> dossier filtres WMI </strong> pour le domaine dans l’arborescence de la console GPMC.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-143">WMI filters are managed under the <strong>WMI Filters</strong> folder for the domain in the console tree of the GPMC.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="2ab3c-144">Rapports</span><span class="sxs-lookup"><span data-stu-id="2ab3c-144">Reports</span></span>


<span data-ttu-id="2ab3c-145">Les boutons **paramètres** et **différences** affichent des rapports sur les paramètres de l’objet de stratégie de groupe pour la ou les versions de l’objet GPO sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-145">The **Settings** and **Differences** buttons display reports about GPO settings for the GPO version or versions selected.</span></span> <span data-ttu-id="2ab3c-146">Lorsque vous cliquez avec le bouton droit sur les versions de l’objet de stratégie de groupe, vous pouvez également afficher des rapports XML.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-146">Right-clicking GPO versions provides the option to display XML-based reports as well.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ab3c-147">Bouton</span><span class="sxs-lookup"><span data-stu-id="2ab3c-147">Button</span></span></th>
<th align="left"><span data-ttu-id="2ab3c-148">Effet</span><span class="sxs-lookup"><span data-stu-id="2ab3c-148">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2ab3c-149">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ab3c-149">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-150">Générer un rapport HTML affichant les paramètres dans la version sélectionnée de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-150">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2ab3c-151">Diffère</span><span class="sxs-lookup"><span data-stu-id="2ab3c-151">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-152">Générer un rapport HTML comparant les paramètres de plusieurs versions sélectionnées de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-152">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="2ab3c-153">Clé pour différencier les rapports</span><span class="sxs-lookup"><span data-stu-id="2ab3c-153">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2ab3c-154">Symbole</span><span class="sxs-lookup"><span data-stu-id="2ab3c-154">Symbol</span></span></th>
<th align="left"><span data-ttu-id="2ab3c-155">Signification</span><span class="sxs-lookup"><span data-stu-id="2ab3c-155">Meaning</span></span></th>
<th align="left"><span data-ttu-id="2ab3c-156">Couleur</span><span class="sxs-lookup"><span data-stu-id="2ab3c-156">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2ab3c-157">None</span><span class="sxs-lookup"><span data-stu-id="2ab3c-157">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-158">L’élément existe avec des paramètres identiques dans les deux objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2ab3c-158">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-159">Varie selon le niveau</span><span class="sxs-lookup"><span data-stu-id="2ab3c-159">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2ab3c-160">[#]</span><span class="sxs-lookup"><span data-stu-id="2ab3c-160">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-161">L’élément existe dans les deux objets de stratégie de groupe, mais avec les paramètres modifiés</span><span class="sxs-lookup"><span data-stu-id="2ab3c-161">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-162">Bleu</span><span class="sxs-lookup"><span data-stu-id="2ab3c-162">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="2ab3c-163">[-]</span><span class="sxs-lookup"><span data-stu-id="2ab3c-163">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-164">L’élément existe uniquement dans le premier objet GPO</span><span class="sxs-lookup"><span data-stu-id="2ab3c-164">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-165">Rouge</span><span class="sxs-lookup"><span data-stu-id="2ab3c-165">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="2ab3c-166">[+]</span><span class="sxs-lookup"><span data-stu-id="2ab3c-166">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-167">L’élément existe uniquement dans le second objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2ab3c-167">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="2ab3c-168">Vert</span><span class="sxs-lookup"><span data-stu-id="2ab3c-168">Green</span></span></p></td>
</tr>
</tbody>
</table>



-   <span data-ttu-id="2ab3c-169">Pour les éléments ayant modifié des paramètres, les paramètres modifiés sont identifiés lorsque l’élément est étendu.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-169">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="2ab3c-170">La valeur de l’attribut dans chaque objet GPO est affichée dans l’ordre dans lequel les objets de stratégie de groupe sont affichés dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-170">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="2ab3c-171">Certaines modifications apportées aux paramètres peuvent entraîner le signalement d’un élément sous la forme de deux éléments différents (un seul présent dans le premier objet de stratégie de groupe, le premier uniquement dans le second), plutôt qu’un élément modifié.</span><span class="sxs-lookup"><span data-stu-id="2ab3c-171">Some changes to settings may cause an item to be reported as two different items (one present only in the first GPO, one present only in the second), rather than as one item that has changed.</span></span>

### <span data-ttu-id="2ab3c-172">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2ab3c-172">Additional references</span></span>

-   [<span data-ttu-id="2ab3c-173">Onglet Contenu</span><span class="sxs-lookup"><span data-stu-id="2ab3c-173">Contents Tab</span></span>](contents-tab-agpm30ops.md)









