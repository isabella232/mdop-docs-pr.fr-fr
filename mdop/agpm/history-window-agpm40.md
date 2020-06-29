---
title: Fenêtre Historique
description: Fenêtre Historique
author: dansimp
ms.assetid: 5bea62e7-d267-40b2-a66d-fb1be7373a1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81f19e3834e945a45238856e23f6ee4a86407c4a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808449"
---
# <span data-ttu-id="cd657-103">Fenêtre Historique</span><span class="sxs-lookup"><span data-stu-id="cd657-103">History Window</span></span>


<span data-ttu-id="cd657-104">L’historique d’un objet de stratégie de groupe peut être affiché en double-cliquant sur un objet GPO ou en cliquant avec le bouton droit sur un objet de stratégie de groupe, puis en cliquant sur **historique**.</span><span class="sxs-lookup"><span data-stu-id="cd657-104">The history of a Group Policy Object (GPO) can be displayed by double-clicking a GPO or by right-clicking a GPO and then clicking **History**.</span></span> <span data-ttu-id="cd657-105">Il est également affiché dans la console de gestion des stratégies de groupe (GPMC) en tant qu’onglet pour chaque GPO.</span><span class="sxs-lookup"><span data-stu-id="cd657-105">It is also displayed in the Group Policy Management Console (GPMC) as a tab for each GPO.</span></span>

<span data-ttu-id="cd657-106">L’historique fournit un enregistrement des événements pendant la durée de vie de l’objet de stratégie de groupe sélectionné.</span><span class="sxs-lookup"><span data-stu-id="cd657-106">The history provides a record of events in the lifetime of the selected GPO.</span></span> <span data-ttu-id="cd657-107">Dans la fenêtre **historique** , vous pouvez obtenir un rapport sur les paramètres dans une version de l’objet de stratégie de groupe, comparer plusieurs versions d’un objet de stratégie de groupe ou restaurer une version antérieure d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="cd657-107">From the **History** window, you can obtain a report of the settings in a version of the GPO, compare multiple versions of a GPO, or roll back to an earlier version of a GPO.</span></span>

## <span data-ttu-id="cd657-108">Filtrage d’événements dans la fenêtre historique</span><span class="sxs-lookup"><span data-stu-id="cd657-108">Filtering events in the History window</span></span>


<span data-ttu-id="cd657-109">Les onglets de la fenêtre **historique** permettent de filtrer les États de l’historique de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="cd657-109">The tabs within the **History** window filter the states in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cd657-110">Eux</span><span class="sxs-lookup"><span data-stu-id="cd657-110">Tabs</span></span></th>
<th align="left"><span data-ttu-id="cd657-111">Filtre</span><span class="sxs-lookup"><span data-stu-id="cd657-111">Filtering</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cd657-112">Tous les États</span><span class="sxs-lookup"><span data-stu-id="cd657-112">All States</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-113">Affichez tous les États de l’historique de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="cd657-113">Display all states in the history of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cd657-114">Versions uniques</span><span class="sxs-lookup"><span data-stu-id="cd657-114">Unique Versions</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-115">Afficher uniquement les versions uniques de l’objet de stratégie de groupe archivé dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="cd657-115">Display only unique versions of the GPO checked into the archive.</span></span> <span data-ttu-id="cd657-116">La version déployée dans l’environnement de production, les raccourcis vers des versions uniques et les États d’information sont omis de cette liste.</span><span class="sxs-lookup"><span data-stu-id="cd657-116">The version deployed to the production environment, shortcuts to unique versions, and informational states are omitted from this list.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="cd657-117">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="cd657-117">Event information</span></span>


<span data-ttu-id="cd657-118">Des informations sont fournies pour chaque État de l’historique de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="cd657-118">Information is provided for each state in the history of the GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cd657-119">Attribut d’objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="cd657-119">GPO attribute</span></span></th>
<th align="left"><span data-ttu-id="cd657-120">Description</span><span class="sxs-lookup"><span data-stu-id="cd657-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cd657-121">Changer la date</span><span class="sxs-lookup"><span data-stu-id="cd657-121">Change Date</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-122">Horodatage du moment où l’action dans la <strong> </strong> colonne État a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="cd657-122">Time stamp of when the action in the <strong>State</strong> column was performed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cd657-123">État</span><span class="sxs-lookup"><span data-stu-id="cd657-123">State</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-124">État de l’historique de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="cd657-124">A state in the history of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cd657-125">Modifié par</span><span class="sxs-lookup"><span data-stu-id="cd657-125">Changed By</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-126">Personne ayant archivé ou déployé l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="cd657-126">The person who checked in or deployed the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cd657-127">Comment</span><span class="sxs-lookup"><span data-stu-id="cd657-127">Comment</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-128">Commentaire entré par la personne qui a archivé ou déployé un objet de stratégie de groupe lors de la modification de cette version, utile pour identifier les spécificités de la version dans le cas où il est nécessaire de revenir à une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="cd657-128">A comment entered by the person who checked in or deployed a GPO at the time that this version was changed, useful for identifying the specifics of the version in case of the need to roll back to an earlier version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cd657-129">Supprimé</span><span class="sxs-lookup"><span data-stu-id="cd657-129">Deletable</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-130">Si cette version de l’objet de stratégie de groupe peut être supprimée si le nombre de versions uniques de chaque GPO conservé dans l’archive est limité.</span><span class="sxs-lookup"><span data-stu-id="cd657-130">Whether this version of the GPO can be deleted if the number of unique versions of each GPO retained in the archive is limited.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="cd657-131">Remarque</span><span class="sxs-lookup"><span data-stu-id="cd657-131">Note</span></span></strong><br/><p><span data-ttu-id="cd657-132">Vous pouvez modifier l’état d’une version d’un objet de stratégie de groupe en cliquant avec le bouton droit sur celui-ci, puis en cliquant sur <strong> ne pas autoriser la suppression </strong> ou <strong> autoriser la suppression </strong> .</span><span class="sxs-lookup"><span data-stu-id="cd657-132">You can change whether a version of a GPO can be deleted by right-clicking the GPO and then clicking <strong>Do Not Allow Deletion</strong> or <strong>Allow Deletion</strong>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cd657-133">Version de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="cd657-133">Computer Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-134">Version générée automatiquement de la partie configuration de l’ordinateur de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="cd657-134">Automatically generated version of the Computer Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cd657-135">Version utilisateur</span><span class="sxs-lookup"><span data-stu-id="cd657-135">User Version</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-136">Version générée automatiquement de la partie de configuration utilisateur de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="cd657-136">Automatically generated version of the User Configuration part of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cd657-137">État de l’objet GPO</span><span class="sxs-lookup"><span data-stu-id="cd657-137">GPO Status</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-138">La configuration de l’ordinateur et la configuration de l’utilisateur peuvent être gérées indépendamment les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="cd657-138">The Computer Configuration and the User Configuration can be managed separately from each other.</span></span> <span data-ttu-id="cd657-139">Cet état indique les parties de l’objet GPO qui sont activées.</span><span class="sxs-lookup"><span data-stu-id="cd657-139">This status shows which portions of the GPO are enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cd657-140">Informations sur l’objet GPO source</span><span class="sxs-lookup"><span data-stu-id="cd657-140">Source GPO Information</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-141">Dans le cas d’un objet de stratégie de groupe importé à partir d’une autre forêt, nom de l’objet GPO original, domaine et date associée à la dernière modification.</span><span class="sxs-lookup"><span data-stu-id="cd657-141">For a GPO that has been imported from another forest, the original GPO name, domain, and user and date associated with the last change.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="cd657-142">Rapports</span><span class="sxs-lookup"><span data-stu-id="cd657-142">Reports</span></span>


<span data-ttu-id="cd657-143">Les boutons **paramètres** et **différences** affichent des rapports sur les paramètres de l’objet de stratégie de groupe pour la ou les versions de l’objet GPO sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="cd657-143">The **Settings** and **Differences** buttons display reports about GPO settings for the GPO version or versions selected.</span></span> <span data-ttu-id="cd657-144">En outre, le fait de cliquer avec le bouton droit sur une version ou une version d’un objet de stratégie de groupe vous permet d’afficher des rapports XML.</span><span class="sxs-lookup"><span data-stu-id="cd657-144">Also, right-clicking a GPO version or versions provides the option to display XML-based reports.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cd657-145">Bouton</span><span class="sxs-lookup"><span data-stu-id="cd657-145">Button</span></span></th>
<th align="left"><span data-ttu-id="cd657-146">Effet</span><span class="sxs-lookup"><span data-stu-id="cd657-146">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cd657-147">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd657-147">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-148">Générer un rapport HTML affichant les paramètres dans la version sélectionnée de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="cd657-148">Generate an HTML-based report displaying the settings within the selected version of the GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cd657-149">Diffère</span><span class="sxs-lookup"><span data-stu-id="cd657-149">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-150">Générer un rapport HTML comparant les paramètres de plusieurs versions sélectionnées de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="cd657-150">Generate an HTML-based report comparing the settings within multiple selected versions of the GPO.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="cd657-151">Clé pour différencier les rapports</span><span class="sxs-lookup"><span data-stu-id="cd657-151">Key to difference reports</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cd657-152">Symbole</span><span class="sxs-lookup"><span data-stu-id="cd657-152">Symbol</span></span></th>
<th align="left"><span data-ttu-id="cd657-153">Signification</span><span class="sxs-lookup"><span data-stu-id="cd657-153">Meaning</span></span></th>
<th align="left"><span data-ttu-id="cd657-154">Couleur</span><span class="sxs-lookup"><span data-stu-id="cd657-154">Color</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd657-155">None</span><span class="sxs-lookup"><span data-stu-id="cd657-155">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd657-156">L’élément existe avec des paramètres identiques dans les deux objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="cd657-156">Item exists with identical settings in both GPOs</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd657-157">Varie selon le niveau</span><span class="sxs-lookup"><span data-stu-id="cd657-157">Varies with level</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cd657-158">[#]</span><span class="sxs-lookup"><span data-stu-id="cd657-158">[#]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-159">L’élément existe dans les deux objets de stratégie de groupe, mais avec les paramètres modifiés</span><span class="sxs-lookup"><span data-stu-id="cd657-159">Item exists in both GPOs, but with changed settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd657-160">Bleu</span><span class="sxs-lookup"><span data-stu-id="cd657-160">Blue</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="cd657-161">[-]</span><span class="sxs-lookup"><span data-stu-id="cd657-161">[-]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-162">L’élément existe uniquement dans le premier objet GPO</span><span class="sxs-lookup"><span data-stu-id="cd657-162">Item exists only in the first GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd657-163">Rouge</span><span class="sxs-lookup"><span data-stu-id="cd657-163">Red</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="cd657-164">[+]</span><span class="sxs-lookup"><span data-stu-id="cd657-164">[+]</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="cd657-165">L’élément existe uniquement dans le second objet de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="cd657-165">Item exists only in the second GPO</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd657-166">Vert</span><span class="sxs-lookup"><span data-stu-id="cd657-166">Green</span></span></p></td>
</tr>
</tbody>
</table>



-   <span data-ttu-id="cd657-167">Pour les éléments ayant modifié des paramètres, les paramètres modifiés sont identifiés lorsque l’élément est étendu.</span><span class="sxs-lookup"><span data-stu-id="cd657-167">For items with changed settings, the changed settings are identified when the item is expanded.</span></span> <span data-ttu-id="cd657-168">La valeur de l’attribut dans chaque objet GPO est affichée dans l’ordre dans lequel les objets de stratégie de groupe sont affichés dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="cd657-168">The value for the attribute in each GPO is displayed in the same order that the GPOs are displayed in the report.</span></span>

-   <span data-ttu-id="cd657-169">Certaines modifications apportées aux paramètres peuvent entraîner le signalement d’un élément sous la forme de deux éléments (le premier est présent uniquement dans le premier objet de stratégie de groupe, le premier uniquement dans le second), au lieu d’un élément modifié.</span><span class="sxs-lookup"><span data-stu-id="cd657-169">Some changes to settings may cause an item to be reported as two items (one present only in the first GPO, one present only in the second), instead of one item that has changed.</span></span>

### <span data-ttu-id="cd657-170">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cd657-170">Additional references</span></span>

-   [<span data-ttu-id="cd657-171">Onglet Contenu</span><span class="sxs-lookup"><span data-stu-id="cd657-171">Contents Tab</span></span>](contents-tab-agpm40.md)









