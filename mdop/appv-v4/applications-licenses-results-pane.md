---
title: Volet de résultats Licences d'applications
description: Volet de résultats Licences d'applications
author: dansimp
ms.assetid: 8b519715-b2fe-451e-ad9b-e9b73f454961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e5a86c22e67e061ec873317c455958536fae75b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807934"
---
# <span data-ttu-id="786f1-103">Volet de résultats Licences d'applications</span><span class="sxs-lookup"><span data-stu-id="786f1-103">Applications Licenses Results Pane</span></span>


<span data-ttu-id="786f1-104">Le volet de **résultats de licences applications** de la console de gestion du serveur d’applications, affiche une liste des groupes de licences d’application disponibles et des licences d’application.</span><span class="sxs-lookup"><span data-stu-id="786f1-104">The **Applications Licenses Results** pane in the Application Virtualization Server Management Console displays a list of the available application license groups and application licenses.</span></span>

<span data-ttu-id="786f1-105">Cliquez avec le bouton droit sur un groupe de licences d’application pour afficher un menu contextuel contenant les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="786f1-105">Right-click any application license group to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-unlimited-license"></a>**<span data-ttu-id="786f1-106">Nouvelle licence illimitée</span><span class="sxs-lookup"><span data-stu-id="786f1-106">New Unlimited License</span></span>**  
<span data-ttu-id="786f1-107">Affiche la nouvelle licence illimité de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="786f1-107">Displays the New Unlimited License Wizard.</span></span> <span data-ttu-id="786f1-108">Cette option n’est disponible que si le groupe de licences n’a pas de licence.</span><span class="sxs-lookup"><span data-stu-id="786f1-108">This option is available only when the license group has no licenses.</span></span> <span data-ttu-id="786f1-109">Cet Assistant comporte trois pages:</span><span class="sxs-lookup"><span data-stu-id="786f1-109">This wizard consists of three pages:</span></span>

1.  <span data-ttu-id="786f1-110">Entrez un nom de groupe dans le champ **nom du groupe de licences applications** et une valeur (en minutes) dans le champ **Avertissement d’expiration** de la licence.</span><span class="sxs-lookup"><span data-stu-id="786f1-110">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="786f1-111">(Vous pouvez entrer n’importe quelle valeur comprise entre 0 et 100.) Vous pouvez également utiliser les flèches vers le haut et le bas pour sélectionner le nombre de minutes.</span><span class="sxs-lookup"><span data-stu-id="786f1-111">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="786f1-112">Entrez un texte descriptif bref dans le champ de **Description de licence** , puis activez la case à cocher **activé** .</span><span class="sxs-lookup"><span data-stu-id="786f1-112">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box.</span></span> <span data-ttu-id="786f1-113">Vous pouvez également utiliser le champ **Date d’expiration** pour spécifier une date d’expiration pour la licence.</span><span class="sxs-lookup"><span data-stu-id="786f1-113">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="786f1-114">Vous pouvez activer la case à cocher par défaut ou utiliser l’utilitaire calendrier pour accéder à la date d’expiration souhaitée.</span><span class="sxs-lookup"><span data-stu-id="786f1-114">You can select the default check box or use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="786f1-115">Cliquez sur **Terminer** pour ajouter la nouvelle licence.</span><span class="sxs-lookup"><span data-stu-id="786f1-115">Click **Finish** to add the new license.</span></span>

<a href="" id="new-concurrent-license"></a>**<span data-ttu-id="786f1-116">Nouvelle licence simultanée</span><span class="sxs-lookup"><span data-stu-id="786f1-116">New Concurrent License</span></span>**  
<span data-ttu-id="786f1-117">Affiche le nouvel Assistant licence concomitante.</span><span class="sxs-lookup"><span data-stu-id="786f1-117">Displays the New Concurrent License Wizard.</span></span> <span data-ttu-id="786f1-118">Cette option n’est disponible que si le groupe de licences ne dispose pas de licences illimitées.</span><span class="sxs-lookup"><span data-stu-id="786f1-118">This option is available only when the license group has no unlimited licenses.</span></span> <span data-ttu-id="786f1-119">Cet Assistant comprend les pages suivantes et est presque identique au nouvel Assistant licence illimité:</span><span class="sxs-lookup"><span data-stu-id="786f1-119">This wizard consists of the following pages and is almost identical to the New Unlimited License Wizard:</span></span>

1.  <span data-ttu-id="786f1-120">Entrez un nom de groupe dans le champ **nom du groupe de licences applications** et une valeur (en minutes) dans le champ **Avertissement d’expiration** de la licence.</span><span class="sxs-lookup"><span data-stu-id="786f1-120">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="786f1-121">(Vous pouvez entrer n’importe quelle valeur comprise entre 0 et 100.) Vous pouvez également utiliser les flèches vers le haut et le bas pour sélectionner le nombre de minutes.</span><span class="sxs-lookup"><span data-stu-id="786f1-121">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="786f1-122">Entrez un texte descriptif bref dans le champ Description de la **licence** , puis entrez une valeur dans le champ **nombre de licences simultanées** .</span><span class="sxs-lookup"><span data-stu-id="786f1-122">Enter brief descriptive text in the **License Description** field, and enter a value in the **Concurrent License Quantity** field.</span></span> <span data-ttu-id="786f1-123">Vous pouvez également utiliser les flèches haut et bas pour spécifier le nombre de licences simultanées.</span><span class="sxs-lookup"><span data-stu-id="786f1-123">You can also use the up and down arrows to specify the number of concurrent licenses.</span></span> <span data-ttu-id="786f1-124">Cochez la case **activé** pour activer la licence.</span><span class="sxs-lookup"><span data-stu-id="786f1-124">Select the **Enabled** check box to enable the license.</span></span> <span data-ttu-id="786f1-125">Vous pouvez également utiliser le champ **Date d’expiration** pour sélectionner une date d’expiration pour la licence.</span><span class="sxs-lookup"><span data-stu-id="786f1-125">Optionally, you can use the **Expiration Date** field to select an expiration date for the license.</span></span> <span data-ttu-id="786f1-126">Vous pouvez activer la case à cocher pour utiliser la date d’expiration affichée ou vous pouvez utiliser l’utilitaire calendrier pour accéder à la date d’expiration souhaitée.</span><span class="sxs-lookup"><span data-stu-id="786f1-126">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="786f1-127">Cliquez sur **Terminer** pour ajouter les nouvelles licences.</span><span class="sxs-lookup"><span data-stu-id="786f1-127">Click **Finish** to add the new licenses.</span></span>

<a href="" id="new-named-license"></a>**<span data-ttu-id="786f1-128">Nouvelle licence nommée</span><span class="sxs-lookup"><span data-stu-id="786f1-128">New Named License</span></span>**  
<span data-ttu-id="786f1-129">Affiche la nouvelle Assistant licence nommée.</span><span class="sxs-lookup"><span data-stu-id="786f1-129">Displays the New Named License Wizard.</span></span> <span data-ttu-id="786f1-130">Cette option n’est disponible que si le groupe de licences ne dispose pas de licences illimitées.</span><span class="sxs-lookup"><span data-stu-id="786f1-130">This option is available only when the license group has no unlimited licenses.</span></span> <span data-ttu-id="786f1-131">Cet Assistant comprend les pages suivantes:</span><span class="sxs-lookup"><span data-stu-id="786f1-131">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="786f1-132">Entrez un nom de groupe dans le champ **nom du groupe de licences applications** et une valeur (en minutes) dans le champ **Avertissement d’expiration** de la licence.</span><span class="sxs-lookup"><span data-stu-id="786f1-132">Enter a group name in the **Applications License Group Name** field and a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="786f1-133">(Vous pouvez entrer n’importe quelle valeur comprise entre 0 et 100.) Vous pouvez également utiliser les flèches vers le haut et le bas pour sélectionner le nombre de minutes.</span><span class="sxs-lookup"><span data-stu-id="786f1-133">(You can enter any value from 0–100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="786f1-134">Entrez un texte descriptif bref dans la description de la **licence**, puis activez la case à cocher **activé** .</span><span class="sxs-lookup"><span data-stu-id="786f1-134">Enter brief descriptive text in the **License Description**, and select the **Enabled** check box.</span></span> <span data-ttu-id="786f1-135">Vous pouvez également utiliser le champ **Date d’expiration** pour spécifier une date d’expiration pour la licence.</span><span class="sxs-lookup"><span data-stu-id="786f1-135">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="786f1-136">Vous pouvez activer la case à cocher pour utiliser la date d’expiration affichée ou utiliser l’utilitaire calendrier pour accéder à la date d’expiration souhaitée.</span><span class="sxs-lookup"><span data-stu-id="786f1-136">You can select the check box to use the displayed expiration date, or use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="786f1-137">Cliquez sur **Ajouter**, **modifier**ou **supprimer** des utilisateurs nommés.</span><span class="sxs-lookup"><span data-stu-id="786f1-137">Click **Add**, **Edit**, or **Remove** named users.</span></span>

4.  <span data-ttu-id="786f1-138">Cliquez sur **Terminer** pour ajouter la nouvelle licence.</span><span class="sxs-lookup"><span data-stu-id="786f1-138">Click **Finish** to add the new license.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="786f1-139">Nouvelle fenêtre à partir de cet emplacement</span><span class="sxs-lookup"><span data-stu-id="786f1-139">New Window from Here</span></span>**  
<span data-ttu-id="786f1-140">Ouvre une nouvelle console de gestion avec le nœud sélectionné en tant que nœud racine.</span><span class="sxs-lookup"><span data-stu-id="786f1-140">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="786f1-141">Delete</span><span class="sxs-lookup"><span data-stu-id="786f1-141">Delete</span></span>**  
<span data-ttu-id="786f1-142">Supprime le groupe de licences de la liste.</span><span class="sxs-lookup"><span data-stu-id="786f1-142">Deletes the license group from the list.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="786f1-143">Rename</span><span class="sxs-lookup"><span data-stu-id="786f1-143">Rename</span></span>**  
<span data-ttu-id="786f1-144">Change le nom du groupe de licences d’applications.</span><span class="sxs-lookup"><span data-stu-id="786f1-144">Changes the name of the applications license group.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="786f1-145">Propriétés</span><span class="sxs-lookup"><span data-stu-id="786f1-145">Properties</span></span>**  
<span data-ttu-id="786f1-146">Affiche la boîte de dialogue **Propriétés** pour les groupes de licences d’application sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="786f1-146">Displays the **Properties** dialog box for the selected application license groups.</span></span> <span data-ttu-id="786f1-147">Cette boîte de dialogue comporte les onglets suivants:</span><span class="sxs-lookup"><span data-stu-id="786f1-147">This dialog box has the following tabs:</span></span>

-   <span data-ttu-id="786f1-148">Onglet **général** : affiche des informations générales sur le groupe de licences.</span><span class="sxs-lookup"><span data-stu-id="786f1-148">**General** tab—Displays general information about the license group.</span></span> <span data-ttu-id="786f1-149">Dans cet onglet, vous pouvez modifier la valeur d’heure (en minutes) dans le champ **Avertissement d’expiration** de la licence.</span><span class="sxs-lookup"><span data-stu-id="786f1-149">From this tab, you can change the time value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="786f1-150">Vous pouvez entrer une valeur comprise entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="786f1-150">You can enter any value from 0–100.</span></span>

-   <span data-ttu-id="786f1-151">Onglet **applications** : affiche la liste des applications associées au groupe de licences.</span><span class="sxs-lookup"><span data-stu-id="786f1-151">**Applications** tab—Displays the list of applications associated with the license group.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="786f1-152">Help</span><span class="sxs-lookup"><span data-stu-id="786f1-152">Help</span></span>**  
<span data-ttu-id="786f1-153">Affiche le système d’aide de la console de gestion du serveur applicatif.</span><span class="sxs-lookup"><span data-stu-id="786f1-153">Displays the Application Virtualization Server Management Console help system.</span></span>

<span data-ttu-id="786f1-154">Lorsque le volet **résultats** affiche des groupes de licences d’application, cliquez avec le bouton droit n’importe où dans le volet **résultats** , à l’exception du groupe de licences, pour afficher un menu contextuel contenant les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="786f1-154">When the **Results** pane displays application license groups, right-click anywhere in the **Results** pane, except on a license group, to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="786f1-155">Actualiser</span><span class="sxs-lookup"><span data-stu-id="786f1-155">Refresh</span></span>**  
<span data-ttu-id="786f1-156">Actualise l’affichage du serveur.</span><span class="sxs-lookup"><span data-stu-id="786f1-156">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="786f1-157">Exporter la liste</span><span class="sxs-lookup"><span data-stu-id="786f1-157">Export List</span></span>**  
<span data-ttu-id="786f1-158">Crée un fichier texte délimité par des tabulations, qui contient le contenu du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="786f1-158">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="786f1-159">Cet élément affiche une boîte de dialogue **enregistrement de fichier** standard dans laquelle vous spécifiez l’emplacement du fichier texte que vous créez.</span><span class="sxs-lookup"><span data-stu-id="786f1-159">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="786f1-160">View (Afficher)</span><span class="sxs-lookup"><span data-stu-id="786f1-160">View</span></span>**  
<span data-ttu-id="786f1-161">Change l’aspect et le contenu du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="786f1-161">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="arrange-line-up-icons"></a>**<span data-ttu-id="786f1-162">Icônes réorganiser/aligner sur les lignes</span><span class="sxs-lookup"><span data-stu-id="786f1-162">Arrange/Line Up Icons</span></span>**  
<span data-ttu-id="786f1-163">Change le mode d’affichage des icônes dans le volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="786f1-163">Changes how the icons are displayed in the **Results** pane.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="786f1-164">Help</span><span class="sxs-lookup"><span data-stu-id="786f1-164">Help</span></span>**  
<span data-ttu-id="786f1-165">Affiche le système d’aide pour la console de gestion du serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="786f1-165">Displays the help system for the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="786f1-166">Lorsque le volet **résultats** affiche des licences, cliquez avec le bouton droit sur une licence d’application pour afficher un menu contextuel contenant les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="786f1-166">When the **Results** pane displays licenses, right-click any application license to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="786f1-167">Delete</span><span class="sxs-lookup"><span data-stu-id="786f1-167">Delete</span></span>**  
<span data-ttu-id="786f1-168">Supprime la licence de la liste.</span><span class="sxs-lookup"><span data-stu-id="786f1-168">Deletes the license from the list.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="786f1-169">Rename</span><span class="sxs-lookup"><span data-stu-id="786f1-169">Rename</span></span>**  
<span data-ttu-id="786f1-170">Change le nom de la licence.</span><span class="sxs-lookup"><span data-stu-id="786f1-170">Changes the name of the license.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="786f1-171">Propriétés</span><span class="sxs-lookup"><span data-stu-id="786f1-171">Properties</span></span>**  
<span data-ttu-id="786f1-172">Affiche la boîte de dialogue **Propriétés** pour la licence d’application sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="786f1-172">Displays the **Properties** dialog box for the selected application license.</span></span>

<span data-ttu-id="786f1-173">L’onglet **général** de la boîte de dialogue **Propriétés** affiche des informations sur la licence et vous permet de modifier les informations de statut activé, de date d’expiration de la licence et de clé de licence.</span><span class="sxs-lookup"><span data-stu-id="786f1-173">The **General** tab of the **Properties** dialog box displays information about the license and lets you change the enabled status, license expiration date, and license key information.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="786f1-174">Help</span><span class="sxs-lookup"><span data-stu-id="786f1-174">Help</span></span>**  
<span data-ttu-id="786f1-175">Affiche le système d’aide de la console de gestion du serveur.</span><span class="sxs-lookup"><span data-stu-id="786f1-175">Displays the server management console help system.</span></span>

<span data-ttu-id="786f1-176">Lorsque le volet **résultats** affiche une licence, cliquez avec le bouton droit n’importe où dans le volet **résultats** , sauf sur une licence, pour afficher un menu contextuel contenant les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="786f1-176">When the **Results** pane displays licenses, right-click anywhere in the **Results** pane, except on a license, to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="786f1-177">Exporter la liste</span><span class="sxs-lookup"><span data-stu-id="786f1-177">Export List</span></span>**  
<span data-ttu-id="786f1-178">Crée un fichier texte délimité par des tabulations, qui contient le contenu du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="786f1-178">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="786f1-179">Cet élément affiche une boîte de dialogue **enregistrement de fichier** standard dans laquelle vous spécifiez l’emplacement du fichier texte que vous créez.</span><span class="sxs-lookup"><span data-stu-id="786f1-179">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="786f1-180">View (Afficher)</span><span class="sxs-lookup"><span data-stu-id="786f1-180">View</span></span>**  
<span data-ttu-id="786f1-181">Change l’aspect et le contenu du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="786f1-181">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="arrange-line-up-icons"></a>**<span data-ttu-id="786f1-182">Icônes réorganiser/aligner sur les lignes</span><span class="sxs-lookup"><span data-stu-id="786f1-182">Arrange/Line Up Icons</span></span>**  
<span data-ttu-id="786f1-183">Change le mode d’affichage des icônes dans le volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="786f1-183">Changes how the icons are displayed in the **Results** pane.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="786f1-184">Propriétés</span><span class="sxs-lookup"><span data-stu-id="786f1-184">Properties</span></span>**  
<span data-ttu-id="786f1-185">Affiche la boîte de dialogue **Propriétés** pour la licence sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="786f1-185">Displays the **Properties** dialog box for the selected license.</span></span>

<span data-ttu-id="786f1-186">L’onglet **général** de la boîte de dialogue **Propriétés** affiche des informations sur la licence et vous permet de modifier les informations de statut activé, de date d’expiration de la licence et de clé de licence.</span><span class="sxs-lookup"><span data-stu-id="786f1-186">The **General** tab of the **Properties** dialog box displays information about the license and lets you change the enabled status, license expiration date, and license key information.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="786f1-187">Help</span><span class="sxs-lookup"><span data-stu-id="786f1-187">Help</span></span>**  
<span data-ttu-id="786f1-188">Affiche le système d’aide pour la console de gestion du serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="786f1-188">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="786f1-189">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="786f1-189">Related topics</span></span>


[<span data-ttu-id="786f1-190">À propos de l'octroi de licence pour les applications</span><span class="sxs-lookup"><span data-stu-id="786f1-190">About Application Licensing</span></span>](about-application-licensing.md)

[<span data-ttu-id="786f1-191">Procédure pour gérer des licences d'applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="786f1-191">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="786f1-192">Server Management Console: nœud Licences d'applications</span><span class="sxs-lookup"><span data-stu-id="786f1-192">Server Management Console: Application Licenses Node</span></span>](server-management-console-application-licenses-node.md)

 

 





