---
title: Comment générer des rapports
description: Comment générer des rapports
author: dansimp
ms.assetid: 9f8ba28e-1993-4c11-a28a-493718051e5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 930b7061d3e5e2fb9951d45b1422915836cbc00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812089"
---
# <span data-ttu-id="a28b4-103">Comment générer des rapports</span><span class="sxs-lookup"><span data-stu-id="a28b4-103">How to Generate Reports</span></span>


<span data-ttu-id="a28b4-104">Les types de rapports suivants peuvent être créés par les administrateurs dans MED-V:</span><span class="sxs-lookup"><span data-stu-id="a28b4-104">The following report types can be created by administrators in MED-V:</span></span>

-   <span data-ttu-id="a28b4-105">[État](#bkmk-generatingastatusreport): utilisez le rapport d’État pour passer en revue l’état actuel de tous les utilisateurs actifs et de tous les espaces de travail MED-V de chaque utilisateur sur la base d’une période de temps définie.</span><span class="sxs-lookup"><span data-stu-id="a28b4-105">[Status](#bkmk-generatingastatusreport)—Use the status report to review the current status of all active users and all MED-V workspaces of each user based on a defined period of time.</span></span> <span data-ttu-id="a28b4-106">Cela inclut l’affichage d’ordinateurs actuellement connectés au serveur ou, s’ils ne sont pas connectés, la date et l’heure de la dernière connexion au serveur, l’état de chaque ordinateur et d’autres informations pertinentes.</span><span class="sxs-lookup"><span data-stu-id="a28b4-106">This includes viewing computers that are currently connected to the server or, if they are not currently connected, the date and time they were last connected to the server, the status of each computer, and other relevant information.</span></span>

-   <span data-ttu-id="a28b4-107">[Journal d’activité](#bkmk-generatinganactivitylogreport): ce rapport permet de passer en revue les événements provenant d’un hôte ou d’un utilisateur spécifique dans une plage de dates définie.</span><span class="sxs-lookup"><span data-stu-id="a28b4-107">[Activity Log](#bkmk-generatinganactivitylogreport)—Use this report to review events that originated from a specific host or user in a defined date range.</span></span>

-   <span data-ttu-id="a28b4-108">[Journal des erreurs](#bkmk-generatinganerrorlogreport): ce rapport vous permet d’afficher les erreurs provenant d’un hôte ou d’un utilisateur spécifique dans une plage de dates définie.</span><span class="sxs-lookup"><span data-stu-id="a28b4-108">[Error Log](#bkmk-generatinganerrorlogreport)—Use this report to view errors that originated from a specific host or user in a defined date range.</span></span>

<span data-ttu-id="a28b4-109">Les résultats du rapport peuvent être triés par n’importe quelle colonne en cliquant sur le nom de colonne approprié.</span><span class="sxs-lookup"><span data-stu-id="a28b4-109">The report results can be sorted by any column by clicking the appropriate column name.</span></span>

<span data-ttu-id="a28b4-110">Vous pouvez regrouper les résultats d’un rapport en faisant glisser un en-tête de colonne vers le haut de l’État.</span><span class="sxs-lookup"><span data-stu-id="a28b4-110">The report results can be grouped by dragging a column header to the top of the report.</span></span> <span data-ttu-id="a28b4-111">Faites glisser plusieurs en-têtes de colonnes pour regrouper une colonne après l’autre.</span><span class="sxs-lookup"><span data-stu-id="a28b4-111">Drag multiple column headers to group one column after another.</span></span>

## <a href="" id="bkmk-generatingastatusreport"></a><span data-ttu-id="a28b4-112">Génération d’un rapport d’État</span><span class="sxs-lookup"><span data-stu-id="a28b4-112">How to Generate a Status Report</span></span>


**<span data-ttu-id="a28b4-113">Pour générer un rapport d’État</span><span class="sxs-lookup"><span data-stu-id="a28b4-113">To generate a status report</span></span>**

1.  <span data-ttu-id="a28b4-114">Cliquez sur le bouton gestion des **rapports** .</span><span class="sxs-lookup"><span data-stu-id="a28b4-114">Click the **Reports** management button.</span></span>

2.  <span data-ttu-id="a28b4-115">Dans le module **rapports** , dans le menu **types de rapports** , sélectionnez **statut**, puis cliquez sur **générer**.</span><span class="sxs-lookup"><span data-stu-id="a28b4-115">In the **Reports** module, on the **Report Types** menu, select **Status**, and click **Generate**.</span></span>

    <span data-ttu-id="a28b4-116">La boîte de dialogue Paramètres du rapport s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a28b4-116">The Report Parameters dialog box appears.</span></span>

3.  <span data-ttu-id="a28b4-117">Dans la boîte de dialogue **paramètres du rapport** , dans le champ **nombre de jours** , entrez un nombre ou utilisez les flèches pour sélectionner le nombre de jours à inclure dans le rapport d’État, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a28b4-117">In the **Report Parameters** dialog box, in the **Number of days** field, enter a number or use the arrows to select the number of days to include in the status report, and click **OK**.</span></span>

    <span data-ttu-id="a28b4-118">Un rapport d’État est généré.</span><span class="sxs-lookup"><span data-stu-id="a28b4-118">A status report is generated.</span></span> <span data-ttu-id="a28b4-119">Les paramètres du rapport sont définis dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a28b4-119">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="a28b4-120">Propriétés d’espace de travail MED-V du client</span><span class="sxs-lookup"><span data-stu-id="a28b4-120">Client MED-V Workspace Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a28b4-121">Propriété</span><span class="sxs-lookup"><span data-stu-id="a28b4-121">Property</span></span></th>
<th align="left"><span data-ttu-id="a28b4-122">Description</span><span class="sxs-lookup"><span data-stu-id="a28b4-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a28b4-123">Durée</span><span class="sxs-lookup"><span data-stu-id="a28b4-123">Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-124">Date et heure de l’événement.</span><span class="sxs-lookup"><span data-stu-id="a28b4-124">The date and time the event occurred.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a28b4-125">Remarque</span><span class="sxs-lookup"><span data-stu-id="a28b4-125">Note</span></span></strong><br/><p><span data-ttu-id="a28b4-126">Par défaut, les événements s’affichent dans l’ordre décroissant de dates.</span><span class="sxs-lookup"><span data-stu-id="a28b4-126">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="a28b4-127">Néanmoins, il peut être modifié en cliquant sur la colonne heure de réception.</span><span class="sxs-lookup"><span data-stu-id="a28b4-127">However, it can be changed by clicking the Time Received column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a28b4-128">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a28b4-128">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-129">Utilisateur qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="a28b4-129">The user who initiated the event.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a28b4-130">Remarque</span><span class="sxs-lookup"><span data-stu-id="a28b4-130">Note</span></span></strong><br/><p><span data-ttu-id="a28b4-131">Si l’événement s’est produit avant la connexion de l’utilisateur, le nom d’utilisateur est système.</span><span class="sxs-lookup"><span data-stu-id="a28b4-131">If the event occurred before a user logged on, the user name is SYSTEM.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a28b4-132">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="a28b4-132">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-133">Nom de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="a28b4-133">The name of the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a28b4-134">Nom de l’espace de travail</span><span class="sxs-lookup"><span data-stu-id="a28b4-134">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-135">Nom de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="a28b4-135">The name of the MED-V workspace.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a28b4-136">Espace de travail nom de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="a28b4-136">Workspace Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-137">Nom de l’ordinateur sur lequel l’espace de travail MED-V est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a28b4-137">The name of the computer the MED-V workspace is running on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a28b4-138">Online</span><span class="sxs-lookup"><span data-stu-id="a28b4-138">Online</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-139">État actuel de l’ordinateur client:</span><span class="sxs-lookup"><span data-stu-id="a28b4-139">The current state of the client computer:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="a28b4-140">Ne</span><span class="sxs-lookup"><span data-stu-id="a28b4-140">Stopped</span></span></strong></p></li>
<li><p><strong><span data-ttu-id="a28b4-141">Démarré à &lt; la date et heure de démarrage de l’espace de travail&gt;</span><span class="sxs-lookup"><span data-stu-id="a28b4-141">Started at &lt;date and time the workspace was started&gt;</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a28b4-142">Version du client</span><span class="sxs-lookup"><span data-stu-id="a28b4-142">Client Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-143">Numéro de version du client.</span><span class="sxs-lookup"><span data-stu-id="a28b4-143">The version number of the client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a28b4-144">Version de la stratégie</span><span class="sxs-lookup"><span data-stu-id="a28b4-144">Policy Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-145">Version de stratégie utilisée actuellement par l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="a28b4-145">The policy version that the MED-V workspace is currently using.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a28b4-146">Nom de l’image</span><span class="sxs-lookup"><span data-stu-id="a28b4-146">Image Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-147">Nom de l’image.</span><span class="sxs-lookup"><span data-stu-id="a28b4-147">The name of the image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a28b4-148">Version d’image</span><span class="sxs-lookup"><span data-stu-id="a28b4-148">Image Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-149">Version d’image utilisée actuellement par l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="a28b4-149">The image version that the MED-V workspace is currently using.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a28b4-150">Remarque</span><span class="sxs-lookup"><span data-stu-id="a28b4-150">Note</span></span></strong><br/><p><span data-ttu-id="a28b4-151">La version de l’espace de travail MED-V peut être inconnue s’il n’a pas encore été téléchargé sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a28b4-151">MED-V workspace version can be Unknown if it has not yet been downloaded onto a computer.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganactivitylogreport"></a><span data-ttu-id="a28b4-152">Génération d’un rapport du journal d’activité</span><span class="sxs-lookup"><span data-stu-id="a28b4-152">How to Generate an Activity Log Report</span></span>


**<span data-ttu-id="a28b4-153">Pour générer un rapport du journal d’activité</span><span class="sxs-lookup"><span data-stu-id="a28b4-153">To generate an activity log report</span></span>**

1.  <span data-ttu-id="a28b4-154">Cliquez sur le bouton gestion des **rapports** .</span><span class="sxs-lookup"><span data-stu-id="a28b4-154">Click the **Reports** management button.</span></span>

    <span data-ttu-id="a28b4-155">Le module rapports apparaît.</span><span class="sxs-lookup"><span data-stu-id="a28b4-155">The Reports module appears.</span></span>

2.  <span data-ttu-id="a28b4-156">Dans le module **rapports** , dans le menu **types de rapports** , sélectionnez journal d' **activité**, puis cliquez sur **générer**.</span><span class="sxs-lookup"><span data-stu-id="a28b4-156">In the **Reports** module, on the **Report Types** menu, select **Activity Log**, and click **Generate**.</span></span>

3.  <span data-ttu-id="a28b4-157">Dans la boîte de dialogue **paramètres du rapport** , configurez un ou plusieurs des paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="a28b4-157">In the **Report Parameters** dialog box, configure one or more of the following parameters:</span></span>

    -   <span data-ttu-id="a28b4-158">**Nombre de jours**: le nombre de jours à afficher dans l’État.</span><span class="sxs-lookup"><span data-stu-id="a28b4-158">**Number of days**—The number of days to display in the report.</span></span>

    -   <span data-ttu-id="a28b4-159">**Nom d’utilisateur contient**: tout événement pour lequel le nom d’utilisateur contient le texte entré est inclus dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="a28b4-159">**User name contains**—Any event where the user name contains the text entered is included in the report.</span></span>

    -   <span data-ttu-id="a28b4-160">**Nom d’hôte contient**: tout événement pour lequel le nom d’hôte contient le texte entré est inclus dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="a28b4-160">**Host name contains**—Any event where the host name contains the text entered is included in the report.</span></span>

4.  <span data-ttu-id="a28b4-161">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a28b4-161">Click **OK**.</span></span>

    <span data-ttu-id="a28b4-162">Un rapport est généré avec les événements et les dates sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="a28b4-162">A report is generated with the events and dates selected.</span></span> <span data-ttu-id="a28b4-163">Les paramètres du rapport sont définis dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a28b4-163">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="a28b4-164">Propriétés du rapport du journal d’activité</span><span class="sxs-lookup"><span data-stu-id="a28b4-164">Activity Log Report Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a28b4-165">Propriété</span><span class="sxs-lookup"><span data-stu-id="a28b4-165">Property</span></span></th>
<th align="left"><span data-ttu-id="a28b4-166">Description</span><span class="sxs-lookup"><span data-stu-id="a28b4-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a28b4-167">ID d’événement</span><span class="sxs-lookup"><span data-stu-id="a28b4-167">Event ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-168">ID de l’événement.</span><span class="sxs-lookup"><span data-stu-id="a28b4-168">The event ID.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a28b4-169">Gravité</span><span class="sxs-lookup"><span data-stu-id="a28b4-169">Severity</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="a28b4-170">Informations, erreur, avertissement</span><span class="sxs-lookup"><span data-stu-id="a28b4-170">Information, Error, Warning</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a28b4-171">Catégorie</span><span class="sxs-lookup"><span data-stu-id="a28b4-171">Category</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-172">Module référencé par le rapport.</span><span class="sxs-lookup"><span data-stu-id="a28b4-172">The module that the report is referring to.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a28b4-173">Description</span><span class="sxs-lookup"><span data-stu-id="a28b4-173">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-174">Description de l’événement.</span><span class="sxs-lookup"><span data-stu-id="a28b4-174">A description of the event.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a28b4-175">Temps reçu</span><span class="sxs-lookup"><span data-stu-id="a28b4-175">Time Received</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-176">Date et heure de réception de l’événement sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="a28b4-176">The date and time the event was received on the server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a28b4-177">Remarque</span><span class="sxs-lookup"><span data-stu-id="a28b4-177">Note</span></span></strong><br/><p><span data-ttu-id="a28b4-178">Si le client est en mode hors connexion, le serveur reçoit les rapports lorsque le client est connecté.</span><span class="sxs-lookup"><span data-stu-id="a28b4-178">If the client is working offline, the server receives the reports when the client is online.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="a28b4-179">Remarque</span><span class="sxs-lookup"><span data-stu-id="a28b4-179">Note</span></span></strong><br/><p><span data-ttu-id="a28b4-180">Par défaut, les événements s’affichent dans l’ordre décroissant de dates.</span><span class="sxs-lookup"><span data-stu-id="a28b4-180">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="a28b4-181">Néanmoins, il peut être modifié en cliquant sur la <strong> colonne heure de réception </strong> .</span><span class="sxs-lookup"><span data-stu-id="a28b4-181">However, it can be changed by clicking the <strong>Time Received</strong> column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a28b4-182">Temps client</span><span class="sxs-lookup"><span data-stu-id="a28b4-182">Client Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-183">Date et heure auxquelles l’événement s’est produit en fonction de l’horloge du client.</span><span class="sxs-lookup"><span data-stu-id="a28b4-183">The date and time the event occurred according to the client clock.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a28b4-184">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="a28b4-184">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-185">Nom de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="a28b4-185">The name of the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a28b4-186">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a28b4-186">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-187">Utilisateur qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="a28b4-187">The user who initiated the event.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a28b4-188">Nom de l’espace de travail</span><span class="sxs-lookup"><span data-stu-id="a28b4-188">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-189">Nom de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="a28b4-189">The name of the MED-V workspace.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a28b4-190">Espace de travail nom de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="a28b4-190">Workspace Computer Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-191">Nom de l’ordinateur sur lequel l’espace de travail MED-V est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a28b4-191">The name of the computer the MED-V workspace is running on.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-generatinganerrorlogreport"></a><span data-ttu-id="a28b4-192">Génération d’un rapport du journal des erreurs</span><span class="sxs-lookup"><span data-stu-id="a28b4-192">How to Generate an Error Log Report</span></span>


**<span data-ttu-id="a28b4-193">Pour générer un rapport du journal des erreurs</span><span class="sxs-lookup"><span data-stu-id="a28b4-193">To generate an error log report</span></span>**

1.  <span data-ttu-id="a28b4-194">Cliquez sur le bouton gestion des **rapports** .</span><span class="sxs-lookup"><span data-stu-id="a28b4-194">Click the **Reports** management button.</span></span>

2.  <span data-ttu-id="a28b4-195">Dans le module **rapports** , dans le menu **types de rapports** , sélectionnez journal des **Erreurs**, puis cliquez sur **générer**.</span><span class="sxs-lookup"><span data-stu-id="a28b4-195">In the **Reports** module, on the **Report Types** menu, select **Error Log**, and click **Generate**.</span></span>

3.  <span data-ttu-id="a28b4-196">Dans la boîte de dialogue **paramètres du rapport** , configurez un ou plusieurs des paramètres suivants:</span><span class="sxs-lookup"><span data-stu-id="a28b4-196">In the **Report Parameters** dialog box, configure one or more of the following parameters:</span></span>

    -   <span data-ttu-id="a28b4-197">**Nombre de jours**: le nombre de jours à afficher dans l’État.</span><span class="sxs-lookup"><span data-stu-id="a28b4-197">**Number of days**—The number of days to display in the report.</span></span>

    -   <span data-ttu-id="a28b4-198">**Nom d’utilisateur contient**: tout événement pour lequel le nom d’utilisateur contient le texte entré est inclus dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="a28b4-198">**User name contains**—Any event where the user name contains the text entered is included in the report.</span></span>

    -   <span data-ttu-id="a28b4-199">**Nom d’hôte contient**: tout événement pour lequel le nom d’hôte contient le texte entré est inclus dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="a28b4-199">**Host name contains**—Any event where the host name contains the text entered is included in the report.</span></span>

4.  <span data-ttu-id="a28b4-200">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a28b4-200">Click **OK**.</span></span>

    <span data-ttu-id="a28b4-201">Un rapport est généré avec les événements et les dates sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="a28b4-201">A report is generated with the events and dates selected.</span></span> <span data-ttu-id="a28b4-202">Les paramètres du rapport sont définis dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a28b4-202">The report parameters are defined in the following table.</span></span>

**<span data-ttu-id="a28b4-203">Propriétés du rapport du journal des erreurs</span><span class="sxs-lookup"><span data-stu-id="a28b4-203">Error Log Report Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a28b4-204">Propriété</span><span class="sxs-lookup"><span data-stu-id="a28b4-204">Property</span></span></th>
<th align="left"><span data-ttu-id="a28b4-205">Description</span><span class="sxs-lookup"><span data-stu-id="a28b4-205">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a28b4-206">ID d’événement</span><span class="sxs-lookup"><span data-stu-id="a28b4-206">Event ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-207">ID de l’événement.</span><span class="sxs-lookup"><span data-stu-id="a28b4-207">The event ID.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a28b4-208">Catégorie</span><span class="sxs-lookup"><span data-stu-id="a28b4-208">Category</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-209">Module référencé par le rapport.</span><span class="sxs-lookup"><span data-stu-id="a28b4-209">The module that the report is referring to.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a28b4-210">Description</span><span class="sxs-lookup"><span data-stu-id="a28b4-210">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-211">Description de l’événement.</span><span class="sxs-lookup"><span data-stu-id="a28b4-211">A description of the event.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a28b4-212">Temps reçu</span><span class="sxs-lookup"><span data-stu-id="a28b4-212">Time Received</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-213">Date et heure de réception de l’événement sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="a28b4-213">The date and time the event was received on the server.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="a28b4-214">Remarque</span><span class="sxs-lookup"><span data-stu-id="a28b4-214">Note</span></span></strong><br/><p><span data-ttu-id="a28b4-215">Si le client est en mode hors connexion, le serveur reçoit les rapports lorsque le client est connecté.</span><span class="sxs-lookup"><span data-stu-id="a28b4-215">If the client is working offline, the server receives the reports when the client is online.</span></span></p>
</div>
<div>

</div>
<div class="alert">
<strong><span data-ttu-id="a28b4-216">Remarque</span><span class="sxs-lookup"><span data-stu-id="a28b4-216">Note</span></span></strong><br/><p><span data-ttu-id="a28b4-217">Par défaut, les événements s’affichent dans l’ordre décroissant de dates.</span><span class="sxs-lookup"><span data-stu-id="a28b4-217">By default, the events are displayed in descending date order.</span></span> <span data-ttu-id="a28b4-218">Néanmoins, il peut être modifié en cliquant sur la <strong> colonne heure de réception </strong> .</span><span class="sxs-lookup"><span data-stu-id="a28b4-218">However, it can be changed by clicking the <strong>Time Received</strong> column.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a28b4-219">Temps client</span><span class="sxs-lookup"><span data-stu-id="a28b4-219">Client Time</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-220">Date et heure auxquelles l’événement s’est produit en fonction de l’horloge du client.</span><span class="sxs-lookup"><span data-stu-id="a28b4-220">The date and time the event occurred according to the client clock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a28b4-221">Nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="a28b4-221">Host Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-222">Nom de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="a28b4-222">The name of the host computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a28b4-223">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="a28b4-223">User Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-224">Utilisateur qui a déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="a28b4-224">The user who initiated the event.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a28b4-225">Nom de l’espace de travail</span><span class="sxs-lookup"><span data-stu-id="a28b4-225">Workspace Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="a28b4-226">Nom de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="a28b4-226">The name of the MED-V workspace.</span></span></p></td>
</tr>
</tbody>
</table>











