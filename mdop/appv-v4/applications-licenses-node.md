---
title: Nœud Licences d'applications
description: Nœud Licences d'applications
author: dansimp
ms.assetid: 2b8752ff-aa56-483e-b844-966941af2d94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 720de1860e72ae2c71298f93e9b346afd66da569
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807937"
---
# <span data-ttu-id="c74cd-103">Nœud Licences d'applications</span><span class="sxs-lookup"><span data-stu-id="c74cd-103">Applications Licenses Node</span></span>


<span data-ttu-id="c74cd-104">Le nœud **applications licenses** est le niveau inférieur au nœud système de virtualisation des applications dans le volet de l' **étendue** de la console de gestion du serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="c74cd-104">The **Applications Licenses** node is one level below the Application Virtualization System node in the **Scope** pane in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="c74cd-105">Lorsque vous sélectionnez ce nœud, le volet **résultats** affiche une liste de licences et de groupes de licences.</span><span class="sxs-lookup"><span data-stu-id="c74cd-105">When you select this node, the **Results** pane displays a list of licenses and license groups.</span></span> <span data-ttu-id="c74cd-106">Les types de licence suivants sont disponibles:</span><span class="sxs-lookup"><span data-stu-id="c74cd-106">The following license types are available:</span></span>

-   <span data-ttu-id="c74cd-107">**Licence illimitée**: permet d’accéder à un nombre d’utilisateurs simultanés.</span><span class="sxs-lookup"><span data-stu-id="c74cd-107">**Unlimited License**—Provides access for any number of simultaneous users.</span></span> <span data-ttu-id="c74cd-108">Cette méthode de gestion des licences est appropriée lorsque vous voulez associer une licence à l’échelle de l’entreprise à une application.</span><span class="sxs-lookup"><span data-stu-id="c74cd-108">This method of licensing is appropriate when you want to associate an enterprise-wide license with an application.</span></span>

-   <span data-ttu-id="c74cd-109">**Licence simultanée**: permet de définir le nombre maximal d’utilisateurs simultanés autorisés à utiliser l’application.</span><span class="sxs-lookup"><span data-stu-id="c74cd-109">**Concurrent License**—Enables you to define the maximum number of concurrent users who are allowed to use the application.</span></span>

-   <span data-ttu-id="c74cd-110">**Licence nommée**: vous permet d’attribuer une licence à un utilisateur individuel.</span><span class="sxs-lookup"><span data-stu-id="c74cd-110">**Named License**—Enables you to assign a license to an individual user.</span></span> <span data-ttu-id="c74cd-111">Une licence nommée peut être utilisée pour s’assurer qu’un utilisateur particulier sera toujours en mesure d’exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="c74cd-111">A named license can be used to ensure that a particular user will always be able to run the application.</span></span>

<span data-ttu-id="c74cd-112">**Remarques**  Vous pouvez combiner des licences concomitantes et nommées pour la même application.</span><span class="sxs-lookup"><span data-stu-id="c74cd-112">**Note** You can combine concurrent and named licenses for the same application.</span></span>

 

<span data-ttu-id="c74cd-113">Cliquez avec le bouton droit sur le nœud **applications** pour afficher un menu contextuel contenant les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="c74cd-113">Right-click the **Applications Licenses** node to display a pop-up menu that contains the following elements.</span></span>

<a href="" id="new-unlimited-license"></a>**<span data-ttu-id="c74cd-114">Nouvelle licence illimitée</span><span class="sxs-lookup"><span data-stu-id="c74cd-114">New Unlimited License</span></span>**  
<span data-ttu-id="c74cd-115">Affiche la nouvelle licence illimité de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="c74cd-115">Displays the New Unlimited License Wizard.</span></span> <span data-ttu-id="c74cd-116">Cet Assistant comprend les pages suivantes:</span><span class="sxs-lookup"><span data-stu-id="c74cd-116">This wizard consists of the following pages:</span></span>

1.  <span data-ttu-id="c74cd-117">Entrez le nom du groupe de licences dans le champ **nom du groupe de licences applications** , puis entrez une valeur (en minutes) dans le champ **Avertissement d’expiration** de la licence.</span><span class="sxs-lookup"><span data-stu-id="c74cd-117">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="c74cd-118">(Vous pouvez entrer n’importe quelle valeur comprise entre 0 et 100.) Vous pouvez également utiliser les flèches vers le haut et le bas pour sélectionner le nombre de minutes.</span><span class="sxs-lookup"><span data-stu-id="c74cd-118">(You can enter any value from 0 through 100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="c74cd-119">Entrez un texte descriptif bref dans le champ de **Description de licence** , puis activez la case à cocher **activé** pour activer la licence.</span><span class="sxs-lookup"><span data-stu-id="c74cd-119">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="c74cd-120">Vous pouvez également utiliser le champ **Date d’expiration** pour spécifier une date d’expiration pour la licence.</span><span class="sxs-lookup"><span data-stu-id="c74cd-120">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="c74cd-121">Vous pouvez activer la case à cocher pour utiliser la date d’expiration affichée ou vous pouvez utiliser l’utilitaire calendrier pour accéder à la date d’expiration souhaitée.</span><span class="sxs-lookup"><span data-stu-id="c74cd-121">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="c74cd-122">Cliquez sur **Terminer** pour ajouter la nouvelle licence.</span><span class="sxs-lookup"><span data-stu-id="c74cd-122">Click **Finish** to add the new license.</span></span>

<a href="" id="new-concurrent-license"></a>**<span data-ttu-id="c74cd-123">Nouvelle licence simultanée</span><span class="sxs-lookup"><span data-stu-id="c74cd-123">New Concurrent License</span></span>**  
<span data-ttu-id="c74cd-124">Affiche le nouvel Assistant licence concomitante.</span><span class="sxs-lookup"><span data-stu-id="c74cd-124">Displays the New Concurrent License Wizard.</span></span> <span data-ttu-id="c74cd-125">Cet Assistant comporte les trois pages suivantes et est presque identique au nouvel Assistant licence illimité:</span><span class="sxs-lookup"><span data-stu-id="c74cd-125">This wizard consists of the following three pages and is almost identical to the New Unlimited License Wizard:</span></span>

1.  <span data-ttu-id="c74cd-126">Entrez le nom du groupe de licences dans le champ **nom du groupe de licences applications** , puis entrez une valeur (en minutes) dans le champ **Avertissement d’expiration** de la licence.</span><span class="sxs-lookup"><span data-stu-id="c74cd-126">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="c74cd-127">(Vous pouvez entrer n’importe quelle valeur comprise entre 0 et 100.) Vous pouvez également utiliser les flèches vers le haut et le bas pour sélectionner le nombre de minutes.</span><span class="sxs-lookup"><span data-stu-id="c74cd-127">(You can enter any value from 0 through 100.) You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="c74cd-128">Entrez un texte descriptif bref dans le champ Description de la **licence** , puis entrez une valeur dans le champ **nombre de licences simultanées** .</span><span class="sxs-lookup"><span data-stu-id="c74cd-128">Enter brief descriptive text in the **License Description** field, and enter a value in the **Concurrent License Quantity** field.</span></span>

    <span data-ttu-id="c74cd-129">Vous pouvez également utiliser les flèches haut et bas pour spécifier le nombre de licences simultanées.</span><span class="sxs-lookup"><span data-stu-id="c74cd-129">You can also use the up and down arrows to specify the number of concurrent licenses.</span></span> <span data-ttu-id="c74cd-130">Cochez la case **activé** pour activer la licence.</span><span class="sxs-lookup"><span data-stu-id="c74cd-130">Select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="c74cd-131">Vous pouvez également utiliser le champ **Date d’expiration** pour spécifier une date d’expiration pour la licence.</span><span class="sxs-lookup"><span data-stu-id="c74cd-131">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="c74cd-132">Vous pouvez activer la case à cocher pour utiliser la date d’expiration affichée ou vous pouvez utiliser l’utilitaire calendrier pour accéder à la date d’expiration souhaitée.</span><span class="sxs-lookup"><span data-stu-id="c74cd-132">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="c74cd-133">Cliquez sur **Terminer** pour ajouter les nouvelles licences.</span><span class="sxs-lookup"><span data-stu-id="c74cd-133">Click **Finish** to add the new licenses.</span></span>

<a href="" id="new-named-license"></a>**<span data-ttu-id="c74cd-134">Nouvelle licence nommée</span><span class="sxs-lookup"><span data-stu-id="c74cd-134">New Named License</span></span>**  
<span data-ttu-id="c74cd-135">Affiche la nouvelle Assistant licence nommée.</span><span class="sxs-lookup"><span data-stu-id="c74cd-135">Displays the New Named License Wizard.</span></span> <span data-ttu-id="c74cd-136">Cet Assistant comporte les quatre pages suivantes:</span><span class="sxs-lookup"><span data-stu-id="c74cd-136">This wizard consists of the following four pages:</span></span>

1.  <span data-ttu-id="c74cd-137">Entrez le nom du groupe de licences dans le champ **nom du groupe de licences applications** , puis entrez une valeur (en minutes) dans le champ **Avertissement d’expiration** de la licence.</span><span class="sxs-lookup"><span data-stu-id="c74cd-137">Enter the name of the license group in the **Applications License Group Name** field, and enter a value (in minutes) in the **License Expiration Warning** field.</span></span> <span data-ttu-id="c74cd-138">(Vous pouvez entrer n’importe quelle valeur comprise entre 0 et 100).</span><span class="sxs-lookup"><span data-stu-id="c74cd-138">(You can enter any value from 0 through 100).</span></span> <span data-ttu-id="c74cd-139">Vous pouvez également utiliser les flèches vers le haut et le bas pour sélectionner le nombre de minutes.</span><span class="sxs-lookup"><span data-stu-id="c74cd-139">You can also use the up and down arrows to select the number of minutes.</span></span>

2.  <span data-ttu-id="c74cd-140">Entrez un texte descriptif bref dans le champ de **Description de licence** , puis activez la case à cocher **activé** pour activer la licence.</span><span class="sxs-lookup"><span data-stu-id="c74cd-140">Enter brief descriptive text in the **License Description** field, and select the **Enabled** check box to enable the license.</span></span>

    <span data-ttu-id="c74cd-141">Vous pouvez également utiliser le champ **Date d’expiration** pour spécifier une date d’expiration pour la licence.</span><span class="sxs-lookup"><span data-stu-id="c74cd-141">Optionally, you can use the **Expiration Date** field to specify an expiration date for the license.</span></span> <span data-ttu-id="c74cd-142">Vous pouvez activer la case à cocher pour utiliser la date d’expiration affichée ou vous pouvez utiliser l’utilitaire calendrier pour accéder à la date d’expiration souhaitée.</span><span class="sxs-lookup"><span data-stu-id="c74cd-142">You can select the check box to use the displayed expiration date, or you can use the calendar utility to browse to the desired expiration date.</span></span>

3.  <span data-ttu-id="c74cd-143">Cliquez sur **Ajouter**, **modifier**ou **supprimer** des utilisateurs nommés.</span><span class="sxs-lookup"><span data-stu-id="c74cd-143">Click **Add**, **Edit**, or **Remove** named users.</span></span>

4.  <span data-ttu-id="c74cd-144">Cliquez sur **Terminer** pour ajouter la nouvelle licence.</span><span class="sxs-lookup"><span data-stu-id="c74cd-144">Click **Finish** to add the new license.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="c74cd-145">View (Afficher)</span><span class="sxs-lookup"><span data-stu-id="c74cd-145">View</span></span>**  
<span data-ttu-id="c74cd-146">Change l’aspect et le contenu du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="c74cd-146">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="c74cd-147">Nouvelle fenêtre à partir de cet emplacement</span><span class="sxs-lookup"><span data-stu-id="c74cd-147">New Window from Here</span></span>**  
<span data-ttu-id="c74cd-148">Ouvre une nouvelle console de gestion avec le nœud sélectionné en tant que nœud racine.</span><span class="sxs-lookup"><span data-stu-id="c74cd-148">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="refresh"></a>**<span data-ttu-id="c74cd-149">Actualiser</span><span class="sxs-lookup"><span data-stu-id="c74cd-149">Refresh</span></span>**  
<span data-ttu-id="c74cd-150">Actualise l’affichage du serveur.</span><span class="sxs-lookup"><span data-stu-id="c74cd-150">Refreshes the view of the server.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="c74cd-151">Exporter la liste</span><span class="sxs-lookup"><span data-stu-id="c74cd-151">Export List</span></span>**  
<span data-ttu-id="c74cd-152">Crée un fichier texte délimité par des tabulations, qui contient le contenu du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="c74cd-152">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="c74cd-153">Cet élément affiche une boîte de dialogue **enregistrement de fichier** standard dans laquelle vous spécifiez l’emplacement du fichier texte que vous créez.</span><span class="sxs-lookup"><span data-stu-id="c74cd-153">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="c74cd-154">Help</span><span class="sxs-lookup"><span data-stu-id="c74cd-154">Help</span></span>**  
<span data-ttu-id="c74cd-155">Affiche le système d’aide pour la console de gestion du serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="c74cd-155">Displays the help system for the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="c74cd-156">Si vous cliquez sur un groupe de licences ou une licence qui s’affiche sous le nœud **licences d’application** dans le volet de l' **étendue** , les éléments suivants sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="c74cd-156">If you click a license group or license that appears under the **Application Licenses** node in the **Scope** pane, the following elements are available.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="c74cd-157">View (Afficher)</span><span class="sxs-lookup"><span data-stu-id="c74cd-157">View</span></span>**  
<span data-ttu-id="c74cd-158">Change l’aspect et le contenu du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="c74cd-158">Changes the appearance and content of the **Results** pane.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="c74cd-159">Nouvelle fenêtre à partir de cet emplacement</span><span class="sxs-lookup"><span data-stu-id="c74cd-159">New Window from Here</span></span>**  
<span data-ttu-id="c74cd-160">Ouvre une nouvelle console de gestion avec le nœud sélectionné en tant que nœud racine.</span><span class="sxs-lookup"><span data-stu-id="c74cd-160">Opens a new management console with the selected node as the root node.</span></span>

<a href="" id="delete"></a>**<span data-ttu-id="c74cd-161">Delete</span><span class="sxs-lookup"><span data-stu-id="c74cd-161">Delete</span></span>**  
<span data-ttu-id="c74cd-162">Supprime un package du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="c74cd-162">Deletes a package from the **Results** pane.</span></span>

<a href="" id="rename"></a>**<span data-ttu-id="c74cd-163">Rename</span><span class="sxs-lookup"><span data-stu-id="c74cd-163">Rename</span></span>**  
<span data-ttu-id="c74cd-164">Modifie le nom d’un package dans le volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="c74cd-164">Changes the name of a package in the **Results** pane.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="c74cd-165">Exporter la liste</span><span class="sxs-lookup"><span data-stu-id="c74cd-165">Export List</span></span>**  
<span data-ttu-id="c74cd-166">Crée un fichier texte délimité par des tabulations, qui contient le contenu du volet **résultats** .</span><span class="sxs-lookup"><span data-stu-id="c74cd-166">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="c74cd-167">Cet élément affiche une boîte de dialogue **enregistrement de fichier** standard dans laquelle vous spécifiez l’emplacement du fichier texte que vous créez.</span><span class="sxs-lookup"><span data-stu-id="c74cd-167">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="properties"></a>**<span data-ttu-id="c74cd-168">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c74cd-168">Properties</span></span>**  
<span data-ttu-id="c74cd-169">Affiche la boîte de dialogue **Propriétés** du groupe de licences sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c74cd-169">Displays the **Properties** dialog box for the selected license group.</span></span> <span data-ttu-id="c74cd-170">L’onglet **général** de la boîte de dialogue **Propriétés** affiche des informations sur le groupe de licences et vous permet de changer la valeur d’heure dans le champ **Avertissement d’expiration** de la licence.</span><span class="sxs-lookup"><span data-stu-id="c74cd-170">The **General** tab of the **Properties** dialog box displays information about the license group and lets you change the time value in the **License Expiration Warning** field.</span></span> <span data-ttu-id="c74cd-171">L’onglet **applications** affiche la liste des applications associées au groupe de licences.</span><span class="sxs-lookup"><span data-stu-id="c74cd-171">The **Applications** tab displays the list of applications associated with the license group.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="c74cd-172">Help</span><span class="sxs-lookup"><span data-stu-id="c74cd-172">Help</span></span>**  
<span data-ttu-id="c74cd-173">Affiche le système d’aide pour la console de gestion du serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="c74cd-173">Displays the help system for the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="c74cd-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c74cd-174">Related topics</span></span>


[<span data-ttu-id="c74cd-175">À propos de l'octroi de licence pour les applications</span><span class="sxs-lookup"><span data-stu-id="c74cd-175">About Application Licensing</span></span>](about-application-licensing.md)

[<span data-ttu-id="c74cd-176">Procédure pour gérer des licences d'applications dans Server Management Console</span><span class="sxs-lookup"><span data-stu-id="c74cd-176">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="c74cd-177">Server Management Console: nœud Licences d'applications</span><span class="sxs-lookup"><span data-stu-id="c74cd-177">Server Management Console: Application Licenses Node</span></span>](server-management-console-application-licenses-node.md)

 

 





