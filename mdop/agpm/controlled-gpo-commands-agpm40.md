---
title: Commandes d'objet de stratégie de groupe contrôlé
description: Commandes d'objet de stratégie de groupe contrôlé
author: dansimp
ms.assetid: 370d3db9-4efc-4799-983d-e29ba5f32b07
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 65e9d06beb4c36762e845e452bab497a8d3da747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808578"
---
# <span data-ttu-id="83923-103">Commandes d'objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="83923-103">Controlled GPO Commands</span></span>


<span data-ttu-id="83923-104">Onglet **contrôlé** :</span><span class="sxs-lookup"><span data-stu-id="83923-104">The **Controlled** tab:</span></span>

-   <span data-ttu-id="83923-105">Affiche une liste des objets de stratégie de groupe gérés par Advanced Group Policy Management (AGPM).</span><span class="sxs-lookup"><span data-stu-id="83923-105">Displays a list of Group Policy Objects (GPOs) managed by Advanced Group Policy Management (AGPM).</span></span>

-   <span data-ttu-id="83923-106">Fournit un menu contextuel contenant des commandes pour gérer les objets de stratégie de groupe et afficher l’historique et les rapports pour les objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="83923-106">Provides a shortcut menu with commands for managing GPOs and for displaying the history and reports for GPOs.</span></span>

-   <span data-ttu-id="83923-107">Affiche la liste des groupes et des utilisateurs qui ont l’autorisation d’accéder à un objet de stratégie de groupe sélectionné.</span><span class="sxs-lookup"><span data-stu-id="83923-107">Displays a list of the groups and users who have permission to access a selected GPO.</span></span>

<span data-ttu-id="83923-108">Lorsque vous cliquez avec le bouton droit sur la liste d' **objets de stratégie de groupe** dans cet onglet, un menu contextuel s’affiche.</span><span class="sxs-lookup"><span data-stu-id="83923-108">Right-clicking the **Group Policy Objects** list on this tab displays a shortcut menu.</span></span> <span data-ttu-id="83923-109">Ce menu inclut les options suivantes:</span><span class="sxs-lookup"><span data-stu-id="83923-109">This menu includes whichever of the following options are applicable.</span></span>

## <span data-ttu-id="83923-110">Contrôle et historique</span><span class="sxs-lookup"><span data-stu-id="83923-110">Control and history</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83923-111">Commande</span><span class="sxs-lookup"><span data-stu-id="83923-111">Command</span></span></th>
<th align="left"><span data-ttu-id="83923-112">Effet</span><span class="sxs-lookup"><span data-stu-id="83923-112">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="83923-113">Nouvel objet de stratégie de groupe contrôlé</span><span class="sxs-lookup"><span data-stu-id="83923-113">New Controlled GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-114">Créez un nouvel objet de stratégie de groupe avec le contrôle de modification géré via AGPM et déployez-le dans l’environnement de production du domaine.</span><span class="sxs-lookup"><span data-stu-id="83923-114">Create a new GPO with change control managed through AGPM and deploy it to the production environment of the domain.</span></span> <span data-ttu-id="83923-115">Si vous n’êtes pas autorisé à créer un objet de stratégie de groupe, vous êtes invité à le faire.</span><span class="sxs-lookup"><span data-stu-id="83923-115">If you do not have permission to create a GPO, you are prompted to submit a request.</span></span> <span data-ttu-id="83923-116">(Cette option s’affiche si aucun objet GPO n’est sélectionné lorsque vous cliquez avec le bouton droit dans la <strong> Liste d’objets de stratégie de groupe </strong> .)</span><span class="sxs-lookup"><span data-stu-id="83923-116">(This option is displayed if no GPO is selected when right-clicking in the <strong>Group Policy Objects</strong> list.)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="83923-117">Historique</span><span class="sxs-lookup"><span data-stu-id="83923-117">History</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-118">Ouvrir une fenêtre répertoriant toutes les versions de l’objet de stratégie de groupe sélectionné enregistrées dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="83923-118">Open a window listing all versions of the selected GPO saved within the archive.</span></span> <span data-ttu-id="83923-119">À partir de l’historique, vous pouvez obtenir un rapport sur les paramètres d’un objet de stratégie de groupe, comparer deux versions d’un objet de stratégie de groupe, comparer un objet GPO à un modèle, ou restaurer une version antérieure d’un objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="83923-119">From the history, you can obtain a report of the settings within a GPO, compare two versions of a GPO, compare a GPO to a template, or roll back to an earlier version of a GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="83923-120">Rapports</span><span class="sxs-lookup"><span data-stu-id="83923-120">Reports</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83923-121">Commande</span><span class="sxs-lookup"><span data-stu-id="83923-121">Command</span></span></th>
<th align="left"><span data-ttu-id="83923-122">Effet</span><span class="sxs-lookup"><span data-stu-id="83923-122">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="83923-123">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83923-123">Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-124">Générer un rapport HTML ou XML affichant les paramètres de l’objet de stratégie de groupe sélectionné ou afficher les liens vers les objets ou objets de stratégie de groupe sélectionnés à partir des unités d’organisation, au moment de la dernière vérification, de l’importation ou de l’archivage des objets de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="83923-124">Generate an HTML-based or XML-based report displaying the settings within the selected GPO or display links to the selected GPO(s) from organizational units as of when the GPO(s) was most recently controlled, imported, or checked in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="83923-125">Diffère</span><span class="sxs-lookup"><span data-stu-id="83923-125">Differences</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-126">Générer un rapport HTML ou XML comparant les paramètres de deux objets de stratégie de groupe sélectionnés ou dans l’objet de stratégie de groupe sélectionné et un modèle.</span><span class="sxs-lookup"><span data-stu-id="83923-126">Generate an HTML-based or XML-based report comparing the settings within two selected GPOs or within the selected GPO and a template.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="83923-127">Édition</span><span class="sxs-lookup"><span data-stu-id="83923-127">Editing</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83923-128">Commande</span><span class="sxs-lookup"><span data-stu-id="83923-128">Command</span></span></th>
<th align="left"><span data-ttu-id="83923-129">Effet</span><span class="sxs-lookup"><span data-stu-id="83923-129">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="83923-130">Edit</span><span class="sxs-lookup"><span data-stu-id="83923-130">Edit</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-131">Ouvrir la <strong> fenêtre de l’éditeur de gestion des stratégies </strong> de groupe pour modifier l’objet de stratégie de groupe sélectionné</span><span class="sxs-lookup"><span data-stu-id="83923-131">Open the <strong>Group Policy Management Editor</strong> window to change the selected GPO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="83923-132">Vérifier</span><span class="sxs-lookup"><span data-stu-id="83923-132">Check Out</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-133">Obtenez une copie de l’objet de stratégie de groupe sélectionné dans l’Archive pour l’édition en mode hors connexion et interdisez à quiconque de modifier l’objet de stratégie de groupe jusqu’à ce qu’il soit réintégré dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="83923-133">Obtain a copy of the selected GPO from the archive for offline editing and prohibit anyone else from editing the GPO until it is checked back into the archive.</span></span> <span data-ttu-id="83923-134">Extraire peut être substitué par un administrateur AGPM (contrôle total).</span><span class="sxs-lookup"><span data-stu-id="83923-134">Check Out can be overridden by an AGPM Administrator (Full Control).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="83923-135">Date d'arrivée</span><span class="sxs-lookup"><span data-stu-id="83923-135">Check In</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-136">Vérifier la version modifiée de l’objet de stratégie de groupe sélectionné dans l’archive, de sorte que d’autres éditeurs autorisés puissent y apporter des modifications ou qu’un approbateur puisse déployer l’objet GPO dans l’environnement de production du domaine.</span><span class="sxs-lookup"><span data-stu-id="83923-136">Check the edited version of the selected GPO into the archive, so other authorized Editors can make changes or an Approver can deploy the GPO to the production environment of the domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="83923-137">Annuler l’extraction</span><span class="sxs-lookup"><span data-stu-id="83923-137">Undo Check Out</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-138">Renvoi d’un objet de stratégie de groupe extraits de l’archive sans modification.</span><span class="sxs-lookup"><span data-stu-id="83923-138">Return a checked out GPO to the archive without any changes.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="83923-139">Gestion des versions</span><span class="sxs-lookup"><span data-stu-id="83923-139">Version management</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83923-140">Commande</span><span class="sxs-lookup"><span data-stu-id="83923-140">Command</span></span></th>
<th align="left"><span data-ttu-id="83923-141">Effet</span><span class="sxs-lookup"><span data-stu-id="83923-141">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="83923-142">Importation à partir de la production</span><span class="sxs-lookup"><span data-stu-id="83923-142">Import from Production</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-143">Pour l’objet de stratégie de groupe sélectionné, copiez la version dans l’environnement de production du domaine dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="83923-143">For the selected GPO, copy the version in the production environment of the domain to the archive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="83923-144">Importer à partir d’un fichier</span><span class="sxs-lookup"><span data-stu-id="83923-144">Import from File</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-145">Remplacer les paramètres de stratégie de l’objet de stratégie de groupe sélectionné et extrait par ceux d’un fichier de sauvegarde d’objet GPO.</span><span class="sxs-lookup"><span data-stu-id="83923-145">Replace the policy settings of the selected, checked-out GPO with those from a GPO backup file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="83923-146">Delete</span><span class="sxs-lookup"><span data-stu-id="83923-146">Delete</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-147">Déplacer l’objet de stratégie de groupe sélectionné vers la corbeille et indiquer si vous souhaitez conserver la version déployée (le cas échéant) en production ou supprimer la version déployée en plus de la version dans l’archive.</span><span class="sxs-lookup"><span data-stu-id="83923-147">Move the selected GPO to the Recycle Bin and indicate whether to leave the deployed version (if one exists) in production or to delete the deployed version in addition to the version in the archive.</span></span> <span data-ttu-id="83923-148">Si vous n’êtes pas autorisé à supprimer un objet de stratégie de groupe, vous êtes invité à le faire.</span><span class="sxs-lookup"><span data-stu-id="83923-148">If you do not have permission to delete a GPO, you are prompted to submit a request.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="83923-149">Déployer</span><span class="sxs-lookup"><span data-stu-id="83923-149">Deploy</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-150">Déplacer l’objet de stratégie de groupe sélectionné archivé dans l’archive dans l’environnement de production du domaine.</span><span class="sxs-lookup"><span data-stu-id="83923-150">Move the selected GPO that is checked into the archive to the production environment of the domain.</span></span> <span data-ttu-id="83923-151">Le rendez-vous actif sur le réseau et écrase la version précédemment active de l’objet de stratégie de groupe s’il existait.</span><span class="sxs-lookup"><span data-stu-id="83923-151">This action makes it active on the network and overwrites the previously active version of the GPO if one existed.</span></span> <span data-ttu-id="83923-152">Si vous n’êtes pas autorisé à déployer un objet de stratégie de groupe, vous serez invité à le faire.</span><span class="sxs-lookup"><span data-stu-id="83923-152">If you do not have permission to deploy a GPO, you will be prompted to submit a request.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="83923-153">Exporter vers</span><span class="sxs-lookup"><span data-stu-id="83923-153">Export to</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-154">Enregistrez l’objet de stratégie de groupe sélectionné dans un fichier de sauvegarde pour pouvoir le copier vers un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="83923-154">Save the selected GPO to a backup file so that you can copy it to another domain.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="83923-155">Label</span><span class="sxs-lookup"><span data-stu-id="83923-155">Label</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-156">Marquer l’objet de stratégie de groupe sélectionné avec une étiquette descriptive (par exemple, &quot; bon &quot; ) et un commentaire de conservation des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="83923-156">Mark the selected GPO with a descriptive label (such as &quot;Known good&quot;) and comment for record keeping.</span></span> <span data-ttu-id="83923-157">Les étiquettes apparaissent dans <strong> la </strong> colonne État et les commentaires dans la <strong> </strong> colonne commentaire de la <strong> </strong> fenêtre historique.</span><span class="sxs-lookup"><span data-stu-id="83923-157">Labels appear in the <strong>State</strong> column and comments in the <strong>Comment</strong> column of the <strong>History</strong> window.</span></span> <span data-ttu-id="83923-158">Ils vous permettent d’identifier les versions antérieures d’un objet de stratégie de groupe pour pouvoir revenir en cas de problème.</span><span class="sxs-lookup"><span data-stu-id="83923-158">They help you identify earlier versions of a GPO so that you can roll back if a problem occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="83923-159">Rename</span><span class="sxs-lookup"><span data-stu-id="83923-159">Rename</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-160">Changer le nom de l’objet de stratégie de groupe sélectionné.</span><span class="sxs-lookup"><span data-stu-id="83923-160">Change the name of the selected GPO.</span></span> <span data-ttu-id="83923-161">Si l’objet GPO a déjà été déployé, il est mis à jour dans l’environnement de production du domaine lorsque celui-ci est redéployé.</span><span class="sxs-lookup"><span data-stu-id="83923-161">If the GPO has already been deployed, the name will be updated in the production environment of the domain when the GPO is redeployed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="83923-162">Enregistrer en tant que modèle</span><span class="sxs-lookup"><span data-stu-id="83923-162">Save as Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-163">Créer un nouveau modèle basé sur les paramètres de l’objet de stratégie de groupe sélectionné.</span><span class="sxs-lookup"><span data-stu-id="83923-163">Create a new template based on the settings of the selected GPO.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="83923-164">Divers</span><span class="sxs-lookup"><span data-stu-id="83923-164">Miscellaneous</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83923-165">Commande</span><span class="sxs-lookup"><span data-stu-id="83923-165">Command</span></span></th>
<th align="left"><span data-ttu-id="83923-166">Effet</span><span class="sxs-lookup"><span data-stu-id="83923-166">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="83923-167">Actualiser</span><span class="sxs-lookup"><span data-stu-id="83923-167">Refresh</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-168">Mettez à jour l’affichage de la console de gestion des stratégies de groupe (GPMC) pour incorporer les modifications.</span><span class="sxs-lookup"><span data-stu-id="83923-168">Update the display of the Group Policy Management Console (GPMC) to incorporate any changes.</span></span> <span data-ttu-id="83923-169">Certaines modifications ne sont pas visibles tant que l’affichage n’est pas actualisé.</span><span class="sxs-lookup"><span data-stu-id="83923-169">Some changes are not visible until the display is refreshed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="83923-170">Help</span><span class="sxs-lookup"><span data-stu-id="83923-170">Help</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="83923-171">Afficher l’aide d’AGPM.</span><span class="sxs-lookup"><span data-stu-id="83923-171">Display help for AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="83923-172">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="83923-172">Additional references</span></span>

-   [<span data-ttu-id="83923-173">Onglet Contenu</span><span class="sxs-lookup"><span data-stu-id="83923-173">Contents Tab</span></span>](contents-tab-agpm40.md)

-   [<span data-ttu-id="83923-174">Exécution de tâches d'éditeur</span><span class="sxs-lookup"><span data-stu-id="83923-174">Performing Editor Tasks</span></span>](performing-editor-tasks-agpm40.md)

-   [<span data-ttu-id="83923-175">Exécution de tâches d'approbateur</span><span class="sxs-lookup"><span data-stu-id="83923-175">Performing Approver Tasks</span></span>](performing-approver-tasks-agpm40.md)

-   [<span data-ttu-id="83923-176">Exécution de tâches de réviseur</span><span class="sxs-lookup"><span data-stu-id="83923-176">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm40.md)

 

 





