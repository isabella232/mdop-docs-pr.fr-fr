---
title: Commandes d'objet de stratégie de groupe contrôlé
description: Commandes d'objet de stratégie de groupe contrôlé
author: dansimp
ms.assetid: 82db4772-154a-4a8d-99cd-2c69e1738698
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8e537751107a2796727e5ed71511649b6bce953a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807682"
---
# <span data-ttu-id="8bd92-103">Commandes d'objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="8bd92-103">Controlled GPO Commands</span></span>


<span data-ttu-id="8bd92-104">Onglet **contrôlé** :</span><span class="sxs-lookup"><span data-stu-id="8bd92-104">The **Controlled** tab:</span></span>

-   <span data-ttu-id="8bd92-105">Affiche une liste des objets de stratégie de groupe gérés par Advanced Group Policy Management (AGPM).</span><span class="sxs-lookup"><span data-stu-id="8bd92-105">Displays a list of Group Policy Objects (GPOs) managed by Advanced Group Policy Management (AGPM).</span></span>

-   <span data-ttu-id="8bd92-106">Fournit un menu contextuel contenant des commandes pour gérer les objets de stratégie de groupe et afficher l’historique et les rapports pour les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8bd92-106">Provides a shortcut menu with commands for managing GPOs and for displaying the history and reports for GPOs.</span></span>

-   <span data-ttu-id="8bd92-107">Affiche la liste des groupes et des utilisateurs qui ont l’autorisation d’accéder à un objet de stratégie de groupe sélectionné.</span><span class="sxs-lookup"><span data-stu-id="8bd92-107">Displays a list of the groups and users who have permission to access a selected GPO.</span></span>

<span data-ttu-id="8bd92-108">Lorsque vous cliquez avec le bouton droit sur la liste d' **objets de stratégie de groupe** dans cet onglet, un menu contextuel s’affiche, dont les options suivantes s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="8bd92-108">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu, including whichever of the following options are applicable.</span></span>

## <span data-ttu-id="8bd92-109">Contrôle et historique</span><span class="sxs-lookup"><span data-stu-id="8bd92-109">Control and history</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8bd92-110">Commande</span><span class="sxs-lookup"><span data-stu-id="8bd92-110">Command</span></span></th>
<th align="left"><span data-ttu-id="8bd92-111">Effet</span><span class="sxs-lookup"><span data-stu-id="8bd92-111">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8bd92-112">Nouvel objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="8bd92-112">New Controlled GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-113">Créez un nouvel objet de stratégie de groupe avec le contrôle de modification géré via AGPM et déployez-le dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="8bd92-113">Create a new GPO with change control managed through AGPM and deploy it to the production environment.</span></span> <span data-ttu-id="8bd92-114">Si vous n’êtes pas autorisé à créer un objet de stratégie de groupe, vous serez invité à le faire.</span><span class="sxs-lookup"><span data-stu-id="8bd92-114">If you do not have permission to create a GPO, you will be prompted to submit a request.</span></span> <span data-ttu-id="8bd92-115">(Cette option s’affiche si aucun objet GPO n’est sélectionné lorsque vous cliquez avec le bouton droit dans la <strong> Liste d’objets de stratégie de groupe </strong> .)</span><span class="sxs-lookup"><span data-stu-id="8bd92-115">(This option is displayed if no GPO is selected when right-clicking in the <strong>Group Policy Objects</strong> list.)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8bd92-116">Historique</span><span class="sxs-lookup"><span data-stu-id="8bd92-116">History</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-117">Ouvrir une fenêtre répertoriant toutes les versions de l’objet de stratégie de groupe sélectionné enregistrées dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="8bd92-117">Open a window listing all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="8bd92-118">À partir de l’historique, vous pouvez obtenir un rapport sur les paramètres d’un objet de stratégie de groupe, comparer deux versions d’un objet de stratégie de groupe, comparer un objet GPO à un modèle, ou restaurer une version précédente d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8bd92-118">From the history, you can obtain a report of the settings within a GPO, compare two versions of a GPO, compare a GPO to a template, or roll back to a previous version of a GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8bd92-119">Rapports</span><span class="sxs-lookup"><span data-stu-id="8bd92-119">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8bd92-120">Commande</span><span class="sxs-lookup"><span data-stu-id="8bd92-120">Command</span></span></th>
<th align="left"><span data-ttu-id="8bd92-121">Effet</span><span class="sxs-lookup"><span data-stu-id="8bd92-121">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8bd92-122">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bd92-122">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-123">Générer un rapport HTML ou XML affichant les paramètres de l’objet de stratégie de groupe sélectionné ou afficher les liens vers les objets ou objets de stratégie de groupe sélectionnés à partir des unités d’organisation, au moment de la dernière vérification, de l’importation ou de l’archivage des objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8bd92-123">Generate an HTML-based or XML-based report displaying the settings within the selected GPO or display links to the selected GPO(s) from organizational units as of when the GPO(s) was most recently controlled, imported, or checked in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8bd92-124">Diffère</span><span class="sxs-lookup"><span data-stu-id="8bd92-124">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-125">Générer un rapport HTML ou XML comparant les paramètres de deux objets de stratégie de groupe sélectionnés ou dans l’objet de stratégie de groupe sélectionné et un modèle.</span><span class="sxs-lookup"><span data-stu-id="8bd92-125">Generate an HTML-based or XML-based report comparing the settings within two selected GPOs or within the selected GPO and a template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8bd92-126">Édition</span><span class="sxs-lookup"><span data-stu-id="8bd92-126">Editing</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8bd92-127">Commande</span><span class="sxs-lookup"><span data-stu-id="8bd92-127">Command</span></span></th>
<th align="left"><span data-ttu-id="8bd92-128">Effet</span><span class="sxs-lookup"><span data-stu-id="8bd92-128">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8bd92-129">Edit</span><span class="sxs-lookup"><span data-stu-id="8bd92-129">Edit</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-130">Ouvrir la <strong> fenêtre de l’éditeur de gestion des stratégies </strong> de groupe pour apporter des modifications à l’objet GPO sélectionné.</span><span class="sxs-lookup"><span data-stu-id="8bd92-130">Open the <strong>Group Policy Management Editor</strong> window to make changes to the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8bd92-131">Vérifier</span><span class="sxs-lookup"><span data-stu-id="8bd92-131">Check Out</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-132">Obtenez une copie de l’objet de stratégie de groupe que vous avez sélectionné dans l’archive en vue d’une modification hors connexion et interdisez-lui de le modifier jusqu’à ce qu’il soit réintégré dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="8bd92-132">Obtain a copy of the selected GPO from the archive for offline editing and prohibit anyone else from editing it until it is checked back into the archive.</span></span> <span data-ttu-id="8bd92-133">(Extraire peut être substitué par un administrateur AGPM (contrôle total).)</span><span class="sxs-lookup"><span data-stu-id="8bd92-133">(Check Out can be overridden by an AGPM Administrator (Full Control).)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8bd92-134">Date d'arrivée</span><span class="sxs-lookup"><span data-stu-id="8bd92-134">Check In</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-135">Vérifier la version modifiée de l’objet de stratégie de groupe sélectionné dans l’archive, de sorte que d’autres éditeurs autorisés puissent y apporter des modifications ou qu’un approbateur puisse la déployer dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="8bd92-135">Check the edited version of the selected GPO into the archive, so other authorized Editors can make changes or an Approver can deploy it to the production environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8bd92-136">Annuler l’extraction</span><span class="sxs-lookup"><span data-stu-id="8bd92-136">Undo Check Out</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-137">Renvoi d’un objet de stratégie de groupe extraits de l’archive sans modification.</span><span class="sxs-lookup"><span data-stu-id="8bd92-137">Return a checked out GPO to the archive without any changes.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8bd92-138">Gestion des versions</span><span class="sxs-lookup"><span data-stu-id="8bd92-138">Version management</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8bd92-139">Commande</span><span class="sxs-lookup"><span data-stu-id="8bd92-139">Command</span></span></th>
<th align="left"><span data-ttu-id="8bd92-140">Effet</span><span class="sxs-lookup"><span data-stu-id="8bd92-140">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8bd92-141">Importation à partir de la production</span><span class="sxs-lookup"><span data-stu-id="8bd92-141">Import from Production</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-142">Pour l’objet de stratégie de groupe sélectionné, copiez la version dans l’environnement de production dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="8bd92-142">For the selected GPO, copy the version in the production environment to the archive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8bd92-143">Delete</span><span class="sxs-lookup"><span data-stu-id="8bd92-143">Delete</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-144">Déplacer l’objet de stratégie de groupe sélectionné vers la corbeille et indiquer si vous souhaitez conserver la version déployée (le cas échéant) en production ou pour la supprimer ainsi que la version dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="8bd92-144">Move the selected GPO to the Recycle Bin and indicate whether to leave the deployed version (if one exists) in production or to delete it as well as the version in the archive.</span></span> <span data-ttu-id="8bd92-145">Si vous n’êtes pas autorisé à supprimer un objet de stratégie de groupe, vous serez invité à le faire.</span><span class="sxs-lookup"><span data-stu-id="8bd92-145">If you do not have permission to delete a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8bd92-146">Déployer</span><span class="sxs-lookup"><span data-stu-id="8bd92-146">Deploy</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-147">Déplacer l’objet de stratégie de groupe sélectionné archivé dans l’archive dans l’environnement de production.</span><span class="sxs-lookup"><span data-stu-id="8bd92-147">Move the selected GPO that is checked into the archive to the production environment.</span></span> <span data-ttu-id="8bd92-148">Le rendez-vous actif sur le réseau et écrase la version précédemment active de l’objet de stratégie de groupe s’il existait.</span><span class="sxs-lookup"><span data-stu-id="8bd92-148">This action makes it active on the network and overwrites the previously active version of the GPO if one existed.</span></span> <span data-ttu-id="8bd92-149">Si vous n’êtes pas autorisé à déployer un objet de stratégie de groupe, vous serez invité à le faire.</span><span class="sxs-lookup"><span data-stu-id="8bd92-149">If you do not have permission to deploy a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8bd92-150">Label</span><span class="sxs-lookup"><span data-stu-id="8bd92-150">Label</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-151">Marquer l’objet de stratégie de groupe sélectionné avec une étiquette descriptive (par exemple, &quot; bon &quot; ) et un commentaire de conservation des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="8bd92-151">Mark the selected GPO with a descriptive label (such as &quot;Known good&quot;) and comment for record keeping.</span></span> <span data-ttu-id="8bd92-152">Les étiquettes apparaissent dans <strong> la </strong> colonne État et les commentaires dans la <strong> </strong> colonne commentaire de la <strong> </strong> fenêtre historique, ce qui vous permet d’identifier facilement les versions précédentes d’un objet de stratégie de groupe identifiées par une étiquette particulière, de sorte que vous puissiez revenir en arrière en cas de problème.</span><span class="sxs-lookup"><span data-stu-id="8bd92-152">Labels appear in the <strong>State</strong> column and comments in the <strong>Comment</strong> column of the <strong>History</strong> window, enabling you to easily identify previous versions of a GPO identified with a particular label, so you can roll back if a problem occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8bd92-153">Rename</span><span class="sxs-lookup"><span data-stu-id="8bd92-153">Rename</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-154">Changer le nom de l’objet de stratégie de groupe sélectionné.</span><span class="sxs-lookup"><span data-stu-id="8bd92-154">Change the name of the selected GPO.</span></span> <span data-ttu-id="8bd92-155">Si l’objet GPO a déjà été déployé, il est mis à jour dans l’environnement de production lors du redéploiement de l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8bd92-155">If the GPO has already been deployed, the name will be updated in the production environment when the GPO is redeployed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8bd92-156">Enregistrer en tant que modèle</span><span class="sxs-lookup"><span data-stu-id="8bd92-156">Save as Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-157">Créer un nouveau modèle basé sur les paramètres de l’objet de stratégie de groupe sélectionné.</span><span class="sxs-lookup"><span data-stu-id="8bd92-157">Create a new template based on the settings of the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8bd92-158">Divers</span><span class="sxs-lookup"><span data-stu-id="8bd92-158">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8bd92-159">Commande</span><span class="sxs-lookup"><span data-stu-id="8bd92-159">Command</span></span></th>
<th align="left"><span data-ttu-id="8bd92-160">Effet</span><span class="sxs-lookup"><span data-stu-id="8bd92-160">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8bd92-161">Actualiser</span><span class="sxs-lookup"><span data-stu-id="8bd92-161">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-162">Mettez à jour l’affichage de la console de gestion des stratégies de groupe (GPMC) pour incorporer les modifications.</span><span class="sxs-lookup"><span data-stu-id="8bd92-162">Update the display of the Group Policy Management Console (GPMC) to incorporate any changes.</span></span> <span data-ttu-id="8bd92-163">Certaines modifications ne sont pas visibles tant que l’affichage n’est pas actualisé.</span><span class="sxs-lookup"><span data-stu-id="8bd92-163">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="8bd92-164">Help</span><span class="sxs-lookup"><span data-stu-id="8bd92-164">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8bd92-165">Afficher l’aide d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="8bd92-165">Display help for AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="8bd92-166">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="8bd92-166">Additional references</span></span>

-   [<span data-ttu-id="8bd92-167">Onglet Contenu</span><span class="sxs-lookup"><span data-stu-id="8bd92-167">Contents Tab</span></span>](contents-tab-agpm30ops.md)

-   [<span data-ttu-id="8bd92-168">Exécution de tâches d'éditeur</span><span class="sxs-lookup"><span data-stu-id="8bd92-168">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm30ops.md)

-   [<span data-ttu-id="8bd92-169">Exécution de tâches d'approbateur</span><span class="sxs-lookup"><span data-stu-id="8bd92-169">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm30ops.md)

-   [<span data-ttu-id="8bd92-170">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="8bd92-170">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





